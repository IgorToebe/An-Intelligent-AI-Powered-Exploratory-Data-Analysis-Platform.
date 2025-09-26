# 🚀 Guia de Deploy - Streamlit Cloud

Este guia contém instruções específicas para fazer deploy da aplicação no Streamlit Cloud.

## ✅ Preparação Completada

O projeto já foi limpo e otimizado para produção:

- ❌ Removidos arquivos de teste e debug
- ❌ Removidos caches Python (**pycache**)
- ❌ Removido ambiente virtual (.venv)
- ❌ Removidos gráficos temporários de teste
- ✅ Configurado suporte a st.secrets
- ✅ Criado .streamlit/config.toml
- ✅ Atualizado .gitignore
- ✅ Removidos prints de debug

## 📋 Checklist Pré-Deploy

### 1. Estrutura de Arquivos

```
Programa/
├── .streamlit/
│   ├── config.toml              ✅ Configurações do Streamlit
│   └── secrets.toml.example     ✅ Exemplo de secrets
├── agente/                      ✅ Módulos do agente IA
├── processamento/               ✅ Processamento de dados
├── visualizacao/                ✅ Geração de gráficos
├── temp_graficos/               ✅ Diretório vazio (será usado em runtime)
├── app.py                       ✅ Aplicação principal
├── requirements.txt             ✅ Dependências Python
├── .gitignore                   ✅ Arquivos a ignorar
├── README.md                    ✅ Documentação
└── LICENSE                      ✅ Licença
```

### 2. Configurações Necessárias

#### API Key do Google Gemini

1. Obtenha em: https://makersuite.google.com/app/apikey
2. Configure no Streamlit Cloud em "Settings" → "Secrets"
3. Formato:
   ```toml
   GOOGLE_API_KEY = "sua_chave_aqui"
   ```

## 🚀 Passos para Deploy

### 1. Preparar Repositório

```bash
# Fazer push para GitHub/GitLab
git add .
git commit -m "Projeto limpo e pronto para produção"
git push origin main
```

### 2. Deploy no Streamlit Cloud

1. Acesse [share.streamlit.io](https://share.streamlit.io)
2. Faça login com GitHub/Google
3. Clique "New app"
4. Selecione seu repositório
5. Main file path: `app.py`
6. Configure os Secrets com sua API key
7. Deploy!

### 3. Configurar Secrets

Na interface do Streamlit Cloud:

```toml
GOOGLE_API_KEY = "AIzaSy..."
GEMINI_MODEL = "gemini-1.5-flash"
GEMINI_TEMPERATURE = "0.1"
```

## 🔧 Configurações Opcionais

### Custom Domain

- Configure um domínio customizado nas configurações do app

### Environment Variables

Além dos secrets, você pode configurar:

- `STREAMLIT_THEME_PRIMARY_COLOR`
- `STREAMLIT_SERVER_MAX_UPLOAD_SIZE`

## 🚨 Troubleshooting

### Problemas Comuns

1. **API Key não funciona**

   - Verifique se a chave está correta nos secrets
   - Confirme que a API do Google Gemini está habilitada

2. **Import errors**

   - Verifique requirements.txt
   - Todas as dependências estão listadas

3. **File not found errors**

   - Verifique se todos os arquivos necessários foram commitados
   - Confirme estrutura de diretórios

4. **Memory issues**
   - Otimize carregamento de dados
   - Use st.cache_data para funções pesadas

### Logs e Debug

- Use st.error() para mostrar erros ao usuário
- Streamlit Cloud mostra logs na interface
- Configure logging para produção

## 📊 Monitoramento

### Métricas Importantes

- Tempo de carregamento inicial
- Uso de memória
- Número de usuários concorrentes
- Erros de API

### Performance

- Use st.cache_data para dados
- st.cache_resource para modelos
- Otimize imports (lazy loading)

## 🔄 Updates

Para atualizar a aplicação:

1. Fazer push de mudanças para o repositório
2. Streamlit Cloud fará redeploy automaticamente
3. Monitorar logs para garantir sucesso

## 📞 Suporte

Em caso de problemas:

- Documentação: https://docs.streamlit.io/streamlit-community-cloud
- Fórum: https://discuss.streamlit.io/
- GitHub Issues do projeto

---

**🎉 Seu projeto está pronto para produção!**
