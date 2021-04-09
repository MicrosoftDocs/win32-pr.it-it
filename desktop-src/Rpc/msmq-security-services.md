---
title: Servizi di sicurezza MSMQ
description: I messaggi RPC sincroni possono utilizzare le funzionalità di sicurezza disponibili in fase di esecuzione RPC. Per ulteriori informazioni, vedere sicurezza.
ms.assetid: 0f4d45c4-7457-4449-8736-e141a95f6930
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffd2e12cd9f32a571088de769adb079327caab9b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104118095"
---
# <a name="msmq-security-services"></a><span data-ttu-id="d390f-104">Servizi di sicurezza MSMQ</span><span class="sxs-lookup"><span data-stu-id="d390f-104">MSMQ Security Services</span></span>

<span data-ttu-id="d390f-105">I messaggi RPC sincroni possono utilizzare le funzionalità di sicurezza disponibili in fase di esecuzione RPC.</span><span class="sxs-lookup"><span data-stu-id="d390f-105">Synchronous RPC messages can use any of the security features available from the RPC run time.</span></span> <span data-ttu-id="d390f-106">Per ulteriori informazioni, vedere [sicurezza](security.md) .</span><span class="sxs-lookup"><span data-stu-id="d390f-106">See [Security](security.md) for more details.</span></span>

<span data-ttu-id="d390f-107">Le chiamate asincrone al \[ [messaggio](/windows/desktop/Midl/message) \] non possono utilizzare la sicurezza RPC perché non esiste un handshake tra client e server.</span><span class="sxs-lookup"><span data-stu-id="d390f-107">Asynchronous \[ [message](/windows/desktop/Midl/message)\] calls cannot use RPC security because there is no handshake between client and server.</span></span> <span data-ttu-id="d390f-108">Infatti, il server potrebbe non essere ancora in esecuzione al momento della chiamata.</span><span class="sxs-lookup"><span data-stu-id="d390f-108">In fact, the server may not even be running at the time of the call.</span></span> <span data-ttu-id="d390f-109">Per accedere ai servizi di sicurezza forniti da servizi di Accodamento messaggi (MSMQ), l'applicazione client deve chiamare [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) per controllare il livello di autenticazione e privacy per le chiamate al server.</span><span class="sxs-lookup"><span data-stu-id="d390f-109">To access the security services provided by Message Queuing Services (MSMQ), the client application should call [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) to control the level of authentication and privacy for its calls to the server.</span></span>

<span data-ttu-id="d390f-110">L'applicazione server può chiamare [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) dall'interno di una chiamata di procedura remota per determinare il livello di sicurezza per la chiamata.</span><span class="sxs-lookup"><span data-stu-id="d390f-110">The server application can call [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) from within a remote procedure call to determine the security level for that call.</span></span> <span data-ttu-id="d390f-111">La tabella seguente illustra il mapping tra le costanti di sicurezza RPC e la sicurezza MSMQ.</span><span class="sxs-lookup"><span data-stu-id="d390f-111">The mapping between RPC security constants and MSMQ security is shown in the following table.</span></span>



| <span data-ttu-id="d390f-112">Livello di sicurezza RPC</span><span class="sxs-lookup"><span data-stu-id="d390f-112">RPC security level</span></span>                | <span data-ttu-id="d390f-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d390f-113">Description</span></span>                                                                                |
|-----------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="d390f-114">\_livello di autenticazione \_ RPC \_ None</span><span class="sxs-lookup"><span data-stu-id="d390f-114">RPC\_AUTHN\_LEVEL\_NONE</span></span>           | <span data-ttu-id="d390f-115">La chiamata non è autenticata o crittografata.</span><span class="sxs-lookup"><span data-stu-id="d390f-115">The call is not authenticated or encrypted.</span></span>                                                |
| <span data-ttu-id="d390f-116">\_ \_ integrità PKT a livello di autenticazione \_ RPC \_</span><span class="sxs-lookup"><span data-stu-id="d390f-116">RPC\_AUTHN\_LEVEL\_PKT\_INTEGRITY</span></span> | <span data-ttu-id="d390f-117">La chiamata viene autenticata utilizzando la sicurezza MSMQ.</span><span class="sxs-lookup"><span data-stu-id="d390f-117">The call is authenticated using MSMQ security.</span></span>                                             |
| <span data-ttu-id="d390f-118">\_ \_ privacy PKT a livello di autenticazione \_ RPC \_</span><span class="sxs-lookup"><span data-stu-id="d390f-118">RPC\_AUTHN\_LEVEL\_PKT\_PRIVACY</span></span>   | <span data-ttu-id="d390f-119">La chiamata viene autenticata e crittografata mentre viene spostata tra la coda del client e del server.</span><span class="sxs-lookup"><span data-stu-id="d390f-119">The call is authenticated and encrypted as it travels between the client and server queue.</span></span> |



 

<span data-ttu-id="d390f-120">Il server è anche in grado di forzare l'autenticazione e la crittografia delle chiamate chiamando [**RpcServerUseProtseqEpEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex) e impostando il livello di autenticazione RPC c mq, l'integrità PKT e i flag di privacy del livello auth c mq di RPC \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ nella struttura dei [**\_ criteri RPC**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy) .</span><span class="sxs-lookup"><span data-stu-id="d390f-120">The server can also force call authentication and encryption by calling [**RpcServerUseProtseqEpEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex) and setting the RPC\_C\_MQ\_AUTHN\_LEVEL\_NONE, RPC\_C\_MQ\_AUTHN\_LEVEL\_PKT\_INTEGRITY and RPC\_C\_MQ\_AUTHN\_LEVEL\_PKT\_PRIVACY flags in the [**RPC\_POLICY**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy) structure.</span></span>

 

 