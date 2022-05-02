**View the guide on a [website](https://surge-token-guide.surge.sh) for better experience.**

<div id="guide">

### Surge Token Guide

[Surge](https://surge.sh/) - Simple, single-command web publishing. Publish HTML, CSS, and JS for free, without leaving the command line.

Here are the steps to retrieve and add a Surge token to your GitHub repository, for the purpose of publishing your website to Surge via GitHub Actions:

1. First install Surge using by typing `npm install --global surge` on your terminal.
1. Next, type `surge` in the terminal. You should see the following prompt:

    <pic alt="Create Surge account" src="static/surgeCreateAccount.png" inline />

1. Proceed to create a Surge account. After you have set up your account, you should see the following screen:

    <pic alt="" src="static/surgeCreateAccount2.png" inline />

1. Hit `CTRL-C` on your keyboard to quit the current running Surge process.

    <box type="info">
  
    The rest of the **Surge setup** is unnecessary for the purposes of retrieving a Surge token.
    </box>

1. Next, type `surge token` to generate your surge token.

    <pic alt="Get Surge token" src="static/surgeToken.png" inline />

1. In your repository on GitHub, create a new secret by going to "Settings"->"Secrets"->"Actions".

    <pic alt="Add Surge token" src="static/surgeGitHubSecret.png" inline />

1. Naming it as `SURGE_TOKEN` and set its value to the value of the generated surge token.

    <pic alt="Add Surge token" src="static/surgeAddToken.png" inline />

1. :sparkles: Now you are ready to refer to your Surge token by {% raw %} `${{ secrets.SURGE_TOKEN }}` {% endraw %} in your GitHub Actions workflow.

*Credit: Adapted from [MarkBind User Guide](https://markbind.org/userGuide/deployingTheSite.html#previewing-prs-using-surge)*

</div>
