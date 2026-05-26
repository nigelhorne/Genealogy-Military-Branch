# Genealogy::Military::Branch

Extract and identify the military branch from a free-text string describing
a person's military service.

## Synopsis

```perl
use Genealogy::Military::Branch;

my $detector = Genealogy::Military::Branch->new();

my $branch = $detector->detect(
    text => 'He served in the Royal Navy from 1914 to 1918',
);
# Returns 'navy'

my $branch = $detector->detect(
    text => 'Served with the RAF in Bomber Command',
);
# Returns 'RAF'

my $branch = $detector->detect(
    text => 'Some unrelated text',
);
# Returns 'military'
```

## Description

Scans free-text military service notes from genealogy records and returns
the name of the branch.  Designed to replace the `service()` helper in the
`gedcom` and `ged2site` distributions.

The returned string is localised to the system locale (English, French, and
German supported).

## Author

Nigel Horne `<njh@bandsman.co.uk>`

## Licence

GPL2
