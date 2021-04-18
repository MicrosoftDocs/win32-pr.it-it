---
title: Ultimo attributo noto-padre
description: Nome distinto (DN) dell'ultimo elemento padre noto di un oggetto orfano.
ms.assetid: 6cf7be1a-8ff0-42f7-9e7a-c15cbc652ec5
ms.tgt_platform: multiple
keywords:
- Ultimo schema AD attributo padre noto
- Schema AD dell'attributo lastKnownParent
topic_type:
- apiref
api_name:
- Last-Known-Parent
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d83ae15f910d2e2f2dbc23ff39bb28cd27d56b2
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "106303322"
---
# <a name="last-known-parent-attribute"></a><span data-ttu-id="df023-105">Ultimo attributo noto-padre</span><span class="sxs-lookup"><span data-stu-id="df023-105">Last-Known-Parent attribute</span></span>

<span data-ttu-id="df023-106">Nome distinto (DN) dell'ultimo elemento padre noto di un oggetto orfano.</span><span class="sxs-lookup"><span data-stu-id="df023-106">The Distinguished Name (DN) of the last known parent of an orphaned object.</span></span>



| <span data-ttu-id="df023-107">Voce</span><span class="sxs-lookup"><span data-stu-id="df023-107">Entry</span></span> | <span data-ttu-id="df023-108">Valore</span><span class="sxs-lookup"><span data-stu-id="df023-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="df023-109">CN</span><span class="sxs-lookup"><span data-stu-id="df023-109">CN</span></span>                | <span data-ttu-id="df023-110">Ultimo elemento padre noto</span><span class="sxs-lookup"><span data-stu-id="df023-110">Last-Known-Parent</span></span>                       |
| <span data-ttu-id="df023-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="df023-111">Ldap-Display-Name</span></span> | <span data-ttu-id="df023-112">lastKnownParent</span><span class="sxs-lookup"><span data-stu-id="df023-112">lastKnownParent</span></span>                         |
| <span data-ttu-id="df023-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="df023-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="df023-114">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="df023-114">Update Privilege</span></span>  | <span data-ttu-id="df023-115">Questo valore viene impostato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="df023-115">This value is set by the system.</span></span>        |
| <span data-ttu-id="df023-116">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="df023-116">Update Frequency</span></span>  | <span data-ttu-id="df023-117">Ogni volta che un oggetto è orfano.</span><span class="sxs-lookup"><span data-stu-id="df023-117">Whenever an object is orphaned.</span></span>         |
| <span data-ttu-id="df023-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="df023-118">Attribute-Id</span></span>      | <span data-ttu-id="df023-119">1.2.840.113556.1.4.781</span><span class="sxs-lookup"><span data-stu-id="df023-119">1.2.840.113556.1.4.781</span></span>                  |
| <span data-ttu-id="df023-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="df023-120">System-Id-Guid</span></span>    | <span data-ttu-id="df023-121">52ab8670-5709-11d1-a9c6-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="df023-121">52ab8670-5709-11d1-a9c6-0000f80367c1</span></span>    |
| <span data-ttu-id="df023-122">Sintassi</span><span class="sxs-lookup"><span data-stu-id="df023-122">Syntax</span></span>            | [<span data-ttu-id="df023-123">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="df023-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="df023-124">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="df023-124">Implementations</span></span>

-   [<span data-ttu-id="df023-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="df023-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="df023-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="df023-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="df023-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="df023-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="df023-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="df023-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="df023-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="df023-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="df023-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="df023-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="df023-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="df023-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="df023-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="df023-132">Windows 2000 Server</span></span>



| <span data-ttu-id="df023-133">Voce</span><span class="sxs-lookup"><span data-stu-id="df023-133">Entry</span></span> | <span data-ttu-id="df023-134">Valore</span><span class="sxs-lookup"><span data-stu-id="df023-134">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="df023-135">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="df023-135">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="df023-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="df023-136">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="df023-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="df023-137">System-Only</span></span>            | <span data-ttu-id="df023-138">Falso</span><span class="sxs-lookup"><span data-stu-id="df023-138">False</span></span>                           |
| <span data-ttu-id="df023-139">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="df023-139">Is-Single-Valued</span></span>       | <span data-ttu-id="df023-140">Vero</span><span class="sxs-lookup"><span data-stu-id="df023-140">True</span></span>                            |
| <span data-ttu-id="df023-141">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="df023-141">Is Indexed</span></span>             | <span data-ttu-id="df023-142">Falso</span><span class="sxs-lookup"><span data-stu-id="df023-142">False</span></span>                           |
| <span data-ttu-id="df023-143">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="df023-143">In Global Catalog</span></span>      | <span data-ttu-id="df023-144">Falso</span><span class="sxs-lookup"><span data-stu-id="df023-144">False</span></span>                           |
| <span data-ttu-id="df023-145">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="df023-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="df023-146">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="df023-146">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="df023-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="df023-147">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="df023-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="df023-148">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="df023-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="df023-149">Search-Flags</span></span>           | <span data-ttu-id="df023-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="df023-150">0x00000000</span></span>                      |
| <span data-ttu-id="df023-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="df023-151">System-Flags</span></span>           | <span data-ttu-id="df023-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="df023-152">0x00000010</span></span>                      |
| <span data-ttu-id="df023-153">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="df023-153">Classes used in</span></span>        | [<span data-ttu-id="df023-154">**In alto**</span><span class="sxs-lookup"><span data-stu-id="df023-154">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="df023-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="df023-155">Windows Server 2003</span></span>



| <span data-ttu-id="df023-156">Voce</span><span class="sxs-lookup"><span data-stu-id="df023-156">Entry</span></span> | <span data-ttu-id="df023-157">Valore</span><span class="sxs-lookup"><span data-stu-id="df023-157">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="df023-158">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="df023-158">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="df023-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="df023-159">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="df023-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="df023-160">System-Only</span></span>            | <span data-ttu-id="df023-161">Falso</span><span class="sxs-lookup"><span data-stu-id="df023-161">False</span></span>                           |
| <span data-ttu-id="df023-162">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="df023-162">Is-Single-Valued</span></span>       | <span data-ttu-id="df023-163">Vero</span><span class="sxs-lookup"><span data-stu-id="df023-163">True</span></span>                            |
| <span data-ttu-id="df023-164">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="df023-164">Is Indexed</span></span>             | <span data-ttu-id="df023-165">Falso</span><span class="sxs-lookup"><span data-stu-id="df023-165">False</span></span>                           |
| <span data-ttu-id="df023-166">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="df023-166">In Global Catalog</span></span>      | <span data-ttu-id="df023-167">Falso</span><span class="sxs-lookup"><span data-stu-id="df023-167">False</span></span>                           |
| <span data-ttu-id="df023-168">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="df023-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="df023-169">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="df023-169">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="df023-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="df023-170">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="df023-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="df023-171">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="df023-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="df023-172">Search-Flags</span></span>           | <span data-ttu-id="df023-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="df023-173">0x00000000</span></span>                      |
| <span data-ttu-id="df023-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="df023-174">System-Flags</span></span>           | <span data-ttu-id="df023-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="df023-175">0x00000010</span></span>                      |
| <span data-ttu-id="df023-176">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="df023-176">Classes used in</span></span>        | [<span data-ttu-id="df023-177">**In alto**</span><span class="sxs-lookup"><span data-stu-id="df023-177">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="df023-178">ADAM</span><span class="sxs-lookup"><span data-stu-id="df023-178">ADAM</span></span>



| <span data-ttu-id="df023-179">Voce</span><span class="sxs-lookup"><span data-stu-id="df023-179">Entry</span></span> | <span data-ttu-id="df023-180">Valore</span><span class="sxs-lookup"><span data-stu-id="df023-180">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="df023-181">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="df023-181">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="df023-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="df023-182">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="df023-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="df023-183">System-Only</span></span>            | <span data-ttu-id="df023-184">Falso</span><span class="sxs-lookup"><span data-stu-id="df023-184">False</span></span>                           |
| <span data-ttu-id="df023-185">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="df023-185">Is-Single-Valued</span></span>       | <span data-ttu-id="df023-186">Vero</span><span class="sxs-lookup"><span data-stu-id="df023-186">True</span></span>                            |
| <span data-ttu-id="df023-187">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="df023-187">Is Indexed</span></span>             | <span data-ttu-id="df023-188">Falso</span><span class="sxs-lookup"><span data-stu-id="df023-188">False</span></span>                           |
| <span data-ttu-id="df023-189">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="df023-189">In Global Catalog</span></span>      | <span data-ttu-id="df023-190">Falso</span><span class="sxs-lookup"><span data-stu-id="df023-190">False</span></span>                           |
| <span data-ttu-id="df023-191">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="df023-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="df023-192">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="df023-192">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="df023-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="df023-193">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="df023-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="df023-194">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="df023-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="df023-195">Search-Flags</span></span>           | <span data-ttu-id="df023-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="df023-196">0x00000000</span></span>                      |
| <span data-ttu-id="df023-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="df023-197">System-Flags</span></span>           | <span data-ttu-id="df023-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="df023-198">0x00000010</span></span>                      |
| <span data-ttu-id="df023-199">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="df023-199">Classes used in</span></span>        | [<span data-ttu-id="df023-200">**In alto**</span><span class="sxs-lookup"><span data-stu-id="df023-200">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="df023-201">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="df023-201">Windows Server 2003 R2</span></span>



| <span data-ttu-id="df023-202">Voce</span><span class="sxs-lookup"><span data-stu-id="df023-202">Entry</span></span> | <span data-ttu-id="df023-203">Valore</span><span class="sxs-lookup"><span data-stu-id="df023-203">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="df023-204">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="df023-204">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="df023-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="df023-205">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="df023-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="df023-206">System-Only</span></span>            | <span data-ttu-id="df023-207">Falso</span><span class="sxs-lookup"><span data-stu-id="df023-207">False</span></span>                           |
| <span data-ttu-id="df023-208">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="df023-208">Is-Single-Valued</span></span>       | <span data-ttu-id="df023-209">Vero</span><span class="sxs-lookup"><span data-stu-id="df023-209">True</span></span>                            |
| <span data-ttu-id="df023-210">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="df023-210">Is Indexed</span></span>             | <span data-ttu-id="df023-211">Falso</span><span class="sxs-lookup"><span data-stu-id="df023-211">False</span></span>                           |
| <span data-ttu-id="df023-212">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="df023-212">In Global Catalog</span></span>      | <span data-ttu-id="df023-213">Falso</span><span class="sxs-lookup"><span data-stu-id="df023-213">False</span></span>                           |
| <span data-ttu-id="df023-214">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="df023-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="df023-215">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="df023-215">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="df023-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="df023-216">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="df023-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="df023-217">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="df023-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="df023-218">Search-Flags</span></span>           | <span data-ttu-id="df023-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="df023-219">0x00000000</span></span>                      |
| <span data-ttu-id="df023-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="df023-220">System-Flags</span></span>           | <span data-ttu-id="df023-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="df023-221">0x00000010</span></span>                      |
| <span data-ttu-id="df023-222">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="df023-222">Classes used in</span></span>        | [<span data-ttu-id="df023-223">**In alto**</span><span class="sxs-lookup"><span data-stu-id="df023-223">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="df023-224">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="df023-224">Windows Server 2008</span></span>



| <span data-ttu-id="df023-225">Voce</span><span class="sxs-lookup"><span data-stu-id="df023-225">Entry</span></span> | <span data-ttu-id="df023-226">Valore</span><span class="sxs-lookup"><span data-stu-id="df023-226">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="df023-227">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="df023-227">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="df023-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="df023-228">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="df023-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="df023-229">System-Only</span></span>            | <span data-ttu-id="df023-230">Falso</span><span class="sxs-lookup"><span data-stu-id="df023-230">False</span></span>                           |
| <span data-ttu-id="df023-231">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="df023-231">Is-Single-Valued</span></span>       | <span data-ttu-id="df023-232">Vero</span><span class="sxs-lookup"><span data-stu-id="df023-232">True</span></span>                            |
| <span data-ttu-id="df023-233">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="df023-233">Is Indexed</span></span>             | <span data-ttu-id="df023-234">Falso</span><span class="sxs-lookup"><span data-stu-id="df023-234">False</span></span>                           |
| <span data-ttu-id="df023-235">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="df023-235">In Global Catalog</span></span>      | <span data-ttu-id="df023-236">Falso</span><span class="sxs-lookup"><span data-stu-id="df023-236">False</span></span>                           |
| <span data-ttu-id="df023-237">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="df023-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="df023-238">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="df023-238">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="df023-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="df023-239">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="df023-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="df023-240">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="df023-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="df023-241">Search-Flags</span></span>           | <span data-ttu-id="df023-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="df023-242">0x00000000</span></span>                      |
| <span data-ttu-id="df023-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="df023-243">System-Flags</span></span>           | <span data-ttu-id="df023-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="df023-244">0x00000010</span></span>                      |
| <span data-ttu-id="df023-245">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="df023-245">Classes used in</span></span>        | [<span data-ttu-id="df023-246">**In alto**</span><span class="sxs-lookup"><span data-stu-id="df023-246">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="df023-247">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="df023-247">Windows Server 2008 R2</span></span>



| <span data-ttu-id="df023-248">Voce</span><span class="sxs-lookup"><span data-stu-id="df023-248">Entry</span></span> | <span data-ttu-id="df023-249">Valore</span><span class="sxs-lookup"><span data-stu-id="df023-249">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="df023-250">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="df023-250">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="df023-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="df023-251">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="df023-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="df023-252">System-Only</span></span>            | <span data-ttu-id="df023-253">Falso</span><span class="sxs-lookup"><span data-stu-id="df023-253">False</span></span>                           |
| <span data-ttu-id="df023-254">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="df023-254">Is-Single-Valued</span></span>       | <span data-ttu-id="df023-255">Vero</span><span class="sxs-lookup"><span data-stu-id="df023-255">True</span></span>                            |
| <span data-ttu-id="df023-256">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="df023-256">Is Indexed</span></span>             | <span data-ttu-id="df023-257">Falso</span><span class="sxs-lookup"><span data-stu-id="df023-257">False</span></span>                           |
| <span data-ttu-id="df023-258">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="df023-258">In Global Catalog</span></span>      | <span data-ttu-id="df023-259">Falso</span><span class="sxs-lookup"><span data-stu-id="df023-259">False</span></span>                           |
| <span data-ttu-id="df023-260">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="df023-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="df023-261">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="df023-261">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="df023-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="df023-262">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="df023-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="df023-263">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="df023-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="df023-264">Search-Flags</span></span>           | <span data-ttu-id="df023-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="df023-265">0x00000000</span></span>                      |
| <span data-ttu-id="df023-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="df023-266">System-Flags</span></span>           | <span data-ttu-id="df023-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="df023-267">0x00000010</span></span>                      |
| <span data-ttu-id="df023-268">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="df023-268">Classes used in</span></span>        | [<span data-ttu-id="df023-269">**In alto**</span><span class="sxs-lookup"><span data-stu-id="df023-269">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="df023-270">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="df023-270">Windows Server 2012</span></span>



| <span data-ttu-id="df023-271">Voce</span><span class="sxs-lookup"><span data-stu-id="df023-271">Entry</span></span> | <span data-ttu-id="df023-272">Valore</span><span class="sxs-lookup"><span data-stu-id="df023-272">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="df023-273">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="df023-273">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="df023-274">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="df023-274">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="df023-275">System-Only</span><span class="sxs-lookup"><span data-stu-id="df023-275">System-Only</span></span>            | <span data-ttu-id="df023-276">Falso</span><span class="sxs-lookup"><span data-stu-id="df023-276">False</span></span>                           |
| <span data-ttu-id="df023-277">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="df023-277">Is-Single-Valued</span></span>       | <span data-ttu-id="df023-278">Vero</span><span class="sxs-lookup"><span data-stu-id="df023-278">True</span></span>                            |
| <span data-ttu-id="df023-279">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="df023-279">Is Indexed</span></span>             | <span data-ttu-id="df023-280">Falso</span><span class="sxs-lookup"><span data-stu-id="df023-280">False</span></span>                           |
| <span data-ttu-id="df023-281">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="df023-281">In Global Catalog</span></span>      | <span data-ttu-id="df023-282">Falso</span><span class="sxs-lookup"><span data-stu-id="df023-282">False</span></span>                           |
| <span data-ttu-id="df023-283">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="df023-283">NT-Security-Descriptor</span></span> | <span data-ttu-id="df023-284">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="df023-284">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="df023-285">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="df023-285">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="df023-286">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="df023-286">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="df023-287">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="df023-287">Search-Flags</span></span>           | <span data-ttu-id="df023-288">0x00000000</span><span class="sxs-lookup"><span data-stu-id="df023-288">0x00000000</span></span>                      |
| <span data-ttu-id="df023-289">System-Flags</span><span class="sxs-lookup"><span data-stu-id="df023-289">System-Flags</span></span>           | <span data-ttu-id="df023-290">0x00000010</span><span class="sxs-lookup"><span data-stu-id="df023-290">0x00000010</span></span>                      |
| <span data-ttu-id="df023-291">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="df023-291">Classes used in</span></span>        | [<span data-ttu-id="df023-292">**In alto**</span><span class="sxs-lookup"><span data-stu-id="df023-292">**Top**</span></span>](c-top.md)<br/> |



 

 





