# Project Description
                          ----------Participaion at HackTheHill-2 with amazing teamates known as the IKEA BOYZ.----------

**PREVIEW**

![Home](/home.png)
![Sending Page](/Send.png)
![Log In Page](/Log.png)

**Inspiration:**
  People deserve the privacy that is not provided to them often. In such cases, it's often easy to forget how much vulnerable these protocols make us, and how they are often abused. We wanted to learn the whole network aspect of software engineering, which was new to all of us, to understand how stuff around us works, and how we can make it safe for our community.

**What it does:**

  That's the meat of it. We privately send files between two or more devices. We create a private connection network between devices to act as a decentralized file sharing platform. Each device acts both as a client and a server, and each file is shared as a combination of smaller decentralized chunks. This protocol makes the sharing resilient against data loss, disconnections, and outages; and therefore, greatly reduces redundant downloads. It also has a frontend for the user to interact with.

**How we built it:**
  We implemented our TCP/IP communication layer using python. Then wrapping it with the intuitive NextJS UI. On node instantiation its location gets advertised to all the listening connections on the local network. If a node wants to share data it first tokenizes it by generating header information like file name, size and type, then the contents of the file are divided in 512 byte blocks, each block is hashed and inserted in an indexed block object. The resulting file with extension .hackthehill gets hashed to create the original file unique identifier, which can be shared with others to setup a communication channel.   Whenever a node needs to retrieve some information it asks its network peers for the file unique identifier, if it's present the sender node transfers the .hackthehill file to the receiver, which makes use of it to retrieve the the blocks necessary to assemble the resulting downloadable file.

**Challenges we ran into:**
  Being a new technology for us, it was a challenge to learn the basic fundamentals of networking and implement them right away. A lot of concepts that we took for granted, like firewall protection and communication through ip addresses, they challenged our interpretation about the networking world. They were also major roadblocks that motivated us to keep upgrading our project to incorporate changes. One major roadblock we ran into was the matter of two nodes communicating and sending the .hackthehill file object. It took a deeper understanding of IPs and networks to get the insight into uOttawa's mesh wifi system, which way to connect with one another, and how to use multi-threading processing to get data in real time.

**Accomplishments that we're proud of:**
  It took a mastery of Git for us to incorporate our different approaches to the same problem. And the record time that it took for us to understand and implement networking protocols surprised even us. We had to scratch a lot of first attempt, we had to approach the problem from 100 different views and perspectives.

**What we learned:**
  We learnt about how networking actually works, and how communication happens over deep layers of networks around the world.

**What's next for Ciena P2P File Sharing Challenge:**
Inter-Network Communication and more testing with increasing number of nodes.

Built With:
bash
nextjs
python

# hack-the-hill-p2p

pip install -r requirements.txt

## Central server
python central_sockets.py
