## Install requirements for windows machine
```
virtualenv env --python=python3.8
./env/bin/activate.ps1
pip install -r requirements.txt
```

## Reset DB
```
$env:FLASK_APP = "core/server.py"
rm core/store.sqlite3
flask db upgrade -d core/migrations/
```

## Start application
```
flask run
```

## Run Tests
```
pytest -vvv -s tests/

# for test coverage report
pytest --cov=core --cov-report=html
```
![image](https://github.com/user-attachments/assets/9a60958b-9172-4b19-b649-df7b8b5de139)

