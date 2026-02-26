
# 📊 Automatizando Análise de Dados com LLM
Este projeto automatiza a classificação de sentimentos em avaliações de clientes utilizando Inteligência Artificial. Através da API do Google Gemini, o script processa uma base de dados (CSV) e categoriza feedbacks em Positivo, Negativo ou Neutro de forma automática e em escala.

# 🚀 Sobre o Projeto
O objetivo principal foi substituir a análise manual de centenas de linhas de feedback por um processo automatizado e inteligente.

# Como funciona:
Entrada: O script lê uma coluna de um DataFrame (proveniente de um CSV) contendo as resenhas textuais.

Processamento: Cada resenha é enviada ao modelo gemini-2.0-flash com um prompt estruturado para garantir que a resposta seja padronizada.

Saída: O sentimento retornado é armazenado em uma nova coluna do conjunto de dados original.

# 🛠️ Tecnologias Utilizadas
Python: Linguagem base para o script.

Pandas: Para manipulação e estruturação dos dados.

Google Generative AI SDK: Para integração com o modelo Gemini.

Google Colab: Ambiente de desenvolvimento utilizado.

# 📋 Pré-requisitos
Para rodar este script, você precisará de:

Uma API KEY do Google Gemini (obtida no Google AI Studio).

Configurar a chave nos Secrets do seu Google Colab com o nome GEMINI_API_KEY_ALURA.

# 💻 Exemplo de Código

### O núcleo do processamento utiliza o modelo Gemini 2.0 Flash

` ` `for review_numero, resenha in enumerate(coluna_reviews):
    resposta = client.models.generate_content(
        model="gemini-2.0-flash",
        contents=f"Analise o sentimento desta resenha e responda apenas 'positiva', 'negativa' ou 'neutra': {resenha}"
    )
    lista_de_analises_de_sentimentos.append(resposta.text)` ` `
# 🎓 Créditos
Projeto desenvolvido com o apoio e base de conhecimento da Alura, focado em aplicar LLMs (Large Language Models) para resolver problemas reais de análise de dados.
