//---------------------------------------------------------------------------

#include <vcl.h>
#pragma hdrstop

#include "Unit1.h"
//---------------------------------------------------------------------------
#pragma package(smart_init)
#pragma resource "*.dfm"
TForm1 *Form1;
//---------------------------------------------------------------------------
__fastcall TForm1::TForm1(TComponent* Owner)
        : TForm(Owner)
{
}
//---------------------------------------------------------------------------

void __fastcall TForm1::Image3Click(TObject *Sender)
{
        if (OpenDialog1 -> Execute())
        {
                try {
                        Memo1 -> Lines -> LoadFromFile(OpenDialog1 -> FileName);
                        Memo1 -> Visible = true;
                        Button1 -> Visible = true;
                        Button2 -> Visible = true;
                }
                catch (...) {
                        ShowMessage("Plik nie istnieje lub jest uszkodzony.");
                }
        }
}
//---------------------------------------------------------------------------
void __fastcall TForm1::Button1Click(TObject *Sender)
{
        Memo1 -> Visible = false;
        Button1 -> Visible = false;
        Button2 -> Visible = false;
        if (Application->MessageBoxA("Czy chcesz zachowaæ zmiany?", "PotwierdŸ", MB_YESNOCANCEL | MB_ICONQUESTION) == IDYES)
        {
                SaveDialog1 -> FileName = "Sen";
        }
}
//---------------------------------------------------------------------------
void __fastcall TForm1::Image2Click(TObject *Sender)
{
        Memo1 -> Visible = true;
        Button1 -> Visible = true;
        Button2 -> Visible = true;
        Memo1 -> Lines -> Text = Memo1->Lines->Text.Insert("Tytu³: \nData: \nOpis: \n\n\n\n\n\n\n\nOcena snu: ",Memo1->SelStart+1);
}
//---------------------------------------------------------------------------
void __fastcall TForm1::Button2Click(TObject *Sender)
{
        if (SaveDialog1 -> Execute())
        {
                try {
                        Memo1 -> Lines -> SaveToFile(SaveDialog1 -> FileName);
                }
                catch (...) {
                        ShowMessage("Nie uda³o siê zapisac pliku!");
                }
        }
}
//---------------------------------------------------------------------------
