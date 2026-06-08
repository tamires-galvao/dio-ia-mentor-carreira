# Tutorial de Git e GitHub (Passo a Passo)

Este guia em português brasileiro cobre o fluxo completo para começar e trabalhar com Git no dia a dia.

## 1) Instalação

### Windows
1. Baixe o instalador: https://git-scm.com/download/win  
2. Execute o instalador com as opções padrão.
3. Abra **Git Bash** e rode:
   ```bash
   git --version
   ```

### macOS
Opção com Homebrew:
```bash
brew install git
git --version
```
Ou instale via Xcode Command Line Tools:
```bash
xcode-select --install
git --version
```

### Linux (Debian/Ubuntu)
```bash
sudo apt update
sudo apt install git -y
git --version
```

## 2) Configuração inicial

Defina seu nome e e-mail:
```bash
git config --global user.name "Seu Nome"
git config --global user.email "seuemail@exemplo.com"
```

Configurações úteis:
```bash
git config --global init.defaultBranch main
git config --global core.editor "code --wait"
git config --global pull.rebase false
```

Verificar:
```bash
git config --global --list
```

## 3) Criar conta no GitHub

1. Acesse https://github.com/
2. Clique em **Sign up**.
3. Confirme e-mail e configure autenticação em dois fatores (2FA).
4. (Opcional recomendado) Gere uma chave SSH e adicione ao GitHub:
   ```bash
   ssh-keygen -t ed25519 -C "seuemail@exemplo.com"
   cat ~/.ssh/id_ed25519.pub
   ```
   Depois adicione em **Settings > SSH and GPG keys**.

## 4) Criar um repositório

No GitHub:
1. Clique em **New repository**.
2. Defina nome, descrição e visibilidade.
3. Clique em **Create repository**.

## 5) Primeiro push

No seu projeto local:
```bash
git init
git add .
git commit -m "feat: estrutura inicial do projeto"
git branch -M main
git remote add origin git@github.com:SEU-USUARIO/SEU-REPO.git
git push -u origin main
```

## 6) Fluxo diário de trabalho

```bash
git checkout main
git pull origin main
git checkout -b feat/nova-funcionalidade
# editar arquivos
git add .
git commit -m "feat: adiciona nova funcionalidade"
git push -u origin feat/nova-funcionalidade
```
Depois, abra um Pull Request no GitHub.

## 7) Boas mensagens de commit (Conventional Commits)

Formato:
```text
tipo(escopo opcional): descrição curta
```

Tipos comuns:
- `feat`: nova funcionalidade
- `fix`: correção de bug
- `docs`: documentação
- `refactor`: refatoração sem alterar comportamento
- `test`: criação/ajuste de testes
- `chore`: tarefas de manutenção

Exemplos:
- `feat(auth): adiciona login com JWT`
- `fix(api): corrige validação de payload`
- `docs: atualiza guia de contribuição`

## 8) Branches

Criar branch:
```bash
git checkout -b feature/minha-branch
```

Listar:
```bash
git branch
```

Trocar:
```bash
git checkout main
```

Apagar branch local:
```bash
git branch -d feature/minha-branch
```

## 9) Pull (sincronizar mudanças remotas)

Atualizar branch atual:
```bash
git pull origin main
```

Fluxo seguro (atualizar antes de começar):
```bash
git checkout main
git pull origin main
git checkout sua-branch
git merge main
```

## 10) Desfazer mudanças

Descartar alterações não adicionadas:
```bash
git restore arquivo.txt
```

Remover do stage:
```bash
git restore --staged arquivo.txt
```

Voltar último commit mantendo alterações:
```bash
git reset --soft HEAD~1
```

Voltar último commit descartando alterações locais (use com cuidado):
```bash
git reset --hard HEAD~1
```

## 11) .gitignore

Use `.gitignore` para não versionar arquivos gerados localmente, build, dependências e segredos.

Exemplos comuns:
- `node_modules/`
- `target/`
- `build/`
- `.env`
- `.idea/` e `.vscode/`

## 12) Referência rápida de comandos mais usados

```bash
git status
git add .
git commit -m "mensagem"
git push
git pull
git log --oneline --graph --decorate
git diff
git branch
git checkout -b nome-branch
git merge nome-branch
git restore arquivo
git reset --soft HEAD~1
```

Com este roteiro, você cobre o ciclo completo: configurar, versionar, colaborar e manter um histórico limpo no GitHub.

