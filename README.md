# Arquitetura de Pastas para Projetos React
Esta documento descreve a estrutura de pastas recomendada para projetos React, visando facilitar a organização, a escalabilidade e a manutenção do código.

## Estrutura de Pastas
### Raiz do Projeto

```
/my-react-app
├── public
├── src
│   ├── assets
│   ├── components
│   ├── containers
│   ├── contexts
│   ├── hooks
│   ├── pages
│   ├── routes
│   ├── services
│   ├── styles
│   ├── utils
│   ├── App.ts
│   ├── index.ts
│   ├── reportWebVitals.ts
│   └── setupTests.ts
├── .gitignore
├── package.json
├── README.md
└── package-lock.json
```

### Descrição das Pastas e Arquivos
**public/**: Contém arquivos públicos que não são processados pelo Webpack. Normalmente, contém o arquivo index.html e outros recursos estáticos.

**src/**: Contém todo o código fonte do projeto.

- **assets/:** Contém imagens, fontes, ícones e outros recursos estáticos.
```
/assets
├── images
├── fonts
└── icons
```

- **components/:** Contém componentes reutilizáveis e pequenos, que não estão diretamente ligados a uma página específica. Dividido em subpastas por funcionalidade ou tipo de componente.
```
/components
├── Button
│   ├── index.ts
│   ├── Button.tsx
│   ├── Button.styles.ts
│   ├── Button.types.ts
│   ├── Button.spec.ts
└── Navbar
    ├── index.ts
    ├── Navbar.tsx
    ├── Navbar.styles.ts
    ├── Navbar.types.ts
    ├── Navbar.spec.ts
```

- **containers/:** Contém componentes de ordem superior (HOCs) ou componentes que conectam os componentes de apresentação aos estados globais (como Redux).
```
/containers
└── DashboardContainer
    ├── index.ts
    ├── DashboardContainer.tsx
    ├── DashboardContainer.styles.ts
    ├── DashboardContainer.types.ts
    ├── DashboardContainer.spec.ts
```

- **contexts/:** Contém contextos criados com a API de Contexto do React.
```
/contexts
└── AuthContext
|   ├── index.ts
│   ├── AuthContext.tsx
│   ├── AuthContext.types.ts
└── ThemeContext.ts
    ├── index.ts
    ├── ThemeContext.tsx
    ├── ThemeContext.types.ts
```

- **hooks/:** Contém hooks personalizados que encapsulam lógica reutilizável.
```
/hooks
├── useAuth
|   ├── index.ts
|   ├── useAuth.ts
|   ├── useAuth.types.ts
└── useFetch
    ├── index.ts
    ├── useFetch.ts
    ├── useFetch.types.ts
```

- **pages/:** Contém componentes de página. Cada página é um componente que representa uma rota específica.
```
/pages
├── HomePage
│   ├── index.tsx
│   ├── HomePage.tsx
│   ├── HomePage.styles.ts
│   ├── HomePage.types.ts
│   ├── HomePage.spec.ts
├── LoginPage
│   ├── index.tsx
│   ├── LoginPage.tsx
│   ├── LoginPage.styles.ts
│   ├── LoginPage.types.ts
│   ├── LoginPage.spec.ts
└── DashboardPage
    ├── index.tsx
    ├── DashboardPage.tsx
    ├── DashboardPage.styles.ts
    ├── DashboardPage.types.ts
    ├── DashboardPage.spec.ts
```

- **routes/:** Contém a configuração de rotas da aplicação.
```
/routes
└── AppRoutes.ts
```

- **services/:** Contém lógica de interação com APIs ou outras funcionalidades externas.
```
/services
├── api.ts
└── auth
    ├── auth.ts
    ├── auth.types.ts
```

- **styles/:** Contém estilos globais da aplicação.
```
/styles
├── variables.css
└── global.css
```

- **utils/:** Contém funções utilitárias e helpers que são reutilizados em várias partes do aplicativo.
```
/utils
├── formatDate
|   ├── index.ts
|   ├── types.ts
└── calculateAge
    ├── index.ts
    ├── types.ts
```

**App.tsx:** Componente raiz da aplicação, onde geralmente são configurados provedores de estado e rotas principais.

**index.ts:** Ponto de entrada da aplicação React. Este arquivo renderiza o componente App na árvore DOM.

**reportWebVitals.ts:** Utilizado para medir a performance da aplicação (opcional).

**setupTests.ts:** Configuração para testes, utilizado pelo Jest (opcional).

**Arquivos de Configuração e Metadados**
.gitignore: Lista de arquivos e pastas que o Git deve ignorar.
package.json: Contém metadados do projeto e dependências.
README.md: Documentação do projeto.
CHANGELOG.md: Detalhes do versionamento do projeto.
package-lock.json: Lockfile de dependências, gerado automaticamente pelo gerenciador de pacotes.
