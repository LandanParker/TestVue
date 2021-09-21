FROM mcr.microsoft.com/dotnet/sdk:5.0 AS build
COPY bin/Release/net5.0/publish/ App/
WORKDIR /App
RUN dotnet dev-certs https --trust
ENTRYPOINT ["dotnet", "TestVue.dll"]
ENV ASPNETCORE_URLS=http://+:5000;https://+:5001
EXPOSE 5001/tcp
EXPOSE 5000/tcp