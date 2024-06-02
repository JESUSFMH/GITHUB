# GITHUB
class Flor:
    def __init__(self, nome, cor, preco):
        self.nome = nome
        self.cor = cor
        self.preco = preco

class Carrinho:
    def __init__(self):
        self.itens = []

    def adicionar_flor(self, flor, quantidade):
        self.itens.append({"flor": flor, "quantidade": quantidade})

    def calcular_total(self):
        total = 0
        for item in self.itens:
            total += item["flor"].preco * item["quantidade"]
        return total

def main():
    rosa = Flor("Rosa", "vermelho", 2.50)
    margarida = Flor("Margarida", "branco", 1.75)
    girassol = Flor("Girassol", "amarelo", 3.00)

    carrinho = Carrinho()
    carrinho.adicionar_flor(rosa, 2)
    carrinho.adicionar_flor(margarida, 3)
    carrinho.adicionar_flor(girassol, 1)

    total = carrinho.calcular_total()
    print(f"Total da compra: R$ {total:.2f}")

if __name__ == "__main__":
    main()
