---
description: Nella tabella seguente sono elencati gli algoritmi supportati dal provider di crittografia Microsoft Advanced Encryption Standard (AES).
ms.assetid: 34d0479f-9d1e-41cd-87b0-6bc18c7a062b
title: Algoritmi del provider AES
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e5e197100060d53304bb5233560dcccae083756
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312807"
---
# <a name="aes-provider-algorithms"></a>Algoritmi del provider AES

Nella tabella seguente sono elencati gli algoritmi supportati dal provider di crittografia Microsoft [*Advanced Encryption Standard*](../secgloss/a-gly.md) (AES).



| ID algoritmo       | Descrizione                                                                                                                                                     | Commenti                                                                                                                                                   |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_3DES CALG         | Triple DES.                                                                                                                                                     | Lunghezza della chiave: 168 bit. Modalità predefinita: concatenamento di blocchi crittografici.<br/> Dimensioni blocco: 64 bit.<br/> Nessun Salt consentito.<br/>                          |
| CALG \_ 3des \_ 112    | Crittografia [*triple des*](../secgloss/t-gly.md) a due chiavi.                                                            | Lunghezza della chiave: 112 bit. Modalità predefinita: concatenamento di blocchi crittografici.<br/> Dimensioni blocco: 64 bit.<br/> Nessun Salt consentito.<br/>                          |
| CALG \_ AES \_ 128     | Algoritmo di crittografia a blocchi AES.                                                                                                                                 | Lunghezza della chiave: 128 bit.                                                                                                                                      |
| CALG \_ AES \_ 192     | Algoritmo di crittografia a blocchi AES.                                                                                                                                 | Lunghezza della chiave: 192 bit.                                                                                                                                      |
| CALG \_ AES \_ 256     | Algoritmo di crittografia a blocchi AES.                                                                                                                                 | Lunghezza della chiave: 256 bit.                                                                                                                                      |
| CALG \_ des          | Crittografia DES.                                                                                                                                                 | Lunghezza della chiave: 56 bit. Modalità predefinita: concatenamento di blocchi crittografici.<br/> Dimensioni blocco: 64 bit.<br/> Nessun Salt consentito.<br/>                           |
| CALG \_ HMAC         | Algoritmo hash con chiave MAC.                                                                                                                                       | Calcolo HMAC.                                                                                                                                          |
| \_Mac CALG          | Algoritmo hash con chiave [*Message Authentication Code*](../secgloss/m-gly.md) (Mac). | Blocca il MAC crittografato.                                                                                                                                          |
| \_MD2 CALG          | Algoritmo di hash MD2.                                                                                                                                          | Per ulteriori informazioni, vedere [*algoritmo MD2*](../secgloss/m-gly.md).                                       |
| \_MD5 CALG          | Algoritmo di hash MD5.                                                                                                                                          | Per altre informazioni, vedere [*algoritmo MD5*](../secgloss/m-gly.md).                                       |
| CALG \_ RC2          | Algoritmo di crittografia a blocchi RC2.                                                                                                                                 | Lunghezza della chiave: 128 bit. Modalità predefinita: concatenamento di blocchi crittografici.<br/> Dimensioni blocco: 64 bit.<br/> Lunghezza del Salt: è possibile impostare.<br/>                  |
| CALG \_ RC4          | Algoritmo di crittografia del flusso RC4.                                                                                                                                | Lunghezza della chiave: 128 bit. Lunghezza del Salt: è possibile impostare.<br/>                                                                                                  |
| CALG \_ RSA \_ KEYX    | Algoritmo di scambio di chiave pubblica RSA.                                                                                                                              | Lunghezza della chiave: è possibile impostare 384 bit su 16.384 bit negli incrementi a 8 bit. Lunghezza chiave predefinita: 1.024 bit.<br/>                                            |
| CALG \_ - \_ firma RSA    | Algoritmo di firma della chiave pubblica RSA.                                                                                                                             | Lunghezza della chiave: è possibile impostare 384 bit su 16.384 bit negli incrementi a 8 bit. Lunghezza chiave predefinita: 1.024 bit.<br/> La firma è conforme a PKCS \# 6.<br/> |
| \_Sha CALG          | Algoritmo di hash SHA.                                                                                                                                          | Per ulteriori informazioni, vedere [*Secure Hash Algorithm*](../secgloss/s-gly.md).               |
| CALG \_ SHA1         | Uguale a **CALG \_ Sha**.                                                                                                                                          | Per ulteriori informazioni, vedere [*Secure Hash Algorithm*](../secgloss/s-gly.md).               |
| \_SHA \_ 256 di CALG     | Algoritmo di hash SHA.                                                                                                                                          | Lunghezza della chiave: 256 bit. **Windows XP:** Questo algoritmo non è supportato.<br/>                                                                           |
| \_SHA \_ 384 di CALG     | Algoritmo di hash SHA.                                                                                                                                          | Lunghezza della chiave: 384 bit. **Windows XP:** Questo algoritmo non è supportato.<br/>                                                                           |
| \_SHA \_ 512 di CALG     | Algoritmo di hash SHA.                                                                                                                                          | Lunghezza della chiave: 512 bit. **Windows XP:** Questo algoritmo non è supportato.<br/>                                                                           |
| CALG \_ SSL3 \_ SHAMD5 | Algoritmo di autenticazione client di SSL3.                                                                                                                           | Per altre informazioni, vedere [creazione di un \_ hash CALG SSL3 \_ SHAMD5](creating-a-calg-ssl3-shamd5-hash.md).                                                      |



 

 

 
