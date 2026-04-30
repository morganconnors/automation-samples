# Gitlab Runner Registration Script

TLDR: make token, run script.

Pretty simple script, I personally run it from Ansible. It works well, just don't leak your token.

Get your token from Gitlab [here](https://gitlab.com/-/user_settings/personal_access_tokens?page=1&state=active&sort=expires_asc) (or at this link for your self-hosted version: `gitlab.example.org/-/user_settings/personal_access_tokens?page=1&state=active&sort=expires_asc`). Then, select the `create_runner` permission and create your token.

If you want to change it at all, these [docs](https://docs.gitlab.com/api/users/#create-a-runner-linked-to-a-user) will be useful for the API call and these [docs](https://docs.gitlab.com/runner/register/) will be useful for registering the runner.

For using with Ansible, just set an environment variable in your task and add tell the script to use it.