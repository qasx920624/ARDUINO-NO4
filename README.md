# ARDUINO 第三篇
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
  // put your setup code here, to run once:
  for(int i=2;i<10;i++)
  {
    pinMode(i,OUTPUT);
    digitalWrite(i,HIGH);
  }
}

void loop() {
  // put your main code here, to run repeatedly:
   for(int i=10;i>=2;i--)
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
  // put your setup code here, to run once:
  for(int i=2;i<10;i++)
  {
    pinMode(i,OUTPUT);
    digitalWrite(i,HIGH);
  }
}

void loop() {
  // put your main code here, to run repeatedly:
   for(int i=2;i<=10;i++)
   {
  digitalWrite(i,LOW);
  delay(300);
  digitalWrite(i,HIGH); 
   }
  
}
```
