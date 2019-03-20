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
