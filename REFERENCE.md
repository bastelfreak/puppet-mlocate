# Reference
<!-- DO NOT EDIT: This document was generated by Puppet Strings -->

## Table of Contents

**Classes**

_Public Classes_

* [`mlocate`](#mlocate): mlocate class , install and configure mlocate

_Private Classes_

* `mlocate::config`: This class handles configuration of mlocate
* `mlocate::install`: This class handles installation of mlocate

## Classes

### mlocate

mlocate class , install and configure mlocate

#### Examples

##### 

```puppet
class{'mlocate':
  prunepaths   => ['/afs', '/mnt' ],
  prunefs      => ['afs', 'fuse'],
  prunenames   => ['.cache', '.git'],
  period       => weekly,
  force_update => true,
}
```

#### Parameters

The following parameters are available in the `mlocate` class.

##### `ensure`

Data type: `Boolean`

Install mlocate or remove mlocate

Default value: `true`

##### `prunefs`

Data type: `Array[String[1]]`

List of filesystem types to ignore

Default value: []

##### `prune_bind_mounts`

Data type: `Boolean`

Should bind mounts be searched?

Default value: `true`

##### `prunepaths`

Data type: `Array[Stdlib::Unixpath]`

List of file systems paths not to search

Default value: []

##### `prunenames`

Data type: `Array[String[1]]`

List of directory or files names to match adn not include.

Default value: []

##### `period`

Data type: `Enum['infinite','daily','weekly','monthly']`

Should the update interval be daily, weekly, monthly or infinite.

Default value: 'daily'

##### `package_cron`

Data type: `Optional[Stdlib::Unixpath]`

Path to a cron file entry to be purged.

Default value: `undef`

##### `fore_updatedb`

Should puppet run updatedb if no database already exists.

##### `force_updatedb`

Data type: `Boolean`



Default value: `false`
