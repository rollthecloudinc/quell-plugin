Quell Plugin Starter Kit

Quell plugins are completely independent Angular applications that can be included at runtime into any Quell based application. Any plugin can be added without modifying Quell core and/or host application that the plugin will be used. This enables development of plugins that extend Quell independent of the core platform itself. Plugin authors deploy plugins on CDNs to publish publically. Once published any Quell publisher can add plugins at runtime in the browser when building pages without changing any code.

The best way to udnerstand this is to checkout the below demo.

* https://demo.carbonfreed.app/tractorbeam-test-v3
* https://demo.carbonfreed.app/tractorbeam-test-v3/manage

The mfe1 download pane is provided by a completely separate Angular application. This is done by adding the plugin using using a context. Once a module context is added the plugins supplied by that application become available to use in the Quell editor.

<img width="1440" alt="Screen Shot 2023-06-15 at 4 11 53 AM" src="https://github.com/rollthecloudinc/quell-plugin/assets/73197190/fa6e348a-4b69-4f01-a31d-360c4ba616cd">

<img width="1440" alt="Screen Shot 2023-06-15 at 4 14 03 AM" src="https://github.com/rollthecloudinc/quell-plugin/assets/73197190/7a765f97-3730-4543-899a-3d795e605654">
