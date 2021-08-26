---
description: "A differenza dell'API di crittografia (CryptoAPI), l'API di crittografia CNG (Cryptography API: Next Generation) separa i provider di crittografia dai provider di archiviazione chiavi."
ms.assetid: ce29bc97-049e-4c82-979f-4c805a318ba0
title: Provider di algoritmi di crittografia CNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fd98a7eb6fd159c54977cdf8b72ebffd747da48
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467078"
---
# <a name="cng-cryptographic-algorithm-providers"></a>Provider di algoritmi di crittografia CNG

A differenza dell'API di crittografia (CryptoAPI), l'API di crittografia CNG (Cryptography API: Next Generation) separa i provider di crittografia dai provider di archiviazione chiavi. Le operazioni di base dell'algoritmo di crittografia, ad esempio l'hashing e la firma, sono chiamate operazioni primitive o semplicemente primitive. CNG include un provider che implementa gli algoritmi seguenti.

-   [Algoritmi simmetrici](#symmetric-algorithms)
-   [Algoritmi asimmetrici](#asymmetric-algorithms)
-   [Algoritmi di hashing](#hashing-algorithms)
-   [Algoritmi Exchange chiave](#key-exchange-algorithms)
-   [Argomenti correlati](#related-topics)

## <a name="symmetric-algorithms"></a>Algoritmi simmetrici



| Nome                                   | Modalità supportate                                                                                                                                                                                                 | Dimensioni della chiave in bit (predefinita/min/max) |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------|
| Advanced Encryption Standard (AES)     | ECB, CBC, CFB8, CFB128, GCM, CCM, GMAC, CMAC, AES Key Wrap, XTS<br/> **Windows 8:** Inizia il supporto per le modalità CFB128 e CMAC.<br/> **Windows 10:** Viene avviato il supporto per la modalità XTS-AES.<br/> | 128/192/256                        |
| Data Encryption Standard (DES)         | BCE, CBC, CFB8, CFB64<br/> **Windows 8:** Viene avviato il supporto per la modalità CFB64.<br/>                                                                                                                   | 56/56/56                           |
| Data Encryption Standard XORed(DESX)   | BCE, CBC, CFB8, CFB64 <br/> **Windows 8:** Viene avviato il supporto per la modalità CFB64.<br/>                                                                                                                  | 192/192/192                        |
| Triple Data Encryption Standard (3DES) | BCE, CBC, CFB8, CFB64 <br/> **Windows 8:** Viene avviato il supporto per la modalità CFB64.<br/>                                                                                                                  | 112/168                            |
| RSA Data Security 2 (RC2)              | Sono supportate le modalità BCE, CBC, CFB8, CFB64.<br/> **Windows 8:** Viene avviato il supporto per la modalità CFB64.<br/>                                                                                              | Da 16 a 128 in incrementi a 8 bit      |
| RSA Data Security 4 (RC4)              |                                                                                                                                                                                                                 | Da 8 a 512, in incrementi a 8 bit      |



 

## <a name="asymmetric-algorithms"></a>Algoritmi asimmetrici



| Nome                              | Note                                                                                                                                                                             | Dimensioni della chiave in bit (predefinita/min/max)                                                                            |
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Algoritmo di firma digitale (DSA) | L'implementazione è conforme a FIPS 186-3 per le dimensioni delle chiavi tra 1024 e 3072 bit. <br/> L'implementazione è conforme a FIPS 186-2 per le dimensioni delle chiavi da 512 a 1024 bit.<br/> | Da 512 a 3072, in incrementi a 64 bit<br/> **Windows 8:** Inizia il supporto per una chiave a 3072 bit.<br/> |
| RSA                               | Include algoritmi RSA che usano PKCS1, la codifica o la spaziatura interna OAEP (Optimal Asymmetric Encryption Padding) o psabilistic Signature Scheme (PSS) in testo non crittografato               | Da 512 a 16384, in incrementi a 64 bit                                                                            |



 

## <a name="hashing-algorithms"></a>Algoritmi di hashing



| Nome                               | Note               | Dimensioni della chiave in bit (predefinita/min/max) |
|------------------------------------|---------------------|------------------------------------|
| Secure Hash Algorithm 1 (SHA1)     | Include HmacSha1   | 160/160/160                        |
| Algoritmo hash sicuro 256 (SHA256) | Include HmacSha256 | 256/256/256                        |
| Algoritmo hash sicuro 384 (SHA384) | Include HmacSha384 | 384/384/384                        |
| Algoritmo hash sicuro 512 (SHA512) | Include HmacSha512 | 512/512/512                        |
| Message Digest 2 (MD2)             | Include HmacMd2    | 128/128/128                        |
| Message Digest 4 (MD4)             | Include HmacMd4    | 128/128/128                        |
| Message Digest 5 (MD5)             | Include HmacMd5    | 128/128/128                        |



 

## <a name="key-exchange-algorithms"></a>Algoritmi Exchange chiave




| Nome algoritmo | Note | Dimensioni della chiave in bit (predefinita/min/max) | 
|----------------|-------|------------------------------------|
| Diffie-Hellman algoritmo Exchange chiave | Da 512 a 4096, in incrementi a 64 bit | 
| Curva ellittica Diffie-Hellman (ECDH) | Include curve che usano chiavi pubbliche a 256, 384 e 521 bit, come specificato in SP800-56A. | 256/384/521 | 
| Algoritmo di firma digitale a curva ellittica (ECDSA) | Include curve che usano chiavi pubbliche a 256, 384 e 521 bit, come specificato in FIPS 186-3.<blockquote>[!Note]<br />Per visualizzare tutte le curve ellittiche denominate, usare <strong>certutil displayEccCurve</strong>.</blockquote><br /> | 256/384/521 | 




 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Identificatori di algoritmi CNG**](/windows/desktop/SecCNG/cng-algorithm-identifiers)
</dt> <dt>

[Funzioni primitive crittografiche CNG](/windows/desktop/SecCNG/cng-cryptographic-primitive-functions)
</dt> <dt>

[Informazioni sui provider di crittografia](understanding-cryptographic-providers.md)
</dt> </dl>

 

