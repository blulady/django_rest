# Django_rest
An API created with the Django Rest Framework<br><br>

Here I have followed the tutorial from https://www.django-rest-framework.org/ to learn how to create an API. I learned how to make `Serializers`, define their fields by using Django Rest Framework's `Serializers` class `HyperlinkedModelSerializer`, to represent relationships using a url instead of a primary key, and Meta Class (this was my introduction to the Meta Class and type).The tutorial guided me in naming the URL patterns. <br>
I made use of Django's class based views and Django Rest Framework decorators to include the `Serializers` I made and DRF's `Permissions` to handle authentication. I use the DRF's `Viewsets` to provide CRUD procedures. <br>
I created a permissions.py file to custom define object level permissions in the class `IsOwnerOrReadOnly` which we import into views to restrict updating to only authenticated users and create another user class for looking at snippets without accessing them. We build the `IsOwnerOrReadOnly` from DRF's `BasePermission` class from `Permissions`. <br>
I also makee use of the `ReadOnlyModelViewSet` class from Django Rest Framework's viewsets to create the read only views. Then multiple views are created from each ViewSet class by binding the HTTP methods to the action for each view and registering them with the URL conf utilizing `format_suffix_patterns` to add provide an endpoint for the API.<br>
The tutorial uses the browsable API so you can login and create snippets in the browser.
