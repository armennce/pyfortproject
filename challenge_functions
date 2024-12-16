#armence
import random

def challenge_function():
    challenges = [chance_challenge(), shell_game()] # liste des fonctions challenge

    #choisir un défi aléatoirement
    challenge = random.choice(challenges)

    #on appelle la fonction sélectionnée
    res = challenge
    print("You'll play to {res}.")

def chance_challenge():
    #message de bienvenu pour les chance_challenge
    print("Welcome to the chamber of chance !")
    print("Here you'll be able to try two ")
    print("chance challenges. The shell-challenge")
    print("or the the rolling dice. ")

def shell_game():

    list_shell = ['A', 'B', 'C'] #liste des coquillages
    max_attempts = 2 # maximum essais
    attempts = 0 #compteur essais

    # étape 2 --> on affiche le message de bienvenu + règles du jeu
    print("You will play the shell- game !")
    print("I will hide a key under one of ")
    print(" the three shells. You will have ")
    print("three two attempts. If you find ")
    print("the key, you can take it. But if ")
    print("you don't, I will keep it. ")

    #étape 3 --> on fait une boucle selon le nombre de tentatives
    while attempts < max_attempts:
        #on choisit aléatoirement un coquillage où cacher la clé
        hidden_shell = random.choice(list_shell)

        #étape 4 --> on affiche le nombre d'attempts restants, il va incrémenter au fil du jeu
        print("Tentative {attempt + 1}/{max_attempts}.")
        print("Coquilles disponibles : A, B, C")

        #étape 5 --> on demande au joueur de choisir un coquillage
        player_choice = input("Chose a shell between A, B or C").strip().upper()

        #étape 6 --> on vérifie si le choix est valide
        #on vérifie direct que le choix du joueur soit dans la liste de coquillage donnée
        if player_choice in list_shell:
            #cas 1 --> si le choix du joueur est égal à celui du hidden_shell
            if player_choice == hidden_shell:
                print("Congratulations ! You found the key! ")
                return True  # Le joueur a gagné
            else:
                print("Too bad... The key isn't here :/")
        else:
            #cas 2 --> si le choix de l'utilisateur n'est pas valide
            print("Ahhh too bad ... Your answer is not valid :/")
        #étape 7 --> on incrémente le nombre d'essai
        attempts +=1
    #étape 8 --> si le nombre de tentatives est épuisé
    print("\nVous avez utilisé toutes vos tentatives.")
    print("La clé se trouvait sous la coquille : {hidden_shell}.")
    return False  # Le joueur a perdu

def roll_dice_game():
    max_attemps = 3
    attempts = 0

    #message de bienvenu au challenge + règles du jeu
    print("Welcome to the rolling dice game ! ")
    print("The aime of this game is simple: the")
    print("first one to get a six with his dices")
    print("wins. If you win, you'll get a key. If")
    print("you don't, I'll keep it. ")

    #étape 1 --> on lance la boucle
    while attempts < max_attemps:
        print(("Tentative {attempt + 1}/{max_attempts}.").strip().upper())
        #étape 2 --> on demande au joueur de lancer les dés
        #print(input("press Enter"))
        # étape 3 --> on génère aléatoirement deux chiffres pour le joueur
        player_dice = (random.randint(1, 6), random.randint(1, 6))
        print("You obtained : {player_dice[0]} et {player_dice[1]}")

        #étape 4 --> checker si le joueur à obtenu un 6
        if 6 in player_dice:
            print("Congratulations, you got a 6 !")
            print("You can have the key ;)")
            return True

        #étape 5 --> on demande au maître du jeu de lancer les dés
        master_dice = (random.randint(1, 6), random.randint(1, 6))
        print("You obtained : {master_dice[0]} et {master_dice[1]} ")

        #étape 6 --> checker si le maître de jeu a obtenu un 6
        if 6 in master_dice:
            print("Well, congratulations to me :) I got a 6 ;)")
            print("Thus, I will keep the key.")
            return False
        #étape 7 --> dans le cas où personne n'a eu de 6 on continue la partie
        print("Nobody has a 6. We can go on.")
        attempts +=1

    #étape 8 --> si personne n'a obtenu de 6 sur les trois tentatives, match nul
    print("Well, seems like nobody won.")
    print("It's a draw.")
    return False





            




















