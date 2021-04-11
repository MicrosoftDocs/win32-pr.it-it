---
title: attributo ms-DS-NC-REPL-Cursors
description: Un elenco di partner di replica precedenti e presenti e il modo in cui vengono aggiornati.
ms.assetid: febe8614-b68a-4001-b6ae-dae3fe6eb25f
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo ms-DS-NC-REPL-Cursors
- attributo msDS-NCReplCursors-schema AD
topic_type:
- apiref
api_name:
- ms-DS-NC-Repl-Cursors
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 555a09520079df624fffb2cb3cb3aa34b81502c2
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104122518"
---
# <a name="ms-ds-nc-repl-cursors-attribute"></a><span data-ttu-id="05bcb-105">attributo ms-DS-NC-REPL-Cursors</span><span class="sxs-lookup"><span data-stu-id="05bcb-105">ms-DS-NC-Repl-Cursors attribute</span></span>

<span data-ttu-id="05bcb-106">Un elenco di partner di replica precedenti e presenti e il modo in cui vengono aggiornati.</span><span class="sxs-lookup"><span data-stu-id="05bcb-106">A list of past and present replication partners, and how current we are with each of them.</span></span>



| <span data-ttu-id="05bcb-107">Voce</span><span class="sxs-lookup"><span data-stu-id="05bcb-107">Entry</span></span> | <span data-ttu-id="05bcb-108">Valore</span><span class="sxs-lookup"><span data-stu-id="05bcb-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="05bcb-109">CN</span><span class="sxs-lookup"><span data-stu-id="05bcb-109">CN</span></span>                | <span data-ttu-id="05bcb-110">ms-DS-NC-REPL-cursori</span><span class="sxs-lookup"><span data-stu-id="05bcb-110">ms-DS-NC-Repl-Cursors</span></span>                       |
| <span data-ttu-id="05bcb-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="05bcb-111">Ldap-Display-Name</span></span> | <span data-ttu-id="05bcb-112">msDS-NCReplCursors</span><span class="sxs-lookup"><span data-stu-id="05bcb-112">msDS-NCReplCursors</span></span>                          |
| <span data-ttu-id="05bcb-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="05bcb-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="05bcb-114">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="05bcb-114">Update Privilege</span></span>  | <span data-ttu-id="05bcb-115">Questo valore viene impostato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="05bcb-115">This value is set by the system.</span></span>            |
| <span data-ttu-id="05bcb-116">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="05bcb-116">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="05bcb-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="05bcb-117">Attribute-Id</span></span>      | <span data-ttu-id="05bcb-118">1.2.840.113556.1.4.1704</span><span class="sxs-lookup"><span data-stu-id="05bcb-118">1.2.840.113556.1.4.1704</span></span>                     |
| <span data-ttu-id="05bcb-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="05bcb-119">System-Id-Guid</span></span>    | <span data-ttu-id="05bcb-120">8a167ce4-f9e8-47eb-8d78-f7fe80abb2cc</span><span class="sxs-lookup"><span data-stu-id="05bcb-120">8a167ce4-f9e8-47eb-8d78-f7fe80abb2cc</span></span>        |
| <span data-ttu-id="05bcb-121">Sintassi</span><span class="sxs-lookup"><span data-stu-id="05bcb-121">Syntax</span></span>            | [<span data-ttu-id="05bcb-122">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="05bcb-122">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="05bcb-123">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="05bcb-123">Implementations</span></span>

-   [<span data-ttu-id="05bcb-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="05bcb-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="05bcb-125">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="05bcb-125">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="05bcb-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="05bcb-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="05bcb-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="05bcb-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="05bcb-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="05bcb-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="05bcb-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="05bcb-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="05bcb-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="05bcb-130">Windows Server 2003</span></span>



| <span data-ttu-id="05bcb-131">Voce</span><span class="sxs-lookup"><span data-stu-id="05bcb-131">Entry</span></span> | <span data-ttu-id="05bcb-132">Valore</span><span class="sxs-lookup"><span data-stu-id="05bcb-132">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="05bcb-133">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="05bcb-133">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="05bcb-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="05bcb-134">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="05bcb-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="05bcb-135">System-Only</span></span>            | <span data-ttu-id="05bcb-136">Falso</span><span class="sxs-lookup"><span data-stu-id="05bcb-136">False</span></span>                           |
| <span data-ttu-id="05bcb-137">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="05bcb-137">Is-Single-Valued</span></span>       | <span data-ttu-id="05bcb-138">Falso</span><span class="sxs-lookup"><span data-stu-id="05bcb-138">False</span></span>                           |
| <span data-ttu-id="05bcb-139">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="05bcb-139">Is Indexed</span></span>             | <span data-ttu-id="05bcb-140">Falso</span><span class="sxs-lookup"><span data-stu-id="05bcb-140">False</span></span>                           |
| <span data-ttu-id="05bcb-141">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="05bcb-141">In Global Catalog</span></span>      | <span data-ttu-id="05bcb-142">Falso</span><span class="sxs-lookup"><span data-stu-id="05bcb-142">False</span></span>                           |
| <span data-ttu-id="05bcb-143">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="05bcb-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="05bcb-144">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="05bcb-144">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="05bcb-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="05bcb-145">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="05bcb-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="05bcb-146">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="05bcb-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="05bcb-147">Search-Flags</span></span>           | <span data-ttu-id="05bcb-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="05bcb-148">0x00000000</span></span>                      |
| <span data-ttu-id="05bcb-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="05bcb-149">System-Flags</span></span>           | <span data-ttu-id="05bcb-150">0x00000014</span><span class="sxs-lookup"><span data-stu-id="05bcb-150">0x00000014</span></span>                      |
| <span data-ttu-id="05bcb-151">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="05bcb-151">Classes used in</span></span>        | [<span data-ttu-id="05bcb-152">**In alto**</span><span class="sxs-lookup"><span data-stu-id="05bcb-152">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="05bcb-153">ADAM</span><span class="sxs-lookup"><span data-stu-id="05bcb-153">ADAM</span></span>



| <span data-ttu-id="05bcb-154">Voce</span><span class="sxs-lookup"><span data-stu-id="05bcb-154">Entry</span></span> | <span data-ttu-id="05bcb-155">Valore</span><span class="sxs-lookup"><span data-stu-id="05bcb-155">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="05bcb-156">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="05bcb-156">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="05bcb-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="05bcb-157">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="05bcb-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="05bcb-158">System-Only</span></span>            | <span data-ttu-id="05bcb-159">Falso</span><span class="sxs-lookup"><span data-stu-id="05bcb-159">False</span></span>                           |
| <span data-ttu-id="05bcb-160">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="05bcb-160">Is-Single-Valued</span></span>       | <span data-ttu-id="05bcb-161">Falso</span><span class="sxs-lookup"><span data-stu-id="05bcb-161">False</span></span>                           |
| <span data-ttu-id="05bcb-162">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="05bcb-162">Is Indexed</span></span>             | <span data-ttu-id="05bcb-163">Falso</span><span class="sxs-lookup"><span data-stu-id="05bcb-163">False</span></span>                           |
| <span data-ttu-id="05bcb-164">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="05bcb-164">In Global Catalog</span></span>      | <span data-ttu-id="05bcb-165">Falso</span><span class="sxs-lookup"><span data-stu-id="05bcb-165">False</span></span>                           |
| <span data-ttu-id="05bcb-166">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="05bcb-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="05bcb-167">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="05bcb-167">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="05bcb-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="05bcb-168">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="05bcb-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="05bcb-169">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="05bcb-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="05bcb-170">Search-Flags</span></span>           | <span data-ttu-id="05bcb-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="05bcb-171">0x00000000</span></span>                      |
| <span data-ttu-id="05bcb-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="05bcb-172">System-Flags</span></span>           | <span data-ttu-id="05bcb-173">0x00000014</span><span class="sxs-lookup"><span data-stu-id="05bcb-173">0x00000014</span></span>                      |
| <span data-ttu-id="05bcb-174">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="05bcb-174">Classes used in</span></span>        | [<span data-ttu-id="05bcb-175">**In alto**</span><span class="sxs-lookup"><span data-stu-id="05bcb-175">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="05bcb-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="05bcb-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="05bcb-177">Voce</span><span class="sxs-lookup"><span data-stu-id="05bcb-177">Entry</span></span> | <span data-ttu-id="05bcb-178">Valore</span><span class="sxs-lookup"><span data-stu-id="05bcb-178">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="05bcb-179">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="05bcb-179">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="05bcb-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="05bcb-180">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="05bcb-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="05bcb-181">System-Only</span></span>            | <span data-ttu-id="05bcb-182">Falso</span><span class="sxs-lookup"><span data-stu-id="05bcb-182">False</span></span>                           |
| <span data-ttu-id="05bcb-183">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="05bcb-183">Is-Single-Valued</span></span>       | <span data-ttu-id="05bcb-184">Falso</span><span class="sxs-lookup"><span data-stu-id="05bcb-184">False</span></span>                           |
| <span data-ttu-id="05bcb-185">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="05bcb-185">Is Indexed</span></span>             | <span data-ttu-id="05bcb-186">Falso</span><span class="sxs-lookup"><span data-stu-id="05bcb-186">False</span></span>                           |
| <span data-ttu-id="05bcb-187">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="05bcb-187">In Global Catalog</span></span>      | <span data-ttu-id="05bcb-188">Falso</span><span class="sxs-lookup"><span data-stu-id="05bcb-188">False</span></span>                           |
| <span data-ttu-id="05bcb-189">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="05bcb-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="05bcb-190">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="05bcb-190">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="05bcb-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="05bcb-191">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="05bcb-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="05bcb-192">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="05bcb-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="05bcb-193">Search-Flags</span></span>           | <span data-ttu-id="05bcb-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="05bcb-194">0x00000000</span></span>                      |
| <span data-ttu-id="05bcb-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="05bcb-195">System-Flags</span></span>           | <span data-ttu-id="05bcb-196">0x00000014</span><span class="sxs-lookup"><span data-stu-id="05bcb-196">0x00000014</span></span>                      |
| <span data-ttu-id="05bcb-197">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="05bcb-197">Classes used in</span></span>        | [<span data-ttu-id="05bcb-198">**In alto**</span><span class="sxs-lookup"><span data-stu-id="05bcb-198">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="05bcb-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="05bcb-199">Windows Server 2008</span></span>



| <span data-ttu-id="05bcb-200">Voce</span><span class="sxs-lookup"><span data-stu-id="05bcb-200">Entry</span></span> | <span data-ttu-id="05bcb-201">Valore</span><span class="sxs-lookup"><span data-stu-id="05bcb-201">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="05bcb-202">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="05bcb-202">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="05bcb-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="05bcb-203">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="05bcb-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="05bcb-204">System-Only</span></span>            | <span data-ttu-id="05bcb-205">Falso</span><span class="sxs-lookup"><span data-stu-id="05bcb-205">False</span></span>                           |
| <span data-ttu-id="05bcb-206">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="05bcb-206">Is-Single-Valued</span></span>       | <span data-ttu-id="05bcb-207">Falso</span><span class="sxs-lookup"><span data-stu-id="05bcb-207">False</span></span>                           |
| <span data-ttu-id="05bcb-208">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="05bcb-208">Is Indexed</span></span>             | <span data-ttu-id="05bcb-209">Falso</span><span class="sxs-lookup"><span data-stu-id="05bcb-209">False</span></span>                           |
| <span data-ttu-id="05bcb-210">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="05bcb-210">In Global Catalog</span></span>      | <span data-ttu-id="05bcb-211">Falso</span><span class="sxs-lookup"><span data-stu-id="05bcb-211">False</span></span>                           |
| <span data-ttu-id="05bcb-212">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="05bcb-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="05bcb-213">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="05bcb-213">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="05bcb-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="05bcb-214">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="05bcb-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="05bcb-215">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="05bcb-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="05bcb-216">Search-Flags</span></span>           | <span data-ttu-id="05bcb-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="05bcb-217">0x00000000</span></span>                      |
| <span data-ttu-id="05bcb-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="05bcb-218">System-Flags</span></span>           | <span data-ttu-id="05bcb-219">0x00000014</span><span class="sxs-lookup"><span data-stu-id="05bcb-219">0x00000014</span></span>                      |
| <span data-ttu-id="05bcb-220">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="05bcb-220">Classes used in</span></span>        | [<span data-ttu-id="05bcb-221">**In alto**</span><span class="sxs-lookup"><span data-stu-id="05bcb-221">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="05bcb-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="05bcb-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="05bcb-223">Voce</span><span class="sxs-lookup"><span data-stu-id="05bcb-223">Entry</span></span> | <span data-ttu-id="05bcb-224">Valore</span><span class="sxs-lookup"><span data-stu-id="05bcb-224">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="05bcb-225">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="05bcb-225">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="05bcb-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="05bcb-226">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="05bcb-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="05bcb-227">System-Only</span></span>            | <span data-ttu-id="05bcb-228">Falso</span><span class="sxs-lookup"><span data-stu-id="05bcb-228">False</span></span>                           |
| <span data-ttu-id="05bcb-229">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="05bcb-229">Is-Single-Valued</span></span>       | <span data-ttu-id="05bcb-230">Falso</span><span class="sxs-lookup"><span data-stu-id="05bcb-230">False</span></span>                           |
| <span data-ttu-id="05bcb-231">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="05bcb-231">Is Indexed</span></span>             | <span data-ttu-id="05bcb-232">Falso</span><span class="sxs-lookup"><span data-stu-id="05bcb-232">False</span></span>                           |
| <span data-ttu-id="05bcb-233">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="05bcb-233">In Global Catalog</span></span>      | <span data-ttu-id="05bcb-234">Falso</span><span class="sxs-lookup"><span data-stu-id="05bcb-234">False</span></span>                           |
| <span data-ttu-id="05bcb-235">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="05bcb-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="05bcb-236">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="05bcb-236">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="05bcb-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="05bcb-237">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="05bcb-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="05bcb-238">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="05bcb-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="05bcb-239">Search-Flags</span></span>           | <span data-ttu-id="05bcb-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="05bcb-240">0x00000000</span></span>                      |
| <span data-ttu-id="05bcb-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="05bcb-241">System-Flags</span></span>           | <span data-ttu-id="05bcb-242">0x00000014</span><span class="sxs-lookup"><span data-stu-id="05bcb-242">0x00000014</span></span>                      |
| <span data-ttu-id="05bcb-243">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="05bcb-243">Classes used in</span></span>        | [<span data-ttu-id="05bcb-244">**In alto**</span><span class="sxs-lookup"><span data-stu-id="05bcb-244">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="05bcb-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="05bcb-245">Windows Server 2012</span></span>



| <span data-ttu-id="05bcb-246">Voce</span><span class="sxs-lookup"><span data-stu-id="05bcb-246">Entry</span></span> | <span data-ttu-id="05bcb-247">Valore</span><span class="sxs-lookup"><span data-stu-id="05bcb-247">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="05bcb-248">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="05bcb-248">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="05bcb-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="05bcb-249">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="05bcb-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="05bcb-250">System-Only</span></span>            | <span data-ttu-id="05bcb-251">Falso</span><span class="sxs-lookup"><span data-stu-id="05bcb-251">False</span></span>                           |
| <span data-ttu-id="05bcb-252">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="05bcb-252">Is-Single-Valued</span></span>       | <span data-ttu-id="05bcb-253">Falso</span><span class="sxs-lookup"><span data-stu-id="05bcb-253">False</span></span>                           |
| <span data-ttu-id="05bcb-254">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="05bcb-254">Is Indexed</span></span>             | <span data-ttu-id="05bcb-255">Falso</span><span class="sxs-lookup"><span data-stu-id="05bcb-255">False</span></span>                           |
| <span data-ttu-id="05bcb-256">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="05bcb-256">In Global Catalog</span></span>      | <span data-ttu-id="05bcb-257">Falso</span><span class="sxs-lookup"><span data-stu-id="05bcb-257">False</span></span>                           |
| <span data-ttu-id="05bcb-258">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="05bcb-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="05bcb-259">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="05bcb-259">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="05bcb-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="05bcb-260">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="05bcb-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="05bcb-261">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="05bcb-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="05bcb-262">Search-Flags</span></span>           | <span data-ttu-id="05bcb-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="05bcb-263">0x00000000</span></span>                      |
| <span data-ttu-id="05bcb-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="05bcb-264">System-Flags</span></span>           | <span data-ttu-id="05bcb-265">0x00000014</span><span class="sxs-lookup"><span data-stu-id="05bcb-265">0x00000014</span></span>                      |
| <span data-ttu-id="05bcb-266">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="05bcb-266">Classes used in</span></span>        | [<span data-ttu-id="05bcb-267">**In alto**</span><span class="sxs-lookup"><span data-stu-id="05bcb-267">**Top**</span></span>](c-top.md)<br/> |



 

 





