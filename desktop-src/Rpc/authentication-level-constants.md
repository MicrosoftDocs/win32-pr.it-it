---
title: Costanti Authentication-Level (rpcdce. h)
description: Le costanti a livello di autenticazione rappresentano i livelli di autenticazione passati a varie funzioni di run-time.
ms.assetid: b8bb2517-e1a0-4607-a672-259f8686fc3e
topic_type:
- apiref
api_name:
- RPC_C_AUTHN_LEVEL_DEFAULT
- RPC_C_AUTHN_LEVEL_NONE
- RPC_C_AUTHN_LEVEL_CONNECT
- RPC_C_AUTHN_LEVEL_CALL
- RPC_C_AUTHN_LEVEL_PKT
- RPC_C_AUTHN_LEVEL_PKT_INTEGRITY
- RPC_C_AUTHN_LEVEL_PKT_PRIVACY
api_location:
- Rpcdce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 114e5624b2cbc8af0b86a29daff2c1761f6fee39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518729"
---
# <a name="authentication-level-constants"></a><span data-ttu-id="40d5b-103">Costanti a livello di autenticazione</span><span class="sxs-lookup"><span data-stu-id="40d5b-103">Authentication-Level Constants</span></span>

<span data-ttu-id="40d5b-104">Le costanti a livello di autenticazione rappresentano i livelli di autenticazione passati a varie funzioni di run-time.</span><span class="sxs-lookup"><span data-stu-id="40d5b-104">The authentication-level constants represent authentication levels passed to various run-time functions.</span></span> <span data-ttu-id="40d5b-105">Questi livelli sono elencati per aumentare l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="40d5b-105">These levels are listed in order of increasing authentication.</span></span> <span data-ttu-id="40d5b-106">Ogni nuovo livello aggiunge l'autenticazione fornita dal livello precedente.</span><span class="sxs-lookup"><span data-stu-id="40d5b-106">Each new level adds to the authentication provided by the previous level.</span></span> <span data-ttu-id="40d5b-107">Se la libreria di runtime RPC non supporta il livello specificato, viene automaticamente aggiornata al livello superiore supportato successivo.</span><span class="sxs-lookup"><span data-stu-id="40d5b-107">If the RPC run-time library does not support the specified level, it automatically upgrades to the next higher supported level.</span></span>



| <span data-ttu-id="40d5b-108">Costante</span><span class="sxs-lookup"><span data-stu-id="40d5b-108">Constant</span></span>                                                                                                                                                                                                                | <span data-ttu-id="40d5b-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="40d5b-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_AUTHN_LEVEL_DEFAULT"></span><span id="rpc_c_authn_level_default"></span><dl> <span data-ttu-id="40d5b-110"><dt>**\_ \_ \_ valore predefinito del livello auth C RPC \_**</dt></span><span class="sxs-lookup"><span data-stu-id="40d5b-110"><dt>**RPC\_C\_AUTHN\_LEVEL\_DEFAULT**</dt></span></span> </dl>                    | <span data-ttu-id="40d5b-111">Utilizza il livello di autenticazione predefinito per il servizio di autenticazione specificato.</span><span class="sxs-lookup"><span data-stu-id="40d5b-111">Uses the default authentication level for the specified authentication service.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                    |
| <span id="RPC_C_AUTHN_LEVEL_NONE"></span><span id="rpc_c_authn_level_none"></span><dl> <span data-ttu-id="40d5b-112"><dt>**\_ \_ livello auth C \_ RPC \_**</dt></span><span class="sxs-lookup"><span data-stu-id="40d5b-112"><dt>**RPC\_C\_AUTHN\_LEVEL\_NONE**</dt></span></span> </dl>                             | <span data-ttu-id="40d5b-113">Non esegue alcuna autenticazione.</span><span class="sxs-lookup"><span data-stu-id="40d5b-113">Performs no authentication.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="RPC_C_AUTHN_LEVEL_CONNECT"></span><span id="rpc_c_authn_level_connect"></span><dl> <span data-ttu-id="40d5b-114"><dt>**\_connessione a \_ livello auth \_ C \_ RPC**</dt></span><span class="sxs-lookup"><span data-stu-id="40d5b-114"><dt>**RPC\_C\_AUTHN\_LEVEL\_CONNECT**</dt></span></span> </dl>                    | <span data-ttu-id="40d5b-115">L'autenticazione viene eseguita solo quando il client stabilisce una relazione con un server.</span><span class="sxs-lookup"><span data-stu-id="40d5b-115">Authenticates only when the client establishes a relationship with a server.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                       |
| <span id="RPC_C_AUTHN_LEVEL_CALL"></span><span id="rpc_c_authn_level_call"></span><dl> <span data-ttu-id="40d5b-116"><dt>**\_chiamata al \_ livello auth \_ C \_ RPC**</dt></span><span class="sxs-lookup"><span data-stu-id="40d5b-116"><dt>**RPC\_C\_AUTHN\_LEVEL\_CALL**</dt></span></span> </dl>                             | <span data-ttu-id="40d5b-117">Esegue l'autenticazione solo all'inizio di ogni chiamata di procedura remota quando il server riceve la richiesta.</span><span class="sxs-lookup"><span data-stu-id="40d5b-117">Authenticates only at the beginning of each remote procedure call when the server receives the request.</span></span> <span data-ttu-id="40d5b-118">Non si applica alle chiamate a procedure remote effettuate utilizzando le sequenze di protocollo basate sulla connessione (quelle che iniziano con il prefisso "ncacn").</span><span class="sxs-lookup"><span data-stu-id="40d5b-118">Does not apply to remote procedure calls made using the connection-based protocol sequences (those that start with the prefix "ncacn").</span></span> <span data-ttu-id="40d5b-119">Se la sequenza di protocollo in un handle di associazione è una sequenza di protocollo basata sulla connessione e si specifica questo livello, questa routine utilizzerà invece la \_ \_ costante PKT del livello auth C RPC \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="40d5b-119">If the protocol sequence in a binding handle is a connection-based protocol sequence and you specify this level, this routine instead uses the RPC\_C\_AUTHN\_LEVEL\_PKT constant.</span></span><br/> |
| <span id="RPC_C_AUTHN_LEVEL_PKT"></span><span id="rpc_c_authn_level_pkt"></span><dl> <span data-ttu-id="40d5b-120"><dt>**\_ \_ \_ PKT livello auth C RPC \_**</dt></span><span class="sxs-lookup"><span data-stu-id="40d5b-120"><dt>**RPC\_C\_AUTHN\_LEVEL\_PKT**</dt></span></span> </dl>                                | <span data-ttu-id="40d5b-121">Autentica solo che tutti i dati ricevuti sono dal client previsto.</span><span class="sxs-lookup"><span data-stu-id="40d5b-121">Authenticates only that all data received is from the expected client.</span></span> <span data-ttu-id="40d5b-122">Non convalida i dati stessi.</span><span class="sxs-lookup"><span data-stu-id="40d5b-122">Does not validate the data itself.</span></span><br/>                                                                                                                                                                                                                                                                                                                          |
| <span id="RPC_C_AUTHN_LEVEL_PKT_INTEGRITY"></span><span id="rpc_c_authn_level_pkt_integrity"></span><dl> <span data-ttu-id="40d5b-123"><dt>**\_ \_ \_ integrità PKT del livello auth \_ C \_ RPC**</dt></span><span class="sxs-lookup"><span data-stu-id="40d5b-123"><dt>**RPC\_C\_AUTHN\_LEVEL\_PKT\_INTEGRITY**</dt></span></span> </dl> | <span data-ttu-id="40d5b-124">Autentica e verifica che nessuno dei dati trasferiti tra il client e il server sia stato modificato.</span><span class="sxs-lookup"><span data-stu-id="40d5b-124">Authenticates and verifies that none of the data transferred between client and server has been modified.</span></span><br/>                                                                                                                                                                                                                                                                                                                          |
| <span id="RPC_C_AUTHN_LEVEL_PKT_PRIVACY"></span><span id="rpc_c_authn_level_pkt_privacy"></span><dl> <span data-ttu-id="40d5b-125"><dt>**\_ \_ \_ privacy PKT a livello di autenticazione C \_ RPC \_**</dt></span><span class="sxs-lookup"><span data-stu-id="40d5b-125"><dt>**RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**</dt></span></span> </dl>       | <span data-ttu-id="40d5b-126">Include tutti i livelli precedenti e garantisce che i dati di testo non crittografati possano essere visualizzati solo dal mittente e dal destinatario.</span><span class="sxs-lookup"><span data-stu-id="40d5b-126">Includes all previous levels, and ensures clear text data can only be seen by the sender and the receiver.</span></span> <span data-ttu-id="40d5b-127">Nel caso locale, ciò comporta l'uso di un canale sicuro.</span><span class="sxs-lookup"><span data-stu-id="40d5b-127">In the local case, this involves using a secure channel.</span></span> <span data-ttu-id="40d5b-128">Nel caso remoto, questo implica la crittografia del valore dell'argomento di ogni chiamata di procedura remota.</span><span class="sxs-lookup"><span data-stu-id="40d5b-128">In the remote case, this involves encrypting the argument value of each remote procedure call.</span></span><br/>                                                                                                                                                                 |



## <a name="remarks"></a><span data-ttu-id="40d5b-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="40d5b-129">Remarks</span></span>

<span data-ttu-id="40d5b-130">Indipendentemente dal valore specificato dalla costante, **ncalrpc** usa sempre la \_ \_ \_ privacy PKT del livello auth C di RPC \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="40d5b-130">Regardless of the value specified by the constant, **ncalrpc** always uses RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY.</span></span>

## <a name="requirements"></a><span data-ttu-id="40d5b-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="40d5b-131">Requirements</span></span>



| <span data-ttu-id="40d5b-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="40d5b-132">Requirement</span></span> | <span data-ttu-id="40d5b-133">Valore</span><span class="sxs-lookup"><span data-stu-id="40d5b-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="40d5b-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="40d5b-134">Minimum supported client</span></span><br/> | <span data-ttu-id="40d5b-135">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="40d5b-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="40d5b-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="40d5b-136">Minimum supported server</span></span><br/> | <span data-ttu-id="40d5b-137">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="40d5b-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="40d5b-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="40d5b-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="40d5b-139"><dt>Rpcdce. h</dt></span><span class="sxs-lookup"><span data-stu-id="40d5b-139"><dt>Rpcdce.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40d5b-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="40d5b-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40d5b-141">**RpcBindingInqAuthInfo**</span><span class="sxs-lookup"><span data-stu-id="40d5b-141">**RpcBindingInqAuthInfo**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthinfo)
</dt> <dt>

[<span data-ttu-id="40d5b-142">**RpcBindingSetAuthInfo**</span><span class="sxs-lookup"><span data-stu-id="40d5b-142">**RpcBindingSetAuthInfo**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo)
</dt> <dt>

[<span data-ttu-id="40d5b-143">**RpcMgmtInqDefaultProtectLevel**</span><span class="sxs-lookup"><span data-stu-id="40d5b-143">**RpcMgmtInqDefaultProtectLevel**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqdefaultprotectlevel)
</dt> <dt>

[<span data-ttu-id="40d5b-144">**RpcBindingInqAuthClient**</span><span class="sxs-lookup"><span data-stu-id="40d5b-144">**RpcBindingInqAuthClient**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient)
</dt> <dt>

[<span data-ttu-id="40d5b-145">**RpcBindingInqAuthClientEx**</span><span class="sxs-lookup"><span data-stu-id="40d5b-145">**RpcBindingInqAuthClientEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclientex)
</dt> <dt>

[<span data-ttu-id="40d5b-146">**RpcBindingSetAuthInfoEx**</span><span class="sxs-lookup"><span data-stu-id="40d5b-146">**RpcBindingSetAuthInfoEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa)
</dt> <dt>

[<span data-ttu-id="40d5b-147">**RpcBindingInqAuthInfoEx**</span><span class="sxs-lookup"><span data-stu-id="40d5b-147">**RpcBindingInqAuthInfoEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthinfoexa)
</dt> </dl>

 

 





