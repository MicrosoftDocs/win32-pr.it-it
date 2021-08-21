---
title: Com e pacchetti di sicurezza
description: Windows supporta NTLMSSP (LAN Manager Security Support Provider), il protocollo di autenticazione Kerberos v5 e il pacchetto di sicurezza Schannel, che fornisce i protocolli PCT 1.0, SSL 2.0, SSL 3.0 e TLS 1.0.
ms.assetid: a0c095a8-93b7-4350-aac6-a9a066cccffd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15ec80a1ea610725716da3640b6e38b2fd0f3282ce6ce778e632c6a5c8e72c8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048719"
---
# <a name="com-and-security-packages"></a>Com e pacchetti di sicurezza

Windows supporta NTLMSSP (LAN Manager Security Support Provider), il protocollo di autenticazione Kerberos v5 e il pacchetto di sicurezza Schannel, che fornisce i protocolli PCT 1.0, SSL 2.0, SSL 3.0 e TLS 1.0. È supportato anche Snego, che verifica la presenza di pacchetti di sicurezza disponibili e seleziona quello più appropriato.

La tabella seguente illustra i livelli di autenticazione supportati dai vari pacchetti di sicurezza.



| Autenticazione server/client                                                                                           | Supporto dei pacchetti di sicurezza                                         |
|------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| Nessuno dei due può ottenere il nome dell'altro.<br/>                                                                      | Nessuno<br/>                                                  |
| Il client può autenticare il server, ma non viceversa.<br/>                                                 | SChannel<br/>                                              |
| Il client non è in grado di individuare il server, ma il server può ottenere l'ID utente del client.<br/>                    | NTLMSSP<br/>                                               |
| Autenticazione reciproca: sia il client che il server possono conoscere il nome dell'altro, se viene concessa l'autorizzazione.<br/> | NTLMSSP (localmente), protocollo Kerberos v5 e Schannel<br/> |



 

Per altre informazioni su questi pacchetti di sicurezza, vedere gli argomenti seguenti in questa sezione:

-   [NTLMSSP](ntlmssp.md)
-   [Protocollo Kerberos v5](kerberos-v5-protocol.md)
-   [Schannel](schannel.md)
-   [Snego](snego.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sicurezza in COM](security-in-com.md)
</dt> </dl>

 

 





