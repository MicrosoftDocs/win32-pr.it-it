---
title: Attributo DSA-Signature
description: Il DSA-Signature di un oggetto è l'ID chiamata dell'ultima directory per la modifica dell'oggetto.
ms.assetid: 7ae65f15-b0c9-4d73-8a65-92c23d0a239b
ms.tgt_platform: multiple
keywords:
- Schema AD DSA-Signature attribute
- Schema AD dell'attributo dSASignature
topic_type:
- apiref
api_name:
- DSA-Signature
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdfed9e2cb871f3418c8bdbf4401d03c1e78492b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "106302934"
---
# <a name="dsa-signature-attribute"></a><span data-ttu-id="a505b-105">Attributo DSA-Signature</span><span class="sxs-lookup"><span data-stu-id="a505b-105">DSA-Signature attribute</span></span>

<span data-ttu-id="a505b-106">Il DSA-Signature di un oggetto è l'ID chiamata dell'ultima directory per la modifica dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a505b-106">The DSA-Signature of an object is the Invocation-ID of the last directory to modify the object.</span></span>



| <span data-ttu-id="a505b-107">Voce</span><span class="sxs-lookup"><span data-stu-id="a505b-107">Entry</span></span> | <span data-ttu-id="a505b-108">Valore</span><span class="sxs-lookup"><span data-stu-id="a505b-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="a505b-109">CN</span><span class="sxs-lookup"><span data-stu-id="a505b-109">CN</span></span>                | <span data-ttu-id="a505b-110">DSA-Signature</span><span class="sxs-lookup"><span data-stu-id="a505b-110">DSA-Signature</span></span>                                         |
| <span data-ttu-id="a505b-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="a505b-111">Ldap-Display-Name</span></span> | <span data-ttu-id="a505b-112">dSASignature</span><span class="sxs-lookup"><span data-stu-id="a505b-112">dSASignature</span></span>                                          |
| <span data-ttu-id="a505b-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="a505b-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="a505b-114">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="a505b-114">Update Privilege</span></span>  | <span data-ttu-id="a505b-115">Questo valore viene impostato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="a505b-115">This value is set by the system.</span></span>                      |
| <span data-ttu-id="a505b-116">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="a505b-116">Update Frequency</span></span>  | <span data-ttu-id="a505b-117">Ogni volta che un oggetto viene modificato.</span><span class="sxs-lookup"><span data-stu-id="a505b-117">Whenever an object is modified.</span></span>                       |
| <span data-ttu-id="a505b-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a505b-118">Attribute-Id</span></span>      | <span data-ttu-id="a505b-119">1.2.840.113556.1.2.74</span><span class="sxs-lookup"><span data-stu-id="a505b-119">1.2.840.113556.1.2.74</span></span>                                 |
| <span data-ttu-id="a505b-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="a505b-120">System-Id-Guid</span></span>    | <span data-ttu-id="a505b-121">167757bc-47f3-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="a505b-121">167757bc-47f3-11d1-a9c3-0000f80367c1</span></span>                  |
| <span data-ttu-id="a505b-122">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a505b-122">Syntax</span></span>            | [<span data-ttu-id="a505b-123">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="a505b-123">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="a505b-124">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="a505b-124">Implementations</span></span>

-   [<span data-ttu-id="a505b-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="a505b-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="a505b-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a505b-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a505b-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="a505b-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="a505b-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a505b-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a505b-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a505b-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a505b-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a505b-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a505b-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a505b-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="a505b-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a505b-132">Windows 2000 Server</span></span>



| <span data-ttu-id="a505b-133">Voce</span><span class="sxs-lookup"><span data-stu-id="a505b-133">Entry</span></span> | <span data-ttu-id="a505b-134">Valore</span><span class="sxs-lookup"><span data-stu-id="a505b-134">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a505b-135">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="a505b-135">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="a505b-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a505b-136">MAPI-Id</span></span>                | <span data-ttu-id="a505b-137">0x8077</span><span class="sxs-lookup"><span data-stu-id="a505b-137">0x8077</span></span>                          |
| <span data-ttu-id="a505b-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="a505b-138">System-Only</span></span>            | <span data-ttu-id="a505b-139">Falso</span><span class="sxs-lookup"><span data-stu-id="a505b-139">False</span></span>                           |
| <span data-ttu-id="a505b-140">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="a505b-140">Is-Single-Valued</span></span>       | <span data-ttu-id="a505b-141">Vero</span><span class="sxs-lookup"><span data-stu-id="a505b-141">True</span></span>                            |
| <span data-ttu-id="a505b-142">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="a505b-142">Is Indexed</span></span>             | <span data-ttu-id="a505b-143">Falso</span><span class="sxs-lookup"><span data-stu-id="a505b-143">False</span></span>                           |
| <span data-ttu-id="a505b-144">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="a505b-144">In Global Catalog</span></span>      | <span data-ttu-id="a505b-145">Falso</span><span class="sxs-lookup"><span data-stu-id="a505b-145">False</span></span>                           |
| <span data-ttu-id="a505b-146">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="a505b-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="a505b-147">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="a505b-147">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a505b-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a505b-148">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a505b-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a505b-149">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a505b-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a505b-150">Search-Flags</span></span>           | <span data-ttu-id="a505b-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a505b-151">0x00000000</span></span>                      |
| <span data-ttu-id="a505b-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a505b-152">System-Flags</span></span>           | <span data-ttu-id="a505b-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a505b-153">0x00000010</span></span>                      |
| <span data-ttu-id="a505b-154">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="a505b-154">Classes used in</span></span>        | [<span data-ttu-id="a505b-155">**In alto**</span><span class="sxs-lookup"><span data-stu-id="a505b-155">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="a505b-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a505b-156">Windows Server 2003</span></span>



| <span data-ttu-id="a505b-157">Voce</span><span class="sxs-lookup"><span data-stu-id="a505b-157">Entry</span></span> | <span data-ttu-id="a505b-158">Valore</span><span class="sxs-lookup"><span data-stu-id="a505b-158">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a505b-159">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="a505b-159">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="a505b-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a505b-160">MAPI-Id</span></span>                | <span data-ttu-id="a505b-161">0x8077</span><span class="sxs-lookup"><span data-stu-id="a505b-161">0x8077</span></span>                          |
| <span data-ttu-id="a505b-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="a505b-162">System-Only</span></span>            | <span data-ttu-id="a505b-163">Falso</span><span class="sxs-lookup"><span data-stu-id="a505b-163">False</span></span>                           |
| <span data-ttu-id="a505b-164">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="a505b-164">Is-Single-Valued</span></span>       | <span data-ttu-id="a505b-165">Vero</span><span class="sxs-lookup"><span data-stu-id="a505b-165">True</span></span>                            |
| <span data-ttu-id="a505b-166">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="a505b-166">Is Indexed</span></span>             | <span data-ttu-id="a505b-167">Falso</span><span class="sxs-lookup"><span data-stu-id="a505b-167">False</span></span>                           |
| <span data-ttu-id="a505b-168">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="a505b-168">In Global Catalog</span></span>      | <span data-ttu-id="a505b-169">Falso</span><span class="sxs-lookup"><span data-stu-id="a505b-169">False</span></span>                           |
| <span data-ttu-id="a505b-170">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="a505b-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="a505b-171">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="a505b-171">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a505b-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a505b-172">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a505b-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a505b-173">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a505b-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a505b-174">Search-Flags</span></span>           | <span data-ttu-id="a505b-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a505b-175">0x00000000</span></span>                      |
| <span data-ttu-id="a505b-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a505b-176">System-Flags</span></span>           | <span data-ttu-id="a505b-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a505b-177">0x00000010</span></span>                      |
| <span data-ttu-id="a505b-178">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="a505b-178">Classes used in</span></span>        | [<span data-ttu-id="a505b-179">**In alto**</span><span class="sxs-lookup"><span data-stu-id="a505b-179">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="a505b-180">ADAM</span><span class="sxs-lookup"><span data-stu-id="a505b-180">ADAM</span></span>



| <span data-ttu-id="a505b-181">Voce</span><span class="sxs-lookup"><span data-stu-id="a505b-181">Entry</span></span> | <span data-ttu-id="a505b-182">Valore</span><span class="sxs-lookup"><span data-stu-id="a505b-182">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a505b-183">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="a505b-183">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="a505b-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a505b-184">MAPI-Id</span></span>                | <span data-ttu-id="a505b-185">0x8077</span><span class="sxs-lookup"><span data-stu-id="a505b-185">0x8077</span></span>                          |
| <span data-ttu-id="a505b-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="a505b-186">System-Only</span></span>            | <span data-ttu-id="a505b-187">Falso</span><span class="sxs-lookup"><span data-stu-id="a505b-187">False</span></span>                           |
| <span data-ttu-id="a505b-188">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="a505b-188">Is-Single-Valued</span></span>       | <span data-ttu-id="a505b-189">Vero</span><span class="sxs-lookup"><span data-stu-id="a505b-189">True</span></span>                            |
| <span data-ttu-id="a505b-190">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="a505b-190">Is Indexed</span></span>             | <span data-ttu-id="a505b-191">Falso</span><span class="sxs-lookup"><span data-stu-id="a505b-191">False</span></span>                           |
| <span data-ttu-id="a505b-192">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="a505b-192">In Global Catalog</span></span>      | <span data-ttu-id="a505b-193">Falso</span><span class="sxs-lookup"><span data-stu-id="a505b-193">False</span></span>                           |
| <span data-ttu-id="a505b-194">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="a505b-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="a505b-195">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="a505b-195">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a505b-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a505b-196">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a505b-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a505b-197">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a505b-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a505b-198">Search-Flags</span></span>           | <span data-ttu-id="a505b-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a505b-199">0x00000000</span></span>                      |
| <span data-ttu-id="a505b-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a505b-200">System-Flags</span></span>           | <span data-ttu-id="a505b-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a505b-201">0x00000010</span></span>                      |
| <span data-ttu-id="a505b-202">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="a505b-202">Classes used in</span></span>        | [<span data-ttu-id="a505b-203">**In alto**</span><span class="sxs-lookup"><span data-stu-id="a505b-203">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a505b-204">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a505b-204">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a505b-205">Voce</span><span class="sxs-lookup"><span data-stu-id="a505b-205">Entry</span></span> | <span data-ttu-id="a505b-206">Valore</span><span class="sxs-lookup"><span data-stu-id="a505b-206">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a505b-207">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="a505b-207">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="a505b-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a505b-208">MAPI-Id</span></span>                | <span data-ttu-id="a505b-209">0x8077</span><span class="sxs-lookup"><span data-stu-id="a505b-209">0x8077</span></span>                          |
| <span data-ttu-id="a505b-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="a505b-210">System-Only</span></span>            | <span data-ttu-id="a505b-211">Falso</span><span class="sxs-lookup"><span data-stu-id="a505b-211">False</span></span>                           |
| <span data-ttu-id="a505b-212">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="a505b-212">Is-Single-Valued</span></span>       | <span data-ttu-id="a505b-213">Vero</span><span class="sxs-lookup"><span data-stu-id="a505b-213">True</span></span>                            |
| <span data-ttu-id="a505b-214">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="a505b-214">Is Indexed</span></span>             | <span data-ttu-id="a505b-215">Falso</span><span class="sxs-lookup"><span data-stu-id="a505b-215">False</span></span>                           |
| <span data-ttu-id="a505b-216">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="a505b-216">In Global Catalog</span></span>      | <span data-ttu-id="a505b-217">Falso</span><span class="sxs-lookup"><span data-stu-id="a505b-217">False</span></span>                           |
| <span data-ttu-id="a505b-218">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="a505b-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="a505b-219">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="a505b-219">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a505b-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a505b-220">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a505b-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a505b-221">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a505b-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a505b-222">Search-Flags</span></span>           | <span data-ttu-id="a505b-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a505b-223">0x00000000</span></span>                      |
| <span data-ttu-id="a505b-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a505b-224">System-Flags</span></span>           | <span data-ttu-id="a505b-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a505b-225">0x00000010</span></span>                      |
| <span data-ttu-id="a505b-226">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="a505b-226">Classes used in</span></span>        | [<span data-ttu-id="a505b-227">**In alto**</span><span class="sxs-lookup"><span data-stu-id="a505b-227">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a505b-228">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a505b-228">Windows Server 2008</span></span>



| <span data-ttu-id="a505b-229">Voce</span><span class="sxs-lookup"><span data-stu-id="a505b-229">Entry</span></span> | <span data-ttu-id="a505b-230">Valore</span><span class="sxs-lookup"><span data-stu-id="a505b-230">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a505b-231">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="a505b-231">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="a505b-232">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a505b-232">MAPI-Id</span></span>                | <span data-ttu-id="a505b-233">0x8077</span><span class="sxs-lookup"><span data-stu-id="a505b-233">0x8077</span></span>                          |
| <span data-ttu-id="a505b-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="a505b-234">System-Only</span></span>            | <span data-ttu-id="a505b-235">Falso</span><span class="sxs-lookup"><span data-stu-id="a505b-235">False</span></span>                           |
| <span data-ttu-id="a505b-236">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="a505b-236">Is-Single-Valued</span></span>       | <span data-ttu-id="a505b-237">Vero</span><span class="sxs-lookup"><span data-stu-id="a505b-237">True</span></span>                            |
| <span data-ttu-id="a505b-238">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="a505b-238">Is Indexed</span></span>             | <span data-ttu-id="a505b-239">Falso</span><span class="sxs-lookup"><span data-stu-id="a505b-239">False</span></span>                           |
| <span data-ttu-id="a505b-240">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="a505b-240">In Global Catalog</span></span>      | <span data-ttu-id="a505b-241">Falso</span><span class="sxs-lookup"><span data-stu-id="a505b-241">False</span></span>                           |
| <span data-ttu-id="a505b-242">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="a505b-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="a505b-243">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="a505b-243">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a505b-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a505b-244">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a505b-245">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a505b-245">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a505b-246">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a505b-246">Search-Flags</span></span>           | <span data-ttu-id="a505b-247">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a505b-247">0x00000000</span></span>                      |
| <span data-ttu-id="a505b-248">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a505b-248">System-Flags</span></span>           | <span data-ttu-id="a505b-249">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a505b-249">0x00000010</span></span>                      |
| <span data-ttu-id="a505b-250">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="a505b-250">Classes used in</span></span>        | [<span data-ttu-id="a505b-251">**In alto**</span><span class="sxs-lookup"><span data-stu-id="a505b-251">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a505b-252">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a505b-252">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a505b-253">Voce</span><span class="sxs-lookup"><span data-stu-id="a505b-253">Entry</span></span> | <span data-ttu-id="a505b-254">Valore</span><span class="sxs-lookup"><span data-stu-id="a505b-254">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a505b-255">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="a505b-255">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="a505b-256">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a505b-256">MAPI-Id</span></span>                | <span data-ttu-id="a505b-257">0x8077</span><span class="sxs-lookup"><span data-stu-id="a505b-257">0x8077</span></span>                          |
| <span data-ttu-id="a505b-258">System-Only</span><span class="sxs-lookup"><span data-stu-id="a505b-258">System-Only</span></span>            | <span data-ttu-id="a505b-259">Falso</span><span class="sxs-lookup"><span data-stu-id="a505b-259">False</span></span>                           |
| <span data-ttu-id="a505b-260">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="a505b-260">Is-Single-Valued</span></span>       | <span data-ttu-id="a505b-261">Vero</span><span class="sxs-lookup"><span data-stu-id="a505b-261">True</span></span>                            |
| <span data-ttu-id="a505b-262">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="a505b-262">Is Indexed</span></span>             | <span data-ttu-id="a505b-263">Falso</span><span class="sxs-lookup"><span data-stu-id="a505b-263">False</span></span>                           |
| <span data-ttu-id="a505b-264">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="a505b-264">In Global Catalog</span></span>      | <span data-ttu-id="a505b-265">Falso</span><span class="sxs-lookup"><span data-stu-id="a505b-265">False</span></span>                           |
| <span data-ttu-id="a505b-266">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="a505b-266">NT-Security-Descriptor</span></span> | <span data-ttu-id="a505b-267">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="a505b-267">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a505b-268">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a505b-268">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a505b-269">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a505b-269">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a505b-270">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a505b-270">Search-Flags</span></span>           | <span data-ttu-id="a505b-271">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a505b-271">0x00000000</span></span>                      |
| <span data-ttu-id="a505b-272">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a505b-272">System-Flags</span></span>           | <span data-ttu-id="a505b-273">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a505b-273">0x00000010</span></span>                      |
| <span data-ttu-id="a505b-274">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="a505b-274">Classes used in</span></span>        | [<span data-ttu-id="a505b-275">**In alto**</span><span class="sxs-lookup"><span data-stu-id="a505b-275">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a505b-276">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a505b-276">Windows Server 2012</span></span>



| <span data-ttu-id="a505b-277">Voce</span><span class="sxs-lookup"><span data-stu-id="a505b-277">Entry</span></span> | <span data-ttu-id="a505b-278">Valore</span><span class="sxs-lookup"><span data-stu-id="a505b-278">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a505b-279">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="a505b-279">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="a505b-280">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a505b-280">MAPI-Id</span></span>                | <span data-ttu-id="a505b-281">0x8077</span><span class="sxs-lookup"><span data-stu-id="a505b-281">0x8077</span></span>                          |
| <span data-ttu-id="a505b-282">System-Only</span><span class="sxs-lookup"><span data-stu-id="a505b-282">System-Only</span></span>            | <span data-ttu-id="a505b-283">Falso</span><span class="sxs-lookup"><span data-stu-id="a505b-283">False</span></span>                           |
| <span data-ttu-id="a505b-284">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="a505b-284">Is-Single-Valued</span></span>       | <span data-ttu-id="a505b-285">Vero</span><span class="sxs-lookup"><span data-stu-id="a505b-285">True</span></span>                            |
| <span data-ttu-id="a505b-286">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="a505b-286">Is Indexed</span></span>             | <span data-ttu-id="a505b-287">Falso</span><span class="sxs-lookup"><span data-stu-id="a505b-287">False</span></span>                           |
| <span data-ttu-id="a505b-288">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="a505b-288">In Global Catalog</span></span>      | <span data-ttu-id="a505b-289">Falso</span><span class="sxs-lookup"><span data-stu-id="a505b-289">False</span></span>                           |
| <span data-ttu-id="a505b-290">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="a505b-290">NT-Security-Descriptor</span></span> | <span data-ttu-id="a505b-291">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="a505b-291">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a505b-292">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a505b-292">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a505b-293">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a505b-293">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a505b-294">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a505b-294">Search-Flags</span></span>           | <span data-ttu-id="a505b-295">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a505b-295">0x00000000</span></span>                      |
| <span data-ttu-id="a505b-296">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a505b-296">System-Flags</span></span>           | <span data-ttu-id="a505b-297">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a505b-297">0x00000010</span></span>                      |
| <span data-ttu-id="a505b-298">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="a505b-298">Classes used in</span></span>        | [<span data-ttu-id="a505b-299">**In alto**</span><span class="sxs-lookup"><span data-stu-id="a505b-299">**Top**</span></span>](c-top.md)<br/> |



 

 





