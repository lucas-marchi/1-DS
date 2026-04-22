# Atividade Avaliativa Prática: Desenvolvimento Modular Orientado a Versionamento

**Disciplina:** Programação de Aplicativos & Lógica de Programação II
**Valor Total:** 10,0 pontos
**Formato de Entrega:** Link do repositório Git e Apresentação em Sala de Aula

---

## 1. Descrição da Atividade

Nesta atividade, você atuará como o desenvolvedor principal responsável por criar uma **Aplicação de Linha de Comando (CLI)** ou com Interface Gráfica. O tema, a interface e a linguagem de programação são de livre escolha sua! 

O objetivo principal desta avaliação não é puni-lo pela complexidade do aplicativo, mas sim validar sua proficiência em boas práticas de programação: o uso de **Modularidade (Funções)** e o **Versionamento de Código (Git)**.

### 1.1 Requisitos Obrigatórios do Sistema (4,0 pontos)
- Você deve desenvolver o código em **qualquer linguagem de programação**.
- **Modularidade de Código:** É estritamente proibido colocar todo o seu código em um único bloco contínuo ou apenas na função principal (Main). O aplicativo deve ser estruturado utilizando **Funções (ou Métodos)**.
  - Deve conter, no mínimo, **3 funções distintas**, que recebam parâmetros e retornem valores.
  - *Exemplo de Divisão Organizacional:* Uma função para coletar/tratar dados, uma função para executar a lógica ou cálculos principais e uma função para exibir as informações ao usuário.

### 1.2 Controle de Versão com Git (3,0 pontos)
- O projeto não pode ser simplesmente salvo no seu computador de uma vez só e concluído. Ele **deve ser versionado**.
- Construa o projeto incrementalmente gerando commits ao finalizar cada etapa (ex: `git commit -m "feat: cria função de calculo do imc"`).
- O repositório deverá ter, no mínimo, **5 commits** distribuídos ao longo do avanço do desenvolvimento.
- O código final deverá ser enviado a um repositório remoto (ex: **GitHub**, **GitLab** ou **Bitbucket**) que será entregue ao professor.

---

## 2. Apresentação e Demonstração da Solução / "Pitch" (3,0 pontos)

Nenhum bom software sobrevive se o desenvolvedor não consegue explicá-lo! Como parte do seu trabalho de conclusão desta etapa, você fará uma **apresentação de até 5 minutos** descrevendo o que desenvolveu. 

**Roteiro obrigatório a ser seguido na sua apresentação:**
1. **O Problema e a Solução:** Que aplicativo você escolheu criar e qual problema ele resolve? Como funciona para o usuário? (Faça o teste ao vivo!).
2. **Exposição do Código (Modularidade):** Mostre uma de suas funções na tela e explique aos colegas para que ela serve, o que as variáveis de entrada recebem e o que ela processa internamente.
3. **Visão do Repositório (Git):** Mostre o histórico do seu repositório Git, comprovando a progressão no desenvolvimento da aplicação de forma sequencial, justificando as mensagens dos seus commits.

---

## Critérios de Avaliação e Rubrica

| Critério                   | Peso    | Especificação para nota máxima                                                                                                  |
| :------------------------- | :------ | :------------------------------------------------------------------------------------------------------------------------------ |
| **Lógica e Funcionamento** | 2,0 pts | O programa executa do início ao fim sem erros pesados e resolve o problema proposto.                                            |
| **Uso de Funções**         | 2,0 pts | O código possui pelo menos 3 funções independentes e bem nomeadas com parâmetros e/ou retornos claros.                          |
| **Histórico e Git**        | 3,0 pts | Repositório publicado com múltiplos commits em estágios de evolução claros da aplicação.                                        |
| **Domínio e Comunicação**  | 3,0 pts | Discurso seguro durante a apresentação; soube demonstrar e explicar o código criado (especialmente as funções e o repositório). |

**Data Limite para Commit Final:** 05/05/2026
**Data de Apresentação e Defesa:** 05/05/2026

> **Dica do Professor:** Comecem pelo planejamento mental (ou no papel) do que as funções de vocês vão fazer. Depois que a estrutura estiver concebida, inicializem o repositório (`git init`), façam o primeiro commit base e só então comecem a colocar a mão no código em si. Boa sorte!
