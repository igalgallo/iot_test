node {

stage('Clone Repository')
{
checkout scm
}

stage('Show me the files'){
sh "ls -l"
}

stage('Build docker image'){

sh "docker build -t iot_test:latest ."
}

stage('Docker login to hub and push the image'){
sh "docker login -u 'igalgallo' -p 'tx@Molsal75' "
sh "docker tag iot_test:latest igalgallo/iot_test:latest"
sh "docker push igalgallo/iot_test:latest"
}

stage('Apply changes to the environment') {
sh "ls -l"
}


}