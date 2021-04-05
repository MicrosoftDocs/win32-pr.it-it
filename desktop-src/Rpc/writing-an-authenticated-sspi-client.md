---
title: Scrittura di un client SSPI autenticato
description: Scrittura di un client SSPI autenticato e di una chiamata di procedura remota (RPC).
ms.assetid: db39d3bf-84fa-466e-9ba1-ba17f64c8f8d
keywords:
- RPC (Remote Procedure Call), attività, scrittura di un client SSPI autenticato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c8476772a2ed652f6646b078c2876234cbcc0d6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104118138"
---
# <a name="writing-an-authenticated-sspi-client"></a><span data-ttu-id="ffcf9-104">Scrittura di un client SSPI autenticato</span><span class="sxs-lookup"><span data-stu-id="ffcf9-104">Writing an Authenticated SSPI Client</span></span>

<span data-ttu-id="ffcf9-105">Per tutte le sessioni client/server RPC è necessaria un'associazione tra il client e il server.</span><span class="sxs-lookup"><span data-stu-id="ffcf9-105">All RPC client/server sessions require a binding between the client and the server.</span></span> <span data-ttu-id="ffcf9-106">Per aggiungere sicurezza alle applicazioni client/server, i programmi devono utilizzare un'associazione autenticata.</span><span class="sxs-lookup"><span data-stu-id="ffcf9-106">To add security to client/server applications, the programs must use an authenticated binding.</span></span> <span data-ttu-id="ffcf9-107">In questa sezione viene descritto il processo di creazione di un'associazione autenticata tra il client e il server.</span><span class="sxs-lookup"><span data-stu-id="ffcf9-107">This section describes the process of creating an authenticated binding between the client and the server.</span></span>

-   [<span data-ttu-id="ffcf9-108">Creazione di handle di binding lato client</span><span class="sxs-lookup"><span data-stu-id="ffcf9-108">Creating Client-side Binding Handles</span></span>](#creating-client-side-binding-handles)
-   [<span data-ttu-id="ffcf9-109">Fornire le credenziali client al server</span><span class="sxs-lookup"><span data-stu-id="ffcf9-109">Providing Client Credentials to the Server</span></span>](#providing-client-credentials-to-the-server)

<span data-ttu-id="ffcf9-110">Per informazioni correlate, vedere [procedure utilizzate con la maggior parte dei pacchetti di sicurezza e protocolli](/windows/desktop/SecAuthN/procedures-used-with-most-security-packages-and-protocols) nel Software Development Kit (SDK) della piattaforma.</span><span class="sxs-lookup"><span data-stu-id="ffcf9-110">For related information, see [Procedures Used with Most Security Packages and Protocols](/windows/desktop/SecAuthN/procedures-used-with-most-security-packages-and-protocols) in the Platform Software Development Kit (SDK).</span></span>

## <a name="creating-client-side-binding-handles"></a><span data-ttu-id="ffcf9-111">Creazione di handle di binding lato client</span><span class="sxs-lookup"><span data-stu-id="ffcf9-111">Creating Client-side Binding Handles</span></span>

<span data-ttu-id="ffcf9-112">Per creare una sessione autenticata con un programma server, le applicazioni client devono fornire informazioni di autenticazione con il relativo handle di binding.</span><span class="sxs-lookup"><span data-stu-id="ffcf9-112">To create an authenticated session with a server program, client applications must provide authentication information with their binding handle.</span></span> <span data-ttu-id="ffcf9-113">Per impostare un handle di binding autenticato, i client richiamano la funzione [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) o [**RpcBindingSetAuthInfoEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa) .</span><span class="sxs-lookup"><span data-stu-id="ffcf9-113">To set up an authenticated binding handle, clients invoke the [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) or [**RpcBindingSetAuthInfoEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa) function.</span></span> <span data-ttu-id="ffcf9-114">Queste due funzioni sono quasi identiche.</span><span class="sxs-lookup"><span data-stu-id="ffcf9-114">These two functions are nearly identical.</span></span> <span data-ttu-id="ffcf9-115">L'unica differenza è che il client può specificare la qualità del servizio con la funzione **RpcBindingSetAuthInfoEx** .</span><span class="sxs-lookup"><span data-stu-id="ffcf9-115">The only difference between them is that the client can specify the quality of service with the **RpcBindingSetAuthInfoEx** function.</span></span>

<span data-ttu-id="ffcf9-116">Il frammento di codice seguente mostra come potrebbe apparire una chiamata a [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) .</span><span class="sxs-lookup"><span data-stu-id="ffcf9-116">The following code fragment shows how a call to [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) might look.</span></span>


```C++
// This code fragment assumes that rpcBinding is a valid binding 
// handle between the client and the server. It also assumes that
// pAuthCredentials is a valid pointer to a data structure which
// contains the user's authentication credentials.

dwStatus = DsMakeSpn(
    "ldap",
    "ServerName.domain.com",
    NULL,
    0,
    NULL,
    &pcSpnLength,
    pszSpn);

//...

rpcStatus = RpcBindingSetAuthInfo(
    rpcBinding,                       // Valid binding handle
    pszSpn,                           // Principal name 
    RPC_C_AUTHN_LEVEL_PKT_INTEGRITY,  // Authentication level
    RPC_C_AUTHN_GSS_NEGOTIATE,        // Use Negotiate SSP
    NULL,                             // Authentication credentials <entity type="ndash"/> use current thread credentials
    RPC_C_AUTHZ_NAME);                // Authorization service
```



<span data-ttu-id="ffcf9-117">Dopo che il client ha correttamente chiamato le funzioni [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) o [**RpcBindingSetAuthInfoEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa) , la libreria di runtime RPC autentica automaticamente tutte le chiamate RPC nell'associazione.</span><span class="sxs-lookup"><span data-stu-id="ffcf9-117">After the client successfully calls the [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) or [**RpcBindingSetAuthInfoEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa) functions, the RPC run-time library automatically authenticates all RPC calls on the binding.</span></span> <span data-ttu-id="ffcf9-118">Il livello di sicurezza e autenticazione selezionato dal client si applica solo a tale handle di associazione.</span><span class="sxs-lookup"><span data-stu-id="ffcf9-118">The level of security and authentication that the client selects applies only to that binding handle.</span></span> <span data-ttu-id="ffcf9-119">Gli handle di contesto derivati dall'handle di associazione utilizzeranno le stesse informazioni di sicurezza, ma le modifiche successive all'handle di associazione non verranno riflesse negli handle di contesto.</span><span class="sxs-lookup"><span data-stu-id="ffcf9-119">Context handles derived from the binding handle will use the same security information, but subsequent modifications to the binding handle will not be reflected in the context handles.</span></span> <span data-ttu-id="ffcf9-120">Per altre informazioni, vedere [handle di contesto](context-handles.md).</span><span class="sxs-lookup"><span data-stu-id="ffcf9-120">For more information, see [Context Handles](context-handles.md).</span></span>

<span data-ttu-id="ffcf9-121">Il livello di autenticazione rimane attivo fino a quando il client non sceglie un altro livello o fino a quando non termina il processo.</span><span class="sxs-lookup"><span data-stu-id="ffcf9-121">The authentication level stays in effect until the client chooses another level, or until the process terminates.</span></span> <span data-ttu-id="ffcf9-122">Per la maggior parte delle applicazioni non è necessaria una modifica nel livello di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="ffcf9-122">Most applications will not require a change in the security level.</span></span> <span data-ttu-id="ffcf9-123">Il client può eseguire una query su qualsiasi handle di binding per ottenere le informazioni di autorizzazione richiamando [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) e passando l'handle di associazione.</span><span class="sxs-lookup"><span data-stu-id="ffcf9-123">The client can query any binding handle to obtain its authorization information by invoking [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) and passing it the binding handle.</span></span>

## <a name="providing-client-credentials-to-the-server"></a><span data-ttu-id="ffcf9-124">Fornire le credenziali client al server</span><span class="sxs-lookup"><span data-stu-id="ffcf9-124">Providing Client Credentials to the Server</span></span>

<span data-ttu-id="ffcf9-125">Per applicare la sicurezza, i server utilizzano le informazioni di associazione del client.</span><span class="sxs-lookup"><span data-stu-id="ffcf9-125">Servers use the client's binding information to enforce security.</span></span> <span data-ttu-id="ffcf9-126">I client passano sempre un handle di associazione come primo parametro di una chiamata di procedura remota.</span><span class="sxs-lookup"><span data-stu-id="ffcf9-126">Clients always pass a binding handle as the first parameter of a remote procedure call.</span></span> <span data-ttu-id="ffcf9-127">Tuttavia, i server non possono utilizzare l'handle a meno che non venga dichiarato come primo parametro per le procedure remote nel file IDL o nel file di configurazione dell'applicazione (ACF) del server.</span><span class="sxs-lookup"><span data-stu-id="ffcf9-127">However, servers cannot use the handle unless it is declared as the first parameter to remote procedures in either the IDL file or in the server's application configuration file (ACF).</span></span> <span data-ttu-id="ffcf9-128">È possibile scegliere di elencare il punto di controllo dell'associazione nel file IDL, ma ciò impone a tutti i client di dichiarare e manipolare l'handle di binding anziché utilizzare l'associazione automatica o implicita.</span><span class="sxs-lookup"><span data-stu-id="ffcf9-128">You can choose to list the binding handle in the IDL file, but this forces all clients to declare and manipulate the binding handle rather than using automatic or implicit binding.</span></span> <span data-ttu-id="ffcf9-129">Per ulteriori informazioni, vedere [i file IDL e ACF](the-idl-and-acf-files.md).</span><span class="sxs-lookup"><span data-stu-id="ffcf9-129">For further information, see [The IDL and ACF Files](the-idl-and-acf-files.md).</span></span>

<span data-ttu-id="ffcf9-130">Un altro metodo consiste nel lasciare gli handle dell'associazione fuori dal file IDL e inserire l' **attributo \_ handle esplicito** nell'ACF del server.</span><span class="sxs-lookup"><span data-stu-id="ffcf9-130">Another method is to leave the binding handles out of the IDL file and to place the **explicit\_handle** attribute into the server's ACF.</span></span> <span data-ttu-id="ffcf9-131">In questo modo, il client può utilizzare il tipo di associazione più adatto all'applicazione, mentre il server utilizza l'handle di associazione come se fosse stato dichiarato in modo esplicito.</span><span class="sxs-lookup"><span data-stu-id="ffcf9-131">In this way, the client can use the type of binding best suited to the application, while the server uses the binding handle as though it were declared explicitly.</span></span>

<span data-ttu-id="ffcf9-132">Il processo di estrazione delle credenziali client dall'handle di binding si verifica nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="ffcf9-132">The process of extracting the client credentials from the binding handle occurs as follows:</span></span>

-   <span data-ttu-id="ffcf9-133">I client RPC chiamano [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) e includono le informazioni di autenticazione come parte delle informazioni di binding passate al server.</span><span class="sxs-lookup"><span data-stu-id="ffcf9-133">RPC clients call [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) and include their authentication information as part of the binding information passed to the server.</span></span>
-   <span data-ttu-id="ffcf9-134">Il server chiama in genere [**RpcImpersonateClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient) per comportarsi come se fosse il client.</span><span class="sxs-lookup"><span data-stu-id="ffcf9-134">Usually, the server calls [**RpcImpersonateClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient) in order to behave as though it were the client.</span></span> <span data-ttu-id="ffcf9-135">Se l'handle di associazione non è autenticato, la chiamata ha esito negativo e \_ \_ non è \_ disponibile alcun contesto \_ .</span><span class="sxs-lookup"><span data-stu-id="ffcf9-135">If the binding handle is not authenticated, the call fails with RPC\_S\_NO\_CONTEXT\_AVAILABLE.</span></span> <span data-ttu-id="ffcf9-136">Per ottenere il nome utente del client, chiamare [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) durante la rappresentazione o in Windows XP o versioni successive di Windows, chiamare [**RpcGetAuthorizationContextForClient**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient) per ottenere il contesto di autorizzazione, quindi utilizzare le funzioni Authz per recuperare il nome.</span><span class="sxs-lookup"><span data-stu-id="ffcf9-136">To obtain the client's user name, call [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) while impersonating, or on Windows XP or later versions of Windows, call [**RpcGetAuthorizationContextForClient**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient) to get the authorization context, then use Authz functions to retrieve the name.</span></span>
-   <span data-ttu-id="ffcf9-137">Il server di solito chiamerà [**CreatePrivateObjectSecurity**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createprivateobjectsecurity) per creare oggetti con ACL.</span><span class="sxs-lookup"><span data-stu-id="ffcf9-137">The server will normally call [**CreatePrivateObjectSecurity**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createprivateobjectsecurity) to create objects with ACLs.</span></span> <span data-ttu-id="ffcf9-138">Una volta completata questa operazione, i controlli di sicurezza successivi diventano automatici.</span><span class="sxs-lookup"><span data-stu-id="ffcf9-138">After this is accomplished, later security checks become automatic.</span></span>

 

 