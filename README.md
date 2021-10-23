# Compila o código desejado
    
       gcc trab1.c -o trab1

# Lista todos os processos e faz um filtro pelo processo desejado

    top -p `pgrep trab1 | tr "\\n" "," | sed 's/,$//'`

# Mostra a árvore de processos e realiza um filtro pelo processo desejado

    pstree -snp `pgrep gnome-terminal | head -1`

# ps = process status

    ps aux | grep trab1








































### `VIRTUALENVS` == Virtual Environments

Comando do python que cria a virtualenv (Ambiente isolado python. Normalmente não é colocada no github, cada pessoa pode criar seu próprio ambiente)

    python -m venv virtualenv

Comando para ativar a virtualenv (É diferente no Windows)

    source virtualenv/bin/activate

Comando para atualizar o instalador de pacotes da virtualenv

    pip install --upgrade pip


Comando para instalar pacote dentro da virtualenv

Os pacotes podem ser buscados através do índice de pacotes do python [PyPI](https://pypi.org/)

    pip install pacote

Comando para listar os pacotes instalados na sua virtualenv

    pip list

Comando para criar um arquivo de texto com os pacotes instalados na virtualenv e suas versões

    pip freeze > requirements.txt

Comando para instalar na virtualenv os requisitos listados em requirements.txt

    pip install -r requirements.txt

### `DOCKER`

Comando para criar os containers listados no docker-compose.yml e Dockerfile

    docker-compose up

### `EXECUÇÃO`

Comando para executar os testes

    python src/main.py

Comando executar o framework de testes mais famoso do python e framework selenium-base

    pytest src/main.py





