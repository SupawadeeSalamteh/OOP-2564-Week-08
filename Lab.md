# การทดลอง #

## วิธีการทำงานส่ง ##
1. Fork repo นี้ไปที่ git account  ของตนเอง
2. clone ไปที่เครื่องของตนเอง
3. สร้าง folder ส่วนตัว (รหัสนักศึกษา)
4. copy ไฟล์ใบงานไปไว้ใน folder ส่วนตัว เปลี่ยนชื่อให้มีรหัส 3 ตัวท้ายต่อท้ายชื่อไฟล์ เช่น Lab-002.md, Lab-045.md (เปลี่ยนทุกไฟล์ใบงาน)
5. ทำงานแล้วบันทึกผลต่างๆ ลงในไฟล์ใบงานนั้น
6. ส่วนที่ต้องสร้าง project ให้สร้างแยกไว้ตาม folder (ดูหมายเหตุด้านล่าง) 
7. เมื่อทำงานเสร็จ ให้ pull request ไปที่ repo ของ organization รายวิชา

หมายเหตุ เมื่อทำงานเสร็จ ใน repo ของนักศึกษาจะมีโครงสร้างต่อไปนี้
```txt 
[]-(root of repo)
|-------- ไฟล์ต่างๆ ของอาจารย์ (ใบงาน, slides,  ฯลฯ)
+--(6x03xxxx)-+
|             |--- file งานของนักศึกษา (copy มาจากใบงานของอาจารย์)
|             |--- ไฟล์ .gitignore  (visual studio)  <-- (นักศึกษาต้องสร้างเอง)
|             +--(Project8.1)--+
|             |                |--- Visual Studio project files 
|             |                 
|             |                 
|             +--(Project8.2)--+
|             |                |--- Visual Studio project files 
|             |                  
|             |
|             +--(Project___)-+
|                             | 
|                             |--- Visual Studio project files 
|
|                
+--(6x03xxxx)-+ <--(ถ้ามี folder ของเพื่อนติดมาด้วยก็ไม่ต้องไปสนใจ)
|
|
```






## คำถามก่อนการทดลอง ##

1. ให้นักศึกษาพิจารณาชื่อตัวแปรตามตารางต่อไปนี้ ว่าสามารถใช้ได้หรือไม่ พร้อมบอกเหตุผล

| ที่ | ชื่อตัวแปร | ใช้ได้/ไม่ได้ | เหตุผล |
|---:|:-------:|-----------|-------|
|  1.1 | xxx    |ใช้ได้    |ไม่มีตัวอักษรที่ละเมิดกฎการตั้งชื่อ
|  1.2 | null    |ใช้ไม่ได้    |เป็นคำสงวนในภาษา C#
|  1.3 | _value|ใช้ได้ | ไม่มีตัวอักษรที่ละเมิดกฎการตั้งชื่อ        
|  1.4 | First-name  | ใช้ไม่ได้  | ตัวแปรจะต้องไม่ประกอบไปด้วยอักษรพิเศษทุกชนิด         
|  1.5 | Hello!  | ใช้ไม่ได้  | ตัวแปรจะต้องไม่ประกอบไปด้วยอักษรพิเศษทุกชนิด        
|  1.6 | w*h  | ใช้ไม่ได้  |   ตัวแปรจะต้องไม่ประกอบไปด้วยอักษรพิเศษทุกชนิด      
|  1.7 | time  |  ใช้ได้ |  ไม่มีตัวอักษรที่ละเมิดกฎการตั้งชื่อ      
|  1.8 | do  | ใช้ไม่ได้  |  เป็นคำสงวนในภาษา C#      
|  1.9 | Do  |  ใช้ได้ |  ไม่มีตัวอักษรที่ละเมิดกฎการตั้งชื่อ      
| 1.10 |  21November  |  ใช้ไม่ได้ |  ละเมิดกฎการตั้งชื่อ      
| 1.11 |  ladkrabang  |  ใช้ได้ |  ไม่มีตัวอักษรที่ละเมิดกฎการตั้งชื่อ      
| 1.12 | Double  | ใช้ได้  |  ไม่มีตัวอักษรที่ละเมิดกฎการตั้งชื่อ      
| 1.13 | My Car  | ใช้ไม่ได้  |   ละเมิดกฎการตั้งชื่อ     
| 1.14 | my_home  | ใช้ได้  |   ไม่มีตัวอักษรที่ละเมิดกฎการตั้งชื่อ     
| 1.15 | Int   | ใช้ได้  |  ไม่มีตัวอักษรที่ละเมิดกฎการตั้งชื่อ
     


2. จงบอกชนิดข้อมูลที่สามารถรองรับค่าต่อไปนี้อย่างเหมาะสมพร้อมทั้งใส่ค่าเริ่มต้นตามที่กำหนดให้ ถ้าข้อใดมีหลายตัวแปร ให้ระบุให้ครบ
 

2.1 (ตัวอย่าง) เสียงเดินทางด้วยความเร็ว 340.0 เมตรต่อวินาที

```csharp
    float speedOfSound = 340.0;
```

2.2 จำนวนนักศึกษาในชั้นเรียนนี้คือ 42 คน

2.3 ระยะห่างจากดวงอาทิตย์ถึงโลกคือ 149,668,992 กิโลเมตร

2.4 ชาวนามีวัว 12 ตัว ม้า 68 ตัว และ ไก่ 12,000 ตัว ตามกฎหมาย เมืองนี้อนุญาตให้เลี้ยงสัตว์ที่เท้าได้ไม่เกินครอบครัวละ 200 ตัว (มี 3 ตัวแปร)

2.5 แดงวัดขนาดของบ้าน พบว่าต้องใช้อิฐจำนวน 1325.8 ชิ้น แต่เมื่อไปถึงร้านก่อสร้าง พบว่าเขาขายอิฐเป็นยก ยกละ 10 ก้อน ไม่ขายเป็นเศษ

2.6 แสงเดินทางด้วยความเร็ว 299,337.984 กิโลเมตรต่อวินาที  ดาวศุกร์ห่างจากดวงอาทิตย์ 108,200,000 กิโลเมตร อยากทราบว่าแสงใช้เวลาในการเดินทางกี่วินาที (มี 3 ตัวแปร)

---
## การทดลอง ## 

นักศึกษาได้ผ่านการทดลองเขียนโปรแกรมมาพอสมควร ดังนั้นในใบงานจะไม่แสดงรายละเอียดการสร้าง project สิ่งที่เห็นในใบงานจะมีเพียงส่วนของ source code ซึ่งต้องเขียนไว้ใน Main() 

__ถ้าต้องเขียนเป็นอย่างอื่น จะแจ้งไว้ในใบงานเป็นกรณีไป__ 

### Project 8.1 การประกาศตัวแปร ## 
1. สร้าง consol project
2. ใน method main ให้ประกาศตัวแปรดังต่อไปนี้

``` cs
    int var = 30;
    int var1;
    int var2, var3;
    int var4 = var5;
    int var6 = 2, var7;
    int var8 = 10 * 5;
    int var9 = var;
    int var10, char c1, float f1;
    double d1 = false;
    bool b1 = 0;
```

3. มีบรรทัดใดบ้าง ที่มีข้อความผิดพลาด 
  3.1 compiler ฟ้องว่าอะไร
  ![image](https://user-images.githubusercontent.com/92082685/169080902-faba4c0c-6d8c-4a7e-a990-a48dfef024a4.png)

  3.2 นักศึกษาคิดว่าที่ผิดพลาดนั้นเกิดจากอะไร
  ตอบ เกิดจากการใช้ตัวแปรแบบไม่ถูกต้องและใช้ผิดประเภท
  3.3 จะแก้ไขให้ถูกต้องได้อย่างไร
  ตอบ ใช้ตัวแปรให้ถูกต้องตามประเภทและการเรียกใช้

---- 
### Project 8.2 การใช้งานตัวแปรใน string interpreter ## 

String interpreter จะช่วยตีความให้ค่าในตัวแปรชนิดต่างๆ กลายเป็น string โดยอัตโนมัติ ดังตัวอย่าง

 ```cs
    int a = 100;
    string s = $"a = {a}";
 ```

ตัวแปร `a` ในเครื่องหมาย `{ }` จะถูกแปลงเป็นข้อความ เทียบเท่ากับการใช้ `a.ToString();` 


1. สร้าง consol project
2. ใน method Main() ให้เขียนโปรแกรมต่อไปนี้ (แบ่งเป็นรอบๆ ตามชุดที่กำหนด) รันและบันทึกผล 
3. อธิบายสิ่งที่เกิดขึ้นในแต่ละบรรทัด


#### ชุดที่ 1 ####
```cs
    Console.WriteLine("{0} and {1}", 3,5);
    Console.WriteLine("{0} and {1}", 3.0,5.0);
    Console.WriteLine("{0} and {1}", 3.0d, 5.0d);
    Console.WriteLine("{0:F1} and {1:F1}", 3.0, 5.0);
    Console.WriteLine("{0:F2} and {1:F2}", 3.0d, 5.0d);
```
#### อธิบายชุดที่ 1 ####
![image](https://user-images.githubusercontent.com/92082685/169082893-f36d1c15-7520-490b-bbe7-7ad6b9a74c4a.png)
    
     1 แปลง 3 , 5 ให้เป็น String และแสดงผล
     2 แปลง 3.0 , 5.0 ให้เป็น String และแสดงผล จะไม่แสดงทศนิยมที่เป็น .0
     3 แปลง 3.0 , 5.0 ให้เป็น String และแสดงผล จะไม่แสดงทศนิยมที่เป็น .0
     4 แปลง 3.0 , 5.0 ให้เป็น String และแสดงผล จะแสดงทศนิยมตำแหน่งเดียว
     5 แปลง 3.0 , 5.0 ให้เป็น String และแสดงผล จะแสดงทศนิยมสองตำแหน่ง

 
#### ชุดที่ 2 ####
```cs
    Console.WriteLine($"{3} and {1}");
    Console.WriteLine($"{3} and {1}");
    Console.WriteLine($"{3.0d} and {1.0001d}");
    Console.WriteLine($"{3:F2} and {1000.123:F1}");
    Console.WriteLine($"{3.123456:F2} and {5.123000:F4}");
```
#### อธิบายชุดที่ 2 ####
![image](https://user-images.githubusercontent.com/92082685/169083384-6bbf338d-42df-4091-8dee-a08e008ce116.png)

    1 แปลง 3 และ 5 ใน {} ให้เป็น String แสดงผล
    2 แปลง 3 และ 5 ใน {} ให้เป็น String แสดงผล
    3 แปลง 3.0 และ 1.0001 ใน {} ให้เป็น String และแสดงผลจะไม่แสดงทศนิยมที่เป็น .0
    4 แปลง 3 และ 1000.123 ใน {} ให้เป็น String และแสดงผลจะแสดงเลข 3 เป็น 3.00 และเลข 1000.123 เป็น 1000.1
    5 แปลง 3.123456 และ 5.123000 ใน {} ให้เป็น String และแสดงผลจะแสดงเลข 3.123456 เป็น 3.12 และเลข 5.123000   เป็น 5.1230
#### ชุดที่ 3 ####
```cs
    Console.WriteLine($"         1111111111222222");
    Console.WriteLine($"1234567890123456789012345");
    Console.WriteLine($"{1,0}");
    Console.WriteLine($"{1,1}");
    Console.WriteLine($"{1,2}");
    Console.WriteLine($"{1,3}");
    Console.WriteLine($"{1,4}");
    Console.WriteLine($"{1,5}");
    Console.WriteLine($"{1,10}");
    Console.WriteLine($"{1,15}");
    Console.WriteLine($"{1,20}");
    Console.WriteLine($"{1,22}");
    Console.WriteLine($"{1,25}");
```
#### อธิบายชุดที่ 3 ####
![image](https://user-images.githubusercontent.com/92082685/169085954-1f5b060a-f947-4f86-8795-8d2f15ca531b.png)

    1   แสดง 1111111111222222
    2   แสดง 1234567890123456789012345
    3   แสดงเลข 1 และมีการเว้นบรรทัด 0
    4   แสดงเลข 1 และมีการเว้นบรรทัด 1
    5   แสดงเลข 1 และมีการเว้นบรรทัด 2
    6   แสดงเลข 1 และมีการเว้นบรรทัด 3
    7   แสดงเลข 1 และมีการเว้นบรรทัด 4
    8   แสดงเลข 1 และมีการเว้นบรรทัด 5
    9   แสดงเลข 1 และมีการเว้นบรรทัด 10
    10  แสดงเลข 1 และมีการเว้นบรรทัด 15
    11  แสดงเลข 1 และมีการเว้นบรรทัด 20
    12  แสดงเลข 1 และมีการเว้นบรรทัด 22
    13  แสดงเลข 1 และมีการเว้นบรรทัด 25
#### ชุดที่ 4 ####
```cs
    int i = 123456789;
    Console.WriteLine("Regular string format");
    Console.WriteLine("{0}",i);
    Console.WriteLine("String interpreter");
    Console.WriteLine($"None ==> {i}");
    Console.WriteLine($"   E ==> {i:E}");
    Console.WriteLine($"   F ==> {i:F}");
    Console.WriteLine($"   G ==> {i:G}");
    Console.WriteLine($"   N ==> {i:N}");
    Console.WriteLine($"   P ==> {i:P}");
    Console.WriteLine($"   X ==> {i:X}");
```
#### อธิบายชุดที่ 4 ####
![image](https://user-images.githubusercontent.com/92082685/169086328-231928b1-3daf-4e15-95fb-89439ed0abed.png)

    1   ประกาศตัวแปร i = 123456789 
    2   แสดงข้อความ Regular string format
    3   จัดรูปแบบชนิดข้อมูลของตัวแปร i ให้เป็นชนิด String และแสดงผลในตัวแปร i
    4   แสดงผล String interpreter
    5   แสดงผล None ==> 123456789 รูปแบบ String 
    6   แสดงผล    E ==> 12345678E+008 (Scientific) รูปแบบ String 
    7   แสดงผล    F ==> 123456789.00 (Fixed point) รูปแบบ String 
    8   แสดงผล    G ==> 123456789 (General) รูปแบบ String 
    9   แสดงผล    N ==> 123,456,789.00 (Number) รูปแบบ String 
    10  แสดงผล    P ==> 12,345,678,900.00% (Percent) รูปแบบ String 
    11  แสดงผล    X ==> 75BCD15 (Hexadecimal) รูปแบบ String 

#### ชุดที่ 5 ####
```cs
    int i = 123456789;
    Console.WriteLine("Regular string format");
    Console.WriteLine("         {0,20}",i);
    Console.WriteLine("String interpreter");
    Console.WriteLine($"None ==> {i,20}");
    Console.WriteLine($"   E ==> {i,20:E}");
    Console.WriteLine($"   F ==> {i,20:F}");
    Console.WriteLine($"   G ==> {i,20:G}");
    Console.WriteLine($"   N ==> {i,20:N}");
    Console.WriteLine($"   P ==> {i,20:P}");
    Console.WriteLine($"   X ==> {i,20:X}");
```
#### อธิบายชุดที่ 5 ####
![image](https://user-images.githubusercontent.com/92082685/169086457-232d090b-6683-4709-a28f-2f4e5feaaca1.png)

    1   ประกาศตัวแปร i = 123456789 
    2   แสดงผล Regular string format
    3   จัดรูปแบบชนิดข้อมูลของตัวแปร i ให้เป็นชนิด String แสดงผลในตัวแปร i และเว้นบรรทัด 20
    4   แสดงผล String 
    5   แสดงผล None ==> 123456789 จัดรูปแบบ String  และเว้นบรรทัด 20
    6   แสดงผล  E ==> 12345678E+008 (Scientific) จัดรูปแบบ String  และเว้นบรรทัด 20
    7   แสดงผล  F ==> 123456789.00 (Fixed point) จัดรูปแบบ String  และเว้นบรรทัด 20
    8   แสดงผล  G ==> 123456789 (General) จัดรูปแบบ String  และเว้นบรรทัด 20
    9   แสดงผล  N ==> 123,456,789.00 (Number) จัดรูปแบบ String  และเว้นบรรทัด 20
    10  แสดงผล  P ==> 12,345,678,900.00% (Percent) จัดรูปแบบ String  และเว้นบรรทัด 20
    11  แสดงผล  X ==> 75BCD15 (Hexadecimal) จัดรูปแบบ String และเว้นบรรทัด 20

#### ชุดที่ 6 ####
```cs
    const double i = 123.456789;
    Console.WriteLine($"{i,10:F1}");
    Console.WriteLine($"{i,10:F2}");
    Console.WriteLine($"{i,10:F3}");
    Console.WriteLine($"{i,10:F4}");
    Console.WriteLine($"{i,10:F5}");
```
#### อธิบายชุดที่ 6 ####
![image](https://user-images.githubusercontent.com/92082685/169086612-ecf48e1c-6aab-4c71-9b60-bdec53745316.png)

    1  กำหนดตัวแปร i เป็นชนิด double มีค่า 123.456789
    2  แสดงค่าในตัวแปร i คือ 123.5 เว้นบรรทัด 10 มีทศนิยม 1 ตำแหน่ง
    3  แสดงค่าในตัวแปร i คือ 123.46 เว้นบรรทัด 10 มีทศนิยม 2 ตำแหน่ง
    4  แสดงค่าในตัวแปร i คือ 123.457 เว้นบรรทัด 10 มีทศนิยม 3 ตำแหน่ง
    5  แสดงค่าในตัวแปร i คือ 123.4568 เว้นบรรทัด 10 มีทศนิยม 4 ตำแหน่ง
    6  แสดงค่าในตัวแปร i คือ 123.45679 เว้นบรรทัด 10 มีทศนิยม 5 ตำแหน่ง
#### ชุดที่ 7 ####
```cs
    string name = "Hello";
    Console.WriteLine(String.Format("{0} there. I said {0}! {0}???", name));
    Console.WriteLine($"{2:d} {0:d} {1:d}", 1, 2, 3);
    Console.WriteLine($"Hello " + $"World");
    Console.WriteLine($"Here comes a slash \\");
    Console.WriteLine($"|{999, 10}|");
    Console.WriteLine($"|{000,-10}|");
    Console.WriteLine($"The value: {500}.");
    Console.WriteLine($"The value: {500:C}.");
    Console.WriteLine($"{12.3456789,-10:F4}");
    Console.WriteLine($"{12.3456789,-10:C}");
    Console.WriteLine($"{12.3456789,-10:E3}");
    Console.WriteLine($"{65535,-10:x}");
    Console.WriteLine($"{65535,-10:X}");
    int i;
    Console.WriteLine("Value\tSquared\tCubed");
    for (i = 1; i < 10; i++)
        Console.WriteLine($"{i}\t{i*i}\t{i*i*i}");
    Console.WriteLine($"{1234.56789:#.###}.");
```
#### อธิบายชุดที่ 7 ####
![image](https://user-images.githubusercontent.com/92082685/169086960-def1862a-bc07-430a-b582-0dd431acce52.png)

  1. ตัวแปร name เป็น string ค่าคือ Hello
  2. ใช้ String.Format แสดงผล Hello there. I said Hello! Hello???
  3. แสดงผล 2 0 1
  4. แสดงผล Hello World ใช้ + เพื่อต่อข้อความ
  5. แสดงผล Here comes a slash \
  6. แสดงผล 999 เว้นบรรทัด 10
  7. แสดงผล 000 เว้นบรรทัด -10 เว้นบรรทัดหลัง 000
  8. แสดงผล The value: 500.
  9. แสดงผล The value: ฿500.00.0 (Currency)
  10. แสดงผล 12.3457 เว้นบรรทัด -10 เว้นบรรทัดหลัง 12.3457 
  11. แสดงผล ฿12.35 (Currency) เว้นบรรทัด -10 เว้นบรรทัดหลัง ฿12.35
  12. แสดงผล 1.235E+001 (Scientific) เว้นบรรทัด -10 เว้นบรรทัดหลัง 1.235E+001
  13. แสดงผล ffff (Hexadecimal) ตัวพิมพ์เล็ก เว้นบรรทัด -10 เว้นบรรทัดหลัง ffff
  14. แสดงผล FFFF (Hexadecimal) ตัวพิมพ์ใหญ่ เว้นบรรทัด -10 เว้นบรรทัดหลัง FFFF
  15. ประกาศ i เป็น int
  16. แสดงผล Value Squared Cubed การที่ \t คือการเว้นช่องว่าง
  17. กำหนด loop for ให้ i = 1 ถ้า i < 10 เพิ่มค่า i ขึ้นทีละ 1
  18. แสดงผลในตัวแปร i ตามจำนวน loop for 
  19. แสดงผล 1234.568. ทศนิยม 3 ตำแหน่งด้วย ###
---- 
### Project 8.3 static keyword ## 
1. สร้าง project ชนิด console
2. เขียนโปรแกรมต่อไปนี้

```cs
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;


namespace method_examples
{
    class number
    {
        static public int numberInt1;
        static public double numberDouble1;
        public int numberInt2;
        public double  numberDouble2;
    }
    class Program
    {
        static void Main()
        {
            number.numberInt1 = 10;
            number.numberInt2 = 20;
            number.numberDouble1 = 100.500;
            number.numberDouble2 = 200.500;

            Console.WriteLine($"numberInt1 = {number.numberInt1}");
            Console.WriteLine($"numberInt2 = {number.numberInt2}");
            Console.WriteLine($"numberDouble1 = {number.numberDouble1}");
            Console.WriteLine($"numberDouble2 = {number.numberDouble2}");

        }
    }
}
```

### คำถาม ###
1. ผลการทำงานเป็นอย่างไร

ตอบ Error รันโปรแกรมไม่ได้ 

2. บรรทัดไหนของโปรแกรมที่มี error บ้าง เพราะอะไร

ตอบ บรรทัด 22,24,27,29 เพราะไม่ได้ประกาศตัวแปรเป็นที่เป็น static

3. ถ้าจะให้โปรแกรมทำงานได้ สามารถแก้ไขอย่างไรได้บ้าง

ตอบ ประกาศให้เป็น static
