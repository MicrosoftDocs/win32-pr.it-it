---
description: Microsoft Base Cryptographic Provider supporta gli algoritmi seguenti.
ms.assetid: 767d5192-6e8f-488a-b954-29d56488ccbb
title: Algoritmi del provider di base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6b6f3af49529ad46e70dd154c06febf433f5fb483861f7c0b2530af7ebbef2c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119879751"
---
# <a name="base-provider-algorithms"></a>Algoritmi del provider di base

Microsoft Base Cryptographic Provider supporta gli algoritmi seguenti.



| ID algoritmo                  | Descrizione                                                                                                                                                               | Commenti                                                                                                                                                                |
|-------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CALG \_ MD2<br/>          | Algoritmo hash MD2<br/>                                                                                                                                          | Per altre informazioni, vedere [*Algoritmo MD2*](../secgloss/m-gly.md).<br/>                                         |
| CALG \_ MD5<br/>          | Algoritmo hash MD5<br/>                                                                                                                                          | Per altre informazioni, vedere [*Algoritmo MD5*](../secgloss/m-gly.md).<br/>                                         |
| CALG \_ SHA<br/>          | Algoritmo hash SHA<br/>                                                                                                                                          | Per altre informazioni, vedere [*Secure Hash Algorithm*](../secgloss/s-gly.md).<br/>                 |
| CALG \_ SHA1<br/>         | Uguale a CALG \_ SHA<br/>                                                                                                                                              | Per altre informazioni, vedere [*Secure Hash Algorithm*](../secgloss/s-gly.md).<br/>                 |
| CALG \_ MAC<br/>          | [*Message Authentication Code*](../secgloss/m-gly.md) (MAC) keyed-hash<br/> | Mac di crittografia a blocchi.<br/>                                                                                                                                            |
| CALG \_ HMAC<br/>         | Algoritmo mac keyed-hash<br/>                                                                                                                                       | Calcolo HMAC.<br/>                                                                                                                                            |
| CALG \_ SSL3 \_ SHAMD5<br/> | Algoritmo di autenticazione client SLL3<br/>                                                                                                                           | Per altre informazioni, vedere [Creazione di un hash \_ CALG SSL3 \_ SHAMD5.](creating-a-calg-ssl3-shamd5-hash.md)<br/>                                                        |
| FIRMA RSA CALG \_ \_<br/>    | Algoritmo di firma a chiave pubblica RSA<br/>                                                                                                                             | Lunghezza della chiave: può essere impostata da 384 bit a 16.384 bit in incrementi a 8 bit.<br/> Lunghezza predefinita della chiave: 512 bit.<br/> La firma è conforme a PKCS \# 6.<br/> |
| CALG \_ RSA \_ KEYX<br/>    | Algoritmo di scambio di chiavi pubbliche RSA<br/>                                                                                                                              | Lunghezza della chiave: può essere impostata da 384 bit a 1024 bit in incrementi a 8 bit.<br/> Lunghezza predefinita della chiave: 512 bit.<br/>                                              |
| CALG \_ RC2<br/>          | Algoritmo di crittografia a blocchi RC2<br/>                                                                                                                                 | Lunghezza della chiave: 40 bit.<br/> Modalità predefinita: concatenamento di blocchi di crittografia.<br/> Dimensioni del blocco: 64 bit.<br/> Lunghezza del sale: 88 bit.<br/>                        |
| CALG \_ RC4<br/>          | Algoritmo di crittografia del flusso RC4<br/>                                                                                                                                | Lunghezza della chiave: 40 bit.<br/> Lunghezza del sale: 88 bit.<br/>                                                                                                        |
| CALG \_ DES<br/>          | Crittografia DES<br/>                                                                                                                                                 | Per altre informazioni, vedere [*Data Encryption Standard*](../secgloss/d-gly.md) (DES).<br/>  |



 

 

 
