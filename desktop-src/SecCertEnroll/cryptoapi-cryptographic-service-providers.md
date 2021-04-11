---
description: I provider associati all'API di crittografia (CryptoAPI) sono detti provider del servizio di crittografia (CSP) in questa documentazione.
ms.assetid: 28c9d348-7a37-4346-8b75-396d1349b152
title: Provider del servizio di crittografia CryptoAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50b3820a0d45534bc5c492d843352be038f7ffc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129890"
---
# <a name="cryptoapi-cryptographic-service-providers"></a>Provider del servizio di crittografia CryptoAPI

I provider associati all'API di crittografia ([*CryptoAPI*](/windows/desktop/SecGloss/c-gly)) sono detti provider del servizio di crittografia (CSP) in questa documentazione. I CSP implementano in genere algoritmi crittografici e forniscono l'archiviazione delle chiavi. I provider associati a CNG, invece, separano l'implementazione dell'algoritmo dall'archiviazione delle chiavi. I CSP Microsoft seguenti sono distribuiti con Windows Vista e Windows Server 2008.

## <a name="microsoft-base-cryptographic-provider-v10"></a>Microsoft Base Cryptographic Provider v1.0

Implementa gli algoritmi seguenti per l'hashing, la firma e la crittografia del contenuto.



| Nome                                            | Uso          | Tipo  | Dimensioni chiave (valore predefinito/min/max) |
|-------------------------------------------------|--------------|-------|----------------------------|
| Data Encryption Standard (DES)                  | Crittografia   | Blocca | 56/56/56                   |
| Checksum di autenticazione del messaggio con hash (HMAC)   | Hashing      | Qualsiasi   | 0/0/0                      |
| Checksum di autenticazione messaggi (MAC)           | Hashing      | Qualsiasi   | 0/0/0                      |
| Messaggio digest 2 (MD2)                          | Hashing      | Qualsiasi   | 128/128/128                |
| Digest del messaggio 4 (MD4)                          | Hashing      | Qualsiasi   | 128/128/128                |
| Digest del messaggio 5 (MD5)                          | Hashing      | Qualsiasi   | 128/128/128                |
| RSA Data Security 2 (RC2)                       | Crittografia   | Blocca | 40/40/56                   |
| RSA Data Security 4 (RC4)                       | Crittografia   | Blocca | 40/40/56                   |
| Scambio di chiavi RSA                                | Scambio di chiave | RSA   | 512/384/1024               |
| Firma RSA                                   | per la firma      | RSA   | 512/384/16384              |
| Algoritmo Secure Hash Algorithm (SHA1)                    | Hashing      | Qualsiasi   | 160/160/160                |
| Secure Socket Layer 3 SHA e MD5 (SSL3 SHAMD5) | Hashing      | Qualsiasi   | 288/288/288                |



 

## <a name="microsoft-base-dss-and-diffie-hellman-cryptographic-provider"></a>Provider di crittografia di Microsoft Base DSS e Diffie-Hellman

Implementa gli algoritmi seguenti per supportare l'hashing, la firma, la crittografia e lo scambio di chiave Diffie-Hellman.



| Nome                                  | Uso          | Tipo           | Dimensioni chiave (valore predefinito/min/max) |
|---------------------------------------|--------------|----------------|----------------------------|
| Algoritmo di crittografia del messaggio CYLINK   | Crittografia   | Blocca          | 40/40/40                   |
| Data Encryption Standard (DES)        | Crittografia   | Blocca          | 56/56/56                   |
| Algoritmo di scambio delle chiavi Diffie-Hellman | Scambio di chiave | Diffie-Hellman | 512/512/1024               |
| Algoritmo effimero Diffie-Hellman    | Scambio di chiave | Diffie-Hellman | 512/512/1024               |
| Algoritmo di firma digitale (DSA)     | per la firma      | DSS            | 1024/512/1024              |
| Digest del messaggio 5 (MD5)                | Hashing      | Qualsiasi            | 128/128/128                |
| RSA Data Security 2 (RC2)             | Crittografia   | Blocca          | 40/40/56                   |
| RSA Data Security 4 (RC4)             | Crittografia   | Stream         | 40/40/56                   |
| Algoritmo Secure Hash Algorithm (SHA1)          | Hashing      | Qualsiasi            | 160/160/160                |



 

## <a name="microsoft-base-dss-cryptographic-provider"></a>Microsoft Base DSS Cryptographic Provider

Implementa gli algoritmi seguenti per la firma e il contenuto hash:



| Nome                              | Uso     | Tipo | Dimensioni chiave (valore predefinito/min/max) |
|-----------------------------------|---------|------|----------------------------|
| Algoritmo di firma digitale (DSA) | per la firma | DSS  | 1024/512/1024              |
| Digest del messaggio 5 (MD5)            | Hashing | Qualsiasi  | 128/128/128                |
| Algoritmo Secure Hash Algorithm (SHA1)      | Hashing | Qualsiasi  | 160/160/160                |



 

## <a name="microsoft-base-smart-card-crypto-provider"></a>Microsoft Base Smart Card Crypto Provider

Supporta le smart card e implementa gli algoritmi seguenti per l'hashing, la firma e la crittografia del contenuto.

| Nome                                            | Uso          | Tipo   | Dimensioni chiave (valore predefinito/min/max) |
|-------------------------------------------------|--------------|--------|----------------------------|
| Advanced Encryption Standard 128 (AES128)       | Crittografia   | Blocca  | 128/128/128                |
| Advanced Encryption Standard 192 (AES192)       | Crittografia   | Blocca  | 192/192/192                |
| Advanced Encryption Standard 256 (AES256)       | Crittografia   | Blocca  | 256/256/256                |
| Data Encryption Standard (DES)                  | Crittografia   | Blocca  | 56/56/56                   |
| Due triple DES chiave                              | Crittografia   | Blocca  | 112/112/112                |
| Tre chiavi Triple DES                            | Crittografia   | Blocca  | 168/168/168                |
| Checksum di autenticazione del messaggio con hash (HMAC)   | Hashing      | Qualsiasi    | 0/0/0                      |
| Checksum di autenticazione messaggi (MAC)           | Hashing      | Qualsiasi    | 0/0/0                      |
| Messaggio digest 2 (MD2)                          | Hashing      | Qualsiasi    | 128/128/128                |
| Digest del messaggio 4 (MD4)                          | Hashing      | Qualsiasi    | 128/128/128                |
| Digest del messaggio 5 (MD5)                          | Hashing      | Qualsiasi    | 128/128/128                |
| RSA Data Security 2 (RC2)                       | Crittografia   | Blocca  | 128/40/128                 |
| RSA Data Security 4 (RC4)                       | Crittografia   | Stream | 128/40/128                 |
| Scambio di chiavi RSA                                | Scambio di chiave | RSA    | 1024/1024/4096             |
| Firma RSA                                   | per la firma      | RSA    | 1024/1024/4096             |
| Algoritmo Secure Hash Algorithm (SHA1)                    | Hashing      | Qualsiasi    | 160/160/160                |
| Algoritmo Secure Hash Algorithm 256 (SHA256)              | Hashing      | Qualsiasi    | 256/256/256                |
| Algoritmo Secure Hash Algorithm 384 (SHA384)              | Hashing      | Qualsiasi    | 384/384/384                |
| Algoritmo Secure Hash Algorithm 512 (SHA512)              | Hashing      | Qualsiasi    | 512/512/512                |
| Secure Socket Layer 3 SHA e MD5 (SSL3 SHAMD5) | Hashing      | Qualsiasi    | 288/288/288                |



 

## <a name="microsoft-dh-schannel-cryptographic-provider"></a>Provider di crittografia Microsoft DH SChannel

Supporta il pacchetto di sicurezza del canale sicuro (Schannel) che implementa i protocolli di autenticazione di Secure Sockets Layer (SSL) e Transport Layer Security (TLS). Questo CSP supporta inoltre Diffie-Hellman scambio di chiave e implementa gli algoritmi seguenti.



| Nome                                   | Uso                | Tipo           | Dimensioni chiave (valore predefinito/min/max) |
|----------------------------------------|--------------------|----------------|----------------------------|
| Algoritmo di crittografia del messaggio CYLINK    | Crittografia         | Blocca          | 40/40/40                   |
| Data Encryption Standard (DES)         | Crittografia         | Blocca          | 56/56/56                   |
| Due triple DES chiave                     | Crittografia         | Blocca          | 112/112/112                |
| Tre chiavi Triple DES                   | Crittografia         | Blocca          | 168/168/168                |
| Algoritmo di scambio delle chiavi Diffie-Hellman  | Scambio di chiave       | Diffie-Hellman | 512/512/4096               |
| Algoritmo effimero Diffie-Hellman     | Scambio di chiave       | Diffie-Hellman | 512/512/4096               |
| Algoritmo di firma digitale (DSA)      | per la firma            | DSS            | 1024/512/1024              |
| Digest del messaggio 5 (MD5)                 | Hashing            | Qualsiasi            | 128/128/128                |
| RSA Data Security 2 (RC2)              | Crittografia         | Blocca          | 40/40/128                  |
| RSA Data Security 4 (RC4)              | Crittografia         | Stream         | 40/40/128                  |
| Algoritmo Secure Hash Algorithm (SHA1)           | Hashing            | Qualsiasi            | 160/160/160                |
| Chiave di crittografia Schannel                | Crittografia         | SChannel       | 0/0/-1                     |
| Chiave MAC Schannel                       | Crittografia/hashing | SChannel       | 0/0/-1                     |
| Hash Master Schannel                   | Crittografia/hashing | SChannel       | 0/0/-1                     |
| Master Secure Sockets Layer (SSL3)     | Crittografia         | SChannel       | 384/384/384                |
| Master Transport Layer Security (TLS1) | Crittografia         | SChannel       | 384/384/384                |



 

## <a name="microsoft-enhanced-cryptographic-provider-v10"></a>Microsoft Enhanced Cryptographic Provider v1.0

Offre una sicurezza più avanzata rispetto a Microsoft Base Cryptographic Provider v 1.0 utilizzando chiavi più lunghe con alcuni degli algoritmi esistenti e implementando algoritmi aggiuntivi.



| Nome                                            | Uso          | Tipo   | Dimensioni chiave (valore predefinito/min/max) |
|-------------------------------------------------|--------------|--------|----------------------------|
| Data Encryption Standard (DES)                  | Crittografia   | Blocca  | 56/56/56                   |
| Due triple DES chiave                              | Crittografia   | Blocca  | 112/112/112                |
|                                                 | Crittografia   | Blocca  | 168/168/168                |
| Checksum di autenticazione del messaggio con hash (HMAC)   | Hashing      | Qualsiasi    | 0/0/0                      |
| Checksum di autenticazione messaggi (MAC)           | Hashing      | Qualsiasi    | 0/0/0                      |
| Messaggio digest 2 (MD2)                          | Hashing      | Qualsiasi    | 128/128/128                |
| Digest del messaggio 4 (MD4)                          | Hashing      | Qualsiasi    | 128/128/128                |
| Digest del messaggio 5 (MD5)                          | Hashing      | Qualsiasi    | 128/128/128                |
| RSA Data Security 2 (RC2)                       | Crittografia   | Blocca  | 128/40/128                 |
| RSA Data Security 4 (RC4)                       | Crittografia   | Stream | 128/40/128                 |
| Scambio di chiavi RSA                                | Scambio di chiave | RSA    | 1024/384/16384             |
| Firma RSA                                   | per la firma      | RSA    | 1024/384/16384             |
| Algoritmo di hash sicuro (SHA1)                     | Hashing      | Qualsiasi    | 160/160/160                |
| Secure Socket Layer 3 SHA e MD5 (SSL3 SHAMD5) | Hashing      | Qualsiasi    | 288/288/288                |



 

## <a name="microsoft-enhanced-dss-and-diffie-hellman-cryptographic-provider"></a>Microsoft Enhanced DSS e Diffie-Hellman provider di crittografia

Offre una sicurezza più avanzata rispetto a Microsoft Base DSS e Diffie-Hellman CSP del provider di crittografia usando chiavi più lunghe con alcuni degli algoritmi esistenti e implementando algoritmi aggiuntivi.



| Nome                                  | Uso          | Tipo           | Dimensioni chiave (valore predefinito/min/max) |
|---------------------------------------|--------------|----------------|----------------------------|
| Algoritmo di crittografia del messaggio CYLINK   | Crittografia   | Blocca          | 40/40/40                   |
| Data Encryption Standard (DES)        | Crittografia   | Blocca          | 56/56/56                   |
| Due triple DES chiave                    | Crittografia   | Blocca          | 112/112/112                |
| Tre chiavi Triple DES                  | Crittografia   | Blocca          | 168/168/168                |
| Algoritmo di scambio delle chiavi Diffie-Hellman | Scambio di chiave | Diffie-Hellman | 1024/512/4096              |
| Algoritmo effimero Diffie-Hellman    | Scambio di chiave | Diffie-Hellman | 1024/512/4096              |
| Algoritmo di firma digitale (DSA)     | per la firma      | DSS            | 1024/512/1024              |
| Digest del messaggio 5 (MD5)                | Hashing      | Qualsiasi            | 128/128/128                |
| RSA Data Security 2 (RC2)             | Crittografia   | Blocca          | 128/128/128                |
| RSA Data Security 4 (RC4)             | Crittografia   | Stream         | 128/128/128                |
| Algoritmo Secure Hash Algorithm (SHA1)          | Hashing      | Qualsiasi            | 160/160/160                |



 

## <a name="microsoft-enhanced-rsa-and-aes-cryptographic-provider"></a>Microsoft Enhanced RSA e AES Cryptographic Provider

Implementa gli algoritmi seguenti per la firma, la crittografia e il contenuto hash.



| Nome                                            | Uso          | Tipo   | Dimensioni chiave (valore predefinito/min/max) |
|-------------------------------------------------|--------------|--------|----------------------------|
| Advanced Encryption Standard 128 (AES128)       | Crittografia   | Blocca  | 128/128/128                |
| Advanced Encryption Standard 192 (AES192)       | Crittografia   | Blocca  | 192/192/192                |
| Advanced Encryption Standard 256 (AES256)       | Crittografia   | Blocca  | 256/256/256                |
| Data Encryption Standard (DES)                  | Crittografia   | Blocca  | 56/56/56                   |
| Due triple DES chiave                              | Crittografia   | Blocca  | 112/112/112                |
| Tre chiavi Triple DES                            | Crittografia   | Blocca  | 168/168/168                |
| Checksum di autenticazione del messaggio con hash (HMAC)   | Hashing      | Qualsiasi    | 0/0/0                      |
| Checksum di autenticazione messaggi (MAC)           | Hashing      | Qualsiasi    | 0/0/0                      |
| Messaggio digest 2 (MD2)                          | Hashing      | Qualsiasi    | 128/128/128                |
| Digest del messaggio 4 (MD4)                          | Hashing      | Qualsiasi    | 128/128/128                |
| Digest del messaggio 5 (MD5)                          | Hashing      | Qualsiasi    | 128/128/128                |
| RSA Data Security 2 (RC2)                       | Crittografia   | Blocca  | 128/128/128                |
| RSA Data Security 4 (RC4)                       | Crittografia   | Stream | 128/128/128                |
| Scambio di chiavi RSA                                | Scambio di chiave | RSA    | 1024/384/16384             |
| Firma RSA                                   | per la firma      | RSA    | 1024/384/16384             |
| Algoritmo Secure Hash Algorithm (SHA1)                    | Hashing      | Qualsiasi    | 160/160/160                |
| Algoritmo Secure Hash Algorithm (SHA256)                  | Hashing      | Qualsiasi    | 256/256/256                |
| Algoritmo Secure Hash Algorithm (SHA384)                  | Hashing      | Qualsiasi    | 384/384/384                |
| Algoritmo Secure Hash Algorithm (SHA512)                  | Hashing      | Qualsiasi    | 512/512/512                |
| Secure Socket Layer 3 SHA e MD5 (SSL3 SHAMD5) | Hashing      | Qualsiasi    | 288/288/288                |



 

## <a name="microsoft-rsa-schannel-cryptographic-provider"></a>Provider di crittografia Microsoft RSA SChannel

Supporta il pacchetto di sicurezza di RSA Secure Channel (Schannel) che implementa i protocolli di autenticazione di Secure Sockets Layer (SSL) e Transport Layer Security (TLS).



| Nome                                            | Uso                | Tipo     | Dimensioni chiave (valore predefinito/min/max) |
|-------------------------------------------------|--------------------|----------|----------------------------|
| Advanced Encryption Standard 128 (AES128)       | Crittografia         | Blocca    | 128/128/128                |
| Advanced Encryption Standard 256 (AES256)       | Crittografia         | Blocca    | 256/256/256                |
| Data Encryption Standard (DES)                  | Crittografia         | Blocca    | 56/56/56                   |
| Due triple DES chiave                              | Crittografia         | Blocca    | 112/112/112                |
| Tre chiavi Triple DES                            | Crittografia         | Blocca    | 168/168/168                |
| Checksum di autenticazione del messaggio con hash (HMAC)   | Hashing            | Qualsiasi      | 0/0/0                      |
| Checksum di autenticazione messaggi (MAC)           | Hashing            | Qualsiasi      | 0/0/0                      |
| Digest del messaggio 5 (MD5)                          | Hashing            | Qualsiasi      | 128/128/128                |
| RSA Data Security 2 (RC2)                       | Crittografia         | Blocca    | 128/128/128                |
| RSA Data Security 4 (RC4)                       | Crittografia         | Stream   | 128/128/128                |
| Scambio di chiavi RSA                                | Scambio di chiave       | RSA      | 1024/384/16384             |
| Chiave di crittografia Schannel                         | Crittografia         | SChannel | 0/0/-1                     |
| Hash Master Schannel                            | Crittografia/hashing | SChannel | 0/0/-1                     |
| Chiave MAC Schannel                                | Crittografia/hashing | SChannel | 0/0/-1                     |
| Algoritmo Secure Hash Algorithm (SHA1)                    | Hashing            | Qualsiasi      | 160/160/160                |
| Master Secure Socket Layer 2 (SSL2)             | Crittografia         | SChannel | 40/40/192                  |
| Master Secure Socket Layer 3 (SSL3)             | Crittografia         | SChannel | 384/384/384                |
| Secure Socket Layer 3 SHA e MD5 (SSL3 SHAMD5) | Hashing            | Qualsiasi      | 288/288/288                |
| Master Transport Layer Security (TLS1)          | Crittografia         | SChannel | 384/384/384                |



 

## <a name="microsoft-strong-cryptographic-provider"></a>Microsoft Strong Cryptographic Provider

Implementa gli algoritmi seguenti.



| Nome                                            | Uso          | Tipo   | Dimensioni chiave (valore predefinito/min/max) |
|-------------------------------------------------|--------------|--------|----------------------------|
| Data Encryption Standard (DES)                  | Crittografia   | Blocca  | 56/56/56                   |
| Due triple DES chiave                              | Crittografia   | Blocca  | 112/112/112                |
| Tre chiavi Triple DES                            | Crittografia   | Blocca  | 168/168/168                |
| Checksum di autenticazione del messaggio con hash (HMAC)   | Hashing      | Qualsiasi    | 0/0/0                      |
| Checksum di autenticazione messaggi (MAC)           | Hashing      | Qualsiasi    | 0/0/0                      |
| Messaggio digest 2 (MD2)                          | Hashing      | Qualsiasi    | 128/128/128                |
| Digest del messaggio 4 (MD4)                          | Hashing      | Qualsiasi    | 128/128/128                |
| Digest del messaggio 5 (MD5)                          | Hashing      | Qualsiasi    | 128/128/128                |
| RSA Data Security 2 (RC2)                       | Crittografia   | Blocca  | 128/40/128                 |
| RSA Data Security 4 (RC4)                       | Crittografia   | Stream | 128/40/128                 |
| Scambio di chiavi RSA                                | Scambio di chiave | RSA    | 1024/384/16384             |
| Firma RSA                                   | per la firma      | RSA    | 1024/384/16384             |
| Algoritmo Secure Hash Algorithm (SHA1)                    | Hashing      | Qualsiasi    | 160/160/160                |
| Secure Socket Layer 3 SHA e MD5 (SSL3 SHAMD5) | Hashing      | Qualsiasi    | 288/288/288                |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sui provider di crittografia](understanding-cryptographic-providers.md)
</dt> </dl>

 

 
