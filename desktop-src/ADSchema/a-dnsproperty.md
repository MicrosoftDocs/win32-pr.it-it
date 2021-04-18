---
title: Attributo DNS-Property
description: Utilizzato per archiviare le impostazioni binarie (proprietà) negli oggetti zona DNS.
ms.assetid: 55ea38cd-6b5b-4500-8e68-ae4d35e4b177
ms.tgt_platform: multiple
keywords:
- Schema AD DNS-Property attribute
- Schema AD dell'attributo dNSProperty
topic_type:
- apiref
api_name:
- DNS-Property
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f8fd18f4524ec0bf61a609d21a361668ed295b6
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "106302940"
---
# <a name="dns-property-attribute"></a><span data-ttu-id="e4d90-105">Attributo DNS-Property</span><span class="sxs-lookup"><span data-stu-id="e4d90-105">DNS-Property attribute</span></span>

<span data-ttu-id="e4d90-106">Utilizzato per archiviare le impostazioni binarie (proprietà) negli oggetti zona DNS.</span><span class="sxs-lookup"><span data-stu-id="e4d90-106">Used to store binary settings (properties) on DNS zone objects.</span></span>



| <span data-ttu-id="e4d90-107">Voce</span><span class="sxs-lookup"><span data-stu-id="e4d90-107">Entry</span></span> | <span data-ttu-id="e4d90-108">Valore</span><span class="sxs-lookup"><span data-stu-id="e4d90-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="e4d90-109">CN</span><span class="sxs-lookup"><span data-stu-id="e4d90-109">CN</span></span>                | <span data-ttu-id="e4d90-110">DNS-Property</span><span class="sxs-lookup"><span data-stu-id="e4d90-110">DNS-Property</span></span>                                          |
| <span data-ttu-id="e4d90-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="e4d90-111">Ldap-Display-Name</span></span> | <span data-ttu-id="e4d90-112">dNSProperty</span><span class="sxs-lookup"><span data-stu-id="e4d90-112">dNSProperty</span></span>                                           |
| <span data-ttu-id="e4d90-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="e4d90-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="e4d90-114">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="e4d90-114">Update Privilege</span></span>  | <span data-ttu-id="e4d90-115">Questo valore viene impostato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="e4d90-115">This value is set by the system.</span></span>                      |
| <span data-ttu-id="e4d90-116">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="e4d90-116">Update Frequency</span></span>  | <span data-ttu-id="e4d90-117">Ogni volta che i record della zona DNS cambiano.</span><span class="sxs-lookup"><span data-stu-id="e4d90-117">Whenever DNS zone records change.</span></span>                     |
| <span data-ttu-id="e4d90-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e4d90-118">Attribute-Id</span></span>      | <span data-ttu-id="e4d90-119">1.2.840.113556.1.4.1306</span><span class="sxs-lookup"><span data-stu-id="e4d90-119">1.2.840.113556.1.4.1306</span></span>                               |
| <span data-ttu-id="e4d90-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="e4d90-120">System-Id-Guid</span></span>    | <span data-ttu-id="e4d90-121">675a15fe-3b70-11d2-90cc-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="e4d90-121">675a15fe-3b70-11d2-90cc-00c04fd91ab1</span></span>                  |
| <span data-ttu-id="e4d90-122">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e4d90-122">Syntax</span></span>            | [<span data-ttu-id="e4d90-123">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="e4d90-123">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="e4d90-124">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="e4d90-124">Implementations</span></span>

-   [<span data-ttu-id="e4d90-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="e4d90-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="e4d90-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e4d90-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e4d90-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e4d90-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e4d90-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e4d90-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e4d90-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e4d90-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e4d90-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e4d90-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="e4d90-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e4d90-131">Windows 2000 Server</span></span>



| <span data-ttu-id="e4d90-132">Voce</span><span class="sxs-lookup"><span data-stu-id="e4d90-132">Entry</span></span> | <span data-ttu-id="e4d90-133">Valore</span><span class="sxs-lookup"><span data-stu-id="e4d90-133">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="e4d90-134">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="e4d90-134">Link-Id</span></span>                | \-                                                                                |
| <span data-ttu-id="e4d90-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e4d90-135">MAPI-Id</span></span>                | \-                                                                                |
| <span data-ttu-id="e4d90-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="e4d90-136">System-Only</span></span>            | <span data-ttu-id="e4d90-137">Falso</span><span class="sxs-lookup"><span data-stu-id="e4d90-137">False</span></span>                                                                             |
| <span data-ttu-id="e4d90-138">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="e4d90-138">Is-Single-Valued</span></span>       | <span data-ttu-id="e4d90-139">Falso</span><span class="sxs-lookup"><span data-stu-id="e4d90-139">False</span></span>                                                                             |
| <span data-ttu-id="e4d90-140">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="e4d90-140">Is Indexed</span></span>             | <span data-ttu-id="e4d90-141">Falso</span><span class="sxs-lookup"><span data-stu-id="e4d90-141">False</span></span>                                                                             |
| <span data-ttu-id="e4d90-142">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="e4d90-142">In Global Catalog</span></span>      | <span data-ttu-id="e4d90-143">Falso</span><span class="sxs-lookup"><span data-stu-id="e4d90-143">False</span></span>                                                                             |
| <span data-ttu-id="e4d90-144">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="e4d90-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="e4d90-145">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="e4d90-145">O:BAG:BAD:S:</span></span>                                                                      |
| <span data-ttu-id="e4d90-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e4d90-146">Range-Lower</span></span>            | \-                                                                                |
| <span data-ttu-id="e4d90-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e4d90-147">Range-Upper</span></span>            | \-                                                                                |
| <span data-ttu-id="e4d90-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e4d90-148">Search-Flags</span></span>           | <span data-ttu-id="e4d90-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e4d90-149">0x00000000</span></span>                                                                        |
| <span data-ttu-id="e4d90-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e4d90-150">System-Flags</span></span>           | <span data-ttu-id="e4d90-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e4d90-151">0x00000010</span></span>                                                                        |
| <span data-ttu-id="e4d90-152">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="e4d90-152">Classes used in</span></span>        | [<span data-ttu-id="e4d90-153">**DNS-nodo**</span><span class="sxs-lookup"><span data-stu-id="e4d90-153">**Dns-Node**</span></span>](c-dnsnode.md)<br/> [<span data-ttu-id="e4d90-154">**Zona DNS**</span><span class="sxs-lookup"><span data-stu-id="e4d90-154">**Dns-Zone**</span></span>](c-dnszone.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="e4d90-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e4d90-155">Windows Server 2003</span></span>



| <span data-ttu-id="e4d90-156">Voce</span><span class="sxs-lookup"><span data-stu-id="e4d90-156">Entry</span></span> | <span data-ttu-id="e4d90-157">Valore</span><span class="sxs-lookup"><span data-stu-id="e4d90-157">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="e4d90-158">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="e4d90-158">Link-Id</span></span>                | \-                                                                                |
| <span data-ttu-id="e4d90-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e4d90-159">MAPI-Id</span></span>                | \-                                                                                |
| <span data-ttu-id="e4d90-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="e4d90-160">System-Only</span></span>            | <span data-ttu-id="e4d90-161">Falso</span><span class="sxs-lookup"><span data-stu-id="e4d90-161">False</span></span>                                                                             |
| <span data-ttu-id="e4d90-162">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="e4d90-162">Is-Single-Valued</span></span>       | <span data-ttu-id="e4d90-163">Falso</span><span class="sxs-lookup"><span data-stu-id="e4d90-163">False</span></span>                                                                             |
| <span data-ttu-id="e4d90-164">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="e4d90-164">Is Indexed</span></span>             | <span data-ttu-id="e4d90-165">Falso</span><span class="sxs-lookup"><span data-stu-id="e4d90-165">False</span></span>                                                                             |
| <span data-ttu-id="e4d90-166">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="e4d90-166">In Global Catalog</span></span>      | <span data-ttu-id="e4d90-167">Falso</span><span class="sxs-lookup"><span data-stu-id="e4d90-167">False</span></span>                                                                             |
| <span data-ttu-id="e4d90-168">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="e4d90-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="e4d90-169">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="e4d90-169">O:BAG:BAD:S:</span></span>                                                                      |
| <span data-ttu-id="e4d90-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e4d90-170">Range-Lower</span></span>            | \-                                                                                |
| <span data-ttu-id="e4d90-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e4d90-171">Range-Upper</span></span>            | \-                                                                                |
| <span data-ttu-id="e4d90-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e4d90-172">Search-Flags</span></span>           | <span data-ttu-id="e4d90-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e4d90-173">0x00000000</span></span>                                                                        |
| <span data-ttu-id="e4d90-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e4d90-174">System-Flags</span></span>           | <span data-ttu-id="e4d90-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e4d90-175">0x00000010</span></span>                                                                        |
| <span data-ttu-id="e4d90-176">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="e4d90-176">Classes used in</span></span>        | [<span data-ttu-id="e4d90-177">**DNS-nodo**</span><span class="sxs-lookup"><span data-stu-id="e4d90-177">**Dns-Node**</span></span>](c-dnsnode.md)<br/> [<span data-ttu-id="e4d90-178">**Zona DNS**</span><span class="sxs-lookup"><span data-stu-id="e4d90-178">**Dns-Zone**</span></span>](c-dnszone.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e4d90-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e4d90-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e4d90-180">Voce</span><span class="sxs-lookup"><span data-stu-id="e4d90-180">Entry</span></span> | <span data-ttu-id="e4d90-181">Valore</span><span class="sxs-lookup"><span data-stu-id="e4d90-181">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="e4d90-182">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="e4d90-182">Link-Id</span></span>                | \-                                                                                |
| <span data-ttu-id="e4d90-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e4d90-183">MAPI-Id</span></span>                | \-                                                                                |
| <span data-ttu-id="e4d90-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="e4d90-184">System-Only</span></span>            | <span data-ttu-id="e4d90-185">Falso</span><span class="sxs-lookup"><span data-stu-id="e4d90-185">False</span></span>                                                                             |
| <span data-ttu-id="e4d90-186">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="e4d90-186">Is-Single-Valued</span></span>       | <span data-ttu-id="e4d90-187">Falso</span><span class="sxs-lookup"><span data-stu-id="e4d90-187">False</span></span>                                                                             |
| <span data-ttu-id="e4d90-188">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="e4d90-188">Is Indexed</span></span>             | <span data-ttu-id="e4d90-189">Falso</span><span class="sxs-lookup"><span data-stu-id="e4d90-189">False</span></span>                                                                             |
| <span data-ttu-id="e4d90-190">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="e4d90-190">In Global Catalog</span></span>      | <span data-ttu-id="e4d90-191">Falso</span><span class="sxs-lookup"><span data-stu-id="e4d90-191">False</span></span>                                                                             |
| <span data-ttu-id="e4d90-192">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="e4d90-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="e4d90-193">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="e4d90-193">O:BAG:BAD:S:</span></span>                                                                      |
| <span data-ttu-id="e4d90-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e4d90-194">Range-Lower</span></span>            | \-                                                                                |
| <span data-ttu-id="e4d90-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e4d90-195">Range-Upper</span></span>            | \-                                                                                |
| <span data-ttu-id="e4d90-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e4d90-196">Search-Flags</span></span>           | <span data-ttu-id="e4d90-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e4d90-197">0x00000000</span></span>                                                                        |
| <span data-ttu-id="e4d90-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e4d90-198">System-Flags</span></span>           | <span data-ttu-id="e4d90-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e4d90-199">0x00000010</span></span>                                                                        |
| <span data-ttu-id="e4d90-200">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="e4d90-200">Classes used in</span></span>        | [<span data-ttu-id="e4d90-201">**DNS-nodo**</span><span class="sxs-lookup"><span data-stu-id="e4d90-201">**Dns-Node**</span></span>](c-dnsnode.md)<br/> [<span data-ttu-id="e4d90-202">**Zona DNS**</span><span class="sxs-lookup"><span data-stu-id="e4d90-202">**Dns-Zone**</span></span>](c-dnszone.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="e4d90-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e4d90-203">Windows Server 2008</span></span>



| <span data-ttu-id="e4d90-204">Voce</span><span class="sxs-lookup"><span data-stu-id="e4d90-204">Entry</span></span> | <span data-ttu-id="e4d90-205">Valore</span><span class="sxs-lookup"><span data-stu-id="e4d90-205">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="e4d90-206">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="e4d90-206">Link-Id</span></span>                | \-                                                                                |
| <span data-ttu-id="e4d90-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e4d90-207">MAPI-Id</span></span>                | \-                                                                                |
| <span data-ttu-id="e4d90-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="e4d90-208">System-Only</span></span>            | <span data-ttu-id="e4d90-209">Falso</span><span class="sxs-lookup"><span data-stu-id="e4d90-209">False</span></span>                                                                             |
| <span data-ttu-id="e4d90-210">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="e4d90-210">Is-Single-Valued</span></span>       | <span data-ttu-id="e4d90-211">Falso</span><span class="sxs-lookup"><span data-stu-id="e4d90-211">False</span></span>                                                                             |
| <span data-ttu-id="e4d90-212">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="e4d90-212">Is Indexed</span></span>             | <span data-ttu-id="e4d90-213">Falso</span><span class="sxs-lookup"><span data-stu-id="e4d90-213">False</span></span>                                                                             |
| <span data-ttu-id="e4d90-214">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="e4d90-214">In Global Catalog</span></span>      | <span data-ttu-id="e4d90-215">Falso</span><span class="sxs-lookup"><span data-stu-id="e4d90-215">False</span></span>                                                                             |
| <span data-ttu-id="e4d90-216">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="e4d90-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="e4d90-217">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="e4d90-217">O:BAG:BAD:S:</span></span>                                                                      |
| <span data-ttu-id="e4d90-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e4d90-218">Range-Lower</span></span>            | \-                                                                                |
| <span data-ttu-id="e4d90-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e4d90-219">Range-Upper</span></span>            | \-                                                                                |
| <span data-ttu-id="e4d90-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e4d90-220">Search-Flags</span></span>           | <span data-ttu-id="e4d90-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e4d90-221">0x00000000</span></span>                                                                        |
| <span data-ttu-id="e4d90-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e4d90-222">System-Flags</span></span>           | <span data-ttu-id="e4d90-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e4d90-223">0x00000010</span></span>                                                                        |
| <span data-ttu-id="e4d90-224">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="e4d90-224">Classes used in</span></span>        | [<span data-ttu-id="e4d90-225">**DNS-nodo**</span><span class="sxs-lookup"><span data-stu-id="e4d90-225">**Dns-Node**</span></span>](c-dnsnode.md)<br/> [<span data-ttu-id="e4d90-226">**Zona DNS**</span><span class="sxs-lookup"><span data-stu-id="e4d90-226">**Dns-Zone**</span></span>](c-dnszone.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e4d90-227">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e4d90-227">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e4d90-228">Voce</span><span class="sxs-lookup"><span data-stu-id="e4d90-228">Entry</span></span> | <span data-ttu-id="e4d90-229">Valore</span><span class="sxs-lookup"><span data-stu-id="e4d90-229">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="e4d90-230">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="e4d90-230">Link-Id</span></span>                | \-                                                                                |
| <span data-ttu-id="e4d90-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e4d90-231">MAPI-Id</span></span>                | \-                                                                                |
| <span data-ttu-id="e4d90-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="e4d90-232">System-Only</span></span>            | <span data-ttu-id="e4d90-233">Falso</span><span class="sxs-lookup"><span data-stu-id="e4d90-233">False</span></span>                                                                             |
| <span data-ttu-id="e4d90-234">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="e4d90-234">Is-Single-Valued</span></span>       | <span data-ttu-id="e4d90-235">Falso</span><span class="sxs-lookup"><span data-stu-id="e4d90-235">False</span></span>                                                                             |
| <span data-ttu-id="e4d90-236">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="e4d90-236">Is Indexed</span></span>             | <span data-ttu-id="e4d90-237">Falso</span><span class="sxs-lookup"><span data-stu-id="e4d90-237">False</span></span>                                                                             |
| <span data-ttu-id="e4d90-238">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="e4d90-238">In Global Catalog</span></span>      | <span data-ttu-id="e4d90-239">Falso</span><span class="sxs-lookup"><span data-stu-id="e4d90-239">False</span></span>                                                                             |
| <span data-ttu-id="e4d90-240">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="e4d90-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="e4d90-241">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="e4d90-241">O:BAG:BAD:S:</span></span>                                                                      |
| <span data-ttu-id="e4d90-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e4d90-242">Range-Lower</span></span>            | \-                                                                                |
| <span data-ttu-id="e4d90-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e4d90-243">Range-Upper</span></span>            | \-                                                                                |
| <span data-ttu-id="e4d90-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e4d90-244">Search-Flags</span></span>           | <span data-ttu-id="e4d90-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e4d90-245">0x00000000</span></span>                                                                        |
| <span data-ttu-id="e4d90-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e4d90-246">System-Flags</span></span>           | <span data-ttu-id="e4d90-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e4d90-247">0x00000010</span></span>                                                                        |
| <span data-ttu-id="e4d90-248">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="e4d90-248">Classes used in</span></span>        | [<span data-ttu-id="e4d90-249">**DNS-nodo**</span><span class="sxs-lookup"><span data-stu-id="e4d90-249">**Dns-Node**</span></span>](c-dnsnode.md)<br/> [<span data-ttu-id="e4d90-250">**Zona DNS**</span><span class="sxs-lookup"><span data-stu-id="e4d90-250">**Dns-Zone**</span></span>](c-dnszone.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e4d90-251">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e4d90-251">Windows Server 2012</span></span>



| <span data-ttu-id="e4d90-252">Voce</span><span class="sxs-lookup"><span data-stu-id="e4d90-252">Entry</span></span> | <span data-ttu-id="e4d90-253">Valore</span><span class="sxs-lookup"><span data-stu-id="e4d90-253">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="e4d90-254">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="e4d90-254">Link-Id</span></span>                | \-                                                                                |
| <span data-ttu-id="e4d90-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e4d90-255">MAPI-Id</span></span>                | \-                                                                                |
| <span data-ttu-id="e4d90-256">System-Only</span><span class="sxs-lookup"><span data-stu-id="e4d90-256">System-Only</span></span>            | <span data-ttu-id="e4d90-257">Falso</span><span class="sxs-lookup"><span data-stu-id="e4d90-257">False</span></span>                                                                             |
| <span data-ttu-id="e4d90-258">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="e4d90-258">Is-Single-Valued</span></span>       | <span data-ttu-id="e4d90-259">Falso</span><span class="sxs-lookup"><span data-stu-id="e4d90-259">False</span></span>                                                                             |
| <span data-ttu-id="e4d90-260">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="e4d90-260">Is Indexed</span></span>             | <span data-ttu-id="e4d90-261">Falso</span><span class="sxs-lookup"><span data-stu-id="e4d90-261">False</span></span>                                                                             |
| <span data-ttu-id="e4d90-262">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="e4d90-262">In Global Catalog</span></span>      | <span data-ttu-id="e4d90-263">Falso</span><span class="sxs-lookup"><span data-stu-id="e4d90-263">False</span></span>                                                                             |
| <span data-ttu-id="e4d90-264">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="e4d90-264">NT-Security-Descriptor</span></span> | <span data-ttu-id="e4d90-265">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="e4d90-265">O:BAG:BAD:S:</span></span>                                                                      |
| <span data-ttu-id="e4d90-266">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e4d90-266">Range-Lower</span></span>            | \-                                                                                |
| <span data-ttu-id="e4d90-267">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e4d90-267">Range-Upper</span></span>            | \-                                                                                |
| <span data-ttu-id="e4d90-268">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e4d90-268">Search-Flags</span></span>           | <span data-ttu-id="e4d90-269">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e4d90-269">0x00000000</span></span>                                                                        |
| <span data-ttu-id="e4d90-270">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e4d90-270">System-Flags</span></span>           | <span data-ttu-id="e4d90-271">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e4d90-271">0x00000010</span></span>                                                                        |
| <span data-ttu-id="e4d90-272">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="e4d90-272">Classes used in</span></span>        | [<span data-ttu-id="e4d90-273">**DNS-nodo**</span><span class="sxs-lookup"><span data-stu-id="e4d90-273">**Dns-Node**</span></span>](c-dnsnode.md)<br/> [<span data-ttu-id="e4d90-274">**Zona DNS**</span><span class="sxs-lookup"><span data-stu-id="e4d90-274">**Dns-Zone**</span></span>](c-dnszone.md)<br/> |



 

 





