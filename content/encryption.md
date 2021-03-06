---
title: Encryption
order: 11
description: Learn how to enable SSL encryption to secure sensitive data
---

SSL encryption is a security protocol to encrypted connections between servers and clients. We highly recommend that you enable SSL encryption to secure your app's sensitive data and to avoid issues with websockets connecting from behind certain firewalls. You should add the `force-ssl` package to your application to ensure connections over http are redirected to https. Galaxy provides two ways to enable encryption: generating a Let's Encrypt certificate or uploading your own custom certificate.

<h3 id="custom-domain">Before you begin</h3>

Encryption is automatically enabled for all apps deployed to the .meteorapp.com subdomain. To enable encryption for  custom domains, you must first [add a custom domain](/custom-domains.html) on your app settings page and [configure your DNS](/dns.html) to point at Galaxy's DNS. Once added, click on your custom domain to see SSL encryption options.

<h3 id="lets-encrypt">Let's Encrypt</h3>

To enable encryption painlessly, we recommend generating a free [Let's Encrypt](https://letsencrypt.org/) certificate via Galaxy. In just one click Galaxy generates an SSL certificate and configures it for your custom domain.

<img src="images/email-enable-ssl.png" style="width: 500px;">

Let's Encrypt certificates are not available for wildcard (*.) domains.

<h3 id="Custom certificate">Custom certificate</h3>

You can also upload a custom key and certificate. Private keys and certificates should be in the PEM format (this is the same format used by nginx). If intermediate certificates are used in addition to the primary certificate, they should be placed in the same file as the primary certificate. The primary certificate should come first, followed by the intermediate certificates.
