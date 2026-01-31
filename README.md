# Mark85 - Testes automatizados (Robot Framework) ✅

**Objetivo:** Este projeto demonstra como automatizar testes web usando **Robot Framework** com o padrão Page Object — testes para autenticação, cadastro de usuário e gerenciamento de tarefas.

---

## 🔧 Componentes do projeto

- **requirements.txt** — todas as dependências do projeto (Robot Framework, Browser, Pabot, etc.).
- **tests/** — suítes de teste (`login.robot`, `signup.robot`, `online.robot`, `tasks/`).
- **resources/** — recursos compartilhados (variáveis, services, fixtures, e `base.resource` para keywords comuns).
- **pages/** — Page Objects organizados por páginas e componentes (ex.: `LoginPage.resource`, `SignupPage.resource`).
- **libs/** — bibliotecas Python com keywords customizados (ex.: `database.py`).
- **resources/fixtures/** — arquivos JSON com dados de teste (ex.: `tasks.json`).
- **backup/** — arquivos extras e exemplos antigos.

---

## 🧩 Requisitos

- Python 3.11 instalado

- Dependências: Robot Framework, RobotFramework-Browser (Playwright), RobotFramework-Requests, Pabot. Elas estão listadas em `requirements.txt`.

---

## 🚀 Instalação (Windows)

1. Criar e ativar ambiente virtual:

```powershell
python -m venv .venv
# PowerShell
.\.venv\Scripts\Activate.ps1
# ou CMD
.\.venv\Scripts\activate
```

2. Instalar dependências:

```powershell
pip install -r requirements.txt
```

---

## ▶️ Executando os testes

- Executar toda a suíte:

```bash
robot -d results tests
```

- Executar um arquivo específico:

```bash
robot -d results tests/login.robot
```

- Incluir / excluir por tag:

```bash
robot -d results -i critical -e dup tests

---

## 🛠 Estrutura e como estender

- Para adicionar uma página: criar `pages/<MyPage>.resource` com keywords (padrão Page Object).
- Para novos cenários: criar/atualizar arquivos em `tests/` e usar fixtures em `resources/fixtures`.
- Métricas e limpeza de dados: use `libs/database.py` para manipular dados antes/depois dos testes.

---
