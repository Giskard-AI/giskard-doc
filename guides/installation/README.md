---
description: >-
  How to install Giskard on your machine, set up your Python backend and upgrade
  Giskard
---

# Installation & upgrade

{% hint style="info" %}
## Requirements

To install Giskard, you need a **Linux** or **macOS** machine with:

* `git (`[`download`](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)`)`
* `docker (`[`download`](https://docs.docker.com/get-docker/)`)`
* `docker`-`compose (`[`download`](https://docs.docker.com/compose/install/)`)`

To install Giskard in AWS, please go to __ [installation-in-aws.md](installation-in-aws.md "mention")__
{% endhint %}

Run the following commands to install Giskard in your server

```shell
git clone https://github.com/Giskard-AI/giskard.git
cd giskard
docker-compose up -d --force-recreate
```

{% hint style="warning" %}
If you have an error because of the rate limit (`toomanyrequests: Rate exceeded`), please re-execute the docker-compose command line once again.
{% endhint %}

Once the docker-compose starts all the modules, you'll be able to open Giskard at [http://localhost:19000/](http://localhost:19000/)

{% hint style="warning" %}
Since the backend container may take some minutes to load, please wait a bit and refresh the webpage [http://localhost:19000/](http://localhost:19000/)
{% endhint %}

To login, the default credentials are **Login: admin / Password: admin**

You're all set to try Giskard in action. Upload your first model by following the [upload-your-model.md](../upload-your-model.md "mention") tutorial.

## Upgrade Giskard to the latest version

In order to upgrade Giskard to the latest version, please run the following in your Giskard distribution directory

```shell
git pull
docker-compose down && docker-compose pull && docker-compose up -d --force-recreate
```

{% hint style="danger" %}
* If you have an error because of the rate limit (`toomanyrequests: Rate exceeded`), please re-execute the docker-compose command line once again.
*   If you installed in Giskard additional Python libraries or a new Python version, you will need to reinstall them. Please refer to

    [#install-additional-python-libraries](./#install-additional-python-libraries "mention")

    [#install-a-new-python-version](./#install-a-new-python-version "mention")
{% endhint %}

## Troubleshooting[???](https://docs.airbyte.com/deploying-airbyte/on-aws-ec2#troubleshooting)

If you encounter any issues, join our [**Discord**](https://discord.gg/fkv7CAr3FE) on our #support channel. Our community will help!&#x20;
