# <p style="text-align: center;"> JavaScript </p>  

* Used for functionality / behaviour for a web page, DOM manipulation. General purpose language  

* A **high-level, dynamic, weakly typed, prototype-based, multi-paradigm** (supports event-driven, functional, imperative, OO), **interpreted** programming language (VM based so requires environment to live in - **JS Engine**)  

* **No support** for **I/O** (generally provided by host environment)  

* There is **no single JavaScript implementation** - different engines in most web broswers meaning some features might be missing or additional in others  

---  
### JS Engines:  

* V8 - google chrome engine (also used in Node.js)  
* Spidermonkey - Firefox engine  
* JavaScriptCore - marketed as Nitro, used in Safari  
* Node.js - standalone tool to run JS outside browser enabling JavaScript to run server side  

---  
### Using JavaScript:  

* **Inline**   
&emsp;&emsp;`<button id="hellobutton" onclick="alert('Hello World')">Click Me</button>`  
* **Script block**  
&emsp;`<script>` 
&emsp;&emsp;`document.getElementById('hellobutton').onclick = function() {`  
&emsp;&emsp;&emsp;`alert('Hello World');`  
&emsp;&emsp;`}`  
&emsp;`</script>`  
    * Scripts can be placed either inside the head or body sections - however placing inside **body improves display speed** because script interpretation slows down the display  
* **External script**  
    * Call from html file (place in head or **body - recommended**):  
&emsp;&emsp;`<script src="scriptFileName.js"></script>`  
    * Within js file:  
&emsp;&emsp;`function myFunction() {`  
&emsp;&emsp;&emsp;`document.getElementById("demo").innerHTML = "Paragraph changed.";`  
&emsp;&emsp;`}`  
    * Advantages of js file -  
      * Seperates HTML and code  
      * Aids readability  
      * Cached JavaSript files speed up page loads  
      * Reusuable code  
---

### Types, comments, keywords  

#### Variables can be declared:  

* Block level using **let**  
* Function level using **var** or **const**  
* **NO TYPE** attached, any value can be stored in any variable  
* *Value* is **undefined** until initialised  

#### Primative types:  
* **Undefined** - not initialised  
* **Null** - Declared but value is empty  
* **Number** - round with **toFixed()**  
* **String** - Access individual letters using **charAt()**, compare using **==**  
* **Boolean** - **true & false**  
* **Symbol** - unique & immutable identifier  

#### Native objects  
* **Arrays** - lists of values indexted by keys (numeric & zero based indexing)  
* **Date** - signed millisecond count from zero (representing 1970-01-01 00:00:00 UTC)  
* **Error** - Can be used to create custom error messages  
* **Math** - e.g. E, Natural Log, Pi and functions e.g. max, min, random  
* **Regular Expressions** - Store text patterns  
* **Function** - Constructed using Function constructor  

![Comments](./Images/Comments.png)  
![Keywords](./Images/Keywords.png)  

---  

#### Control Structures  

#### If...else  
`if (expr) {`  
&emsp;`// statements;`  
`} else if (expr2) {`  
&emsp;`// statements;`  
`} else {`  
&emsp;`// statements;`  
`}`  

#### Switch statement  
`rswitch (expr) {`  
&emsp;`case SOMEVALUE:`  
&emsp;&emsp;`// statments:`  
&emsp;&emsp;`break;`  
&emsp;`case ANOTHERVALUE:`  
&emsp;&emsp;`// statements;`  
&emsp;&emsp;`break;`  
&emsp;`default:`  
&emsp;&emsp;`// statments;`  
&emsp;&emsp;`break;`  
`}`  

#### Conditional operator  
`result = condition ? expression:`  
`alternative;`  

---  

### Loops  

#### For loop  
`for (initial; condition; loop statment) {`  
&emsp;`/*`  
&emsp;` statements will be executed every time`  
&emsp;` the for{} loop cycles, while the condition is satisfied`  
&emsp;`*/`  
`}`  

#### For In loop  
`for (var property_name in some_object) {`  
&emsp;`// statments using some_object[property_name];`  
`}`  

#### While loop  
`while (condition) {`  
&emsp;`statment1;`  
&emsp;`statment2;`  
&emsp;`statment3;`  
&emsp;`...`  
`}`  

#### Do...While loop  
`do {`  
&emsp;`statement1;`  
&emsp;`statement2;`  
&emsp;`statement3;`  
&emsp;`...`  
`} while (condition);`  

---  

### Functions  

Can declare by 1 of the following:  
1. `function add(x,y) { return x + y; };`  
2. `var add = function(x,y) { return x + y; };`  
3. `var add = new Function('x','y','return x + y');`  

![Objects](./Images/Objects.png)  

---  

### Exception Handling  

`try {`  
&emsp;`// Statments in which exceptions might be thrown`  
`} catch(errorValue) {`  
&emsp;`// Statments that execute in the event of an exception`  
`} finally {`  
&emsp;`// Statments that execute afterward either way`  
`}`  

---  

### Best practices  

[Best practices link](https://www.w3.org/wiki/JavaScript_best_practices)

* Call things by their name - easy, short and readable variable and function names  
* Avoid globals  
* Stick to a strict coding style  
* Comment as much as needed but not more  
* Avoid mixing with other technologies  
* Use shortcut notation when it makes sense  
* Modularise - one function per task  
* Enhance progressively  
* Allow for configuration and translation  
* Avoid heavy nesting  
* Optomise loops  
* Keep DOM access to a minimum  
* Don't yield to browser whims  
* Don't trust any data  
* Add functionality with JavaScript, don't create too much content  
* Build on the sholders of giants  
* Development code is not live code  

---  

### JavaScript / HTML Events  

HTML events are **"things"** that happen to HTML elements. When JavaScript is used in HTML pages, JavaScript can **"react"** on these events  

`<element event='some JavaScript'>`  
* Can use single or double quotes, but **don't mix** (unless using within each other as below)  

Can also use within an anchor tag for example:  
`<p><a href="#" onClick="alert('Hello World');">Click Me</a></p>`  

#### Common HTML Events  

[Full HTML DOM Events](https://www.w3schools.com/jsref/dom_obj_event.asp)  

|Event|Description|
|:---|:---|
|onchange|An HTML element has been changed|
|onclick|The user clicks an HTML element|
|onmouseover|The user moves the mouse over an HTML element|
|onmouseout|The user moves the mouse away from an HTML element|
|onkeydown|The user pushes a keyboard key|
|onload|The browser has finished loading the page|

---  

### JavaScript Debugging  

Modern browsers have a built-in JavaScript debugger  

#### Open console  
`Ctrl + shift + I`  
**or**  
click the `3 dots` top right of browser >> `More tools` >> `Developer tools`  

Click `console` at top  

#### Log to console  
* Can be within a script:  
`console.log(variable/value);`  
* Or after an event:  
  `<p><a href="#" onClick="console.log('Hello World')">Click Me</a></p>`  

#### Set breakpoint  
keyword **debugger** stops executing before it executes the following lines of code  
`let x = 15 * 5;`  
`debugger;`  
`document.getElementById("demo").innerHTML = x;`  