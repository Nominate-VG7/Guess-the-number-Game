//# Guess-the-number-Game
//It's a guess the number game . you have to guess the number between 1 to 100 until you guess it right.

#include <stdio.h>
#include <stdlib.h>
#include <time.h>

int main()
{
    int number, guess, nguesses=0;
    srand(time(0));
    number = rand() % 100 + 1;

    do{
        printf("Guess the number between 1 to 100:\n");
        scanf("%d", &guess);
        nguesses++;
        if(guess > number) {
            printf("lower number please\n");
        }
        else if(guess < number) {
            printf("higher number please\n");
        }
        else {
            printf("you have guessed in %d attempts\n", nguesses);
        }
        
    } while(guess != number);
    return 0;
}
