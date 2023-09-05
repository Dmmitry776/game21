# game21
Учебный командный проект игра 21(BlackJack)
1.Создали основной минимальный функционал.
2.Создали список литер с сообщениями, которые выдаются на консоль.
3.Написали функцию генерации случайного числа gen_chislo().
4.Написали функцию суммирования выданных системой чисел. summ_chislo().
5.Написали перегруженную функцию print() для вывода информации на консоль.
6.Написали функцию check_num(), которая проверяет полученный результат на
 соответствие числу 21.
7. Улучшили логику работы функции rand().
8. Необходимо написать логику работы второго играка, который будет виртуальным.
9. Необходимо написать функцию сравнивающую результаты игрока и компьютера.
10.Необходимо расширить список литер для фраз выдаваемых виртуальному игроку.
11.Изменение логики виртуального игрока на второго реального.
12.Переписать логику функции gen_chislo() так чтобы использовался do_while().
13.Не должны вводиться никакие символы кроме y и n.

14.Логика виртуального игрока:
    выдача числа.
    суммирование чисел.
    сравнение суммы с числом 21.
    вывод информации на консоль.
    логика выбора остановки или продолжения игры.
    замедление работы функций виртуального игрока для 
    создания эффекта реального игрока

15.Продумать хранение данных в игре.
16.Изменить логику функции summ_chislo(), чтобы функция возвращала сумму из вектора.
17.Создать графическое оформление.

void summ_comp_num(vector<int> & summ_comp, int & sum_vec_comp);
void gen_chislo_comp(vector<int> & summ_game_comp, int & sum_vec_comp);
void summ_comp_num(vector<int> & summ_comp, int & sum_vec_comp)
{
    sum_vec_comp = 0;
    for(int number : summ_comp)
    {
        sum_vec_comp += number;
    }
}//Эта функция суммирует числа компьютера в векторе.

void gen_chislo_comp(vector<int> & summ_game_comp, int & sum_vec_comp)
{
    int rand_chislo_comp = 0; // получает рандомное число
    for(int i = 0; i < 4; i++)
    {
        rand_chislo_comp = 2 + rand()%13;
        summ_game_comp.push_back(rand_chislo_comp);
        print(liter::comp_number, rand_chislo_comp);// вывод фразы "Your number is" и числа
        Sleep(500);
        //print(liter::comp_summ_numbers, sum_vec_comp); //вывод фразы "Your summ numbers is" и общей суммы
    }
}