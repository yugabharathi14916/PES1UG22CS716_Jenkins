pipeline {
    agent any
    stages {
        // stage('Clone repository') {
        //     steps {
        //         checkout([$class: 'GitSCM',
        //             branches: [[name: '*/main']],
        //             userRemoteConfigs: [[url: 'https://github.com/yugabharathi14916/PES1UG22CS716_Jenkins.git']]
        //         ])
        //     }
        // }

        stage('Build') {
            steps {
                build 'PES1UG22CS716-1'
                sh 'g++ main.cpp -o output'
            }
        }

        stage('Test') {
            steps {
                sh './output'
            }
        }

        stage('Deploy') {
            steps {
                echo 'deploy'
            }
        }
    }

    post {
        failure {
            error "Pipeline failed"
        }
    }
}
