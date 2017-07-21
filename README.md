# auEduPerson

This repository is a minor update on the `auEduPerson` object class for LDAP. Included are schema files for OpenLDAP (`.schema`), and 389DS and RedHat Directory Server (`.ldif`).

# References

## auEduPerson definition

The `auEduPerson` object class is defined in [documentation](https://aaf.edu.au/media/2016/04/auEduPerson_attribute_vocabulary_v02-1-0.pdf) held by the [Australian Access Federation](https://aaf.edu.au/)

## auEduPerson schema file

This update is based on the schema file provided as a [download](http://wiki.aaf.edu.au/tech-info/aaf-downloads) from the [Australian Access Federation](https://aaf.edu.au/)

## Conversion script

The `ol-schema-migrate.pl` script is from the [389DS OpenLDAP migration documentation](http://directory.fedoraproject.org/docs/389ds/howto/howto-openldapmigration.html)

# Changes

## 20170721
- Removed quotes from around syntax definitions
- Removed `objectIdentifier` variables and explicitly state OIDs for classes and attributes
- Copied descriptions into DESC fields
- Replaced ' with \` in descriptions as they can't be escaped
- Put [DEPRECIATED] into description of depreciated attributes
- Created `.ldif` schema definition using `ol-schema-migrate.pl` script
