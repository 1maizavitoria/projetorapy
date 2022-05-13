from random import randint
# Implementar o jogo de maos conhecido como Jokenpo ou Pedra, Papel, Tesoura.
# Modos de jogo:
# 1 jogador vs jogador
# 2 jogador vs computador
# 3 computador vs computador

while True:

    # Qualquer valor diferente de 0, para verificacao do while.
    jogada_1 = 1
    jogada_2 = 1
    modo_jogo = 1
    # Numero de partidas realizadas, percentual de vitorias de cada jogador, numero de empates.

    # Inicializando variveis para acumulacao 0 = 0 +1.
    numero_partidas = 0
    vitorias_1 = 0
    vitorias_2 = 0
    numero_empates = 0


    print("Use 1 para modo jogador vs jogador;")
    print("Use 2 para modo jogador vs computador;")
    print("Use 3 para modo computador vs computador;")
    print("Digite 0 para sair do jogo.")
    modo_jogo = int(input("Informe o modo de jogo:  "))
    if modo_jogo == 1:
        while (jogada_1 !=0 or jogada_2 != 0):
            jogada_1 = int(input(
                "Jogador 1, escolha sua jogada (1 = Pedra, 2 = Papel, 3 = Tesoura e 0 para sair): "))
            jogada_2 = int(input(
                "Jogador 2, escolha sua jogada (1 = Pedra, 2 = Papel, 3 = Tesoura e 0 para sair): "))

            if ((jogada_1 == 1 and jogada_2 == 3) or (jogada_1 == 2 and jogada_2 == 1) or (jogada_1 == 3 and jogada_2 == 2)):

                print("Jogador 1 eh o vencedor")
                vitorias_1 = vitorias_1 + 1
                numero_partidas = numero_partidas + 1

            elif ((jogada_1 == 3 and jogada_2 == 1) or (jogada_1 == 1 and jogada_2 == 2) or (jogada_1 == 2 and jogada_2 == 3)):

                print("Jogador 2 eh o vencedor")
                vitorias_2 = vitorias_2 + 1
                numero_partidas = numero_partidas + 1

            elif ((jogada_1 == 1 and jogada_2 == 1) or (jogada_1 == 2 and jogada_2 == 2) or (jogada_1 == 3 and jogada_2 == 3)):

                print("Empate!")
                numero_empates = numero_empates + 1
                numero_partidas = numero_partidas + 1

            elif (jogada_1 == 0 and jogada_2 == 0):
                print("")
                print("Quantidade de partidas: ", numero_partidas)

                print("O percentual de vitorias do jogador 1 eh: ",
                      vitorias_1 / numero_partidas * 100, "%")

                print("O percentual de vitorias do jogador 2 eh: ",
                      vitorias_2 / numero_partidas * 100, "%")

                print("Empates: ", numero_empates)
            else:
                print("Jogada invalida")

    elif modo_jogo == 2:
        while jogada_1 != 0:
            jogada_1 = int(input(
                "Jogador, escolha sua jogada (1 = Pedra, 2 = Papel, 3 = Tesoura e 0 para sair): "))
            # rangeint para gerar um numero inteiro.
            jogada_2 = randint(1, 3)
            print(
                "Maquina, escolha sua jogada (1 = Pedra, 2 = Papel, 3 = Tesoura): ", jogada_2)

            if ((jogada_1 == 1 and jogada_2 == 3) or (jogada_1 == 2 and jogada_2 == 1) or (jogada_1 == 3 and jogada_2 == 2)):

                print("Jogador eh o vencedor")
                vitorias_1 = vitorias_1 + 1
                numero_partidas = numero_partidas + 1

            elif ((jogada_1 == 3 and jogada_2 == 1) or (jogada_1 == 1 and jogada_2 == 2) or (jogada_1 == 2 and jogada_2 == 3)):

                print("A maquina eh a vencedora")
                vitorias_2 = vitorias_2 + 1
                numero_partidas = numero_partidas + 1

            elif ((jogada_1 == 1 and jogada_2 == 1) or (jogada_1 == 2 and jogada_2 == 2) or (jogada_1 == 3 and jogada_2 == 3)):

                print("Empate!")
                numero_empates = numero_empates + 1
                numero_partidas = numero_partidas + 1

            elif (jogada_1 and jogada_2) == 0:
                print("")
                print("Quantidade de partidas: ", numero_partidas)

                print("O percentual de vitorias do jogador e: ",
                      vitorias_1 / numero_partidas * 100, "%")

                print("O percentual de vitorias da maquina e: ",
                      vitorias_2 / numero_partidas * 100, "%")

                print("Empates: ", numero_empates)
            else:
                print("Jogada invalida")

    elif modo_jogo == 3:
        contador = int(
            input("Informe o numero de vezes que deseja assistir a partida: "))
        # range (numero inicial, numero final, incrementador -aumenta de x em x)
        for numero_execucao in range(0, contador, 1):
            jogada_1 = randint(1, 3)
            print(
                "Maquina 1, escolha sua jogada (1 = Pedra, 2 = Papel, 3 = Tesoura): ", jogada_1)
            jogada_2 = randint(1, 3)
            print(
                "Maquina 2, escolha sua jogada (1 = Pedra, 2 = Papel, 3 = Tesoura): ", jogada_2)

            if ((jogada_1 == 1 and jogada_2 == 3) or (jogada_1 == 2 and jogada_2 == 1) or (jogada_1 == 3 and jogada_2 == 2)):

                print("A maquina 1 e a vencedora")
                vitorias_1 = vitorias_1 + 1
                numero_partidas = numero_partidas + 1

            elif ((jogada_1 == 3 and jogada_2 == 1) or (jogada_1 == 1 and jogada_2 == 2) or (jogada_1 == 2 and jogada_2 == 3)):

                print("A Maquina 2 e a vencedora")
                vitorias_2 = vitorias_2 + 1
                numero_partidas = numero_partidas + 1

            elif ((jogada_1 == 1 and jogada_2 == 1) or (jogada_1 == 2 and jogada_2 == 2) or (jogada_1 == 3 and jogada_2 == 3)):

                print("Empate!")
                numero_empates = numero_empates + 1
                numero_partidas = numero_partidas + 1

        print("")

        print("Quantidade de partidas: ", numero_partidas)

        print("O percentual de vitorias da maquina 1 e: ",
              vitorias_1 / numero_partidas * 100, "%")

        print("O percentual de vitorias da maquina 2 e: ",
              vitorias_2 / numero_partidas * 100, "%")

        print("Empates: ", numero_empates)

    elif modo_jogo == 0:
        print("Obrigado por jogar")
        break

    else:
        print("Modo de jogo invalido.")
