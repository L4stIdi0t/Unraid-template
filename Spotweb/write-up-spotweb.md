Requirements:
Usenet server
MySQL Server

Setting up MySQL
1.a
Choose which one you want, mysql, mariadb, etc. Personally I am using linuxserver/mariadb as it is easy to use and setup so I'll give an explanation for that.

1.b
With the enviroment variable MYSQL_ROOT_PASSWORD you enter a root password for your root user for the server. (or follow the template and it is the third key)

1.c
To make it easier to manage your MySQL you are gonna want an admin interface like adminer or phpmyadmin. I use adminer.

1.d
Login to adminer(or your preferred interface). Server is the ip:port of the server, for example 127.0.0.1:3306. Username is probably gonna be root. Password which you have set in 1.b and the database can be left empty for now.

1.e
Once logged in you click "Create Database" and enter a database name(it doesn't really matter) and hit save.

1.f
On the new page you go to privileges and hit create user. Enter a username and password, it does not really matter what you enter, standard practices apply.
You can check All privileges to easily setup the permissions or you can specify it what you want(and know what you are doing).

Setting up SpotWeb
2.a
Visit the webUI and login with the default login User: admin Pass: spotweb

2.b
Go to Settings(config) > Newsservers and enter the newsserver data from your newsserver provider and hit save

2.c 
Wait until the cronjob runs(it runs once an hour)

Adding another account with API
3.a
Go to the main page webUI and click add user (top right corner dropdown menu)

3.b
Fillout the data and hit add

3.c
Once again go to the main page webUI and click this time logout and login to the just created user

3.d
Go to the change user option (top right corner dropdown menu) and grab your API key.

For different setups send me a message with how you want it and I'll help as much as I can but I think that this will cover the majority of the users.
