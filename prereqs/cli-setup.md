<!--
#
# Licensed to the Apache Software Foundation (ASF) under one or more
# contributor license agreements.  See the NOTICE file distributed with
# this work for additional information regarding copyright ownership.
# The ASF licenses this file to You under the Apache License, Version 2.0
# (the "License"); you may not use this file except in compliance with
# the License.  You may obtain a copy of the License at
#
#     http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.
#
-->

# Setting Up the IBM Cloud CLI

This section will take you step-by-step through [Getting started with the IBM Cloud CLI and Developer Tools](https://cloud.ibm.com/docs/cli?topic=cloud-cli-getting-started) using the command line option.

## Install IBM Cloud CLI

We have provided the basic instructions here with screenshots, but you can find the canonical IBM Cloud Instructions here: [IBM Cloud CLI Getting Started](https://cloud.ibm.com/docs/cli?topic=cloud-cli-getting-started#step1-install-idt)

Download the `ibmcloud` CLI by running the command appropriate for your operating system:

#### MacOS & Linux

```bash
curl -sL https://ibm.biz/idt-installer | bash
```

#### Windows 10 Pro (Powershell)

Run the following as Administrator:

```bash
[Net.ServicePointManager]::SecurityProtocol = "Tls12"; iex(New-Object Net.WebClient).DownloadString('https://ibm.biz/idt-win-installer')
```

{% hint style="tip" %}
**Tip**: You can right-click the Windows™ PowerShell icon, and select Run as administrator.
{% endhint %}

## Verify the Installation [🔗](https://cloud.ibm.com/docs/cli?topic=cloud-cli-getting-started#step2-verify-idt)

Try running the help command:

```bash
ibmcloud dev help
```

and see if the help instructions are printed, for example:

```bash
NAME:
   ibmcloud dev - Create, develop, deploy, and monitor applications

USAGE:
   ibmcloud dev command [arguments...] [command options]

VERSION:
   2.4.6

COMMANDS:
...
```

## Login and Configure the IBM Cloud CLI [📃](https://cloud.ibm.com/docs/cli?topic=cloud-cli-getting-started#step3-configure-idt-env)

1. Use this command to authenticate the IBM Cloud CLI with your account credentials.

    ```bash
    ibmcloud login
    ```

2. Enter account credentials for your IBM Cloud account.

    ```bash
    Email> josephine.watson@gmail.com
    Password: ********
    Authenticating...
    OK

    Targeted account Josephine Watson's Account (87a302ad58884640a45f959d3da6cc77)
    API endpoint:      https://cloud.ibm.com
    Region:            us-south
    User:              josephine.watson@gmail.com
    Account:           Josephine Watson's Account (87a302ad58884640a45f959d3da6cc77)
    Resource group:    No resource group targeted, use 'ibmcloud target -g RESOURCE_GROUP'
    CF API endpoint:
    Org:
    Space:
    ```

    _Note: If you already have created an IBM Cloud account you may be prompted to select the account you wish the IBM Cloud CLI to use:_

    ```bash
    Select an account (or press enter to skip):
    Select an account:
    1. Josephine Watson's Account (87a302ad58884640a45f959d3da6cc77)
    Enter a number> 1
    ```

3. Configure your Cloud Foundry organization and space the CLI is targeting.

    Run the following interactive command:

    ```bash
    ibmcloud target --cf
    ```

    ```bash
    Targeted Cloud Foundry (https://api.ng.bluemix.net)
    Targeted org josephine.watson@gmail.com
    Targeted space dev

    API endpoint:      https://cloud.ibm.com
    Region:            us-south
    User:              josephine.watson@gmail.com
    Account:           Josephine Watson's Account (87a302ad58884640a45f959d3da6cc77)
    Resource group:    No resource group targeted, use 'ibmcloud target -g RESOURCE_GROUP'
    CF API endpoint:   https://api.ng.bluemix.net (API version: 2.142.0)
    Org:               josephine.watson@gmail.com
    Space:             dev
    ```

    _**Note**: If you already have already created an Namespaces, you may ne prompted to select the Namespace you wish to use as the default for the `cloud-functions` plugin._

{% hint style="success" %}
🎉 **Congratulations, you've successfully registered an IBM Cloud account and logged into the IBM Cloud CLI.** 🎉
{% endhint %}
