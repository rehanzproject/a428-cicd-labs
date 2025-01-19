node {
    // Use Docker with the 'node:16-buster-slim' image
    docker.image('node:16-buster-slim').inside('-p 3000:3000') {
        
        stage('Build') {
            // Run 'npm install' in the Build stage
            sh 'npm install'
        }
        
        stage('Test') {
            // Run the custom test script in the Test stage
            sh './jenkins/scripts/test.sh'
        }
    }
}
