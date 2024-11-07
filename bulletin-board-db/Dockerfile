FROM mcr.microsoft.com/mssql/server:2019-latest

ENV ACCEPT_EULA=Y \
    MSSQL_SA_PASSWORD=DockerCon!!!

WORKDIR /init

# Copiar los archivos de inicialización sin necesidad de cambiar permisos
COPY init-db.* ./

# Ejecutar el servidor y el script de inicialización
CMD /opt/mssql/bin/sqlservr & ./init-db.sh
