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

1. Repositório selecionado: https://github.com/mrdoob/three.js
2. Gráfico selecionado:
<img width="793" height="402" alt="image" src="https://github.com/user-attachments/assets/2bf6ebbc-124a-4264-83fa-d9e1451cb42b" />

3. Explicação:
O gráfico “Classes” do repositório three.js mostra um alto crescimento no número de classes entre 2020 e 2022, saindo de uma base quase nula para algo em torno de 1.700. Esse salto costuma refletir novos recursos, materiais, geometrias, helpers, loaders e exemplos, entre outros, e uma consolidação do design orientado a objetos do projeto: funcionalidades que antes poderiam estar como funções utilitárias passam a ter APIs encapsuladas em classes.

Em 2023 há uma leve retração, que faz sentido como consequência de refatorações e diminuições no código: remoção de duplicidades, unificação de implementações parecidas, extração de partes comuns, entre outros. Em projetos grandes como esse, é comum que depois de uma fase de forte crescimento venha um período de “arrumação da casa”, reduzindo a contagem de classes sem perder as funcionalidades.

A partir de 2024 a curva retoma a alta e chega a cerca de 2.500 em 2025, sugerindo uma nova onda de funcionalidades (ex.: melhorias de renderização, novos loaders/formats, utilitários de XR/AR/VR, pós-processamento, exemplos e extensões) implementadas de forma modular. Do ponto de vista de boas práticas, é positiva: o uso de classes torna a API mais previsível e extensível, mas vale monitorar se o crescimento vem acompanhado de coerência arquitetural e de documentação atualizada, sinais de que o aumento representa evolução de qualidade e não apenas complexidade acidental.



