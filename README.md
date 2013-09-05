# OpenShift DataVirtualizaton Cartridge

## Summary
This cartridge provides the RedHat JBoss **_DataVirtualization Platform_** running in the JBoss application server on OpenShift. 

The [DataVirtualization Cartridge](https://github.com/mdrillin/openshift-cartridge-datavirtualization) provides the RedHat JBoss **DataVirtualization** components.

The following components are included

  - [Teiid](http://www.jboss.org/teiid/) - Data Virtualization system
  - [Modeshape](http://www.jboss.org/modeshape/) - Content Repository
  - Dashboard Builder

## Cartridge Installation
For OpenShift Online, you will need a user account - [instructions here](https://openshift.redhat.com/app/getting_started)

To install the DataVirtualization cartridge to OpenShift via command line, enter this:

```
rhc app create [MYAPP] https://raw.github.com/mdrillin/openshift-cartridge-datavirtualization/master/metadata/manifest.yml
```

Alternately, you can install the cartridge via the [OpenShift Web Console](https://openshift.redhat.com/app/console/applications)

## Getting started with the DataVirtualization cartridge
Once the cartridge installation has completed, enter this address to verify success

* http://[MYAPP]-[MYDOMAIN].rhcloud.com

### Teiid Data Virtualization
Two demo web applications are deployed with the Teiid OpenShift installation:

* http://[MYAPP]-[MYDOMAIN].rhcloud.com/vdbmanager - 'VDBManager' application

* http://[MYAPP]-[MYDOMAIN].rhcloud.com/webquery - 'WebQuery' application

A series of [Demo Articles](https://community.jboss.org/wiki/TeiidOnOpenShiftDemo-Part1-SourceManagement) are also provided, which walk you through an integration example.

### Modeshape Content Repository
You can access Modeshape at

* http://[MYAPP]-[MYDOMAIN].rhcloud.com/modeshape-webdav

* http://[MYAPP]-[MYDOMAIN].rhcloud.com/modeshape-rest

Two users are provided with the installation for testing

* admin/admin - admin user
* guest/guest - guest user

Consult the [Modeshape Documentation](http://www.jboss.org/modeshape/) for more information.

### Dashboard Builder
Access the dashboard builder at the following address

* http://[MYAPP]-[MYDOMAIN].rhcloud.com/dashbuilder

Two users are provided with the installation for testing

* dbadmin/dbadmin - dashboard admin user with edit capability
* dbuser/dbuser - dashboard user with readonly capability

More information regarding Dashboard Builder will be coming soon.




