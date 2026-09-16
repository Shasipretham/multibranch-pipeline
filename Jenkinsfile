pipeline {
    agent any
    stages {
        stage ("Build") {
            steps {
                sh 'docker build -t shasi5612/muiltibranch:bank .'
            }
        }
        stage ("Deploy") {
            steps {
                sh 'docker run -itd --name bank2 -p 4455:80 shasi5612/muiltibranch:bank'
            }
        }
    }
}
