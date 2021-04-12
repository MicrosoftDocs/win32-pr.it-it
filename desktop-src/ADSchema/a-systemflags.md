---
title: Attributo System-Flags
description: Valore intero che contiene i flag che definiscono proprietà aggiuntive della classe.
ms.assetid: ce24322c-fb01-462a-aefe-cb422851f782
ms.tgt_platform: multiple
keywords:
- Schema AD System-Flags attribute
- Schema AD dell'attributo systemFlags
topic_type:
- apiref
api_name:
- System-Flags
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d34bf4286cbdadc84bf340eea3f6cbec741c7920
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104480224"
---
# <a name="system-flags-attribute"></a><span data-ttu-id="bca38-105">Attributo System-Flags</span><span class="sxs-lookup"><span data-stu-id="bca38-105">System-Flags attribute</span></span>

<span data-ttu-id="bca38-106">Valore intero che contiene i flag che definiscono proprietà aggiuntive della classe.</span><span class="sxs-lookup"><span data-stu-id="bca38-106">An integer value that contains flags that define additional properties of the class.</span></span> <span data-ttu-id="bca38-107">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="bca38-107">See Remarks.</span></span>



| <span data-ttu-id="bca38-108">Voce</span><span class="sxs-lookup"><span data-stu-id="bca38-108">Entry</span></span> | <span data-ttu-id="bca38-109">Valore</span><span class="sxs-lookup"><span data-stu-id="bca38-109">Value</span></span> |
|-------------------|------------------------------------------------|
| <span data-ttu-id="bca38-110">CN</span><span class="sxs-lookup"><span data-stu-id="bca38-110">CN</span></span>                | <span data-ttu-id="bca38-111">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bca38-111">System-Flags</span></span>                                   |
| <span data-ttu-id="bca38-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="bca38-112">Ldap-Display-Name</span></span> | <span data-ttu-id="bca38-113">systemFlags</span><span class="sxs-lookup"><span data-stu-id="bca38-113">systemFlags</span></span>                                    |
| <span data-ttu-id="bca38-114">Dimensione</span><span class="sxs-lookup"><span data-stu-id="bca38-114">Size</span></span>              | \-                                             |
| <span data-ttu-id="bca38-115">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="bca38-115">Update Privilege</span></span>  | <span data-ttu-id="bca38-116">Questo valore viene impostato dall'amministratore dello schema.</span><span class="sxs-lookup"><span data-stu-id="bca38-116">This value is set by the schema administrator.</span></span> |
| <span data-ttu-id="bca38-117">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="bca38-117">Update Frequency</span></span>  | <span data-ttu-id="bca38-118">Ogni volta che lo stato dell'oggetto viene modificato.</span><span class="sxs-lookup"><span data-stu-id="bca38-118">Whenever the state of the object changes.</span></span>      |
| <span data-ttu-id="bca38-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="bca38-119">Attribute-Id</span></span>      | <span data-ttu-id="bca38-120">1.2.840.113556.1.4.375</span><span class="sxs-lookup"><span data-stu-id="bca38-120">1.2.840.113556.1.4.375</span></span>                         |
| <span data-ttu-id="bca38-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="bca38-121">System-Id-Guid</span></span>    | <span data-ttu-id="bca38-122">e0fa1e62-9b45-11d0-afdd-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="bca38-122">e0fa1e62-9b45-11d0-afdd-00c04fd930c9</span></span>           |
| <span data-ttu-id="bca38-123">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bca38-123">Syntax</span></span>            | [<span data-ttu-id="bca38-124">**Enumerazione**</span><span class="sxs-lookup"><span data-stu-id="bca38-124">**Enumeration**</span></span>](s-enumeration.md)           |



## <a name="implementations"></a><span data-ttu-id="bca38-125">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="bca38-125">Implementations</span></span>

-   [<span data-ttu-id="bca38-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="bca38-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="bca38-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="bca38-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="bca38-128">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="bca38-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="bca38-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="bca38-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="bca38-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="bca38-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="bca38-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="bca38-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="bca38-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="bca38-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="bca38-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="bca38-133">Windows 2000 Server</span></span>



| <span data-ttu-id="bca38-134">Voce</span><span class="sxs-lookup"><span data-stu-id="bca38-134">Entry</span></span> | <span data-ttu-id="bca38-135">Valore</span><span class="sxs-lookup"><span data-stu-id="bca38-135">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="bca38-136">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="bca38-136">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="bca38-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bca38-137">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="bca38-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="bca38-138">System-Only</span></span>            | <span data-ttu-id="bca38-139">Vero</span><span class="sxs-lookup"><span data-stu-id="bca38-139">True</span></span>                            |
| <span data-ttu-id="bca38-140">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="bca38-140">Is-Single-Valued</span></span>       | <span data-ttu-id="bca38-141">Vero</span><span class="sxs-lookup"><span data-stu-id="bca38-141">True</span></span>                            |
| <span data-ttu-id="bca38-142">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="bca38-142">Is Indexed</span></span>             | <span data-ttu-id="bca38-143">Falso</span><span class="sxs-lookup"><span data-stu-id="bca38-143">False</span></span>                           |
| <span data-ttu-id="bca38-144">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="bca38-144">In Global Catalog</span></span>      | <span data-ttu-id="bca38-145">Falso</span><span class="sxs-lookup"><span data-stu-id="bca38-145">False</span></span>                           |
| <span data-ttu-id="bca38-146">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="bca38-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="bca38-147">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="bca38-147">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="bca38-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bca38-148">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="bca38-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bca38-149">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="bca38-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bca38-150">Search-Flags</span></span>           | <span data-ttu-id="bca38-151">0x00000008</span><span class="sxs-lookup"><span data-stu-id="bca38-151">0x00000008</span></span>                      |
| <span data-ttu-id="bca38-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bca38-152">System-Flags</span></span>           | <span data-ttu-id="bca38-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bca38-153">0x00000010</span></span>                      |
| <span data-ttu-id="bca38-154">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="bca38-154">Classes used in</span></span>        | [<span data-ttu-id="bca38-155">**In alto**</span><span class="sxs-lookup"><span data-stu-id="bca38-155">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="bca38-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="bca38-156">Windows Server 2003</span></span>



| <span data-ttu-id="bca38-157">Voce</span><span class="sxs-lookup"><span data-stu-id="bca38-157">Entry</span></span> | <span data-ttu-id="bca38-158">Valore</span><span class="sxs-lookup"><span data-stu-id="bca38-158">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="bca38-159">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="bca38-159">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="bca38-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bca38-160">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="bca38-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="bca38-161">System-Only</span></span>            | <span data-ttu-id="bca38-162">Vero</span><span class="sxs-lookup"><span data-stu-id="bca38-162">True</span></span>                            |
| <span data-ttu-id="bca38-163">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="bca38-163">Is-Single-Valued</span></span>       | <span data-ttu-id="bca38-164">Vero</span><span class="sxs-lookup"><span data-stu-id="bca38-164">True</span></span>                            |
| <span data-ttu-id="bca38-165">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="bca38-165">Is Indexed</span></span>             | <span data-ttu-id="bca38-166">Falso</span><span class="sxs-lookup"><span data-stu-id="bca38-166">False</span></span>                           |
| <span data-ttu-id="bca38-167">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="bca38-167">In Global Catalog</span></span>      | <span data-ttu-id="bca38-168">Falso</span><span class="sxs-lookup"><span data-stu-id="bca38-168">False</span></span>                           |
| <span data-ttu-id="bca38-169">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="bca38-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="bca38-170">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="bca38-170">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="bca38-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bca38-171">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="bca38-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bca38-172">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="bca38-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bca38-173">Search-Flags</span></span>           | <span data-ttu-id="bca38-174">0x00000008</span><span class="sxs-lookup"><span data-stu-id="bca38-174">0x00000008</span></span>                      |
| <span data-ttu-id="bca38-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bca38-175">System-Flags</span></span>           | <span data-ttu-id="bca38-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bca38-176">0x00000010</span></span>                      |
| <span data-ttu-id="bca38-177">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="bca38-177">Classes used in</span></span>        | [<span data-ttu-id="bca38-178">**In alto**</span><span class="sxs-lookup"><span data-stu-id="bca38-178">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="bca38-179">ADAM</span><span class="sxs-lookup"><span data-stu-id="bca38-179">ADAM</span></span>



| <span data-ttu-id="bca38-180">Voce</span><span class="sxs-lookup"><span data-stu-id="bca38-180">Entry</span></span> | <span data-ttu-id="bca38-181">Valore</span><span class="sxs-lookup"><span data-stu-id="bca38-181">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="bca38-182">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="bca38-182">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="bca38-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bca38-183">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="bca38-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="bca38-184">System-Only</span></span>            | <span data-ttu-id="bca38-185">Vero</span><span class="sxs-lookup"><span data-stu-id="bca38-185">True</span></span>                            |
| <span data-ttu-id="bca38-186">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="bca38-186">Is-Single-Valued</span></span>       | <span data-ttu-id="bca38-187">Vero</span><span class="sxs-lookup"><span data-stu-id="bca38-187">True</span></span>                            |
| <span data-ttu-id="bca38-188">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="bca38-188">Is Indexed</span></span>             | <span data-ttu-id="bca38-189">Falso</span><span class="sxs-lookup"><span data-stu-id="bca38-189">False</span></span>                           |
| <span data-ttu-id="bca38-190">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="bca38-190">In Global Catalog</span></span>      | <span data-ttu-id="bca38-191">Falso</span><span class="sxs-lookup"><span data-stu-id="bca38-191">False</span></span>                           |
| <span data-ttu-id="bca38-192">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="bca38-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="bca38-193">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="bca38-193">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="bca38-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bca38-194">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="bca38-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bca38-195">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="bca38-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bca38-196">Search-Flags</span></span>           | <span data-ttu-id="bca38-197">0x00000008</span><span class="sxs-lookup"><span data-stu-id="bca38-197">0x00000008</span></span>                      |
| <span data-ttu-id="bca38-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bca38-198">System-Flags</span></span>           | <span data-ttu-id="bca38-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bca38-199">0x00000010</span></span>                      |
| <span data-ttu-id="bca38-200">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="bca38-200">Classes used in</span></span>        | [<span data-ttu-id="bca38-201">**In alto**</span><span class="sxs-lookup"><span data-stu-id="bca38-201">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="bca38-202">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="bca38-202">Windows Server 2003 R2</span></span>



| <span data-ttu-id="bca38-203">Voce</span><span class="sxs-lookup"><span data-stu-id="bca38-203">Entry</span></span> | <span data-ttu-id="bca38-204">Valore</span><span class="sxs-lookup"><span data-stu-id="bca38-204">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="bca38-205">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="bca38-205">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="bca38-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bca38-206">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="bca38-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="bca38-207">System-Only</span></span>            | <span data-ttu-id="bca38-208">Vero</span><span class="sxs-lookup"><span data-stu-id="bca38-208">True</span></span>                            |
| <span data-ttu-id="bca38-209">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="bca38-209">Is-Single-Valued</span></span>       | <span data-ttu-id="bca38-210">Vero</span><span class="sxs-lookup"><span data-stu-id="bca38-210">True</span></span>                            |
| <span data-ttu-id="bca38-211">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="bca38-211">Is Indexed</span></span>             | <span data-ttu-id="bca38-212">Falso</span><span class="sxs-lookup"><span data-stu-id="bca38-212">False</span></span>                           |
| <span data-ttu-id="bca38-213">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="bca38-213">In Global Catalog</span></span>      | <span data-ttu-id="bca38-214">Falso</span><span class="sxs-lookup"><span data-stu-id="bca38-214">False</span></span>                           |
| <span data-ttu-id="bca38-215">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="bca38-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="bca38-216">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="bca38-216">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="bca38-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bca38-217">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="bca38-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bca38-218">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="bca38-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bca38-219">Search-Flags</span></span>           | <span data-ttu-id="bca38-220">0x00000008</span><span class="sxs-lookup"><span data-stu-id="bca38-220">0x00000008</span></span>                      |
| <span data-ttu-id="bca38-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bca38-221">System-Flags</span></span>           | <span data-ttu-id="bca38-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bca38-222">0x00000010</span></span>                      |
| <span data-ttu-id="bca38-223">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="bca38-223">Classes used in</span></span>        | [<span data-ttu-id="bca38-224">**In alto**</span><span class="sxs-lookup"><span data-stu-id="bca38-224">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="bca38-225">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bca38-225">Windows Server 2008</span></span>



| <span data-ttu-id="bca38-226">Voce</span><span class="sxs-lookup"><span data-stu-id="bca38-226">Entry</span></span> | <span data-ttu-id="bca38-227">Valore</span><span class="sxs-lookup"><span data-stu-id="bca38-227">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="bca38-228">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="bca38-228">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="bca38-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bca38-229">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="bca38-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="bca38-230">System-Only</span></span>            | <span data-ttu-id="bca38-231">Vero</span><span class="sxs-lookup"><span data-stu-id="bca38-231">True</span></span>                            |
| <span data-ttu-id="bca38-232">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="bca38-232">Is-Single-Valued</span></span>       | <span data-ttu-id="bca38-233">Vero</span><span class="sxs-lookup"><span data-stu-id="bca38-233">True</span></span>                            |
| <span data-ttu-id="bca38-234">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="bca38-234">Is Indexed</span></span>             | <span data-ttu-id="bca38-235">Falso</span><span class="sxs-lookup"><span data-stu-id="bca38-235">False</span></span>                           |
| <span data-ttu-id="bca38-236">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="bca38-236">In Global Catalog</span></span>      | <span data-ttu-id="bca38-237">Falso</span><span class="sxs-lookup"><span data-stu-id="bca38-237">False</span></span>                           |
| <span data-ttu-id="bca38-238">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="bca38-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="bca38-239">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="bca38-239">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="bca38-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bca38-240">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="bca38-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bca38-241">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="bca38-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bca38-242">Search-Flags</span></span>           | <span data-ttu-id="bca38-243">0x00000008</span><span class="sxs-lookup"><span data-stu-id="bca38-243">0x00000008</span></span>                      |
| <span data-ttu-id="bca38-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bca38-244">System-Flags</span></span>           | <span data-ttu-id="bca38-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bca38-245">0x00000010</span></span>                      |
| <span data-ttu-id="bca38-246">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="bca38-246">Classes used in</span></span>        | [<span data-ttu-id="bca38-247">**In alto**</span><span class="sxs-lookup"><span data-stu-id="bca38-247">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="bca38-248">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="bca38-248">Windows Server 2008 R2</span></span>



| <span data-ttu-id="bca38-249">Voce</span><span class="sxs-lookup"><span data-stu-id="bca38-249">Entry</span></span> | <span data-ttu-id="bca38-250">Valore</span><span class="sxs-lookup"><span data-stu-id="bca38-250">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="bca38-251">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="bca38-251">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="bca38-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bca38-252">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="bca38-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="bca38-253">System-Only</span></span>            | <span data-ttu-id="bca38-254">Vero</span><span class="sxs-lookup"><span data-stu-id="bca38-254">True</span></span>                            |
| <span data-ttu-id="bca38-255">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="bca38-255">Is-Single-Valued</span></span>       | <span data-ttu-id="bca38-256">Vero</span><span class="sxs-lookup"><span data-stu-id="bca38-256">True</span></span>                            |
| <span data-ttu-id="bca38-257">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="bca38-257">Is Indexed</span></span>             | <span data-ttu-id="bca38-258">Falso</span><span class="sxs-lookup"><span data-stu-id="bca38-258">False</span></span>                           |
| <span data-ttu-id="bca38-259">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="bca38-259">In Global Catalog</span></span>      | <span data-ttu-id="bca38-260">Falso</span><span class="sxs-lookup"><span data-stu-id="bca38-260">False</span></span>                           |
| <span data-ttu-id="bca38-261">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="bca38-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="bca38-262">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="bca38-262">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="bca38-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bca38-263">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="bca38-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bca38-264">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="bca38-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bca38-265">Search-Flags</span></span>           | <span data-ttu-id="bca38-266">0x00000008</span><span class="sxs-lookup"><span data-stu-id="bca38-266">0x00000008</span></span>                      |
| <span data-ttu-id="bca38-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bca38-267">System-Flags</span></span>           | <span data-ttu-id="bca38-268">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bca38-268">0x00000010</span></span>                      |
| <span data-ttu-id="bca38-269">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="bca38-269">Classes used in</span></span>        | [<span data-ttu-id="bca38-270">**In alto**</span><span class="sxs-lookup"><span data-stu-id="bca38-270">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="bca38-271">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="bca38-271">Windows Server 2012</span></span>



| <span data-ttu-id="bca38-272">Voce</span><span class="sxs-lookup"><span data-stu-id="bca38-272">Entry</span></span> | <span data-ttu-id="bca38-273">Valore</span><span class="sxs-lookup"><span data-stu-id="bca38-273">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="bca38-274">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="bca38-274">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="bca38-275">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bca38-275">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="bca38-276">System-Only</span><span class="sxs-lookup"><span data-stu-id="bca38-276">System-Only</span></span>            | <span data-ttu-id="bca38-277">Vero</span><span class="sxs-lookup"><span data-stu-id="bca38-277">True</span></span>                            |
| <span data-ttu-id="bca38-278">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="bca38-278">Is-Single-Valued</span></span>       | <span data-ttu-id="bca38-279">Vero</span><span class="sxs-lookup"><span data-stu-id="bca38-279">True</span></span>                            |
| <span data-ttu-id="bca38-280">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="bca38-280">Is Indexed</span></span>             | <span data-ttu-id="bca38-281">Falso</span><span class="sxs-lookup"><span data-stu-id="bca38-281">False</span></span>                           |
| <span data-ttu-id="bca38-282">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="bca38-282">In Global Catalog</span></span>      | <span data-ttu-id="bca38-283">Falso</span><span class="sxs-lookup"><span data-stu-id="bca38-283">False</span></span>                           |
| <span data-ttu-id="bca38-284">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="bca38-284">NT-Security-Descriptor</span></span> | <span data-ttu-id="bca38-285">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="bca38-285">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="bca38-286">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bca38-286">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="bca38-287">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bca38-287">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="bca38-288">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bca38-288">Search-Flags</span></span>           | <span data-ttu-id="bca38-289">0x00000008</span><span class="sxs-lookup"><span data-stu-id="bca38-289">0x00000008</span></span>                      |
| <span data-ttu-id="bca38-290">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bca38-290">System-Flags</span></span>           | <span data-ttu-id="bca38-291">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bca38-291">0x00000010</span></span>                      |
| <span data-ttu-id="bca38-292">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="bca38-292">Classes used in</span></span>        | [<span data-ttu-id="bca38-293">**In alto**</span><span class="sxs-lookup"><span data-stu-id="bca38-293">**Top**</span></span>](c-top.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="bca38-294">Commenti</span><span class="sxs-lookup"><span data-stu-id="bca38-294">Remarks</span></span>

<span data-ttu-id="bca38-295">Questo attributo può essere zero o una combinazione di uno o più dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="bca38-295">This attribute can be zero or a combination of one or more of the following values.</span></span>



| <span data-ttu-id="bca38-296">Valore</span><span class="sxs-lookup"><span data-stu-id="bca38-296">Value</span></span>                   | <span data-ttu-id="bca38-297">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bca38-297">Description</span></span>                                                                                                                                                                                                                                                                                     |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bca38-298">1 (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="bca38-298">1 (0x00000001)</span></span>          | <span data-ttu-id="bca38-299">Quando viene applicato a un attributo, l'attributo non verrà replicato. Quando viene applicato a un oggetto di [**riferimento incrociato**](c-crossref.md) , il contesto dei nomi è in NTDS.</span><span class="sxs-lookup"><span data-stu-id="bca38-299">When applied to an attribute, the attribute will not be replicated.When applied to a [**Cross-Ref**](c-crossref.md) object, the naming context is in NTDS.</span></span><br/>                                                                                                                          |
| <span data-ttu-id="bca38-300">2 (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="bca38-300">2 (0x00000002)</span></span>          | <span data-ttu-id="bca38-301">Quando viene applicato a un attributo, l'attributo verrà replicato nel catalogo globale. Quando viene applicato a un oggetto di [**riferimento incrociato**](c-crossref.md) , il contesto dei nomi è un dominio.</span><span class="sxs-lookup"><span data-stu-id="bca38-301">When applied to an attribute, the attribute will be replicated to the global catalog.When applied to a [**Cross-Ref**](c-crossref.md) object, the naming context is a domain.</span></span><br/>                                                                                                       |
| <span data-ttu-id="bca38-302">4 (0x00000004)</span><span class="sxs-lookup"><span data-stu-id="bca38-302">4 (0x00000004)</span></span>          | <span data-ttu-id="bca38-303">Quando viene applicato a un attributo, l'attributo viene costruito.</span><span class="sxs-lookup"><span data-stu-id="bca38-303">When applied to an attribute, the attribute is constructed.</span></span>                                                                                                                                                                                                                                     |
| <span data-ttu-id="bca38-304">16 (0x00000010)</span><span class="sxs-lookup"><span data-stu-id="bca38-304">16 (0x00000010)</span></span>         | <span data-ttu-id="bca38-305">Quando impostato, indica che l'oggetto è un oggetto di categoria 1.</span><span class="sxs-lookup"><span data-stu-id="bca38-305">When set, indicates the object is a category 1 object.</span></span> <span data-ttu-id="bca38-306">Un oggetto di categoria 1 è una classe o un attributo incluso nello schema di base incluso nel sistema.</span><span class="sxs-lookup"><span data-stu-id="bca38-306">A category 1 object is a class or attribute that is included in the base schema included with the system.</span></span>                                                                                                                                |
| <span data-ttu-id="bca38-307">33554432 (0x02000000)</span><span class="sxs-lookup"><span data-stu-id="bca38-307">33554432 (0x02000000)</span></span>   | <span data-ttu-id="bca38-308">L'oggetto non viene spostato nel contenitore degli oggetti eliminati quando viene eliminato.</span><span class="sxs-lookup"><span data-stu-id="bca38-308">The object is not moved to the Deleted Objects container when it is deleted.</span></span> <span data-ttu-id="bca38-309">Verrà eliminato immediatamente.</span><span class="sxs-lookup"><span data-stu-id="bca38-309">It will be deleted immediately.</span></span>                                                                                                                                                                                    |
| <span data-ttu-id="bca38-310">67108864 (0x04000000)</span><span class="sxs-lookup"><span data-stu-id="bca38-310">67108864 (0x04000000)</span></span>   | <span data-ttu-id="bca38-311">Impossibile spostare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="bca38-311">The object cannot be moved.</span></span>                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="bca38-312">134217728 (0x08000000)</span><span class="sxs-lookup"><span data-stu-id="bca38-312">134217728 (0x08000000)</span></span>  | <span data-ttu-id="bca38-313">Impossibile rinominare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="bca38-313">The object cannot be renamed.</span></span>                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="bca38-314">268435456 (0x10000000)</span><span class="sxs-lookup"><span data-stu-id="bca38-314">268435456 (0x10000000)</span></span>  | <span data-ttu-id="bca38-315">Per gli oggetti nella partizione di configurazione, se questo flag è impostato, è possibile spostare l'oggetto con restrizioni. in caso contrario, l'oggetto non può essere spostato.</span><span class="sxs-lookup"><span data-stu-id="bca38-315">For objects in the configuration partition, if this flag is set, the object can be moved with restrictions; otherwise, the object cannot be moved.</span></span> <span data-ttu-id="bca38-316">Per impostazione predefinita, questo flag non è impostato per i nuovi oggetti creati nella partizione di configurazione.</span><span class="sxs-lookup"><span data-stu-id="bca38-316">By default, this flag is not set on new objects created under the configuration partition.</span></span> <span data-ttu-id="bca38-317">Questo flag può essere impostato solo durante la creazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="bca38-317">This flag can only be set during object creation.</span></span> |
| <span data-ttu-id="bca38-318">536870912 (0x20000000)</span><span class="sxs-lookup"><span data-stu-id="bca38-318">536870912 (0x20000000)</span></span>  | <span data-ttu-id="bca38-319">Per gli oggetti nella partizione di configurazione, se questo flag è impostato, è possibile spostare l'oggetto; in caso contrario, l'oggetto non può essere spostato.</span><span class="sxs-lookup"><span data-stu-id="bca38-319">For objects in the configuration partition, if this flag is set, the object can be moved; otherwise, the object cannot be moved.</span></span> <span data-ttu-id="bca38-320">Per impostazione predefinita, questo flag non è impostato per i nuovi oggetti creati nella partizione di configurazione.</span><span class="sxs-lookup"><span data-stu-id="bca38-320">By default, this flag is not set on new objects created under the configuration partition.</span></span> <span data-ttu-id="bca38-321">Questo flag può essere impostato solo durante la creazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="bca38-321">This flag can only be set during object creation.</span></span>                   |
| <span data-ttu-id="bca38-322">1073741824 (0x40000000)</span><span class="sxs-lookup"><span data-stu-id="bca38-322">1073741824 (0x40000000)</span></span> | <span data-ttu-id="bca38-323">Per gli oggetti nella partizione di configurazione, se questo flag è impostato, l'oggetto può essere rinominato. in caso contrario, l'oggetto non può essere rinominato.</span><span class="sxs-lookup"><span data-stu-id="bca38-323">For objects in the configuration partition, if this flag is set, the object can be renamed; otherwise, the object cannot be renamed.</span></span> <span data-ttu-id="bca38-324">Per impostazione predefinita, questo flag non è impostato per i nuovi oggetti creati nella partizione di configurazione.</span><span class="sxs-lookup"><span data-stu-id="bca38-324">By default, this flag is not set on new objects created under the configuration partition.</span></span> <span data-ttu-id="bca38-325">Questo flag può essere impostato solo durante la creazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="bca38-325">This flag can only be set during object creation.</span></span>               |
| <span data-ttu-id="bca38-326">2147483648 (0x80000000)</span><span class="sxs-lookup"><span data-stu-id="bca38-326">2147483648 (0x80000000)</span></span> | <span data-ttu-id="bca38-327">Non è possibile eliminare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="bca38-327">The object cannot be deleted.</span></span>                                                                                                                                                                                                                                                                   |



 

 

 





