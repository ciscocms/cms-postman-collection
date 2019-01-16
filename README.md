# Postman Collection for Cisco Meeting Server API

Two **.json** files to be imported into Postman, one **Collection** and one sample **Environment** file, containing all the variables used in the Collection.

The requests currently do not contain all possible attributes/parameters and may have an unexpected subset of them checked.
Always verify to only submit request parameters you need / want. Set the correct values for these and uncheck anything else present and checked.

## Installing the files

Latest, stand-alone Postman app is strongly recommended - download it from [Postman's official website](https://www.getpostman.com/postman)

If you cannot or prefer not to install Postman, you can consider using [the portable build](https://github.com/portapps/postman-portable/releases).

Once in the app:
1. hit Import, then drag & drop each of the two **.json** files in this project.
2. Select Collections tab (should be next to your History tab on the left) and open **CMS API collection**
3. From the environments drop-down select **CMS sample environment** (upper right corner)
4. Edit the environment to match your settings (see next section)

## Managing environments

In Postman you can have one environment per CMS server you are connecting to. 
Depending on your needs, one environment per cluster may be enough, although system specific queries will 
not show up for each server.


* The cogwheel icon next to the environments drop-down will show a list of environments.
* You can duplicate the "CMS sample environment", or you can edit that one.
* Clicking on the name of an environment will allow you to edit the environment variables
* **mmpHost** is the IP/FQDN of your CMS _with the port included_
  * Ex: _cms1.dcloud.cisco.com:445_
* **mmpUser** and **mmpPass** are credentials for an API user that can access your CMS server's API
* other variables do not need to be edited here, although of course can be.
* you can set _any_ environment variable, by highlighting any text and right clicking on it. Then Select from the menu: **Set: [environment name]** >> and the variable you want to set
  * A good example is highlighting node IDs from results. Only highlight the string between the quotation marks, do not include quotation marks!

## Updating the files

You can safely re-import the collection and choose to replace your existing collection. I don't expect there would be 
much use to keep multiple copies of the collection, unless you intend to contribute to this repository.

The environment is likely not worthy to re-import, as all API variables should be already added to it.
Nevertheless, since only the CMS server name and credentials really need to persist, you are safe to re-import and 
clone again for your servers, or just add any new variables to your own environments if needed.

By default, Postman will highlight a variable it cannot find (not empty value, but missing) in a different color, 
so it should be straight forward to identify it if needed.

## Other notes

The Chrome based Postman app does not support inherited authentication used here, so I would strongly recommend 
using the stand-alone Postman, most recent version.

In the stand-alone version you can disable certificate verification in the settings. You will need this unless you 
connect to a CMS with FQDN and a valid certificate trusted by Postman (and your system). 

The environment can be replicated for each CMS cluster (or even node) you want to configure.

The folder structure and order of requests are following the CMS API guide.

**Be aware, that request parameters are not yet complete and/or always correct. Always check in the latest API guide.**

## API reference guides, examples, labs 

* [CMS Programming Guides](https://www.cisco.com/c/en/us/support/conferencing/meeting-server/products-programming-reference-guides-list.html)
* [Devnet CMS section](https://developer.cisco.com/site/cisco-meeting-server/#)
* [Devnet Learning Labs for CMS](https://learninglabs.cisco.com/labs/tags/Cisco+Meeting+Server/page/1)

## Credits

This collection was originally created by @flynnibus for CMS 2.2.

Reorganized, cleaned up, expanded with more recent API changes, documented and published by @zoltan-k. 
