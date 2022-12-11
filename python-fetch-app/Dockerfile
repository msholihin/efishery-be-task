FROM python:3.9

WORKDIR /usr/src/app

COPY ./python-fetch-app ./app
COPY ./cache/ ./cache
COPY ./.jwt_pass ./.jwt_pass

RUN cd ./app && pip install --no-cache-dir -r requirements.txt

EXPOSE 5000/tcp

WORKDIR ./app

ENTRYPOINT ["python"]

CMD ["app.py"]
