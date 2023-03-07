FROM ubuntu:latest

WORKDIR /var/wwww

RUN apt-get update && \
    apt-get install -y wget

RUN wget https://packages.microsoft.com/config/debian/11/packages-microsoft-prod.deb -O packages-microsoft-prod.deb && \
    dpkg -i packages-microsoft-prod.deb && \
    rm packages-microsoft-prod.deb

RUN apt-get update && \
    apt-get install -y dotnet-sdk-6.0

RUN dotnet new webapp && \
    dotnet restore && \
    dotnet build

ENTRYPOINT [ "dotnet", "run" ]

## pode ser subustituido
CMD ["--urls=http://0.0.0.0:5001"] 