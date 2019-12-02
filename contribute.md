---
title: How to Contribute to RageQuit.tips
subtitle: Share your resources or your story and help others deal with burnout.
img_path: /images/burntout3.png
menus:
  main:
    title: Contribute
    weight: 4
layout: page
---

RageQuit.tips was designed to be a resource for the community maintained by the community. Thus, anyone can contribute to the site. The only thing required to contribute is a [GitHub account](https://github.com/), but no knowledge of git or GitHub is required.

There are multiple ways to contribute. We give you full access to the CMS via GitHub authentication. You can click the "authenticate" button below and authenticate with GitHub by using an existing account or creating a new one.

<p><a href="#" id="login" class="button">Authenticate</a></p>

You will be asked to give permissions to the site as shown below.

![Authenticate with GitHub](/images/GitHub_authenticate_sm.png)

This will allow you access to the [CMS admin](/admin/) where you can make additions or changes to the content of the site. This uses a feature in our CMS called "open authoring". Changes via GitHub are processed as what GitHub calls a "fork" that awaits approval before being accepted into the site.

![GitHub fork](/images/GitHub_fork_sm.png)

For more details on the technologies running the site, see [the technical details](#the-technical-details) below. If you are having issues with contributing, email [brian@stackbit.com](mailto:brian@stackbit.com)

## Adding Resources

## Adding a Blog Post

## The Technical Details

This site was built using the following technologies:
* [Stackbit](https://www.stackbit.com/) - Stackbit allowed the site and CMS to be easily generated using a theme, which was later customized to meet our specific needs.
* [Jekyll](https://jekyllrb.com/) - The underlying site uses Jekyll as its static site generator. This was chosen to make contributions easier as it is one of the most widely known static site generators.
* [Netlify CMS](https://www.netlifycms.org/) - This is an open source, git-based CMS. This was chosen to take advantage of the [open authoring](https://www.netlifycms.org/docs/open-authoring) feature, which is currently available in the beta release.
* [Netlify](https://www.netlify.com/) - Netlify is used to deploy and host the site, but also maintains the hooks needed to authenticate into the CMS via GitHub.
* [GitHub](https://github.com) - GitHub manages the repository that contains the site code and content. It also enables the authentication that is managed via Netlify.

You can submit issues or changes via our [GitHub repository](https://github.com/remotesynth/ragequit-tips).