Download Link: https://assignmentchef.com/product/solved-csc20-programming-concepts-and-methodology-ii-lab-10
<br>
<strong> </strong><strong>Objective</strong>: The objective of this lab is to get you some experience in using generic classes, enums, foreach loops and the Java class library.

<strong>The Java class library</strong>: The Java Class Library is a set of dynamically loadable libraries that Java application programs can call at runtime. Like other standard code libraries, Java class library provides the programmer a well-known set of functions to perform common tasks, such as maintaining lists of items or performing complex string parsing. For Java 1.5 or later, some generic classes and generic interfaces are included in the Java class library. Examples:




import java.util.*;

public class <strong>Stack&lt;E&gt;</strong> extends Vector&lt;E&gt; {       public <strong>Stack</strong>(); // constructor  public Boolean <strong>empty</strong>();  public E <strong>peek</strong>();            public E <strong>pop</strong>();             public E <strong>push</strong>(E item);

}

public class <strong>LinkedList&lt;E&gt;</strong> extends AbstractSequentialList&lt;E&gt;

implements List&lt;E&gt;, Queue&lt;E&gt;, Cloneable, Serializable {

<strong>public LinkedList</strong>(); // constructor

public E <strong>getFirst</strong>();       public E <strong>removeFirst</strong>();  public void <strong>addLast</strong>(E item);

public Boolean <strong>isEmpty</strong>();

}

<strong>The programming assignment</strong>: In your lab07,




<ol>

 <li>Replace your stack of Object with the generic class Stack&lt;E&gt;.</li>

 <li>Replace your queue of Object with the generic class LinkedList&lt;E&gt;.</li>

 <li>Replace Post.toString() method with a for-each loop.</li>

 <li>Replace your exception classes with the following exception class.</li>

 <li><strong>Remove all unnecessary type casts</strong>.</li>

</ol>




enum <strong>errorType</strong> { ExcessLeftParenthesis, ExcessRightParenthesis, ExcessOperator, ExcessOperand}; class <strong>infixException</strong> extends Exception {      private errorType etype;

public <strong>infixException</strong>(errorType et) { // constructor

etype = et;

}

public String <strong>toString</strong>() {

return etype.name();

}

}