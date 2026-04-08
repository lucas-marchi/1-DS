**Disciplina:** Programação de Aplicativos  
**Dinâmica:** Código guiado com versionamento passo a passo.

## 1. Setup do Projeto

Antes de escrever qualquer lógica, vamos preparar o terreno. Agora abram o terminal e o editor de código.

**Passo a passo com a turma:**

1. Agora criem uma pasta chamada `calculadora_pizzaria`.
    
2. Dentro dela, iniciem o controle de versão: `git init`.
    
3. Agora criem o arquivo principal: `app.py`.
    
4. Abram o arquivo, escrevam um comentário simples como `# Módulo de Cálculos da Pizzaria` e salvem.
    
5. Façam o primeiro commit oficial do projeto:
    
    - `git add .`
        
    - `git commit -m "Inicia o projeto da calculadora de pizzaria"`
        

## 2. Teoria Rápida: O que é uma Função?

Não percam muito tempo com abstrações. Vou direto ao ponto:

- _"Até agora, nosso código era uma tripa reta que rodava de cima para baixo. Funções são 'mini-fábricas' dentro do código. Você entrega a matéria-prima (Parâmetros), a fábrica processa o cálculo lá dentro, e te devolve o produto final (Retorno)."_
    
- **A Vantagem:** Reuso. Se você precisa calcular a gorjeta para 50 mesas diferentes, você não escreve a conta 50 vezes. Você escreve a fábrica uma vez e a chama 50 vezes.
    

## 3. Criando a Primeira "Fábrica"

Agora vamos criar uma função que calcula o valor da gorjeta que o cliente deve deixar, sabendo que a regra é 10% do valor total da conta.

**No código:**

```python
# Módulo de Cálculos da Pizzaria

def calcular_gorjeta(total_conta):
    # A regra é 10% do total da conta
    gorjeta = total_conta * 0.10
    return gorjeta
```

- **Explique:** `total_conta` é a porta de entrada (parâmetro). O `return` é a porta de saída. A variável `gorjeta` morre assim que a função termina (escopo local).
    

**O Checkpoint do Git:**

A primeira funcionalidade está pronta! Hora de salvar o estado na máquina do tempo.

No terminal:

- `git status` (para vocês verem que o app.py foi modificado)
    
- `git add .`
    
- `git commit -m "Cria funcao de calculo de gorjeta"`
    

## 4. Segunda Função: Múltiplos Parâmetros

Agora vamos complicar um pouco. Uma função para calcular o custo total de um pedido. Ela precisa de duas matérias-primas: o número de pizzas e o valor por pizza.

**No código:**

```python
def calcular_custo_total_pedido(quantidade_pizzas, preco_por_pizza):
    custo_total = quantidade_pizzas * preco_por_pizza
    return custo_total
```

- **Explique:** Podemos ter quantos parâmetros quisermos, separados por vírgula. A ordem importa na hora de usar a função!
    

**O Checkpoint do Git:**

Mais uma feature finalizada.

- `git add .`
    
- `git commit -m "Cria funcao de calculo de custos de pedido"`
    

## 5. Juntando as Peças

Até agora, as "fábricas" existem, mas estão desligadas. Ninguém apertou o botão de ligar. Agora vamos criar a interação com o usuário para usar as funções criadas.

**No código (no final do arquivo):**

```python
print("--- SISTEMA DE GESTÃO DA PIZZARIA ---")

# Coletando os dados
total_conta = float(input("Digite o valor total da conta em reais: "))

# Chamando a função e guardando o retorno em uma variável
gorjeta_recomendada = calcular_gorjeta(total_conta)

print(f"A gorjeta recomendada é de {gorjeta_recomendada} reais.")
```

**O Checkpoint do Git Final:**

O app está rodando de ponta a ponta.

- `git add .`
    
- `git commit -m "Implementa interface do usuario e integracao das funcoes"`
    

## 6. Desafio Final

Agora que vocês entenderam o ciclo, façam o desafio em dupla e subam para o GitHub:

**A Missão:**

1. Criem uma nova _branch_ chamada `feature-lucro`: `git branch feature-lucro` e `git checkout feature-lucro`.
    
2. No código, criem uma terceira função chamada `calcular_lucro` que recebe dois parâmetros: `preco_custo` e `preco_venda`. A função deve retornar a diferença entre os dois.
    
3. Façam a chamada dessa função no fluxo principal do programa imprimindo o resultado na tela.
    
4. Façam o commit dessa alteração ("Adiciona função de cálculo de lucro").
    
5. Voltem para a branch `main` (`git checkout main`), façam o merge (`git merge feature-lucro`) e, se houver internet no laboratório, deem um `git push` para o repositório de vocês.