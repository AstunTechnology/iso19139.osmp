# Ordnance Survey Extended Metadata Profile schema plugin

Ordnance Survey Metadata Profile

## GeoNetwork versions to use with this plugin

**Use the correct branch for your version of GeoNetwork. This is for GeoNetwork 4.2.**

## Installing the plugin in GeoNetwork 4.2.x

### Adding to an existing installation

 * Download or clone this repository, ensuring you choose the correct branch. 
 * Copy `src/main/plugin/iso19139.osmp` to `INSTALL_DIR/geonetwork/WEB_INF/data/config/schema_plugins/iso19139.osmp` in your installation.
 * Copy `target/schema-iso19139.osmp-3.7.jar` to `INSTALL_DIR/geonetwork/WEB_INF/lib`
 * Restart GeoNetwork
 * Check that the schema is registered by visiting Admin Console -> Metadata and Templates -> Standards in GeoNetwork. If you do not see iso19139.osmp then it is not correctly deployed. Check your GeoNetwork log files for errors.

### Adding the plugin to the source code prior to compiling GeoNetwork

The best approach is to add the plugin as a submodule. Use https://github.com/geonetwork/core-geonetwork/blob/main/add-schema.sh for automatic deployment (change to use the correct branch):

```
./add-schema.sh iso19139.osmp http://github.com/astuntechnology/iso19139.osmp 4.2.x
```

#### Building the application 

See https://geonetwork-opensource.org/manuals/trunk/en/maintainer-guide/installing/installing-from-source-code.html. 

Once the application is built `web/target/geonetwork.war` will contain GeoNetwork with the OSMP schema plugin included.