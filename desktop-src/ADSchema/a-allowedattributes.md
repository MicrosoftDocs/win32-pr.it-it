---
title: Attributo Allowed-Attributes
description: Attributi che saranno autorizzati a essere assegnati a una classe.
ms.assetid: ea73d3b9-51fc-486e-a5c7-f5123c5620bf
ms.tgt_platform: multiple
keywords:
- Schema AD Allowed-Attributes attribute
- Schema AD dell'attributo allowedAttributes
topic_type:
- apiref
api_name:
- Allowed-Attributes
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3049a6d03d17cb68062a38508baa09a4cdc91d6f
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104122190"
---
# <a name="allowed-attributes-attribute"></a><span data-ttu-id="c475a-105">Attributo Allowed-Attributes</span><span class="sxs-lookup"><span data-stu-id="c475a-105">Allowed-Attributes attribute</span></span>

<span data-ttu-id="c475a-106">Attributi che saranno autorizzati a essere assegnati a una classe.</span><span class="sxs-lookup"><span data-stu-id="c475a-106">Attributes that will be permitted to be assigned to a class.</span></span>



| <span data-ttu-id="c475a-107">Voce</span><span class="sxs-lookup"><span data-stu-id="c475a-107">Entry</span></span> | <span data-ttu-id="c475a-108">Valore</span><span class="sxs-lookup"><span data-stu-id="c475a-108">Value</span></span> |
|-------------------|-----------------------------------------------------------------|
| <span data-ttu-id="c475a-109">CN</span><span class="sxs-lookup"><span data-stu-id="c475a-109">CN</span></span>                | <span data-ttu-id="c475a-110">Allowed-Attributes</span><span class="sxs-lookup"><span data-stu-id="c475a-110">Allowed-Attributes</span></span>                                              |
| <span data-ttu-id="c475a-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="c475a-111">Ldap-Display-Name</span></span> | <span data-ttu-id="c475a-112">allowedAttributes</span><span class="sxs-lookup"><span data-stu-id="c475a-112">allowedAttributes</span></span>                                               |
| <span data-ttu-id="c475a-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="c475a-113">Size</span></span>              | \-                                                              |
| <span data-ttu-id="c475a-114">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="c475a-114">Update Privilege</span></span>  | \-                                                              |
| <span data-ttu-id="c475a-115">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="c475a-115">Update Frequency</span></span>  | \-                                                              |
| <span data-ttu-id="c475a-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c475a-116">Attribute-Id</span></span>      | <span data-ttu-id="c475a-117">1.2.840.113556.1.4.913</span><span class="sxs-lookup"><span data-stu-id="c475a-117">1.2.840.113556.1.4.913</span></span>                                          |
| <span data-ttu-id="c475a-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="c475a-118">System-Id-Guid</span></span>    | <span data-ttu-id="c475a-119">9a7ad940-ca53-11d1-bbd0-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="c475a-119">9a7ad940-ca53-11d1-bbd0-0080c76670c0</span></span>                            |
| <span data-ttu-id="c475a-120">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c475a-120">Syntax</span></span>            | [<span data-ttu-id="c475a-121">**String(Object-Identifier)**</span><span class="sxs-lookup"><span data-stu-id="c475a-121">**String(Object-Identifier)**</span></span>](s-string-object-identifier.md) |



## <a name="implementations"></a><span data-ttu-id="c475a-122">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="c475a-122">Implementations</span></span>

-   [<span data-ttu-id="c475a-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="c475a-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="c475a-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c475a-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c475a-125">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="c475a-125">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="c475a-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c475a-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c475a-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c475a-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c475a-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c475a-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c475a-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c475a-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="c475a-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c475a-130">Windows 2000 Server</span></span>



| <span data-ttu-id="c475a-131">Voce</span><span class="sxs-lookup"><span data-stu-id="c475a-131">Entry</span></span> | <span data-ttu-id="c475a-132">Valore</span><span class="sxs-lookup"><span data-stu-id="c475a-132">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c475a-133">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="c475a-133">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="c475a-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c475a-134">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="c475a-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="c475a-135">System-Only</span></span>            | <span data-ttu-id="c475a-136">Vero</span><span class="sxs-lookup"><span data-stu-id="c475a-136">True</span></span>                            |
| <span data-ttu-id="c475a-137">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="c475a-137">Is-Single-Valued</span></span>       | <span data-ttu-id="c475a-138">Falso</span><span class="sxs-lookup"><span data-stu-id="c475a-138">False</span></span>                           |
| <span data-ttu-id="c475a-139">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="c475a-139">Is Indexed</span></span>             | <span data-ttu-id="c475a-140">Falso</span><span class="sxs-lookup"><span data-stu-id="c475a-140">False</span></span>                           |
| <span data-ttu-id="c475a-141">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="c475a-141">In Global Catalog</span></span>      | <span data-ttu-id="c475a-142">Falso</span><span class="sxs-lookup"><span data-stu-id="c475a-142">False</span></span>                           |
| <span data-ttu-id="c475a-143">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="c475a-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="c475a-144">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="c475a-144">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c475a-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c475a-145">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="c475a-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c475a-146">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="c475a-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c475a-147">Search-Flags</span></span>           | <span data-ttu-id="c475a-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c475a-148">0x00000000</span></span>                      |
| <span data-ttu-id="c475a-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c475a-149">System-Flags</span></span>           | <span data-ttu-id="c475a-150">0x08000014</span><span class="sxs-lookup"><span data-stu-id="c475a-150">0x08000014</span></span>                      |
| <span data-ttu-id="c475a-151">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="c475a-151">Classes used in</span></span>        | [<span data-ttu-id="c475a-152">**In alto**</span><span class="sxs-lookup"><span data-stu-id="c475a-152">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="c475a-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c475a-153">Windows Server 2003</span></span>



| <span data-ttu-id="c475a-154">Voce</span><span class="sxs-lookup"><span data-stu-id="c475a-154">Entry</span></span> | <span data-ttu-id="c475a-155">Valore</span><span class="sxs-lookup"><span data-stu-id="c475a-155">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c475a-156">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="c475a-156">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="c475a-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c475a-157">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="c475a-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="c475a-158">System-Only</span></span>            | <span data-ttu-id="c475a-159">Vero</span><span class="sxs-lookup"><span data-stu-id="c475a-159">True</span></span>                            |
| <span data-ttu-id="c475a-160">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="c475a-160">Is-Single-Valued</span></span>       | <span data-ttu-id="c475a-161">Falso</span><span class="sxs-lookup"><span data-stu-id="c475a-161">False</span></span>                           |
| <span data-ttu-id="c475a-162">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="c475a-162">Is Indexed</span></span>             | <span data-ttu-id="c475a-163">Falso</span><span class="sxs-lookup"><span data-stu-id="c475a-163">False</span></span>                           |
| <span data-ttu-id="c475a-164">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="c475a-164">In Global Catalog</span></span>      | <span data-ttu-id="c475a-165">Falso</span><span class="sxs-lookup"><span data-stu-id="c475a-165">False</span></span>                           |
| <span data-ttu-id="c475a-166">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="c475a-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="c475a-167">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="c475a-167">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c475a-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c475a-168">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="c475a-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c475a-169">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="c475a-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c475a-170">Search-Flags</span></span>           | <span data-ttu-id="c475a-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c475a-171">0x00000000</span></span>                      |
| <span data-ttu-id="c475a-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c475a-172">System-Flags</span></span>           | <span data-ttu-id="c475a-173">0x08000014</span><span class="sxs-lookup"><span data-stu-id="c475a-173">0x08000014</span></span>                      |
| <span data-ttu-id="c475a-174">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="c475a-174">Classes used in</span></span>        | [<span data-ttu-id="c475a-175">**In alto**</span><span class="sxs-lookup"><span data-stu-id="c475a-175">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="c475a-176">ADAM</span><span class="sxs-lookup"><span data-stu-id="c475a-176">ADAM</span></span>



| <span data-ttu-id="c475a-177">Voce</span><span class="sxs-lookup"><span data-stu-id="c475a-177">Entry</span></span> | <span data-ttu-id="c475a-178">Valore</span><span class="sxs-lookup"><span data-stu-id="c475a-178">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c475a-179">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="c475a-179">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="c475a-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c475a-180">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="c475a-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="c475a-181">System-Only</span></span>            | <span data-ttu-id="c475a-182">Vero</span><span class="sxs-lookup"><span data-stu-id="c475a-182">True</span></span>                            |
| <span data-ttu-id="c475a-183">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="c475a-183">Is-Single-Valued</span></span>       | <span data-ttu-id="c475a-184">Falso</span><span class="sxs-lookup"><span data-stu-id="c475a-184">False</span></span>                           |
| <span data-ttu-id="c475a-185">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="c475a-185">Is Indexed</span></span>             | <span data-ttu-id="c475a-186">Falso</span><span class="sxs-lookup"><span data-stu-id="c475a-186">False</span></span>                           |
| <span data-ttu-id="c475a-187">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="c475a-187">In Global Catalog</span></span>      | <span data-ttu-id="c475a-188">Falso</span><span class="sxs-lookup"><span data-stu-id="c475a-188">False</span></span>                           |
| <span data-ttu-id="c475a-189">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="c475a-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="c475a-190">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="c475a-190">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c475a-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c475a-191">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="c475a-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c475a-192">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="c475a-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c475a-193">Search-Flags</span></span>           | <span data-ttu-id="c475a-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c475a-194">0x00000000</span></span>                      |
| <span data-ttu-id="c475a-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c475a-195">System-Flags</span></span>           | <span data-ttu-id="c475a-196">0x08000014</span><span class="sxs-lookup"><span data-stu-id="c475a-196">0x08000014</span></span>                      |
| <span data-ttu-id="c475a-197">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="c475a-197">Classes used in</span></span>        | [<span data-ttu-id="c475a-198">**In alto**</span><span class="sxs-lookup"><span data-stu-id="c475a-198">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c475a-199">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c475a-199">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c475a-200">Voce</span><span class="sxs-lookup"><span data-stu-id="c475a-200">Entry</span></span> | <span data-ttu-id="c475a-201">Valore</span><span class="sxs-lookup"><span data-stu-id="c475a-201">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c475a-202">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="c475a-202">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="c475a-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c475a-203">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="c475a-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="c475a-204">System-Only</span></span>            | <span data-ttu-id="c475a-205">Vero</span><span class="sxs-lookup"><span data-stu-id="c475a-205">True</span></span>                            |
| <span data-ttu-id="c475a-206">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="c475a-206">Is-Single-Valued</span></span>       | <span data-ttu-id="c475a-207">Falso</span><span class="sxs-lookup"><span data-stu-id="c475a-207">False</span></span>                           |
| <span data-ttu-id="c475a-208">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="c475a-208">Is Indexed</span></span>             | <span data-ttu-id="c475a-209">Falso</span><span class="sxs-lookup"><span data-stu-id="c475a-209">False</span></span>                           |
| <span data-ttu-id="c475a-210">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="c475a-210">In Global Catalog</span></span>      | <span data-ttu-id="c475a-211">Falso</span><span class="sxs-lookup"><span data-stu-id="c475a-211">False</span></span>                           |
| <span data-ttu-id="c475a-212">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="c475a-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="c475a-213">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="c475a-213">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c475a-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c475a-214">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="c475a-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c475a-215">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="c475a-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c475a-216">Search-Flags</span></span>           | <span data-ttu-id="c475a-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c475a-217">0x00000000</span></span>                      |
| <span data-ttu-id="c475a-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c475a-218">System-Flags</span></span>           | <span data-ttu-id="c475a-219">0x08000014</span><span class="sxs-lookup"><span data-stu-id="c475a-219">0x08000014</span></span>                      |
| <span data-ttu-id="c475a-220">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="c475a-220">Classes used in</span></span>        | [<span data-ttu-id="c475a-221">**In alto**</span><span class="sxs-lookup"><span data-stu-id="c475a-221">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c475a-222">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c475a-222">Windows Server 2008</span></span>



| <span data-ttu-id="c475a-223">Voce</span><span class="sxs-lookup"><span data-stu-id="c475a-223">Entry</span></span> | <span data-ttu-id="c475a-224">Valore</span><span class="sxs-lookup"><span data-stu-id="c475a-224">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c475a-225">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="c475a-225">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="c475a-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c475a-226">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="c475a-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="c475a-227">System-Only</span></span>            | <span data-ttu-id="c475a-228">Vero</span><span class="sxs-lookup"><span data-stu-id="c475a-228">True</span></span>                            |
| <span data-ttu-id="c475a-229">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="c475a-229">Is-Single-Valued</span></span>       | <span data-ttu-id="c475a-230">Falso</span><span class="sxs-lookup"><span data-stu-id="c475a-230">False</span></span>                           |
| <span data-ttu-id="c475a-231">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="c475a-231">Is Indexed</span></span>             | <span data-ttu-id="c475a-232">Falso</span><span class="sxs-lookup"><span data-stu-id="c475a-232">False</span></span>                           |
| <span data-ttu-id="c475a-233">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="c475a-233">In Global Catalog</span></span>      | <span data-ttu-id="c475a-234">Falso</span><span class="sxs-lookup"><span data-stu-id="c475a-234">False</span></span>                           |
| <span data-ttu-id="c475a-235">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="c475a-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="c475a-236">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="c475a-236">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c475a-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c475a-237">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="c475a-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c475a-238">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="c475a-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c475a-239">Search-Flags</span></span>           | <span data-ttu-id="c475a-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c475a-240">0x00000000</span></span>                      |
| <span data-ttu-id="c475a-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c475a-241">System-Flags</span></span>           | <span data-ttu-id="c475a-242">0x08000014</span><span class="sxs-lookup"><span data-stu-id="c475a-242">0x08000014</span></span>                      |
| <span data-ttu-id="c475a-243">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="c475a-243">Classes used in</span></span>        | [<span data-ttu-id="c475a-244">**In alto**</span><span class="sxs-lookup"><span data-stu-id="c475a-244">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c475a-245">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c475a-245">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c475a-246">Voce</span><span class="sxs-lookup"><span data-stu-id="c475a-246">Entry</span></span> | <span data-ttu-id="c475a-247">Valore</span><span class="sxs-lookup"><span data-stu-id="c475a-247">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c475a-248">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="c475a-248">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="c475a-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c475a-249">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="c475a-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="c475a-250">System-Only</span></span>            | <span data-ttu-id="c475a-251">Vero</span><span class="sxs-lookup"><span data-stu-id="c475a-251">True</span></span>                            |
| <span data-ttu-id="c475a-252">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="c475a-252">Is-Single-Valued</span></span>       | <span data-ttu-id="c475a-253">Falso</span><span class="sxs-lookup"><span data-stu-id="c475a-253">False</span></span>                           |
| <span data-ttu-id="c475a-254">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="c475a-254">Is Indexed</span></span>             | <span data-ttu-id="c475a-255">Falso</span><span class="sxs-lookup"><span data-stu-id="c475a-255">False</span></span>                           |
| <span data-ttu-id="c475a-256">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="c475a-256">In Global Catalog</span></span>      | <span data-ttu-id="c475a-257">Falso</span><span class="sxs-lookup"><span data-stu-id="c475a-257">False</span></span>                           |
| <span data-ttu-id="c475a-258">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="c475a-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="c475a-259">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="c475a-259">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c475a-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c475a-260">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="c475a-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c475a-261">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="c475a-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c475a-262">Search-Flags</span></span>           | <span data-ttu-id="c475a-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c475a-263">0x00000000</span></span>                      |
| <span data-ttu-id="c475a-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c475a-264">System-Flags</span></span>           | <span data-ttu-id="c475a-265">0x08000014</span><span class="sxs-lookup"><span data-stu-id="c475a-265">0x08000014</span></span>                      |
| <span data-ttu-id="c475a-266">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="c475a-266">Classes used in</span></span>        | [<span data-ttu-id="c475a-267">**In alto**</span><span class="sxs-lookup"><span data-stu-id="c475a-267">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c475a-268">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c475a-268">Windows Server 2012</span></span>



| <span data-ttu-id="c475a-269">Voce</span><span class="sxs-lookup"><span data-stu-id="c475a-269">Entry</span></span> | <span data-ttu-id="c475a-270">Valore</span><span class="sxs-lookup"><span data-stu-id="c475a-270">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c475a-271">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="c475a-271">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="c475a-272">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c475a-272">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="c475a-273">System-Only</span><span class="sxs-lookup"><span data-stu-id="c475a-273">System-Only</span></span>            | <span data-ttu-id="c475a-274">Vero</span><span class="sxs-lookup"><span data-stu-id="c475a-274">True</span></span>                            |
| <span data-ttu-id="c475a-275">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="c475a-275">Is-Single-Valued</span></span>       | <span data-ttu-id="c475a-276">Falso</span><span class="sxs-lookup"><span data-stu-id="c475a-276">False</span></span>                           |
| <span data-ttu-id="c475a-277">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="c475a-277">Is Indexed</span></span>             | <span data-ttu-id="c475a-278">Falso</span><span class="sxs-lookup"><span data-stu-id="c475a-278">False</span></span>                           |
| <span data-ttu-id="c475a-279">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="c475a-279">In Global Catalog</span></span>      | <span data-ttu-id="c475a-280">Falso</span><span class="sxs-lookup"><span data-stu-id="c475a-280">False</span></span>                           |
| <span data-ttu-id="c475a-281">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="c475a-281">NT-Security-Descriptor</span></span> | <span data-ttu-id="c475a-282">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="c475a-282">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c475a-283">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c475a-283">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="c475a-284">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c475a-284">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="c475a-285">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c475a-285">Search-Flags</span></span>           | <span data-ttu-id="c475a-286">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c475a-286">0x00000000</span></span>                      |
| <span data-ttu-id="c475a-287">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c475a-287">System-Flags</span></span>           | <span data-ttu-id="c475a-288">0x08000014</span><span class="sxs-lookup"><span data-stu-id="c475a-288">0x08000014</span></span>                      |
| <span data-ttu-id="c475a-289">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="c475a-289">Classes used in</span></span>        | [<span data-ttu-id="c475a-290">**In alto**</span><span class="sxs-lookup"><span data-stu-id="c475a-290">**Top**</span></span>](c-top.md)<br/> |



 

 





