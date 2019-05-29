# Luuna Data Engineering Challenge

Welcome to Luuna's Data Engineering challenge.


## Important

* If at any point you feel confused or don't know how to do something, we encourage you to search for it on the internet. We do not expect you to know everything, we value your ability to learn new skills.

* Incomplete solutions are still considered.

Any ambiguity is probably intended and meant for you to make design decisions. 

Email any further questions or problems to **data@luuna.mx**.


## Setup

You will need Docker and Docker Compose installed.

In order to run the infrastructure necessary to solve this challenge, simply clone or fork and clone this repository, cd into it's folder and execute the following command: 

```bash
docker-compose up 
```

After a couple of minutes, you will have a MySQL database available at:

```bash
localhost:3306
```
* The user is **root**. 
* The password is **luuna**. 

You have full admin privileges over this database. Feel free to explore.

You will also have a web server available at:

```bash
localhost:3000
```
The purpose of these endpoints is explained in the following section.

## Problem Description

* Luuna employs salespeople.

* Each salesperson has an ID number.

* Each salesperson has a base salary.

* Both of these values are stored inside your MySQL database.

Each salesperson is compensated according to their speed, which is provided by a third party service via a REST API. 

Their daily salary is calculated according to the following formula:

```bash
base_salary + base_salary*(day_average_speed)
```

Average speed for the day is calculated by sampling their speed at 5 second intervals for 5 minutes.

You can get the speed of currently active salesmen by performing an HTTP/GET request to:

```bash
localhost:3000/speed
```
You will receive a JSON object, containing employees and their current speed. If an employee is not included, they are assumed to be inactive and therefore their current speed is 0.

## Goal

 Design and implement a script, system or module to calculate the individual salaries of Luuna's salespeople and produce a report for the finance deparment. It must run daily on a schedule. 


## Restrictions

None. Use whatever tools you feel comfortable with.

Bonus points for using some of the tools we use at Luuna:

* R
* Shiny
* RMarkdown
* Docker
* Docker Swarm
* Cron
* Go
* Node.js
* Python
* Git

## Finished?

Run

```bash
docker-compose down 
```
Email your solution to data@luuna.mx or link us to your repository. 

## Good luck!

