pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                // Шаг для клонирования репозитория, если необходимо
                // Например, если файлы конфигурации Terraform находятся в репозитории
                checkout scm
            }
        }
        
        stage('Terraform Init') {
            steps {
                // Инициализация Terraform
                sh 'terraform init'
            }
        }
        
        stage('Terraform Plan') {
            steps {
                // Создание плана Terraform
                sh 'terraform plan'
            }
        }
        
        stage('Terraform Apply') {
            steps {
                // Применение изменений Terraform
                sh 'terraform apply'
            }
        }
    }
}
