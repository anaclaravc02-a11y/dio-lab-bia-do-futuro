# Código da Aplicação

Esta pasta contém o código da aplicação da **Ananda**, uma agente financeira desenvolvida para auxiliar empresários na organização das finanças, análise de dívidas e recuperação da saúde financeira do negócio.

## Estrutura Sugerida

```text
src/
├── app.py                  # Aplicação principal (Streamlit)
├── agente.py               # Lógica e comportamento da Ananda
├── config.py               # Configurações e variáveis de ambiente
├── dados/                  # Base de conhecimento do agente
│   ├── historico_atendimento.csv
│   ├── perfil_empresarial.json
│   ├── dividas.json
│   ├── transacoes.csv
│   ├── metodos_renda_extra.json
│   └── plano_financeiro.json
└── requirements.txt        # Dependências do projeto
```

## Exemplo de requirements.txt

```text
streamlit
openai
python-dotenv
pandas
```

## Como Rodar

```bash
# Criar e ativar o ambiente virtual
python -m venv venv

# Windows
venv\Scripts\activate

# Instalar as dependências
pip install -r requirements.txt

# Executar a aplicação
streamlit run app.py
```

## Configuração

As informações sensíveis, como chaves de API, devem ser armazenadas em variáveis de ambiente ou em um arquivo `.env`.

Exemplo:

```text
OPENAI_API_KEY=sua_chave_aqui
```

> ⚠️ Não compartilhe chaves de API ou outras credenciais no GitHub.

## Funcionamento

A aplicação utiliza o **Streamlit** para disponibilizar a interface da Ananda e arquivos **JSON e CSV** como base de conhecimento.

A agente consulta os dados financeiros disponíveis para:

* Analisar faturamento e despesas;
* Consultar transações;
* Organizar dívidas;
* Identificar oportunidades de melhoria;
* Sugerir estratégias de geração de receita;
* Criar um plano financeiro mediante autorização do usuário.

Quando não houver dados suficientes, a Ananda deve solicitar as informações necessárias em vez de inventar ou assumir valores.

## ⚠️ Observação

Este projeto possui finalidade **educacional e demonstrativa**. A Ananda não garante resultados financeiros e suas orientações não substituem a avaliação de profissionais especializados.
