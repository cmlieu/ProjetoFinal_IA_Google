# ProjetoFinal_IA_Google

# Comparador de Preços Inteligente

## Objetivo do Projeto

Cansado de visitar vários sites de supermercados, atacados e lojas para encontrar o menor preço para os seus produtos essenciais? Imagine ter um assistente pessoal que faz essa busca para você, de forma inteligente e rápida, apresentando a melhor opção para economizar em suas compras. É exatamente isso que este projeto propõe! Desenvolvemos um **Comparador de Preços Inteligente** que utiliza a poderosa inteligência artificial do Gemini para pesquisar em diversas fontes online, analisar os resultados e identificar a loja com o menor preço total para a sua lista de compras, considerando a sua localização. Pare de perder tempo e dinheiro, comece a comprar de forma mais estratégica com a ajuda da IA!

## Sobre o Projeto

Este projeto implementa um comparador de preços baseado em agentes de IA, utilizando a Google AI SDK. Ele funciona da seguinte forma:

1.  **Coleta de Dados:** Um "agente buscador" utiliza a ferramenta Google Search para encontrar preços e links dos produtos desejados em diversas lojas online na localidade especificada pelo usuário.
2.  **Análise Inteligente:** Um "agente analisador" recebe os dados coletados, verifica a validade das informações (preço numérico e link para todos os produtos) e calcula o preço total da lista de compras em cada loja.
3.  **Resultado Otimizado:** O agente analisador identifica a loja com o menor preço total e apresenta os resultados de forma clara, incluindo o nome da loja, o preço total e os preços individuais com links para cada produto.

## Tecnologias Utilizadas

*   Python
*   Google Colab
*   Google AI SDK (para comunicação com modelos Gemini)
*   Google Search Tool (para realizar buscas online)
*   Bibliotecas Python: `google-genai`, `google-adk`, `google-api-python-client`, `IPython.display`, `textwrap`, `datetime`, `requests`, `warnings`.

## Como Executar o Projeto no Google Colab

Para rodar este projeto no Google Colab, siga os passos abaixo:

1.  **Abra o Notebook:** Abra o arquivo `.ipynb` deste projeto no Google Colab.
2.  **Configure sua Chave API:**
    *   Você precisará de uma chave API do Google para acessar o Gemini e a ferramenta Google Search. Obtenha sua chave API no Google AI Studio ou na Google Cloud Platform.
    *   No Google Colab, clique no ícone de "chave" (Secrets) no painel esquerdo.
    *   Clique em "ADD NEW SECRET".
    *   No campo "Name", insira exatamente `GOOGLE_API_KEY`.
    *   No campo "Value", cole a sua chave API.
    *   Certifique-se de que a opção "Notebook access" esteja marcada.
3.  **Execute a Célula de Código:** Clique na célula que contém todo o código (ou use "Ambiente de execução" -> "Executar tudo"). O código está estruturado para instalar as dependências e iniciar a execução automaticamente.
4.  **Interaja com o Chatbot:** O programa irá iniciar uma interface de linha de comando no output da célula, solicitando que você insira os produtos e a cidade para iniciar a busca de preços.

## Estrutura do Código

O código está organizado em funções para modularizar as diferentes partes do fluxo:

*   **`inicializar_chat()`:** Configura a comunicação com o modelo Gemini e define a persona do assistente.
*   **`call_agent()`:** Função auxiliar para executar os agentes e obter suas respostas.
*   **`agente_buscador()`:** Responsável por realizar as buscas de preços no Google Search com base na lista de produtos e localização.
*   **`agente_analisador()`:** Analisa os resultados do agente buscador para encontrar a loja com o menor preço total.
*   **`to_markdown()`:** Função auxiliar para formatar a saída em Markdown no Colab.
*   **`main()`:** Contém o fluxo principal do programa, incluindo a interação com o usuário e a chamada dos agentes.
*   O bloco `if __name__ == "__main__":` no final garante a instalação das dependências e a execução da função `main()`.

## Contribuição

Contribuições são bem-vindas! Se você tiver ideias para melhorar o projeto, sinta-se à vontade para abrir um pull request ou uma issue.

## Licença

GNU GPLv3

## Autor

CMLU
