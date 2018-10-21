node {
    checkout scm
    
    stage ('Deploy To Kube') {
        docker.withServer('tcp://docker.for.mac.localhost:1234') {
            sh 'echo Working on deploy to Kubernetes Cocker CE integration w/Kuberneses orchestration'
            sh 'docker stack deploy app --compose-file /home/project/kube-compose.yml'
        }
    }
    // docker.withDockerServer('unix:///var/run/docker.sock') {
    // docker.withServer('tcp://docker.for.mac.localhost') {
        //sh 'echo Working on deploy to Kubernetes docker single-node cluster'
        //sh 'docker stack deploy --compose-file /home/project/kube-compose.yml tc'
    //}
        
}