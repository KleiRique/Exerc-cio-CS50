# Exerc-cio-CS50
Laboratório 1: crescimento populacional

#include <stdio.h>
#include <math.h>
#include <cs50.h>

int main(void)
{
    // Solicite o valor inicial ao usuário
    int start;
    do
    {
        start = get_int("Insert initional population size (bigger than 9): ");
    }
    while (start < 9);
    {
        printf("Start size: %i\n", start);
    }
    // Solicite o valor final ao usuário
    int end;
    do
    {
        end = get_int("Insert end populiaton size (bigger than initional): ");
    }
    while (end < start);
    {
        printf("End size: %i\n", end);
    }
    // Calcule o número de anos até o limite
    int year = 0;
    while (start < end)
    {
        start = start + (start / 3) - (start / 4);
        year++;
    }
    // Imprima o número de anos
    {
        printf("Years: %i\n", year);
    }
}
