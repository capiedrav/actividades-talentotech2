FROM python:3.11-slim

ENV PYTHONDONTWRITEBYTECODE=1
ENV PYTHONUNBUFFERED=1

# create user app_user
RUN addgroup --gid 1000 app_user && \
    adduser --uid 1000 --gid 1000 --disabled-password --gecos "" app_user --home /home/app_user

EXPOSE 8000

WORKDIR /home/app_user/drf-quickstart

# install requirements
COPY ./requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

# copy source code
COPY . .

# change ownership and permissions
RUN chown -R app_user:app_user . && chmod -R 755 .

# set app_user as default user
USER app_user

# start the app
CMD ["python",  "/home/app_user/drf-quickstart/manage.py", "runserver", "0.0.0.0:8000"]
