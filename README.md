# Dorks

Google dork search queries 

### **1. Finding Vulnerable Files and Directories**

- **Find `.env` files (environment variables):**
  ```plaintext
  filetype:env
  ```

- **Find `.git` directories:**
  ```plaintext
  intitle:".git" -gitignore
  ```

- **Find configuration files:**
  ```plaintext
  filetype:conf
  filetype:ini
  filetype:config
  ```

- **Find `.backup` files:**
  ```plaintext
  filetype:bak
  filetype:backup
  ```

- **Find sensitive backups and source files:**
  ```plaintext
  "database dump" | "db dump" | "backup" | "backup.sql"
  ```

### **2. Discovering Login Pages and Forms**

- **Find login pages:**
  ```plaintext
  intitle:"login" | inurl:"login" | inurl:"signin" | inurl:"auth"
  ```

- **Find admin panels:**
  ```plaintext
  intitle:"admin" | inurl:"admin" | inurl:"cpanel" | inurl:"administrator"
  ```

### **3. Identifying Exposed Documents and Data**

- **Find PDF documents with sensitive information:**
  ```plaintext
  filetype:pdf "confidential" | "internal use" | "secret"
  ```

- **Find Excel files with sensitive data:**
  ```plaintext
  filetype:xls "sensitive" | "confidential"
  ```

- **Find Word documents with sensitive data:**
  ```plaintext
  filetype:doc "confidential" | "sensitive"
  ```

### **4. Locating Security Issues**

- **Find exposed security cameras:**
  ```plaintext
  inurl:"/view.shtml" | inurl:"/admin" | inurl:"/cgi-bin" | inurl:"/camera"
  ```

- **Find publicly accessible AWS S3 buckets:**
  ```plaintext
  site:s3.amazonaws.com "index of" | "public access"
  ```

- **Find exposed MongoDB databases:**
  ```plaintext
  inurl:"mongo" | inurl:"mongodb" | inurl:":27017"
  ```

### **5. Finding Web Servers and Technologies**

- **Find websites running specific technologies:**
  ```plaintext
  "powered by WordPress" | "powered by Joomla" | "powered by Drupal"
  ```

- **Find specific CMS login pages:**
  ```plaintext
  intitle:"Joomla" | inurl:"/user/login" | intitle:"WordPress" | inurl:"wp-login.php"
  ```

### **6. Exploring Specific Domains and IP Ranges**

- **Find subdomains of a domain:**
  ```plaintext
  site:example.com -www
  ```

- **Find exposed IP addresses:**
  ```plaintext
  intitle:"index of" "ip address" | "public IP"
  ```

### **7. Searching for Specific File Types**

- **Find `.sql` files:**
  ```plaintext
  filetype:sql
  ```

- **Find `.xml` files:**
  ```plaintext
  filetype:xml
  ```

- **Find `.log` files:**
  ```plaintext
  filetype:log
  ```

### **8. Detecting Exposed APIs**

- **Find API endpoints:**
  ```plaintext
  inurl:"api" | inurl:"/v1/" | inurl:"/v2/"
  ```

- **Find exposed API keys in files:**
  ```plaintext
  filetype:json "api_key" | "apikey"
  ```

### **9. Uncovering Directory Listings**

- **Find open directory listings:**
  ```plaintext
  "index of /" "parent directory"
  ```

- **Find directories with specific file types:**
  ```plaintext
  "index of /files" filetype:pdf | filetype:doc
  ```

### **10. Other Useful Queries**

- **Find URLs with sensitive query parameters:**
  ```plaintext
  inurl:"id=" | inurl:"user=" | inurl:"password="
  ```

- **Find misconfigured AWS IAM policies:**
  ```plaintext
  "AWS IAM Policy" "s3" "public"
  ```

- **Find exposed Elasticsearch instances:**
  ```plaintext
  inurl:"_search" "Elasticsearch"
  ```

### **11. Specific Vulnerability Searches**

- **Find SQL database dumps:**
  ```plaintext
  filetype:sql "CREATE DATABASE" | "INSERT INTO"
  ```

- **Find exposed Redis instances:**
  ```plaintext
  inurl:"redis" | "redis-cli" | inurl:"6379"
  ```

- **Find exposed PostgreSQL instances:**
  ```plaintext
  inurl:"postgres" | "postgresql" | inurl:"5432"
  ```

### **12. Finding Security-Related Files**

- **Find `.htaccess` files:**
  ```plaintext
  filetype:htaccess
  ```

- **Find `.gitignore` files:**
  ```plaintext
  filetype:gitignore
  ```

- **Find `.env` files with specific keywords:**
  ```plaintext
  filetype:env "DB_PASSWORD" | "SECRET_KEY" | "API_KEY"
  ```

### **13. Locating Exposed Administrative Interfaces**

- **Find administrative pages:**
  ```plaintext
  intitle:"Administration" | intitle:"Admin Panel" | intitle:"Control Panel"
  ```

- **Find exposed cPanel interfaces:**
  ```plaintext
  intitle:"cPanel" | inurl:"cpanel"
  ```

- **Find exposed Webmin interfaces:**
  ```plaintext
  intitle:"Webmin" | inurl:"webmin"
  ```

### **14. Discovering Open Ports and Services**

- **Find open ports using specific keywords:**
  ```plaintext
  "port 80" | "port 443" | "port 3306"
  ```

- **Find exposed FTP servers:**
  ```plaintext
  intitle:"index of" "ftp"
  ```

### **15. Uncovering Cloud Services**

- **Find exposed Google Cloud Storage buckets:**
  ```plaintext
  site:storage.googleapis.com "index of" | "public access"
  ```

- **Find exposed Azure Blob Storage:**
  ```plaintext
  site:blob.core.windows.net "index of" | "public access"
  ```

### **16. Locating Specific File Types in Web Directories**

- **Find `.php` files with vulnerabilities:**
  ```plaintext
  filetype:php "base64_decode" | "eval("
  ```

- **Find `.aspx` files:**
  ```plaintext
  filetype:aspx "login" | "admin"
  ```

- **Find `.jsp` files:**
  ```plaintext
  filetype:jsp "admin" | "login"
  ```

### **17. Discovering Misconfigured Web Servers**

- **Find misconfigured Apache servers:**
  ```plaintext
  intitle:"Apache" "server at"
  ```

- **Find misconfigured Nginx servers:**
  ```plaintext
  intitle:"Nginx" "server at"
  ```

### **18. Locating Sensitive API Endpoints**

- **Find API endpoints with sensitive information:**
  ```plaintext
  inurl:"/api" "token" | "key" | "password"
  ```

- **Find RESTful APIs:**
  ```plaintext
  inurl:"/api/v1/" | inurl:"/api/v2/"
  ```

### **19. Searching for Specific Technologies**

- **Find sites using specific CMS:**
  ```plaintext
  intitle:"Powered by WordPress" | intitle:"Powered by Joomla" | intitle:"Powered by Drupal"
  ```

- **Find specific versions of software:**
  ```plaintext
  "WordPress 5.8" | "Drupal 9.2" | "Joomla 3.9"
  ```

### **20. Detecting Insecure Configuration Files**

- **Find configuration files exposing sensitive settings:**
  ```plaintext
  filetype:config "password" | "username" | "secret"
  ```

- **Find `.cnf` (MySQL config) files:**
  ```plaintext
  filetype:cnf "password" | "user"
  ```

### **21. Exploring Forensic Data**

- **Find log files with sensitive data:**
  ```plaintext
  filetype:log "error" | "exception" | "warning"
  ```

- **Find `.sql` files with specific patterns:**
  ```plaintext
  filetype:sql "CREATE TABLE" | "INSERT INTO" | "DROP TABLE"
  ```

### **22. Miscellaneous Useful Queries**

- **Find exposed Redis servers:**
  ```plaintext
  inurl:"redis" | inurl:"6379" | "redis-cli"
  ```

- **Find exposed Elasticsearch instances:**
  ```plaintext
  inurl:"_search" | inurl:"/_cluster/health" | "Elasticsearch"
  ```

- **Find exposed MongoDB databases:**
  ```plaintext
  inurl:"mongo" | inurl:"mongodb" | inurl:":27017"
  ```

### **23. Finding Exposed Docker Containers**

- **Find Docker API endpoints:**
  ```plaintext
  inurl:"/containers/json" | inurl:"/images/json"
  ```

- **Find Docker Daemon API endpoints:**
  ```plaintext
  inurl:"/v1.24" | inurl:"/v1.41"
  ```
