#Real2Time
Real2Time is a new approach of how we use Big Data in Real Time. Our target is to simplify this.

### How we do it?
We use Storm as engine. Storm is a beautiful project of apache (http://storm.apache.org/), but the use of Storm is very complex and requires a great effort, so we decided to design and code a new way.

### What advantages do you have?
You only have to log in the editor, use and connect all of things that you need. Save and run!

### And that's it?
For the time being,   we have only three spouts and three bolts, but we hope code more and more spouts/bolts and the community too!

### Is it really so easy?
Well… is a little bit more complicated, but in fact, this is our vision.

## Tech
A picture is worth a thousand words:
![screenshot]

### Parts
##### 1. Web
First of all, you need to sign up for create a new user. Then you can login with this user and show your own topologies.
![login]
Maybe you want edit one topology, so use these beautiful icons for this purpose.
![listTopologies]
In the editor, drag and drop the widgets in sublist. A new box appears and you can link one box to other, if this boxes are compatible. You really want to connect the price of a stock with a geolocation? If you want, I tell you how (you need search geolocation with other spout).
![editor]
And then.. Run and profit!
![comp]
In backend, a json send to server.py.

View stats of storm topology without login? No more. Users can only see their own topologies and they can disable, rebalance or kill. We are working in a better representation of stats
![stats]

##### 2. Server.py
server.py is a server tcp write in python. It receives a json that represent a topology designed in the web. Then use a template for write this topology, compiles and submit to your Storm Cluster.

##### 3. Docker
We integrate both parts in Docker technology (https://www.docker.com/), and deploying became into a easy game. Web and Server.py run in separate containers 

## Why we decided make Real2Time open source?
The ecosystem of big data is marvelous, but at the same time too complicated. Until now everything revolved around batch processing (Hadoop,Spark..) but three years ago, in a logical movement, Storm born.
If you look, a lot of use cases needs real time and Real2Time is a small approximation about what Big Data should be.
We would be grateful if you want share yours Spouts or Bolts. Our intention is that we can provide feedback to each other and this is our modest proposal.

#Contact
<info@real2time.com>
#Contributors
Adrian Portabales Goberna <adrian.portabales@real2time.com>

Jose Manuel Santorum Bello <jm.santorum@real2time.com>

[screenshot]:http://i.imgur.com/zobI0Ur.png
[login]:http://i.imgur.com/RbygLCe.png
[signup]:http://i.imgur.com/ODxcXp0.png
[comp]:http://i.imgur.com/NJqdY5J.png
