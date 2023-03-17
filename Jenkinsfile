node {
    def app

    stage('Clone repository') {
      

        checkout scm
    }

    stage('Build image') {
  
       app = docker.build("Diego/simplejavaapp")
    }

    stage('Test image') {
  
        docker.image('Diego/simplejavaapp:latest').withRun() { c ->
            sh ' echo "tested" '
    }
        
    }
  
   
}
