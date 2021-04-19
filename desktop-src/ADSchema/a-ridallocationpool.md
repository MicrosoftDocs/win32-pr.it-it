---
title: RID-allocation-attributo pool
description: Un pool che è stato preceduto per l'uso da parte del gestore RID quando è stato utilizzato il RID-Previous-allocation-pool.
ms.assetid: 6d49b497-322f-424c-badc-4801f51481f3
ms.tgt_platform: multiple
keywords:
- RID-allocation-schema AD dell'attributo del pool
- Schema AD dell'attributo rIDAllocationPool
topic_type:
- apiref
api_name:
- RID-Allocation-Pool
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a035cef460cc3081144d66391db78fb32c61108b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "106303140"
---
# <a name="rid-allocation-pool-attribute"></a><span data-ttu-id="c2a6c-105">RID-allocation-attributo pool</span><span class="sxs-lookup"><span data-stu-id="c2a6c-105">RID-Allocation-Pool attribute</span></span>

<span data-ttu-id="c2a6c-106">Un pool che è stato preceduto per l'uso da parte del gestore RID quando è stato utilizzato il RID-Previous-allocation-pool.</span><span class="sxs-lookup"><span data-stu-id="c2a6c-106">A pool that was prefetched for use by the RID manager when the RID-Previous-Allocation-Pool has been used up.</span></span>



| <span data-ttu-id="c2a6c-107">Voce</span><span class="sxs-lookup"><span data-stu-id="c2a6c-107">Entry</span></span> | <span data-ttu-id="c2a6c-108">Valore</span><span class="sxs-lookup"><span data-stu-id="c2a6c-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="c2a6c-109">CN</span><span class="sxs-lookup"><span data-stu-id="c2a6c-109">CN</span></span>                | <span data-ttu-id="c2a6c-110">RID-allocazione-pool</span><span class="sxs-lookup"><span data-stu-id="c2a6c-110">RID-Allocation-Pool</span></span>                  |
| <span data-ttu-id="c2a6c-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="c2a6c-111">Ldap-Display-Name</span></span> | <span data-ttu-id="c2a6c-112">rIDAllocationPool</span><span class="sxs-lookup"><span data-stu-id="c2a6c-112">rIDAllocationPool</span></span>                    |
| <span data-ttu-id="c2a6c-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="c2a6c-113">Size</span></span>              | <span data-ttu-id="c2a6c-114">8 byte</span><span class="sxs-lookup"><span data-stu-id="c2a6c-114">8 bytes</span></span>                              |
| <span data-ttu-id="c2a6c-115">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="c2a6c-115">Update Privilege</span></span>  | <span data-ttu-id="c2a6c-116">Questo valore viene impostato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="c2a6c-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="c2a6c-117">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="c2a6c-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="c2a6c-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c2a6c-118">Attribute-Id</span></span>      | <span data-ttu-id="c2a6c-119">1.2.840.113556.1.4.371</span><span class="sxs-lookup"><span data-stu-id="c2a6c-119">1.2.840.113556.1.4.371</span></span>               |
| <span data-ttu-id="c2a6c-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="c2a6c-120">System-Id-Guid</span></span>    | <span data-ttu-id="c2a6c-121">66171889-8f3c-11d0-afda-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="c2a6c-121">66171889-8f3c-11d0-afda-00c04fd930c9</span></span> |
| <span data-ttu-id="c2a6c-122">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c2a6c-122">Syntax</span></span>            | [<span data-ttu-id="c2a6c-123">**Interval**</span><span class="sxs-lookup"><span data-stu-id="c2a6c-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="c2a6c-124">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="c2a6c-124">Implementations</span></span>

-   [<span data-ttu-id="c2a6c-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="c2a6c-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="c2a6c-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c2a6c-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c2a6c-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c2a6c-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c2a6c-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c2a6c-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c2a6c-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c2a6c-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c2a6c-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c2a6c-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="c2a6c-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c2a6c-131">Windows 2000 Server</span></span>



| <span data-ttu-id="c2a6c-132">Voce</span><span class="sxs-lookup"><span data-stu-id="c2a6c-132">Entry</span></span> | <span data-ttu-id="c2a6c-133">Valore</span><span class="sxs-lookup"><span data-stu-id="c2a6c-133">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="c2a6c-134">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="c2a6c-134">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="c2a6c-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c2a6c-135">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="c2a6c-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="c2a6c-136">System-Only</span></span>            | <span data-ttu-id="c2a6c-137">Vero</span><span class="sxs-lookup"><span data-stu-id="c2a6c-137">True</span></span>                                   |
| <span data-ttu-id="c2a6c-138">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="c2a6c-138">Is-Single-Valued</span></span>       | <span data-ttu-id="c2a6c-139">Vero</span><span class="sxs-lookup"><span data-stu-id="c2a6c-139">True</span></span>                                   |
| <span data-ttu-id="c2a6c-140">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="c2a6c-140">Is Indexed</span></span>             | <span data-ttu-id="c2a6c-141">Falso</span><span class="sxs-lookup"><span data-stu-id="c2a6c-141">False</span></span>                                  |
| <span data-ttu-id="c2a6c-142">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="c2a6c-142">In Global Catalog</span></span>      | <span data-ttu-id="c2a6c-143">Falso</span><span class="sxs-lookup"><span data-stu-id="c2a6c-143">False</span></span>                                  |
| <span data-ttu-id="c2a6c-144">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="c2a6c-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="c2a6c-145">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="c2a6c-145">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="c2a6c-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c2a6c-146">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="c2a6c-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c2a6c-147">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="c2a6c-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c2a6c-148">Search-Flags</span></span>           | <span data-ttu-id="c2a6c-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c2a6c-149">0x00000000</span></span>                             |
| <span data-ttu-id="c2a6c-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c2a6c-150">System-Flags</span></span>           | <span data-ttu-id="c2a6c-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c2a6c-151">0x00000010</span></span>                             |
| <span data-ttu-id="c2a6c-152">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="c2a6c-152">Classes used in</span></span>        | [<span data-ttu-id="c2a6c-153">**Set RID**</span><span class="sxs-lookup"><span data-stu-id="c2a6c-153">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="c2a6c-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c2a6c-154">Windows Server 2003</span></span>



| <span data-ttu-id="c2a6c-155">Voce</span><span class="sxs-lookup"><span data-stu-id="c2a6c-155">Entry</span></span> | <span data-ttu-id="c2a6c-156">Valore</span><span class="sxs-lookup"><span data-stu-id="c2a6c-156">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="c2a6c-157">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="c2a6c-157">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="c2a6c-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c2a6c-158">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="c2a6c-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="c2a6c-159">System-Only</span></span>            | <span data-ttu-id="c2a6c-160">Vero</span><span class="sxs-lookup"><span data-stu-id="c2a6c-160">True</span></span>                                   |
| <span data-ttu-id="c2a6c-161">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="c2a6c-161">Is-Single-Valued</span></span>       | <span data-ttu-id="c2a6c-162">Vero</span><span class="sxs-lookup"><span data-stu-id="c2a6c-162">True</span></span>                                   |
| <span data-ttu-id="c2a6c-163">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="c2a6c-163">Is Indexed</span></span>             | <span data-ttu-id="c2a6c-164">Falso</span><span class="sxs-lookup"><span data-stu-id="c2a6c-164">False</span></span>                                  |
| <span data-ttu-id="c2a6c-165">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="c2a6c-165">In Global Catalog</span></span>      | <span data-ttu-id="c2a6c-166">Falso</span><span class="sxs-lookup"><span data-stu-id="c2a6c-166">False</span></span>                                  |
| <span data-ttu-id="c2a6c-167">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="c2a6c-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="c2a6c-168">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="c2a6c-168">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="c2a6c-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c2a6c-169">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="c2a6c-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c2a6c-170">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="c2a6c-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c2a6c-171">Search-Flags</span></span>           | <span data-ttu-id="c2a6c-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c2a6c-172">0x00000000</span></span>                             |
| <span data-ttu-id="c2a6c-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c2a6c-173">System-Flags</span></span>           | <span data-ttu-id="c2a6c-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c2a6c-174">0x00000010</span></span>                             |
| <span data-ttu-id="c2a6c-175">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="c2a6c-175">Classes used in</span></span>        | [<span data-ttu-id="c2a6c-176">**Set RID**</span><span class="sxs-lookup"><span data-stu-id="c2a6c-176">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c2a6c-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c2a6c-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c2a6c-178">Voce</span><span class="sxs-lookup"><span data-stu-id="c2a6c-178">Entry</span></span> | <span data-ttu-id="c2a6c-179">Valore</span><span class="sxs-lookup"><span data-stu-id="c2a6c-179">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="c2a6c-180">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="c2a6c-180">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="c2a6c-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c2a6c-181">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="c2a6c-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="c2a6c-182">System-Only</span></span>            | <span data-ttu-id="c2a6c-183">Vero</span><span class="sxs-lookup"><span data-stu-id="c2a6c-183">True</span></span>                                   |
| <span data-ttu-id="c2a6c-184">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="c2a6c-184">Is-Single-Valued</span></span>       | <span data-ttu-id="c2a6c-185">Vero</span><span class="sxs-lookup"><span data-stu-id="c2a6c-185">True</span></span>                                   |
| <span data-ttu-id="c2a6c-186">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="c2a6c-186">Is Indexed</span></span>             | <span data-ttu-id="c2a6c-187">Falso</span><span class="sxs-lookup"><span data-stu-id="c2a6c-187">False</span></span>                                  |
| <span data-ttu-id="c2a6c-188">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="c2a6c-188">In Global Catalog</span></span>      | <span data-ttu-id="c2a6c-189">Falso</span><span class="sxs-lookup"><span data-stu-id="c2a6c-189">False</span></span>                                  |
| <span data-ttu-id="c2a6c-190">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="c2a6c-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="c2a6c-191">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="c2a6c-191">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="c2a6c-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c2a6c-192">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="c2a6c-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c2a6c-193">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="c2a6c-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c2a6c-194">Search-Flags</span></span>           | <span data-ttu-id="c2a6c-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c2a6c-195">0x00000000</span></span>                             |
| <span data-ttu-id="c2a6c-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c2a6c-196">System-Flags</span></span>           | <span data-ttu-id="c2a6c-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c2a6c-197">0x00000010</span></span>                             |
| <span data-ttu-id="c2a6c-198">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="c2a6c-198">Classes used in</span></span>        | [<span data-ttu-id="c2a6c-199">**Set RID**</span><span class="sxs-lookup"><span data-stu-id="c2a6c-199">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c2a6c-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c2a6c-200">Windows Server 2008</span></span>



| <span data-ttu-id="c2a6c-201">Voce</span><span class="sxs-lookup"><span data-stu-id="c2a6c-201">Entry</span></span> | <span data-ttu-id="c2a6c-202">Valore</span><span class="sxs-lookup"><span data-stu-id="c2a6c-202">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="c2a6c-203">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="c2a6c-203">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="c2a6c-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c2a6c-204">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="c2a6c-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="c2a6c-205">System-Only</span></span>            | <span data-ttu-id="c2a6c-206">Vero</span><span class="sxs-lookup"><span data-stu-id="c2a6c-206">True</span></span>                                   |
| <span data-ttu-id="c2a6c-207">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="c2a6c-207">Is-Single-Valued</span></span>       | <span data-ttu-id="c2a6c-208">Vero</span><span class="sxs-lookup"><span data-stu-id="c2a6c-208">True</span></span>                                   |
| <span data-ttu-id="c2a6c-209">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="c2a6c-209">Is Indexed</span></span>             | <span data-ttu-id="c2a6c-210">Falso</span><span class="sxs-lookup"><span data-stu-id="c2a6c-210">False</span></span>                                  |
| <span data-ttu-id="c2a6c-211">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="c2a6c-211">In Global Catalog</span></span>      | <span data-ttu-id="c2a6c-212">Falso</span><span class="sxs-lookup"><span data-stu-id="c2a6c-212">False</span></span>                                  |
| <span data-ttu-id="c2a6c-213">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="c2a6c-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="c2a6c-214">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="c2a6c-214">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="c2a6c-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c2a6c-215">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="c2a6c-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c2a6c-216">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="c2a6c-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c2a6c-217">Search-Flags</span></span>           | <span data-ttu-id="c2a6c-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c2a6c-218">0x00000000</span></span>                             |
| <span data-ttu-id="c2a6c-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c2a6c-219">System-Flags</span></span>           | <span data-ttu-id="c2a6c-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c2a6c-220">0x00000010</span></span>                             |
| <span data-ttu-id="c2a6c-221">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="c2a6c-221">Classes used in</span></span>        | [<span data-ttu-id="c2a6c-222">**Set RID**</span><span class="sxs-lookup"><span data-stu-id="c2a6c-222">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c2a6c-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c2a6c-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c2a6c-224">Voce</span><span class="sxs-lookup"><span data-stu-id="c2a6c-224">Entry</span></span> | <span data-ttu-id="c2a6c-225">Valore</span><span class="sxs-lookup"><span data-stu-id="c2a6c-225">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="c2a6c-226">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="c2a6c-226">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="c2a6c-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c2a6c-227">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="c2a6c-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="c2a6c-228">System-Only</span></span>            | <span data-ttu-id="c2a6c-229">Vero</span><span class="sxs-lookup"><span data-stu-id="c2a6c-229">True</span></span>                                   |
| <span data-ttu-id="c2a6c-230">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="c2a6c-230">Is-Single-Valued</span></span>       | <span data-ttu-id="c2a6c-231">Vero</span><span class="sxs-lookup"><span data-stu-id="c2a6c-231">True</span></span>                                   |
| <span data-ttu-id="c2a6c-232">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="c2a6c-232">Is Indexed</span></span>             | <span data-ttu-id="c2a6c-233">Falso</span><span class="sxs-lookup"><span data-stu-id="c2a6c-233">False</span></span>                                  |
| <span data-ttu-id="c2a6c-234">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="c2a6c-234">In Global Catalog</span></span>      | <span data-ttu-id="c2a6c-235">Falso</span><span class="sxs-lookup"><span data-stu-id="c2a6c-235">False</span></span>                                  |
| <span data-ttu-id="c2a6c-236">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="c2a6c-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="c2a6c-237">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="c2a6c-237">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="c2a6c-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c2a6c-238">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="c2a6c-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c2a6c-239">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="c2a6c-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c2a6c-240">Search-Flags</span></span>           | <span data-ttu-id="c2a6c-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c2a6c-241">0x00000000</span></span>                             |
| <span data-ttu-id="c2a6c-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c2a6c-242">System-Flags</span></span>           | <span data-ttu-id="c2a6c-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c2a6c-243">0x00000010</span></span>                             |
| <span data-ttu-id="c2a6c-244">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="c2a6c-244">Classes used in</span></span>        | [<span data-ttu-id="c2a6c-245">**Set RID**</span><span class="sxs-lookup"><span data-stu-id="c2a6c-245">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c2a6c-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c2a6c-246">Windows Server 2012</span></span>



| <span data-ttu-id="c2a6c-247">Voce</span><span class="sxs-lookup"><span data-stu-id="c2a6c-247">Entry</span></span> | <span data-ttu-id="c2a6c-248">Valore</span><span class="sxs-lookup"><span data-stu-id="c2a6c-248">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="c2a6c-249">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="c2a6c-249">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="c2a6c-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c2a6c-250">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="c2a6c-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="c2a6c-251">System-Only</span></span>            | <span data-ttu-id="c2a6c-252">Vero</span><span class="sxs-lookup"><span data-stu-id="c2a6c-252">True</span></span>                                   |
| <span data-ttu-id="c2a6c-253">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="c2a6c-253">Is-Single-Valued</span></span>       | <span data-ttu-id="c2a6c-254">Vero</span><span class="sxs-lookup"><span data-stu-id="c2a6c-254">True</span></span>                                   |
| <span data-ttu-id="c2a6c-255">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="c2a6c-255">Is Indexed</span></span>             | <span data-ttu-id="c2a6c-256">Falso</span><span class="sxs-lookup"><span data-stu-id="c2a6c-256">False</span></span>                                  |
| <span data-ttu-id="c2a6c-257">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="c2a6c-257">In Global Catalog</span></span>      | <span data-ttu-id="c2a6c-258">Falso</span><span class="sxs-lookup"><span data-stu-id="c2a6c-258">False</span></span>                                  |
| <span data-ttu-id="c2a6c-259">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="c2a6c-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="c2a6c-260">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="c2a6c-260">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="c2a6c-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c2a6c-261">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="c2a6c-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c2a6c-262">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="c2a6c-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c2a6c-263">Search-Flags</span></span>           | <span data-ttu-id="c2a6c-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c2a6c-264">0x00000000</span></span>                             |
| <span data-ttu-id="c2a6c-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c2a6c-265">System-Flags</span></span>           | <span data-ttu-id="c2a6c-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c2a6c-266">0x00000010</span></span>                             |
| <span data-ttu-id="c2a6c-267">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="c2a6c-267">Classes used in</span></span>        | [<span data-ttu-id="c2a6c-268">**Set RID**</span><span class="sxs-lookup"><span data-stu-id="c2a6c-268">**RID-Set**</span></span>](c-ridset.md)<br/> |



 

 





