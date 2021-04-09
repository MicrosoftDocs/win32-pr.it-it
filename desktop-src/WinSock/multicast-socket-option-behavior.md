---
description: Questa pagina descrive il comportamento delle opzioni dei socket multicast basate su diversi Stati delle impostazioni delle opzioni del socket.
ms.assetid: a411e831-7b28-4ab5-a09a-650db99a7cd5
title: Comportamento dell'opzione socket multicast
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fd10094750bea59b844ad1fcdac70be0c7f9646
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049482"
---
# <a name="multicast-socket-option-behavior"></a><span data-ttu-id="d5d5f-103">Comportamento dell'opzione socket multicast</span><span class="sxs-lookup"><span data-stu-id="d5d5f-103">Multicast Socket Option Behavior</span></span>

<span data-ttu-id="d5d5f-104">Questa pagina descrive il comportamento delle opzioni dei socket multicast basate su diversi Stati delle impostazioni delle opzioni del socket.</span><span class="sxs-lookup"><span data-stu-id="d5d5f-104">This page describes the behavior of multicast socket options based on various socket option settings states.</span></span>

<span data-ttu-id="d5d5f-105">Ad esempio, in questa pagina viene descritto il comportamento quando \_ l' \_ opzione IP Aggiungi origine \_ socket è impostata su un socket per il quale \_ è \_ già stata impostata l'opzione di appartenenza all'origine IP Aggiungi \_ con la coppia gruppo/origine specificata nella stessa interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="d5d5f-105">For example, this page describes the behavior when the IP\_ADD\_SOURCE\_MEMBERSHIP socket option is set on a socket for which the IP\_ADD\_SOURCE\_MEMBERSHIP option has already been set with the specified group/source pair on the same network interface.</span></span> <span data-ttu-id="d5d5f-106">È consentito chiamare l'appartenenza all' \_ origine IP Aggiungi nello \_ \_ stesso gruppo in un'interfaccia di rete diversa.</span><span class="sxs-lookup"><span data-stu-id="d5d5f-106">It is permitted to call IP\_ADD\_SOURCE\_MEMBERSHIP on the same group on a different network interface.</span></span>

<span data-ttu-id="d5d5f-107">Questa pagina supporta la progettazione e la risoluzione dei problemi delle applicazioni multicast Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="d5d5f-107">This page assists in properly designing and troubleshooting Windows Sockets multicast applications.</span></span> 

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="d5d5f-108">Opzione socket iniziale</span><span class="sxs-lookup"><span data-stu-id="d5d5f-108">Initial socket option</span></span></th>
<th><span data-ttu-id="d5d5f-109">Opzione socket successiva in conflitto</span><span class="sxs-lookup"><span data-stu-id="d5d5f-109">Conflicting subsequent socket option</span></span></th>
<th><span data-ttu-id="d5d5f-110">Errore restituito</span><span class="sxs-lookup"><span data-stu-id="d5d5f-110">Error returned</span></span></th>
<th><span data-ttu-id="d5d5f-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="d5d5f-111">Remarks</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="4"><span data-ttu-id="d5d5f-112">IP_ADD_MEMBERSHIP $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="d5d5f-112">IP_ADD_MEMBERSHIP${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="d5d5f-113">IP_ADD_MEMBERSHIP</span><span class="sxs-lookup"><span data-stu-id="d5d5f-113">IP_ADD_MEMBERSHIP</span></span></td>
<td><span data-ttu-id="d5d5f-114">WSAEADDRNOTAVAIL</span><span class="sxs-lookup"><span data-stu-id="d5d5f-114">WSAEADDRNOTAVAIL</span></span></td>
<td><span data-ttu-id="d5d5f-115">Non chiamare IP_ADD_MEMBERSHIP con lo stesso gruppo più di una volta nella stessa interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="d5d5f-115">Do not call IP_ADD_MEMBERSHIP with the same group more than once on the same network interface.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d5d5f-116">IP_ADD_SOURCE_MEMBERSHIP</span><span class="sxs-lookup"><span data-stu-id="d5d5f-116">IP_ADD_SOURCE_MEMBERSHIP</span></span></td>
<td><span data-ttu-id="d5d5f-117">WSAEADDRNOTAVAIL</span><span class="sxs-lookup"><span data-stu-id="d5d5f-117">WSAEADDRNOTAVAIL</span></span></td>
<td><span data-ttu-id="d5d5f-118">Non chiamare IP_ADD_SOURCE_MEMBERSHIP con lo stesso gruppo precedentemente chiamato con IP_ADD_MEMBERSHIP nella stessa interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="d5d5f-118">Do not call IP_ADD_SOURCE_MEMBERSHIP with the same group previously called with IP_ADD_MEMBERSHIP on the same network interface.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="d5d5f-119">IP_DROP_SOURCE_MEMBERSHIP</span><span class="sxs-lookup"><span data-stu-id="d5d5f-119">IP_DROP_SOURCE_MEMBERSHIP</span></span></td>
<td><span data-ttu-id="d5d5f-120">WSAEINVAL</span><span class="sxs-lookup"><span data-stu-id="d5d5f-120">WSAEINVAL</span></span></td>
<td><span data-ttu-id="d5d5f-121">In alternativa, usare IP_BLOCK_SOURCE.</span><span class="sxs-lookup"><span data-stu-id="d5d5f-121">Use IP_BLOCK_SOURCE instead.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="d5d5f-122">IP_UNBLOCK_SOURCE</span><span class="sxs-lookup"><span data-stu-id="d5d5f-122">IP_UNBLOCK_SOURCE</span></span></td>
<td><span data-ttu-id="d5d5f-123">WSAEINVAL</span><span class="sxs-lookup"><span data-stu-id="d5d5f-123">WSAEINVAL</span></span></td>
<td><span data-ttu-id="d5d5f-124">Restituisce un errore quando si tenta di sbloccare una coppia gruppo/origine che non è stata precedentemente bloccata nella stessa interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="d5d5f-124">Returns an error when attempting to unblock a group/source pair that has not previously been blocked on the same network interface.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="d5d5f-125">IP_DROP_MEMBERSHIP</span><span class="sxs-lookup"><span data-stu-id="d5d5f-125">IP_DROP_MEMBERSHIP</span></span></td>
<td><span data-ttu-id="d5d5f-126">Qualsiasi chiamata successiva sulla stessa coppia gruppo/gruppo/origine</span><span class="sxs-lookup"><span data-stu-id="d5d5f-126">Any subsequent call on the same group or group/source pair</span></span></td>
<td><span data-ttu-id="d5d5f-127">WSAEINVAL</span><span class="sxs-lookup"><span data-stu-id="d5d5f-127">WSAEINVAL</span></span></td>
<td><span data-ttu-id="d5d5f-128">L'esecuzione di chiamate di opzioni socket su una coppia gruppo o gruppo/origine non attualmente presente nell'elenco di inclusione (a causa della rimozione dell'appartenenza o in caso contrario) genera un errore.</span><span class="sxs-lookup"><span data-stu-id="d5d5f-128">Making socket option calls on a group or group/source pair not currently in the inclusion list (due to dropping membership, or otherwise) results in an error.</span></span></td>
</tr>
<tr class="even">
<td rowspan="3"><span data-ttu-id="d5d5f-129">IP_ADD_SOURCE_MEMBERSHIP $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="d5d5f-129">IP_ADD_SOURCE_MEMBERSHIP${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="d5d5f-130">IP_ADD_MEMBERSHIP</span><span class="sxs-lookup"><span data-stu-id="d5d5f-130">IP_ADD_MEMBERSHIP</span></span></td>
<td><span data-ttu-id="d5d5f-131">WSAEADDRNOTAVAIL</span><span class="sxs-lookup"><span data-stu-id="d5d5f-131">WSAEADDRNOTAVAIL</span></span></td>
<td><span data-ttu-id="d5d5f-132">Non chiamare IP_ADD_MEMBERSHIP con lo stesso gruppo precedentemente chiamato con IP_ADD_SOURCE_MEMBERSHIP nella stessa interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="d5d5f-132">Do not call IP_ADD_MEMBERSHIP with the same group previously called with IP_ADD_SOURCE_MEMBERSHIP on the same network interface.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d5d5f-133">IP_ADD_SOURCE_MEMBERSHIP</span><span class="sxs-lookup"><span data-stu-id="d5d5f-133">IP_ADD_SOURCE_MEMBERSHIP</span></span></td>
<td><span data-ttu-id="d5d5f-134">WSAEADDRNOTAVAIL</span><span class="sxs-lookup"><span data-stu-id="d5d5f-134">WSAEADDRNOTAVAIL</span></span></td>
<td><span data-ttu-id="d5d5f-135">Non chiamare IP_ADD_SOURCE_MEMBERSHIP con la stessa coppia gruppo/origine chiamata in precedenza con IP_ADD_SOURCE_MEMBERSHIP nella stessa interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="d5d5f-135">Do not call IP_ADD_SOURCE_MEMBERSHIP with the same group/source pair previously called with IP_ADD_SOURCE_MEMBERSHIP on the same network interface.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="d5d5f-136">IP_UNBLOCK_SOURCE</span><span class="sxs-lookup"><span data-stu-id="d5d5f-136">IP_UNBLOCK_SOURCE</span></span></td>
<td><span data-ttu-id="d5d5f-137">WSAEINVAL</span><span class="sxs-lookup"><span data-stu-id="d5d5f-137">WSAEINVAL</span></span></td>
<td><span data-ttu-id="d5d5f-138">Restituisce un errore quando si tenta di sbloccare una coppia gruppo/origine che non è stata precedentemente bloccata nella stessa interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="d5d5f-138">Returns an error when attempting to unblock a group/source pair that has not previously been blocked on the same network interface.</span></span></td>

</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="d5d5f-139">IP_DROP_SOURCE_MEMBERSHIP $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="d5d5f-139">IP_DROP_SOURCE_MEMBERSHIP${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="d5d5f-140">IP_UNBLOCK_SOURCE</span><span class="sxs-lookup"><span data-stu-id="d5d5f-140">IP_UNBLOCK_SOURCE</span></span></td>
<td><span data-ttu-id="d5d5f-141">WSAEINVAL</span><span class="sxs-lookup"><span data-stu-id="d5d5f-141">WSAEINVAL</span></span></td>
<td><span data-ttu-id="d5d5f-142">Restituisce un errore quando si tenta di sbloccare una coppia gruppo/origine che non è stata precedentemente bloccata nella stessa interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="d5d5f-142">Returns an error when attempting to unblock a group/source pair that has not previously been blocked on the same network interface.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d5d5f-143">IP_DROP_SOURCE_MEMBERSHIP</span><span class="sxs-lookup"><span data-stu-id="d5d5f-143">IP_DROP_SOURCE_MEMBERSHIP</span></span></td>
<td><span data-ttu-id="d5d5f-144">WSAEADDRNOTAVAIL</span><span class="sxs-lookup"><span data-stu-id="d5d5f-144">WSAEADDRNOTAVAIL</span></span></td>
<td><span data-ttu-id="d5d5f-145">Restituisce un errore quando si tenta di eliminare una coppia gruppo/origine che non è presente nell'elenco di inclusione nella stessa interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="d5d5f-145">Returns an error when attempting to drop a group/source pair that is not in the inclusion list on the same network interface.</span></span></td>

</tr>
<tr class="odd">
<td rowspan="3"><span data-ttu-id="d5d5f-146">IP_BLOCK_SOURCE $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="d5d5f-146">IP_BLOCK_SOURCE${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="d5d5f-147">IP_BLOCK_SOURCE</span><span class="sxs-lookup"><span data-stu-id="d5d5f-147">IP_BLOCK_SOURCE</span></span></td>
<td><span data-ttu-id="d5d5f-148">WSAEADDRNOTAVAIL</span><span class="sxs-lookup"><span data-stu-id="d5d5f-148">WSAEADDRNOTAVAIL</span></span></td>
<td><span data-ttu-id="d5d5f-149">Restituisce un errore quando si tenta di bloccare una coppia gruppo/origine che è già bloccata nella stessa interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="d5d5f-149">Returns an error when attempting to block a group/source pair that is already blocked on the same network interface.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d5d5f-150">IP_ADD_SOURCE_MEMBERSHIP</span><span class="sxs-lookup"><span data-stu-id="d5d5f-150">IP_ADD_SOURCE_MEMBERSHIP</span></span></td>
<td><span data-ttu-id="d5d5f-151">WSAEINVAL</span><span class="sxs-lookup"><span data-stu-id="d5d5f-151">WSAEINVAL</span></span></td>
<td><span data-ttu-id="d5d5f-152">In alternativa, usare IP_UNBLOCK_SOURCE.</span><span class="sxs-lookup"><span data-stu-id="d5d5f-152">Use IP_UNBLOCK_SOURCE instead.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="d5d5f-153">IP_ADD_MEMBERSHIP</span><span class="sxs-lookup"><span data-stu-id="d5d5f-153">IP_ADD_MEMBERSHIP</span></span></td>
<td><span data-ttu-id="d5d5f-154">WSAEINVAL</span><span class="sxs-lookup"><span data-stu-id="d5d5f-154">WSAEINVAL</span></span></td>
<td><span data-ttu-id="d5d5f-155">In alternativa, usare IP_UNBLOCK_SOURCE.</span><span class="sxs-lookup"><span data-stu-id="d5d5f-155">Use IP_UNBLOCK_SOURCE instead.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="d5d5f-156">IP_UNBLOCK_SOURCE</span><span class="sxs-lookup"><span data-stu-id="d5d5f-156">IP_UNBLOCK_SOURCE</span></span></td>
<td><span data-ttu-id="d5d5f-157">IP_UNBLOCK_SOURCE</span><span class="sxs-lookup"><span data-stu-id="d5d5f-157">IP_UNBLOCK_SOURCE</span></span></td>
<td><span data-ttu-id="d5d5f-158">WSAEADDRNOTAVAIL</span><span class="sxs-lookup"><span data-stu-id="d5d5f-158">WSAEADDRNOTAVAIL</span></span></td>
<td><span data-ttu-id="d5d5f-159">Restituisce un errore quando si tenta di sbloccare una coppia gruppo/origine che non è presente nell'elenco bloccato nella stessa interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="d5d5f-159">Returns an error when attempting to unblock a group/source pair that is not in the blocked list on the same network interface.</span></span></td>
</tr>
</tbody>
</table>



 

 

 



