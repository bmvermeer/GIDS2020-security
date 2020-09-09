# GIDS 2020 Security Workshop

This workshop is specifically created for the GIDS 2020 
GIDS.JAVA Live Workshop (11 September 2020)

GIDS.Java Live Workshop (11 September) features a 3.5 hours live workshop led by 
- Steve Poole (DevOps Practitioner and Developer Advocate, IBM)
- Brian Vermeer (Developer Advocate at Snyk)

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

# Introduction

This workshop contains a demo Java application build on with Spring boot and Thymeleaf.
It contains a number of security issues in the source code.
During this workshop, you will locate, exploit and fix the vulnerabilities in this application.

The vulnerabilities covered in this workshop:
- XML External entity injection (XXE)
- SQL injection
- Cross-site scripting (XSS)
- Encryption
- 

## Installation 

- Check out the repository [bmvermeer/java-security-code-workshop](https://github.com/bmvermeer/java-security-code-workshop)
- go to the `java-code-workshop` folder
- Run `mvn clean package`
- Run `mvn spring-boot:run`

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
