# External Services for Open Neuroscience

There is a growing number of websites/portals which provide *services* for data which is provided from external URLs.

Some times they are just client-side (in browser) JavaScript libraries which would download those files to your local computer.
The other times they might be some cloud services providing powerful frameworks.
In any of those cases, for portals which host or just know about locations of the files, and where CORR configuration of the web-server explicitly allows for those websites to access the data, it opens great opportunities or integrations.
Two first such services which became known to us were https://bioimagesuiteweb.github.io and http://nwbexplorer.opensourcebrain.org.
Both were "integrated" within https://dandiarchive.org and https://datasets.datalad.org so for files which are hosted on those archives (datasets.datalad.org hosts only few), it is possible to view them on those external services.

Example: visit https://datasets.datalad.org/?dir=/dbic/QA/sub-emmet/ses-20180531/anat, hover over .nii.gz file and click on `⠇` to be provided with a URL to view that file on bioimagesuiteweb. Similar functionality is available for .nwb and .nii.gz files on https://dandiarchive.org.

## Purpose of this project

Provide a centralized registry of such services, so external projects (such as datasets.datalad.org and dandiarchive.org) could just use that registry instead of hardcoding and maintaining their own listing.

## Example uses

So far this registry is not yet used directly anywhere, but here are the locations where it was explicitly "embedded" in aforementioned two sample projects:

- **datasets.datalad.org**: part of the (deprecated) DataLad Web UI within [datalad-deprecated](https://github.com/datalad/datalad-deprecated/blob/9a4c33867b7034e1ec75f913c9196e3cc4ffb27c/datalad_deprecated/resources/website/assets/js/main.js#L21)
- **dandiarchive.org**: [datalad-archive](https://github.com/dandi/dandi-archive/blob/HEAD/web/src/views/FileBrowserView/FileBrowser.vue#L244)

# Contributing

Please suggest additional services by adding them to [registry.yaml](./registry.yaml) file and submitting Pull Requests.

# References

- [some extra additional initial thoughts](https://github.com/dandi/dandiarchive-legacy/wiki/WiP:-dump-of-thoughts-on-%22services-registry%22)