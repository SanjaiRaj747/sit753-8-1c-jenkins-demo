pipeline {
  agent any
  triggers { pollSCM('H/2 * * * *') } // matches the job trigger
  stages {
    stage('Build') { steps { echo 'Build: e.g., Maven/Gradle' } }
    stage('Unit & Integration Tests') { steps { echo 'Run unit + integration tests' } }
    stage('Code Analysis') { steps { echo 'Static analysis (e.g., Sonar/Checkstyle)' } }
    stage('Security Scan') { steps { echo 'SCA/SAST scan' } }
    stage('Deploy to Staging') { steps { echo 'Deploy to staging (EC2/Docker)' } }
    stage('Integration Tests on Staging') { steps { echo 'E2E/contract tests' } }
    stage('Deploy to Production') { steps { echo 'Production deploy (approval)' } }
  }
}

