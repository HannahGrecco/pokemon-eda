# ⚡ Pokémon EDA 🇧🇷 Leia em Português | 🇺🇸 [Read in English](README.md)

Análise exploratória de dados do universo Pokémon investigando o que define um Pokémon poderoso e se as gerações mais recentes são mais fortes.
 
**Dataset:** [The Complete Pokémon Dataset](https://www.kaggle.com/datasets/rounakbanik/pokemon) — ~800 Pokémon com atributos de batalha, tipo, geração e status lendário.
 
---
 
## Estrutura
 
```
pokemon-eda/
├── data/
│   ├── pokemon.csv
│   └── pokemon_clean.csv
├── notebooks/
│   ├── 01_cleaning.ipynb
│   └── 02_analysis.ipynb
└── README.md
```
 
---
 
## Etapas
 
**01_cleaning.ipynb** — seleção de colunas, tratamento de nulos e exportação do dataset limpo.
 
**02_analysis.ipynb** — medidas de posição, dispersão e forma; histograma, gráfico de barras, dispersão, boxplot e linhas.
 
---
 
## Principais conclusões
 
- O tipo Dragon tem o maior poder total médio, mas não lidera nenhum atributo isolado, é consistentemente forte em todas as dimensões.
- Não existe um tipo dominante: cada tipo tem sua especialidade, indicando que o jogo é bem balanceado.
- Attack é o atributo com maior dispersão entre os Pokémon; HP é o mais homogêneo, sugerindo que o jogo equaliza a sobrevivência mas diferencia o poder ofensivo por tipo.
- Lendários concentram-se nos extremos do gráfico de dispersão (Attack × Defense), mas os valores absolutos mais altos de defesa pertencem a Pokémon comuns.
- As gerações mais recentes não são linearmente mais fortes: as gerações 4 e 7 se destacam das demais em poder total médio.
---
 
## Como rodar
 
```bash
pipenv install
pipenv shell
python -m ipykernel install --user --name=pokemon-eda
```
 
Abra os notebooks na ordem numérica. O `02_analysis.ipynb` depende do CSV gerado pelo `01_cleaning.ipynb`.
