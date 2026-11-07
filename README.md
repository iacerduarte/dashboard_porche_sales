# 🏁 Porsche Sales Dashboard

> Um painel analítico de alta performance para monitoramento de vendas de veículos Porsche, desenvolvido com Inteligência Artificial e inspirado na sofisticação, elegância e minimalismo do site oficial da **Porsche Brasil**.

Esse projeto foi desenvolvido como parte de um desafio prático de dados, aplicando técnicas de engenharia de prompt com **ChatGPT (Canvas)** para consolidar e visualizar os resultados de uma base de dados sanitizada de 100 vendas.

📦 **Link do Repositório:** `https://github.com`  
🌐 **Dashboard em Produção:** `https://iacerduarte.github.io/dashboard_porche_sales`

---

## 📊 Perguntas de Negócio & KPIs Escolhidos

A inteligência de um painel de dados reside na sua capacidade de responder a dores de negócio, e não apenas acumular gráficos. Para este painel, foram selecionadas as seguintes perguntas:

1. **Quais os principais modelos de carro vendido por cidade?**
   * *Motivo:* Permite ao time de marketing entender quais praças possuem maior afinidade com veículos específicos (ex: Porsche 911 vs. Cayenne), otimizando a distribuição e alocação de estoque por praça.
2. **Qual o ano de modelo (Model Year) de carro mais saiu em um período?**
   * *Motivo:* Identifica se o mercado está absorvendo mais os lançamentos do ano corrente ou se há forte demanda por seminovos de anos anteriores, direcionando as campanhas de captação e precificação.
3. **Quais os insights de vendas de carros populares (modelos de entrada/maior volume) com base nos dados de cada cidade?**
   * *Motivo:* Localiza quais regiões geográficas possuem maior volume de vendas para os modelos de entrada (foco em market share), permitindo diferenciar estratégias de volume versus estratégias de hiperluxo.
4. **Volume de Vendas por Estado (State)**
   * *Motivo:* Uma visão macro-regional fundamental para a liderança nacional mapear a concentração de receita e expansão de concessionárias.

### 📈 Indicadores de Topo (KPIs)
* **Total de Vendas Realizadas** (Volume absoluto)
* **Faturamento Bruto Total** (Receita acumulada em R\$)
* **Ticket Médio** (Valor médio gasto por transação)

---

## ⚙️ Tratamento e Preparação da Base de Dados

Antes de alimentar a Inteligência Artificial, a planilha original passou por um processo rigoroso de higienização no *Curso Criando Agentes de Tratamento de Dados*:

* **Filtro de Consistência:** Isolamos apenas as colunas que continham dados perfeitamente sanitizados.
* **Conversão de Tipos:** Valores monetários de preço e anos dos modelos foram convertidos de texto puro para o formato estritamente numérico.
* **Remoção de Fórmulas:** Todos os dados foram colados exclusivamente como "Valores" para eliminar dependências de fórmulas quebradas ou erros de referência (`#REF!`).
* **Anonimização e Segurança:** Garantia total de que nenhum dado sensível ou de clientes reais foi exposto, mantendo os registros embutidos de forma segura no código da aplicação.

---

## 🤖 Engenharia de Prompt e Refinamento (ChatGPT + Canvas)

O desenvolvimento utilizou a interface **ChatGPT Plus com Canvas**, que permitiu a criação e o refinamento do código HTML/JS em tempo real de forma interativa. 

### O Prompt Inicial Utilizado:
```text
Atue como um Desenvolvedor Front-End Sênior e Especialista em UI/UX. 
Crie uma dashboard de vendas para a marca Porsche em um único arquivo HTML estruturado.
Utilize a biblioteca Chart.js para renderizar os gráficos de forma limpa e dinâmica.
A base de dados de 100 vendas está fornecida abaixo e deve ser embutida diretamente no JavaScript como um array de objetos.

Planilha base Porche (sanitizada).xlsx

Diretrizes Visuais (Inspirado no site da Porsche Brasil):
- Paleta de cores: Fundo majoritariamente branco, tons de cinza muito claro (#F8F9FA) para os cards, tipografia e detalhes em preto profundo, e vermelho Porsche clássico (#D5001C) usado estritamente como cor de destaque (highlights/botões selecionados).
- Tipografia: Serifada ou Sans-serif extremamente limpa, refinada, com espaçamento elegante.

Funcionalidades Obrigatórias:
1. Filtros Interativos (Dropdowns): Modelo da Porsche, Model Year, City e Pay Method. Todos os gráficos e KPIs devem se recalcular instantaneamente ao alterar os filtros.
2. KPIs de Topo: Total de Vendas, Receita Total e Ticket Médio.
3. Gráficos:
   - Gráfico de Barras: Principais modelos vendidos por cidade.
   - Gráfico de Linha ou Área: Evolução/Distribuição de vendas por Model Year.
   - Gráfico de Dispersão ou Barras Agrupadas: Insight de carros de maior volume por cidade.
   - Gráfico de Mapa Coroplético ou Barras Horizontais: Vendas por Estado (State).
```

### O que mudou até a versão final?
* **Ajuste de UI:** A primeira versão gerada abusou de fundos escuros (Dark Mode genérico). Foi refinado via linguagem natural para adotar o visual clean, minimalista e luxuoso do site oficial da Porsche.
* **Conserto de Scripts:** Correção na lógica dos filtros do `Chart.js` para garantir que a remoção de um filtro recalculasse o estado global da base corretamente, evitando gráficos vazios.

---

## 🛠️ Tecnologias Utilizadas

* **HTML5 & CSS3** (Estruturação e estilização customizada sem frameworks pesados para garantir leveza)
* **JavaScript (ES6+)** (Motor de filtragem de dados e manipulação do DOM)
* **Chart.js** (Biblioteca para renderização de gráficos responsivos e elegantes)
* **GitHub Pages** (Hospedagem e deploy contínuo e gratuito da aplicação)

---

## 🚀 Como Executar o Projeto Localmente

Como a aplicação foi consolidada em um **arquivo único de HTML**, executá-la é extremamente simples:

1. Clone este repositório na sua máquina:
   ```bash
   git clone https://github.com.git
   ```
2. Navegue até a pasta do projeto:
   ```bash
   cd dashboard_porche_sales
   ```
3. Abra o arquivo `index.html` diretamente no seu navegador de preferência ou utilize a extensão *Live Server* do VS Code.

---

Elaborado com dedicação para o portfólio de Análise de Dados. 🏁
