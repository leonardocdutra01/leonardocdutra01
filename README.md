class Fila:
    def __init__(self):
        self.items = []

    def vazia(self):
        return self.items == []

    def enfileirar(self, item):
        self.items.append(item)

    def desenfileirar(self):
        if not self.vazia():
            return self.items.pop(0)
        else:
            return None

    def tamanho(self):
        return len(self.items)

    def frente(self):
        if not self.vazia():
            return self.items[0]
        else:
            return None

# Função para simular a fila de espera no caixa do supermercado
def simulacao_caixa():
    fila = Fila()

    # Clientes chegando
    fila.enfileirar("Cliente 1")
    fila.enfileirar("Cliente 2")
    fila.enfileirar("Cliente 3")
    fila.enfileirar("Cliente 4")

    # Atendimento no caixa
    print("Atendimento no caixa:")
    while not fila.vazia():
        cliente_atual = fila.desenfileirar()
        print("Atendendo:", cliente_atual)

    print("Todos os clientes foram atendidos.")

# Chamada da função de simulação
simulacao_caixa()
