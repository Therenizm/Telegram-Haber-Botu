# Telegram-Haber-Botu
Telegram Haber Botu Kurulum için Readme Aç




Telegram Haber Botu

Bu Python tabanlı bot, belirlediğiniz kategorilerde güncel haberleri otomatik olarak çekip, Telegram kanalınıza gönderir. Ayrıca günlük haber raporunu mail adresinize iletir. Kullanıcılar bot ile /dil komutunu kullanarak dil tercihlerini değiştirebilirler.



Özellikler

Çeşitli haber kategorileri: Genel, ekonomi, savaş, teknoloji gibi kategorilerde haber toplar.

Çoklu dil desteği: Türkçe ve İngilizce haber alma seçenekleri.

Telegram kanalına otomatik gönderim: Haberleri kanalınıza HTML formatında gönderir.

Günlük mail raporu: Gönderilen haberlerin günlük özeti mail adresinize iletilir.

Bitly link kısaltma (isteğe bağlı): Haber linklerini kısaltabilir.

Hata durumunda mail bildirimi: Bot hata aldığında size mail gönderir.

Kolay komut kontrolü: Kullanıcılar /dil [tr/en] komutu ile dil ayarlarını değiştirebilir.



Gereksinimler

Python 3.7+

Gmail hesabı (mail gönderimi için)

Telegram bot tokenı (BotFather'dan alınır)

Telegram kanal ID'si (haberlerin gönderileceği kanal)

NewsAPI API anahtarı (https://newsapi.org adresinden ücretsiz alınabilir)



Kurulum Adımları

1. Python Yükleme

Python bilgisayarınızda kurulu değilse, https://www.python.org/downloads/ adresinden Python 3.7 veya üzeri sürümü indirip kurun.

2. Gerekli Kütüphaneleri Yükleme

Terminal veya Komut İstemi'ni açarak aşağıdaki komutu çalıştırın:

pip install requests

requests kütüphanesi internet üzerinden API çağrıları yapmamızı sağlar.

3. Telegram Bot Token Alma

Telegram'da @BotFather hesabına gidin.

/newbot komutunu kullanarak yeni bot oluşturun.

Botunuz için bir isim ve kullanıcı adı belirleyin.

Size verilen token değerini not edin.


4. Telegram Kanal ID'sini Öğrenme

Kanalınıza botu yönetici olarak ekleyin.

Kanal ID'sini öğrenmek için farklı yöntemler var, en kolay yöntem:

Telegram’da @RawDataBot veya @userinfobot gibi botları kullanarak kanal ID'sini alabilirsiniz.

Kanal ID genellikle -100 ile başlayan uzun bir sayıdır.



5. NewsAPI Anahtarı Alma

https://newsapi.org/ adresine gidin.

Ücretsiz hesap oluşturun ve API anahtarınızı alın.


6. Gmail Ayarları

Gmail hesabınız için Uygulama Şifresi oluşturun (iki adımlı doğrulama açık olmalı).

Bu uygulama şifresini MAIL_PASSWORD olarak kullanacaksınız.


7. config Ayarları

Kod dosyanızda aşağıdaki yerleri kendi bilgilerinize göre değiştirin:

TOKEN = "BotFather'dan aldığınız Telegram bot tokeni"
MAIL_SENDER = "gmailadresiniz@gmail.com"
MAIL_PASSWORD = "gmail uygulama şifreniz"
MAIL_RECEIVER = "raporlar geleceği mail adresi"
NEWS_API_KEY = "NewsAPI'den aldığınız anahtar"
KANAL_ID = -100XXXXXXXXXX  # Telegram kanal ID'niz

8. Botu Çalıştırma

Terminal veya komut isteminde bot dosyasının bulunduğu klasöre gidin ve:

python botdosyasi.py

komutunu çalıştırın.

Bot 10 dakikada bir haberleri kontrol edecek ve yeni haberleri Telegram kanalınıza gönderecektir.



Komutlar

/dil tr — Haber dili Türkçe olur.

/dil en — Haber dili İngilizce olur.


Bilinmeyen komutlar veya diğer mesajlara bot yanıt vermez.



Öneriler ve İpuçları

Kodunuzu GitHub gibi herkese açık ortamlarda paylaşırken, API anahtarlarınızı, tokenlarınızı ve şifrelerinizi config dosyası veya ortam değişkenleriyle yönetin.

Telegram kanalınıza botu yönetici olarak eklemeyi unutmayın.

Mail gönderiminde hata almamak için Gmail uygulama şifresi kullanmanız önemli.

Haber kategorilerini ve anahtar kelimelerini KATEGORI_KEYWORDS sözlüğünden kolayca özelleştirebilirsiniz.



Lisans & İletişim

Bu bot therenizm tarafından geliştirilmiştir.

Herhangi bir sorun veya öneri için iletişime geçebilirsiniz.



🇺🇸 LANGUAGE



Telegram News Bot

This Python-based bot automatically fetches the latest news in specified categories and posts them to your Telegram channel. It also sends a daily news summary report to your email. Users can change the news language preference using the bot’s /dil command.



Features

Multiple news categories: General, Economy, War, Technology, etc.

Multi-language support: Get news in Turkish or English.

Automatic Telegram channel posting: Sends news in HTML format to your channel.

Daily email report: Sends a summary of the sent news to your email.

Optional Bitly link shortening: Shortens news URLs if configured.

Error notifications via email: Get notified by email if the bot encounters errors.

Simple user commands: Users can change language preference with /dil [tr/en].



Requirements

Python 3.7+

Internet connection

Gmail account (for sending emails)

Telegram bot token (obtained from BotFather)

Telegram channel ID (where news will be posted)

NewsAPI API key (free API key from https://newsapi.org)



Setup Instructions

1. Install Python

If Python is not installed on your machine, download and install Python 3.7 or higher from https://www.python.org/downloads/.

2. Install Required Libraries

Open your terminal or command prompt and run:

pip install requests

This installs the requests library used for making API requests.

3. Get Telegram Bot Token

Open Telegram and search for @BotFather.

Use the /newbot command to create a new bot.

Follow the instructions to name your bot and set a username.

Copy the token provided by BotFather.


4. Get Your Telegram Channel ID

Add your bot as an administrator to your Telegram channel.

To find your channel ID, you can use Telegram bots like @RawDataBot or @userinfobot.

The channel ID usually starts with -100 followed by numbers.


5. Get NewsAPI API Key

Visit https://newsapi.org/.

Create a free account and generate an API key.


6. Setup Gmail for Sending Emails

Enable two-factor authentication on your Gmail account.

Create an App Password for your Gmail (see Google’s instructions).

Use this app password as your MAIL_PASSWORD.


7. Configure the Bot Settings

In your Python script, update the following placeholders with your information:

TOKEN = "Your Telegram bot token from BotFather"
MAIL_SENDER = "yourgmail@gmail.com"
MAIL_PASSWORD = "your gmail app password"
MAIL_RECEIVER = "email_to_receive_daily_reports@example.com"
NEWS_API_KEY = "Your NewsAPI API key"
KANAL_ID = -100XXXXXXXXXX  # Your Telegram channel ID

8. Run the Bot

In the terminal, navigate to the folder containing the bot script and run:

python your_bot_script.py

The bot will check for new news every 10 minutes and send them to your Telegram channel.


Commands

/dil tr — Set news language to Turkish.

/dil en — Set news language to English.


Unknown commands or other messages will be ignored by the bot.


Tips & Recommendations

When sharing your code publicly (e.g., GitHub), never include your API keys, tokens, or passwords. Use environment variables or separate config files instead.

Make sure to add the bot as an admin to your Telegram channel so it can post messages.

Use Gmail app passwords for reliable email sending.

Customize your news categories and keywords in the KATEGORI_KEYWORDS dictionary.


License & Contact

This bot is developed by therenizm.

Feel free to reach out for issues or suggestions. 
