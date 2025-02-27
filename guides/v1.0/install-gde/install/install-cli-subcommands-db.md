---
layout: default
group: install 
subgroup: T_Command-line installation
title: Create the Magento database schema
menu_title: Create the Magento database schema
menu_node: 
menu_order: 15
github_link: install-gde/install/install-cli-subcommands-db.md
---

  
<h4>Contents</h4>

See one of the following sections:

*	<a href="#instgde-install-cli-first">First steps</a>
*	<a href="#instgde-cli-subcommands-store-prereq">Prerequisites</a>
*	<a href="#instgde-cli-dbconfig">Configure the database and add data</a>


<h2 id="instgde-cli-before">First steps</h2>
{% include install/first-steps-cli.html %}

<h2 id="instgde-cli-subcommands-db-prereq">Prerequisites</h2>
Before you run this command, you must <a href="{{ site.gdeurl }}install-gde/install/install-cli-subcommands-deployment.html">Create or update the deployment configuration, config.php</a>.

<h2 id="instgde-cli-dbconfig">Configure the database and add data</h2>
Command usage:

	php magento setup:db-schema:upgrade
	php magento setup:db-data:upgrade

To see the status of the database, enter

	php magento setup:db:status

#### Related topics

*	<a href="{{ site.gdeurl }}install-gde/install/install-cli-install.html">Installing the Magento software using the command line</a>
*	<a href="{{ site.gdeurl }}install-gde/install/install-cli-subcommands-enable.html">Enable or disable modules</a>
*	<a href="{{ site.gdeurl }}install-gde/install/install-cli-subcommands-maint.html">Enable or disable maintenance mode</a>
*	<a href="{{ site.gdeurl }}install-gde/install/install-cli-subcommands-deployment.html">Create the deployment configuration, config.php</a>
*	<a href="{{ site.gdeurl }}install-gde/install/install-cli-subcommands-admin.html">Create a Magento administrator</a>
*	<a href="{{ site.gdeurl }}install-gde/install/install-cli-subcommands-store.html">Configure the store</a>
*	<a href="{{ site.gdeurl }}install-gde/install/install-cli-uninstall.html#instgde-install-uninstall">Uninstall the Magento software</a>
*	<a href="{{ site.gdeurl }}install-gde/install/install-cli-uninstall.html#instgde-install-magento-update">Update the Magento software</a>
*	<a href="{{ site.gdeurl }}install-gde/install/install-cli-uninstall.html#instgde-install-magento-reinstall">Reinstall the Magento software</a>