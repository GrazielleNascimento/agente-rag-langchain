# Agente-rag-langchain

Coleção de implementações RAG (Retrieval-Augmented Generation) aplicadas a bases documentais em PDF, com pipelines prontos para produção: ingestão de documentos, chunking semântico, enriquecimento com metadados, armazenamento vetorial (Chroma) e integração com modelos conversacionais da OpenAI. Projetos inclusos demonstram abordagens reutilizáveis para transformar coleções de PDFs (manuais, bulas, políticas) em agentes consultivos confiáveis.

---

## Valor e casos de uso
- Transformar documentação corporativa (políticas, procedimentos, manuais) em assistentes consultivos consultáveis por linguagem natural.
- Construir agentes de suporte que respondem com base estrita no conteúdo do acervo, reduzindo risco de alucinações.
- Provar conceitos e acelerar provas de conceito (PoC) para integração de LLMs com bases documentais internas.
- Fornecer exemplos prontos de produção: recuperação semântica, reranking com LLM e interface web (Streamlit).

---

## Principais funcionalidades
- Leitura e pré-processamento de PDFs (carregamento, limpeza, chunking com overlap).
- Enriquecimento de chunks com metadados (origem, categoria, página).
- Geração de embeddings via OpenAI e persistência em Chroma vector store.
- Recuperação semântica (retriever) com opção de reranking por LLM para priorizar trechos mais relevantes.
- Geração de respostas condicionadas estritamente ao contexto recuperado (RAG).
- Interface web pronta (Projeto 3) para consulta interativa; notebooks para investigação e ajustes.

---

## Estrutura do repositório
```text
Projeto1/
  Projeto 1.ipynb           # Notebook: Agente para Regras do Futebol (PDF: regras_futebol.pdf)
  regras_futebol.pdf
Projeto2/
  Projeto 2.ipynb           # Notebook: Agente para Bulas (dipirona.pdf, paracetamol.pdf)
  dipirona.pdf
  paracetamol.pdf
Projeto3/
  Projeto 3.py              # App Streamlit: Agente de RH com RAG + reranking
  codigo_conduta.pdf
  politica_ferias.pdf
  politica_home_office.pdf
