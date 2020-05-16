# FirstTP

#include <stdio.h>
#include <time.h>
#include <stdlib.h>

// FIN DES DIRECTIVES PREPROCESSEURS //

                            /////////////////////////////////// DEBUT DU MAIN /////////////////////////////////////////////
                            ///////////////////////////////////     HAEYX     ////////////////////////////////////////////

int main(int argc, char* argv[])
{

    // 0 // CI DESSOUS CE SONT LES TYPES ET VARIABLES DE MON CODAGE /// 0 ///
  
    int NombreMystere = 0, NombreEntrer = 0;
    int NombreDeCoups = 0, Mode = 0;
    int TryAgain = 1;
    int MAX = 0, MIN = 1;

  



    // 0 // FIN DES TYPES ET VARIABLES // 0 //

    // 1 // L'INTRODUCTION A MON JEU PLUS OU MOINS ET SES FONCTIONNEMENT // 1 //

    printf("Bonjour je suis HAEYX ! Bienvenue dans mon premier jeu PLUS OU MOINS !\n\n");
    printf("Le but du jeu est simple, il suffit de trouver le nombre generer automatiquement par l'ordinateur !\n");
    printf("\n\n");
    // 1 //          FIN DE L'INTRODUCTION DU JEU PLUS OU MOINS         // 1 //

    do // CETTE BOUCLE PERMET DE RELANCER LE JEU //
    {
        int MAX = 0, MIN = 1;
        int NombreDeCoups = 0, Mode = 0;
        int NombreMystere = 0, NombreEntrer = 0;

    printf("*IMPORTANT* VEUILLEZ BIEN ECRIRE LES INSTRUCTIONS UNIQUEMENT AVEC DES CHIFFRES !!\n\n");
  
    ////         CHOIX DU MODE DE JEU       ////

    printf("Quel mode de jeu souhaiter vous ?\n");
    printf("------------------------------\n\n");
    printf("Mode 1 joueur  : 1 \n\n");
    printf("Mode 2 joueur  : 2 \n\n");
    printf("------------------------------\n");
    printf("\n");
    do
    {
        scanf_s("%d%s",&Mode);

        switch (Mode)
        {
            ///////////////////////////////////////////////
        case 1:
            printf("Vous avez choisit le mode SOLO \n\n");
            Mode = 100;
            break;
            //////////////////////////////////////////////
        case 2:
            printf("Vous avez choisit le mode DUO \n\n");
            Mode = 200;
            break;
            //////////////////////////////////////////////
        default:
            Mode = 0;
            printf("Je n'ai pas compris votre saisit \n");
            printf("Veuillez choisir le mode 1 ou le mode 2 \n");
            break;
        }
    } while (Mode < 10);
     
     ////     FIN CHOIX DU JEU     ////

    // 2 //       INDICATION DU NIVEAU DE JEU    // 2 //

    printf("Voici les differents niveaux : Choisissez de 1 a 5 \n\n");
    printf("------------------------------------------------------------------------------- \n\n");
    printf("| Niveau 1 | Nombres entre 1 - 100  | TRES FACILE      | Nombres de coups a battre : 10 | \n\n");
    printf("| Niveau 2 | Nombres entre 1 - 200  | FACILE           | Nombres de coups a battre : 9  | \n\n");
    printf("| Niveau 3 | Nombres entre 1 - 500  | DIFFICILE        | Nombres de coups a battre : 8  | \n\n");
    printf("| Niveau 4 | Nombres entre 1 - 1500 | TRES DIFFICILE   | Nombres de coups a battre : 7  | \n\n");
    printf("| Niveau 5 | Nombres entre 1 - 5000 | EXTREME          | Nombres de coups a battre : 6  | \n\n");
    printf("------------------------------------------------------------------------------- \n\n");

    // 2 //  FIN D'INDICATION DES NIVEAUX DE JEU // 2 //

    // 3 // DEBUT DE LA BOUCLE DO WHILE  // ON DEMANDE LE NIVEAU DE JEU A L'UTILISATEUR AVEC UNE BOUCLE DO WHILE ET UN SCANF_S   // 3 //
    do
    {
        printf("Quel niveau voulez vous choisir ?\n");
        scanf_s("%d", &MAX);

        switch (MAX)
        {
            ///////////////////////////////////////////
        case 1:
            MAX = 100;
            printf("-------------------------------------\n\n");
            printf("Vous avez choisit le niveau 1 :      \n\n");
            printf("Le nombre mystere sera de 1 a %d \n\n", MAX);
            printf("-------------------------------------\n\n");
            break;
            ///////////////////////////////////////////
        case 2:
            MAX = 200;
            printf("-------------------------------------\n\n");
            printf("Vous avez choisit le niveau 2 :        \n");
            printf("Le nombre mystere sera de 1 a %d \n\n", MAX);
            printf("-------------------------------------\n\n");
            break;
            //////////////////////////////////////////
        case 3:
            MAX = 500;
            printf("-------------------------------------\n\n");
            printf("Vous avez choisit le niveau 3 :         \n");
            printf("Le nombre mystere sera de 1 a %d \n\n", MAX);
            printf("-------------------------------------\n\n");
            break;
            //////////////////////////////////////////
        case 4:
            MAX = 1500;
            printf("-------------------------------------\n\n");
            printf("Vous avez choisit le niveau 4 :        \n");
            printf("Le nombre mystere sera de 1 a %d \n\n", MAX);
            printf("-------------------------------------\n\n");
            break;
            //////////////////////////////////////////
        case 5:
            MAX = 5000;
            printf("-------------------------------------\n\n");
            printf("Vous avez choisit le niveau 5 :        \n");
            printf("Le nombre mystere sera de 1 a %d\n\n", MAX);
            printf("-------------------------------------\n\n");
            break;
            //////////////////////////////////////////
        default:
            printf("Je n'ai pas compris votre choix, Veuillez choisir entre 1 et 5 !\n\n");
            MAX = 0;
            break;
            //////////////////////////////////////////
        }
    } while (MAX < 10);

    // 3 //                                        FIN DE LA BOUCLE DO WHILE SELECTION DU NIVEAU DE JEU                                // 3 //

      /// 4 /// GENERATEUR AUTOMATIQUE DU NOMBRE MYSTERE /// 4 ///
    
    if (Mode <= 100)
    { 

    srand(time(NULL));
    NombreMystere = (rand() % (MAX - MIN + 1)) + MIN;

    }

    if (Mode >= 200)
    {
        printf("**COMMANDE UNIQUEMENT POUR LE JOUEUR 2**\n");
        printf("Joueur 2\n\n Quel nombre voulez vous choisir ?\n");
        scanf_s("%d", &NombreMystere);
        printf("\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n");
        printf("Le Joueur 2 a choisit son nombre \n");

    }


    /// 4 /// FIN DU GENERATEUR ALEATOIRE DU NOMBRES MYSTERE /// 4 ///

    printf(" Maintenant le jeu peux commencer !\n\n");
    printf(" C'est partit ! \n\n");
    printf("\n\n");

    // 5 // DEBUT DU JEU // 5 //
    do {

        printf("Quel est le nombres ? : ");
        scanf_s("%d", &NombreEntrer);

        if (NombreEntrer != NombreMystere);
        {NombreDeCoups++; };

        if (NombreMystere > NombreEntrer)
            printf("Le nombre est plus grand !!\n\n ");

        if (NombreMystere < NombreEntrer)
            printf("Le nombre est plus petit !!\n\n");

    } while (NombreMystere != NombreEntrer);

    printf("\n\n");
    printf("!!! BRAVO TU AS TROUVE LE NOMBRE MYSTERE EN ( %d ) COUPS BIEN JOUE !!!", NombreDeCoups);

    printf("\n\n\n");

 

 
    printf("Souhaiter vous faire une autre partie ?\n\n");
    printf("OUI = 1 || NON = 0\n\n");
    scanf_s("%d", &TryAgain);
    
    if(TryAgain == 1)
    {
        printf("\n\n\n\n\n\n\n\n\n");
        printf("LET'S GOOO !!\n\n");

    }


  }while (TryAgain == 1 );

  printf("TRES BIEN !!\n\n ");
  printf("MERCI D'AVOIR PRIT LE TEMPS DE JOUER AVEC MOI\n AU REVOIR !!");

  printf("\n\n");

  printf("REALISER PAR HAEYX");



                                                                    // 5 // FIN DU JEU // 5 //

    printf("\n\n\n\n");



    return 0;






}

//////////////////////////////////////////// FIN DU MAIN ///////////////////////////////////////////////
                                ////////////    HAEYX    ////////////
