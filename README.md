using System;

namespace MyApp // Note: actual namespace depends on the project name.
{
    internal class Program

    {
        public static int Sum(int num1, int num2)

        {
            int total;
            total = num1 + num2;
            return total;
        }


        static void Main(string[] args)
        {


            string Greeting = Console.ReadLine();
            string pName = "John";

            if (Greeting == "hello")
            {
                Console.WriteLine("Welcome Friend" + " " + pName + "\nHave a nice day");

            }
            else
            {
                Environment.Exit(0);
            }
            Console.Writeline("what two numbers would you like to add together?");
            Console.Write("Enter a number: ");
            int n1 = Convert.ToInt32(Console.ReadLine());
            Console.Write("Enter another number: ");
            int n2 = Convert.ToInt32(Console.ReadLine());
            Console.WriteLine("the answer is" + " " + Sum(n1, n2));
            Console.WriteLine("write a sentance and i will tell you how much space");


            int SpaceCount(string str)
            {
                int spcctr = 0;
                string str1;
                for (int i = 0; i < str.Length; i++)
                {
                    str1 = str.Substring(i, 1);
                    if (str1 == " ")
                        spcctr++;
                }
                return spcctr;
            }
            string str2;
            Console.Write("Please Enter a sentance: ");
            str2 = Console.ReadLine();
            Console.WriteLine("\"" + str2 + "\"" + " contains {0} spaces", SpaceCount(str2));

            int[] arraydata = { 0, 5, 1, 7, 2, 3, 3, 2, 4, 9, };
            Console.WriteLine("\nArray: [{0}]", string.Join(", ", arraydata));
            var sum = 0;
            for (var k = 0; k < arraydata.Length; k++)
            {
                sum += arraydata[k];
            }
            Console.WriteLine("the sum of the ellement is " + sum);

            {
                int First, Second, temp;
                Console.Write("\nEnter the First Number : ");
                First = int.Parse(Console.ReadLine());
                Console.Write("\nEnter the Second Number : ");
                Second = int.Parse(Console.ReadLine());
                temp = First;
                First = Second;
                Second = temp;
                Console.Write("\nAfter Swapping : ");
                Console.Write("\nFirst Number : " + First);
                Console.Write("\nSecond Number : " + Second);

            }

            {
                int Base1;
                int exponent1;
                Console.Write("\nTo calculate the result of raising an integer number to another");
                Console.Write("\n\nEnter Base number: ");
                Base1 = Convert.ToInt32(Console.ReadLine());
                Console.Write("Enter the Exponent : ");
                exponent1 = Convert.ToInt32(Console.ReadLine());
                Console.WriteLine("So, the number {0} ^ (to the power) {1} = {2} ", Base1, exponent1, PowerRaising(Base1, exponent1));
            }
            static int PowerRaising(int num, int exp)
            {
                int rvalue = 1;
                int i;
                for (i = 1; i <= exp; i++)
                    rvalue = rvalue * num;
                return rvalue;
            }
            {
                Console.WriteLine(" \ndidn't understand what to do with question 8"); // need to do more research on Fibonacci 
            }
            {
                int n, i, m = 0, flag = 0;
                Console.Write("Enter the Number to check Prime: ");
                n = int.Parse(Console.ReadLine());
                m = n / 2;
                for (i = 2; i <= m; i++)
                {
                    if (n % i == 0)
                    {
                        Console.Write("Number is not Prime.");
                        flag = 1;
                        break;
                    }
                }
                if (flag == 0)
                    Console.Write("Number is Prime.");
                // need to work more on Fibonacci and what it means
                {
                    Console.WriteLine("thank you for your time");
                }
                

            }
        }
    }
}

            
            
        
    
