# CodePath BR — Design Instrucional
## Módulo 1: Pensar como Programador · Unidade 1: Lógica de Programação

> Princípio-guia: ensinar a **pensar** antes de ensinar a **digitar**.
> Regra dura de cada conceito: ≤ 60 palavras de explicação + 1 exemplo + 1 checagem.

---

## Hierarquia e fluxo

```
MÓDULO 1 — Pensar como Programador
  └─ UNIDADE 1 — Lógica de Programação
       ├─ Tópico 1.1 — O que é um programa?
       ├─ Tópico 1.2 — Sequência: a ordem importa
       ├─ Tópico 1.3 — Entrada e saída
       ├─ Tópico 1.4 — Tomar decisões (a ideia do "se")
       ├─ Tópico 1.5 — Repetir tarefas (a ideia do "enquanto")
       └─ REVISÃO da Unidade 1
            ↓
       UNIDADE 2 — Primeiros passos em Python (desbloqueada)
```

### Fluxo dentro de um Tópico

```
CONCEITO (1 tela)
  ├─ Explicação ≤ 60 palavras, linguagem do dia a dia
  ├─ 1 exemplo concreto (analogia do mundo real, não código ainda)
  └─ 1 PERGUNTA DE CHECAGEM (múltipla escolha, 1 clique)
       acertou → libera prática | errou → reexplica em 1 frase, tenta de novo
  ↓
PRÁTICA (3-4 exercícios, dificuldade crescente)
  ├─ Ex 1 — Fácil  (reconhecer / escolher)
  ├─ Ex 2 — Médio  (ordenar passos)
  ├─ Ex 3 — Médio  (completar)
  └─ Ex 4 — Desafio (aplicar em situação nova)
  ↓
Regra de erro: após 3 tentativas no mesmo exercício → botão "Pular por enquanto"
  → tópico é marcado como "revisar" → reaparece na REVISÃO da unidade
```

### Revisão da Unidade (repetição espaçada)

```
Gatilho: ao concluir os 5 tópicos da unidade
Conteúdo: 1 exercício de cada tópico marcado "revisar" (onde o aluno errou/pulou)
  └─ Se o aluno não marcou nenhum → puxa os 2 exercícios mais difíceis da unidade
Aprovação: acertar ≥ 70% libera a próxima unidade
```

---

## Tipos de exercício (todos determinísticos, sem IA, custo zero)

Na Unidade de **lógica**, propositalmente quase não há execução de código — o foco é raciocínio. Isso é mais barato e mais didático.

| Tipo | O que o aluno faz | Validação |
|------|-------------------|-----------|
| **Múltipla escolha** | Escolhe 1 opção | Compara índice escolhido |
| **Ordenar passos** | Arrasta blocos pra ordem certa | Compara sequência |
| **Completar** | Preenche 1 lacuna | Compara texto |
| **Verdadeiro/Falso** | Toca V ou F | Compara booleano |
| **Saída esperada** (só no fim) | Prevê o que o programa imprime | Compara string |

A execução real de código (Pyodide) entra de verdade só na **Unidade 2** (Python), onde já validamos que roda rápido.

---

# CONTEÚDO REAL — Unidade 1 completa

## Tópico 1.1 — O que é um programa?

**CONCEITO**
> Um programa é uma receita: uma lista de instruções que o computador segue, uma por uma, na ordem em que você escreveu. Ele não adivinha nada — faz exatamente o que você manda. Toda a programação nasce dessa ideia simples: dar ordens claras, na ordem certa.

*Exemplo (mundo real):* Uma receita de bolo é um programa. "Misture os ovos. Adicione farinha. Asse 40 min." Trocar a ordem estraga o bolo.

**CHECAGEM**
Pergunta: O que o computador faz com as instruções de um programa?
- a) Adivinha o que você quis dizer
- b) ✅ Segue exatamente, na ordem escrita
- c) Escolhe a ordem que achar melhor

*Se errar:* "Lembre: o computador não adivinha. Ele obedece ao pé da letra."

**PRÁTICA**
1. *(Múltipla escolha — fácil)* Qual destes é um "programa" no dia a dia?
   - a) Uma foto · b) ✅ Um manual de montagem de móvel · c) Uma música
2. *(V/F — fácil)* "Um computador faz o que você quis dizer, mesmo se você escrever errado." → **Falso**
3. *(Ordenar — médio)* Coloque na ordem para fazer um café:
   `[ligar a máquina] [colocar o pó] [apertar o botão] [pegar a xícara]`
4. *(Múltipla escolha — desafio)* Se um programa tem os passos na ordem errada, o que acontece?
   - a) ✅ Ele faz a coisa errada, mesmo sem dar "erro" · b) Ele se corrige sozinho · c) Nada

---

## Tópico 1.2 — Sequência: a ordem importa

**CONCEITO**
> Sequência é a ordem das instruções. O computador executa de cima para baixo, uma de cada vez. Mudar a ordem muda o resultado — às vezes quebra tudo. Pensar no programa é, antes de mais nada, pensar na ordem certa dos passos.

*Exemplo:* "Vista a meia. Calce o sapato." funciona. Invertido, não.

**CHECAGEM**
Em que ordem o computador lê as instruções?
- a) ✅ De cima para baixo, uma por vez
- b) Todas ao mesmo tempo
- c) Da que ele achar mais importante

*Se errar:* "Uma de cada vez, de cima para baixo. Sempre."

**PRÁTICA**
1. *(Ordenar — fácil)* Sair de casa: `[abrir a porta] [pegar a chave] [sair] [trancar a porta]`
2. *(Múltipla escolha — médio)* "Servir o suco" e "Encher o copo" — qual vem primeiro? → **Encher o copo**
3. *(Ordenar — médio)* Enviar uma mensagem: `[abrir o app] [escrever o texto] [escolher o contato] [tocar enviar]`
4. *(Múltipla escolha — desafio)* Dois passos: "1. Apague o fogo. 2. Coloque a panela no fogo." O que está errado? → **A ordem: a panela tem que ir antes de apagar**

---

## Tópico 1.3 — Entrada e saída

**CONCEITO**
> Programas recebem informação (entrada) e devolvem um resultado (saída). Você digita uma senha (entrada), o app diz "correto" ou "errado" (saída). Quase todo programa é isto: pega algo, processa, devolve algo.

*Exemplo:* Calculadora — entrada: "2 + 2". Saída: "4".

**CHECAGEM**
Numa busca do Google, o que é a SAÍDA?
- a) O que você digita
- b) ✅ A lista de resultados que aparece
- c) O botão de buscar

*Se errar:* "Entrada é o que você dá. Saída é o que o programa devolve."

**PRÁTICA**
1. *(Múltipla escolha — fácil)* No caixa eletrônico, digitar o valor do saque é... → **Entrada**
2. *(V/F — fácil)* "O dinheiro que sai do caixa é uma saída." → **Verdadeiro**
3. *(Completar — médio)* "Num termômetro digital, a temperatura mostrada é a ____." → **saída**
4. *(Múltipla escolha — desafio)* Num jogo, apertar o botão de pulo é entrada. E o personagem pulando na tela? → **Saída**

---

## Tópico 1.4 — Tomar decisões (a ideia do "se")

**CONCEITO**
> Programas tomam decisões. "SE estiver chovendo, leve o guarda-chuva." O computador checa uma condição e, dependendo da resposta (sim ou não), faz uma coisa ou outra. Essa é a base de toda inteligência num programa.

*Exemplo:* "SE o saldo for maior que o preço, ENTÃO aprove a compra. SENÃO, recuse."

**CHECAGEM**
Na frase "SE a senha estiver certa, libere o acesso" — o que é a condição?
- a) Liberar o acesso
- b) ✅ A senha estar certa
- c) O usuário

*Se errar:* "A condição é o que vem depois do SE — o que precisa ser checado."

**PRÁTICA**
1. *(Múltipla escolha — fácil)* "SE tiver 18 anos ou mais, pode dirigir." A condição é... → **ter 18 anos ou mais**
2. *(V/F — fácil)* "Uma decisão sempre tem só uma resposta possível." → **Falso**
3. *(Completar — médio)* "SE o semáforo estiver vermelho, então ____." → **pare** (aceita variações)
4. *(Ordenar — desafio)* Monte a decisão: `[SE] [a nota for >= 7] [ENTÃO aprovado] [SENÃO reprovado]`

---

## Tópico 1.5 — Repetir tarefas (a ideia do "enquanto")

**CONCEITO**
> Computadores são ótimos em repetir. Em vez de escrever a mesma ordem 100 vezes, você diz: "ENQUANTO faltar louça, continue lavando." O programa repete até a condição deixar de ser verdade. Isso se chama repetição (ou laço).

*Exemplo:* "ENQUANTO o balde não estiver cheio, jogue mais água."

**CHECAGEM**
"ENQUANTO houver e-mail novo, baixe o próximo." Quando o programa PARA?
- a) ✅ Quando não houver mais e-mail novo
- b) Nunca para
- c) Depois do primeiro e-mail

*Se errar:* "A repetição para quando a condição vira falsa — aqui, quando acabam os e-mails."

**PRÁTICA**
1. *(Múltipla escolha — fácil)* "ENQUANTO tiver degrau, suba." Isso descreve... → **subir uma escada**
2. *(V/F — fácil)* "Uma repetição pode rodar zero vezes, se a condição já for falsa no início." → **Verdadeiro**
3. *(Completar — médio)* "ENQUANTO o jogo não acabar, ____ jogando." → **continue**
4. *(Múltipla escolha — desafio)* O que acontece se a condição de uma repetição NUNCA virar falsa? → **O programa repete pra sempre (laço infinito)**

---

## REVISÃO — Unidade 1

Puxa 1 exercício de cada tópico onde o aluno errou ou pulou. Exemplo de revisão para um aluno que tropeçou em 1.4 e 1.5:

1. *(de 1.4)* "SE o cliente for VIP, dê desconto." A condição é... → **o cliente ser VIP**
2. *(de 1.5)* "ENQUANTO houver páginas, imprima." Para quando? → **quando acabarem as páginas**
3. *(síntese)* Ordene um mini-programa completo:
   `[receber a idade] [SE idade >= 18] [mostrar "maior"] [SENÃO mostrar "menor"]`

Aprovação: ≥ 70% de acerto → desbloqueia **Unidade 2 — Primeiros passos em Python**.

---

## Decisões de design registradas (Audit Trail)

| Decisão | Justificativa |
|---------|---------------|
| Lógica antes de sintaxe | Reduz desistência; ensina a pensar antes de digitar |
| ≤ 60 palavras por conceito | Iniciante abandona em parede de texto |
| Checagem antes da prática | Garante que o conceito foi entendido, não pulado |
| Pular após 3 tentativas | Evita frustração travante; erro vira dado |
| Revisão por repetição espaçada | Revisa o que errou, não tudo igual (memória real) |
| Quase sem código na Unid. 1 | Mais barato (sem Pyodide) e mais didático |
| Múltipla escolha / ordenar como base | Validação determinística, custo zero de API |

---

## O que falta para virar produto (honestidade v5.3.1)

Este é o **design + conteúdo da Unidade 1**. Para virar produto ainda precisa:
- Protótipo navegável dos novos tipos de exercício (ordenar, V/F, checagem)
- Conteúdo das Unidades 2+ (aí sim entra Python e Pyodide)
- Persistência do "tópicos a revisar" (IndexedDB)
- O gerador em batch para escalar conteúdo além do que foi autorado à mão aqui
