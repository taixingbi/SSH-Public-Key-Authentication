
## test ec2 with nginx
```bash
sudo service nginx start 
```  

```bash
sudo service nginx stop 
```

## django with docker on ec2

#### start docker 
```bash
sudo systemctl status docker
```

```bash
sudo docker info
```

https://www.digitalocean.com/community/tutorials/how-to-install-and-use-docker-on-ubuntu-18-04

#### djnago docker
```bash
sudo docker-compose run web django-admin startproject composeexample .  
```

```bash
sudo systemctl stop docker
```

```bash
sudo systemctl restart docker 
```

```bash 
sudo chown -R $USER:$USER .     
```

```bash
sudo docker-compose up   
```

https://docs.docker.com/compose/django/  

##### more docker 
```bash 
sudo docker rm -vf $(sudo docker ps -a -q)
```

```bash 
sudo docker rmi -f $(sudo docker images -a -q)
```


## deploy django with pipenv on AWS
https://www.digitalocean.com/community/tutorials/how-to-install-the-django-web-framework-on-ubuntu-18-04

```bash 
sudo chmod -R 777 django
```
```bash 
mkdir media
```
## Running the Project Locally

Install the requirements:

```bash
pipenv install -r requirements.txt
```

Apply the migrations:


```bash
python manage.py makemigrations
```

```bash
python manage.py migrate
```

Finally, run the development server:

```bash
python manage.py runserver 
```

```bash
pip freeze  > requirements.txt
```

```bash
pip install -r requirements.txt
```

```bash
source pipenv/bin/activate
```

```bash
python manage.py runserver 0.0.0.0:8000          
python manage.py runserver 0.0.0.0:8000 --noreload        
```

```bash
deactivate
```

```bash
python manage.py createsuperuser
```
### ec2 ip
```bash
3.226.255.245:8000/api/test/       
3.226.255.245:8000/api/boto/      
3.226.255.245:8000/api/depression/      
```

### load cnn model and audio
```bash
http://0.0.0.0:8000/api/boto/
```
then stop and run again 
```bash
python manage.py runserver 0.0.0.0:8000          
```


### issue
ERROR: Could not find a version that satisfies the requirement python-magic-bin==0.4.14 (from -r requirements.txt (line 32)) (from versions: none)   
ERROR: No matching distribution found for python-magic-bin==0.4.14 (from -r requirements.txt (line 32))  

### issue
docker 8000 is used   
https://github.com/docker/compose/issues/4950
