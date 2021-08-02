node{

    stage('SCM Checkout')
    {
        git credentialsId: '7154b1ef-ece6-49cb-91d1-de2f4d959a21', url: 'https://github.com/dharish008/phpmysql-app.git'
    }
    
    stage('Run Docker Compose File')
    {
        sh 'sudo docker-compose build'
        sh 'sudo docker-compose up -d'
    }
  stage('PUSH image to Docker Hub')
    {
      /* withCredentials([string(credentialsId: 'harishtestdocker', variable: 'DHPWD')]) 
        {
            sh "docker login -u dharish008 -p ${DHPWD}"
        }
        sh 'docker push dharish008/phpmysql_app'
        */
        //docker.withRegistry( 'https://registry.hub.docker.com', 'DockerHubPassword' ) {
             
             sh 'sudo docker login -u "dharish008" -p "J#0led!IR65J%j$5" docker.io'
             //sh 'sudo docker push upasanatestdocker/mysql'
             //sh 'sudo docker push upasanatestdocker/job1_web1.0'
             sh 'sudo docker push dharish008/job1_web2.0'
            // sh 'docker push upasanatestdocker/mysql'
          
    }
}
