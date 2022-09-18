# DZ_Seminar_8

// Задача 54: Задайте двумерный массив. Напишите программу, которая упорядочит по убыванию элементы каждой строки двумерного массива.
// Например, задан массив:
// 1 4 7 2
// 5 9 2 3
// 8 4 2 4
// В итоге получается вот такой массив:
// 7 4 2 1
// 9 5 3 2
// 8 4 4 2

// void FillArray(int[,] matr)
//  {
//      for (int m = 0; m < matr.GetLength(0); m++)
//      {
//          for (int n = 0; n < matr.GetLength(1); n++)
//          {
//              matr[m, n] = new Random().Next(1, 10);
//          }
//      }
//  }

//  void PrintArray(int[,] matr)
//  {
//      for (int m = 0; m < matr.GetLength(0); m++)
//      {
//          for (int n = 0; n < matr.GetLength(1); n++)
//          {
//              Console.Write(matr[m, n] + " ");
//          }
//          Console.WriteLine();
//      }
//  }

//  void Ordering(int[,] matr)
//  {
//      for (int m = 0; m < matr.GetLength(0); m++)
//      {
//          for (int n = 0; n < matr.GetLength(1); n++)
//          {
//              for (int k = 0; k < matr.GetLength(1) - n - 1; k++)
//              {
//                  if (matr[m, k] < matr[m, k + 1])
//                  {
//                      int t = matr[m, k];
//                      matr[m, k] = matr[m, k + 1];
//                      matr[m, k + 1] = t;
//                  }
//              }
//          }
//      }
//  }

//  int[,] matrix = new int[5, 5];
//  FillArray(matrix);
//  PrintArray(matrix);
//  Console.WriteLine();
//  Ordering(matrix);
//  PrintArray(matrix);

// Задача 56: Задайте прямоугольный двумерный массив. Напишите программу, которая будет находить строку с наименьшей суммой элементов.
// Например, задан массив:
// 1 4 7 2
// 5 9 2 3
// 8 4 2 4
// 5 2 6 7
// Программа считает сумму элементов в каждой строке и выдаёт номер строки с наименьшей суммой элементов: 1 строка

// void FillArray(int[,] matr)
//  {
//      for (int m = 0; m < matr.GetLength(0); m++)
//      {
//          for (int n = 0; n < matr.GetLength(1); n++)
//          {
//              matr[m, n] = new Random().Next(1, 10);
//          }
//      }
//  }
//  void PrintArray(int[,] matr)
//  {
//      for (int m = 0; m < matr.GetLength(0); m++)
//      {
//          for (int n = 0; n < matr.GetLength(1); n++)
//          {
//              Console.Write(matr[m, n] + " ");
//          }
//          Console.WriteLine();
//      }
//  }
//  int Sum(int[,] matr)
//  {
//      int sum = 0;
//      int minSum = 0;
//      int minNum = 0;
//      for (int m = 0; m < matr.GetLength(0); m++)
//      {
//          for (int n = 0; n < matr.GetLength(1); n++)
//          {
//              if (m == 0) 
//              {
//                  sum += matr[m, n];
//                  minSum += matr[m, n]; 
//              }
//              else sum += matr[m, n]; 
//          }
//          if (sum < minSum)
//          {
//              minSum = sum;
//              minNum = m;
//          }
//          sum = 0;
//      }
//      return minNum;
//  }
//  int[,] matrix = new int[4, 4];

//  FillArray(matrix);
//  PrintArray(matrix);
//  Console.WriteLine($"Cтрока с наименьшей суммой элементов: " + Sum(matrix)  + " строка (по номеру индекса)");


// Задача 58: Задайте две матрицы. Напишите программу, которая будет находить произведение двух матриц.
// Например, даны 2 матрицы:
// 2 4 | 3 4
// 3 2 | 3 3
// Результирующая матрица будет:
// 18 20
// 15 18

// void FillArray(int[,] matr, int[,] matr1)
//  {
//      for (int m = 0; m < matr.GetLength(0); m++)
//      {
//          for (int n = 0; n < matr.GetLength(1); n++)
//          {
//              matr[m, n] = new Random().Next(1, 10);
//          }
//      }
//      for (int m = 0; m < matr1.GetLength(0); m++)
//      {
//          for (int n = 0; n < matr1.GetLength(1); n++)
//          {
//              matr1[m, n] = new Random().Next(1, 10);
//          }
//      }
//  }
//  void PrintArray(int[,] matr, int[,] matr1)
//  {
//      for (int m = 0; m < matr.GetLength(0); m++)
//      {
//          for (int n = 0; n < matr.GetLength(1); n++)
//          {
//              Console.Write(matr[m, n] + " ");
//          }
//          Console.WriteLine();
//      }
//      Console.WriteLine();
//      for (int m = 0; m < matr1.GetLength(0); m++)
//      {
//          for (int n = 0; n < matr1.GetLength(1); n++)
//          {
//              Console.Write(matr1[m, n] + " ");
//          }
//          Console.WriteLine();
//      }
//  }
//  void Composition(int[,] matr, int[,] matr1, int[,] compMatr)
//  {
//      for (int m = 0; m < matr.GetLength(0); m++)
//      {
//          for (int n = 0; n < matr.GetLength(1); n++)
//          {
//              compMatr[m, n] = matr[m, n] * matr1[m, n];
//          }
//      }
//  }
//  void PrintCompArray(int[,] compMatr)
//  {
//      for (int m = 0; m < compMatr.GetLength(0); m++)
//      {
//          for (int n = 0; n < compMatr.GetLength(1); n++)
//          {
//              Console.Write(compMatr[m, n] + " ");
//          }
//          Console.WriteLine();
//      }
//  }

//  int[,] matrix = new int[2, 2];
//  int[,] matrix1 = new int[2, 2];
//  int[,] compMatrix = new int[2, 2];
//  FillArray(matrix, matrix1);
//  PrintArray(matrix, matrix1);
 
//  Console.WriteLine();
//  Composition(matrix, matrix1, compMatrix);
//  PrintCompArray(compMatrix);


// Задача 62. Напишите программу, которая заполнит спирально массив 4 на 4. 
// Например, на выходе получается вот такой массив:
// 01 02 03 04
// 12 13 14 05
// 11 16 15 06
// 10 09 08 07

// int[,] sqareMatrix = new int[4, 4];

// int t = 1;
// int m = 0;
// int n = 0;

// while (t <= sqareMatrix.GetLength(0) * sqareMatrix.GetLength(1))
// {
//   sqareMatrix[m, n] = t;
//   t++;
//   if (m <= n + 1 && m + n < sqareMatrix.GetLength(1) - 1)
//     n++;
//   else if (m < n && m + n >= sqareMatrix.GetLength(0) - 1)
//     m++;
//   else if (m >= n && m + n > sqareMatrix.GetLength(1) - 1)
//     n--;
//   else
//     m--;
// }

// WriteArray(sqareMatrix);

// void WriteArray (int[,] array)
// {
//   for (int m = 0; m < array.GetLength(0); m++)
//   {
//     for (int n = 0; n < array.GetLength(1); n++)
//     {
//       if (array[m,n] / 10 <= 0)
//       Console.Write($" {array[m,n]} ");

//       else Console.Write($"{array[m,n]} ");
//     }
//     Console.WriteLine();
//   }
// }