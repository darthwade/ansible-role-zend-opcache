# Ansible Role: Zend OpCache
[![Build Status](https://travis-ci.org/darthwade/ansible-role-zend-opcache.png)](https://travis-ci.org/darthwade/ansible-role-zend-opcache)
[![Gittip](http://img.shields.io/gittip/darthwade.svg)](https://www.gittip.com/darthwade/)

Ansible role that installs & configures Zend OpCache.

Features include:
- Installation of Zend OpCache and it's dependencies
- Automatic configuration

## Installation

Using `ansible-galaxy`:
```shell 
$ ansible-galaxy install darthwade.zend-opcache
```

Using `arm` ([Ansible Role Manager](https://github.com/mirskytech/ansible-role-manager/)):
```shell 
$ arm install darthwade.zend-opcache
```

Using `git`:
```shell 
$ git clone https://github.com/darthwade/ansible-role-zend-opcache.git
```

## Requirements & Dependencies
- Ansible 1.4 or higher
- PHP
- PHP PECL (darthwade.php-pecl)

## Variables
Here is a list of all the default variables for this role, which are also available in `defaults/main.yml`.

```yaml
opcache_version: 7.0.3
opcache_memory_consumption: 128
opcache_interned_strings_buffer: 8
opcache_max_accelerated_files: 4000
opcache_revalidate_freq: 60
opcache_fast_shutdown: 1
opcache_enable_cli: 1
opcache_save_comments: 0
```

## Example playbook
```yaml
- hosts: all
  vars:
    opcache_version: 7.0.2
  roles:
    - darthwade.zend-opcache
```

## Testing
```shell 
$ git clone https://github.com/darthwade/ansible-role-zend-opcache.git
$ cd ansible-role-zend-opcache
$ vagrant up
```

## Contributing
In lieu of a formal styleguide, take care to maintain the existing coding style. Add unit tests and examples for any new or changed functionality.

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request

## License

Licensed under the MIT License. See the LICENSE file for details.

Copyright (c) 2014 [Vadym Petrychenko](http://petrychenko.com/)