---
layout: post
title: ldapsearch issues in an Oracle environment
categories: [Oracle, tips]
---


There are two types of errors that you may encounter when executing ldapsearch in an Oracle environment.

# ldap_sasl_interactive_bind_s error

* ldap_sasl_interactive_bind_s: Can't contact LDAP server (-1)
* ldap_sasl_interactive_bind_s: Unknown authentication method (-6)

## Solution
Use "-x" parameter. Refer to the [man page for ldapsearch] ( http://www.openldap.org/software/man.cgi?query=ldapsearch&apropos=0&sektion=0&manpath=OpenLDAP+2.4-Release&format=html )

ldapsearch -x -h example.com -p 1389 -b "dc=example, dc=com" -D "cn=Directory Manager" -w password "objectclass=*"


# Context initialization error

## Solution
Ensure ORACLE_HOME variable is set appropriately.
export ORACLE_HOME=/.../Oracle_IDM1
