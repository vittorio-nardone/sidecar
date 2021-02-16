FROM python:3.7-alpine
WORKDIR /
ENV FLASK_APP=/sidecar/src/app.py
ENV FLASK_RUN_HOST=0.0.0.0
ENV FLASK_ENV=development 
RUN apk add --no-cache gcc musl-dev linux-headers git
COPY requirements.txt requirements.txt
RUN pip install -r requirements.txt
EXPOSE 5000
CMD ["flask", "run"]