# Object Relation Mapping in Django [![forthebadge](https://forthebadge.com/images/badges/made-with-python.svg)](https://forthebadge.com) <img alt="Django" src="https://img.shields.io/badge/django-%23092E20.svg?&style=for-the-badge&logo=django&logoColor=white"/>

> ### Object Relational Mapping has been showcased in this project

* Foreign Key
* ManytoMany Mapping

> ### Few Set of queries are also run on the database

```
python manage.py shell

from posts.models import Blog
b = Blog(name="Food Blog", tagline="Chaato Ungliyan")
>>> b.save()
>>> Blog.objects.all()
<QuerySet [<Blog: Quickstart>, <Blog: Flask>, <Blog: Food Blog>]>
>>> b = Blog(name="Pets Blog", tagline="My Chotu")
>>> b.save()
>>> Blog.objects.all() 
<QuerySet [<Blog: Quickstart>, <Blog: Flask>, <Blog: Food Blog>, <Blog: Pets Blog>]>
>>> Blog.objects.filter(name="Pets")
<QuerySet []>
>>> Blog.objects.filter(name="Pets Blog") 
<QuerySet [<Blog: Pets Blog>]>
j= Blog.objects.filter(tagline__startswith="Lets")  
>>> j
<QuerySet [<Blog: Quickstart>, <Blog: Flask>]>
>>> j= Blog.objects.filter(tagline__endswith="u")    
>>> j
<QuerySet [<Blog: Pets Blog>]>
>>> j= Blog.objects.get(tagline__endswith="u")    
>>> j
<Blog: Pets Blog>
>>> j.tagline
'My Chotu'
>>> j= Blog.objects.filter(tagline__iexact="My Chotu") 
>>> j
<QuerySet [<Blog: Pets Blog>]>
>>> j= Blog.objects.get(tagline__iexact="My Chotu")
>>> j
<Blog: Pets Blog>
>>> j.tagline
'My Chotu'
>>> j.name
'Pets Blog'
>>> j= Blog.objects.filter(tagline__icontains="Let")
>>> j
<QuerySet [<Blog: Quickstart>, <Blog: Flask>]>
>>> j= Blog.objects.filter(tagline__icontains="LeT")
>>> j
<QuerySet [<Blog: Quickstart>, <Blog: Flask>]>
```

Get the query set file [here](https://github.com/pranavarora1895/make_django_queries/blob/main/queries.txt).

* Follow Me On Instagram at [Pranav Arora](https://www.instagram.com/arorapranav187)
* Lets Get Connected on Linkedin at [Pranav Arora](https://www.linkedin.com/in/pranav-arora-354b71bb/)


### ThankYou!
