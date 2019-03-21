# fullstack-learning


<h2> Day 1 </h2>

<div>
<p> work flow -> project structure -> pkg used (read doc </p>

<p> head -> metadata</p>
<p> "!doctype html -> define html5" </p>
<p>alt -> img alternative text if img not shown</p>
<p>disable -> for button, if condition not meet</p>

<p>title -> display as tool tip</p>
<p>DOM doc object model -> allows program and script to access and update content</p>
<p>display none ->remove element from dom ex: toggle click button twice will not show</p>
<p>visibility hidden ->not shown but would take place in dom</p>

<p>bagel to transpile es6 to es5</p>

<p>#a -> id selector</p>
<p>.a  ->  class</p>
<p>a  -> element

<p>responsive web design -> provide optimal viewing experience, resizing, panning, scroll </p>
<p>bootstrap, media query </p>

<p>Media query</p>
<p>@media only sceen and max-width ->  only less than xxx show </p>

<p>JS -> Client side scripting language</p>
<p>Use strict </p>

<p>naming convention:</p>
<p>usually remove  a,e,i,o,u</p>

<p>debugger; comon use break point</p>
<p>prompt, alert and confirm</p>

<p>always put script in the end so it can find element (html excute line by line</p>




<p>switch stop when reaches break;</p>
<p>pre increment vs post increment performance ?question</p>

<p>do while < 5 will  1+2+3+4+5</p>

<p>functiion expression vs declaration (hoisted)</p>
<p>const vs let: cannot reassign const</p>


<p>call, apply, bind</p>
<p>call(this, arg1, arg2)</p>
<p>apply(this, [argsArray])</p>
<p>bind(object you want to bind, arg)</p>
<p>splice()</p>
</div>



<h2> Day 2 </h2>

<div>
Primitive(number, string...) vs reference(object):
  when b = a in object, it shares same memory
  then, to copy a reference use: deepclone, ...operator
  
 a = null;
 a;  is undefined
 why use const rather than var? question.
 
 <h3> JS advanced</h3>
 Scopre: 
 IIFE: immedate invoke function. only invoke once. when call only the return part invoke
 
 6 888 6 888 888
 
 in arrow function this is decalre when declaration 
 
 
 callback or promise for data getting. So it will get the data then process the rest
 
 async/await new feature in js.
 
 
 callback hell -> not readable not undestandable thats why use promise.
 what is prototype? to use for inheritance. because js is not oop. 
 
 CRUD
 get -> read 
 post -> create 
 put -> update
 delete -> d
 
 <b>const and let</b> adavantage: fix scope problem
 http is asynchro
 understand http request in js 
 
 Arrow function
 functionname = (parm1, parm2 ..) => {}
 
 
</div>


<h3> Day 3</h3>
<div> 
  <h4> SQL </h4>
  <ul>
  <li>DDL - data definition language ( create, alter, drop, truncate </li>
  <li>DML - data manipulation language ( create, insert, delete, update </li>
  <li>DCL - data control language ( grant revoke </li>
  <li>TCL - transaction control language </li>
  </ul>
  
  <pre> "CREATE TABLE table_name( 
   column_name datatype(size), 
   column_name datatype(size),  
   ..... 
   column_name datatype(size) PRIMARY KEY);" 
   
   CREATE DATABASE db_name
   
  Ex: 
   CREATE TABLE dbo.EmployeeSales  
   ( DataSource   varchar(20) NOT NULL,  
      BusinessEntityID   varchar(11) NOT NULL,  
     LastName     varchar(40) NOT NULL,  
     SalesDollars money NOT NULL  
    );  
   
   </pre>
   
   <h4>ALTER - modify exist entites </h4>
  
   <pre> ALTER TABLE table_name( 
   ALTER COLUMN column_name datatype(size), 
   ..... 
   );" 
   
   ALTER DATABASE {database_name | current} {
   MODIFY NAME = new_database_name | COLLATE collation_name
   .....
   }
   
   EX: 
       ALTER DATABASE AdventureWorks2012
       Modify Name = Northwind ;
       GO
       
       CREATE DATABASE testdb
       COLLATE SQL_Latin1_General_CP1_CI_AS ;
       GO

       ALTER DATABASE testDB
       COLLATE French_CI_AI ;
       GO
   
   </pre>
   
   <h4>DROP - remove data, structure, and lost forever </h4>
  
   <pre> DROP DATABASE [ IF EXISTS ] { database_name | database_snapshot_name } [ ,...n ] [;]
    DROP TABLE [IF EXISTS] [db_name.[schema_name | table_name] [..,n] ]
    
    Ex: 
        DROP TABLE ProductVendor1 ;
        DROP TABLE AdventureWorks2012.dbo.SalesPerson2 ; //drop SalesPerson2 table in db "AdventureWorks2012"

   </pre>
   
   <h4>TRUNCATE - remove table without logging it and left structure </h4>
   <p> cannot truncate table which referenced by a FOREIGN KEY constraint, no trigger </p>
   <pre> 
    TRUNCATE TABLE HumanResources.JobCandidate;  
    TRUNCATE TABLE PartitionTable1   
    WITH (PARTITIONS (2, 4, 6 TO 8));  
   
   
   </pre>
   
   <h4>INSERT - add one or more row to table or view </h4>
   <p> A syntax error is raised if a column list is not provided. </p>
   <pre> 
    INSERT INTO <target_table> SELECT <columns> FROM <source_table>
    
   EX:
    INSERT single/multiple row data:
    INSERT INTO Production.UnitMeasure  
    VALUES (N'FT', N'Feet', '20080414'), ...; 
    
    INSERT not in the same order as the table columns:
    INSERT INTO Production.UnitMeasure (Name, UnitMeasureCode,  
    ModifiedDate)  
    VALUES (N'Square Yards', N'Y2', GETDATE());  
 
   
   
   </pre>
   
   <h4>DELETE - remove one or more row to table or view </h4>
   <p> The DELETE statement is always fully logged. can have trigger </p>
   <pre> 
    DELETE * FROM  table_name;
    DELETE FROM  table_name WHERE some_col = some_val;
  
   EX:
    DELETE FROM list WHERE name = 'David';
   
   
   </pre>
   
   
    <h4>UPDATE - change exist data in table or view </h4>
    
   <pre> 
    UPDATE table_name
      SET
      col_name = new_val;
      col_name = new_val
      WHERE some_col = some_val (condition)
  
   EX:
    UPDATE TraineeList
      SET
      first_name = 'ben'
      WHERE id = 5
   
   </pre>
   
   
    <h4>SELECT</h4>
   <pre> 
    SELECT select_list [ INTO new_table ]
    [ FROM table_source ] [ WHERE search_condition ]
    [ GROUP BY group_by_expression ]
    [ HAVING search_condition ]
    [ ORDER BY order_expression [ ASC | DESC ] ]


  
   EX:
    SELECT e.*  
    FROM DimEmployee AS e  
    ORDER BY LastName; 
   
   </pre>
   
   
   
   
   ####################
  table have two page, sertion page
  normailization redundency remove. 
  easy to maniputlate 
  
<p>n keyword means uni-code varchar(ex: for other language </p>
<p>varchar is 2</p>
<p>nvarchar is 4</p>
<p>internal conversion: automatically if data type allow</p>

<p>external conversion: manually</p>
  format of data, specify data type of each colum
  safer to manipulate data
  
  check or remove duplicate from existing table


  view is virtual table which doesn't include actual data. we store query in view not data
  why use view? query in it when created. user can acess the view but deny acess to the table
  materialize view. (adv level
  
  insert into view 
  multiple database. if insert into from different db will not work. enforce
  trigger for view(later discuss
  
  
  temp table in system db.
  why use temp ?
  do not want to change datasource, we use temp table.
  Using a view will change data source.
  view is not a table cannot have table property. but you can have it in temp table.
  if there is one set of data always use it, first create but rest access. private data source, query fasater(temp table
  
  substring, replace in sql
  <b>date/time </b>
  
  sample 1 records,  , dulipcate 25 25
  
  scalar function not much discuss
  always have GO
  constraint: 6 types: primary, foreign, unique, not null, check 
  
</div>
