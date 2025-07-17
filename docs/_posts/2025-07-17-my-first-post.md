---
title: "我的第一篇教學文章：用 Python 傳送 Email"
categories:
  - Python
tags:
  - email
  - 自動化
  - SMTP
---

在這篇文章中，我會教你如何用 Python 發送 Email，不需第三方平台，只要設定 Gmail 的應用程式密碼即可：

```python
import smtplib
from email.mime.text import MIMEText

msg = MIMEText("這是測試郵件")
msg["Subject"] = "測試主旨"
msg["From"] = "you@example.com"
msg["To"] = "target@example.com"

server = smtplib.SMTP_SSL("smtp.gmail.com", 465)
server.login("you@example.com", "你的應用程式密碼")
server.send_message(msg)
server.quit()

希望這篇對你有幫助，更多內容敬請期待！
