SequoiaDB README
=================

Welcome to SequoiaDB!

SequoiaDB is a distributed document-oriented NoSQL Database.

Engine:
-----------------
	sequoiadb       -- SequoiaDB Engine
	sdbstart        -- SequoiaDB Engine start
	sdbstop         -- SequoiaDB Engine stop
	sdblist         -- SequoiaDB Engine list
	sdbfmp          -- SequoiaDB fenced mode process


Shell:
-----------------
	sdb             -- SequoiaDB client
	sdbbp           -- SequoiaDB client backend process


Cluster Manager:
-----------------
	sdbcm           -- SequoiaDB cluster manager
	sdbcmart        -- SequoiaDB cluster manager start
	sdbcmtop        -- SequoiaDB cluster manager stop
	sdbcmd          -- SequoiaDB cluster manager daemon


Tools:
-----------------
	sdbdpsdump      -- SequoiaDB log dump
	sdbexprt        -- SequoiaDB export
	sdbimprt        -- SequoiaDB import
	sdbinspt        -- SequoiaDB data inspection
	sdbrestore      -- SequoiaDB restore
	sdbtop          -- SequoiaDB TOP
	sdbperfcol      -- SequoiaDB performance collection
	sdbwsart        -- SequoiaDB web service start
	sdbwstop        -- SequoiaDB web service stop


Drivers:
-----------------
	C Driver:
		libsdbc.a
		libsdbc.so
	C++ Driver:
		libsdbcpp.a
		libsdbcpp.so
	PHP Driver:
		libsdbphp-x.x.x.so
	JAVA Driver:
		sequoiadb.jar
	PYTHON Driver:
		lib.linux-x86_64-2.6
	.NET Driver:
		sequoiadb.dll
	Python Driver:
		pysequoiadb.tar.gz


Connectors:
-----------------
	Hadoop Connector:
		hadoop-connector.jar
	Hive Connector:
		hive-sequoiadb-apache.jar
	Storm Connector:
		storm-sequoiadb.jar


Building Prerequisites:
-----------------
	scons ( 2.3.0 )
	ant ( 1.8.2 )
        Python ( 2.7.3 )
	Linux x86-64:
		g++ ( 4.3.4 )
		gcc ( 4.3.4 )
		make ( 3.81 )
		kernel ( 3.0.13-0.27-default )
        Linux PPC64:
                g++ ( 4.3.4 )
                gcc ( 4.3.4 )
                make ( 3.81 )
                kernel ( 3.0.13-0.27-ppc64 )
	Windows:
		Windows SDK 7.1 ( Installation path must be C:\Program Files\Microsoft SDKs\Windows\v7.1 or
		C:\Program Files (x86)\Microsoft SDKs\Windows\v7.1 )
	Note:
		The utility and kernel version are for recommendation only.
		Users may use different version but may need to deal with any incompatibility issues.


Building Engine:
-----------------
	Engine Only:
		scons --engine
	C/C++ Client:
		scons --client
	Shell:
		scons --shell
	Tools:
		scons --tool
	Testcase:
		scons --testcase
	FMP:
		scons --fmp
	All ( except drivers ):
		scons --all
	Note:
		adding option "--dd" for debug build


Building Drivers:
-----------------
	C/C++ Client:
		scons --client
	PHP Client:
		cd driver/php5
		scons --phpversion=5.3.10
		Note:
			PHP source code is located in thirdparty/php directory
			The dir name must be "php-<version>"
	Python Client:
		cd driver/python
		scons
	Java Client:
		cd driver/java
		scons
	.Net Client:
		cd driver/C#.Net
		scons


Building Connectors:
-----------------
	Hadoop Connector:
		cd driver/java
		scons
		cd driver/hadoop/hadoop-connector
		ant -Dhadoop.version=2.2
	Hive Connector:
		cd driver/java
<<<<<<< HEAD
		scons
=======
                scons
>>>>>>> 32a62ef9ff03d7fa0756c3be203c3400f591b0cf
		cd driver/hadoop/hive
		ant
	Storm Connector:
		cd driver/storm
		ant
	PostgreSQL FDW:
		cd driver/postgresql
		make local
		# Make sure pg_config is in PATH
		make install


Running:
-----------------
	For command line options to start SequoiaDB, invoke:
		$ ./sdbstart --help
	For command line options to stop SequoiaDB, invoke:
		$ ./sdbstop --help
	For command line options to start cluster manager, invoke:
		$ ./sdbcmart --help
	For command line options to stop cluster manager, invoke:
		$ ./sdbcmtop --help


	To run in standalone mode:
		$ mkdir /sequoiadb/data
		$ /opt/sequoiadb/bin/sdbstart
		$ # sequoiadb start successful
		$ # start sequoiadb shell
		$ /opt/sequoiadb/bin/sdb
		> var db = new Sdb() ;
		> db.help() ;


	To run in cluster mode, please refer SequoiaDB Infomation Center.


Documentation:
-----------------
<<<<<<< HEAD
[SequoiaDB Home Page](http://www.sequoiadb.com/)
=======
	http://www.sequoiadb.com/
>>>>>>> 32a62ef9ff03d7fa0756c3be203c3400f591b0cf


Restrictions:
-----------------
<<<<<<< HEAD
	- SequoiaDB officially supports x86_64 and ppc64 Linux build on CentOS, Redhat, SUSE and Ubuntu.
=======
	- SequoiaDB officially only support 64 bit Linux build on CentOS, Redhat, SUSE and Ubuntu.
>>>>>>> 32a62ef9ff03d7fa0756c3be203c3400f591b0cf
	- Windows build and 32 bit build are for testing purpose only.


License:
-----------------
	Most SequoiaDB source files are made available under the terms of the
	GNU Affero General Public License (AGPL). See individual files for details.