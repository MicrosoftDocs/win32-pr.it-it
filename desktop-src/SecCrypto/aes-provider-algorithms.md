---
description: Nella tabella seguente sono elencati gli algoritmi supportati dal provider di crittografia Microsoft Advanced Encryption Standard (AES).
ms.assetid: 34d0479f-9d1e-41cd-87b0-6bc18c7a062b
title: Algoritmi del provider AES
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a06381c3f7fcf3d410a9a9a90c70633cab17c1ffd2e3e967ba6f3e7c3787fbb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117773776"
---
# <a name="aes-provider-algorithms"></a>Algoritmi del provider AES

Nella tabella seguente sono elencati gli algoritmi supportati dal provider di crittografia Microsoft [*Advanced Encryption Standard*](../secgloss/a-gly.md) (AES).



| ID algoritmo       | Descrizione                                                                                                                                                     | Commenti                                                                                                                                                   |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CALG \_ 3DES         | Triple DES.                                                                                                                                                     | Lunghezza della chiave: 168 bit. Modalità predefinita: concatenamento di blocchi di crittografia.<br/> Dimensioni del blocco: 64 bit.<br/> Non è consentito alcun salt.<br/>                          |
| CALG \_ 3DES \_ 112    | Crittografia DES [*tripla a due*](../secgloss/t-gly.md) chiavi.                                                            | Lunghezza della chiave: 112 bit. Modalità predefinita: concatenamento di blocchi di crittografia.<br/> Dimensioni del blocco: 64 bit.<br/> Non è consentito alcun salt.<br/>                          |
| CALG \_ AES \_ 128     | Algoritmo di crittografia a blocchi AES.                                                                                                                                 | Lunghezza della chiave: 128 bit.                                                                                                                                      |
| CALG \_ AES \_ 192     | Algoritmo di crittografia a blocchi AES.                                                                                                                                 | Lunghezza della chiave: 192 bit.                                                                                                                                      |
| CALG \_ AES \_ 256     | Algoritmo di crittografia a blocchi AES.                                                                                                                                 | Lunghezza della chiave: 256 bit.                                                                                                                                      |
| CALG \_ DES          | Crittografia DES.                                                                                                                                                 | Lunghezza della chiave: 56 bit. Modalità predefinita: concatenamento di blocchi di crittografia.<br/> Dimensioni del blocco: 64 bit.<br/> Non è consentito alcun salt.<br/>                           |
| CALG \_ HMAC         | Algoritmo hash con chiave MAC.                                                                                                                                       | Calcolo HMAC.                                                                                                                                          |
| CALG \_ MAC          | [*Message Authentication Code*](../secgloss/m-gly.md) algoritmo hash con chiave MAC. | Mac di crittografia a blocchi.                                                                                                                                          |
| CALG \_ MD2          | Algoritmo di hash MD2.                                                                                                                                          | Per altre informazioni, vedere [*Algoritmo MD2*](../secgloss/m-gly.md).                                       |
| CALG \_ MD5          | Algoritmo di hash MD5.                                                                                                                                          | Per altre informazioni, vedere [*Algoritmo MD5*](../secgloss/m-gly.md).                                       |
| CALG \_ RC2          | Algoritmo di crittografia a blocchi RC2.                                                                                                                                 | Lunghezza della chiave: 128 bit. Modalità predefinita: concatenamento di blocchi di crittografia.<br/> Dimensioni del blocco: 64 bit.<br/> Lunghezza salt: può essere impostata.<br/>                  |
| CALG \_ RC4          | Algoritmo di crittografia del flusso RC4.                                                                                                                                | Lunghezza della chiave: 128 bit. Lunghezza salt: può essere impostata.<br/>                                                                                                  |
| CALG \_ RSA \_ KEYX    | Algoritmo di scambio di chiavi pubbliche RSA.                                                                                                                              | Lunghezza chiave: può essere impostata da 384 bit a 16.384 bit in incrementi a 8 bit. Lunghezza predefinita della chiave: 1.024 bit.<br/>                                            |
| FIRMA RSA CALG \_ \_    | Algoritmo di firma a chiave pubblica RSA.                                                                                                                             | Lunghezza chiave: può essere impostata da 384 bit a 16.384 bit in incrementi a 8 bit. Lunghezza predefinita della chiave: 1.024 bit.<br/> La firma è conforme a PKCS \# 6.<br/> |
| CALG \_ SHA          | Algoritmo di hash SHA.                                                                                                                                          | Per altre informazioni, vedere [*Secure Hash Algorithm*](../secgloss/s-gly.md).               |
| CALG \_ SHA1         | Uguale a **CALG \_ SHA.**                                                                                                                                          | Per altre informazioni, vedere [*Secure Hash Algorithm*](../secgloss/s-gly.md).               |
| CALG \_ SHA \_ 256     | Algoritmo di hash SHA.                                                                                                                                          | Lunghezza della chiave: 256 bit. **Windows XP:** Questo algoritmo non è supportato.<br/>                                                                           |
| CALG \_ SHA \_ 384     | Algoritmo di hash SHA.                                                                                                                                          | Lunghezza della chiave: 384 bit. **Windows XP:** Questo algoritmo non è supportato.<br/>                                                                           |
| CALG \_ SHA \_ 512     | Algoritmo di hash SHA.                                                                                                                                          | Lunghezza della chiave: 512 bit. **Windows XP:** Questo algoritmo non è supportato.<br/>                                                                           |
| CALG \_ SSL3 \_ SHAMD5 | Algoritmo di autenticazione client SSL3.                                                                                                                           | Per altre informazioni, vedere [Creazione di un hash \_ CALG SSL3 \_ SHAMD5](creating-a-calg-ssl3-shamd5-hash.md).                                                      |



 

 

 
