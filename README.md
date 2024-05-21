import random

def jogar_jogo():
    # Gerar um número aleatório entre 1 e 100
    numero_secreto = random.randint(1, 100)
    tentativas = 0
    palpite = None
    
    print("Bem-vindo ao jogo de adivinhação!")
    print("Tente adivinhar o número secreto entre 1 e 100.")
    
    while palpite != numero_secreto:
        try:
            palpite = int(input("Digite o seu palpite: "))
            tentativas += 1
            
            if palpite < numero_secreto:
                print("Tente um número maior.")
            elif palpite > numero_secreto:
                print("Tente um número menor.")
            else:
                print(f"Parabéns! Você acertou o número secreto {numero_secreto} em {tentativas} tentativas.")
        except ValueError:
            print("Por favor, digite um número válido.")
            
    print("Fim do jogo!")

if __name__ == "__main__":
    jogar_jogo()
