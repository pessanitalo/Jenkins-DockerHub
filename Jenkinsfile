pipeline {
    agent any

    stages {
        stage('Start') {
            steps {
                echo 'Iniciando o build'
            }
        }
        stage('criando a imagem'){
            steps{
                script{
                    alpine = docker.build("italopessan/alpine:latest", '.')
                }
            }
        }
        stage('enviando a imagem para o docherhub'){
            steps{
                script{
                    docker.withRegistry('https://registry.hub.docker.com', 'dockerhub'){
                    alpine.push('latest')
                    }
                }
            }
        }

    }
}
