# CSharp_SimpleCalculator
using System;

class Program
{
    static void Main()
    {
        Console.WriteLine("Simple Calculator using C#");
        Console.WriteLine("--------------------------");

        Console.Write("Enter first number: ");
        double num1 = Convert.ToDouble(Console.ReadLine());

        Console.Write("Enter second number: ");
        double num2 = Convert.ToDouble(Console.ReadLine());

        Console.WriteLine("Choose operation: + - * /");
        char op = Convert.ToChar(Console.ReadLine());

        double result = 0;
        bool valid = true;

        switch (op)
        {
            case '+':
                result = num1 + num2;
                break;

            case '-':
                result = num1 - num2;
                break;

            case '*':
                result = num1 * num2;
                break;

            case '/':
                if (num2 != 0)
                    result = num1 / num2;
                else
                {
                    Console.WriteLine("Cannot divide by zero!");
                    valid = false;
                }
                break;

            default:
                Console.WriteLine("Invalid operation.");
                valid = false;
                break;
        }

        if (valid)
            Console.WriteLine("Result: " + result);
    }
}
