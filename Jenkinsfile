node {
  stage('Build traefik') {
    checkout scm
    docker.withRegistry('https://jenkins.paulbunyan.net:5000', 'pbc-docker-registry') {
      def img = docker.build('traefik')
      img.push('latest')
  }
}