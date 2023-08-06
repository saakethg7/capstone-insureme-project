node {
    
    stage('checkout code'){
        
        echo "checkout code from git"
        git 'https://github.com/saakethg7/capstone-insureme-project.git'
    }
    
    stage('code build,test, package'){
        echo "maven clean... compile... test... package"
        sh 'mvn clean package'
    }   
   
    
}
