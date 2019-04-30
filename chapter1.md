# django filter another model

refer to [https://docs.djangoproject.com/en/2.2/ref/models/lookups/](https://docs.djangoproject.com/en/2.2/ref/models/lookups/)

first need use foreign key

```
class Bbb(models.Model):
    b_index = models.AutoField(primary_key=True)

class Test(models.Model):
    xxx = models.Foreignkey('bbb')
```

and for here

```
Test.objects.filter(xxx__b_index=30)
```

Note that

using another model

* use foreignkey 
* '_' contain this string  \_\_\_ to connect Model_\_\_field= xxx



