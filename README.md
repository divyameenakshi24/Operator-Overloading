# Operator-Overloading

## Aim:
 To write a C# program to find the volume of a box using operator overloading
 
 ## Algorithm:
1.Create a class for operator overloading

2.Get inputs for length,breadthandheight of the box fromthe user and then calculate the volume in overloading function

3.After that return a new object for the calculated volume

4.Then create a new object to store the return object

5.After that print the calculated volume
 
 ## Program:
 
```
using System;
namespace ConsoleApp1
{
    class tech
    {
        public int length, breadth, height, volume;
        public static tech operator+(tech t1, tech t2)
        {
            tech t3 = new tech();
            t3.length = t1.length + t2.length;
            t3.breadth = t1.breadth + t2.breadth;
            t3.height = t1.height + t3.volume;
            t3.volume = t3.length * t3.breadth * t3.height;
            t2.volume  = t2.length * t2.breadth * t2.height;
            t1.volume = t1.length * t1.breadth * t1.height;
            return t3;
        }
        public static void Main()
        {
            tech t1 = new tech();
            Console.WriteLine("Enter the length of box1:");
            t1.length = Convert.ToInt32(Console.ReadLine());
            Console.WriteLine("Enter the breadth of box1:");
            t1.breadth = Convert.ToInt32(Console.ReadLine());
            Console.WriteLine("Enter the height of box1:");
            t1.height = Convert.ToInt32(Console.ReadLine());

            tech t2 = new tech();
            Console.WriteLine("Enter the length of box2:");
            t2.length = Convert.ToInt32(Console.ReadLine());
            Console.WriteLine("Enter the breadth of box2:");
            t2.breadth = Convert.ToInt32(Console.ReadLine());
            Console.WriteLine("Enter the height of box2:");
            t2.height = Convert.ToInt32(Console.ReadLine());

            tech t4 = new tech();
            t4 = t1 + t2;
            Console.WriteLine("Box3 volume");
            Console.WriteLine(t4.volume);
            Console.WriteLine("Box1 volume");
            Console.WriteLine(t1.volume);
            Console.WriteLine("Box2 volume");
            Console.WriteLine(t2.volume);

        }
    }
}
```
 
 ## Output:
 ![c#](https://user-images.githubusercontent.com/75235402/170473665-bf78feda-6da5-4d98-8bf6-24e7eafe6c8f.PNG)

 
 ## Result:
 Thus the C# program to find the volume of a box using operator overloading is implemented successfully.
