# การทดลอง Constants #

## การทดลอง 10.3 Constants ##

1. ให้นักศึกษาสร้าง project ชนิด Console application แล้วเขียน code ต่อไปนี้

``` cs
using System;
class Circle
{
    public const double PI = 3.14;
    static public void CalculateArea(double radius)
    {
        Console.WriteLine($"Area of circle = {PI * radius * radius} square unit.");
    }
    
}
class Program
{
    static void Main()
    {
        Circle.CalculateArea(radius: 10.0);
    }
}
```

2. บันทึกผลจากการรันโปรแกรม

![image](https://user-images.githubusercontent.com/92080550/169265600-28464c5a-f797-4344-ab1a-be1b2b72efeb.png)


3. ค่า PI จากตัวอย่างที่แล้ว เป็นค่าโดยประมาณที่ขาดความละเอียด จึงได้กดเครื่องคิดเลข ได้ค่า PI มาเป็นทศนิยม 10 หลัก จึงนำมาใส่ในโปรแกรมแทนที่ค่า PI เดิม ก่อนหาพื้นที่

```cs
using System;
class Circle
{
    public const double PI = 3.14;
    static public void CalculateArea(double radius)
    {
        // คำนวณจากเครื่องคิดเลข ได้ค่าที่ละเอียดกว่า จึงนำมาเปลี่ยนก่อนคำนวณพื้นที่
        PI = 3.14159265359;
        Console.WriteLine($"Area of circle = {PI * radius * radius} square unit.");
    }
    
}
class Program
{
    static void Main()
    {
        Circle.CalculateArea(radius: 10.0);
    }
}

```
4. บันทึกผลจากการรันโปรแกรม

![image](https://user-images.githubusercontent.com/92080550/169265898-9325a117-f16b-4d38-b1c2-b9ceddb78d50.png)



5. เปรียบเทียบและอธิบายสิ่งที่ได้จากการรันโปรแกรมในข้อ 1 และ ข้อ 3

ตอบ ข้อที่ 1 สามารถรันได้ปกติ เพราะไม่ได้มีการเปลี่ยนแปลงค่าคงที่ของตัวแปรที่ได้ประกาศไว้
ข้อที่ 3 ไม่สามารถรันได้ เพราะมีการเปลี่ยนแปลงค่าคงที่ของตัวแปรที่ได้ประกาศไว้

### คำถาม ###
1. โปรแกรมในข้อ 1 และ 3 สามารถทำงานได้ตามปกตือหรือไม่

ตอบ โปรแกรมในข้อ 1 สามารภทำงานได้ปกติ
โปรแกรมในข้อ 3 ไม่สามารภทำงานได้

2. ข้อใดรันได้หรือไม่ได้

ตอบ โปรแกรมในข้อ 1 สามารภรันโปรแกรมได้ปกติ
โปรแกรมในข้อ 3 ไม่สามารถรันโปรแกรมได้

3. ถ้าจะให้แก้ไขโปรแกรม ต้องแก้ที่จุดไหน อย่างไร

ตอบ กำหนดในตัวแปรตั้งแต่แรก เช่น public const double PI = 3.14159265359 หรือ ไม่ใช้ตัวแปรแบบค่าคงที่ ก็จะสามารถเปลี่ยนแปลงค่าได้
