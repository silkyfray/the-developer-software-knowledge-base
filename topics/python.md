## Python

### Pip

-

### Poetry

A dependency management system like `pip`.

#### Initialise a new project interactively

```
poetry init
```

##### Install packages

```
poetry install
```

#### Create a new shell within the project

https://python-poetry.org/docs/basic-usage/#activating-the-virtual-environment

```
poetry shell
```

#### How to update the lock file after conflicts without updating the package versions

````
poetry lock --no-update

### Pyenv
Manages python versions. Let's you switch  the global python version. It's like `nvm` for nodejs.

```
pyenv install 3.9.7 # install specific version
pyenv global 3.9.7 # use version globally
pyenv local 3.97 # use version locally. Also creates a local .python-version file
```

#### How to activate a virtual environment after it's been created?
```
source ~/.pyenv/versions/<python-version>/envs/<env-name>/bin/activate
```

#### What is the difference between the python virtual environment tools?
https://stackoverflow.com/a/41573588/1709981
https://nickolaskraus.org/articles/isolating-python-environments-with-pyenv-virtualenv-and-virtualenvwrapper/

### MyPy

### SQLAlchemy

SQLAlchemy is an ORM for Python.

#### How to use Python code for SQL Queries

[This](https://hackersandslackers.com/database-queries-sqlalchemy-orm/) article has excellent presentation how to use queries "LINQ" style.

### Celery

Celery is a distributed task queue that allows you to run async tasks from your Python script. It is often paired with a task broker like [RabbitMQ](./rabbitmq.md)

#### Commands

You can manually invoke a celery task through the command line as shown in this [answer](https://stackoverflow.com/questions/12900023/how-can-i-run-a-celery-periodic-task-from-the-shell-manually). Alternatively:

```python
# import the task definition within python
python
>>> celery_app.send_emails.apply()
INFO:root:send email result: <emails.backend.SMTPResponse status_code=250 status_text=b'OK queued as 491fc166-5f34-486f-b1d0-98a9c5f6a9ee'>
INFO:root:send email result: <emails.backend.SMTPResponse status_code=250 status_text=b'OK queued as 759af8e3-4c7d-4071-8117-21a8a0813711'>
INFO:celery.app.trace:Task app.core.celery_app.send_emails[8734ef99-277b-46e0-a5d9-f11acbdbd742] succeeded in 0.8479202999733388s: None
<EagerResult: 8734ef99-277b-46e0-a5d9-f11acbdbd742>
````

### Alembic

Alembic is a database migration tool used with SQLAlchemy.

Generating a new revision and let alembic decide the upgrade/downgrade schema

```bash
alembic revision --autogenerate -m "add organization"

```

### Pytest

Pytest is Python's premier testing tool

### Playwright

A python library to automate browser testing. Like cypress.

#### How to debug?

https://playwright.dev/python/docs/debug

#### How to select text input?

https://playwright.dev/python/docs/input/#text-input
