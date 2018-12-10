node {
	stage 'Checkout'
		checkout scm

	stage 'Build'
		bat 'nuget restore jenkinscore1Demo.sln'
		bat "\"${tool 'MSBuild'}\" jenkinscore1Demo.sln /p:Configuration=Release /p:Platform=\"Any CPU\" /p:ProductVersion=1.0.0.${env.BUILD_NUMBER}"

	stage 'Archive'
		archive 'jenkinscore1Demo/bin/Release/**'

}