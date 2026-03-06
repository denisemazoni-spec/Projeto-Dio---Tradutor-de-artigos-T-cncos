# Projeto-Dio-Tradutor de artigos Técnicos
Criação de um tradutor de arquivos web, de inglês para português, utilizando o o serviço OpenAI do Azure

# Análise Automatizada de Documentos com Azure AI

![Status](https://img.shields.io/badge/status-active-brightgreen)
![Azure](https://img.shields.io/badge/Azure-Document%20Intelligence-0078D4?logo=microsoft-azure)
![Python](https://img.shields.io/badge/Python-3.10+-blue?logo=python)
![Streamlit](https://img.shields.io/badge/Streamlit-App-FF4B4B?logo=streamlit)
![License](https://img.shields.io/badge/license-MIT-lightgrey)

Projeto completo para análise automatizada de cartões de crédito usando **Azure Document Intelligence**, **Azure Blob Storage** e uma interface Web construída com **Streamlit**.

---
## Funcionalidades
- Upload de imagens (PNG/JPG)
- Envio automático ao Azure Blob Storage
- Processamento via modelo `prebuilt-creditCard` do Azure
- Extração de informações do cartão
- Validação automática e exibição amigável ao usuário

---
## Estrutura do Projeto
```
dio-azureai-anti-fraude/
├── README.md
├── assets/
│   ├── img_01.png
│   ├── img_02.png
├── DOCS/
│   └── sobre.txt
├── src/
│   ├── app.py
│   ├── requirements.txt
│   ├── .env.example
│   ├── services/
│   │   ├── blob_service.py
│   │   ├── credit_card_service.py
│   │   └── typing_fix.py
│   └── utils/
│       └── config.py
└── .gitignore
```
---
## Instalação e Execução
```bash
cd src
pip install -r requirements.txt
cp .env.example .env
# Preencha suas credenciais do Azure
streamlit run app.py
```

---
## Galeria
(As imagens serão renderizadas no GitHub)
```markdown
![Imagem 1](assets/img_01.png)
![Imagem 2](assets/img_02.png)
```

---
## Arquitetura
```
[Usuário] → [Interface Streamlit] → [Azure Blob Storage] → [Azure Document Intelligence]
          → [Extração] → [Validação] → [Resultado]
```

---
## Licença
Este projeto está sob a licença **MIT**.

#PARTE DOIS DO COPILOT
# Análise Automatizada de Documentos com Azure AI

![Static Badge](https://img.shields.io/badge/STATUS-ATIVO-green)
![Static Badge](https://img.shields.io/badge/AZURE-Document%20Intelligence-blue)
![Static Badge](https://img.shields.io/badge/STREAMLIT-WebApp-orange)
![Static Badge](https://img.shields.io/badge/PYTHON-3.10+-yellow)

Este projeto demonstra uma solução completa para análise automatizada de documentos com foco em identificação de possíveis fraudes em **cartões de crédito**, utilizando Azure Document Intelligence, Azure Blob Storage e uma interface desenvolvida em Streamlit.

---
## Tecnologias Utilizadas
- **Python 3.10+**
- **Azure Blob Storage**
- **Azure Document Intelligence** (modelo *prebuilt-creditCard*)
- **Streamlit**
- **dotenv** para variáveis de ambiente

---
## Estrutura do Projeto
```
dio-azureai-anti-fraude/
├── README.md
├── assets/
│   ├── img_01.png
│   ├── img_02.png
├── DOCS/
│   └── sobre.txt
├── src/
│   ├── app.py
│   ├── requirements.txt
│   ├── .env.example
│   ├── services/
│   │   ├── blob_service.py
│   │   ├── credit_card_service.py
│   │   └── typing_fix.py
│   └── utils/
│       └── config.py
└── .gitignore
```
---
## Como Funciona
1. O usuário faz upload de uma imagem (PNG/JPG/JPEG).
2. A imagem é enviada para o **Azure Blob Storage**.
3. A URL pública do Blob é usada para consulta ao modelo **Azure Document Intelligence**.
4. O modelo retorna dados extraídos como:
   - Nome do titular
   - Banco emissor
   - Número do cartão
   - Data de validade
5. A aplicação valida e exibe as informações na interface Streamlit.

---
## Como Executar Localmente
### 1 Criar ambiente virtual (opcional)
```bash
python -m venv .venv
source .venv/bin/activate   # Linux/Mac
# Windows: .venv\Scripts\activate
```
### 2 Instalar dependências
```bash
pip install -r requirements.txt
```
### 3 Criar arquivo `.env` baseado no `.env.example`
```ini
ENDPOINT="https://<sua-instancia>.cognitiveservices.azure.com/"
SUBSCRIPTION_KEY="<sua-chave>"
AZURE_STORAGE_CONNECTION_STRING="<sua-connection-string>"
CONTAINER_NAME="cartoes"
```
 **Nunca envie o `.env` para o GitHub!**

### 4 Executar o Streamlit
```bash
streamlit run app.py
```
---
## Galeria de Imagens
As imagens abaixo foram extraídas automaticamente do arquivo `DIO.docx`:

![img_01](assets/img_01.png)
![img_02](assets/img_02.png)

---
## Licença
Este projeto pode ser reutilizado livremente **para fins educacionais**.

---
## Autor
Projeto automatizado com apoio do **M365 Copilot**.

