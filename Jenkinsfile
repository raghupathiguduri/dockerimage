pipeline {
   agent {
        docker {
            image 'gcr.io/cloub-builders/docker'
	}
   }
   stages {
       stage( 'Build' ) {
           steps {
               sh 'docker build . --tag=hello-new'
           }
       }
       stage( 'deploy' ) {
           steps {
               sh 'docker run -d -p 80:80 hello-new'
           }
       }
   }
}
