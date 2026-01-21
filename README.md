# Financial Data Analysis with SQL

## 📌 Contexto
Em ambientes corporativos, dados financeiros frequentemente apresentam inconsistências que impactam relatórios, pagamentos e tomadas de decisão.

Este projeto simula um cenário real de **análise e validação de dados financeiros**, semelhante ao encontrado em sistemas ERP.

---

## 🎯 Objetivo
Desenvolver consultas SQL para:
- Analisar contas a pagar e receber
- Classificar tipos de pagamento
- Identificar inconsistências nos dados
- Apoiar decisões financeiras e operacionais

---

## 🧠 Abordagem Técnica
Foram utilizadas consultas SQL com foco em:
- JOINs entre múltiplas tabelas
- Aplicação de regras de negócio via CASE
- Validação de dados financeiros
- Organização de resultados para leitura gerencial

---

## 🛠️ Tecnologias Utilizadas
- SQL
- Banco de dados relacional
- Conceitos de dados financeiros e ERP

---

## 📊 Exemplo de Consulta
```sql
SELECT
  conta,
  data_emissao,
  data_vencimento,
  tipo_pagamento,
  valor
FROM contas_financeiras
WHERE data_vencimento < CURRENT_DATE
  AND status = 'EM ABERTO';
