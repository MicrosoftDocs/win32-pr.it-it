---
title: Attributo From-Entry
description: Si tratta di un attributo costruito che è TRUE se l'oggetto è scrivibile e FALSE se è di sola lettura, ad esempio un'istanza di replica GC.
ms.assetid: b43e979d-15f9-4425-8a58-c9ed71bab1e4
ms.tgt_platform: multiple
keywords:
- Schema AD From-Entry attribute
- Schema AD dell'attributo fromEntry
topic_type:
- apiref
api_name:
- From-Entry
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c5f5e45e2897b917ad442f1b1b5d77246fa079c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "106303024"
---
# <a name="from-entry-attribute"></a><span data-ttu-id="2b2da-105">Attributo From-Entry</span><span class="sxs-lookup"><span data-stu-id="2b2da-105">From-Entry attribute</span></span>

<span data-ttu-id="2b2da-106">Si tratta di un attributo costruito che è **true** se l'oggetto è scrivibile e **false** se è di sola lettura, ad esempio un'istanza di replica GC.</span><span class="sxs-lookup"><span data-stu-id="2b2da-106">This is a constructed attribute that is **TRUE** if the object is writable and **FALSE** if it is read-only, for example, a GC replica instance.</span></span>



| <span data-ttu-id="2b2da-107">Voce</span><span class="sxs-lookup"><span data-stu-id="2b2da-107">Entry</span></span> | <span data-ttu-id="2b2da-108">Valore</span><span class="sxs-lookup"><span data-stu-id="2b2da-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="2b2da-109">CN</span><span class="sxs-lookup"><span data-stu-id="2b2da-109">CN</span></span>                | <span data-ttu-id="2b2da-110">From-Entry</span><span class="sxs-lookup"><span data-stu-id="2b2da-110">From-Entry</span></span>                           |
| <span data-ttu-id="2b2da-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="2b2da-111">Ldap-Display-Name</span></span> | <span data-ttu-id="2b2da-112">fromEntry</span><span class="sxs-lookup"><span data-stu-id="2b2da-112">fromEntry</span></span>                            |
| <span data-ttu-id="2b2da-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="2b2da-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="2b2da-114">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="2b2da-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="2b2da-115">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="2b2da-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="2b2da-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="2b2da-116">Attribute-Id</span></span>      | <span data-ttu-id="2b2da-117">1.2.840.113556.1.4.910</span><span class="sxs-lookup"><span data-stu-id="2b2da-117">1.2.840.113556.1.4.910</span></span>               |
| <span data-ttu-id="2b2da-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="2b2da-118">System-Id-Guid</span></span>    | <span data-ttu-id="2b2da-119">9a7ad949-ca53-11d1-bbd0-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="2b2da-119">9a7ad949-ca53-11d1-bbd0-0080c76670c0</span></span> |
| <span data-ttu-id="2b2da-120">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2b2da-120">Syntax</span></span>            | [<span data-ttu-id="2b2da-121">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="2b2da-121">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="2b2da-122">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="2b2da-122">Implementations</span></span>

-   [<span data-ttu-id="2b2da-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="2b2da-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="2b2da-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="2b2da-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="2b2da-125">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="2b2da-125">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="2b2da-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="2b2da-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="2b2da-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="2b2da-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="2b2da-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="2b2da-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="2b2da-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="2b2da-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="2b2da-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2b2da-130">Windows 2000 Server</span></span>



| <span data-ttu-id="2b2da-131">Voce</span><span class="sxs-lookup"><span data-stu-id="2b2da-131">Entry</span></span> | <span data-ttu-id="2b2da-132">Valore</span><span class="sxs-lookup"><span data-stu-id="2b2da-132">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="2b2da-133">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="2b2da-133">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="2b2da-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2b2da-134">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="2b2da-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="2b2da-135">System-Only</span></span>            | <span data-ttu-id="2b2da-136">Vero</span><span class="sxs-lookup"><span data-stu-id="2b2da-136">True</span></span>                            |
| <span data-ttu-id="2b2da-137">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="2b2da-137">Is-Single-Valued</span></span>       | <span data-ttu-id="2b2da-138">Falso</span><span class="sxs-lookup"><span data-stu-id="2b2da-138">False</span></span>                           |
| <span data-ttu-id="2b2da-139">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="2b2da-139">Is Indexed</span></span>             | <span data-ttu-id="2b2da-140">Falso</span><span class="sxs-lookup"><span data-stu-id="2b2da-140">False</span></span>                           |
| <span data-ttu-id="2b2da-141">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="2b2da-141">In Global Catalog</span></span>      | <span data-ttu-id="2b2da-142">Falso</span><span class="sxs-lookup"><span data-stu-id="2b2da-142">False</span></span>                           |
| <span data-ttu-id="2b2da-143">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="2b2da-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="2b2da-144">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="2b2da-144">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="2b2da-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2b2da-145">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="2b2da-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2b2da-146">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="2b2da-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2b2da-147">Search-Flags</span></span>           | <span data-ttu-id="2b2da-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2b2da-148">0x00000000</span></span>                      |
| <span data-ttu-id="2b2da-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2b2da-149">System-Flags</span></span>           | <span data-ttu-id="2b2da-150">0x08000014</span><span class="sxs-lookup"><span data-stu-id="2b2da-150">0x08000014</span></span>                      |
| <span data-ttu-id="2b2da-151">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="2b2da-151">Classes used in</span></span>        | [<span data-ttu-id="2b2da-152">**In alto**</span><span class="sxs-lookup"><span data-stu-id="2b2da-152">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="2b2da-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2b2da-153">Windows Server 2003</span></span>



| <span data-ttu-id="2b2da-154">Voce</span><span class="sxs-lookup"><span data-stu-id="2b2da-154">Entry</span></span> | <span data-ttu-id="2b2da-155">Valore</span><span class="sxs-lookup"><span data-stu-id="2b2da-155">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="2b2da-156">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="2b2da-156">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="2b2da-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2b2da-157">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="2b2da-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="2b2da-158">System-Only</span></span>            | <span data-ttu-id="2b2da-159">Vero</span><span class="sxs-lookup"><span data-stu-id="2b2da-159">True</span></span>                            |
| <span data-ttu-id="2b2da-160">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="2b2da-160">Is-Single-Valued</span></span>       | <span data-ttu-id="2b2da-161">Falso</span><span class="sxs-lookup"><span data-stu-id="2b2da-161">False</span></span>                           |
| <span data-ttu-id="2b2da-162">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="2b2da-162">Is Indexed</span></span>             | <span data-ttu-id="2b2da-163">Falso</span><span class="sxs-lookup"><span data-stu-id="2b2da-163">False</span></span>                           |
| <span data-ttu-id="2b2da-164">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="2b2da-164">In Global Catalog</span></span>      | <span data-ttu-id="2b2da-165">Falso</span><span class="sxs-lookup"><span data-stu-id="2b2da-165">False</span></span>                           |
| <span data-ttu-id="2b2da-166">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="2b2da-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="2b2da-167">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="2b2da-167">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="2b2da-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2b2da-168">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="2b2da-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2b2da-169">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="2b2da-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2b2da-170">Search-Flags</span></span>           | <span data-ttu-id="2b2da-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2b2da-171">0x00000000</span></span>                      |
| <span data-ttu-id="2b2da-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2b2da-172">System-Flags</span></span>           | <span data-ttu-id="2b2da-173">0x08000014</span><span class="sxs-lookup"><span data-stu-id="2b2da-173">0x08000014</span></span>                      |
| <span data-ttu-id="2b2da-174">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="2b2da-174">Classes used in</span></span>        | [<span data-ttu-id="2b2da-175">**In alto**</span><span class="sxs-lookup"><span data-stu-id="2b2da-175">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="2b2da-176">ADAM</span><span class="sxs-lookup"><span data-stu-id="2b2da-176">ADAM</span></span>



| <span data-ttu-id="2b2da-177">Voce</span><span class="sxs-lookup"><span data-stu-id="2b2da-177">Entry</span></span> | <span data-ttu-id="2b2da-178">Valore</span><span class="sxs-lookup"><span data-stu-id="2b2da-178">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="2b2da-179">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="2b2da-179">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="2b2da-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2b2da-180">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="2b2da-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="2b2da-181">System-Only</span></span>            | <span data-ttu-id="2b2da-182">Vero</span><span class="sxs-lookup"><span data-stu-id="2b2da-182">True</span></span>                            |
| <span data-ttu-id="2b2da-183">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="2b2da-183">Is-Single-Valued</span></span>       | <span data-ttu-id="2b2da-184">Falso</span><span class="sxs-lookup"><span data-stu-id="2b2da-184">False</span></span>                           |
| <span data-ttu-id="2b2da-185">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="2b2da-185">Is Indexed</span></span>             | <span data-ttu-id="2b2da-186">Falso</span><span class="sxs-lookup"><span data-stu-id="2b2da-186">False</span></span>                           |
| <span data-ttu-id="2b2da-187">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="2b2da-187">In Global Catalog</span></span>      | <span data-ttu-id="2b2da-188">Falso</span><span class="sxs-lookup"><span data-stu-id="2b2da-188">False</span></span>                           |
| <span data-ttu-id="2b2da-189">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="2b2da-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="2b2da-190">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="2b2da-190">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="2b2da-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2b2da-191">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="2b2da-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2b2da-192">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="2b2da-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2b2da-193">Search-Flags</span></span>           | <span data-ttu-id="2b2da-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2b2da-194">0x00000000</span></span>                      |
| <span data-ttu-id="2b2da-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2b2da-195">System-Flags</span></span>           | <span data-ttu-id="2b2da-196">0x08000014</span><span class="sxs-lookup"><span data-stu-id="2b2da-196">0x08000014</span></span>                      |
| <span data-ttu-id="2b2da-197">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="2b2da-197">Classes used in</span></span>        | [<span data-ttu-id="2b2da-198">**In alto**</span><span class="sxs-lookup"><span data-stu-id="2b2da-198">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="2b2da-199">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="2b2da-199">Windows Server 2003 R2</span></span>



| <span data-ttu-id="2b2da-200">Voce</span><span class="sxs-lookup"><span data-stu-id="2b2da-200">Entry</span></span> | <span data-ttu-id="2b2da-201">Valore</span><span class="sxs-lookup"><span data-stu-id="2b2da-201">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="2b2da-202">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="2b2da-202">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="2b2da-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2b2da-203">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="2b2da-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="2b2da-204">System-Only</span></span>            | <span data-ttu-id="2b2da-205">Vero</span><span class="sxs-lookup"><span data-stu-id="2b2da-205">True</span></span>                            |
| <span data-ttu-id="2b2da-206">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="2b2da-206">Is-Single-Valued</span></span>       | <span data-ttu-id="2b2da-207">Falso</span><span class="sxs-lookup"><span data-stu-id="2b2da-207">False</span></span>                           |
| <span data-ttu-id="2b2da-208">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="2b2da-208">Is Indexed</span></span>             | <span data-ttu-id="2b2da-209">Falso</span><span class="sxs-lookup"><span data-stu-id="2b2da-209">False</span></span>                           |
| <span data-ttu-id="2b2da-210">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="2b2da-210">In Global Catalog</span></span>      | <span data-ttu-id="2b2da-211">Falso</span><span class="sxs-lookup"><span data-stu-id="2b2da-211">False</span></span>                           |
| <span data-ttu-id="2b2da-212">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="2b2da-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="2b2da-213">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="2b2da-213">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="2b2da-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2b2da-214">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="2b2da-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2b2da-215">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="2b2da-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2b2da-216">Search-Flags</span></span>           | <span data-ttu-id="2b2da-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2b2da-217">0x00000000</span></span>                      |
| <span data-ttu-id="2b2da-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2b2da-218">System-Flags</span></span>           | <span data-ttu-id="2b2da-219">0x08000014</span><span class="sxs-lookup"><span data-stu-id="2b2da-219">0x08000014</span></span>                      |
| <span data-ttu-id="2b2da-220">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="2b2da-220">Classes used in</span></span>        | [<span data-ttu-id="2b2da-221">**In alto**</span><span class="sxs-lookup"><span data-stu-id="2b2da-221">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="2b2da-222">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2b2da-222">Windows Server 2008</span></span>



| <span data-ttu-id="2b2da-223">Voce</span><span class="sxs-lookup"><span data-stu-id="2b2da-223">Entry</span></span> | <span data-ttu-id="2b2da-224">Valore</span><span class="sxs-lookup"><span data-stu-id="2b2da-224">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="2b2da-225">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="2b2da-225">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="2b2da-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2b2da-226">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="2b2da-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="2b2da-227">System-Only</span></span>            | <span data-ttu-id="2b2da-228">Vero</span><span class="sxs-lookup"><span data-stu-id="2b2da-228">True</span></span>                            |
| <span data-ttu-id="2b2da-229">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="2b2da-229">Is-Single-Valued</span></span>       | <span data-ttu-id="2b2da-230">Falso</span><span class="sxs-lookup"><span data-stu-id="2b2da-230">False</span></span>                           |
| <span data-ttu-id="2b2da-231">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="2b2da-231">Is Indexed</span></span>             | <span data-ttu-id="2b2da-232">Falso</span><span class="sxs-lookup"><span data-stu-id="2b2da-232">False</span></span>                           |
| <span data-ttu-id="2b2da-233">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="2b2da-233">In Global Catalog</span></span>      | <span data-ttu-id="2b2da-234">Falso</span><span class="sxs-lookup"><span data-stu-id="2b2da-234">False</span></span>                           |
| <span data-ttu-id="2b2da-235">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="2b2da-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="2b2da-236">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="2b2da-236">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="2b2da-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2b2da-237">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="2b2da-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2b2da-238">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="2b2da-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2b2da-239">Search-Flags</span></span>           | <span data-ttu-id="2b2da-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2b2da-240">0x00000000</span></span>                      |
| <span data-ttu-id="2b2da-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2b2da-241">System-Flags</span></span>           | <span data-ttu-id="2b2da-242">0x08000014</span><span class="sxs-lookup"><span data-stu-id="2b2da-242">0x08000014</span></span>                      |
| <span data-ttu-id="2b2da-243">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="2b2da-243">Classes used in</span></span>        | [<span data-ttu-id="2b2da-244">**In alto**</span><span class="sxs-lookup"><span data-stu-id="2b2da-244">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="2b2da-245">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2b2da-245">Windows Server 2008 R2</span></span>



| <span data-ttu-id="2b2da-246">Voce</span><span class="sxs-lookup"><span data-stu-id="2b2da-246">Entry</span></span> | <span data-ttu-id="2b2da-247">Valore</span><span class="sxs-lookup"><span data-stu-id="2b2da-247">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="2b2da-248">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="2b2da-248">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="2b2da-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2b2da-249">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="2b2da-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="2b2da-250">System-Only</span></span>            | <span data-ttu-id="2b2da-251">Vero</span><span class="sxs-lookup"><span data-stu-id="2b2da-251">True</span></span>                            |
| <span data-ttu-id="2b2da-252">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="2b2da-252">Is-Single-Valued</span></span>       | <span data-ttu-id="2b2da-253">Falso</span><span class="sxs-lookup"><span data-stu-id="2b2da-253">False</span></span>                           |
| <span data-ttu-id="2b2da-254">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="2b2da-254">Is Indexed</span></span>             | <span data-ttu-id="2b2da-255">Falso</span><span class="sxs-lookup"><span data-stu-id="2b2da-255">False</span></span>                           |
| <span data-ttu-id="2b2da-256">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="2b2da-256">In Global Catalog</span></span>      | <span data-ttu-id="2b2da-257">Falso</span><span class="sxs-lookup"><span data-stu-id="2b2da-257">False</span></span>                           |
| <span data-ttu-id="2b2da-258">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="2b2da-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="2b2da-259">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="2b2da-259">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="2b2da-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2b2da-260">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="2b2da-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2b2da-261">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="2b2da-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2b2da-262">Search-Flags</span></span>           | <span data-ttu-id="2b2da-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2b2da-263">0x00000000</span></span>                      |
| <span data-ttu-id="2b2da-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2b2da-264">System-Flags</span></span>           | <span data-ttu-id="2b2da-265">0x08000014</span><span class="sxs-lookup"><span data-stu-id="2b2da-265">0x08000014</span></span>                      |
| <span data-ttu-id="2b2da-266">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="2b2da-266">Classes used in</span></span>        | [<span data-ttu-id="2b2da-267">**In alto**</span><span class="sxs-lookup"><span data-stu-id="2b2da-267">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="2b2da-268">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2b2da-268">Windows Server 2012</span></span>



| <span data-ttu-id="2b2da-269">Voce</span><span class="sxs-lookup"><span data-stu-id="2b2da-269">Entry</span></span> | <span data-ttu-id="2b2da-270">Valore</span><span class="sxs-lookup"><span data-stu-id="2b2da-270">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="2b2da-271">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="2b2da-271">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="2b2da-272">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2b2da-272">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="2b2da-273">System-Only</span><span class="sxs-lookup"><span data-stu-id="2b2da-273">System-Only</span></span>            | <span data-ttu-id="2b2da-274">Vero</span><span class="sxs-lookup"><span data-stu-id="2b2da-274">True</span></span>                            |
| <span data-ttu-id="2b2da-275">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="2b2da-275">Is-Single-Valued</span></span>       | <span data-ttu-id="2b2da-276">Falso</span><span class="sxs-lookup"><span data-stu-id="2b2da-276">False</span></span>                           |
| <span data-ttu-id="2b2da-277">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="2b2da-277">Is Indexed</span></span>             | <span data-ttu-id="2b2da-278">Falso</span><span class="sxs-lookup"><span data-stu-id="2b2da-278">False</span></span>                           |
| <span data-ttu-id="2b2da-279">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="2b2da-279">In Global Catalog</span></span>      | <span data-ttu-id="2b2da-280">Falso</span><span class="sxs-lookup"><span data-stu-id="2b2da-280">False</span></span>                           |
| <span data-ttu-id="2b2da-281">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="2b2da-281">NT-Security-Descriptor</span></span> | <span data-ttu-id="2b2da-282">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="2b2da-282">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="2b2da-283">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2b2da-283">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="2b2da-284">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2b2da-284">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="2b2da-285">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2b2da-285">Search-Flags</span></span>           | <span data-ttu-id="2b2da-286">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2b2da-286">0x00000000</span></span>                      |
| <span data-ttu-id="2b2da-287">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2b2da-287">System-Flags</span></span>           | <span data-ttu-id="2b2da-288">0x08000014</span><span class="sxs-lookup"><span data-stu-id="2b2da-288">0x08000014</span></span>                      |
| <span data-ttu-id="2b2da-289">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="2b2da-289">Classes used in</span></span>        | [<span data-ttu-id="2b2da-290">**In alto**</span><span class="sxs-lookup"><span data-stu-id="2b2da-290">**Top**</span></span>](c-top.md)<br/> |



 

 





