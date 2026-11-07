# 💈 Barbearia — Sistema de Agendamento

<p align="center">
  Sistema web para apresentação de serviços e agendamento de horários em uma barbearia.
</p>

---

## 📌 Sobre o projeto

Projeto acadêmico de desenvolvimento de um site para uma barbearia, com apresentação de serviços, avaliações de clientes e sistema de agendamento online.

## 🚀 Tecnologias utilizadas

| Tecnologia | Aplicação |
|---|---|
| HTML5 | Estrutura das páginas |
| CSS3 | Estilização e layout |
| JavaScript | Interatividade |
| Python | Desenvolvimento do backend |
| Flask | Framework web |
| SQLite | Banco de dados durante o desenvolvimento |
| PostgreSQL | Banco de dados em produção |
| Flask-SQLAlchemy | Integração com o banco de dados |
| Git e GitHub | Versionamento e colaboração |
| Render | Hospedagem da aplicação |

## ✨ Funcionalidades

- 🏠 Página inicial e apresentação da barbearia.
- ℹ️ Página institucional.
- ✂️ Catálogo de serviços, preços e duração.
- 📅 Sistema de agendamento de cortes.
- ⭐ Exibição de avaliações dos clientes.
- 🔒 Validação de horários e prevenção de agendamentos duplicados.

## 📁 Estrutura do projeto

```text
barbearia/
│
├── backend/
│   ├── app/
│   │   ├── __init__.py
│   │   ├── config.py
│   │   ├── models.py
│   │   ├── routes.py
│   │   │
│   │   ├── templates/
│   │   │   ├── base.html
│   │   │   ├── index.html
│   │   │   ├── sobre.html
│   │   │   ├── servicos.html
│   │   │   ├── agendamento.html
│   │   │   ├── avaliacoes.html
│   │   │   └── partials/
│   │   │       ├── navbar.html
│   │   │       └── footer.html
│   │   │
│   │   └── static/
│   │       ├── css/
│   │       │   └── style.css
│   │       ├── js/
│   │       │   ├── main.js
│   │       │   └── agendamento.js
│   │       └── img/
│   │           ├── logo.png
│   │           ├── banner.jpg
│   │           └── servicos/
│   │
│   ├── requirements.txt
│   ├── run.py
│   └── .env.example
│
├── .gitignore
├── README.md
└── render.yaml
```

## ⚙️ Organização do backend

| Arquivo | Responsabilidade |
|---|---|
| `__init__.py` | Inicialização da aplicação Flask |
| `config.py` | Configurações do sistema |
| `models.py` | Modelos e tabelas do banco de dados |
| `routes.py` | Rotas e funcionalidades |
| `run.py` | Inicialização do servidor |

## 🌐 Páginas do sistema

| Página | Descrição |
|---|---|
| `index.html` | Página inicial |
| `sobre.html` | Apresentação da barbearia |
| `servicos.html` | Serviços e preços |
| `agendamento.html` | Formulário de agendamento |
| `avaliacoes.html` | Avaliações dos clientes |

> **Templates:** utilizaremos Jinja2 para compartilhar componentes, como menu de navegação e rodapé, evitando a repetição de código HTML.

## 🗄️ Banco de dados

A aplicação utilizará SQLAlchemy para gerenciar a comunicação com o banco de dados.

### Tabelas principais

| Tabela | Descrição |
|---|---|
| `clientes` | Dados dos clientes |
| `servicos` | Serviços, preços e duração |
| `agendamentos` | Datas, horários e status |
| `avaliacoes` | Notas e comentários dos clientes |

Os relacionamentos serão definidos por meio de chaves primárias (PK) e estrangeiras (FK).

O sistema também deverá verificar a disponibilidade dos horários e o funcionamento da barbearia antes de confirmar um agendamento.

## 🔗 Principais rotas

| Método | Rota | Funcionalidade |
|---|---|---|
| GET | `/` | Página inicial |
| GET | `/sobre` | Página sobre |
| GET | `/servicos` | Listagem de serviços |
| GET/POST | `/agendamento` | Agendamento |
| GET | `/avaliacoes` | Exibição de avaliações |
| POST | `/api/agendamentos` | Registrar agendamento |
| GET | `/api/servicos` | Consultar serviços |

## 📦 Dependências Python

As dependências serão gerenciadas pelo arquivo `requirements.txt`.

```txt
Flask
Flask-SQLAlchemy
Flask-Migrate
python-dotenv
psycopg2-binary
gunicorn
```

## 🌍 Desenvolvimento e hospedagem

O projeto será desenvolvido de forma colaborativa, utilizando Git e GitHub para versionamento e integração dos códigos.

### Fluxo de desenvolvimento

1. **Desenvolvimento local:** cada integrante trabalha em sua respectiva parte.
2. **Versionamento:** envio e integração das alterações pelo GitHub.
3. **Deploy:** configuração e publicação da aplicação na Render.
4. **Produção:** aplicação Flask executando no servidor e PostgreSQL armazenando os dados.

### 🔐 Configurações importantes

- Utilizar `.gitignore` para arquivos que não devem ser versionados.
- Não enviar arquivos `.env` ao GitHub.
- Armazenar credenciais em variáveis de ambiente.
- Utilizar PostgreSQL em produção.
- Configurar o Gunicorn para executar a aplicação.

## 👥 Colaboração

Todos os integrantes poderão contribuir com o desenvolvimento por meio do repositório GitHub, respeitando a estrutura de pastas e a organização do projeto.

---

<p align="center">
  Desenvolvido como projeto acadêmico de Análise e Desenvolvimento de Sistemas.
</p>
