# DevopsWorkflow

## Parte 1

API em Python/FastAPI com o endpoint `GET /hello`, que retorna `Hello World`.
A aplicação é empacotada em uma imagem Docker (`python:3.12-slim` + uvicorn na porta 8000).

Build e execução local: `docker build -t luskation:1.0 .` e `docker run -p 8080:8000 luskation:1.0` (acesse `http://localhost:8080/hello`).
A cada push na `main`, o GitHub Actions faz o build da imagem, verifica se ela foi criada e publica no Docker Hub como `joseaaneto/luskation:1.0`.
