---
title: Attributo Tombstone-Lifetime
description: Il numero di giorni prima che un oggetto eliminato venga rimosso dai servizi directory.
ms.assetid: 58898097-912b-4fe6-b6ea-91f49aaa2b1b
ms.tgt_platform: multiple
keywords:
- Schema AD Tombstone-Lifetime attribute
- Schema AD dell'attributo tombstoneLifetime
topic_type:
- apiref
api_name:
- Tombstone-Lifetime
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb2bd0b7b970270c626437ee65288fd07bf48272
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103875506"
---
# <a name="tombstone-lifetime-attribute"></a><span data-ttu-id="8fb47-105">Attributo Tombstone-Lifetime</span><span class="sxs-lookup"><span data-stu-id="8fb47-105">Tombstone-Lifetime attribute</span></span>

<span data-ttu-id="8fb47-106">Il numero di giorni prima che un oggetto eliminato venga rimosso dai servizi directory.</span><span class="sxs-lookup"><span data-stu-id="8fb47-106">The number of days before a deleted object is removed from the directory services.</span></span> <span data-ttu-id="8fb47-107">Questa operazione consente di rimuovere oggetti dai server replicati e di impedire che i ripristini riintroducano un oggetto eliminato.</span><span class="sxs-lookup"><span data-stu-id="8fb47-107">This assists in removing objects from replicated servers and preventing restores from reintroducing a deleted object.</span></span> <span data-ttu-id="8fb47-108">Questo valore si trova nell'oggetto servizio directory nella scheda di interfaccia di rete di configurazione.</span><span class="sxs-lookup"><span data-stu-id="8fb47-108">This value is in the Directory Service object in the configuration NIC.</span></span>



| <span data-ttu-id="8fb47-109">Voce</span><span class="sxs-lookup"><span data-stu-id="8fb47-109">Entry</span></span> | <span data-ttu-id="8fb47-110">Valore</span><span class="sxs-lookup"><span data-stu-id="8fb47-110">Value</span></span> |
|-------------------|-----------------------------------------------------------|
| <span data-ttu-id="8fb47-111">CN</span><span class="sxs-lookup"><span data-stu-id="8fb47-111">CN</span></span>                | <span data-ttu-id="8fb47-112">Tombstone-Lifetime</span><span class="sxs-lookup"><span data-stu-id="8fb47-112">Tombstone-Lifetime</span></span>                                        |
| <span data-ttu-id="8fb47-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="8fb47-113">Ldap-Display-Name</span></span> | <span data-ttu-id="8fb47-114">tombstoneLifetime</span><span class="sxs-lookup"><span data-stu-id="8fb47-114">tombstoneLifetime</span></span>                                         |
| <span data-ttu-id="8fb47-115">Dimensione</span><span class="sxs-lookup"><span data-stu-id="8fb47-115">Size</span></span>              | <span data-ttu-id="8fb47-116">4 byte.</span><span class="sxs-lookup"><span data-stu-id="8fb47-116">4 bytes.</span></span> <span data-ttu-id="8fb47-117">Il valore predefinito è 60 giorni quando non viene immesso alcun valore.</span><span class="sxs-lookup"><span data-stu-id="8fb47-117">The default is 60 days when no value is entered.</span></span> |
| <span data-ttu-id="8fb47-118">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="8fb47-118">Update Privilege</span></span>  | \-                                                        |
| <span data-ttu-id="8fb47-119">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="8fb47-119">Update Frequency</span></span>  | \-                                                        |
| <span data-ttu-id="8fb47-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="8fb47-120">Attribute-Id</span></span>      | <span data-ttu-id="8fb47-121">1.2.840.113556.1.2.54</span><span class="sxs-lookup"><span data-stu-id="8fb47-121">1.2.840.113556.1.2.54</span></span>                                     |
| <span data-ttu-id="8fb47-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="8fb47-122">System-Id-Guid</span></span>    | <span data-ttu-id="8fb47-123">16c3a860-1273-11d0-a060-00aa006c33ed</span><span class="sxs-lookup"><span data-stu-id="8fb47-123">16c3a860-1273-11d0-a060-00aa006c33ed</span></span>                      |
| <span data-ttu-id="8fb47-124">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8fb47-124">Syntax</span></span>            | [<span data-ttu-id="8fb47-125">**Enumerazione**</span><span class="sxs-lookup"><span data-stu-id="8fb47-125">**Enumeration**</span></span>](s-enumeration.md)                      |



## <a name="implementations"></a><span data-ttu-id="8fb47-126">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="8fb47-126">Implementations</span></span>

-   [<span data-ttu-id="8fb47-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="8fb47-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="8fb47-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="8fb47-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="8fb47-129">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="8fb47-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="8fb47-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="8fb47-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="8fb47-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="8fb47-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="8fb47-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="8fb47-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="8fb47-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="8fb47-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="8fb47-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8fb47-134">Windows 2000 Server</span></span>



| <span data-ttu-id="8fb47-135">Voce</span><span class="sxs-lookup"><span data-stu-id="8fb47-135">Entry</span></span> | <span data-ttu-id="8fb47-136">Valore</span><span class="sxs-lookup"><span data-stu-id="8fb47-136">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="8fb47-137">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="8fb47-137">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="8fb47-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8fb47-138">MAPI-Id</span></span>                | <span data-ttu-id="8fb47-139">0x8145</span><span class="sxs-lookup"><span data-stu-id="8fb47-139">0x8145</span></span>                                           |
| <span data-ttu-id="8fb47-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="8fb47-140">System-Only</span></span>            | <span data-ttu-id="8fb47-141">Falso</span><span class="sxs-lookup"><span data-stu-id="8fb47-141">False</span></span>                                            |
| <span data-ttu-id="8fb47-142">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="8fb47-142">Is-Single-Valued</span></span>       | <span data-ttu-id="8fb47-143">Vero</span><span class="sxs-lookup"><span data-stu-id="8fb47-143">True</span></span>                                             |
| <span data-ttu-id="8fb47-144">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="8fb47-144">Is Indexed</span></span>             | <span data-ttu-id="8fb47-145">Falso</span><span class="sxs-lookup"><span data-stu-id="8fb47-145">False</span></span>                                            |
| <span data-ttu-id="8fb47-146">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="8fb47-146">In Global Catalog</span></span>      | <span data-ttu-id="8fb47-147">Falso</span><span class="sxs-lookup"><span data-stu-id="8fb47-147">False</span></span>                                            |
| <span data-ttu-id="8fb47-148">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="8fb47-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="8fb47-149">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="8fb47-149">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="8fb47-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8fb47-150">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="8fb47-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8fb47-151">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="8fb47-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8fb47-152">Search-Flags</span></span>           | <span data-ttu-id="8fb47-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8fb47-153">0x00000000</span></span>                                       |
| <span data-ttu-id="8fb47-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8fb47-154">System-Flags</span></span>           | <span data-ttu-id="8fb47-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8fb47-155">0x00000010</span></span>                                       |
| <span data-ttu-id="8fb47-156">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="8fb47-156">Classes used in</span></span>        | [<span data-ttu-id="8fb47-157">**NTDS-Service**</span><span class="sxs-lookup"><span data-stu-id="8fb47-157">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="8fb47-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8fb47-158">Windows Server 2003</span></span>



| <span data-ttu-id="8fb47-159">Voce</span><span class="sxs-lookup"><span data-stu-id="8fb47-159">Entry</span></span> | <span data-ttu-id="8fb47-160">Valore</span><span class="sxs-lookup"><span data-stu-id="8fb47-160">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="8fb47-161">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="8fb47-161">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="8fb47-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8fb47-162">MAPI-Id</span></span>                | <span data-ttu-id="8fb47-163">0x8145</span><span class="sxs-lookup"><span data-stu-id="8fb47-163">0x8145</span></span>                                           |
| <span data-ttu-id="8fb47-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="8fb47-164">System-Only</span></span>            | <span data-ttu-id="8fb47-165">Falso</span><span class="sxs-lookup"><span data-stu-id="8fb47-165">False</span></span>                                            |
| <span data-ttu-id="8fb47-166">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="8fb47-166">Is-Single-Valued</span></span>       | <span data-ttu-id="8fb47-167">Vero</span><span class="sxs-lookup"><span data-stu-id="8fb47-167">True</span></span>                                             |
| <span data-ttu-id="8fb47-168">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="8fb47-168">Is Indexed</span></span>             | <span data-ttu-id="8fb47-169">Falso</span><span class="sxs-lookup"><span data-stu-id="8fb47-169">False</span></span>                                            |
| <span data-ttu-id="8fb47-170">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="8fb47-170">In Global Catalog</span></span>      | <span data-ttu-id="8fb47-171">Falso</span><span class="sxs-lookup"><span data-stu-id="8fb47-171">False</span></span>                                            |
| <span data-ttu-id="8fb47-172">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="8fb47-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="8fb47-173">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="8fb47-173">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="8fb47-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8fb47-174">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="8fb47-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8fb47-175">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="8fb47-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8fb47-176">Search-Flags</span></span>           | <span data-ttu-id="8fb47-177">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8fb47-177">0x00000000</span></span>                                       |
| <span data-ttu-id="8fb47-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8fb47-178">System-Flags</span></span>           | <span data-ttu-id="8fb47-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8fb47-179">0x00000010</span></span>                                       |
| <span data-ttu-id="8fb47-180">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="8fb47-180">Classes used in</span></span>        | [<span data-ttu-id="8fb47-181">**NTDS-Service**</span><span class="sxs-lookup"><span data-stu-id="8fb47-181">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="adam"></a><span data-ttu-id="8fb47-182">ADAM</span><span class="sxs-lookup"><span data-stu-id="8fb47-182">ADAM</span></span>



| <span data-ttu-id="8fb47-183">Voce</span><span class="sxs-lookup"><span data-stu-id="8fb47-183">Entry</span></span> | <span data-ttu-id="8fb47-184">Valore</span><span class="sxs-lookup"><span data-stu-id="8fb47-184">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="8fb47-185">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="8fb47-185">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="8fb47-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8fb47-186">MAPI-Id</span></span>                | <span data-ttu-id="8fb47-187">0x8145</span><span class="sxs-lookup"><span data-stu-id="8fb47-187">0x8145</span></span>                                           |
| <span data-ttu-id="8fb47-188">System-Only</span><span class="sxs-lookup"><span data-stu-id="8fb47-188">System-Only</span></span>            | <span data-ttu-id="8fb47-189">Falso</span><span class="sxs-lookup"><span data-stu-id="8fb47-189">False</span></span>                                            |
| <span data-ttu-id="8fb47-190">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="8fb47-190">Is-Single-Valued</span></span>       | <span data-ttu-id="8fb47-191">Vero</span><span class="sxs-lookup"><span data-stu-id="8fb47-191">True</span></span>                                             |
| <span data-ttu-id="8fb47-192">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="8fb47-192">Is Indexed</span></span>             | <span data-ttu-id="8fb47-193">Falso</span><span class="sxs-lookup"><span data-stu-id="8fb47-193">False</span></span>                                            |
| <span data-ttu-id="8fb47-194">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="8fb47-194">In Global Catalog</span></span>      | <span data-ttu-id="8fb47-195">Falso</span><span class="sxs-lookup"><span data-stu-id="8fb47-195">False</span></span>                                            |
| <span data-ttu-id="8fb47-196">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="8fb47-196">NT-Security-Descriptor</span></span> | <span data-ttu-id="8fb47-197">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="8fb47-197">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="8fb47-198">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8fb47-198">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="8fb47-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8fb47-199">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="8fb47-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8fb47-200">Search-Flags</span></span>           | <span data-ttu-id="8fb47-201">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8fb47-201">0x00000000</span></span>                                       |
| <span data-ttu-id="8fb47-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8fb47-202">System-Flags</span></span>           | <span data-ttu-id="8fb47-203">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8fb47-203">0x00000010</span></span>                                       |
| <span data-ttu-id="8fb47-204">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="8fb47-204">Classes used in</span></span>        | [<span data-ttu-id="8fb47-205">**NTDS-Service**</span><span class="sxs-lookup"><span data-stu-id="8fb47-205">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="8fb47-206">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="8fb47-206">Windows Server 2003 R2</span></span>



| <span data-ttu-id="8fb47-207">Voce</span><span class="sxs-lookup"><span data-stu-id="8fb47-207">Entry</span></span> | <span data-ttu-id="8fb47-208">Valore</span><span class="sxs-lookup"><span data-stu-id="8fb47-208">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="8fb47-209">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="8fb47-209">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="8fb47-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8fb47-210">MAPI-Id</span></span>                | <span data-ttu-id="8fb47-211">0x8145</span><span class="sxs-lookup"><span data-stu-id="8fb47-211">0x8145</span></span>                                           |
| <span data-ttu-id="8fb47-212">System-Only</span><span class="sxs-lookup"><span data-stu-id="8fb47-212">System-Only</span></span>            | <span data-ttu-id="8fb47-213">Falso</span><span class="sxs-lookup"><span data-stu-id="8fb47-213">False</span></span>                                            |
| <span data-ttu-id="8fb47-214">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="8fb47-214">Is-Single-Valued</span></span>       | <span data-ttu-id="8fb47-215">Vero</span><span class="sxs-lookup"><span data-stu-id="8fb47-215">True</span></span>                                             |
| <span data-ttu-id="8fb47-216">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="8fb47-216">Is Indexed</span></span>             | <span data-ttu-id="8fb47-217">Falso</span><span class="sxs-lookup"><span data-stu-id="8fb47-217">False</span></span>                                            |
| <span data-ttu-id="8fb47-218">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="8fb47-218">In Global Catalog</span></span>      | <span data-ttu-id="8fb47-219">Falso</span><span class="sxs-lookup"><span data-stu-id="8fb47-219">False</span></span>                                            |
| <span data-ttu-id="8fb47-220">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="8fb47-220">NT-Security-Descriptor</span></span> | <span data-ttu-id="8fb47-221">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="8fb47-221">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="8fb47-222">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8fb47-222">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="8fb47-223">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8fb47-223">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="8fb47-224">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8fb47-224">Search-Flags</span></span>           | <span data-ttu-id="8fb47-225">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8fb47-225">0x00000000</span></span>                                       |
| <span data-ttu-id="8fb47-226">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8fb47-226">System-Flags</span></span>           | <span data-ttu-id="8fb47-227">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8fb47-227">0x00000010</span></span>                                       |
| <span data-ttu-id="8fb47-228">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="8fb47-228">Classes used in</span></span>        | [<span data-ttu-id="8fb47-229">**NTDS-Service**</span><span class="sxs-lookup"><span data-stu-id="8fb47-229">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="8fb47-230">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8fb47-230">Windows Server 2008</span></span>



| <span data-ttu-id="8fb47-231">Voce</span><span class="sxs-lookup"><span data-stu-id="8fb47-231">Entry</span></span> | <span data-ttu-id="8fb47-232">Valore</span><span class="sxs-lookup"><span data-stu-id="8fb47-232">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="8fb47-233">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="8fb47-233">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="8fb47-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8fb47-234">MAPI-Id</span></span>                | <span data-ttu-id="8fb47-235">0x8145</span><span class="sxs-lookup"><span data-stu-id="8fb47-235">0x8145</span></span>                                           |
| <span data-ttu-id="8fb47-236">System-Only</span><span class="sxs-lookup"><span data-stu-id="8fb47-236">System-Only</span></span>            | <span data-ttu-id="8fb47-237">Falso</span><span class="sxs-lookup"><span data-stu-id="8fb47-237">False</span></span>                                            |
| <span data-ttu-id="8fb47-238">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="8fb47-238">Is-Single-Valued</span></span>       | <span data-ttu-id="8fb47-239">Vero</span><span class="sxs-lookup"><span data-stu-id="8fb47-239">True</span></span>                                             |
| <span data-ttu-id="8fb47-240">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="8fb47-240">Is Indexed</span></span>             | <span data-ttu-id="8fb47-241">Falso</span><span class="sxs-lookup"><span data-stu-id="8fb47-241">False</span></span>                                            |
| <span data-ttu-id="8fb47-242">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="8fb47-242">In Global Catalog</span></span>      | <span data-ttu-id="8fb47-243">Falso</span><span class="sxs-lookup"><span data-stu-id="8fb47-243">False</span></span>                                            |
| <span data-ttu-id="8fb47-244">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="8fb47-244">NT-Security-Descriptor</span></span> | <span data-ttu-id="8fb47-245">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="8fb47-245">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="8fb47-246">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8fb47-246">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="8fb47-247">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8fb47-247">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="8fb47-248">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8fb47-248">Search-Flags</span></span>           | <span data-ttu-id="8fb47-249">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8fb47-249">0x00000000</span></span>                                       |
| <span data-ttu-id="8fb47-250">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8fb47-250">System-Flags</span></span>           | <span data-ttu-id="8fb47-251">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8fb47-251">0x00000010</span></span>                                       |
| <span data-ttu-id="8fb47-252">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="8fb47-252">Classes used in</span></span>        | [<span data-ttu-id="8fb47-253">**NTDS-Service**</span><span class="sxs-lookup"><span data-stu-id="8fb47-253">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="8fb47-254">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8fb47-254">Windows Server 2008 R2</span></span>



| <span data-ttu-id="8fb47-255">Voce</span><span class="sxs-lookup"><span data-stu-id="8fb47-255">Entry</span></span> | <span data-ttu-id="8fb47-256">Valore</span><span class="sxs-lookup"><span data-stu-id="8fb47-256">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="8fb47-257">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="8fb47-257">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="8fb47-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8fb47-258">MAPI-Id</span></span>                | <span data-ttu-id="8fb47-259">0x8145</span><span class="sxs-lookup"><span data-stu-id="8fb47-259">0x8145</span></span>                                           |
| <span data-ttu-id="8fb47-260">System-Only</span><span class="sxs-lookup"><span data-stu-id="8fb47-260">System-Only</span></span>            | <span data-ttu-id="8fb47-261">Falso</span><span class="sxs-lookup"><span data-stu-id="8fb47-261">False</span></span>                                            |
| <span data-ttu-id="8fb47-262">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="8fb47-262">Is-Single-Valued</span></span>       | <span data-ttu-id="8fb47-263">Vero</span><span class="sxs-lookup"><span data-stu-id="8fb47-263">True</span></span>                                             |
| <span data-ttu-id="8fb47-264">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="8fb47-264">Is Indexed</span></span>             | <span data-ttu-id="8fb47-265">Falso</span><span class="sxs-lookup"><span data-stu-id="8fb47-265">False</span></span>                                            |
| <span data-ttu-id="8fb47-266">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="8fb47-266">In Global Catalog</span></span>      | <span data-ttu-id="8fb47-267">Falso</span><span class="sxs-lookup"><span data-stu-id="8fb47-267">False</span></span>                                            |
| <span data-ttu-id="8fb47-268">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="8fb47-268">NT-Security-Descriptor</span></span> | <span data-ttu-id="8fb47-269">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="8fb47-269">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="8fb47-270">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8fb47-270">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="8fb47-271">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8fb47-271">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="8fb47-272">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8fb47-272">Search-Flags</span></span>           | <span data-ttu-id="8fb47-273">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8fb47-273">0x00000000</span></span>                                       |
| <span data-ttu-id="8fb47-274">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8fb47-274">System-Flags</span></span>           | <span data-ttu-id="8fb47-275">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8fb47-275">0x00000010</span></span>                                       |
| <span data-ttu-id="8fb47-276">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="8fb47-276">Classes used in</span></span>        | [<span data-ttu-id="8fb47-277">**NTDS-Service**</span><span class="sxs-lookup"><span data-stu-id="8fb47-277">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="8fb47-278">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8fb47-278">Windows Server 2012</span></span>



| <span data-ttu-id="8fb47-279">Voce</span><span class="sxs-lookup"><span data-stu-id="8fb47-279">Entry</span></span> | <span data-ttu-id="8fb47-280">Valore</span><span class="sxs-lookup"><span data-stu-id="8fb47-280">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="8fb47-281">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="8fb47-281">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="8fb47-282">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8fb47-282">MAPI-Id</span></span>                | <span data-ttu-id="8fb47-283">0x8145</span><span class="sxs-lookup"><span data-stu-id="8fb47-283">0x8145</span></span>                                           |
| <span data-ttu-id="8fb47-284">System-Only</span><span class="sxs-lookup"><span data-stu-id="8fb47-284">System-Only</span></span>            | <span data-ttu-id="8fb47-285">Falso</span><span class="sxs-lookup"><span data-stu-id="8fb47-285">False</span></span>                                            |
| <span data-ttu-id="8fb47-286">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="8fb47-286">Is-Single-Valued</span></span>       | <span data-ttu-id="8fb47-287">Vero</span><span class="sxs-lookup"><span data-stu-id="8fb47-287">True</span></span>                                             |
| <span data-ttu-id="8fb47-288">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="8fb47-288">Is Indexed</span></span>             | <span data-ttu-id="8fb47-289">Falso</span><span class="sxs-lookup"><span data-stu-id="8fb47-289">False</span></span>                                            |
| <span data-ttu-id="8fb47-290">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="8fb47-290">In Global Catalog</span></span>      | <span data-ttu-id="8fb47-291">Falso</span><span class="sxs-lookup"><span data-stu-id="8fb47-291">False</span></span>                                            |
| <span data-ttu-id="8fb47-292">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="8fb47-292">NT-Security-Descriptor</span></span> | <span data-ttu-id="8fb47-293">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="8fb47-293">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="8fb47-294">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8fb47-294">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="8fb47-295">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8fb47-295">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="8fb47-296">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8fb47-296">Search-Flags</span></span>           | <span data-ttu-id="8fb47-297">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8fb47-297">0x00000000</span></span>                                       |
| <span data-ttu-id="8fb47-298">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8fb47-298">System-Flags</span></span>           | <span data-ttu-id="8fb47-299">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8fb47-299">0x00000010</span></span>                                       |
| <span data-ttu-id="8fb47-300">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="8fb47-300">Classes used in</span></span>        | [<span data-ttu-id="8fb47-301">**NTDS-Service**</span><span class="sxs-lookup"><span data-stu-id="8fb47-301">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



 

 





