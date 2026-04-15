# Laboratório Prático Avançado de Funções

**Pré-requisitos:** Uso do comando `def`, passagem de parâmetros, escopo de variáveis e retorno numérico (`return`).

Este material prático tem o objetivo de treinar a construção de códigos modulares. Na programação profissional real, a regra principal para desenvolver sistemas fáceis de manter é: **Cada função deve ter um objetivo claro e único.**

Siga as instruções abaixo e construa suas soluções etapa por etapa no mesmo arquivo.

---

## Atividade 1: Retornos Numéricos e Interface com o Usuário

Nesta etapa, vamos coletar os dados informados pelo usuário, enviá-los para uma função realizar o cálculo e, por fim, resgatar a resposta numérica. Dessa forma, garantimos que a matemática fique completamente separada dos comandos de texto (`print`).

**Tarefa 1.1: A Função de Cálculo Numérico**
Crie uma função chamada `calcular_desconto(valor_original, percentual_desconto)`.
Esta função **não deve possuir** o comando `print()`. O trabalho dela é estritamente matemático: ela vai receber os dois valores passados nos parâmetros, calcular a quantia do desconto, abater isso do valor original e devolver o preço finalizado através do comando `return`.

**Tarefa 1.2: A Lógica do Programa Principal**
Fora da função acima, construa a estrutura principal do tipo `main` que vai interagir o usuário do seu sistema:
1. Use o comando `input()` pedindo ao usuário que digite o preço de um produto e converta o dado para o formato numérico `float`.
2. Utilize um segundo `input()` pedindo que a pessoa informe a porcentagem do desconto.
3. Chame a função `calcular_desconto`, enviando esses dois valores recém-lidos como parâmetros.
4. Crie uma variável para salvar a resposta que a função gerar.
5. Finalmente, imprima na tela o resultado obtido usando `print()`. Exemplo: *"O preço final com desconto é: R$ 85.00"*.

---

## Atividade 2: Processamento e Atualização de Listas (Vetores)

Uma função também é plenamente capaz de receber uma lista inteira como parâmetro, e processá-la usando laços de repetição automatizados no seu núcleo.

Inicie essa atividade declarando no seu programa a seguinte lista de itens correntes:
`vendas_do_dia = [14.50, 400.90, 50.00, 10.00, 310.20]`

**Tarefa 2.1: Analisando Desempenho (Contador de Ocorrências)**
Construa a função `filtrar_metas(lista_de_vendas)`. 
A função deve receber a lista de faturamento e utilizar um laço `for` para inspecionar cada elemento ali contido. Use a condicional `if` para contabilizar numa nova variável quantas vendas superaram a margem de R$ 300,00. No final, use o `return` para devolver essa quantidade bruta contada. Não utilize `print()` dentro da função.

**Tarefa 2.2: Reajuste em Massa da Lista**
Construa uma segunda função chamada `aplicar_tributacao(lista_de_vendas)`.
Essa função receberá a lista e utilizará um laço de repetição para aplicar um aumento fixo de 5% sobre absolutamente cada um dos valores registrados lá dentro. A diferença aqui está no retorno: ao invés de devolver um número solitário simples, utilize no final dela o `return` para devolver a **lista inteira reajustada**.

> **Lembrete Lógico:** O local exato e correto para disparar a chamada dessas duas funções recém criadas e exibir os resultados ao usuário é no fluxo principal final (as linhas fora da função no fim do seu script).

---

## Atividade 3: Terminal Bancário

Vamos agora consolidar os aprendizados em um produto focado num console aplicável. Faremos a simulação de um terminal de Caixa Eletrônico usando Laços e Condicionais para orquestrar e organizar seu código através de funções.

**Configuração do Ambiente:**
Antes da inicialização direta nas lógicas abaixo, você precisará criar logo nas primeiras linhas duas variáveis principais no seu código:
`saldo_conta = 0.0`
`extrato_geral = []` (Usaremos ela como uma lista base para guardar e enfileirar as strings com texto do nosso histórico de transações).

**Passo 1: Desenhando as Funções de Serviço**

1. **Função `depositar()`:** Esta função deve receber um valor numérico por parâmetro e somá-lo livremente ao `saldo_conta`. Use o comando `.append()` para adicionar uma string descritiva com o registro da operação à lista de extrato (Exemplo de string a adicionar: `"DEPÓSITO REALIZADO: + R$ 100.00"`). Por fim, use o `return` para devolver o novo saldo da conta.
2. **Função `sacar()`:** O saque exige regras firmes. A função checará primeiro se o valor que o usuário deseja sacar é menor ou igual ao que existe no saldo atual. Se ele tentar sacar mais do que a conta possui, exiba uma mensagem de erro na tela ("Fundo insuficiente!") e não realize a dedução. Caso haja saldo positivo cobrindo a transação, então subtraia normalmente o valor em conta, injete com `.append()` a string informacional (`"SAQUE PROCESSADO: - R$ 20.00"`) na lista preenchendo seu extrato, e retorne o seu novo saldo restante via `return`.
3. **Função `imprimir_extrato()`:** Esta função vai apenas se preocupar com a exibição limpa. Receba a variável de extrato como parâmetro e engate um laço de iteração `for`. A ideia é percorrer a lista extraindo elemento a elemento, escrevendo sequencialmente na tela para o usuário imprimir linha a linha o seu relatório de histórico em formato de texto base.

**Passo 2: Motorizando o Menu Interativo (O Laço Principal `while True`)**

Chegou a hora de juntar as três funções. Mantenha o terminal rodando infinitamente criando um projeto de repetição amparado com `while True`. Crie um menu interativo exibindo textos visuais no `input` para listar as opções que direcionam e captam escolhas do usuário operante:

- `[1] Ver Saldo Atual` 
- `[2] Efetuar um Depósito` (Peça ao usuário que digite um valor num input separado. Chame a sua função `depositar()` passando esse valor repassado na variável principal e lembre de salvar o retorno numérico para regravar e atualizar de volta o `saldo_conta` primário).
- `[3] Efetuar um Saque` (Funciona idêntico ao processo anterior de depósito. Peça o valor e passe esse valor disparando a função `sacar()` responsável por averiguar a dedução se houver validade matemática garantindo que ela não ocorra caso barrem os fundos).
- `[4] Obter e Ler Extratos` (Chame unicamente a rotina `imprimir_extrato()` pronta reencaminhando a variável lista inteira para ela ler o que está contido impresso no visual).
- `[0] Sair do Caixa` (Desligue a constância funcional de tela interativa ordenando comando estrito base de ruptura e evadindo com `break`).

Teste se o sistema avisa corretamente e impede o saque caso você tente cobrar um valor superior ao que tem em conta.
