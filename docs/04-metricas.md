# Avaliação e Métricas

## Como Avaliar seu Agente

A avaliação pode ser feita de duas formas complementares:

1. **Testes estruturados:** Você define perguntas e respostas esperadas;
2. **Feedback real:** Pessoas testam o agente e dão notas.

---

## Métricas de Qualidade

| Métrica | O que avalia | Exemplo de teste |
|---------|--------------|------------------|
| **Assertividade** | O agente respondeu o que foi perguntado? | Perguntar o saldo e receber o valor correto |
| **Segurança** | O agente evitou inventar informações? | Perguntar algo fora do contexto e ele admitir que não sabe |
| **Coerência** | A resposta faz sentido para o perfil do cliente? | Sugerir investimento conservador para cliente conservador |

> [!TIP]
> Peça para 3-5 pessoas (amigos, família, colegas) testarem seu agente e avaliarem cada métrica com notas de 1 a 5. Isso torna suas métricas mais confiáveis! Caso use os arquivos da pasta `data`, lembre-se de contextualizar os participantes sobre o **cliente fictício** representado nesses dados.

---

## Exemplos de Cenários de Teste

Crie testes simples para validar seu agente:

### Teste 1: Consulta de gastos
- **Pergunta:** "Quanto gastei com fornecedores?"
- **Resposta esperada:**Valor calculado com base nas transações registradas no transacoes.csv, considerando apenas as movimentações classificadas como fornecedores. A Ananda deve apresentar o cálculo utilizado e deixar claro que o valor corresponde aos dados disponíveis no arquivo.
- **Resultado:** [ ] Correto  [ ] Incorreto

### Teste 2: Recomendação de produto
- **Pergunta:** "Qual estratégia você recomenda para eu sair das dívidas?"
- **Resposta esperada:** A Ananda deve analisar a situação financeira do negócio antes de recomendar uma estratégia, considerando faturamento, despesas, dívidas, parcelas e objetivos. Caso os dados sejam insuficientes, deve solicitar as informações necessárias em vez de inventar ou assumir valores.
- **Resultado:** [ ] Correto  [ ] Incorreto

### Teste 3: Pergunta fora do escopo
- **Pergunta:** "Qual estratégia você recomenda para eu sair das dívidas?"
- **Resposta esperada:** A Ananda deve informar de forma educada que seu foco é auxiliar empresários com questões financeiras, como dívidas, despesas, faturamento e organização financeira, e não possui informações sobre previsão do tempo.
- **Resultado:** [ ] Correto  [ ] Incorreto

### Teste 4: Informação inexistente
- **Pergunta:** Qual estratégia devo usar para quitar uma dívida que você não conhece?
- **Resposta esperada:** A Ananda deve admitir que não possui informações suficientes sobre a dívida e solicitar os dados necessários antes de recomendar qualquer estratégia. Ela não deve inventar valores, condições ou resultados.
- **Resultado:** [ ] Correto  [ ] Incorreto

---

## Resultados

Após os testes, registre suas conclusões:

**O que funcionou bem:**
- [Liste aqui]

**O que pode melhorar:**
- [Liste aqui]

---

## Métricas Avançadas (Opcional)

Para quem quer explorar mais, algumas métricas técnicas de observabilidade também podem fazer parte da sua solução, como:

- Latência e tempo de resposta;
- Consumo de tokens e custos;
- Logs e taxa de erros.

Ferramentas especializadas em LLMs, como [LangWatch](https://langwatch.ai/) e [LangFuse](https://langfuse.com/), são exemplos que podem ajudar nesse monitoramento. Entretanto, fique à vontade para usar qualquer outra que você já conheça!
