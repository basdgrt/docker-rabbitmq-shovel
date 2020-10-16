## Docker RabbitMQ Shovel

A RabbitMQ Dockerfile with the `rabbitmq_shovel` and `rabbitmq_shovel_management` plugins enabled.

## How to use this image

RabbitMQ stores data based on what it calls the "Node Name", which defaults to the hostname. For usage in Docker we should specify `-h`/`--hostname` 
explicitly so that we don't get a random hostname and can keep track of our data:

`docker run --name rabbitmq-shovel --rm -d -it --hostname my-rabbit -p 15672:15672 -p 5672:5672 bdg91/rabbitmq-shovel:latest`

After startup the RabbitMQ management interface will be available at: `http://localhost:15672`
