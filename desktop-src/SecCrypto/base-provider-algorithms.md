---
description: Il provider di crittografia di base Microsoft supporta gli algoritmi seguenti.
ms.assetid: 767d5192-6e8f-488a-b954-29d56488ccbb
title: Algoritmi del provider di base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dee99bc67769e0a7e91f2d0ecc635576336fd5ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318952"
---
# <a name="base-provider-algorithms"></a>Algoritmi del provider di base

Il provider di crittografia di base Microsoft supporta gli algoritmi seguenti.



| ID algoritmo                  | Descrizione                                                                                                                                                               | Commenti                                                                                                                                                                |
|-------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_MD2 CALG<br/>          | Algoritmo di hash MD2<br/>                                                                                                                                          | Per ulteriori informazioni, vedere [*algoritmo MD2*](../secgloss/m-gly.md).<br/>                                         |
| \_MD5 CALG<br/>          | Algoritmo di hash MD5<br/>                                                                                                                                          | Per altre informazioni, vedere [*algoritmo MD5*](../secgloss/m-gly.md).<br/>                                         |
| \_Sha CALG<br/>          | Algoritmo di hash SHA<br/>                                                                                                                                          | Per ulteriori informazioni, vedere [*Secure Hash Algorithm*](../secgloss/s-gly.md).<br/>                 |
| CALG \_ SHA1<br/>         | Uguale a CALG \_ Sha<br/>                                                                                                                                              | Per ulteriori informazioni, vedere [*Secure Hash Algorithm*](../secgloss/s-gly.md).<br/>                 |
| \_Mac CALG<br/>          | Algoritmo hash con chiave [*Message Authentication Code*](../secgloss/m-gly.md) (Mac)<br/> | Blocca il MAC crittografato.<br/>                                                                                                                                            |
| CALG \_ HMAC<br/>         | Algoritmo hash con chiave MAC<br/>                                                                                                                                       | Calcolo HMAC.<br/>                                                                                                                                            |
| CALG \_ SSL3 \_ SHAMD5<br/> | Algoritmo di autenticazione client SLL3<br/>                                                                                                                           | Per altre informazioni, vedere [creazione di un \_ hash CALG SSL3 \_ SHAMD5](creating-a-calg-ssl3-shamd5-hash.md).<br/>                                                        |
| CALG \_ - \_ firma RSA<br/>    | Algoritmo di firma della chiave pubblica RSA<br/>                                                                                                                             | Lunghezza della chiave: può essere impostata da 384 bit a 16.384 bit negli incrementi a 8 bit.<br/> Lunghezza chiave predefinita: 512 bit.<br/> La firma è conforme a PKCS \# 6.<br/> |
| CALG \_ RSA \_ KEYX<br/>    | Algoritmo di scambio di chiave pubblica RSA<br/>                                                                                                                              | Lunghezza della chiave: può essere impostata da 384 bit a 1024 bit negli incrementi a 8 bit.<br/> Lunghezza chiave predefinita: 512 bit.<br/>                                              |
| CALG \_ RC2<br/>          | Algoritmo di crittografia a blocchi RC2<br/>                                                                                                                                 | Lunghezza della chiave: 40 bit.<br/> Modalità predefinita: concatenamento di blocchi crittografici.<br/> Dimensioni blocco: 64 bit.<br/> Lunghezza del Salt: 88 bit.<br/>                        |
| CALG \_ RC4<br/>          | Algoritmo di crittografia del flusso RC4<br/>                                                                                                                                | Lunghezza della chiave: 40 bit.<br/> Lunghezza del Salt: 88 bit.<br/>                                                                                                        |
| CALG \_ des<br/>          | Crittografia DES<br/>                                                                                                                                                 | Per ulteriori informazioni, vedere [*Data Encryption Standard*](../secgloss/d-gly.md) (des).<br/>  |



 

 

 
