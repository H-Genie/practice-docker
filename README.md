fronted>
docker build -t frontend-img .
docker run --name frontend-con -v ${pwd}:/home/node/app -p 8080:8080 frontend-img

database>
docker build -t database-img.
docker run --name database-con -p 3306:3306 database-img

backend>
docker build -t backend-img.
docker run --name backend-con -p 5000:5000 backend-img

root>
docker-compose up
