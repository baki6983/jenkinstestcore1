pipeline {
agent any
environment {
dotnet = 'path\to\dotnet.exe'
}
stages {
stage ('Checkout') {
}
stage ('Restore PACKAGES') {
steps {
bat "dotnet restore --configfile NuGet.Config"
}
}
stage('Clean') {
steps {
bat 'dotnet clean'
}
}
stage('Build') {
steps {
bat 'dotnet build --configuration Release'
}
}
stage('Pack') {
steps {
bat 'dotnet pack --no-build --output nupkgs'
}
}