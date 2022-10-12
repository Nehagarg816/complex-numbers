# complex-numbers
This is a program for algebra on complex numbers using classes and objects in C++ OOPs


#include <stdio.h>
#include <iostream>
using namespace std;

class complex
{
private:
    int a;
    int b;

public:
    void setcomplex(int v1, int v2);
    void getcomplex(complex a1, complex a2);
    void getmultiComplex(complex b1, complex b2);
    void printmultiComplex();
    void printsumComplex();
    void printcomplex();
};

void complex::setcomplex(int v1, int v2)
{
    a = v1;
    b = v2;
}

void complex::getcomplex(complex a1, complex a2)
{
    a = a1.a + a2.a;
    b = a1.b + a2.b;
}

void complex::printsumComplex()
{
    std::cout << "Sum of given complex numbers is " << a << "+" << b << "i" << std::endl;
}

void complex::printcomplex()
{
    std::cout << "The given complex number is " << a << "+" << b << "i" << std::endl;
}

void complex::getmultiComplex(complex b1, complex b2)
{
    a = (b1.a * b2.a) - (b1.b * b2.b);
    b = (b1.a * b2.b) + (b1.b * b2.a);
}

void complex::printmultiComplex()
{
    std::cout << "Multiplication of given complex number is " << a << "+" << b << "i" << std::endl;
}

int main()
{
    complex c1, c2, c3;
    c1.setcomplex(2, 4);
    c1.printcomplex();

    c2.setcomplex(3, 6);
    c2.printcomplex();

    c3.getcomplex(c1, c2);
    c3.printsumComplex();
    c3.getmultiComplex(c1, c2);
    c3.printmultiComplex();

    return 0;
}
