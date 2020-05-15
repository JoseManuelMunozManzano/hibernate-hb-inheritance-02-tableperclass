# HIBERNATE - INHERITANCE - TABLE PER CLASS
This repository holds hibernate code example for mapping inheritance - table per class

A table for subclass.

It's required to use the table generation strategy in the superclass.

@GeneratedValue(strategy = GenerationType.TABLE)


In hibernate.cfg.xml is necessary to increase pool size since additional connections are needed for accessing sequence table

```xml
<property name="connection.pool_size">10</property>
```

And, needed for the creation of the sequence table, we have to upgrade dialect to MySql 8

```xml
<property name="dialect">org.hibernate.dialect.MySQL8Dialect</property>
```


For ease of development and testing, we'll use auto configuration

```xml
<property name="hibernate.hbm2ddl.auto">create</property>
```

Database tables are dropped first and then created from scratch.

Do this only in development/testing!!!

Note: See sql-scripts folder. Inside are the SQLs that you need to create the schema.