## Exercice 1 - Calcul automatique de l'IMC d'un individu

Ecrire une fonction qui calcule l'indice de masse corporelle (IMC) d'un(e) patient(e) donné(e)

* La fonction nécessitera 2 paramètres en entrée, le poids (en $kg$) et la taille (en $m$), et renverra la valeur de l'IMC en sortie
* Suivant la valeur d'IMC, la fonction devra également fournir une interprétation du résultat (maigreur, IMC normal, surpoids, obésité, obésité massive)
* Tester la fonction avec différents couples de valeurs poids/taille


Réponse 1: 
def indice_de_masse_corporelle(poids,taille):
    imc = poids/(taille**2) # Indiquer la formule pour calculer l'IMC.
    print("IMC = {:0.1f}".format(imc))
    if imc <= 18.5:
        print("Valeur d'IMC indiquant une maigreur")
    elif 18.5 < imc <= 24.9 :
        print("Valeur d'IMC normal")
    elif 24.9 < imc <= 29.9 :
        print("Valeur d'IMC indiquant un surpoids")
    elif 29.9 < imc <= 40 :
        print("Valeur d'IMC indiquant un obésité")
    else :
        print("Valeur d'IMC indiquant une obésité massive")
    return imc

imc = indice_de_masse_corporelle(73,1.71)