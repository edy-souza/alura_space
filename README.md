# 🚀 Alura Space

Galeria de imagens astronômicas desenvolvida com Django, criada durante os cursos da [Alura](https://www.alura.com.br/). O projeto permite navegar por fotos do espaço com uma interface temática e responsiva.

---

## 📋 Índice

- [Sobre o Projeto](#sobre-o-projeto)
- [Funcionalidades](#funcionalidades)
- [Tecnologias](#tecnologias)
- [Estrutura do Projeto](#estrutura-do-projeto)
- [Pré-requisitos](#pré-requisitos)
- [Instalação e Configuração](#instalação-e-configuração)
- [Como Executar](#como-executar)

---

## Sobre o Projeto

O **Alura Space** é uma aplicação web de galeria de imagens com temática espacial. Ela exibe fotografias astronômicas — como nebulosas — organizadas em uma interface moderna com navegação por categorias (mais curtidas, mais vistas, novas e surpreenda-me).

---

## Funcionalidades

- Página inicial com galeria de imagens astronômicas
- Página de detalhe de cada imagem
- Navegação por categorias (Novas, Mais curtidas, Mais vistas, Surpreenda-me)
- Layout responsivo com CSS customizado
- Painel administrativo Django para gerenciamento do conteúdo
- Variáveis de ambiente via `.env` para proteção da `SECRET_KEY`

---

## Tecnologias

| Tecnologia | Versão |
|---|---|
| Python | 3.x |
| Django | 6.0.3 |
| python-dotenv | 1.2.2 |
| SQLite | (banco padrão) |
| HTML/CSS | — |

---

## Estrutura do Projeto

```
Alura-Space/
├── galeria/                  # App principal
│   ├── migrations/
│   ├── admin.py
│   ├── apps.py
│   ├── models.py
│   ├── urls.py
│   └── views.py
├── setup/                    # Configurações do projeto
│   ├── settings.py
│   ├── urls.py
│   ├── wsgi.py
│   ├── asgi.py
│   └── static/
│       ├── assets/
│       │   ├── favicon/
│       │   ├── imagens/
│       │   ├── logo/
│       │   └── ícones/
│       └── styles/
│           └── style.css
├── templates/
│   └── galeria/
│       ├── base.html
│       ├── index.html
│       ├── imagem.html
│       └── partials/
│           └── _footer.html
├── static/                   # Arquivos estáticos coletados
├── manage.py
├── requirements.txt
└── .env
```

---

## Pré-requisitos

- Python 3.8 ou superior
- pip

---

## Instalação e Configuração

**1. Clone o repositório**

```bash
git clone <url-do-repositorio>
cd Alura-Space
```

**2. Crie e ative o ambiente virtual**

```bash
# Windows
python -m venv venv
venv\Scripts\activate

# Linux/macOS
python -m venv venv
source venv/bin/activate
```

**3. Instale as dependências**

```bash
pip install -r requirements.txt
```

**4. Configure as variáveis de ambiente**

Crie um arquivo `.env` na raiz do projeto:

```env
SECRET_KEY = sua-chave-secreta-aqui
```

> ⚠️ Nunca compartilhe ou versione sua `SECRET_KEY` real.

**5. Execute as migrações**

```bash
python manage.py migrate
```

**6. (Opcional) Crie um superusuário para o painel admin**

```bash
python manage.py createsuperuser
```

**7. Colete os arquivos estáticos**

```bash
python manage.py collectstatic
```

---

## Como Executar

```bash
python manage.py runserver
```

Acesse no navegador:

- Galeria: [http://localhost:8000/](http://localhost:8000/)
- Detalhe de imagem: [http://localhost:8000/imagem/](http://localhost:8000/imagem/)
- Painel administrativo: [http://localhost:8000/admin/](http://localhost:8000/admin/)

---

## Rotas da Aplicação

| Rota | View | Descrição |
|---|---|---|
| `/` | `index` | Página principal com a galeria |
| `/imagem/` | `imagem` | Página de detalhe de uma imagem |
| `/admin/` | Django Admin | Painel de administração |

---

Projeto desenvolvido como parte da formação Django na [Alura](https://www.alura.com.br/) 🚀
