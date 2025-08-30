# 🛡️ Burp Suite Web Application Testing Setup & Report

![Status](https://img.shields.io/badge/Status-Completed-brightgreen)
![Tool](https://img.shields.io/badge/Tool-Burp%20Suite-orange)
![Category](https://img.shields.io/badge/Category-Web%20Security-blue)
![Language](https://img.shields.io/badge/Language-MD-yellow)

---

## 🎯 Objective
The objective of this project is to **set up Burp Suite on Kali Linux**, configure it to intercept traffic from Firefox, and demonstrate its use in **web application security testing**.  

This includes:  
- Configuring the proxy  
- Capturing HTTP(S) traffic  
- Performing basic scanning  

---

## 🛠️ Tools Used
- **Burp Suite (Community Edition)**  
- **Firefox (Browser)**  
- **Kali Linux (Pentesting Environment)**  

---

## ⚙️ Installation of Burp Suite

1. **Install Burp Suite** (if not pre-installed):  
```bash
sudo apt update
sudo apt install burpsuite
```

2. **Launch Burp Suite**:  
```bash
burpsuite &
```

3. **Start a Temporary Project**  
   - Choose *Temporary Project*  
   - Click *Start Burp*  

---

## 🌐 Configuring Burp Suite to Intercept Traffic

### 🔧 Setting Proxy in Firefox
1. Open Firefox → Type `about:preferences`.  
2. Go to **Network Settings → Settings...**  
3. Select **Manual Proxy Configuration**:  
   - HTTP Proxy: `127.0.0.1`  
   - Port: `8080`  
   - Check: *Use this proxy for all protocols*  
4. Save settings.  

---

## 🔐 Installing Burp Suite's SSL Certificate

1. Open Firefox and navigate to: `http://burp`.  
2. Download the CA certificate.  
3. Go to **Preferences → Certificates → View Certificates**.  
4. Import the certificate & trust it for identifying websites.  

---

## 📡 Intercepting Web Traffic

1. Go to **Proxy → Intercept** in Burp.  
2. Turn ON intercept (button should be green).  
3. Open a vulnerable site → e.g., `http://testphp.vulnweb.com`.  
4. Burp will capture the request → options:  
   - Modify request  
   - Forward request  
   - Drop request  

---

## 🧪 Capturing & Testing HTTP Traffic

- Visit `http://testphp.vulnweb.com` in Firefox.  
- Burp captures requests in **Intercept tab**.  
- Requests can be analyzed or sent to:  
  - **Repeater** → Manual testing  
  - **Intruder** → Automated fuzzing  

---

## ✅ Conclusion
Burp Suite was successfully set up on Kali Linux and tested with Firefox.  

✔️ Proxy configured for HTTP(S) traffic  
✔️ SSL certificate installed for HTTPS interception  
✔️ Captured and analyzed web requests against a vulnerable site  

This project demonstrates **Burp Suite's role in web application penetration testing**.  

---

## 🚀 Future Improvements
- Use **Burp Suite Pro** for automated scanning  
- Explore **Intruder** for SQLi & XSS testing  
- Configure for **mobile app traffic interception**  
- Experiment with **external proxies**  

---

## 🔗 References
- [Burp Suite Documentation](https://portswigger.net/burp/documentation)  
- [OWASP ZAP vs Burp Suite](https://www.acunetix.com/blog/owasp-zap-vs-burp-suite/)  

---
