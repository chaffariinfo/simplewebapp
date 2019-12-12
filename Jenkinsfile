node{
        stage('phase de validation de code') 
        { 
            echo 'phase de validation de code '
            bat 'mvn validate'
        }
        stage('phase de compilation')
		{ 
            echo 'phase de compilation '
            bat 'mvn compile'
        }
        stage('phase de test') 
        { 
            echo 'phase de test '
            bat 'mvn test'
        }
		stage('test de qualite')
		{
			echo 'phase test de qualite'
			bat 'mvn sonar:sonar'
		}
        stage('phase de packaging') 
        { 
            echo 'phase de construstion package'
            bat 'mvn package'
        }
	stage('phase de test de qualité')
	{
		echo('phase test de qualité')
		bat 'mvn sonar:sonar'
	}
        stage('phase installation package') 
        { 
            echo 'phase d_intallation de pachake dans votre repo local '
            bat 'mvn install'
        }
        stage('deploiement vers nexus') 
        { 
            echo 'phase de deploiement artefact dans le référentiel distant'
            bat 'mvn deploy'
        }
 }
