pipeline {
    agent any

    stages {
        stage('Clonar repositório de teste na interfaceweb repositório') {
            steps {
                git branch: 'main', url: 'https://github.com/EBAC-QE/testes-e2e-ebac-shop'
            }
        }
        stage('Instalar dependências do projeto (Com base no sistema Windows)') {
            steps {
                bat 'npm install'
            }
        }
        stage('Executar testes do projeto (Com base no sistema Windows)') {
            steps {
                bat 'npm run cy:run'
            }
        }
    }
}