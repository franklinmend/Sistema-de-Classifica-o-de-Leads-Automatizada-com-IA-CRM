# Sistema-de-Classifica-o-de-Leads-Automatizada-com-IA-CRM

# 🚀 Sistema de Inteligência Comercial com IA
Chatbot com RAG + Classificação Automática de Leads

n8n • OpenAI • Redis • HubSpot

## 📌 Visão Geral

Este projeto é um sistema de chatbot com Inteligência Artificial integrado a uma página de produtos de tecnologia, com foco em transformar atendimento em inteligência comercial.

A solução combina:

Atendimento automatizado com RAG

Memória persistente

Classificação automática de leads

Integração direta com CRM (HubSpot)

O objetivo é transformar dúvidas de produto em oportunidades comerciais organizadas.

# 🎯 Problema

Em muitos e-commerces:

Produtos não possuem detalhes técnicos suficientes

Clientes têm dúvidas e abandonam a página

Leads chegam ao CRM sem contexto

Não há priorização automática de oportunidades

Isso reduz conversão e gera desorganização comercial.

# 💡 Solução

O sistema permite que o usuário:

Tire dúvidas diretamente na página do produto

Receba respostas técnicas baseadas em RAG

Tenha sua conversa analisada automaticamente

Seja classificado como lead FRIO, MORNO ou QUENTE

Tenha seus dados organizados no HubSpot

O atendimento deixa de ser apenas suporte e passa a gerar inteligência comercial estruturada.

# 🧠 Arquitetura do Sistema

O fluxo é dividido em quatro blocos principais.

# 1️⃣ Recebimento e Buffer Inteligente

Webhook recebe a mensagem do site

Redis armazena temporariamente

Buffer de 15 segundos evita múltiplas execuções

Verificação de duplicidade

Limpeza automática do cache

Objetivo: controle de custo, estabilidade e performance.

# 2️⃣ Agente de Atendimento com RAG

Responsável por:

Responder dúvidas técnicas

Utilizar embeddings + retrieval

Manter memória de sessão via Redis

Solicitar nome e e-mail

Criar ou buscar contato no HubSpot

Separação clara entre atendimento e inteligência comercial.

# 3️⃣ Tratamento Estruturado de Dados

Extração do e-mail via regex

Extração da conversa limpa

Validação de formato

Verificação condicional antes de envio ao CRM

Garante integridade dos dados e evita falhas na API.

# 4️⃣ Classificação Automática de Leads

Segundo agente de IA responsável exclusivamente por:

Analisar a conversa

Classificar o lead como:

🔵 FRIO → Dúvidas informativas
🟡 MORNO → Interesse comercial moderado
🔴 QUENTE → Intenção clara de compra

Após a classificação:

Atualiza o contato no HubSpot

Insere resumo da conversa

Registra a classificação no campo "Messages"

Permite priorização automática pelo time comercial.

## 👤 Contato com Especialista

Caso o cliente solicite falar com um especialista, o sistema fornece um número de contato configurado no fluxo.

Não há transferência automática, apenas disponibilização do contato mediante solicitação.

# 🔥 Diferenciais Técnicos

Arquitetura modular em camadas

Separação entre agente de atendimento e agente comercial

Classificação automática integrada ao CRM

Buffer inteligente anti-sobrecarga

Validação estruturada de dados

Pipeline comercial automatizado

# 🏗 Tecnologias Utilizadas

n8n (orquestração de workflows)

OpenAI GPT

Redis

HubSpot API

JavaScript (nodes customizados)

RAG (Embeddings + Retrieval)

# 📊 Fluxo Geral

Webhook
→ Redis (Buffer)
→ Agente de Atendimento (RAG)
→ Tratamento de Dados
→ Agente de Classificação
→ Atualização no HubSpot

# 🎯 Resultado

O sistema transforma atendimento em:

Inteligência comercial estruturada

Leads organizados automaticamente

Classificação estratégica para vendas

Redução de trabalho manual

Arquitetura escalável

# 🧠 O que este projeto demonstra

Engenharia de sistemas com IA

Arquitetura de automação complexa

Integração real com CRM

Modelagem de fluxo comercial automatizado

Separação de responsabilidades entre agentes
