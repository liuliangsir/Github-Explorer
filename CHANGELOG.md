# Change Log
All notable changes to the "vscode-file-system-sample" extension will be documented in this file.

Check [Keep a Changelog](https://keepachangelog.com/) for recommendations on how to structure this file.

# *Remote - Github* 0.2.0 Release

*Remote - Github* is currently in **preview**, thank you all for trying it. 

I recevied a lot of different views, most of them are helpful. Thanks to every one using *Remote - Github*, it would be better with your feedback.

Here's what's new in 0.2.0:

## Big Feature

**Enable VS Code Full Feature Set By Providing Mount Point**

VS Code supports **Intellisense**, **Code Navigation**, **File Searching**, etc. Browing code would be much easier with these amazing features, but people find they cannot do this with files loaded by *Remote - Github*. 

It is because *Remote - Github* stores them to memory, namely, virtual file system first, so the vscode could not analyze it, neither do other tools like `npm`, `maven`, etc.

*Remote - Github* now gives you a choice to enable all these features by writing loaded files to your local fs. It's really simple, all you need is provide a "mount point" (just an absolute path to store the whole *github* folder):

![Image](https://pic4.zhimg.com/80/v2-901592099811a0179a28df76710c29d8.png)

Once the mount point is provided, all loaded file would be written to a newly created `github` folder under your mount point, and everything works just like before except that vscode features are enabled.

After that, you could find anything in your local github folder, and you can compile it, modify and save it, and run it.

## Repository Searching

In 0.1, if you want to open `vscode` repo, you need to input `https://github.com/microsoft/vscode`. To do this, you have to open github and find this repo, paste link to *Remote-Github*.

With *Repository Searching*, all you have to do it provide a single keyword like "vscode", and *Remote-Github* would provide you several searching results for you to pick:

![Image](https://pic4.zhimg.com/80/v2-58de08328148776bbafe7c27939c03bb.png)

This would not break the old behavior, if you provide full link, everything works like in 0.1.

### Resolved Issues

1. Can not invoke `Remote - Github: Setup Workspace` when in workspace.
2. Wrong link in readme.
3. username and password not trimmed before being encoded.








