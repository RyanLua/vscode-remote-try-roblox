# Try Out Development Containers: Roblox

[![Open in Dev Containers](https://img.shields.io/static/v1?label=Dev%20Containers&message=Open&color=blue&logo=visualstudiocode)](https://vscode.dev/redirect?url=vscode://ms-vscode-remote.remote-containers/cloneInVolume?url=https://github.com/RyanLua/vscode-remote-try-roblox)

A **development container** is a running container with a well-defined tool/runtime stack and its prerequisites. You can try out development containers with **[GitHub Codespaces](https://github.com/features/codespaces)** or **[Visual Studio Code Dev Containers](https://aka.ms/vscode-remote/containers)**.

This is a sample project that lets you try out either option in a few easy steps. Microsoft has a variety of other [vscode-remote-try-*](https://github.com/search?q=org%3Amicrosoft+vscode-remote-try-&type=Repositories) sample projects, too.

> **Note:** If you already have a codespace or dev container, you can jump to the [Things to try](#things-to-try) section. 

## Setting up the development container

### GitHub Codespaces
Follow these steps to open this sample in a Codespace:
1. Click the **Code** drop-down menu.
2. Click on the **Codespaces** tab.
3. Click **Create codespace on main** .

For more information on creating your codespace, visit the [GitHub documentation](https://docs.github.com/en/free-pro-team@latest/github/developing-online-with-codespaces/creating-a-codespace#creating-a-codespace).

### VS Code Dev Containers

If you already have VS Code and Docker installed, you can click the badge above or [here](https://vscode.dev/redirect?url=vscode://ms-vscode-remote.remote-containers/cloneInVolume?url=https://github.com/microsoft/vscode-remote-try-python) to get started. Clicking these links will cause VS Code to automatically install the Dev Containers extension if needed, clone the source code into a container volume, and spin up a dev container for use.

Follow these steps to open this sample in a container using the VS Code Dev Containers extension:

1. If this is your first time using a development container, please ensure your system meets the prerequisites (i.e. have Docker installed) in the [getting started steps](https://aka.ms/vscode-remote/containers/getting-started).

2. To use this repository, you can open a locally cloned copy of the code:

   - Clone this repository to your local filesystem.
   - Press <kbd>F1</kbd> and select the **Dev Containers: Open Folder in Container...** command.
   - Select the cloned copy of this folder, wait for the container to start, and try things out!

## Things to try

Once you have this sample opened, you'll be able to work with it like you would locally.

Some things to try:

1. **Edit:**
   - Open `src/shared/Hello.luau`
   - Try adding some code and check out the language features.
   - Make a spelling mistake and notice it is detected. The [Code Spell Checker](https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker) extension was automatically installed because it is referenced in `.devcontainer/devcontainer.json`.
   - Also notice that utilities like `selene` and the [Rojo](https://marketplace.visualstudio.com/items?itemName=evaera.vscode-rojo) extension are installed. Tools are installed in the `mcr.microsoft.com/devcontainers/base:ubuntu` image and Dev Container settings and metadata are automatically picked up from [image labels](https://containers.dev/implementors/reference/#labels). The `ghcr.io/ryanlua/features/rojo` feature provides [Rojo](https://github.com/rojo-rbx/rojo) for project management tool the [Rokit](https://github.com/rojo-rbx/rokit) toolchain manager.

2. **Terminal:** 
    - Press <kbd>ctrl</kbd>+<kbd>shift</kbd>+<kbd>\`</kbd> to open a terminal window.
    <!-- - Type `rojo build --output vscode-remote-try-roblox.rbxlx` to build the Rojo project into a place file.
        - The terminal will say Rojo `Built project to vscode-remote-try-roblox.rbxlx`. Open the `vscode-remote-try-roblox.rbxlx` file in Roblox Studio to see the project. You may need to right-click the file and **Download...** to your computer. -->
    - Type `rojo serve default.project.json --port 34872` to start the Rojo server.
         - The terminal will say your Rojo server is running on the `localhost` address and port `34872`.
    - In Roblox Studio with the [Rojo plugin installed](https://rojo.space/docs/v7/getting-started/installation/#installing-the-plugin), open a new file/place. Open the Rojo plugin, click **Connect** and when prompted, click **Accept**.
         - A notification in Roblox Studio will appear saying you successfully `Connected to sesson`.

   > **Note:** In Dev Containers, you can access your Rojo project at `http://localhost:34872` in a local browser. But in a browser-based Codespace, you must click the link from the notification or the `Ports` view, right-click the port **Rojo (34872)**, click the **Port Visibility**, then click **Public**. To the right of the local address for the port, click the copy icon. Open Rojo plugin, paste the copied address into the `localhost` and type `80` into `34872`. Remove `https://` at the beginning and `/` at the end of the pasted address. Then you can connect in the Rojo plugin.

3. **Install Python using a Dev Container Feature:**
   - Press <kbd>F1</kbd> and select the **Dev Containers: Configure Container Features...** or **Codespaces: Configure Container Features...** command.
   - Type "python" in the text box at the top.
   - Check the check box next to "Python" (published by devcontainers) 
   - Click OK
   - Press <kbd>F1</kbd> and select the **Dev Containers: Rebuild Container** or **Codespaces: Rebuild Container** command so the modifications are picked up.

### More samples

- [Roblox Showcase Rojo Template](https://github.com/RyanLua/rojo-showcase-template)
