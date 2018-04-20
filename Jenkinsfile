node {
    
    stage('checkout') {
  checkout scm
  // git 'http://github.com/dlukyanovgrid/jenkins2-course-spring-boot.git'
    
    def project_path = "spring-boot-samples/spring-boot-sample-atmosphere"
    
    dir(project_path) {
         stage('compiling, test, packaging') {
        sh 'mvn clean package'
         stage('archival') {
        archiveArtifacts "target/*.jar"
         }
         }
    }
}

    
}
