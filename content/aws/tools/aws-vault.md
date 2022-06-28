---
title: AWS Vault
weight: 1
description: Tool to manage AWS credentials and store in OS keychain
---

# AWS Vault

AWS Vault is a tool to securely store and access AWS credentials in a development environment.

[Official site](https://github.com/99designs/aws-vault)

---

AWS Vault stores IAM credentials in your operating system's secure keystore and then generates temporary credentials from those to expose to your shell and applications. It's designed to be complementary to the AWS CLI tools, and is aware of your [profiles and configuration in `~/.aws/config`](https://docs.aws.amazon.com/cli/latest/userguide/cli-chap-getting-started.html#cli-config-files).

Check out the [announcement blog post](https://99designs.com.au/tech-blog/blog/2015/10/26/aws-vault/) for more details.

## Installing

You can install AWS Vault:
- by downloading the [latest release](https://github.com/99designs/aws-vault/releases/latest)
- on macOS with [Homebrew Cask](https://formulae.brew.sh/cask/aws-vault): `brew install --cask aws-vault`
- on macOS with [MacPorts](https://ports.macports.org/port/aws-vault/summary): `port install aws-vault`
- on Windows with [Chocolatey](https://chocolatey.org/packages/aws-vault): `choco install aws-vault`
- on Windows with [Scoop](https://scoop.sh/): `scoop install aws-vault`
- on Linux with [Homebrew on Linux](https://formulae.brew.sh/formula/aws-vault): `brew install aws-vault`
- on [Arch Linux](https://www.archlinux.org/packages/community/x86_64/aws-vault/): `pacman -S aws-vault`
- on [Gentoo Linux](https://github.com/gentoo/guru/tree/master/app-admin/aws-vault): `emerge --ask app-admin/aws-vault` ([enable Guru first](https://wiki.gentoo.org/wiki/Project:GURU/Information_for_End_Users))
- on [FreeBSD](https://www.freshports.org/security/aws-vault/): `pkg install aws-vault`
- on [OpenSUSE](https://software.opensuse.org/package/aws-vault): enable devel:languages:go repo then `zypper install aws-vault`
- with [Nix](https://search.nixos.org/packages?show=aws-vault&query=aws-vault): `nix-env -i aws-vault`
- with [asdf-vm](https://github.com/karancode/asdf-aws-vault): `asdf plugin-add aws-vault https://github.com/karancode/asdf-aws-vault.git && asdf install aws-vault <version>`

## Documentation

Config, usage, tips and tricks are available in the [USAGE.md](./USAGE.md) file.

## Vaulting Backends

The supported vaulting backends are:

* [macOS Keychain](https://support.apple.com/en-au/guide/keychain-access/welcome/mac)
* [Windows Credential Manager](https://support.microsoft.com/en-au/help/4026814/windows-accessing-credential-manager)
* Secret Service ([Gnome Keyring](https://wiki.gnome.org/Projects/GnomeKeyring), [KWallet](https://kde.org/applications/system/org.kde.kwalletmanager5))
* [KWallet](https://kde.org/applications/system/org.kde.kwalletmanager5)
* [Pass](https://www.passwordstore.org/)
* Encrypted file

