FROM python:{{cookiecutter.python_version}}

WORKDIR /app

RUN apt-get update && apt-get install --no-install-recommends -y \
  vim-tiny \
  binutils \
  libproj-dev \
  gdal-bin \
  python3-gdal \
  && rm -rf /var/lib/apt/lists/* && pip install pip-tools

COPY requirements.in /app/requirements.in
RUN pip-compile && pip install --no-cache-dir -r requirements.txt

COPY . /app
ENV PYTHONUNBUFFERED 1

CMD ["gunicorn", "--reload", "--workers={{cookiecutter.gunicorn_worker}}", "--worker-tmp-dir", "/dev/shm", "--bind=0.0.0.0:80", "--chdir", "/app/{{cookiecutter.project_name}}", "{{cookiecutter.project_name}}.wsgi"]
