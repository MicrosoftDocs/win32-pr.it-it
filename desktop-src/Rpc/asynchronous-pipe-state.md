---
title: Stato di pipe asincrono
description: Questa pagina descrive lo stato asincrono della pipe per le chiamate RPC.
ms.assetid: af937eba-6b70-447a-af76-a8e27f5754e3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8396b08c7ef7b8152457d9426883645fab39bdef
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104046317"
---
# <a name="asynchronous-pipe-state"></a><span data-ttu-id="7a7eb-103">Stato di pipe asincrono</span><span class="sxs-lookup"><span data-stu-id="7a7eb-103">Asynchronous Pipe State</span></span>

<span data-ttu-id="7a7eb-104">Questa pagina descrive lo stato asincrono della pipe per le chiamate RPC.</span><span class="sxs-lookup"><span data-stu-id="7a7eb-104">This page describes the Asynchronous Pipe State for RPC calls.</span></span>

## <a name="in-pipe"></a><span data-ttu-id="7a7eb-105">IN pipe</span><span class="sxs-lookup"><span data-stu-id="7a7eb-105">IN Pipe</span></span>

<span data-ttu-id="7a7eb-106">Comportamento del client</span><span class="sxs-lookup"><span data-stu-id="7a7eb-106">Client Behavior</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7a7eb-107">State</span><span class="sxs-lookup"><span data-stu-id="7a7eb-107">State</span></span></th>
<th><span data-ttu-id="7a7eb-108">State Name</span><span class="sxs-lookup"><span data-stu-id="7a7eb-108">State Name</span></span></th>
<th><span data-ttu-id="7a7eb-109">Azione</span><span class="sxs-lookup"><span data-stu-id="7a7eb-109">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7a7eb-110">C</span><span class="sxs-lookup"><span data-stu-id="7a7eb-110">C</span></span></td>
<td><span data-ttu-id="7a7eb-111">Eseguire la chiamata</span><span class="sxs-lookup"><span data-stu-id="7a7eb-111">Make the call</span></span></td>
<td><span data-ttu-id="7a7eb-112">Eseguire la chiamata RPC</span><span class="sxs-lookup"><span data-stu-id="7a7eb-112">Make the RPC</span></span>
<ul>
<li><span data-ttu-id="7a7eb-113">Alla riuscita Vai a stato WS</span><span class="sxs-lookup"><span data-stu-id="7a7eb-113">On success go to state WS</span></span></li>
<li><span data-ttu-id="7a7eb-114">All'eccezione Vai alla fine</span><span class="sxs-lookup"><span data-stu-id="7a7eb-114">On exception go to End</span></span></li>
</ul>
<span data-ttu-id="7a7eb-115">Per avere esito negativo: passare a Can</span><span class="sxs-lookup"><span data-stu-id="7a7eb-115">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7a7eb-116">P</span><span class="sxs-lookup"><span data-stu-id="7a7eb-116">P</span></span></td>
<td><span data-ttu-id="7a7eb-117">Push</span><span class="sxs-lookup"><span data-stu-id="7a7eb-117">Push</span></span></td>
<td><span data-ttu-id="7a7eb-118">Eseguire un push</span><span class="sxs-lookup"><span data-stu-id="7a7eb-118">Make a push</span></span>
<ul>
<li><span data-ttu-id="7a7eb-119">In caso di errore Vai alla fine</span><span class="sxs-lookup"><span data-stu-id="7a7eb-119">On failure go to End</span></span></li>
<li><span data-ttu-id="7a7eb-120">Alla riuscita andare a WS</span><span class="sxs-lookup"><span data-stu-id="7a7eb-120">On success go to WS</span></span></li>
</ul>
<span data-ttu-id="7a7eb-121">Per avere esito negativo: passare a Can</span><span class="sxs-lookup"><span data-stu-id="7a7eb-121">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7a7eb-122">WS</span><span class="sxs-lookup"><span data-stu-id="7a7eb-122">WS</span></span></td>
<td><span data-ttu-id="7a7eb-123">Attendi invio</span><span class="sxs-lookup"><span data-stu-id="7a7eb-123">Wait for Send</span></span></td>
<td><span data-ttu-id="7a7eb-124">Attendi notifica</span><span class="sxs-lookup"><span data-stu-id="7a7eb-124">Wait for notification</span></span>
<ul>
<li><span data-ttu-id="7a7eb-125">In caso di errore di ricevere una notifica, passare a Can</span><span class="sxs-lookup"><span data-stu-id="7a7eb-125">On failure to get a notification go to Can</span></span></li>
<li><span data-ttu-id="7a7eb-126">Se viene ricevuto un <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> di esito positivo ed è necessario inviare più dati, passare a P</span><span class="sxs-lookup"><span data-stu-id="7a7eb-126">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> is received and more data needs to be sent go to P</span></span></li>
<li><span data-ttu-id="7a7eb-127">Se viene ricevuta una <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> con esito positivo e non è necessario inviare più dati, passare a NP</span><span class="sxs-lookup"><span data-stu-id="7a7eb-127">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> is received and more data does not need to be sent go to NP</span></span></li>
<li><span data-ttu-id="7a7eb-128">Se viene ricevuto un errore <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcCallComplete</strong></a> go comp</span><span class="sxs-lookup"><span data-stu-id="7a7eb-128">If a failure <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcCallComplete</strong></a> is received go Comp</span></span></li>
</ul>
<span data-ttu-id="7a7eb-129">Per avere esito negativo: passare a Can</span><span class="sxs-lookup"><span data-stu-id="7a7eb-129">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7a7eb-130">NP</span><span class="sxs-lookup"><span data-stu-id="7a7eb-130">NP</span></span></td>
<td><span data-ttu-id="7a7eb-131">Push null</span><span class="sxs-lookup"><span data-stu-id="7a7eb-131">Null Push</span></span></td>
<td><span data-ttu-id="7a7eb-132">Push 0 byte (push null)</span><span class="sxs-lookup"><span data-stu-id="7a7eb-132">Push 0 bytes (null push)</span></span>
<ul>
<li><span data-ttu-id="7a7eb-133">In caso di errore Vai alla fine</span><span class="sxs-lookup"><span data-stu-id="7a7eb-133">On failure go to End</span></span></li>
<li><span data-ttu-id="7a7eb-134">In riuscita andare a WComp</span><span class="sxs-lookup"><span data-stu-id="7a7eb-134">On success go to WComp</span></span></li>
</ul>
<span data-ttu-id="7a7eb-135">Per avere esito negativo: passare a Can</span><span class="sxs-lookup"><span data-stu-id="7a7eb-135">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7a7eb-136">Capacità</span><span class="sxs-lookup"><span data-stu-id="7a7eb-136">Can</span></span></td>
<td><span data-ttu-id="7a7eb-137">Annulla la chiamata</span><span class="sxs-lookup"><span data-stu-id="7a7eb-137">Cancel the Call</span></span></td>
<td><span data-ttu-id="7a7eb-138">Chiama <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>RpcAsyncCancelCall</strong></a>Vai a WComp</span><span class="sxs-lookup"><span data-stu-id="7a7eb-138">Call <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>RpcAsyncCancelCall</strong></a>Go to WComp</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7a7eb-139">WComp</span><span class="sxs-lookup"><span data-stu-id="7a7eb-139">WComp</span></span></td>
<td><span data-ttu-id="7a7eb-140">Attendi completamento</span><span class="sxs-lookup"><span data-stu-id="7a7eb-140">Wait for Completion</span></span></td>
<td><span data-ttu-id="7a7eb-141">Attendere la ricezione della notifica notificationCall-complete.</span><span class="sxs-lookup"><span data-stu-id="7a7eb-141">Wait for notificationCall-complete notification should be received.</span></span><br/> <span data-ttu-id="7a7eb-142">Vai a comp</span><span class="sxs-lookup"><span data-stu-id="7a7eb-142">Go to Comp</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7a7eb-143">Comp</span><span class="sxs-lookup"><span data-stu-id="7a7eb-143">Comp</span></span></td>
<td><span data-ttu-id="7a7eb-144">Completion</span><span class="sxs-lookup"><span data-stu-id="7a7eb-144">Completion</span></span></td>
<td><span data-ttu-id="7a7eb-145">Problema <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>Vai alla fine</span><span class="sxs-lookup"><span data-stu-id="7a7eb-145">Issue <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>Go to End</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7a7eb-146">Fine</span><span class="sxs-lookup"><span data-stu-id="7a7eb-146">End</span></span></td>


</tr>
</tbody>
</table>



 

<span data-ttu-id="7a7eb-147">Comportamento del server</span><span class="sxs-lookup"><span data-stu-id="7a7eb-147">Server Behavior</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7a7eb-148">State</span><span class="sxs-lookup"><span data-stu-id="7a7eb-148">State</span></span></th>
<th><span data-ttu-id="7a7eb-149">State Name</span><span class="sxs-lookup"><span data-stu-id="7a7eb-149">State Name</span></span></th>
<th><span data-ttu-id="7a7eb-150">Azione</span><span class="sxs-lookup"><span data-stu-id="7a7eb-150">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7a7eb-151">D</span><span class="sxs-lookup"><span data-stu-id="7a7eb-151">D</span></span></td>
<td><span data-ttu-id="7a7eb-152">Dispatch</span><span class="sxs-lookup"><span data-stu-id="7a7eb-152">Dispatch</span></span></td>
<td><span data-ttu-id="7a7eb-153">La chiamata viene inviata dal runtime RPC Vai a P</span><span class="sxs-lookup"><span data-stu-id="7a7eb-153">The call is dispatched by the RPC runtime Go to P</span></span><br/> <span data-ttu-id="7a7eb-154">Per avere esito negativo (durante l'esecuzione sul thread RPC): Genera eccezione; Vai alla fine</span><span class="sxs-lookup"><span data-stu-id="7a7eb-154">To fail fatally (while executing on the RPC thread): Raise exception; go to End</span></span><br/> <span data-ttu-id="7a7eb-155">Per eseguire correttamente l'errore: passare a un</span><span class="sxs-lookup"><span data-stu-id="7a7eb-155">To fail gracefully: Go to A</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7a7eb-156">P</span><span class="sxs-lookup"><span data-stu-id="7a7eb-156">P</span></span></td>
<td><span data-ttu-id="7a7eb-157">Pull</span><span class="sxs-lookup"><span data-stu-id="7a7eb-157">Pull</span></span></td>
<td><span data-ttu-id="7a7eb-158">Eseguire un pull</span><span class="sxs-lookup"><span data-stu-id="7a7eb-158">Make a pull</span></span>
<ul>
<li><span data-ttu-id="7a7eb-159">In caso di errore Vai alla fine</span><span class="sxs-lookup"><span data-stu-id="7a7eb-159">On failure go to End</span></span></li>
<li><span data-ttu-id="7a7eb-160">Al completamento dell'operazione riuscita e sincrona con byte diversi da zero, vai a P</span><span class="sxs-lookup"><span data-stu-id="7a7eb-160">On success and synchronous completion with non-zero bytes read go to P</span></span></li>
<li><span data-ttu-id="7a7eb-161">Al completamento dell'operazione riuscita e sincrona con zero byte letti (pull null) Vai a comp</span><span class="sxs-lookup"><span data-stu-id="7a7eb-161">On success and synchronous completion with zero bytes read (null pull) go to Comp</span></span></li>
<li><span data-ttu-id="7a7eb-162">Alla riuscita e al completamento asincrono (ERROR_IO_PENDING viene restituito) andare a WP</span><span class="sxs-lookup"><span data-stu-id="7a7eb-162">On success and asynchronous completion (ERROR_IO_PENDING is returned) go to WP</span></span></li>
</ul>
<span data-ttu-id="7a7eb-163">Per avere esito negativo: passare a un</span><span class="sxs-lookup"><span data-stu-id="7a7eb-163">To fail: go to A</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7a7eb-164">WP</span><span class="sxs-lookup"><span data-stu-id="7a7eb-164">WP</span></span></td>
<td><span data-ttu-id="7a7eb-165">Attendi pull</span><span class="sxs-lookup"><span data-stu-id="7a7eb-165">Wait for Pull</span></span></td>
<td><span data-ttu-id="7a7eb-166">Attendi notifica</span><span class="sxs-lookup"><span data-stu-id="7a7eb-166">Wait for notification</span></span>
<ul>
<li><span data-ttu-id="7a7eb-167">In caso di errore per ottenere un completamento, passare a</span><span class="sxs-lookup"><span data-stu-id="7a7eb-167">On failure to get a completion go to A</span></span></li>
<li><span data-ttu-id="7a7eb-168">Se viene ricevuto un errore <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> , passare a un</span><span class="sxs-lookup"><span data-stu-id="7a7eb-168">If a failure <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> is received go to A</span></span></li>
<li><span data-ttu-id="7a7eb-169">Se viene ricevuto un <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> con esito positivo con byte diversi da zero, vedere Vai a P</span><span class="sxs-lookup"><span data-stu-id="7a7eb-169">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> is received with non-zero bytes read go to P</span></span></li>
<li><span data-ttu-id="7a7eb-170">Se viene ricevuto un <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> con esito positivo con zero byte letti (pull null) Vai a comp</span><span class="sxs-lookup"><span data-stu-id="7a7eb-170">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> is received with zero bytes read (null pull) go to Comp</span></span></li>
<li><span data-ttu-id="7a7eb-171">Se viene ricevuto un errore, passare a un</span><span class="sxs-lookup"><span data-stu-id="7a7eb-171">If a failure is received go to A</span></span></li>
</ul>
<span data-ttu-id="7a7eb-172">Per avere esito negativo: passare a un</span><span class="sxs-lookup"><span data-stu-id="7a7eb-172">To fail: go to A</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7a7eb-173">A</span><span class="sxs-lookup"><span data-stu-id="7a7eb-173">A</span></span></td>
<td><span data-ttu-id="7a7eb-174">Interrompi la chiamata</span><span class="sxs-lookup"><span data-stu-id="7a7eb-174">Abort the Call</span></span></td>
<td><span data-ttu-id="7a7eb-175">Chiama <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall"><strong>RpcAsyncAbortCall</strong></a>Vai alla fine</span><span class="sxs-lookup"><span data-stu-id="7a7eb-175">Call <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall"><strong>RpcAsyncAbortCall</strong></a>Go to End</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7a7eb-176">Comp</span><span class="sxs-lookup"><span data-stu-id="7a7eb-176">Comp</span></span></td>
<td><span data-ttu-id="7a7eb-177">Completion</span><span class="sxs-lookup"><span data-stu-id="7a7eb-177">Completion</span></span></td>
<td><span data-ttu-id="7a7eb-178">Chiama <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>Vai alla fine</span><span class="sxs-lookup"><span data-stu-id="7a7eb-178">Call <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>Go to End</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7a7eb-179">Fine</span><span class="sxs-lookup"><span data-stu-id="7a7eb-179">End</span></span></td>


</tr>
</tbody>
</table>



 

## <a name="out-pipe"></a><span data-ttu-id="7a7eb-180">Pipe OUT</span><span class="sxs-lookup"><span data-stu-id="7a7eb-180">OUT Pipe</span></span>

<span data-ttu-id="7a7eb-181">Comportamento del client</span><span class="sxs-lookup"><span data-stu-id="7a7eb-181">Client Behavior</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7a7eb-182">State</span><span class="sxs-lookup"><span data-stu-id="7a7eb-182">State</span></span></th>
<th><span data-ttu-id="7a7eb-183">State Name</span><span class="sxs-lookup"><span data-stu-id="7a7eb-183">State Name</span></span></th>
<th><span data-ttu-id="7a7eb-184">Azione</span><span class="sxs-lookup"><span data-stu-id="7a7eb-184">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7a7eb-185">C</span><span class="sxs-lookup"><span data-stu-id="7a7eb-185">C</span></span></td>
<td><span data-ttu-id="7a7eb-186">Eseguire la chiamata</span><span class="sxs-lookup"><span data-stu-id="7a7eb-186">Make the call</span></span></td>
<td><span data-ttu-id="7a7eb-187">Eseguire la chiamata RPC</span><span class="sxs-lookup"><span data-stu-id="7a7eb-187">Make the RPC</span></span>
<ul>
<li><span data-ttu-id="7a7eb-188">Alla riuscita andare a P</span><span class="sxs-lookup"><span data-stu-id="7a7eb-188">On success go to P</span></span></li>
<li><span data-ttu-id="7a7eb-189">In caso di errore Vai a comp</span><span class="sxs-lookup"><span data-stu-id="7a7eb-189">On failure go to Comp</span></span></li>
</ul>
<span data-ttu-id="7a7eb-190">Per avere esito negativo: passare a Can</span><span class="sxs-lookup"><span data-stu-id="7a7eb-190">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7a7eb-191">P</span><span class="sxs-lookup"><span data-stu-id="7a7eb-191">P</span></span></td>
<td><span data-ttu-id="7a7eb-192">Pull</span><span class="sxs-lookup"><span data-stu-id="7a7eb-192">Pull</span></span></td>
<td><span data-ttu-id="7a7eb-193">Eseguire un pull</span><span class="sxs-lookup"><span data-stu-id="7a7eb-193">Make a pull</span></span>
<ul>
<li><span data-ttu-id="7a7eb-194">In caso di errore Vai alla fine</span><span class="sxs-lookup"><span data-stu-id="7a7eb-194">On failure go to End</span></span></li>
<li><span data-ttu-id="7a7eb-195">Al completamento dell'operazione riuscita e sincrona con byte diversi da zero, vai a P</span><span class="sxs-lookup"><span data-stu-id="7a7eb-195">On success and synchronous completion with non-zero bytes read go to P</span></span></li>
<li><span data-ttu-id="7a7eb-196">Al completamento dell'operazione riuscita e sincrona con zero byte letti (pull null) passare a WComp</span><span class="sxs-lookup"><span data-stu-id="7a7eb-196">On success and synchronous completion with zero bytes read (null pull) go to WComp</span></span></li>
<li><span data-ttu-id="7a7eb-197">Alla riuscita e al completamento asincrono (ERROR_IO_PENDING viene restituito) andare a WP</span><span class="sxs-lookup"><span data-stu-id="7a7eb-197">On success and asynchronous completion (ERROR_IO_PENDING is returned) go to WP</span></span></li>
</ul>
<span data-ttu-id="7a7eb-198">Per avere esito negativo: passare a Can</span><span class="sxs-lookup"><span data-stu-id="7a7eb-198">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7a7eb-199">WP</span><span class="sxs-lookup"><span data-stu-id="7a7eb-199">WP</span></span></td>
<td><span data-ttu-id="7a7eb-200">Attendi pull</span><span class="sxs-lookup"><span data-stu-id="7a7eb-200">Wait for Pull</span></span></td>
<td><span data-ttu-id="7a7eb-201">Attendi notifica</span><span class="sxs-lookup"><span data-stu-id="7a7eb-201">Wait for notification</span></span>
<ul>
<li><span data-ttu-id="7a7eb-202">In caso di errore per ottenere un completamento, passare a Can</span><span class="sxs-lookup"><span data-stu-id="7a7eb-202">On failure to get a completion go to Can</span></span></li>
<li><span data-ttu-id="7a7eb-203">Se viene ricevuto un errore <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> , passare a Can</span><span class="sxs-lookup"><span data-stu-id="7a7eb-203">If a failure <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> is received go to Can</span></span></li>
<li><span data-ttu-id="7a7eb-204">Se viene ricevuto un <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> con esito positivo con byte diversi da zero, vedere Vai a P</span><span class="sxs-lookup"><span data-stu-id="7a7eb-204">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> is received with non-zero bytes read go to P</span></span></li>
<li><span data-ttu-id="7a7eb-205">Se viene ricevuto un <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> con esito positivo con zero byte letti (pull null) Vai a comp</span><span class="sxs-lookup"><span data-stu-id="7a7eb-205">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> is received with zero bytes read (null pull) go to Comp</span></span></li>
<li><span data-ttu-id="7a7eb-206">Se viene ricevuto un errore, Go può</span><span class="sxs-lookup"><span data-stu-id="7a7eb-206">If a failure is received go Can</span></span></li>
</ul>
<span data-ttu-id="7a7eb-207">Per avere esito negativo: passare a Can</span><span class="sxs-lookup"><span data-stu-id="7a7eb-207">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7a7eb-208">Capacità</span><span class="sxs-lookup"><span data-stu-id="7a7eb-208">Can</span></span></td>
<td><span data-ttu-id="7a7eb-209">Annulla la chiamata</span><span class="sxs-lookup"><span data-stu-id="7a7eb-209">Cancel the Call</span></span></td>
<td><span data-ttu-id="7a7eb-210">Chiama <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>RpcAsyncCancelCall</strong></a>Vai a WComp</span><span class="sxs-lookup"><span data-stu-id="7a7eb-210">Call <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>RpcAsyncCancelCall</strong></a>Go to WComp</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7a7eb-211">WComp</span><span class="sxs-lookup"><span data-stu-id="7a7eb-211">WComp</span></span></td>
<td><span data-ttu-id="7a7eb-212">Attendi completamento</span><span class="sxs-lookup"><span data-stu-id="7a7eb-212">Wait for Completion</span></span></td>
<td><span data-ttu-id="7a7eb-213">Attendere la notifica.</span><span class="sxs-lookup"><span data-stu-id="7a7eb-213">Wait for notification.</span></span> <span data-ttu-id="7a7eb-214">È necessario ricevere una notifica di completamento della chiamata.</span><span class="sxs-lookup"><span data-stu-id="7a7eb-214">Call-complete notification should be received.</span></span><br/> <span data-ttu-id="7a7eb-215">Vai a comp</span><span class="sxs-lookup"><span data-stu-id="7a7eb-215">Go to Comp</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7a7eb-216">Comp</span><span class="sxs-lookup"><span data-stu-id="7a7eb-216">Comp</span></span></td>
<td><span data-ttu-id="7a7eb-217">Completion</span><span class="sxs-lookup"><span data-stu-id="7a7eb-217">Completion</span></span></td>
<td><span data-ttu-id="7a7eb-218">Problema <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>Vai alla fine</span><span class="sxs-lookup"><span data-stu-id="7a7eb-218">Issue <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>Go to End</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7a7eb-219">Fine</span><span class="sxs-lookup"><span data-stu-id="7a7eb-219">End</span></span></td>


</tr>
</tbody>
</table>



 

<span data-ttu-id="7a7eb-220">Comportamento del server</span><span class="sxs-lookup"><span data-stu-id="7a7eb-220">Server Behavior</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7a7eb-221">State</span><span class="sxs-lookup"><span data-stu-id="7a7eb-221">State</span></span></th>
<th><span data-ttu-id="7a7eb-222">State Name</span><span class="sxs-lookup"><span data-stu-id="7a7eb-222">State Name</span></span></th>
<th><span data-ttu-id="7a7eb-223">Azione</span><span class="sxs-lookup"><span data-stu-id="7a7eb-223">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7a7eb-224">D</span><span class="sxs-lookup"><span data-stu-id="7a7eb-224">D</span></span></td>
<td><span data-ttu-id="7a7eb-225">Dispatch</span><span class="sxs-lookup"><span data-stu-id="7a7eb-225">Dispatch</span></span></td>
<td><span data-ttu-id="7a7eb-226">La chiamata viene inviata dal runtime RPC Vai a P</span><span class="sxs-lookup"><span data-stu-id="7a7eb-226">The call is dispatched by the RPC runtime Go to P</span></span><br/> <span data-ttu-id="7a7eb-227">Per avere esito negativo (durante l'esecuzione sul thread RPC): Genera eccezione; Vai alla fine</span><span class="sxs-lookup"><span data-stu-id="7a7eb-227">To fail fatally (while executing on the RPC thread): Raise exception; go to End</span></span><br/> <span data-ttu-id="7a7eb-228">Per eseguire correttamente l'errore: passare a un</span><span class="sxs-lookup"><span data-stu-id="7a7eb-228">To fail gracefully: Go to A</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7a7eb-229">P</span><span class="sxs-lookup"><span data-stu-id="7a7eb-229">P</span></span></td>
<td><span data-ttu-id="7a7eb-230">Push</span><span class="sxs-lookup"><span data-stu-id="7a7eb-230">Push</span></span></td>
<td><span data-ttu-id="7a7eb-231">Eseguire un push</span><span class="sxs-lookup"><span data-stu-id="7a7eb-231">Make a push</span></span>
<ul>
<li><span data-ttu-id="7a7eb-232">In riuscita andare a WP</span><span class="sxs-lookup"><span data-stu-id="7a7eb-232">On success go to WP</span></span></li>
<li><span data-ttu-id="7a7eb-233">In caso di errore Vai alla fine</span><span class="sxs-lookup"><span data-stu-id="7a7eb-233">On failure go to End</span></span></li>
</ul>
<span data-ttu-id="7a7eb-234">Per avere esito negativo: passare a un</span><span class="sxs-lookup"><span data-stu-id="7a7eb-234">To fail: go to A</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7a7eb-235">WP</span><span class="sxs-lookup"><span data-stu-id="7a7eb-235">WP</span></span></td>
<td><span data-ttu-id="7a7eb-236">Attendi push</span><span class="sxs-lookup"><span data-stu-id="7a7eb-236">Wait for Push</span></span></td>
<td><span data-ttu-id="7a7eb-237">Attendi notifica</span><span class="sxs-lookup"><span data-stu-id="7a7eb-237">Wait for notification</span></span>
<ul>
<li><span data-ttu-id="7a7eb-238">In caso di errore per ottenere un completamento, passare a</span><span class="sxs-lookup"><span data-stu-id="7a7eb-238">On failure to get a completion go to A</span></span></li>
<li><span data-ttu-id="7a7eb-239">Se viene ricevuto un <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> di esito positivo ed è necessario inviare più dati, passare a P</span><span class="sxs-lookup"><span data-stu-id="7a7eb-239">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> is received and more data needs to be sent go to P</span></span></li>
<li><span data-ttu-id="7a7eb-240">Se viene ricevuta una <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> con esito positivo e non è necessario inviare più dati, passare a NP</span><span class="sxs-lookup"><span data-stu-id="7a7eb-240">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> is received and more data does not need to be sent go to NP</span></span></li>
<li><span data-ttu-id="7a7eb-241">Se viene ricevuto un errore go comp</span><span class="sxs-lookup"><span data-stu-id="7a7eb-241">If a failure is received go Comp</span></span></li>
</ul>
<span data-ttu-id="7a7eb-242">Per avere esito negativo: passare a un</span><span class="sxs-lookup"><span data-stu-id="7a7eb-242">To fail: go to A</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7a7eb-243">NP</span><span class="sxs-lookup"><span data-stu-id="7a7eb-243">NP</span></span></td>
<td><span data-ttu-id="7a7eb-244">Push null</span><span class="sxs-lookup"><span data-stu-id="7a7eb-244">Null Push</span></span></td>
<td><span data-ttu-id="7a7eb-245">Push 0 byte</span><span class="sxs-lookup"><span data-stu-id="7a7eb-245">Push 0 bytes</span></span>
<ul>
<li><span data-ttu-id="7a7eb-246">in riuscita andare a WNP</span><span class="sxs-lookup"><span data-stu-id="7a7eb-246">on success go to WNP</span></span></li>
<li><span data-ttu-id="7a7eb-247">in caso di errore Vai a comp</span><span class="sxs-lookup"><span data-stu-id="7a7eb-247">on failure go to Comp</span></span></li>
</ul>
<span data-ttu-id="7a7eb-248">Per avere esito negativo: passare a un</span><span class="sxs-lookup"><span data-stu-id="7a7eb-248">To fail: go to A</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7a7eb-249">WNP</span><span class="sxs-lookup"><span data-stu-id="7a7eb-249">WNP</span></span></td>
<td><span data-ttu-id="7a7eb-250">Attendi push null</span><span class="sxs-lookup"><span data-stu-id="7a7eb-250">Wait for Null Push</span></span></td>
<td><span data-ttu-id="7a7eb-251">Attendi notifica</span><span class="sxs-lookup"><span data-stu-id="7a7eb-251">Wait for notification</span></span>
<ul>
<li><span data-ttu-id="7a7eb-252">In caso di errore per ottenere un completamento, passare a</span><span class="sxs-lookup"><span data-stu-id="7a7eb-252">On failure to get a completion go to A</span></span></li>
<li><span data-ttu-id="7a7eb-253">Se viene ricevuto un errore go comp</span><span class="sxs-lookup"><span data-stu-id="7a7eb-253">If a failure is received go Comp</span></span></li>
<li><span data-ttu-id="7a7eb-254">Se viene ricevuta una riuscita, vai comp</span><span class="sxs-lookup"><span data-stu-id="7a7eb-254">If a success is received go Comp</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7a7eb-255">A</span><span class="sxs-lookup"><span data-stu-id="7a7eb-255">A</span></span></td>
<td><span data-ttu-id="7a7eb-256">Interrompi la chiamata</span><span class="sxs-lookup"><span data-stu-id="7a7eb-256">Abort the Call</span></span></td>
<td><span data-ttu-id="7a7eb-257">Chiama <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall"><strong>RpcAsyncAbortCall</strong></a>; Vai alla fine</span><span class="sxs-lookup"><span data-stu-id="7a7eb-257">Call <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall"><strong>RpcAsyncAbortCall</strong></a>; go to End</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7a7eb-258">Comp</span><span class="sxs-lookup"><span data-stu-id="7a7eb-258">Comp</span></span></td>
<td><span data-ttu-id="7a7eb-259">Completion</span><span class="sxs-lookup"><span data-stu-id="7a7eb-259">Completion</span></span></td>
<td><span data-ttu-id="7a7eb-260">Problema <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>; Vai alla fine</span><span class="sxs-lookup"><span data-stu-id="7a7eb-260">Issue <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>; go to End</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7a7eb-261">Fine</span><span class="sxs-lookup"><span data-stu-id="7a7eb-261">End</span></span></td>


</tr>
</tbody>
</table>



 

## <a name="in-out-pipe"></a><span data-ttu-id="7a7eb-262">Pipe IN uscita</span><span class="sxs-lookup"><span data-stu-id="7a7eb-262">IN-OUT Pipe</span></span>

<span data-ttu-id="7a7eb-263">Comportamento del client</span><span class="sxs-lookup"><span data-stu-id="7a7eb-263">Client Behavior</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7a7eb-264">State</span><span class="sxs-lookup"><span data-stu-id="7a7eb-264">State</span></span></th>
<th><span data-ttu-id="7a7eb-265">State Name</span><span class="sxs-lookup"><span data-stu-id="7a7eb-265">State Name</span></span></th>
<th><span data-ttu-id="7a7eb-266">Azione</span><span class="sxs-lookup"><span data-stu-id="7a7eb-266">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7a7eb-267">C</span><span class="sxs-lookup"><span data-stu-id="7a7eb-267">C</span></span></td>
<td><span data-ttu-id="7a7eb-268">Eseguire la chiamata</span><span class="sxs-lookup"><span data-stu-id="7a7eb-268">Make the call</span></span></td>
<td><span data-ttu-id="7a7eb-269">Eseguire la chiamata RPC</span><span class="sxs-lookup"><span data-stu-id="7a7eb-269">Make the RPC</span></span>
<ul>
<li><span data-ttu-id="7a7eb-270">Alla riuscita andare a WS</span><span class="sxs-lookup"><span data-stu-id="7a7eb-270">On success go to WS</span></span></li>
<li><span data-ttu-id="7a7eb-271">All'eccezione Vai alla fine</span><span class="sxs-lookup"><span data-stu-id="7a7eb-271">On exception go to End</span></span></li>
</ul>
<span data-ttu-id="7a7eb-272">Per avere esito negativo: passare a Can</span><span class="sxs-lookup"><span data-stu-id="7a7eb-272">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7a7eb-273">PS</span><span class="sxs-lookup"><span data-stu-id="7a7eb-273">PS</span></span></td>
<td><span data-ttu-id="7a7eb-274">Push</span><span class="sxs-lookup"><span data-stu-id="7a7eb-274">Push</span></span></td>
<td><span data-ttu-id="7a7eb-275">Eseguire un push</span><span class="sxs-lookup"><span data-stu-id="7a7eb-275">Make a push</span></span>
<ul>
<li><span data-ttu-id="7a7eb-276">In caso di errore Vai alla fine</span><span class="sxs-lookup"><span data-stu-id="7a7eb-276">On failure go to End</span></span></li>
<li><span data-ttu-id="7a7eb-277">Alla riuscita andare a WS</span><span class="sxs-lookup"><span data-stu-id="7a7eb-277">On success go to WS</span></span></li>
</ul>
<span data-ttu-id="7a7eb-278">Per avere esito negativo: passare a Can</span><span class="sxs-lookup"><span data-stu-id="7a7eb-278">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7a7eb-279">WS</span><span class="sxs-lookup"><span data-stu-id="7a7eb-279">WS</span></span></td>
<td><span data-ttu-id="7a7eb-280">Attendi invio</span><span class="sxs-lookup"><span data-stu-id="7a7eb-280">Wait for Send</span></span></td>
<td><span data-ttu-id="7a7eb-281">Attendi notifica</span><span class="sxs-lookup"><span data-stu-id="7a7eb-281">Wait for notification</span></span>
<ul>
<li><span data-ttu-id="7a7eb-282">In caso di errore di ricevere una notifica, passare a Can</span><span class="sxs-lookup"><span data-stu-id="7a7eb-282">On failure to get a notification go to Can</span></span></li>
<li><span data-ttu-id="7a7eb-283">Se viene ricevuto un <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> di esito positivo ed è necessario inviare più dati, passare a PS</span><span class="sxs-lookup"><span data-stu-id="7a7eb-283">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> is received and more data needs to be sent go to PS</span></span></li>
<li><span data-ttu-id="7a7eb-284">Se viene ricevuta una <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> con esito positivo e non è necessario inviare più dati, passare a NP</span><span class="sxs-lookup"><span data-stu-id="7a7eb-284">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> is received and more data does not need to be sent go to NP</span></span></li>
<li><span data-ttu-id="7a7eb-285">Se viene ricevuto un errore <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcCallComplete</strong></a> go comp</span><span class="sxs-lookup"><span data-stu-id="7a7eb-285">If a failure <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcCallComplete</strong></a> is received go Comp</span></span></li>
</ul>
<span data-ttu-id="7a7eb-286">Per avere esito negativo: passare a Can</span><span class="sxs-lookup"><span data-stu-id="7a7eb-286">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7a7eb-287">NP</span><span class="sxs-lookup"><span data-stu-id="7a7eb-287">NP</span></span></td>
<td><span data-ttu-id="7a7eb-288">Push null</span><span class="sxs-lookup"><span data-stu-id="7a7eb-288">Null Push</span></span></td>
<td><span data-ttu-id="7a7eb-289">Push 0 byte (push null)</span><span class="sxs-lookup"><span data-stu-id="7a7eb-289">Push 0 bytes (null push)</span></span>
<ul>
<li><span data-ttu-id="7a7eb-290">In caso di errore Vai alla fine</span><span class="sxs-lookup"><span data-stu-id="7a7eb-290">On failure go to End</span></span></li>
<li><span data-ttu-id="7a7eb-291">Alla riuscita andare a PL</span><span class="sxs-lookup"><span data-stu-id="7a7eb-291">On success go to PL</span></span></li>
</ul>
<span data-ttu-id="7a7eb-292">Per avere esito negativo: passare a Can</span><span class="sxs-lookup"><span data-stu-id="7a7eb-292">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7a7eb-293">PL</span><span class="sxs-lookup"><span data-stu-id="7a7eb-293">PL</span></span></td>
<td><span data-ttu-id="7a7eb-294">Pull</span><span class="sxs-lookup"><span data-stu-id="7a7eb-294">Pull</span></span></td>
<td><span data-ttu-id="7a7eb-295">Eseguire un pull</span><span class="sxs-lookup"><span data-stu-id="7a7eb-295">Make a pull</span></span>
<ul>
<li><span data-ttu-id="7a7eb-296">In caso di errore Vai alla fine</span><span class="sxs-lookup"><span data-stu-id="7a7eb-296">On failure go to End</span></span></li>
<li><span data-ttu-id="7a7eb-297">Se il completamento è stato completato e sincrono con byte diversi da zero, leggi Vai a PL</span><span class="sxs-lookup"><span data-stu-id="7a7eb-297">On success and synchronous completion with non-zero bytes read go to PL</span></span></li>
<li><span data-ttu-id="7a7eb-298">Al completamento dell'operazione riuscita e sincrona con zero byte letti (pull null) passare a WComp</span><span class="sxs-lookup"><span data-stu-id="7a7eb-298">On success and synchronous completion with zero bytes read (null pull) go to WComp</span></span></li>
<li><span data-ttu-id="7a7eb-299">In seguito all'esito positivo e al completamento asincrono (ERROR_IO_PENDING viene restituito) passare a WPL</span><span class="sxs-lookup"><span data-stu-id="7a7eb-299">On success and asynchronous completion (ERROR_IO_PENDING is returned) go to WPL</span></span></li>
</ul>
<span data-ttu-id="7a7eb-300">Per avere esito negativo: passare a Can</span><span class="sxs-lookup"><span data-stu-id="7a7eb-300">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7a7eb-301">WPL</span><span class="sxs-lookup"><span data-stu-id="7a7eb-301">WPL</span></span></td>
<td><span data-ttu-id="7a7eb-302">Attendi pull</span><span class="sxs-lookup"><span data-stu-id="7a7eb-302">Wait for Pull</span></span></td>
<td><span data-ttu-id="7a7eb-303">Attendi notifica</span><span class="sxs-lookup"><span data-stu-id="7a7eb-303">Wait for notification</span></span>
<ul>
<li><span data-ttu-id="7a7eb-304">In caso di errore per ottenere un completamento, passare a Can</span><span class="sxs-lookup"><span data-stu-id="7a7eb-304">On failure to get a completion go to Can</span></span></li>
<li><span data-ttu-id="7a7eb-305">Se viene ricevuto un errore <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> , passare a Can</span><span class="sxs-lookup"><span data-stu-id="7a7eb-305">If a failure <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> is received go to Can</span></span></li>
<li><span data-ttu-id="7a7eb-306">Se viene ricevuta una <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> con esito positivo con byte diversi da zero, leggi Vai a pl</span><span class="sxs-lookup"><span data-stu-id="7a7eb-306">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> is received with non-zero bytes read go to PL</span></span></li>
<li><span data-ttu-id="7a7eb-307">Se viene ricevuto un <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> con esito positivo con zero byte lettura Vai a comp</span><span class="sxs-lookup"><span data-stu-id="7a7eb-307">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> is received with zero bytes read go to Comp</span></span></li>
<li><span data-ttu-id="7a7eb-308">Se viene ricevuto un errore, Go può</span><span class="sxs-lookup"><span data-stu-id="7a7eb-308">If a failure is received go Can</span></span></li>
</ul>
<span data-ttu-id="7a7eb-309">Per avere esito negativo: passare a Can</span><span class="sxs-lookup"><span data-stu-id="7a7eb-309">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7a7eb-310">Capacità</span><span class="sxs-lookup"><span data-stu-id="7a7eb-310">Can</span></span></td>
<td><span data-ttu-id="7a7eb-311">Annulla la chiamata</span><span class="sxs-lookup"><span data-stu-id="7a7eb-311">Cancel the Call</span></span></td>
<td><span data-ttu-id="7a7eb-312">Chiama <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>RpcAsyncCancelCall</strong></a>Vai a WComp</span><span class="sxs-lookup"><span data-stu-id="7a7eb-312">Call <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>RpcAsyncCancelCall</strong></a>Go to WComp</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7a7eb-313">WComp</span><span class="sxs-lookup"><span data-stu-id="7a7eb-313">WComp</span></span></td>
<td><span data-ttu-id="7a7eb-314">Attendi completamento</span><span class="sxs-lookup"><span data-stu-id="7a7eb-314">Wait for Completion</span></span></td>
<td><span data-ttu-id="7a7eb-315">Attendere la notifica.</span><span class="sxs-lookup"><span data-stu-id="7a7eb-315">Wait for notification.</span></span> <span data-ttu-id="7a7eb-316">È necessario ricevere una notifica CallComplete.</span><span class="sxs-lookup"><span data-stu-id="7a7eb-316">CallComplete notification should be received.</span></span><br/> <span data-ttu-id="7a7eb-317">Vai a comp</span><span class="sxs-lookup"><span data-stu-id="7a7eb-317">Go to Comp</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7a7eb-318">Comp</span><span class="sxs-lookup"><span data-stu-id="7a7eb-318">Comp</span></span></td>
<td><span data-ttu-id="7a7eb-319">Completion</span><span class="sxs-lookup"><span data-stu-id="7a7eb-319">Completion</span></span></td>
<td><span data-ttu-id="7a7eb-320">Problema <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>Vai alla fine</span><span class="sxs-lookup"><span data-stu-id="7a7eb-320">Issue <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>Go to End</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7a7eb-321">Fine</span><span class="sxs-lookup"><span data-stu-id="7a7eb-321">End</span></span></td>


</tr>
</tbody>
</table>



 

<span data-ttu-id="7a7eb-322">Comportamento del server</span><span class="sxs-lookup"><span data-stu-id="7a7eb-322">Server Behavior</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7a7eb-323">State</span><span class="sxs-lookup"><span data-stu-id="7a7eb-323">State</span></span></th>
<th><span data-ttu-id="7a7eb-324">State Name</span><span class="sxs-lookup"><span data-stu-id="7a7eb-324">State Name</span></span></th>
<th><span data-ttu-id="7a7eb-325">Azione</span><span class="sxs-lookup"><span data-stu-id="7a7eb-325">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7a7eb-326">D</span><span class="sxs-lookup"><span data-stu-id="7a7eb-326">D</span></span></td>
<td><span data-ttu-id="7a7eb-327">Dispatch</span><span class="sxs-lookup"><span data-stu-id="7a7eb-327">Dispatch</span></span></td>
<td><span data-ttu-id="7a7eb-328">La chiamata viene inviata dal runtimeGo RPC a PL</span><span class="sxs-lookup"><span data-stu-id="7a7eb-328">The call is dispatched by the RPC runtimeGo to PL</span></span><br/> <span data-ttu-id="7a7eb-329">Per avere esito negativo (durante l'esecuzione sul thread RPC): Genera eccezione; Vai alla fine</span><span class="sxs-lookup"><span data-stu-id="7a7eb-329">To fail fatally (while executing on the RPC thread): Raise exception; go to End</span></span><br/> <span data-ttu-id="7a7eb-330">Per eseguire correttamente l'errore: passare a un</span><span class="sxs-lookup"><span data-stu-id="7a7eb-330">To fail gracefully: Go to A</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7a7eb-331">PL</span><span class="sxs-lookup"><span data-stu-id="7a7eb-331">PL</span></span></td>
<td><span data-ttu-id="7a7eb-332">Pull</span><span class="sxs-lookup"><span data-stu-id="7a7eb-332">Pull</span></span></td>
<td><span data-ttu-id="7a7eb-333">Eseguire un pull</span><span class="sxs-lookup"><span data-stu-id="7a7eb-333">Make a pull</span></span>
<ul>
<li><span data-ttu-id="7a7eb-334">In caso di errore Vai alla fine</span><span class="sxs-lookup"><span data-stu-id="7a7eb-334">On failure go to End</span></span></li>
<li><span data-ttu-id="7a7eb-335">Se il completamento è stato completato e sincrono con byte diversi da zero, leggi Vai a PL</span><span class="sxs-lookup"><span data-stu-id="7a7eb-335">On success and synchronous completion with non-zero bytes read go to PL</span></span></li>
<li><span data-ttu-id="7a7eb-336">Al completamento dell'operazione riuscita e sincrona con zero byte letti (pull null) andare a PS</span><span class="sxs-lookup"><span data-stu-id="7a7eb-336">On success and synchronous completion with zero bytes read (null pull) go to PS</span></span></li>
<li><span data-ttu-id="7a7eb-337">In seguito all'esito positivo e al completamento asincrono (ERROR_IO_PENDING viene restituito) passare a WPL</span><span class="sxs-lookup"><span data-stu-id="7a7eb-337">On success and asynchronous completion (ERROR_IO_PENDING is returned) go to WPL</span></span></li>
</ul>
<span data-ttu-id="7a7eb-338">Per avere esito negativo: passare a un</span><span class="sxs-lookup"><span data-stu-id="7a7eb-338">To fail: go to A</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7a7eb-339">WPL</span><span class="sxs-lookup"><span data-stu-id="7a7eb-339">WPL</span></span></td>
<td><span data-ttu-id="7a7eb-340">Attendi pull</span><span class="sxs-lookup"><span data-stu-id="7a7eb-340">Wait for Pull</span></span></td>
<td><span data-ttu-id="7a7eb-341">Attendi notifica</span><span class="sxs-lookup"><span data-stu-id="7a7eb-341">Wait for notification</span></span>
<ul>
<li><span data-ttu-id="7a7eb-342">In caso di errore per ottenere un completamento, passare a</span><span class="sxs-lookup"><span data-stu-id="7a7eb-342">On failure to get a completion go to A</span></span></li>
<li><span data-ttu-id="7a7eb-343">Se viene ricevuto un errore <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> , passare a un</span><span class="sxs-lookup"><span data-stu-id="7a7eb-343">If a failure <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> is received go to A</span></span></li>
<li><span data-ttu-id="7a7eb-344">Se viene ricevuta una <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> con esito positivo con byte diversi da zero, leggi Vai a pl</span><span class="sxs-lookup"><span data-stu-id="7a7eb-344">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> is received with non-zero bytes read go to PL</span></span></li>
<li><span data-ttu-id="7a7eb-345">Se viene ricevuto un <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> con esito positivo con zero byte letti, vai a PS</span><span class="sxs-lookup"><span data-stu-id="7a7eb-345">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> is received with zero bytes read go to PS</span></span></li>
<li><span data-ttu-id="7a7eb-346">Se viene ricevuto un errore, passare A</span><span class="sxs-lookup"><span data-stu-id="7a7eb-346">If a failure is received go A</span></span></li>
</ul>
<span data-ttu-id="7a7eb-347">Per avere esito negativo: passare a un</span><span class="sxs-lookup"><span data-stu-id="7a7eb-347">To fail: go to A</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7a7eb-348">PS</span><span class="sxs-lookup"><span data-stu-id="7a7eb-348">PS</span></span></td>
<td><span data-ttu-id="7a7eb-349">Push</span><span class="sxs-lookup"><span data-stu-id="7a7eb-349">Push</span></span></td>
<td><span data-ttu-id="7a7eb-350">Eseguire un push</span><span class="sxs-lookup"><span data-stu-id="7a7eb-350">Make a push</span></span>
<ul>
<li><span data-ttu-id="7a7eb-351">In riuscita passare a WPS</span><span class="sxs-lookup"><span data-stu-id="7a7eb-351">On success go to WPS</span></span></li>
<li><span data-ttu-id="7a7eb-352">In caso di errore Vai alla fine</span><span class="sxs-lookup"><span data-stu-id="7a7eb-352">On failure go to End</span></span></li>
</ul>
<span data-ttu-id="7a7eb-353">Per avere esito negativo: passare a un</span><span class="sxs-lookup"><span data-stu-id="7a7eb-353">To fail: go to A</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7a7eb-354">WPS</span><span class="sxs-lookup"><span data-stu-id="7a7eb-354">WPS</span></span></td>
<td><span data-ttu-id="7a7eb-355">Attendi push</span><span class="sxs-lookup"><span data-stu-id="7a7eb-355">Wait for Push</span></span></td>
<td><span data-ttu-id="7a7eb-356">Attendi notifica</span><span class="sxs-lookup"><span data-stu-id="7a7eb-356">Wait for notification</span></span>
<ul>
<li><span data-ttu-id="7a7eb-357">In caso di errore per ottenere un completamento, passare a</span><span class="sxs-lookup"><span data-stu-id="7a7eb-357">On failure to get a completion go to A</span></span></li>
<li><span data-ttu-id="7a7eb-358">Se viene ricevuto un <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> di esito positivo ed è necessario inviare più dati, passare a PS</span><span class="sxs-lookup"><span data-stu-id="7a7eb-358">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> is received and more data needs to be sent go to PS</span></span></li>
<li><span data-ttu-id="7a7eb-359">Se viene ricevuta una <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> con esito positivo e non è necessario inviare più dati, passare a NP</span><span class="sxs-lookup"><span data-stu-id="7a7eb-359">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> is received and more data does not need to be sent go to NP</span></span></li>
<li><span data-ttu-id="7a7eb-360">Se viene ricevuto un errore go comp</span><span class="sxs-lookup"><span data-stu-id="7a7eb-360">If a failure is received go Comp</span></span></li>
</ul>
<span data-ttu-id="7a7eb-361">Per avere esito negativo: passare a un</span><span class="sxs-lookup"><span data-stu-id="7a7eb-361">To fail: go to A</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7a7eb-362">NP</span><span class="sxs-lookup"><span data-stu-id="7a7eb-362">NP</span></span></td>
<td><span data-ttu-id="7a7eb-363">Push null</span><span class="sxs-lookup"><span data-stu-id="7a7eb-363">Null Push</span></span></td>
<td><span data-ttu-id="7a7eb-364">Push 0 byte</span><span class="sxs-lookup"><span data-stu-id="7a7eb-364">Push 0 bytes</span></span>
<ul>
<li><span data-ttu-id="7a7eb-365">in riuscita andare a WNP</span><span class="sxs-lookup"><span data-stu-id="7a7eb-365">on success go to WNP</span></span></li>
<li><span data-ttu-id="7a7eb-366">in caso di errore Vai a comp</span><span class="sxs-lookup"><span data-stu-id="7a7eb-366">on failure go to Comp</span></span></li>
</ul>
<span data-ttu-id="7a7eb-367">Per avere esito negativo: passare a un</span><span class="sxs-lookup"><span data-stu-id="7a7eb-367">To fail: go to A</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7a7eb-368">WNP</span><span class="sxs-lookup"><span data-stu-id="7a7eb-368">WNP</span></span></td>
<td><span data-ttu-id="7a7eb-369">Attendi push null</span><span class="sxs-lookup"><span data-stu-id="7a7eb-369">Wait for Null Push</span></span></td>
<td><span data-ttu-id="7a7eb-370">Attendi notifica</span><span class="sxs-lookup"><span data-stu-id="7a7eb-370">Wait for notification</span></span>
<ul>
<li><span data-ttu-id="7a7eb-371">In caso di errore per ottenere un completamento, passare a</span><span class="sxs-lookup"><span data-stu-id="7a7eb-371">On failure to get a completion go to A</span></span></li>
<li><span data-ttu-id="7a7eb-372">Se viene ricevuto un errore go comp</span><span class="sxs-lookup"><span data-stu-id="7a7eb-372">If a failure is received go Comp</span></span></li>
<li><span data-ttu-id="7a7eb-373">Se viene ricevuta una riuscita, vai comp</span><span class="sxs-lookup"><span data-stu-id="7a7eb-373">If a success is received go Comp</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7a7eb-374">A</span><span class="sxs-lookup"><span data-stu-id="7a7eb-374">A</span></span></td>
<td><span data-ttu-id="7a7eb-375">Interrompi la chiamata</span><span class="sxs-lookup"><span data-stu-id="7a7eb-375">Abort the Call</span></span></td>
<td><span data-ttu-id="7a7eb-376">Chiama <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall"><strong>RpcAsyncAbortCall</strong></a>; Vai alla fine</span><span class="sxs-lookup"><span data-stu-id="7a7eb-376">Call <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall"><strong>RpcAsyncAbortCall</strong></a>; go to End</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7a7eb-377">Comp</span><span class="sxs-lookup"><span data-stu-id="7a7eb-377">Comp</span></span></td>
<td><span data-ttu-id="7a7eb-378">Completion</span><span class="sxs-lookup"><span data-stu-id="7a7eb-378">Completion</span></span></td>
<td><span data-ttu-id="7a7eb-379">Problema <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>; Vai alla fine</span><span class="sxs-lookup"><span data-stu-id="7a7eb-379">Issue <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>; go to End</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7a7eb-380">Fine</span><span class="sxs-lookup"><span data-stu-id="7a7eb-380">End</span></span></td>


</tr>
</tbody>
</table>



 

 

 





