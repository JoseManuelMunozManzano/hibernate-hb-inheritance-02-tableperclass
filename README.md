# HIBERNATE - INHERITANCE - TABLE PER CLASS
This repository holds hibernate code example for mapping inheritance - table per class

A table for subclass.

For ease of development and testing, we'll use auto configuration

```xml
<property name="hibernate.hbm2ddl.auto">create</property>
```

Database tables are dropped first and then created from scratch.

Do this only in development/testing!!!

Note: See sql-scripts folder. Inside are the SQLs that you need to create the schema.