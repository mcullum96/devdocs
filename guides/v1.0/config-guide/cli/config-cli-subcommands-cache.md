---
layout: default
group: config-guide 
subgroup: CLI
title: Manage the cache
menu_title: Manage the cache
menu_node: 
menu_order: 5
github_link: config-guide/cli/config-cli-subcommands-cache.md
---


#### Contents

*	<a href="#config-cli-before">First steps</a>
*	<a href="#config-cli-subcommands-cache-status">View the cache status</a>
*	<a href="#config-cli-subcommands-cache-en">Enable or disable the cache</a> 
*	<a href="#config-cli-subcommands-cache-clean">Clean and flush cache types</a>

<h2 id="config-cli-before">First steps</h2>
{% include install/first-steps-cli.html %}

<!-- <h2 id="config-cli-subcommands-cache-clean">Overview of cache types</h2> -->

<h2 id="config-cli-subcommands-cache-status">View the cache status</h2>
To view the status of the cache, enter

	php magento cache:status [--bootstrap="<url-encoded array>"]

where `--bootstrap=` is a URL-encoded associative array of Magento <a href="{{ site.gdeurl }}config-guide/bootstrap/magento-how-to-set.html#config-bootparam-overview">application bootstrap parameters</a> and values.

A sample follows:

                        config: 1
                        layout: 1
                    block_html: 1
           view_files_fallback: 1
      view_files_preprocessing: 1
                   collections: 1
                        db_ddl: 1
                           eav: 1
                     full_page: 1
                     translate: 1
            config_integration: 1
        config_integration_api: 1
             config_webservice: 1

<h2 id="config-cli-subcommands-cache-en">Enable or disable cache types</h2>
This command enables you to enable or disable all cache types or only the ones you specify. Disabling cache types is useful during development because you see the results of your changes without having to flush the cache; however, disabling cache types has an adverse affect on performance.

Command options:

	php magento cache:enable [--all] [--bootstrap="<url-encoded array>"] [type] ... [type]
	php magento cache:disable [--all] [--bootstrap="<url-encoded array>"] [type] ... [type]

where

`--all` enables or disables all cache types at the same time.

`type` is a space-separated list of cache types.

`--bootstrap=` is a URL-encoded associative array of Magento <a href="{{ site.gdeurl }}config-guide/bootstrap/magento-how-to-set.html#config-bootparam-overview">application bootstrap parameters</a> and values.

To list cache types and their status, enter

	php magento cache:status

For example, to disable the full page cache and the DDL cache, enter 

	php magento cache:disable db_ddl full_page

Sample result:

	Changed cache status:	
                        db_ddl: 1 -> 0
                     full_page: 1 -> 0

<div class="bs-callout bs-callout-info" id="info">
<span class="glyphicon-class">
  <p>Enabling a cache type automatically clears that cache type.</p></span>
</div> 

<h2 id="config-cli-subcommands-cache-clean">Clean and flush cache types</h2>
To purge out-of-date items from the cache, you can *clean* or *flush* cache types:

*	Cleaning a cache type deletes all items from enabled cache types only.

	Disabled cache types are not cleaned.

*	Flushing a cache type purges the cache storage.

	All cache types that use the specified storage are flushed.

Command usage:

	php magento cache:clean [--all] [--bootstrap="..."] [type] ... [type]
	php magento cache:flush [--all] [--bootstrap="..."] [type] ... [type]

where

`--all` cleans or flushes all cache types at the same time.

`type` is a space-separated list of cache types.

`--bootstrap=` is a URL-encoded associative array of Magento <a href="{{ site.gdeurl }}config-guide/bootstrap/magento-how-to-set.html#config-bootparam-overview">application bootstrap parameters</a> and values.

For example, to flush all cache types, enter

	php magento cache:flush --all

Sample result:

	Flushed cache types:
	config
	layout
	block_html
	view_files_fallback
	view_files_preprocessing
	collections
	db_ddl
	eav
	full_page
	translate
	config_integration
	config_integration_api
	config_webservice


#### Related topics

*	<a href="{{ site.gdeurl }}config-guide/cli/config-cli-subcommands-index.html">Manage the indexers</a>
*	<a href="{{ site.gdeurl }}config-guide/cli/config-cli-subcommands-compiler-multi.html">Multi-tenant compiler</a>
*	<a href="{{ site.gdeurl }}config-guide/cli/config-cli-subcommands-compiler-single.html">Single-tenant compiler</a>
*	<a href="{{ site.gdeurl }}config-guide/cli/config-cli-subcommands-log.html">Clean the logs</a>
*	<a href="{{ site.gdeurl }}config-guide/cli/config-cli-subcommands-i18n.html">Translation dictionaries and language packages</a>
*	<a href="{{ site.gdeurl }}config-guide/cli/config-cli-subcommands-static-view.html">Deploy static view files</a>
*	<a href="{{ site.gdeurl }}config-guide/cli/config-cli-subcommands-less-sass.html">Create LESS from CSS</a>
*	<a href="{{ site.gdeurl }}config-guide/cli/config-cli-subcommands-test.html">Run tests</a>