node {
    ansiColor('xterm') {
        stage('Prepare Env') {
            checkout scm
        }
        stage('Deploy') {
            def deploy_dir = 'deploy/k8s/'
            sh "kubectl apply -f ${deploy_dir}namespace"
            sh "kubectl apply -f ${deploy_dir}kube_state_metrics"
            sh "kubectl apply -f ${deploy_dir}prometheus/node_exporter"
            sh "kubectl apply -f ${deploy_dir}prometheus"
            sh "kubectl apply -f ${deploy_dir}grafana"
        }
    }
}
