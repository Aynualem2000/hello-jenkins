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
                bat 'mvn clean package deploy -Dmule.version=${mule.version} -Dusername=${anypoint.username} -Dpassword=${anypoint.password} -Denvironment=${cloudhub.environment} -Dworkers=${cloudhub.worker} -Dworker.type=MICRO -Dapplication.name=${cloudhub.app}-API -DmuleDeploy'
            }
        }
    }
}