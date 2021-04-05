---
title: Provider di sicurezza da usare
description: Tutti gli altri elementi sono uguali, usano RPC \_ c \_ AuthN \_ GSS \_ Kerberos o RPC \_ c \_ AuthN \_ GSS \_ Negotiate.
ms.assetid: 921975ae-17e7-433a-bbc5-e6b95989d31a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33248d989031390b1b57730c637829922d15166a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710570"
---
# <a name="which-security-provider-to-use"></a><span data-ttu-id="76de6-103">Provider di sicurezza da usare</span><span class="sxs-lookup"><span data-stu-id="76de6-103">Which Security Provider to Use</span></span>

<span data-ttu-id="76de6-104">Tutti gli altri elementi sono uguali, usano RPC \_ c \_ AuthN \_ GSS \_ Kerberos o RPC \_ c \_ AuthN \_ GSS \_ Negotiate.</span><span class="sxs-lookup"><span data-stu-id="76de6-104">All other things being equal, use RPC\_C\_AUTHN\_GSS\_KERBEROS or RPC\_C\_AUTHN\_GSS\_NEGOTIATE.</span></span> <span data-ttu-id="76de6-105">Ogni fornisce il servizio più scalabile e sicuro.</span><span class="sxs-lookup"><span data-stu-id="76de6-105">Each provides the most scalable and secure service.</span></span> <span data-ttu-id="76de6-106">Se si usa \_ \_ \_ la negoziazione GSS C AuthN GSS \_ sul server, ciò consente ai client legacy, ad esempio i client NTLM, di connettersi al server.</span><span class="sxs-lookup"><span data-stu-id="76de6-106">If you use RPC\_C\_AUTHN\_GSS\_NEGOTIATE on the server, this allows down-level clients, such as NTLM clients, to connect to your server.</span></span> <span data-ttu-id="76de6-107">Se ciò non è auspicabile, limitare la scelta al solo tipo di autenticazione in base al protocollo di autenticazione basata su \_ \_ GSS di RPC C \_ \_ oppure chiamare [**RpcBindingInqAuthClientEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclientex) per determinare il provider di sicurezza utilizzato dal client e negare l'accesso ai client tramite NTLM.</span><span class="sxs-lookup"><span data-stu-id="76de6-107">If that is undesirable, either limit the choice to RPC\_C\_AUTHN\_GSS\_KERBEROS only, or call [**RpcBindingInqAuthClientEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclientex) to determine which security provider the client is using, and deny access to clients using NTLM.</span></span> <span data-ttu-id="76de6-108">Il metodo preferito per stabilire il provider di sicurezza usato dal client è la funzione [**RpcServerInqCallAttributes**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcserverinqcallattributesa) .</span><span class="sxs-lookup"><span data-stu-id="76de6-108">The preferred method of establishing which security provider the client is using is the [**RpcServerInqCallAttributes**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcserverinqcallattributesa) function.</span></span>

 

 




