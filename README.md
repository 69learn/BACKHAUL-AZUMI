
نام پروژه : اسکریپت backhaul

<div align="right">
    <img src="https://github.com/69learn/6to4-azumi/blob/main/assets/119934376/project-management.png" alt="Video Title" width="100">
  </a>
</div>
  </details>
</div>
---------------------------------------------------------------

**نسخه v0.6.5 اپدیت شد**

**ده سرور ایران و یک کلاینت خارج اضافه شد**

**مشکل ipv6 حل شد و aggressive pool هم اضافه شد**( از داخل edit هم میتوانید از ایپی 4 به 6 یا برعکس تغییر بدهید)

**ویرایش ریست تایمر اضافه شد**


**امکانات**
-----------------------
<div align="right">
    <img src="https://github.com/69learn/6to4-azumi/blob/main/assets/119934376/ability.png" alt="Video Title" width="100">
  </a>
</div>
  </details>
</div>

-----------------------

- ریورس تانل به صورت single یا multi
- یک سرور ایران و ده کلاینت خارج
- ده سرور ایران و یک کلاینت خارج
- مانیتور پورت توسط tcpdump (تست)
- دارای ویرایش تمام سرور ها و کلاینت ها
- دارای status و نمایش لاگ ها
- پشتیبانی از ws, wss, tcp, tcpmux, wsmux, wssmux و udp
- پورت فوروارد و امکان فوروارد پورت از یک ایپی بر روی ایپی دیگر
- امکان استفاده از لوکال ایپی ها به همراه این تانل
- داری حذف کامل تانل
- داری retry interval و mux
- پشتیبانی از nodelay
- پشتیبانی از selft signed certs
- پشتیبانی از authentication token
- دارای ریست تایمر بر حسب دقیقه یا ساعت
- پشتیبانی از Port range
- دارای ویرایش ریست تایمر برای single و multi
- پشتیبانی از arm64 / amd64

------------------------------------------------------


 <div align="right">
  <details>
    <summary><strong><img src="https://github.com/69learn/6to4-azumi/blob/main/assets/119934376/warning.png" width="40" alt="Image"> </strong>نکات</summary>


- ادرس cert ها در این مکان میباشد  < /etc/backhaul
- ادرس sniff در حالت single در این directory میباشد > /etc/backhaul.json
- ادرس sniff در حالت multi در این directory میباشد > /etc/backhaul_server1.json  یا /etc/backhaul_client1.json
- در حالت مولتی هر کانفیگ در سرور ایران برای یک کلاینت خارج میباشد. به عبارتی اگر دو کلاینت خارج دارم، پس باید در سرور ایران دو کانفیگ داشته باشم
- در حالت مولتی، برای 10 سرور ایران و یک کلاینت خارج : برای هر تعداد سرور ایران، یک کانفیگ در کلاینت خارج میخواهیم. به عبارتی اگر 3 سرور ایران دارم در کلاینت خارج، 3 کانفیگ خواهم داشت. اموزش آن مانند 1 سرور ایران و 10 کلاینت خارج میباشد
- برای تغییر یا ویرایش پس از انجام تغییرات، گزینه save را بزنید

  </details>
</div>
  
 ------------------------
 <div align="right">
  <details>
    <summary><strong><img src="https://github.com/69learn/6to4-azumi/blob/main/assets/119934376/youtube.png" width="40" alt="Image"> ویدیوهای آموزشی</strong></summary>
------------------------------------  
- ویدیوی آموزشی توسط 69

<div align="right">
  <a href="https://www.youtube.com/watch?v=AjNrYOpNaQE">
    <img src="https://github.com/69learn/6to4-azumi/blob/main/assets/119934376/backhaul.jpg" alt="Video Title" width="300">
  </a>
</div>
  </details>
</div>


------------------------ 
------------------------
 <div align="right">
  <details>
    <summary><strong><img src="https://github.com/69learn/6to4-azumi/blob/main/assets/119934376/script.png" width="40" alt="Image">اسکریپت من</strong></summary>
------------------------------------   

- نصب پیش نیاز ها
```
apt install python3 -y && sudo apt install python3-pip &&  pip install colorama && pip install netifaces && apt install curl -y
pip3 install colorama
sudo apt-get install python-pip -y  &&  apt-get install python3 -y && alias python=python3 && python -m pip install colorama && python -m pip install netifaces
sudo apt update -y && sudo apt install -y python3 python3-pip curl && pip3 install --upgrade pip && pip3 install netifaces colorama requests

```
- اجرای اسکریپت
```
bash -c "$(curl -fsSL https://raw.githubusercontent.com/69learn/BACKHAUL-AZUMI/refs/heads/main/backhaul.sh)"
```
- در صورتی که سرور شما externally managed بود، از کامند زیر استفاده نمایید
```
bash -c "$(curl -fsSL https://raw.githubusercontent.com/69learn/BACKHAUL-AZUMI/refs/heads/main/managed.sh)"
```
---------------------------------------------
