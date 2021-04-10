---
description: Microsoft Negotiate è un Security Support Provider che funge da livello di applicazione tra l'interfaccia del provider di supporto della sicurezza e gli altri SSP.
ms.assetid: 3aa7e979-8b55-416d-bed1-28296055d38e
title: Negoziazione Microsoft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7ce57a8f8924120dcce51e50e05de90fd6774b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966625"
---
# <a name="microsoft-negotiate"></a>Negoziazione Microsoft

Microsoft Negotiate è un [*Security Support Provider*](../secgloss/s-gly.md) (SSP) che funge da livello di applicazione tra [*Security Support Provider Interface*](../secgloss/s-gly.md) ([SSPI](sspi.md)) e gli altri SSP. Un'applicazione che chiama l'interfaccia SSPI per accedere a una rete può specificare un provider SSP per l'elaborazione della richiesta. Se l'applicazione specifica Negotiate, Negotiate analizza la richiesta e sceglie il provider SSP migliore per gestire la richiesta in base ai criteri di sicurezza configurati dal cliente.

Attualmente, il pacchetto di sicurezza Negotiate seleziona tra [Kerberos](microsoft-kerberos.md) e [NTLM](microsoft-ntlm.md). Negotiate seleziona Kerberos, a meno che non possa essere utilizzato da uno dei sistemi interessati dall'autenticazione o se l'applicazione chiamante non ha fornito informazioni sufficienti per l'utilizzo di Kerberos.

Per consentire a Negotiate di selezionare il provider di sicurezza [Kerberos](microsoft-kerberos.md) , l'applicazione client deve fornire un [*nome dell'entità servizio*](../secgloss/s-gly.md) (SPN), un nome dell'entità utente (UPN) o un nome di account NetBIOS come nome di destinazione. In caso contrario, Negotiate seleziona sempre il provider di sicurezza [NTLM](microsoft-ntlm.md) .

Un server che utilizza il pacchetto Negotiate è in grado di rispondere alle applicazioni client che selezionano in modo specifico il provider di sicurezza [Kerberos](microsoft-kerberos.md) o [NTLM](microsoft-ntlm.md) . È tuttavia necessario che un'applicazione client sappia che un server supporta il pacchetto Negotiate per richiedere l'autenticazione tramite Negotiate. Un server che non supporta Negotiate non è sempre in grado di rispondere alle richieste provenienti dai client che specificano Negotiate come SSP.

## <a name="reasons-to-use-the-negotiate-package"></a>Motivi per utilizzare il pacchetto Negotiate

-   Consente al sistema di utilizzare il protocollo più sicuro disponibile.
-   Garantisce la compatibilità con le edizioni con le applicazioni.
-   Garantisce che l'applicazione mostri il comportamento in base ai criteri di sicurezza impostati dal cliente.

 

 
