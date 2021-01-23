using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace HW2_3
{
    class Program
    {
        static void Main(string[] args)
        {
            int numOfUser = int.Parse(Console.ReadLine());

            if(numOfUser%2==0)
                Console.WriteLine("Число является четным");
            else 
            {
                Console.WriteLine("Число является нечетным");
            }


            Console.ReadLine();

        }
    }
}

using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace HW2_5_2_2_2_1
{
    class Program
    {
        static void Main(string[] args)
        {
            int numOfMonth = int.Parse(Console.ReadLine());
            switch (numOfMonth)
            {
                case 1:
                    Console.WriteLine("January");
                    break;
                case 2:
                    Console.WriteLine("February");
                    break;
                case 3:
                    Console.WriteLine("March");
                    break;
                case 4:
                    Console.WriteLine("April");
                    break;
                case 5:
                    Console.WriteLine("May");
                    break;
                case 6:
                    Console.WriteLine("June");
                    break;
                case 7:
                    Console.WriteLine("July");
                    break;
                case 8:
                    Console.WriteLine("August");
                    break;
                case 9:
                    Console.WriteLine("September");
                    break;
                case 10:
                    Console.WriteLine("October");
                    break;
                case 11:
                    Console.WriteLine("November");
                    break;
                case 12:
                    Console.WriteLine("December");
                    break;
                default:
                    Console.WriteLine("Ошибка! Такого месяца не существует!");
                    break;
            }

            Console.WriteLine("Введите максимальную температуру за сутки");
            uint maxTemperature = uint.Parse(Console.ReadLine());
            Console.WriteLine("Введите минимальную температуру за сутки");
            uint minTemperature = uint.Parse(Console.ReadLine());

            uint middleTemperature = (maxTemperature + minTemperature) / 2;

            if (numOfMonth==1||numOfMonth==2||numOfMonth==12)
                if(middleTemperature>0)
                    Console.WriteLine("Дождливая зима");


          Console.ReadLine();  
        }
    }
}

using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace HW2_4
{
    class Program
    {
        static void Main(string[] args)
        {
            string nameOfShop = "Alcor";
            string dateOfBuy = "21.01.21";
            long orderNumberOfPurchase = 13005469863;
            int stepOfNumberBuy = 1;

            Console.WriteLine("***************************************");
            Console.WriteLine("*              "+nameOfShop+"                  *");
            Console.WriteLine("*            8-800-123-45-67          *");
            Console.WriteLine("***************************************");
            Console.WriteLine("          КАССОВЫЙ ЧЕК ПРИХОДА         ");
            Console.WriteLine("Касса АНК   Продавец 60      Кассир 58 ");
            Console.WriteLine("           Чек 100040426               ");
            Console.WriteLine("---------------------------------------");
            Console.WriteLine((orderNumberOfPurchase+stepOfNumberBuy)+" Шампунь для укрепления волос ");
            Console.WriteLine("                   300      *2      =600");
            Console.WriteLine((orderNumberOfPurchase + stepOfNumberBuy) + " Маска ");
            Console.WriteLine("                   540      *2     =1080");
            Console.WriteLine("----------------------------------------");
            Console.WriteLine("ИТОГО                               1680");
            Console.WriteLine("     Получено:                      2000");
            Console.WriteLine("     Сдача:                          320");
            Console.WriteLine("----------------------------------------");
            Console.WriteLine("НАЛИЧНЫМИ                          =1680");
            Console.WriteLine("СУММА НДС 20/120                    =280");
            Console.WriteLine("СНО ОСН");
            Console.WriteLine("Кассир  Кружилина Лилия Витальевна      ");
            Console.WriteLine("Пользователь " + nameOfShop);
            Console.WriteLine("Адрес: 162390, Вологодская область,     ");
            Console.WriteLine("г. Великий Устюг, ул. Красная, д. 128   ");
            Console.WriteLine("Сайт проверки               www.nalog.ru");
            Console.WriteLine("ЗН ККТ 04725482548  РН ККТ 3548563892638");
            Console.WriteLine("ПРИХОД =1680         СМЕНА 0125 ЧЕК 0056");
            Console.WriteLine("ФП 343863 ФД 1517 "+dateOfBuy+" 18:35:34");
            Console.ReadLine();

        }
    }
}

//1 ВАРИАНТ 6 ЗАДАЧИ 

public enum week
    {
        Monday      = 0b_1000000,
        Tuesday     = 0b_0100000,
        Wednesday   = 0b_0010000,
        Thursday    = 0b_0001000,
        Friday      = 0b_0000100,
        Saturday    = 0b_0000010,
        Sunday      = 0b_0000001
    }
и использовать switch

switch (day)
{
case "пн":
bitMaskDay = week.Monday;
break;
case "вт":
bitMaskDay = week.Tuesday;
break;
case "ср":
bitMaskDay = week.Wednesday;
break;
case "чт":
bitMaskDay = week.Thursday;
break;
case "пт":
bitMaskDay = week.Friday;
break;
case "сб":
bitMaskDay = week.Saturday;
break;
case "вс":
bitMaskDay = week.Sunday;
break;
default:
bitMaskDay = 0;
break;
}

//2ВАРИАНТ ЗАДАЧИ (МОЙ ПОЛНОСТЬЮ)

  static void Main(string[] args)
        {
            Console.WriteLine("Введите рабочий день");
            int randomWorkDay = Convert.ToInt32(Console.ReadLine());
            if(randomWorkDay== 0000001 | randomWorkDay== 0000100 | randomWorkDay== 0010000)
                Console.WriteLine("В этот день работает первый офис");
            else if (randomWorkDay == 0000010 | randomWorkDay == 0001000 | randomWorkDay == 0100000)
                Console.WriteLine("В этот день работает второй офис");
            else if(randomWorkDay == 100_0000)
                Console.WriteLine("В этот день -выходной");
            else
                Console.WriteLine("Ошибка! Данные введены неверно!");

            Console.ReadLine();

        }
