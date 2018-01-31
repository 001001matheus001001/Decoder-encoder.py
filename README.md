# Decoder-encoder.py
# Script feito por Matheus Silva
# Dependencias python3 programado em GNU/LINUX
# 30/01/2018 Hs 02:29
# Deus Ajuda quem cedo madruga shaushuahsuahsuhausha

mensagem = input("entre com a mensagem para codificar ou decodificar: ") # Obtém a menssagem

mensagem = mensagem.upper()             # Faz com que ela tenha somente LETRAS MAIUSCULAS :)

saida = ""                            # Cria uma string vazia pra armazenar a saida da mesma

for escrita in mensagem:                               # Percorre todas as letras da mensagem
    if escrita.isupper():                              # se a letra estiver no alfabeto (A-Z)
        valor = ord(escrita) + 13                            # desloca em 13 o valor da letra
        escrita = chr (valor)                     # transforma o valor de volta em uma letra,
        if not escrita.isupper():                           # e verifica se deslocamos demais
            valor -= 26                                        # Se afirmativo, da a volta ,
                                                                           # e passa de Z->A
            escrita = chr(valor)                            # Subtraindo 26 di valor da letra
    saida += escrita                               # Adiciona a letra a nossa string de saida
print("saida da mensagem:", saida)      # Manda um print com a saida codificada/decodificada
