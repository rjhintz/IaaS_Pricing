#Notes
##Tech
Python 3.4
Atom
[Requests -HTTP library for Python](http://docs.python-requests.org/en/latest/user/quickstart/)
[BeautifulSoup - a Python library for pulling data out of HTML and XML files](http://www.crummy.com/software/BeautifulSoup/bs4/doc/)
[unittest](https://docs.python.org/3/library/unittest.html)

Didn't know about [Python testing tools compendium](https://wiki.python.org/moin/PythonTestingToolsTaxonomy)

##Objective
Get current pricing from vendors and display comparatively, vendor to vendor, and by time.

Vendors considered:
* AWS
* GCE
* Azure
* Softlayer
* Centurylink

###20150802
Use *Test-Driven Development with Python*, Harry Percivasl, O'Reilly, 2014, as a guide to do the development using functional and unit tests.

####Setup
Create `development/scrape` directory

Make Atom default editor for Git Commit

Create `FuncScrape.py` for functional tests code

Python ignores for `.gitignore`
```
echo "__pycache__" >> .gitignore
echo "*.pyc" >> .gitignore
```

####Write user story
```
#Get IaaS pricing from vendor web sites. 
#Don't look like a robot.
User agent string to identify as a human, not a bot.

From http://www.useragentstring.com/
```
Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/45.0.2454.15 Safari/537.36
```
#Go to AWS pricing site

#Get pricing for current generation EC2 instances

#Store results in a useful format

#Compare results, vendor to vendor and over time

###20150803
See Stack Overflow [get ec2 pricing programmatically?](http://stackoverflow.com/questions/7334035/get-ec2-pricing-programmatically)
```
curl http://aws.amazon.com/ec2/pricing/ 2>/dev/null | grep 'model:' | sed -e "s/.*'\(.*\)'.*/http:\\1/"
```

See also [Netflix tools](https://github.com/Netflix/ice)


