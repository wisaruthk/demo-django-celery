1.Start Celery
celery -A mysite worker -l INFO



2. Runtask
./manage.py shell 

from demoapp.tasks import add, mul, xsum
res = add.delay(3,4)
res.get()
>>> 7