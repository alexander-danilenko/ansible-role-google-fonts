<p align="center">
  <img src="https://upload.wikimedia.org/wikipedia/commons/e/ee/Google_Fonts_logo.svg" width="400" />
</p>

<h1 align="center">
  Ansible Role for Google Fonts
</h1>

<p>
  <a href="./LICENSE" target="_blank">
    <img alt="License: MIT" src="https://img.shields.io/badge/License-MIT-green.svg?style=for-the-badge" />
  </a>
</p>

> This repo contains Ansible role that installs fonts from the [Google Fonts library](https://fonts.google.com/) to the target host system using <a href="https://google-webfonts-helper.herokuapp.com/">Google Webfonts Helper</a> service.

## Requirements

Following system packages are required and will be installed if needed:

- curl
- tar

## Example Ansible Playbook

```yaml
- hosts: 127.0.0.1
  roles:
    - role: ansible-role-google-fonts
      vars:
        google_fonts_install_dir: '{{ ansible_env.HOME }}/.fonts'
        google_fonts_download_formats: [ttf]
        google_fonts_list:
          - jetbrains-mono
          - open-sans
          - open-sans-condensed
          - roboto
          - roboto-condensed
          - roboto-mono
          - roboto-slab
          - ubuntu
          - ubuntu-condensed
          - ubuntu-mono
```
## Where can I find font ids?

- :godmode: **Option 1 (recommended)**: 
  
  The following command will print all available font ids to a terminal.

  ```bash
  curl https://google-webfonts-helper.herokuapp.com/api/fonts/ | jq ".[].id" | sort
  ```
  > ⚠️ Note: command relies on `jq` and `curl` packages that needs to be installed first.

- :feelsgood: **Option 2**:

  Find in raw JSON fonts list: https://google-webfonts-helper.herokuapp.com/api/fonts

## Author

👤 **Alexander Danilenko**

* Website: https://danilenko.in
* Github: [@alexander-danilenko](https://github.com/alexander-danilenko)
* LinkedIn: [@alexander-danilenko](https://linkedin.com/in/alexander-danilenko)


## 🤝 Contributing

Contributions, issues and feature requests are welcome!<br />Feel free to check [issues page](https://github.com/alexander-danilenko/ansible-role-google-fonts/issues).

## Show your support

Give a ⭐️ if this project helped you!

## Special thanks

**[Mario Ranftl](https://github.com/majodev)** and all [project](https://github.com/majodev/google-webfonts-helper) [contributors](https://github.com/majodev/google-webfonts-helper/graphs/contributors) of the awesome [Google Webfonts Helper](https://google-webfonts-helper.herokuapp.com/)!

<img src="https://badges.pufler.dev/contributors/majodev/google-webfonts-helper?bots=false&size=42" />

---

## 📝 License

Copyright © 2022 [Alexander Danilenko](https://github.com/alexander-danilenko).<br />
This project is [MIT](./LICENSE) licensed.

***
_This README was generated with ❤️ by [readme-md-generator](https://github.com/kefranabg/readme-md-generator)_