pipeline {
    agent {
        docker {
            image 'https://github.com/carlossg/docker-maven/blob/32760466401d45fabb8166b5dcf9003b07598918/eclipse-temurin-11/Dockerfile' 
            args '-v /root/.m2:/root/.m2' 
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
