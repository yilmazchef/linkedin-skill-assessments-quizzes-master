## Django

#### Q1. To cache your entire site for an application in Django, you add all except which of these settings?

- [ ] django.middleware.common.CommonMiddleware
- [ ] django.middleware.cache.UpdateCacheMiddleware
- [ ] django.middleware.cache.FetchFromCacheMiddleware
- [x] django.middleware.cache.AcceleratedCacheMiddleware

#### Q2. In which programming language is Django written?

- [ ] C++
- [ ] Java
- [x] Python
- [ ] Ruby

#### Q3. To automatically provide a value for a field, or to do validation that requires access to more than a single field, you should override the `___` method in the `___` class.

- [ ] validate(); Model
- [ ] group(); Model
- [ ] validate(); Form
- [x] clean(); Field

#### Q4. A client wants their site to be able to load "Rick & Morty" episodes by number or by title—e.g., shows/3/3 or shows/picklerick. Which URL pattern do you recommend?

- [ ]

```
url(r'shows/<int:season>/<int:episode>/', views.episode_number),
url(r'shows/<slug:episode_name>/', views.episode_name)
```

- [x]

```
path('shows/<int:season>/<int:episode>/', views.episode_number),
path(r'shows/<slug:episode_name>/', views.episode_name)
```

- [ ]

```
path('shows/<int:season>/<int:episode>', views.episode_number),
path(r'shows/<slug:episode_name>/', views.episode_number)
```

- [ ]

```
url(r'^show/(?P<season>[0-9]+)/(?P<episode>[0-9]+)/$', views.episode_number),
url(r'^show/(?P<episode_name>[\w-]+)/', views.episode_name
```

#### Q5. How do you determine at startup time if a piece of middleware should be used?

- [x] Raise MiddlewareNotUsed in the **init** function of your middleware.
- [ ] Implement the not_used method in your middleware class.
- [ ] List the middleware beneath an entry of django.middleware.IgnoredMiddleware.
- [ ] Write code to remove the middleware from the settings in [app]/**init**.py.

#### Q6. How do you turn off Django’s automatic HTML escaping for part of a web page?

- [ ] Place that section between paragraph tags containing the autoescape=off switch.
- [ ] Wrap that section between { percentage mark autoescape off percentage mark} and {percentage mark endautoescape percentage mark} tags.
- [ ] Wrap that section between {percentage mark autoescapeoff percentage mark} and {percentage mark endautoescapeoff percentage mark} tags.
- [x] You don't need to do anything—autoescaping is off by default.

#### Q7. Which step would NOT help you troubleshoot the error "django-admin: command not found"?

- [ ] Check that the bin folder inside your Django directory is on your system path.
- [ ] Make sure you have activated the virtual environment you have set up containing Django.
- [ ] Check that you have installed Django.
- [x] Make sure that you have created a Django project.

#### Q8. Every time a user is saved, their quiz_score needs to be recalculated. Where might be an ideal place to add this logic?

- [ ] template
- [x] model
- [ ] database
- [ ] view

#### Q9. What is the correct way to begin a class called "Rainbow" in Python?

- [ ] Rainbow {}
- [ ] export Rainbow:
- [x] class Rainbow:
- [ ] def Rainbow:

#### Q10. You have inherited a Django project and need to get it running locally. It comes with a requirements.txt file containing all its dependencies. Which command should you use?

- [ ] django-admin startproject requirements.txt
- [ ] python install -r requirements.txt
- [x] pip install -r requirements.txt
- [ ] pip install Django

#### Q11. Which best practice is NOT relevant to migrations?

- [x] To make sure that your migrations are up to date, you should run updatemigrations before running your tests.
- [ ] You should back up your production database before running a migration.
- [ ] Your migration code should be under source control.
- [ ] If a project has a lot of data, you should test against a staging copy before running the migration on production.

#### Q12. What will this URL pattern match? url(r'^\$', views.hello)

- [ ] a string beginning with the letter Ra string beginning with the letter R
- [x] an empty string at the server root
- [ ] a string containing ^ and $a string containing ^ and $
- [ ] an empty string anywhere in the URLan empty string anywhere in the URL

#### Q13. What is the typical order of an HTTP request/response cycle in Django?

- [x] URL > view > template
- [ ] form > model > view
- [ ] template > view > model
- [ ] URL > template > view > model

#### Q14. Django's class-based generic views provide which classes that implement common web development tasks?

- [ ] concrete
- [ ] thread-safe
- [x] abstract
- [ ] dynamic

#### Q15. Which skills do you need to maintain a set of Django templates?

- [ ] template syntax
- [x] HTML and template syntax
- [ ] Python, HTML, and template syntax
- [ ] Python and template syntax

#### Q17. How would you define the relationship between a star and a constellation in a Django model?

- [x]

```
class Star(models.Model):
name = models.CharField(max_length=100)
class Constellation(models.Model):
stars = models.ManyToManyField(Star)
```

- [ ]

```
class Star(models.Model):
constellation = models.ForeignKey(Constellation, on_delete=models.CASCADE)
class Constellation(models.Model):
stars = models.ForeignKey(Star, on_delete=models.CASCADE)
```

- [ ]

```
class Star(models.Model):
name = models.CharField(max_length=100)
class Constellation(models.Model):
stars = models.OneToManyField(Star)
```

- [ ]

```
class Star(models.Model):
constellation = models.ManyToManyField(Constellation)
class Constellation(models.Model):
name = models.CharField(max_length=100)
```

#### Q18. Which is NOT a valid step in configuring your Django 2.x instance to serve up static files such as images or CSS?

- [x] In your urls file, add a pattern that includes the name of your static directory.
- [ ] Create a directory named static inside your app directory.
- [ ] Create a directory named after the app under the static directory, and place static files inside.
- [ ] Use the template tag {percentage mark load static percentage mark}.

#### Q19. What is the correct way to make a variable available to all of your templates?

- [ ] Set a session variable.
- [ ] Use a global variable.
- [ ] Add a dictionary to the template context.
- [x] Use RequestContext.

#### Q20. Should you create a custom user model for new projects?

- [ ] No. Using a custom user model could break the admin interface and some third-party apps.
- [ ] Yes. It is easier to make changes once it goes into production.
- [x] No. Django's built-in models.User class has been tried and tested—no point in reinventing the wheel.
- [ ] Yes, as there is no other option.

#### Q21. You want to create a page that allows editing of two classes connected by a foreign key (e.g., a question and answer that reside in separate tables). What Django feature can you use?

- [x] actions
- [ ] admin
- [ ] mezcal
- [ ] inlines

#### Q22. Why are QuerySets considered "lazy"?

- [ ] The results of a QuerySet are not ordered.
- [x] QuerySets do not create any database activity until they are evaluated.
- [ ] QuerySets do not load objects into memory until they are needed.
- [ ] Using QuerySets, you cannot execute more complex queries.

#### Q23. You receive a `MultiValueDictKeyError` when trying to access a request parameter with the following code: request.GET['search_term']. Which solution will NOT help you in this scenario?

- [x] Switch to using POST instead of GET as the request method.
- [ ] Make sure the input field in your form is also named "search_term".
- [ ] Use MultiValueDict's GET method instead of hitting the dictionary directly like this: request.GET.get('search_term', '').
- [ ] Check if the search_term parameter is present in the request before attempting to access it.

#### Q24. Which function of Django's Form class will render a form's fields as a series of <p> tags?

- [ ] show_fields()
- [x] as_p()
- [ ] as_table()
- [ ] fields()

#### Q25. You have found a bug in Django and you want to submit a patch. Which is the correct procedure?

- [ ] Fork the Django repository GitHub.
- [ ] Submit a pull request.
- [x] all of these answers.
- [ ] Run Django's test suite.

#### Q26. Django supplies sensible default values for settings. In which Python module can you find these settings?

- [ ] django.utils.default_settings.py
- [ ] django.utils.global_settings.py
- [ ] django.conf.default_settings.py
- [x] django.conf.global_settings.py

#### Q27. Which variable name is best according to PEP 8 guidelines?

- [ ] numFingers
- [ ] number-of-Fingers
- [x] number_of_fingers
- [ ] finger_num

#### Q28. A project has accumulated 500 migrations. Which course of action would you pursue?

- [ ] Manually merge your migration files to reduce the number
- [ ] Don't worry about the number
- [ ] Try to minimize the number of migrations
- [x] Use squashmigrations to reduce the number

#### Q29. What does an F() object allow you when dealing with models?

- [x] perform db operations without fetching a model object
- [ ] define db transaction isolation levels
- [ ] use aggregate functions more easily
- [ ] build reusable QuerySets

#### Q30. Which is not a django filed type for integers?

- [ ] SmallIntegerField
- [x] NegativeIntegerField
- [ ] BigAutoField
- [ ] PositiveIntegerField

#### Q31. Which will show the currently installed version?

- [ ] print (django.version)
- [ ] import django django.getVersion()
- [x] import django django.get_version()
- [ ] python -c django --version

#### Q32. You should use the http method `___` to read data and `___` to update or create data

- [ ] READ; WRITE
- [x] GET; POST
- [ ] POST; GET
- [ ] GET; PATCH

#### Q33. When should you employ the POST method over GET for submitting data?

- [ ] when efficiency is important
- [ ] when you want the data to be cached
- [ ] when you want to use your browser to help with debugging
- [x] when the data in the form may be sensitive

#### Q34. When to use the Django sites framework?

- [x] if your single installation powers more than one site
- [ ] if you need to serve static as well as dynamic content
- [ ] if you want your app have a fully qualified domain name
- [ ] if you are expecting more than 10.000 users

#### Q35. Which infrastructure do you need:

`title=models.charfield(max_length=100, validators=[validate_spelling])`

- [ ] inizialized array called validators
- [x] a validators file containing a function called validate_spelling imported at the top of model
- [ ] a validators file containing a function called validate imported at the top of model
- [ ] spelling package imported at the top of model

#### Q36. What decorator is used to require that a view accepts only the get and head methods?

- [x] require_safe()
- [ ] require_put()
- [ ] require_post()
- [ ] require_get()

#### Q37. How would you define the relation between a book and an author - book has only one author.

- [ ]

```
class Author (models.model):
book=models.foreignkey(Book,on_delete=models.cascade)
class Book(models.model):
name=models.charfield(max_length=100)
```

- [x]

```python
class Author (models.model):
name=models.charfield(max_length=100)
class Book(models.model):
author=models.foreignkey(Author,on_delete=models.cascade)
```

- [ ]

```
class Author (models.model):
name=models.charfield(max_length=100)
class Book(models.model):
author=models.foreignkey(Author)
```

- [ ]

```
class Author (models.model):
name=models.charfield(max_length=100)
class Book(models.model):
author=models.foreignkey(Author,on_delete=models.cascade)
```

- [ ]

```
class Author (models.model):
name=models.charfield(max_length=100)
class Book(models.model):
author=Author.name
```

#### Q38. What is a callable that takes a value and raises an error if the value fails?

- [x] validator
- [ ] deodorizer
- [ ] mediator
- [ ] regular expression

#### Q39. To secure an API endpoint, making it accessible to registered users only, you can replace the rest_framework.permissions.allowAny value in the default_permissions section of your settings.py to

- [ ] rest_framework.permissions.IsAdminUser
- [x] rest_framework.permissions.IsAuthenticated
- [ ] rest_framework.permissions.IsAuthorized
- [ ] rest_framework.permissions.IsRegistered

#### Q40. Which command would you use to apply a migration?

- [ ] makemigration
- [ ] update_db
- [ ] applymigration
- [x] migrate

#### Q41. Which type of class allows QuerySets and model instances to be converted to native Python data types for use in APIs?

- [ ] objectwriters
- [x] serializers
- [ ] picklers
- [ ] viewsets

#### Q42. How should the code end?

```
{ percentage if spark >= 50 percentage }
Lots of spark
{percentage elif spark == 42 percentage}
```

- [ ] { percentage else percentage}
- [x] {percentage endif percentage}
- [ ] Nothing needed
- [ ] {percentage end percentage}

#### Q43 Which code block will create a serializer?

```
from rest_framework import serializers
from .models import Planet
```

- [x]

```
class PlanetSerializer(serializers.ModelSerializer):
class Meta:
model=Planet
fields=('name','position', 'mass', 'rings')
```

- [ ]

```
from rest_framework import serializers
from .models import Planet
class PlanetSerializer():
class Meta:
fields=('name','position', 'mass', 'rings')
model=Planet
```

- [ ]

```
from django.db import serializers
from .models import Planet
class PlanetSerializer(serializers.ModelSerializer):
fields=('name','position', 'mass', 'rings')
model=Sandwich
```

- [ ]

```
from django.db import serializers
from .models import Planet
class PlanetSerializer(serializers.ModelSerializer):
class Meta:
fields=('name')
model=Planet
```

#### Q44 Which class allows you to automatically create a Serializer class with fields and validators that correspond to your model's fields?

- [x] ModelSerializer
- [ ] Model
- [ ] DataSerializer
- [ ] ModelToSerializer

#### Q45 Which command to access the built-in admin tool for the first time?

- [ ] django-admin setup
- [ ] django-admin runserver
- [ ] python manage.py createuser
- [x] python manage.py createsuperuser

#### Q46. Virtual environments are for managing dependencies. Which granularity works best?

- [x] you should set up a new virtualenv for each Django project
- [ ] They should not be used
- [ ] Use the same venv for all your Django work
- [ ] Use a new venv for each Django app

#### Q47. What executes various Django commands such as running a webserver or creating an app?

- [ ] migrate.py
- [ ] wsgi.py
- [x] manage.py
- [ ] runserver

#### Q48. What do Django best practice suggest should be "fat"?

- [x] models
- [ ] controllers
- [ ] programmers
- [ ] clients

#### Q49. Which is not part of Django's design philosophy?

- [ ] Loose Coupling
- [ ] Less Code
- [ ] Fast Development
- [x] Implicit over explicit

#### Q50. What is the result of this template code?

```
{{"live long and prosper"|truncate:3}}
```

- [x] live long and ...
- [ ] live long and
- [ ] a compilation error
- [ ] liv

#### Q51. When does this code load data into memory?

```
1 sandwiches = Sandwich.objects.filter(is_vegan=True)
2 for sandwich in sandwiches:
3   print(sandwich.name + " - " + sandwich.spice_level)
```

- [ ] line 1
- [x] It depends on how many results return by query.
- [ ] It depends on cache.
- [ ] line 2

#### Q52. You are building a web application using a React front end and a Django back end. For what will you need to provision?\*\*

- [ ] an NGINX web server
- [ ] a NoSQL database
- [ ] a larger hard drive
- [ ] CORS middleware

#### Q53. To expose an existing model via an API endpoint, what do you need to implement?\*\*

- [ ] an HTTP request
- [ ] a JSON object
- [ ] a query
- [x] a serializer

#### Q54. How would you stop Django from performing database table creation or deletion operations via migrations for a particular model?\*\*

- [ ] Run the `migrate` command with `--exclude=[model_name]`.
- [ ] Move the model definition from `models.py` into its own file.
- [x] Set `managed=False` inside the model.
- [ ] Don't run the `migrate` command.

#### Q55. what method can you use to check if form data has changed when using a form instance?

- [x] has_changed()
- [ ] its_changed()
- [ ] has_updated()
- [ ] None of This

#### Q56. What is WSGI?

- [x] a server
- [ ] an interface specification
- [ ] a Python module
- [ ] a framework

#### Q57. Which generic view should be used for displaying the tittles of all Django Reinhardt's songs?

- [ ] DetailView
- [ ] TittleView
- [ ] SongView
- [x] ListView

#### Q58. Which statement is most acurate, regarding using the default SQLite database on your local/development machine but Postgres in production

- [x] There's less chance of introducing bugs since SQLite already works out the box
- [ ] It's fine, you just need to keep both instances synchronized
- [ ] It's a bad idea and could lead to issues down the road
- [ ] It's the most efficient way to build a project

#### Q59. Why might you want to write a custom model Manager?

- [ ] to perform database queries
- [ ] to set up a database for testing
- [x] to modify the initial QuerySet that the Manager returns
- [ ] to filter the results that a database query returns

#### Q60. In Django, what are used to customize the data that is sent to the templates?

- [ ] models
- [x] views
- [ ] forms
- [ ] serializers

#### Q61. To complete the conditional, what should this block of code end with?

```shell
% if sparles >= 50 %
  Lots of sparkles!
% elif sparkles == 42 %
  The answer to life, the universe, and everything!
```

- [x] `% endif %`
- [ ] Nothing else is needed.
- [ ] `% end%`
- [ ] `% else %`

#### Q62. You have inherited a Django project and need to get it running locally. It comes with a requirements.txt file containing all its dependencies. Which command should you use?

- [ ] python install -r requirements.txt
- [ ] django-admin startproject requirements.txt
- [ ] pip install Django
- [x] pip install -r requirements.txt

#### Q63. When should you employ the POST method over the GET method for submitting data from a form?

- [x] when the data in the form may be sensitive
- [ ] when you want the data to be cached
- [ ] when you want to use your browser to help with debugging
- [ ] when efficiency is important

#### Q64. What is a callable that takes a value and raises an error if the value fails to meet some criteria?

- [ ] mediator
- [x] validator
- [ ] regular expression
- [ ] deodorizer

#### Q65. You are uploading a file to Django from a form and you want to save the received file as a field on a model object. You can simply assign the file object from**\_to a field of type\_\_**in the model.

- [ ] request.META; FileField
- [ ] request.FILES; BLOBField
- [x] request.FILES; FileField
- [ ] request.META.Files; CLOBField

#### Q66. What python module might be used to store the current state of a Django model in a file?

- [x] pickle
- [ ] struct
- [ ] marshal
- [ ] serialize

#### Q66. To add a new app to an existing Django project, you must edit the **_ section of the _** file.

- [ ] ALLOWED_HOSTS; settings.py
- [ ] APPS; manage.py
- [x] INSTALLED_APPS; settings.py
- [ ] TEMPLATES; urls.py

#### Q67. Which is not third-party package commonly used for authentication?

- [ ] django-guardian
- [ ] django-rest-auth
- [ ] authtoken
- [x] django-rest-framework-jwt

#### Q68. Which function in the django.urls package can help you avoid hardcoding URLS by generating a URL given the name of a view?

- [ ] get_script_prefix()
- [ ] redirect()
- [x] reverse()
- [ ] resolve()

#### Q69. Which is Fictional HTTP request method?

- [ ] POST
- [ ] PUT
- [x] PAUSE
- [ ] PATCH
