pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/TegarAdityaS/Devops-laravel.git'
            }
        }
        stage('Build') {
            steps {
                sh 'composer install'
                sh 'php artisan migrate'
            }
        }
    }
}
