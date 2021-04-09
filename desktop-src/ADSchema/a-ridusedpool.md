---
title: RID-usato-attributo pool
description: Pool RID utilizzati da un controller di dominio.
ms.assetid: ca779461-5b8f-4ab2-b9cf-5f829889f10d
ms.tgt_platform: multiple
keywords:
- RID-usato-schema AD dell'attributo del pool
- Schema AD dell'attributo rIDUsedPool
topic_type:
- apiref
api_name:
- RID-Used-Pool
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84547d99b162da9da6e634a7c35eb9700e84e2a6
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104122366"
---
# <a name="rid-used-pool-attribute"></a><span data-ttu-id="1f8b1-105">RID-usato-attributo pool</span><span class="sxs-lookup"><span data-stu-id="1f8b1-105">RID-Used-Pool attribute</span></span>

<span data-ttu-id="1f8b1-106">Pool RID utilizzati da un controller di dominio.</span><span class="sxs-lookup"><span data-stu-id="1f8b1-106">The RID Pools that have been used by a DC.</span></span>



| <span data-ttu-id="1f8b1-107">Voce</span><span class="sxs-lookup"><span data-stu-id="1f8b1-107">Entry</span></span> | <span data-ttu-id="1f8b1-108">Valore</span><span class="sxs-lookup"><span data-stu-id="1f8b1-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="1f8b1-109">CN</span><span class="sxs-lookup"><span data-stu-id="1f8b1-109">CN</span></span>                | <span data-ttu-id="1f8b1-110">RID-usato-pool</span><span class="sxs-lookup"><span data-stu-id="1f8b1-110">RID-Used-Pool</span></span>                        |
| <span data-ttu-id="1f8b1-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="1f8b1-111">Ldap-Display-Name</span></span> | <span data-ttu-id="1f8b1-112">rIDUsedPool</span><span class="sxs-lookup"><span data-stu-id="1f8b1-112">rIDUsedPool</span></span>                          |
| <span data-ttu-id="1f8b1-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="1f8b1-113">Size</span></span>              | <span data-ttu-id="1f8b1-114">8 byte</span><span class="sxs-lookup"><span data-stu-id="1f8b1-114">8 bytes</span></span>                              |
| <span data-ttu-id="1f8b1-115">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="1f8b1-115">Update Privilege</span></span>  | <span data-ttu-id="1f8b1-116">Questo valore viene impostato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="1f8b1-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="1f8b1-117">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="1f8b1-117">Update Frequency</span></span>  | <span data-ttu-id="1f8b1-118">Ogni volta che un pool di RID viene svuotato.</span><span class="sxs-lookup"><span data-stu-id="1f8b1-118">Whenever a RID pool is emptied.</span></span>      |
| <span data-ttu-id="1f8b1-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="1f8b1-119">Attribute-Id</span></span>      | <span data-ttu-id="1f8b1-120">1.2.840.113556.1.4.373</span><span class="sxs-lookup"><span data-stu-id="1f8b1-120">1.2.840.113556.1.4.373</span></span>               |
| <span data-ttu-id="1f8b1-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="1f8b1-121">System-Id-Guid</span></span>    | <span data-ttu-id="1f8b1-122">6617188b-8f3c-11d0-afda-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="1f8b1-122">6617188b-8f3c-11d0-afda-00c04fd930c9</span></span> |
| <span data-ttu-id="1f8b1-123">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1f8b1-123">Syntax</span></span>            | [<span data-ttu-id="1f8b1-124">**Interval**</span><span class="sxs-lookup"><span data-stu-id="1f8b1-124">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="1f8b1-125">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="1f8b1-125">Implementations</span></span>

-   [<span data-ttu-id="1f8b1-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="1f8b1-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="1f8b1-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="1f8b1-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="1f8b1-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="1f8b1-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="1f8b1-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="1f8b1-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="1f8b1-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="1f8b1-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="1f8b1-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="1f8b1-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="1f8b1-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1f8b1-132">Windows 2000 Server</span></span>



| <span data-ttu-id="1f8b1-133">Voce</span><span class="sxs-lookup"><span data-stu-id="1f8b1-133">Entry</span></span> | <span data-ttu-id="1f8b1-134">Valore</span><span class="sxs-lookup"><span data-stu-id="1f8b1-134">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="1f8b1-135">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="1f8b1-135">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="1f8b1-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1f8b1-136">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="1f8b1-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="1f8b1-137">System-Only</span></span>            | <span data-ttu-id="1f8b1-138">Vero</span><span class="sxs-lookup"><span data-stu-id="1f8b1-138">True</span></span>                                   |
| <span data-ttu-id="1f8b1-139">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="1f8b1-139">Is-Single-Valued</span></span>       | <span data-ttu-id="1f8b1-140">Vero</span><span class="sxs-lookup"><span data-stu-id="1f8b1-140">True</span></span>                                   |
| <span data-ttu-id="1f8b1-141">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="1f8b1-141">Is Indexed</span></span>             | <span data-ttu-id="1f8b1-142">Falso</span><span class="sxs-lookup"><span data-stu-id="1f8b1-142">False</span></span>                                  |
| <span data-ttu-id="1f8b1-143">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="1f8b1-143">In Global Catalog</span></span>      | <span data-ttu-id="1f8b1-144">Falso</span><span class="sxs-lookup"><span data-stu-id="1f8b1-144">False</span></span>                                  |
| <span data-ttu-id="1f8b1-145">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="1f8b1-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="1f8b1-146">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="1f8b1-146">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="1f8b1-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1f8b1-147">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="1f8b1-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1f8b1-148">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="1f8b1-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1f8b1-149">Search-Flags</span></span>           | <span data-ttu-id="1f8b1-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1f8b1-150">0x00000000</span></span>                             |
| <span data-ttu-id="1f8b1-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1f8b1-151">System-Flags</span></span>           | <span data-ttu-id="1f8b1-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1f8b1-152">0x00000010</span></span>                             |
| <span data-ttu-id="1f8b1-153">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="1f8b1-153">Classes used in</span></span>        | [<span data-ttu-id="1f8b1-154">**Set RID**</span><span class="sxs-lookup"><span data-stu-id="1f8b1-154">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="1f8b1-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1f8b1-155">Windows Server 2003</span></span>



| <span data-ttu-id="1f8b1-156">Voce</span><span class="sxs-lookup"><span data-stu-id="1f8b1-156">Entry</span></span> | <span data-ttu-id="1f8b1-157">Valore</span><span class="sxs-lookup"><span data-stu-id="1f8b1-157">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="1f8b1-158">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="1f8b1-158">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="1f8b1-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1f8b1-159">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="1f8b1-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="1f8b1-160">System-Only</span></span>            | <span data-ttu-id="1f8b1-161">Vero</span><span class="sxs-lookup"><span data-stu-id="1f8b1-161">True</span></span>                                   |
| <span data-ttu-id="1f8b1-162">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="1f8b1-162">Is-Single-Valued</span></span>       | <span data-ttu-id="1f8b1-163">Vero</span><span class="sxs-lookup"><span data-stu-id="1f8b1-163">True</span></span>                                   |
| <span data-ttu-id="1f8b1-164">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="1f8b1-164">Is Indexed</span></span>             | <span data-ttu-id="1f8b1-165">Falso</span><span class="sxs-lookup"><span data-stu-id="1f8b1-165">False</span></span>                                  |
| <span data-ttu-id="1f8b1-166">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="1f8b1-166">In Global Catalog</span></span>      | <span data-ttu-id="1f8b1-167">Falso</span><span class="sxs-lookup"><span data-stu-id="1f8b1-167">False</span></span>                                  |
| <span data-ttu-id="1f8b1-168">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="1f8b1-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="1f8b1-169">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="1f8b1-169">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="1f8b1-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1f8b1-170">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="1f8b1-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1f8b1-171">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="1f8b1-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1f8b1-172">Search-Flags</span></span>           | <span data-ttu-id="1f8b1-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1f8b1-173">0x00000000</span></span>                             |
| <span data-ttu-id="1f8b1-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1f8b1-174">System-Flags</span></span>           | <span data-ttu-id="1f8b1-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1f8b1-175">0x00000010</span></span>                             |
| <span data-ttu-id="1f8b1-176">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="1f8b1-176">Classes used in</span></span>        | [<span data-ttu-id="1f8b1-177">**Set RID**</span><span class="sxs-lookup"><span data-stu-id="1f8b1-177">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="1f8b1-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="1f8b1-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="1f8b1-179">Voce</span><span class="sxs-lookup"><span data-stu-id="1f8b1-179">Entry</span></span> | <span data-ttu-id="1f8b1-180">Valore</span><span class="sxs-lookup"><span data-stu-id="1f8b1-180">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="1f8b1-181">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="1f8b1-181">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="1f8b1-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1f8b1-182">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="1f8b1-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="1f8b1-183">System-Only</span></span>            | <span data-ttu-id="1f8b1-184">Vero</span><span class="sxs-lookup"><span data-stu-id="1f8b1-184">True</span></span>                                   |
| <span data-ttu-id="1f8b1-185">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="1f8b1-185">Is-Single-Valued</span></span>       | <span data-ttu-id="1f8b1-186">Vero</span><span class="sxs-lookup"><span data-stu-id="1f8b1-186">True</span></span>                                   |
| <span data-ttu-id="1f8b1-187">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="1f8b1-187">Is Indexed</span></span>             | <span data-ttu-id="1f8b1-188">Falso</span><span class="sxs-lookup"><span data-stu-id="1f8b1-188">False</span></span>                                  |
| <span data-ttu-id="1f8b1-189">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="1f8b1-189">In Global Catalog</span></span>      | <span data-ttu-id="1f8b1-190">Falso</span><span class="sxs-lookup"><span data-stu-id="1f8b1-190">False</span></span>                                  |
| <span data-ttu-id="1f8b1-191">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="1f8b1-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="1f8b1-192">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="1f8b1-192">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="1f8b1-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1f8b1-193">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="1f8b1-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1f8b1-194">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="1f8b1-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1f8b1-195">Search-Flags</span></span>           | <span data-ttu-id="1f8b1-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1f8b1-196">0x00000000</span></span>                             |
| <span data-ttu-id="1f8b1-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1f8b1-197">System-Flags</span></span>           | <span data-ttu-id="1f8b1-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1f8b1-198">0x00000010</span></span>                             |
| <span data-ttu-id="1f8b1-199">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="1f8b1-199">Classes used in</span></span>        | [<span data-ttu-id="1f8b1-200">**Set RID**</span><span class="sxs-lookup"><span data-stu-id="1f8b1-200">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="1f8b1-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1f8b1-201">Windows Server 2008</span></span>



| <span data-ttu-id="1f8b1-202">Voce</span><span class="sxs-lookup"><span data-stu-id="1f8b1-202">Entry</span></span> | <span data-ttu-id="1f8b1-203">Valore</span><span class="sxs-lookup"><span data-stu-id="1f8b1-203">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="1f8b1-204">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="1f8b1-204">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="1f8b1-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1f8b1-205">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="1f8b1-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="1f8b1-206">System-Only</span></span>            | <span data-ttu-id="1f8b1-207">Vero</span><span class="sxs-lookup"><span data-stu-id="1f8b1-207">True</span></span>                                   |
| <span data-ttu-id="1f8b1-208">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="1f8b1-208">Is-Single-Valued</span></span>       | <span data-ttu-id="1f8b1-209">Vero</span><span class="sxs-lookup"><span data-stu-id="1f8b1-209">True</span></span>                                   |
| <span data-ttu-id="1f8b1-210">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="1f8b1-210">Is Indexed</span></span>             | <span data-ttu-id="1f8b1-211">Falso</span><span class="sxs-lookup"><span data-stu-id="1f8b1-211">False</span></span>                                  |
| <span data-ttu-id="1f8b1-212">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="1f8b1-212">In Global Catalog</span></span>      | <span data-ttu-id="1f8b1-213">Falso</span><span class="sxs-lookup"><span data-stu-id="1f8b1-213">False</span></span>                                  |
| <span data-ttu-id="1f8b1-214">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="1f8b1-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="1f8b1-215">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="1f8b1-215">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="1f8b1-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1f8b1-216">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="1f8b1-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1f8b1-217">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="1f8b1-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1f8b1-218">Search-Flags</span></span>           | <span data-ttu-id="1f8b1-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1f8b1-219">0x00000000</span></span>                             |
| <span data-ttu-id="1f8b1-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1f8b1-220">System-Flags</span></span>           | <span data-ttu-id="1f8b1-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1f8b1-221">0x00000010</span></span>                             |
| <span data-ttu-id="1f8b1-222">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="1f8b1-222">Classes used in</span></span>        | [<span data-ttu-id="1f8b1-223">**Set RID**</span><span class="sxs-lookup"><span data-stu-id="1f8b1-223">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="1f8b1-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1f8b1-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="1f8b1-225">Voce</span><span class="sxs-lookup"><span data-stu-id="1f8b1-225">Entry</span></span> | <span data-ttu-id="1f8b1-226">Valore</span><span class="sxs-lookup"><span data-stu-id="1f8b1-226">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="1f8b1-227">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="1f8b1-227">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="1f8b1-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1f8b1-228">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="1f8b1-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="1f8b1-229">System-Only</span></span>            | <span data-ttu-id="1f8b1-230">Vero</span><span class="sxs-lookup"><span data-stu-id="1f8b1-230">True</span></span>                                   |
| <span data-ttu-id="1f8b1-231">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="1f8b1-231">Is-Single-Valued</span></span>       | <span data-ttu-id="1f8b1-232">Vero</span><span class="sxs-lookup"><span data-stu-id="1f8b1-232">True</span></span>                                   |
| <span data-ttu-id="1f8b1-233">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="1f8b1-233">Is Indexed</span></span>             | <span data-ttu-id="1f8b1-234">Falso</span><span class="sxs-lookup"><span data-stu-id="1f8b1-234">False</span></span>                                  |
| <span data-ttu-id="1f8b1-235">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="1f8b1-235">In Global Catalog</span></span>      | <span data-ttu-id="1f8b1-236">Falso</span><span class="sxs-lookup"><span data-stu-id="1f8b1-236">False</span></span>                                  |
| <span data-ttu-id="1f8b1-237">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="1f8b1-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="1f8b1-238">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="1f8b1-238">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="1f8b1-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1f8b1-239">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="1f8b1-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1f8b1-240">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="1f8b1-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1f8b1-241">Search-Flags</span></span>           | <span data-ttu-id="1f8b1-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1f8b1-242">0x00000000</span></span>                             |
| <span data-ttu-id="1f8b1-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1f8b1-243">System-Flags</span></span>           | <span data-ttu-id="1f8b1-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1f8b1-244">0x00000010</span></span>                             |
| <span data-ttu-id="1f8b1-245">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="1f8b1-245">Classes used in</span></span>        | [<span data-ttu-id="1f8b1-246">**Set RID**</span><span class="sxs-lookup"><span data-stu-id="1f8b1-246">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="1f8b1-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1f8b1-247">Windows Server 2012</span></span>



| <span data-ttu-id="1f8b1-248">Voce</span><span class="sxs-lookup"><span data-stu-id="1f8b1-248">Entry</span></span> | <span data-ttu-id="1f8b1-249">Valore</span><span class="sxs-lookup"><span data-stu-id="1f8b1-249">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="1f8b1-250">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="1f8b1-250">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="1f8b1-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1f8b1-251">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="1f8b1-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="1f8b1-252">System-Only</span></span>            | <span data-ttu-id="1f8b1-253">Vero</span><span class="sxs-lookup"><span data-stu-id="1f8b1-253">True</span></span>                                   |
| <span data-ttu-id="1f8b1-254">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="1f8b1-254">Is-Single-Valued</span></span>       | <span data-ttu-id="1f8b1-255">Vero</span><span class="sxs-lookup"><span data-stu-id="1f8b1-255">True</span></span>                                   |
| <span data-ttu-id="1f8b1-256">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="1f8b1-256">Is Indexed</span></span>             | <span data-ttu-id="1f8b1-257">Falso</span><span class="sxs-lookup"><span data-stu-id="1f8b1-257">False</span></span>                                  |
| <span data-ttu-id="1f8b1-258">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="1f8b1-258">In Global Catalog</span></span>      | <span data-ttu-id="1f8b1-259">Falso</span><span class="sxs-lookup"><span data-stu-id="1f8b1-259">False</span></span>                                  |
| <span data-ttu-id="1f8b1-260">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="1f8b1-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="1f8b1-261">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="1f8b1-261">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="1f8b1-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1f8b1-262">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="1f8b1-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1f8b1-263">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="1f8b1-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1f8b1-264">Search-Flags</span></span>           | <span data-ttu-id="1f8b1-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1f8b1-265">0x00000000</span></span>                             |
| <span data-ttu-id="1f8b1-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1f8b1-266">System-Flags</span></span>           | <span data-ttu-id="1f8b1-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1f8b1-267">0x00000010</span></span>                             |
| <span data-ttu-id="1f8b1-268">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="1f8b1-268">Classes used in</span></span>        | [<span data-ttu-id="1f8b1-269">**Set RID**</span><span class="sxs-lookup"><span data-stu-id="1f8b1-269">**RID-Set**</span></span>](c-ridset.md)<br/> |



 

 





