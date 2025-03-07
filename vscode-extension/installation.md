# Installing Tanzu Dev Tools for Visual Studio Code

This page explains how to install the VMware Tanzu Developer Tools extension for Visual Studio Code (VS Code).

## <a id=on-this-page></a> On this page

- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Configuration](#configuration)
- [Uninstallation](#uninstallation)
- [What’s Next](#whats-next)

## <a id="prerequisites"></a> Prerequisites

> **Note:** The Tanzu Developer Tools extension currently only supports VS Code, Mac OS, and Java Applications.

Before installing the Tanzu Developer Tools IDE extension, you must have:

- [VS Code](https://code.visualstudio.com/download)
- The Kubernetes command-line tool. For more information, see the [kubectl section of the Kubernetes Install Tools page](https://kubernetes.io/docs/tasks/tools/#kubectl).
- [Tilt](https://docs.tilt.dev/install.html) v0.24.0 or later (Docker Desktop and local Kubernetes are not prerequisites for using Tanzu Developer Tools for VS Code)
- The Tanzu CLI and plug-ins. Follow the instructions on the [Installing the Tanzu CLI page](../install-tanzu-cli.md#-install-or-update-the-tanzu-cli-and-plug-ins).
- A cluster with Tanzu Application Platform’s [Iterate or Full profiles](../install.md#-install-your-tanzu-application-platform-profile). Download these from [Tanzu Network](https://network.tanzu.vmware.com/products/tanzu-application-platform/). For installation instructions, see [Installing the Tanzu Application Platform](../install.md).

> **Note:** If you are an application developer the Tanzu Application Platform environment may have been set up by someone else in your organization. Contact the correct group within your organization to determine if a Tanzu Application Platform environment already exists.

## <a id="installation"></a> Installation

To install VMware Tanzu Developer Tools for Visual Studio Code:

1. Download Tanzu Developer Tools for Visual Studio Code from the Tanzu Network.
1. Open VS Code.
  1. From the Command Palette (cmd + shift + P), run "Extensions: Install from VSIX...".
  1. Select the extension file, tanzu-vscode-extension.vsix.
  ![Command palette open showing text Extensions: INSTALL FROM VSIX...](../images/vscode-install1.png)
  1. or select the Extensions tab
  ![The extensions tab icon which is a square cut in fourths with the top-right fourth moved away from the other three](../images/vscode-install2.png)
  1. and select `Install from VSIX…` from the overflow menu
  ![The VS Code interface showing the extensions tab open, the overflow menu in the extensions tab open, and the "Install from VSIX..." option highlighted](../images/vscode-install3.png)
  1. If you do not already have the Debugger for Java, Language Support for Java(™) by Red Hat, and YAML extensions installed, the Tanzu Developer Tools extension should install them automatically for you. The Tanzu Developer Tools extension depends on these additional extensions to function.
    1. Note: If the extensions do not automatically install, manually install the following extensions from the VS Code Marketplace:
      - [Debugger for Java](https://marketplace.visualstudio.com/items?itemName=vscjava.vscode-java-debug)
      - [Language Support for Java(™) by Red Hat](https://marketplace.visualstudio.com/items?itemName=redhat.java)
      - [YAML](https://marketplace.visualstudio.com/items?itemName=redhat.vscode-yaml)
  1. Ensure Language Support for Java is running in [Standard Mode](https://code.visualstudio.com/docs/java/java-project#_lightweight-mode).
    - This can be configured in the Settings menu **Code -> Preferences -> Settings** under `Java > Server: Launch Mode`
  ![The VS Code settings open to the Extensions > Java section, highlighting the option "Java > Server: Launch Mode" with that option changed to "Standard"](../images/vscode-install4.png)
  When the JDK and Language Support for Java are configured correctly, you see that the integrated development environment creates a directory "target" where the code is compiled.

## <a id="configuration"></a> Configuration

To configure the VMware Tanzu Developer Tools extension for Visual Studio Code:
1. Ensure that you are targeting the correct cluster. See [Configure Access to Multiple Clusters](https://kubernetes.io/docs/tasks/access-application-cluster/configure-access-multiple-clusters/) in the Kubernetes documentation.
1. Select **File -> Preferences -> Settings -> Extensions -> Tanzu** and set the following:
- [Source Image](../glossary.md#source-image) (required): Destination for an image containing source code to be published
  - Example: `your-registry.io/project/tanzu-java-web-app-source`
- [Local Path](../glossary.md#local-path) (optional): Path on the local file system to a directory of source code to build (defaults to current directory)
- [Namespace](../glossary.md#namespace) (optional): Namespace that workloads are be deployed into (defaults to namespace set in kubeconfig)

## <a id="uninstallation"></a> Uninstallation

To uninstall the Tanzu Dev Tools extension:
1. Navigate to the extensions menu.
![The extensions tab icon which is a square cut in fourths with the top-right fourth moved away from the other three](../images/vscode-install2.png)
1. Right-click the Tanzu Dev Tools extension and select `Uninstall`.

## <a id="whats-next"></a> What's Next

When finished on this page, proceed to the [Getting Started](../vscode-extension/getting-started.md) page.
