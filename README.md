# docker-nginx-gunicorn-Django
Configuration for docker-compose project: docker - nginx - gunicorn - Django.
Requires global packeges: 
- docker-compose: https://docs.docker.com/compose/
- docker: https://docs.docker.com/engine/installation/

To run this repo you will need to build and start the project. In the directory with docker-compose.yml file:
- *$ sudo docker-compose build*
- *$ sudo docker-compose up*

Project should be running on 0.0.0.0:8000 (for this Django example 0.0.0.0:8000/map).

Nginx acts as proxy server of gunicorn. It will also manage all static files required by Django. 
If you want to use your own project don't forget to properly configure Django setup.py file so it matches with nginx config (/config/nginx/.).
Dockerfile uses python3.5 image and installs all requirements from /config/requirements.txt (pip freeze > requirement.txt)

## Config files ##
- nginx: ./config/conf/nginx/Satelite_Tracking.conf
- Docker: ./docker-compose.yml
