# BCMS: MySQL Optimization

BrowserCMS can use a little pep when it has a lot of data.  The best way to speed your performance is to add the appropriate indexes to the database tables.

## Steps to install

1. Copy the migration file under your *db/migrate* folder.
2. Run: *bundle exec rake db:migrate*

The indexes that this migration creates have been tested to show the best performance through the usage of the *EXPLAIN* function of MySQL.  Each query was analyzed and the indexes were formulated based on the most common queries that are executed within BrowserCMS. After setting up these indexes, my local copy of BrowerCMS sped up significantly.

## Note

The table definitions in this file do not account for any sort of namespacing.  Please adjust the migration as necessary to fit your table names.