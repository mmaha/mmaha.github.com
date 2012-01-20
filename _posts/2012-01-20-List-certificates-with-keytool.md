---
layout: post
title: List certificates with java keytool
category: tips
---

Just run the following:

    keytool -list -v -storepass changeit -keystore /path/to/jdk/jre/lib/security/cacerts