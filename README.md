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
