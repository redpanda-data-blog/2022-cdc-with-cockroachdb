FROM python:3-alpine
USER root
RUN adduser -D muser
RUN pip install psycopg2-binary
ADD manager.py /home/muser
RUN chmod a+x /home/muser/manager.py
USER muser
ENTRYPOINT ["/home/muser/manager.py"]