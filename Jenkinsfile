pipeline {
    agent {
        label 'test'
    }

    stages {
        stage('clone') {
            steps {
              git branch: 'main', url: 'https://github.com/udamale/terraform-cicd.git'
            }
        }
        stage('init') {
            steps {
                sh 'terraform init'
            }
        }
         stage('Terraform plan') {
            steps {
                sh 'terraform plan'
            }
        }
        stage('Terraform Apply') {
            steps {
                sh 'terraform apply -auto-approve'
            }
        }
        stage('Terraform Destroy') {
            steps {
                sh 'terraform destroy -auto-approve'
            }
        }
    }
}
