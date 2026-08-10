# Voucher Bot

Telegram bot for Ruijie WiFiDog voucher brute force.

## Railway Deploy

1. **GitHub မှာ repo တင်ပါ**
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git branch -M main
   git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO.git
   git push -u origin main
   ```

2. **Railway မှာ New Project → Deploy from GitHub repo**

3. **Variables ထည့်ပါ (Settings → Variables)**
   ```
   BOT_TOKEN = သင့်ရဲ့bot_token
   ADMIN_ID  = သင့်ရဲ့telegram_user_id
   ```
   `PORT` နဲ့ `CONCURRENCY` ကို မထည့်ရင် default အလုပ်လုပ်ပါမယ်။

4. **Deploy**

## Environment Variables

| Variable | Required | Default | Description |
|----------|----------|---------|-------------|
| `BOT_TOKEN` | ✅ | - | Telegram Bot Token |
| `ADMIN_ID` | ✅ | - | Telegram Admin User ID |
| `PORT` | ❌ | `8080` | Web server port (Railway auto-assigns) |
| `CONCURRENCY` | ❌ | `80` | Max concurrent requests |

## Commands

- `/start` - Bot စတင်
- `/help` - အသုံးပြုနည်း
- `/setup <url>` - Session URL ထည့်ရန်
- `/brute <mode> <length> [target]` - Brute force စတင်
- `/stop` - ရပ်တန့်
- `/resume` - ဆက်လက်
- `/status` - အခြေအနေ
- `/saved` - ရလဒ်များ
- `/delete_saved` - ရလဒ်ဖျက်
- `/recheck` - ပြန်စစ်
- `/notify` - Notification ON/OFF
