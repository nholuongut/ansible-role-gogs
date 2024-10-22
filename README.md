# Ansible Role: Gogs

**DEPRECATED**: This project is no longer actively maintained. I recommend using an alternative like [Gitea](https://gitea.com).

![](https://i.imgur.com/waxVImv.png)
### [View all Roadmaps](https://github.com/nholuongut/all-roadmaps) &nbsp;&middot;&nbsp; [Best Practices](https://github.com/nholuongut/all-roadmaps/blob/main/public/best-practices/) &nbsp;&middot;&nbsp; [Questions](https://www.linkedin.com/in/nholuong/)
<br/>

Installs [Gogs](https://github.com/gogits/gogs), a Go-based front-end to Git, on RedHat or Debian-based linux systems.

After the playbook is finished, visit the gogs server (on port 3000 by default), and you will be redirected to the /install page, where you can configure an administrator account and other default options.

## Requirements

Requires git (via `nholuong.git`), and at least the Gogs HTTP port (3000 by default) open on your system's firewall. Install MySQL (e.g. via `nholuong.mysql`) prior to installing Gogs if you would like to use MySQL instead of built-in SQLite support.

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

    gogs_user: git
    gogs_user_home: /home/git

The user and home under which Gogs will run and be installed.

    gogs_binary_url: https://github.com/gogits/gogs/releases/download/v0.3.1/linux_amd64.zip

Download URL for the Gogs binary.

    gogs_http_port: "3000"

HTTP port over which Gogs will be accessed.

    gogs_use_mysql: false
    gogs_db_name: gogs
    gogs_db_username: gogs
    gogs_db_password: root

MySQL database support. Set `gogs_use_mysql` to `true` to configure MySQL for gogs, using the database name, username, and password defined by the respective variables.

## Dependencies

  - nholuong.git

## Example Playbook

    - hosts: servers
      vars_files:
        - vars/main.yml
      roles:
        - nholuong.gogs

*Inside `vars/main.yml`*:

    gogs_http_port: "8080"

# 🚀 I'm are always open to your feedback.  Please contact as bellow information:
### [Contact ]
* [Name: nho Luong]
* [Skype](luongutnho_skype)
* [Github](https://github.com/nholuongut/)
* [Linkedin](https://www.linkedin.com/in/nholuong/)
* [Email Address](luongutnho@hotmail.com)

![](https://i.imgur.com/waxVImv.png)
![](Donate.png)
[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/nholuong)

# License
* Nho Luong (c). All Rights Reserved.🌟
