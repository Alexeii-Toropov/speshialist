m1:
Console.WriteLine("Введите кол-во элементов массива");
int number = 0;
try
{
    number = Convert.ToInt32(Console.ReadLine());
}
catch
{
    Console.WriteLine("Введены некорректные данные (нужно вводить числа)");
    goto m1;
}

string[] mas = new string[number];
string[] res = new string[number];

for (int i = 0; i < number; i++)
{
    Console.WriteLine("mas[{0}]", i + 1);
    mas[i] = Console.ReadLine();
}

Console.WriteLine("Начальный массив: ");
for (int i = 0; i < number; i++)
{
    Console.Write(mas[i] + " ");
}

string str = "";

for (int i = 0; i < number; i++)
{
    str = mas[i];

    if (str.Length <= 3)
    {
        res[i] = str;
    }
}

Console.WriteLine(" ");
Console.WriteLine("Конечный массив: ");
for (int i = 0; i < number; i++)
{
    Console.Write(res[i] + " ");
}
