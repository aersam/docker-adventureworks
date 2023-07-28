FROM mcr.microsoft.com/mssql/server:2022-latest
ARG BAK_FILE
ARG SA_PASSWORD
ENV MSSQL_PID=Express
ENV SA_PASSWORD=${SA_PASSWORD}
EXPOSE 1433
WORKDIR /
COPY $BAK_FILE ./adventureworks.bak
COPY ./install.sql .
COPY ./install.sh .
COPY ./startup.sh .
CMD /bin/bash ./startup.sh