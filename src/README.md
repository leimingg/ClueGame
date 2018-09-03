# Getting Started

## Java
### Get Apache Ant
If you don't already have Apache Ant, you can find a download for 
Apache Ant at <http://ant.apache.org/bindownload.cgi>.

On Mac OSX you should be able to run:

    brew install ant

Note: You may have to try the install a couple times and install XCode extras.

On linux, the usual package management methods should work,
whether its yum, dnf, or apt installations.

On Windows, there is the Apache manual at <http://ant.apache.org/manual/install.html#installing> and an unofficial tutorial at <https://www.mkyong.com/ant/how-to-install-apache-ant-on-windows/>

### Build With Apache Ant
From a console, goto the java directory and run the following:

    ant

If you want to clean the project files, run:

    ant clean

### Run The Code From A Jar
If you want to run the server or client from the jar:

    java -cp dist/clueless.jar ServerRun
    java -cp dist/clueless.jar ClientRun

### Run Code With Arguments
You can use argument to control the network config. The synopsis:

    java -cp dist/clueless.jar ServerRun [--port PORT] [--backlog BACKLOG] [--address IP_ADDRESS]

Example usage assuming you want to listen on 192.168.1.5:6543:

    java -cp dist/clueless.jar ServerRun --port 6543 --address 192.168.1.5

No arguments will default to backlog of 6, port of 2323, and address of 0.0.0.0 (any address).

