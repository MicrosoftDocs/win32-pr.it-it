---
title: Attributo PKT
description: Tabella delle informazioni sulle partizioni DFS. Descrive la struttura di una gerarchia di file system distribuito.
ms.assetid: a7b2e9ee-04c0-40e8-8670-8261575a45ab
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo PKT
- Schema AD dell'attributo pKT
topic_type:
- apiref
api_name:
- PKT
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1647e2730b254121763b6598a8ec365b376dd52d
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104121990"
---
# <a name="pkt-attribute"></a><span data-ttu-id="08625-106">Attributo PKT</span><span class="sxs-lookup"><span data-stu-id="08625-106">PKT attribute</span></span>

<span data-ttu-id="08625-107">Tabella delle informazioni sulle partizioni DFS.</span><span class="sxs-lookup"><span data-stu-id="08625-107">DFS Partition Knowledge Table.</span></span> <span data-ttu-id="08625-108">Descrive la struttura di una gerarchia di file system distribuito.</span><span class="sxs-lookup"><span data-stu-id="08625-108">Describes the structure of a Distributed File System hierarchy.</span></span>



| <span data-ttu-id="08625-109">Voce</span><span class="sxs-lookup"><span data-stu-id="08625-109">Entry</span></span> | <span data-ttu-id="08625-110">Valore</span><span class="sxs-lookup"><span data-stu-id="08625-110">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="08625-111">CN</span><span class="sxs-lookup"><span data-stu-id="08625-111">CN</span></span>                | <span data-ttu-id="08625-112">PKT</span><span class="sxs-lookup"><span data-stu-id="08625-112">PKT</span></span>                                                   |
| <span data-ttu-id="08625-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="08625-113">Ldap-Display-Name</span></span> | <span data-ttu-id="08625-114">pKT</span><span class="sxs-lookup"><span data-stu-id="08625-114">pKT</span></span>                                                   |
| <span data-ttu-id="08625-115">Dimensione</span><span class="sxs-lookup"><span data-stu-id="08625-115">Size</span></span>              | \-                                                    |
| <span data-ttu-id="08625-116">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="08625-116">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="08625-117">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="08625-117">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="08625-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="08625-118">Attribute-Id</span></span>      | <span data-ttu-id="08625-119">1.2.840.113556.1.4.206</span><span class="sxs-lookup"><span data-stu-id="08625-119">1.2.840.113556.1.4.206</span></span>                                |
| <span data-ttu-id="08625-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="08625-120">System-Id-Guid</span></span>    | <span data-ttu-id="08625-121">8447f9f1-1027-11d0-a05f-00aa006c33ed</span><span class="sxs-lookup"><span data-stu-id="08625-121">8447f9f1-1027-11d0-a05f-00aa006c33ed</span></span>                  |
| <span data-ttu-id="08625-122">Sintassi</span><span class="sxs-lookup"><span data-stu-id="08625-122">Syntax</span></span>            | [<span data-ttu-id="08625-123">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="08625-123">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="08625-124">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="08625-124">Implementations</span></span>

-   [<span data-ttu-id="08625-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="08625-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="08625-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="08625-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="08625-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="08625-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="08625-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="08625-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="08625-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="08625-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="08625-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="08625-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="08625-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="08625-131">Windows 2000 Server</span></span>



| <span data-ttu-id="08625-132">Voce</span><span class="sxs-lookup"><span data-stu-id="08625-132">Entry</span></span> | <span data-ttu-id="08625-133">Valore</span><span class="sxs-lookup"><span data-stu-id="08625-133">Value</span></span> |
|------------------------|--------------------------------------|
| <span data-ttu-id="08625-134">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="08625-134">Link-Id</span></span>                | \-                                   |
| <span data-ttu-id="08625-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="08625-135">MAPI-Id</span></span>                | \-                                   |
| <span data-ttu-id="08625-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="08625-136">System-Only</span></span>            | <span data-ttu-id="08625-137">Falso</span><span class="sxs-lookup"><span data-stu-id="08625-137">False</span></span>                                |
| <span data-ttu-id="08625-138">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="08625-138">Is-Single-Valued</span></span>       | <span data-ttu-id="08625-139">Vero</span><span class="sxs-lookup"><span data-stu-id="08625-139">True</span></span>                                 |
| <span data-ttu-id="08625-140">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="08625-140">Is Indexed</span></span>             | <span data-ttu-id="08625-141">Falso</span><span class="sxs-lookup"><span data-stu-id="08625-141">False</span></span>                                |
| <span data-ttu-id="08625-142">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="08625-142">In Global Catalog</span></span>      | <span data-ttu-id="08625-143">Falso</span><span class="sxs-lookup"><span data-stu-id="08625-143">False</span></span>                                |
| <span data-ttu-id="08625-144">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="08625-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="08625-145">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="08625-145">O:BAG:BAD:S:</span></span>                         |
| <span data-ttu-id="08625-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="08625-146">Range-Lower</span></span>            | \-                                   |
| <span data-ttu-id="08625-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="08625-147">Range-Upper</span></span>            | \-                                   |
| <span data-ttu-id="08625-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="08625-148">Search-Flags</span></span>           | <span data-ttu-id="08625-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="08625-149">0x00000000</span></span>                           |
| <span data-ttu-id="08625-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="08625-150">System-Flags</span></span>           | <span data-ttu-id="08625-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="08625-151">0x00000010</span></span>                           |
| <span data-ttu-id="08625-152">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="08625-152">Classes used in</span></span>        | [<span data-ttu-id="08625-153">**FT-DFS**</span><span class="sxs-lookup"><span data-stu-id="08625-153">**FT-Dfs**</span></span>](c-ftdfs.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="08625-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="08625-154">Windows Server 2003</span></span>



| <span data-ttu-id="08625-155">Voce</span><span class="sxs-lookup"><span data-stu-id="08625-155">Entry</span></span> | <span data-ttu-id="08625-156">Valore</span><span class="sxs-lookup"><span data-stu-id="08625-156">Value</span></span> |
|------------------------|--------------------------------------|
| <span data-ttu-id="08625-157">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="08625-157">Link-Id</span></span>                | \-                                   |
| <span data-ttu-id="08625-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="08625-158">MAPI-Id</span></span>                | \-                                   |
| <span data-ttu-id="08625-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="08625-159">System-Only</span></span>            | <span data-ttu-id="08625-160">Falso</span><span class="sxs-lookup"><span data-stu-id="08625-160">False</span></span>                                |
| <span data-ttu-id="08625-161">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="08625-161">Is-Single-Valued</span></span>       | <span data-ttu-id="08625-162">Vero</span><span class="sxs-lookup"><span data-stu-id="08625-162">True</span></span>                                 |
| <span data-ttu-id="08625-163">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="08625-163">Is Indexed</span></span>             | <span data-ttu-id="08625-164">Falso</span><span class="sxs-lookup"><span data-stu-id="08625-164">False</span></span>                                |
| <span data-ttu-id="08625-165">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="08625-165">In Global Catalog</span></span>      | <span data-ttu-id="08625-166">Falso</span><span class="sxs-lookup"><span data-stu-id="08625-166">False</span></span>                                |
| <span data-ttu-id="08625-167">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="08625-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="08625-168">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="08625-168">O:BAG:BAD:S:</span></span>                         |
| <span data-ttu-id="08625-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="08625-169">Range-Lower</span></span>            | \-                                   |
| <span data-ttu-id="08625-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="08625-170">Range-Upper</span></span>            | \-                                   |
| <span data-ttu-id="08625-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="08625-171">Search-Flags</span></span>           | <span data-ttu-id="08625-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="08625-172">0x00000000</span></span>                           |
| <span data-ttu-id="08625-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="08625-173">System-Flags</span></span>           | <span data-ttu-id="08625-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="08625-174">0x00000010</span></span>                           |
| <span data-ttu-id="08625-175">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="08625-175">Classes used in</span></span>        | [<span data-ttu-id="08625-176">**FT-DFS**</span><span class="sxs-lookup"><span data-stu-id="08625-176">**FT-Dfs**</span></span>](c-ftdfs.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="08625-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="08625-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="08625-178">Voce</span><span class="sxs-lookup"><span data-stu-id="08625-178">Entry</span></span> | <span data-ttu-id="08625-179">Valore</span><span class="sxs-lookup"><span data-stu-id="08625-179">Value</span></span> |
|------------------------|--------------------------------------|
| <span data-ttu-id="08625-180">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="08625-180">Link-Id</span></span>                | \-                                   |
| <span data-ttu-id="08625-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="08625-181">MAPI-Id</span></span>                | \-                                   |
| <span data-ttu-id="08625-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="08625-182">System-Only</span></span>            | <span data-ttu-id="08625-183">Falso</span><span class="sxs-lookup"><span data-stu-id="08625-183">False</span></span>                                |
| <span data-ttu-id="08625-184">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="08625-184">Is-Single-Valued</span></span>       | <span data-ttu-id="08625-185">Vero</span><span class="sxs-lookup"><span data-stu-id="08625-185">True</span></span>                                 |
| <span data-ttu-id="08625-186">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="08625-186">Is Indexed</span></span>             | <span data-ttu-id="08625-187">Falso</span><span class="sxs-lookup"><span data-stu-id="08625-187">False</span></span>                                |
| <span data-ttu-id="08625-188">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="08625-188">In Global Catalog</span></span>      | <span data-ttu-id="08625-189">Falso</span><span class="sxs-lookup"><span data-stu-id="08625-189">False</span></span>                                |
| <span data-ttu-id="08625-190">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="08625-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="08625-191">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="08625-191">O:BAG:BAD:S:</span></span>                         |
| <span data-ttu-id="08625-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="08625-192">Range-Lower</span></span>            | \-                                   |
| <span data-ttu-id="08625-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="08625-193">Range-Upper</span></span>            | \-                                   |
| <span data-ttu-id="08625-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="08625-194">Search-Flags</span></span>           | <span data-ttu-id="08625-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="08625-195">0x00000000</span></span>                           |
| <span data-ttu-id="08625-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="08625-196">System-Flags</span></span>           | <span data-ttu-id="08625-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="08625-197">0x00000010</span></span>                           |
| <span data-ttu-id="08625-198">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="08625-198">Classes used in</span></span>        | [<span data-ttu-id="08625-199">**FT-DFS**</span><span class="sxs-lookup"><span data-stu-id="08625-199">**FT-Dfs**</span></span>](c-ftdfs.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="08625-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="08625-200">Windows Server 2008</span></span>



| <span data-ttu-id="08625-201">Voce</span><span class="sxs-lookup"><span data-stu-id="08625-201">Entry</span></span> | <span data-ttu-id="08625-202">Valore</span><span class="sxs-lookup"><span data-stu-id="08625-202">Value</span></span> |
|------------------------|--------------------------------------|
| <span data-ttu-id="08625-203">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="08625-203">Link-Id</span></span>                | \-                                   |
| <span data-ttu-id="08625-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="08625-204">MAPI-Id</span></span>                | \-                                   |
| <span data-ttu-id="08625-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="08625-205">System-Only</span></span>            | <span data-ttu-id="08625-206">Falso</span><span class="sxs-lookup"><span data-stu-id="08625-206">False</span></span>                                |
| <span data-ttu-id="08625-207">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="08625-207">Is-Single-Valued</span></span>       | <span data-ttu-id="08625-208">Vero</span><span class="sxs-lookup"><span data-stu-id="08625-208">True</span></span>                                 |
| <span data-ttu-id="08625-209">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="08625-209">Is Indexed</span></span>             | <span data-ttu-id="08625-210">Falso</span><span class="sxs-lookup"><span data-stu-id="08625-210">False</span></span>                                |
| <span data-ttu-id="08625-211">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="08625-211">In Global Catalog</span></span>      | <span data-ttu-id="08625-212">Falso</span><span class="sxs-lookup"><span data-stu-id="08625-212">False</span></span>                                |
| <span data-ttu-id="08625-213">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="08625-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="08625-214">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="08625-214">O:BAG:BAD:S:</span></span>                         |
| <span data-ttu-id="08625-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="08625-215">Range-Lower</span></span>            | \-                                   |
| <span data-ttu-id="08625-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="08625-216">Range-Upper</span></span>            | \-                                   |
| <span data-ttu-id="08625-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="08625-217">Search-Flags</span></span>           | <span data-ttu-id="08625-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="08625-218">0x00000000</span></span>                           |
| <span data-ttu-id="08625-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="08625-219">System-Flags</span></span>           | <span data-ttu-id="08625-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="08625-220">0x00000010</span></span>                           |
| <span data-ttu-id="08625-221">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="08625-221">Classes used in</span></span>        | [<span data-ttu-id="08625-222">**FT-DFS**</span><span class="sxs-lookup"><span data-stu-id="08625-222">**FT-Dfs**</span></span>](c-ftdfs.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="08625-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="08625-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="08625-224">Voce</span><span class="sxs-lookup"><span data-stu-id="08625-224">Entry</span></span> | <span data-ttu-id="08625-225">Valore</span><span class="sxs-lookup"><span data-stu-id="08625-225">Value</span></span> |
|------------------------|--------------------------------------|
| <span data-ttu-id="08625-226">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="08625-226">Link-Id</span></span>                | \-                                   |
| <span data-ttu-id="08625-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="08625-227">MAPI-Id</span></span>                | \-                                   |
| <span data-ttu-id="08625-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="08625-228">System-Only</span></span>            | <span data-ttu-id="08625-229">Falso</span><span class="sxs-lookup"><span data-stu-id="08625-229">False</span></span>                                |
| <span data-ttu-id="08625-230">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="08625-230">Is-Single-Valued</span></span>       | <span data-ttu-id="08625-231">Vero</span><span class="sxs-lookup"><span data-stu-id="08625-231">True</span></span>                                 |
| <span data-ttu-id="08625-232">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="08625-232">Is Indexed</span></span>             | <span data-ttu-id="08625-233">Falso</span><span class="sxs-lookup"><span data-stu-id="08625-233">False</span></span>                                |
| <span data-ttu-id="08625-234">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="08625-234">In Global Catalog</span></span>      | <span data-ttu-id="08625-235">Falso</span><span class="sxs-lookup"><span data-stu-id="08625-235">False</span></span>                                |
| <span data-ttu-id="08625-236">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="08625-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="08625-237">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="08625-237">O:BAG:BAD:S:</span></span>                         |
| <span data-ttu-id="08625-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="08625-238">Range-Lower</span></span>            | \-                                   |
| <span data-ttu-id="08625-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="08625-239">Range-Upper</span></span>            | \-                                   |
| <span data-ttu-id="08625-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="08625-240">Search-Flags</span></span>           | <span data-ttu-id="08625-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="08625-241">0x00000000</span></span>                           |
| <span data-ttu-id="08625-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="08625-242">System-Flags</span></span>           | <span data-ttu-id="08625-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="08625-243">0x00000010</span></span>                           |
| <span data-ttu-id="08625-244">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="08625-244">Classes used in</span></span>        | [<span data-ttu-id="08625-245">**FT-DFS**</span><span class="sxs-lookup"><span data-stu-id="08625-245">**FT-Dfs**</span></span>](c-ftdfs.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="08625-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="08625-246">Windows Server 2012</span></span>



| <span data-ttu-id="08625-247">Voce</span><span class="sxs-lookup"><span data-stu-id="08625-247">Entry</span></span> | <span data-ttu-id="08625-248">Valore</span><span class="sxs-lookup"><span data-stu-id="08625-248">Value</span></span> |
|------------------------|--------------------------------------|
| <span data-ttu-id="08625-249">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="08625-249">Link-Id</span></span>                | \-                                   |
| <span data-ttu-id="08625-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="08625-250">MAPI-Id</span></span>                | \-                                   |
| <span data-ttu-id="08625-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="08625-251">System-Only</span></span>            | <span data-ttu-id="08625-252">Falso</span><span class="sxs-lookup"><span data-stu-id="08625-252">False</span></span>                                |
| <span data-ttu-id="08625-253">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="08625-253">Is-Single-Valued</span></span>       | <span data-ttu-id="08625-254">Vero</span><span class="sxs-lookup"><span data-stu-id="08625-254">True</span></span>                                 |
| <span data-ttu-id="08625-255">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="08625-255">Is Indexed</span></span>             | <span data-ttu-id="08625-256">Falso</span><span class="sxs-lookup"><span data-stu-id="08625-256">False</span></span>                                |
| <span data-ttu-id="08625-257">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="08625-257">In Global Catalog</span></span>      | <span data-ttu-id="08625-258">Falso</span><span class="sxs-lookup"><span data-stu-id="08625-258">False</span></span>                                |
| <span data-ttu-id="08625-259">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="08625-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="08625-260">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="08625-260">O:BAG:BAD:S:</span></span>                         |
| <span data-ttu-id="08625-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="08625-261">Range-Lower</span></span>            | \-                                   |
| <span data-ttu-id="08625-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="08625-262">Range-Upper</span></span>            | \-                                   |
| <span data-ttu-id="08625-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="08625-263">Search-Flags</span></span>           | <span data-ttu-id="08625-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="08625-264">0x00000000</span></span>                           |
| <span data-ttu-id="08625-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="08625-265">System-Flags</span></span>           | <span data-ttu-id="08625-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="08625-266">0x00000010</span></span>                           |
| <span data-ttu-id="08625-267">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="08625-267">Classes used in</span></span>        | [<span data-ttu-id="08625-268">**FT-DFS**</span><span class="sxs-lookup"><span data-stu-id="08625-268">**FT-Dfs**</span></span>](c-ftdfs.md)<br/> |



 

 





