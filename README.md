#Задачи с лабораторной
2 лаба
#include <iostream>
#import <cmath>
#//int main()
#//{
    #//float a = 0.5;
    #//float b = 0.5;
    #//double y = sqrt((pow(a, pow(sin(b), 2) + cos(pow(b, 3))) + cbrt(pow(b, 2))) / pow(fabs((a * tan(b)) / (1 - exp(sqrt(a)))), 1.0 / 4.0));
    #//std::cout << y << std::endl;
    #//return 0;
#}

Задача с 3 лабы (18)
#include <iostream>
#int main() {
    #int n;
    #std::cout << "Введите количество четырехугольников: ";
    #std::cin >> n;
    #int k1 = 0;
    #int k2 = 0;
    #for (int i = 1; i <= n; ++i) {
        #double a, b, c, d;
        #std::cout << "Введите стороны " << i << "- го четырехугольника: ";
        #std::cin >> a >> b >> c >> d;
        
        #if (a == c && b == d && a == b) {
            #k1 = k1 + 1;
        #} else if (a == c && b == d) {
            #k2 = k2 + 1;
        #}
    #}
    
    #std::cout << "РОМБОВ-" << k1 << " ПАРАЛЛЕЛОГРАММОВ-" << k2 << std::endl;
    #return 0;
#}
