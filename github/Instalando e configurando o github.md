# 🐱 Git para Iniciantes — Do Zero ao Repositório!

> **Bem-vindo(a), futuro(a) mestre do controle de versões!** 🎉
> 
> Imagine que o Git é uma **máquina do tempo** para o seu código. Ele guarda um "retrato" do seu projeto em cada momento importante, e você pode voltar a qualquer um desses momentos quando quiser. Incrível, né?

---

## 📚 Sumário

1. [O que é o Git?](#-o-que-é-o-git)
2. [Instalando o Git no Windows](#-instalando-o-git-no-windows)
3. [Configurando o Git no VSCode](#-configurando-o-git-no-vscode)
4. [Criando sua conta no GitHub](#-criando-sua-conta-no-github)
5. [Criando um repositório no GitHub](#-criando-um-repositório-no-github)
6. [Subindo sua pasta para o repositório](#-subindo-sua-pasta-para-o-repositório)
7. [Fazendo commits (salvando seu progresso)](#-fazendo-commits-salvando-seu-progresso)
8. [Push e Pull — trabalhando em outro PC](#-push-e-pull---trabalhando-em-outro-pc)
9. [Resumo dos comandos essenciais](#-resumo-dos-comandos-essenciais)

---

## 🤔 O que é o Git?

Pense assim: você está escrevendo um livro. Toda vez que termina um capítulo importante, tira uma **foto** do manuscrito. Se errar algo depois, é só voltar para a foto anterior.

O **Git** faz exatamente isso com o seu código! Cada "foto" se chama **commit**.

O **GitHub** é como uma **nuvem** onde você guarda essas fotos, podendo acessá-las de qualquer computador do mundo 🌍.

---

## 🛠 Instalando o Git no Windows

### Passo 1 — Baixar o instalador

Acesse: **https://git-scm.com/download/win**

O download vai começar automaticamente. É de graça! 💸

### Passo 2 — Executar o instalador

Abra o arquivo baixado (algo como `Git-2.xx.x-64-bit.exe`) e siga os passos:

> 💡 **Dica:** Pode clicar em **Next** em todas as telas sem medo. As configurações padrão já são ótimas para iniciantes!

As únicas telas que merecem atenção:
```bash
|                     Tela                     |                           O que fazer                        |
+----------------------------------------------+--------------------------------------------------------------+
| **Choosing the default editor**              | Selecione `Use Visual Studio Code as Git's default editor`   |
| **Adjusting the name of the initial branch** | Selecione `Override the default branch name` e digite `main` |
| Todas as outras                              | Pode deixar o padrão e clicar **Next**                       |
```
### Passo 3 — Verificar a instalação

Abra o **Prompt de Comando** (pressione `Win + R`, digite `cmd` e Enter) e digite:

```bash
git --version
```

Se aparecer algo como `git version 2.xx.x`, funcionou! 🎉 Senão... xiiiii... não sei o que houve, chama o Prof. Erich (kkkkkkkkkkkkk)

### Passo 4 — Apresentar-se ao Git

O Git precisa saber quem você é para assinar os commits. Execute os dois comandos abaixo (substituindo pelos seus dados):

```bash
git config --global user.name "Seu Nome Aqui"
git config --global user.email "seu@email.com"
```

> 📌 Use o **mesmo e-mail** que você vai usar no GitHub, ai ai ai, se liga nisso ai!

---

## 💻 Configurando o Git no VSCode

O VSCode já vem com suporte nativo ao Git! Você só precisa garantir que ele está encontrando o Git instalado.

### Verificando se o VSCode reconhece o Git

1. Abra o **VSCode**
2. Pressione `Ctrl + Shift + P` para abrir a paleta de comandos
3. Digite `Git: Show Git Output` e pressione Enter

Se não aparecer nenhum erro, está tudo certo! ✅ Uhuuuuuu!!!

### A aba "Source Control" (Controle do Código-Fonte)

Olhe na barra lateral esquerda do VSCode — há um ícone que parece um **"Y" estilizado** (ou três bolinhas conectadas). Esse é o painel do Git no VSCode!

```
Ícone na barra lateral:
┌─────────────────┐
│  🔍 Explorer      ← Arquivos
│  🔎 Search        ← Busca
│  🔀 Source Ctrl   ← Git está aqui!
│  🐛 Debug         ← Depuração
│  📦 Extensions    ← Extensões
└─────────────────┘
```

### Extensão recomendada: GitLens 🔭

No VSCode, vá em **Extensions** (`Ctrl + Shift + X`), pesquise por **GitLens** e instale. Ela deixa as informações do Git muito mais visuais e fáceis de entender! hahah você vai gostar disso!!! =)

---

## 👤 Criando sua conta no GitHub

Se ainda não tem conta, acesse **https://github.com** e clique em **Sign up**. Olha como é lindo ele é gratuito! 

> 🔐 **Importante:** Guarde bem seu usuário e senha. Você vai precisar deles em breve!

---

## 📦 Criando um repositório no GitHub

Um **repositório** (ou "repo") é como uma pasta especial no GitHub onde seu projeto vive.

### Passo a passo:

1. Acesse **https://github.com** e faça login
2. Clique no botão verde **New** (ou no `+` no canto superior direito → `New repository`)
3. Preencha as informações:
```bash
|          Campo       |                      O que colocar                       |
+----------------------+----------------------------------------------------------+
| **Repository name**  | Nome do seu projeto (ex: `meu-site`, `calculadora`)      |
| **Description**      | Uma frase descrevendo o projeto (opcional)               |
| **Public / Private** | `Public` = qualquer um vê / `Private` = só você vê       |
| **Add a README**     | ❌ Deixe **desmarcado** (vamos enviar nossos arquivos!)  |
```
4. Clique em **Create repository** 🚀

Após criar, o GitHub vai mostrar uma página com instruções. Não feche essa aba! Vamos precisar dela.

---

## 📤 Subindo sua pasta para o repositório

Agora vem a parte emocionante: **enviar seu projeto para o GitHub**!

### Abrindo o Terminal no VSCode

Com sua pasta de projeto aberta no VSCode, vá em:
**Terminal → New Terminal** (ou `Ctrl + '`)

Um terminal vai aparecer na parte inferior do VSCode — é por aqui que vamos "conversar" com o Git.

### Sequência de comandos

Execute os comandos abaixo **um por vez**, pressionando Enter após cada um:

**1️⃣ Inicializar o Git na sua pasta:**
```bash
git init
```
> Isso cria uma "memória" na sua pasta. O Git começa a "observar" os arquivos!

**2️⃣ Adicionar todos os arquivos para serem salvos:**
```bash
git add .
```
> O ponto `.` significa "adicionar TUDO". É como selecionar todos os arquivos antes de tirar a foto.

**3️⃣ Criar o primeiro commit (a primeira "foto"):**
```bash
git commit -m "Primeiro commit - inicio do projeto"
```
> A mensagem entre aspas é como uma etiqueta na foto. Escreva algo que descreva o que foi feito!

**4️⃣ Definir que a branch principal se chama `main`:**
```bash
git branch -M main
```

**5️⃣ Conectar sua pasta ao repositório do GitHub:**
```bash
git remote add origin https://github.com/SEU-USUARIO/NOME-DO-REPO.git
```
> ⚠️ Substitua `SEU-USUARIO` pelo seu usuário do GitHub e `NOME-DO-REPO` pelo nome do repositório que você criou. Você encontra essa URL na página do repositório que deixou aberta!

**6️⃣ Enviar os arquivos para o GitHub:**
```bash
git push -u origin main
```
> Esse comando "empurra" (push) seus arquivos para a nuvem! 🌐

### Autenticação no GitHub

Na primeira vez, o Git vai pedir sua senha ou um token. O GitHub não aceita mais senha direta — você precisa criar um **token de acesso**:

1. Acesse **https://github.com/settings/tokens**
2. Clique em **Generate new token (classic)**
3. Dê um nome ao token (ex: `meu-pc`)
4. Marque a opção **repo**
5. Clique em **Generate token**
6. **Copie o token gerado** (você não vai conseguir ver ele de novo!)
7. Use esse token **no lugar da senha** quando o Git pedir

> 💾 Salve esse token em algum lugar seguro (como no bloco de notas protegido por senha)!

---

## 💾 Fazendo commits (salvando seu progresso)

Lembra que o commit é como uma "foto" do projeto? Você deve fazer commits sempre que fizer uma mudança importante!

### O ciclo de vida de uma mudança

```
Você edita um arquivo
        ↓
   git add .          ← "Seleciona" as mudanças
        ↓
git commit -m "msg"   ← Tira a "foto"
        ↓
   git push           ← Envia para o GitHub
```

### Exemplo prático do dia a dia

Você alterou o arquivo `index.php` e adicionou um novo `style.css`. Veja como salvar:

```bash
# Verificar o que mudou (opcional, mas muito útil!)
git status

# Adicionar as mudanças
git add .

# Criar o commit com uma mensagem descritiva
git commit -m "Adiciona menu de navegação e estilo visual"

# Enviar para o GitHub
git push
```

### Dicas para mensagens de commit 📝
```bash
| ❌ Mensagem ruim |            ✅ Mensagem boa            |
|-------------------+---------------------------------------+
| `commit`          | `Corrige bug no login`                |
| `mudancas`        | `Adiciona página de contato`          |
| `arrumei`         | `Melhora responsividade no mobile`    |
| `aaa`             | `Remove função duplicada no carrinho` |
```
> 💡 Uma boa mensagem responde: **"O que esse commit faz?"**

---

## 🔄 Push e Pull — trabalhando em outro PC

Imagine que você trabalha no projeto no **computador de casa** durante a semana, e na sexta leva o notebook para continuar no fim de semana. É aqui que o Git brilha! ✨

### 📤 Push — Enviando seu trabalho (no PC de origem)

Sempre que terminar de trabalhar, envie suas mudanças para o GitHub:

```bash
git add .
git commit -m "Descreva o que você fez"
git push
```

> 🎒 É como colocar seus pertences na mochila antes de sair de casa!

---

### 📥 Pull — Baixando seu trabalho (no PC de destino)

Chegou no outro computador e quer continuar de onde parou? Primeiro, você precisa ter o repositório clonado. Se for a **primeira vez** nesse PC:

**Clonando o repositório (só na primeira vez no PC novo):**
```bash
git clone https://github.com/SEU-USUARIO/NOME-DO-REPO.git
```

Isso vai baixar toda a pasta do projeto com todo o histórico de commits! 📂

---

Se o repositório **já está** no PC e você só quer pegar as atualizações:

```bash
git pull
```

> 📬 É como abrir a caixa de correio e pegar as novidades que chegaram!

---

### 🔁 O ciclo completo em dois PCs

```
PC DE CASA                         GITHUB (nuvem)                    NOTEBOOK
=================                  =================                 =================
Faz alterações
git add .
git commit -m "..."
git push          ----------------→  📦 Código atualizado
                                                       ←------------ git pull
                                                                      Continua trabalhando
                                                                      git add .
                                                                      git commit -m "..."
                                    📦 Código atualizado  ←--------- git push
git pull          ←----------------
Continua em casa!
```

---

## 📋 Resumo dos comandos essenciais
```bash
|        Comando        |            O que faz          |            Quando usar            |
|-----------------------+-------------------------------+---------------------------------- +
| `git init`            | Inicializa o Git na pasta     | Apenas uma vez, no início         |
| `git status`          | Mostra o que mudou            | Sempre que quiser ver o status    |
| `git add .`           | Prepara TODOS os arquivos     | Antes de todo commit              |
| `git add arquivo.php` | Prepara um arquivo específico | Quando quiser ser seletivo        |
| `git commit -m "msg"` | Salva uma "foto" do projeto   | Após o `git add`                  |
| `git push`            | Envia para o GitHub           | Após o commit                     |
| `git pull`            | Baixa atualizações do GitHub  | Ao começar a trabalhar em novo PC |
| `git clone URL`       | Baixa o repositório completo  | Primeira vez em um PC novo        |
| `git log`             | Mostra o histórico de commits | Para ver o passado do projeto     |
```
---

## 🏆 Fluxo completo — Do zero ao GitHub

```
1. git init                          ← Liga a "máquina do tempo"
2. git add .                         ← Seleciona os arquivos
3. git commit -m "Primeiro commit"   ← Tira a primeira foto
4. git branch -M main                ← Nomeia a linha do tempo
5. git remote add origin URL         ← Conecta ao GitHub
6. git push -u origin main           ← Envia para a nuvem! 🚀
```

**Para os dias seguintes:**
```
1. (faz alterações no código)
2. git add .
3. git commit -m "Descreve o que fez"
4. git push
```

---

## 🆘 Erros comuns e como resolver

### ❌ "fatal: not a git repository"
Você esqueceu de rodar o `git init`! Execute-o na pasta do seu projeto.

### ❌ "Please tell me who you are"
Você não configurou seu nome/e-mail. Execute:
```bash
git config --global user.name "Seu Nome"
git config --global user.email "seu@email.com"
```

### ❌ "rejected — non-fast-forward"
O GitHub tem mudanças que você não baixou ainda. Execute primeiro:
```bash
git pull
```
E depois tente o `git push` novamente.

### ❌ "Authentication failed"
O GitHub mudou a política de autenticação. Use um **token de acesso pessoal** no lugar da senha (veja a seção de autenticação acima).

---

## 🎓 Parabéns!

Se chegou até aqui, você já sabe o essencial para usar o Git no seu dia a dia como desenvolvedor(a)! 🎊

Lembre-se: **o segredo é a prática**. Quanto mais você usar, mais natural vai ficar.

> 💬 _"Todo especialista já foi um dia um iniciante."_

---

