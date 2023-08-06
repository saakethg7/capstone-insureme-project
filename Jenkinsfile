node{
        stage('git checkout'){
            echo "checking out the code from github"
            cleanWs()
            git poll: true, url: 'https://github.com/saakethg7/capstone-insureme-project.git'
        }
        
        stage('maven build'){
            sh 'mvn clean package'
        }
        
        stage('build docker image'){
            sh 'docker build -t saakethg7/insure-me:2.0 .'
        }
        
        stage('push docker image to docker hub registry')
        {
            echo 'pushing images to registry'
            withCredentials([string(credentialsId: 'dockerHubPassword', variable: 'dockerHubPwd')])
            {
                sh "docker login -u saakethg7 -p ${dockerHubPwd}"
                sh 'docker push saakethg7/insure-me:2.0'
            }
        }
    }
