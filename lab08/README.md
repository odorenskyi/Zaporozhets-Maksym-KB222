# Лабораторна робота № 8

Тема Реалізация статичних бібліотек модулів лінійних обчислювальних процесів

Мета полягає у набутті ґрунтовних вмінь і практичних навичок застосування теоретичних положень методології модульного програмування, реалізації метода функціональної декомпозиції задач, метода модульного (блочного) тестування, представлення мовою програмування C++ даних скалярних типів, арифметичних і логічних операцій, потокового введення й виведення інформації, розроблення програмних модулів та засобів у кросплатформовому середовищі Code::Blocks (GNU GCC Compiler).

Завдання 1. Реалізувати статичну бібліотеку модулів libModulesПрізвище C/C++, яка містить функцію розв’язування задачі 8.1.
Задача 8.1 За значеннями x, y, z обчислюється S:
#include <iostream>
#include <Math.h>
#include <math.h>
#define _USE_MATH_DEFINES #include <cmath>
using namespace std; double first_function(double, double, double); int main()
{ double S, x, y, z;
double pi = M_PI; cout << "x="; cin >> x; cout << "y="; cin >> y; cout << "z="; cin >> z;
S = first_function(x,y,z); cout << S; return 0; } double first_function(double x, double y, double z){
if (x < 0){
std::cout << "";
} double S;
S = pow(x,2) - pow(y,3) + sqrt(abs(pow(z,2)* pow(M_E,x))/12*x+(pow(y,2)-
M_PI*sqrt(z))); return S;
}
2. Реалізувати програмне забезпечення розв’язування задачі 8.2 — консольний застосунок.
Задача 8.2 За послідовними запитами вводяться числа x, y, z та символи a і b. Вивести (включити у потік STL - cout)*:
8.2.1 Прізвище та ім’я розробника програми зі знаком охорони авторського права «©»
#include <iostream>
using namespace std;

void printAuthor() { int x, y, z; char a, b;

// Ввід чисел та символів
cout << "Введіть числа x, y, z: ";
cin >> x >> y >> z;

cout << "Введіть символи a та b: ";
cin >> a >> b;

// Виведення прізвища та імені автора
cout << "© Розробник програми: Запорожець Максим" << end1;
}
int main() { printAuthor(); 
return 0; }
8.2.2 Результат логічного виразу в числовому вигляді (1/0): a<=b-32 ?
#include <iostream>
int main() {
    int x, y, z;
    char a, b;
    // Введення чисел x, y, z та символів a і b
    std::cout << "Введіть число x: ";
    std::cin >> x;

    std::cout << "Введіть число y: ";
    std::cin >> y;

    std::cout << "Введіть число z: ";
    std::cin >> z;

    std::cout << "Введіть символ a: ";
    std::cin >> a;

    std::cout << "Введіть символ b: ";
    std::cin >> b;
    // Обчислення та виведення результату логічного виразу a <= b - 32
    int result = (a <= b - 32) ? 1 : 0;
    std::cout << "Результат виразу a <= b - 32: " << result << std::endl;
    return 0;}

8.2.3 Значення x, y, z в десятковій і шістнадцятковій системах числення; S, що обчислюється функцією s_calculation() Заголовкового файлу Modules.Прізвище.h
#include <iostream> #include <string> #include "modulesZaporozhets.h" 
using namespace std;
int main() { int x, y, z; 
char a, b; 
cout << "Enter x, y, z: "; 
cin >> x >> y >> z; 
cout << "x = " << x << " (hex: " << hex << x << ")" << endl; 
cout << "y = " << y << " (hex: " << hex << y << ")" << endl; 
cout << "z = " << z << " (hex: " << hex << z << ")" << endl; 
cout << "Enter a, b: "; 
cin >> a >> b; 
#ifndef MODULESZAPOROZHETS_H 
#define MODULESZAPOROZHETS_H
int s_calculation(int x, int y, int z, char a, char b) { // обчислення s за допомогою x, y, z, a та b
}
#endif // MODULESZAPOROZHETS_H
cout << "s = " << s << endl;
return 0;
}


Варіант № 4


Кропивницький | <a href="http://www.kntu.kr.ua/">ЦНТУ</a> | 2023
