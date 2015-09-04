# swu mirrors to docker

## How to use it

1. Make sure you are in current directory now!
2. Run ```sudo docker build -t swu-mysql .``` to build a image
3. Run ```sudo docker run -p 3306:3306 --name my-mysql -d swu-mysql ``` to make your container up!
4. Now you can work with the port 3306 at your server.

## Tips

1. There is your configure file in ```config/mysql.cnf``` ,you can change it before build image.
2. About how to link to other application, please use google or baidu to find answer.