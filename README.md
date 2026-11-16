# ProjetoFinal

Portfólio sobre o curso **Fundamentos de Git e GitHub**, feito como Projeto Integrador Final.

## Objetivo

Usar o Git e o GitHub para organizar este projeto, mostrando na prática o que foi estudado no curso.


## Tecnologias utilizadas

- Git e GitHub
- Markdown (README e reflexão)
- HTML e CSS (página inicial)
- Visual Studio Code

## Pré-requisitos

- Git instalado (confirme com `git --version`).
- Conta no GitHub.
- Chave SSH cadastrada no GitHub, para clonar pelo endereço SSH.
- Navegador de internet para abrir a página.

## Como usar

1. Clone o repositório:
   ```bash
   git clone git@github.com:marisxzh/projetoFinal.git
   ```
2. Entre na pasta do projeto:
   ```bash
   cd projetoFinal
   ```
3. Abra o arquivo `index.html` no navegador.
4. Para ver o histórico de commits:
   ```bash
   git log --oneline --graph --all
   ```

## Estrutura do repositório

```
ProjetoFinal/
├── README.md       # documentação do projeto
├── reflexao.md     # análise crítica do aprendizado
└── index.html      # página inicial
```

## Fluxo de trabalho

Cada Issue foi resolvida em uma branch e integrada à `main` por Pull Request, usando `Closes #N` para fechar a Issue automaticamente.

| Issue | Branch | Resultado |
|---|---|---|
| #1 | `fix/readme` | README corrigido e completo |
| #2 | `fix/reflexao` | Reflexão corrigida e completa |
| #3 | `feat/index` | Página inicial criada |

## Autora

**Mariana** ([@marisxzh](https://github.com/marisxzh))
Engenharia de Computação, CEFET-MG