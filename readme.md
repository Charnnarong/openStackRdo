###Proof of concept for single node.
----
Just a wrapper for RdoProject. Please refer to https://www.rdoproject.org/install/quickstart/ for more details.

It would be nice if we have something satisfy the following conditions.
1. I want that isolate from my system.
2. I want to have all of that up and running with mininum amount of afford i.e. no more than 'vagrant up' of typing.
3. I should be able to control the final result, thus all configurations must be transparent.  

The project **openStackRdo** is simply answer all those question. 
So let's '**vagrant up**' and claim our coffee time back automatically. Enjoy :)


####Requirement
----
- Vagrant ( with vagrant-vbguest installed )
- Virtualbox ( If any one argue. Yes, you are right. The choice on your mind is definitely a better alternative)
  

####Dashboard
----
user     = admin
password = password

for more confiurations. Please refer to 
openStackRdo\resources\ansible\roles\rdo-all-in-one\files\packstack-answers.cfg

