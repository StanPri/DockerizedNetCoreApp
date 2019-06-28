FROM mcr.microsoft.com/dotnet/core/runtime:2.2
WORKDIR /app

# Copy csproj and restore as distinct layers
COPY *.csproj ./
RUN dotnet restore

# Copy everything else and build
COPY bin/Release/netcoreapp2.2/publish/ app/
ENTRYPOINT ["dotnet", "DockerizedApplication.dll"]