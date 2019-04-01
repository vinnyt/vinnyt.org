pipeline {
    agent {
      label 'mr-mime'
    }
    stages {
	   stage ('build') {
      steps{
		    sh 'hugo -D -F -b "http://10.1.1.77"'
	    }
    }
	   stage ('deploy') {
	    steps{
		    sh 'rsync -r "$WORKSPACE/public/" ryan@ponyta:/usr/share/nginx/html/'
	    }
	   }
    }
}
