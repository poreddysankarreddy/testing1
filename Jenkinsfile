pipeline {
agent {  label 'linux-node' }
stages {
stage('---clean---'){
tools {
maven 'mvn 3.8.5'
}
steps {

sh "mvn clean"
}
}
stage('---test---') {
tools {
maven 'mvn 3.6.1'
}
steps {

sh "mvn test"
}
}
stage('---package---'){

steps {

sh "mvn package"
}
}
}
post {
success {
echo 'job was built successfully'
}
failure {
echo 'job was not build..it was failed'
}
}
}
