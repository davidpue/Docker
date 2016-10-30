FROM microsoft/windowsservercore

SHELL ["powershell", "-Command", "$ErrorActionPreference = 'Stop';"]

RUN New-Item -Path C:\\MyApp -Type Directory
RUN netsh http add urlacl url=http://+:80/ user=ContainerAdministrator
WORKDIR C:\\MyApp

ADD Debug .

EXPOSE 80
CMD .\SelfHost.exe