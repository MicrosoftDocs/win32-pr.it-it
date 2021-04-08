---
title: Modifica attributo timestamp
description: Attributo calcolato che rappresenta la data dell'Ultima modifica apportata all'oggetto. Questo valore non viene replicato.
ms.assetid: ad8fea90-9a78-484d-9549-26d78e87ec44
ms.tgt_platform: multiple
keywords:
- Modifica dello schema AD dell'attributo Time-Stamp
- Schema AD dell'attributo modifyTimeStamp
topic_type:
- apiref
api_name:
- Modify-Time-Stamp
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48c032d19c3bd2bf5a6ee0cfe038e9fa9b184d36
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744338"
---
# <a name="modify-time-stamp-attribute"></a><span data-ttu-id="49c57-106">Modifica attributo timestamp</span><span class="sxs-lookup"><span data-stu-id="49c57-106">Modify-Time-Stamp attribute</span></span>

<span data-ttu-id="49c57-107">Attributo calcolato che rappresenta la data dell'Ultima modifica apportata all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="49c57-107">A computed attribute that represents the date when this object was last changed.</span></span> <span data-ttu-id="49c57-108">Questo valore non viene replicato.</span><span class="sxs-lookup"><span data-stu-id="49c57-108">This value is not replicated.</span></span>



| <span data-ttu-id="49c57-109">Voce</span><span class="sxs-lookup"><span data-stu-id="49c57-109">Entry</span></span> | <span data-ttu-id="49c57-110">Valore</span><span class="sxs-lookup"><span data-stu-id="49c57-110">Value</span></span> |
|-------------------|---------------------------------------------------------------|
| <span data-ttu-id="49c57-111">CN</span><span class="sxs-lookup"><span data-stu-id="49c57-111">CN</span></span>                | <span data-ttu-id="49c57-112">Modifica-timestamp</span><span class="sxs-lookup"><span data-stu-id="49c57-112">Modify-Time-Stamp</span></span>                                             |
| <span data-ttu-id="49c57-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="49c57-113">Ldap-Display-Name</span></span> | <span data-ttu-id="49c57-114">modifyTimeStamp</span><span class="sxs-lookup"><span data-stu-id="49c57-114">modifyTimeStamp</span></span>                                               |
| <span data-ttu-id="49c57-115">Dimensione</span><span class="sxs-lookup"><span data-stu-id="49c57-115">Size</span></span>              | <span data-ttu-id="49c57-116">8 byte</span><span class="sxs-lookup"><span data-stu-id="49c57-116">8 bytes</span></span>                                                       |
| <span data-ttu-id="49c57-117">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="49c57-117">Update Privilege</span></span>  | <span data-ttu-id="49c57-118">Questo valore viene impostato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="49c57-118">This value is set by the system.</span></span>                              |
| <span data-ttu-id="49c57-119">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="49c57-119">Update Frequency</span></span>  | \-                                                            |
| <span data-ttu-id="49c57-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="49c57-120">Attribute-Id</span></span>      | <span data-ttu-id="49c57-121">2.5.18.2</span><span class="sxs-lookup"><span data-stu-id="49c57-121">2.5.18.2</span></span>                                                      |
| <span data-ttu-id="49c57-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="49c57-122">System-Id-Guid</span></span>    | <span data-ttu-id="49c57-123">9a7ad94a-ca53-11d1-bbd0-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="49c57-123">9a7ad94a-ca53-11d1-bbd0-0080c76670c0</span></span>                          |
| <span data-ttu-id="49c57-124">Sintassi</span><span class="sxs-lookup"><span data-stu-id="49c57-124">Syntax</span></span>            | [<span data-ttu-id="49c57-125">**String(Generalized-Time)**</span><span class="sxs-lookup"><span data-stu-id="49c57-125">**String(Generalized-Time)**</span></span>](s-string-generalized-time.md) |



## <a name="implementations"></a><span data-ttu-id="49c57-126">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="49c57-126">Implementations</span></span>

-   [<span data-ttu-id="49c57-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="49c57-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="49c57-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="49c57-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="49c57-129">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="49c57-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="49c57-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="49c57-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="49c57-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="49c57-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="49c57-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="49c57-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="49c57-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="49c57-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="49c57-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="49c57-134">Windows 2000 Server</span></span>



| <span data-ttu-id="49c57-135">Voce</span><span class="sxs-lookup"><span data-stu-id="49c57-135">Entry</span></span> | <span data-ttu-id="49c57-136">Valore</span><span class="sxs-lookup"><span data-stu-id="49c57-136">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="49c57-137">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="49c57-137">Link-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="49c57-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="49c57-138">MAPI-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="49c57-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="49c57-139">System-Only</span></span>            | <span data-ttu-id="49c57-140">Vero</span><span class="sxs-lookup"><span data-stu-id="49c57-140">True</span></span>                                                                        |
| <span data-ttu-id="49c57-141">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="49c57-141">Is-Single-Valued</span></span>       | <span data-ttu-id="49c57-142">Vero</span><span class="sxs-lookup"><span data-stu-id="49c57-142">True</span></span>                                                                        |
| <span data-ttu-id="49c57-143">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="49c57-143">Is Indexed</span></span>             | <span data-ttu-id="49c57-144">Falso</span><span class="sxs-lookup"><span data-stu-id="49c57-144">False</span></span>                                                                       |
| <span data-ttu-id="49c57-145">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="49c57-145">In Global Catalog</span></span>      | <span data-ttu-id="49c57-146">Falso</span><span class="sxs-lookup"><span data-stu-id="49c57-146">False</span></span>                                                                       |
| <span data-ttu-id="49c57-147">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="49c57-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="49c57-148">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="49c57-148">O:BAG:BAD:S:</span></span>                                                                |
| <span data-ttu-id="49c57-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="49c57-149">Range-Lower</span></span>            | \-                                                                          |
| <span data-ttu-id="49c57-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="49c57-150">Range-Upper</span></span>            | \-                                                                          |
| <span data-ttu-id="49c57-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="49c57-151">Search-Flags</span></span>           | <span data-ttu-id="49c57-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="49c57-152">0x00000000</span></span>                                                                  |
| <span data-ttu-id="49c57-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="49c57-153">System-Flags</span></span>           | <span data-ttu-id="49c57-154">0x08000014</span><span class="sxs-lookup"><span data-stu-id="49c57-154">0x08000014</span></span>                                                                  |
| <span data-ttu-id="49c57-155">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="49c57-155">Classes used in</span></span>        | [<span data-ttu-id="49c57-156">**Sottoschema**</span><span class="sxs-lookup"><span data-stu-id="49c57-156">**SubSchema**</span></span>](c-subschema.md)<br/> [<span data-ttu-id="49c57-157">**In alto**</span><span class="sxs-lookup"><span data-stu-id="49c57-157">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="49c57-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="49c57-158">Windows Server 2003</span></span>



| <span data-ttu-id="49c57-159">Voce</span><span class="sxs-lookup"><span data-stu-id="49c57-159">Entry</span></span> | <span data-ttu-id="49c57-160">Valore</span><span class="sxs-lookup"><span data-stu-id="49c57-160">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="49c57-161">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="49c57-161">Link-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="49c57-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="49c57-162">MAPI-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="49c57-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="49c57-163">System-Only</span></span>            | <span data-ttu-id="49c57-164">Vero</span><span class="sxs-lookup"><span data-stu-id="49c57-164">True</span></span>                                                                        |
| <span data-ttu-id="49c57-165">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="49c57-165">Is-Single-Valued</span></span>       | <span data-ttu-id="49c57-166">Vero</span><span class="sxs-lookup"><span data-stu-id="49c57-166">True</span></span>                                                                        |
| <span data-ttu-id="49c57-167">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="49c57-167">Is Indexed</span></span>             | <span data-ttu-id="49c57-168">Falso</span><span class="sxs-lookup"><span data-stu-id="49c57-168">False</span></span>                                                                       |
| <span data-ttu-id="49c57-169">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="49c57-169">In Global Catalog</span></span>      | <span data-ttu-id="49c57-170">Falso</span><span class="sxs-lookup"><span data-stu-id="49c57-170">False</span></span>                                                                       |
| <span data-ttu-id="49c57-171">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="49c57-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="49c57-172">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="49c57-172">O:BAG:BAD:S:</span></span>                                                                |
| <span data-ttu-id="49c57-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="49c57-173">Range-Lower</span></span>            | \-                                                                          |
| <span data-ttu-id="49c57-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="49c57-174">Range-Upper</span></span>            | \-                                                                          |
| <span data-ttu-id="49c57-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="49c57-175">Search-Flags</span></span>           | <span data-ttu-id="49c57-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="49c57-176">0x00000000</span></span>                                                                  |
| <span data-ttu-id="49c57-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="49c57-177">System-Flags</span></span>           | <span data-ttu-id="49c57-178">0x08000014</span><span class="sxs-lookup"><span data-stu-id="49c57-178">0x08000014</span></span>                                                                  |
| <span data-ttu-id="49c57-179">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="49c57-179">Classes used in</span></span>        | [<span data-ttu-id="49c57-180">**Sottoschema**</span><span class="sxs-lookup"><span data-stu-id="49c57-180">**SubSchema**</span></span>](c-subschema.md)<br/> [<span data-ttu-id="49c57-181">**In alto**</span><span class="sxs-lookup"><span data-stu-id="49c57-181">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="49c57-182">ADAM</span><span class="sxs-lookup"><span data-stu-id="49c57-182">ADAM</span></span>



| <span data-ttu-id="49c57-183">Voce</span><span class="sxs-lookup"><span data-stu-id="49c57-183">Entry</span></span> | <span data-ttu-id="49c57-184">Valore</span><span class="sxs-lookup"><span data-stu-id="49c57-184">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="49c57-185">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="49c57-185">Link-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="49c57-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="49c57-186">MAPI-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="49c57-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="49c57-187">System-Only</span></span>            | <span data-ttu-id="49c57-188">Vero</span><span class="sxs-lookup"><span data-stu-id="49c57-188">True</span></span>                                                                        |
| <span data-ttu-id="49c57-189">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="49c57-189">Is-Single-Valued</span></span>       | <span data-ttu-id="49c57-190">Vero</span><span class="sxs-lookup"><span data-stu-id="49c57-190">True</span></span>                                                                        |
| <span data-ttu-id="49c57-191">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="49c57-191">Is Indexed</span></span>             | <span data-ttu-id="49c57-192">Falso</span><span class="sxs-lookup"><span data-stu-id="49c57-192">False</span></span>                                                                       |
| <span data-ttu-id="49c57-193">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="49c57-193">In Global Catalog</span></span>      | <span data-ttu-id="49c57-194">Falso</span><span class="sxs-lookup"><span data-stu-id="49c57-194">False</span></span>                                                                       |
| <span data-ttu-id="49c57-195">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="49c57-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="49c57-196">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="49c57-196">O:BAG:BAD:S:</span></span>                                                                |
| <span data-ttu-id="49c57-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="49c57-197">Range-Lower</span></span>            | \-                                                                          |
| <span data-ttu-id="49c57-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="49c57-198">Range-Upper</span></span>            | \-                                                                          |
| <span data-ttu-id="49c57-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="49c57-199">Search-Flags</span></span>           | <span data-ttu-id="49c57-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="49c57-200">0x00000000</span></span>                                                                  |
| <span data-ttu-id="49c57-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="49c57-201">System-Flags</span></span>           | <span data-ttu-id="49c57-202">0x08000014</span><span class="sxs-lookup"><span data-stu-id="49c57-202">0x08000014</span></span>                                                                  |
| <span data-ttu-id="49c57-203">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="49c57-203">Classes used in</span></span>        | [<span data-ttu-id="49c57-204">**Sottoschema**</span><span class="sxs-lookup"><span data-stu-id="49c57-204">**SubSchema**</span></span>](c-subschema.md)<br/> [<span data-ttu-id="49c57-205">**In alto**</span><span class="sxs-lookup"><span data-stu-id="49c57-205">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="49c57-206">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="49c57-206">Windows Server 2003 R2</span></span>



| <span data-ttu-id="49c57-207">Voce</span><span class="sxs-lookup"><span data-stu-id="49c57-207">Entry</span></span> | <span data-ttu-id="49c57-208">Valore</span><span class="sxs-lookup"><span data-stu-id="49c57-208">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="49c57-209">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="49c57-209">Link-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="49c57-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="49c57-210">MAPI-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="49c57-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="49c57-211">System-Only</span></span>            | <span data-ttu-id="49c57-212">Vero</span><span class="sxs-lookup"><span data-stu-id="49c57-212">True</span></span>                                                                        |
| <span data-ttu-id="49c57-213">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="49c57-213">Is-Single-Valued</span></span>       | <span data-ttu-id="49c57-214">Vero</span><span class="sxs-lookup"><span data-stu-id="49c57-214">True</span></span>                                                                        |
| <span data-ttu-id="49c57-215">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="49c57-215">Is Indexed</span></span>             | <span data-ttu-id="49c57-216">Falso</span><span class="sxs-lookup"><span data-stu-id="49c57-216">False</span></span>                                                                       |
| <span data-ttu-id="49c57-217">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="49c57-217">In Global Catalog</span></span>      | <span data-ttu-id="49c57-218">Falso</span><span class="sxs-lookup"><span data-stu-id="49c57-218">False</span></span>                                                                       |
| <span data-ttu-id="49c57-219">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="49c57-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="49c57-220">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="49c57-220">O:BAG:BAD:S:</span></span>                                                                |
| <span data-ttu-id="49c57-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="49c57-221">Range-Lower</span></span>            | \-                                                                          |
| <span data-ttu-id="49c57-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="49c57-222">Range-Upper</span></span>            | \-                                                                          |
| <span data-ttu-id="49c57-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="49c57-223">Search-Flags</span></span>           | <span data-ttu-id="49c57-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="49c57-224">0x00000000</span></span>                                                                  |
| <span data-ttu-id="49c57-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="49c57-225">System-Flags</span></span>           | <span data-ttu-id="49c57-226">0x08000014</span><span class="sxs-lookup"><span data-stu-id="49c57-226">0x08000014</span></span>                                                                  |
| <span data-ttu-id="49c57-227">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="49c57-227">Classes used in</span></span>        | [<span data-ttu-id="49c57-228">**Sottoschema**</span><span class="sxs-lookup"><span data-stu-id="49c57-228">**SubSchema**</span></span>](c-subschema.md)<br/> [<span data-ttu-id="49c57-229">**In alto**</span><span class="sxs-lookup"><span data-stu-id="49c57-229">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="49c57-230">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="49c57-230">Windows Server 2008</span></span>



| <span data-ttu-id="49c57-231">Voce</span><span class="sxs-lookup"><span data-stu-id="49c57-231">Entry</span></span> | <span data-ttu-id="49c57-232">Valore</span><span class="sxs-lookup"><span data-stu-id="49c57-232">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="49c57-233">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="49c57-233">Link-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="49c57-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="49c57-234">MAPI-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="49c57-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="49c57-235">System-Only</span></span>            | <span data-ttu-id="49c57-236">Vero</span><span class="sxs-lookup"><span data-stu-id="49c57-236">True</span></span>                                                                        |
| <span data-ttu-id="49c57-237">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="49c57-237">Is-Single-Valued</span></span>       | <span data-ttu-id="49c57-238">Vero</span><span class="sxs-lookup"><span data-stu-id="49c57-238">True</span></span>                                                                        |
| <span data-ttu-id="49c57-239">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="49c57-239">Is Indexed</span></span>             | <span data-ttu-id="49c57-240">Falso</span><span class="sxs-lookup"><span data-stu-id="49c57-240">False</span></span>                                                                       |
| <span data-ttu-id="49c57-241">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="49c57-241">In Global Catalog</span></span>      | <span data-ttu-id="49c57-242">Falso</span><span class="sxs-lookup"><span data-stu-id="49c57-242">False</span></span>                                                                       |
| <span data-ttu-id="49c57-243">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="49c57-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="49c57-244">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="49c57-244">O:BAG:BAD:S:</span></span>                                                                |
| <span data-ttu-id="49c57-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="49c57-245">Range-Lower</span></span>            | \-                                                                          |
| <span data-ttu-id="49c57-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="49c57-246">Range-Upper</span></span>            | \-                                                                          |
| <span data-ttu-id="49c57-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="49c57-247">Search-Flags</span></span>           | <span data-ttu-id="49c57-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="49c57-248">0x00000000</span></span>                                                                  |
| <span data-ttu-id="49c57-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="49c57-249">System-Flags</span></span>           | <span data-ttu-id="49c57-250">0x08000014</span><span class="sxs-lookup"><span data-stu-id="49c57-250">0x08000014</span></span>                                                                  |
| <span data-ttu-id="49c57-251">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="49c57-251">Classes used in</span></span>        | [<span data-ttu-id="49c57-252">**Sottoschema**</span><span class="sxs-lookup"><span data-stu-id="49c57-252">**SubSchema**</span></span>](c-subschema.md)<br/> [<span data-ttu-id="49c57-253">**In alto**</span><span class="sxs-lookup"><span data-stu-id="49c57-253">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="49c57-254">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="49c57-254">Windows Server 2008 R2</span></span>



| <span data-ttu-id="49c57-255">Voce</span><span class="sxs-lookup"><span data-stu-id="49c57-255">Entry</span></span> | <span data-ttu-id="49c57-256">Valore</span><span class="sxs-lookup"><span data-stu-id="49c57-256">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="49c57-257">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="49c57-257">Link-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="49c57-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="49c57-258">MAPI-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="49c57-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="49c57-259">System-Only</span></span>            | <span data-ttu-id="49c57-260">Vero</span><span class="sxs-lookup"><span data-stu-id="49c57-260">True</span></span>                                                                        |
| <span data-ttu-id="49c57-261">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="49c57-261">Is-Single-Valued</span></span>       | <span data-ttu-id="49c57-262">Vero</span><span class="sxs-lookup"><span data-stu-id="49c57-262">True</span></span>                                                                        |
| <span data-ttu-id="49c57-263">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="49c57-263">Is Indexed</span></span>             | <span data-ttu-id="49c57-264">Falso</span><span class="sxs-lookup"><span data-stu-id="49c57-264">False</span></span>                                                                       |
| <span data-ttu-id="49c57-265">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="49c57-265">In Global Catalog</span></span>      | <span data-ttu-id="49c57-266">Falso</span><span class="sxs-lookup"><span data-stu-id="49c57-266">False</span></span>                                                                       |
| <span data-ttu-id="49c57-267">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="49c57-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="49c57-268">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="49c57-268">O:BAG:BAD:S:</span></span>                                                                |
| <span data-ttu-id="49c57-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="49c57-269">Range-Lower</span></span>            | \-                                                                          |
| <span data-ttu-id="49c57-270">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="49c57-270">Range-Upper</span></span>            | \-                                                                          |
| <span data-ttu-id="49c57-271">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="49c57-271">Search-Flags</span></span>           | <span data-ttu-id="49c57-272">0x00000000</span><span class="sxs-lookup"><span data-stu-id="49c57-272">0x00000000</span></span>                                                                  |
| <span data-ttu-id="49c57-273">System-Flags</span><span class="sxs-lookup"><span data-stu-id="49c57-273">System-Flags</span></span>           | <span data-ttu-id="49c57-274">0x08000014</span><span class="sxs-lookup"><span data-stu-id="49c57-274">0x08000014</span></span>                                                                  |
| <span data-ttu-id="49c57-275">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="49c57-275">Classes used in</span></span>        | [<span data-ttu-id="49c57-276">**Sottoschema**</span><span class="sxs-lookup"><span data-stu-id="49c57-276">**SubSchema**</span></span>](c-subschema.md)<br/> [<span data-ttu-id="49c57-277">**In alto**</span><span class="sxs-lookup"><span data-stu-id="49c57-277">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="49c57-278">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="49c57-278">Windows Server 2012</span></span>



| <span data-ttu-id="49c57-279">Voce</span><span class="sxs-lookup"><span data-stu-id="49c57-279">Entry</span></span> | <span data-ttu-id="49c57-280">Valore</span><span class="sxs-lookup"><span data-stu-id="49c57-280">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="49c57-281">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="49c57-281">Link-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="49c57-282">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="49c57-282">MAPI-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="49c57-283">System-Only</span><span class="sxs-lookup"><span data-stu-id="49c57-283">System-Only</span></span>            | <span data-ttu-id="49c57-284">Vero</span><span class="sxs-lookup"><span data-stu-id="49c57-284">True</span></span>                                                                        |
| <span data-ttu-id="49c57-285">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="49c57-285">Is-Single-Valued</span></span>       | <span data-ttu-id="49c57-286">Vero</span><span class="sxs-lookup"><span data-stu-id="49c57-286">True</span></span>                                                                        |
| <span data-ttu-id="49c57-287">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="49c57-287">Is Indexed</span></span>             | <span data-ttu-id="49c57-288">Falso</span><span class="sxs-lookup"><span data-stu-id="49c57-288">False</span></span>                                                                       |
| <span data-ttu-id="49c57-289">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="49c57-289">In Global Catalog</span></span>      | <span data-ttu-id="49c57-290">Falso</span><span class="sxs-lookup"><span data-stu-id="49c57-290">False</span></span>                                                                       |
| <span data-ttu-id="49c57-291">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="49c57-291">NT-Security-Descriptor</span></span> | <span data-ttu-id="49c57-292">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="49c57-292">O:BAG:BAD:S:</span></span>                                                                |
| <span data-ttu-id="49c57-293">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="49c57-293">Range-Lower</span></span>            | \-                                                                          |
| <span data-ttu-id="49c57-294">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="49c57-294">Range-Upper</span></span>            | \-                                                                          |
| <span data-ttu-id="49c57-295">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="49c57-295">Search-Flags</span></span>           | <span data-ttu-id="49c57-296">0x00000000</span><span class="sxs-lookup"><span data-stu-id="49c57-296">0x00000000</span></span>                                                                  |
| <span data-ttu-id="49c57-297">System-Flags</span><span class="sxs-lookup"><span data-stu-id="49c57-297">System-Flags</span></span>           | <span data-ttu-id="49c57-298">0x08000014</span><span class="sxs-lookup"><span data-stu-id="49c57-298">0x08000014</span></span>                                                                  |
| <span data-ttu-id="49c57-299">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="49c57-299">Classes used in</span></span>        | [<span data-ttu-id="49c57-300">**Sottoschema**</span><span class="sxs-lookup"><span data-stu-id="49c57-300">**SubSchema**</span></span>](c-subschema.md)<br/> [<span data-ttu-id="49c57-301">**In alto**</span><span class="sxs-lookup"><span data-stu-id="49c57-301">**Top**</span></span>](c-top.md)<br/> |



 

 





