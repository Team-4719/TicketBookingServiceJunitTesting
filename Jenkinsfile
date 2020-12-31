pipeline {
    agent any
    stages {
        stage('Back-end') {
            
            steps {
                sh 'mvn --version'
            }
        }
        stage('git repo & clean') {
            steps {
                sh "mvn clean -f TicketBookingServiceJunitTesting"
            }
        }
        stage('install') {
            steps {
                sh "mvn install -f TicketBookingServiceJunitTesting"
            }
        }
        stage('test') {
            steps {
                sh "mvn test -f TicketBookingServiceJunitTesting"
            }
        }
        stage('package') {
            steps {
                sh "mvn package -f TicketBookingServiceJunitTesting"
            }
        }
    }
}
