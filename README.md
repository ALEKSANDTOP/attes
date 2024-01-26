/*Задача: Написать программу, которая из имеющегося массива строк формирует новый массив из строк, длина которых меньше, либо равна 3 символам. 
Примеры:
[“Hello”, “2”, “world”, “:-)”] → [“2”, “:-)”]
[“1234”, “1567”, “-2”, “computer science”] → [“-2”]
[“Russia”, “Denmark”, “Kazan”] → []*/

string [] GenArray (int size)
{
    string [] array = new string [size];
    Console.Write($"Введите {size} значений: ");
    for (int i = 0; i < array.Length; i++)
    {
        array[i] = Console.ReadLine();
    }
    return array;
}
void ConcArray(string [] array)
{
    for (int i = 0; i < array.Length; i++)
    {
        Console.Write( array[i] + " " );
    }
}
string [] SortingArray (string [] array, int size)
{
    string [] sortArray = new string [size];
    int j = 0;
    for (int i = 0; i < array.Length; i++)
    {
        if(array[i].Length <= 3 )
        {
              sortArray[j] = array[i];
              j++;
        }
    }
    return sortArray;
}
Console.WriteLine("Введите размер массива: ");
int size = Convert.ToInt32(Console.ReadLine());
string [] strArray = GenArray(size);
string [] array = SortingArray(strArray, size);
ConcArray(array);