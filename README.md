<!-- # vps-hosting

1. linux_setup_configuration:
file name: vi setup.sh (ctrl+shift+v diye  file ta paste korbo, esc press and write :wq for save the file, press-> ls for seeing the file, run the file--> bash setup.sh, do you want to change default shell to zsh:y dibo, complete hole -> exit type dibo)

2. git_user_setup.sh:
file name: vi git.sh --> bash git.sh(q/a--> Github.com,HTTPS,Yes,login with a web browser)
press enter--> github.com/login/device
one time code:
SMTech24-official->continue
press enter: email--> github@smtech24.com, github username

3. folder create--
mkdir /var/www-->create
cd /var/www--> folder er moddhe
www pwd --> file er path
www git clone https...
www cd project_name-->cd ..
www clear

4. nginx deployment conf.d
www cd
pwd  (/root - e thakte hobe)
vi deploy.sh-->(ctrl+shift+v paste it )--> :wq for save --> run korar jonno -->bash deploy.sh

backend port:
domain name(http thaka jabe na)
email jekono(official dile better)

5. 
nginx create hoyeche ta dekhar jonno-->cd /etc/nginx/conf.d
conf.d ls
conf.d cat file_name  --> dekhar jonno
conf.d cd /var/www
www ls
www cd file name
ls

pnpm i &&pnpm prisma generate && pnpm build && pm2 restart ecosystem.config.js && systemctl restart nginx 

pnpm i && pnpm build && pm2 restart ecosystem.config.js && systemctl restart nginx 

pm2 restart ecosystem.config.js && systemctl restart nginx

pm2 logs number_dao


bcrypt error: npm rebuild bcrypt and again pnpm i ....

abar root e jete hobe frontend krte hole:
www cd --> bash deploy.sh
frontend port:
domain,email

6. frontnd run
cd /var/www
www ls
www cd file_name
prisma drkr nai frontend e

jodi ecosystem na thake

vi ecosystem.config.js file name diye pastre kore save korbo. 
then pnpm i .. chalabo and prisma chara

for not secure issue: sudo certbot -d domain_name -d www.domain_name

7. local db te mongodb er jonno jodi krte chai

mongod.sh--> root -e  korbo
cd
vi mongod.sh paste kore save kore
:wq
.env te gia url change kora 
 -->


# VPS Hosting Full Deployment Guide

## 1. Linux Setup Configuration
**File:** `setup.sh`
```bash
vi setup.sh
# (Ctrl + Shift + V to paste the script)
# Save: ESC → :wq → Enter
ls
bash setup.sh
# When asked: "Do you want to change default shell to zsh?" → type: y
exit
```

---

## 2. Git User Setup
**File:** `git.sh`
```bash
vi git.sh
# Paste script → save (:wq)
bash git.sh
```
Setup Steps:
- q / a → Github.com
- HTTPS
- Yes
- Login with browser
- Visit: https://github.com/login/device
- Enter One-time code
- Email: `github@smtech24.com`
- Username: Your GitHub username

---

## 3. Project Folder Setup
```bash
mkdir /var/www
cd /var/www
pwd
# clone project
git clone https://...
cd project_name
cd ..
clear
```

---

## 4. Nginx Deployment (conf.d)
**From root folder:**
```bash
cd
vi deploy.sh
# paste → :wq
bash deploy.sh
```
Inputs:
- Backend port
- Domain name (NO http/https)
- Email (official recommended)

---

## 5. Verify Nginx Setup
```bash
cd /etc/nginx/conf.d
ls
cat file_name.conf

cd /var/www
ls
cd project_name
ls
```

### Common Commands
```bash
pnpm i && pnpm prisma generate && pnpm build && pm2 restart ecosystem.config.js && systemctl restart nginx
pnpm i && pnpm build && pm2 restart ecosystem.config.js && systemctl restart nginx
pm2 restart ecosystem.config.js && systemctl restart nginx
pm2 logs <number>
```

### bcrypt error fix
```bash
npm rebuild bcrypt
pnpm i
```

### Frontend deploy (from root)
```bash
cd
bash deploy.sh
# Provide frontend port + domain + email
```

---

## 6. Frontend Run Guide
```bash
cd /var/www
ls
cd frontend_name
# No prisma needed in frontend
```
If ecosystem file missing:
```bash
vi ecosystem.config.js
# paste config → save
pnpm i
```
SSL Fix:
```bash
sudo certbot -d domain.com -d www.domain.com
```

---

## 7. Local MongoDB Setup
**File:** `mongod.sh`
```bash
cd
vi mongod.sh
# paste → save (:wq)
```
Update `.env` with new MongoDB URL.

---

This guide contains all deployment commands and setup steps in file form.

