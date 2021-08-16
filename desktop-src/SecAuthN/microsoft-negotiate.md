---
description: Microsoft Negotiate è un provider di supporto per la sicurezza che funge da livello applicazione tra Security Support Provider Interface e gli altri provider di servizi SSP.
ms.assetid: 3aa7e979-8b55-416d-bed1-28296055d38e
title: Negoziazione Microsoft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebd223267a2e7d0e4dc23ae356a6fa2e6224c742c491e428369f15fb6d46ff73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117786953"
---
# <a name="microsoft-negotiate"></a>Negoziazione Microsoft

Microsoft Negotiate è un provider di [*supporto*](../secgloss/s-gly.md) per la sicurezza (SSP) che funge da livello dell'applicazione tra [*Security Support Provider Interface*](../secgloss/s-gly.md) [(SSPI)](sspi.md)e gli altri provider di servizi di sicurezza. Un'applicazione che chiama l'interfaccia SSPI per accedere a una rete può specificare un provider SSP per l'elaborazione della richiesta. Se l'applicazione specifica Negotiate, Negotiate analizza la richiesta e sceglie il provider di servizi di configurazione migliore per gestire la richiesta in base ai criteri di sicurezza configurati dal cliente.

Attualmente, il pacchetto di sicurezza Negotiate seleziona tra [Kerberos](microsoft-kerberos.md) [e NTLM.](microsoft-ntlm.md) Negotiate seleziona Kerberos a meno che non possa essere utilizzato da uno dei sistemi coinvolti nell'autenticazione o l'applicazione chiamante non abbia fornito informazioni sufficienti per utilizzare Kerberos.

Per consentire a Negotiate di selezionare il provider di sicurezza [Kerberos,](microsoft-kerberos.md) l'applicazione client deve fornire un nome dell'entità servizio [](../secgloss/s-gly.md) (SPN), un nome dell'entità utente (UPN) o un nome di account NetBIOS come nome di destinazione. In caso contrario, Negotiate seleziona sempre il provider [di sicurezza NTLM.](microsoft-ntlm.md)

Un server che utilizza il pacchetto Negotiate è in grado di rispondere alle applicazioni client che selezionano in modo specifico il provider di sicurezza [Kerberos](microsoft-kerberos.md) [o NTLM.](microsoft-ntlm.md) Tuttavia, un'applicazione client deve sapere che un server supporta il pacchetto Negotiate per richiedere l'autenticazione tramite Negotiate. Un server che non supporta Negotiate non può sempre rispondere alle richieste dei client che specificano Negotiate come SSP.

## <a name="reasons-to-use-the-negotiate-package"></a>Motivi per usare il pacchetto Negotiate

-   Consente al sistema di usare il protocollo più sicuro disponibile.
-   Garantisce la compatibilità con l'inoltro per l'applicazione.
-   Garantisce che l'applicazione presenti un comportamento conforme ai criteri di sicurezza impostati dal cliente.

 

 
