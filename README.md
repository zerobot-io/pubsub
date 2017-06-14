# pubsub
Prototype Kombu transport for Google pubsub
-------------------------------------------

This is a simple Django prototype project with a Kombu consumer.  
The key piece is the Kombu transport in
[kombu_transport.py](pubsub/kombu_transport.py). There are a few views that
send messages in one way or another. There is also a consumer that pulls those messages.

To install::

    virtualenv -v python3.5 ve
    . ve/bin/activate
    pip install -r requirements.txt

To run the consumer::

    python pubsub/consumer.py

To run the web server::

    ./manage.py runserver

To send a message, browse to any of the following:

    http://localhost:9000/send-message/
    http://localhost:9000/send-message-pools/
    http://localhost:9000/run-task/
