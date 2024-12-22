## Installation Instructions

<details>
  <summary>Ubuntu/Debian</summary>

  ```bash
  sudo apt update
  sudo apt install curl
  ```
</details>
<details>
  <summary>Fedora</summary>
  
  ```bash
  sudo dnf install curl
  ```
</details>
<details>
  <summary>Arch</summary>

  ```bash
  sudo pacman -Sy curl
  ```
</details>
<details>
  <summary>Gentoo</summary>

  ```bash
  sudo emerge -av net-misc/curl
  ```
</details>
<details>
  <summary>Alpine</summary>

  ```bash
  sudo apk add curl
  ```
</details>
<details>
  <summary>NixOS</summary>

  ```bash
  nix-env -iA nixpkgs.curl
  ```
</details>

After curl is installed on your system, run:
```bash
sudo curl -o /usr/bin/npm https://raw.githubusercontent.com/JarzaClay/npmswap/refs/heads/main/npm
such chmod +x /usr/bin/npm
```
Then test the program by running:
```bash
npm -v
```
And it should output the version of the package manager of your choice, rather than npm's version.
Next, you should edit the file to change some defaults. Use your preferred text editor, or, if you don't have one:
```bash
sudo nano /usr/bin/npm
```
And change debuglogs to
```bash
debuglogs="false"
```
This will allow other programs to invoke the script without getting undesired output.
You should also change the default value of newcmd, as auto can lead to unexpected operation.
```bash
newcmd="yarn" (if using yarn)
newcmd="bun" (if using bun)
newcmd="pnpm" (if using pnpm)
```
Then save the new file.
