pipeline {
    agent any

    stages {
        stage('Build Application') {
            steps {
                bat 'mvn clean install'
            }
        }
        stage('Test Application') {
            steps {
                bat 'mvn clean test'
            }
        }
        stage('Deploy Application') {
            steps {
                bat 'mvn clean package deploy -Dmule.version=4.3.3 -Dusername=Banchi -Dpassword=Aynu761555 -Denvironment=Sandbox -Dworkers=1 -Dworker.type=MICRO -Dapplication.name=hello-jenkins-API -DmuleDeploy'
            }
        }
    }
}