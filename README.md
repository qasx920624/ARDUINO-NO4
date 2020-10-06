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
    pinMode(i,OUTPUT);</p>
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
