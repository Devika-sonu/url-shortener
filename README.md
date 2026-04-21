<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/00539c9f-610e-489d-9aa1-ccf045e93641" /># URL Shortener Project

## Objective
Convert long URLs into short URLs and redirect to original link.

## How it Works
1. User enters a long URL
2. System generates a short code (example: abc123)
3. Store short code and long URL
4. When user opens short URL, redirect to original URL

## Example
abc123 → https://google.com

## Components
- User
- Backend (Java)
- Storage

## Optional Features
- Custom short URL
- Expiration time

## Technology Choice

### Java
I chose Java because:
- Strong backend support  
- Platform independent  
- Good performance  

### MySQL (Relational Database)
- Structured data  
- Easy to query using SQL  
- Supports constraints like UNIQUE  

---

## Database Schema

```sql
CREATE TABLE urls (
    id INT AUTO_INCREMENT PRIMARY KEY,
    short_code VARCHAR(10) UNIQUE NOT NULL,
    long_url TEXT NOT NULL,
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
    expiry_date TIMESTAMP NULL
);
```
