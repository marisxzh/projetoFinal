# Reflexão sobre o curso Fundamentos de Git e GitHub

## 1. Controle de versão, Git e GitHub

O controle de versão registra o histórico de um projeto, permitindo saber quem alterou, o quê e quando foi alterado, e voltar a uma versão anterior com segurança. Os sistemas podem ser locais, centralizados, ou distribuídos.

O Git é a ferramenta que gerencia o histórico na máquina local. O GitHub é a plataforma que hospeda os repositórios na nuvem e acrescenta recursos de colaboração, como Pull Requests e Issues.

## 2. Ciclo de vida local

O Git organiza os arquivos em três áreas:

- **Working Directory:** pasta onde os arquivos são editados.
- **Staging Area:** área de triagem, onde se escolhe o que entra no próximo commit (`git add`).
- **Repositório local:** banco de dados na pasta `.git`, onde cada commit guarda um registro do projeto naquele momento.

A mensagem de cada commit documenta o motivo da mudança. O padrão Conventional Commits (`tipo(escopo): descrição`) usa tipos como `feat`, `fix` e `docs` para facilitar a compreensão das mudanças feitas. O arquivo `.gitignore` define o que não deve ser monitorado, como credenciais e dependências, e os comandos `git log` e `git diff` permitem consultar o histórico e comparar alterações.

## 3. Desfazendo erros

Cada comando atua em uma situação:

- `git restore` descarta alterações ainda não commitadas, de forma irreversível.
- `git commit --amend` corrige o último commit e só deve ser usado em commits não publicados.
- `git revert` desfaz um commit criando outro com a alteração inversa, preservando o histórico.
- `git stash` guarda temporariamente um trabalho incompleto, sem gerar commit.

## 4. Conexão com o GitHub

A autenticação por chave SSH usa um par de chaves: a pública é cadastrada no GitHub e a privada nunca deve ser compartilhada. O repositório local é vinculado ao remoto com `git remote add origin`. O `git push` envia commits ao GitHub, o `git pull` baixa e integra alterações, o `git fetch` baixa sem integrar e o `git clone` copia um repositório remoto completo.

## 5. Branches, merge e rebase

Uma branch é um ponteiro para um commit e permite desenvolver uma funcionalidade sem afetar a `main`. O merge integra uma branch em outra. Quando duas branches alteram o mesmo trecho de um arquivo, ocorre um conflito, resolvido manualmente: escolhe-se o conteúdo final, removem-se os marcadores do Git e conclui-se o commit.

O rebase reaplica commits sobre outra base, gerando um histórico linear, mas reescreve o histórico e deve ser usado apenas em branches locais. O merge preserva o histórico original e é indicado para branches compartilhadas.

## 6. Trabalho em equipe

O GitHub Flow organiza o trabalho em etapas: criar uma branch, fazer commits, publicar, abrir um Pull Request, passar por revisão e fazer o merge na `main`. O Pull Request deve ter título claro, descrição do motivo da mudança e vínculo com a Issue por meio de `Closes #N`, que a fecha automaticamente. 
As Issues registram tarefas e problemas, e a revisão de código (Code Review) melhora a qualidade das alterações. O Gitflow é um modelo mais rígido, usado em projetos com ciclos de lançamento definidos.

## 7. GitHub Pages

O GitHub Pages hospeda gratuitamente páginas estáticas (HTML, CSS e JavaScript) a partir de um repositório. Para publicar, é necessário um arquivo `index.html` na raiz e a ativação da publicação em *Settings → Pages*, escolhendo a branch e a pasta de origem.

## Considerações finais

Esses conceitos foram praticados ao longo do curso em repositórios locais, conexões com o GitHub, branches, conflitos e Pull Requests, o que permitiu compreender como o Git e o GitHub se complementam no controle de versão e no trabalho em equipe.