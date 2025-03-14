node {
    checkout scm

    stage("Build") {
        docker.image('shippingdocker/php-composer:7.4').inside("--user root") {
            sh 'rm composer.lock'
            sh 'composer install'
        }
    }

    stage("Testing") {
        docker.image('ubuntu').inside("--user root") {
            sh 'echo "Ini adalah test"'
        }
    }
}
