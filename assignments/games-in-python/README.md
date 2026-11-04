# 📘 Atividade: Jogo da Forca

## 🎯 Objetivo

Construa o clássico jogo de adivinhar palavras usando strings, loops e entrada de dados do usuário em Python. Os alunos aprenderão manipulação de strings, loops, condicionais e seleção aleatória.

## 📝 Tarefas

### 🛠️ Implementar Seleção Aleatória de Palavras

#### Descrição
Crie uma função que seleciona aleatoriamente uma palavra de uma lista predefinida para servir como a palavra-alvo do jogo.

#### Requisitos
O programa concluído deve:

- Importar o módulo `random` para seleção aleatória
- Definir uma lista de palavras predefinidas
- Retornar uma palavra aleatória da lista
- Converter a palavra para letras maiúsculas para padronização


### 🛠️ Exibir Progresso e Aceitar Palpites

#### Descrição
Implemente o loop principal do jogo que exibe o progresso atual da palavra oculta (usando underscores) e aceita palpites de letras do jogador.

#### Requisitos
O programa concluído deve:

- Exibir a palavra oculta no formato `_ _ _` (com espaços entre as letras)
- Aceitar palpites de letras do usuário via entrada
- Verificar se a letra está na palavra-alvo
- Revelar todas as ocorrências da letra adivinada
- Rastrear tentativas incorretas restantes


### 🛠️ Implementar Lógica de Vitória e Derrota

#### Descrição
Complete o jogo adicionando a lógica para determinar quando o jogador ganha ou perde, e exiba mensagens apropriadas.

#### Requisitos
O programa concluído deve:

- Verificar se a palavra foi completamente adivinhada (vitória)
- Verificar se as tentativas esgotaram (derrota)
- Exibir mensagem de vitória quando a palavra for revelada
- Exibir mensagem de derrota e a palavra correta quando as tentativas acabarem
- Oferecer a opção de jogar novamente