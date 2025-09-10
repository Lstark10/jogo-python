# 🎮 Jogo de Batalha em Python - Demonstração de POO

Um jogo de batalha em turnos desenvolvido em Python para demonstrar e aplicar os principais conceitos de **Programação Orientada a Objetos (POO)**. O projeto foca na implementação prática de herança, polimorfismo, encapsulamento e abstração de forma didática.

## 📋 Sobre o Projeto

Este é um projeto educacional que simula uma batalha entre um herói e um inimigo, onde o jogador pode escolher entre ataques normais e especiais. O objetivo principal é demonstrar como os conceitos fundamentais da POO podem ser aplicados em um contexto prático e divertido.

## 🎯 Conceitos de POO Demonstrados

### 1. **Encapsulamento** 🔒
- **Atributos privados**: Utilização de `__nome`, `__vida`, `__nivel` para proteger os dados internos das classes
- **Métodos getters**: `get_nome()`, `get_vida()`, `get_nivel()` para acesso controlado aos atributos
- **Controle de acesso**: Os atributos só podem ser modificados através de métodos específicos da classe

### 2. **Herança** 🧬
- **Classe base**: `Personagem` como classe pai que define características comuns
- **Classes filhas**: `Heroi` e `Inimigo` herdam de `Personagem` e adicionam características específicas
- **Reutilização de código**: Métodos e atributos da classe pai são aproveitados pelas classes filhas

### 3. **Polimorfismo** 🎭
- **Sobrescrita de métodos**: O método `exibir_detalhes()` é redefinido nas classes filhas
- **Comportamento específico**: Cada classe implementa o método de forma adequada às suas necessidades
- **Interface comum**: Todas as classes podem usar os mesmos métodos com comportamentos diferentes

### 4. **Abstração** 💭
- **Modelagem do mundo real**: Classes representam conceitos como personagens, heróis e inimigos
- **Simplificação**: Detalhes complexos são encapsulados dentro das classes
- **Separação de responsabilidades**: Cada classe tem uma função bem definida

## 🏗️ Estrutura do Projeto

```
jogo-python-main/
├── jogo.py          # Arquivo principal com todas as classes e lógica do jogo
└── README.md        # Este arquivo de documentação
```

### Classes Implementadas

#### `Personagem` (Classe Base)
- **Atributos**: nome, vida, nível
- **Métodos**: `atacar()`, `receber_ataque()`, `exibir_detalhes()`
- **Função**: Define o comportamento básico de qualquer personagem do jogo

#### `Heroi` (Herda de Personagem)
- **Atributos adicionais**: habilidade especial
- **Métodos específicos**: `ataque_especial()`
- **Função**: Representa o personagem controlado pelo jogador

#### `Inimigo` (Herda de Personagem)
- **Atributos adicionais**: tipo de inimigo
- **Função**: Representa o oponente na batalha

#### `Jogo` (Classe Orquestradora)
- **Função**: Gerencia o fluxo da batalha e a interação entre personagens

## 🚀 Como Executar

1. Certifique-se de ter Python 3.x instalado em seu sistema
2. Clone ou baixe este repositório
3. Execute o arquivo principal:

```bash
python jogo.py
```

## 🎮 Como Jogar

1. O jogo inicia automaticamente uma batalha entre Artorias (herói) e Malenia (inimiga)
2. A cada turno, você pode escolher:
   - **1**: Ataque Normal (dano baseado no nível do personagem)
   - **2**: Ataque Especial (maior dano usando a habilidade especial)
3. Após seu ataque, o inimigo contra-ataca automaticamente
4. A batalha continua até que um dos personagens tenha sua vida reduzida a 0

## 🎲 Mecânicas do Jogo

- **Dano Aleatório**: Os ataques causam dano variável usando `random.randint()`
- **Ataque Normal**: Dano entre `nível × 2` e `nível × 4`
- **Ataque Especial**: Dano entre `nível × 5` e `nível × 8`
- **Sistema de Turnos**: Jogador ataca primeiro, depois o inimigo


## 👨‍💻 Tecnologias Utilizadas

- **Python 3.x**
- **Módulo random** (para geração de números aleatórios)
