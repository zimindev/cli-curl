# 🌀 `curl` — Command Line Tool for Transferring Data with URLs

`curl` is a powerful command-line tool used to transfer data from or to a server using protocols like HTTP, HTTPS, FTP, SFTP, SCP, and more.

---

## ✅ Features

- Supports multiple protocols: HTTP(S), FTP, SCP, SFTP, LDAP, etc.  
- Upload and download capabilities  
- Can send HTTP POST, PUT, DELETE, and other methods  
- Supports cookies and sessions  
- Supports authentication  
- Works with proxies and custom headers  
- SSL/TLS support  

---

## 🔧 Installation

### On Debian/Ubuntu:
```bash
sudo apt update && sudo apt install curl
```

### On Red Hat/CentOS/Fedora:
```bash
sudo dnf install curl
```

### On Arch Linux:
```bash
sudo pacman -S curl
```

---

## 🚀 Basic Usage

### 📥 Download a file:
```bash
curl -O https://example.com/file.zip
```

### 💾 Save with custom filename:
```bash
curl -o myfile.zip https://example.com/file.zip
```

### 📄 Show output in terminal:
```bash
curl https://example.com
```

---

## 📤 Uploading Data

### Send form data (like HTML forms):
```bash
curl -d "name=John&email=john@example.com" -X POST https://example.com/form
```

### Send data from a file:
```bash
curl -d @data.json -H "Content-Type: application/json" -X POST https://example.com/api
```

---

## 🔑 Authentication

### HTTP Basic Auth:
```bash
curl -u username:password https://example.com/protected
```

### Bearer Token Auth:
```bash
curl -H "Authorization: Bearer YOUR_TOKEN" https://api.example.com/data
```

---

## 📦 Sending Custom Headers

```bash
curl -H "X-Custom-Header: value" https://example.com
```

---

## 🧪 HTTP Methods

- GET (default):
  ```bash
  curl https://api.example.com/items
  ```

- POST:
  ```bash
  curl -X POST -d "param=value" https://api.example.com/items
  ```

- PUT:
  ```bash
  curl -X PUT -d @file.json -H "Content-Type: application/json" https://api.example.com/items/1
  ```

- DELETE:
  ```bash
  curl -X DELETE https://api.example.com/items/1
  ```

---

## 🍪 Cookies

### Save and send cookies:
```bash
curl -c cookies.txt -b cookies.txt https://example.com
```

---

## 📁 FTP/SFTP

### Download file from FTP:
```bash
curl -u username:password ftp://ftp.example.com/file.zip -O
```

### Upload file to FTP:
```bash
curl -T upload.zip -u username:password ftp://ftp.example.com/
```

---

## 🛡️ SSL and Certificates

### Ignore SSL certificate check:
```bash
curl -k https://self-signed.example.com
```

---

## 🔄 Follow Redirects

```bash
curl -L https://example.com
```

---

## ⏱️ Timing and Speed

### Limit download speed:
```bash
curl --limit-rate 100k https://example.com/file.zip
```

### Measure time:
```bash
curl -w "@curl-format.txt" -o /dev/null -s https://example.com
```

---

## 📚 More Info

- Website: [https://curl.se](https://curl.se)
- GitHub: [https://github.com/curl/curl](https://github.com/curl/curl)
- Man Page: `man curl`  
- Help: `curl --help`

---

## 🧩 Alternatives

- `wget` — Great for downloading and mirroring websites  
- `httpie` — User-friendly CLI for APIs
