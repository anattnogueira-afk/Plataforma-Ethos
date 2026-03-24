# Plataforma Ethos

**Visão do Produto:** Para empresas de tecnologia que não têm equipe de compliance, cujos usuários têm dificuldade de prever situações éticas futuras ou inéditas que podem causar problemas sensíveis para usuários e para a imagem da empresa. A Plataforma Ethos é uma plataforma de consulta sobre ética para empresas de tecnologia que expõe futuros problemas éticos e/ou inéditos e propõe uma tomada de decisão em menor tempo — diferentemente das soluções genéricas sem validação social e de plataformas com comunicação muito técnica. O nosso produto é uma trilha que exclui más decisões e atribui notas de impacto para cada parâmetro definido.

**Persona Cláudia:** Profissional de tecnologia em PME de software, 38 anos, atua no desenvolvimento de sistemas em ambiente ágil e de múltiplos projetos, participa de decisões técnicas. Discute decisões éticas em grupo, analisa padrões e recorrências, não casos isolados, toma decisões com base em boas práticas, valoriza soluções práticas e objetivas. Necessidade: avaliar decisões técnicas sob ótica ética, integração ao fluxo de desenvolvimento, não possui suporte na empresa sobre questões éticas, diretrizes éticas claras e aplicáveis, validação simples de conformidade ética, segurança psicológica.

---

## Backend — `ethos-api`

> Repositório: [LucasMCFidelis/ethos-api](https://github.com/LucasMCFidelis/ethos-api)

API REST da Plataforma Ethos, responsável por toda a lógica de negócio, persistência de dados e exposição dos endpoints consumidos pelo frontend.

### Stack

| Camada | Tecnologia |
|---|---|
| Runtime | Node.js 24 |
| Framework | Fastify 5 |
| Linguagem | TypeScript 5 |
| ORM | Prisma 7 |
| Banco de dados | PostgreSQL |
| Validação | Zod |
| Documentação | Swagger (OpenAPI 3.0) via `@fastify/swagger` |
| Linting / Format | ESLint + Prettier |
| CI/CD | GitHub Actions |
| Deploy | Render |

### Estrutura

```
src/
├── app.ts            ← inicialização do servidor Fastify e registro de plugins
├── lib/
│   └── prisma.ts     ← instância do Prisma Client
├── plugins/
│   ├── config.ts     ← variáveis de ambiente via @fastify/env
│   └── swagger.ts    ← configuração do Swagger UI
└── routes/
    └── health.ts     ← endpoint de health check da API e do banco
prisma/
└── schema.prisma     ← definição do schema do banco de dados
```

### Scripts principais

```bash
npm run dev              # inicia em modo desenvolvimento com hot-reload (tsx watch)
npm run build            # compila TypeScript para JavaScript
npm run start            # executa o build de produção
npm run db:generate      # gera o Prisma Client
npm run db:migrate       # executa migrations em desenvolvimento
npm run db:migrate:prod  # executa migrations em produção
npm run db:studio        # abre o Prisma Studio
```

### URLs

| Ambiente | URL |
|---|---|
| Desenvolvimento | https://ethos-api-develop.onrender.com |
| Produção | `<!-- URL de produção -->` |
| Documentação (Swagger) | https://ethos-api-develop.onrender.com/api/v1/docs |

---

## Frontend — `ethos-frontend`

> Repositório: [LucasMCFidelis/ethos-frontend](https://github.com/LucasMCFidelis/ethos-frontend)

Interface web da Plataforma Ethos, responsável pela experiência do usuário na consulta e avaliação de cenários éticos, exibição de trilhas de decisão e visualização dos impactos atribuídos a cada parâmetro analisado.

### Stack

| Camada | Tecnologia |
|---|---|
| Framework | React 18 |
| Bundler | Vite 5 (com plugin SWC) |
| Linguagem | TypeScript 5 |
| Estilização | Tailwind CSS 3 |
| Componentes UI | shadcn/ui (Radix UI primitives) |
| Roteamento | React Router DOM v6 |
| Formulários | React Hook Form + Zod |
| Data fetching | TanStack Query (React Query) v5 |
| Temas | next-themes |
| Geração assistida | [Lovable](https://lovable.dev) (`lovable-tagger`) |
| Testes unitários | Vitest + Testing Library |

### Estrutura

```
src/
├── App.tsx                  ← componente raiz e configuração de rotas
├── main.tsx                 ← ponto de entrada da aplicação
├── components/
│   ├── .tsx                 ← componentes personalizados
│   └── ui/                  ← componentes shadcn/ui (gerados via CLI)
├── hooks/
├── pages/
├── test/
│   ├── setup.ts             ← configuração global dos testes
│   └── example.test.ts      ← testes de exemplo
public/                      ← assets estáticos
```

> Os arquivos `playwright.config.ts` e `playwright-fixture.ts` são configurações de testes E2E geradas automaticamente pela plataforma Lovable e não fazem parte do fluxo de desenvolvimento deste projeto.

### Sobre o Lovable

O frontend será estruturado e desenvolvido principalmente usando o Lovable, plataforma de desenvolvimento assistido por IA, com desenvolvimento complementar e interação com a API do backend realizado diretamente no código.

### Scripts principais

```bash
npm run dev           # inicia em modo desenvolvimento
npm run build         # gera o build de produção
npm run build:dev     # gera o build em modo development
npm run preview       # serve o build localmente para preview
npm run test          # executa os testes unitários (Vitest)
npm run lint          # verifica o código com ESLint
```

### URLs

| Ambiente | URL |
|---|---|
| Desenvolvimento | https://ethos-frontend-develop.onrender.com |
| Produção | `<!-- URL de produção -->` |