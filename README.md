<a href="https://moringaschool.com/">
    <img src="" alt="Moringa logo" title="Aimeos" align="right" height="60" />
</a>

# Aimeos TYPO3 extension

[![Total Downloads](https://poser.pugx.org/aimeos/aimeos-typo3/d/total.svg)](https://packagist.org/packages/aimeos/aimeos-typo3)
[![Scrutinizer Code Quality](https://scrutinizer-ci.com/g/aimeos/aimeos-typo3/badges/quality-score.png?b=master)](https://scrutinizer-ci.com/g/aimeos/aimeos-typo3/?branch=master)
[![License](https://poser.pugx.org/aimeos/aimeos-typo3/license.svg)](https://packagist.org/packages/aimeos/aimeos-typo3)

:star: Star us on GitHub — it motivates us a lot!

[Aimeos](https://aimeos.org/TYPO3) is THE professional, full-featured and
high performance e-commerce extension for TYPO3!  You can install it in your
existing TYPO3 web site within 5 minutes and can adapt, extend, overwrite
and customize anything to your needs.

[![Aimeos TYPO3 demo](https://aimeos.org/fileadmin/user_upload/typo3-demo.jpg)](http://typo3.demo.aimeos.org/)

## Table of content

- [Installation](#installation)
    - [TER](#typo3-extension-repository)
    - [Composer](#composer)
- [TYPO3 setup](#typo3-setup)
    - [Extension](#extension)
    - [Database](#database)
- [Page setup](#page-setup)
    - [Upload the page tree file](#upload-the-page-tree-file)
    - [Go to the import view](#go-to-the-import-view)
    - [Import the page tree](#import-the-page-tree)
    - [SEO-friendly URLs](#seo-friendly-urls)
- [License](#license)
- [Links](#links)

## Installation

 **This Document has been created for angular FAQs and Error debugging**.



### Composer

**Note:** composer 2.1+ is required!

The latest version can be installed via composer too. This is especially useful if you want to create new TYPO3 installations automatically or play with the latest code. You need to install the composer package first if it isn't already available:

`php -r "readfile('https://getcomposer.org/installer');" | php -- --filename=composer`

In order to tell install TYPO3, you have to execute

`composer create-project typo3/cms-base-distribution myshop`

This will install TYPO3 into the `./myshop/` directory.

Then, change to the `./mshop/` directory and install the Aimeos extension for TYPO3 with:

`composer req aimeos/aimeos-typo3:~21.10`

This will install stable TYPO3 version and the latest Aimeos TYPO3 extension. If you want a more or less working installation out of the box for new installations, you should install the Bootstrap package too:

`composer req bk2k/bootstrap-package`


```
'DB' => [
    'Connections' => [
        'Default' => [
            'tableoptions' => [
                'charset' => 'utf8',
                'collate' => 'utf8_unicode_ci',
            ],
            // ...
        ],
    ],
],
```



#### TYPO3 11

When using TYPO3 11, you have to run these commands from your installation directory:

```bash
php ./vendor/bin/typo3 extension:setup
php ./vendor/bin/typo3 aimeos:setup --option=setup/default/demo:1
```

If you don't want to add the Aimeos demo data, you should remove `--option=setup/default/demo:1` from the Aimeos setup command.



### TER Extension


![Install Aimeos TYPO3 extension](https://aimeos.org/docs/images/Aimeos-typo3-extmngr-install.png)

Afterwards, you have to execute the update script of the extension to create the required database structure:

![Execute update script](https://aimeos.org/docs/images/Aimeos-typo3-extmngr-update-7.x.png)



## Page setup

The page setup for an Aimeos web shop is easy if you import the example page tree for TYPO3 10/11:

* [21.10+ page tree](https://aimeos.org/fileadmin/download/Aimeos-pages_21.10.t3d) only

**Note:** The Aimeos layout expects [Bootstrap](https://getbootstrap.com) providing the grid layout!




## License

The FAQs extension is licensed under the terms of the GPL Open Source
license and is available for free.

## Links

* [Web site]
* [Documentation]
* [Forum]
* [Issue tracker]
* [Source code]
