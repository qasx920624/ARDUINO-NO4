# ARDUINO 第四篇
題目如下(●=亮 ; ○=滅)</p>
STEP0 ○○○○○○○○</p>
STEP1 ●○○○○○○○</p>
STEP2 ○●○○○○○○</p>
STEP3 ○○●○○○○○</p>
STEP4 ○○○●○○○○</p>
STEP5 ○○○○●○○○</p>
STEP6 ○○○○○●○○</p>
STEP7 ○○○○○○●○</p>
STEP8 ○○○○○○○●</p>
STEP9 reset</p>

程式如下</p>
```C++
void setup() {
  for(int i=2;i<10;i++)//設定2~10的腳位
  {
    pinMode(i,OUTPUT);
    digitalWrite(i,HIGH);
  }
}

void loop() {
   for(int i=10;i>=2;i--)//LED10在最左邊,往LED2方向亮滅(向右
   {
  digitalWrite(i,LOW);
  delay(300);
  digitalWrite(i,HIGH); 
   }
  
}
```
加分題題目如下</p>
STEP0 ○○○○○○○○</p>
STEP1 ○○○○○○○●</p>
STEP2 ○○○○○○●○</p>
STEP3 ○○○○○●○○</p>
STEP4 ○○○○●○○○</p>
STEP5 ○○○●○○○○</p>
STEP6 ○○●○○○○○</p>
STEP7 ○●○○○○○○</p>
STEP8 ●○○○○○○○</p>
STEP9 reset</p>
程式如下
```C++
void setup() {
  for(int i=2;i<10;i++)//宣告
  {
    pinMode(i,OUTPUT);
    digitalWrite(i,HIGH);
  }
}

void loop() {
   for(int i=2;i<=10;i++)//LED2在最右邊,往LED10方向亮滅(向左
   {
  digitalWrite(i,LOW);
  delay(300);
  digitalWrite(i,HIGH); 
   }
  
}
```
```c++
void setup() {
for(int i=2;i<4;i++)
pinMode(i,OUTPUT);
pinMode(8,INPUT);
pinMode(9,INPUT);
digitalWrite(8,1);
digitalWrite(9,1);
}
int x =0;
int s =-15;
int m = 255;
int ch = 1;

void loop() {
if(digitalRead(8)==0)
{
while(digitalRead(8)==0)delay(50);
x++;
if(x>3)x=1;

}
mod();
}
void led(int a,int b,int c)
{
analogWrite(2,a);
analogWrite(3,b);
analogWrite(4,c);
}
void mod()
{
switch(x)
{
case 1:
led(150,0,0); delay(300);
led(0,150,0); delay(300);
led(0,0,150); delay(300);
led(150,150,0);delay(300);
led(0,150,150);delay(300);
led(150,0,150);delay(300);
break;
case 2:
if(m>=255||m<=0){s=-s;}
m=m-s;
analogWrite(3,m);
delay(70);
led(0,0,0);
break;
case 3:
if(digitalRead(9)==0)
{
while(digitalRead(9)==0)delay(50);
ch++;
if(ch>6)ch=1;
}
switch(ch)
{
case 1:{ led(150,0,0); break;}
case 2:{led(0,150,0); break;}
case 3:{led(0,0,150); break;}
case 4:{led(150,150,0);break;}
case 5:{led(150,0,150);break;}
case 6:{led(150,150,150); break;}
}
}
}
```
