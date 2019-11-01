# 🔒 Common Security Practices for NodeJS

## 1. Compromised Database 😱

1. Strongly encrypt passwords with salt and hash (bcrypt)
2. Strongly encrypt password reset tokens (SHA256)

## 2. Brute Force Attacks 💪🏽

- Use bcrypt (to make login requests slow)
- Implement rate limiting (express-rate-limit)
- Implement maximum login attempts

## 3. Cross-Site Scripting (XSS) Attacks ❌

- Store JWT in HTTPonly cookies
- Sanitize user input data
- Set Special HTTP headers (helmet package)

## 4. Denial-Of-Service (DOS) Attack ✋🏽

- Implement rate limiting (express-rate-limit)
- Limit body payload (in body-parser)
- Avoid evil regular expressions

## 5. Query Injection 💉

- Use mongoose for MongoDB (because of SchemaTypes)
- Use Sequelize for SQL
- Sanitize user input data

## 6. Other Best Practices and Suggestions ❓

- Always use HTTPS
- Create random password tokens with expiry dates
- Deny access to JWT after password change
- Don't commit sensitive data to Git
- Don't send error details to clients
- Prevent Cross-Site Request Forgery (csurf package)
- Require re-authentication before a high-value action e.g. making payment.
- Implement a blacklist of untrusted JWT
- Confirm user email address after first creating account
- Keep user logged in with refresh tokens
- Implement two-factor authentication
- Prevent parameter pollution causing Uncaught Exceptions

Credit: [Jonas Schmedtman](https://twitter.com/jonasschmedtman)
