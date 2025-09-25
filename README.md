# Project Setup Guide  

## 1. Clone Project  
```bash
git clone <your-repo-url>
cd <project-folder>
```

---

## 2. Install Dependencies  

Run the following scripts to install **Docker** and **Docker Compose**:  

```bash
cd scripts && sh install-docker.sh          # Install Docker
cd scripts && sh install-docker-compose.sh  # Install Docker Compose
cd scripts/ssl && sh install.sh             # Install SSL
```

---

## 3. Start Containers  

Once Docker and Docker Compose are installed, start the containers:  

```bash
docker-compose up -d
```

---

## 4. Switch PHP Version  

You can use a different PHP version by editing the `docker-compose.yml` file.  
Uncomment the desired image line, then restart the containers:  

```bash
docker-compose up -d
```

### Available PHP Versions:
- `kalpit/ultimatephpdev:7.0` → PHP 7.0  
- `kalpit/ultimatephpdev:7.2` → PHP 7.2  
- `kalpit/ultimatephpdev:7.3.3` → PHP 7.3.3  
- `kalpit/ultimatephpdev:7.4` → PHP 7.4  
- `kalpit/addweb:5.6` → PHP 5.6  
- `bhardwaj2803/ultimatephpdev:8.0_latest` → PHP 8.0 (latest)  
- `addwebsolution/php:8.4` → PHP 8.4  
- `addwebsolution/php:8.3` → PHP 8.3  
- `addwebsolution/php:8.2` → PHP 8.2  
- `addwebsolution/php:8.1` → PHP 8.1 (**default**)  
- `addwebsolution/php:8.0` → PHP 8.0  

---

## 5. Run Composer  

After starting the containers, bash into the **code container** using the helper script:  

```bash
sh infonew.sh
```

Then run the following commands inside the container:  

```bash
cd /root/.composer && composer install
cd /root/.composer && php installer.phar
```

---

✅ Your environment should now be ready!
