---
title: Scrittura di un server SSPI autenticato
description: Prima che la comunicazione autenticata possa essere eseguita tra i programmi client e server, il server deve registrare le informazioni di autenticazione.
ms.assetid: 723ae1ee-d729-4748-9ef1-062a0c6f60d0
keywords:
- RPC (Remote Procedure Call), attività, scrittura di un server SSPI autenticato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19b1cb06cfc626bc8130f3c4b0cee0a7b6d7893e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044665"
---
# <a name="writing-an-authenticated-sspi-server"></a><span data-ttu-id="0d07c-104">Scrittura di un server SSPI autenticato</span><span class="sxs-lookup"><span data-stu-id="0d07c-104">Writing an Authenticated SSPI Server</span></span>

<span data-ttu-id="0d07c-105">Prima che la comunicazione autenticata possa essere eseguita tra i programmi client e server, il server deve registrare le informazioni di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="0d07c-105">Before authenticated communication can take place between the client and server programs, the server must register its authentication information.</span></span> <span data-ttu-id="0d07c-106">In particolare, il server deve registrare il nome principale e specificare il servizio di autenticazione usato.</span><span class="sxs-lookup"><span data-stu-id="0d07c-106">In particular, the server must register its principal name and specify the authentication service it uses.</span></span> <span data-ttu-id="0d07c-107">Per ulteriori informazioni sui nomi di entità, vedere [nomi principali](principal-names.md).</span><span class="sxs-lookup"><span data-stu-id="0d07c-107">For more information on principal names, see [Principal Names](principal-names.md).</span></span> <span data-ttu-id="0d07c-108">Per informazioni dettagliate sui servizi di autenticazione, vedere [servizi di autenticazione](authentication-services.md).</span><span class="sxs-lookup"><span data-stu-id="0d07c-108">For details about authentication services, see [Authentication Services](authentication-services.md).</span></span>

<span data-ttu-id="0d07c-109">Per registrare le informazioni di autenticazione, i server chiamano la funzione [**RpcServerRegisterAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterauthinfo) .</span><span class="sxs-lookup"><span data-stu-id="0d07c-109">To register its authentication information, servers call the [**RpcServerRegisterAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterauthinfo) function.</span></span> <span data-ttu-id="0d07c-110">Passare un puntatore al nome dell'entità come valore del primo parametro.</span><span class="sxs-lookup"><span data-stu-id="0d07c-110">Pass a pointer to the principal name as the value of the first parameter.</span></span> <span data-ttu-id="0d07c-111">Impostare il secondo parametro su una costante che indica il servizio di autenticazione che l'applicazione utilizzerà.</span><span class="sxs-lookup"><span data-stu-id="0d07c-111">Set the second parameter to a constant indicating the authentication service that the application will use.</span></span> <span data-ttu-id="0d07c-112">Per una descrizione dei servizi di autenticazione, vedere [costanti del servizio di autenticazione](authentication-service-constants.md).</span><span class="sxs-lookup"><span data-stu-id="0d07c-112">For a description of authentication services, see [Authentication-Service Constants](authentication-service-constants.md).</span></span>

<span data-ttu-id="0d07c-113">Il server può anche passare l'indirizzo di una funzione di acquisizione chiave come valore del terzo parametro.</span><span class="sxs-lookup"><span data-stu-id="0d07c-113">The server may also pass the address of a key acquisition function as the value of the third parameter.</span></span> <span data-ttu-id="0d07c-114">Vedere [funzioni di acquisizione chiavi](key-acquisition-functions.md).</span><span class="sxs-lookup"><span data-stu-id="0d07c-114">See [Key Acquisition Functions](key-acquisition-functions.md).</span></span> <span data-ttu-id="0d07c-115">Per usare la funzione di acquisizione chiave predefinita per il servizio di autenticazione selezionato, impostare il terzo parametro su **null**.</span><span class="sxs-lookup"><span data-stu-id="0d07c-115">To use the default key acquisition function for the selected authentication service, set the third parameter to **NULL**.</span></span> <span data-ttu-id="0d07c-116">L'ultimo parametro della funzione [**RpcServerRegisterAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterauthinfo) è costituito dai dati del puntatore da passare alla funzione di acquisizione della chiave, se si specifica una funzione di acquisizione della chiave.</span><span class="sxs-lookup"><span data-stu-id="0d07c-116">The last parameter to the [**RpcServerRegisterAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterauthinfo) function is a pointer data to pass to the key acquisition function, if you provide a key acquisition function.</span></span> <span data-ttu-id="0d07c-117">Nel frammento di codice seguente viene mostrata una chiamata a **RpcServerRegisterAuthInfo** .</span><span class="sxs-lookup"><span data-stu-id="0d07c-117">A call to **RpcServerRegisterAuthInfo** is shown in the following code fragment.</span></span>


```C++
dwStatus = DsMakeSpn(
    "ldap",
    "ServerName.domain.com",
    NULL,
    0,
    NULL,
    &pcSpnLength,
    pszSpn);

rpcStatus = RpcServerRegisterAuthInfo (
    psz,                                   // Server principal name
    RPC_C_AUTHN_GSS_NEGOTIATE,             // Authentication service
    NULL,                                  // Use default key function
    NULL);                                 // No arg for key function
```



<span data-ttu-id="0d07c-118">Inoltre, il server può fornire la libreria di runtime RPC con una funzione di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="0d07c-118">In addition, the server may provide the RPC run-time library with an authorization function.</span></span> <span data-ttu-id="0d07c-119">Per impostare una funzione di autorizzazione, chiamare la funzione [**RpcMgmtSetAuthorizationFn**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetauthorizationfn) .</span><span class="sxs-lookup"><span data-stu-id="0d07c-119">To set an authorization function, call the [**RpcMgmtSetAuthorizationFn**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetauthorizationfn) function.</span></span>

<span data-ttu-id="0d07c-120">La parte relativa al server di un'applicazione distribuita può chiamare la funzione [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) o [**RpcBindingInqAuthClientEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclientex) per eseguire una query su un handle di binding per le informazioni di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="0d07c-120">The server portion of a distributed application can call the function [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) or [**RpcBindingInqAuthClientEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclientex) to query a binding handle for authentication information.</span></span>

<span data-ttu-id="0d07c-121">Se il server viene registrato con un Security Support Provider, le chiamate client con credenziali non valide non verranno inviate.</span><span class="sxs-lookup"><span data-stu-id="0d07c-121">If your server registers with a security support provider, client calls with invalid credentials will not be dispatched.</span></span> <span data-ttu-id="0d07c-122">Tuttavia, le chiamate senza credenziali verranno inviate.</span><span class="sxs-lookup"><span data-stu-id="0d07c-122">However, calls with no credentials will be dispatched.</span></span> <span data-ttu-id="0d07c-123">Esistono tre modi per evitare che ciò accada:</span><span class="sxs-lookup"><span data-stu-id="0d07c-123">There are three ways to prevent this from happening:</span></span>

-   <span data-ttu-id="0d07c-124">Registrare l'interfaccia usando [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)con una funzione di callback di sicurezza. in questo modo la libreria di runtime RPC rifiuterà automaticamente le chiamate non autenticate a tale interfaccia.</span><span class="sxs-lookup"><span data-stu-id="0d07c-124">Register the interface using [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex), with a security callback function; this will cause the RPC run-time library to automatically reject unauthenticated calls to that interface.</span></span> <span data-ttu-id="0d07c-125">La registrazione di una funzione di callback è compatibile con altri metodi di controllo delle credenziali di accesso. la funzione di callback può chiamare le funzioni [**RpcImpersonateClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient), [**RpcGetAuthorizationContextForClient**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient)o [**RpcBindingInqAuthClientEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) o altre.</span><span class="sxs-lookup"><span data-stu-id="0d07c-125">Registering a callback function is compatible with other methods of checking access credentials; the callback function can itself call the [**RpcImpersonateClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient), [**RpcGetAuthorizationContextForClient**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient), or [**RpcBindingInqAuthClientEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) functions, or others.</span></span> <span data-ttu-id="0d07c-126">Tuttavia, queste funzioni non possono usare gli argomenti passati alla funzione, in quanto non vengono sottoposte a marshalling.</span><span class="sxs-lookup"><span data-stu-id="0d07c-126">However, these functions cannot use the arguments passed to the function, as they are not unmarshalled at that point.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0d07c-127">La registrazione dell'interfaccia tramite [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) con una funzione di callback di sicurezza è il metodo più consigliato per verificare le credenziali client.</span><span class="sxs-lookup"><span data-stu-id="0d07c-127">Registering the interface using [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) with a security callback function is the most heavily recommended method of checking client credentials.</span></span>

 

-   <span data-ttu-id="0d07c-128">Chiamare [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) per determinare il livello di sicurezza utilizzato dal client.</span><span class="sxs-lookup"><span data-stu-id="0d07c-128">Call [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) to determine the security level that the client is using.</span></span> <span data-ttu-id="0d07c-129">Lo stub può quindi restituire un errore se il client non è autenticato.</span><span class="sxs-lookup"><span data-stu-id="0d07c-129">Your stub can then return an error if the client is unauthenticated.</span></span>

 

 




