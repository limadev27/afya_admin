# afya_admin# Afya Admin — Dashboard com Blazor WebAssembly e MudBlazor

## Identificação

| | |
|---|---|
| **Aluno(a)** | Isac ... (COMPLETE com seu nome completo) |
| **Matrícula** | 000000 |
| **Faculdade** | Afya ... (nome da faculdade) |
| **Curso** | Nome do curso |
| **Disciplina** | Programação de Sistemas Web (confira o nome oficial) |
| **Professor(a)** | Nome do professor(a) |
| **Semestre** | 2026.2 |

## Objetivo do projeto

_ESCREVA AQUI, com suas palavras (2 a 4 parágrafos): o que é o projeto, o que a página faz (sidebar, AppBar, KPIs, gráficos, Performance, Atividades, tabela), que os dados são fictícios e que todo o visual vem do MudBlazor, sem CSS próprio._

## Tecnologias utilizadas

- .NET 10 / Blazor WebAssembly (aplicação autônoma, sem servidor)
- MudBlazor 9 (componentes, tema e classes utilitárias)
- C# e Razor
- Fonte Inter (Google Fonts), aplicada pelo tema
- Git e GitHub (versionamento)
- VS Code com C# Dev Kit

## Como executar

Pré-requisito: **.NET SDK 10** (confira com `dotnet --version`, que deve começar com `10.`).

```bash
git clone https://github.com/SEU-USUARIO/afya-admin.git
cd afya-admin
dotnet watch
```

O terminal mostra a URL (algo como `http://localhost:5147`; a porta pode variar). Use a que aparecer.

## Telas

### Tema claro
![Dashboard — tema claro](docs/prints/tema-claro.png)

### Tema escuro
![Dashboard — tema escuro](docs/prints/tema-escuro.png)

### Versão mobile
![Dashboard — celular](docs/prints/mobile.png)

### HTML gerado (DevTools)
![Inspeção do HTML no DevTools](docs/prints/devtools.png)

_ESCREVA AQUI, olhando o seu print, em poucas linhas: qual elemento você inspecionou (KPI e botão), quais tags HTML o Blazor gerou para `MudPaper`, `MudStack` e `MudButton`, quais classes apareceram (`mud-paper`, `mud-elevation-1`...) e onde aparece o `pa-4` que você escreveu no código._

## Estrutura do projeto

```
afya-admin/
├── Components/
│   ├── AtividadesRecentes.razor
│   ├── CabecalhoPagina.razor
│   ├── DashboardCard.razor
│   ├── GraficoDistribuicaoClientes.razor
│   ├── GraficoReceita.razor
│   ├── KpiCard.razor
│   ├── PerformanceProjetos.razor
│   ├── ProjetosRecentes.razor
│   ├── SeletorPeriodo.razor
│   └── Ui.cs
├── Data/
│   └── DashboardData.cs
├── docs/
│   └── prints/
├── Layout/
│   ├── MainLayout.razor
│   └── NavMenu.razor
├── Pages/
│   ├── Dashboard.razor
│   └── NotFound.razor
├── Properties/launchSettings.json
├── wwwroot/
│   ├── css/app.css
│   ├── img/alex-morgan.jpg
│   └── index.html
├── _Imports.razor
├── afya-admin.csproj
├── App.razor
└── Program.cs
```

- `Components/`: componentes reutilizáveis que desenham cada bloco da tela, mais o `Ui.cs` com funções auxiliares de apresentação.
- `Data/`: modelos (records) e dados fictícios do dashboard.
- `Layout/`: a "moldura" da aplicação (`MainLayout` com AppBar e sidebar, e o `NavMenu`).
- `Pages/`: páginas com rota (`Dashboard` em `/` e `NotFound` para o 404).
- `wwwroot/`: arquivos estáticos servidos ao navegador (`index.html`, imagens, CSS do template).
- `docs/prints/`: imagens usadas neste README.

## Componentes criados

| Componente | Responsabilidade | Parâmetros que recebe |
|---|---|---|
| `DashboardCard` | Card base reutilizável: título, subtítulo, ações, menu "⋮" e conteúdo | `Titulo`, `Subtitulo`, `Acoes`, `Menu`, `ChildContent` |
| `CabecalhoPagina` | Título da página com subtítulo e botões à direita | `Titulo`, `Subtitulo`, `Acoes` |
| `SeletorPeriodo` | Menu em forma de botão para escolher o período | `Opcoes`, `Valor`, `ValorChanged` |
| `KpiCard` | Card de indicador com ícone, valor, variação e sparkline | `Kpi` |
| `GraficoReceita` | Gráfico de linha Receita x Meta | `Meses`, `Receita`, `Meta` |
| `GraficoDistribuicaoClientes` | Gráfico de rosca com o total no centro e legenda própria | `Total`, `Segmentos` |
| `PerformanceProjetos` | Lista de projetos com barras de progresso | `Projetos` |
| `AtividadesRecentes` | Feed de atividades da equipe | `Atividades` |
| `ProjetosRecentes` | Tabela de projetos recentes | `Projetos` |

## O que aprendi

> Responda com suas próprias palavras, mencionando o SEU projeto (nomes de arquivos, componentes, trechos que você digitou). Um parágrafo curto por pergunta.

**1. Como uma aplicação Blazor WebAssembly inicia no navegador? Qual é o papel do `index.html`, da `<div id="app">` e do `Program.cs`?**

_Escreva aqui._

**2. Qual é a diferença entre um Layout, uma Page e um Component neste projeto? Dê um exemplo de cada.**

_Escreva aqui._

**3. O que é um `RenderFragment` e como o `DashboardCard` usa esse recurso para ser reutilizado por vários cards?**

_Escreva aqui._

**4. Como funciona o `@bind-Valor` no `SeletorPeriodo`? Qual é o papel do `ValorChanged`?**

_Escreva aqui._

**5. Por que os dados ficam na pasta `Data`, separados dos componentes? Que vantagem isso traz se, no futuro, os dados vierem de uma API?**

_Escreva aqui._

**6. Como o `MudGrid` com `xs`, `sm` e `lg` faz os cards de KPI se reorganizarem em telas de tamanhos diferentes?**

_Escreva aqui._

**7. Como foi possível estilizar a página inteira sem escrever CSS? Explique o papel do tema (`MudTheme`) e das classes utilitárias.**

_Escreva aqui._

**8. Por que o namespace do projeto é `afya_admin` e não `afya-admin`?**

_Escreva aqui._

## Dificuldades e soluções

_Descreva pelo menos dois problemas reais que VOCÊ enfrentou e como resolveu cada um (sintoma, causa, solução). Dica: lembre do que aconteceu no seu caminho até aqui, por exemplo com os arquivos dos prints ou com o repositório Git._

1. _Escreva aqui._
2. _Escreva aqui._

## Melhorias futuras (opcional)

_Se fez algum desafio da seção 20 do tutorial, descreva aqui. Se não, diga o que implementaria a seguir._