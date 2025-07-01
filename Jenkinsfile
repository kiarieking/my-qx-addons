pipeline{
    agent any

    stages{
        stage("A"){
            steps{
                echo "========updating odoo modules========"

                sh '''
                    cd /opt/odoo14

                    ./odoo-bin -u all -d kiariedb212 --stop-after-init

                    '''
            }
            post{
                always{
                    echo "========always========"
                }
                success{
                    echo "========A executed successfully========"
                }
                failure{
                    echo "========A execution failed========"
                }
            }
        }
    }
    post{
        always{
            echo "========always========"
        }
        success{
            echo "========pipeline executed successfully ========"
        }
        failure{
            echo "========pipeline execution failed========"
        }
    }
}