# xray for PaaS

TIPS: You can create a private repository based on the original repository by clicking on "Use this template" in the repository

![image](https://user-images.githubusercontent.com/122191366/212063458-2def0e1a-805a-4451-ae62-324b67abee47.png)

## Project Features

* This project is used to deploy xray on any PaaS cloud provider using Nginx + WebSocket + VMess/Vless/Trojan/Shadowsocks + TLS
* xray core files and configuration files are "special" and different for each project, greatly reducing the risk of blocking and collusion
* uuid for vmess and vless or password for trojan and shadowsocks, paths can be either customized or used as default
* Integrate with Nezha probe, you can choose to install it or not
* If you find that you can't access the Internet after deployment, please check whether the domain name is walled, you can use Cloudflare CDN or worker to solve it.

## Deployment

* Register any PaaS cloud service provider
* Bind your own github account or use the Actions provided by the project to generate a DockerHub image according to the PaaS cloud provider, alts + private library is seriously recommended
* Variables available to the project

  | Variable Name | Required | Default | Remarks |
  | ------------ | ------ | ------ | ------ |
  | UUID | No | de04add9-5c68-8bab-950c-08cd5320df18 | Can be generated online at https://www.uuidgenerator.net/ |
  | VMESS_WSPATH | no | /vmess | starts with / |
  | VLESS_WSPATH | no | /vless | starts with / |
  | TROJAN_WSPATH |no | /trojan | starts with / |
  | SS_WSPATH | no | /shadowsocks | starts with / |
  | NEZHA_SERVER | No | | The server address of the Nezha probe server |
  | NEZHA_PORT | No | |  The port of the Nezha probe server |
  | NEZHA_KEY | No | | Nezha Probe client-specific key |

* Variables used by GitHub Actions

  | Variable Name | Remarks |
  | ------------- | -------------- |
  |DOCKER_USERNAME|Docker Hub username|
  |DOCKER_PASSWORD|Docker Hub password|
  |DOCKER_REPO|Docker Hub repository name|

![image](https://user-images.githubusercontent.com/116990986/211692321-34df154a-320a-448f-9abe-2efab9c53550.png)

## Acknowledgements

ifeng's v2ray project: https://github.com/hiifeng

## Disclaimers

* This program is for learning purposes only, not for profit, please delete within 24 hours after downloading, not for any commercial use, the text, data and images are copyrighted, if reproduced, please cite the source.
* Use of this program is subject to the deployment disclaimer. Use of this program is subject to the laws and regulations of the country where the server is deployed and the country where the user is located, and the author of the program is not responsible for any misconduct of the user.

## Sponsorship

afdian: https://afdian.net/a/Misaka-blog

![afdian-MisakaNo の 小破站](https://user-images.githubusercontent.com/122191366/211533469-351009fb-9ae8-4601-992a-abbf54665b68.jpg)