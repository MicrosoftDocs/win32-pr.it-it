---
title: Flag di registrazione dell'interfaccia (rpcdce. h)
description: Le costanti seguenti vengono usate nel parametro flags delle funzioni RpcServerRegisterIf2 e RpcServerRegisterIfEx.
ms.assetid: 387311c0-13df-4497-a0ac-ce6aec0e726c
topic_type:
- apiref
api_name:
- RPC_IF_ALLOW_CALLBACKS_WITH_NO_AUTH
- RPC_IF_ALLOW_LOCAL_ONLY
- RPC_IF_AUTOLISTEN
- RPC_IF_OLE
- RPC_IF_ALLOW_UNKNOWN_AUTHORITY
- RPC_IF_ALLOW_SECURE_ONLY
- RPC_IF_SEC_NO_CACHE
api_location:
- Rpcdce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8af938038d2bc7000d80268fb4cb00941f6b282b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121118"
---
# <a name="interface-registration-flags"></a><span data-ttu-id="888d9-103">Flag di registrazione dell'interfaccia</span><span class="sxs-lookup"><span data-stu-id="888d9-103">Interface Registration Flags</span></span>

<span data-ttu-id="888d9-104">Le costanti seguenti vengono usate nel parametro *Flags* delle funzioni [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) e [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) .</span><span class="sxs-lookup"><span data-stu-id="888d9-104">The following constants are used in the *Flags* parameter of the [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) and [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) functions.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="888d9-105">Costante</span><span class="sxs-lookup"><span data-stu-id="888d9-105">Constant</span></span></th>
<th style="text-align: left;"><span data-ttu-id="888d9-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="888d9-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="0"></span><dl> <span data-ttu-id="888d9-107"><dt><strong>0</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="888d9-107"><dt><strong>0</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="888d9-108">Semantica dell'interfaccia standard.</span><span class="sxs-lookup"><span data-stu-id="888d9-108">Standard interface semantics.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="RPC_IF_ALLOW_CALLBACKS_WITH_NO_AUTH"></span><span id="rpc_if_allow_callbacks_with_no_auth"></span><dl> <span data-ttu-id="888d9-109"><dt><strong>RPC_IF_ALLOW_CALLBACKS_WITH_NO_AUTH</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="888d9-109"><dt><strong>RPC_IF_ALLOW_CALLBACKS_WITH_NO_AUTH</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="888d9-110">Quando questo flag di interfaccia viene registrato, il runtime RPC richiama il callback di sicurezza registrato per tutte le chiamate, indipendentemente dall'identità, dalla sequenza di protocollo o dal livello di autenticazione del client.</span><span class="sxs-lookup"><span data-stu-id="888d9-110">When this interface flag is registered, the RPC runtime invokes the registered security callback for all calls, regardless of identity, protocol sequence, or authentication level of the client.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="888d9-111">Questo flag è disponibile a partire da Windows XP con SP2 e Windows Server 2003 con SP1.</span><span class="sxs-lookup"><span data-stu-id="888d9-111">This flag is available starting with Windows XP with SP2 and Windows Server 2003 with SP1.</span></span> <span data-ttu-id="888d9-112">Quando questo flag non è impostato, RPC filtra automaticamente tutte le chiamate non autenticate prima che raggiungano il callback di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="888d9-112">When this flag is not set, RPC automatically filters all unauthenticated calls before they reach the security callback.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="RPC_IF_ALLOW_LOCAL_ONLY"></span><span id="rpc_if_allow_local_only"></span><dl> <span data-ttu-id="888d9-113"><dt><strong>RPC_IF_ALLOW_LOCAL_ONLY</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="888d9-113"><dt><strong>RPC_IF_ALLOW_LOCAL_ONLY</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="888d9-114">Quando questo flag di interfaccia viene registrato, il runtime RPC rifiuta le chiamate effettuate dai client remoti.</span><span class="sxs-lookup"><span data-stu-id="888d9-114">When this interface flag is registered, the RPC runtime rejects calls made by remote clients.</span></span> <span data-ttu-id="888d9-115">Vengono rifiutate anche tutte le chiamate locali che usano le sequenze di protocollo ncadg_ \* e ncacn_ \*, ad eccezione di ncacn_np.</span><span class="sxs-lookup"><span data-stu-id="888d9-115">All local calls using ncadg_\* and ncacn_\* protocol sequences are also rejected, with the exception of ncacn_np.</span></span> <span data-ttu-id="888d9-116">RPC consente ncacn_NP chiamate solo se la chiamata non proviene da SRV.</span><span class="sxs-lookup"><span data-stu-id="888d9-116">RPC allows ncacn_NP calls only if the call does not come from SRV.</span></span> <span data-ttu-id="888d9-117">Le chiamate da Ncalrpc vengono sempre elaborate.</span><span class="sxs-lookup"><span data-stu-id="888d9-117">Calls from ncalrpc are always processed.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="888d9-118">Questo flag è disponibile a partire da Windows XP con SP2 e Windows Server 2003 con SP1.</span><span class="sxs-lookup"><span data-stu-id="888d9-118">This flag is available starting with Windows XP with SP2 and Windows Server 2003 with SP1.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="RPC_IF_AUTOLISTEN"></span><span id="rpc_if_autolisten"></span><dl> <span data-ttu-id="888d9-119"><dt><strong>RPC_IF_AUTOLISTEN</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="888d9-119"><dt><strong>RPC_IF_AUTOLISTEN</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="888d9-120">Si tratta di un'interfaccia di <strong>ascolto automatico</strong> .</span><span class="sxs-lookup"><span data-stu-id="888d9-120">This is an <strong>auto-listen</strong> interface.</span></span> <span data-ttu-id="888d9-121">Il tempo di esecuzione inizia ad ascoltare le chiamate non appena viene registrata la prima interfaccia autolisten e interrompe l'ascolto quando viene annullata la registrazione dell'ultima interfaccia Autolist.</span><span class="sxs-lookup"><span data-stu-id="888d9-121">The run time begins listening for calls as soon as the first autolisten interface is registered, and stops listening when the last autolisten interface is unregistered.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="RPC_IF_OLE"></span><span id="rpc_if_ole"></span><dl> <span data-ttu-id="888d9-122"><dt><strong>RPC_IF_OLE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="888d9-122"><dt><strong>RPC_IF_OLE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="888d9-123">Riservato per OLE.</span><span class="sxs-lookup"><span data-stu-id="888d9-123">Reserved for OLE.</span></span> <span data-ttu-id="888d9-124">Non usare questo flag.</span><span class="sxs-lookup"><span data-stu-id="888d9-124">Do not use this flag.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="RPC_IF_ALLOW_UNKNOWN_AUTHORITY"></span><span id="rpc_if_allow_unknown_authority"></span><dl> <span data-ttu-id="888d9-125"><dt><strong>RPC_IF_ALLOW_UNKNOWN_AUTHORITY</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="888d9-125"><dt><strong>RPC_IF_ALLOW_UNKNOWN_AUTHORITY</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="888d9-126">Attualmente non implementato.</span><span class="sxs-lookup"><span data-stu-id="888d9-126">Currently not implemented.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="RPC_IF_ALLOW_SECURE_ONLY"></span><span id="rpc_if_allow_secure_only"></span><dl> <span data-ttu-id="888d9-127"><dt><strong>RPC_IF_ALLOW_SECURE_ONLY</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="888d9-127"><dt><strong>RPC_IF_ALLOW_SECURE_ONLY</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="888d9-128">Limita le connessioni ai client che utilizzano un livello di autorizzazione superiore a RPC_C_AUTHN_LEVEL_NONE.</span><span class="sxs-lookup"><span data-stu-id="888d9-128">Limits connections to clients that use an authorization level higher than RPC_C_AUTHN_LEVEL_NONE.</span></span> <span data-ttu-id="888d9-129">La specifica di questo flag consente ai client di passare alla sessione <strong>null</strong> .</span><span class="sxs-lookup"><span data-stu-id="888d9-129">Specifying this flag allows clients to come through on the <strong>NULL</strong> session.</span></span> <span data-ttu-id="888d9-130">In Windows XP e Windows Server 2003 tali client non sono consentiti.</span><span class="sxs-lookup"><span data-stu-id="888d9-130">On Windows XP and Windows Server 2003, such clients are not allowed.</span></span> <span data-ttu-id="888d9-131">I client che non riescono a RPC_IF_ALLOW_SECURE_ONLY test ricevono un errore RPC_S_ACCESS_DENIED.</span><span class="sxs-lookup"><span data-stu-id="888d9-131">Clients that fail the RPC_IF_ALLOW_SECURE_ONLY test receive an RPC_S_ACCESS_DENIED error.</span></span> <span data-ttu-id="888d9-132">L'utilizzo del flag RPC_IF_ALLOW_SECURE_ONLY non implica né garantisce un livello di privilegio elevato per la parte dell'utente chiamante.</span><span class="sxs-lookup"><span data-stu-id="888d9-132">Using the RPC_IF_ALLOW_SECURE_ONLY flag does not imply or guarantee a high level of privilege on the part of the calling user.</span></span> <span data-ttu-id="888d9-133">RPC verifica solo che l'utente disponga di credenziali valide. l'utente chiamante può usare l'account Guest o altri account con privilegi limitati.</span><span class="sxs-lookup"><span data-stu-id="888d9-133">RPC only checks that the user has valid credentials; the calling user may be using the guest account or other low privileged accounts.</span></span> <span data-ttu-id="888d9-134">Non presupporre privilegi elevati quando viene usato RPC_IF_ALLOW_SECURE_ONLY.</span><span class="sxs-lookup"><span data-stu-id="888d9-134">Do not assume high privilege when RPC_IF_ALLOW_SECURE_ONLY is used.</span></span><br/> <span data-ttu-id="888d9-135"><strong>Windows NT 4,0 e Windows Me/98/95:  </strong></span><span class="sxs-lookup"><span data-stu-id="888d9-135"><strong>Windows NT 4.0 and Windows Me/98/95:  </strong></span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="RPC_IF_SEC_NO_CACHE"></span><span id="rpc_if_sec_no_cache"></span><dl> <span data-ttu-id="888d9-136"><dt><strong>RPC_IF_SEC_NO_CACHE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="888d9-136"><dt><strong>RPC_IF_SEC_NO_CACHE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="888d9-137">Disabilita la memorizzazione nella cache di callback di sicurezza, forzando un callback di sicurezza per ogni chiamata RPC su una determinata interfaccia.</span><span class="sxs-lookup"><span data-stu-id="888d9-137">Disables security callback caching, forcing a security callback for each RPC call on a given interface.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="888d9-138">Questo flag è disponibile a partire da Windows XP con SP2 e Windows Server 2003 con SP1.</span><span class="sxs-lookup"><span data-stu-id="888d9-138">This flag is available starting with Windows XP with SP2 and Windows Server 2003 with SP1.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="888d9-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="888d9-139">Requirements</span></span>



| <span data-ttu-id="888d9-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="888d9-140">Requirement</span></span> | <span data-ttu-id="888d9-141">Valore</span><span class="sxs-lookup"><span data-stu-id="888d9-141">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="888d9-142">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="888d9-142">Minimum supported client</span></span><br/> | <span data-ttu-id="888d9-143">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="888d9-143">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="888d9-144">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="888d9-144">Minimum supported server</span></span><br/> | <span data-ttu-id="888d9-145">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="888d9-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="888d9-146">Intestazione</span><span class="sxs-lookup"><span data-stu-id="888d9-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="888d9-147"><dt>Rpcdce. h</dt></span><span class="sxs-lookup"><span data-stu-id="888d9-147"><dt>Rpcdce.h</dt></span></span> </dl> |



 

 





