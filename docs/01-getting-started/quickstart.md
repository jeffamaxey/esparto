Quickstart
==========

The esparto library can be installed with pip:

```bash
pip install esparto
```

<br>

Documents start with a Page object, to which user content can be added iteratively.
Creating a page, adding basic content, and saving the file can be achieved in a few
short lines:

```python
import esparto as es

my_page = es.Page(title="Esparto Quickstart")

content_md = """
Your *content* goes **here!**
"""

my_page += content_md
my_page.save("esparto-quick.html")
```
<br>

The rendered HTML document:

<img src='../esparto-quickstart-screenshot.png' style='border: 1px dotted lightgrey; width: 60%; height: auto'>

<br>

To add an image, pass a filepath to the page:

```python
import esparto as es

my_page = es.Page(title="Esparto Quickstart")

content_md = """
Your *content* goes **here!**
"""

my_page += content_md
my_page += "image.jpg"

html = my_page.save("esparto-quick-image.html")
```
<br>

Esparto determines that the string points to a valid image and loads the file:

<img src='../esparto-image-screenshot.png' height=70% style='border: 1px dotted lightgrey; width: 60%; height: auto%'>

<br>

Please see the [examples page](../02-user-guide/examples.md) for more.

<br>