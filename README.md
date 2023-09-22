### About the Titanic

The sinking of the Titanic was one of the best-known maritime accidents in human history.
On April 15, 1912, during her maiden voyage, the widely considered “unsinkable” RMS Titanic sank after colliding with an iceberg. Unfortunately, there weren’t enough lifeboats for everyone onboard, resulting in the death of 1502 out of 2224 passengers and crew.

In this project we will explore the kaggle's data (https://www.kaggle.com/c/titanic) and we will to build a predictive model that answers the question: “what sorts of people were more likely to survive?” using passenger data (ie name, age, gender, socio-economic class, etc).

The objective is not be part of kaggle's challenge but study some models for binary classification.

### About the documents of project
This project was developed with the help of the poetry package manager. 
To use it, you need to install poetry on your machine and, once installed, download the project. 
At the link https://python-poetry.org/docs/basic-usage/ it is possible to understand how the package manager works.
Instead of creating a new project, Poetry can be used to 'initialize' a pre-populated directory. 
To interactively create a pyproject.toml file in the pre-existing-project directory:

```bash
cd pre-existing-project
poetry init
```

The document ending in .lock has all the necessary packages in the version used to run the notebooks
from the project. If you run notebooks with packages in different versions, the result may not be 
what is observed in the project.

Another possibility is to download the project and install the necessary libraries using pip install or 
conda intall.

---------------------------------------------------------------------------------------------------------
### Sobre o Titanic

O naufrágio do Titanic foi um dos acidentes marítimos mais conhecidos da história da humanidade.
Em 15 de abril de 1912, durante sua viagem inaugural, o RMS Titanic, amplamente considerado “inafundável”, afundou após colidir com um iceberg. Infelizmente, não havia botes salva-vidas suficientes para todos a bordo, resultando na morte de 1.502 dos 2.224 passageiros e tripulantes.

Neste projeto exploraremos os dados do kaggle (https://www.kaggle.com/c/titanic) e construiremos um modelo preditivo que responda à pergunta: “que tipos de pessoas tinham maior probabilidade de sobreviver?” usando dados de passageiros (ou seja, nome, idade, sexo, classe socioeconômica, etc.).

O objetivo não é fazer parte do desafio do kaggle, mas estudar alguns modelos para classificação binária.

### Sobre os documentos do projeto
Este projeto foi desenvolvido com o auxílio do gerenciador de pacotes de poetry.
Para utilizá-lo, é necessário instalar o Poetry em sua máquina e, depois de instalado, baixar o projeto.
No link https://python-poetry.org/docs/basic-usage/ é possível entender como funciona o gerenciador de pacotes.
Em vez de criar um novo projeto, o Poetry pode ser usado para 'inicializar' um diretório pré-preenchido.
Para criar interativamente um arquivo pyproject.toml no diretório de projeto pré-existente:

```bash
cd pre-existing-project
poetry init
```

O documento com terminação .lock possui todos os pacotes necessários na versão utilizada para rodar os notebooks
do projeto. Caso execute os notebooks com pacotes em versões diferentes, o resultado pode não ser o observado no projeto.

Outra possibilidade é baixar o projeto e instalar as bibliotecas necessárias usando pip install ou
conda intall.
