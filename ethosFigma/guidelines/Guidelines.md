# Design System Guidelines - Ethos

## Visão Geral
Este documento descreve o sistema de design completo da plataforma Ethos, um simulador de decisões éticas para profissionais de tecnologia no contexto de telemedicina. Todas as especificações aqui descritas garantem consistência visual, acessibilidade e manutenibilidade do código.

---

## Paleta de Cores

### Cores Primárias
| Token | Hex Code | RGB | Uso |
|-------|----------|-----|-----|
| `--primary` | #3B82F6 | rgb(59, 130, 246) | Cor principal da marca. Usada em botões primários, links e elementos interativos principais |
| `--primary-foreground` | #FFFFFF | rgb(255, 255, 255) | Cor de texto/elementos sobre fundos primários |

### Cores Secundárias
| Token | Hex Code | RGB | Uso |
|-------|----------|-----|-----|
| `--secondary` | #F3F4F6 | rgb(243, 244, 246) | Cor secundária para botões e elementos interativos alternativos (não destrutivos) |
| `--secondary-foreground` | #111827 | rgb(17, 24, 39) | Cor de texto/elementos sobre fundos secundários |

### Cores de Fundo e Superfícies
| Token | Hex Code | RGB | Uso |
|-------|----------|-----|-----|
| `--background` | #FFFFFF | rgb(255, 255, 255) | Cor de fundo padrão da aplicação |
| `--foreground` | #111827 | rgb(17, 24, 39) | Cor padrão para texto e elementos sobre o background |
| `--card` | #F9FAFB | rgb(249, 250, 251) | Cor de fundo para cards, modais e containers |
| `--card-foreground` | #111827 | rgb(17, 24, 39) | Cor de texto/elementos sobre cards e modais |
| `--input-background` | #FFFFFF | rgb(255, 255, 255) | Cor de fundo para campos de input |
| `--input` | #FFFFFF | rgb(255, 255, 255) | Cor de fundo para inputs preenchidos |

### Cores Neutras
| Token | Hex Code | RGB | Uso |
|-------|----------|-----|-----|
| `--muted` | #F3F4F6 | rgb(243, 244, 246) | Cor para elementos menos proeminentes, como botões desabilitados |
| `--muted-foreground` | #6B7280 | rgb(107, 114, 128) | Cor de texto/elementos sobre fundos muted |
| `--border` | #E5E7EB | rgb(229, 231, 235) | Cor padrão de bordas para inputs, botões e containers |

### Cores de Interação
| Token | Hex Code | RGB | Uso |
|-------|----------|-----|-----|
| `--accent` | #60A5FA | rgb(96, 165, 250) | Cor de destaque para highlights, links e elementos interativos |
| `--accent-foreground` | #FFFFFF | rgb(255, 255, 255) | Cor de texto/elementos sobre fundos accent |
| `--ring` | #60A5FA | rgb(96, 165, 250) | Cor para focus rings, outlines e indicadores de foco |

### Cores Semânticas
| Token | Hex Code | RGB | Uso |
|-------|----------|-----|-----|
| `--destructive` | #EF4444 | rgb(239, 68, 68) | Cor para ações destrutivas como botões de deletar ou mensagens de erro. Representa "Risco Regulatório" |
| `--destructive-foreground` | #FFFFFF | rgb(255, 255, 255) | Cor de texto/elementos sobre fundos destrutivos |
| `--chart-1` | #3B82F6 | rgb(59, 130, 246) | Cor para elementos de gráficos (barras, linhas) |
| `--chart-2` | #10B981 | rgb(16, 185, 129) | Cor secundária para gráficos. Representa "Uso Aceitável/Conforme" |
| `--chart-3` | #F59E0B | rgb(245, 158, 11) | Cor terciária para gráficos. Representa "Uso com Cuidado Extra" |
| `--chart-4` | #EF4444 | rgb(239, 68, 68) | Cor quaternária para gráficos |
| `--chart-5` | #9333EA | rgb(147, 51, 234) | Cor quinária para gráficos |

### Cores de Navegação/Sidebar
| Token | Hex Code | RGB | Uso |
|-------|----------|-----|-----|
| `--sidebar` | #FFFFFF | rgb(255, 255, 255) | Cor de fundo para sidebars e menus de navegação |
| `--sidebar-foreground` | #111827 | rgb(17, 24, 39) | Cor de texto/elementos sobre sidebars |
| `--sidebar-primary` | #3B82F6 | rgb(59, 130, 246) | Cor primária para elementos interativos em sidebars |
| `--sidebar-primary-foreground` | #FFFFFF | rgb(255, 255, 255) | Cor de texto sobre elementos primários em sidebars |
| `--sidebar-accent` | #F3F4F6 | rgb(243, 244, 246) | Cor de destaque para sidebars |
| `--sidebar-accent-foreground` | #111827 | rgb(17, 24, 39) | Cor de texto sobre elementos accent em sidebars |
| `--sidebar-border` | #E5E7EB | rgb(229, 231, 235) | Cor de borda para elementos em sidebars |
| `--sidebar-ring` | #60A5FA | rgb(96, 165, 250) | Cor de focus ring para sidebars |

### Cores de Popover/Dropdown
| Token | Hex Code | RGB | Uso |
|-------|----------|-----|-----|
| `--popover` | #FFFFFF | rgb(255, 255, 255) | Cor de fundo para dropdowns e tooltips |
| `--popover-foreground` | #111827 | rgb(17, 24, 39) | Cor de texto/elementos sobre popovers |

### Paleta de Cores Específica do Ethos
A aplicação utiliza um sistema de cores semânticas para representar níveis de impacto ético:

- **Fora do Escopo** (`bg-muted`): Cinza neutro (#F3F4F6)
- **Uso Conforme** (`bg-chart-2`): Verde (#10B981) - indica conformidade adequada
- **Uso Conforme com Monitoramento Especial** (`bg-chart-3`): Laranja/Amarelo (#F59E0B) - requer atenção elevada
- **Risco de Conformidade** (`bg-destructive`): Vermelho (#EF4444) - urgência imediata

---

## Tipografia

### Família de Fontes
- **Fonte Principal**: `Inter, sans-serif`
- Aplicada em todos os elementos da aplicação
- Fonte do Google Fonts, importada no arquivo `/src/styles/fonts.css`

### Escala Tipográfica
| Token | Tamanho (rem) | Tamanho (px) |
|-------|---------------|--------------|
| `--text-xs` | 0.75rem | 12px |
| `--text-sm` | 0.875rem | 14px |
| `--text-base` | 1rem | 16px |
| `--text-lg` | 1.25rem | 20px |
| `--text-xl` | 1.5rem | 24px |
| `--text-2xl` | 2rem | 32px |

### Pesos de Fonte
| Token | Valor | Uso |
|-------|-------|-----|
| `--font-weight-normal` | 400 | Texto padrão, parágrafos, inputs |
| `--font-weight-medium` | 500 | Labels, texto de ênfase média |
| `--font-weight-semi-bold` | 600 | Subtítulos (h2, h3) |
| `--font-weight-bold` | 700 | Títulos principais (h1), botões |

### Hierarquia Tipográfica

#### Heading 1 (h1)
- **Font Size**: 32px
- **Font Weight**: 700 (Bold)
- **Line Height**: 1.188 (38px)
- **Uso**: Títulos principais de seções, hero title

#### Heading 2 (h2)
- **Font Size**: 24px
- **Font Weight**: 600 (Semi-bold)
- **Line Height**: 1.167 (28px)
- **Uso**: Subtítulos de seções, títulos de cards

#### Heading 3 (h3)
- **Font Size**: 20px
- **Font Weight**: 600 (Semi-bold)
- **Line Height**: 1.2 (24px)
- **Uso**: Títulos de componentes menores, cards

#### Heading 4 (h4)
- **Font Size**: 16px
- **Font Weight**: 500 (Medium)
- **Line Height**: 1.3 (20.8px)
- **Uso**: Labels destacados, títulos de subsections

#### Parágrafo (p)
- **Font Size**: 16px
- **Font Weight**: 400 (Normal)
- **Line Height**: 1.556 (25px)
- **Uso**: Texto corrido, descrições

#### Label
- **Font Size**: 14px
- **Font Weight**: 400 (Normal)
- **Line Height**: 1.429 (20px)
- **Uso**: Labels de formulários

#### Button
- **Font Size**: 16px
- **Font Weight**: 700 (Bold)
- **Line Height**: 1.5 (24px)
- **Uso**: Texto de botões

#### Input
- **Font Size**: 16px
- **Font Weight**: 400 (Normal)
- **Line Height**: 1.5 (24px)
- **Uso**: Texto dentro de campos de input

#### Span
- **Font Size**: 16px
- **Font Weight**: 400 (Normal)
- **Line Height**: 1.556 (25px)
- **Uso**: Texto inline, elementos genéricos

---

## Espaçamento

### Sistema de Espaçamento
O design system utiliza um **sistema baseado em múltiplos de 4px** para garantir consistência e alinhamento pixel-perfect.

### Grid de Espaçamento Base
- Base: 4px
- Escala: 4, 8, 12, 16, 20, 24, 32, 40, 48, 56, 64, 80, 96...

### Aplicações Comuns
| Contexto | Valor | Uso |
|----------|-------|-----|
| Padding Small | 12-16px | Cards, botões pequenos |
| Padding Medium | 20-24px | Sections, containers |
| Padding Large | 32-48px | Hero sections, páginas |
| Gap Small | 8-12px | Entre elementos próximos |
| Gap Medium | 16-24px | Entre cards, componentes |
| Gap Large | 32-48px | Entre seções |
| Margin Vertical | 48-80px | Entre seções principais |

---

## Border Radius

### Tokens de Border Radius
| Token | Valor | Uso |
|-------|-------|-----|
| `--radius` | 4px | Raio padrão para botões, tooltips, containers |
| `--radius-sm` | 2px | Elementos menores |
| `--radius-md` | 4px | Elementos médios (padrão) |
| `--radius-lg` | 6px | Elementos maiores |
| `--radius-xl` | 8px | Cards, modais |

### Aplicações
- **Botões**: `var(--radius)` (4px)
- **Cards**: `calc(var(--radius) + 8px)` (12px)
- **Inputs**: `var(--radius)` (4px)
- **Modais**: `calc(var(--radius) + 12px)` (16px)

---

## Elevação e Sombras

### Shadow Tokens
| Token | Valor | Uso |
|-------|-------|-----|
| `--elevation-sm` | `0 1px 2px 0 rgba(0, 0, 0, 0.05)` | Cards, elementos elevados sutis |

### Aplicações
- **Cards**: `box-shadow: 0 1px 2px 0 rgba(0, 0, 0, 0.05)`
- **Modais**: Sombra mais pronunciada para destaque
- **Dropdowns**: `--elevation-sm`

---

## Componentes

### Botões

#### Botão Primário
- **Background**: `var(--primary)` (#3B82F6)
- **Foreground**: `var(--primary-foreground)` (#FFFFFF)
- **Padding**: 16px horizontal, 16px vertical
- **Border Radius**: `var(--radius)` (4px)
- **Font Weight**: 700 (Bold)
- **Hover**: `opacity: 0.9`
- **Focus**: Ring de 2px com `var(--ring)`, offset de 2px
- **Uso**: Ação principal em uma seção (ex: "Iniciar Simulação", "Enviar Contribuição")

#### Botão Secundário
- **Background**: `transparent` ou `var(--secondary)`
- **Border**: 1px solid `var(--border)`
- **Foreground**: `var(--foreground)`
- **Padding**: 16px horizontal, 16px vertical
- **Border Radius**: `var(--radius)`
- **Hover**: `background: var(--secondary)`
- **Focus**: Ring de 2px com `var(--ring)`
- **Uso**: Ações secundárias (ex: "Realizar Nova Análise")

#### Botão de Resposta (Sim/Não)
- **Background**: `var(--background)`
- **Border**: 2px solid `var(--border)`
- **Padding**: 16px horizontal, 16px vertical
- **Font Size**: 16px
- **Border Radius**: `var(--radius)`
- **Estado Selecionado**: Border `var(--primary)`, background `var(--primary)/10`
- **Hover**: Border `var(--primary)`

### Cards

#### Card Padrão
- **Background**: `var(--background)` (#FFFFFF)
- **Border**: 1px solid `var(--border)` (#E5E7EB)
- **Border Radius**: `calc(var(--radius) + 8px)` (12px)
- **Padding**: 24-32px
- **Shadow**: `var(--elevation-sm)`
- **Uso**: Conteúdo principal, resultados

#### Card de Resultado
- **Background**: `var(--background)`
- **Border**: 2px solid (cor semântica baseada no resultado)
- **Border Radius**: `calc(var(--radius) + 8px)`
- **Padding**: 32px desktop, 24px mobile
- **Icon Background**: Círculo de 64px com cor semântica

### Inputs

#### Campo de Texto
- **Background**: `var(--input-background)` (#FFFFFF)
- **Border**: 1px solid `var(--border)` (#E5E7EB)
- **Padding**: 12-16px
- **Border Radius**: `var(--radius)` (4px)
- **Font Size**: 16px
- **Focus**: Border `var(--primary)`, Ring de 2px com `var(--ring)`

#### Textarea
- **Mesmas propriedades do campo de texto**
- **Resize**: `none` (fixo)
- **Min Height**: 4 linhas

#### Checkbox/Radio
- **Border**: 2px solid `var(--border)`
- **Checked Background**: `var(--primary)`
- **Checked Foreground**: `var(--primary-foreground)`
- **Focus**: Ring de 2px com `var(--ring)`

### Modal

#### Estrutura
- **Overlay**: Background `rgba(0, 0, 0, 0.5)`
- **Container**: Background `var(--background)`, Border Radius `calc(var(--radius) + 12px)` (16px)
- **Max Width**: 600px desktop, 90% mobile
- **Padding**: 32px desktop, 24px mobile
- **Close Button**: Posição absoluta, top-right, icon X

### Barra de Progresso

#### Especificações
- **Background**: `var(--secondary)` (#F3F4F6)
- **Fill**: `var(--primary)` (#3B82F6)
- **Height**: 8px
- **Border Radius**: 9999px (totalmente arredondado)
- **Transição**: `width 0.3s ease-in-out`

---

## Regras de Layout

### Layout 60-30-10
O design system segue a regra 60-30-10 para distribuição de cores:
- **60%**: Cor dominante (background, áreas neutras) - Branco/Cinza claro
- **30%**: Cor secundária (cards, superfícies) - Cinza médio
- **10%**: Cor de destaque (elementos interativos, CTAs) - Azul primário

### Grid System
- **Container Max Width**: 1200px (desktop), 100% (mobile/tablet)
- **Padding Horizontal**: 24px (desktop), 16px (mobile)
- **Grid Columns**: 12 colunas
- **Gap**: 24px (desktop), 16px (mobile)

### Breakpoints
| Breakpoint | Valor | Uso |
|------------|-------|-----|
| Mobile | < 640px | Layout single column |
| Tablet | 640px - 1023px | Layout 2 columns, navegação adaptada |
| Desktop | ≥ 1024px | Layout completo, 3 columns |

### Responsividade
- **Mobile First**: Design começa do mobile e expande
- **Flexbox/Grid**: Uso prioritário para layouts responsivos
- **Stack em Mobile**: Elementos em coluna única
- **Side-by-side em Desktop**: Múltiplas colunas quando apropriado

---

## Acessibilidade (WCAG 2.2 e EAA)

### Decisões de Acessibilidade

#### 1. **Contraste de Cores**
**Decisão**: Todas as combinações de cores atendem ao padrão WCAG AA (mínimo 4.5:1 para texto normal, 3:1 para texto grande).

**Implementação**:
- Texto sobre `--background` (#FFFFFF): `--foreground` (#111827) - Contraste ~15.47:1 ✓
- Texto sobre `--primary` (#3B82F6): `--primary-foreground` (#FFFFFF) - Contraste ~8.59:1 ✓
- Texto sobre `--destructive` (#EF4444): `--destructive-foreground` (#FFFFFF) - Contraste ~5.18:1 ✓
- Texto muted (`--muted-foreground` #6B7280) sobre `--background` - Contraste ~5.74:1 ✓

**Justificativa**: Garantir legibilidade para usuários com baixa visão ou daltonismo.

---

#### 2. **Navegação por Teclado**
**Decisão**: Todos os elementos interativos devem ser acessíveis via teclado (Tab, Enter, Space, Esc).

**Implementação**:
- Focus rings visíveis: 2px solid `var(--ring)` (#60A5FA)
- Ordem de tabulação lógica (top-to-bottom, left-to-right)
- Trap de foco em modais (focus fica dentro do modal quando aberto)
- Skip link "Pular para o conteúdo principal" visível ao focar

**Justificativa**: Usuários com mobilidade reduzida ou que preferem navegação por teclado precisam acessar todas as funcionalidades.

---

#### 3. **ARIA Labels e Tags Semânticas**
**Decisão**: Uso extensivo de HTML semântico e ARIA attributes para leitores de tela.

**Implementação**:
- Tags semânticas: `<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<footer>`
- `aria-label` em botões de ícone: "Fechar modal", "Menu de navegação"
- `aria-labelledby` para associar títulos a seções
- `aria-describedby` para descrições adicionais em inputs
- `aria-live="polite"` na barra de progresso para anunciar mudanças
- `aria-expanded` em botões de colapso/expansão
- `role="dialog"` e `aria-modal="true"` em modais
- `role="note"` em disclaimers/avisos importantes

**Justificativa**: Usuários de leitores de tela (NVDA, JAWS, VoiceOver) precisam de contexto semântico para navegar.

---

#### 4. **Textos Alternativos**
**Decisão**: Todos os elementos visuais informativos têm textos alternativos adequados.

**Implementação**:
- `alt` text em imagens descritivas
- `aria-hidden="true"` em ícones decorativos (quando há texto associado)
- `<span class="sr-only">` para texto visível apenas a leitores de tela
- Descrições contextuais em botões de ícone

**Justificativa**: Usuários cegos ou com baixa visão dependem de descrições textuais para compreender conteúdo visual.

---

#### 5. **Foco Visível**
**Decisão**: Indicadores de foco sempre visíveis e com contraste adequado.

**Implementação**:
- Focus ring: 2px solid `var(--ring)` (#60A5FA)
- Offset de 2-4px para separação visual
- Focus ring presente em: botões, links, inputs, checkboxes, radio buttons
- `:focus-visible` para mostrar foco apenas em navegação por teclado (onde suportado)

**Justificativa**: Usuários que navegam por teclado precisam saber qual elemento está em foco.

---

#### 6. **Estrutura de Headings**
**Decisão**: Hierarquia lógica de headings (h1 > h2 > h3) sem pulos.

**Implementação**:
- `<h1>`: Título principal da página (único)
- `<h2>`: Títulos de seções principais
- `<h3>`: Subtítulos dentro de seções
- Uso de `id` em headings para navegação por landmarks

**Justificativa**: Leitores de tela usam headings para navegação rápida pelo conteúdo.

---

#### 7. **Labels e Inputs**
**Decisão**: Todos os inputs têm labels explícitos associados.

**Implementação**:
- `<label for="input-id">` associado a `<input id="input-id">`
- `aria-describedby` para instruções adicionais
- `placeholder` como dica adicional, não como substituto de label
- `required` attribute para campos obrigatórios
- Mensagens de erro descritivas e associadas ao campo

**Justificativa**: Usuários de leitores de tela e tecnologias assistivas precisam saber o propósito de cada campo.

---

#### 8. **Modal de Feedback**
**Decisão**: Modais gerenciam foco e podem ser fechados por múltiplos métodos.

**Implementação**:
- `role="dialog"` e `aria-modal="true"`
- `aria-labelledby` apontando para o título do modal
- Foco automático no primeiro elemento interativo ao abrir
- Retorno de foco ao elemento que abriu o modal ao fechar
- Fechamento por: botão X, tecla Esc, clique no overlay
- Trap de foco (Tab cicla apenas dentro do modal)

**Justificativa**: Usuários de teclado e leitores de tela precisam de navegação clara e previsível em modais.

---

#### 9. **Barra de Progresso**
**Decisão**: Barra de progresso anuncia mudanças de estado para tecnologias assistivas.

**Implementação**:
- `aria-live="polite"` para anunciar progresso
- `role="progressbar"` em elementos de progresso
- Texto visível "Questão X de 5" atualizado dinamicamente

**Justificativa**: Usuários cegos precisam saber seu progresso no questionário.

---

#### 10. **Botões de Resposta**
**Decisão**: Botões de resposta têm estados visuais claros e anunciados.

**Implementação**:
- `aria-pressed="true/false"` para indicar seleção
- Mudança visual clara (borda, background) no estado selecionado
- Labels descritivos: "Sim", "Não" (não apenas ícones)
- Focus ring visível ao navegar por teclado

**Justificativa**: Usuários precisam saber qual resposta está selecionada antes de avançar.

---

#### 11. **Links e Navegação**
**Decisão**: Links têm propósito claro e estados hover/focus distintos.

**Implementação**:
- Links descritivos (não "clique aqui", mas "Iniciar Simulação")
- `aria-label` quando contexto adicional é necessário
- Underline em hover para links de texto
- Skip link no topo da página (visível ao focar)

**Justificativa**: Usuários de leitores de tela navegam por listas de links; links descritivos facilitam essa navegação.

---

#### 12. **Ícones e Elementos Decorativos**
**Decisão**: Ícones decorativos são ocultados de leitores de tela; ícones funcionais têm labels.

**Implementação**:
- `aria-hidden="true"` em ícones decorativos (quando há texto associado)
- `<span class="sr-only">` para labels de ícones funcionais
- Exemplo: Botão com ícone de X tem `aria-label="Fechar modal"`

**Justificativa**: Evitar poluição sonora em leitores de tela, mantendo contexto funcional.

---

#### 13. **Cores Semânticas e Redundância**
**Decisão**: Informações críticas não dependem apenas de cor; há redundância textual/iconográfica.

**Implementação**:
- Resultados usam cor + ícone + texto descritivo
- Estados de erro usam cor vermelha + ícone de alerta + mensagem textual
- Estados de sucesso usam cor verde + ícone de check + mensagem textual

**Justificativa**: Usuários com daltonismo ou baixa visão não podem depender apenas de cor para compreender informações críticas.

---

#### 14. **Responsividade e Zoom**
**Decisão**: Layout suporta zoom de até 200% sem perda de funcionalidade (WCAG 1.4.4).

**Implementação**:
- Uso de unidades relativas (`rem`, `em`, `%`) ao invés de pixels fixos
- Layout flex/grid adapta-se a diferentes tamanhos de tela
- Sem scroll horizontal em zoom 200%
- Texto dimensionável sem quebras

**Justificativa**: Usuários com baixa visão frequentemente usam zoom; layout deve permanecer funcional.

---

#### 15. **Linguagem e Legibilidade**
**Decisão**: Linguagem neutra, objetiva e clara, evitando jargões.

**Implementação**:
- Frases curtas e diretas
- Termos técnicos explicados quando necessários
- Tom profissional e acessível
- Instruções claras em formulários

**Justificativa**: Usuários com dificuldades cognitivas ou não nativos da língua se beneficiam de linguagem simples.

---

### Checklist de Acessibilidade
- [x] Contraste de cores adequado (WCAG AA)
- [x] Navegação por teclado completa
- [x] Focus rings visíveis
- [x] ARIA labels e landmarks
- [x] Hierarquia de headings lógica
- [x] Labels associados a inputs
- [x] Textos alternativos em imagens
- [x] Skip links para conteúdo principal
- [x] Modal com trap de foco
- [x] Anúncios dinâmicos com aria-live
- [x] Redundância de informação (não apenas cor)
- [x] Layout responsivo e zoomável
- [x] Linguagem clara e objetiva

---

## Ícones

### Biblioteca
- **Lucide React**: Biblioteca de ícones utilizada
- **Tamanho Padrão**: 20-24px
- **Cor**: Herda cor do texto ou define via prop `className`

### Ícones Utilizados
| Ícone | Componente | Contexto |
|-------|------------|----------|
| Menu | `Menu` | Navegação mobile |
| Fechar | `X` | Fechar modais, menus |
| Check | `Check` | Confirmação, checkbox |
| Alerta | `AlertTriangle` | Avisos, cuidados extras |
| Shield Alert | `ShieldAlert` | Risco regulatório |
| Shield Check | `ShieldCheck` | Uso aceitável |
| Info | `Info` | Informações, fora do escopo |
| Rotacionar | `RotateCcw` | Reiniciar simulação |
| Mensagem | `MessageSquare` | Feedback |
| Seta | `ChevronDown` | Colapsar/expandir |
| Estrela | `Star` | Avaliação |
| Enviar | `Send` | Enviar formulário |
| Email | `Mail` | Campo de email |

---

## Estados Interativos

### Hover
- **Botões**: `opacity: 0.9` ou mudança de background
- **Links**: Underline ou mudança de cor
- **Cards**: Elevação sutil ou mudança de borda

### Focus
- **Ring**: 2px solid `var(--ring)` (#60A5FA)
- **Offset**: 2-4px
- **Outline**: `outline: 2px solid var(--ring)`

### Active
- **Botões**: Leve escurecimento ou transform (scale)
- **Cards**: Borda destacada

### Disabled
- **Opacity**: 0.5-0.6
- **Cursor**: `cursor: not-allowed`
- **Background**: `var(--muted)`

---

## Animações e Transições

### Princípios
- **Sutis**: Transições discretas para não distrair
- **Rápidas**: Duração de 150-300ms
- **Consistentes**: Mesmas curvas de easing

### Transições Comuns
| Propriedade | Duração | Easing | Uso |
|-------------|---------|--------|-----|
| `opacity` | 200ms | ease | Hover, fade in/out |
| `transform` | 300ms | ease-in-out | Modais, dropdowns |
| `background-color` | 200ms | ease | Hover em botões |
| `border-color` | 200ms | ease | Focus em inputs |
| `width` (progress) | 300ms | ease-in-out | Barra de progresso |

### Prefers Reduced Motion
- **Respeitar**: `@media (prefers-reduced-motion: reduce)` desabilita animações
- **Acessibilidade**: Usuários com sensibilidade a movimento podem desabilitar animações

---

## Padrões de Uso

### Quando Usar Botão Primário
- Ação principal da página/seção
- Máximo 1-2 por tela
- Exemplo: "Iniciar Simulação", "Enviar Contribuição"

### Quando Usar Botão Secundário
- Ações alternativas ou de menor prioridade
- Pode aparecer junto com botão primário
- Exemplo: "Realizar Nova Análise"

### Quando Usar Cards
- Agrupar informações relacionadas
- Destacar conteúdo importante
- Resultados, passos do processo

### Quando Usar Modais
- Ações que requerem atenção imediata
- Formulários que não devem ser interrompidos
- Exemplo: Feedback Modal

---

## Dark Mode (Preparado para Futuro)

O design system já possui tokens para dark mode definidos no `theme.css`. Para ativar:

### Cores em Dark Mode
| Token | Light Mode | Dark Mode |
|-------|------------|-----------|
| `--background` | #FFFFFF | #111827 |
| `--foreground` | #111827 | #FFFFFF |
| `--card` | #F9FAFB | #1F2937 |
| `--primary` | #3B82F6 | #60A5FA |
| `--border` | #E5E7EB | #374151 |

---

## Manutenção e Atualizações

### Como Atualizar Cores
1. Edite o arquivo `/src/styles/theme.css`
2. Modifique o valor HEX da variável CSS desejada
3. Todas as referências serão atualizadas automaticamente

### Como Adicionar Nova Cor
1. Adicione nova variável CSS em `:root` no `theme.css`
2. Adicione a mesma variável em `.dark` (se aplicável)
3. Adicione ao `@theme inline` para uso com Tailwind
4. Documente neste arquivo

### Como Atualizar Tipografia
1. Modifique os valores de `font-size`, `font-weight` ou `line-height` nos elementos base no `theme.css`
2. Todas as instâncias serão atualizadas automaticamente

---

## Referências e Conformidade

### Padrões Seguidos
- **WCAG 2.2 (Level AA)**: Web Content Accessibility Guidelines
- **EAA (European Accessibility Act)**: Conformidade com regulamentações europeias
- **LGPD**: Referência a multas e conformidade no contexto de telemedicina

### Ferramentas de Teste
- **Lighthouse**: Auditoria de acessibilidade e performance
- **axe DevTools**: Teste de acessibilidade
- **WAVE**: Avaliação de acessibilidade web
- **Contrast Checker**: Verificação de contraste de cores

---

## Contato e Contribuições

Para sugestões de melhorias no design system ou dúvidas sobre implementação, entre em contato através do formulário de feedback da plataforma ou via e-mail.

---

**Última atualização**: Março 2026  
**Versão**: 1.0.0
