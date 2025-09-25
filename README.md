#GUIDE:-

1. Clone project

2. Run below commands to install docker and docker-compose
	
      	1. cd scripts && sh install-docker.sh			 #To install docker
        2. cd scripts && sh install-docker-compose.sh	 #To install docker-compose
      	3. cd scripts/ssl && sh install.sh

3. To start containers, Run 
	docker-compose up -d

4. To use different php version, uncomment string from below and run `docker-compose up -d` command.


	1. #image: kalpit/ultimatephpdev:7.0    		 #To use php7.0
    	2. #image: kalpit/ultimatephpdev:7.2			 #To use php7.2
    	3. #image: kalpit/ultimatephpdev:7.3.3			 #To use php7.3.3
   	4. #image: kalpit/ultimatephpdev:7.4			 #To use php7.4
    	5. #image: "kalpit/addweb:5.6"			 	 #To use php5.6
    	6. #image: bhardwaj2803/ultimatephpdev:8.0_latest 	 #To use php8.0
   	7. #image: addwebsolution/php:8.4			 #To use php8.4
    	8. #image: addwebsolution/php:8.3			 #To use php8.3
    	9. #image: addwebsolution/php:8.2			 #To use php8.2
    	10. #image: addwebsolution/php:8.0			 #To use php8.0
    	11. image: addwebsolution/php:8.1			 #To use php8.1

5. After starting containers, bash into code container with `infonew.sh` script and run below commands,
	
      	1. cd /root/.composer && composer install
      	2. cd /root/.composer && php installer.phar
