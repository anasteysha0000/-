# -
пз2 (Переверткина Анастасия М3О-121Б-21)
#include <iostream>
int main()
{
    int32_t chislo, chislo1, stepen, count, rez, i;
    std::cin >> chislo;
    stepen = 1;
    count = 0;
    chislo1 = chislo;
    while (chislo1 != 0){
        count++;
        stepen *= 10;
        chislo1 /= 10;
    }
    i = chislo;

    for (count;count>=0;count--){
        stepen = stepen/10;
        rez = (i/stepen);
        i = i % stepen;
        if (rez == 0){}
        else{
            if (count > 1 and count !=0 and i > 0){
                std::cout << rez << "*10^" << count-1 << "+";
            }
            else{
                std::cout << rez << "*10^" << count-1;
            }
    }}
}
