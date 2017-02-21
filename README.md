# postgres-automated-backup
Scripts that backups all databases in a cluster individually, optionally only backing up the schema for a set list. This also provides the option of specifying which databases you only want the schema of. The idea is to run these in a nightly cron job.

1. pg_backup.config - The main configuration file. This should be the only file which needs user modifications.
2. pg_backup.sh - The normal backup script which will go through each database and save a gzipped and/or a custom format copy of the backup into a date-based directory.
3. pg_backup_rotated.sh - The same as above except it will delete expired backups based on the configuration.

[Automated Backup on Linux](https://wiki.postgresql.org/wiki/Automated_Backup_on_Linux)
