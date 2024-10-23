pipeline {
    agent any 
    stages {
        stage('Checkout') {
            steps {
                echo "Building"
                sh 'cat README.md'
            }
        }
    }
    post {
      always {
            cleanWs()
            dir("${env.WORKSPACE}@tmp") {
              deleteDir()
            }
            dir("${env.WORKSPACE}@script") {
              deleteDir()
            }
            dir("${env.WORKSPACE}@script@tmp") {
              deleteDir()
            }
      }
    }
}


//     git branch: 'main', url: 'git@github.com:HsuShelley/A.git'
// }
// dir('b') {
//     git branch: 'main', url: 'git@github.com:HsuShelley/B.git'
// }
