# 🕸️ Web Scraping Notes (Beginner → Advanced)

---

## 📌 1. What is Web Scraping?

**Web Scraping = Website se data automatically extract karna**

Instead of:

* Copy-paste ❌

We use:

* Code to fetch data ✅

---

## 🌐 2. How Web Works (Basic Flow)

```
Browser → Request → Server → HTML → Render UI
```

👉 Scraping me:

* Browser ki jagah **code request bhejta hai**
* HTML directly milta hai

---

## 🧱 3. Core Concept

👉 **HTML = Data ka source**

Example:

```html
<div class="product">
  <h2>iPhone 15</h2>
  <span class="price">₹80,000</span>
</div>
```

👉 Extract:

* Name → `h2`
* Price → `.price`

---

## ⚙️ 4. Scraping Process (Step-by-Step)

### 1. Request bhejna

```js
axios.get(url)
```

### 2. HTML load karna

```js
const $ = cheerio.load(html);
```

### 3. Data find karna

```js
$(".price").text()
```

### 4. Data store/use karna

* DB me save
* API me send
* UI me show

---

## 🟢 5. Static vs Dynamic Websites

### ✅ Static Website

* Data HTML me hota hai
* Easy scraping

Examples:

* Blogs
* Simple sites

---

### 🔴 Dynamic Website

* Data JavaScript se load hota hai
* HTML me directly nahi milta

Examples:

* Flipkart
* Instagram

---

## 🔥 6. Dynamic Website se Data Kaise Le?

### ✔ Method 1: Browser Automation

* Puppeteer / Playwright
* Real browser ki tarah kaam karta hai

```js
await page.goto(url);
await page.waitForSelector(".price");
```

---

### ✔ Method 2: API Reverse Engineering (BEST)

Steps:

1. Inspect → Network tab
2. XHR / Fetch filter
3. API URL copy

```js
axios.get("API_URL")
```

👉 Direct JSON milta hai (fast + clean)

---

## 🛠️ 7. Tools & Libraries

### JavaScript:

* Axios → request bhejne ke liye
* Cheerio → HTML parse
* Puppeteer → browser automation

### Python:

* BeautifulSoup
* Scrapy

---

## 🔄 8. Scraping Types

### 1. One-time Scraping

* Ek baar data nikala

### 2. Scheduled Scraping

```js
setInterval(scrape, 5000);
```

### 3. Real-time Scraping

* Continuous updates
* Live systems

---

## 🏗️ 9. Architecture

```
Website → Scraper → Backend → Database → API → Frontend
```

---

## ⚠️ 10. Challenges

### ❌ Anti-Scraping

* CAPTCHA
* IP Block

### ❌ HTML Changes

* Selectors break ho jate hain

### ❌ Legal Issues

* Terms & Conditions check karo

---

## 💡 11. Best Practices

* Always check robots.txt
* API mile to scraping mat karo
* Delay use karo (rate limit)

```js
await new Promise(r => setTimeout(r, 2000));
```

---

## 🚀 12. Real Project Use Cases

* Price comparison apps
* News aggregator
* Job listing scraper
* Data analytics tools

---

## 📌 13. Summary

👉 Web scraping = HTML se data nikalna
👉 Static = easy
👉 Dynamic = Puppeteer ya API
👉 Best = API approach



