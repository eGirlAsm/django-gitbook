do

```
./manage.py migrate
```

throw django.db.utils.IntegrityError: \(1215, 'Cannot add foreign key constraint'\)



just delete all app/migrations/\*.py except **\_\_init\_\_.py **

and recreate migrations files

```
./manage.py makemigrations
```

finally try 

```
./manage.py migrate
```



