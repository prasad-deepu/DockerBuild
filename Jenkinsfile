pipeline {
agent any
stages {
stage('Verify Branches') {
steps {
	echo "$GIT_BRANCH"
}
}

stage('Docker Build'){
	steps{
			
			sh(script: 'sudo docker images -a')
			sh(script : """
			cd /home/prasad_deepu
			sudo docker build -t jenkins-pipeline .
			sudo docker images -a
			""")

}
}
}
}
