pipeline 
{
    agnent any
    stages
    {
       stage('scm checkout')
       {steps { git branch: 'master', url: 'https://github.com/neerajchauhan514/demodevops---java-maven-sonar-argocd-k8s.git'}}

        stage('compile the code')    //mnv compile command to compile the code
        {steps { withMaven(globalMavenSettingsConfig: '', jdk: 'JAVA_HOME', maven: 'MAVEN_HOME', mavenSettingsConfig: '', traceability: true) 
       {sh 'mvn compile'}} }
        stage('unit test execution') //mnv test command to execute the unit test case
        {steps { withMaven(globalMavenSettingsConfig: '', jdk: 'JAVA_HOME', maven: 'MAVEN_HOME', mavenSettingsConfig: '', traceability: true) 
         {sh 'mvn test'}} }

          stage('unit test artifact') //mnv package to generate artifact
        {steps { withMaven(globalMavenSettingsConfig: '', jdk: 'JAVA_HOME', maven: 'MAVEN_HOME', mavenSettingsConfig: '', traceability: true) 
         {sh 'mvn package'}} }
    }
}