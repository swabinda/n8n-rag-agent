# 🤖 Nexus Weave RAG Agent (Intelligent Email Automation)

An enterprise-grade, fully automated Customer Support and Knowledge Retrieval pipeline built on **n8n**. Powered by a **Multi-Agent RAG (Retrieval-Augmented Generation)** architecture, this system securely processes user inquiries, retrieves context from a vector database, builds professional human-like solutions, and automates premium email deliveries.

---

## 🔄 Workflow Architecture & Processing Stages
[User Form Ingestion] ➔ [Pinecone Vector Retrieval] ➔ [OpenAI Core Reasoning Agent] ➔ [AI Subject Generator] ➔ [AI Plaintext-to-HTML Compiler] ➔ [Gmail Auto-Dispatch] ➔ [Google Sheets Logging]

1. **Data Ingestion:** Collects user information (`Name`, `Email`, `Phone`, `Query`) securely via an **n8n Webhook** trigger.
2. **Semantic Context Retrieval:** Uses **OpenAI Embeddings** to perform a similarity search inside a **Pinecone Vector Database** (`nexus-weave` index) to extract verified company data.
3. **Reasoning Agent:** Powered by **OpenAI GPT-4o-mini**, it analyzes the query against the context and formulates a concise, benefit-driven business resolution.
4. **Subject Line Optimization:** A dedicated copywriting agent generates a high-open-rate, non-spammy email subject line based on the dynamic response.
5. **HTML Design Engine:** Converts raw text replies into a modern, responsive, ultra-premium dark-themed (`#030C1B`) **HTML Email Layout** using inline CSS styles.
6. **Automated Dispatch:** Instantly fires the beautifully rendered HTML email to the user using **Gmail API**.
7. **CRM Database Tracking:** Appends a historical log containing customer metadata, raw queries, and exact agent replies into a **Google Sheet** (`Customers Info`) for sales pipeline analysis.

---

## 🛠️ Tech Stack & Integrations

* **Automation Engine:** n8n (Advanced AI & LangChain Framework)
* **LLM Model Core:** OpenAI (`gpt-4o-mini`)
* **Vector Database:** Pinecone DB
* **Embedding Model:** OpenAI Embeddings (`text-embedding-ada-002` / `text-embedding-3`)
* **Communications:** Gmail OAuth2 node
* **Database Ledger:** Google Sheets API

---

## 🌟 Key Product Features

* **Context-Driven Responses:** Mitigates AI hallucinations by cross-referencing information within the vector database before responding.
* **No-Code Inline Styling Boilerplate:** Includes a robust plain-text to HTML email agent, guaranteeing visual layout consistency across Apple Mail, Outlook, and Gmail.
* **Enterprise Guardrails:** Explicitly configured fallback rules handle pricing and internal system edge-cases gracefully without revealing technical backend specifics.

---

## 💻 Setup & Local Installation

### Prerequisites
* An active **n8n** deployment (v1+ supporting advanced LangChain nodes).
* API Keys and setups for:
  * OpenAI Developer Platform
  * Pinecone Index (`nexus-weave`)
  * Gmail Developer Account (OAuth2)
  * Google Sheets Workspace (OAuth2)

### Deployment Instructions
1. Download or clone the `Nexus Weave Rag Agent.json` file from this repository.
2. In your n8n panel, open a blank canvas, click on the top-right menu (three dots), and click **Import from File**.
3. Upload the JSON file.
4. Update credentials for **OpenAI**, **Pinecone**, **Gmail**, and **Google Sheets**.
5. Connect your Google Sheet (`Customers Info`) and match the headers exactly: `Name`, `Email`, `Phone`, `Query`, and `     Qury Reply`.
6. Activate the workflow toggle.

---

## 📌 Repository Tags (Topics)
`n8n` `rag-agent` `pinecone` `vector-database` `openai-api` `email-automation` `langchain` `ai-agents` `customer-support-automation`
