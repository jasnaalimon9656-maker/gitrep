pipeline{
    agent any
    stages{
        stage('checkout'){
            steps{
                deleteDir()
                echo "building started"
                sh '''
                    git clone https://github.com/jasnaalimon9656-maker/gitrep.git
                    ls -l
                '''
            }
        }
        stage('deploy'){
            steps{
                echo "deployment started"
                sh '''
                    rm -rf /var/www/html/*
                    cp -r gitrep/* /var/www/html/
                    ls -l /var/www/html/
                '''
            }
        }
    }
}
