# Operator-Overloading

## Aim:
 To write a C# program to pass values through constructors(default and parameterized) and also overload equal operators by checking whether objects are equal using operator overloading. 
 
 ## Algorithm:
 ### Step 1:
Create a class for operator overloading
### Step 2:
Get inputs for length,breadth from the user in overloading function.
### Step 3:
Compare the inputs such as length and breadth.
### Step 4:
Using equal to(==) and not equal to(!=) operator we can compare the inputs.
### Step 5:
After that print the result.

## Program:
```
Developed by: S.Sham Rathan
Register Num: 212221230093

using System;
namespace Inheritance_Constructors
{
   class box
   {
       public int breadth;
       public int length;
       public box(int a, int b)
       {
           this.length = b;
           this.breadth = a;

           Console.WriteLine("this is a parameterized constucted\n The value of Length is {0} and breadth is {1}", this.length , this.breadth );
       }
       public box()
       {
           this.length = this.breadth = 10;
           Console.WriteLine("this is a default constructor");
       }
       public static bool operator ==(box length, box breadth)
       {
           bool status = false;
           if (length == breadth)
           {
               status = true;
           }
           return status;

       }
       public static bool operator !=(box length, box breadth)
       {
           bool status = false;
           if (length != breadth)
           {
               status = true;
           }
           return status;

       }
       public static void Main(string[] args)
       {
           //box l1 = new box();
           box l1 = new box(10 , 14);
           if (l1.length == l1.breadth)
           {
               Console.WriteLine("They both are equal");
           }
           else if (l1.length != l1.breadth)
           {
               Console.WriteLine("They both are different ");
           }

       }

   }
}

```
 
## Output:

![11](https://user-images.githubusercontent.com/93587823/199152560-acc35b03-5721-44be-8e64-3caadce7ab7b.png)

 
 
## Result:
Thus the C# program to find the volume of a box using operator overloading is implemented successfully.
