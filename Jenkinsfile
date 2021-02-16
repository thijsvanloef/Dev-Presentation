node( 'docker-agent' ) {
    checkout scm
    stage('Build'){
        docker.withServer( 'tcp://172.17.0.1:2375' ) {
            docker.image( 'node:12' ).inside {
                sh 'node --version'
            }
        }
    }
}
