---
title: Attributo When-Changed
description: Data dell'Ultima modifica apportata all'oggetto. Questo valore non viene replicato ed esiste nel catalogo globale.
ms.assetid: 32dc9458-5692-4bce-abc1-7bea3ea680a9
ms.tgt_platform: multiple
keywords:
- Schema AD When-Changed attribute
- Schema AD dell'attributo whenChanged
topic_type:
- apiref
api_name:
- When-Changed
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7c3608a33aa5d5ac52b226cd7a3d94ff0b95520
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103874766"
---
# <a name="when-changed-attribute"></a><span data-ttu-id="bc7ad-106">Attributo When-Changed</span><span class="sxs-lookup"><span data-stu-id="bc7ad-106">When-Changed attribute</span></span>

<span data-ttu-id="bc7ad-107">Data dell'Ultima modifica apportata all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="bc7ad-107">The date when this object was last changed.</span></span> <span data-ttu-id="bc7ad-108">Questo valore non viene replicato ed esiste nel catalogo globale.</span><span class="sxs-lookup"><span data-stu-id="bc7ad-108">This value is not replicated and exists in the global catalog.</span></span>



| <span data-ttu-id="bc7ad-109">Voce</span><span class="sxs-lookup"><span data-stu-id="bc7ad-109">Entry</span></span> | <span data-ttu-id="bc7ad-110">Valore</span><span class="sxs-lookup"><span data-stu-id="bc7ad-110">Value</span></span> |
|-------------------|---------------------------------------------------------------|
| <span data-ttu-id="bc7ad-111">CN</span><span class="sxs-lookup"><span data-stu-id="bc7ad-111">CN</span></span>                | <span data-ttu-id="bc7ad-112">When-Changed</span><span class="sxs-lookup"><span data-stu-id="bc7ad-112">When-Changed</span></span>                                                  |
| <span data-ttu-id="bc7ad-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="bc7ad-113">Ldap-Display-Name</span></span> | <span data-ttu-id="bc7ad-114">whenChanged</span><span class="sxs-lookup"><span data-stu-id="bc7ad-114">whenChanged</span></span>                                                   |
| <span data-ttu-id="bc7ad-115">Dimensione</span><span class="sxs-lookup"><span data-stu-id="bc7ad-115">Size</span></span>              | <span data-ttu-id="bc7ad-116">8 byte</span><span class="sxs-lookup"><span data-stu-id="bc7ad-116">8 bytes</span></span>                                                       |
| <span data-ttu-id="bc7ad-117">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="bc7ad-117">Update Privilege</span></span>  | <span data-ttu-id="bc7ad-118">Questo valore viene impostato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="bc7ad-118">This value is set by the system.</span></span>                              |
| <span data-ttu-id="bc7ad-119">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="bc7ad-119">Update Frequency</span></span>  | <span data-ttu-id="bc7ad-120">Ogni volta che l'oggetto viene modificato.</span><span class="sxs-lookup"><span data-stu-id="bc7ad-120">Each time the object is changed.</span></span>                              |
| <span data-ttu-id="bc7ad-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="bc7ad-121">Attribute-Id</span></span>      | <span data-ttu-id="bc7ad-122">1.2.840.113556.1.2.3</span><span class="sxs-lookup"><span data-stu-id="bc7ad-122">1.2.840.113556.1.2.3</span></span>                                          |
| <span data-ttu-id="bc7ad-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="bc7ad-123">System-Id-Guid</span></span>    | <span data-ttu-id="bc7ad-124">bf967a77-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="bc7ad-124">bf967a77-0de6-11d0-a285-00aa003049e2</span></span>                          |
| <span data-ttu-id="bc7ad-125">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bc7ad-125">Syntax</span></span>            | [<span data-ttu-id="bc7ad-126">**String(Generalized-Time)**</span><span class="sxs-lookup"><span data-stu-id="bc7ad-126">**String(Generalized-Time)**</span></span>](s-string-generalized-time.md) |



## <a name="implementations"></a><span data-ttu-id="bc7ad-127">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="bc7ad-127">Implementations</span></span>

-   [<span data-ttu-id="bc7ad-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="bc7ad-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="bc7ad-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="bc7ad-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="bc7ad-130">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="bc7ad-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="bc7ad-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="bc7ad-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="bc7ad-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="bc7ad-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="bc7ad-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="bc7ad-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="bc7ad-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="bc7ad-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="bc7ad-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="bc7ad-135">Windows 2000 Server</span></span>



| <span data-ttu-id="bc7ad-136">Voce</span><span class="sxs-lookup"><span data-stu-id="bc7ad-136">Entry</span></span> | <span data-ttu-id="bc7ad-137">Valore</span><span class="sxs-lookup"><span data-stu-id="bc7ad-137">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="bc7ad-138">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="bc7ad-138">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="bc7ad-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bc7ad-139">MAPI-Id</span></span>                | <span data-ttu-id="bc7ad-140">0x3008</span><span class="sxs-lookup"><span data-stu-id="bc7ad-140">0x3008</span></span>                          |
| <span data-ttu-id="bc7ad-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="bc7ad-141">System-Only</span></span>            | <span data-ttu-id="bc7ad-142">Vero</span><span class="sxs-lookup"><span data-stu-id="bc7ad-142">True</span></span>                            |
| <span data-ttu-id="bc7ad-143">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="bc7ad-143">Is-Single-Valued</span></span>       | <span data-ttu-id="bc7ad-144">Vero</span><span class="sxs-lookup"><span data-stu-id="bc7ad-144">True</span></span>                            |
| <span data-ttu-id="bc7ad-145">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="bc7ad-145">Is Indexed</span></span>             | <span data-ttu-id="bc7ad-146">Falso</span><span class="sxs-lookup"><span data-stu-id="bc7ad-146">False</span></span>                           |
| <span data-ttu-id="bc7ad-147">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="bc7ad-147">In Global Catalog</span></span>      | <span data-ttu-id="bc7ad-148">Vero</span><span class="sxs-lookup"><span data-stu-id="bc7ad-148">True</span></span>                            |
| <span data-ttu-id="bc7ad-149">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="bc7ad-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="bc7ad-150">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="bc7ad-150">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="bc7ad-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bc7ad-151">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="bc7ad-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bc7ad-152">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="bc7ad-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bc7ad-153">Search-Flags</span></span>           | <span data-ttu-id="bc7ad-154">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bc7ad-154">0x00000000</span></span>                      |
| <span data-ttu-id="bc7ad-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bc7ad-155">System-Flags</span></span>           | <span data-ttu-id="bc7ad-156">0x00000013</span><span class="sxs-lookup"><span data-stu-id="bc7ad-156">0x00000013</span></span>                      |
| <span data-ttu-id="bc7ad-157">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="bc7ad-157">Classes used in</span></span>        | [<span data-ttu-id="bc7ad-158">**In alto**</span><span class="sxs-lookup"><span data-stu-id="bc7ad-158">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="bc7ad-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="bc7ad-159">Windows Server 2003</span></span>



| <span data-ttu-id="bc7ad-160">Voce</span><span class="sxs-lookup"><span data-stu-id="bc7ad-160">Entry</span></span> | <span data-ttu-id="bc7ad-161">Valore</span><span class="sxs-lookup"><span data-stu-id="bc7ad-161">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="bc7ad-162">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="bc7ad-162">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="bc7ad-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bc7ad-163">MAPI-Id</span></span>                | <span data-ttu-id="bc7ad-164">0x3008</span><span class="sxs-lookup"><span data-stu-id="bc7ad-164">0x3008</span></span>                          |
| <span data-ttu-id="bc7ad-165">System-Only</span><span class="sxs-lookup"><span data-stu-id="bc7ad-165">System-Only</span></span>            | <span data-ttu-id="bc7ad-166">Vero</span><span class="sxs-lookup"><span data-stu-id="bc7ad-166">True</span></span>                            |
| <span data-ttu-id="bc7ad-167">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="bc7ad-167">Is-Single-Valued</span></span>       | <span data-ttu-id="bc7ad-168">Vero</span><span class="sxs-lookup"><span data-stu-id="bc7ad-168">True</span></span>                            |
| <span data-ttu-id="bc7ad-169">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="bc7ad-169">Is Indexed</span></span>             | <span data-ttu-id="bc7ad-170">Falso</span><span class="sxs-lookup"><span data-stu-id="bc7ad-170">False</span></span>                           |
| <span data-ttu-id="bc7ad-171">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="bc7ad-171">In Global Catalog</span></span>      | <span data-ttu-id="bc7ad-172">Vero</span><span class="sxs-lookup"><span data-stu-id="bc7ad-172">True</span></span>                            |
| <span data-ttu-id="bc7ad-173">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="bc7ad-173">NT-Security-Descriptor</span></span> | <span data-ttu-id="bc7ad-174">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="bc7ad-174">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="bc7ad-175">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bc7ad-175">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="bc7ad-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bc7ad-176">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="bc7ad-177">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bc7ad-177">Search-Flags</span></span>           | <span data-ttu-id="bc7ad-178">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bc7ad-178">0x00000000</span></span>                      |
| <span data-ttu-id="bc7ad-179">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bc7ad-179">System-Flags</span></span>           | <span data-ttu-id="bc7ad-180">0x00000013</span><span class="sxs-lookup"><span data-stu-id="bc7ad-180">0x00000013</span></span>                      |
| <span data-ttu-id="bc7ad-181">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="bc7ad-181">Classes used in</span></span>        | [<span data-ttu-id="bc7ad-182">**In alto**</span><span class="sxs-lookup"><span data-stu-id="bc7ad-182">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="bc7ad-183">ADAM</span><span class="sxs-lookup"><span data-stu-id="bc7ad-183">ADAM</span></span>



| <span data-ttu-id="bc7ad-184">Voce</span><span class="sxs-lookup"><span data-stu-id="bc7ad-184">Entry</span></span> | <span data-ttu-id="bc7ad-185">Valore</span><span class="sxs-lookup"><span data-stu-id="bc7ad-185">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="bc7ad-186">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="bc7ad-186">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="bc7ad-187">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bc7ad-187">MAPI-Id</span></span>                | <span data-ttu-id="bc7ad-188">0x3008</span><span class="sxs-lookup"><span data-stu-id="bc7ad-188">0x3008</span></span>                          |
| <span data-ttu-id="bc7ad-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="bc7ad-189">System-Only</span></span>            | <span data-ttu-id="bc7ad-190">Vero</span><span class="sxs-lookup"><span data-stu-id="bc7ad-190">True</span></span>                            |
| <span data-ttu-id="bc7ad-191">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="bc7ad-191">Is-Single-Valued</span></span>       | <span data-ttu-id="bc7ad-192">Vero</span><span class="sxs-lookup"><span data-stu-id="bc7ad-192">True</span></span>                            |
| <span data-ttu-id="bc7ad-193">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="bc7ad-193">Is Indexed</span></span>             | <span data-ttu-id="bc7ad-194">Falso</span><span class="sxs-lookup"><span data-stu-id="bc7ad-194">False</span></span>                           |
| <span data-ttu-id="bc7ad-195">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="bc7ad-195">In Global Catalog</span></span>      | <span data-ttu-id="bc7ad-196">Vero</span><span class="sxs-lookup"><span data-stu-id="bc7ad-196">True</span></span>                            |
| <span data-ttu-id="bc7ad-197">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="bc7ad-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="bc7ad-198">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="bc7ad-198">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="bc7ad-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bc7ad-199">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="bc7ad-200">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bc7ad-200">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="bc7ad-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bc7ad-201">Search-Flags</span></span>           | <span data-ttu-id="bc7ad-202">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bc7ad-202">0x00000000</span></span>                      |
| <span data-ttu-id="bc7ad-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bc7ad-203">System-Flags</span></span>           | <span data-ttu-id="bc7ad-204">0x00000013</span><span class="sxs-lookup"><span data-stu-id="bc7ad-204">0x00000013</span></span>                      |
| <span data-ttu-id="bc7ad-205">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="bc7ad-205">Classes used in</span></span>        | [<span data-ttu-id="bc7ad-206">**In alto**</span><span class="sxs-lookup"><span data-stu-id="bc7ad-206">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="bc7ad-207">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="bc7ad-207">Windows Server 2003 R2</span></span>



| <span data-ttu-id="bc7ad-208">Voce</span><span class="sxs-lookup"><span data-stu-id="bc7ad-208">Entry</span></span> | <span data-ttu-id="bc7ad-209">Valore</span><span class="sxs-lookup"><span data-stu-id="bc7ad-209">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="bc7ad-210">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="bc7ad-210">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="bc7ad-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bc7ad-211">MAPI-Id</span></span>                | <span data-ttu-id="bc7ad-212">0x3008</span><span class="sxs-lookup"><span data-stu-id="bc7ad-212">0x3008</span></span>                          |
| <span data-ttu-id="bc7ad-213">System-Only</span><span class="sxs-lookup"><span data-stu-id="bc7ad-213">System-Only</span></span>            | <span data-ttu-id="bc7ad-214">Vero</span><span class="sxs-lookup"><span data-stu-id="bc7ad-214">True</span></span>                            |
| <span data-ttu-id="bc7ad-215">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="bc7ad-215">Is-Single-Valued</span></span>       | <span data-ttu-id="bc7ad-216">Vero</span><span class="sxs-lookup"><span data-stu-id="bc7ad-216">True</span></span>                            |
| <span data-ttu-id="bc7ad-217">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="bc7ad-217">Is Indexed</span></span>             | <span data-ttu-id="bc7ad-218">Falso</span><span class="sxs-lookup"><span data-stu-id="bc7ad-218">False</span></span>                           |
| <span data-ttu-id="bc7ad-219">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="bc7ad-219">In Global Catalog</span></span>      | <span data-ttu-id="bc7ad-220">Vero</span><span class="sxs-lookup"><span data-stu-id="bc7ad-220">True</span></span>                            |
| <span data-ttu-id="bc7ad-221">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="bc7ad-221">NT-Security-Descriptor</span></span> | <span data-ttu-id="bc7ad-222">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="bc7ad-222">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="bc7ad-223">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bc7ad-223">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="bc7ad-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bc7ad-224">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="bc7ad-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bc7ad-225">Search-Flags</span></span>           | <span data-ttu-id="bc7ad-226">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bc7ad-226">0x00000000</span></span>                      |
| <span data-ttu-id="bc7ad-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bc7ad-227">System-Flags</span></span>           | <span data-ttu-id="bc7ad-228">0x00000013</span><span class="sxs-lookup"><span data-stu-id="bc7ad-228">0x00000013</span></span>                      |
| <span data-ttu-id="bc7ad-229">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="bc7ad-229">Classes used in</span></span>        | [<span data-ttu-id="bc7ad-230">**In alto**</span><span class="sxs-lookup"><span data-stu-id="bc7ad-230">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="bc7ad-231">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bc7ad-231">Windows Server 2008</span></span>



| <span data-ttu-id="bc7ad-232">Voce</span><span class="sxs-lookup"><span data-stu-id="bc7ad-232">Entry</span></span> | <span data-ttu-id="bc7ad-233">Valore</span><span class="sxs-lookup"><span data-stu-id="bc7ad-233">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="bc7ad-234">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="bc7ad-234">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="bc7ad-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bc7ad-235">MAPI-Id</span></span>                | <span data-ttu-id="bc7ad-236">0x3008</span><span class="sxs-lookup"><span data-stu-id="bc7ad-236">0x3008</span></span>                          |
| <span data-ttu-id="bc7ad-237">System-Only</span><span class="sxs-lookup"><span data-stu-id="bc7ad-237">System-Only</span></span>            | <span data-ttu-id="bc7ad-238">Vero</span><span class="sxs-lookup"><span data-stu-id="bc7ad-238">True</span></span>                            |
| <span data-ttu-id="bc7ad-239">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="bc7ad-239">Is-Single-Valued</span></span>       | <span data-ttu-id="bc7ad-240">Vero</span><span class="sxs-lookup"><span data-stu-id="bc7ad-240">True</span></span>                            |
| <span data-ttu-id="bc7ad-241">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="bc7ad-241">Is Indexed</span></span>             | <span data-ttu-id="bc7ad-242">Falso</span><span class="sxs-lookup"><span data-stu-id="bc7ad-242">False</span></span>                           |
| <span data-ttu-id="bc7ad-243">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="bc7ad-243">In Global Catalog</span></span>      | <span data-ttu-id="bc7ad-244">Vero</span><span class="sxs-lookup"><span data-stu-id="bc7ad-244">True</span></span>                            |
| <span data-ttu-id="bc7ad-245">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="bc7ad-245">NT-Security-Descriptor</span></span> | <span data-ttu-id="bc7ad-246">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="bc7ad-246">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="bc7ad-247">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bc7ad-247">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="bc7ad-248">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bc7ad-248">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="bc7ad-249">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bc7ad-249">Search-Flags</span></span>           | <span data-ttu-id="bc7ad-250">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bc7ad-250">0x00000000</span></span>                      |
| <span data-ttu-id="bc7ad-251">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bc7ad-251">System-Flags</span></span>           | <span data-ttu-id="bc7ad-252">0x00000013</span><span class="sxs-lookup"><span data-stu-id="bc7ad-252">0x00000013</span></span>                      |
| <span data-ttu-id="bc7ad-253">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="bc7ad-253">Classes used in</span></span>        | [<span data-ttu-id="bc7ad-254">**In alto**</span><span class="sxs-lookup"><span data-stu-id="bc7ad-254">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="bc7ad-255">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="bc7ad-255">Windows Server 2008 R2</span></span>



| <span data-ttu-id="bc7ad-256">Voce</span><span class="sxs-lookup"><span data-stu-id="bc7ad-256">Entry</span></span> | <span data-ttu-id="bc7ad-257">Valore</span><span class="sxs-lookup"><span data-stu-id="bc7ad-257">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="bc7ad-258">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="bc7ad-258">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="bc7ad-259">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bc7ad-259">MAPI-Id</span></span>                | <span data-ttu-id="bc7ad-260">0x3008</span><span class="sxs-lookup"><span data-stu-id="bc7ad-260">0x3008</span></span>                          |
| <span data-ttu-id="bc7ad-261">System-Only</span><span class="sxs-lookup"><span data-stu-id="bc7ad-261">System-Only</span></span>            | <span data-ttu-id="bc7ad-262">Vero</span><span class="sxs-lookup"><span data-stu-id="bc7ad-262">True</span></span>                            |
| <span data-ttu-id="bc7ad-263">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="bc7ad-263">Is-Single-Valued</span></span>       | <span data-ttu-id="bc7ad-264">Vero</span><span class="sxs-lookup"><span data-stu-id="bc7ad-264">True</span></span>                            |
| <span data-ttu-id="bc7ad-265">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="bc7ad-265">Is Indexed</span></span>             | <span data-ttu-id="bc7ad-266">Falso</span><span class="sxs-lookup"><span data-stu-id="bc7ad-266">False</span></span>                           |
| <span data-ttu-id="bc7ad-267">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="bc7ad-267">In Global Catalog</span></span>      | <span data-ttu-id="bc7ad-268">Vero</span><span class="sxs-lookup"><span data-stu-id="bc7ad-268">True</span></span>                            |
| <span data-ttu-id="bc7ad-269">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="bc7ad-269">NT-Security-Descriptor</span></span> | <span data-ttu-id="bc7ad-270">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="bc7ad-270">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="bc7ad-271">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bc7ad-271">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="bc7ad-272">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bc7ad-272">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="bc7ad-273">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bc7ad-273">Search-Flags</span></span>           | <span data-ttu-id="bc7ad-274">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bc7ad-274">0x00000000</span></span>                      |
| <span data-ttu-id="bc7ad-275">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bc7ad-275">System-Flags</span></span>           | <span data-ttu-id="bc7ad-276">0x00000013</span><span class="sxs-lookup"><span data-stu-id="bc7ad-276">0x00000013</span></span>                      |
| <span data-ttu-id="bc7ad-277">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="bc7ad-277">Classes used in</span></span>        | [<span data-ttu-id="bc7ad-278">**In alto**</span><span class="sxs-lookup"><span data-stu-id="bc7ad-278">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="bc7ad-279">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="bc7ad-279">Windows Server 2012</span></span>



| <span data-ttu-id="bc7ad-280">Voce</span><span class="sxs-lookup"><span data-stu-id="bc7ad-280">Entry</span></span> | <span data-ttu-id="bc7ad-281">Valore</span><span class="sxs-lookup"><span data-stu-id="bc7ad-281">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="bc7ad-282">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="bc7ad-282">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="bc7ad-283">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bc7ad-283">MAPI-Id</span></span>                | <span data-ttu-id="bc7ad-284">0x3008</span><span class="sxs-lookup"><span data-stu-id="bc7ad-284">0x3008</span></span>                          |
| <span data-ttu-id="bc7ad-285">System-Only</span><span class="sxs-lookup"><span data-stu-id="bc7ad-285">System-Only</span></span>            | <span data-ttu-id="bc7ad-286">Vero</span><span class="sxs-lookup"><span data-stu-id="bc7ad-286">True</span></span>                            |
| <span data-ttu-id="bc7ad-287">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="bc7ad-287">Is-Single-Valued</span></span>       | <span data-ttu-id="bc7ad-288">Vero</span><span class="sxs-lookup"><span data-stu-id="bc7ad-288">True</span></span>                            |
| <span data-ttu-id="bc7ad-289">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="bc7ad-289">Is Indexed</span></span>             | <span data-ttu-id="bc7ad-290">Falso</span><span class="sxs-lookup"><span data-stu-id="bc7ad-290">False</span></span>                           |
| <span data-ttu-id="bc7ad-291">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="bc7ad-291">In Global Catalog</span></span>      | <span data-ttu-id="bc7ad-292">Vero</span><span class="sxs-lookup"><span data-stu-id="bc7ad-292">True</span></span>                            |
| <span data-ttu-id="bc7ad-293">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="bc7ad-293">NT-Security-Descriptor</span></span> | <span data-ttu-id="bc7ad-294">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="bc7ad-294">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="bc7ad-295">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bc7ad-295">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="bc7ad-296">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bc7ad-296">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="bc7ad-297">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bc7ad-297">Search-Flags</span></span>           | <span data-ttu-id="bc7ad-298">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bc7ad-298">0x00000000</span></span>                      |
| <span data-ttu-id="bc7ad-299">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bc7ad-299">System-Flags</span></span>           | <span data-ttu-id="bc7ad-300">0x00000013</span><span class="sxs-lookup"><span data-stu-id="bc7ad-300">0x00000013</span></span>                      |
| <span data-ttu-id="bc7ad-301">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="bc7ad-301">Classes used in</span></span>        | [<span data-ttu-id="bc7ad-302">**In alto**</span><span class="sxs-lookup"><span data-stu-id="bc7ad-302">**Top**</span></span>](c-top.md)<br/> |



 

 





