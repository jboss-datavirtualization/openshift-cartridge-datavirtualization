## DataVirtualizaton Cartridge for OpenShift

## Summary
This cartridge provides the RedHat JBoss **_DataVirtualization Platform_** for easy deployment to OpenShift. 

The [DataVirtualization Cartridge](https://github.com/jboss-datavirtualization/openshift-cartridge-datavirtualization) provides the RedHat JBoss **DataVirtualization** components:

  - [Teiid](http://www.jboss.org/teiid/) - Data Virtualization system
  - [Modeshape](http://www.jboss.org/modeshape/) - Content Repository
  - [Dashboard Builder](https://access.redhat.com/site/documentation/en-US/Red_Hat_JBoss_Data_Virtualization/6/html/Administration_and_Configuration_Guide/chap-Dashboard_Builder.html) - interactive dashboard and report creation 

## Cartridge Installation
Create your free OpenShift user account - [instructions here](https://openshift.redhat.com/app/getting_started)

Deploy the cartridge via the [OpenShift Web Console](https://openshift.redhat.com/app/console/applications) .  On the Applications tab, choose 'Add Application...' - then select the 'JBoss Data Virtualization 6' cartridge under the xPaaS section.  Full [installation instructions](https://community.jboss.org/wiki/ProvisionDataVirtualizationOnOpenShift) are provided.
 
Alternately, if you have the OpenShift command line tools installed, you can deploy the DataVirtualization cartridge via command line:

```
rhc app-create <myApp> jboss-dv-6.0.0
```

When the installation completes, you will be presented with a list of generated users and passwords similar to the screencap below.  Make sure you save them!
![installation users](https://github.com/jboss-datavirtualization/openshift-cartridge-datavirtualization/raw/6.0.0/InstallationUsers.png)

## Getting started with Data Virtualization
After the cartridge finishes deployment, enter this address to verify success

* http://[MYAPP]-[MYDOMAIN].rhcloud.com

### Teiid Data Virtualization
A few 'how-to' articles are available to help you get started:
* [Intro to the Data Virtualization Web Interface](https://developer.jboss.org/wiki/IntroToTheDataVirtualizationWebInterfaceOnOpenShift)
* [Provision Data Virtualization on OpenShift and Connect from Teiid Designer](https://community.jboss.org/wiki/ProvisionDataVirtualizationOnOpenShiftAndConnectFromTeiidDesigner)
* [Salesforce as a REST Service using Data Virtualization](https://community.jboss.org/wiki/SalesforceAsARESTServiceUsingDataVirtualization)
* [Any source as an OData feed using Data Virtualization](https://community.jboss.org/wiki/AnySourceAsAnODataFeedUsingDataVirtualization)
* [Add a MySQL database to your OpenShift Data Virtualization instance](https://community.jboss.org/wiki/AddAMySQLDatabaseToYourOpenShiftDataVirtualizationInstance)
* [Utilize the MySQL database on OpenShift Data Virtualization in Designer](https://community.jboss.org/wiki/UtilizeTheMySQLDatabaseOnOpenShiftDataVirtualizationInDesigner)

A teiid user is generated with the installation.  It is granted the user, odata and rest roles.
* user,  {generated password}

Consult the [Teiid Documentation](http://www.jboss.org/teiid/docs) for more information.

### Modeshape Content Repository
You can access Modeshape at

* http://[MYAPP]-[MYDOMAIN].rhcloud.com/modeshape-webdav

* http://[MYAPP]-[MYDOMAIN].rhcloud.com/modeshape-rest

Two modeshape users are generated with the installation
* msuser, {generated password} - (modeshape user)  
* msadmin, {generated password} - (modeshape admin)

Consult the [Modeshape Documentation](http://www.jboss.org/modeshape/) for more information.

### Dashboard Builder
Access the dashboard builder at the following address

* http://[MYAPP]-[MYDOMAIN].rhcloud.com/dashboard

A dashboard admin is generated with the installation.  (The teiid 'user' is allowed dashboard readonly user access)
* dbadmin, {generated password)

Consult the [Dashboard Documentation](https://access.redhat.com/site/documentation/en-US/Red_Hat_JBoss_Data_Virtualization/6/html/Administration_and_Configuration_Guide/chap-Dashboard_Builder_Technology_Preview.html) for more information.


