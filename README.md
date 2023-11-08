from abc import ABC, abstractmethod

class AnimalDeEstimacao(ABC):

    @abstractmethod
    def __init__(self):
        self.nome = input("Nome do animal: ")
        self.raca = input("Raça do animal: ")
        self.idade = int(input("Idade do animal: "))
        self.nome_responsavel = input("Nome do responsável: ")
        self.telefone_responsavel = input("Telefone do responsável: ")

    @abstractmethod
    def exibir_cadastro(self):
        print("\nCadastro do animal de estimação:")
        print(f"Nome: {self.nome}")
        print(f"Raça: {self.raca}")
        print(f"Idade: {self.idade}")
        print(f"Nome do responsável: {self.nome_responsavel}")
        print(f"Telefone do responsável: {self.telefone_responsavel}")

# Testando a classe abstrata
class Cachorro(AnimalDeEstimacao):

    def __init__(self):
        super().__init__()

    def exibir_cadastro(self):
        super().exibir_cadastro()
        print("Este é um cadastro de cachorro.")

class Gato(AnimalDeEstimacao):

    def __init__(self):
        super().__init__()

    def exibir_cadastro(self):
        super().exibir_cadastro()
        print("Este é um cadastro de gato.")

# Testando a classe Cachorro
animal1 = Cachorro()
animal1.exibir_cadastro()

# Testando a classe Gato
animal2 = Gato()
animal2.exibir_cadastro()# atividade-3
