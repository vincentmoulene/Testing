Changelog
=========

3.0.0 (unreleased)
------------------

* **2019-07-26**: [BC-BREAK] Remove deprecated `BaseTestCase::getClient`, use `BaseTestCase::getFrameworkBundleClient` instead.
* **2019-02-28**: [BC-BREAK] Remove `DatabaseTestListener`, use scripts in `bin/make/` to ramp up your testing environment for several test suites
* **2019-02-28**: [BC-BREAK] Introduce PHPUnit 6 Support, Remove PHPUnit 5.7.
* **2019-02-28**: Add testing scenarios for Symfony 4.2 and 4.3 (allowed to fail for now)

2.1.12
------

* **2019-07-26**: Work around name collision with Symfony 4.3.
  `BaseTestCase::getClient` is deprecated, use `BaseTestCase::getFrameworkBundleClient` instead.

2.1.0
-----

* **2017-01-18**: Introduce a `TestCompilePass` to make services public, which are needed 
in i.e. a WebTest.
 * **2017-11-08**: Removed php 5.6 and 7.0 support, removed Symfony 3.0.* and 3.1.* support
 introduce KERNEL_CLASS handling to avoid deprecated KERNEL_DIR, removed usage of `ProcessBuilder`

2.0.1
-----

 * **2018-01-02**: Remove dependency on symfony/symfony in favor of more specific packages. Its a
   bug of the package using testing if it does not declare its dependencies.

2.0.0
-----

2.0.0-RC2
---------

 * **2017-01-25**: Added WebServerBundle support
 * **2017-01-25**: Dropped PHP <5.6 support

2.0.0-RC1
---------

 * **2016-06-21**: [BC BREAK] Deleted the `sonata_admin` bundle set
 * **2016-06-21**: [BC BREAK] Deleted the `LoadBaseData` data fixtures
 * **2016-06-21**: [BC BREAK] Deleted the `Content` document
 * **2016-06-21**: [BC BREAK] Dropped PHP <5.5 support
 * **2016-06-21**: [BC BREAK] Dropped Symfony <2.8 support

1.3.0
-----

1.3.0-RC1
---------

* **2015-10-17**: Symfony 3 is supported
* **2015-10-17**: [BC Break] `resources/config/dist/framework.yml` has been
                  renamed to `resources/config/dist/framework.php`
* **2015-04-26**: Added `BaseTestCase::assertResponseSuccess()` to provide
                  helpfull output in case the response errored
* **2015-04-19**: The package now requires `symfony/phpunit-bridge`
* **2015-01-18**: Added required `--force` for the `doctrine:phpcr:init:dbal`
                  command to support Jackalope 1.2

1.2.0-RC2
---------

* **2014-10-06**: Added purgeDatabase method to ORM manager

1.2.0-RC1
---------

* **2014-07-27**: Added DataFixture support to the ORM DbManager
* **2014-06-16**: Initializer for phpcr fixture loading
* **2014-06-06**: Updated to PSR-4 autoloading

1.1.0-RC2
---------

* **2014-06-11**: fetch manager by its name
* **2014-04-24**: [DEPRECATE] Deprecated the `sonata_admin` bundle set
* **2014-04-24**: added bundle sets: `sonata_admin_orm` and `sonata_admin_phpcr`
* **2014-04-11**: dropped Symfony 2.2 compatibility

1.1.0-RC1
---------

* **2013-04-07**: [DEPRECATE] Deprecated `LoadBaseData` DataFixture, it will be removed in 2.0
* **2013-04-02**: [DEPRECATE] Deprecated `Content` document, it will be removed in 2.0
* **2013-12-27**: Added `XmlSchemaTestCase` to test XML schema's
* **2013-11-17**: Added `DatabaseTestListener` to support database testing
