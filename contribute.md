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

There are multiple ways to contribute. We give you full access to the CMS via GitHub authentication. You can go to the [CMS admin](/admin/) and click the "Login with GitHub" button to authenticate with GitHub by using an existing account or creating a new one. You will be asked to give permissions to the site as shown below.

![Authenticate with GitHub](/images/GitHub_authenticate_sm.png)

You will be asked to fork the repo. Click the "fork the repo" button to continue.

![GitHub fork](/images/GitHub_fork_sm.png)

This will allow you access to the [CMS admin](/admin/) where you can make additions or changes to the content of the site. This uses a feature in our CMS called "open authoring". Changes via GitHub are processed as what GitHub calls a "fork" that awaits approval before being accepted into the site.

For more details on the technologies running the site, see [the technical details](#the-technical-details) below. If you are having issues with contributing, email [brian@stackbit.com](mailto:brian@stackbit.com)

## Adding Resources

Our [resource section](/resources/) aims to be a one stop for information as well as links to articles, research, services and other information around the web related to burnout.

### Modifying Existing Pages

Every existing page within the resources section has an "edit this page" link at the bottom. Clicking this button will take you to the CMS to edit the contents of that specific page. If you are not already authenticated with GitHub as shown above, you will need to do so at this time.

Once you have made your edits, you will need to click the "save" button in the upper-left hand corner of the page.

![save your changes](/images/save_cms.png)

Once you have completed all of your changes, change the status of the content to "In Review" via the drop-down in the upper-right hand corner of the page.

![in review status](/images/in_review.png)

This will submit your changes to be reviewed and accepted into the site.

### Adding New Pages to Existing Sections

Every existing page within the resources sections has an "add a new page to this section" link at the bottom. Clicking this button will take you to the CMS to create a new page under that specific subsection of resources. If you are not already authenticated with GitHub as shown above, you will need to do so at this time.

Fill in all the required content and then click the "save" button.

![save your changes to a new page](/images/save_cms_newpage.png)

You can continue to make changes to the new page. When you are ready to submit your page for publishing, change the status of the content to "In Review" via the drop-down in the upper-right hand corner of the page.

![in review status](/images/in_review.png)

This will submit your changes to be reviewed and accepted into the site.

## Adding a Blog Post

All blog pages and posts have an "add your story to our blog" link at the bottom. Clicking this button will take you to the CMS to create a new post under the blog. If you are not already authenticated with GitHub as shown above, you will need to do so at this time.

Fill in all the required content and then click the "save" button.

![save your changes to a new post](/images/save_cms_newpost.png)

You can continue to make changes to the post. When you are ready to submit your post for publishing, change the status of the content to "In Review" via the drop-down in the upper-right hand corner of the page.

![in review status](/images/in_review.png)

This will submit your changes to be reviewed and accepted into the site.

### Adding New Sections

New resource sections require a bit of additional work, so, unless you have experience using GitHub and configuring Netlify CMS, you're best bet is to email the request to [brian@stackbit.com](mailto:brian@stackbit.com) with details about the type of section and content you wish to add. Once a new section is added for you, adding pages can follow the directions above.

For those of you technical enough, here are the basic steps to add a new resource section:

1. Add a folder in under resources. Optionally, you can add an `index.md` file within the folder with the proper front matter or you can do this later via the CMS.
2. Add your folder name into the `sections` array in `/data/doc_sections.yml`.
3. Because Netlify CMS does not currently support collections with content in subfolders, you'll need to add a new collection to the Netlify CMS configuration at `/admin/config.yml`. Copy any of the other resource sections and modify the `name`, `label` and `folder` values. Note that the `name` should be "resources" + underscore + "folder name". For example, if you added a folder named "foo", the value of `name` would be `resources_foo`.
4. If you wish to use the CMS to add content, you'll need to submit your pull request for the new section now. Once it is accepted, new content can be added via the CMS. Otherwise, you are free to add `.md` files in your new folder manually.

## The Technical Details

This site was built using the following technologies:
* [Stackbit](https://www.stackbit.com/) - Stackbit allowed the site and CMS to be easily generated using a theme, which was later customized to meet our specific needs.
* [Jekyll](https://jekyllrb.com/) - The underlying site uses Jekyll as its static site generator. This was chosen to make contributions easier as it is one of the most widely known static site generators.
* [Netlify CMS](https://www.netlifycms.org/) - This is an open source, git-based CMS. This was chosen to take advantage of the [open authoring](https://www.netlifycms.org/docs/open-authoring) feature, which is currently available in the beta release.
* [Netlify](https://www.netlify.com/) - Netlify is used to deploy and host the site, but also maintains the hooks needed to authenticate into the CMS via GitHub.
* [GitHub](https://github.com) - GitHub manages the repository that contains the site code and content. It also enables the authentication that is managed via Netlify.

You can submit issues or changes via our [GitHub repository](https://github.com/remotesynth/ragequit-tips).