# Análise do Desenvolvimento Humano e Econômico Global (Gapminder)

Trabalho da disciplina **Python para Ciências de Dados** (PUC Minas), ministrada pelo prof. Leandro Lessa.

## Integrantes

- Kamilla Silveira Pone de Souza Leão
- Gabriel Ubiratã de Lima Santos
- Samuel Guimaraes Ferreira
- Davidson Loiolla Gomes

## Introdução

Este trabalho tem como objetivo coletar, tratar, descrever e extrair insights da base de dados disponibilizada pela **Gapminder**, que reúne informações de expectativa de vida, PIB per capita e tamanho populacional de países de diferentes continentes, em uma janela temporal que vai de 1952 a 2007.

Além de exercitar técnicas fundamentais de uso do Python para lidar com dados, o trabalho permitiu verificar como países e regiões estão posicionados em termos de riqueza, qualidade de vida e desenvolvimento humano. O olhar aprofundado sobre dados reais levou, inclusive, a conclusões que, antes da análise empírica, pareciam completamente diferentes.

O trabalho está dividido em três partes:

1. **Coleta:** carregamento do dataset a partir de um arquivo CSV.
2. **Limpeza:** exclusão de registros duplicados, verificação de informações inválidas e ajustes de formato.
3. **Análise descritiva:** exploração da base sob diferentes perspectivas, abordando todas as variáveis disponíveis, em busca de conclusões.

## Base de dados

A base `gapminder_full.csv` é derivada do trabalho da Fundação Gapminder e traz observações por país e ano, em intervalos de cinco anos, entre 1952 e 2007.

| Coluna original | Coluna após o tratamento | Descrição |
|---|---|---|
| `country` | `pais` | País |
| `continent` | `continente` | Continente |
| `year` | `ano` | Ano de referência |
| `lifeExp` | `expectativa_vida` | Expectativa de vida ao nascer (anos) |
| `pop` | `populacao` | População total (habitantes) |
| `gdpPercap` | `pib_percapita` | PIB per capita |

## Tratamento dos dados

1. Inspeção da estrutura da base (registros, colunas, tipos e valores não nulos).
2. Identificação e remoção de registros duplicados, mantendo a primeira ocorrência e preservando a base original em uma cópia.
3. Verificação de dados ausentes.
4. Conversão da coluna `pop` para o tipo inteiro (`int64`).
5. Renomeação das colunas para o português.

## Análise exploratória

A análise explora a evolução e a distribuição das variáveis ao longo do tempo, globalmente, por continente e por país (com comparações pontuais, como Brasil e Argentina). Cada visualização é acompanhada de uma interpretação e da justificativa do tipo de gráfico escolhido.

- Expectativa de vida: evolução global, por continente e por país; mediana por continente e ano; distribuição por continente (boxplot).
- PIB per capita: evolução global, por continente e por país; distribuição por continente (boxplot).
- População: evolução global e por continente.
- Correlações entre expectativa de vida, PIB per capita e população (matriz de correlação e gráficos de dispersão).

Foram criadas funções reutilizáveis e parametrizáveis para o cálculo de médias e medianas, a geração de gráficos de linha, boxplots, matrizes de correlação e gráficos de dispersão.

## Principais insights

- A expectativa de vida e o PIB per capita cresceram de forma contínua entre 1952 e 2007, com disparidades relevantes entre os continentes.
- Europa e Oceania lideram em longevidade e renda; a África concentra os menores valores e apresenta estagnação da expectativa de vida na década de 1990.
- A Ásia se destacou pelo crescimento populacional acentuado e pela forte evolução da expectativa de vida e do PIB per capita.
- Há correlação positiva moderada (coeficiente de 0,58) entre PIB per capita e expectativa de vida. A relação não é linear: a expectativa de vida sobe rapidamente nas faixas mais baixas de renda e depois se estabiliza próximo dos 80 anos.
- A população não mostrou relação relevante com as demais variáveis.
- O crescimento financeiro, por si só, exige estratégias complementares, o que serve de subsídio para políticas públicas voltadas à saúde básica, à redução de desigualdades regionais e ao desenvolvimento humano sustentável.

## Conclusão e reflexão

### Quais foram os maiores desafios?

O principal desafio foi de natureza técnica, já que os membros do grupo não têm experiência cotidiana com Python. Ainda assim, as listas de exercícios e os exemplos em aula, o trabalho em equipe e as consultas à documentação das bibliotecas permitiram realizar o que foi proposto com relativa facilidade.

Outro desafio foi encontrar o formato ideal para apresentar os dados. A partir de discussões em grupo, buscaram-se visualizações com clareza, ausência de viés e facilidade de leitura.

Por fim, algumas questões exigem maior repertório e vão além do escopo do trabalho, como a possível causalidade entre duas variáveis e os motivos pelos quais determinadas regiões e países oferecem piores condições de qualidade de vida.

### O que foi aprendido?

O trabalho desenvolveu habilidades em Python, que se mostrou versátil e útil para trabalhar com dados. O grupo concluiu que dominar a ferramenta é fundamental e que a ascensão da IA não elimina a necessidade de conhecê-la para construir análises robustas, confiáveis e que façam sentido.

Também foram obtidas evidências sobre padrões globais de qualidade de vida:

- países ricos tendem a ter maior expectativa de vida;
- há enorme disparidade de renda e de qualidade de vida entre os continentes;
- houve forte aumento da expectativa de vida e da riqueza média no mundo, com particularidades por continente, e a África seguiu um padrão distinto.

### Como a experiência ajudou no desenvolvimento de habilidades analíticas?

A proposta de buscar diferentes análises possíveis para a base tornou-se mais desafiadora a partir de certo ponto. Depois de esgotadas as perguntas óbvias, o grupo foi levado a formular questionamentos que vão além do senso comum, o que estimulou o senso crítico, a criatividade e a reflexão aprofundada, além de construir um repertório de perguntas úteis para trabalhos semelhantes.

## Ferramentas utilizadas

- **Pandas:** manipulação e organização dos dados em DataFrames
- **NumPy:** operações matemáticas e numéricas
- **Matplotlib e Seaborn:** gráficos e visualizações estatísticas
- **Openpyxl:** leitura e escrita de arquivos Excel
- **Google Colab:** ambiente de execução em nuvem
- **Git / GitHub:** versionamento e hospedagem da base

## Referências

- Fundação Gapminder: https://www.gapminder.org
- Enunciado da atividade: disciplina Python para Ciências de Dados, PUC Minas.
