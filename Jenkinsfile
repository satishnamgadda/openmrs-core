pipeline {
    agent { label 'build' }
    stages {
        stage('vcs') {
            steps {
                git url: "https://github.com/satishnamgadda/openmrs-core.git",
                    branch: "master"
            }
        }
        stage('buidstage') {
            steps {
                sh 'docker info'
                sh 'docker image build -t satish1990/openmrs:1.0 .'
                
            }
        }
        stage('push') {
            steps {
                sh 'docker image push satish1990/openmrs:1.0'
            }
        }
    }
}