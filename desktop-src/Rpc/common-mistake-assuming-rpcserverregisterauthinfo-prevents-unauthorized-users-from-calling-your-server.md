---
title: Errore comune che presuppone che RpcServerRegisterAuthInfo impedisca a utenti non autorizzati di chiamare il server
description: Quando i provider di sicurezza sono registrati nel server con la funzione RpcServerRegisterAuthInfo, viene aggiunta un'opzione, non un requisito.
ms.assetid: c8db8973-6d47-47b4-b927-72cfb464e9f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 453a60c800d377dc122de561b87c41a5ec635328
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713339"
---
# <a name="common-mistake-assuming-rpcserverregisterauthinfo-prevents-unauthorized-users-from-calling-your-server"></a><span data-ttu-id="caf60-103">Errore comune: supponendo che RpcServerRegisterAuthInfo impedisca a utenti non autorizzati di chiamare il server</span><span class="sxs-lookup"><span data-stu-id="caf60-103">Common Mistake: Assuming RpcServerRegisterAuthInfo Prevents Unauthorized Users from Calling your Server</span></span>

<span data-ttu-id="caf60-104">Quando i provider di sicurezza sono registrati nel server con la funzione [**RpcServerRegisterAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterauthinfo) , viene aggiunta un'opzione, non un requisito.</span><span class="sxs-lookup"><span data-stu-id="caf60-104">When security providers are registered on the server with the [**RpcServerRegisterAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterauthinfo) function, an option is added, not a requirement.</span></span> <span data-ttu-id="caf60-105">Ciò significa che le registrazioni precedenti con **RpcServerRegisterAuthInfo** non vengono sostituite.</span><span class="sxs-lookup"><span data-stu-id="caf60-105">This means previous registrations with **RpcServerRegisterAuthInfo** are not replaced.</span></span> <span data-ttu-id="caf60-106">Ciò significa anche che i client non autenticati possono ancora connettersi.</span><span class="sxs-lookup"><span data-stu-id="caf60-106">This also means unauthenticated clients still can connect.</span></span> <span data-ttu-id="caf60-107">Chiamando la funzione **RpcServerRegisterAuthInfo** , i client non autenticati non sono consentiti dalla connessione. possono comunque connettersi, ma le chiamate di funzione, ad esempio [**RpcImpersonateClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient) e [**RpcGetAuthorizationContextForClient**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient) , avranno esito negativo.</span><span class="sxs-lookup"><span data-stu-id="caf60-107">By calling the **RpcServerRegisterAuthInfo** function, unauthenticated clients are not disallowed from connecting; they can still connect, but function calls such as [**RpcImpersonateClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient) and [**RpcGetAuthorizationContextForClient**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient) will fail.</span></span> <span data-ttu-id="caf60-108">Quindi, quando viene chiamata la funzione **RpcServerRegisterAuthInfo** , i potenziali utenti malintenzionati non sono stati eliminati, ma i client che dovrebbero avere accesso hanno la possibilità di dimostrare la propria identità.</span><span class="sxs-lookup"><span data-stu-id="caf60-108">So when the **RpcServerRegisterAuthInfo** function is called, potential attackers have not been weeded out—rather, clients that ought to have access are given a chance to prove their identity.</span></span> <span data-ttu-id="caf60-109">È necessario che siano ancora presenti controlli per determinare se i potenziali utenti malintenzionati tentano di connettersi.</span><span class="sxs-lookup"><span data-stu-id="caf60-109">Checks must still be in place to determine whether potential attackers are attempting to connect.</span></span>

 

 




