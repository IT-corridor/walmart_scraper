## Walmart Product Scraper and Export Project

#### Install python2.7
#### Install project
	git clone <repo>
	apt-get install python-dev python-pip libxml2-dev libxslt1-dev zlib1g-dev libffi-dev libssl-dev
	pip install -r requirements.txt

#### Migrate the database:
	python manage.py makemigrations product
	python manage.py migrate

#### Create a superuser
	python manage.py createsuperuser

#### Run the project:
	cd Product-Scraper/
	nohup python manage.py runserver 0.0.0.0:80 < /dev/null &

#### Edit crontab entry
	* * * * * python /root/paultitov-walmart/cron_task.py
	*/30 * * * * sudo sync & sysctl -w vm.drop_caches=3
	
#### Create an export directory    
    mkdir /home/exports
    
