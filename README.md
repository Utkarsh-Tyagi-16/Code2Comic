# XKCD Comic Subscription Service

A PHP-based service that allows users to subscribe to daily XKCD comics via email. The service includes email verification, daily comic delivery, and an unsubscribe feature.

## 🌟 Features

- **Email Subscription**: Subscribe to receive daily XKCD comics
- **Email Verification**: Secure 6-digit verification code system
- **Daily Comics**: Receive a random XKCD comic every 24 hours
- **Easy Unsubscribe**: Simple one-click unsubscribe process with verification

## 🚀 Getting Started

### Prerequisites

- PHP 8.3 or higher
- Web server (Apache/Nginx)
- Mail server configuration

### Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/xkcd-comic-subscription.git
cd xkcd-comic-subscription
```

2. Configure your web server to point to the `src` directory

3. Set up the CRON job:
```bash
cd src
chmod +x setup_cron.sh
./setup_cron.sh
```

## 📧 How to Use

### Subscribe to Comics

1. Visit the homepage
2. Enter your email address
3. Check your inbox for a verification code
4. Enter the code to complete subscription

### Unsubscribe

1. Click the unsubscribe link in any comic email
2. Enter your email address
3. Check your inbox for a verification code
4. Enter the code to confirm unsubscription

## 🔧 Technical Details

- Uses PHP's native `mail()` function for sending emails
- Stores subscriber emails in `registered_emails.txt`
- Fetches comics from the XKCD API
- Sends HTML-formatted emails with comic images

## 📝 File Structure

```
src/
├── index.php              # Main subscription page
├── verify.php            # Email verification handler
├── unsubscribe.php       # Unsubscribe page
├── verify_unsubscribe.php # Unsubscribe verification
├── functions.php         # Core functionality
├── cron.php             # Daily comic sender
├── setup_cron.sh        # CRON job setup script
└── registered_emails.txt # Subscriber database
```

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

