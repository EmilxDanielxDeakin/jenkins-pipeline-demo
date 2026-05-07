pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                echo 'Stage 1: Build'
                echo 'Task: Compile and package the source code into a deployable artifact.'
                echo 'Auto-triggering.'
                echo 'Tool: Maven - used to manage dependencies and build the Java project (mvn clean package).'
            }
        }

        stage('Unit and Integration Tests') {
            steps {
                echo 'Stage 2: Unit and Integration Tests'
                echo 'Task: Run unit tests to verify individual components, and integration tests to verify component interactions.'
                echo 'Tools: JUnit (unit testing), Selenium (integration/UI testing).'
            }
        }

        stage('Code Analysis') {
            steps {
                echo 'Stage 3: Code Analysis'
                echo 'Task: Analyse source code for style issues, bugs, and standards compliance.'
                echo 'Tool: SonarQube - performs static code analysis and enforces quality gates.'
            }
        }

        stage('Security Scan') {
            steps {
                echo 'Stage 4: Security Scan'
                echo 'Task: Scan dependencies and code for known CVEs and security vulnerabilities.'
                echo 'Tool: OWASP Dependency-Check - identifies vulnerable third-party libraries.'
            }
        }

        stage('Deploy to Staging') {
            steps {
                echo 'Stage 5: Deploy to Staging'
                echo 'Task: Deploy the packaged application to a staging server for pre-production testing.'
                echo 'Tool: AWS CLI / Elastic Beanstalk - deploys artifact to a staging EC2 instance on AWS.'
            }
        }

        stage('Integration Tests on Staging') {
            steps {
                echo 'Stage 6: Integration Tests on Staging'
                echo 'Task: Run integration tests against the live staging environment to validate end-to-end behaviour.'
                echo 'Tool: Postman/Newman - runs API test collections against the staging server endpoints.'
            }
        }

        stage('Deploy to Production') {
            steps {
                echo 'Stage 7: Deploy to Production'
                echo 'Task: Deploy the verified application build to the production server.'
                echo 'Tool: AWS CLI / CodeDeploy - automates blue/green deployment to production EC2 instances.'
            }
        }

    }
}
