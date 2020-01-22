pipeline {
    agent {
        docker {
            image 'maven:3-alpine'
            args '-v /root/.m2:/Users/denismitin/.m2/repository'
        }
    }
    stages {
        stage('Build') {
            steps {
                sh 'mvn -B -DskipTests clean package'
            }
        }
    }
}