# projetoIMC
Este é um projeto simples feito em Python para calcular o IMC (Índice de Massa Corporal) de uma pessoa com base em seu peso e altura.
## 🧮 Como funciona:
- O usuário digita o peso em kg e a altura em metros.
- O programa calcula o IMC com a fórmula:
- # Projeto: Cálculo de IMC (Índice de Massa Corporal)
# Autor: Erica Costa de Eça
# Descrição: Este programa calcula o IMC do usuário e exibe a classificação de acordo com a OMS.


def calcular_imc(peso, altura):
    """Calcula o IMC com base no peso e altura."""
    return peso / (altura ** 2)

def classificar_imc(imc):
    """Retorna a classificação do IMC de acordo com a tabela da OMS."""
    if imc < 18.5:
        return "Baixo peso"
    elif 18.5 <= imc <= 24.9:
        return "Peso normal"
    elif 25.0 <= imc <= 29.9:
        return "Sobrepeso"
    elif 30.0 <= imc <= 34.9:
        return "Obesidade grau I"
    elif 35.0 <= imc <= 39.9:
        return "Obesidade grau II"
    else:
        return "Obesidade grau III (mórbida)"

def main():
    print("=== Cálculo de IMC ===")
    
    try:
        peso = float(input("Informe seu peso (em kg): "))
        altura = float(input("Informe sua altura (em metros): "))
        
        imc = calcular_imc(peso, altura)
        classificacao = classificar_imc(imc)

        print(f"\nSeu IMC é: {imc:.2f}")
        print(f"Classificação: {classificacao}")
    except ValueError:
        print("Entrada inválida! Por favor, digite números válidos para peso e altura.")

if __name__ == "__main__":
    main()    
