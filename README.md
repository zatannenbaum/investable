# investable
Investing data for making decisions

## Setup


### Set Up virtual env: 
make sure you have python3 installed by calling `which python3` in terminal and copy the path returned
`virtualenv env -p [path to python3]`

Before starting your virtualenv, you'll need to set environment variables, so open `env/bin/activate` and under `deactivate()` put:
```
unset DATABASE_NAME
unset DATABASE_USER
unset DATABASE_PASSWORD
```

And at the very bottom of the same file put:
```
export DATABASE_NAME='investable'
export DATABASE_USER='investor'
export DATABASE_PASSWORD='investable'
```


Now we can run:

```
source env/bin/activate
pip install -r requirements.txt
```

### For Postgres DB:

Download postgres here and follow the download instructions: https://github.com/PostgresApp/PostgresApp/releases/download/v2.0.2/Postgres-2.0.2.dmg

Make sure that Postgres is open (there should be an elephant on top of your screen. Then on the command line:
```
createdb investable
psql -c "CREATE USER investor WITH PASSWORD 'investable';"
```
