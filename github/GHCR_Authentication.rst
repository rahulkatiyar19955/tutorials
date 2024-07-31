Authenticating GHCR with a personal access token
=================================================

GitHub Packages only supports authentication using a personal access token (classic). For more information, see "Managing your personal access tokens."

1. Create a new personal access token (classic) with the appropriate scopes for the tasks you want to accomplish. If your organization requires SSO, you must enable SSO for your new token.

.. note::
  Note: By default, when you select the write:packages scope for your personal access token (classic) in the user interface, the repo scope will also be selected. The repo scope offers unnecessary and broad access, which we recommend you avoid using for GitHub Actions workflows in particular. For more information, see "Security hardening for GitHub Actions." As a workaround, you can select just the write:packages scope for your personal access token (classic) in the user interface with this url: https://github.com/settings/tokens/new?scopes=write:packages.

* Select the read:packages scope to download container images and read their metadata.
* Select the write:packages scope to download and upload container images and read and write their metadata.
* Select the delete:packages scope to delete container images.

For more information, see `Managing your personal access tokens. <https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token>`_

2. Save your personal access token (classic). We recommend saving your token as an environment variable.

.. raw:: html

  <div class="shell-wrap">
    <div class="shell-top-bar">Terminal</div>
    <div class="shell-body">
      <div class="command">export CR_PAT=YOUR_TOKEN</div>
    </div>
  </div>

3. Using the CLI for your container type, sign in to the Container registry service at ghcr.io.

.. raw:: html

  <div class="shell-wrap">
      <div class="shell-top-bar">Terminal</div>
      <div class="shell-body">
        <div class="command">echo $CR_PAT | docker login ghcr.io -u USERNAME --password-stdin
          <div class="output"> > Login Succeeded</div>
        </div>
      </div>
   </div>
