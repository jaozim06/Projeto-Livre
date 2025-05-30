# 📝 Projeto de Gerenciamento de Usuários e Arquivos

Este é um projeto web desenvolvido com **Python (Flask)** que permite o gerenciamento de usuários e arquivos por meio de uma interface simples. O sistema conta com duas visões principais: uma de **administrador**, que pode cadastrar e excluir usuários, e uma de **usuário comum**, que pode fazer upload e download de arquivos.

---

## 🔧 Tecnologias Utilizadas

- **Python 3**
- **Flask**
- **HTML/CSS**
- **JSON** (para armazenamento de usuários)
- **JavaScript (mínimo uso)**
- **Arquivos estáticos (imagens e CSS)**

---

## ⚙️ Funcionalidades
- **Área Administrativa**:
  - ✅ Cadastro/remoção de usuários
  - 📤 Upload de documentos
  - 👥 Listagem de usuários
- **Área do Usuário**:
  - 🔐 Login seguro
  - 📥 Download de arquivos
    
### 👤 Login
- Acesso via rota `/`
- O login é feito com nome e senha (dados armazenados no arquivo `usuarios.json`)
- Caso o login seja do administrador (`adm` / `000`), redireciona para a interface de gerenciamento

### 🔐 Administração (`/adm`)
- Visualização dos usuários cadastrados
- Cadastro de novos usuários
- Exclusão de usuários existentes
- Upload de arquivos

### 👥 Área do Usuário (`/usuarios`)
- Lista de arquivos disponíveis
- Possibilidade de download

---

## 📁 Estrutura de Arquivos

```
.
├── main.py                 # Código principal em Flask
├── login.html             # Página inicial de login
├── usuarios.json          # Lista de usuários cadastrados
├── administrador.css      # Estilo da interface administrativa
├── usuarios.css           # Estilo da interface de usuários
├── home.css               # Estilo compartilhado
├── fundo.png              # Imagem de fundo
└── 001/
    └── arquivos/          # Pasta de armazenamento de arquivos enviados
```

---

## ▶️ Executando o Projeto

1. Instale o Flask:
   ```bash
   pip install flask
   ```

2. Execute o servidor:
   ```bash
   python main.py
   ```

3. Acesse no navegador:
   ```
   http://localhost:2005/
   ```

---

## 🧪 Usuários Padrão para Teste

- **Administrador:**
  - Usuário: `adm`
  - Senha: `000`

- **Usuários Comuns (exemplo):**
  - Usuário: `igor` / Senha: `123`
  - Usuário: `joao` / Senha: `789`

---
👨‍💻 Autor
João Paulo da Silva Pereira - GitHub

## ⚠️ Observações

- Os dados dos usuários são armazenados em JSON, sem criptografia.
- A aplicação utiliza uma variável global `logado`
- O diretório de arquivos é fixo como `001/arquivos`.
