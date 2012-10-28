openstreetmap-changeset-replication
===================================

Simple Ruby script to replicate changes to changeset metadata to a stream.

The replicator needs two YAML files:

* a configuration file, to be passed as a command line argument.
* a state file, which can be empty the first time it's used.

The configuration file should look like:

 state_file: state.yaml
 db: host=localhost dbname=openstreetmap user=openstreetmap password=XXXXX
 data_dir: replication/

Replicated files will be created under the `data_dir` directory as gzipped `.osm` files.
