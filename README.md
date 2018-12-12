# docker-phpcs-security-audit
Dockerized version of PHPCS-Security-Audit

# About
phpcs-security-audit is a set of PHP_CodeSniffer rules that find vulnerabilities and weaknesses related to security in PHP code.

It currently has core PHP rules as well as Drupal 7 specific rules.

The tool also checks for CVE issues and security advisories related to CMS/framework. Using it, you can follow the versioning of components during static code analysis.

The main reason for this project for being an extension of PHP_CodeSniffer is to have easy integration into continuous integration systems. It is also able to find security bugs that are not detected with object-oriented analysis (like in RIPS or PHPMD).

phpcs-security-audit is backed by [Floe design + technologies](https://floedesign.ca/) and written by [Jonathan Marcil](https://twitter.com/jonathanmarcil).

# Run

## Default Rules

```bash
docker run -v /path/to/code/:/opt/mount/ guardrails/phpcs-security-audit:latest
```

## JSON Output

```bash
docker run -t -v `pwd`:/opt/mount/ guardrails/phpcs-security-audit:latest --report=json
```
