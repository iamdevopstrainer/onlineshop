node{

    stage('SCM Checkout')
    {
        git 'https://github.com/iamdevopstrainer/onlineshop.git'
    }
    
    stage('Run Docker Compose File')
    {
        sh 'sudo docker-compose build'
    }
    
    stage('Push Docker Image to HUB')
    {
        sh 'sudo docker tag onlineshop_web iamdevopstrainer/onlineshop_web'
        sh 'sudo docker push iamdevopstrainer/onlineshop_web'
    }
    
    stage('Run Docker Container')
    {
        sh 'sudo docker run -itd -P iamdevopstrainer/onlineshop_web'
    }
    
}
