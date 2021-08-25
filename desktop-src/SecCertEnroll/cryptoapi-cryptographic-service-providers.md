---
description: I provider associati all'API di crittografia (CryptoAPI) sono denominati provider del servizio di crittografia (CSP) in questa documentazione.
ms.assetid: 28c9d348-7a37-4346-8b75-396d1349b152
title: Provider del servizio di crittografia CryptoAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32c095fe4801cd57d4665fed0deec1649eb0a64420c13e4e5f486c7afc805447
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119906581"
---
# <a name="cryptoapi-cryptographic-service-providers"></a>Provider del servizio di crittografia CryptoAPI

I provider associati all'API di crittografia [*(CryptoAPI)*](/windows/desktop/SecGloss/c-gly)sono denominati provider del servizio di crittografia (CSP) in questa documentazione. I CSP in genere implementano algoritmi di crittografia e forniscono l'archiviazione delle chiavi. I provider associati a CNG, d'altra parte, separano l'implementazione dell'algoritmo dall'archiviazione delle chiavi. I CSP Microsoft seguenti vengono distribuiti con Windows Vista e Windows Server 2008.

## <a name="microsoft-base-cryptographic-provider-v10"></a>Microsoft Base Cryptographic Provider v1.0

Implementa gli algoritmi seguenti per l'hashing, la firma e la crittografia del contenuto.



| Nome                                            | Uso          | Tipo  | Dimensioni chiave (predefinito/min/max) |
|-------------------------------------------------|--------------|-------|----------------------------|
| Data Encryption Standard (DES)                  | Crittografia   | Blocca | 56/56/56                   |
| Hashed Message Authentication Checksum (HMAC)   | Hashing      | Qualsiasi   | 0/0/0                      |
| Checksum di autenticazione dei messaggi (MAC)           | Hashing      | Qualsiasi   | 0/0/0                      |
| Message Digest 2 (MD2)                          | Hashing      | Qualsiasi   | 128/128/128                |
| Message Digest 4 (MD4)                          | Hashing      | Qualsiasi   | 128/128/128                |
| Message Digest 5 (MD5)                          | Hashing      | Qualsiasi   | 128/128/128                |
| RSA Data Security 2 (RC2)                       | Crittografia   | Blocca | 40/40/56                   |
| RSA Data Security 4 (RC4)                       | Crittografia   | Blocca | 40/40/56                   |
| Chiave RSA Exchange                                | Scambio di chiave | RSA   | 512/384/1024               |
| Firma RSA                                   | per la firma      | RSA   | 512/384/16384              |
| Secure Hash Algorithm (SHA1)                    | Hashing      | Qualsiasi   | 160/160/160                |
| Secure Socket Layer 3 SHA e MD5 (SSL3 SHAMD5) | Hashing      | Qualsiasi   | 288/288/288                |



 

## <a name="microsoft-base-dss-and-diffie-hellman-cryptographic-provider"></a>Microsoft Base DSS e Diffie-Hellman Cryptographic Provider

Implementa gli algoritmi seguenti per supportare l'hashing, la firma, la crittografia e Diffie-Hellman scambio di chiavi.



| Nome                                  | Uso          | Tipo           | Dimensioni chiave (predefinito/min/max) |
|---------------------------------------|--------------|----------------|----------------------------|
| Algoritmo CYLINK Message Encryption   | Crittografia   | Blocca          | 40/40/40                   |
| Data Encryption Standard (DES)        | Crittografia   | Blocca          | 56/56/56                   |
| Diffie-Hellman algoritmo di Exchange chiave | Scambio di chiave | Diffie-Hellman | 512/512/1024               |
| Diffie-Hellman algoritmo ffemero    | Scambio di chiave | Diffie-Hellman | 512/512/1024               |
| Algoritmo di firma digitale (DSA)     | per la firma      | Dss            | 1024/512/1024              |
| Message Digest 5 (MD5)                | Hashing      | Qualsiasi            | 128/128/128                |
| RSA Data Security 2 (RC2)             | Crittografia   | Blocca          | 40/40/56                   |
| RSA Data Security 4 (RC4)             | Crittografia   | Stream         | 40/40/56                   |
| Secure Hash Algorithm (SHA1)          | Hashing      | Qualsiasi            | 160/160/160                |



 

## <a name="microsoft-base-dss-cryptographic-provider"></a>Microsoft Base DSS Cryptographic Provider

Implementa gli algoritmi seguenti per firmare e hashare il contenuto:



| Nome                              | Uso     | Tipo | Dimensioni chiave (impostazione predefinita/min/max) |
|-----------------------------------|---------|------|----------------------------|
| Algoritmo di firma digitale (DSA) | per la firma | Dss  | 1024/512/1024              |
| Message Digest 5 (MD5)            | Hashing | Qualsiasi  | 128/128/128                |
| Algoritmo hash sicuro (SHA1)      | Hashing | Qualsiasi  | 160/160/160                |



 

## <a name="microsoft-base-smart-card-crypto-provider"></a>Microsoft Base Smart Card Crypto Provider

Supporta le smart card e implementa gli algoritmi seguenti per l'hash, la firma e la crittografia del contenuto.

| Nome                                            | Uso          | Tipo   | Dimensioni chiave (impostazione predefinita/min/max) |
|-------------------------------------------------|--------------|--------|----------------------------|
| Advanced Encryption Standard 128 (AES128)       | Crittografia   | Blocca  | 128/128/128                |
| Advanced Encryption Standard 192 (AES192)       | Crittografia   | Blocca  | 192/192/192                |
| Advanced Encryption Standard 256 (AES256)       | Crittografia   | Blocca  | 256/256/256                |
| Data Encryption Standard (DES)                  | Crittografia   | Blocca  | 56/56/56                   |
| Des con tripla chiave a due chiavi                              | Crittografia   | Blocca  | 112/112/112                |
| Des tripla chiave a tre chiavi                            | Crittografia   | Blocca  | 168/168/168                |
| Checksum di autenticazione dei messaggi con hash (HMAC)   | Hashing      | Qualsiasi    | 0/0/0                      |
| Checksum di autenticazione dei messaggi (MAC)           | Hashing      | Qualsiasi    | 0/0/0                      |
| Message Digest 2 (MD2)                          | Hashing      | Qualsiasi    | 128/128/128                |
| Message Digest 4 (MD4)                          | Hashing      | Qualsiasi    | 128/128/128                |
| Message Digest 5 (MD5)                          | Hashing      | Qualsiasi    | 128/128/128                |
| RSA Data Security 2 (RC2)                       | Crittografia   | Blocca  | 128/40/128                 |
| RSA Data Security 4 (RC4)                       | Crittografia   | Stream | 128/40/128                 |
| Chiave RSA Exchange                                | Scambio di chiave | RSA    | 1024/1024/4096             |
| Firma RSA                                   | per la firma      | RSA    | 1024/1024/4096             |
| Algoritmo hash sicuro (SHA1)                    | Hashing      | Qualsiasi    | 160/160/160                |
| Algoritmo hash sicuro 256 (SHA256)              | Hashing      | Qualsiasi    | 256/256/256                |
| Algoritmo hash sicuro 384 (SHA384)              | Hashing      | Qualsiasi    | 384/384/384                |
| Algoritmo hash sicuro 512 (SHA512)              | Hashing      | Qualsiasi    | 512/512/512                |
| Secure Socket Layer 3 SHA e MD5 (SSL3 SHAMD5) | Hashing      | Qualsiasi    | 288/288/288                |



 

## <a name="microsoft-dh-schannel-cryptographic-provider"></a>Provider di crittografia Microsoft DH Schannel

Supporta il pacchetto di sicurezza Schannel (Secure Channel) che implementa i protocolli di autenticazione Secure Sockets Layer (SSL) e Transport Layer Security (TLS). Questo provider di servizi di configurazione supporta anche Diffie-Hellman scambio di chiavi e implementa gli algoritmi seguenti.



| Nome                                   | Uso                | Tipo           | Dimensioni chiave (impostazione predefinita/min/max) |
|----------------------------------------|--------------------|----------------|----------------------------|
| Algoritmo di crittografia dei messaggi CYLINK    | Crittografia         | Blocca          | 40/40/40                   |
| Data Encryption Standard (DES)         | Crittografia         | Blocca          | 56/56/56                   |
| Des con tripla chiave a due chiavi                     | Crittografia         | Blocca          | 112/112/112                |
| Des tripla chiave a tre chiavi                   | Crittografia         | Blocca          | 168/168/168                |
| Diffie-Hellman algoritmo Exchange chiave  | Scambio di chiave       | Diffie-Hellman | 512/512/4096               |
| Diffie-Hellman algoritmo ffemero     | Scambio di chiave       | Diffie-Hellman | 512/512/4096               |
| Algoritmo di firma digitale (DSA)      | per la firma            | Dss            | 1024/512/1024              |
| Message Digest 5 (MD5)                 | Hashing            | Qualsiasi            | 128/128/128                |
| RSA Data Security 2 (RC2)              | Crittografia         | Blocca          | 40/40/128                  |
| RSA Data Security 4 (RC4)              | Crittografia         | Stream         | 40/40/128                  |
| Algoritmo hash sicuro (SHA1)           | Hashing            | Qualsiasi            | 160/160/160                |
| Chiave di crittografia Schannel                | Crittografia         | SChannel       | 0/0/-1                     |
| Chiave MAC Schannel                       | Crittografia/hash | SChannel       | 0/0/-1                     |
| Schannel Master Hash                   | Crittografia/hash | SChannel       | 0/0/-1                     |
| Secure Sockets Layer (SSL3) Master     | Crittografia         | SChannel       | 384/384/384                |
| Transport Layer Security (TLS1) Master | Crittografia         | SChannel       | 384/384/384                |



 

## <a name="microsoft-enhanced-cryptographic-provider-v10"></a>Microsoft Enhanced Cryptographic Provider v1.0

Offre una sicurezza più avanzata rispetto a Microsoft Base Cryptographic Provider v1.0 usando chiavi più lunghe con alcuni degli algoritmi esistenti e implementando algoritmi aggiuntivi.



| Nome                                            | Uso          | Tipo   | Dimensioni chiave (impostazione predefinita/min/max) |
|-------------------------------------------------|--------------|--------|----------------------------|
| Data Encryption Standard (DES)                  | Crittografia   | Blocca  | 56/56/56                   |
| Des con tripla chiave a due chiavi                              | Crittografia   | Blocca  | 112/112/112                |
|                                                 | Crittografia   | Blocca  | 168/168/168                |
| Checksum di autenticazione dei messaggi con hash (HMAC)   | Hashing      | Qualsiasi    | 0/0/0                      |
| Checksum di autenticazione dei messaggi (MAC)           | Hashing      | Qualsiasi    | 0/0/0                      |
| Message Digest 2 (MD2)                          | Hashing      | Qualsiasi    | 128/128/128                |
| Message Digest 4 (MD4)                          | Hashing      | Qualsiasi    | 128/128/128                |
| Message Digest 5 (MD5)                          | Hashing      | Qualsiasi    | 128/128/128                |
| RSA Data Security 2 (RC2)                       | Crittografia   | Blocca  | 128/40/128                 |
| RSA Data Security 4 (RC4)                       | Crittografia   | Stream | 128/40/128                 |
| Chiave RSA Exchange                                | Scambio di chiave | RSA    | 1024/384/16384             |
| Firma RSA                                   | per la firma      | RSA    | 1024/384/16384             |
| Secure Hash Algorithm (SHA1)                     | Hashing      | Qualsiasi    | 160/160/160                |
| Secure Socket Layer 3 SHA e MD5 (SSL3 SHAMD5) | Hashing      | Qualsiasi    | 288/288/288                |



 

## <a name="microsoft-enhanced-dss-and-diffie-hellman-cryptographic-provider"></a>Microsoft Enhanced DSS e Diffie-Hellman Cryptographic Provider

Offre maggiore sicurezza rispetto a Microsoft Base DSS e Diffie-Hellman Cryptographic Provider CSP usando chiavi più lunghe con alcuni degli algoritmi esistenti e implementando algoritmi aggiuntivi.



| Nome                                  | Uso          | Tipo           | Dimensioni chiave (predefinito/min/max) |
|---------------------------------------|--------------|----------------|----------------------------|
| Algoritmo CYLINK Message Encryption   | Crittografia   | Blocca          | 40/40/40                   |
| Data Encryption Standard (DES)        | Crittografia   | Blocca          | 56/56/56                   |
| Two Key Triple DES                    | Crittografia   | Blocca          | 112/112/112                |
| Three Key Triple DES                  | Crittografia   | Blocca          | 168/168/168                |
| Diffie-Hellman algoritmo di Exchange chiave | Scambio di chiave | Diffie-Hellman | 1024/512/4096              |
| Diffie-Hellman algoritmo ffemero    | Scambio di chiave | Diffie-Hellman | 1024/512/4096              |
| Algoritmo di firma digitale (DSA)     | per la firma      | Dss            | 1024/512/1024              |
| Message Digest 5 (MD5)                | Hashing      | Qualsiasi            | 128/128/128                |
| RSA Data Security 2 (RC2)             | Crittografia   | Blocca          | 128/128/128                |
| RSA Data Security 4 (RC4)             | Crittografia   | Stream         | 128/128/128                |
| Secure Hash Algorithm (SHA1)          | Hashing      | Qualsiasi            | 160/160/160                |



 

## <a name="microsoft-enhanced-rsa-and-aes-cryptographic-provider"></a>Microsoft Enhanced RSA and AES Cryptographic Provider

Implementa gli algoritmi seguenti per firmare, crittografare e hash del contenuto.



| Nome                                            | Uso          | Tipo   | Dimensioni chiave (predefinito/min/max) |
|-------------------------------------------------|--------------|--------|----------------------------|
| Advanced Encryption Standard 128 (AES128)       | Crittografia   | Blocca  | 128/128/128                |
| Advanced Encryption Standard 192 (AES192)       | Crittografia   | Blocca  | 192/192/192                |
| Advanced Encryption Standard 256 (AES256)       | Crittografia   | Blocca  | 256/256/256                |
| Data Encryption Standard (DES)                  | Crittografia   | Blocca  | 56/56/56                   |
| Two Key Triple DES                              | Crittografia   | Blocca  | 112/112/112                |
| Three Key Triple DES                            | Crittografia   | Blocca  | 168/168/168                |
| Hashed Message Authentication Checksum (HMAC)   | Hashing      | Qualsiasi    | 0/0/0                      |
| Checksum di autenticazione dei messaggi (MAC)           | Hashing      | Qualsiasi    | 0/0/0                      |
| Message Digest 2 (MD2)                          | Hashing      | Qualsiasi    | 128/128/128                |
| Message Digest 4 (MD4)                          | Hashing      | Qualsiasi    | 128/128/128                |
| Message Digest 5 (MD5)                          | Hashing      | Qualsiasi    | 128/128/128                |
| RSA Data Security 2 (RC2)                       | Crittografia   | Blocca  | 128/128/128                |
| RSA Data Security 4 (RC4)                       | Crittografia   | Stream | 128/128/128                |
| Chiave RSA Exchange                                | Scambio di chiave | RSA    | 1024/384/16384             |
| Firma RSA                                   | per la firma      | RSA    | 1024/384/16384             |
| Secure Hash Algorithm (SHA1)                    | Hashing      | Qualsiasi    | 160/160/160                |
| Secure Hash Algorithm (SHA256)                  | Hashing      | Qualsiasi    | 256/256/256                |
| Secure Hash Algorithm (SHA384)                  | Hashing      | Qualsiasi    | 384/384/384                |
| Secure Hash Algorithm (SHA512)                  | Hashing      | Qualsiasi    | 512/512/512                |
| Secure Socket Layer 3 SHA e MD5 (SSL3 SHAMD5) | Hashing      | Qualsiasi    | 288/288/288                |



 

## <a name="microsoft-rsa-schannel-cryptographic-provider"></a>Provider del servizio di crittografia Microsoft RSA Schannel

Supporta il pacchetto di sicurezza RSA Secure Channel (Schannel) che implementa i protocolli di autenticazione Secure Sockets Layer (SSL) e Transport Layer Security (TLS).



| Nome                                            | Uso                | Tipo     | Dimensioni chiave (predefinito/min/max) |
|-------------------------------------------------|--------------------|----------|----------------------------|
| Advanced Encryption Standard 128 (AES128)       | Crittografia         | Blocca    | 128/128/128                |
| Advanced Encryption Standard 256 (AES256)       | Crittografia         | Blocca    | 256/256/256                |
| Data Encryption Standard (DES)                  | Crittografia         | Blocca    | 56/56/56                   |
| Two Key Triple DES                              | Crittografia         | Blocca    | 112/112/112                |
| Three Key Triple DES                            | Crittografia         | Blocca    | 168/168/168                |
| Checksum di autenticazione dei messaggi con hash (HMAC)   | Hashing            | Qualsiasi      | 0/0/0                      |
| Checksum di autenticazione dei messaggi (MAC)           | Hashing            | Qualsiasi      | 0/0/0                      |
| Message Digest 5 (MD5)                          | Hashing            | Qualsiasi      | 128/128/128                |
| RSA Data Security 2 (RC2)                       | Crittografia         | Blocca    | 128/128/128                |
| RSA Data Security 4 (RC4)                       | Crittografia         | Stream   | 128/128/128                |
| Chiave RSA Exchange                                | Scambio di chiave       | RSA      | 1024/384/16384             |
| Chiave di crittografia Schannel                         | Crittografia         | SChannel | 0/0/-1                     |
| Schannel Master Hash                            | Crittografia/hash | SChannel | 0/0/-1                     |
| Chiave MAC Schannel                                | Crittografia/hash | SChannel | 0/0/-1                     |
| Algoritmo hash sicuro (SHA1)                    | Hashing            | Qualsiasi      | 160/160/160                |
| Secure Socket Layer 2 (SSL2) Master             | Crittografia         | SChannel | 40/40/192                  |
| Secure Socket Layer 3 (SSL3) Master             | Crittografia         | SChannel | 384/384/384                |
| Secure Socket Layer 3 SHA e MD5 (SSL3 SHAMD5) | Hashing            | Qualsiasi      | 288/288/288                |
| Transport Layer Security (TLS1) Master          | Crittografia         | SChannel | 384/384/384                |



 

## <a name="microsoft-strong-cryptographic-provider"></a>Microsoft Strong Cryptographic Provider

Implementa gli algoritmi seguenti.



| Nome                                            | Uso          | Tipo   | Dimensioni chiave (impostazione predefinita/min/max) |
|-------------------------------------------------|--------------|--------|----------------------------|
| Data Encryption Standard (DES)                  | Crittografia   | Blocca  | 56/56/56                   |
| Des con tripla chiave a due chiavi                              | Crittografia   | Blocca  | 112/112/112                |
| Des tripla chiave a tre chiavi                            | Crittografia   | Blocca  | 168/168/168                |
| Checksum di autenticazione dei messaggi con hash (HMAC)   | Hashing      | Qualsiasi    | 0/0/0                      |
| Checksum di autenticazione dei messaggi (MAC)           | Hashing      | Qualsiasi    | 0/0/0                      |
| Message Digest 2 (MD2)                          | Hashing      | Qualsiasi    | 128/128/128                |
| Message Digest 4 (MD4)                          | Hashing      | Qualsiasi    | 128/128/128                |
| Message Digest 5 (MD5)                          | Hashing      | Qualsiasi    | 128/128/128                |
| RSA Data Security 2 (RC2)                       | Crittografia   | Blocca  | 128/40/128                 |
| RSA Data Security 4 (RC4)                       | Crittografia   | Stream | 128/40/128                 |
| Chiave RSA Exchange                                | Scambio di chiave | RSA    | 1024/384/16384             |
| Firma RSA                                   | per la firma      | RSA    | 1024/384/16384             |
| Algoritmo hash sicuro (SHA1)                    | Hashing      | Qualsiasi    | 160/160/160                |
| Secure Socket Layer 3 SHA e MD5 (SSL3 SHAMD5) | Hashing      | Qualsiasi    | 288/288/288                |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sui provider di crittografia](understanding-cryptographic-providers.md)
</dt> </dl>

 

 
