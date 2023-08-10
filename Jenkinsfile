pipeline {
  agent {
    label 'mm-websrv-05'
//    customWorkspace '/var/www/html/react-app'
  }
  environment {
    APP_DIR = '/var/www/html/jenkins' // Custom application directory
  }
  stages {
    stage('Checkout') {
      steps {
 //       git url: 'https://github.com/your-username/your-nodejs-app.git', branch: 'main', credentialsId: 'correct-git-credentials-id'
	checkout scm
      }
    }
    stage('Move Files to Project Directory') {
      steps {
        sh "rsync -avz --exclude '.git' /var/www/html/jenkins/workspace/react-app/ ${APP_DIR}/"
}
}
   
  }
}
