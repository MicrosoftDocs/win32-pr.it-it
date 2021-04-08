---
title: Attributo MSMQ-out-routing-Servers
description: DN si collega ai server di routing MSMQ attraverso i quali deve essere indirizzato tutto il traffico in uscita per questo computer.
ms.assetid: 169558e4-d2a6-4555-bc5f-7e6a89e51789
ms.tgt_platform: multiple
keywords:
- Schema di AD per l'attributo MSMQ-out-routing-Servers
- Schema AD dell'attributo mSMQOutRoutingServers
topic_type:
- apiref
api_name:
- MSMQ-Out-Routing-Servers
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfc2265b2d809b7a73cd19faace87473552471a3
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103875318"
---
# <a name="msmq-out-routing-servers-attribute"></a><span data-ttu-id="2e4c8-105">Attributo MSMQ-out-routing-Servers</span><span class="sxs-lookup"><span data-stu-id="2e4c8-105">MSMQ-Out-Routing-Servers attribute</span></span>

<span data-ttu-id="2e4c8-106">DN si collega ai server di routing MSMQ attraverso i quali deve essere indirizzato tutto il traffico in uscita per questo computer.</span><span class="sxs-lookup"><span data-stu-id="2e4c8-106">DN links to MSMQ routing servers through which all outgoing traffic for this computer should be routed.</span></span>



| <span data-ttu-id="2e4c8-107">Voce</span><span class="sxs-lookup"><span data-stu-id="2e4c8-107">Entry</span></span> | <span data-ttu-id="2e4c8-108">Valore</span><span class="sxs-lookup"><span data-stu-id="2e4c8-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="2e4c8-109">CN</span><span class="sxs-lookup"><span data-stu-id="2e4c8-109">CN</span></span>                | <span data-ttu-id="2e4c8-110">MSMQ-out-routing-server</span><span class="sxs-lookup"><span data-stu-id="2e4c8-110">MSMQ-Out-Routing-Servers</span></span>                |
| <span data-ttu-id="2e4c8-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="2e4c8-111">Ldap-Display-Name</span></span> | <span data-ttu-id="2e4c8-112">mSMQOutRoutingServers</span><span class="sxs-lookup"><span data-stu-id="2e4c8-112">mSMQOutRoutingServers</span></span>                   |
| <span data-ttu-id="2e4c8-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="2e4c8-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="2e4c8-114">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="2e4c8-114">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="2e4c8-115">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="2e4c8-115">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="2e4c8-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="2e4c8-116">Attribute-Id</span></span>      | <span data-ttu-id="2e4c8-117">1.2.840.113556.1.4.928</span><span class="sxs-lookup"><span data-stu-id="2e4c8-117">1.2.840.113556.1.4.928</span></span>                  |
| <span data-ttu-id="2e4c8-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="2e4c8-118">System-Id-Guid</span></span>    | <span data-ttu-id="2e4c8-119">9a0dc32b-c100-11d1-bbc5-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="2e4c8-119">9a0dc32b-c100-11d1-bbc5-0080c76670c0</span></span>    |
| <span data-ttu-id="2e4c8-120">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2e4c8-120">Syntax</span></span>            | [<span data-ttu-id="2e4c8-121">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="2e4c8-121">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="2e4c8-122">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="2e4c8-122">Implementations</span></span>

-   [<span data-ttu-id="2e4c8-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="2e4c8-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="2e4c8-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="2e4c8-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="2e4c8-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="2e4c8-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="2e4c8-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="2e4c8-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="2e4c8-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="2e4c8-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="2e4c8-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="2e4c8-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="2e4c8-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2e4c8-129">Windows 2000 Server</span></span>



| <span data-ttu-id="2e4c8-130">Voce</span><span class="sxs-lookup"><span data-stu-id="2e4c8-130">Entry</span></span> | <span data-ttu-id="2e4c8-131">Valore</span><span class="sxs-lookup"><span data-stu-id="2e4c8-131">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="2e4c8-132">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="2e4c8-132">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="2e4c8-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2e4c8-133">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="2e4c8-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="2e4c8-134">System-Only</span></span>            | <span data-ttu-id="2e4c8-135">Falso</span><span class="sxs-lookup"><span data-stu-id="2e4c8-135">False</span></span>                                                        |
| <span data-ttu-id="2e4c8-136">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="2e4c8-136">Is-Single-Valued</span></span>       | <span data-ttu-id="2e4c8-137">Falso</span><span class="sxs-lookup"><span data-stu-id="2e4c8-137">False</span></span>                                                        |
| <span data-ttu-id="2e4c8-138">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="2e4c8-138">Is Indexed</span></span>             | <span data-ttu-id="2e4c8-139">Falso</span><span class="sxs-lookup"><span data-stu-id="2e4c8-139">False</span></span>                                                        |
| <span data-ttu-id="2e4c8-140">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="2e4c8-140">In Global Catalog</span></span>      | <span data-ttu-id="2e4c8-141">Vero</span><span class="sxs-lookup"><span data-stu-id="2e4c8-141">True</span></span>                                                         |
| <span data-ttu-id="2e4c8-142">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="2e4c8-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="2e4c8-143">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="2e4c8-143">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="2e4c8-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2e4c8-144">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="2e4c8-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2e4c8-145">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="2e4c8-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2e4c8-146">Search-Flags</span></span>           | <span data-ttu-id="2e4c8-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2e4c8-147">0x00000000</span></span>                                                   |
| <span data-ttu-id="2e4c8-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2e4c8-148">System-Flags</span></span>           | <span data-ttu-id="2e4c8-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2e4c8-149">0x00000010</span></span>                                                   |
| <span data-ttu-id="2e4c8-150">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="2e4c8-150">Classes used in</span></span>        | [<span data-ttu-id="2e4c8-151">**Configurazione MSMQ**</span><span class="sxs-lookup"><span data-stu-id="2e4c8-151">**MSMQ-Configuration**</span></span>](c-msmqconfiguration.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="2e4c8-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2e4c8-152">Windows Server 2003</span></span>



| <span data-ttu-id="2e4c8-153">Voce</span><span class="sxs-lookup"><span data-stu-id="2e4c8-153">Entry</span></span> | <span data-ttu-id="2e4c8-154">Valore</span><span class="sxs-lookup"><span data-stu-id="2e4c8-154">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="2e4c8-155">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="2e4c8-155">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="2e4c8-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2e4c8-156">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="2e4c8-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="2e4c8-157">System-Only</span></span>            | <span data-ttu-id="2e4c8-158">Falso</span><span class="sxs-lookup"><span data-stu-id="2e4c8-158">False</span></span>                                                        |
| <span data-ttu-id="2e4c8-159">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="2e4c8-159">Is-Single-Valued</span></span>       | <span data-ttu-id="2e4c8-160">Falso</span><span class="sxs-lookup"><span data-stu-id="2e4c8-160">False</span></span>                                                        |
| <span data-ttu-id="2e4c8-161">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="2e4c8-161">Is Indexed</span></span>             | <span data-ttu-id="2e4c8-162">Falso</span><span class="sxs-lookup"><span data-stu-id="2e4c8-162">False</span></span>                                                        |
| <span data-ttu-id="2e4c8-163">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="2e4c8-163">In Global Catalog</span></span>      | <span data-ttu-id="2e4c8-164">Vero</span><span class="sxs-lookup"><span data-stu-id="2e4c8-164">True</span></span>                                                         |
| <span data-ttu-id="2e4c8-165">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="2e4c8-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="2e4c8-166">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="2e4c8-166">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="2e4c8-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2e4c8-167">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="2e4c8-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2e4c8-168">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="2e4c8-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2e4c8-169">Search-Flags</span></span>           | <span data-ttu-id="2e4c8-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2e4c8-170">0x00000000</span></span>                                                   |
| <span data-ttu-id="2e4c8-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2e4c8-171">System-Flags</span></span>           | <span data-ttu-id="2e4c8-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2e4c8-172">0x00000010</span></span>                                                   |
| <span data-ttu-id="2e4c8-173">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="2e4c8-173">Classes used in</span></span>        | [<span data-ttu-id="2e4c8-174">**Configurazione MSMQ**</span><span class="sxs-lookup"><span data-stu-id="2e4c8-174">**MSMQ-Configuration**</span></span>](c-msmqconfiguration.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="2e4c8-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="2e4c8-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="2e4c8-176">Voce</span><span class="sxs-lookup"><span data-stu-id="2e4c8-176">Entry</span></span> | <span data-ttu-id="2e4c8-177">Valore</span><span class="sxs-lookup"><span data-stu-id="2e4c8-177">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="2e4c8-178">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="2e4c8-178">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="2e4c8-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2e4c8-179">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="2e4c8-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="2e4c8-180">System-Only</span></span>            | <span data-ttu-id="2e4c8-181">Falso</span><span class="sxs-lookup"><span data-stu-id="2e4c8-181">False</span></span>                                                        |
| <span data-ttu-id="2e4c8-182">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="2e4c8-182">Is-Single-Valued</span></span>       | <span data-ttu-id="2e4c8-183">Falso</span><span class="sxs-lookup"><span data-stu-id="2e4c8-183">False</span></span>                                                        |
| <span data-ttu-id="2e4c8-184">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="2e4c8-184">Is Indexed</span></span>             | <span data-ttu-id="2e4c8-185">Falso</span><span class="sxs-lookup"><span data-stu-id="2e4c8-185">False</span></span>                                                        |
| <span data-ttu-id="2e4c8-186">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="2e4c8-186">In Global Catalog</span></span>      | <span data-ttu-id="2e4c8-187">Vero</span><span class="sxs-lookup"><span data-stu-id="2e4c8-187">True</span></span>                                                         |
| <span data-ttu-id="2e4c8-188">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="2e4c8-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="2e4c8-189">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="2e4c8-189">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="2e4c8-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2e4c8-190">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="2e4c8-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2e4c8-191">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="2e4c8-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2e4c8-192">Search-Flags</span></span>           | <span data-ttu-id="2e4c8-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2e4c8-193">0x00000000</span></span>                                                   |
| <span data-ttu-id="2e4c8-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2e4c8-194">System-Flags</span></span>           | <span data-ttu-id="2e4c8-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2e4c8-195">0x00000010</span></span>                                                   |
| <span data-ttu-id="2e4c8-196">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="2e4c8-196">Classes used in</span></span>        | [<span data-ttu-id="2e4c8-197">**Configurazione MSMQ**</span><span class="sxs-lookup"><span data-stu-id="2e4c8-197">**MSMQ-Configuration**</span></span>](c-msmqconfiguration.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="2e4c8-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2e4c8-198">Windows Server 2008</span></span>



| <span data-ttu-id="2e4c8-199">Voce</span><span class="sxs-lookup"><span data-stu-id="2e4c8-199">Entry</span></span> | <span data-ttu-id="2e4c8-200">Valore</span><span class="sxs-lookup"><span data-stu-id="2e4c8-200">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="2e4c8-201">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="2e4c8-201">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="2e4c8-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2e4c8-202">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="2e4c8-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="2e4c8-203">System-Only</span></span>            | <span data-ttu-id="2e4c8-204">Falso</span><span class="sxs-lookup"><span data-stu-id="2e4c8-204">False</span></span>                                                        |
| <span data-ttu-id="2e4c8-205">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="2e4c8-205">Is-Single-Valued</span></span>       | <span data-ttu-id="2e4c8-206">Falso</span><span class="sxs-lookup"><span data-stu-id="2e4c8-206">False</span></span>                                                        |
| <span data-ttu-id="2e4c8-207">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="2e4c8-207">Is Indexed</span></span>             | <span data-ttu-id="2e4c8-208">Falso</span><span class="sxs-lookup"><span data-stu-id="2e4c8-208">False</span></span>                                                        |
| <span data-ttu-id="2e4c8-209">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="2e4c8-209">In Global Catalog</span></span>      | <span data-ttu-id="2e4c8-210">Vero</span><span class="sxs-lookup"><span data-stu-id="2e4c8-210">True</span></span>                                                         |
| <span data-ttu-id="2e4c8-211">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="2e4c8-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="2e4c8-212">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="2e4c8-212">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="2e4c8-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2e4c8-213">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="2e4c8-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2e4c8-214">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="2e4c8-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2e4c8-215">Search-Flags</span></span>           | <span data-ttu-id="2e4c8-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2e4c8-216">0x00000000</span></span>                                                   |
| <span data-ttu-id="2e4c8-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2e4c8-217">System-Flags</span></span>           | <span data-ttu-id="2e4c8-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2e4c8-218">0x00000010</span></span>                                                   |
| <span data-ttu-id="2e4c8-219">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="2e4c8-219">Classes used in</span></span>        | [<span data-ttu-id="2e4c8-220">**Configurazione MSMQ**</span><span class="sxs-lookup"><span data-stu-id="2e4c8-220">**MSMQ-Configuration**</span></span>](c-msmqconfiguration.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="2e4c8-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2e4c8-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="2e4c8-222">Voce</span><span class="sxs-lookup"><span data-stu-id="2e4c8-222">Entry</span></span> | <span data-ttu-id="2e4c8-223">Valore</span><span class="sxs-lookup"><span data-stu-id="2e4c8-223">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="2e4c8-224">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="2e4c8-224">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="2e4c8-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2e4c8-225">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="2e4c8-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="2e4c8-226">System-Only</span></span>            | <span data-ttu-id="2e4c8-227">Falso</span><span class="sxs-lookup"><span data-stu-id="2e4c8-227">False</span></span>                                                        |
| <span data-ttu-id="2e4c8-228">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="2e4c8-228">Is-Single-Valued</span></span>       | <span data-ttu-id="2e4c8-229">Falso</span><span class="sxs-lookup"><span data-stu-id="2e4c8-229">False</span></span>                                                        |
| <span data-ttu-id="2e4c8-230">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="2e4c8-230">Is Indexed</span></span>             | <span data-ttu-id="2e4c8-231">Falso</span><span class="sxs-lookup"><span data-stu-id="2e4c8-231">False</span></span>                                                        |
| <span data-ttu-id="2e4c8-232">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="2e4c8-232">In Global Catalog</span></span>      | <span data-ttu-id="2e4c8-233">Vero</span><span class="sxs-lookup"><span data-stu-id="2e4c8-233">True</span></span>                                                         |
| <span data-ttu-id="2e4c8-234">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="2e4c8-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="2e4c8-235">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="2e4c8-235">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="2e4c8-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2e4c8-236">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="2e4c8-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2e4c8-237">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="2e4c8-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2e4c8-238">Search-Flags</span></span>           | <span data-ttu-id="2e4c8-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2e4c8-239">0x00000000</span></span>                                                   |
| <span data-ttu-id="2e4c8-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2e4c8-240">System-Flags</span></span>           | <span data-ttu-id="2e4c8-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2e4c8-241">0x00000010</span></span>                                                   |
| <span data-ttu-id="2e4c8-242">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="2e4c8-242">Classes used in</span></span>        | [<span data-ttu-id="2e4c8-243">**Configurazione MSMQ**</span><span class="sxs-lookup"><span data-stu-id="2e4c8-243">**MSMQ-Configuration**</span></span>](c-msmqconfiguration.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="2e4c8-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2e4c8-244">Windows Server 2012</span></span>



| <span data-ttu-id="2e4c8-245">Voce</span><span class="sxs-lookup"><span data-stu-id="2e4c8-245">Entry</span></span> | <span data-ttu-id="2e4c8-246">Valore</span><span class="sxs-lookup"><span data-stu-id="2e4c8-246">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="2e4c8-247">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="2e4c8-247">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="2e4c8-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2e4c8-248">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="2e4c8-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="2e4c8-249">System-Only</span></span>            | <span data-ttu-id="2e4c8-250">Falso</span><span class="sxs-lookup"><span data-stu-id="2e4c8-250">False</span></span>                                                        |
| <span data-ttu-id="2e4c8-251">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="2e4c8-251">Is-Single-Valued</span></span>       | <span data-ttu-id="2e4c8-252">Falso</span><span class="sxs-lookup"><span data-stu-id="2e4c8-252">False</span></span>                                                        |
| <span data-ttu-id="2e4c8-253">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="2e4c8-253">Is Indexed</span></span>             | <span data-ttu-id="2e4c8-254">Falso</span><span class="sxs-lookup"><span data-stu-id="2e4c8-254">False</span></span>                                                        |
| <span data-ttu-id="2e4c8-255">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="2e4c8-255">In Global Catalog</span></span>      | <span data-ttu-id="2e4c8-256">Vero</span><span class="sxs-lookup"><span data-stu-id="2e4c8-256">True</span></span>                                                         |
| <span data-ttu-id="2e4c8-257">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="2e4c8-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="2e4c8-258">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="2e4c8-258">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="2e4c8-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2e4c8-259">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="2e4c8-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2e4c8-260">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="2e4c8-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2e4c8-261">Search-Flags</span></span>           | <span data-ttu-id="2e4c8-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2e4c8-262">0x00000000</span></span>                                                   |
| <span data-ttu-id="2e4c8-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2e4c8-263">System-Flags</span></span>           | <span data-ttu-id="2e4c8-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2e4c8-264">0x00000010</span></span>                                                   |
| <span data-ttu-id="2e4c8-265">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="2e4c8-265">Classes used in</span></span>        | [<span data-ttu-id="2e4c8-266">**Configurazione MSMQ**</span><span class="sxs-lookup"><span data-stu-id="2e4c8-266">**MSMQ-Configuration**</span></span>](c-msmqconfiguration.md)<br/> |



 

 





