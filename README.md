Quell Plugin Starter Kit

Quell plugins are completely independent Angular applications that can be included at runtime into any Quell based application. Any plugin can be added without modifying Quell core and/or host application that the plugin will be used. This enables development of plugins that extend Quell independent of the core platform itself. Plugin authors deploy plugins on CDNs to publish publically. Once published any Quell publisher can add plugins at runtime in the browser when building pages without changing any code.

The best way to udnerstand this is to checkout the below demo.

* https://demo.carbonfreed.app/tractorbeam-test-v3
* https://demo.carbonfreed.app/tractorbeam-test-v3/manage

The mfe1 download pane is provided by a completely separate Angular application. This is done by adding the plugin using using a context. Once a module context is added the plugins supplied by that application become available to use in the Quell editor.

<img width="1440" alt="Screen Shot 2023-06-15 at 4 11 53 AM" src="https://github.com/rollthecloudinc/quell-plugin/assets/73197190/fa6e348a-4b69-4f01-a31d-360c4ba616cd">

<img width="1440" alt="Screen Shot 2023-06-15 at 4 14 03 AM" src="https://github.com/rollthecloudinc/quell-plugin/assets/73197190/7a765f97-3730-4543-899a-3d795e605654">

## Plugin Workflow

Onboarding workflow for dev to get up and running creating quell plugins working specifically on extending core without needing to modify quell core code, minimal understanding of core.

1. Running spearhead
1. Creating Plugins
1. Invoking plugin

## Running Spearhead

[spearhead](https://github.com/rollthecloudinc/spearhead) is the designated app starter kit for easily running Quell. Spearhead doesn’t maintain any Quell core libraries. Instead the latest releases are pulled down from GitHub as packages when installing the node packages using npm install. Spearhead is supped up Angular starter kit with all magic of Quell already wired up. Spearhead can be treated like any other Angular project once cloned.

## Creating Plugins

Similar in nature to spearhead plugin is the app starter kit for creating a Quell extension. An extension is any Webpack 5 micro frontend compatible with [module federation](https://webpack.js.org/concepts/module-federation/). Angular is the official framework of Quell therefore the plugin starter kit is configured to work with Angular. In the future there will be spell starters for specific frameworks like quell-plugin-react, quell-plugin-vue, quell-plugin-ts, etc.

## Invoking Plugin

Using a plugin inside Quell is known as *plugin invocation*. This process involves loading the plugin as a *context* into the [Quell editor](https://demo.druidcloud.io/pages/create-panel-page). Once complete the plugin has been innvocated and all plugins within the plugin module accessible from the the Quell shell / editor. In this way plugins are not your typical micro frontend. Plugins don’t typically have a default ui. Instead they define plugin implantations which provides the piping needed to extend core without ever touching Quell core code.

The context system is a pivotal part of Quell and loosely based on the [Drupal context system](https://www.drupal.org/project/context). More detail will be provided in future docs.

