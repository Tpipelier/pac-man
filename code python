"""
Programme réalisé par Pipelier, Théo, 1G7
"""
import pygame


#variables du niveau
NB_TILES = 28   #nombre de tiles a charger (ici de 00.png à 27.png) 28 au total
TITLE_SIZE=32   #definition du dessin (carré)
largeur=16       #hauteur du niveau
hauteur=16       #largeur du niveau
tiles=[]       #liste d'images tiles

#variables de gestion du pacman
pacX=1          #position x y du pacman dans le niveau
pacY=1
pacVX=1
pacVY=1
compteurBilles=0
direction=0
#variables de gestion du fantome
FRAMERATE_FANTOME= 80      #vitesse du fantome chiffre elevé = vitesse lente
NB_DEPLACEMENT_FANTOME =15   #le fantome se deplace sur 16 cases
positionFantome=1
frameRateCounterFantome=0
posfX=11                        #position initiale du fantome
posfY=3

FRAMERATE_FANTOMEB= 80      #vitesse du fantome chiffre elevé = vitesse lente
NB_DEPLACEMENT_FANTOMEB =37   #le fantome se deplace sur 36 cases
positionFantomeB=1
frameRateCounterFantomeB=1
posBfX=2                        #position initiale du fantome
posBfY=6

FRAMERATE_FANTOMER= 80      #vitesse du fantome chiffre elevé = vitesse lente
NB_DEPLACEMENT_FANTOMER =44   #le fantome se deplace sur 44 cases
positionFantomeR=1
frameRateCounterFantomeR=1
posRfX=14                        #position initiale du fantome
posRfY=6

#definition du niveau

niveau=[[1,5,5,5,5,5,5,5,5,5,5,5,5,5,5,2],
     [6,0,12,12,12,12,12,12,12,12,12,12,12,12,13,6],
     [7,5,5,24,12,23,5,10,5,2,12,12,12,12,12,6],
     [6,13,12,12,12,12,12,6,12,25,12,23,24,12,12,6],
     [6,12,12,12,12,12,12,6,12,12,12,12,12,12,12,6],
     [6,12,12,26,12,26,12,25,12,23,5,5,5,10,5,9],
     [6,12,12,6,12,6,12,12,12,12,12,12,12,6,12,6],
     [7,5,10,8,10,8,24,12,12,13,12,12,12,6,12,6],
     [6,13,6,12,6,12,12,12,12,12,12,12,12,6,12,6],
     [6,12,6,12,6,12,23,5,24,12,23,24,12,6,12,6],
     [6,12,6,12,6,12,12,12,12,12,12,12,12,6,12,6],
     [6,12,6,12,3,5,5,5,24,12,23,5,5,9,12,6],
     [6,12,6,12,12,12,12,12,12,12,12,12,12,6,12,6],
     [6,12,3,5,5,5,5,5,24,12,23,5,5,4,12,6],
     [6,12,12,12,12,12,12,12,12,12,12,12,12,12,13,6],
     [3,5,5,5,5,5,5,5,5,5,5,5,5,5,5,4]]
#definition de l'accueil
accueil=[[27,27,27,27,27,27,27,27,27,27,27,27,27,27,27,27],
     [27,27,27,27,27,27,27,27,27,27,27,27,27,27,27,27],
     [27,27,27,27,27,27,27,27,27,27,27,27,27,27,27,27],
     [27,27,27,27,27,27,27,27,27,27,27,27,27,27,27,27],
     [27,27,27,27,27,27,27,27,27,27,27,27,27,27,27,27],
     [27,27,27,27,27,27,27,27,27,27,27,27,27,27,27,27],
     [27,27,27,27,27,27,27,27,27,27,27,27,27,27,27,27],
     [27,27,27,27,27,27,14,13,15,20,27,27,27,27,27,27],
     [27,27,27,27,27,27,27,27,27,27,27,27,27,27,27,27],
     [27,27,27,27,27,27,27,27,27,27,27,27,27,27,27,27],
     [27,27,27,27,27,27,27,27,27,27,27,27,27,27,27,27],
     [27,27,27,27,27,27,27,27,27,27,27,27,27,27,27,27],
     [27,27,27,27,27,27,27,27,27,27,27,27,27,27,27,27],
     [27,27,27,27,27,27,27,27,27,27,27,27,27,27,27,27],
     [27,27,27,27,27,27,27,27,27,27,27,27,27,27,27,27],
     [27,27,27,27,27,27,27,27,27,27,27,27,27,27,27,27]]

fantome=[[0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0],
     [0,0,0,0,0,0,0,0,0,0,12,13,0,0,0,0],
     [0,0,0,0,0,0,0,0,0,0,11,14,1,2,3,0],
     [0,0,0,0,0,0,0,0,0,0,10,0,0,0,4,0],
     [0,0,0,0,0,0,0,0,0,0,9,8,7,6,5,0],
     [0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0],
     [0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0],
     [0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0],
     [0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0],
     [0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0],
     [0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0],
     [0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0],
     [0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0],
     [0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0],
     [0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0],
     [0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0]]

fantomeB=[[0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0],
     [0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0],
     [0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0],
     [0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0],
     [0,36,35,34,33,32,31,0,0,0,0,0,0,0,0,0],
     [0,1,0,0,0,0,30,0,0,0,0,0,0,0,0,0],
     [0,2,0,0,0,0,29,28,27,26,0,0,0,0,0,0],
     [0,3,0,0,0,0,0,0,0,25,0,0,0,0,0,0],
     [0,4,0,0,0,0,0,0,0,24,0,0,0,0,0,0],
     [0,5,0,0,0,0,0,0,0,23,0,0,0,0,0,0],
     [0,6,0,0,0,0,0,0,0,22,0,0,0,0,0,0],
     [0,7,0,0,0,0,0,0,0,21,0,0,0,0,0,0],
     [0,8,0,0,0,0,0,0,0,20,0,0,0,0,0,0],
     [0,9,0,0,0,0,0,0,0,19,0,0,0,0,0,0],
     [0,10,11,12,13,14,15,16,17,18,0,0,0,0,0,0],
     [0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0]]
fantomeR=[[0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0],
     [0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0],
     [0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0],
     [0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0],
     [0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0],
     [0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0],
     [0,0,0,0,0,0,0,0,0,0,0,0,41,42,43,0],
     [0,0,0,0,0,0,0,0,0,0,0,0,40,0,1,0],
     [0,0,0,18,0,28,0,0,0,0,0,0,39,0,2,0],
     [0,0,0,19,0,29,0,0,0,0,0,0,38,0,3,0],
     [0,0,0,20,0,30,31,32,33,34,35,36,37,0,4,0],
     [0,0,0,21,0,0,0,0,0,0,0,0,0,0,5,0],
     [0,0,0,22,23,24,25,26,27,15,16,17,0,0,6,0],
     [0,0,0,0,0,0,0,0,0,14,0,0,0,0,7,0],
     [0,0,0,0,0,0,0,0,0,13,12,11,10,9,8,0],
     [0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0]]


#la taille de la fenetre dépend de la largeur et de la hauteur du niveau
#on rajoute une rangée de 32 pixels en bas de la fentre pour afficher le score d'ou (hauteur +1)
pygame.init()
fenetre = pygame.display.set_mode((largeur*TITLE_SIZE, (hauteur+1)*TITLE_SIZE))
pygame.display.set_caption("Pac-Man")
font = pygame.font.Font('freesansbold.ttf', 20)


def chargetiles(tiles):
    """
    fonction permettant de charger les images tiles dans une liste tiles[]
    """
    for n in range(0,NB_TILES):
        print('data/'+str(n)+'.png')
        tiles.append(pygame.image.load('data/'+str(n)+'.png')) #attention au chemin


def afficheNiveau(niveau):
    """
    affiche le niveau a partir de la liste a deux dimensions niveau[][]
    """
    for y in range(hauteur):
        for x in range(largeur):
            fenetre.blit(tiles[niveau[y][x]],(x*TITLE_SIZE,y*TITLE_SIZE))
def afficheAcueill(accueil):
    """
    affiche le niveau a partir de la liste a deux dimensions niveau[][]
    """

    for y in range(hauteur):
        for x in range(largeur):
            fenetre.blit(tiles[accueil[y][x]],(x*TITLE_SIZE,y*TITLE_SIZE))



def affichePac(numero):
    """
    Affiche le Pac-Man dans la direction correspondante
    """
    global pacX, pacY
    fenetre.blit(tiles[numero],(pacX * TITLE_SIZE,pacY * TITLE_SIZE))



def afficheScore(score):
    """
    affiche le score
    """

    scoreAafficher = font.render("Score : "+str(score), True, (255, 255, 255))
    fenetre.blit(scoreAafficher,(340,500))



def rechercheFantome(fantome,position): #recherche les coord du fantome dans la liste fantome
    """
    recherche les coordonnées du fantome en fonction du numéro de sa postion dans le parcours
    """
    print(position)                     #la position doit etre dans la liste fantome sinon plantage
    for y in range(hauteur):
        for x in range(largeur):
            if fantome[y][x]==position:
                coodFantome=x,y
    return coodFantome          #les coord du fantome x et y sont dans un tuple coodFantome
def rechercheFantomeB(fantomeB,positionB): #recherche les coord du fantome dans la liste fantome
    """
    recherche les coordonnées du fantomeB en fonction du numéro de sa postion dans le parcours
    """
    print(positionB)                     #la position doit etre dans la liste fantome sinon plantage
    for y in range(hauteur):
        for x in range(largeur):
            if fantomeB[y][x]==positionB:
                coodFantomeB=x,y
    return coodFantomeB          #les coord du fantome x et y sont dans un tuple coodFantome
def rechercheFantomeR(fantomeR,positionR): #recherche les coord du fantome dans la liste fantome
    """
    recherche les coordonnées du fantomeB en fonction du numéro de sa postion dans le parcours
    """
    print(positionR)                     #la position doit etre dans la liste fantome sinon plantage
    for y in range(hauteur):
        for x in range(largeur):
            if fantomeR[y][x]==positionR:
                coodFantomeR=x,y
    return coodFantomeR          #les coord du fantome x et y sont dans un tuple coodFantome
def afficheVie(vie):
      vieAafficher = font.render("Vie : "+ str(vie), True, (255, 255, 255))
      fenetre.blit(vieAafficher,(120,500))



def deplaceFantome(fantome):
    """
    Incrémente automatiquement le déplacement du fantome, gère sa vitesse et son affichage
    """
    global frameRateCounterFantome
    global positionFantome
    global posfX,posfY
    if frameRateCounterFantome==FRAMERATE_FANTOME:      #ralenti la viteese du fantome
        posfX,posfY=rechercheFantome(fantome,positionFantome)   #deballage du tuple coordonnées du fantome
        positionFantome+=1
        if positionFantome==NB_DEPLACEMENT_FANTOME:     #un tour est fait donc on passe à la 1ere position
            positionFantome=1
        frameRateCounterFantome=0                       #compteur de vitesse à zero
    fenetre.blit(tiles[15],(posfX * TITLE_SIZE,posfY * TITLE_SIZE)) #affichage du fantome
    frameRateCounterFantome+=1                          #incrémentation du compteur de vitesse
def deplaceFantomeB(fantomeB):
    """
    Incrémente automatiquement le déplacement du fantome, gère sa vitesse et son affichage
    """
    global frameRateCounterFantomeB
    global positionFantomeB
    global posBfX,posBfY
    if frameRateCounterFantomeB==FRAMERATE_FANTOMEB:      #ralenti la viteese du fantome
        posBfX,posBfY=rechercheFantomeB(fantomeB,positionFantomeB)   #deballage du tuple coordonnées du fantome
        positionFantomeB+=1
        if positionFantomeB==NB_DEPLACEMENT_FANTOMEB:     #un tour est fait donc on passe à la 1ere position
            positionFantomeB=1
        frameRateCounterFantomeB=0                       #compteur de vitesse à zero
    fenetre.blit(tiles[20],(posBfX * TITLE_SIZE,posBfY * TITLE_SIZE)) #affichage du fantome
    frameRateCounterFantomeB+=1                          #incrémentation du compteur de vitesse
def deplaceFantomeR(fantomeB):
    """
    Incrémente automatiquement le déplacement du fantome, gère sa vitesse et son affichage
    """
    global frameRateCounterFantomeR
    global positionFantomeR
    global posRfX,posRfY
    if frameRateCounterFantomeR==FRAMERATE_FANTOMER:      #ralenti la viteese du fantome
        posRfX,posRfY=rechercheFantomeR(fantomeR,positionFantomeR)   #deballage du tuple coordonnées du fantome
        positionFantomeR+=1
        if positionFantomeR==NB_DEPLACEMENT_FANTOMER:     #un tour est fait donc on passe à la 1ere position
            positionFantomeR=1
        frameRateCounterFantomeR=0                       #compteur de vitesse à zero
    fenetre.blit(tiles[21],(posRfX * TITLE_SIZE,posRfY * TITLE_SIZE)) #affichage du fantome
    frameRateCounterFantomeR+=1



chargetiles(tiles)  #chargement des images
vie=3
r=0
fluidité=0
loop=True


while loop==True:
    for event in pygame.event.get():
        if event.type == pygame.QUIT:
            loop = False            #fermeture de la fenetre (croix rouge)
        elif event.type == pygame.KEYDOWN:  #une touche a été pressée...laquelle ?
            if flu==0 and compteurBilles<121 and r==1 and vie>0 and event.key == pygame.K_UP:    #est-ce la touche UP

                posY = pacY - 1             #on deplace le pacman virtuellement
                posX = pacX
                numeroTile = niveau[posY][posX]       #on regarde le numéro du tile
                print("up",numeroTile,end=':')
                direction=1

                if (numeroTile == 12 or numeroTile == 0 or numeroTile == 13):#si le tile est une bille ou un fond noir alors le déplacement est possible
                    flu+=1
                    print("deplacement possible",pacVX,pacVY)
                    for n in range(pacY*TITLE_SIZE,(posY*TITLE_SIZE)-1):
                        fenetre.blit(tiles[18],(n,pacY*TITLE_SIZE))
                        pygame.display.update()
                    pacY-=1#on monte donc il faut décrémenter pacY



                else:
                    print("deplacement impossible")

            elif flu==0 and compteurBilles<121 and r==1 and vie>0 and event.key == pygame.K_DOWN:  #est-ce la touche DOWN


                posY = pacVY + 1
                posX = pacX
                numeroTile = niveau[posY][posX]
                print("down",numeroTile,end=':')
                direction=2
                if (numeroTile == 12 or numeroTile == 0 or numeroTile == 13):
                    flu+=1
                    pacY += 1
                    print("deplacement possible",pacX,pacY)
                else:
                    print("deplacement impossible")







            elif flu==0 and compteurBilles<121 and r==1 and vie>0 and event.key == pygame.K_RIGHT:  #est-ce la touche RIGHT
                posY = pacY
                posX = pacX+1
                numeroTile = niveau[posY][posX]
                print("Right",numeroTile,end=':')
                direction=3

                if (numeroTile == 12 or numeroTile == 0 or numeroTile == 13):
                    flu+=1
                    print("deplacement possible",pacVX,pacVY)
                    for n in range(pacX*TITLE_SIZE,(posX*TITLE_SIZE)+1):
                        fenetre.blit(tiles[14],(n,pacY*TITLE_SIZE))
                        pygame.display.update()
                    pacX+=1


                else:
                    print("deplacement impossible")



            elif flu==0 and compteurBilles<121 and r==1 and vie>0 and event.key == pygame.K_LEFT:  #est-ce la touche LEFT

                posY = pacY
                posX = pacX- 1

                numeroTile = niveau[posY][posX]
                print("Left",numeroTile,end=':')
                direction=4

                if (numeroTile == 12 or numeroTile == 0 or numeroTile == 13):
                    flu+=1
                    print("deplacement possible",pacVX,pacVY)
                    for n in range(pacX*TITLE_SIZE,(posX*TITLE_SIZE)-1):
                        fenetre.blit(tiles[17],(n,pacY*TITLE_SIZE))
                        pygame.display.update()
                    pacX-=1

                else:
                    print("deplacement impossible")






            if compteurBilles<121 and vie>0 and r==1 and numeroTile==12:  #si le numero du tile est 12 c'est que l'on est sur une nouvelle bille
                compteurBilles+=1   #alors on incrémente le score
                niveau[posY][posX]=0    #et on efface la bille dans le niveau
                print("nouvelle bille")
            elif vie>0 and r==1 and numeroTile == 13:
                vie+=1
                niveau[posY][posX]=0
            else :
                print("fond noir")

            if r==1 and (event.key == pygame.K_ESCAPE or event.unicode == 'q'): #touche q pour quitter

                loop=False
            elif r==0 and event.unicode == 's': #touche q pour quitter

                r=r+1

            else :
                print("déplacement impossible")

    if fluidite==1:
        cptpixel+=1
        if cptpixel==32:
            fluidite=0
            cptpixel=0
    fenetre.fill((0,0,0))   #efface la fenetre



    if posfX==pacX and posfY==pacY or posBfX==pacX and posBfY==pacY  or posRfX==pacX and posRfY==pacY:
        vie=vie-1
        pacX=1
        pacY=1
    if vie>0 and 0<r<2:
        afficheNiveau(niveau)










    deplaceFantome(fantome) #mettre un commentaire pour desactiver le déplacement du fantome
    deplaceFantomeB(fantomeB)
    deplaceFantomeR(fantomeR)

    if compteurBilles>=121:
        afficheAcueill(accueil)
        WinnerAafficher = font.render("Winner", True, (255, 255, 0))
        QuitterAafficher = font.render("Stop game      'q'", True, (255, 0, 0))
        fenetre.blit(WinnerAafficher,(220,260))
        fenetre.blit(QuitterAafficher,(180,280))
        pacX=1
        pacY=1


    elif vie==0 or r==0 :

        if r==0 :
            afficheAcueill(accueil)
            StartAafficher = font.render("Start game      's'", True, (0, 200, 255))
            QuitterAafficher = font.render("Stop game      'q'", True, (255, 0, 0))
            fenetre.blit(StartAafficher,(180,260))
            fenetre.blit(QuitterAafficher,(180,280))
            deplaceFantomeB(fantomeB)
            deplaceFantome(fantome)
        elif vie==0 :
            afficheAcueill(accueil)
            GameOverAafficher = font.render("Game Over", True, (255, 255, 255))
            QuitterAafficher = font.render("Quitter avec 'q'", True, (255, 255, 255))
            fenetre.blit(GameOverAafficher,(200,260))
            fenetre.blit(QuitterAafficher,(180,300))

    afficheScore(compteurBilles)
    afficheVie(vie)
    affichePac(direction)#affiche la pacman et le score
    pygame.display.update() #mets à jour la fenetre graphique
pygame.quit()

