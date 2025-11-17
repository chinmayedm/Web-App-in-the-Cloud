
# Set Up a Web App in the Cloud 
![web app](https://github.com/chinmayedm/Web-App-in-the-Cloud/blob/main/Screenshot%202025-11-17%20at%2014.35.35.png?raw=true)
# What is VSCode and Why Is It Useful?

I used VSCode in today’s project to edit and manage the Java web app’s files. 
I installed the Remote - SSH extension, connected to the EC2 instance, and used VSCode’s file explorer to explore, edit, and update the project’s index.jsp and other files.

# How I'm Using VSCode in This Project

I used VSCode in today’s project to edit and manage the Java web app’s files. 
I installed the Remote - SSH extension, connected to the EC2 instance, and used VSCode’s file explorer to explore, edit, and update the project’s index.jsp and other files.

# One Thing I Didn’t Expect

One thing I didn’t expect in this project was the need to troubleshoot setup steps, like configuring Java, Maven, and SSH connections. 
It took time to ensure everything worked properly before I could start editing and building the web app.

# Launching an EC2 Instance

I started this project by launching an EC2 instance because it allows us to create a customizable virtual machine tailored to the project's needs, including CPU, memory, storage, and networking capacity, ensuring a flexible and scalable environment.

# Enabling SSH

SSH is a protocol that ensures only authorized users can access a remote server. I enabled SSH so that when connecting to my EC2 instance, it verifies my private key matches the server’s public key, establishing a secure, encrypted connection.

# Key Pairs

A key pair is a set of cryptographic keys used for secure access to an EC2 instance. We use RSA, a trusted algorithm known for its strength and security. After generating the key pair, AWS downloaded a .pem file to my local computer. This file is widely used for cryptographic keys and is compatible with EC2 and many servers.

# Setting Up VSCode

VSCode is a free, open-source code editor. It provides features like syntax highlighting, debugging tools, extensions, and an integrated terminal, making it ideal for software development, including working with remote servers like EC2.

I installed VSCode to write and edit code efficiently, set up a terminal for connecting to my EC2 instance, and manage my project files. It also allows me to use extensions that improve functionality and streamline development.
![VS code](https://github.com/chinmayedm/Web-App-in-the-Cloud/blob/main/Screenshot%202025-11-17%20at%2014.36.05.png?raw=true)

# My First Terminal Commands

The terminal is a text-based interface that allows users to interact with the operating system through commands.

The first command I ran was:

``` command line
cd ~/Desktop/DevOps
```

This navigated me to the project directory.

I then updated my private key’s permissions using:

``` command line
chmod 400 chinmaye-keypair.pem
```

This ensures the private key is readable only by me, which is required for secure SSH access.
![terminal](https://github.com/chinmayedm/Web-App-in-the-Cloud/blob/main/Screenshot%202025-11-17%20at%2014.36.28.png?raw=true)

# SSH Connection to EC2

To connect to my EC2 instance, I ran:

``` command line
ssh -i /path/to/keypair.pem ec2-user@<EC2-public-DNS>
```


This provides secure access using my .pem file with correct permissions (400).

The connection requires the EC2 instance’s IPv4 DNS, which is the public address used to find and connect to the server.
![SSH connection](https://github.com/chinmayedm/Web-App-in-the-Cloud/blob/main/Screenshot%202025-11-17%20at%2014.36.56.png?raw=true)

# Maven & Java

Apache Maven is a tool for building and managing Java projects. It automates the build process, manages dependencies, and provides a standardized structure.

Java is required to run Maven and build the web application. Amazon Corretto 8 is the Java version used in this project.

# Creating the Application

I generated a Java web app using the command:

```
mvn archetype:generate \
-DgroupId=com.nextwork.app \
-DartifactId=nextwork-web-project \
-DarchetypeArtifactId=maven-archetype-webapp \
-DinteractiveMode=false
```
![application](https://github.com/chinmayedm/Web-App-in-the-Cloud/blob/main/Screenshot%202025-11-17%20at%2014.37.19.png?raw=true)
![web directory](https://github.com/chinmayedm/Web-App-in-the-Cloud/blob/main/Screenshot%202025-11-17%20at%2014.37.38.png?raw=true)

# Using Remote - SSH

I installed the Remote - SSH extension to connect to the EC2 instance and manage files directly from VSCode.

An SSH Host is the server you are connecting to. The required configuration details include the EC2 instance IP, the private key path (e.g., chinmaye-keypair.pem), and the username (ec2-user).
![web app](https://github.com/chinmayedm/Web-App-in-the-Cloud/blob/main/Screenshot%202025-11-17%20at%2014.35.35.png?raw=true)

# Exploring the Project Structure

Using VSCode’s file explorer, I could see the project’s directory structure, including folders like src, pom.xml, and other essential files.

Two key folders created by Maven are:

src — contains the Java source code (src/main/java)

webapp — contains web-related resources like HTML, JSP, and configuration files

# Editing index.jsp

index.jsp is the default landing page of the web application. It displays dynamic content and can contain Java code along with HTML.

I edited index.jsp using VSCode by making changes to the HTML and Java code inside the file and saving it. This updated the content and functionality displayed on the landing page of the web app.

