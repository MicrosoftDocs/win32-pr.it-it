---
title: Attributo Mastered-By
description: Collegamento all'indietro per l'attributo has-Master-NCs. Nome distinto per i relativi oggetti Impostazioni NTDS.
ms.assetid: bd14998c-1691-4167-83c4-3c1ec1181b7f
ms.tgt_platform: multiple
keywords:
- Schema AD Mastered-By attribute
- Schema AD dell'attributo masteredBy
topic_type:
- apiref
api_name:
- Mastered-By
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85cf02f78363e1e8db06bddfb2c389cc78077090
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104122134"
---
# <a name="mastered-by-attribute"></a><span data-ttu-id="9d584-106">Attributo Mastered-By</span><span class="sxs-lookup"><span data-stu-id="9d584-106">Mastered-By attribute</span></span>

<span data-ttu-id="9d584-107">Collegamento all'indietro per l'attributo has-Master-NCs.</span><span class="sxs-lookup"><span data-stu-id="9d584-107">Backward link for Has-Master-NCs attribute.</span></span> <span data-ttu-id="9d584-108">Nome distinto per i relativi oggetti Impostazioni NTDS.</span><span class="sxs-lookup"><span data-stu-id="9d584-108">The distinguished name for its NTDS Settings objects.</span></span>



| <span data-ttu-id="9d584-109">Voce</span><span class="sxs-lookup"><span data-stu-id="9d584-109">Entry</span></span> | <span data-ttu-id="9d584-110">Valore</span><span class="sxs-lookup"><span data-stu-id="9d584-110">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="9d584-111">CN</span><span class="sxs-lookup"><span data-stu-id="9d584-111">CN</span></span>                | <span data-ttu-id="9d584-112">Mastered-By</span><span class="sxs-lookup"><span data-stu-id="9d584-112">Mastered-By</span></span>                             |
| <span data-ttu-id="9d584-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="9d584-113">Ldap-Display-Name</span></span> | <span data-ttu-id="9d584-114">masteredBy</span><span class="sxs-lookup"><span data-stu-id="9d584-114">masteredBy</span></span>                              |
| <span data-ttu-id="9d584-115">Dimensione</span><span class="sxs-lookup"><span data-stu-id="9d584-115">Size</span></span>              | \-                                      |
| <span data-ttu-id="9d584-116">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="9d584-116">Update Privilege</span></span>  | <span data-ttu-id="9d584-117">Questo valore viene impostato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="9d584-117">This value is set by the system.</span></span>        |
| <span data-ttu-id="9d584-118">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="9d584-118">Update Frequency</span></span>  | <span data-ttu-id="9d584-119">Quando viene creato il contesto dei nomi.</span><span class="sxs-lookup"><span data-stu-id="9d584-119">When the Naming Context is created.</span></span>     |
| <span data-ttu-id="9d584-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="9d584-120">Attribute-Id</span></span>      | <span data-ttu-id="9d584-121">1.2.840.113556.1.4.1409</span><span class="sxs-lookup"><span data-stu-id="9d584-121">1.2.840.113556.1.4.1409</span></span>                 |
| <span data-ttu-id="9d584-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="9d584-122">System-Id-Guid</span></span>    | <span data-ttu-id="9d584-123">e48e64e0-12c9-11d3-9102-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="9d584-123">e48e64e0-12c9-11d3-9102-00c04fd91ab1</span></span>    |
| <span data-ttu-id="9d584-124">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9d584-124">Syntax</span></span>            | [<span data-ttu-id="9d584-125">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="9d584-125">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="9d584-126">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="9d584-126">Implementations</span></span>

-   [<span data-ttu-id="9d584-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="9d584-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="9d584-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="9d584-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="9d584-129">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="9d584-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="9d584-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="9d584-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="9d584-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="9d584-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="9d584-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="9d584-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="9d584-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="9d584-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="9d584-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9d584-134">Windows 2000 Server</span></span>



| <span data-ttu-id="9d584-135">Voce</span><span class="sxs-lookup"><span data-stu-id="9d584-135">Entry</span></span> | <span data-ttu-id="9d584-136">Valore</span><span class="sxs-lookup"><span data-stu-id="9d584-136">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="9d584-137">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="9d584-137">Link-Id</span></span>                | <span data-ttu-id="9d584-138">77</span><span class="sxs-lookup"><span data-stu-id="9d584-138">77</span></span>                              |
| <span data-ttu-id="9d584-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9d584-139">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="9d584-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="9d584-140">System-Only</span></span>            | <span data-ttu-id="9d584-141">Vero</span><span class="sxs-lookup"><span data-stu-id="9d584-141">True</span></span>                            |
| <span data-ttu-id="9d584-142">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="9d584-142">Is-Single-Valued</span></span>       | <span data-ttu-id="9d584-143">Falso</span><span class="sxs-lookup"><span data-stu-id="9d584-143">False</span></span>                           |
| <span data-ttu-id="9d584-144">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="9d584-144">Is Indexed</span></span>             | <span data-ttu-id="9d584-145">Falso</span><span class="sxs-lookup"><span data-stu-id="9d584-145">False</span></span>                           |
| <span data-ttu-id="9d584-146">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="9d584-146">In Global Catalog</span></span>      | <span data-ttu-id="9d584-147">Falso</span><span class="sxs-lookup"><span data-stu-id="9d584-147">False</span></span>                           |
| <span data-ttu-id="9d584-148">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="9d584-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="9d584-149">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="9d584-149">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="9d584-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9d584-150">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="9d584-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9d584-151">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="9d584-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9d584-152">Search-Flags</span></span>           | <span data-ttu-id="9d584-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9d584-153">0x00000000</span></span>                      |
| <span data-ttu-id="9d584-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9d584-154">System-Flags</span></span>           | <span data-ttu-id="9d584-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9d584-155">0x00000010</span></span>                      |
| <span data-ttu-id="9d584-156">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="9d584-156">Classes used in</span></span>        | [<span data-ttu-id="9d584-157">**In alto**</span><span class="sxs-lookup"><span data-stu-id="9d584-157">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="9d584-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9d584-158">Windows Server 2003</span></span>



| <span data-ttu-id="9d584-159">Voce</span><span class="sxs-lookup"><span data-stu-id="9d584-159">Entry</span></span> | <span data-ttu-id="9d584-160">Valore</span><span class="sxs-lookup"><span data-stu-id="9d584-160">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="9d584-161">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="9d584-161">Link-Id</span></span>                | <span data-ttu-id="9d584-162">77</span><span class="sxs-lookup"><span data-stu-id="9d584-162">77</span></span>                              |
| <span data-ttu-id="9d584-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9d584-163">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="9d584-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="9d584-164">System-Only</span></span>            | <span data-ttu-id="9d584-165">Vero</span><span class="sxs-lookup"><span data-stu-id="9d584-165">True</span></span>                            |
| <span data-ttu-id="9d584-166">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="9d584-166">Is-Single-Valued</span></span>       | <span data-ttu-id="9d584-167">Falso</span><span class="sxs-lookup"><span data-stu-id="9d584-167">False</span></span>                           |
| <span data-ttu-id="9d584-168">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="9d584-168">Is Indexed</span></span>             | <span data-ttu-id="9d584-169">Falso</span><span class="sxs-lookup"><span data-stu-id="9d584-169">False</span></span>                           |
| <span data-ttu-id="9d584-170">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="9d584-170">In Global Catalog</span></span>      | <span data-ttu-id="9d584-171">Falso</span><span class="sxs-lookup"><span data-stu-id="9d584-171">False</span></span>                           |
| <span data-ttu-id="9d584-172">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="9d584-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="9d584-173">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="9d584-173">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="9d584-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9d584-174">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="9d584-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9d584-175">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="9d584-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9d584-176">Search-Flags</span></span>           | <span data-ttu-id="9d584-177">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9d584-177">0x00000000</span></span>                      |
| <span data-ttu-id="9d584-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9d584-178">System-Flags</span></span>           | <span data-ttu-id="9d584-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9d584-179">0x00000010</span></span>                      |
| <span data-ttu-id="9d584-180">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="9d584-180">Classes used in</span></span>        | [<span data-ttu-id="9d584-181">**In alto**</span><span class="sxs-lookup"><span data-stu-id="9d584-181">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="9d584-182">ADAM</span><span class="sxs-lookup"><span data-stu-id="9d584-182">ADAM</span></span>



| <span data-ttu-id="9d584-183">Voce</span><span class="sxs-lookup"><span data-stu-id="9d584-183">Entry</span></span> | <span data-ttu-id="9d584-184">Valore</span><span class="sxs-lookup"><span data-stu-id="9d584-184">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="9d584-185">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="9d584-185">Link-Id</span></span>                | <span data-ttu-id="9d584-186">77</span><span class="sxs-lookup"><span data-stu-id="9d584-186">77</span></span>                              |
| <span data-ttu-id="9d584-187">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9d584-187">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="9d584-188">System-Only</span><span class="sxs-lookup"><span data-stu-id="9d584-188">System-Only</span></span>            | <span data-ttu-id="9d584-189">Vero</span><span class="sxs-lookup"><span data-stu-id="9d584-189">True</span></span>                            |
| <span data-ttu-id="9d584-190">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="9d584-190">Is-Single-Valued</span></span>       | <span data-ttu-id="9d584-191">Falso</span><span class="sxs-lookup"><span data-stu-id="9d584-191">False</span></span>                           |
| <span data-ttu-id="9d584-192">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="9d584-192">Is Indexed</span></span>             | <span data-ttu-id="9d584-193">Falso</span><span class="sxs-lookup"><span data-stu-id="9d584-193">False</span></span>                           |
| <span data-ttu-id="9d584-194">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="9d584-194">In Global Catalog</span></span>      | <span data-ttu-id="9d584-195">Falso</span><span class="sxs-lookup"><span data-stu-id="9d584-195">False</span></span>                           |
| <span data-ttu-id="9d584-196">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="9d584-196">NT-Security-Descriptor</span></span> | <span data-ttu-id="9d584-197">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="9d584-197">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="9d584-198">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9d584-198">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="9d584-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9d584-199">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="9d584-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9d584-200">Search-Flags</span></span>           | <span data-ttu-id="9d584-201">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9d584-201">0x00000000</span></span>                      |
| <span data-ttu-id="9d584-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9d584-202">System-Flags</span></span>           | <span data-ttu-id="9d584-203">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9d584-203">0x00000010</span></span>                      |
| <span data-ttu-id="9d584-204">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="9d584-204">Classes used in</span></span>        | [<span data-ttu-id="9d584-205">**In alto**</span><span class="sxs-lookup"><span data-stu-id="9d584-205">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="9d584-206">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="9d584-206">Windows Server 2003 R2</span></span>



| <span data-ttu-id="9d584-207">Voce</span><span class="sxs-lookup"><span data-stu-id="9d584-207">Entry</span></span> | <span data-ttu-id="9d584-208">Valore</span><span class="sxs-lookup"><span data-stu-id="9d584-208">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="9d584-209">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="9d584-209">Link-Id</span></span>                | <span data-ttu-id="9d584-210">77</span><span class="sxs-lookup"><span data-stu-id="9d584-210">77</span></span>                              |
| <span data-ttu-id="9d584-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9d584-211">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="9d584-212">System-Only</span><span class="sxs-lookup"><span data-stu-id="9d584-212">System-Only</span></span>            | <span data-ttu-id="9d584-213">Vero</span><span class="sxs-lookup"><span data-stu-id="9d584-213">True</span></span>                            |
| <span data-ttu-id="9d584-214">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="9d584-214">Is-Single-Valued</span></span>       | <span data-ttu-id="9d584-215">Falso</span><span class="sxs-lookup"><span data-stu-id="9d584-215">False</span></span>                           |
| <span data-ttu-id="9d584-216">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="9d584-216">Is Indexed</span></span>             | <span data-ttu-id="9d584-217">Falso</span><span class="sxs-lookup"><span data-stu-id="9d584-217">False</span></span>                           |
| <span data-ttu-id="9d584-218">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="9d584-218">In Global Catalog</span></span>      | <span data-ttu-id="9d584-219">Falso</span><span class="sxs-lookup"><span data-stu-id="9d584-219">False</span></span>                           |
| <span data-ttu-id="9d584-220">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="9d584-220">NT-Security-Descriptor</span></span> | <span data-ttu-id="9d584-221">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="9d584-221">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="9d584-222">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9d584-222">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="9d584-223">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9d584-223">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="9d584-224">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9d584-224">Search-Flags</span></span>           | <span data-ttu-id="9d584-225">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9d584-225">0x00000000</span></span>                      |
| <span data-ttu-id="9d584-226">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9d584-226">System-Flags</span></span>           | <span data-ttu-id="9d584-227">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9d584-227">0x00000010</span></span>                      |
| <span data-ttu-id="9d584-228">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="9d584-228">Classes used in</span></span>        | [<span data-ttu-id="9d584-229">**In alto**</span><span class="sxs-lookup"><span data-stu-id="9d584-229">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="9d584-230">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9d584-230">Windows Server 2008</span></span>



| <span data-ttu-id="9d584-231">Voce</span><span class="sxs-lookup"><span data-stu-id="9d584-231">Entry</span></span> | <span data-ttu-id="9d584-232">Valore</span><span class="sxs-lookup"><span data-stu-id="9d584-232">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="9d584-233">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="9d584-233">Link-Id</span></span>                | <span data-ttu-id="9d584-234">77</span><span class="sxs-lookup"><span data-stu-id="9d584-234">77</span></span>                              |
| <span data-ttu-id="9d584-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9d584-235">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="9d584-236">System-Only</span><span class="sxs-lookup"><span data-stu-id="9d584-236">System-Only</span></span>            | <span data-ttu-id="9d584-237">Vero</span><span class="sxs-lookup"><span data-stu-id="9d584-237">True</span></span>                            |
| <span data-ttu-id="9d584-238">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="9d584-238">Is-Single-Valued</span></span>       | <span data-ttu-id="9d584-239">Falso</span><span class="sxs-lookup"><span data-stu-id="9d584-239">False</span></span>                           |
| <span data-ttu-id="9d584-240">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="9d584-240">Is Indexed</span></span>             | <span data-ttu-id="9d584-241">Falso</span><span class="sxs-lookup"><span data-stu-id="9d584-241">False</span></span>                           |
| <span data-ttu-id="9d584-242">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="9d584-242">In Global Catalog</span></span>      | <span data-ttu-id="9d584-243">Falso</span><span class="sxs-lookup"><span data-stu-id="9d584-243">False</span></span>                           |
| <span data-ttu-id="9d584-244">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="9d584-244">NT-Security-Descriptor</span></span> | <span data-ttu-id="9d584-245">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="9d584-245">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="9d584-246">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9d584-246">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="9d584-247">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9d584-247">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="9d584-248">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9d584-248">Search-Flags</span></span>           | <span data-ttu-id="9d584-249">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9d584-249">0x00000000</span></span>                      |
| <span data-ttu-id="9d584-250">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9d584-250">System-Flags</span></span>           | <span data-ttu-id="9d584-251">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9d584-251">0x00000010</span></span>                      |
| <span data-ttu-id="9d584-252">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="9d584-252">Classes used in</span></span>        | [<span data-ttu-id="9d584-253">**In alto**</span><span class="sxs-lookup"><span data-stu-id="9d584-253">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="9d584-254">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9d584-254">Windows Server 2008 R2</span></span>



| <span data-ttu-id="9d584-255">Voce</span><span class="sxs-lookup"><span data-stu-id="9d584-255">Entry</span></span> | <span data-ttu-id="9d584-256">Valore</span><span class="sxs-lookup"><span data-stu-id="9d584-256">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="9d584-257">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="9d584-257">Link-Id</span></span>                | <span data-ttu-id="9d584-258">77</span><span class="sxs-lookup"><span data-stu-id="9d584-258">77</span></span>                              |
| <span data-ttu-id="9d584-259">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9d584-259">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="9d584-260">System-Only</span><span class="sxs-lookup"><span data-stu-id="9d584-260">System-Only</span></span>            | <span data-ttu-id="9d584-261">Vero</span><span class="sxs-lookup"><span data-stu-id="9d584-261">True</span></span>                            |
| <span data-ttu-id="9d584-262">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="9d584-262">Is-Single-Valued</span></span>       | <span data-ttu-id="9d584-263">Falso</span><span class="sxs-lookup"><span data-stu-id="9d584-263">False</span></span>                           |
| <span data-ttu-id="9d584-264">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="9d584-264">Is Indexed</span></span>             | <span data-ttu-id="9d584-265">Falso</span><span class="sxs-lookup"><span data-stu-id="9d584-265">False</span></span>                           |
| <span data-ttu-id="9d584-266">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="9d584-266">In Global Catalog</span></span>      | <span data-ttu-id="9d584-267">Falso</span><span class="sxs-lookup"><span data-stu-id="9d584-267">False</span></span>                           |
| <span data-ttu-id="9d584-268">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="9d584-268">NT-Security-Descriptor</span></span> | <span data-ttu-id="9d584-269">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="9d584-269">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="9d584-270">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9d584-270">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="9d584-271">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9d584-271">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="9d584-272">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9d584-272">Search-Flags</span></span>           | <span data-ttu-id="9d584-273">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9d584-273">0x00000000</span></span>                      |
| <span data-ttu-id="9d584-274">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9d584-274">System-Flags</span></span>           | <span data-ttu-id="9d584-275">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9d584-275">0x00000010</span></span>                      |
| <span data-ttu-id="9d584-276">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="9d584-276">Classes used in</span></span>        | [<span data-ttu-id="9d584-277">**In alto**</span><span class="sxs-lookup"><span data-stu-id="9d584-277">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="9d584-278">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9d584-278">Windows Server 2012</span></span>



| <span data-ttu-id="9d584-279">Voce</span><span class="sxs-lookup"><span data-stu-id="9d584-279">Entry</span></span> | <span data-ttu-id="9d584-280">Valore</span><span class="sxs-lookup"><span data-stu-id="9d584-280">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="9d584-281">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="9d584-281">Link-Id</span></span>                | <span data-ttu-id="9d584-282">77</span><span class="sxs-lookup"><span data-stu-id="9d584-282">77</span></span>                              |
| <span data-ttu-id="9d584-283">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9d584-283">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="9d584-284">System-Only</span><span class="sxs-lookup"><span data-stu-id="9d584-284">System-Only</span></span>            | <span data-ttu-id="9d584-285">Vero</span><span class="sxs-lookup"><span data-stu-id="9d584-285">True</span></span>                            |
| <span data-ttu-id="9d584-286">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="9d584-286">Is-Single-Valued</span></span>       | <span data-ttu-id="9d584-287">Falso</span><span class="sxs-lookup"><span data-stu-id="9d584-287">False</span></span>                           |
| <span data-ttu-id="9d584-288">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="9d584-288">Is Indexed</span></span>             | <span data-ttu-id="9d584-289">Falso</span><span class="sxs-lookup"><span data-stu-id="9d584-289">False</span></span>                           |
| <span data-ttu-id="9d584-290">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="9d584-290">In Global Catalog</span></span>      | <span data-ttu-id="9d584-291">Falso</span><span class="sxs-lookup"><span data-stu-id="9d584-291">False</span></span>                           |
| <span data-ttu-id="9d584-292">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="9d584-292">NT-Security-Descriptor</span></span> | <span data-ttu-id="9d584-293">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="9d584-293">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="9d584-294">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9d584-294">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="9d584-295">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9d584-295">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="9d584-296">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9d584-296">Search-Flags</span></span>           | <span data-ttu-id="9d584-297">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9d584-297">0x00000000</span></span>                      |
| <span data-ttu-id="9d584-298">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9d584-298">System-Flags</span></span>           | <span data-ttu-id="9d584-299">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9d584-299">0x00000010</span></span>                      |
| <span data-ttu-id="9d584-300">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="9d584-300">Classes used in</span></span>        | [<span data-ttu-id="9d584-301">**In alto**</span><span class="sxs-lookup"><span data-stu-id="9d584-301">**Top**</span></span>](c-top.md)<br/> |



 

 





