Here I am using Visual studio 2019 for creating docker container and run my application using docker container.
I created a ASP .NET CORE Web Application named as DockerApp.
Steps-

1. enable docker linux support
2. The docker file is the file used inside docker to define how your container will be executed.
3. Here In docker file it metioned from image what inside and what does it contains and so on and it provide the sdk
4. WORKDIR-- Work directory , that i say I will go through the app file or folder
5. EXPOSE 80--- that I need to connect to 80 port.
6. FROM --actually do the building for my project like copy image and it sit the working directory and copy, the project it restores the nuget packages for this 
and build the project as release "RUN dotnet build "DockerApp.csproj" -c Release -o /app/build"
7. Publish run the application and atlast ENTRYPOINT for the application, which will connect the dotnet cli command to the dll for the project
--------------------------------
To run you must have docker app installed in your system.
Now application is running inside the docker containers.
