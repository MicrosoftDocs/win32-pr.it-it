---
title: Attributo partial-attribute-deletion-List
description: Tiene traccia dello stato di replica interno delle repliche parziali, ovvero nei cataloghi globali. Attributo dell'oggetto NC della replica parziale. Utilizzato quando il Garbage Collector è in corso di rimozione degli attributi dagli oggetti nel relativo NCs di replica parziale.
ms.assetid: 0084774b-7231-4cfc-8f60-c014006da2b9
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo partial-attribute-deletion-List
- Schema AD dell'attributo partialAttributeDeletionList
topic_type:
- apiref
api_name:
- Partial-Attribute-Deletion-List
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c2c6c0428d71dbba4199eeb441c838fb54a4463
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "106303165"
---
# <a name="partial-attribute-deletion-list-attribute"></a><span data-ttu-id="61920-107">Attributo partial-attribute-deletion-List</span><span class="sxs-lookup"><span data-stu-id="61920-107">Partial-Attribute-Deletion-List attribute</span></span>

<span data-ttu-id="61920-108">Tiene traccia dello stato di replica interno delle repliche parziali, ovvero nei cataloghi globali.</span><span class="sxs-lookup"><span data-stu-id="61920-108">Tracks the internal replication state of partial replicas (that is, on GCs).</span></span> <span data-ttu-id="61920-109">Attributo dell'oggetto NC della replica parziale.</span><span class="sxs-lookup"><span data-stu-id="61920-109">Attribute of the partial replica NC object.</span></span> <span data-ttu-id="61920-110">Utilizzato quando il Garbage Collector è in corso di rimozione degli attributi dagli oggetti nel relativo NCs di replica parziale.</span><span class="sxs-lookup"><span data-stu-id="61920-110">Used when the GC is in the process of removing attributes from the objects in its partial replica NCs.</span></span>



| <span data-ttu-id="61920-111">Voce</span><span class="sxs-lookup"><span data-stu-id="61920-111">Entry</span></span> | <span data-ttu-id="61920-112">Valore</span><span class="sxs-lookup"><span data-stu-id="61920-112">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="61920-113">CN</span><span class="sxs-lookup"><span data-stu-id="61920-113">CN</span></span>                | <span data-ttu-id="61920-114">Elenco di eliminazione-attributo parziale</span><span class="sxs-lookup"><span data-stu-id="61920-114">Partial-Attribute-Deletion-List</span></span>                       |
| <span data-ttu-id="61920-115">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="61920-115">Ldap-Display-Name</span></span> | <span data-ttu-id="61920-116">partialAttributeDeletionList</span><span class="sxs-lookup"><span data-stu-id="61920-116">partialAttributeDeletionList</span></span>                          |
| <span data-ttu-id="61920-117">Dimensione</span><span class="sxs-lookup"><span data-stu-id="61920-117">Size</span></span>              | \-                                                    |
| <span data-ttu-id="61920-118">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="61920-118">Update Privilege</span></span>  | <span data-ttu-id="61920-119">Questo valore viene impostato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="61920-119">This value is set by the system.</span></span>                      |
| <span data-ttu-id="61920-120">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="61920-120">Update Frequency</span></span>  | <span data-ttu-id="61920-121">Durante la replica</span><span class="sxs-lookup"><span data-stu-id="61920-121">During replication</span></span>                                    |
| <span data-ttu-id="61920-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="61920-122">Attribute-Id</span></span>      | <span data-ttu-id="61920-123">1.2.840.113556.1.4.663</span><span class="sxs-lookup"><span data-stu-id="61920-123">1.2.840.113556.1.4.663</span></span>                                |
| <span data-ttu-id="61920-124">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="61920-124">System-Id-Guid</span></span>    | <span data-ttu-id="61920-125">28630ec0-41d5-11d1-a9c1-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="61920-125">28630ec0-41d5-11d1-a9c1-0000f80367c1</span></span>                  |
| <span data-ttu-id="61920-126">Sintassi</span><span class="sxs-lookup"><span data-stu-id="61920-126">Syntax</span></span>            | [<span data-ttu-id="61920-127">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="61920-127">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="61920-128">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="61920-128">Implementations</span></span>

-   [<span data-ttu-id="61920-129">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="61920-129">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="61920-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="61920-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="61920-131">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="61920-131">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="61920-132">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="61920-132">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="61920-133">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="61920-133">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="61920-134">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="61920-134">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="61920-135">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="61920-135">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="61920-136">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="61920-136">Windows 2000 Server</span></span>



| <span data-ttu-id="61920-137">Voce</span><span class="sxs-lookup"><span data-stu-id="61920-137">Entry</span></span> | <span data-ttu-id="61920-138">Valore</span><span class="sxs-lookup"><span data-stu-id="61920-138">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="61920-139">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="61920-139">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="61920-140">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="61920-140">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="61920-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="61920-141">System-Only</span></span>            | <span data-ttu-id="61920-142">Vero</span><span class="sxs-lookup"><span data-stu-id="61920-142">True</span></span>                            |
| <span data-ttu-id="61920-143">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="61920-143">Is-Single-Valued</span></span>       | <span data-ttu-id="61920-144">Vero</span><span class="sxs-lookup"><span data-stu-id="61920-144">True</span></span>                            |
| <span data-ttu-id="61920-145">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="61920-145">Is Indexed</span></span>             | <span data-ttu-id="61920-146">Falso</span><span class="sxs-lookup"><span data-stu-id="61920-146">False</span></span>                           |
| <span data-ttu-id="61920-147">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="61920-147">In Global Catalog</span></span>      | <span data-ttu-id="61920-148">Vero</span><span class="sxs-lookup"><span data-stu-id="61920-148">True</span></span>                            |
| <span data-ttu-id="61920-149">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="61920-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="61920-150">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="61920-150">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="61920-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="61920-151">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="61920-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="61920-152">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="61920-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="61920-153">Search-Flags</span></span>           | <span data-ttu-id="61920-154">0x00000000</span><span class="sxs-lookup"><span data-stu-id="61920-154">0x00000000</span></span>                      |
| <span data-ttu-id="61920-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="61920-155">System-Flags</span></span>           | <span data-ttu-id="61920-156">0x00000013</span><span class="sxs-lookup"><span data-stu-id="61920-156">0x00000013</span></span>                      |
| <span data-ttu-id="61920-157">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="61920-157">Classes used in</span></span>        | [<span data-ttu-id="61920-158">**In alto**</span><span class="sxs-lookup"><span data-stu-id="61920-158">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="61920-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="61920-159">Windows Server 2003</span></span>



| <span data-ttu-id="61920-160">Voce</span><span class="sxs-lookup"><span data-stu-id="61920-160">Entry</span></span> | <span data-ttu-id="61920-161">Valore</span><span class="sxs-lookup"><span data-stu-id="61920-161">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="61920-162">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="61920-162">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="61920-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="61920-163">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="61920-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="61920-164">System-Only</span></span>            | <span data-ttu-id="61920-165">Vero</span><span class="sxs-lookup"><span data-stu-id="61920-165">True</span></span>                            |
| <span data-ttu-id="61920-166">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="61920-166">Is-Single-Valued</span></span>       | <span data-ttu-id="61920-167">Vero</span><span class="sxs-lookup"><span data-stu-id="61920-167">True</span></span>                            |
| <span data-ttu-id="61920-168">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="61920-168">Is Indexed</span></span>             | <span data-ttu-id="61920-169">Falso</span><span class="sxs-lookup"><span data-stu-id="61920-169">False</span></span>                           |
| <span data-ttu-id="61920-170">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="61920-170">In Global Catalog</span></span>      | <span data-ttu-id="61920-171">Vero</span><span class="sxs-lookup"><span data-stu-id="61920-171">True</span></span>                            |
| <span data-ttu-id="61920-172">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="61920-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="61920-173">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="61920-173">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="61920-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="61920-174">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="61920-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="61920-175">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="61920-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="61920-176">Search-Flags</span></span>           | <span data-ttu-id="61920-177">0x00000000</span><span class="sxs-lookup"><span data-stu-id="61920-177">0x00000000</span></span>                      |
| <span data-ttu-id="61920-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="61920-178">System-Flags</span></span>           | <span data-ttu-id="61920-179">0x00000013</span><span class="sxs-lookup"><span data-stu-id="61920-179">0x00000013</span></span>                      |
| <span data-ttu-id="61920-180">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="61920-180">Classes used in</span></span>        | [<span data-ttu-id="61920-181">**In alto**</span><span class="sxs-lookup"><span data-stu-id="61920-181">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="61920-182">ADAM</span><span class="sxs-lookup"><span data-stu-id="61920-182">ADAM</span></span>



| <span data-ttu-id="61920-183">Voce</span><span class="sxs-lookup"><span data-stu-id="61920-183">Entry</span></span> | <span data-ttu-id="61920-184">Valore</span><span class="sxs-lookup"><span data-stu-id="61920-184">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="61920-185">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="61920-185">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="61920-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="61920-186">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="61920-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="61920-187">System-Only</span></span>            | <span data-ttu-id="61920-188">Vero</span><span class="sxs-lookup"><span data-stu-id="61920-188">True</span></span>                            |
| <span data-ttu-id="61920-189">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="61920-189">Is-Single-Valued</span></span>       | <span data-ttu-id="61920-190">Vero</span><span class="sxs-lookup"><span data-stu-id="61920-190">True</span></span>                            |
| <span data-ttu-id="61920-191">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="61920-191">Is Indexed</span></span>             | <span data-ttu-id="61920-192">Falso</span><span class="sxs-lookup"><span data-stu-id="61920-192">False</span></span>                           |
| <span data-ttu-id="61920-193">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="61920-193">In Global Catalog</span></span>      | <span data-ttu-id="61920-194">Vero</span><span class="sxs-lookup"><span data-stu-id="61920-194">True</span></span>                            |
| <span data-ttu-id="61920-195">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="61920-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="61920-196">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="61920-196">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="61920-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="61920-197">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="61920-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="61920-198">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="61920-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="61920-199">Search-Flags</span></span>           | <span data-ttu-id="61920-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="61920-200">0x00000000</span></span>                      |
| <span data-ttu-id="61920-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="61920-201">System-Flags</span></span>           | <span data-ttu-id="61920-202">0x00000013</span><span class="sxs-lookup"><span data-stu-id="61920-202">0x00000013</span></span>                      |
| <span data-ttu-id="61920-203">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="61920-203">Classes used in</span></span>        | [<span data-ttu-id="61920-204">**In alto**</span><span class="sxs-lookup"><span data-stu-id="61920-204">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="61920-205">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="61920-205">Windows Server 2003 R2</span></span>



| <span data-ttu-id="61920-206">Voce</span><span class="sxs-lookup"><span data-stu-id="61920-206">Entry</span></span> | <span data-ttu-id="61920-207">Valore</span><span class="sxs-lookup"><span data-stu-id="61920-207">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="61920-208">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="61920-208">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="61920-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="61920-209">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="61920-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="61920-210">System-Only</span></span>            | <span data-ttu-id="61920-211">Vero</span><span class="sxs-lookup"><span data-stu-id="61920-211">True</span></span>                            |
| <span data-ttu-id="61920-212">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="61920-212">Is-Single-Valued</span></span>       | <span data-ttu-id="61920-213">Vero</span><span class="sxs-lookup"><span data-stu-id="61920-213">True</span></span>                            |
| <span data-ttu-id="61920-214">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="61920-214">Is Indexed</span></span>             | <span data-ttu-id="61920-215">Falso</span><span class="sxs-lookup"><span data-stu-id="61920-215">False</span></span>                           |
| <span data-ttu-id="61920-216">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="61920-216">In Global Catalog</span></span>      | <span data-ttu-id="61920-217">Vero</span><span class="sxs-lookup"><span data-stu-id="61920-217">True</span></span>                            |
| <span data-ttu-id="61920-218">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="61920-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="61920-219">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="61920-219">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="61920-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="61920-220">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="61920-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="61920-221">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="61920-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="61920-222">Search-Flags</span></span>           | <span data-ttu-id="61920-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="61920-223">0x00000000</span></span>                      |
| <span data-ttu-id="61920-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="61920-224">System-Flags</span></span>           | <span data-ttu-id="61920-225">0x00000013</span><span class="sxs-lookup"><span data-stu-id="61920-225">0x00000013</span></span>                      |
| <span data-ttu-id="61920-226">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="61920-226">Classes used in</span></span>        | [<span data-ttu-id="61920-227">**In alto**</span><span class="sxs-lookup"><span data-stu-id="61920-227">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="61920-228">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="61920-228">Windows Server 2008</span></span>



| <span data-ttu-id="61920-229">Voce</span><span class="sxs-lookup"><span data-stu-id="61920-229">Entry</span></span> | <span data-ttu-id="61920-230">Valore</span><span class="sxs-lookup"><span data-stu-id="61920-230">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="61920-231">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="61920-231">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="61920-232">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="61920-232">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="61920-233">System-Only</span><span class="sxs-lookup"><span data-stu-id="61920-233">System-Only</span></span>            | <span data-ttu-id="61920-234">Vero</span><span class="sxs-lookup"><span data-stu-id="61920-234">True</span></span>                            |
| <span data-ttu-id="61920-235">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="61920-235">Is-Single-Valued</span></span>       | <span data-ttu-id="61920-236">Vero</span><span class="sxs-lookup"><span data-stu-id="61920-236">True</span></span>                            |
| <span data-ttu-id="61920-237">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="61920-237">Is Indexed</span></span>             | <span data-ttu-id="61920-238">Falso</span><span class="sxs-lookup"><span data-stu-id="61920-238">False</span></span>                           |
| <span data-ttu-id="61920-239">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="61920-239">In Global Catalog</span></span>      | <span data-ttu-id="61920-240">Vero</span><span class="sxs-lookup"><span data-stu-id="61920-240">True</span></span>                            |
| <span data-ttu-id="61920-241">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="61920-241">NT-Security-Descriptor</span></span> | <span data-ttu-id="61920-242">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="61920-242">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="61920-243">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="61920-243">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="61920-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="61920-244">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="61920-245">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="61920-245">Search-Flags</span></span>           | <span data-ttu-id="61920-246">0x00000000</span><span class="sxs-lookup"><span data-stu-id="61920-246">0x00000000</span></span>                      |
| <span data-ttu-id="61920-247">System-Flags</span><span class="sxs-lookup"><span data-stu-id="61920-247">System-Flags</span></span>           | <span data-ttu-id="61920-248">0x00000013</span><span class="sxs-lookup"><span data-stu-id="61920-248">0x00000013</span></span>                      |
| <span data-ttu-id="61920-249">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="61920-249">Classes used in</span></span>        | [<span data-ttu-id="61920-250">**In alto**</span><span class="sxs-lookup"><span data-stu-id="61920-250">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="61920-251">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="61920-251">Windows Server 2008 R2</span></span>



| <span data-ttu-id="61920-252">Voce</span><span class="sxs-lookup"><span data-stu-id="61920-252">Entry</span></span> | <span data-ttu-id="61920-253">Valore</span><span class="sxs-lookup"><span data-stu-id="61920-253">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="61920-254">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="61920-254">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="61920-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="61920-255">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="61920-256">System-Only</span><span class="sxs-lookup"><span data-stu-id="61920-256">System-Only</span></span>            | <span data-ttu-id="61920-257">Vero</span><span class="sxs-lookup"><span data-stu-id="61920-257">True</span></span>                            |
| <span data-ttu-id="61920-258">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="61920-258">Is-Single-Valued</span></span>       | <span data-ttu-id="61920-259">Vero</span><span class="sxs-lookup"><span data-stu-id="61920-259">True</span></span>                            |
| <span data-ttu-id="61920-260">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="61920-260">Is Indexed</span></span>             | <span data-ttu-id="61920-261">Falso</span><span class="sxs-lookup"><span data-stu-id="61920-261">False</span></span>                           |
| <span data-ttu-id="61920-262">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="61920-262">In Global Catalog</span></span>      | <span data-ttu-id="61920-263">Vero</span><span class="sxs-lookup"><span data-stu-id="61920-263">True</span></span>                            |
| <span data-ttu-id="61920-264">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="61920-264">NT-Security-Descriptor</span></span> | <span data-ttu-id="61920-265">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="61920-265">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="61920-266">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="61920-266">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="61920-267">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="61920-267">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="61920-268">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="61920-268">Search-Flags</span></span>           | <span data-ttu-id="61920-269">0x00000000</span><span class="sxs-lookup"><span data-stu-id="61920-269">0x00000000</span></span>                      |
| <span data-ttu-id="61920-270">System-Flags</span><span class="sxs-lookup"><span data-stu-id="61920-270">System-Flags</span></span>           | <span data-ttu-id="61920-271">0x00000013</span><span class="sxs-lookup"><span data-stu-id="61920-271">0x00000013</span></span>                      |
| <span data-ttu-id="61920-272">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="61920-272">Classes used in</span></span>        | [<span data-ttu-id="61920-273">**In alto**</span><span class="sxs-lookup"><span data-stu-id="61920-273">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="61920-274">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="61920-274">Windows Server 2012</span></span>



| <span data-ttu-id="61920-275">Voce</span><span class="sxs-lookup"><span data-stu-id="61920-275">Entry</span></span> | <span data-ttu-id="61920-276">Valore</span><span class="sxs-lookup"><span data-stu-id="61920-276">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="61920-277">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="61920-277">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="61920-278">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="61920-278">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="61920-279">System-Only</span><span class="sxs-lookup"><span data-stu-id="61920-279">System-Only</span></span>            | <span data-ttu-id="61920-280">Vero</span><span class="sxs-lookup"><span data-stu-id="61920-280">True</span></span>                            |
| <span data-ttu-id="61920-281">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="61920-281">Is-Single-Valued</span></span>       | <span data-ttu-id="61920-282">Vero</span><span class="sxs-lookup"><span data-stu-id="61920-282">True</span></span>                            |
| <span data-ttu-id="61920-283">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="61920-283">Is Indexed</span></span>             | <span data-ttu-id="61920-284">Falso</span><span class="sxs-lookup"><span data-stu-id="61920-284">False</span></span>                           |
| <span data-ttu-id="61920-285">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="61920-285">In Global Catalog</span></span>      | <span data-ttu-id="61920-286">Vero</span><span class="sxs-lookup"><span data-stu-id="61920-286">True</span></span>                            |
| <span data-ttu-id="61920-287">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="61920-287">NT-Security-Descriptor</span></span> | <span data-ttu-id="61920-288">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="61920-288">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="61920-289">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="61920-289">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="61920-290">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="61920-290">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="61920-291">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="61920-291">Search-Flags</span></span>           | <span data-ttu-id="61920-292">0x00000000</span><span class="sxs-lookup"><span data-stu-id="61920-292">0x00000000</span></span>                      |
| <span data-ttu-id="61920-293">System-Flags</span><span class="sxs-lookup"><span data-stu-id="61920-293">System-Flags</span></span>           | <span data-ttu-id="61920-294">0x00000013</span><span class="sxs-lookup"><span data-stu-id="61920-294">0x00000013</span></span>                      |
| <span data-ttu-id="61920-295">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="61920-295">Classes used in</span></span>        | [<span data-ttu-id="61920-296">**In alto**</span><span class="sxs-lookup"><span data-stu-id="61920-296">**Top**</span></span>](c-top.md)<br/> |



 

 





