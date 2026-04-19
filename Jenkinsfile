pipeline {
    agent any
    environment {
        IMAGE_NAME = "webapp"
    }

    stages {

        // Job1: Build
        stage('Build') {
            steps {
                echo "Building Docker Image"
                sh 'docker build -t $IMAGE_NAME .'
            }
        }

        //Job2: Test
        stage('Test') {
            steps {
                echo "Running Test Container"
                sh 'docker rm -f test-container || true'
                sh 'docker run -d --name test-container -p 8083:80 $IMAGE_NAME'
            }
<<<<<<< Updated upstream
 	}
        
=======
        }

>>>>>>> Stashed changes
    }
}
