---
title: Stato di chiamata asincrono
description: Questa pagina descrive lo stato di chiamata asincrono per le chiamate RPC.
ms.assetid: 4a594dad-a8a1-44e9-8648-ddc2539c234c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96331a18b267b2e44072840727c8fd06afd11d6b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856970"
---
# <a name="asynchronous-call-state"></a><span data-ttu-id="05d6a-103">Stato di chiamata asincrono</span><span class="sxs-lookup"><span data-stu-id="05d6a-103">Asynchronous Call State</span></span>

<span data-ttu-id="05d6a-104">Questa pagina descrive lo stato di chiamata asincrono per le chiamate RPC.</span><span class="sxs-lookup"><span data-stu-id="05d6a-104">This page describes the Asynchronous Call State for RPC calls.</span></span>

## <a name="client-behavior"></a><span data-ttu-id="05d6a-105">Comportamento del client</span><span class="sxs-lookup"><span data-stu-id="05d6a-105">Client Behavior</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="05d6a-106">State</span><span class="sxs-lookup"><span data-stu-id="05d6a-106">State</span></span></th>
<th><span data-ttu-id="05d6a-107">Nome dello stato</span><span class="sxs-lookup"><span data-stu-id="05d6a-107">State name</span></span></th>
<th><span data-ttu-id="05d6a-108">Azione</span><span class="sxs-lookup"><span data-stu-id="05d6a-108">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="05d6a-109">C</span><span class="sxs-lookup"><span data-stu-id="05d6a-109">C</span></span></td>
<td><span data-ttu-id="05d6a-110">Eseguire la chiamata</span><span class="sxs-lookup"><span data-stu-id="05d6a-110">Make the call</span></span></td>
<td><span data-ttu-id="05d6a-111">Eseguire la chiamata RPC</span><span class="sxs-lookup"><span data-stu-id="05d6a-111">Make the RPC</span></span>
<ul>
<li><span data-ttu-id="05d6a-112">In riuscita Vai a stato WComp</span><span class="sxs-lookup"><span data-stu-id="05d6a-112">On success go to state WComp</span></span></li>
<li><span data-ttu-id="05d6a-113">All'eccezione Vai alla fine</span><span class="sxs-lookup"><span data-stu-id="05d6a-113">On exception go to End</span></span></li>
</ul>
<span data-ttu-id="05d6a-114">Per avere esito negativo: passare a Can</span><span class="sxs-lookup"><span data-stu-id="05d6a-114">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="05d6a-115">Capacità</span><span class="sxs-lookup"><span data-stu-id="05d6a-115">Can</span></span></td>
<td><span data-ttu-id="05d6a-116">Annulla la chiamata</span><span class="sxs-lookup"><span data-stu-id="05d6a-116">Cancel the call</span></span></td>
<td><span data-ttu-id="05d6a-117">Chiama <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>RpcAsyncCancelCall</strong></a>Vai a WComp</span><span class="sxs-lookup"><span data-stu-id="05d6a-117">Call <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>RpcAsyncCancelCall</strong></a>Go to WComp</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="05d6a-118">WComp</span><span class="sxs-lookup"><span data-stu-id="05d6a-118">WComp</span></span></td>
<td><span data-ttu-id="05d6a-119">Attendi completamento</span><span class="sxs-lookup"><span data-stu-id="05d6a-119">Wait for completion</span></span></td>
<td><span data-ttu-id="05d6a-120">Attendi notificationCall-è necessario ricevere una notifica completa</span><span class="sxs-lookup"><span data-stu-id="05d6a-120">Wait for notificationCall-complete notification should be received</span></span><br/> <span data-ttu-id="05d6a-121">Vai a comp</span><span class="sxs-lookup"><span data-stu-id="05d6a-121">Go to Comp</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="05d6a-122">Comp</span><span class="sxs-lookup"><span data-stu-id="05d6a-122">Comp</span></span></td>
<td><span data-ttu-id="05d6a-123">Completion</span><span class="sxs-lookup"><span data-stu-id="05d6a-123">Completion</span></span></td>
<td><span data-ttu-id="05d6a-124">Problema <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>Vai alla fine</span><span class="sxs-lookup"><span data-stu-id="05d6a-124">Issue <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>Go to End</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="05d6a-125">Fine</span><span class="sxs-lookup"><span data-stu-id="05d6a-125">End</span></span></td>


</tr>
</tbody>
</table>



 

## <a name="server-behavior"></a><span data-ttu-id="05d6a-126">Comportamento del server</span><span class="sxs-lookup"><span data-stu-id="05d6a-126">Server Behavior</span></span>



| <span data-ttu-id="05d6a-127">State</span><span class="sxs-lookup"><span data-stu-id="05d6a-127">State</span></span> | <span data-ttu-id="05d6a-128">Nome dello stato</span><span class="sxs-lookup"><span data-stu-id="05d6a-128">State name</span></span>     | <span data-ttu-id="05d6a-129">Azione</span><span class="sxs-lookup"><span data-stu-id="05d6a-129">Action</span></span>                                                                                                                                                                                                              |
|-------|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05d6a-130">D</span><span class="sxs-lookup"><span data-stu-id="05d6a-130">D</span></span>     | <span data-ttu-id="05d6a-131">Dispatch</span><span class="sxs-lookup"><span data-stu-id="05d6a-131">Dispatch</span></span>       | <span data-ttu-id="05d6a-132">La chiamata viene inviata dal runtimeProcess RPC</span><span class="sxs-lookup"><span data-stu-id="05d6a-132">The call is dispatched by the RPC runtimeProcess</span></span><br/> <span data-ttu-id="05d6a-133">Vai a comp</span><span class="sxs-lookup"><span data-stu-id="05d6a-133">Go to Comp</span></span><br/> <span data-ttu-id="05d6a-134">Per avere esito negativo (durante l'esecuzione sul thread RPC): Genera eccezione; Vai alla fine</span><span class="sxs-lookup"><span data-stu-id="05d6a-134">To fail fatally (while executing on the RPC thread): Raise exception; go to End</span></span><br/> <span data-ttu-id="05d6a-135">Per eseguire correttamente l'errore: passare a un</span><span class="sxs-lookup"><span data-stu-id="05d6a-135">To fail gracefully: go to A</span></span><br/> |
| <span data-ttu-id="05d6a-136">A</span><span class="sxs-lookup"><span data-stu-id="05d6a-136">A</span></span>     | <span data-ttu-id="05d6a-137">Interrompi la chiamata</span><span class="sxs-lookup"><span data-stu-id="05d6a-137">Abort the call</span></span> | <span data-ttu-id="05d6a-138">Chiama [**RpcAsyncAbortCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall)Vai alla fine</span><span class="sxs-lookup"><span data-stu-id="05d6a-138">Call [**RpcAsyncAbortCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall)Go to End</span></span><br/>                                                                                                                                             |
| <span data-ttu-id="05d6a-139">Comp</span><span class="sxs-lookup"><span data-stu-id="05d6a-139">Comp</span></span>  | <span data-ttu-id="05d6a-140">Completion</span><span class="sxs-lookup"><span data-stu-id="05d6a-140">Completion</span></span>     | <span data-ttu-id="05d6a-141">Problema [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall)Vai alla fine</span><span class="sxs-lookup"><span data-stu-id="05d6a-141">Issue [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall)Go to End</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="05d6a-142">Fine</span><span class="sxs-lookup"><span data-stu-id="05d6a-142">End</span></span>   |                |                                                                                                                                                                                                                     |



 

 

 





