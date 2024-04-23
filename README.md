# What is amqp?
AMQP stands for Advanced Message Queuing Protocol12. It is an open standard for passing business messages between applications or organizations
# What it means? guest:guest@localhost:5672 , what is the first quest, and what is the second guest, and what is localhost:5672 is for?
The first `guest` is the username, the second `guest` is the password for authentication, `localhost` is the hostname where the AMQP broker (like RabbitMQ) is running, and `5672` is the port on which the broker is listening
![image](https://github.com/g0lgi/tutorial8subscriber/assets/119854906/749d7124-0cb8-4add-9ca7-da8b6a1d249c)
My queued message peaked at 15, and this queue happens because messages are being published faster than they can be consumed. 
![Screenshot (117)](https://github.com/g0lgi/tutorial8subscriber/assets/119854906/0dc74bc7-7914-4eaf-b3d0-7e116029e4d9)
I executed `cargo run` 5 times in publisher, but as we can see, the queued messages went down much quicker. This is because when we run multiple subscribers, each one can consume messages from the queue concurrently. So, even if I run the publisher more often, the rate at which messages are removed from the queue increases when I add more subscribers.
