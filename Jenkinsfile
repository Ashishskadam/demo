node {
    stage('Build') {
       
    }
    stage('Test') {
        sh 'make check'
        junit 'reports/**/*.xml'
    }
    if (currentBuild.currentResult == 'SUCCESS') {
        stage('Deploy') {
            sh 'make publish'
        }
    }
}
