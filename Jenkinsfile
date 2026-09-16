pipeline {
    agent any
    stages {
        stage ("Build") {
            steps {
                sh 'docker build -t shasi5612/muiltibranch:train .'
            }
        }
        stage ("Deploy") {
            steps {
                sh 'docker run -itd --name train -p 9999:80 shasi5612/muiltibranch:train'
            }
        }
    }
}
