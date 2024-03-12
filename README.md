# CODESPACES SETUP

## Introdução

Para minimizar os problemas de instalação de aplicativos e pacotes nas dezenas de máquinas do laboratório de informática, é recomendado utilizar aplicações em nuvem como o [Github Codespaces](https://github.com/features/codespaces), [Google Colab](https://colab.research.google.com/) ou [Posit Cloud](https://posit.cloud/). Neste projeto, utilizaremos o Github Codespaces para criar um ambiente de desenvolvimento para projetos em R, especificamente para a disciplina de Insumo-Produto do Programa de Pós-Graduação em Economia da Universidade Federal do Espírito Santo (PPGEco/UFES).

## Configuração

Para qualquer projeto baseado em R, é necessário uma imagem de container com o R e os pacotes necessários. O arquivo `.devcontainer/Dockerfile` é responsável por criar essa imagem e o arquivo `.devcontainer/devcontainer.json` é responsável por configurar o ambiente de desenvolvimento no Github Codespaces.

No arquivo `Dockerfile`, é indicada a imagem ([Rocker, para o R](https://rocker-project.org/)), a versão do R e os pacotes desejados, assim como os pacotes Python para o uso do [Radian](https://github.com/randy3k/radian).

No arquivo `devcontainer.json`, é indicado o arquivo Docker a ser utilizado para montar o ambiente e as configurações de montagem, como a instalação do [Quarto](https://quarto.org/) para escrita científica e as extensões do VSCode desejadas.

## Utilização

Para utilizar o ambiente de desenvolvimento, copie o diretório `.devcontainer` para o seu projeto e faça as modificações desejadas, caso houver, nos arquivos `Dockerfile` e `devcontainer.json`. Em seguida, crie um repositório no Github e adicione o diretório do projeto. Por fim, crie um novo Codespace no repositório e aguarde a montagem do ambiente.