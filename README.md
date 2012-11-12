# earch-helper cookbook
This recipe brings in a `Helpers::Search` module that adds/wrapps chefs search function.

# Usage
Include this recipe in your run_list, and `Chef::Recipe` namespace will get these methods.

you can Open up and mix these methods in other namespaces if needed
     
      class Chef
        class Template
          include Helpers::Search  
        end
      end

# Methods
### scoped_search
|args|type|default|
|scope|strong| |
|\*args| "standard search args" |
|&block| Ruby Block |

This wraps chef's search to add domain or environment awareness.

#### Usage 
     
     scoped_search("domain", :node, "attrib:match" )

#### Available "scopes"

* domain
* environemnt 

# Recipes
## default
  Does nothing, just makes sure the libs are loaded


# Author
Author:: Jesse Nelson (<spheromak@gmail.com>)
