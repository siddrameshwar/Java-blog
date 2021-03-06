## Java and Spring
<!--
You can use the [editor on GitHub](https://github.com/siddrameshwar/blog/edit/master/README.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.
-->


### Iterating through a Map
```markdown
Map<String, String> map = new HashMap<>();
map.put("Name", "Henry");
map.put("Country", "England");
map.put("City", "London");

for(Map.Entry entry: map.entrySet()) {
    System.out.println(entry.getKey() + " -> " + entry.getValue());
}

output: Country -> England                                                                                                       
        City -> London                                                                                                           
        Name -> Henry

```
### Converting int Array to ArrayList
```markdown
int[] intArray = {2,4,5};
List<Integer> intList = new ArrayList<Integer>(intArray.length);
for(int val: intArray)
    intList.add(val);
intList.forEach(System.out::print);
        
Output: 245
```

### Converting Integer ArrayList to int Array
```markdown
List<Integer> intList = new ArrayList<Integer>();
intList.add(44);
intList.add(25);
intList.add(33);

int[] intArray = new int[intList.size()];
for(int i = 0; i < intArray.length; i++)
    intArray[i] = intList.get(i);
    
for(int val: intArray)
    System.out.print(val + " ");
                                   
output: 44 25 33                                
```

## Arrays.copyOfRange() in Java
```markdown
copyOfRange(int[] original, int from, int to)
Copies the specified range of the specified array into a new array.
```

## Some Important points about Java
```markdown
●	Java also takes care of memory management and it also provides an automatic garbage collector.
●	Java is a platform-independent language-> intermediate byte code
●	The name of the class defined by the program is HelloWorld, which is same as name of file(HelloWorld.java). This is not a coincidence. In Java, all codes must reside inside a class and there is at most one public class which contain main() method.
●	By convention, the name of the main class(class which contain main method) should match the name of the file that holds the program.
●	Statically typed language -> specify variable type unlike in dynamically typed languages like python and ruby.
●	Strings are immutable.
●	Enums are used when we know all possible values at compile time, such as choices on a menu, rounding modes, command line flags, etc. It is not necessary that the set of constants in an enum type stay fixed for all time.
●	What is heap?
●	Methods and variables can be of 4 types. But class and Interfaces can have only 2 - public, default. Nested interfaces and classes can have all access specifiers.
●	The byte stream created is platform independent.
●	Static data members and transient data members are not saved via Serialization process
●	The Serialization runtime associates a version number with each Serializable class called a SerialVersionUID
●	ArrayList is better for storing and accessing data. ArrayList internally uses a dynamic array to store the elements.
●	LinkedList is better for manipulating data. LinkedList internally uses a doubly linked list to store the elements.
●	Final methods can not be overridden. private methods are not overridden and so are static methods.
●	Dynamic method dispatch allow Java to support overriding of methods which is central for run-time polymorphism.
●	In you don’t have any common code between rectangle and circle then go with interface, otherwise use Abstract class.
●	public void myDraw(Shape shape) { shape.draw() }; We can pass any Shape objects or any of its children objects.
```

## Spring
```markdown
●	What does Spring framework provides?
○	Application context and dependency injection
○	Data access(JDBC was pain)
○	Spring MVC
●	Dependency injection -> A way in which you decouple the conventional dependency relations between objects.
●	Spring can integrate with hibernate and struts.
●	Spring boot is a layer on top of Spring framework. It reduces configuration part for developers.
●	If we are using just spring, we would have to deploy the war file on to a separate server(tomcat) to run the application. But it spring boot we would have jar file instead of war file and it will have embedded server in it. You can run this on any JVM.
●	Spring will provide -> spring-boot-starter-web or spring-boot-starter-jdbc. Spring boot will do the configuration for you. If we want to change configuration we will have to change application.properties
●	Dependency injection container
●	@Component class HitachiHD implements HardDrive{...}
●	class Laptop { @Autowired HardDrive obj1;}
●	Dependency injection will help in loose coupling and aides in unit testing.

•	JPA is interface and Hibernate is Implementation of ORM
•	DAO service helps us to store the contents of class to table. We use @Repository annotation for it.
•	Most Important feature of Spring Framework is Dependency injection. At the core of Spring modules in Dependency injection or IOC Inversion of control. If we don't define dependency then we can't test our application. Spring takes care of all its beans and their dependencies. DI can be used to build Loosely coupled applications. Easy to test and maintain
```

```markdown
Integer.toBinaryString() //will convert number into binary value
str1.compareTo(str2)  // will do lexicographic comparison
```

```markdown
## Unit Testing using Junits and Mockito

Annotations for mocking
assertNotNull, assertEquals, assertTrue, assertFalse, BeforeEach, BeforeAll.

Stub is a kind of fake Object but we do not return any value(Logger). We implement the stub because we are not testing logger and we
don't want to spend time running it.
But for Mock object we return a mock object on which we do assertion. We are not testing the methods of the method for which we return 
mock objects, but we need the result of the object for the next lines of code or testing.

Try to include both positive and negative test cases. 

class ClassUnderTestTest {
    @InjectMocks   //It will inject the mock classes that we created for the interfaces inside of this class(interface) into the class
    ClassUnderTest objectOfClassUnderTet
    
    @Mock
    Interface interface;
    
    @BeforeEach
    void setUp() throws exception {
        MockitoAnnotations.initMocks(this); //For mockito to instatiate an object of the class under test. 
    }

    @Test
    testMethodTest() {
        Object object = new Object("name");
        when( interface.getMethod( anyString() ).thenReturn( object );
        assertEquals("name", interface.getMethod().getName());
    }
    
    //ObjectNotFoundException should be thrown if interface.getMethod() returns null;
    @Test
    testMethodTest_ObjectNotFoundException {
        //We do want others to change the exception type we are throwing
        when( interface.getMethod( anyString() ).thenReturn( null );
        assertThrows(ObjectNotFoundException, ()-> {
            interface.getMethod("test");
        }
    }
}
```
<!--
### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

[comment]: <> (Bulleted)
- List

1. Numbered
2. List
**BOLD
**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/siddrameshwar/blog/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.

 -->
