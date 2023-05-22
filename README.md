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

//digit

         int number = int.Parse(Console.ReadLine()); 
            int firstDigit = number / 100; 
            int secondDigit = (number / 10) % 10; 
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
        
        
        
