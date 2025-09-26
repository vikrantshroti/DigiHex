# DigiHex

An **Android/iOS SDK** that enables execution of **cURL commands on mobile devices**. Currently, mobile vendors do not provide native support for cURL execution, making it difficult for developers and testers to measure critical network parameters directly from mobile apps.  

**DigiHex** bridges this gap by allowing apps to run cURL-like commands and fetch important diagnostic and performance metrics.  

⚠️ **Note:** This SDK is currently **internal only** and **not for public use**. Public release will be announced once it is production-ready.  

---

## 🚀 Features

- **Execute cURL commands on Android & iOS**  
- Extract and calculate crucial network parameters:  
  - TTL (Time To Live)  
  - DNS IP  
  - Public & Host IP  
  - Speed at Data Caching Centres  
  - Connection time, download speed, and response headers  
  - Other cURL-based performance insights  
- Lightweight and easy to integrate  
- Works offline (no vendor dependency)  

---

## 📦 Installation

Currently, installation is **restricted to internal use only**.  
Packages will not be available on **Maven Central**, **CocoaPods**, or **SPM** until public release.  

---

## 🛠️ Usage

### Android (Kotlin)

```kotlin
val result = DigiHex.execute("curl -I https://example.com")
println("DNS IP: ${result.dnsIp}")
println("TTL: ${result.ttl}")
println("Speed: ${result.speedAtCachingCenter}")
