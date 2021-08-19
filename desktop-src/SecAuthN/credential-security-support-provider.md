---
description: Il protocollo CredSSP (Credential Security Support Provider Protocol) è un provider di supporto per la sicurezza implementato tramite l'interfaccia SSPI (Security Support Provider Interface).
ms.assetid: b3006b89-d9fc-4444-a3c8-ad2698de501c
title: Provider di supporto per la sicurezza delle credenziali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b4059da0dcc1e6c963ab011ad03415175849191374732f3d1df395914aebe49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008739"
---
# <a name="credential-security-support-provider"></a>Provider di supporto per la sicurezza delle credenziali

Il protocollo CredSSP (Credential Security Support Provider Protocol) è un provider di supporto per la sicurezza implementato tramite l'interfaccia[SSPI](sspi.md)(Security Support Provider Interface). CredSSP consente a un'applicazione di delegare le credenziali dell'utente dal client al server di destinazione per l'autenticazione remota. CredSSP fornisce un canale Transport Layer Security [Protocol](transport-layer-security-protocol.md) crittografato. Il client viene autenticato tramite il canale crittografato usando il protocollo Simple and Protected Negotiate (SPNEGO) con [Microsoft Kerberos](microsoft-kerberos.md) o [Microsoft NTLM.](microsoft-ntlm.md)

> [!Caution]  
> Non si tratta di delega vincolata. CredSSP passa le credenziali complete dell'utente al server senza alcun vincolo.

 

Per informazioni su SPNEGO, vedere [Microsoft Negotiate](microsoft-negotiate.md).

Dopo l'autenticazione del client e del server, il client passa le credenziali dell'utente al server. Le credenziali vengono doppiamente crittografate con le chiavi di sessione SPNEGO e TLS. CredSSP supporta l'accesso basato su password e smart card basato su [*X.509*](/windows/desktop/SecGloss/x-gly) e PKINIT.

> [!IMPORTANT]
> CredSSP non supporta i client Wow64.

 

Per altre informazioni su CredSSP, vedere gli argomenti seguenti.



| Argomento                                                                         | Descrizione                                                                                       |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [CredSSP Criteri di gruppo Impostazioni](credssp-group-policy-settings.md)<br/> | La delega delle credenziali da parte di CredSSP può essere controllata tramite le impostazioni di Criteri di gruppo.<br/> |



 

 

