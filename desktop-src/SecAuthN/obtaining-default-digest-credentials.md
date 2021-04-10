---
description: Sia i client che i server devono ottenere le credenziali prima di poter stabilire un contesto di sicurezza per lo scambio di messaggi.
ms.assetid: a72404b8-1ec9-4f58-b3a6-09811070ea29
title: Recupero delle credenziali del digest predefinite
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12e870d6bad1c3b4ef9e889a91444e98159bc758
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227379"
---
# <a name="obtaining-default-digest-credentials"></a>Recupero delle credenziali del digest predefinite

Sia i client che i server devono ottenere le [*credenziali*](../secgloss/c-gly.md) prima di poter stabilire un [*contesto di sicurezza*](../secgloss/s-gly.md) per lo scambio di messaggi. Il comportamento predefinito della funzione [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) è fornire le credenziali per l'entità di sicurezza associata alla [*sessione*](../secgloss/s-gly.md)di accesso corrente.

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



La chiamata sul lato client per le credenziali predefinite è identica, ad eccezione del terzo parametro è necessario specificare SECPKG \_ cred \_ in uscita per indicare che il client utilizzerà l'handle delle credenziali restituito dalla funzione.

Per un esempio in cui viene illustrato come ottenere le credenziali per un'entità di sicurezza diversa dall'utente connesso, vedere [acquisizione di credenziali alternative](obtaining-alternate-digest-credentials.md).

 

 
