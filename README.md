## MicroHams WordPress deployment
### Topology
The current [Microhams site](http://microhams.com) is hosted on[ WindowsAzure](https://portal.azure.com):
  * WordPress app is hosted in a Azure AppService with PHP 5.6 and IIS enabled
  * MySql DB is hosted as ClearDB instance via Azure portal
  * media files (images, docs, videos etc.) are stored in a Azure Storage account, using the [Azure Storage WP plugin](https://wordpress.org/support/plugin/windows-azure-storage)

### Deployment
Updates to WP or its plugins should happen via this git repo. Once changes are pushed to this [github repo](https://github.com/microhams/microhams-wp),
the Azure AppService will pull the latest changes and refresh the running AppService.

The wp-config.php is for obvious reasons NOT part of this repo.
