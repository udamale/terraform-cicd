pipeline {
    agent any

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
         stage('plan') {
            steps {
                sh 'terraform plan'
            }
        }
    }
}
