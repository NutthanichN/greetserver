pipeline {
     agent { label 'master' }
     environment {
          HOME = '.'
     }
     stages {
          stage('Source') {
               steps {
                    git branch: 'main',
                        url: 'https://github.com/NutthanichN/greetserver.git'
               }
          }
          stage('Build') {
               steps {
                    // sh 'npm install'
                    bat 'npm install'
               }
          }
          stage('Test') {
               steps {
                    echo 'testing...'
               }
          }
          stage('Deploy') {
               steps {
                    // sh 'npm start'
                    bat 'npm start'
               }
          }
     }
}
