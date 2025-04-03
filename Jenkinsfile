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
    }
}
