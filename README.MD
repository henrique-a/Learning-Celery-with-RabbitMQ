# Learning-Celery-with-RabbitMQ

## Setup RabbitMQ
1. Install RabbitMQ on Ubuntu
```
sudo apt-get install rabbitmq-server
```
2. Enable RabbitMQ
```
sudo systemctl enable rabbitmq-server
```
3. Start RabbitMQ
```
sudo systemctl start rabbitmq-server
```
4. Check if the service is working
```
sudo systemctl status rabbitmq-server
```

## Setup Celery
1. Install Celry
```
pip install celery
```
2. Turn on Celery
```
cd proj && celery -A proj worker -l info
```

## Run the task
```
python manage.py shell
>>> from app1.tasks import add
>>> add.delay(2,2)
```

## Stop RabbitMQ service
```
sudo rabbitmqctl stop
```