
1.

Write a regex to extract all the numbers with orange color background
	from the below text in italics (Output should be a list).

{"orders":[{"id":1},{"id":2},{"id":3},{"id":4},{"id":5},{"id":6},{"id":7},{"id":8},{"id":9},{"id":10},
{"id":11},{"id":648},{"id":649},{"id":650},{"id":651},{"id":652},{"id":653}],"errors":[{"code"
:3,"message":"[PHP Warning #2] count(): Parameter must be an array or an
object that implements Countable (153)"}]}


answer:

import re

text = '{"orders":[{"id":1},{"id":2},{"id":3},{"id":4},{"id":5},{"id":6},{"id":7},{"id":8},{"id":9},{"id":10},{"id":11},{"id":648},{"id":649},{"id":650},{"id":651},{"id":652},{"id":653}],"errors":[{"code":3,"message":"[PHP Warning #2] count(): Parameter must be an array or an object that implements Countable (153)"}]}'

numbers = re.findall(r'"id":(\d+)', text)
print(numbers)




3

 A. Write and share a small note about your choice of system to schedule periodic tasks (such as downloading a list of ISINs every 24 hours). Why did
     you choose it? Is it reliable enough; Or will it scale? If not, what are the problems with it? And, what else would you recommend to fix this problem at
     scale in production?
	
	a. Scheduling tasks for the Later is an essential tool for developer. 
	b. While much of the programming we create aims to respond to explicit triggers or user events, background processes performed at regular intervals.
	c. We use a scheduler to execute a defined method or task on specific time interval on every day,week,month,years.
	example:celery,Q

	Is it reliable
	   a.managing workload
	   b.By scheduling activities, you can prioritize your tasks and allocate your time accordingly. 
	   c.Scheduling the task can help you to focus on one task at a time, which can increase your productivity.

 	 problems.
	   a.scaling multiple times per min or hour for accessing database(mongodb) with unindexed fields.database will be locked up
	   b.If we duplicate data from your database in your task arguments, it can go stale in the queue before the task executes.
	
	

  B. In what circumstances would you use Flask instead of Django and vice-versa?

	when to use Flask...
		a.when we want to develop an applicatioon from scratch
		b.for developing static websites,restful web services
		c.when we want  to use ingenious SQL queries.

	when to use Django...
		a.built API,dymanic social networking website.
		b.built enterprise level apps. As it contain inbuilt modules and libraries
		c.support ORM(object relational mapping) and planning to integrate machine learning in future.

		