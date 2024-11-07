FROM mcr.microsoft.com/mssql/server:2019-latest

ENV ACCEPT_EULA=Y \
    MSSQL_SA_PASSWORD=DockerCon!!!

WORKDIR /init
COPY init-db.* ./

RUN chmod +x ./init-db.sh

# Ejecuta el servidor y el script de inicialización
CMD /opt/mssql/bin/sqlservr & ./init-db.sh
