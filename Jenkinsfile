pipeline {
agent any
stages {
stage('Clone Repository') {
steps {
git 'https://github.com/YOUR_USERNAME/Maven-Jenkins-App.git'
}
}
stage('Check Java Version') {
steps { sh 'java -version' }
}
stage('Check Maven Version') {
steps { sh 'mvn -version' }
}
stage('Clean Project') {
steps { sh 'mvn clean' }
}
stage('Build Project') {
steps { sh 'mvn clean install' }
}
stage('Run Tests') {
steps { sh 'mvn test' }
}
stage('Package Application') {
steps { sh 'mvn package' }
}
stage('Custom Message') {
steps {
echo 'Maven Build and Jenkins Pipeline Executed Successfully!'
}
}
}
post {
success { echo 'BUILD SUCCESS' }
failure { echo 'BUILD FAILED' }
always { echo 'Pipeline execution finished.' }
}
}
