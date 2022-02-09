
# pedro
hello world
var
  Form1: TForm1;
  k:integer;  
procedure TForm1.FormCreate(Sender: TObject);
 var k:integer;
begin
  Timer1.Enabled:=false;
  Shape1.Visible:=false;
  Shape2.Visible:=false;
  Shape3.Visible:=false;
end;                     
procedure TForm1.Button1Click(Sender: TObject);
 begin
  Timer1.Interval:=StrToInt(Edit1.text);
  k:=0;
  Timer1.Enabled:=true;
end;

procedure TForm1.Button2Click(Sender: TObject);
  begin
  Timer1.Enabled:=false;
  Shape1.Visible:=false;
  Shape2.Visible:=false;
  Shape3.Visible:=false;
end;

procedure TForm1.Timer1Timer(Sender: TObject);
begin
 k:=k+1;
 //определяем,фигура с каким номером
 //в данный момент должна быть видимой
 if k mod 3=1 then
 begin
   Shape1.Visible:=true;
   Shape2.Visible:=false;
   Shape3.Visible:=false;
 end
  else
 if k mod 3=2 then
 begin
   Shape1.Visible:=false;
   Shape2.Visible:=true;
   Shape3.Visible:=false;
end
