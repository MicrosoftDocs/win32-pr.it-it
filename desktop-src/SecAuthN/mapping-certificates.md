---
description: Mapping dei certificati
ms.assetid: 4139f927-54f4-4968-a9eb-020401bb536d
title: Mapping dei certificati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 397a9ef8822d4f191ae37cdb998166fa54c2b12d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758258"
---
# <a name="mapping-certificates"></a><span data-ttu-id="7ebc9-103">Mapping dei certificati</span><span class="sxs-lookup"><span data-stu-id="7ebc9-103">Mapping Certificates</span></span>

> [!Note]  
> <span data-ttu-id="7ebc9-104">Le informazioni contenute in questo argomento sono valide solo per i server che richiedono l'autenticazione client.</span><span class="sxs-lookup"><span data-stu-id="7ebc9-104">The information in this topic is valid only for servers that require client authentication.</span></span>

 

<span data-ttu-id="7ebc9-105">Quando un'applicazione server richiede l'autenticazione client, Schannel prova automaticamente a eseguire il mapping del certificato fornito dal client a un account utente.</span><span class="sxs-lookup"><span data-stu-id="7ebc9-105">When a server application requires client authentication, Schannel automatically attempts to map the certificate supplied by the client to a user account.</span></span>

<span data-ttu-id="7ebc9-106">Una volta stabilito il [*contesto di sicurezza*](../secgloss/s-gly.md) , l'applicazione server può utilizzare la funzione [**QuerySecurityContextToken**](/windows/desktop/api/Sspi/nf-sspi-querysecuritycontexttoken) per ottenere un [*token di accesso*](../secgloss/a-gly.md) per l'account utente a cui è stato eseguito il mapping del [*certificato client*](../secgloss/c-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="7ebc9-106">After the [*security context*](../secgloss/s-gly.md) has been established, the server application can use the [**QuerySecurityContextToken**](/windows/desktop/api/Sspi/nf-sspi-querysecuritycontexttoken) function to obtain an [*access token*](../secgloss/a-gly.md) for the user account to which the [*client certificate*](../secgloss/c-gly.md) was mapped.</span></span> <span data-ttu-id="7ebc9-107">Inoltre, il server può utilizzare la funzione [**ImpersonateSecurityContext**](/windows/desktop/api/Sspi/nf-sspi-impersonatesecuritycontext) per rappresentare il client.</span><span class="sxs-lookup"><span data-stu-id="7ebc9-107">Also, the server can use the [**ImpersonateSecurityContext**](/windows/desktop/api/Sspi/nf-sspi-impersonatesecuritycontext) function to impersonate the client.</span></span>

<span data-ttu-id="7ebc9-108">Per ulteriori informazioni sull'autenticazione, vedere [esecuzione dell'autenticazione tramite Schannel](performing-authentication-using-schannel.md).</span><span class="sxs-lookup"><span data-stu-id="7ebc9-108">For more information on authentication, see [Performing Authentication Using Schannel](performing-authentication-using-schannel.md).</span></span>

 

 
