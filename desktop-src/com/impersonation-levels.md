---
title: Livelli di rappresentazione (COM)
description: Se la rappresentazione ha esito positivo, significa che il client ha accettato di consentire al server di essere il client a un certo livello.
ms.assetid: 7539bbee-063f-4788-aece-7b70684826c8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85286e5fa880ea7620d6f6ccb6107bf139ec2005
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103872978"
---
# <a name="impersonation-levels"></a><span data-ttu-id="4f9ee-103">Livelli di rappresentazione</span><span class="sxs-lookup"><span data-stu-id="4f9ee-103">Impersonation Levels</span></span>

<span data-ttu-id="4f9ee-104">Se la rappresentazione ha esito positivo, significa che il client ha accettato di consentire al server di essere il client a un certo livello.</span><span class="sxs-lookup"><span data-stu-id="4f9ee-104">If impersonation succeeds, it means that the client has agreed to let the server be the client to some degree.</span></span> <span data-ttu-id="4f9ee-105">I vari gradi di rappresentazione sono denominati *livelli di rappresentazione* e indicano la quantità di autorità assegnata al server durante la rappresentazione del client.</span><span class="sxs-lookup"><span data-stu-id="4f9ee-105">The varying degrees of impersonation are called *impersonation levels*, and they indicate how much authority is given to the server when it is impersonating the client.</span></span>

<span data-ttu-id="4f9ee-106">Attualmente sono disponibili quattro livelli di rappresentazione: *anonima*, *Identificazione*, *rappresentazione* e *delegato*.</span><span class="sxs-lookup"><span data-stu-id="4f9ee-106">Currently, there are four impersonation levels: *anonymous*, *identify*, *impersonate*, and *delegate*.</span></span> <span data-ttu-id="4f9ee-107">Nell'elenco seguente viene brevemente descritto ogni livello di rappresentazione:</span><span class="sxs-lookup"><span data-stu-id="4f9ee-107">The following list briefly describes each impersonation level:</span></span>

<dl> <dt>

<span data-ttu-id="4f9ee-108"><span id="anonymous__RPC_C_IMP_LEVEL_ANONYMOUS_"></span><span id="anonymous__rpc_c_imp_level_anonymous_"></span><span id="ANONYMOUS__RPC_C_IMP_LEVEL_ANONYMOUS_"></span>Anonimo ( \_ \_ livello IMP C \_ RPC \_ anonimo)</span><span class="sxs-lookup"><span data-stu-id="4f9ee-108"><span id="anonymous__RPC_C_IMP_LEVEL_ANONYMOUS_"></span><span id="anonymous__rpc_c_imp_level_anonymous_"></span><span id="ANONYMOUS__RPC_C_IMP_LEVEL_ANONYMOUS_"></span>anonymous (RPC\_C\_IMP\_LEVEL\_ANONYMOUS)</span></span>
</dt> <dd>

<span data-ttu-id="4f9ee-109">Il client è anonimo per il server.</span><span class="sxs-lookup"><span data-stu-id="4f9ee-109">The client is anonymous to the server.</span></span> <span data-ttu-id="4f9ee-110">Il processo del server può rappresentare il client, ma il token di rappresentazione non contiene informazioni sul client.</span><span class="sxs-lookup"><span data-stu-id="4f9ee-110">The server process can impersonate the client, but the impersonation token does not contain any information about the client.</span></span> <span data-ttu-id="4f9ee-111">Questo livello è supportato solo per il trasporto di comunicazione interprocesso locale.</span><span class="sxs-lookup"><span data-stu-id="4f9ee-111">This level is only supported over the local interprocess communication transport.</span></span> <span data-ttu-id="4f9ee-112">Tutti gli altri trasporti promuovono automaticamente questo livello per identificare.</span><span class="sxs-lookup"><span data-stu-id="4f9ee-112">All other transports silently promote this level to identify.</span></span>

</dd> <dt>

<span data-ttu-id="4f9ee-113"><span id="identify__RPC_C_IMP_LEVEL_IDENTIFY_"></span><span id="identify__rpc_c_imp_level_identify_"></span><span id="IDENTIFY__RPC_C_IMP_LEVEL_IDENTIFY_"></span>identificazione ( \_ Identificazione del \_ livello IMP C di RPC \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="4f9ee-113"><span id="identify__RPC_C_IMP_LEVEL_IDENTIFY_"></span><span id="identify__rpc_c_imp_level_identify_"></span><span id="IDENTIFY__RPC_C_IMP_LEVEL_IDENTIFY_"></span>identify (RPC\_C\_IMP\_LEVEL\_IDENTIFY)</span></span>
</dt> <dd>

<span data-ttu-id="4f9ee-114">Livello predefinito del sistema.</span><span class="sxs-lookup"><span data-stu-id="4f9ee-114">The system default level.</span></span> <span data-ttu-id="4f9ee-115">Il server può ottenere l'identità del client e può rappresentarlo per le verifiche degli elenchi di controllo dell'accesso (ACL).</span><span class="sxs-lookup"><span data-stu-id="4f9ee-115">The server can obtain the client's identity, and the server can impersonate the client to do ACL checks.</span></span>

</dd> <dt>

<span data-ttu-id="4f9ee-116"><span id="impersonate__RPC_C_IMP_LEVEL_IMPERSONATE_"></span><span id="impersonate__rpc_c_imp_level_impersonate_"></span><span id="IMPERSONATE__RPC_C_IMP_LEVEL_IMPERSONATE_"></span>rappresenta (rappresentazione a livello di RPC \_ C \_ Imp \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="4f9ee-116"><span id="impersonate__RPC_C_IMP_LEVEL_IMPERSONATE_"></span><span id="impersonate__rpc_c_imp_level_impersonate_"></span><span id="IMPERSONATE__RPC_C_IMP_LEVEL_IMPERSONATE_"></span>impersonate (RPC\_C\_IMP\_LEVEL\_IMPERSONATE)</span></span>
</dt> <dd>

<span data-ttu-id="4f9ee-117">Il server può rappresentare il contesto di sicurezza del client quando rappresenta il client.</span><span class="sxs-lookup"><span data-stu-id="4f9ee-117">The server can impersonate the client's security context while acting on behalf of the client.</span></span> <span data-ttu-id="4f9ee-118">Il server può accedere alle risorse locali come client.</span><span class="sxs-lookup"><span data-stu-id="4f9ee-118">The server can access local resources as the client.</span></span> <span data-ttu-id="4f9ee-119">Se il server è locale, può accedere alle risorse di rete come client.</span><span class="sxs-lookup"><span data-stu-id="4f9ee-119">If the server is local, it can access network resources as the client.</span></span> <span data-ttu-id="4f9ee-120">Se il server è remoto, può accedere solo alle risorse che si trovano nello stesso computer del server.</span><span class="sxs-lookup"><span data-stu-id="4f9ee-120">If the server is remote, it can access only resources that are on the same computer as the server.</span></span>

</dd> <dt>

<span data-ttu-id="4f9ee-121"><span id="delegate__RPC_C_IMP_LEVEL_DELEGATE_"></span><span id="delegate__rpc_c_imp_level_delegate_"></span><span id="DELEGATE__RPC_C_IMP_LEVEL_DELEGATE_"></span>Delegate ( \_ \_ delegato livello IMP C RPC \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="4f9ee-121"><span id="delegate__RPC_C_IMP_LEVEL_DELEGATE_"></span><span id="delegate__rpc_c_imp_level_delegate_"></span><span id="DELEGATE__RPC_C_IMP_LEVEL_DELEGATE_"></span>delegate (RPC\_C\_IMP\_LEVEL\_DELEGATE)</span></span>
</dt> <dd>

<span data-ttu-id="4f9ee-122">Livello massimo di rappresentazione.</span><span class="sxs-lookup"><span data-stu-id="4f9ee-122">The most powerful impersonation level.</span></span> <span data-ttu-id="4f9ee-123">Quando si seleziona questo livello, il server, sia locale che remoto, può rappresentare il contesto di sicurezza del client quando agisce per conto del client.</span><span class="sxs-lookup"><span data-stu-id="4f9ee-123">When this level is selected, the server (whether local or remote) can impersonate the client's security context while acting on behalf of the client.</span></span> <span data-ttu-id="4f9ee-124">Durante la rappresentazione, le credenziali del client, sia locali che di rete, possono essere passate a un numero qualsiasi di computer.</span><span class="sxs-lookup"><span data-stu-id="4f9ee-124">During impersonation, the client's credentials (both local and network) can be passed to any number of computers.</span></span>

<span data-ttu-id="4f9ee-125">Affinché la rappresentazione funzioni a livello di delegato, è necessario soddisfare i requisiti seguenti:</span><span class="sxs-lookup"><span data-stu-id="4f9ee-125">For impersonation to work at the delegate level, the following requirements must be met:</span></span>

-   <span data-ttu-id="4f9ee-126">Il client deve impostare il livello di rappresentazione sul delegato RPC \_ C \_ Imp \_ level \_ .</span><span class="sxs-lookup"><span data-stu-id="4f9ee-126">The client must set the impersonation level to RPC\_C\_IMP\_LEVEL\_DELEGATE.</span></span>
-   <span data-ttu-id="4f9ee-127">L'account client non deve essere contrassegnato come "l'account è sensibile e non può essere delegato" nel servizio Active Directory.</span><span class="sxs-lookup"><span data-stu-id="4f9ee-127">The client account must not be marked "Account is sensitive and cannot be delegated" in the Active Directory Service.</span></span>
-   <span data-ttu-id="4f9ee-128">L'account del server deve essere contrassegnato con l'attributo "trusted per la delega" nel servizio Active Directory.</span><span class="sxs-lookup"><span data-stu-id="4f9ee-128">The server account must be marked with the "Trusted for delegation" attribute in the Active Directory Service.</span></span>
-   <span data-ttu-id="4f9ee-129">I computer che ospitano il client, il server e tutti i server "downstream" devono essere tutti in esecuzione in un dominio.</span><span class="sxs-lookup"><span data-stu-id="4f9ee-129">The computers hosting the client, the server, and any "downstream" servers must all be running in a domain.</span></span>

</dd> </dl>

<span data-ttu-id="4f9ee-130">Scegliendo il livello di rappresentazione, il client comunica al server fino a che punto può passare a rappresentare il client.</span><span class="sxs-lookup"><span data-stu-id="4f9ee-130">By choosing the impersonation level, the client tells the server how far it can go in impersonating the client.</span></span> <span data-ttu-id="4f9ee-131">Il client imposta il livello di rappresentazione sul proxy utilizzato per comunicare con il server.</span><span class="sxs-lookup"><span data-stu-id="4f9ee-131">The client sets the impersonation level on the proxy it uses to communicate with the server.</span></span>

## <a name="setting-the-impersonation-level"></a><span data-ttu-id="4f9ee-132">Impostazione del livello di rappresentazione</span><span class="sxs-lookup"><span data-stu-id="4f9ee-132">Setting the Impersonation Level</span></span>

<span data-ttu-id="4f9ee-133">Esistono due modi per impostare il livello di rappresentazione:</span><span class="sxs-lookup"><span data-stu-id="4f9ee-133">There are two ways to set the impersonation level:</span></span>

-   <span data-ttu-id="4f9ee-134">Il client può impostarlo processwide tramite una chiamata a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="4f9ee-134">The client can set it processwide, through a call to [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span>
-   <span data-ttu-id="4f9ee-135">Un client può impostare la sicurezza a livello di proxy su un'interfaccia di un oggetto remoto tramite una chiamata a [**IClientSecurity:: Seblankt**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) (o alla funzione helper [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)).</span><span class="sxs-lookup"><span data-stu-id="4f9ee-135">A client can set proxy-level security on an interface of a remote object through a call to [**IClientSecurity::SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) (or the helper function [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)).</span></span>

<span data-ttu-id="4f9ee-136">Per impostare il livello di rappresentazione, passare un \_ \_ valore xxx del livello di RPC C appropriato \_ \_ a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) o [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) tramite il parametro *dwImpLevel* .</span><span class="sxs-lookup"><span data-stu-id="4f9ee-136">You set the impersonation level by passing an appropriate RPC\_C\_IMP\_LEVEL\_xxx value to [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) or [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) through the *dwImpLevel* parameter.</span></span>

<span data-ttu-id="4f9ee-137">Diversi servizi di autenticazione supportano la rappresentazione a livello di delegato in extent diversi.</span><span class="sxs-lookup"><span data-stu-id="4f9ee-137">Different authentication services support delegate-level impersonation to different extents.</span></span> <span data-ttu-id="4f9ee-138">Ad esempio, NTLMSSP supporta la rappresentazione a livello di delegato cross-thread e tra processi, ma non tra computer.</span><span class="sxs-lookup"><span data-stu-id="4f9ee-138">For instance, NTLMSSP supports cross-thread and cross-process delegate-level impersonation, but not cross-computer.</span></span> <span data-ttu-id="4f9ee-139">D'altra parte, il protocollo Kerberos supporta la rappresentazione a livello di delegato attraverso i limiti del computer, mentre Schannel non supporta alcuna rappresentazione a livello di delegato.</span><span class="sxs-lookup"><span data-stu-id="4f9ee-139">On the other hand, the Kerberos protocol supports delegate-level impersonation across computer boundaries, while Schannel does not support any impersonation at the delegate level.</span></span> <span data-ttu-id="4f9ee-140">Se si dispone di un proxy al livello di rappresentazione e si desidera impostare il livello di rappresentazione su delegare, è necessario chiamare il metodo [**Seblankt**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) utilizzando le costanti predefinite per ogni parametro eccetto il livello di rappresentazione.</span><span class="sxs-lookup"><span data-stu-id="4f9ee-140">If you have a proxy at impersonate level and you want to set the impersonation level to delegate, you should call [**SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) using the default constants for every parameter except the impersonation level.</span></span> <span data-ttu-id="4f9ee-141">COM sceglierà NTLM localmente e il protocollo Kerberos in modalità remota (quando il protocollo Kerberos funzionerà).</span><span class="sxs-lookup"><span data-stu-id="4f9ee-141">COM will choose NTLM locally and the Kerberos protocol remotely (when the Kerberos protocol will work).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4f9ee-142">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4f9ee-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4f9ee-143">Delega e rappresentazione</span><span class="sxs-lookup"><span data-stu-id="4f9ee-143">Delegation and Impersonation</span></span>](delegation-and-impersonation.md)
</dt> </dl>

 

 