# 🤖 Plataforma de Análise Exploratória Inteligente

Uma aplicação web avançada para análise exploratória de dados usando inteligência artificial.

## ✨ Funcionalidades

- **🔍 Análise Exploratória Automática**: Análise inteligente de datasets com insights automáticos
- **📊 Visualizações Avançadas**: Gráficos interativos e personalizáveis
- **🤖 Análises Avançadas**: Clustering inteligente (K-Means, DBSCAN) com otimização automática
- **📈 Testes Estatísticos**: Testes de normalidade, correlação, Mann-Whitney, qui-quadrado
- **🎨 Interface Moderna**: Interface web responsiva e intuitiva

## 🛠️ Stack Tecnológico

- **Frontend**: Streamlit
- **Backend**: Python 3.11+
- **IA**: Google Gemini API + LangChain
- **Análises Avançadas**: Scikit-learn
- **Análise**: Pandas + NumPy
- **Visualização**: Matplotlib + Seaborn
- **Estatística**: SciPy

## 🚀 Instalação

### 💻 Desenvolvimento Local

1. **Clone o repositório**

   ```bash
   git clone <repository-url>
   cd Programa
   ```

2. **Instale as dependências**

   ```bash
   pip install -r requirements.txt
   ```

3. **Configure a API Key**

   ```bash
   cp .streamlit/secrets.toml.example .streamlit/secrets.toml
   # Edite o secrets.toml e adicione sua GOOGLE_API_KEY
   ```

4. **Execute a aplicação**
   ```bash
   streamlit run app.py
   ```

### ☁️ Deploy no Streamlit Cloud

1. **Faça fork/clone do repositório no GitHub**

2. **Acesse [share.streamlit.io](https://share.streamlit.io)**

3. **Configure os Secrets na interface do Streamlit Cloud:**

   - Vá em "Settings" → "Secrets"
   - Adicione:
     ```toml
     GOOGLE_API_KEY = "sua_chave_api_do_google_gemini"
     ```

4. **Deploy automático** - A aplicação será implantada automaticamente!

## 📝 Como Usar

1. **Upload de Dados**: Faça upload de um arquivo CSV
2. **Análise IA**: Use linguagem natural para fazer perguntas sobre seus dados
3. **Visualizações**: Explore gráficos interativos e análises estatísticas
4. **Análises Avançadas**: Aplique clustering, redução de dimensionalidade e outros algoritmos de análise exploratória

## 📊 Exemplos de Comandos

```
"Analise a distribuição da coluna Amount"
"Execute clustering K-means com 4 grupos"
"Teste a normalidade dos dados de V1"
"Compare Amount entre grupos de Class"
"Detecte outliers na coluna Time"
```

## 📁 Estrutura do Projeto

```
Programa/
├── app.py                  # Aplicação principal Streamlit
├── agente/                 # Módulos do agente IA
│   ├── agente_core.py     # Core do agente
│   ├── ferramentas.py     # Ferramentas de análise
│   └── memoria.py         # Sistema de memória
├── processamento/         # Processamento de dados
│   ├── carregador_dados.py # Carregamento de arquivos
│   └── motor_analise.py   # Motor de análise
├── visualizacao/          # Geração de gráficos
│   └── gerador_graficos.py
├── temp_graficos/         # Gráficos temporários
├── requirements.txt       # Dependências Python
└── README.md             # Este arquivo
```

## ⚙️ Configuração

### 🔑 Obter API Key do Google Gemini

1. Acesse [Google AI Studio](https://makersuite.google.com/app/apikey)
2. Faça login com sua conta Google
3. Clique em "Create API Key"
4. Copie a chave gerada

### 🏠 Desenvolvimento Local

Crie um arquivo `.streamlit/secrets.toml`:

```toml
GOOGLE_API_KEY = "sua_chave_api_aqui"
```

### ☁️ Streamlit Cloud

Configure os secrets na interface web do Streamlit Cloud com a mesma estrutura acima.

## 🤝 Contribuição

1. Fork o projeto
2. Crie uma branch (`git checkout -b feature/nova-funcionalidade`)
3. Commit suas mudanças (`git commit -am 'Adiciona nova funcionalidade'`)
4. Push para a branch (`git push origin feature/nova-funcionalidade`)
5. Abra um Pull Request

## 📄 Licença

Este projeto está sob a licença MIT. Veja o arquivo LICENSE para mais detalhes.

© 2025 Igor Töebe Lopes Farias. Todos os direitos reservados.
