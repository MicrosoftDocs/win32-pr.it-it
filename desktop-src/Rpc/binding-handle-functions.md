---
title: Funzioni di handle di associazione
description: La tabella seguente contiene l'elenco delle routine di runtime RPC che operano sugli handle di associazione e specifica il tipo di handle di associazione consentito.
ms.assetid: 16effe59-ebe2-48c3-b97a-90656b6d3b51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89e00b3cbb2d5fc5637b9414d6f009cfb2e4ade4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297799"
---
# <a name="binding-handle-functions"></a><span data-ttu-id="d9a04-103">Funzioni di handle di associazione</span><span class="sxs-lookup"><span data-stu-id="d9a04-103">Binding Handle Functions</span></span>

<span data-ttu-id="d9a04-104">La tabella seguente contiene l'elenco delle routine di runtime RPC che operano sugli handle di associazione e specifica il tipo di handle di associazione consentito.</span><span class="sxs-lookup"><span data-stu-id="d9a04-104">The following table contains the list of RPC run-time routines that operate on binding handles and specifies the type of binding handle allowed.</span></span>



| <span data-ttu-id="d9a04-105">Routine</span><span class="sxs-lookup"><span data-stu-id="d9a04-105">Routine</span></span>                                                            | <span data-ttu-id="d9a04-106">Argomento di input</span><span class="sxs-lookup"><span data-stu-id="d9a04-106">Input argument</span></span>   | <span data-ttu-id="d9a04-107">Argomento di output</span><span class="sxs-lookup"><span data-stu-id="d9a04-107">Output argument</span></span> |
|--------------------------------------------------------------------|------------------|-----------------|
| [<span data-ttu-id="d9a04-108">**RpcBindingCopy**</span><span class="sxs-lookup"><span data-stu-id="d9a04-108">**RpcBindingCopy**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingcopy)                           | <span data-ttu-id="d9a04-109">Server</span><span class="sxs-lookup"><span data-stu-id="d9a04-109">Server</span></span>           | <span data-ttu-id="d9a04-110">Server</span><span class="sxs-lookup"><span data-stu-id="d9a04-110">Server</span></span>          |
| [<span data-ttu-id="d9a04-111">**RpcBindingFree**</span><span class="sxs-lookup"><span data-stu-id="d9a04-111">**RpcBindingFree**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfree)                           | <span data-ttu-id="d9a04-112">Server</span><span class="sxs-lookup"><span data-stu-id="d9a04-112">Server</span></span>           | <span data-ttu-id="d9a04-113">nessuno</span><span class="sxs-lookup"><span data-stu-id="d9a04-113">None</span></span>            |
| [<span data-ttu-id="d9a04-114">**Errore in RpcBindingFromStringBinding**</span><span class="sxs-lookup"><span data-stu-id="d9a04-114">**RpcBindingFromStringBinding**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) | <span data-ttu-id="d9a04-115">nessuno</span><span class="sxs-lookup"><span data-stu-id="d9a04-115">None</span></span>             | <span data-ttu-id="d9a04-116">Server</span><span class="sxs-lookup"><span data-stu-id="d9a04-116">Server</span></span>          |
| [<span data-ttu-id="d9a04-117">**RpcBindingInqAuthClient**</span><span class="sxs-lookup"><span data-stu-id="d9a04-117">**RpcBindingInqAuthClient**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient)         | <span data-ttu-id="d9a04-118">Client</span><span class="sxs-lookup"><span data-stu-id="d9a04-118">Client</span></span>           | <span data-ttu-id="d9a04-119">nessuno</span><span class="sxs-lookup"><span data-stu-id="d9a04-119">None</span></span>            |
| [<span data-ttu-id="d9a04-120">**RpcBindingInqAuthInfo**</span><span class="sxs-lookup"><span data-stu-id="d9a04-120">**RpcBindingInqAuthInfo**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthinfo)             | <span data-ttu-id="d9a04-121">Server</span><span class="sxs-lookup"><span data-stu-id="d9a04-121">Server</span></span>           | <span data-ttu-id="d9a04-122">nessuno</span><span class="sxs-lookup"><span data-stu-id="d9a04-122">None</span></span>            |
| [<span data-ttu-id="d9a04-123">**RpcBindingInqObject**</span><span class="sxs-lookup"><span data-stu-id="d9a04-123">**RpcBindingInqObject**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqobject)                 | <span data-ttu-id="d9a04-124">Server o client</span><span class="sxs-lookup"><span data-stu-id="d9a04-124">Server or client</span></span> | <span data-ttu-id="d9a04-125">nessuno</span><span class="sxs-lookup"><span data-stu-id="d9a04-125">None</span></span>            |
| [<span data-ttu-id="d9a04-126">**RpcBindingReset**</span><span class="sxs-lookup"><span data-stu-id="d9a04-126">**RpcBindingReset**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset)                         | <span data-ttu-id="d9a04-127">Server</span><span class="sxs-lookup"><span data-stu-id="d9a04-127">Server</span></span>           | <span data-ttu-id="d9a04-128">nessuno</span><span class="sxs-lookup"><span data-stu-id="d9a04-128">None</span></span>            |
| [<span data-ttu-id="d9a04-129">**RpcBindingSetAuthInfo**</span><span class="sxs-lookup"><span data-stu-id="d9a04-129">**RpcBindingSetAuthInfo**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo)             | <span data-ttu-id="d9a04-130">Server</span><span class="sxs-lookup"><span data-stu-id="d9a04-130">Server</span></span>           | <span data-ttu-id="d9a04-131">nessuno</span><span class="sxs-lookup"><span data-stu-id="d9a04-131">None</span></span>            |
| [<span data-ttu-id="d9a04-132">**RpcBindingSetObject**</span><span class="sxs-lookup"><span data-stu-id="d9a04-132">**RpcBindingSetObject**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetobject)                 | <span data-ttu-id="d9a04-133">Server</span><span class="sxs-lookup"><span data-stu-id="d9a04-133">Server</span></span>           | <span data-ttu-id="d9a04-134">nessuno</span><span class="sxs-lookup"><span data-stu-id="d9a04-134">None</span></span>            |
| [<span data-ttu-id="d9a04-135">**RpcBindingToStringBinding**</span><span class="sxs-lookup"><span data-stu-id="d9a04-135">**RpcBindingToStringBinding**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding)     | <span data-ttu-id="d9a04-136">Server o client</span><span class="sxs-lookup"><span data-stu-id="d9a04-136">Server or client</span></span> | <span data-ttu-id="d9a04-137">nessuno</span><span class="sxs-lookup"><span data-stu-id="d9a04-137">None</span></span>            |
| [<span data-ttu-id="d9a04-138">**RpcBindingVectorFree**</span><span class="sxs-lookup"><span data-stu-id="d9a04-138">**RpcBindingVectorFree**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingvectorfree)               | <span data-ttu-id="d9a04-139">Server</span><span class="sxs-lookup"><span data-stu-id="d9a04-139">Server</span></span>           | <span data-ttu-id="d9a04-140">nessuno</span><span class="sxs-lookup"><span data-stu-id="d9a04-140">None</span></span>            |
| [<span data-ttu-id="d9a04-141">**RpcNsBindingExport**</span><span class="sxs-lookup"><span data-stu-id="d9a04-141">**RpcNsBindingExport**</span></span>](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta)                   | <span data-ttu-id="d9a04-142">Server</span><span class="sxs-lookup"><span data-stu-id="d9a04-142">Server</span></span>           | <span data-ttu-id="d9a04-143">nessuno</span><span class="sxs-lookup"><span data-stu-id="d9a04-143">None</span></span>            |
| [<span data-ttu-id="d9a04-144">**RpcNsBindingImportNext**</span><span class="sxs-lookup"><span data-stu-id="d9a04-144">**RpcNsBindingImportNext**</span></span>](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext)           | <span data-ttu-id="d9a04-145">nessuno</span><span class="sxs-lookup"><span data-stu-id="d9a04-145">None</span></span>             | <span data-ttu-id="d9a04-146">Server</span><span class="sxs-lookup"><span data-stu-id="d9a04-146">Server</span></span>          |
| [<span data-ttu-id="d9a04-147">**RpcNsBindingLookupNext**</span><span class="sxs-lookup"><span data-stu-id="d9a04-147">**RpcNsBindingLookupNext**</span></span>](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupnext)           | <span data-ttu-id="d9a04-148">nessuno</span><span class="sxs-lookup"><span data-stu-id="d9a04-148">None</span></span>             | <span data-ttu-id="d9a04-149">Server</span><span class="sxs-lookup"><span data-stu-id="d9a04-149">Server</span></span>          |
| [<span data-ttu-id="d9a04-150">**RpcNsBindingSelect**</span><span class="sxs-lookup"><span data-stu-id="d9a04-150">**RpcNsBindingSelect**</span></span>](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingselect)                   | <span data-ttu-id="d9a04-151">Server</span><span class="sxs-lookup"><span data-stu-id="d9a04-151">Server</span></span>           | <span data-ttu-id="d9a04-152">Server</span><span class="sxs-lookup"><span data-stu-id="d9a04-152">Server</span></span>          |
| [<span data-ttu-id="d9a04-153">**RpcServerInqBindings**</span><span class="sxs-lookup"><span data-stu-id="d9a04-153">**RpcServerInqBindings**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings)               | <span data-ttu-id="d9a04-154">nessuno</span><span class="sxs-lookup"><span data-stu-id="d9a04-154">None</span></span>             | <span data-ttu-id="d9a04-155">Server</span><span class="sxs-lookup"><span data-stu-id="d9a04-155">Server</span></span>          |



 

 

 




