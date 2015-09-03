# SQL Monitor
Want to manages sql server performance? Check out SQL Monitor, it can monitor sql server processes and jobs, analyze performance, analyse system, object version control, view executing sql query, kill process / job, object explorer, database shrink/log truncate/backup/detach/attach etc.:

https://github.com/unruledboy/SQLMonitor


# Overflow Stack
The overflow stack family (Web Front End Stack, Database Stack, .NET Stack etc.):
http://overflowstack.github.io

# Localization
中文: 
http://www.cnblogs.com/unruledboy/p/DatabaseStack.html

# DatabaseStack
database technology stack, including MS SQL Server, Azure etc.

![Image of The Database Stack](https://raw.githubusercontent.com/unruledboy/DatabaseStack/master/preview.png)

# What and why?
Have you ever wondered:
* what technologies database server really includes? 
* how many do I possess?


I could not find a really comprehensive diagram that shows the database technology stack, so I come up with my own version.

There might be issues here and there, like the category, the individual ones, but the beautity is you can modify it as you want.



# The Database Stack

You can have a graphical preview here (use mouse to move / zoom): 

https://rawgit.com/unruledboy/DatabaseStack/master/ux/DatabaseStack.htm 

<!--BUILD_START-->

- Database
	- RDBMS
		- Basics
			- Normalisation
				- Normal Form
					- First Normal Form (1NF)
					- Second Normal Form (2NF)
					- Third Normal Form (3NF)
				- Transaction
					- ACID
						- Atomicity
						- Consistency
						- Isolation
						- Durability
		- MS SQL Server
			- SQL OS
				- Memory Management
				- Buffer Pool
				- Deadlock detection
				- Exception handling
				- Schedulers
				- InterOp
			- Storage Engine
				- Transaction Services
				- File Manager
				- Data File
				- Extents
				- Pages
				- Log File
					- Write Ahead Log (WAL)
					- Recovery
						- Full
						- Bulk-logged
					- Dirty Pages
					- Lazy Writer
					- Checkpoint
					- Log Sequence Number (LSN)
			- Relational Engine
				- Query Processing
					- Parser
					- Optimizer
						- Stat
						- Hinting
						- Plan
							- Compilation
							- Caching
							- Recompilation
					- SQL Manager
					- Database Manager
					- Query Executor
				- Memory Management
				- Thread and Task Management
				- Buffer Management
				- Distributed Query Processing
			- Communication
				- SQL Server Network Interface (SNI)
				- Tabular Data Stream (TDS)
				- Protocols
					- TCP/IP
					- Named pipes
					- Shared memory
					- Virtual Interface Adapter (VIA)
					- Web Services
			- Core Concepts
				- Instance
					- Default
					- Named
					- Alias
				- Port
					- Default: 1433
					- Dynamic
				- Transaction
					- ACID
						- Atomic
						- Consistent
						- Isolated
						- Durable
					- Types
						- Implicit
							- single UPDATE/DELETE
						- Explicit
							- BEGIN/COMMIT/ROLLBACK
					- Checkpoint
					- Isolation Levels
						- Read uncommitted
						- Read committed
						- Repeatable read
						- Snapshot
						- Serializable
				- Concurrency
					- Lock
						- Optimistic
						- Pessimistic
						- Exclusive
						- Shared
					- Wait
					- Latch
					- Deadlock
						- Kill
					- sync/async
					- Blocking
					- Row versioning
			- Core Objects
				- Database
					- Recovery Models
						- Simple
						- Full
						- Bulk logged
					- Compatibility Levels
						- Version Number
							- Effectively SQL Server version number
							- @@VERSION
						- 130: SQL  Server 2016
						- 120: SQL  Server 2014
						- 110: SQL  Server 2012
						- 100: SQL  Server 2008
						- 90: SQL  Server 2005
						- 80: SQL Server 2000
					- Encryption
					- Copy
				- Table
					- Standard
						- Partition
						- Compression
					- Table Variable
					- Temp Table
						- Local
						- Global
					- FileTable
				- View
					- Standard
					- Indexed
					- Partitioned
				- Stored Procedure (SP)
				- Function (FN)
					- Table-valued Function
					- Scalar-valued Function
				- Data Type
					- Types
						- System Type
						- User-defined Type (UDT)
					- Conversion
					- Precedence
					- Synonym
					- Precision/Scale/Length
					- XML
					- JSON
					- Spatial (CLR)
				- Index
					- Index Types
						- Clustered Index
						- Non-clustered Index
					- Index Setting
						- Include
						- Filter
					- Index Management
						- Rebuild
						- Reorganise
						- Disable
						- Enable
						- Drop
				- Column
					- columnstore
					- NTFS FileStream
				- Schema
				- Trigger
					- Table Trigger
						- BEFORE
						- FOR/AFTER
						- INSTEAD OF
				- Constraint
				- Key
				- Default
				- Synonym
				- Cursor
				- Collation
				- Login
				- User
				- Rule
				- Server role
				- Endpoint
				- Job
					- Job Agent
					- Job Activity Monitor
					- Alert
					- Operator
					- SQL Job
						- Step
						- Schedule
						- Notification
				- SQL CLR (.NET CLR)
					- Assembly
					- Managed Code Types
						- Function
						- Stored Procedure
						- Trigger
						- UDF
						- UDA
						- UDT
					- Security Levels
				- Linked Server
				- Service Broker
			- Standard
				- ANSI 92
			- Languages
				- Query Language
					- T-SQL (Transact-SQL)
					- MDX (MultiDimensional eXpressions)
				- Data Manipulation Language (DML)
					- CRUD
						- Create (INSERT)
						- Retrieve (SELECT)
						- Update (UPDATE)
						- Delete (DELETE)
					- MERGE
					- TEXT
						- UPDATETEXT
						- WRITETEXT
						- READTEXT
					- BULK INSERT
					- EXECUTE
				- Data Definition Language (DDL)
					- CREATE
					- ALTER
					- DROP
					- TRUNCATE
					- RESTORE
					- RECONFIGURE
				- Data Control Language (DCL)
					- GRANT
					- REVOKE
				- Transaction Control Language (TCL)
					- BEGIN TRANSACTION
					- COMMIT
					- ROLLBACK
					- SAVE TRANSACTION
			- System Databases
				- master (dbs, logins, configs)
				- tempdb (temp tables / sps)
				- msdb (jobs/alerts/backups)
				- model (template for new db)
				- resource (invisible, system objects)
			- File
				- primary (MDF)
				- secondary (NDF)
				- log (LDF)
				- File/Filegroup
				- Auto Grow
			- Runtime
				- Process
				- Worker
				- Connection
				- Request
				- Stall
				- Stats
				- Cache
					- aging
				- Catalog Views
				- Dynamic Management Views (DMV)
					- Execution count
					- Execution io/cpu/perf
				- Full Text Search (FTS)
					- Integrated Full Text Search (iFTS)
				- Trace flags
			- Replication
				- Log Shipping
				- Publish/Subscribe
					- Transactional
					- Merge
					- Snapshot
				- Mirroring
					- Core
						- Principal
						- Witness
					- Database Mirroring Monitor
				- AlwaysOn
				- Clustering
					- Core
						- Shared Disk Array
						- Quorum
					- Failover
						- Active/Active
						- Active/Passive
				- Snapshot
			- Versions
				- Express
				- BI
				- Web
				- Standard
				- Enterprise
				- Datacenter
				- Local DB
			- Management
				- SQL Server Management Studio (SSMS)
				- SQL Server Command Line Util (sqlcmd)
				- SQL Monitor ;-)
			- Maintenance
				- Maintenance Plan
				- Logs
				- Database Mail
				- Database
					- Backup/Restore
						- Mode
							- Full
							- Differential
							- Transaction log
					- Online/Offline
					- Attach/Dettach
					- Shrink
				- Import/Export
				- DBCC
				- Bulk Copy (bcp command line)
				- Resource governor
				- Facets
			- Business Intelligence (BI)
				- SQL Server Integration Service (SSIS)
				- SQL Server Reporting Service (SSRS)
				- SQL Server Analysis Service (SSAS)
			- Troubleshoot
				- Dedicated Administrator Connection (DAC)
					- ADMIN:INSTANCE
					- SQL Browser service must be running
				- SQL Server Profiler
				- Activity Monitor
				- Error
					- Severity Levels
					- Error Log
					- sys.xp_readerrorlog
			- Performance
				- Seek
				- Scan
				- Fragmentation
				- Partitioning
				- Database Engine Tuning Advisor
			- Services
				- SQL Server
				- SQL Server Browser
				- SQL Server Agent
			- Connectivity
				- ADO.NET
				- ODBC
		- Oracle
		- MySQL
		- PostgreSQL
		- Informix
	- Cloud
		- Azure
			- Database
			- Redis Cache
			- Storage
				- Blobs
				- Tables
				- Queues
				- StorSimple
				- Files and Disks
			- StorSimple
			- SQL Data Warehouse
	- NoSQL
		- Azure Document DB

<!--BUILD_END-->	
