---
title: Attributo partial-set
description: Tiene traccia dello stato di replica interno delle repliche parziali, ovvero nei cataloghi globali. Attributo dell'oggetto NC della replica parziale. Definisce il set di attributi presenti in un particolare NC della replica parziale.
ms.assetid: 2840d2b7-e186-4ef2-9107-f1e5c0c2f760
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo set di attributi parziali
- Schema AD dell'attributo partialAttributeSet
topic_type:
- apiref
api_name:
- Partial-Attribute-Set
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e932c07b0d4a8e3ea8f30f504194093d61912b7b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "106303390"
---
# <a name="partial-attribute-set-attribute"></a><span data-ttu-id="2ebd1-107">Attributo partial-set</span><span class="sxs-lookup"><span data-stu-id="2ebd1-107">Partial-Attribute-Set attribute</span></span>

<span data-ttu-id="2ebd1-108">Tiene traccia dello stato di replica interno delle repliche parziali, ovvero nei cataloghi globali.</span><span class="sxs-lookup"><span data-stu-id="2ebd1-108">Tracks the internal replication state of partial replicas (that is, on GCs).</span></span> <span data-ttu-id="2ebd1-109">Attributo dell'oggetto NC della replica parziale.</span><span class="sxs-lookup"><span data-stu-id="2ebd1-109">Attribute of the partial replica NC object.</span></span> <span data-ttu-id="2ebd1-110">Definisce il set di attributi presenti in un particolare NC della replica parziale.</span><span class="sxs-lookup"><span data-stu-id="2ebd1-110">Defines the set of attributes present on a particular partial replica NC.</span></span>



| <span data-ttu-id="2ebd1-111">Voce</span><span class="sxs-lookup"><span data-stu-id="2ebd1-111">Entry</span></span> | <span data-ttu-id="2ebd1-112">Valore</span><span class="sxs-lookup"><span data-stu-id="2ebd1-112">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="2ebd1-113">CN</span><span class="sxs-lookup"><span data-stu-id="2ebd1-113">CN</span></span>                | <span data-ttu-id="2ebd1-114">Set di attributi parziali</span><span class="sxs-lookup"><span data-stu-id="2ebd1-114">Partial-Attribute-Set</span></span>                                 |
| <span data-ttu-id="2ebd1-115">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="2ebd1-115">Ldap-Display-Name</span></span> | <span data-ttu-id="2ebd1-116">partialAttributeSet</span><span class="sxs-lookup"><span data-stu-id="2ebd1-116">partialAttributeSet</span></span>                                   |
| <span data-ttu-id="2ebd1-117">Dimensione</span><span class="sxs-lookup"><span data-stu-id="2ebd1-117">Size</span></span>              | \-                                                    |
| <span data-ttu-id="2ebd1-118">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="2ebd1-118">Update Privilege</span></span>  | <span data-ttu-id="2ebd1-119">Questo valore viene impostato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="2ebd1-119">This value is set by the system.</span></span>                      |
| <span data-ttu-id="2ebd1-120">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="2ebd1-120">Update Frequency</span></span>  | <span data-ttu-id="2ebd1-121">Durante la replica</span><span class="sxs-lookup"><span data-stu-id="2ebd1-121">During replication</span></span>                                    |
| <span data-ttu-id="2ebd1-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="2ebd1-122">Attribute-Id</span></span>      | <span data-ttu-id="2ebd1-123">1.2.840.113556.1.4.640</span><span class="sxs-lookup"><span data-stu-id="2ebd1-123">1.2.840.113556.1.4.640</span></span>                                |
| <span data-ttu-id="2ebd1-124">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="2ebd1-124">System-Id-Guid</span></span>    | <span data-ttu-id="2ebd1-125">19405b9e-3cfa-11d1-a9c0-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="2ebd1-125">19405b9e-3cfa-11d1-a9c0-0000f80367c1</span></span>                  |
| <span data-ttu-id="2ebd1-126">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2ebd1-126">Syntax</span></span>            | [<span data-ttu-id="2ebd1-127">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="2ebd1-127">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="2ebd1-128">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="2ebd1-128">Implementations</span></span>

-   [<span data-ttu-id="2ebd1-129">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="2ebd1-129">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="2ebd1-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="2ebd1-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="2ebd1-131">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="2ebd1-131">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="2ebd1-132">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="2ebd1-132">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="2ebd1-133">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="2ebd1-133">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="2ebd1-134">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="2ebd1-134">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="2ebd1-135">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="2ebd1-135">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="2ebd1-136">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2ebd1-136">Windows 2000 Server</span></span>



| <span data-ttu-id="2ebd1-137">Voce</span><span class="sxs-lookup"><span data-stu-id="2ebd1-137">Entry</span></span> | <span data-ttu-id="2ebd1-138">Valore</span><span class="sxs-lookup"><span data-stu-id="2ebd1-138">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="2ebd1-139">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="2ebd1-139">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="2ebd1-140">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2ebd1-140">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="2ebd1-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="2ebd1-141">System-Only</span></span>            | <span data-ttu-id="2ebd1-142">Vero</span><span class="sxs-lookup"><span data-stu-id="2ebd1-142">True</span></span>                            |
| <span data-ttu-id="2ebd1-143">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="2ebd1-143">Is-Single-Valued</span></span>       | <span data-ttu-id="2ebd1-144">Vero</span><span class="sxs-lookup"><span data-stu-id="2ebd1-144">True</span></span>                            |
| <span data-ttu-id="2ebd1-145">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="2ebd1-145">Is Indexed</span></span>             | <span data-ttu-id="2ebd1-146">Falso</span><span class="sxs-lookup"><span data-stu-id="2ebd1-146">False</span></span>                           |
| <span data-ttu-id="2ebd1-147">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="2ebd1-147">In Global Catalog</span></span>      | <span data-ttu-id="2ebd1-148">Vero</span><span class="sxs-lookup"><span data-stu-id="2ebd1-148">True</span></span>                            |
| <span data-ttu-id="2ebd1-149">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="2ebd1-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="2ebd1-150">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="2ebd1-150">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="2ebd1-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2ebd1-151">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="2ebd1-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2ebd1-152">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="2ebd1-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2ebd1-153">Search-Flags</span></span>           | <span data-ttu-id="2ebd1-154">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2ebd1-154">0x00000000</span></span>                      |
| <span data-ttu-id="2ebd1-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2ebd1-155">System-Flags</span></span>           | <span data-ttu-id="2ebd1-156">0x00000013</span><span class="sxs-lookup"><span data-stu-id="2ebd1-156">0x00000013</span></span>                      |
| <span data-ttu-id="2ebd1-157">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="2ebd1-157">Classes used in</span></span>        | [<span data-ttu-id="2ebd1-158">**In alto**</span><span class="sxs-lookup"><span data-stu-id="2ebd1-158">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="2ebd1-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2ebd1-159">Windows Server 2003</span></span>



| <span data-ttu-id="2ebd1-160">Voce</span><span class="sxs-lookup"><span data-stu-id="2ebd1-160">Entry</span></span> | <span data-ttu-id="2ebd1-161">Valore</span><span class="sxs-lookup"><span data-stu-id="2ebd1-161">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="2ebd1-162">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="2ebd1-162">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="2ebd1-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2ebd1-163">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="2ebd1-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="2ebd1-164">System-Only</span></span>            | <span data-ttu-id="2ebd1-165">Vero</span><span class="sxs-lookup"><span data-stu-id="2ebd1-165">True</span></span>                            |
| <span data-ttu-id="2ebd1-166">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="2ebd1-166">Is-Single-Valued</span></span>       | <span data-ttu-id="2ebd1-167">Vero</span><span class="sxs-lookup"><span data-stu-id="2ebd1-167">True</span></span>                            |
| <span data-ttu-id="2ebd1-168">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="2ebd1-168">Is Indexed</span></span>             | <span data-ttu-id="2ebd1-169">Falso</span><span class="sxs-lookup"><span data-stu-id="2ebd1-169">False</span></span>                           |
| <span data-ttu-id="2ebd1-170">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="2ebd1-170">In Global Catalog</span></span>      | <span data-ttu-id="2ebd1-171">Vero</span><span class="sxs-lookup"><span data-stu-id="2ebd1-171">True</span></span>                            |
| <span data-ttu-id="2ebd1-172">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="2ebd1-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="2ebd1-173">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="2ebd1-173">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="2ebd1-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2ebd1-174">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="2ebd1-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2ebd1-175">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="2ebd1-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2ebd1-176">Search-Flags</span></span>           | <span data-ttu-id="2ebd1-177">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2ebd1-177">0x00000000</span></span>                      |
| <span data-ttu-id="2ebd1-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2ebd1-178">System-Flags</span></span>           | <span data-ttu-id="2ebd1-179">0x00000013</span><span class="sxs-lookup"><span data-stu-id="2ebd1-179">0x00000013</span></span>                      |
| <span data-ttu-id="2ebd1-180">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="2ebd1-180">Classes used in</span></span>        | [<span data-ttu-id="2ebd1-181">**In alto**</span><span class="sxs-lookup"><span data-stu-id="2ebd1-181">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="2ebd1-182">ADAM</span><span class="sxs-lookup"><span data-stu-id="2ebd1-182">ADAM</span></span>



| <span data-ttu-id="2ebd1-183">Voce</span><span class="sxs-lookup"><span data-stu-id="2ebd1-183">Entry</span></span> | <span data-ttu-id="2ebd1-184">Valore</span><span class="sxs-lookup"><span data-stu-id="2ebd1-184">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="2ebd1-185">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="2ebd1-185">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="2ebd1-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2ebd1-186">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="2ebd1-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="2ebd1-187">System-Only</span></span>            | <span data-ttu-id="2ebd1-188">Vero</span><span class="sxs-lookup"><span data-stu-id="2ebd1-188">True</span></span>                            |
| <span data-ttu-id="2ebd1-189">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="2ebd1-189">Is-Single-Valued</span></span>       | <span data-ttu-id="2ebd1-190">Vero</span><span class="sxs-lookup"><span data-stu-id="2ebd1-190">True</span></span>                            |
| <span data-ttu-id="2ebd1-191">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="2ebd1-191">Is Indexed</span></span>             | <span data-ttu-id="2ebd1-192">Falso</span><span class="sxs-lookup"><span data-stu-id="2ebd1-192">False</span></span>                           |
| <span data-ttu-id="2ebd1-193">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="2ebd1-193">In Global Catalog</span></span>      | <span data-ttu-id="2ebd1-194">Vero</span><span class="sxs-lookup"><span data-stu-id="2ebd1-194">True</span></span>                            |
| <span data-ttu-id="2ebd1-195">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="2ebd1-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="2ebd1-196">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="2ebd1-196">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="2ebd1-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2ebd1-197">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="2ebd1-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2ebd1-198">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="2ebd1-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2ebd1-199">Search-Flags</span></span>           | <span data-ttu-id="2ebd1-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2ebd1-200">0x00000000</span></span>                      |
| <span data-ttu-id="2ebd1-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2ebd1-201">System-Flags</span></span>           | <span data-ttu-id="2ebd1-202">0x00000013</span><span class="sxs-lookup"><span data-stu-id="2ebd1-202">0x00000013</span></span>                      |
| <span data-ttu-id="2ebd1-203">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="2ebd1-203">Classes used in</span></span>        | [<span data-ttu-id="2ebd1-204">**In alto**</span><span class="sxs-lookup"><span data-stu-id="2ebd1-204">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="2ebd1-205">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="2ebd1-205">Windows Server 2003 R2</span></span>



| <span data-ttu-id="2ebd1-206">Voce</span><span class="sxs-lookup"><span data-stu-id="2ebd1-206">Entry</span></span> | <span data-ttu-id="2ebd1-207">Valore</span><span class="sxs-lookup"><span data-stu-id="2ebd1-207">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="2ebd1-208">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="2ebd1-208">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="2ebd1-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2ebd1-209">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="2ebd1-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="2ebd1-210">System-Only</span></span>            | <span data-ttu-id="2ebd1-211">Vero</span><span class="sxs-lookup"><span data-stu-id="2ebd1-211">True</span></span>                            |
| <span data-ttu-id="2ebd1-212">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="2ebd1-212">Is-Single-Valued</span></span>       | <span data-ttu-id="2ebd1-213">Vero</span><span class="sxs-lookup"><span data-stu-id="2ebd1-213">True</span></span>                            |
| <span data-ttu-id="2ebd1-214">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="2ebd1-214">Is Indexed</span></span>             | <span data-ttu-id="2ebd1-215">Falso</span><span class="sxs-lookup"><span data-stu-id="2ebd1-215">False</span></span>                           |
| <span data-ttu-id="2ebd1-216">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="2ebd1-216">In Global Catalog</span></span>      | <span data-ttu-id="2ebd1-217">Vero</span><span class="sxs-lookup"><span data-stu-id="2ebd1-217">True</span></span>                            |
| <span data-ttu-id="2ebd1-218">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="2ebd1-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="2ebd1-219">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="2ebd1-219">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="2ebd1-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2ebd1-220">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="2ebd1-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2ebd1-221">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="2ebd1-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2ebd1-222">Search-Flags</span></span>           | <span data-ttu-id="2ebd1-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2ebd1-223">0x00000000</span></span>                      |
| <span data-ttu-id="2ebd1-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2ebd1-224">System-Flags</span></span>           | <span data-ttu-id="2ebd1-225">0x00000013</span><span class="sxs-lookup"><span data-stu-id="2ebd1-225">0x00000013</span></span>                      |
| <span data-ttu-id="2ebd1-226">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="2ebd1-226">Classes used in</span></span>        | [<span data-ttu-id="2ebd1-227">**In alto**</span><span class="sxs-lookup"><span data-stu-id="2ebd1-227">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="2ebd1-228">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2ebd1-228">Windows Server 2008</span></span>



| <span data-ttu-id="2ebd1-229">Voce</span><span class="sxs-lookup"><span data-stu-id="2ebd1-229">Entry</span></span> | <span data-ttu-id="2ebd1-230">Valore</span><span class="sxs-lookup"><span data-stu-id="2ebd1-230">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="2ebd1-231">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="2ebd1-231">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="2ebd1-232">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2ebd1-232">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="2ebd1-233">System-Only</span><span class="sxs-lookup"><span data-stu-id="2ebd1-233">System-Only</span></span>            | <span data-ttu-id="2ebd1-234">Vero</span><span class="sxs-lookup"><span data-stu-id="2ebd1-234">True</span></span>                            |
| <span data-ttu-id="2ebd1-235">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="2ebd1-235">Is-Single-Valued</span></span>       | <span data-ttu-id="2ebd1-236">Vero</span><span class="sxs-lookup"><span data-stu-id="2ebd1-236">True</span></span>                            |
| <span data-ttu-id="2ebd1-237">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="2ebd1-237">Is Indexed</span></span>             | <span data-ttu-id="2ebd1-238">Falso</span><span class="sxs-lookup"><span data-stu-id="2ebd1-238">False</span></span>                           |
| <span data-ttu-id="2ebd1-239">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="2ebd1-239">In Global Catalog</span></span>      | <span data-ttu-id="2ebd1-240">Vero</span><span class="sxs-lookup"><span data-stu-id="2ebd1-240">True</span></span>                            |
| <span data-ttu-id="2ebd1-241">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="2ebd1-241">NT-Security-Descriptor</span></span> | <span data-ttu-id="2ebd1-242">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="2ebd1-242">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="2ebd1-243">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2ebd1-243">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="2ebd1-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2ebd1-244">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="2ebd1-245">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2ebd1-245">Search-Flags</span></span>           | <span data-ttu-id="2ebd1-246">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2ebd1-246">0x00000000</span></span>                      |
| <span data-ttu-id="2ebd1-247">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2ebd1-247">System-Flags</span></span>           | <span data-ttu-id="2ebd1-248">0x00000013</span><span class="sxs-lookup"><span data-stu-id="2ebd1-248">0x00000013</span></span>                      |
| <span data-ttu-id="2ebd1-249">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="2ebd1-249">Classes used in</span></span>        | [<span data-ttu-id="2ebd1-250">**In alto**</span><span class="sxs-lookup"><span data-stu-id="2ebd1-250">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="2ebd1-251">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2ebd1-251">Windows Server 2008 R2</span></span>



| <span data-ttu-id="2ebd1-252">Voce</span><span class="sxs-lookup"><span data-stu-id="2ebd1-252">Entry</span></span> | <span data-ttu-id="2ebd1-253">Valore</span><span class="sxs-lookup"><span data-stu-id="2ebd1-253">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="2ebd1-254">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="2ebd1-254">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="2ebd1-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2ebd1-255">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="2ebd1-256">System-Only</span><span class="sxs-lookup"><span data-stu-id="2ebd1-256">System-Only</span></span>            | <span data-ttu-id="2ebd1-257">Vero</span><span class="sxs-lookup"><span data-stu-id="2ebd1-257">True</span></span>                            |
| <span data-ttu-id="2ebd1-258">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="2ebd1-258">Is-Single-Valued</span></span>       | <span data-ttu-id="2ebd1-259">Vero</span><span class="sxs-lookup"><span data-stu-id="2ebd1-259">True</span></span>                            |
| <span data-ttu-id="2ebd1-260">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="2ebd1-260">Is Indexed</span></span>             | <span data-ttu-id="2ebd1-261">Falso</span><span class="sxs-lookup"><span data-stu-id="2ebd1-261">False</span></span>                           |
| <span data-ttu-id="2ebd1-262">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="2ebd1-262">In Global Catalog</span></span>      | <span data-ttu-id="2ebd1-263">Vero</span><span class="sxs-lookup"><span data-stu-id="2ebd1-263">True</span></span>                            |
| <span data-ttu-id="2ebd1-264">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="2ebd1-264">NT-Security-Descriptor</span></span> | <span data-ttu-id="2ebd1-265">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="2ebd1-265">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="2ebd1-266">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2ebd1-266">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="2ebd1-267">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2ebd1-267">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="2ebd1-268">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2ebd1-268">Search-Flags</span></span>           | <span data-ttu-id="2ebd1-269">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2ebd1-269">0x00000000</span></span>                      |
| <span data-ttu-id="2ebd1-270">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2ebd1-270">System-Flags</span></span>           | <span data-ttu-id="2ebd1-271">0x00000013</span><span class="sxs-lookup"><span data-stu-id="2ebd1-271">0x00000013</span></span>                      |
| <span data-ttu-id="2ebd1-272">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="2ebd1-272">Classes used in</span></span>        | [<span data-ttu-id="2ebd1-273">**In alto**</span><span class="sxs-lookup"><span data-stu-id="2ebd1-273">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="2ebd1-274">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2ebd1-274">Windows Server 2012</span></span>



| <span data-ttu-id="2ebd1-275">Voce</span><span class="sxs-lookup"><span data-stu-id="2ebd1-275">Entry</span></span> | <span data-ttu-id="2ebd1-276">Valore</span><span class="sxs-lookup"><span data-stu-id="2ebd1-276">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="2ebd1-277">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="2ebd1-277">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="2ebd1-278">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2ebd1-278">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="2ebd1-279">System-Only</span><span class="sxs-lookup"><span data-stu-id="2ebd1-279">System-Only</span></span>            | <span data-ttu-id="2ebd1-280">Vero</span><span class="sxs-lookup"><span data-stu-id="2ebd1-280">True</span></span>                            |
| <span data-ttu-id="2ebd1-281">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="2ebd1-281">Is-Single-Valued</span></span>       | <span data-ttu-id="2ebd1-282">Vero</span><span class="sxs-lookup"><span data-stu-id="2ebd1-282">True</span></span>                            |
| <span data-ttu-id="2ebd1-283">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="2ebd1-283">Is Indexed</span></span>             | <span data-ttu-id="2ebd1-284">Falso</span><span class="sxs-lookup"><span data-stu-id="2ebd1-284">False</span></span>                           |
| <span data-ttu-id="2ebd1-285">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="2ebd1-285">In Global Catalog</span></span>      | <span data-ttu-id="2ebd1-286">Vero</span><span class="sxs-lookup"><span data-stu-id="2ebd1-286">True</span></span>                            |
| <span data-ttu-id="2ebd1-287">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="2ebd1-287">NT-Security-Descriptor</span></span> | <span data-ttu-id="2ebd1-288">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="2ebd1-288">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="2ebd1-289">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2ebd1-289">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="2ebd1-290">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2ebd1-290">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="2ebd1-291">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2ebd1-291">Search-Flags</span></span>           | <span data-ttu-id="2ebd1-292">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2ebd1-292">0x00000000</span></span>                      |
| <span data-ttu-id="2ebd1-293">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2ebd1-293">System-Flags</span></span>           | <span data-ttu-id="2ebd1-294">0x00000013</span><span class="sxs-lookup"><span data-stu-id="2ebd1-294">0x00000013</span></span>                      |
| <span data-ttu-id="2ebd1-295">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="2ebd1-295">Classes used in</span></span>        | [<span data-ttu-id="2ebd1-296">**In alto**</span><span class="sxs-lookup"><span data-stu-id="2ebd1-296">**Top**</span></span>](c-top.md)<br/> |



 

 





