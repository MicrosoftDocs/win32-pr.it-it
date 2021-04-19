---
description: Microsoft Digest esegue un'autenticazione iniziale quando il server riceve la prima risposta di richiesta di verifica da un client.
ms.assetid: c65bb134-d480-4a71-872c-30e2884237a6
title: Autenticazione digest Microsoft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 336d5eb9c2d114bae70c28d07ed9fef64f9d0514
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315867"
---
# <a name="microsoft-digest-authentication"></a><span data-ttu-id="fc7c6-103">Autenticazione digest Microsoft</span><span class="sxs-lookup"><span data-stu-id="fc7c6-103">Microsoft Digest Authentication</span></span>

<span data-ttu-id="fc7c6-104">Microsoft Digest esegue un'autenticazione iniziale quando il server riceve la prima risposta di richiesta di verifica da un client.</span><span class="sxs-lookup"><span data-stu-id="fc7c6-104">Microsoft Digest performs an initial authentication when the server receives the first challenge response from a client.</span></span> <span data-ttu-id="fc7c6-105">Il server verifica che il client non sia stato autenticato, quindi esegue l'autenticazione iniziale accedendo ai servizi di un controller di dominio.</span><span class="sxs-lookup"><span data-stu-id="fc7c6-105">The server verifies that the client has not been authenticated and then performs the initial authentication by accessing the services of a domain controller.</span></span> <span data-ttu-id="fc7c6-106">Per una descrizione dettagliata di questa procedura, vedere [autenticazione iniziale con Microsoft Digest](initial-authentication-using-microsoft-digest.md).</span><span class="sxs-lookup"><span data-stu-id="fc7c6-106">For a detailed description of this procedure, see [Initial Authentication Using Microsoft Digest](initial-authentication-using-microsoft-digest.md).</span></span>

<span data-ttu-id="fc7c6-107">Quando l'autenticazione iniziale ha esito positivo, il server riceve una [*chiave di sessione*](../secgloss/s-gly.md)digest.</span><span class="sxs-lookup"><span data-stu-id="fc7c6-107">When the initial authentication is successful the server receives a Digest [*session key*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="fc7c6-108">Il server memorizza nella cache la chiave e la usa per autenticare le richieste successive di risorse dal client.</span><span class="sxs-lookup"><span data-stu-id="fc7c6-108">The server caches this key and uses it to authenticate subsequent requests for resources from the client.</span></span> <span data-ttu-id="fc7c6-109">Questa autenticazione è locale, ovvero non richiede l'accesso a un controller di dominio.</span><span class="sxs-lookup"><span data-stu-id="fc7c6-109">This authentication is local, that is, it does not require access to a domain controller.</span></span> <span data-ttu-id="fc7c6-110">Per una descrizione dettagliata di questa procedura, vedere [autenticazione delle richieste successive con Microsoft Digest](authenticating-subsequent-requests-using-microsoft-digest.md).</span><span class="sxs-lookup"><span data-stu-id="fc7c6-110">For a detailed description of this procedure see [Authenticating Subsequent Requests Using Microsoft Digest](authenticating-subsequent-requests-using-microsoft-digest.md).</span></span>

<span data-ttu-id="fc7c6-111">Quando si usa HTTP, non viene mantenuta alcuna connessione tra il client e il server.</span><span class="sxs-lookup"><span data-stu-id="fc7c6-111">When using HTTP, there is no connection maintained between client and server.</span></span> <span data-ttu-id="fc7c6-112">Per ridurre il traffico del controller di dominio e migliorare le prestazioni, Microsoft Digest memorizza nella cache le informazioni ricevute dopo il completamento dell'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="fc7c6-112">To reduce domain controller traffic and improve performance, Microsoft Digest caches information received after successful authentication.</span></span> <span data-ttu-id="fc7c6-113">Per informazioni su questo processo, vedere [gestione del contesto di sicurezza tra le connessioni](maintaining-the-security-context-between-connections.md).</span><span class="sxs-lookup"><span data-stu-id="fc7c6-113">For information about this process, see [Maintaining the Security Context Between Connections](maintaining-the-security-context-between-connections.md).</span></span>

 

 
