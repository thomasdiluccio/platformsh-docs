---
title: "Configure Spring for {{< vendor/name >}}"
sidebarTitle: "Configure"
weight: -100
description: |
    Review the basics of what makes up a {{< vendor/name >}} project, including its three principle configuration files and how to define them for Spring.
---

{{% guides/config-desc name="Spring" noService=true %}}

{{% guides/config-app template="spring-mvc-maven-mongodb" %}}
Explaining the file line by line, notice the following settings:

1. `name`: The application name.
2. `type` Where you define the language, in this case, Java, and the version.
3. `disk`: The disk space that the application needs in megabytes.
4. `hooks.build`: The command to package the application.
5. `web.commands`: The order to start the application, where the port is overwritten with `--server.port=$PORT`,
   using the `PORT` environment variable provided by {{< vendor/name >}} to the application container.

{{< /guides/config-app >}}

{{% guides/config-service name=Spring noService=true /%}}

{{% guides/config-routes template="spring-mvc-maven-mongodb" name="Spring" %}}

{{< guide-buttons next="Customize Spring" >}}
