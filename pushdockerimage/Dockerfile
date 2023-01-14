FROM bitnami/python:3.11.1

WORKDIR /app

RUN  apt-get update
RUN  apt-get upgrade
#RUN  apt install python3-pip
#RUN wget google.com
#RUN apt-get install update

#RUN nslookup pypi.org

COPY requirements.txt requirements.txt
#RUN python3 -m pip3 install Flask
RUN pip3 install -r requirements.txt
#RUN python3 -m pip --trusted-host=pypi.python.org --trusted-host=pypi.org --trusted-host=files.pythonhosted.org install -r requirements.txt --user


COPY . .

CMD [ "python3", "-m" , "flask", "run", "--host=0.0.0.0"]