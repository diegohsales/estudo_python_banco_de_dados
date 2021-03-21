### Estudo em python sobre Banco de Dados ##

#Um pequeno estudo sobre banco de dados em Python, fazendo CRUD (CREATE, READ, UPDATE e DELETE - CRIAR, LER, ATUALIZAR e DELETAR).#

## Criando um Amabiente Virtual

pip install flask
pip install flake8

#Verificar e instalar o VENV
python -m virtualenv --version
pip install virtualenv

#Criar o VENV
(Windows) virtualenv venv
(unix) virtualenv venv --python=python3

#Ativar o VENV
(Windows) venv\Scripts\activate

#Instalando o Flask e Flake8
pip install flask flake8

Ou

python -m venv venvSQL
cd venvSQL\Scripts
activate.ps1 ou .\Activate.ps1

Caso precise habilitar politica de Segurança
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope LocalMachine(Politica de Seguraça Windows pelo PowerShell)
