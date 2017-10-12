pipeline {
    agent none
    stages {
        stage('Build') {
            agent {
                docker {
                   image 'maven:3-alpine'
                   args '-v $HOME/.m2:/root/.m2'
                }
            }
            steps {
                git credentialsId: 'b13463b7-4f76-40e0-9f40-c1669db337a0', url: 'git@github.com:sitUboo/Yui.git'
                sh 'mvn package'
            }
        }          
        stage('Test') {
            agent {
                label 'linux'
            }
            steps {
                git credentialsId: 'b13463b7-4f76-40e0-9f40-c1669db337a0', url: 'git@github.com:buildit/jenkins-pipeline-examples.git'
            }
        }
    }
}
