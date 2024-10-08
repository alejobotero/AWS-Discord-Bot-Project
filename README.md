# Project Summary: Discord Bot on AWS EC2 Instance

The project aimed to design and implement a Discord bot hosted on an AWS EC2 instance, demonstrating cloud infrastructure integration with external services. This project was necessary to explore AWS capabilities in a real-world application and automate Discord server tasks with a custom bot. The bot's purpose was to interact with users in a server, process commands, and provide insights into the server's status.

## Problem Statement and Motivation

Creating the Discord bot prototype involved setting up an EC2 instance, configuring it for secure access, and managing bot deployment. A critical challenge was securely connecting to the EC2 instance via SSH. This task was vital because the instance would serve as the bot's host, and successful connectivity was crucial for implementing and running the bot on the cloud.

## Technical Solution and Design

The project began by creating the necessary AWS infrastructure, including an EC2 instance, S3 bucket, and database. The core technical work centered around configuring the EC2 instance to host the bot. After SSHing into the instance and setting up Python3 and pip, the bot's code was deployed.

The Discord bot was written using Python's `discord.py` and `python-dotenv` libraries, following a modular design. The bot reads commands from users in the Discord server and responds accordingly. The bot was secured using environment variables for sensitive information, like the Discord token, and integrated with AWS for future scalability.

## Challenges Faced and Lessons Learned

One of the most significant challenges was related to connecting to the EC2 instance via SSH. The issue stemmed from being in the wrong directory and from the `.pem` key having incorrect permissions. These problems highlighted the importance of correctly managing access control and understanding AWS file security protocols. In particular, ensuring the `.pem` key was placed in a directory with no files that had multiple permissions for other users was essential to enabling secure access.

Once these challenges were resolved, the bot's deployment on the EC2 instance went smoothly. The code was tested, and the bot successfully responded to commands on the Discord server, such as retrieving server details and interacting with members.

## Reflection and Future Improvements

Looking back, the primary challenge was the complexity of managing secure connections to the EC2 instance. Next time, more focus would be placed on file security and permissions from the start, ensuring that SSH access is seamless. Automating the bot's deployment and management using tools like Docker or AWS Lambda could further improve the process. Additionally, integrating more AWS services like DynamoDB or S3 for storing bot data could enhance th
