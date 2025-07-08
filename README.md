 **Linux daemon control commands** you should know. These are used to start, stop, reload, enable, disable, or check the status of system services (daemons):

---

## 📜 Linux Daemon Control Commands

---

### ✅ Using **systemd (systemctl)**

*Modern Linux distributions like RHEL 7+, CentOS 7+, Ubuntu 16.04+*

| Command                                    | Purpose                          |
| :----------------------------------------- | :------------------------------- |
| `sudo systemctl start <service>`           | Start a service immediately      |
| `sudo systemctl stop <service>`            | Stop a service immediately       |
| `sudo systemctl restart <service>`         | Restart a running service        |
| `sudo systemctl reload <service>`          | Reload config without stopping   |
| `sudo systemctl enable <service>`          | Enable service at system startup |
| `sudo systemctl disable <service>`         | Disable service from auto-start  |
| `sudo systemctl status <service>`          | Show current status of service   |
| `sudo systemctl is-enabled <service>`      | Check if service is enabled      |
| `sudo systemctl is-active <service>`       | Check if service is active       |
| `sudo systemctl list-units --type=service` | List all active services         |
| `sudo systemctl daemon-reload`             | Reload systemd manager config    |

---

### ✅ Using **service**

*Legacy systems like RHEL 6, CentOS 6, older Ubuntu*

| Command                          | Purpose             |
| :------------------------------- | :------------------ |
| `sudo service <service> start`   | Start a service     |
| `sudo service <service> stop`    | Stop a service      |
| `sudo service <service> restart` | Restart a service   |
| `sudo service <service> status`  | Show service status |

---

### ✅ Managing Daemon Logs

| Command                      | Purpose                             |
| :--------------------------- | :---------------------------------- |
| `journalctl -u <service>`    | View logs for a systemd service     |
| `journalctl -xe`             | View latest system log with details |
| `tail -f /var/log/<logfile>` | Follow a traditional log file       |

---

### ✅ Background Daemon Execution

| Command             | Purpose                     |                                    |
| :------------------ | :-------------------------- | ---------------------------------- |
| `<command> &`       | Run a command in background |                                    |
| `nohup <command> &` | Run ignoring hangups        |                                    |
| \`ps aux            | grep <service>\`            | Check if daemon process is running |
| `kill <pid>`        | Stop a process by PID       |                                    |

---

## 📌 Example

```bash
sudo systemctl restart nginx
sudo systemctl enable nginx
journalctl -u nginx
```
## 👨‍💻 Author

**Atul Kamble**

- 🌐 [Website](https://www.atulkamble.in)
- 🐙 [GitHub](https://github.com/atulkamble)
- 🐦 [X](https://x.com/Atul_Kamble)
- 💼 [LinkedIn](https://www.linkedin.com/in/atuljkamble)
- 📷 [Instagram](https://www.instagram.com/atuljkamble)
