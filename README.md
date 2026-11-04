# 🛒 Agente de Compras Corporativas

Sistema automatizado composto por um agente de Inteligência Artificial e um Dashboard interativo em React para análise, comparação e adjudicação de propostas empresariais.

## 🚀 Funcionalidades
- Leitura dinâmica do "Padrão Norte" de ficheiros CSV.
- Cálculo automático de "Menor Valor Total" e "Valor Adjudicado" (economia por fracionamento de itens).
- Geração de Pedidos de Compra (PO) em cartões prontos a copiar.

## 🛠️ Como utilizar
1. Aceda ao painel interativo.
2. Carregue o ficheiro `.csv` contendo as propostas (colunas: Produto, Qtd, Fornecedor).
3. Analise os gráficos e copie os Pedidos de Compra gerados.

mermaid
## Fluxo de Decisão do Agente

```mermaid
graph TD
    A[Upload de Planilha CSV] --> B[Extrator Padrão Norte]
    B --> C{Motor de Análise IA}
    C -->|Avalia trade-off| D[Menor Preço Global]
    C -->|Avalia fracionamento| E[Valor Adjudicado por Item]
    D --> F[Dashboard de Resultados]
    E --> F
    F --> G[Geração de Pedido de Compra PO]
    F --> H[Gráficos de Economia Total]
