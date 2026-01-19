# full-stack
Com certeza! O Git pode parecer intimidador no começo, mas depois que você entende o fluxo de trabalho (Workflow), ele se torna uma ferramenta indispensável.

Aqui está um guia prático para você começar a versionar seus projetos com Git e GitHub.

---

## 🚀 Guia Prático de Git & GitHub

### 1. Configuração Inicial

Antes de começar, você precisa se identificar para o Git. Isso é importante para que o GitHub saiba quem fez cada alteração.

```bash
git config --global user.name "Seu Nome"
git config --global user.email "seu-email@exemplo.com"

```

### 2. Iniciando um Repositório

Você tem duas opções: começar um projeto do zero ou baixar um que já existe no GitHub.

* **Para começar um novo projeto local:**
```bash
git init

```


* **Para baixar um projeto existente (Clonagem):**
```bash
git clone https://github.com/usuario/repositorio.git

```



### 3. O Ciclo de Trabalho (Workflow)

O versionamento funciona em camadas. Você move seus arquivos entre essas áreas até que eles sejam enviados para a nuvem.

| Comando | Descrição |
| --- | --- |
| `git status` | Verifica o estado atual dos seus arquivos (quais mudaram). |
| `git add .` | Adiciona todos os arquivos alterados para a **Staging Area** (preparação). |
| `git commit -m "mensagem"` | Salva permanentemente as alterações no seu **repositório local**. |

### 4. Conectando ao GitHub

Se você começou o projeto no seu computador (`git init`), precisa dizer ao Git para onde enviar os arquivos na internet.

1. Crie um repositório no GitHub.
2. Copie a URL do repositório.
3. No terminal, digite:

```bash
git remote add origin https://github.com/usuario/nome-do-projeto.git
git branch -M main
git push -u origin main

```

### 5. Trabalhando com Branches (Ramificações)

As *branches* permitem que você trabalhe em novas funcionalidades sem estragar o código que já está funcionando.

* **Criar uma nova branch:** `git checkout -b nome-da-feature`
* **Trocar de branch:** `git checkout nome-da-branch`
* **Mesclar alterações (Merge):** Primeiro volte para a main (`git checkout main`) e depois use `git merge nome-da-feature`.

### 6. Sincronizando Alterações

Sempre que estiver trabalhando em equipe ou em computadores diferentes:

* **Para enviar:** `git push`
* **Para baixar novidades:** `git pull`

---

### Resumo dos Comandos Essenciais

> 💡 **Dica de Ouro:** Use o comando `git status` constantemente. Ele é o seu melhor amigo para entender o que está acontecendo com seus arquivos.

* `git log`: Mostra o histórico de todos os commits feitos.
* `git diff`: Mostra exatamente o que foi alterado dentro dos arquivos antes do commit.
* `git checkout -- arquivo.txt`: Descarta as alterações feitas em um arquivo (cuidado!).

---

**Gostaria que eu explicasse como resolver "conflitos de merge", que é quando duas pessoas mexem na mesma linha do código?**
