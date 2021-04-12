---
description: Credential Security Support Provider Protocol (CredSSP) è un provider di supporto per la sicurezza implementato mediante SSPI (Security Support Provider Interface).
ms.assetid: b3006b89-d9fc-4444-a3c8-ad2698de501c
title: Provider di supporto per la sicurezza delle credenziali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e9aa961f37043d84dc21280ea7d5ecb9c27c075
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226485"
---
# <a name="credential-security-support-provider"></a>Provider di supporto per la sicurezza delle credenziali

Credential Security Support Provider Protocol (CredSSP) è un provider di supporto per la sicurezza implementato mediante[SSPI](sspi.md)(Security Support Provider Interface). CredSSP consente a un'applicazione di delegare le credenziali dell'utente dal client al server di destinazione per l'autenticazione remota. CredSSP fornisce un canale di [protocollo Transport Layer Security](transport-layer-security-protocol.md) crittografato. Il client viene autenticato sul canale crittografato utilizzando il protocollo Negotiate (Simple and protected Negotiate, SPNEGO) con [Microsoft Kerberos](microsoft-kerberos.md) o [Microsoft NTLM](microsoft-ntlm.md).

> [!Caution]  
> La delega non è vincolata. CredSSP passa le credenziali complete dell'utente al server senza vincoli.

 

Per informazioni su SPNEGO, vedere [Microsoft Negotiate](microsoft-negotiate.md).

Dopo l'autenticazione del client e del server, il client passa le credenziali dell'utente al server. Le credenziali vengono crittografate doppiamente nelle chiavi di sessione SPNEGO e TLS. CredSSP supporta l'accesso basato su password, nonché l'accesso tramite smart card basato su [*X. 509*](/windows/desktop/SecGloss/x-gly) e PKINIT.

> [!IMPORTANT]
> CredSSP non supporta client WOW64.

 

Per ulteriori informazioni su CredSSP, vedere gli argomenti seguenti.



| Argomento                                                                         | Descrizione                                                                                       |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [Impostazioni Criteri di gruppo CredSSP](credssp-group-policy-settings.md)<br/> | La delega delle credenziali da CredSSP può essere controllata tramite le impostazioni di criteri di gruppo.<br/> |



 

 

