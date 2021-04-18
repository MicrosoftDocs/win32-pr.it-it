---
description: Elenca i provider del servizio di crittografia disponibili da Microsoft.
ms.assetid: 1461914e-5506-4f24-97da-3d2148aafd1c
title: Provider del servizio di crittografia Microsoft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 294d00660cbfa89c6113e6e9fcf2600b2f745e6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307672"
---
# <a name="microsoft-cryptographic-service-providers"></a>Provider del servizio di crittografia Microsoft

I [*provider del servizio di crittografia*](../secgloss/c-gly.md) (CSP) seguenti sono attualmente disponibili in Microsoft.



| Provider                                                                                                                                 | Descrizione                                                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Provider di crittografia di base Microsoft](microsoft-base-cryptographic-provider.md)                                                       | Ampia gamma di funzionalità crittografiche di base che possono essere esportate in altri paesi o aree geografiche.                                                                                                                                                     |
| [Microsoft Strong Cryptographic Provider](microsoft-strong-cryptographic-provider.md)                                                   | Estensione del provider di crittografia di base Microsoft disponibile con Windows XP e versioni successive.                                                                                                                                                           |
| [Microsoft Enhanced Cryptographic Provider](microsoft-enhanced-cryptographic-provider.md)                                               | Provider di crittografia di base Microsoft con chiavi più lunghe e algoritmi aggiuntivi.                                                                                                                                                                |
| [Provider di crittografia AES Microsoft](microsoft-aes-cryptographic-provider.md)                                                         | Microsoft Enhanced Cryptographic Provider con supporto per gli algoritmi di crittografia AES.                                                                                                                                                                    |
| [Provider di crittografia Microsoft DSS](microsoft-dss-cryptographic-provider.md)                                                         | Fornisce funzionalità di hashing, firma dei dati e verifica della firma usando gli algoritmi Secure Hash Algorithm ([*Sha*](../secgloss/s-gly.md)) e Digital Signature Standard (DSS). |
| [Provider di crittografia di Microsoft Base DSS e Diffie-Hellman](microsoft-base-dss-and-diffie-hellman-cryptographic-provider.md)         | Superset del provider di crittografia DSS che supporta anche Diffie-Hellman scambio di chiave, hashing, firma dei dati e la verifica della firma usando gli algoritmi Secure Hash Algorithm (SHA) e Digital Signature Standard (DSS).                    |
| [Microsoft Enhanced DSS e Diffie-Hellman provider di crittografia](microsoft-enhanced-dss-and-diffie-hellman-cryptographic-provider.md) | Supporta Diffie-Hellman scambio di chiave (derivato DES a 40 bit), hashing SHA, firma dati DSS e verifica della firma DSS.                                                                                                                           |
| [Provider di crittografia Microsoft DSS e Diffie-Hellman/SChannel](microsoft-dss-and-diffie-hellman-schannel-cryptographic-provider.md) | Supporta l'hashing, la firma dei dati con DSS, la generazione di chiavi di Diffie-Hellman (D-H), lo scambio di chiavi D-H e l'esportazione di una chiave D-H. Questo CSP supporta la derivazione delle chiavi per i protocolli SSL3 e TLS1.                                                           |
| [Provider di crittografia Microsoft RSA/SChannel](microsoft-rsa-schannel-cryptographic-provider.md)                                       | Supporta l'hashing, la firma dei dati e la verifica della firma. L'identificatore dell'algoritmo CALG \_ SSL3 \_ SHAMD5 viene usato per l'autenticazione client SSL 3,0 e TLS 1,0. Questo CSP supporta la derivazione delle chiavi per i protocolli SSL2, PCT1, SSL3 e TLS1.             |
| [Provider di crittografia Microsoft RSA Signature](microsoft-rsa-signature-cryptographic-provider.md)                                     | Fornisce la firma e la verifica della firma dei dati.                                                                                                                                                                                                        |



 

 

 
