pipeline {
 agent any
 environment {
 DOCKER_USER = 'wolf31'
 }
 stages {
 stage('Login Docker') {
 steps {
 withCredentials([string(credentialsId:'DOCKER_PASSWORD_FWO', variable: 'DOCKER_PASS')]) {
 sh 'echo $DOCKER_PASS | docker login -u $DOCKER_USER --password-stdin'
 }
 }
 }
 }
}
