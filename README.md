#include <stdio.h>
#include <stdlib.h>
#include <time.h>
int main()
{
    int random, guess;
    int no_of_guess;
    srand(time(NULL));

    printf("Welcome to the world of Guessing Number.\n");
    random = rand() % 100 + 1; // Generating between 0 to 100;

    printf("Number generates is:%d",random);

    do
    {
        printf("\nPlease enter your Guess between(1 to 100):");
        scanf("%d", &guess);
        no_of_guess++;

        if (guess < random)
        {
            printf("Guess a larger number\n");
        }
        else if (guess > random)
        {
            printf("Guess a smaller number\n");
        }
        else
        {
            printf("Congratulations !!You have sucessfully guessed the nummber in %d attempt", no_of_guess);
        }

    } while (guess != random);

    printf("\n Bye Bye,Thanks for playing");

    printf("\n Developed by:Rudra Sonvane");

    return 0;
}
