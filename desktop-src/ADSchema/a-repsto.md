---
title: Attributo Reps-To
description: Elenca i server a cui la directory invierà una notifica delle modifiche e dei server a cui la directory invierà le modifiche su richiesta per il contesto dei nomi definito.
ms.assetid: d7fd5a57-a0e1-4c69-9b9a-1cdad87610b1
ms.tgt_platform: multiple
keywords:
- Schema AD Reps-To attribute
- Schema AD dell'attributo repsTo
topic_type:
- apiref
api_name:
- Reps-To
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd5c39d19eb12bb801d7ca7fb9b22ed665d59d10
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103965340"
---
# <a name="reps-to-attribute"></a><span data-ttu-id="53208-105">Attributo Reps-To</span><span class="sxs-lookup"><span data-stu-id="53208-105">Reps-To attribute</span></span>

<span data-ttu-id="53208-106">Elenca i server a cui la directory invierà una notifica delle modifiche e dei server a cui la directory invierà le modifiche su richiesta per il contesto dei nomi definito.</span><span class="sxs-lookup"><span data-stu-id="53208-106">Lists the servers that the directory will notify of changes and servers to which the directory will send changes on Request for the defined naming context.</span></span>



| <span data-ttu-id="53208-107">Voce</span><span class="sxs-lookup"><span data-stu-id="53208-107">Entry</span></span> | <span data-ttu-id="53208-108">Valore</span><span class="sxs-lookup"><span data-stu-id="53208-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="53208-109">CN</span><span class="sxs-lookup"><span data-stu-id="53208-109">CN</span></span>                | <span data-ttu-id="53208-110">Reps-To</span><span class="sxs-lookup"><span data-stu-id="53208-110">Reps-To</span></span>                                               |
| <span data-ttu-id="53208-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="53208-111">Ldap-Display-Name</span></span> | <span data-ttu-id="53208-112">repsTo</span><span class="sxs-lookup"><span data-stu-id="53208-112">repsTo</span></span>                                                |
| <span data-ttu-id="53208-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="53208-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="53208-114">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="53208-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="53208-115">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="53208-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="53208-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="53208-116">Attribute-Id</span></span>      | <span data-ttu-id="53208-117">1.2.840.113556.1.2.83</span><span class="sxs-lookup"><span data-stu-id="53208-117">1.2.840.113556.1.2.83</span></span>                                 |
| <span data-ttu-id="53208-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="53208-118">System-Id-Guid</span></span>    | <span data-ttu-id="53208-119">bf967a1e-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="53208-119">bf967a1e-0de6-11d0-a285-00aa003049e2</span></span>                  |
| <span data-ttu-id="53208-120">Sintassi</span><span class="sxs-lookup"><span data-stu-id="53208-120">Syntax</span></span>            | [<span data-ttu-id="53208-121">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="53208-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="53208-122">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="53208-122">Implementations</span></span>

-   [<span data-ttu-id="53208-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="53208-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="53208-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="53208-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="53208-125">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="53208-125">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="53208-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="53208-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="53208-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="53208-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="53208-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="53208-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="53208-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="53208-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="53208-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="53208-130">Windows 2000 Server</span></span>



| <span data-ttu-id="53208-131">Voce</span><span class="sxs-lookup"><span data-stu-id="53208-131">Entry</span></span> | <span data-ttu-id="53208-132">Valore</span><span class="sxs-lookup"><span data-stu-id="53208-132">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="53208-133">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="53208-133">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="53208-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="53208-134">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="53208-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="53208-135">System-Only</span></span>            | <span data-ttu-id="53208-136">Vero</span><span class="sxs-lookup"><span data-stu-id="53208-136">True</span></span>                            |
| <span data-ttu-id="53208-137">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="53208-137">Is-Single-Valued</span></span>       | <span data-ttu-id="53208-138">Falso</span><span class="sxs-lookup"><span data-stu-id="53208-138">False</span></span>                           |
| <span data-ttu-id="53208-139">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="53208-139">Is Indexed</span></span>             | <span data-ttu-id="53208-140">Falso</span><span class="sxs-lookup"><span data-stu-id="53208-140">False</span></span>                           |
| <span data-ttu-id="53208-141">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="53208-141">In Global Catalog</span></span>      | <span data-ttu-id="53208-142">Vero</span><span class="sxs-lookup"><span data-stu-id="53208-142">True</span></span>                            |
| <span data-ttu-id="53208-143">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="53208-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="53208-144">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="53208-144">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="53208-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="53208-145">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="53208-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="53208-146">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="53208-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="53208-147">Search-Flags</span></span>           | <span data-ttu-id="53208-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="53208-148">0x00000000</span></span>                      |
| <span data-ttu-id="53208-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="53208-149">System-Flags</span></span>           | <span data-ttu-id="53208-150">0x00000013</span><span class="sxs-lookup"><span data-stu-id="53208-150">0x00000013</span></span>                      |
| <span data-ttu-id="53208-151">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="53208-151">Classes used in</span></span>        | [<span data-ttu-id="53208-152">**In alto**</span><span class="sxs-lookup"><span data-stu-id="53208-152">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="53208-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="53208-153">Windows Server 2003</span></span>



| <span data-ttu-id="53208-154">Voce</span><span class="sxs-lookup"><span data-stu-id="53208-154">Entry</span></span> | <span data-ttu-id="53208-155">Valore</span><span class="sxs-lookup"><span data-stu-id="53208-155">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="53208-156">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="53208-156">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="53208-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="53208-157">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="53208-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="53208-158">System-Only</span></span>            | <span data-ttu-id="53208-159">Vero</span><span class="sxs-lookup"><span data-stu-id="53208-159">True</span></span>                            |
| <span data-ttu-id="53208-160">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="53208-160">Is-Single-Valued</span></span>       | <span data-ttu-id="53208-161">Falso</span><span class="sxs-lookup"><span data-stu-id="53208-161">False</span></span>                           |
| <span data-ttu-id="53208-162">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="53208-162">Is Indexed</span></span>             | <span data-ttu-id="53208-163">Falso</span><span class="sxs-lookup"><span data-stu-id="53208-163">False</span></span>                           |
| <span data-ttu-id="53208-164">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="53208-164">In Global Catalog</span></span>      | <span data-ttu-id="53208-165">Vero</span><span class="sxs-lookup"><span data-stu-id="53208-165">True</span></span>                            |
| <span data-ttu-id="53208-166">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="53208-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="53208-167">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="53208-167">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="53208-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="53208-168">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="53208-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="53208-169">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="53208-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="53208-170">Search-Flags</span></span>           | <span data-ttu-id="53208-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="53208-171">0x00000000</span></span>                      |
| <span data-ttu-id="53208-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="53208-172">System-Flags</span></span>           | <span data-ttu-id="53208-173">0x00000013</span><span class="sxs-lookup"><span data-stu-id="53208-173">0x00000013</span></span>                      |
| <span data-ttu-id="53208-174">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="53208-174">Classes used in</span></span>        | [<span data-ttu-id="53208-175">**In alto**</span><span class="sxs-lookup"><span data-stu-id="53208-175">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="53208-176">ADAM</span><span class="sxs-lookup"><span data-stu-id="53208-176">ADAM</span></span>



| <span data-ttu-id="53208-177">Voce</span><span class="sxs-lookup"><span data-stu-id="53208-177">Entry</span></span> | <span data-ttu-id="53208-178">Valore</span><span class="sxs-lookup"><span data-stu-id="53208-178">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="53208-179">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="53208-179">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="53208-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="53208-180">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="53208-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="53208-181">System-Only</span></span>            | <span data-ttu-id="53208-182">Vero</span><span class="sxs-lookup"><span data-stu-id="53208-182">True</span></span>                            |
| <span data-ttu-id="53208-183">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="53208-183">Is-Single-Valued</span></span>       | <span data-ttu-id="53208-184">Falso</span><span class="sxs-lookup"><span data-stu-id="53208-184">False</span></span>                           |
| <span data-ttu-id="53208-185">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="53208-185">Is Indexed</span></span>             | <span data-ttu-id="53208-186">Falso</span><span class="sxs-lookup"><span data-stu-id="53208-186">False</span></span>                           |
| <span data-ttu-id="53208-187">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="53208-187">In Global Catalog</span></span>      | <span data-ttu-id="53208-188">Vero</span><span class="sxs-lookup"><span data-stu-id="53208-188">True</span></span>                            |
| <span data-ttu-id="53208-189">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="53208-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="53208-190">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="53208-190">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="53208-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="53208-191">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="53208-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="53208-192">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="53208-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="53208-193">Search-Flags</span></span>           | <span data-ttu-id="53208-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="53208-194">0x00000000</span></span>                      |
| <span data-ttu-id="53208-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="53208-195">System-Flags</span></span>           | <span data-ttu-id="53208-196">0x00000013</span><span class="sxs-lookup"><span data-stu-id="53208-196">0x00000013</span></span>                      |
| <span data-ttu-id="53208-197">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="53208-197">Classes used in</span></span>        | [<span data-ttu-id="53208-198">**In alto**</span><span class="sxs-lookup"><span data-stu-id="53208-198">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="53208-199">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="53208-199">Windows Server 2003 R2</span></span>



| <span data-ttu-id="53208-200">Voce</span><span class="sxs-lookup"><span data-stu-id="53208-200">Entry</span></span> | <span data-ttu-id="53208-201">Valore</span><span class="sxs-lookup"><span data-stu-id="53208-201">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="53208-202">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="53208-202">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="53208-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="53208-203">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="53208-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="53208-204">System-Only</span></span>            | <span data-ttu-id="53208-205">Vero</span><span class="sxs-lookup"><span data-stu-id="53208-205">True</span></span>                            |
| <span data-ttu-id="53208-206">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="53208-206">Is-Single-Valued</span></span>       | <span data-ttu-id="53208-207">Falso</span><span class="sxs-lookup"><span data-stu-id="53208-207">False</span></span>                           |
| <span data-ttu-id="53208-208">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="53208-208">Is Indexed</span></span>             | <span data-ttu-id="53208-209">Falso</span><span class="sxs-lookup"><span data-stu-id="53208-209">False</span></span>                           |
| <span data-ttu-id="53208-210">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="53208-210">In Global Catalog</span></span>      | <span data-ttu-id="53208-211">Vero</span><span class="sxs-lookup"><span data-stu-id="53208-211">True</span></span>                            |
| <span data-ttu-id="53208-212">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="53208-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="53208-213">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="53208-213">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="53208-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="53208-214">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="53208-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="53208-215">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="53208-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="53208-216">Search-Flags</span></span>           | <span data-ttu-id="53208-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="53208-217">0x00000000</span></span>                      |
| <span data-ttu-id="53208-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="53208-218">System-Flags</span></span>           | <span data-ttu-id="53208-219">0x00000013</span><span class="sxs-lookup"><span data-stu-id="53208-219">0x00000013</span></span>                      |
| <span data-ttu-id="53208-220">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="53208-220">Classes used in</span></span>        | [<span data-ttu-id="53208-221">**In alto**</span><span class="sxs-lookup"><span data-stu-id="53208-221">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="53208-222">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="53208-222">Windows Server 2008</span></span>



| <span data-ttu-id="53208-223">Voce</span><span class="sxs-lookup"><span data-stu-id="53208-223">Entry</span></span> | <span data-ttu-id="53208-224">Valore</span><span class="sxs-lookup"><span data-stu-id="53208-224">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="53208-225">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="53208-225">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="53208-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="53208-226">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="53208-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="53208-227">System-Only</span></span>            | <span data-ttu-id="53208-228">Vero</span><span class="sxs-lookup"><span data-stu-id="53208-228">True</span></span>                            |
| <span data-ttu-id="53208-229">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="53208-229">Is-Single-Valued</span></span>       | <span data-ttu-id="53208-230">Falso</span><span class="sxs-lookup"><span data-stu-id="53208-230">False</span></span>                           |
| <span data-ttu-id="53208-231">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="53208-231">Is Indexed</span></span>             | <span data-ttu-id="53208-232">Falso</span><span class="sxs-lookup"><span data-stu-id="53208-232">False</span></span>                           |
| <span data-ttu-id="53208-233">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="53208-233">In Global Catalog</span></span>      | <span data-ttu-id="53208-234">Vero</span><span class="sxs-lookup"><span data-stu-id="53208-234">True</span></span>                            |
| <span data-ttu-id="53208-235">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="53208-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="53208-236">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="53208-236">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="53208-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="53208-237">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="53208-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="53208-238">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="53208-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="53208-239">Search-Flags</span></span>           | <span data-ttu-id="53208-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="53208-240">0x00000000</span></span>                      |
| <span data-ttu-id="53208-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="53208-241">System-Flags</span></span>           | <span data-ttu-id="53208-242">0x00000013</span><span class="sxs-lookup"><span data-stu-id="53208-242">0x00000013</span></span>                      |
| <span data-ttu-id="53208-243">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="53208-243">Classes used in</span></span>        | [<span data-ttu-id="53208-244">**In alto**</span><span class="sxs-lookup"><span data-stu-id="53208-244">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="53208-245">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="53208-245">Windows Server 2008 R2</span></span>



| <span data-ttu-id="53208-246">Voce</span><span class="sxs-lookup"><span data-stu-id="53208-246">Entry</span></span> | <span data-ttu-id="53208-247">Valore</span><span class="sxs-lookup"><span data-stu-id="53208-247">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="53208-248">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="53208-248">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="53208-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="53208-249">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="53208-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="53208-250">System-Only</span></span>            | <span data-ttu-id="53208-251">Vero</span><span class="sxs-lookup"><span data-stu-id="53208-251">True</span></span>                            |
| <span data-ttu-id="53208-252">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="53208-252">Is-Single-Valued</span></span>       | <span data-ttu-id="53208-253">Falso</span><span class="sxs-lookup"><span data-stu-id="53208-253">False</span></span>                           |
| <span data-ttu-id="53208-254">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="53208-254">Is Indexed</span></span>             | <span data-ttu-id="53208-255">Falso</span><span class="sxs-lookup"><span data-stu-id="53208-255">False</span></span>                           |
| <span data-ttu-id="53208-256">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="53208-256">In Global Catalog</span></span>      | <span data-ttu-id="53208-257">Vero</span><span class="sxs-lookup"><span data-stu-id="53208-257">True</span></span>                            |
| <span data-ttu-id="53208-258">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="53208-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="53208-259">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="53208-259">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="53208-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="53208-260">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="53208-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="53208-261">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="53208-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="53208-262">Search-Flags</span></span>           | <span data-ttu-id="53208-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="53208-263">0x00000000</span></span>                      |
| <span data-ttu-id="53208-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="53208-264">System-Flags</span></span>           | <span data-ttu-id="53208-265">0x00000013</span><span class="sxs-lookup"><span data-stu-id="53208-265">0x00000013</span></span>                      |
| <span data-ttu-id="53208-266">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="53208-266">Classes used in</span></span>        | [<span data-ttu-id="53208-267">**In alto**</span><span class="sxs-lookup"><span data-stu-id="53208-267">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="53208-268">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="53208-268">Windows Server 2012</span></span>



| <span data-ttu-id="53208-269">Voce</span><span class="sxs-lookup"><span data-stu-id="53208-269">Entry</span></span> | <span data-ttu-id="53208-270">Valore</span><span class="sxs-lookup"><span data-stu-id="53208-270">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="53208-271">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="53208-271">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="53208-272">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="53208-272">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="53208-273">System-Only</span><span class="sxs-lookup"><span data-stu-id="53208-273">System-Only</span></span>            | <span data-ttu-id="53208-274">Vero</span><span class="sxs-lookup"><span data-stu-id="53208-274">True</span></span>                            |
| <span data-ttu-id="53208-275">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="53208-275">Is-Single-Valued</span></span>       | <span data-ttu-id="53208-276">Falso</span><span class="sxs-lookup"><span data-stu-id="53208-276">False</span></span>                           |
| <span data-ttu-id="53208-277">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="53208-277">Is Indexed</span></span>             | <span data-ttu-id="53208-278">Falso</span><span class="sxs-lookup"><span data-stu-id="53208-278">False</span></span>                           |
| <span data-ttu-id="53208-279">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="53208-279">In Global Catalog</span></span>      | <span data-ttu-id="53208-280">Vero</span><span class="sxs-lookup"><span data-stu-id="53208-280">True</span></span>                            |
| <span data-ttu-id="53208-281">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="53208-281">NT-Security-Descriptor</span></span> | <span data-ttu-id="53208-282">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="53208-282">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="53208-283">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="53208-283">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="53208-284">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="53208-284">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="53208-285">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="53208-285">Search-Flags</span></span>           | <span data-ttu-id="53208-286">0x00000000</span><span class="sxs-lookup"><span data-stu-id="53208-286">0x00000000</span></span>                      |
| <span data-ttu-id="53208-287">System-Flags</span><span class="sxs-lookup"><span data-stu-id="53208-287">System-Flags</span></span>           | <span data-ttu-id="53208-288">0x00000013</span><span class="sxs-lookup"><span data-stu-id="53208-288">0x00000013</span></span>                      |
| <span data-ttu-id="53208-289">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="53208-289">Classes used in</span></span>        | [<span data-ttu-id="53208-290">**In alto**</span><span class="sxs-lookup"><span data-stu-id="53208-290">**Top**</span></span>](c-top.md)<br/> |



 

 





