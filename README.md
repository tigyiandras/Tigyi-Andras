## Welcome to GitHub Pages

You can use the [editor on GitHub](https://github.com/tigyiandras/Tigyi-Andras/edit/main/README.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/tigyiandras/Tigyi-Andras/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
 
 
 
 
 
<html>
<head></head>
<body>
  <div id='page-data'></div>
  <script>
  var xhttp = new XMLHttpRequest();
  xhttp.onreadystatechange = function() {
      if (this.readyState == 4 && this.status == 200) {
        var pageData = '';

        var data = JSON.parse(xhttp.responseText);

        pageData = '<h1>' + data.student.name + '</h1>';
        pageData += '<h4>Let\'s learn some ' + data.class + '!</h4>';
        pageData += '<h4>For homework: ' + data.homework[0] + '</h4>';

        document.getElementById("page-data").innerHTML = pageData;
        console.log('Done!');
      }
  };
  xhttp.open("GET", "https://raw.githubusercontent.com/programming-liftoff/json-simplified/master/jsondata.json", true);
  xhttp.send();
  console.log('here')
  </script>
</body>
</html>
