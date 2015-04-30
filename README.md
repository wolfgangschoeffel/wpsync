wpsync
======

A bash script for synchronizing wordpress over ssh

Use with caution and at your own risk.

Do not add the configuration file to version control!



# Installation

## Make it executable:

    chmod +x /path/to/wpsync/wpsync

## Make it globally available:
  
    ln -s /path/to/wpsync/wpsync /usr/local/bin/wpsync

# Usage
    
Copy the configuration file ```config-sample``` to a folder called ```.wpsync``` and rename it to ```config```

Edit it in your favorite text editor.

The script assumes that you already have ssh access to the remote server through using your ssh keys.

## Available commands

    wpsync push_db
    wpsync pull_db
    wpsync push_files
    wpsync pull_files
    

# Changelog

## 0.0.2 (June 01, 2014)

* add some colors
* search and replace whole database
* move config file to a .wpsync folder where also the backup files will be stored
* add datetime to backup files

## 0.0.3 (April 30, 2015)

* add some new features:
    - replace database charset if ```l_db_charset``` and ```r_db_charset``` are provided. This is because wordpress changed their default database charset to ```utf8mb4``` instead of ```utf8```.
    - new commands: ```push_plugins``` and ```pull_plugins``` via rsync
* fix a small bug (functions were being executed even if they were not defined as allowed commands)
* make ```l_upload_dir``` and ```r_upload_dir``` optional. if they are not defined in the config file the standard ```wp-content/uploads``` will be used.
