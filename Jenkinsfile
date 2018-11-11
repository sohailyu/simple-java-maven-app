node('maven'){
    def mvnHome = tool name: 'maven360', type: 'maven'
    stage('Checkout'){
        echo "Downloading the source code"
        git credentialsId: 'github_id', url: 'https://github.com/sohailyu/simple-java-maven-app'
    }
    stage('Execute Test Cases'){
        echo "Test Execution"
        sh "$mvnHome/bin/mvn clean test"
	archiveArtifacts allowEmptyArchive: true, artifacts: 'target/surefire-reports/*'
	junit allowEmptyResults: true, testResults: 'target/surefire-reports/*.xml'


    }
}   
