# LeoVegas Custom Plugin Repository

This is where we publish IntelliJ IDEA plugins developed by Leo Vegas.

To use this plugin repository;
- Navigate to `IntelliJ IDEA` -> `Preferences...` -> `Plugins` -> Gearwheel button ->
`Manage Plugin Respoitories...`. 
- Add the URL `https://github.com/gutro/idea-plugin-repository/raw/master/updatePlugins.xml`.
- Click `OK`.

You should now be able to find plugins from this repository in the `Marketplace` list.

The published plugins are;
- [JAX-RS To Spring MVC Converter](https://github.com/gutro/jaxrs-to-springmvc-converter)
- [TestNG To Junit 5 Converter](https://github.com/gutro/testng-to-junit5-converter)

## How to publish plugin

To publish a new version of an already published plugin, you need to;
 1. Build the plugin locally (using `./gradlew buildPlugin`).
 1. Create a new tag in your plugin repository.
 1. Copy the .jar from `build/lib/` to [`plugins`](plugins) in this repository.
 1. Update the entry in [`updatePlugins.xml`](updatePlugins.xml) with new file URL, 
 new version and possibly a new idea-version (the idea-version should be copied from 
 `build/patchedPluginXmlFiles/plugin.xml` in your plugin repository).
 1. Commit and push this repository.
