jetbrick-jdbclog
================

<a target="_blank" href="http://shang.qq.com/wpa/qunwpa?idkey=c81a8f922d2b00422761558c4c547a4c4af778edcb0a70c99aadf9e33d80cb11"><img border="0" src="http://pub.idqqimg.com/wpa/images/group.png" alt="QQ群:310491655" title="QQ群:310491655"></a>

This is a jdbc logger project for jetbrick, **Support JDK6+**.

Usage
==================

```java
DriverManagerDataSource ds = new DriverManagerDataSource();
ds.setDriverClassName("jetbrick.jdbclog.JdbcLogDriver");
ds.setUrl("jdbc:oracle:thin:@localhost:1521:orcl");
ds.setUsername("sa");
ds.setPassword("");
```

This JdbcLogDriver can auto identify following drivers.

* MySQL
* Oracle
* JTDS
* SQL Server 97/2000/2005
* DB2
* SyBase
* PostgreSQL
* HSqlDB
* Derby
* Informix
* TimesTen
* IBM-AS400
* SAP DB
* InterBase
* JDBC-ODBC

If you use other driver, you can add real driver class name into connection url string. 
Pattern: CustomizeConnectionUrl = `"jdbclog" ":" [DriverClassName] ":" ConnectionUrl`. 
In customize connection url, the DriverClassName is optional.

For Oracle:
```
jdbclog:oracle.jdbc.driver.OracleDriver:jdbc:oracle:thin:@localhost:1521:orcl
```

If you use `jdbc-odbc Bridge` or `Apache Derby`, you must use customize connection url.

For Derby:
```
jdbclog::jdbc:derby:MyDB;user=test;password=test
```

Maven
==================

```xml
<dependency>
    <groupId>com.github.subchen</groupId>
    <artifactId>jetbrick-jdbclog</artifactId>
    <version>1.0</version>
</dependency>
```

Downloads
==================

* [jetbrick-jdbclog-1.0.jar][1]
* [slf4j-api-1.7.7.jar][2]

[1]: http://search.maven.org/remotecontent?filepath=com/github/subchen/jetbrick-jdbclog/1.0/jetbrick-jdbclog-1.0.jar
[2]: http://search.maven.org/remotecontent?filepath=org/slf4j/slf4j-api/1.7.7/slf4j-api-1.7.7.jar

License
==================

```
Copyright 2013-2014 Guoqiang Chen. All rights reserved. 
Email: subchen@gmail.com

Licensed under the Apache License, Version 2.0 (the "License"); 
you may not use this file except in compliance with the License. 
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

```
