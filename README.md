# PHP Microsite Boilerplate

[![pagespeed-100](https://img.shields.io/badge/Lighthouse%20PageSpeed-100-success.svg)](https://developers.google.com/speed/pagespeed/insights/?url=https://phpmicrosite.jenskuerschner.de)
[![amp-valid](https://img.shields.io/badge/AMP-valid-success.svg)](https://validator.ampproject.org/#url=https%3A%2F%2Fphpmicrosite.jenskuerschner.de%2Famp%2F)
[![pwa-valid](https://img.shields.io/badge/PWA-valid-success.svg)](https://phpmicrosite.jenskuerschner.de/)
[![w3c-css-valid](https://img.shields.io/badge/W3C%20CSS-valid-success.svg)](https://jigsaw.w3.org/css-validator/validator?uri=https%3A%2F%2Fphpmicrosite.jenskuerschner.de%2F&profile=css3svg&usermedium=all)
[![LICENSE](https://img.shields.io/badge/license-GPL%203.0-blue.svg)](https://github.com/jekuer/php-microsite-boilerplate/blob/master/LICENSE.txt)
[![github-stars-image](https://img.shields.io/github/stars/jekuer/php-microsite-boilerplate.svg?label=github%20stars)](https://github.com/jekuer/php-microsite-boilerplate)

_PHP Microsite Boilerplate_ is a PHP framework to create simple, yet strongly functional, fast, and secure websites on basically every environment.

Most frameworks and even boilerplates require an exhausting setup process, where you need to install multiple dependencies. 
This leads to a huge overhead of code, which you often do not need. All of those complexity is also a potential risk for your website. 
Furthermore, it is often not possible to use most solutions, if you need to deploy it on the cheapest shared hosting plan.

This project wants to provide you with a framework and template for this exact case:

-   You need to build a rather small website, with some functionality.
-   You choose PHP, because you want to do server-side scripting, while PHP is also maybe the only language, that runs on basically all hosting options.
-   You build this thing on your own or with a maximum of 1 other person, which makes best practice, but complex code structure more of an unnecessary overhead than a helpful concept.
-   You need to get it done fast, while you do not want to make compromises regarding security or performance.
-   Ideally, the whole project should run without any dependencies, should not require a specific IDE setup, or any specific tooling (including Saas). You can still build this on top, but for the start one should be able to update it remotely from basically any device.

Demo: <https://phpmicrosite.jenskuerschner.de/>

## Key Features

-   Easy routing.
-   [Accelerated Mobile Pages (AMP)](https://amp.dev/) prepared.
-   [Progressive Web App (PWA)](https://web.dev/progressive-web-apps/) prepared.
-   Multilanguage prepared.
-   [Directus CMS](https://directus.io/) integration (incl. local cache).
-   GDPR and CCPA ready (regular site and AMP).
-   Intelligent serviceworker cache.
-   Gettext support for easy translation (+ fallback if not installed on the server).
-   SEO optimized.
-   Automated sitemap generation.
-   Optimized for Social sharing.
-   Extensive in-code documentation.
-   [Security Headers](https://securityheaders.com/) (.htaccess or via PHP)
-   Multiple security features (most of them require an Apache server!)
-   Prepared to run git deployment.
-   Developed to make it extremely easy for you to remove features or add your own things.

## Setup

1.  Download the respective branch/tag and upload it to your website's folder - or clone the repo as you like.

2.  Adjust it to your project: 
    -   Check the .htaccess file, if you run it on Apache. Mind the security headers and places, where a domain/path is specified (look for YOURDOMAIN.com). 
    -   If you do not run it on Apache, check the index.php for the security headers setup and make sure every request (except for files) is send to the index.php. 
    -   Adjust the value within config.php and also mind files, which are mentioned in the comments there. 
    -   Check /templates/general_meta.php and create the respective favicons. 
    -   Define your pages at the routing.php. (Mind legal notice and privacy policy to stay GDPR compliant!) 
    -   Create those pages (as specified before) as single php files within /pages. 
    -   Create respective files within /controller if necessary in your case. 
    -   Check the option to auto-redirect within multi-language at index.php and all.js. 
    -   Build the website with those pages, the style.css, and the all.js. Mind to minimize those files or adjust the way they get included at /templates/header.php and /templates/footer.php. 
    -   Adjust the footer at /templates/footer.php and /templates/footer_amp.php to your needs. 

3.  That's basically it.

You can make more changes and use more features, like:

-   Setting up a deployment script (sample included) or the Directus integration.
-   Do even more - it's a well documented playground!

BTW: It is recommended to use a CDN service (e.g. [Cloudflare](https://www.cloudflare.com/)) in order to speed it up even more.

## Contributing

Anyone is welcome to contribute, but mind the [guidelines](.github/CONTRIBUTING.md):

-   [Bug reports](.github/CONTRIBUTING.md#bugs)
-   [Feature requests](.github/CONTRIBUTING.md#features)
-   [Pull requests](.github/CONTRIBUTING.md#pull-requests)

## Changelog

-   1.4.0: Bug fixes, Docker compose template, sitemap generator update, and intelligent redirect for multilanguage use
-   1.3.5: Bug fixes.
-   1.3.4: Option to add last udpdate to sitemap via Directus.
-   1.3.3: Optimization of redirect feature and Directus caching.
-   1.3.2: Extensive bug fixing.
-   1.3.1: Individual slug per language.
-   1.3.0: Added Gettext support, including emulation fallback for servers not supporting native gettext.
-   1.2.0: Optimization of language switcher and serviceworker cache; new redirect functionality; automated sitemap generation; better Directus support (incl. local cache).
-   1.1.0: Added better multilanguage support (incl. language switcher).
-   1.0.0: Initial release.

## License

The code is available under the [GPU 3.0 license](LICENSE.txt).

## Inspired by

This code has been inspired by the [HTML5 Boilerplate](https://github.com/h5bp/html5-boilerplate).
