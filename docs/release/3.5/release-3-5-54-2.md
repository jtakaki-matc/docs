!!! failure "OSG 3.5 end-of-life"
    The OSG 3.5 end-of-life date was May 1, 2022 per our
    [release policy](https://osg-htc.org/technology/policy/release-series/).
    We recommend
    [updating to OSG 3.6](../updating-to-osg-36.md)
    at your earliest convenience.

OSG Data Release 3.5.54-2
=========================

**Release Date:** 2022-01-27    
**Supported OS Versions:** EL7, EL8

!!!tip "Want faster access to production-ready software?"
    OSG 3.5 offers a rolling release repository where packages are added as soon as they pass acceptance testing.
    To install packages from this repository, enable `[osg-rolling]` in `/etc/yum.repos.d/osg-rolling.repo`:

        [osg-rolling]
        ...
        enabled=1

    Or for one-time installations, append the following to your `yum` command:

        --enablerepo=osg-rolling

Summary of Changes
------------------

-   [VO Package v117](https://github.com/opensciencegrid/osg-vo-config/releases/tag/release-117)
    -   Update GlueX DN
    -   Update hcc-voms2 DN
    -   Add ATLAS IAM vomses entry
-   osg-scitokens-mapfile 5
    -   Add default SciTokens mappings for the FNAL VOs


These [JIRA tickets](https://opensciencegrid.atlassian.net/issues/?jql=project%20%3D%20SOFTWARE%20AND%20fixVersion%20%3D%203.5.54-2%20ORDER%20BY%20priority%20DESC%2C%20key%20DESC) were addressed in this release.

Containers
----------

The [OSG Docker images](https://hub.docker.com/u/opensciencegrid/) have been updated to contain the latest CA certificates.

Updating to the New Release
---------------------------

To update to the OSG 3.5 series from an earlier release series, please consult the page on
[updating between release series](../updating-to-osg-35.md).

For sites using non-RPM worker node client installations, new [tarballs](../../worker-node/install-wn-tarball.md) and
[container images](../../worker-node/using-wn-containers.md) are available:

- Tarball: <https://repo.opensciencegrid.org/tarball-install/3.5/osg-wn-client-latest.el7.x86_64.tar.gz>
- Container Images: <https://hub.docker.com/r/opensciencegrid/osg-wn/>

Need Help?
----------

Do you need help with this release? [Contact us for help](../../common/help.md).

Detailed Changes in This Release
--------------------------------

### Packages

We added or updated the following packages to the production OSG yum repository.
Note that in some cases, there are multiple RPMs for each package.
You can click on any given package to see the set of RPMs or see the complete list [below](#rpms).

#### Enterprise Linux 7

-   [osg-scitokens-mapfile-5-1.osg35.el7](https://koji.chtc.wisc.edu/koji/search?match=glob&type=build&terms=osg-scitokens-mapfile-5-1.osg35.el7)
-   [vo-client-117-1.osg35.el7](https://koji.chtc.wisc.edu/koji/search?match=glob&type=build&terms=vo-client-117-1.osg35.el7)

#### Enterprise Linux 8

-   [osg-scitokens-mapfile-5-1.osg35.el8](https://koji.chtc.wisc.edu/koji/search?match=glob&type=build&terms=osg-scitokens-mapfile-5-1.osg35.el8)
-   [vo-client-117-1.osg35.el8](https://koji.chtc.wisc.edu/koji/search?match=glob&type=build&terms=vo-client-117-1.osg35.el8)

### RPMs

If you wish to manually update your system, you can run yum update against the following packages:

    osg-scitokens-mapfile vo-client vo-client-dcache vo-client-lcmaps-voms 

If you wish to only update the RPMs that changed, the set of RPMs is:

#### Enterprise Linux 7

``` file
osg-scitokens-mapfile-5-1.osg35.el7
vo-client-117-1.osg35.el7
vo-client-dcache-117-1.osg35.el7
vo-client-lcmaps-voms-117-1.osg35.el7
```

#### Enterprise Linux 8

``` file
osg-scitokens-mapfile-5-1.osg35.el8
vo-client-117-1.osg35.el8
vo-client-dcache-117-1.osg35.el8
vo-client-lcmaps-voms-117-1.osg35.el8
```
