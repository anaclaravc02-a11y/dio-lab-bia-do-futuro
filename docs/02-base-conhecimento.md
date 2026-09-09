# Base de Conhecimento

## Dados Utilizados

Descreva se usou os arquivos da pasta `data`, por exemplo:

| Arquivo | Formato | Para que serve a Ananda? |
|---------|---------|---------------------|
| `historico_atendimento.csv` | CSV | Contextualizar interações anteriores e acompanhar a evolução financeira do cliente |
| `perfil_investidor.json` | JSON |Personalizar a análise de acordo com o negócio, faturamento, despesas e situação financeira|
| `produtos_financeiros.json` | JSON | Organizar as dívidas, parcelas, juros, prazos e definir prioridades de pagamento |
| `transacoes.csv` | CSV | Analisar o padrão de entradas e saídas e identificar comportamentos que impactam o caixa |
| `metodos_renda_extra.json` |	JSON |	Apresentar opções realistas de renda extra de acordo com o perfil e a realidade do negócio|
| `plano_financeiro.json`	|JSON |	Registrar metas, valores necessários, estratégias e evolução do plano mensal|

> [!TIP]
> **Quer um dataset mais robusto?** Você pode utilizar datasets públicos do [Hugging Face](https://huggingface.co/datasets) relacionados a finanças, desde que sejam adequados ao contexto do desafio.

---

## Adaptações nos Dados

> Você modificou ou expandiu os dados mockados? Descreva aqui.

Sim. Os dados mockados foram modificados para representar a realidade financeira de um empresário endividado. As transações pessoais foram substituídas por movimentações de um negócio, incluindo vendas, fornecedores, despesas operacionais, salários e pagamentos de dívidas.

---

## Estratégia de Integração

### Como os dados são carregados?
> Descreva como seu agente acessa a base de conhecimento.
Os arquivos JSON e CSV são carregados no início da sessão e disponibilizados ao agente como base de conhecimento. A Ananda consulta esses dados durante a conversa para analisar a situação financeira do empresário e gerar recomendações personalizadas, sempre utilizando apenas as informações disponíveis na base e os dados fornecidos pelo cliente.

### Como os dados são usados no prompt?
> Os dados vão no system prompt? São consultados dinamicamente?

Os dados não ficam todos no system prompt. O system prompt define as regras de comportamento do agente e como ele deve utilizar os dados. As informações do cliente e os dados financeiros são consultados dinamicamente quando necessário, permitindo que a Ananda faça análises personalizadas com base na situação atual do empresário.

---

## Exemplo de Contexto Montado

> Mostre um exemplo de como os dados são formatados para o agente.

```
Dados do Empresário:
- Nome: Carlos Oliveira
- Negócio: Mercadinho do Carlos
- Segmento: Comércio de alimentos
- Faturamento mensal: R$ 22.000
- Despesas mensais: R$ 16.500
- Lucro mensal atual: R$ 5.500
- Dívidas totais: R$ 85.000
- Parcelas mensais das dívidas: R$ 4.200

Dívidas:
- Empréstimos bancários: R$ 45.000
- Fornecedores: R$ 25.000
- Cartão empresarial: R$ 15.000

Objetivo principal:
- Sair das dívidas e recuperar a saúde financeira do negócio

Estratégias disponíveis:
- Redução de despesas
- Aumento de vendas
- Venda de produtos ou serviços adicionais
- Negociação de dívidas
- Plano de quitação acelerada

Regras:
- Não inventar informações
- Explicar os cálculos realizados
- Pedir autorização antes de criar um plano
- Não recomendar formas irreais de renda extra
- Não prometer resultados
...
```
