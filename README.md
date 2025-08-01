#include <stdio.h>
#include <stdlib.h>
#include <time.h>

int main() {
    int nombreMystere, nombreUtilisateur, coups = 0;

    // Initialisation du générateur de nombres aléatoires
    srand(time(NULL));
    nombreMystere = (rand() % 100) + 1; // entre 1 et 100

    printf("=== Jeu du Nombre Mystère ===\n");
    printf("Devine le nombre entre 1 et 100 !\n");

    do {
        printf ("Entre un nombre : ");
        scanf("%d", &nombreUtilisateur);
        coups++;

        if (nombreUtilisateur < nombreMystere) {
            printf("C'est plus !\n");
        } else if (nombreUtilisateur > nombreMystere) {
            printf("C'est moins !\n");
        } else {
            printf("Bravo ! Tu as trouvé en %d coup(s) !\n", coups);
        }

    } while (nombreUtilisateur != nombreMystere);

    return 0;
}
