pipeline {
    agent any
    stages {
        stage ("Build") {
            steps {
                sh 'docker build -t shasi5612/muiltibranch:bus .'
            }
        }
        
        stage ("Deploy") {
            steps {
                sh 'docker run -itd --name bus -p 8888:80 shasi5612/muiltibranch:bus'
            }
        }
    }
}
