## Java tutorials
<!--
You can use the [editor on GitHub](https://github.com/siddrameshwar/blog/edit/master/README.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.
-->


### Iterating through a Map
```markdown
Map<String, String> map = new HashMap<>();
map.put("Country", "England");
map.put("Name", "Henry");
map.put("City", "London");

for(MapEntry entry: map.entrySet()) {
    System.out.println("key " + entry.getKey() + " value " + entry.getValue());
}

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
