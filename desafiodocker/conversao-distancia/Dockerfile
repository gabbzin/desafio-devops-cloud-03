# FROM é para a imagem base, o dockerfile sempre deve começar com FROM
FROM python:3.12.3
# WORKDIR é o mesmo que mkdir /app e cd /app (Cria um diretório e entra no mesmo)
WORKDIR /app
# Instrução que pega um arquivo ou diretório e coloque dentro da imagem (O . se refere ao /app)
COPY requirements.txt .
# Instalando as dependências do projeto
RUN python -m pip install -r requirements.txt
# Copia todos os arquivos para o /app
COPY . .
# Instrução para inicializar o container (Executar)
CMD ["gunicorn", "--bind", "0.0.0.0:5000", "app:app"]