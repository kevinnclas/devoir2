FROM python:latest

#installation des librairies
RUN apt-get update
RUN pip install psycopg2

RUN wget https://raw.githubusercontent.com/vishnubob/wait-for-it/master/wait-for-it.sh -P /
RUN chmod +x /wait-for-it.sh
ENTRYPOINT ["/wait-for-it.sh", "db:5432", "--"]

COPY . /manager

CMD ["python","-m","manager"]

