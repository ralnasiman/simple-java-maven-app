maven {
    docker.image('maven').inside('-p 3000:3000') {
        stage('Build') {
            sh 'mvn clean package'        
        }
        stage('Test') {
            sh "chmod +x -R ${env.WORKSPACE}"
            sh 'mvn test'
        }
    }
}