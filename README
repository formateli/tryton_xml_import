tryton_xml_import
=================

A python command line utility that allows to import
data from xml files to a tryton database.

The main goal is to import data using xml files that are formed
using the tryton definition schema, but with following considerations:

- The attribute 'id' value of 'record' element will not be stored in the database,
so, once imported, you can manipulate the record in tryton client without
problem, avoiding the 'You are not allowed to modify this record.
This record is part of the base configuration.' editing error.

- The 'id' attribute of 'record' element can be ommited.
It is only necesarry if the record is referenced by
any other 'record' in same file or any other file in
current import operation.

- Records are always created (even if the id is already present in database),
so be aware that if you run the script more than once, records will be
duplicated in database. YOU ARE ADVISED!

- Any attribute in 'data' element is ignored.

- Take care with user wich is importing the data, 'admin'
user is a smart election because is not associated with any company,
so property fields will have general values for all companies.

- 'search' and 'pyson' attribute are not implemented at the moment.


Usage
-----

From console you can run the application with specific parameters:

For help::

    tryton_xml_import -h

Import party.xml and product.xml in a 'test_database' using 'admin' user:

    tryton_xml_import party.xml product.xml -d test_database -u admin -c TRYTON_PATH/tryton.cfg

Options:
  -h, --help        show help message and exit
  -v, --version     Show version
  -u user           The Tryton user. Required.
  -c config         The Tryton configuration file. Required.
  -d database       The Tryton database name. Required.
  -t tryton_path    The Tryton package path. Uses the installed one if ignored.
  -x xml_directory  Directory where xml files are located. Default: Application directory.


License
-------

See LICENSE

Copyright
---------

See COPYRIGHT
