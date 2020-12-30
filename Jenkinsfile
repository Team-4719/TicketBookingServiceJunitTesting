pipeline {
    agent any
    stages {
        stage('git repo & clean') {
            steps {
                sh "rmdir ./TicketBookingServiceJunitTesting"
                sh "git clone https://github.com/kishancs2020/TicketBookingServiceJunitTesting.git"
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
