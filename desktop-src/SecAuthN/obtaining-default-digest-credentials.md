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
# <a name="obtaining-default-digest-credentials"></a><span data-ttu-id="9e21a-103">Recupero delle credenziali del digest predefinite</span><span class="sxs-lookup"><span data-stu-id="9e21a-103">Obtaining Default Digest Credentials</span></span>

<span data-ttu-id="9e21a-104">Sia i client che i server devono ottenere le [*credenziali*](../secgloss/c-gly.md) prima di poter stabilire un [*contesto di sicurezza*](../secgloss/s-gly.md) per lo scambio di messaggi.</span><span class="sxs-lookup"><span data-stu-id="9e21a-104">Both clients and servers must obtain [*credentials*](../secgloss/c-gly.md) before they can establish a [*security context*](../secgloss/s-gly.md) for message exchange.</span></span> <span data-ttu-id="9e21a-105">Il comportamento predefinito della funzione [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) è fornire le credenziali per l'entità di sicurezza associata alla [*sessione*](../secgloss/s-gly.md)di accesso corrente.</span><span class="sxs-lookup"><span data-stu-id="9e21a-105">The default behavior of the [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) function is to provide credentials for the security principal associated with the current logon [*session*](../secgloss/s-gly.md).</span></span>

<span data-ttu-id="9e21a-106">Nell'esempio seguente viene illustrata una chiamata sul lato server per ottenere le credenziali predefinite.</span><span class="sxs-lookup"><span data-stu-id="9e21a-106">The following example demonstrates a server-side call to obtain the default credentials.</span></span>


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



<span data-ttu-id="9e21a-107">La chiamata sul lato client per le credenziali predefinite è identica, ad eccezione del terzo parametro è necessario specificare SECPKG \_ cred \_ in uscita per indicare che il client utilizzerà l'handle delle credenziali restituito dalla funzione.</span><span class="sxs-lookup"><span data-stu-id="9e21a-107">The client-side call for default credentials is identical, except the third parameter must specify SECPKG\_CRED\_OUTBOUND to indicate that the client will use the credentials handle returned by the function.</span></span>

<span data-ttu-id="9e21a-108">Per un esempio in cui viene illustrato come ottenere le credenziali per un'entità di sicurezza diversa dall'utente connesso, vedere [acquisizione di credenziali alternative](obtaining-alternate-digest-credentials.md).</span><span class="sxs-lookup"><span data-stu-id="9e21a-108">For an example that demonstrates obtaining credentials for a security principal other than the logged on user, see [Obtaining Alternate Credentials](obtaining-alternate-digest-credentials.md).</span></span>

 

 
