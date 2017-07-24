# auEduPerson

This repository is a minor update on the `auEduPerson` object class for LDAP. Included are schema files for OpenLDAP (`.schema`), and 389DS and RedHat Directory Server (`.ldif`).

# References

## auEduPerson definition

The `auEduPerson` object class is defined in [documentation](https://aaf.edu.au/media/2016/04/auEduPerson_attribute_vocabulary_v02-1-0.pdf) held by the [Australian Access Federation](https://aaf.edu.au/)

## auEduPerson schema file

This update is based on the schema file provided as a [download](http://wiki.aaf.edu.au/tech-info/aaf-downloads) from the [Australian Access Federation](https://aaf.edu.au/)

## Conversion script

The `ol-schema-migrate.pl` script is from the [389DS OpenLDAP migration documentation](http://directory.fedoraproject.org/docs/389ds/howto/howto-openldapmigration.html)

## OID References from 20090820

The following is a list of OIDs defined in the 20090820 `auEduPerson.schema`, these `objectIdentifier` declarations were not handled by the `.ldif` conversion script and were removed in 20170721.

```
objectIdentifier CAUDITARC                  1.3.6.1.4.1.27856 # 1.3.6.1.4.1.27856
objectIdentifier AARNetARC                  1.3.6.1.4.1.8852  # 1.3.6.1.4.1.8852
objectIdentifier auEduPersonARC             CAUDITARC:1       # 1.3.6.1.4.1.27856.1
objectIdentifier auEduPersonObjectClassARC  auEduPersonARC:1  # 1.3.6.1.4.1.27856.1.1
objectIdentifier auEduPersonAttributeARC    auEduPersonARC:2  # 1.3.6.1.4.1.27856.1.2
objectIdentifier WALAPAttributeARC          AARNetARC:4.1.1   # 1.3.6.1.4.1.8852.4.1.1
objectIdentifier WALAPObjectClassARC        AARNetARC:4.1.2   # 1.3.6.1.4.1.8852.4.1.2
```

# Changes

## 20170721
- Removed quotes from around syntax definitions
- Removed `objectIdentifier` variables and explicitly state OIDs for classes and attributes
- Copied descriptions into DESC fields
- Replaced ' with \` in descriptions as they can't be escaped
- Put [DEPRECIATED] into description of depreciated attributes
- Created `.ldif` schema definition using `ol-schema-migrate.pl` script
