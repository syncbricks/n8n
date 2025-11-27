# 🚀 Secure n8n Deployment with Docker Compose

A complete and secure `n8n` automation stack using Docker Compose. This setup includes:

- ✅ PostgreSQL for workflow and credential storage
- ✅ Qdrant for vector DB / AI use cases
- ✅ NGINX reverse proxy with local HTTPS via Let's Encrypt
- ✅ Cloudflare Tunnel for secure public access (no port forwarding needed)

Everything starts with a single command:  
```bash
docker compose up -d
```

---

## 📦 Stack Components

| Service       | Description                                                                 |
|---------------|-----------------------------------------------------------------------------|
| `n8n`         | Workflow automation platform                                                |
| `PostgreSQL`  | Backend DB for persistent workflow storage                                  |
| `Qdrant`      | Vector DB for advanced AI/search integrations                               |
| `NGINX`       | Local reverse proxy with automatic SSL using Let's Encrypt                 |
| `Cloudflared` | Secure tunnel to expose `n8n` publicly (no need to open ports!)             |

---

## 🌍 Local vs Public Access

You can choose how you want to access your n8n:

| Use Case                     | NGINX | Cloudflare Tunnel |
|-----------------------------|:-----:|:------------------:|
| Home lab only               | ✅    | ❌                 |
| Remote access securely      | ✅    | ✅                 |
| Avoid router configuration  | ❌    | ✅                 |
| Maximum flexibility         | ✅    | ✅                 |

> 💡 If you **only want local access**, you can disable/remove the `cloudflared` service.  
> 💡 If you **only want remote access**, you can remove the `nginx` and `acme-companion` services.

---

## 📚 My Courses (Learn More!)

If you're interested in automation, self-hosting, or network security, check out my top-rated courses:

🎯 **[Mastering n8n Automation](https://www.udemy.com/course/n8n-automation-mastery/?referralCode=SYNCBRICKS)**  
💡 Learn how to self-host, build advanced workflows, and integrate APIs with ease.

🛡️ **[pfSense Firewall Complete Guide](https://www.udemy.com/course/pfsense-complete-guide/?referralCode=SYNCBRICKS)**  
Secure your network using open-source pfSense with hands-on labs and real-world use cases.

🖥️ **[Proxmox Virtualization Mastery](https://www.udemy.com/course/proxmox-course/?referralCode=SYNCBRICKS)**  
Build and manage your own homelab or production-grade virtualization platform with Proxmox.

🧠 **[AI Automation Mastery with Low-Code](https://www.udemy.com/course/ai-automation-lowcode/?referralCode=SYNCBRICKS)**  
Create intelligent workflows with AI models, agents, and automation tools.

👨‍💼 **[Generative AI for Leaders](https://www.udemy.com/course/generative-ai-for-leaders/?referralCode=SYNCBRICKS)**  
Perfect for decision-makers looking to leverage AI for innovation and business transformation.

📦 **[Untangle Firewall (Arista) Security](https://www.udemy.com/course/untangle-firewall/?referralCode=SYNCBRICKS)**  
Learn NGFW with real-world scenarios to secure your small business or homelab network.

---



---

## 🛠️ Quick Start


Make sure you:
- Update your domain in `.env` or directly in `docker-compose.yml`
- Replace the Cloudflare token (if using the tunnel)
- Point your domain (e.g., `n8n.syncbricks.com`) to your server

---

## 🙌 Contributions Welcome

Feel free to open issues, suggest improvements, or fork the project.

---

## 🧑‍💻 Connect with Me

- 🌐 [amjidali.com](https://amjidali.com)
- 🎓 [Learn on SyncBricks](https://lms.syncbricks.com)
- 📺 [SyncBricks YouTube Channel](https://youtube.com/@syncbricks)

---

> 🔐 Secure. 🔧 Flexible. 🌍 Accessible.
>  
> Deploy your automation like a pro.

