pipeline {
    agent any
    
    stages{
        stage("restore dependendies"){
          when { branch pattern: "(main)", comparator: "REGEXP" }
           steps{
            bat 'dotnet restore'
           } 
        }

        stage("build the project"){
          when { branch pattern: "(main)", comparator: "REGEXP" }
           steps{
            bat 'dotnet build'
           } 
        }

         stage("run the tests"){
          when { branch pattern: "(main)", comparator: "REGEXP" }
           steps{
            bat 'dotnet test --no-build --verbosity normal'
           } 
        }

   

           
        }
        }
