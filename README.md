# MVCPluginFramework
ASP.NET MVC Plugin Framework

# Now updated to include Twitter Bootstrap plugin site demo #
The codebase now includes a Twitter Bootstrap based MVC demo site that goes along with the original jQuery UI based MVC demo site.

This demo also shows off how the Syrinx ASP.NET MVC menu control can be used to generate html that can conform to Bootstrap so that the Bootstrap JavaScript manages the submenus rather than the Syrinx Menu JavaScript. The Plugin Demo support for adding menu items works in both easily thanks to the flexibility of the Syrinx ASP.NET MVC Menu control.

# The Problem #

    1.Building large web applications in one massive ASP.NET MVC project is not easy to manage, especially with multiple developers.
    2.Having external developers add new functionality to an existing ASP.NET MVC project is not easy to do. Controllers, Models, and business logic can all be put into separate packages, but Razor views are harder to move out of the main web project.
    3.Building generic plugins that can work across a variety of customized systems is best done with a common architecture. For example, I can build a generic Google Analytics plugin that can add analytics JavaScript into any system using the plugin framework, you can use that plugin in your custom ASP.NET MVC site along with any plugins you're building specifically for your system.
    
# The Solution #
The MVC Plugin Framework helps you build web applications that can be extended with plugins. New functionality can be added in controlled ways by adding dll assemblies that export plugin classes. The plugin framework uses MEF to dynamically discover plugins.

Expose your own API for plugins to insert their functionality into your web application. For example, the Demo base application exposes its menu system to plugins so they can add menu items into the site.

The framework comes with support for plugins to register widgets, which are MVC controller actions that return partial views that can be displayed in widget containers. Pages can easily display named widget containers, showing one or more widgets. This is very similar to WordPress widgets and sidebars.

The framework comes with a custom Razor view engine that can get razor views from plugin assemblies as embedded resources (http://support.microsoft.com/kb/319292).

The framework comes with support to dynamically add MVC controller action filters, along with some special support for compound action results so that a plugin can modify the results of a standard MVC action call. For example, a plugin could wrap the html from a partial result with additional html, or it could replace the output.

The Demo base application comes with a starter administrative plugin project that includes one admin page for seeing what plugins are loaded into the site. This will be expanded to allow plugins to be configured and enabled/disabled.

# Support #
The http://mvcplugins.org site has recently been created to show a list of all registered plugins for the MVC Plugin Framework as well as show off some of the features of the ASP.NET MVC Plugin Framework using Twitter Bootstrap and integrated with SharePoint using the SharePoint integration plugin.

Discussions for developers using this framework can be found at http://devinstruct.com/forums/forum/asp-net-mvc-plugin-framework/

# Building on the Work of Others #
There are many aspects of this framework that are built out of other ASP.NET MVC plugin frameworks I've come across. The incomplete list of other code this framework takes ideas from include:

http://fzysqr.com/2010/04/26/asp-net-mvc2-plugin-architecture-tutorial/

http://www.wynia.org/wordpress/2008/12/aspnet-mvc-plugins/

This project is a more complete framework for building production level applications and utilizes the latest features of ASP.NET, MVC, C#, etc.

Last edited Nov 13, 2013 at 3:28 AM by MattFromGA, version 15
