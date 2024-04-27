# Creating a GCP Client Tool in Python

## Why

I often find myself reuuing the same bits of code when working with GCP. It is very important to avoid creating multiple development trees of the same classes. I have done this before for large projects. It will lead to a very difficult to maintain stack of tools that will spaghettify over time. 


## Creating the submodule

### Create an empty directory 

```bash
mkdir gcpuptils
```

### Add the following code to a gcpclient.py file
 
[github link to latest file](https://github.com/justin-napolitano/gcputils/blob/main/gcpclient.py) is the link to the `gcpclient.py` file on GitHub.


###  Initialize like usual 

1. Run ```git init && git add . && git commit -m 'init'```
2. run ```gh repo create``` and follow the prompts
3. run ``` git push``` and follow the prompts



## Importing into your project

In my example i created a repo at ```https://github.com/justin-napolitano/gcputils.git```

to importrun ``` git submodule add -b main https://github.com/justin-napolitano/gcputils.git``` to import the latest repo into your current project. 

The benefit of doing this is that the code can be reused across every project without having to worry about broken development tress.  



