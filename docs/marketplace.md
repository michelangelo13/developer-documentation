## Marketplace

### Maximum exposure to your plugins and themes
The Piwik Marketplace lets you share your Plugins or Themes with all Piwik users. You'll be able to:
 * Keep track of how many people downloaded your plugin
 * Give your plugin and your name lots of exposure in the official Piwik Marketplace!
 * (coming soon) Let people leave comments about your plugin
 * (coming soon) Get your plugin rated against the other Piwik plugins

### Getting started
#### Naming your plugin
Before you can list your plugin on the Marketplace, you'll need to choose a name for your plugin.
The name is a unique identifier that distinguishes your plugin from all other plugins. We encourage you to choose a name that is short, but also reasonably descriptive.

Names are registered on a first come, first serve basis. Registering a name happens automatically the first time you publish a release of your plugin.

#### Creating a plugin.json manifest file

Manifest file must be named `plugin.json`, must live in the root of your repository and exist in your tags. The files must be actual JSON, not just a JavaScript object literal. The *most* important things in your manifest file are the `name` and `version` fields.

The following fields are required:
 * `name` - The name can only contain letters, numbers, and the characters `-` and `_`.
 * `version` - Version number must be a valid semantic version number per [node-semver](https://github.com/isaacs/node-semver).
 * `description` - A short description of your plugin (up to 150 characters). This will be displayed below the plugin name in search results, and displayed below the top-level heading on your plugin's page. You may include Piwik (if you want) and spaces and mixed case, unlike `name`.
 * `keywords` - An array of strings. This helps people discover your plugin as `keywords` are listed on the Marketplace. Keywords may only contain letters, numbers, hyphens, and dots.
 * `license` - License name of your plugin source code. The license must be compatible with the GPLv3 or later. We recommend "GPLv2 or later"
 * `homepage` - The url to the plugin homepage.
 * `authors` - An array of people who created this plugin. An author is an object with a name field and optionally homepage and email. You must define at least one author, like this:

```json
"authors": [
  {
    "name": "Hacker",
    "email": "marketplace@piwik.org",
    "homepage": "http://piwik.org"
  }
]
```
 Both email and homepage are optional.

The following fields are optional:
 * `theme` - A boolean set to true if your plugin is a Theme. A Theme is a plugin that will customize the look and feel of Piwik.
 * `donate` - An array of information on how to donate to the plugin author (you!)
  * `paypal` - Your Paypal email address
  * `flattr` - The url to your Flattr page
  * `bitcoin` - Your Bitcoin address
 For example:

```json
"donate":
  {
    "paypal": "supporters@piwik.org",
    "flattr": "https://flattr.com/thing/131552/Piwik-Web-Analytics-Open-Source",
    "bitcoin": "http://piwik.org"
  }
```

##### Sample plugin.json

View a [plugin.json sample here](https://raw.github.com/tsteur/piwik-livetab-plugin/master/plugin.json)


#### Creating a Readme.md

The Readme.md is used to make your plugin page in the Marketplace useful.
Each plugin should have a readme file named Readme.md that adheres to the Piwik plugin readme file standard.

View a [README.md sample here](https://raw.github.com/tsteur/piwik-livetab-plugin/master/README.md)

The Readme file is written in Markdown format.
You may define the sections "Description", "Installation", "FAQ", "Changelog" and "Support", which will appear as category links on your Plugin page.


### Hosting your plugin code on Github
Next we will publish your plugin code on a Git repository on Github:
 * Create a new GitHub repository ([learn more](https://help.github.com/articles/create-a-repo)).
 * Push your plugin code in your repository. [See example repository](https://github.com/tsteur/piwik-livetab-plugin).

Well done, your plugin is hosted on Github!

### Setting up a WebHook for your Github Repository
Follow the steps to setup the WebHook for your repository:
 * Open your repository on GitHub and go to its settings page
 * Click 'Service Hooks'
 * Click 'WebHook URLs'.
 * Enter in the URL field: `http://plugins.piwik.org/postreceive-hook`
 * Click 'Update Settings'

Now, when you commit a code change or a tag in your repository, the Piwik Marketplace will be notified. We are almost done publishing your plugin!

### Publish your plugin

At this stage you have committed your plugin code to your Github repository which contains at least a plugin.json and a Readme.md file. The post-receive hook will notify the Marketplace that a new tag is available.
Publishing your plugin is now as simple as tagging the version in git and pushing the tag to GitHub:
`
$ git tag 0.1.0

$ git push origin --tags
`

You may use any tag name. If the manifest file is valid, the new Plugin version will be built and added to the Marketplace: congratulations! You will receive an email to confirm your plugin was successfully published.

If there was an error during the validation, you will receive an email with helpful tips.


### Publish an updated version of your plugin

To publish an update of your plugin on the Marketplace, simply update the version number tag in the plugin.json, commit, and create a new tag to trigger the release.

### Troubleshooting

When you create the tag, the Piwik Marketplace will attempt to publish your new plugin's version. If any error is detected during the process, you will receive an email with helpful information on the problem and how to fix the problem.

Some common validation errors are:
 * plugin.json manifest file not found
 * some of plugin.json required fields are not set
 * the version in plugin.json has already been published for this plugin
 * the readme.md file is missing
 * a plugin with this name already exists

If you still encounter trouble getting this process to work with your plugin, please join the IRC channel #piwik on freenode. If you can't seem to connect with someone in the IRC channel, please feel free to email us at hello@piwik.org.

### There are only a few restrictions
 * The plugin must not do anything illegal, or be morally offensive.
 * Your plugin must be compatible with the GNU General Public License v3 or any later version. We strongly recommend using the same license as Piwik — “GPLv3 or later.”
 * If you don’t specify a compatible license (such as in a license.txt file or referencing or declaring a license somewhere in the code or readme.md file), what you publish on the Marketplace is considered GPLv3 or later.
 * No obfuscated code. We believe that obfuscated code violates the spirit, if not the letter, of the GPL license under which we operate.
 * No "phoning home" without user's informed consent. This seemingly simple rule actually covers several different aspects:
  * No unauthorized collection of user data. For example, sending the admin's email address back to your own servers without permission of the user is not allowed; but asking the user for an email address and collecting if they choose to submit it is fine. All actions taken in this respect MUST be of the user's doing, not automatically done by the plugin.
  * All images and scripts shown should be part of the plugin. These should be loaded locally. If the plugin does require that data is loaded from an external site (such as blocklists) this should be made clear in the plugin's admin screens or description. The point is that the user must be informed of what information is being sent where.
 * The plugin page (aka the readme.md file) may not have "sponsored" links on it. Same goes for the translation files and any other linkback type schemes that will have content displayed on [plugins.piwik.org](plugins.piwik.org) and [themes.piwik.org](themes.piwik.org)
 * Don't violate our [trademarks](http://piwik.org/trademark/). Don't use "piwik" in your domain name, instead come up with your own original branding! People remember names.