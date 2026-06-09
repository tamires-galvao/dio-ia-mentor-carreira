# 04 — Projeto de Portfólio: SmartAssist

## Visão do projeto

**SmartAssist** é um assistente corporativo com RAG para responder perguntas sobre políticas, processos e conhecimento interno.

## Stack tecnológica

- Backend: Spring Boot 3 + Spring AI
- Frontend: Angular 17 + TypeScript
- Banco vetorial: PostgreSQL + pgvector
- Infra: Docker (local) e AWS (produção)

## Arquitetura (diagrama textual)

```text
[Angular 17]
    |
    v
[API Spring Boot 3 + Spring AI] ---> [Serviço LLM]
    |                                     ^
    v                                     |
[PostgreSQL + pgvector] <--- [Pipeline de ingestão e embeddings]
```

## Entregáveis

1. API REST para conversação e gestão de contexto.
2. Interface web com chat, histórico e feedback de resposta.
3. Pipeline de ingestão de documentos com geração de embeddings.
4. Busca vetorial por similaridade e composição de contexto.
5. Deploy em ambiente cloud com monitoramento básico.

## Critérios de aceite

- Usuário consegue fazer perguntas e receber respostas contextualizadas.
- Respostas citam fontes/documentos utilizados.
- Tempo de resposta aceitável para uso real (meta inicial: até 5s em cenário padrão).
- Projeto com instruções de execução local e demonstração funcional.

## Passo a passo para começar

1. Criar repositório e configurar estrutura backend/frontend.
2. Subir PostgreSQL com extensão `pgvector`.
3. Implementar ingestão de documentos e persistência de embeddings.
4. Criar endpoint de busca + geração de resposta com Spring AI.
5. Desenvolver interface Angular para chat corporativo.
6. Containerizar com Docker Compose.
7. Publicar primeira versão em AWS.

