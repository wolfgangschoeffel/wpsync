wpsync
======

A bash script for synchronizing wordpress over ssh

Use with caution and at your own risk.



# Installation

## Make it executable:

    chmod +x /path/to/wpsync/wpsync

## Make it globally available:
  
    ln -s /path/to/wpsync/wpsync /usr/local/bin/wpsync

# Usage
    
Copy the configuration file ```wpsync-config-example.sh``` to your wordpess installation’s folder and rename it to ```wpsync-config.sh```

Edit it in your favorite text editor.

The script assumes that you already have ssh access to the remote server through using your ssh keys.

# Changelog
v.0.0.1
