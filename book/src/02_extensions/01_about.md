# Extending chipmunk with plugins
In this section the basics of plugins will be covered as well as how to create a custom plugin for **Chipmunk**.

## Plugin types
To create a plugin, it's necessary to understand what types of plugins exist on **Chipmunk**. There are **3** different types of plugins that already exist on **Chipmunk**:

1. **Angular**      (DLT-Render)
2. **Standalone**   (row.parser.ascii)
3. **Complex**      (Serial, Processes, xTerminal)

### Angular
Plugins of the **Angular** type provide a UI at the front-end in **Chipmunk** with which the user can interact directly with **Chipmunk**. Angular plugin only consist of a front-end and no back-end.
An example from the implemented plugins is `DLT-Render`. `DLT-Render` renders output data of `.dlt` files and puts them into columns.

### Standalone
Plugins of the **Standalone** type exist in the front-end, but don't provide a UI. **Standalone** plugins consist of parser(s). The plugin can modify the output in the main window, e.g. putting the date in front of every line.
An example from the implemented plugins is `row.parser.ascii`. `row.parser.ascii` renders the output data by colorizing specific terms.

### Complex
Plugins of the **Complex** type provide both a UI and functionality in the back-end. The idea in these kind of plugins is to provide the front-end with the necessary data from the back-end when any external sources are requested.
An example from the implemented plugins is `Serial`. `Serial` provides a UI to connect to a port. The connection is being established in the back-end by making use of an external library and informs the front-end about the result of the connection attempt.

## How to create a plugin
One way of creating plugins is to pull the latest version of the plugins from Github **(link coming soon)**. In the plugins folder there will be a template plugin called **myplugin**. The template is provided to save the trouble with all the pre-work and setup. The template plugin will be a complex type of plugin, but can be changed into any kind of plugin.

The creation of a plugin will be further explained in the following chapters, starting with the basics. 