---
description: Microsoft Enhanced Cryptographic Provider supporta gli algoritmi seguenti.
ms.assetid: d58bcd99-c54b-4fda-9fe1-e10a66707d81
title: Algoritmi del provider avanzati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5a8be464a57a482fa74fef07de097508508d7e965a5c20817ccbd884bb169e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117766102"
---
# <a name="enhanced-provider-algorithms"></a>Algoritmi del provider avanzati

Microsoft [Enhanced Cryptographic Provider](microsoft-enhanced-cryptographic-provider.md) supporta gli algoritmi seguenti.



| ID algoritmo       | Descrizione                                                                                                                                                     | Commenti                                                                                                                                                   |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CALG \_ 3DES         | Triple DES.                                                                                                                                                     | Lunghezza della chiave: 168 bit. Modalità predefinita: concatenamento di blocchi di crittografia.<br/> Dimensioni del blocco: 64 bit.<br/> Non è consentito alcun salt.<br/>                           |
| CALG \_ 3DES \_ 112    | Crittografia DES [*tripla a due*](../secgloss/t-gly.md) chiavi.                                                            | Lunghezza della chiave: 112 bit. Modalità predefinita: concatenamento di blocchi di crittografia.<br/> Dimensioni del blocco: 64 bit.<br/> Non è consentito alcun salt.<br/>                           |
| CALG \_ DES          | Crittografia DES.                                                                                                                                                 | Lunghezza della chiave: 56 bit. Modalità predefinita: concatenamento di blocchi di crittografia.<br/> Dimensioni del blocco: 64 bit.<br/> Non è consentito alcun salt.<br/>                            |
| CALG \_ HMAC         | Algoritmo hash con chiave MAC.                                                                                                                                       | Calcolo HMAC.                                                                                                                                          |
| CALG \_ MAC          | [*Message Authentication Code*](../secgloss/m-gly.md) algoritmo hash con chiave MAC. | Mac di crittografia a blocchi.                                                                                                                                          |
| CALG \_ MD2          | Algoritmo di hash MD2.                                                                                                                                          | Per altre informazioni, vedere [*Algoritmo MD2*](../secgloss/m-gly.md).                                       |
| CALG \_ MD5          | Algoritmo di hash MD5.                                                                                                                                          | Per altre informazioni, vedere [*Algoritmo MD5*](../secgloss/m-gly.md).                                       |
| CALG \_ RC2          | Algoritmo di crittografia a blocchi RC2.                                                                                                                                 | Lunghezza della chiave: 128 bit. Modalità predefinita: concatenamento di blocchi di crittografia.<br/> Dimensioni del blocco: 64 bit.<br/> Lunghezza salt: può essere impostata.<br/>                   |
| CALG \_ RC4          | Algoritmo di crittografia del flusso RC4.                                                                                                                                | Lunghezza della chiave: 128 bit. Lunghezza salt: può essere impostata.<br/>                                                                                                   |
| CALG \_ RSA \_ KEYX    | Algoritmo di scambio di chiavi pubbliche RSA.                                                                                                                              | Lunghezza della chiave: può essere impostata da 384 bit a 16.384 bit in incrementi a 8 bit. Lunghezza predefinita della chiave: 1.024 bit.<br/>                                            |
| FIRMA RSA CALG \_ \_    | Algoritmo di firma a chiave pubblica RSA.                                                                                                                             | Lunghezza della chiave: può essere impostata da 384 bit a 16.384 bit in incrementi a 8 bit. Lunghezza predefinita della chiave: 1.024 bit.<br/> La firma è conforme a PKCS \# 6.<br/> |
| CALG \_ SHA          | Algoritmo di hash SHA.                                                                                                                                          | Per altre informazioni, vedere [*Secure Hash Algorithm*](../secgloss/s-gly.md).               |
| CALG \_ SHA1         | Uguale a CALG \_ SHA.                                                                                                                                              | Per altre informazioni, vedere [*Secure Hash Algorithm*](../secgloss/s-gly.md).               |
| CALG \_ SSL3 \_ SHAMD5 | Algoritmo di autenticazione client SSL3.                                                                                                                           | Per altre informazioni, vedere [Creazione di un hash \_ CALG SSL3 \_ SHAMD5.](creating-a-calg-ssl3-shamd5-hash.md)                                                      |



 

 

 
