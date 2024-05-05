## Jogo sudoko em python 

## Descrição 
O jogo utiliza a fila em Python. Além disso, o código inclui algumas funções auxiliares para gerar um tabuleiro aleatório de Sudoku, imprimir o tabuleiro e verificar a solução do jogo.

## Estrutura de dados
O código apresenta duas classes principais: Node e Queue, que são usadas para implementar uma fila (queue) utilizando listas encadeadas em Python. Além disso, o código inclui algumas funções auxiliares para gerar um tabuleiro aleatório de Sudoku, imprimir o tabuleiro e verificar a solução do jogo.
    
    class Node:
          def __init__(self, data):
              self.data = data
              self.next = None

    class Queue:
        def __init__(self):
            self.head = None
            self.tail = None

    def enqueue(self, data):
        new_node = Node(data)
        if self.is_empty():
            self.head = new_node
        else:
            self.tail.next = new_node
        self.tail = new_node

    def dequeue(self):
        if self.is_empty():
            return None
        data = self.head.data
        self.head = self.head.next
        if self.head is None:
            self.tail = None
        return data

    def is_empty(self):
        return self.head is None
        
A fila segue o conceito de "primeiro a entrar, primeiro a sair" (FIFO - First In, First Out),  seu papel é importante, por mais que seja simples já que possui o papel de desfazer a última jogada. Então quando o jogador faz uma jogada válida, o programa armazena as coordenadas da célula modificada e o valor anterior na fila. Se o jogador decidir desfazer a última jogada, o programa recupera essas informações da fila e restaura o valor anterior na célula modificada.


## Como jogar

Sudoku é um jogo de lógica e raciocínio onde o objetivo é preencher um tabuleiro 9x9 com números de 1 a 9 de forma que cada linha, coluna e região 3x3 contenha todos os números de 1 a 9 sem repetição. Resumindo : Não podem haver números repetidos nas linhas horizontais e verticais. 
Começa com partes preenchidas, para preencher as células pode usar APENAS números de 1 a 9, será dado como inválido qualquer coisa diferente. Caso você responda corretamente será preenchido e ficará verde e imútavel, caso fique amarelo, deve usar o -1 quando pedir para digitar a célula e poderá tentar novamente, só que aumenta o somador de erros. 
O jogo acaba quando estiver totalmente preenchido e aparecer a mensagem de "Parábens!"

## Requisitos 

Nenhuma, 
Recomendo penas execute e aumente o terminal para ficar melhor a visibilidade. 

## Autor

Lucas Santana 

## Referências 



## OBRIGADO POR TER LIDO ATÉ AQUI!
