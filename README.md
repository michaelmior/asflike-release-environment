ASF-like release environment
============================

Apache Software Foundation [release process](http://www.apache.org/dev/release-publishing.html)
requires staging and publishing the artifacts via SVN.

Unfortunately, there's no test instances for SVN, Git, Nexus, and usage of production instances
for testing purposes might cause non-intended releases.

The purpose of the current Vagrant script is to create throwaway services for testing purposes.


Usage
-----

1. Install [Docker](https://www.docker.com/)
1. Install [Vagrant](https://www.vagrantup.com/)
1. Boot the services: `vagrant up`
1. Shut down docker images: `vagrant destroy`

URLs
----

Note: Docker uses IPv4, so `localhost` might not work.

Login: `test`, password: `test`

* SVN web: http://127.0.0.1/svn
* SVN: svn://127.0.0.1:3960
* Nexus: not implemented. Nexus OSS does not support staging which is crucial since ASF Nexus requires staging.
* Git: not implemented. [Gogs](https://hub.docker.com/r/gogs/gogs) would likely suit.

License
-------

Apache License 2.0

Changelog
---------

2019-04-16
* SVN repository

Author
------

Vladimir Sitnikov <sitnikov.vladimir@gmail.com>
