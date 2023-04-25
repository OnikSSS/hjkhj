using System;
using System.Linq;
using System.Collections.Generic;
using System.Text;

namespace HelloWold;

public static class Program
{
    public static void Main()
    {
        Console.InputEncoding = Encoding.Unicode;
        Console.OutputEncoding = Encoding.Unicode;
        int num1;
        int num2;
        string dia;
        int vidpovid;
        float dilenie;
        Console.Write("Введіть перше число:");
        num1 = Convert.ToInt32(Console.ReadLine());
        Console.Write("Введіть друге число:");
        num2 = Convert.ToInt32(Console.ReadLine());
        Console.Write("Виберіть дію:");
        dia = Console.ReadLine();
        switch (dia)
        {
            case "+":
                vidpovid = num1 + num2;
                Console.Write($"Ваша відповідь: {num1} {dia} {num2} = {vidpovid}");
                break;
            case "*":
                vidpovid = num1 * num2;
                Console.Write($"Ваша відповідь: {num1} {dia} {num2} = {vidpovid}");
                break;
            case "/":
                if (num2 == 0)
                {
                 Console.Write($"На {num2} ділити не можна!");
                }
                else if (num2 != 0)      
                {
                 dilenie = Convert.ToSingle(num1) / num2;
                 Console.Write($"Ваша відповідь: {num1} {dia} {num2} = {dilenie}");
                }
                break;
            case "-":
                vidpovid = num1 - num2;
                Console.Write($"Ваша відповідь: {num1} {dia} {num2} = {vidpovid}");
                break;
            default:
                Console.Write("В моїй програмі такої дії немає");
                break;
        }

    }

}
