pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                // Perform the checkout step
                checkout scm
            }
        }
        
        stage('Terraform Init') {
            steps {
                // Run Terraform init
                sh 'terraform init'
            }
        }
        
        stage('Terraform Plan') {
            steps {
                // Run Terraform plan
                sh 'terraform plan -out=tfplan'
            }
        }
        
        stage('Terraform Apply') {
            steps {
                // Run Terraform apply with auto-approve flag
                sh 'terraform apply -auto-approve tfplan'
            }
        }
    }
}
