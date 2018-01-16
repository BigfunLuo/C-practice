# C-practice
using System;

namespace calculator//name of application;
{
    class Program
    {
        public static float addition(float x, float y)//function also need static and need to use pubilc
        {
            return x + y;                          //function of addition
        }
        public static float subtraction(float x, float y)
        {
            return x - y;                       //function of subtraction
        }
        public static float multiplication(float x, float y)
        {
            return x * y;                  //function of multiplication
        }
        public static float division(float x, float y)
        {
            return x / y;                     //function of division
        }
        public static float reminder(float x, float y)
        {
            return x % y;               //function of reminder
        }
        public static int menu()//function of  menu
        {
            string stringInput;
            int tmp;
            Console.WriteLine(" 1 -  Addition "); //list of menu
            Console.WriteLine(" 2 -  subtraction");
            Console.WriteLine(" 3 -  multiplication");
            Console.WriteLine(" 4 -  division");
            Console.WriteLine(" 5 -  reminder");
            do                                        //do while loop to decide to continue
            {
                Console.WriteLine("Enter your choice: ");
                stringInput = Console.ReadLine();
                tmp = Convert.ToInt32(stringInput);
            } while (tmp < 1 || tmp > 5);
            return tmp;
        }

        static void Main(string[] args)
        {

            string stringInput;//declare the input to store the data;
            int nb;
            float x, y, sum, sub, multip, divide, remide;//declare the variable;
            Console.WriteLine("\n\t\t Welcome to C# programming!");//writeline=cout to display title;
            Console.WriteLine("Enter first integer value: ");//to display Enter the value;
            stringInput = Console.ReadLine();//readline=cin ;
            x = Convert.ToInt32(stringInput);//to store data x to variable;
            Console.WriteLine("Enter second integer value: ");
            stringInput = Console.ReadLine();//to store data x to variable;
            y = Convert.ToInt32(stringInput);
            sum = addition(x, y);//use function addition
            sub = subtraction(x, y);//use function subtraction
            multip = multiplication(x, y);//use function multiplication
            divide = division(x, y);//use function division
            remide = reminder(x, y);//use function reminder
            nb = menu();
            if(nb==1)//to call the calculate function
            {
                Console.WriteLine("\n x + y = " + sum);
            }
            else if(nb==2)
            {
                Console.WriteLine("\n x - y = " + sub);
            }
            else if (nb == 3)
            {
                Console.WriteLine("\n x * y = " + multip);
            }
            else if (nb == 4)
            {
                Console.WriteLine("\n x / y = " + divide);
            }
            else if (nb ==5 )
            {
                Console.WriteLine("\n x % y = " + remide);
            }
            Console.ReadKey();//the function to system pause
        }

    }
}
