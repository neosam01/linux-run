pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
               git branch: 'main', url: 'https://github.com/neosam01/jenkinstf.git'
            }
        }
        stage('Terraform init'){
         steps {
                sh 'terraform init'
         }
        }   
        stage('Terraform apply'){
         steps {
                sh 'terraform apply --auto-approve'
        }
        }   
        
         stage('Terraform destroy'){
         steps {
                sh 'terraform destroy --auto-approve'
        }
        }
        
    }
}
