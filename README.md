# Шаблонный класс полиномов
Создать шаблонный класс полиномов, чтобы в качеcтве коэффициентов полинома помимо простых типов (int, double), могли выступать комплексные числа (std::complex), и [кватернионы](https://ru.wikipedia.org/wiki/%D0%9A%D0%B2%D0%B0%D1%82%D0%B5%D1%80%D0%BD%D0%B8%D0%BE%D0%BD), которые надо реализовать в классе Quat.

Возможные операции с полиномами - сложение, вычитание, умножение.

## Входные данные:
Входные данные задаются непосредственно в программе.
Коэффициенты полинома хранятся в std::vector по возрастающим степеням полинома начиная со свободного члена. 
Пример для простых типов
```
std::vector<double> vd {1., 2., 3.}; // 1 + 2*x + 3*x^2
```
Пример для std::complex
```
std::vector<std::complex<double>> vc {{1., 2.}, {3., 4.}, {5., 6.}}; 
// где {1.,2.} вещественная и мнимая часть
```
Пример для класса Quat
```
std::vector<Quat> vq {{1., 2., 3., 4.}, {5., 6., 7., 8.}}; 
// где {1., 2., 3., 4.} четыре числа, задающие кватернион
```

## Пример вывода для трех типов полиномов:
Исходные полиномы соответствующих типов заданы в файле main.cpp. \
Для каждой пары приведено три операции: +, -, *.

```
Simple polynoms:
3 + 7*x + 9*x^2 + 4*x^3
-1 - 3*x - 3*x^2 + 4*x^3
2 + 9*x + 22*x^2 + 35*x^3 + 38*x^4 + 24*x^5

Complex polynoms:
(3 + 6j) + (9 + 12j)*x + (15 + 18j)*x^2 + (-10 + 14j)*x^3
(-1 + -2j) + (-3 + -4j)*x + (-5 + -6j)*x^2 + (10 + -14j)*x^3
(-6 + 8j) + (-20 + 40j)*x + (-42 + 112j)*x^2 + (-74 + 146j)*x^3 + (-108 + 122j)*x^4 + (-134 + 10j)*x^5

Quaternion polynoms:
(3 + 6*i + 9*j + 12*k) + (15 + 18*i + 21*j + 24*k)*x
(-1 + -2*i + -3*j + -4*k) + (-5 + -6*i + -7*j + -8*k)*x
(-56 + 8*i + 12*j + 16*k) + (-240 + 64*i + 88*j + 112*k)*x + (-248 + 120*i + 140*j + 160*k)*x^2
```