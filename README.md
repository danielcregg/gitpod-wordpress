# Gitpod WordPress

![WordPress](https://img.shields.io/badge/WordPress-21759B?style=flat-square&logo=wordpress&logoColor=white)
![PHP](https://img.shields.io/badge/PHP-777BB4?style=flat-square&logo=php&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=flat-square)

> **Note:** This repository is a fork of [luizbills/gitpod-wordpress](https://github.com/luizbills/gitpod-wordpress).

A ready-to-code WordPress development environment powered by [Gitpod](https://www.gitpod.io). Develop WordPress plugins or themes directly from your browser with a single click.

## Overview

Gitpod WordPress provides a pre-configured, cloud-based development environment for WordPress. It includes a full LAMP stack, WP-CLI, Composer, Node.js, and debugging tools so you can start building plugins and themes immediately without any local setup.

## Features

- **LAMP Stack** -- Apache, MySQL, and PHP (configurable version) pre-installed
- **WP-CLI** -- Full WordPress command-line interface support
- **Composer & NPM** -- Dependency management for PHP and JavaScript
- **Xdebug** -- Built-in PHP debugging with VS Code integration
- **Adminer** -- Browser-based database management
- **MailHog** -- Local SMTP testing and email capture
- **Node.js (LTS)** -- Managed via NVM for frontend tooling
- **Git & SVN** -- Version control systems included

## Prerequisites

- A [Gitpod](https://www.gitpod.io) account (free tier available)
- A GitHub repository containing your WordPress plugin or theme

## Getting Started

### Installation

1. Copy `.gitpod.yml` and `.gitpod.dockerfile` to your project root directory.
2. Push the files to your remote repository.
3. If your project is a **theme**, change `wp-setup-plugin` to `wp-setup-theme` in `.gitpod.yml`.
4. To change the PHP version, edit `ENV PHP_VERSION` in `.gitpod.dockerfile`.

### Usage

Open your project in Gitpod by navigating to:

```
https://gitpod.io/#<url-of-your-github-project>
```

**Default Admin Credentials:**

| Field    | Value      |
|----------|------------|
| Username | `admin`    |
| Password | `password` |

**Available Terminal Commands:**

| Command            | Description                          |
|--------------------|--------------------------------------|
| `browse-home`      | Open the WordPress homepage          |
| `browse-wpadmin`   | Open the WordPress admin panel       |
| `browse-dbadmin`   | Open Adminer for database management |
| `browse-phpinfo`   | View PHP configuration info          |
| `browse-emails`    | Open the MailHog email client        |

**Custom Initialization:**

Add a `.init.sh` file to your project root to run custom setup commands:

```sh
wp plugin install woocommerce --activate
wp plugin activate ${REPO_NAME}
```

Project dependencies defined in `composer.json` or `package.json` are installed automatically.

## Tech Stack

| Technology | Purpose                        |
|------------|--------------------------------|
| WordPress  | Content management system      |
| PHP 7.4    | Server-side scripting          |
| Apache     | Web server                     |
| MySQL      | Database                       |
| Docker     | Containerized dev environment  |
| Gitpod     | Cloud-based IDE                |
| WP-CLI     | WordPress command-line tooling |
| Xdebug     | PHP debugging                  |

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
