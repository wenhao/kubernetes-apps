### Run a MySQL client to connect to the server:

kubectl run -it --rm --image=mysql:5.6 --restart=Never mysql-client -- mysql -h mysql -p password
