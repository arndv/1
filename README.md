# 1

Посочете коя среда за разработка на кой програмен език съответства?

За програмиране на езика Python:	
PyCharm
 
За програмиране на езика Java:	
IntelliJ IDEA
 
За програмиране на езика C#:	
Visual Studio
 
 
Дефинирайте понятието вложени цикли.

Вложените цикли представляват конструкция, при която в тялото на един цикъл (външен) се изпълнява друг цикъл (вътрешен). За всяко завъртане на външния цикъл, вътрешният се извърта целият. Това се случва по следния начин:
При стартиране на изпълнение на вложени цикли първо стартира външният цикъл: извършва се инициализация на неговата управляваща променлива и след проверка за край на цикъла, се изпълнява кодът в тялото му.
След това се изпълнява вътрешният цикъл. Извършва се инициализация на началната стойност на управляващата му променлива, прави се проверка за край на цикъла и се изпълнява кодът в тялото му.
При достигане на зададената стойност за край на вътрешния цикъл, програмата се връща една стъпка нагоре и се продължава започналото изпълнение предходния (външния) цикъл. Променя се с една стъпка управляващата променлива за външния цикъл, проверява се дали условието за край е удовлетворено и започва ново изпълнение на вложения (вътрешния) цикъл.
Това се повтаря докато променливата на външния цикъл достигне условието за край на цикъла.

Показан е следният програмен фрагмент на C#. Обобщете какъв ще бъде резултатът от изпълнението на програмата?

    int n  = int.Parse(Console.ReadLine());
    for (int i = n; i > 0; i--)
    {
     Console.WriteLine(i);
    }

Правилният отговор е: Програмата прочита едно целочислено число. След което цикълът отпечатва числата от 1 до това число n в обратен ред, като всяко едно от числата се отпечатва на отделен ред.


//zadachata s bananite i domatite
tomato lemon. Когато имаме само една команда в тялото на if конструкцията, можем да пропуснем къдравите скоби, обозначаващи тялото на условния оператор. Когато искаме да изпълним блок от код (група команди), къдравите скоби са задължителни. В случай че ги изпуснем, ще се изпълни само първият ред след if клаузата.

// futbolen mach

    static void Main(string[] args)
        {
            string sector = Console.ReadLine();
            int row = int.Parse(Console.ReadLine());
            int col = int.Parse(Console.ReadLine()); 
            double totalSum = 0;

            switch (sector)
            { 
                case "Sector A":
                    totalSum = GetTotalProfit(row, col, 11.60); 
                    break; 
                case "Sector B":
                    totalSum = GetTotalProfit(row, col, 14.50);
                    break;
                case "Sector C": 
                    totalSum = GetTotalProfit(row, col, 16.10); 
                    break;
                case "Sector D":
                    totalSum = GetTotalProfit(row, col, 8.40);
                    break;
            }
            Console.WriteLine($"{sector} profit is {totalSum:f2} lv.");
        }
        static double GetTotalProfit(int row, int col, double price)
        {
            return row * col * price;
        }
        
        
Формулирайте правилно определението за условни конструкции.

Условните конструкции if и if-else представляват [тип условен контрол], чрез който програмата може да се държи [различно], в зависимост от [някакво условие], което се проверява по време на изпълнение на конструкцията. 



Посочете как задаваме в C# пълната форма на условни конструкции?
if(true) { //some code... } else { //some code... }


//zadachata s elenite na dqdo koleda
      
      int days = int.Parse(Console.ReadLine());
            int kgFood = int.Parse(Console.ReadLine()); 
            double dailyFoodFirst = double.Parse(Console.ReadLine()); 
            double dailyFoodSecond = double.Parse(Console.ReadLine()); 
            double dailyFoodThird = double.Parse(Console.ReadLine()); 

            
            double foodNeeded = days * dailyFoodFirst
                                + days * dailyFoodSecond
                                + days * dailyFoodThird; 

            if (kgFood >= foodNeeded) 
            {
                Console.WriteLine($"{Math.Floor(kgFood - foodNeeded)} kilos of food left.");
            }
            else 
            {
                Console.WriteLine($"{Math.Ceiling(foodNeeded - kgFood)} more kilos of food are needed.");
            }

Дефинирайте понятието "цикли" в програмирането. Избройте видовете цикли в C#.
Конструкции за повторение на група команди, известни в програмирането с понятието "цикли".
В програмирането често пъти се налага да изпълним блок с команди няколко пъти. За целта се използват т.нар. цикли.
Примери: for, while, do-while, foreach.


Дайте пример за метод (напишете примерен код), който сумира числата от 1 до n включително и като резултат връща тази сума. За примера използвайте код написан на програмния език C#.

     public static int SumNumbers(int n)
     {
       int sum = 0;
       for (int i = 1; i <= n; i++)
       {
            sum += i;
        }
       return sum;
     }

Дайте пример за for - цикъл в C#. За пример може да ползвате код, който отпечатва на конзолата числата от 1 до 100.

    for (int i = 1; i <= 100; i++)
    {
      Console.WriteLine(i);
    }


Посочете кое от изброените НЕ е вярно за стойностните типове данни?
Стойностните типове данни съдържат в стека за изпълнение на програмата референция (адрес) към динамичната памет (heap).


Дефинирайте понятието алгоритъм.
Поредица от команди, необходими, за да се свърши определена работа.


//Деление без остатък
  
            int n = int.Parse(Console.ReadLine()); 
            int d2 = 0; //2Т
            int d3 = 0; 
            int d5 = 0; 

            for (int i = 0; i < n; i++) //2Т
            {
                int number = int.Parse(Console.ReadLine());//2Т
                if (number % 2 == 0) 
                {
                    d2++; 
                }//1Т
                if (number % 3 == 0) 
                {
                    d3++; //1Т
                }
                if (number % 5 == 0) //2Т
                {
                    d5++; 
                }
            }

            Console.WriteLine(d2); 
            Console.WriteLine(d3); 
            Console.WriteLine(d5);
            
            
Напишете метод на C#, който отпечатва на конзолата квадрат от звездички с размери nхn. //kvadrat sus zvezdichki//

   
     public void PrintSquare(int n)
        {
            for (int i = 1; i <= n; i++)
            {
                for (int j = 1; j <= n; j++)
                {
                    Console.Write("* ");
                }
                Console.WriteLine();
            }
        }
        
Посоченият по-долу фрагмент на C# събира числото 0.00001 общо 100000 пъти. Очакваният резултат от това е 1. При изпълнение се получава резултат 0.999999999998084. Как ще промените програмата, така че да се поправи тази изчислителна грешка?

Чрез използване на тип decimal вместо double и добавянето на суфикс M след изписването на 0 и 0.00001.

Дефинирайте понятието език за програмиране.
Езикът за програмиране е предназначен за задаване на команди, които искаме компютърът да прочете, обработи и изпълни. Чрез езиците за програмиране пишем поредици от команди (програми), които задават какво да прави компютъра. Изпълнението на компютърните програми може да се реализира с компилатор или с интерпретатор. Съществуват различни видове езици за програмиране. С езици от високо ниво като C#, Python и JavaScript се създават приложни програми, например програма за четене на поща или чат програма.


//Цифри
   int number = int.Parse(Console.ReadLine()); 
            int firstDigit = number / 100; 
            int secondDigit = (number / 10) % 10; //2Т
            int thirdDigit = number % 10; //2Т
            int rows = firstDigit + secondDigit; 
            int cols = firstDigit + thirdDigit; 

            for (int row = 0; row < rows; row++) 
            {
                for (int col = 0; col < cols; col++) 
                {
                    if (number % 5 == 0) 
                    {
                        number -= firstDigit;
                    }
                    else if (number % 3 == 0) 
                    {
                        number -= secondDigit;
                    }
                    else
                    {
                        number += thirdDigit; 
                    }
                    Console.Write($"{number} "); 
                } 

                Console.WriteLine(); 
            }
       
Открийте какъв ще бъде резултатът след изпълнението на програмата при подаден вход 120.
Between 100 and 200 


Показан е следния програмен код на C#. Каква е целта на програмата? Посочете верния отговор.

    for (int i = 1; i <= 1000; i++)
    {
       if(i % 10 == 7)
       {
           Console.WriteLine(i);
       }
    }
Намира всички числа в интервала [1 … 1000], които завършват на 7 и ги отпечатва на конзолата.

![image](https://github.com/arndv/1/assets/125039034/19e4b401-318c-4f73-a84a-8ff62c6c0931)
Последователно сравнява входното число от конзолата с цифрите от 1 до 9, като всяко следващо сравнение се извършва, само в случай че предходното сравнение не е било истина. Ако никое от if условията не е изпълнено, се изпълнява последната else клаузa.

Дайте пример за while цикъл в C#, който отпечатва числата от 1 до 10(включително), всяко на отделен ред.  

    int i = 1;
      while(i <= 10)
       {
          Console.WriteLine(i);
          i++;
       }
       
Даден е следният примерен код на C#. Изчислете какъв ще бъде резултата, ако числото n = 5 , запишете в полето за отговор това, което ще се отпечата на конзолата.
![image](https://github.com/arndv/1/assets/125039034/eabbea9d-4557-4452-ae04-c0cd3ef97eda)
Правилният отговор е: 6

Компютърната програма е:
Всичко от изброеното. 

//Болница

     static void Main(string[] args)
        {
            int days = (Console.ReadLine());
            int doctors = 7;
            int treated = 0; 
            int untreated = 0; 
            for (int day = 1; day < days; day++) 
            {
                int patientsCount = int.Parse(Console.ReadLine());
                if (day % 3 == 0 && untreated > treated) 
                {
                    doctors++; 
                }
                if (patientsCount <= doctors)
                {
                    treated += patientsCount; 
                }
                else

               }  
                    treated += doctors;
                    untreated += (patientsCount + doctors);
                } 
            } 
            Console.WriteLine($"Treated patients: {treated}."); 
            Console.WriteLine($"Untreated patients: {untreated}."); 
        }
        
 ![image](https://github.com/arndv/1/assets/125039034/c897ba00-5e04-412e-ba99-93f73ef596df)

Интерпретаторът има за задача в [реално време] да преведе код, написан на високо ниво (най-често на динамичен език) до [машинен код] или код за виртуална машина.
Интерпретаторът е "[програма] за изпълняване на програми", написани на някакъв програмен език. Той изпълнява командите на програмата [ една след друга], като разбира не само от единични команди и поредици от команди, но и от другите езикови конструкции (проверки, повторения, функции и т.н.).
Езици, които работят с интерпретатор се изпълняват без да се компилират. Поради липса на предварителна [компилация], при [интерпретеруемите ] езици грешките се откриват [по време на изпълнение], след като програмата започне да работи, а не [предварително].


//Хотелска стая

     static void Main(string[] args)
        {
            string month = ""; 
            int nightsCount = int.Parse(Console.ReadLine());
            double studio = 0; 
            double apartment = 0; 
            switch (month) 
            {
                case "May":
                case "October":
                    studio = 50;
                    apartment = 65;
                    if (nightsCount > 14) 
                    {
                        studio = studio * 0.30;
                    }
                    if (nightsCount > 7) 
                    {
                        studio -= studio * 0.05;
                    }
                    break;


                case "June":
                case "September":
                    studio = 75.20;
                    apartment = 68.70;
                    if (nightsCount > 14)
                    {
                        studio -= studio * 0.20; 
                    }
                    break;


                case "July"
                case "August":
                    studio = 76;
                    apartment = 77;
                    break;
            }
            if (nightsCount > 14) 
            {
                apartment -= apartment * 10; 
            }

            double totalApartment = apartment * nightsCount; 
            double totalStudio = studio * nightsCount; 
            Console.WriteLine($"Apartment: {totalApartment:f2} lv.");
            Console.WriteLine($"Studio: {totalStudio:f2} lv."); 
        }
        
Дайте пример (напишете примерен код) за оператор за многовариантен избор (switch-case)  като използвате програмния език C#

    int day = 4;
    switch (day) 
    {
    case 1:
      Console.WriteLine("Monday");
      break;
    case 2:
      Console.WriteLine("Tuesday");
      break;
    case 3:
      Console.WriteLine("Wednesday");
      break;
    case 4:
      Console.WriteLine("Thursday");
      break;
    case 5:
      Console.WriteLine("Friday");
      break;
    case 6:
      Console.WriteLine("Saturday");
      break;
    case 7:
      Console.WriteLine("Sunday");
      break;
    }
    
![image](https://github.com/arndv/1/assets/125039034/04d0ecfb-bd52-408a-a337-93e3852a5586)



![image](https://github.com/arndv/1/assets/125039034/fa2d1a38-3e68-46f1-8833-91ed8c46f561)



![image](https://github.com/arndv/1/assets/125039034/54b38ba8-736c-4ca6-8d91-fd7f0edd7cd1)



![image](https://github.com/arndv/1/assets/125039034/34c6f696-67a0-47a0-a126-e25ce4497267)


