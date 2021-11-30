Kate Arsenault

November 28, 2021

Foundations of Databases & SQL Programming

Assignment 07

https://github.com/ArsenaultKate/DBFoundations-Module07

#User-Defined Functions in SQL

##Introduction
Most SQL programming interfaces like Microsoft SQL Server Management Studio will have a number of incredibly useful built-in functions. However, there are many cases where a programmer may want to implement their own calculations, formats, or even create their own tables of data for reporting. This paper will go over how to use different types of user-defined functions.

##Types of User-Defined Functions
“SQL Server user-defined functions are routines that accept parameters, perform an action, such as a complex calculation, and return the result of that action as a value. The return value can either be a single scalar value or a result set.” (Microsoft Documentation, https://docs.microsoft.com/en-us/sql/relational-databases/user-defined-functions/user-defined-functions?redirectedfrom=MSDN&view=sql-server-ver15, 12/14/2020) (External site)
Functions in SQL are incredibly handy tools in a SQL programmers kit. Functions allow the user to input a parameter, perform a calculation or apply some formatting, then return the result to be used in reports or in other views or stored procedures. Most programming interfaces will include a number of built-in functions that will perform commonly desired calculations like formatting a date or common math calculations like a sum or average. However, these built-in functions can be limited in scope. User-defined functions, or UDFs, are completely defined by the user and perform complex calculations and specific formatting.
There are three main types of user-defined functions which are defined by their outputs. A scalar function will return a single output value. The data returned by a scalar function can be a string, a number, or a date. In contrast, inline and multi-statement functions will return a table of values and together are known as table-valued functions. An inline function will take a single parameter and return multiple columns of data based on the select statement of the function. A multi-statement function is similar to an inline table function but will also define the table output by the function. 

##Using User-Define Functions
All types of UDFs can help keep from repeatedly writing the same code. Once a function is tweaked to your liking, it can be saved and called whenever that calculation or formatting is needed.  Additionally, all types of UDFs are very powerful because of their use of parameters. Using parameters can make the 
Scalar functions incredibly useful when you want to present data in a particular format. Perhaps you wanted to display a date as the month spelled out followed by the year in numbers, like January 2021. There is no built-in function that will format a date this way. Instead, you could write a UDF that would perform this formatting when called. Scalar functions can also be used to build check constrains, especially between different tables within a database, something SQL can’t easily do on its own. 
Both types of table-valued functions will execute once and return a large number of rows, while scalar functions would need to be executed multiple times. This can make table-valued functions much more efficient to run than scalar functions. In addition, the tables returned by table-valued functions can then be queried, joined, and used like a regular table. This can be useful when you repeatedly want to look at a subset of data from multiple tables. Table-valued functions can also perform complex calculations with data from multiple tables more easily because values have been brought into a single table as part of the function. Multi-statement valued table functions can also be used to create custom outputs within the table, something that can be helpful for querying performance indicators. 

##Summary
User-defined functions are useful tools for creating custom formats and tables for use in reports and data analysis. Scalar functions return a single value such as a custom format or calculation. Table-valued functions can created custom tables and perform custom calculations and return defined values for use in queries or to define performance indicators. Overall UDFs are a powerful tool for SQL developers.
