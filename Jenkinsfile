pipeline {
    agent { label 'MAVEN_JDK8' }
    stages {
        stage('vcs') {
            steps {
                git url: 'https://github.com/raviteja811811/hackathon-starterr.git',
                branch: 'try'
            }
        }
         stage('Build') {
            steps {                
                    sh 'npm install'
                    sh 'npm run build'
            }
        }
        stage('Scan Images') {
            steps {
                    sh 'trivy image -d'          
            }  
        }
    }
}


