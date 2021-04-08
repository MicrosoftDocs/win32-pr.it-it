---
title: Attributo USN-Changed
description: Numero di sequenza di aggiornamento (USN) assegnato dalla directory locale per la modifica più recente, inclusa la creazione. Vedere anche, creato con USN.
ms.assetid: ccd61940-2c0a-4d46-af9f-5f23f577a1ad
ms.tgt_platform: multiple
keywords:
- Schema AD USN-Changed attribute
- Schema AD dell'attributo uSNChanged
topic_type:
- apiref
api_name:
- USN-Changed
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0c00f30a2ba7ca38f78246cd14b33ea358da6fa
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744866"
---
# <a name="usn-changed-attribute"></a><span data-ttu-id="e9e76-106">Attributo USN-Changed</span><span class="sxs-lookup"><span data-stu-id="e9e76-106">USN-Changed attribute</span></span>

<span data-ttu-id="e9e76-107">Numero di sequenza di aggiornamento (USN) assegnato dalla directory locale per la modifica più recente, inclusa la creazione.</span><span class="sxs-lookup"><span data-stu-id="e9e76-107">The update sequence number (USN) assigned by the local directory for the latest change, including creation.</span></span> <span data-ttu-id="e9e76-108">Vedere anche, [**creato con USN**](a-usncreated.md).</span><span class="sxs-lookup"><span data-stu-id="e9e76-108">See also , [**USN-Created**](a-usncreated.md).</span></span>



| <span data-ttu-id="e9e76-109">Voce</span><span class="sxs-lookup"><span data-stu-id="e9e76-109">Entry</span></span> | <span data-ttu-id="e9e76-110">Valore</span><span class="sxs-lookup"><span data-stu-id="e9e76-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="e9e76-111">CN</span><span class="sxs-lookup"><span data-stu-id="e9e76-111">CN</span></span>                | <span data-ttu-id="e9e76-112">USN-Changed</span><span class="sxs-lookup"><span data-stu-id="e9e76-112">USN-Changed</span></span>                          |
| <span data-ttu-id="e9e76-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="e9e76-113">Ldap-Display-Name</span></span> | <span data-ttu-id="e9e76-114">uSNChanged</span><span class="sxs-lookup"><span data-stu-id="e9e76-114">uSNChanged</span></span>                           |
| <span data-ttu-id="e9e76-115">Dimensione</span><span class="sxs-lookup"><span data-stu-id="e9e76-115">Size</span></span>              | <span data-ttu-id="e9e76-116">8 byte</span><span class="sxs-lookup"><span data-stu-id="e9e76-116">8 bytes</span></span>                              |
| <span data-ttu-id="e9e76-117">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="e9e76-117">Update Privilege</span></span>  | <span data-ttu-id="e9e76-118">Questo valore viene impostato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="e9e76-118">This value is set by the system.</span></span>     |
| <span data-ttu-id="e9e76-119">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="e9e76-119">Update Frequency</span></span>  | <span data-ttu-id="e9e76-120">Quando l'oggetto viene modificato.</span><span class="sxs-lookup"><span data-stu-id="e9e76-120">When the object is changed.</span></span>          |
| <span data-ttu-id="e9e76-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e9e76-121">Attribute-Id</span></span>      | <span data-ttu-id="e9e76-122">1.2.840.113556.1.2.120</span><span class="sxs-lookup"><span data-stu-id="e9e76-122">1.2.840.113556.1.2.120</span></span>               |
| <span data-ttu-id="e9e76-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="e9e76-123">System-Id-Guid</span></span>    | <span data-ttu-id="e9e76-124">bf967a6f-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="e9e76-124">bf967a6f-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="e9e76-125">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e9e76-125">Syntax</span></span>            | [<span data-ttu-id="e9e76-126">**Interval**</span><span class="sxs-lookup"><span data-stu-id="e9e76-126">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="e9e76-127">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="e9e76-127">Implementations</span></span>

-   [<span data-ttu-id="e9e76-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="e9e76-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="e9e76-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e9e76-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e9e76-130">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="e9e76-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="e9e76-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e9e76-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e9e76-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e9e76-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e9e76-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e9e76-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e9e76-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e9e76-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="e9e76-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e9e76-135">Windows 2000 Server</span></span>



| <span data-ttu-id="e9e76-136">Voce</span><span class="sxs-lookup"><span data-stu-id="e9e76-136">Entry</span></span> | <span data-ttu-id="e9e76-137">Valore</span><span class="sxs-lookup"><span data-stu-id="e9e76-137">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="e9e76-138">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="e9e76-138">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="e9e76-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e9e76-139">MAPI-Id</span></span>                | <span data-ttu-id="e9e76-140">0x8029</span><span class="sxs-lookup"><span data-stu-id="e9e76-140">0x8029</span></span>                          |
| <span data-ttu-id="e9e76-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="e9e76-141">System-Only</span></span>            | <span data-ttu-id="e9e76-142">Vero</span><span class="sxs-lookup"><span data-stu-id="e9e76-142">True</span></span>                            |
| <span data-ttu-id="e9e76-143">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="e9e76-143">Is-Single-Valued</span></span>       | <span data-ttu-id="e9e76-144">Vero</span><span class="sxs-lookup"><span data-stu-id="e9e76-144">True</span></span>                            |
| <span data-ttu-id="e9e76-145">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="e9e76-145">Is Indexed</span></span>             | <span data-ttu-id="e9e76-146">Vero</span><span class="sxs-lookup"><span data-stu-id="e9e76-146">True</span></span>                            |
| <span data-ttu-id="e9e76-147">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="e9e76-147">In Global Catalog</span></span>      | <span data-ttu-id="e9e76-148">Vero</span><span class="sxs-lookup"><span data-stu-id="e9e76-148">True</span></span>                            |
| <span data-ttu-id="e9e76-149">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="e9e76-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="e9e76-150">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="e9e76-150">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="e9e76-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e9e76-151">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="e9e76-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e9e76-152">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="e9e76-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e9e76-153">Search-Flags</span></span>           | <span data-ttu-id="e9e76-154">0x00000009</span><span class="sxs-lookup"><span data-stu-id="e9e76-154">0x00000009</span></span>                      |
| <span data-ttu-id="e9e76-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e9e76-155">System-Flags</span></span>           | <span data-ttu-id="e9e76-156">0x00000013</span><span class="sxs-lookup"><span data-stu-id="e9e76-156">0x00000013</span></span>                      |
| <span data-ttu-id="e9e76-157">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="e9e76-157">Classes used in</span></span>        | [<span data-ttu-id="e9e76-158">**In alto**</span><span class="sxs-lookup"><span data-stu-id="e9e76-158">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="e9e76-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e9e76-159">Windows Server 2003</span></span>



| <span data-ttu-id="e9e76-160">Voce</span><span class="sxs-lookup"><span data-stu-id="e9e76-160">Entry</span></span> | <span data-ttu-id="e9e76-161">Valore</span><span class="sxs-lookup"><span data-stu-id="e9e76-161">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="e9e76-162">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="e9e76-162">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="e9e76-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e9e76-163">MAPI-Id</span></span>                | <span data-ttu-id="e9e76-164">0x8029</span><span class="sxs-lookup"><span data-stu-id="e9e76-164">0x8029</span></span>                          |
| <span data-ttu-id="e9e76-165">System-Only</span><span class="sxs-lookup"><span data-stu-id="e9e76-165">System-Only</span></span>            | <span data-ttu-id="e9e76-166">Vero</span><span class="sxs-lookup"><span data-stu-id="e9e76-166">True</span></span>                            |
| <span data-ttu-id="e9e76-167">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="e9e76-167">Is-Single-Valued</span></span>       | <span data-ttu-id="e9e76-168">Vero</span><span class="sxs-lookup"><span data-stu-id="e9e76-168">True</span></span>                            |
| <span data-ttu-id="e9e76-169">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="e9e76-169">Is Indexed</span></span>             | <span data-ttu-id="e9e76-170">Vero</span><span class="sxs-lookup"><span data-stu-id="e9e76-170">True</span></span>                            |
| <span data-ttu-id="e9e76-171">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="e9e76-171">In Global Catalog</span></span>      | <span data-ttu-id="e9e76-172">Vero</span><span class="sxs-lookup"><span data-stu-id="e9e76-172">True</span></span>                            |
| <span data-ttu-id="e9e76-173">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="e9e76-173">NT-Security-Descriptor</span></span> | <span data-ttu-id="e9e76-174">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="e9e76-174">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="e9e76-175">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e9e76-175">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="e9e76-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e9e76-176">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="e9e76-177">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e9e76-177">Search-Flags</span></span>           | <span data-ttu-id="e9e76-178">0x00000009</span><span class="sxs-lookup"><span data-stu-id="e9e76-178">0x00000009</span></span>                      |
| <span data-ttu-id="e9e76-179">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e9e76-179">System-Flags</span></span>           | <span data-ttu-id="e9e76-180">0x00000013</span><span class="sxs-lookup"><span data-stu-id="e9e76-180">0x00000013</span></span>                      |
| <span data-ttu-id="e9e76-181">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="e9e76-181">Classes used in</span></span>        | [<span data-ttu-id="e9e76-182">**In alto**</span><span class="sxs-lookup"><span data-stu-id="e9e76-182">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="e9e76-183">ADAM</span><span class="sxs-lookup"><span data-stu-id="e9e76-183">ADAM</span></span>



| <span data-ttu-id="e9e76-184">Voce</span><span class="sxs-lookup"><span data-stu-id="e9e76-184">Entry</span></span> | <span data-ttu-id="e9e76-185">Valore</span><span class="sxs-lookup"><span data-stu-id="e9e76-185">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="e9e76-186">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="e9e76-186">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="e9e76-187">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e9e76-187">MAPI-Id</span></span>                | <span data-ttu-id="e9e76-188">0x8029</span><span class="sxs-lookup"><span data-stu-id="e9e76-188">0x8029</span></span>                          |
| <span data-ttu-id="e9e76-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="e9e76-189">System-Only</span></span>            | <span data-ttu-id="e9e76-190">Vero</span><span class="sxs-lookup"><span data-stu-id="e9e76-190">True</span></span>                            |
| <span data-ttu-id="e9e76-191">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="e9e76-191">Is-Single-Valued</span></span>       | <span data-ttu-id="e9e76-192">Vero</span><span class="sxs-lookup"><span data-stu-id="e9e76-192">True</span></span>                            |
| <span data-ttu-id="e9e76-193">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="e9e76-193">Is Indexed</span></span>             | <span data-ttu-id="e9e76-194">Vero</span><span class="sxs-lookup"><span data-stu-id="e9e76-194">True</span></span>                            |
| <span data-ttu-id="e9e76-195">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="e9e76-195">In Global Catalog</span></span>      | <span data-ttu-id="e9e76-196">Vero</span><span class="sxs-lookup"><span data-stu-id="e9e76-196">True</span></span>                            |
| <span data-ttu-id="e9e76-197">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="e9e76-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="e9e76-198">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="e9e76-198">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="e9e76-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e9e76-199">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="e9e76-200">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e9e76-200">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="e9e76-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e9e76-201">Search-Flags</span></span>           | <span data-ttu-id="e9e76-202">0x00000009</span><span class="sxs-lookup"><span data-stu-id="e9e76-202">0x00000009</span></span>                      |
| <span data-ttu-id="e9e76-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e9e76-203">System-Flags</span></span>           | <span data-ttu-id="e9e76-204">0x00000013</span><span class="sxs-lookup"><span data-stu-id="e9e76-204">0x00000013</span></span>                      |
| <span data-ttu-id="e9e76-205">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="e9e76-205">Classes used in</span></span>        | [<span data-ttu-id="e9e76-206">**In alto**</span><span class="sxs-lookup"><span data-stu-id="e9e76-206">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e9e76-207">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e9e76-207">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e9e76-208">Voce</span><span class="sxs-lookup"><span data-stu-id="e9e76-208">Entry</span></span> | <span data-ttu-id="e9e76-209">Valore</span><span class="sxs-lookup"><span data-stu-id="e9e76-209">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="e9e76-210">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="e9e76-210">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="e9e76-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e9e76-211">MAPI-Id</span></span>                | <span data-ttu-id="e9e76-212">0x8029</span><span class="sxs-lookup"><span data-stu-id="e9e76-212">0x8029</span></span>                          |
| <span data-ttu-id="e9e76-213">System-Only</span><span class="sxs-lookup"><span data-stu-id="e9e76-213">System-Only</span></span>            | <span data-ttu-id="e9e76-214">Vero</span><span class="sxs-lookup"><span data-stu-id="e9e76-214">True</span></span>                            |
| <span data-ttu-id="e9e76-215">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="e9e76-215">Is-Single-Valued</span></span>       | <span data-ttu-id="e9e76-216">Vero</span><span class="sxs-lookup"><span data-stu-id="e9e76-216">True</span></span>                            |
| <span data-ttu-id="e9e76-217">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="e9e76-217">Is Indexed</span></span>             | <span data-ttu-id="e9e76-218">Vero</span><span class="sxs-lookup"><span data-stu-id="e9e76-218">True</span></span>                            |
| <span data-ttu-id="e9e76-219">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="e9e76-219">In Global Catalog</span></span>      | <span data-ttu-id="e9e76-220">Vero</span><span class="sxs-lookup"><span data-stu-id="e9e76-220">True</span></span>                            |
| <span data-ttu-id="e9e76-221">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="e9e76-221">NT-Security-Descriptor</span></span> | <span data-ttu-id="e9e76-222">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="e9e76-222">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="e9e76-223">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e9e76-223">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="e9e76-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e9e76-224">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="e9e76-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e9e76-225">Search-Flags</span></span>           | <span data-ttu-id="e9e76-226">0x00000009</span><span class="sxs-lookup"><span data-stu-id="e9e76-226">0x00000009</span></span>                      |
| <span data-ttu-id="e9e76-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e9e76-227">System-Flags</span></span>           | <span data-ttu-id="e9e76-228">0x00000013</span><span class="sxs-lookup"><span data-stu-id="e9e76-228">0x00000013</span></span>                      |
| <span data-ttu-id="e9e76-229">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="e9e76-229">Classes used in</span></span>        | [<span data-ttu-id="e9e76-230">**In alto**</span><span class="sxs-lookup"><span data-stu-id="e9e76-230">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="e9e76-231">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e9e76-231">Windows Server 2008</span></span>



| <span data-ttu-id="e9e76-232">Voce</span><span class="sxs-lookup"><span data-stu-id="e9e76-232">Entry</span></span> | <span data-ttu-id="e9e76-233">Valore</span><span class="sxs-lookup"><span data-stu-id="e9e76-233">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="e9e76-234">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="e9e76-234">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="e9e76-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e9e76-235">MAPI-Id</span></span>                | <span data-ttu-id="e9e76-236">0x8029</span><span class="sxs-lookup"><span data-stu-id="e9e76-236">0x8029</span></span>                          |
| <span data-ttu-id="e9e76-237">System-Only</span><span class="sxs-lookup"><span data-stu-id="e9e76-237">System-Only</span></span>            | <span data-ttu-id="e9e76-238">Vero</span><span class="sxs-lookup"><span data-stu-id="e9e76-238">True</span></span>                            |
| <span data-ttu-id="e9e76-239">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="e9e76-239">Is-Single-Valued</span></span>       | <span data-ttu-id="e9e76-240">Vero</span><span class="sxs-lookup"><span data-stu-id="e9e76-240">True</span></span>                            |
| <span data-ttu-id="e9e76-241">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="e9e76-241">Is Indexed</span></span>             | <span data-ttu-id="e9e76-242">Vero</span><span class="sxs-lookup"><span data-stu-id="e9e76-242">True</span></span>                            |
| <span data-ttu-id="e9e76-243">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="e9e76-243">In Global Catalog</span></span>      | <span data-ttu-id="e9e76-244">Vero</span><span class="sxs-lookup"><span data-stu-id="e9e76-244">True</span></span>                            |
| <span data-ttu-id="e9e76-245">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="e9e76-245">NT-Security-Descriptor</span></span> | <span data-ttu-id="e9e76-246">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="e9e76-246">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="e9e76-247">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e9e76-247">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="e9e76-248">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e9e76-248">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="e9e76-249">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e9e76-249">Search-Flags</span></span>           | <span data-ttu-id="e9e76-250">0x00000009</span><span class="sxs-lookup"><span data-stu-id="e9e76-250">0x00000009</span></span>                      |
| <span data-ttu-id="e9e76-251">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e9e76-251">System-Flags</span></span>           | <span data-ttu-id="e9e76-252">0x00000013</span><span class="sxs-lookup"><span data-stu-id="e9e76-252">0x00000013</span></span>                      |
| <span data-ttu-id="e9e76-253">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="e9e76-253">Classes used in</span></span>        | [<span data-ttu-id="e9e76-254">**In alto**</span><span class="sxs-lookup"><span data-stu-id="e9e76-254">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e9e76-255">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e9e76-255">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e9e76-256">Voce</span><span class="sxs-lookup"><span data-stu-id="e9e76-256">Entry</span></span> | <span data-ttu-id="e9e76-257">Valore</span><span class="sxs-lookup"><span data-stu-id="e9e76-257">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="e9e76-258">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="e9e76-258">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="e9e76-259">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e9e76-259">MAPI-Id</span></span>                | <span data-ttu-id="e9e76-260">0x8029</span><span class="sxs-lookup"><span data-stu-id="e9e76-260">0x8029</span></span>                          |
| <span data-ttu-id="e9e76-261">System-Only</span><span class="sxs-lookup"><span data-stu-id="e9e76-261">System-Only</span></span>            | <span data-ttu-id="e9e76-262">Vero</span><span class="sxs-lookup"><span data-stu-id="e9e76-262">True</span></span>                            |
| <span data-ttu-id="e9e76-263">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="e9e76-263">Is-Single-Valued</span></span>       | <span data-ttu-id="e9e76-264">Vero</span><span class="sxs-lookup"><span data-stu-id="e9e76-264">True</span></span>                            |
| <span data-ttu-id="e9e76-265">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="e9e76-265">Is Indexed</span></span>             | <span data-ttu-id="e9e76-266">Vero</span><span class="sxs-lookup"><span data-stu-id="e9e76-266">True</span></span>                            |
| <span data-ttu-id="e9e76-267">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="e9e76-267">In Global Catalog</span></span>      | <span data-ttu-id="e9e76-268">Vero</span><span class="sxs-lookup"><span data-stu-id="e9e76-268">True</span></span>                            |
| <span data-ttu-id="e9e76-269">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="e9e76-269">NT-Security-Descriptor</span></span> | <span data-ttu-id="e9e76-270">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="e9e76-270">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="e9e76-271">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e9e76-271">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="e9e76-272">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e9e76-272">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="e9e76-273">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e9e76-273">Search-Flags</span></span>           | <span data-ttu-id="e9e76-274">0x00000009</span><span class="sxs-lookup"><span data-stu-id="e9e76-274">0x00000009</span></span>                      |
| <span data-ttu-id="e9e76-275">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e9e76-275">System-Flags</span></span>           | <span data-ttu-id="e9e76-276">0x00000013</span><span class="sxs-lookup"><span data-stu-id="e9e76-276">0x00000013</span></span>                      |
| <span data-ttu-id="e9e76-277">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="e9e76-277">Classes used in</span></span>        | [<span data-ttu-id="e9e76-278">**In alto**</span><span class="sxs-lookup"><span data-stu-id="e9e76-278">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e9e76-279">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e9e76-279">Windows Server 2012</span></span>



| <span data-ttu-id="e9e76-280">Voce</span><span class="sxs-lookup"><span data-stu-id="e9e76-280">Entry</span></span> | <span data-ttu-id="e9e76-281">Valore</span><span class="sxs-lookup"><span data-stu-id="e9e76-281">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="e9e76-282">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="e9e76-282">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="e9e76-283">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e9e76-283">MAPI-Id</span></span>                | <span data-ttu-id="e9e76-284">0x8029</span><span class="sxs-lookup"><span data-stu-id="e9e76-284">0x8029</span></span>                          |
| <span data-ttu-id="e9e76-285">System-Only</span><span class="sxs-lookup"><span data-stu-id="e9e76-285">System-Only</span></span>            | <span data-ttu-id="e9e76-286">Vero</span><span class="sxs-lookup"><span data-stu-id="e9e76-286">True</span></span>                            |
| <span data-ttu-id="e9e76-287">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="e9e76-287">Is-Single-Valued</span></span>       | <span data-ttu-id="e9e76-288">Vero</span><span class="sxs-lookup"><span data-stu-id="e9e76-288">True</span></span>                            |
| <span data-ttu-id="e9e76-289">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="e9e76-289">Is Indexed</span></span>             | <span data-ttu-id="e9e76-290">Vero</span><span class="sxs-lookup"><span data-stu-id="e9e76-290">True</span></span>                            |
| <span data-ttu-id="e9e76-291">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="e9e76-291">In Global Catalog</span></span>      | <span data-ttu-id="e9e76-292">Vero</span><span class="sxs-lookup"><span data-stu-id="e9e76-292">True</span></span>                            |
| <span data-ttu-id="e9e76-293">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="e9e76-293">NT-Security-Descriptor</span></span> | <span data-ttu-id="e9e76-294">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="e9e76-294">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="e9e76-295">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e9e76-295">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="e9e76-296">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e9e76-296">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="e9e76-297">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e9e76-297">Search-Flags</span></span>           | <span data-ttu-id="e9e76-298">0x00000009</span><span class="sxs-lookup"><span data-stu-id="e9e76-298">0x00000009</span></span>                      |
| <span data-ttu-id="e9e76-299">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e9e76-299">System-Flags</span></span>           | <span data-ttu-id="e9e76-300">0x00000013</span><span class="sxs-lookup"><span data-stu-id="e9e76-300">0x00000013</span></span>                      |
| <span data-ttu-id="e9e76-301">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="e9e76-301">Classes used in</span></span>        | [<span data-ttu-id="e9e76-302">**In alto**</span><span class="sxs-lookup"><span data-stu-id="e9e76-302">**Top**</span></span>](c-top.md)<br/> |



 

 





