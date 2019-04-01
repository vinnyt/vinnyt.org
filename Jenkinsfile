pipeline {
    agent {
      label 'mr-mime'
    }
    stages {
	   stage ('build') {
      steps{
		    sh 'hugo -D -F -b "https://vinnyt.org"'
	    }
    }
	   stage ('deploy') {
	    steps{
		    sh 'rsync -r "$WORKSPACE/public/" pi@pi.local:/var/www/html'
	    }
	   }
    }
}
