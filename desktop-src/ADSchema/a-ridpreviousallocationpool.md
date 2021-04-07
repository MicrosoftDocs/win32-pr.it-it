---
title: RID-Previous-allocation-attributo pool
description: Contiene il pool di identificatori relativi (RID) da cui viene allocato un controller di dominio.
ms.assetid: d2f60259-388b-4dea-a1f7-9e650b1a66db
ms.tgt_platform: multiple
keywords:
- RID-precedente-allocazione-schema AD attributo pool
- Schema AD dell'attributo rIDPreviousAllocationPool
topic_type:
- apiref
api_name:
- RID-Previous-Allocation-Pool
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15438d55c9540ecca873395cc329058bc0773399
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103875166"
---
# <a name="rid-previous-allocation-pool-attribute"></a><span data-ttu-id="66211-105">RID-Previous-allocation-attributo pool</span><span class="sxs-lookup"><span data-stu-id="66211-105">RID-Previous-Allocation-Pool attribute</span></span>

<span data-ttu-id="66211-106">L'attributo **RID-Previous-allocation-pool** contiene il pool di identificatori relativi (RID) da cui viene allocato un controller di dominio.</span><span class="sxs-lookup"><span data-stu-id="66211-106">The **RID-Previous-Allocation-Pool** attribute contains the pool of relative identifiers (RIDs) that a domain controller allocates from.</span></span> <span data-ttu-id="66211-107">Questo attributo è un valore di otto byte che contiene una coppia di interi a quattro byte che rappresentano i valori iniziale e finale del pool di RID.</span><span class="sxs-lookup"><span data-stu-id="66211-107">This attribute is an eight-byte value that contains a pair of four-byte integers that represent the start and end values of the RID pool.</span></span> <span data-ttu-id="66211-108">Il valore iniziale è nei quattro byte inferiori e il valore finale è nei quattro byte superiori.</span><span class="sxs-lookup"><span data-stu-id="66211-108">The start value is in the lower four bytes and the end value is in the upper four bytes.</span></span>



| <span data-ttu-id="66211-109">Voce</span><span class="sxs-lookup"><span data-stu-id="66211-109">Entry</span></span> | <span data-ttu-id="66211-110">Valore</span><span class="sxs-lookup"><span data-stu-id="66211-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="66211-111">CN</span><span class="sxs-lookup"><span data-stu-id="66211-111">CN</span></span>                | <span data-ttu-id="66211-112">RID-precedente-allocazione-pool</span><span class="sxs-lookup"><span data-stu-id="66211-112">RID-Previous-Allocation-Pool</span></span>         |
| <span data-ttu-id="66211-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="66211-113">Ldap-Display-Name</span></span> | <span data-ttu-id="66211-114">rIDPreviousAllocationPool</span><span class="sxs-lookup"><span data-stu-id="66211-114">rIDPreviousAllocationPool</span></span>            |
| <span data-ttu-id="66211-115">Dimensione</span><span class="sxs-lookup"><span data-stu-id="66211-115">Size</span></span>              | \-                                   |
| <span data-ttu-id="66211-116">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="66211-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="66211-117">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="66211-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="66211-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="66211-118">Attribute-Id</span></span>      | <span data-ttu-id="66211-119">1.2.840.113556.1.4.372</span><span class="sxs-lookup"><span data-stu-id="66211-119">1.2.840.113556.1.4.372</span></span>               |
| <span data-ttu-id="66211-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="66211-120">System-Id-Guid</span></span>    | <span data-ttu-id="66211-121">6617188a-8f3c-11d0-afda-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="66211-121">6617188a-8f3c-11d0-afda-00c04fd930c9</span></span> |
| <span data-ttu-id="66211-122">Sintassi</span><span class="sxs-lookup"><span data-stu-id="66211-122">Syntax</span></span>            | [<span data-ttu-id="66211-123">**Interval**</span><span class="sxs-lookup"><span data-stu-id="66211-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="66211-124">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="66211-124">Implementations</span></span>

-   [<span data-ttu-id="66211-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="66211-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="66211-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="66211-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="66211-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="66211-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="66211-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="66211-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="66211-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="66211-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="66211-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="66211-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="66211-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="66211-131">Windows 2000 Server</span></span>



| <span data-ttu-id="66211-132">Voce</span><span class="sxs-lookup"><span data-stu-id="66211-132">Entry</span></span> | <span data-ttu-id="66211-133">Valore</span><span class="sxs-lookup"><span data-stu-id="66211-133">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="66211-134">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="66211-134">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="66211-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="66211-135">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="66211-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="66211-136">System-Only</span></span>            | <span data-ttu-id="66211-137">Vero</span><span class="sxs-lookup"><span data-stu-id="66211-137">True</span></span>                                   |
| <span data-ttu-id="66211-138">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="66211-138">Is-Single-Valued</span></span>       | <span data-ttu-id="66211-139">Vero</span><span class="sxs-lookup"><span data-stu-id="66211-139">True</span></span>                                   |
| <span data-ttu-id="66211-140">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="66211-140">Is Indexed</span></span>             | <span data-ttu-id="66211-141">Falso</span><span class="sxs-lookup"><span data-stu-id="66211-141">False</span></span>                                  |
| <span data-ttu-id="66211-142">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="66211-142">In Global Catalog</span></span>      | <span data-ttu-id="66211-143">Falso</span><span class="sxs-lookup"><span data-stu-id="66211-143">False</span></span>                                  |
| <span data-ttu-id="66211-144">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="66211-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="66211-145">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="66211-145">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="66211-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="66211-146">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="66211-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="66211-147">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="66211-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="66211-148">Search-Flags</span></span>           | <span data-ttu-id="66211-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="66211-149">0x00000000</span></span>                             |
| <span data-ttu-id="66211-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="66211-150">System-Flags</span></span>           | <span data-ttu-id="66211-151">0x00000011</span><span class="sxs-lookup"><span data-stu-id="66211-151">0x00000011</span></span>                             |
| <span data-ttu-id="66211-152">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="66211-152">Classes used in</span></span>        | [<span data-ttu-id="66211-153">**Set RID**</span><span class="sxs-lookup"><span data-stu-id="66211-153">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="66211-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="66211-154">Windows Server 2003</span></span>



| <span data-ttu-id="66211-155">Voce</span><span class="sxs-lookup"><span data-stu-id="66211-155">Entry</span></span> | <span data-ttu-id="66211-156">Valore</span><span class="sxs-lookup"><span data-stu-id="66211-156">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="66211-157">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="66211-157">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="66211-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="66211-158">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="66211-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="66211-159">System-Only</span></span>            | <span data-ttu-id="66211-160">Vero</span><span class="sxs-lookup"><span data-stu-id="66211-160">True</span></span>                                   |
| <span data-ttu-id="66211-161">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="66211-161">Is-Single-Valued</span></span>       | <span data-ttu-id="66211-162">Vero</span><span class="sxs-lookup"><span data-stu-id="66211-162">True</span></span>                                   |
| <span data-ttu-id="66211-163">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="66211-163">Is Indexed</span></span>             | <span data-ttu-id="66211-164">Falso</span><span class="sxs-lookup"><span data-stu-id="66211-164">False</span></span>                                  |
| <span data-ttu-id="66211-165">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="66211-165">In Global Catalog</span></span>      | <span data-ttu-id="66211-166">Falso</span><span class="sxs-lookup"><span data-stu-id="66211-166">False</span></span>                                  |
| <span data-ttu-id="66211-167">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="66211-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="66211-168">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="66211-168">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="66211-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="66211-169">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="66211-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="66211-170">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="66211-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="66211-171">Search-Flags</span></span>           | <span data-ttu-id="66211-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="66211-172">0x00000000</span></span>                             |
| <span data-ttu-id="66211-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="66211-173">System-Flags</span></span>           | <span data-ttu-id="66211-174">0x00000011</span><span class="sxs-lookup"><span data-stu-id="66211-174">0x00000011</span></span>                             |
| <span data-ttu-id="66211-175">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="66211-175">Classes used in</span></span>        | [<span data-ttu-id="66211-176">**Set RID**</span><span class="sxs-lookup"><span data-stu-id="66211-176">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="66211-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="66211-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="66211-178">Voce</span><span class="sxs-lookup"><span data-stu-id="66211-178">Entry</span></span> | <span data-ttu-id="66211-179">Valore</span><span class="sxs-lookup"><span data-stu-id="66211-179">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="66211-180">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="66211-180">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="66211-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="66211-181">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="66211-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="66211-182">System-Only</span></span>            | <span data-ttu-id="66211-183">Vero</span><span class="sxs-lookup"><span data-stu-id="66211-183">True</span></span>                                   |
| <span data-ttu-id="66211-184">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="66211-184">Is-Single-Valued</span></span>       | <span data-ttu-id="66211-185">Vero</span><span class="sxs-lookup"><span data-stu-id="66211-185">True</span></span>                                   |
| <span data-ttu-id="66211-186">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="66211-186">Is Indexed</span></span>             | <span data-ttu-id="66211-187">Falso</span><span class="sxs-lookup"><span data-stu-id="66211-187">False</span></span>                                  |
| <span data-ttu-id="66211-188">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="66211-188">In Global Catalog</span></span>      | <span data-ttu-id="66211-189">Falso</span><span class="sxs-lookup"><span data-stu-id="66211-189">False</span></span>                                  |
| <span data-ttu-id="66211-190">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="66211-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="66211-191">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="66211-191">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="66211-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="66211-192">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="66211-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="66211-193">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="66211-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="66211-194">Search-Flags</span></span>           | <span data-ttu-id="66211-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="66211-195">0x00000000</span></span>                             |
| <span data-ttu-id="66211-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="66211-196">System-Flags</span></span>           | <span data-ttu-id="66211-197">0x00000011</span><span class="sxs-lookup"><span data-stu-id="66211-197">0x00000011</span></span>                             |
| <span data-ttu-id="66211-198">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="66211-198">Classes used in</span></span>        | [<span data-ttu-id="66211-199">**Set RID**</span><span class="sxs-lookup"><span data-stu-id="66211-199">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="66211-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="66211-200">Windows Server 2008</span></span>



| <span data-ttu-id="66211-201">Voce</span><span class="sxs-lookup"><span data-stu-id="66211-201">Entry</span></span> | <span data-ttu-id="66211-202">Valore</span><span class="sxs-lookup"><span data-stu-id="66211-202">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="66211-203">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="66211-203">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="66211-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="66211-204">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="66211-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="66211-205">System-Only</span></span>            | <span data-ttu-id="66211-206">Vero</span><span class="sxs-lookup"><span data-stu-id="66211-206">True</span></span>                                   |
| <span data-ttu-id="66211-207">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="66211-207">Is-Single-Valued</span></span>       | <span data-ttu-id="66211-208">Vero</span><span class="sxs-lookup"><span data-stu-id="66211-208">True</span></span>                                   |
| <span data-ttu-id="66211-209">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="66211-209">Is Indexed</span></span>             | <span data-ttu-id="66211-210">Falso</span><span class="sxs-lookup"><span data-stu-id="66211-210">False</span></span>                                  |
| <span data-ttu-id="66211-211">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="66211-211">In Global Catalog</span></span>      | <span data-ttu-id="66211-212">Falso</span><span class="sxs-lookup"><span data-stu-id="66211-212">False</span></span>                                  |
| <span data-ttu-id="66211-213">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="66211-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="66211-214">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="66211-214">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="66211-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="66211-215">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="66211-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="66211-216">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="66211-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="66211-217">Search-Flags</span></span>           | <span data-ttu-id="66211-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="66211-218">0x00000000</span></span>                             |
| <span data-ttu-id="66211-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="66211-219">System-Flags</span></span>           | <span data-ttu-id="66211-220">0x00000011</span><span class="sxs-lookup"><span data-stu-id="66211-220">0x00000011</span></span>                             |
| <span data-ttu-id="66211-221">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="66211-221">Classes used in</span></span>        | [<span data-ttu-id="66211-222">**Set RID**</span><span class="sxs-lookup"><span data-stu-id="66211-222">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="66211-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="66211-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="66211-224">Voce</span><span class="sxs-lookup"><span data-stu-id="66211-224">Entry</span></span> | <span data-ttu-id="66211-225">Valore</span><span class="sxs-lookup"><span data-stu-id="66211-225">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="66211-226">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="66211-226">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="66211-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="66211-227">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="66211-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="66211-228">System-Only</span></span>            | <span data-ttu-id="66211-229">Vero</span><span class="sxs-lookup"><span data-stu-id="66211-229">True</span></span>                                   |
| <span data-ttu-id="66211-230">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="66211-230">Is-Single-Valued</span></span>       | <span data-ttu-id="66211-231">Vero</span><span class="sxs-lookup"><span data-stu-id="66211-231">True</span></span>                                   |
| <span data-ttu-id="66211-232">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="66211-232">Is Indexed</span></span>             | <span data-ttu-id="66211-233">Falso</span><span class="sxs-lookup"><span data-stu-id="66211-233">False</span></span>                                  |
| <span data-ttu-id="66211-234">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="66211-234">In Global Catalog</span></span>      | <span data-ttu-id="66211-235">Falso</span><span class="sxs-lookup"><span data-stu-id="66211-235">False</span></span>                                  |
| <span data-ttu-id="66211-236">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="66211-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="66211-237">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="66211-237">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="66211-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="66211-238">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="66211-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="66211-239">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="66211-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="66211-240">Search-Flags</span></span>           | <span data-ttu-id="66211-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="66211-241">0x00000000</span></span>                             |
| <span data-ttu-id="66211-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="66211-242">System-Flags</span></span>           | <span data-ttu-id="66211-243">0x00000011</span><span class="sxs-lookup"><span data-stu-id="66211-243">0x00000011</span></span>                             |
| <span data-ttu-id="66211-244">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="66211-244">Classes used in</span></span>        | [<span data-ttu-id="66211-245">**Set RID**</span><span class="sxs-lookup"><span data-stu-id="66211-245">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="66211-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="66211-246">Windows Server 2012</span></span>



| <span data-ttu-id="66211-247">Voce</span><span class="sxs-lookup"><span data-stu-id="66211-247">Entry</span></span> | <span data-ttu-id="66211-248">Valore</span><span class="sxs-lookup"><span data-stu-id="66211-248">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="66211-249">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="66211-249">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="66211-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="66211-250">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="66211-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="66211-251">System-Only</span></span>            | <span data-ttu-id="66211-252">Vero</span><span class="sxs-lookup"><span data-stu-id="66211-252">True</span></span>                                   |
| <span data-ttu-id="66211-253">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="66211-253">Is-Single-Valued</span></span>       | <span data-ttu-id="66211-254">Vero</span><span class="sxs-lookup"><span data-stu-id="66211-254">True</span></span>                                   |
| <span data-ttu-id="66211-255">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="66211-255">Is Indexed</span></span>             | <span data-ttu-id="66211-256">Falso</span><span class="sxs-lookup"><span data-stu-id="66211-256">False</span></span>                                  |
| <span data-ttu-id="66211-257">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="66211-257">In Global Catalog</span></span>      | <span data-ttu-id="66211-258">Falso</span><span class="sxs-lookup"><span data-stu-id="66211-258">False</span></span>                                  |
| <span data-ttu-id="66211-259">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="66211-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="66211-260">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="66211-260">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="66211-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="66211-261">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="66211-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="66211-262">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="66211-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="66211-263">Search-Flags</span></span>           | <span data-ttu-id="66211-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="66211-264">0x00000000</span></span>                             |
| <span data-ttu-id="66211-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="66211-265">System-Flags</span></span>           | <span data-ttu-id="66211-266">0x00000011</span><span class="sxs-lookup"><span data-stu-id="66211-266">0x00000011</span></span>                             |
| <span data-ttu-id="66211-267">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="66211-267">Classes used in</span></span>        | [<span data-ttu-id="66211-268">**Set RID**</span><span class="sxs-lookup"><span data-stu-id="66211-268">**RID-Set**</span></span>](c-ridset.md)<br/> |



 

 





