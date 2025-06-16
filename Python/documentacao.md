## Documentação simples - Modulo 1

o arquivo **calculadora_simples.ipynb** estará nesse repositório. baixe-o e abra no seu notebook no **Google colab**.


### Pego o nome do usuario
```
#Calculadora simples

print("Calculadora simples da - Emily Comin")

user = input('Qual seu nome ? ').upper()
```
### Calculadora
```
while True:
  #Começando as variaveis
  valores = []
  calculo = 0
  operação = ''
  resposta = ''


  valor_1 = float(input("\n Digite o primeiro valor: ")) #Pegando valor 1
  valor_2 = float(input("Digite o segundo valor: ")) #Pegando valor 2

  valores.append(valor_1)
  valores.append(valor_2)


  print("\n Escolha entre as opções de operação abaixo ! ")
  print("Adição - Coloque: +")
  print("Subtração - Coloque: -")
  print("Divisão - Coloque: /")
  print("Multiplicação  - Coloque: *\n")

  #Validar a inserção
  while True:
    operacao = input("\n Digite qual operação deseja fazer :")
    if operacao != '+' and operacao != '-' and operacao != '/' and operacao != '*':
       print("\n Digite um valor valido ! \n")
    else:
      break
  # Executando a operação
  if operacao == '+':
    calculo = valores[0] + valores[1]
    print(f"A soma dos valores é :{calculo:.2f}")
  elif operacao == '-':
    calculo = valores[0] - valores[1]
    print(f"A subtração dos valores é :{calculo:.2f}")
  elif operacao == '/':
    if valores[1] == 0:
      print("Não é possivel dividir por 0 ")
    else:
      calculo = valores[0] / valores[1]
      print(f"A divisão dos valores é :{calculo:.2f}")
  else:
    calculo = valores[0] * valores[1]
    print(f"A Multiplicação dos valores é :{calculo:.2f}")

  #Continua sim ou não
  while True:
    resposta = input("Deseja fazer outra operação ? (Sim - digite : s  | não - digite:  n)").lower()
    if resposta != 's' and resposta != 'n':
      print("\n Digite um valor valido ! ")
      continue
    else:
      break
  #Valida a resposta s ou n
  if resposta == 'n':
    print(f"\n Obrigado por utilizar minha calculadora {user}, até a proxima !")
    break
  else:
    print(" Vamos lá ! \n")
    continue

```
