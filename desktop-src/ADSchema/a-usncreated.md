---
title: Attributo USN-Created
description: Numero di sequenza di aggiornamento (USN) assegnato al momento della creazione dell'oggetto. Vedere anche USN-changed.
ms.assetid: c38456b8-fc8f-4ea0-8f3d-e2bb3b44ff50
ms.tgt_platform: multiple
keywords:
- Schema AD USN-Created attribute
- Schema AD dell'attributo uSNCreated
topic_type:
- apiref
api_name:
- USN-Created
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b950ddfe261de5d46980e51b236da0f775fcb01b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "106303102"
---
# <a name="usn-created-attribute"></a><span data-ttu-id="f3678-106">Attributo USN-Created</span><span class="sxs-lookup"><span data-stu-id="f3678-106">USN-Created attribute</span></span>

<span data-ttu-id="f3678-107">Numero di sequenza di aggiornamento (USN) assegnato al momento della creazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f3678-107">The update sequence number (USN) assigned at object creation.</span></span> <span data-ttu-id="f3678-108">Vedere anche [**USN-changed**](a-usnchanged.md).</span><span class="sxs-lookup"><span data-stu-id="f3678-108">See also, [**USN-Changed**](a-usnchanged.md).</span></span>



| <span data-ttu-id="f3678-109">Voce</span><span class="sxs-lookup"><span data-stu-id="f3678-109">Entry</span></span> | <span data-ttu-id="f3678-110">Valore</span><span class="sxs-lookup"><span data-stu-id="f3678-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="f3678-111">CN</span><span class="sxs-lookup"><span data-stu-id="f3678-111">CN</span></span>                | <span data-ttu-id="f3678-112">USN-Created</span><span class="sxs-lookup"><span data-stu-id="f3678-112">USN-Created</span></span>                          |
| <span data-ttu-id="f3678-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="f3678-113">Ldap-Display-Name</span></span> | <span data-ttu-id="f3678-114">uSNCreated</span><span class="sxs-lookup"><span data-stu-id="f3678-114">uSNCreated</span></span>                           |
| <span data-ttu-id="f3678-115">Dimensione</span><span class="sxs-lookup"><span data-stu-id="f3678-115">Size</span></span>              | <span data-ttu-id="f3678-116">8 byte</span><span class="sxs-lookup"><span data-stu-id="f3678-116">8 bytes</span></span>                              |
| <span data-ttu-id="f3678-117">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="f3678-117">Update Privilege</span></span>  | <span data-ttu-id="f3678-118">Questo valore viene impostato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="f3678-118">This value is set by the system.</span></span>     |
| <span data-ttu-id="f3678-119">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="f3678-119">Update Frequency</span></span>  | <span data-ttu-id="f3678-120">Quando viene creato l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f3678-120">When the object is created.</span></span>          |
| <span data-ttu-id="f3678-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f3678-121">Attribute-Id</span></span>      | <span data-ttu-id="f3678-122">1.2.840.113556.1.2.19</span><span class="sxs-lookup"><span data-stu-id="f3678-122">1.2.840.113556.1.2.19</span></span>                |
| <span data-ttu-id="f3678-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="f3678-123">System-Id-Guid</span></span>    | <span data-ttu-id="f3678-124">bf967a70-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="f3678-124">bf967a70-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="f3678-125">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f3678-125">Syntax</span></span>            | [<span data-ttu-id="f3678-126">**Interval**</span><span class="sxs-lookup"><span data-stu-id="f3678-126">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="f3678-127">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="f3678-127">Implementations</span></span>

-   [<span data-ttu-id="f3678-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="f3678-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="f3678-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f3678-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f3678-130">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="f3678-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="f3678-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f3678-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f3678-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f3678-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f3678-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f3678-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f3678-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f3678-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="f3678-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f3678-135">Windows 2000 Server</span></span>



| <span data-ttu-id="f3678-136">Voce</span><span class="sxs-lookup"><span data-stu-id="f3678-136">Entry</span></span> | <span data-ttu-id="f3678-137">Valore</span><span class="sxs-lookup"><span data-stu-id="f3678-137">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f3678-138">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="f3678-138">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="f3678-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f3678-139">MAPI-Id</span></span>                | <span data-ttu-id="f3678-140">0x8154</span><span class="sxs-lookup"><span data-stu-id="f3678-140">0x8154</span></span>                          |
| <span data-ttu-id="f3678-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="f3678-141">System-Only</span></span>            | <span data-ttu-id="f3678-142">Vero</span><span class="sxs-lookup"><span data-stu-id="f3678-142">True</span></span>                            |
| <span data-ttu-id="f3678-143">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="f3678-143">Is-Single-Valued</span></span>       | <span data-ttu-id="f3678-144">Vero</span><span class="sxs-lookup"><span data-stu-id="f3678-144">True</span></span>                            |
| <span data-ttu-id="f3678-145">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="f3678-145">Is Indexed</span></span>             | <span data-ttu-id="f3678-146">Vero</span><span class="sxs-lookup"><span data-stu-id="f3678-146">True</span></span>                            |
| <span data-ttu-id="f3678-147">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="f3678-147">In Global Catalog</span></span>      | <span data-ttu-id="f3678-148">Vero</span><span class="sxs-lookup"><span data-stu-id="f3678-148">True</span></span>                            |
| <span data-ttu-id="f3678-149">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="f3678-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="f3678-150">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="f3678-150">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f3678-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f3678-151">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="f3678-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f3678-152">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="f3678-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f3678-153">Search-Flags</span></span>           | <span data-ttu-id="f3678-154">0x00000009</span><span class="sxs-lookup"><span data-stu-id="f3678-154">0x00000009</span></span>                      |
| <span data-ttu-id="f3678-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f3678-155">System-Flags</span></span>           | <span data-ttu-id="f3678-156">0x00000013</span><span class="sxs-lookup"><span data-stu-id="f3678-156">0x00000013</span></span>                      |
| <span data-ttu-id="f3678-157">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="f3678-157">Classes used in</span></span>        | [<span data-ttu-id="f3678-158">**In alto**</span><span class="sxs-lookup"><span data-stu-id="f3678-158">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="f3678-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f3678-159">Windows Server 2003</span></span>



| <span data-ttu-id="f3678-160">Voce</span><span class="sxs-lookup"><span data-stu-id="f3678-160">Entry</span></span> | <span data-ttu-id="f3678-161">Valore</span><span class="sxs-lookup"><span data-stu-id="f3678-161">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f3678-162">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="f3678-162">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="f3678-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f3678-163">MAPI-Id</span></span>                | <span data-ttu-id="f3678-164">0x8154</span><span class="sxs-lookup"><span data-stu-id="f3678-164">0x8154</span></span>                          |
| <span data-ttu-id="f3678-165">System-Only</span><span class="sxs-lookup"><span data-stu-id="f3678-165">System-Only</span></span>            | <span data-ttu-id="f3678-166">Vero</span><span class="sxs-lookup"><span data-stu-id="f3678-166">True</span></span>                            |
| <span data-ttu-id="f3678-167">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="f3678-167">Is-Single-Valued</span></span>       | <span data-ttu-id="f3678-168">Vero</span><span class="sxs-lookup"><span data-stu-id="f3678-168">True</span></span>                            |
| <span data-ttu-id="f3678-169">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="f3678-169">Is Indexed</span></span>             | <span data-ttu-id="f3678-170">Vero</span><span class="sxs-lookup"><span data-stu-id="f3678-170">True</span></span>                            |
| <span data-ttu-id="f3678-171">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="f3678-171">In Global Catalog</span></span>      | <span data-ttu-id="f3678-172">Vero</span><span class="sxs-lookup"><span data-stu-id="f3678-172">True</span></span>                            |
| <span data-ttu-id="f3678-173">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="f3678-173">NT-Security-Descriptor</span></span> | <span data-ttu-id="f3678-174">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="f3678-174">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f3678-175">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f3678-175">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="f3678-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f3678-176">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="f3678-177">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f3678-177">Search-Flags</span></span>           | <span data-ttu-id="f3678-178">0x00000009</span><span class="sxs-lookup"><span data-stu-id="f3678-178">0x00000009</span></span>                      |
| <span data-ttu-id="f3678-179">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f3678-179">System-Flags</span></span>           | <span data-ttu-id="f3678-180">0x00000013</span><span class="sxs-lookup"><span data-stu-id="f3678-180">0x00000013</span></span>                      |
| <span data-ttu-id="f3678-181">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="f3678-181">Classes used in</span></span>        | [<span data-ttu-id="f3678-182">**In alto**</span><span class="sxs-lookup"><span data-stu-id="f3678-182">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="f3678-183">ADAM</span><span class="sxs-lookup"><span data-stu-id="f3678-183">ADAM</span></span>



| <span data-ttu-id="f3678-184">Voce</span><span class="sxs-lookup"><span data-stu-id="f3678-184">Entry</span></span> | <span data-ttu-id="f3678-185">Valore</span><span class="sxs-lookup"><span data-stu-id="f3678-185">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f3678-186">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="f3678-186">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="f3678-187">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f3678-187">MAPI-Id</span></span>                | <span data-ttu-id="f3678-188">0x8154</span><span class="sxs-lookup"><span data-stu-id="f3678-188">0x8154</span></span>                          |
| <span data-ttu-id="f3678-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="f3678-189">System-Only</span></span>            | <span data-ttu-id="f3678-190">Vero</span><span class="sxs-lookup"><span data-stu-id="f3678-190">True</span></span>                            |
| <span data-ttu-id="f3678-191">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="f3678-191">Is-Single-Valued</span></span>       | <span data-ttu-id="f3678-192">Vero</span><span class="sxs-lookup"><span data-stu-id="f3678-192">True</span></span>                            |
| <span data-ttu-id="f3678-193">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="f3678-193">Is Indexed</span></span>             | <span data-ttu-id="f3678-194">Vero</span><span class="sxs-lookup"><span data-stu-id="f3678-194">True</span></span>                            |
| <span data-ttu-id="f3678-195">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="f3678-195">In Global Catalog</span></span>      | <span data-ttu-id="f3678-196">Vero</span><span class="sxs-lookup"><span data-stu-id="f3678-196">True</span></span>                            |
| <span data-ttu-id="f3678-197">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="f3678-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="f3678-198">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="f3678-198">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f3678-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f3678-199">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="f3678-200">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f3678-200">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="f3678-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f3678-201">Search-Flags</span></span>           | <span data-ttu-id="f3678-202">0x00000009</span><span class="sxs-lookup"><span data-stu-id="f3678-202">0x00000009</span></span>                      |
| <span data-ttu-id="f3678-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f3678-203">System-Flags</span></span>           | <span data-ttu-id="f3678-204">0x00000013</span><span class="sxs-lookup"><span data-stu-id="f3678-204">0x00000013</span></span>                      |
| <span data-ttu-id="f3678-205">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="f3678-205">Classes used in</span></span>        | [<span data-ttu-id="f3678-206">**In alto**</span><span class="sxs-lookup"><span data-stu-id="f3678-206">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f3678-207">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f3678-207">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f3678-208">Voce</span><span class="sxs-lookup"><span data-stu-id="f3678-208">Entry</span></span> | <span data-ttu-id="f3678-209">Valore</span><span class="sxs-lookup"><span data-stu-id="f3678-209">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f3678-210">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="f3678-210">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="f3678-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f3678-211">MAPI-Id</span></span>                | <span data-ttu-id="f3678-212">0x8154</span><span class="sxs-lookup"><span data-stu-id="f3678-212">0x8154</span></span>                          |
| <span data-ttu-id="f3678-213">System-Only</span><span class="sxs-lookup"><span data-stu-id="f3678-213">System-Only</span></span>            | <span data-ttu-id="f3678-214">Vero</span><span class="sxs-lookup"><span data-stu-id="f3678-214">True</span></span>                            |
| <span data-ttu-id="f3678-215">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="f3678-215">Is-Single-Valued</span></span>       | <span data-ttu-id="f3678-216">Vero</span><span class="sxs-lookup"><span data-stu-id="f3678-216">True</span></span>                            |
| <span data-ttu-id="f3678-217">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="f3678-217">Is Indexed</span></span>             | <span data-ttu-id="f3678-218">Vero</span><span class="sxs-lookup"><span data-stu-id="f3678-218">True</span></span>                            |
| <span data-ttu-id="f3678-219">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="f3678-219">In Global Catalog</span></span>      | <span data-ttu-id="f3678-220">Vero</span><span class="sxs-lookup"><span data-stu-id="f3678-220">True</span></span>                            |
| <span data-ttu-id="f3678-221">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="f3678-221">NT-Security-Descriptor</span></span> | <span data-ttu-id="f3678-222">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="f3678-222">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f3678-223">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f3678-223">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="f3678-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f3678-224">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="f3678-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f3678-225">Search-Flags</span></span>           | <span data-ttu-id="f3678-226">0x00000009</span><span class="sxs-lookup"><span data-stu-id="f3678-226">0x00000009</span></span>                      |
| <span data-ttu-id="f3678-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f3678-227">System-Flags</span></span>           | <span data-ttu-id="f3678-228">0x00000013</span><span class="sxs-lookup"><span data-stu-id="f3678-228">0x00000013</span></span>                      |
| <span data-ttu-id="f3678-229">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="f3678-229">Classes used in</span></span>        | [<span data-ttu-id="f3678-230">**In alto**</span><span class="sxs-lookup"><span data-stu-id="f3678-230">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f3678-231">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f3678-231">Windows Server 2008</span></span>



| <span data-ttu-id="f3678-232">Voce</span><span class="sxs-lookup"><span data-stu-id="f3678-232">Entry</span></span> | <span data-ttu-id="f3678-233">Valore</span><span class="sxs-lookup"><span data-stu-id="f3678-233">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f3678-234">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="f3678-234">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="f3678-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f3678-235">MAPI-Id</span></span>                | <span data-ttu-id="f3678-236">0x8154</span><span class="sxs-lookup"><span data-stu-id="f3678-236">0x8154</span></span>                          |
| <span data-ttu-id="f3678-237">System-Only</span><span class="sxs-lookup"><span data-stu-id="f3678-237">System-Only</span></span>            | <span data-ttu-id="f3678-238">Vero</span><span class="sxs-lookup"><span data-stu-id="f3678-238">True</span></span>                            |
| <span data-ttu-id="f3678-239">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="f3678-239">Is-Single-Valued</span></span>       | <span data-ttu-id="f3678-240">Vero</span><span class="sxs-lookup"><span data-stu-id="f3678-240">True</span></span>                            |
| <span data-ttu-id="f3678-241">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="f3678-241">Is Indexed</span></span>             | <span data-ttu-id="f3678-242">Vero</span><span class="sxs-lookup"><span data-stu-id="f3678-242">True</span></span>                            |
| <span data-ttu-id="f3678-243">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="f3678-243">In Global Catalog</span></span>      | <span data-ttu-id="f3678-244">Vero</span><span class="sxs-lookup"><span data-stu-id="f3678-244">True</span></span>                            |
| <span data-ttu-id="f3678-245">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="f3678-245">NT-Security-Descriptor</span></span> | <span data-ttu-id="f3678-246">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="f3678-246">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f3678-247">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f3678-247">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="f3678-248">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f3678-248">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="f3678-249">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f3678-249">Search-Flags</span></span>           | <span data-ttu-id="f3678-250">0x00000009</span><span class="sxs-lookup"><span data-stu-id="f3678-250">0x00000009</span></span>                      |
| <span data-ttu-id="f3678-251">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f3678-251">System-Flags</span></span>           | <span data-ttu-id="f3678-252">0x00000013</span><span class="sxs-lookup"><span data-stu-id="f3678-252">0x00000013</span></span>                      |
| <span data-ttu-id="f3678-253">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="f3678-253">Classes used in</span></span>        | [<span data-ttu-id="f3678-254">**In alto**</span><span class="sxs-lookup"><span data-stu-id="f3678-254">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f3678-255">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f3678-255">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f3678-256">Voce</span><span class="sxs-lookup"><span data-stu-id="f3678-256">Entry</span></span> | <span data-ttu-id="f3678-257">Valore</span><span class="sxs-lookup"><span data-stu-id="f3678-257">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f3678-258">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="f3678-258">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="f3678-259">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f3678-259">MAPI-Id</span></span>                | <span data-ttu-id="f3678-260">0x8154</span><span class="sxs-lookup"><span data-stu-id="f3678-260">0x8154</span></span>                          |
| <span data-ttu-id="f3678-261">System-Only</span><span class="sxs-lookup"><span data-stu-id="f3678-261">System-Only</span></span>            | <span data-ttu-id="f3678-262">Vero</span><span class="sxs-lookup"><span data-stu-id="f3678-262">True</span></span>                            |
| <span data-ttu-id="f3678-263">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="f3678-263">Is-Single-Valued</span></span>       | <span data-ttu-id="f3678-264">Vero</span><span class="sxs-lookup"><span data-stu-id="f3678-264">True</span></span>                            |
| <span data-ttu-id="f3678-265">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="f3678-265">Is Indexed</span></span>             | <span data-ttu-id="f3678-266">Vero</span><span class="sxs-lookup"><span data-stu-id="f3678-266">True</span></span>                            |
| <span data-ttu-id="f3678-267">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="f3678-267">In Global Catalog</span></span>      | <span data-ttu-id="f3678-268">Vero</span><span class="sxs-lookup"><span data-stu-id="f3678-268">True</span></span>                            |
| <span data-ttu-id="f3678-269">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="f3678-269">NT-Security-Descriptor</span></span> | <span data-ttu-id="f3678-270">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="f3678-270">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f3678-271">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f3678-271">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="f3678-272">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f3678-272">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="f3678-273">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f3678-273">Search-Flags</span></span>           | <span data-ttu-id="f3678-274">0x00000009</span><span class="sxs-lookup"><span data-stu-id="f3678-274">0x00000009</span></span>                      |
| <span data-ttu-id="f3678-275">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f3678-275">System-Flags</span></span>           | <span data-ttu-id="f3678-276">0x00000013</span><span class="sxs-lookup"><span data-stu-id="f3678-276">0x00000013</span></span>                      |
| <span data-ttu-id="f3678-277">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="f3678-277">Classes used in</span></span>        | [<span data-ttu-id="f3678-278">**In alto**</span><span class="sxs-lookup"><span data-stu-id="f3678-278">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f3678-279">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f3678-279">Windows Server 2012</span></span>



| <span data-ttu-id="f3678-280">Voce</span><span class="sxs-lookup"><span data-stu-id="f3678-280">Entry</span></span> | <span data-ttu-id="f3678-281">Valore</span><span class="sxs-lookup"><span data-stu-id="f3678-281">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f3678-282">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="f3678-282">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="f3678-283">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f3678-283">MAPI-Id</span></span>                | <span data-ttu-id="f3678-284">0x8154</span><span class="sxs-lookup"><span data-stu-id="f3678-284">0x8154</span></span>                          |
| <span data-ttu-id="f3678-285">System-Only</span><span class="sxs-lookup"><span data-stu-id="f3678-285">System-Only</span></span>            | <span data-ttu-id="f3678-286">Vero</span><span class="sxs-lookup"><span data-stu-id="f3678-286">True</span></span>                            |
| <span data-ttu-id="f3678-287">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="f3678-287">Is-Single-Valued</span></span>       | <span data-ttu-id="f3678-288">Vero</span><span class="sxs-lookup"><span data-stu-id="f3678-288">True</span></span>                            |
| <span data-ttu-id="f3678-289">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="f3678-289">Is Indexed</span></span>             | <span data-ttu-id="f3678-290">Vero</span><span class="sxs-lookup"><span data-stu-id="f3678-290">True</span></span>                            |
| <span data-ttu-id="f3678-291">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="f3678-291">In Global Catalog</span></span>      | <span data-ttu-id="f3678-292">Vero</span><span class="sxs-lookup"><span data-stu-id="f3678-292">True</span></span>                            |
| <span data-ttu-id="f3678-293">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="f3678-293">NT-Security-Descriptor</span></span> | <span data-ttu-id="f3678-294">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="f3678-294">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f3678-295">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f3678-295">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="f3678-296">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f3678-296">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="f3678-297">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f3678-297">Search-Flags</span></span>           | <span data-ttu-id="f3678-298">0x00000009</span><span class="sxs-lookup"><span data-stu-id="f3678-298">0x00000009</span></span>                      |
| <span data-ttu-id="f3678-299">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f3678-299">System-Flags</span></span>           | <span data-ttu-id="f3678-300">0x00000013</span><span class="sxs-lookup"><span data-stu-id="f3678-300">0x00000013</span></span>                      |
| <span data-ttu-id="f3678-301">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="f3678-301">Classes used in</span></span>        | [<span data-ttu-id="f3678-302">**In alto**</span><span class="sxs-lookup"><span data-stu-id="f3678-302">**Top**</span></span>](c-top.md)<br/> |



 

 





