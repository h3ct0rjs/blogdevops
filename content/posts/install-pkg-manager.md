---
title: "Install a Package Manager on Windows Dev Enviroment"
date: 2019-04-13T18:15:36-05:00
draft: false
---

During a long time it’s been really dificult for me to work on Windows development enviroments, it was not a good sensation, but after giving a try during two months I’ve been able to work with, for my tremendous surprise there is a package manager out there, they’ve integrated a linux subsystem in the operative system and so many things more.

If you don’t know what key advantages you get when you use a package manager I will simple describe it as control, with a package manager you will have to install software and it will automatically download the appropriate package from its configured main software repository, install it, and set it up, all without you having to click through wizards or hunt down .exe files on websites that you don’t trust. When an update is released, your package manager notices and downloads the appropriate update.Chocolatey is a windows package manager or as it’s own definition

>Chocolatey is software management automation. Chocolatey works with over 20+ installer technologies for Windows, but it can manage things you would normally xcopy deploy (like runtime binaries and zip files). You can also work with registry settings or managing files and configurations, or any combination. Since it uses PowerShell, if you can dream it, you can do it with Chocolatey. You’re going to do similar things like apt or yum.

- Good CLI that is simple to use.
- Main repository that takes packages contributions from the - community (and is being maintained, and checked with security - scans).
- Ability to use additional/multiple sources.
- Meta packages that can chain dependencies.
- Virtual packages.
- Packages should be easy to create / maintain.
- Packages should be concise and be able to be created without - worrying about distribution rights.
- Unattended installs
- Installation of multiple packages with one command.

So Chocolatey does the hard work, I’ve tested and is amazing to manage binaries and packages, the installation is pretty simple1 running a simple script in your powershell terminal :

{{< highlight powershell "linenos=table" >}}
Set-ExecutionPolicy Bypass -Scope Process -Force; iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))
{{< / highlight >}}

This may not seem very powerful at first, but imagine when you want to upgrade all of the software on your system to the latest, most secure versions, how do you do that now on windows ? Right. Manually, why not execute

{{< highlight powershell "linenos=table" >}}
choco upgrade packagename
{{< / highlight >}}

If we’re going to install chocolatey you can do something like :
