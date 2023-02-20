# Timesheet Access  

Communication Contract 

First, connect to the server 

connection_to_server = pika.BlockingConnection(pika.ConnectionParameters(host="localhost"))
travelling_channel = connection_to_server.channel()

Now, publish the routing_key like this line 

travelling_channel.basic_publish(exchange="", routing_key="Timesheet", body="Timesheet arriving")

The message is received in a string format 

channel.basic_consume(queue="message", on_message_callback=callback, auto_ack=True)

An example: 

(Jacob (Full Name: Jacob Williams Anderson) worked 47.8 hours in the whole week) 

![UML sequence diagram ](https://user-images.githubusercontent.com/102319952/220212838-82ea0d9a-9985-48f5-adcc-16f8e3abfb0d.png)
