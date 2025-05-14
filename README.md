## Template de projeto em Next.js com rotas publicas e autenticadas


## 📁 Estrutura de Pastas

```bash
my-next-project/
│
├── public/                        # Arquivos públicos (imagens, favicon, etc.)
│
├── src/                           # Código-fonte principal
│   ├── app/                       # Estrutura de rotas do Next.js (App Router)
│   |   ├── (private)/             # Pasta estrutural que engloba rotas autenticadas
|   |   |   └── auth/              # Pasta/rota que engloba rotas autenticadas
|   |   |       ├── (home)/        # Pasta estrutural para a home das rotas autenticadas
|   |   |       |   └── Page.tsx   # Arquivo da tela home
|   |   |       └── users/         # Pasta/rota de uma tela de usuários (opcional)
|   |   |           └── Page.tsx   # Arquivo da tela de usuários (opcional)
|   |   ├── (public)/              # Pasta estrutural que engloba todas as rotas publicas
|   |   |   ├── (landing-page)     # Pasta estrutural das telas da landing page
|   |   |   |   └── Page.tsx       # Arquivo para a rota "/" simbolizando a landing page
|   |   |   ├── login/             # Pasta/rota de login
|   |   |   |   └── page.tsx       # Arquivo da tela de login
|   |   |   └── register           # Pasta/rota da tela de cadastro
|   |   |       └── page.tsx       # Arquivo da tela de cadastro
│   |   └── layout.tsx             # Layout raiz
|   |
|   └── middleware.ts              # Middleware execudato a cada acesso, atualização, ou redirecionamento dentro do aplicativo, irá realizar lógicas de validação de autenticação e acesso à rotas públicas e 
|
|
** outras estruturas recomendadas
│   │
│   ├── services/                  # Chamadas de API RESTful
│   │   ├── auth/                  # Chamadas de API referentes a autenticação
|   |   |   └── useLogin.tsx       # Rota de Login
|   |   |   └── useRefresh.tsx     # Rota de refresh token
|   |   |   ...
|   |   └── ...
|   |
│   ├── components/                # Componentes reutilizáveis
│   │   └── Button.tsx             # Exemplo de componente
│   │
│   ├── features/                  # Funcionalidades organizadas por domínio
│   │   └── auth/                  # Ex: login, registro, autenticação
│   │
│   ├── lib/                       # Funções utilitárias e bibliotecas
│   │   └── api.ts                 # Exemplo: cliente fetch/Axios
│   │
│   ├── styles/                    # Arquivos de estilo (CSS/Tailwind/etc)
│   │   └── globals.css            # Estilo global
│   │
│   ├── types/                     # Tipagens TypeScript globais
│   │   └── index.d.ts             # Definições de tipos
│   │
│   └── hooks/                     # React hooks personalizados
│       └── useUser.ts             # Exemplo de hook
**
│
├── .env                    # Variáveis de ambiente
├── next.config.js          # Configuração do Next.js
├── tailwind.config.js      # Configuração do Tailwind CSS (se usar)
├── tsconfig.json           # Configuração do TypeScript
└── package.json            # Dependências e scripts


