FROM python:3.8-slim-buster

WORKDIR /app
RUN wget google.com

COPY requirements.txt requirements.txt
#RUN pip install -r requirements.txt
RUN python3 -m pip --trusted-host=pypi.python.org --trusted-host=pypi.org --trusted-host=files.pythonhosted.org install -r requirements.txt --user


COPY . .

CMD [ "python3", "-m" , "flask", "run", "--host=0.0.0.0"]