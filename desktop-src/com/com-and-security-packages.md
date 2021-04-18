---
title: Pacchetti COM e di sicurezza
description: Windows supporta NTLMSSP (LAN Manager Security Support Provider), il protocollo di autenticazione Kerberos V5 e il pacchetto di sicurezza Schannel, che fornisce i protocolli PCT 1,0, SSL 2,0, SSL 3,0 e TLS 1,0.
ms.assetid: a0c095a8-93b7-4350-aac6-a9a066cccffd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6720ddd56869c5ce93ae70eb313fbe12c140b42
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297975"
---
# <a name="com-and-security-packages"></a>Pacchetti COM e di sicurezza

Windows supporta NTLMSSP (LAN Manager Security Support Provider), il protocollo di autenticazione Kerberos V5 e il pacchetto di sicurezza Schannel, che fornisce i protocolli PCT 1,0, SSL 2,0, SSL 3,0 e TLS 1,0. È supportato anche Snego, che verifica la disponibilità dei pacchetti di sicurezza e seleziona quello più appropriato.

La tabella seguente illustra i livelli di autenticazione supportati dai diversi pacchetti di sicurezza.



| Autenticazione server/client                                                                                           | Supporto del pacchetto di sicurezza                                         |
|------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| Nessuno dei due può ottenere il nome dell'altro.<br/>                                                                      | nessuno<br/>                                                  |
| Il client può autenticare il server, ma non viceversa.<br/>                                                 | SChannel<br/>                                              |
| Il client non è in grado di individuare il server, ma il server può ottenere l'ID utente del client.<br/>                    | NTLMSSP<br/>                                               |
| Autenticazione reciproca: il client e il server possono conoscerne il nome, se l'autorizzazione è concessa.<br/> | NTLMSSP (in locale), protocollo Kerberos V5 e Schannel<br/> |



 

Per ulteriori informazioni su questi pacchetti di sicurezza, vedere gli argomenti seguenti in questa sezione:

-   [NTLMSSP](ntlmssp.md)
-   [Protocollo Kerberos V5](kerberos-v5-protocol.md)
-   [Schannel](schannel.md)
-   [Snego](snego.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sicurezza in COM](security-in-com.md)
</dt> </dl>

 

 





