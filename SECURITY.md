# Security Policy

## Enabling HTTPS Security

To ensure your website is secure and served over HTTPS:

1. **Obtain an SSL/TLS Certificate**
   - Use a trusted Certificate Authority (CA) such as [Let's Encrypt](https://letsencrypt.org/) for a free certificate.
   - Follow your hosting provider's instructions to install the certificate.

2. **Configure Your Web Server**
   - Redirect all HTTP traffic to HTTPS.
   - Set recommended HTTP security headers:
     - `Strict-Transport-Security: max-age=63072000; includeSubDomains; preload`
     - `Content-Security-Policy: default-src 'self'; img-src 'self' https:; script-src 'self' https:; style-src 'self' https: 'unsafe-inline';`
     - `X-Content-Type-Options: nosniff`
     - `X-Frame-Options: SAMEORIGIN`
     - `Referrer-Policy: no-referrer-when-downgrade`
     - `Permissions-Policy: camera=(), microphone=(), geolocation=()`

3. **Update All Resource Links**
   - Ensure all external resources (CDNs, images, scripts) use `https://` URLs.

4. **Test Your Site**
   - Use [SSL Labs](https://www.ssllabs.com/ssltest/) to verify your HTTPS configuration.

## Reporting Vulnerabilities

If you discover a security vulnerability in this project, please report it by emailing [info@aidsa.org](mailto:info@aidsa.org).

- Do **not** create public issues for security vulnerabilities.
- We will respond as soon as possible and work to resolve the issue.

## Additional Resources

- [GitHub HTTPS documentation](https://docs.github.com/en/pages/getting-started-with-github-pages/securing-your-github-pages-site-with-https)
- [Mozilla Observatory](https://observatory.mozilla.org/) for security scanning

