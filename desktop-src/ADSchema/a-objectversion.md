---
title: Attributo Object-Version
description: Questa operazione può essere utilizzata per archiviare un numero di versione per l'oggetto.
ms.assetid: 1aa8520b-c640-4ea2-9230-f28154bf69b0
ms.tgt_platform: multiple
keywords:
- Schema AD Object-Version attribute
- Schema AD dell'attributo objectVersion
topic_type:
- apiref
api_name:
- Object-Version
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f038f6286db575f4141c2e306086bb9a8faac71
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "106303399"
---
# <a name="object-version-attribute"></a><span data-ttu-id="ac460-105">Attributo Object-Version</span><span class="sxs-lookup"><span data-stu-id="ac460-105">Object-Version attribute</span></span>

<span data-ttu-id="ac460-106">Questa operazione può essere utilizzata per archiviare un numero di versione per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="ac460-106">This can be used to store a version number for the object.</span></span>



| <span data-ttu-id="ac460-107">Voce</span><span class="sxs-lookup"><span data-stu-id="ac460-107">Entry</span></span> | <span data-ttu-id="ac460-108">Valore</span><span class="sxs-lookup"><span data-stu-id="ac460-108">Value</span></span> |
|-------------------|----------------------------------------------------------------|
| <span data-ttu-id="ac460-109">CN</span><span class="sxs-lookup"><span data-stu-id="ac460-109">CN</span></span>                | <span data-ttu-id="ac460-110">Object-Version</span><span class="sxs-lookup"><span data-stu-id="ac460-110">Object-Version</span></span>                                                 |
| <span data-ttu-id="ac460-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="ac460-111">Ldap-Display-Name</span></span> | <span data-ttu-id="ac460-112">objectVersion</span><span class="sxs-lookup"><span data-stu-id="ac460-112">objectVersion</span></span>                                                  |
| <span data-ttu-id="ac460-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="ac460-113">Size</span></span>              | <span data-ttu-id="ac460-114">4 byte</span><span class="sxs-lookup"><span data-stu-id="ac460-114">4 bytes</span></span>                                                        |
| <span data-ttu-id="ac460-115">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="ac460-115">Update Privilege</span></span>  | <span data-ttu-id="ac460-116">Il valore verrà impostato dalla finestra di progettazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="ac460-116">The designer of the object would set this value.</span></span>               |
| <span data-ttu-id="ac460-117">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="ac460-117">Update Frequency</span></span>  | <span data-ttu-id="ac460-118">Questo valore deve essere incrementato ogni volta che l'oggetto viene modificato.</span><span class="sxs-lookup"><span data-stu-id="ac460-118">This value should be incremented each time the object changes.</span></span> |
| <span data-ttu-id="ac460-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ac460-119">Attribute-Id</span></span>      | <span data-ttu-id="ac460-120">1.2.840.113556.1.2.76</span><span class="sxs-lookup"><span data-stu-id="ac460-120">1.2.840.113556.1.2.76</span></span>                                          |
| <span data-ttu-id="ac460-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="ac460-121">System-Id-Guid</span></span>    | <span data-ttu-id="ac460-122">16775848-47f3-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="ac460-122">16775848-47f3-11d1-a9c3-0000f80367c1</span></span>                           |
| <span data-ttu-id="ac460-123">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ac460-123">Syntax</span></span>            | [<span data-ttu-id="ac460-124">**Enumerazione**</span><span class="sxs-lookup"><span data-stu-id="ac460-124">**Enumeration**</span></span>](s-enumeration.md)                           |



## <a name="implementations"></a><span data-ttu-id="ac460-125">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="ac460-125">Implementations</span></span>

-   [<span data-ttu-id="ac460-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="ac460-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="ac460-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ac460-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ac460-128">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="ac460-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="ac460-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ac460-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ac460-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ac460-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ac460-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ac460-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ac460-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ac460-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="ac460-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ac460-133">Windows 2000 Server</span></span>



| <span data-ttu-id="ac460-134">Voce</span><span class="sxs-lookup"><span data-stu-id="ac460-134">Entry</span></span> | <span data-ttu-id="ac460-135">Valore</span><span class="sxs-lookup"><span data-stu-id="ac460-135">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ac460-136">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="ac460-136">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ac460-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ac460-137">MAPI-Id</span></span>                | <span data-ttu-id="ac460-138">0x80F7</span><span class="sxs-lookup"><span data-stu-id="ac460-138">0x80F7</span></span>                          |
| <span data-ttu-id="ac460-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="ac460-139">System-Only</span></span>            | <span data-ttu-id="ac460-140">Falso</span><span class="sxs-lookup"><span data-stu-id="ac460-140">False</span></span>                           |
| <span data-ttu-id="ac460-141">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="ac460-141">Is-Single-Valued</span></span>       | <span data-ttu-id="ac460-142">Vero</span><span class="sxs-lookup"><span data-stu-id="ac460-142">True</span></span>                            |
| <span data-ttu-id="ac460-143">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="ac460-143">Is Indexed</span></span>             | <span data-ttu-id="ac460-144">Falso</span><span class="sxs-lookup"><span data-stu-id="ac460-144">False</span></span>                           |
| <span data-ttu-id="ac460-145">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="ac460-145">In Global Catalog</span></span>      | <span data-ttu-id="ac460-146">Falso</span><span class="sxs-lookup"><span data-stu-id="ac460-146">False</span></span>                           |
| <span data-ttu-id="ac460-147">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="ac460-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="ac460-148">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="ac460-148">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ac460-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ac460-149">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="ac460-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ac460-150">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="ac460-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ac460-151">Search-Flags</span></span>           | <span data-ttu-id="ac460-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ac460-152">0x00000000</span></span>                      |
| <span data-ttu-id="ac460-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ac460-153">System-Flags</span></span>           | <span data-ttu-id="ac460-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ac460-154">0x00000010</span></span>                      |
| <span data-ttu-id="ac460-155">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="ac460-155">Classes used in</span></span>        | [<span data-ttu-id="ac460-156">**In alto**</span><span class="sxs-lookup"><span data-stu-id="ac460-156">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="ac460-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ac460-157">Windows Server 2003</span></span>



| <span data-ttu-id="ac460-158">Voce</span><span class="sxs-lookup"><span data-stu-id="ac460-158">Entry</span></span> | <span data-ttu-id="ac460-159">Valore</span><span class="sxs-lookup"><span data-stu-id="ac460-159">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ac460-160">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="ac460-160">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ac460-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ac460-161">MAPI-Id</span></span>                | <span data-ttu-id="ac460-162">0x80F7</span><span class="sxs-lookup"><span data-stu-id="ac460-162">0x80F7</span></span>                          |
| <span data-ttu-id="ac460-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="ac460-163">System-Only</span></span>            | <span data-ttu-id="ac460-164">Falso</span><span class="sxs-lookup"><span data-stu-id="ac460-164">False</span></span>                           |
| <span data-ttu-id="ac460-165">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="ac460-165">Is-Single-Valued</span></span>       | <span data-ttu-id="ac460-166">Vero</span><span class="sxs-lookup"><span data-stu-id="ac460-166">True</span></span>                            |
| <span data-ttu-id="ac460-167">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="ac460-167">Is Indexed</span></span>             | <span data-ttu-id="ac460-168">Falso</span><span class="sxs-lookup"><span data-stu-id="ac460-168">False</span></span>                           |
| <span data-ttu-id="ac460-169">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="ac460-169">In Global Catalog</span></span>      | <span data-ttu-id="ac460-170">Falso</span><span class="sxs-lookup"><span data-stu-id="ac460-170">False</span></span>                           |
| <span data-ttu-id="ac460-171">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="ac460-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="ac460-172">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="ac460-172">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ac460-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ac460-173">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="ac460-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ac460-174">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="ac460-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ac460-175">Search-Flags</span></span>           | <span data-ttu-id="ac460-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ac460-176">0x00000000</span></span>                      |
| <span data-ttu-id="ac460-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ac460-177">System-Flags</span></span>           | <span data-ttu-id="ac460-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ac460-178">0x00000010</span></span>                      |
| <span data-ttu-id="ac460-179">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="ac460-179">Classes used in</span></span>        | [<span data-ttu-id="ac460-180">**In alto**</span><span class="sxs-lookup"><span data-stu-id="ac460-180">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="ac460-181">ADAM</span><span class="sxs-lookup"><span data-stu-id="ac460-181">ADAM</span></span>



| <span data-ttu-id="ac460-182">Voce</span><span class="sxs-lookup"><span data-stu-id="ac460-182">Entry</span></span> | <span data-ttu-id="ac460-183">Valore</span><span class="sxs-lookup"><span data-stu-id="ac460-183">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ac460-184">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="ac460-184">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ac460-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ac460-185">MAPI-Id</span></span>                | <span data-ttu-id="ac460-186">0x80F7</span><span class="sxs-lookup"><span data-stu-id="ac460-186">0x80F7</span></span>                          |
| <span data-ttu-id="ac460-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="ac460-187">System-Only</span></span>            | <span data-ttu-id="ac460-188">Falso</span><span class="sxs-lookup"><span data-stu-id="ac460-188">False</span></span>                           |
| <span data-ttu-id="ac460-189">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="ac460-189">Is-Single-Valued</span></span>       | <span data-ttu-id="ac460-190">Vero</span><span class="sxs-lookup"><span data-stu-id="ac460-190">True</span></span>                            |
| <span data-ttu-id="ac460-191">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="ac460-191">Is Indexed</span></span>             | <span data-ttu-id="ac460-192">Falso</span><span class="sxs-lookup"><span data-stu-id="ac460-192">False</span></span>                           |
| <span data-ttu-id="ac460-193">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="ac460-193">In Global Catalog</span></span>      | <span data-ttu-id="ac460-194">Falso</span><span class="sxs-lookup"><span data-stu-id="ac460-194">False</span></span>                           |
| <span data-ttu-id="ac460-195">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="ac460-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="ac460-196">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="ac460-196">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ac460-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ac460-197">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="ac460-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ac460-198">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="ac460-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ac460-199">Search-Flags</span></span>           | <span data-ttu-id="ac460-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ac460-200">0x00000000</span></span>                      |
| <span data-ttu-id="ac460-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ac460-201">System-Flags</span></span>           | <span data-ttu-id="ac460-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ac460-202">0x00000010</span></span>                      |
| <span data-ttu-id="ac460-203">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="ac460-203">Classes used in</span></span>        | [<span data-ttu-id="ac460-204">**In alto**</span><span class="sxs-lookup"><span data-stu-id="ac460-204">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ac460-205">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ac460-205">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ac460-206">Voce</span><span class="sxs-lookup"><span data-stu-id="ac460-206">Entry</span></span> | <span data-ttu-id="ac460-207">Valore</span><span class="sxs-lookup"><span data-stu-id="ac460-207">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ac460-208">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="ac460-208">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ac460-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ac460-209">MAPI-Id</span></span>                | <span data-ttu-id="ac460-210">0x80F7</span><span class="sxs-lookup"><span data-stu-id="ac460-210">0x80F7</span></span>                          |
| <span data-ttu-id="ac460-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="ac460-211">System-Only</span></span>            | <span data-ttu-id="ac460-212">Falso</span><span class="sxs-lookup"><span data-stu-id="ac460-212">False</span></span>                           |
| <span data-ttu-id="ac460-213">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="ac460-213">Is-Single-Valued</span></span>       | <span data-ttu-id="ac460-214">Vero</span><span class="sxs-lookup"><span data-stu-id="ac460-214">True</span></span>                            |
| <span data-ttu-id="ac460-215">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="ac460-215">Is Indexed</span></span>             | <span data-ttu-id="ac460-216">Falso</span><span class="sxs-lookup"><span data-stu-id="ac460-216">False</span></span>                           |
| <span data-ttu-id="ac460-217">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="ac460-217">In Global Catalog</span></span>      | <span data-ttu-id="ac460-218">Falso</span><span class="sxs-lookup"><span data-stu-id="ac460-218">False</span></span>                           |
| <span data-ttu-id="ac460-219">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="ac460-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="ac460-220">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="ac460-220">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ac460-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ac460-221">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="ac460-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ac460-222">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="ac460-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ac460-223">Search-Flags</span></span>           | <span data-ttu-id="ac460-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ac460-224">0x00000000</span></span>                      |
| <span data-ttu-id="ac460-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ac460-225">System-Flags</span></span>           | <span data-ttu-id="ac460-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ac460-226">0x00000010</span></span>                      |
| <span data-ttu-id="ac460-227">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="ac460-227">Classes used in</span></span>        | [<span data-ttu-id="ac460-228">**In alto**</span><span class="sxs-lookup"><span data-stu-id="ac460-228">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ac460-229">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ac460-229">Windows Server 2008</span></span>



| <span data-ttu-id="ac460-230">Voce</span><span class="sxs-lookup"><span data-stu-id="ac460-230">Entry</span></span> | <span data-ttu-id="ac460-231">Valore</span><span class="sxs-lookup"><span data-stu-id="ac460-231">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ac460-232">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="ac460-232">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ac460-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ac460-233">MAPI-Id</span></span>                | <span data-ttu-id="ac460-234">0x80F7</span><span class="sxs-lookup"><span data-stu-id="ac460-234">0x80F7</span></span>                          |
| <span data-ttu-id="ac460-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="ac460-235">System-Only</span></span>            | <span data-ttu-id="ac460-236">Falso</span><span class="sxs-lookup"><span data-stu-id="ac460-236">False</span></span>                           |
| <span data-ttu-id="ac460-237">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="ac460-237">Is-Single-Valued</span></span>       | <span data-ttu-id="ac460-238">Vero</span><span class="sxs-lookup"><span data-stu-id="ac460-238">True</span></span>                            |
| <span data-ttu-id="ac460-239">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="ac460-239">Is Indexed</span></span>             | <span data-ttu-id="ac460-240">Falso</span><span class="sxs-lookup"><span data-stu-id="ac460-240">False</span></span>                           |
| <span data-ttu-id="ac460-241">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="ac460-241">In Global Catalog</span></span>      | <span data-ttu-id="ac460-242">Falso</span><span class="sxs-lookup"><span data-stu-id="ac460-242">False</span></span>                           |
| <span data-ttu-id="ac460-243">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="ac460-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="ac460-244">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="ac460-244">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ac460-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ac460-245">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="ac460-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ac460-246">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="ac460-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ac460-247">Search-Flags</span></span>           | <span data-ttu-id="ac460-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ac460-248">0x00000000</span></span>                      |
| <span data-ttu-id="ac460-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ac460-249">System-Flags</span></span>           | <span data-ttu-id="ac460-250">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ac460-250">0x00000010</span></span>                      |
| <span data-ttu-id="ac460-251">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="ac460-251">Classes used in</span></span>        | [<span data-ttu-id="ac460-252">**In alto**</span><span class="sxs-lookup"><span data-stu-id="ac460-252">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ac460-253">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ac460-253">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ac460-254">Voce</span><span class="sxs-lookup"><span data-stu-id="ac460-254">Entry</span></span> | <span data-ttu-id="ac460-255">Valore</span><span class="sxs-lookup"><span data-stu-id="ac460-255">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ac460-256">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="ac460-256">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ac460-257">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ac460-257">MAPI-Id</span></span>                | <span data-ttu-id="ac460-258">0x80F7</span><span class="sxs-lookup"><span data-stu-id="ac460-258">0x80F7</span></span>                          |
| <span data-ttu-id="ac460-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="ac460-259">System-Only</span></span>            | <span data-ttu-id="ac460-260">Falso</span><span class="sxs-lookup"><span data-stu-id="ac460-260">False</span></span>                           |
| <span data-ttu-id="ac460-261">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="ac460-261">Is-Single-Valued</span></span>       | <span data-ttu-id="ac460-262">Vero</span><span class="sxs-lookup"><span data-stu-id="ac460-262">True</span></span>                            |
| <span data-ttu-id="ac460-263">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="ac460-263">Is Indexed</span></span>             | <span data-ttu-id="ac460-264">Falso</span><span class="sxs-lookup"><span data-stu-id="ac460-264">False</span></span>                           |
| <span data-ttu-id="ac460-265">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="ac460-265">In Global Catalog</span></span>      | <span data-ttu-id="ac460-266">Falso</span><span class="sxs-lookup"><span data-stu-id="ac460-266">False</span></span>                           |
| <span data-ttu-id="ac460-267">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="ac460-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="ac460-268">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="ac460-268">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ac460-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ac460-269">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="ac460-270">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ac460-270">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="ac460-271">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ac460-271">Search-Flags</span></span>           | <span data-ttu-id="ac460-272">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ac460-272">0x00000000</span></span>                      |
| <span data-ttu-id="ac460-273">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ac460-273">System-Flags</span></span>           | <span data-ttu-id="ac460-274">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ac460-274">0x00000010</span></span>                      |
| <span data-ttu-id="ac460-275">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="ac460-275">Classes used in</span></span>        | [<span data-ttu-id="ac460-276">**In alto**</span><span class="sxs-lookup"><span data-stu-id="ac460-276">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ac460-277">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ac460-277">Windows Server 2012</span></span>



| <span data-ttu-id="ac460-278">Voce</span><span class="sxs-lookup"><span data-stu-id="ac460-278">Entry</span></span> | <span data-ttu-id="ac460-279">Valore</span><span class="sxs-lookup"><span data-stu-id="ac460-279">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ac460-280">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="ac460-280">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ac460-281">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ac460-281">MAPI-Id</span></span>                | <span data-ttu-id="ac460-282">0x80F7</span><span class="sxs-lookup"><span data-stu-id="ac460-282">0x80F7</span></span>                          |
| <span data-ttu-id="ac460-283">System-Only</span><span class="sxs-lookup"><span data-stu-id="ac460-283">System-Only</span></span>            | <span data-ttu-id="ac460-284">Falso</span><span class="sxs-lookup"><span data-stu-id="ac460-284">False</span></span>                           |
| <span data-ttu-id="ac460-285">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="ac460-285">Is-Single-Valued</span></span>       | <span data-ttu-id="ac460-286">Vero</span><span class="sxs-lookup"><span data-stu-id="ac460-286">True</span></span>                            |
| <span data-ttu-id="ac460-287">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="ac460-287">Is Indexed</span></span>             | <span data-ttu-id="ac460-288">Falso</span><span class="sxs-lookup"><span data-stu-id="ac460-288">False</span></span>                           |
| <span data-ttu-id="ac460-289">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="ac460-289">In Global Catalog</span></span>      | <span data-ttu-id="ac460-290">Falso</span><span class="sxs-lookup"><span data-stu-id="ac460-290">False</span></span>                           |
| <span data-ttu-id="ac460-291">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="ac460-291">NT-Security-Descriptor</span></span> | <span data-ttu-id="ac460-292">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="ac460-292">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ac460-293">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ac460-293">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="ac460-294">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ac460-294">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="ac460-295">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ac460-295">Search-Flags</span></span>           | <span data-ttu-id="ac460-296">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ac460-296">0x00000000</span></span>                      |
| <span data-ttu-id="ac460-297">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ac460-297">System-Flags</span></span>           | <span data-ttu-id="ac460-298">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ac460-298">0x00000010</span></span>                      |
| <span data-ttu-id="ac460-299">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="ac460-299">Classes used in</span></span>        | [<span data-ttu-id="ac460-300">**In alto**</span><span class="sxs-lookup"><span data-stu-id="ac460-300">**Top**</span></span>](c-top.md)<br/> |



 

 





