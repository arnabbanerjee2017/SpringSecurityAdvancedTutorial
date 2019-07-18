/*
 * Copyright (c) 2019, ARNAB BANERJEE. All rights reserved.
 * 
 * Redistribution and use in source and binary forms, with or without
 * modification, are permitted only for academic purposes.
 * 
 * For further queries / info: arnab.ban09@gmail.com
 */

DATABASE SUPPORT IN SPRING SECURITY
==================================================================================================================
-> Spring Security can read user account info from database, out-of-the-box.
-> By default, you have to follow Spring Security's predefined table schemas.
-> You can also customize the table schemas. In that case, you will be responsible for developing the code to access the data, like JDBC, 
Hibernate, or Spring Data JPA.
-> For the default tables schemas as suggested by Spring Security, please refer the myhome_users.sql and myhome_authorities.sql. You need to
create those tables in your Database, for me it is MySQL.
-> In Spring Security 5, passwords are stored using a specific format.
	-------------------------
	|  {id}encodedPassword	|
	-------------------------
---------------------------------------------------------------------------------------------
|		id		|		Description															|
---------------------------------------------------------------------------------------------
| noop			| Plain text passwords.														|
---------------------------------------------------------------------------------------------
| bcrypt		| BCrypt password hashing.													|
---------------------------------------------------------------------------------------------
| others are also there.....																|
---------------------------------------------------------------------------------------------
In the SQL files, you can see the passwords. It is currently noop.
					