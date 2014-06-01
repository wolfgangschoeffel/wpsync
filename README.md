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
    
Copy the configuration file ```config-sample``` to a folder called ```.wpsync`` and rename it to ```config```

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
