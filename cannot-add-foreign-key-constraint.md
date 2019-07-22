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

NOTE that the error message cause that when migrate what that nothing changed .

I think that reason is i  droped database and recreate before migrate.

so after recreate database i mean you force truncate the database, then need **delete migrations file** or **makemigrations** to let the project had some changes.

