---
description: Sia i client che i server devono ottenere le credenziali prima di poter stabilire un contesto di sicurezza per lo scambio di messaggi.
ms.assetid: a72404b8-1ec9-4f58-b3a6-09811070ea29
title: Recupero delle credenziali digest predefinite
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93d5a0bb39f59680f2b5232dae1e6cc5c83673cf31c7cc3e0aa1325d5641e161
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117786589"
---
# <a name="obtaining-default-digest-credentials"></a>Recupero delle credenziali digest predefinite

Sia i client che i server devono [*ottenere le credenziali*](../secgloss/c-gly.md) prima di poter stabilire un contesto di sicurezza [*per*](../secgloss/s-gly.md) lo scambio di messaggi. Il comportamento predefinito della [**funzione AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) è fornire le credenziali per l'entità di sicurezza associata alla sessione di accesso [*corrente.*](../secgloss/s-gly.md)

Nell'esempio seguente viene illustrata una chiamata sul lato server per ottenere le credenziali predefinite.


```C++
SECURITY_STATUS SecStatus; 
TimeStamp tsLifetime; 
CredHandle hCred;
SecStatus = AcquireCredentialsHandle (
       NULL,                  // Default principal.
       WDIGEST_SP_NAME,       // Microsoft Digest SSP. 
       SECPKG_CRED_INBOUND,   // Server will use the credentials.
       NULL,                  // Use the current LOGON id.
       NULL,                  // Default credentials.
       NULL,                  // Not used with Digest SSP.
       NULL,                  // Not used with Digest SSP.
       &hCred,                // Receives the credential handle.
       &tsLifetime            // Receives the credential time limit.
);
```



La chiamata lato client per le credenziali predefinite è identica, ad eccezione del fatto che il terzo parametro deve specificare SECPKG CRED OUTBOUND per indicare che il client userà l'handle delle credenziali restituito \_ \_ dalla funzione.

Per un esempio in cui viene illustrato come ottenere le credenziali per un'entità di sicurezza diversa dall'utente connesso, vedere [Obtaining Alternate Credentials](obtaining-alternate-digest-credentials.md).

 

 
