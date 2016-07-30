Redis Triggers
=====================


**tiggers** an execution a function on expiry of a key in redis.

----------


Documents
-------------

### Installation
Two ways to install using pip
```
	pip install redis_triggers
```
Build the repo manually 
```
	git clone https://github.com/abhishek246/redis_triggers.git
	cd redis_triggers
	python setup.py 
```


### Use Cases

How to use: 

PreConfiguration before using this package:
please execute this command in your shell

```
redis-cli config set notify-keyspace-events Kx
```

You should demonize this process using supervisord 
for testing purpose we can run this in the python prompt
```
	from redis_triggers.listener import Listener
	import redis
	from your_file import Yourclass

	#Add you namespace settings, password here while creating the redis object
	redis_client = redis.Redis()
    client = Listener(redis_client, YourClass())
    client.start()     
```


Execute python example.py 
