# ARDUINO-NO6
這次的題目是</p>
按一下開關，LED亮</p>
再按一下開關，LED滅</p>
程式如下：</p>
```c++

void setup() {
 pinMode(3, OUTPUT);
  digitalWrite(3, LOW);
  pinMode(2, INPUT);
  digitalWrite(2, HIGH);
}
bool i = true;
void loop() {
 if(digitalRead(2)==0)
  {
    while(digitalRead(2)==0);{delay(10);}//★防彈跳★
     i =!i;//!是加反閘的意思
     digitalWrite(3,i);
     
  }
}
```
