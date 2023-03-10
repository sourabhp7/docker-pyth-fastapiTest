# 
FROM python:3.9

# Set the current working directory to /code.
#This is where we'll put the requirements.txt file and the app directory.


WORKDIR /code

COPY ./requirements.txt /code/requirements.txt

RUN pip install --no-cache-dir --upgrade -r /code/requirements.txt

COPY . /code
#COPY main.py /code
#COPY schema.py /code
#COPY services.py /code
#COPY __init__.py /code
RUN mkdir -p /code/data
#RUN echo ls

CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "8080"]