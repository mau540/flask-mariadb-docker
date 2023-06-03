# FROM python:3.10.4-alpine
FROM python:3.10.4

# Actualiza e instala bash
# RUN apk update && apk add bash

# Crea una carpeta app y conviertela en el working directory
RUN mkdir /app
WORKDIR /app

# Copia los requerimientos e instalalos
COPY requirements.txt .
RUN pip install -r requirements.txt

# Copia el resto de los archivos
COPY . .

# Exponer el puerto para entrar a la applicación
EXPOSE 5771

# Ejecuta la app
CMD ["python", "app/app.py"]