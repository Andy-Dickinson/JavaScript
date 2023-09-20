# <center> D3 for data Visualisation </center>  

* DOM elements are accessible in HTML (tags), CSS (selectors) and
JavaScript (nodes)  
* A D3 Selection is a wrapper object surrounding DOM nodes in JavaScript  

---  

Many D3 **functions** use the following idiom:  
* When called **with** approrpriate arguments, these functions act as *<u>setters</u>* - setting the corresponding property to the supplied value. Many D3 setters can take an **accessor function** as an argument, which is expected to return a value that will be used to set the property in question  
* When called **without** arguments, these functions act as *<u>getters</u>* - returning the current value of the property  
* To entirely <u>*remove*</u> a property, call the appropriate setter while supplying **null** as argument  

---  

* Two methods can **create selections**:  
  `d3.select(selector)` - selection with the first element matching selector  
  `d3.selectAll(selector)` - selection of all elements matching selector
* If nothing is matched, an empty selection is created  
<br>
* Can be **chained**:  
`mySelection.selectAll(selector)` - access descendants of the DOM node  
`mySelection.append(tag)` - lets you add a direct child to each elements
of your selection, and returns these children as a new selection  
<br>
* Making a selection:
![Making a selection](./Images/making_a_selection.png)  
<br>
* **Binding** data to elements:  
`mySelection.data(myData, key)` - method for binding myData to
elements of mySelection. `key` is an accessor to uniquely match data items to DOM elements.
  * Default key is the data indices  
  * Accessor functions essentially declare how to reach part of data objects, 
e.g., &emsp; d => d.k  
<br>
* **Joining** elements:  
  * Once DOM elements are bound to data entries, we have four possibilities:  
![Joining elements](./Images/joining_elements.png)  
`mySelection.join(…)` - method that gives us access to these three
sub-selections:  
  * **enter selection**, for elements to add  
  * **update selection**, for elements to change  
  * **exit selection**, for elements to remove  
<br>
  * **returns** the fully updated selection (enter+update)  
![binding & joining](./Images/binding_joining1.png)  
![binding & joining](./Images/binding_joining2.png)  
Note the accessor function in the 'data' function  
By **key value**:  
![binding & joining](./Images/binding_joining3.png)  
Without accessor function, takes **objects as passed**:  
![binding & joining](./Images/binding_joining4.png)  
Adding missing elements and removing extra ones is a **default behaviour**  
`mySelection.join(tag)` - shorthand for doing so (refers to the
element that need appending)  

<br> 

---  

**SVG** - Scalable Vector Graphics  
* Markup language (XML based) for 2D vector graphics  
* Manipulated in JavaScript  
* Styled in CSS  
* HTML is for text and input, SVG is for graphics  
<br>
* svg - always the top level element of the graphic  
  * Has width and height attributes to define the viewport  
* g (for group) - aggregator element  
  * Useful to apply transformations to a set of elements  
<br>
* SVG provides explicit tags for a set of predefined simple shapes.
Each shape has a set of specific attributes that control size and posi‐
tion:  
![svg shapes](./Images/svg_shapes.png)  

