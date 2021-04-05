---
description: Microsoft Enhanced Cryptographic Provider supporta gli algoritmi seguenti.
ms.assetid: d58bcd99-c54b-4fda-9fe1-e10a66707d81
title: Algoritmi del provider avanzati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 841c9327e4cc4c7e7e3b86471ef79fea7b478c9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968129"
---
# <a name="enhanced-provider-algorithms"></a>Algoritmi del provider avanzati

[Microsoft Enhanced Cryptographic Provider](microsoft-enhanced-cryptographic-provider.md) supporta gli algoritmi seguenti.



| ID algoritmo       | Descrizione                                                                                                                                                     | Commenti                                                                                                                                                   |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_3DES CALG         | Triple DES.                                                                                                                                                     | Lunghezza della chiave: 168 bit. Modalità predefinita: concatenamento di blocchi crittografici.<br/> Dimensioni blocco: 64 bit.<br/> Nessun Salt consentito.<br/>                           |
| CALG \_ 3des \_ 112    | Crittografia [*triple des*](../secgloss/t-gly.md) a due chiavi.                                                            | Lunghezza della chiave: 112 bit. Modalità predefinita: concatenamento di blocchi crittografici.<br/> Dimensioni blocco: 64 bit.<br/> Nessun Salt consentito.<br/>                           |
| CALG \_ des          | Crittografia DES.                                                                                                                                                 | Lunghezza della chiave: 56 bit. Modalità predefinita: concatenamento di blocchi crittografici.<br/> Dimensioni blocco: 64 bit.<br/> Nessun Salt consentito.<br/>                            |
| CALG \_ HMAC         | Algoritmo hash con chiave MAC.                                                                                                                                       | Calcolo HMAC.                                                                                                                                          |
| \_Mac CALG          | Algoritmo hash con chiave [*Message Authentication Code*](../secgloss/m-gly.md) (Mac). | Blocca il MAC crittografato.                                                                                                                                          |
| \_MD2 CALG          | Algoritmo di hash MD2.                                                                                                                                          | Per ulteriori informazioni, vedere [*algoritmo MD2*](../secgloss/m-gly.md).                                       |
| \_MD5 CALG          | Algoritmo di hash MD5.                                                                                                                                          | Per altre informazioni, vedere [*algoritmo MD5*](../secgloss/m-gly.md).                                       |
| CALG \_ RC2          | Algoritmo di crittografia a blocchi RC2.                                                                                                                                 | Lunghezza della chiave: 128 bit. Modalità predefinita: concatenamento di blocchi crittografici.<br/> Dimensioni blocco: 64 bit.<br/> Lunghezza del Salt: è possibile impostare.<br/>                   |
| CALG \_ RC4          | Algoritmo di crittografia del flusso RC4.                                                                                                                                | Lunghezza della chiave: 128 bit. Lunghezza del Salt: è possibile impostare.<br/>                                                                                                   |
| CALG \_ RSA \_ KEYX    | Algoritmo di scambio di chiave pubblica RSA.                                                                                                                              | Lunghezza della chiave: è possibile impostare 384 bit su 16.384 bit negli incrementi a 8 bit. Lunghezza chiave predefinita: 1.024 bit.<br/>                                            |
| CALG \_ - \_ firma RSA    | Algoritmo di firma della chiave pubblica RSA.                                                                                                                             | Lunghezza della chiave: è possibile impostare 384 bit su 16.384 bit negli incrementi a 8 bit. Lunghezza chiave predefinita: 1.024 bit.<br/> La firma è conforme a PKCS \# 6.<br/> |
| \_Sha CALG          | Algoritmo di hash SHA.                                                                                                                                          | Per ulteriori informazioni, vedere [*Secure Hash Algorithm*](../secgloss/s-gly.md).               |
| CALG \_ SHA1         | Uguale a CALG \_ Sha.                                                                                                                                              | Per ulteriori informazioni, vedere [*Secure Hash Algorithm*](../secgloss/s-gly.md).               |
| CALG \_ SSL3 \_ SHAMD5 | Algoritmo di autenticazione client di SSL3.                                                                                                                           | Per altre informazioni, vedere [creazione di un \_ hash CALG SSL3 \_ SHAMD5](creating-a-calg-ssl3-shamd5-hash.md).                                                      |



 

 

 
