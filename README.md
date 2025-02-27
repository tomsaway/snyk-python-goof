# Dependency Management Workflows

## Option 1: Using `requirements.txt` with `venv`

1. **Change directory to `pip-sample`**
   cd pip-sample

2. **Create a Virtual Environment (if not already installed)**
   python -m venv venv-pip

3. **Activate the Virtual Environment**
   .\venv-pip\Scripts\activate

4. **Install Dependencies from requirements.txt**
   pip install -r requirements.txt

5. **Run Tests with Snyk**
   snyk test --file=requirements.txt

6. **Deactivate the Environment**
   deactivate

cd pip-sample
python -m venv venv-pip
.\venv-pip\Scripts\activate
pip install -r requirements.txt
snyk test --file=requirements.txt
deactivate

## Option 2: Using Pipenv

1. **Change directory to `pipenv-sample`**
   cd ..\pipenv-sample

2. **Install Pipenv (if not already installed)**
   pip install pipenv

3. **Install Dependencies from Pipfile**
   pipenv install Pipfile

4. **Activate the Virtual Environment**
   pipenv shell

5. **Run Tests with Snyk**
   snyk test

6. **Exit the Virtual Environment**
   exit

cd ..\pipenv-sample
pipenv install Pipfile
pipenv shell
snyk test
snyk monitor
exit

## Option 3: Using Poetry

1. **Change directory to `poetry-sample`**
   cd ..\poetry-sample

2. **Install Poetry (if not already installed)**
   curl -sSL https://install.python-poetry.org | python3 -

3. **Install Dependencies from pyproject.toml**
   poetry install

4. **Activate the Virtual Environment**
   poetry shell

5. **Run Tests with Snyk**
   snyk test

6. **Exit the Virtual Environment**
   exit

cd ..\poetry-sample
poetry install
poetry shell
snyk test
snyk monitor
exit

## Option 4: Using setup.py

1. **Change directory to `setup-sample`**
   cd ..\setup-sample

2. **Create a Virtual Environment (if not already installed)**
   python -m venv venv-setup

3. **Activate the Virtual Environment**
   .\venv-setup\Scripts\activate

4. **Install Dependencies from `setup.py` (if not already installed)**
   pip install -e .

5. **Run Tests with Snyk**
   snyk test --file=setup.py

6. **Deactivate the Environment**
   deactivate

cd ..\setup-sample
python -m venv venv-setup
venv-setup\Scripts\activate
pip install -e .
snyk test --file=setup.py
snyk monitor --file=setup.py
deactivate
