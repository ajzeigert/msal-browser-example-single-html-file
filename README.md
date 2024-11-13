# msal-browser example in a single html file

This repository is essentially a clone of [this example](https://github.com/AzureAD/microsoft-authentication-library-for-js/tree/dev/samples/msal-browser-samples/VanillaJSTestApp2.0/app/default) from the main Microsoft Authentication Library for JS repository.

The difference is that all of the javascript has been moved to a single inline module script tag. I created this because there have been occasions where I've wanted to embed small Graph apps into a larger CMS, and referencing external file includes in that context can be a pain. You should be able to paste this HTML into any CMS that allows it and it should function as expected, assuming the CMS doesn't strip out `script` and `link` tags.

So, this exists now, mostly for my own use. It's stripped down to the bone. In fact, it doesn't even had a `head` tag, everything is contained in `body`. 

One major note is that you will need to update `clientId` and `authority` in the `msalConfig` object with ones created in a new Application in Azure EntraID.
