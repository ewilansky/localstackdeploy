node {
    checkout scm
    
    stage ('Deploy To Kube') {
        docker.withServer('tcp://docker.for.mac.localhost:1234') {
            sh 'docker stack deploy app --compose-file /home/project/kube-compose.yml'
        }
    }      
}

// docker.withServer('unix:///var/run/docker.sock') {