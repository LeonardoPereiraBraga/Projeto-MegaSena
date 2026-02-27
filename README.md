# 🍀 MegaSena App
 
> Aplicativo Android que simula o sorteio de números da Mega-Sena, gerando combinações aleatórias prontas para o seu jogo.
 
---
 
## 📋 Descrição do Projeto
 
O **MegaSena App** é um aplicativo mobile desenvolvido para Android com o objetivo de auxiliar jogadores que desejam gerar apostas aleatórias para a Mega-Sena. Com apenas um toque, o app sorteia 6 números únicos dentro do intervalo oficial do jogo (1 a 60), exibindo-os de forma ordenada e formatada na tela.
 
---
 
## 🎯 Escopo
 
O projeto contempla as seguintes funcionalidades:
 
- **Sorteio aleatório** de 6 números únicos entre 1 e 60, respeitando as regras oficiais da Mega-Sena
- **Ordenação automática** dos números sorteados do menor para o maior
- **Formatação visual** com dois dígitos (ex: `01`, `09`), mantendo a interface limpa e padronizada
- **Limpeza dos campos** com restauração dos placeholders padrão (`--`)
- Interface simples e direta, com dois botões de ação: **Sortear** e **Limpar**
 
O escopo não inclui verificação de resultados reais da loteria, conexão com a internet ou armazenamento de histórico de apostas.
 
---
 
## ⚙️ Como Funciona
 
O funcionamento do app é dividido em três etapas principais:
 
### 1. Inicialização
Ao abrir o aplicativo, a tela exibe seis campos com o valor `--`, representando os espaços reservados para os números sorteados. Os botões **Sortear** e **Limpar** ficam disponíveis para interação imediata.
 
### 2. Sorteio (`Botão Sortear`)
Ao pressionar o botão **Sortear**, o método `sortearNumeros()` é executado:
 
- Uma lista vazia é criada para armazenar os números
- Um laço `while` gera números aleatórios entre 1 e 60 usando a classe `Random`
- Antes de adicionar cada número à lista, o app verifica se ele já foi sorteado, garantindo que não haja repetições
- O processo se repete até que 6 números únicos sejam obtidos
- A lista é ordenada em ordem crescente com `Collections.sort()`
- Os números são exibidos nos campos da tela com formatação de dois dígitos (`%02d`)
 
### 3. Limpeza (`Botão Limpar`)
Ao pressionar o botão **Limpar**, o método `limparNumeros()` é executado, redefinindo todos os seis campos de volta ao valor `--`, permitindo um novo sorteio a partir de um estado limpo.
 
---
 
## 🛠️ Tecnologias Utilizadas
 
- **Linguagem:** Java
- **Plataforma:** Android
- **SDK:** AndroidX / AppCompat
- **Componentes:** `TextView`, `Button`, `EdgeToEdge`, `WindowInsetsCompat`
 
---
 
## 📁 Estrutura Principal
 
```
com.example.megasena/
└── MainActivity.java   # Lógica principal do sorteio e controle da interface
res/
└── layout/
    └── activity_main.xml   # Layout com os campos de número e botões
```
 
---
 
## 🚀 Como Executar
 
1. Clone ou importe o projeto no **Android Studio**
2. Aguarde a sincronização do Gradle
3. Execute o app em um emulador ou dispositivo físico Android
4. Pressione **Sortear** para gerar sua aposta e **Limpar** para reiniciar
 
---
 
*Boa sorte na sua aposta! 🍀*
