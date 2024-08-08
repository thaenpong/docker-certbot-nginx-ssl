# Multi-Container Application with Docker Compose

This project sets up a multi-container application consisting of:

* **helloworld:** A container running the `crccheck/hello-world` image (replace with your desired image).
* **certbot:** A container for generating and managing Let's Encrypt SSL certificates.
* **nginx:** A web server container that redirects HTTP traffic to HTTPS and serves content.

**Prerequisites:**

* Docker installed and running on your system.
* A valid domain name for which you want to obtain SSL certificates.
* An email address for Let's Encrypt registration.

**Instructions:**

1. **Create the following directories:**
   - `certbot/conf` (to hold Let's Encrypt configuration)
   - `certbot/www` (to store challenge files required for certificate renewal)
   - `nginx/nginx.conf` (for your custom Nginx configuration)

2. **Replace the placeholders:**
   - `{your_domain.com}` with your actual domain name in both `docker.yml` and `nginx.conf`
   - `{your_email_address}` with your email address in `docker.yml`

3. **Build the application:**
   ```bash
   docker-compose up -d
