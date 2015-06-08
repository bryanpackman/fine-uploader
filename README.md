## Updating FineUploader

Behance maintains our own version of the FineUploader repo that contains built files so that it can be used as a proper bower dependency. In order to update to the latest FineUploader, or to generate a new build, perform the following steps:

1. Merge in latest changes from upstream.
1. run `grunt package`.
1. copy _build/all.fine-uploader.js to dist/all.fine-uploader.js
1. Ensure that Behance's custom changes are in place by grepping the code for comments starting with `BEHANCE:`.
1. Add AMD wrappers around the code to avoid having conflicting globals (this will soon be automated).

Future modifications to FineUploader should be done as pull requests against the behance/fine-uploader repo.