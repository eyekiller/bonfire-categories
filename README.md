bonfire-categories
==================

Menus and categories module for Codeigniter Bonfire.
This module uses drag-and-drop approach to manage menus and menu items, similar to the one used in the Wordpress CMS menus. Please see the screenshot: [screenshot.jpg](/screenshot.jpg)


### Installation instructions

1. Download zip archive with the source code.
2. Upload 'categories' folder to the: application/modules folder on your server.
3. Navigate to: Developer -> Database tools -> Migrations, click on Modules tab and migrate Categories module to the highest version.

The back-end to the Menus and Categories module is located at: yoursite.com/admin/content/categories.
Sample public-facing page / Front-end can be found at: yoursite.com/categories, you may want to look at the index.php in the module's 'views' folder to see how to work with menus and categories in your front-end pages.

### Displaying Navigation in Your Pages

The Categories module comes with the helper file which can be used in your controller or view file. The code to load the helper is: 

```
$this->load->helper('categories/categories');
```

The following functions are available:

**list_all_menus()** - *get the list of menus as an array of objects or empty array if no menu's found*

**list_menu_categories($id)** - *get full navigation for a given menu 'id' _($id is required)_ - the id parameter for the menu.
The function will return an array of category objects (in case navigation have nested categories the function will return the tree object)

**find_a_category($id, $name)** - *find a category by it's 'id' or 'name' field*
_(at least one of parameters is required)_
The function will return a category object if the id or name param matches an existing category, otherwise return false.
