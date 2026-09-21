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




#include <iostream>
#include <cmath>
int main()
{
	unsigned char  hours = 2;
	unsigned char minutes = 43;
	hours = hours % 12;
	float min_grrrr = minutes * 6;
	float housr_grrr = (hours * 30) + (minutes * 0.5);
	float diff = abs(housr_grrr - min_grrrr);
	float d = (diff > 180) ? 360.0 - diff : diff;
	printf("diff = %.1f\n", diff);
	return 0;
}


#include <iostream>
#include <stdio.h>

int main()

{
	int r, k;
	setlocale(LC_ALL, "RUS");
	printf(" рубли копейки: ");
	scanf_s("%d %d",&r, &k);
	unsigned long long money = r * 100 + k;
	unsigned long long mgr_money = money;
	int bstep = 0;
	int s = 0;
	do {
		money = money - 29;
		money = (money % 100) * 100 + (money / 100);
		money > mgr_money ? (mgr_money = money, bstep = s) : 0;
		s++;
	} while (s <= 100);
	printf("%d\n", bstep);
	return 0;
}
#include <stdio.h> #include <math.h> #include <locale.h>
int main() { setlocale(LC_ALL, "Russian"); int nachal; unsigned short hod = 0, max = 0, optimal_hod = 0, summa; do { printf("Введите начальную сумму в копейках: "); scanf_s("%d", &nachal); } while (nachal < 0 || nachal >= 10000);
summa = nachal;
max = summa;
if (summa >= 29)
    do {
        hod++;
        summa -= 29;
        summa = summa % 100 * 100 + summa / 100;
        if (summa > max) {
            max = summa;
            optimal_hod = hod;
        }
    } while (summa >= 29 && summa != nachal);
printf("%d-%d-%d", nachal, max, optimal_hod);
}
