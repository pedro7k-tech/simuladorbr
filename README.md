# 📊 Simulador da Reforma Tributária (CBS + IBS)

Aplicação web responsiva e moderna desenvolvida com **React 19**, **TypeScript**, **Vite** e **Tailwind CSS** para simular os impactos operacionais e financeiros da Reforma Tributária Brasileira (CBS + IBS + Imposto Seletivo).

---

## 📱 Responsividade Mobile

A aplicação foi 100% otimizada para dispositivos móveis (smartphones com telas a partir de 320px de largura):
- **Formulários e Inputs de Toque:** Campos de seleção, botões de opção e controles deslizantes redimensionados para toque confortável.
- **Visualização de Resultados:** Valores numéricos e cartões comparativos ajustados com suporte a quebra de linha responsiva.
- **Tabela Técnica:** Tabela comparativa por tributo com rolagem horizontal fluida e aviso tátil.
- **Gráficos Interativos:** Gráficos de rosca (Recharts) ajustados para não sobrepor telas reduzidas.
- **Modais Roláveis:** Modais de Pix e carregamento com rolagem vertical ativada.

---

## 📁 Estrutura do Projeto

```text
SIMULADOR REFORMA/
├── public/                 # Arquivos estáticos (favicon, imagens públicas)
├── src/
│   ├── components/         # Componentes da Interface (Header, Form, Result, Modais, etc.)
│   │   ├── AccountantMitigation.tsx  # Guia estratégico para o contador
│   │   ├── CompanyForm.tsx           # Formulário de entrada de dados da empresa
│   │   ├── Disclaimer.tsx            # Avisos legais e recomendações
│   │   ├── Footer.tsx                # Rodapé institucional
│   │   ├── Header.tsx                # Cabeçalho e barra superior 2026+
│   │   ├── LoadingModal.tsx          # Modal com progresso animado de simulação
│   │   ├── PixModal.tsx              # Modal de contribuição Pix (R$ 10,00)
│   │   ├── PracticalChanges.tsx      # O que muda na prática (4 pilares)
│   │   ├── ReportActions.tsx         # Ações para baixar PDF e compartilhar no WhatsApp
│   │   ├── SimulationResult.tsx      # Cards principais de comparação mensal/anual
│   │   ├── TaxCharts.tsx             # Gráficos em rosca comparativos (Atual vs Novo)
│   │   └── TaxComparison.tsx         # Tabela detalhada tributo por tributo
│   ├── lib/                # Lógicas matemáticas e utilitários
│   │   ├── formatters.ts     # Formatadores de moeda (BRL) e porcentagem
│   │   ├── generatePDF.ts    # Gerador de relatório executivo em PDF (jsPDF)
│   │   └── taxSimulation.ts  # Algoritmo de cálculo tributário (CBS/IBS/Simples/Presumido/Real)
│   ├── App.tsx             # Componente raiz da aplicação
│   ├── main.tsx            # Ponto de entrada React
│   └── index.css           # Estilos globais Tailwind CSS
├── index.html              # HTML base com meta tag viewport mobile
├── package.json            # Scripts e dependências
├── tailwind.config.js      # Configuração do Tailwind CSS
├── vite.config.ts          # Configuração do empacotador Vite
├── vercel.json             # Configuração para deploy direto na Vercel
└── netlify.toml            # Configuração para deploy direto na Netlify
```

---

## 🚀 Desenvolvimento Local

Para rodar o projeto localmente em seu computador:

1. **Instale as dependências:**
   ```bash
   npm install
   ```

2. **Inicie o servidor de desenvolvimento:**
   ```bash
   npm run dev
   ```

3. Abra o navegador no endereço exibido (geralmente `http://localhost:5173`).

---

## 📦 Como Gerar a Build de Produção

Para testar ou gerar os arquivos compilados de produção:

```bash
npm run build
```

Os arquivos prontos para publicação serão gerados na pasta **`dist/`**.

---

## 🌐 Como Fazer o Deploy (Simplificado)

### Opção 1: Deploy na Vercel (Recomendado - 1 Clique)
1. Crie uma conta ou faça login na [Vercel](https://vercel.com).
2. Clique em **"Add New Project"** e conecte seu repositório Git (GitHub / GitLab).
3. A Vercel detectará o Vite automaticamente.
4. Clique em **"Deploy"**.
5. *Nota:* O arquivo [`vercel.json`](file:///c:/Users/User/OneDrive/%C3%81rea%20de%20Trabalho/SIMULADOR%20REFORMA/vercel.json) já está incluído para evitar erros de rotas 404 ao atualizar a página.

---

### Opção 2: Deploy na Netlify (1 Clique)
1. Crie uma conta ou faça login na [Netlify](https://netlify.com).
2. Clique em **"Add new site"** -> **"Import an existing project"**.
3. Selecione seu repositório.
4. A Netlify usará automaticamente as configurações presentes no arquivo [`netlify.toml`](file:///c:/Users/User/OneDrive/%C3%81rea%20de%20Trabalho/SIMULADOR%20REFORMA/netlify.toml).
5. Clique em **"Deploy Site"**.

---

### Opção 3: Hospedagem Tradicional (cPanel, Hostinger, KingHost, Apache, Nginx)
1. Execute o comando de build na sua máquina:
   ```bash
   npm run build
   ```
2. Abra a pasta **`dist/`** gerada no seu computador.
3. Transfira todo o conteúdo dentro da pasta `dist/` para a pasta raiz da sua hospedagem (geralmente chamada de `public_html` ou `www`) via FTP ou Gerenciador de Arquivos do cPanel.
4. Pronto! O site estará no ar.

---

## 🛡️ Licença & Aviso Legal

Este projeto foi construído para fins informativos e estimativos com base nas diretrizes conhecidas da Reforma Tributária (CBS/IBS). Os resultados gerados não substituem pareceres contábeis ou jurídicos formais.
