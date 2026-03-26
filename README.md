# Explorando evolução de código

Neste exercício, iremos explorar a evolução de código em sistemas reais.

Iremos utilizar a ferramenta [GitEvo](https://github.com/andrehora/gitevo).
Essa ferramenta analisa a evolução de código em repositórios Git nas linguagens Python, JavaScript, TypeScript e Java, e gera relatórios `HTML` como [este](https://andrehora.github.io/gitevo-examples/python/pandas.html).

Mais exemplos de relatórios podem ser podem ser encontrados em https://github.com/andrehora/gitevo-examples.

# Passo 1: Selecionar repositório a ser analisado

Selecione um repositório relevante na linguagem de sua preferência (Python, JavaScript, TypeScript ou Java).
Você pode encontrar projetos interessantes nos links abaixo:

- Python: https://github.com/topics/python?l=python
- JavaScript: https://github.com/topics/javascript?l=javascript
- TypeScript: https://github.com/topics/typescript?l=typescript
- Java: https://github.com/topics/java?l=java

# Passo 2: Instalar e rodar a ferramenta GitEvo

> [!NOTE]
> Antes de instalar a ferramenta, é recomendado criar e ativar um [ambiente virtual Python](https://packaging.python.org/en/latest/guides/installing-using-pip-and-virtual-environments/#create-and-use-virtual-environments).

Instale a ferramenta [GitEvo](https://github.com/andrehora/gitevo) com o comando:

```
$ pip install gitevo
```

Execute a ferramenta no repositório selecionado utilizando o comando abaixo (ajuste conforme a linguagem do repositório).
Substitua `<git_url>` pela URL do repositório que será analisado:

```shell
# Python
$ gitevo -r python <git_url>

# JavaScript
$ gitevo -r javascript <git_url>

# TypeScript
$ gitevo -r typescript <git_url>

# Java
$ gitevo -r java <git_url>
```

Por exemplo, para analisar o projeto Flask escrito em Python:

```
$ gitevo -r python https://github.com/pallets/flask
```

> [!NOTE]
> Essa etapa pode demorar alguns minutos pois o projeto será clonado e analisado localmente.

# Passo 3: Explorar o relatório de evolução de código

Após executar a ferramenta [GitEvo](https://github.com/andrehora/gitevo), é gerado um relatório `HTML` contendo diversos gráficos sobre a evolução do código.

Abra o relatório `HTML` e observe com atenção os gráficos.

# Passo 4: Explicar um gráfico de evolução de código

Selecione um dos gráficos de evolução e explique-o com suas palavras.
Por exemplo, você pode:

- Detalhar a evolução ao longo do tempo
- Detalhar se as curvas estão de acordo com boas práticas
- Explicar grandes alterações nas curvas
- Explorar a documentação do repositório em busca de explicações para grandes alterações
- etc.

Seja criativo!

# Instruções para o exercício

1. Crie um `fork` deste repositório (mais informações sobre forks [aqui](https://docs.github.com/pt/pull-requests/collaborating-with-pull-requests/working-with-forks/fork-a-repo)).
2. Adicione o relatório `HTML` no seu fork.
3. No Moodle, submeta apenas a URL do seu `fork`.

Responda às questões abaixo diretamente neste arquivo `README.md` do seu fork:

1. Repositório selecionado: [https://github.com/mrdoob/three.js](https://github.com/fastapi/fastapi)
2. Gráfico selecionado: <img width="787" height="387" alt="image" src="https://github.com/user-attachments/assets/c905073f-135a-4ac8-89c0-ea1c5f3c28c1" />

3. Explicação: O gráfico apresenta a evolução do uso de diferentes estruturas de dados (dicionários, listas, tuplas e conjuntos) ao longo do tempo no projeto FastAPI, entre os anos de 2021 e 2026.

Observa-se que os dicionários (dictionary) possuem um crescimento significativo, principalmente entre 2023 e 2024. Isso é esperado, pois dicionários são amplamente utilizados em APIs para manipulação de dados em formato JSON, que é o principal formato de comunicação do FastAPI. Esse crescimento pode estar relacionado à adição de novas funcionalidades ou melhorias.

As listas (list) também apresentam crescimento ao longo do tempo, porém de forma mais moderada. Isso indica que continuam sendo utilizadas, mas sem mudanças bruscas.

Já as tuplas (tuple) e conjuntos (set) mantêm valores baixos e relativamente estáveis durante todo o período. Isso é coerente com boas práticas, já que essas estruturas costumam ser utilizadas em casos mais específicos e não como base principal de manipulação de dados em aplicações web.

Entre 2024 e 2025, observa-se uma estabilização no crescimento das estruturas, seguida por uma leve queda em 2026, especialmente nos dicionários. Essa redução pode indicar refatorações no código, remoção de redundâncias ou otimizações na estrutura interna do projeto.

De forma geral, o gráfico demonstra uma evolução saudável do código, com crescimento consistente seguido de estabilização, o que é característico de um projeto maduro.
