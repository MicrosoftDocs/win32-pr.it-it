---
title: Attributo Site-Object
description: Nome distinto per il sito a cui appartiene la subnet.
ms.assetid: 4533c742-4276-48df-b0cd-7ba1641737a7
ms.tgt_platform: multiple
keywords:
- Schema AD Site-Object attribute
- Schema AD dell'attributo siteObject
topic_type:
- apiref
api_name:
- Site-Object
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac43fb4ee0718aec855de4b7eb251a5d67c1a5fd
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103875522"
---
# <a name="site-object-attribute"></a><span data-ttu-id="69c68-105">Attributo Site-Object</span><span class="sxs-lookup"><span data-stu-id="69c68-105">Site-Object attribute</span></span>

<span data-ttu-id="69c68-106">Nome distinto per il sito a cui appartiene la subnet.</span><span class="sxs-lookup"><span data-stu-id="69c68-106">The distinguished name for the site to which this subnet belongs.</span></span>



| <span data-ttu-id="69c68-107">Voce</span><span class="sxs-lookup"><span data-stu-id="69c68-107">Entry</span></span> | <span data-ttu-id="69c68-108">Valore</span><span class="sxs-lookup"><span data-stu-id="69c68-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="69c68-109">CN</span><span class="sxs-lookup"><span data-stu-id="69c68-109">CN</span></span>                | <span data-ttu-id="69c68-110">Site-Object</span><span class="sxs-lookup"><span data-stu-id="69c68-110">Site-Object</span></span>                             |
| <span data-ttu-id="69c68-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="69c68-111">Ldap-Display-Name</span></span> | <span data-ttu-id="69c68-112">siteObject</span><span class="sxs-lookup"><span data-stu-id="69c68-112">siteObject</span></span>                              |
| <span data-ttu-id="69c68-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="69c68-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="69c68-114">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="69c68-114">Update Privilege</span></span>  | <span data-ttu-id="69c68-115">Amministratore di dominio</span><span class="sxs-lookup"><span data-stu-id="69c68-115">Domain administrator</span></span>                    |
| <span data-ttu-id="69c68-116">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="69c68-116">Update Frequency</span></span>  | <span data-ttu-id="69c68-117">Ogni volta che viene creato un sito.</span><span class="sxs-lookup"><span data-stu-id="69c68-117">Whenever a site is created.</span></span>             |
| <span data-ttu-id="69c68-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="69c68-118">Attribute-Id</span></span>      | <span data-ttu-id="69c68-119">1.2.840.113556.1.4.512</span><span class="sxs-lookup"><span data-stu-id="69c68-119">1.2.840.113556.1.4.512</span></span>                  |
| <span data-ttu-id="69c68-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="69c68-120">System-Id-Guid</span></span>    | <span data-ttu-id="69c68-121">3e10944c-c354-11d0-aff8-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="69c68-121">3e10944c-c354-11d0-aff8-0000f80367c1</span></span>    |
| <span data-ttu-id="69c68-122">Sintassi</span><span class="sxs-lookup"><span data-stu-id="69c68-122">Syntax</span></span>            | [<span data-ttu-id="69c68-123">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="69c68-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="69c68-124">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="69c68-124">Implementations</span></span>

-   [<span data-ttu-id="69c68-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="69c68-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="69c68-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="69c68-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="69c68-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="69c68-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="69c68-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="69c68-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="69c68-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="69c68-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="69c68-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="69c68-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="69c68-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="69c68-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="69c68-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="69c68-132">Windows 2000 Server</span></span>



| <span data-ttu-id="69c68-133">Voce</span><span class="sxs-lookup"><span data-stu-id="69c68-133">Entry</span></span> | <span data-ttu-id="69c68-134">Valore</span><span class="sxs-lookup"><span data-stu-id="69c68-134">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="69c68-135">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="69c68-135">Link-Id</span></span>                | <span data-ttu-id="69c68-136">46</span><span class="sxs-lookup"><span data-stu-id="69c68-136">46</span></span>                                    |
| <span data-ttu-id="69c68-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="69c68-137">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="69c68-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="69c68-138">System-Only</span></span>            | <span data-ttu-id="69c68-139">Falso</span><span class="sxs-lookup"><span data-stu-id="69c68-139">False</span></span>                                 |
| <span data-ttu-id="69c68-140">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="69c68-140">Is-Single-Valued</span></span>       | <span data-ttu-id="69c68-141">Vero</span><span class="sxs-lookup"><span data-stu-id="69c68-141">True</span></span>                                  |
| <span data-ttu-id="69c68-142">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="69c68-142">Is Indexed</span></span>             | <span data-ttu-id="69c68-143">Falso</span><span class="sxs-lookup"><span data-stu-id="69c68-143">False</span></span>                                 |
| <span data-ttu-id="69c68-144">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="69c68-144">In Global Catalog</span></span>      | <span data-ttu-id="69c68-145">Falso</span><span class="sxs-lookup"><span data-stu-id="69c68-145">False</span></span>                                 |
| <span data-ttu-id="69c68-146">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="69c68-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="69c68-147">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="69c68-147">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="69c68-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="69c68-148">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="69c68-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="69c68-149">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="69c68-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="69c68-150">Search-Flags</span></span>           | <span data-ttu-id="69c68-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="69c68-151">0x00000000</span></span>                            |
| <span data-ttu-id="69c68-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="69c68-152">System-Flags</span></span>           | <span data-ttu-id="69c68-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="69c68-153">0x00000010</span></span>                            |
| <span data-ttu-id="69c68-154">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="69c68-154">Classes used in</span></span>        | [<span data-ttu-id="69c68-155">**Subnet**</span><span class="sxs-lookup"><span data-stu-id="69c68-155">**Subnet**</span></span>](c-subnet.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="69c68-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="69c68-156">Windows Server 2003</span></span>



| <span data-ttu-id="69c68-157">Voce</span><span class="sxs-lookup"><span data-stu-id="69c68-157">Entry</span></span> | <span data-ttu-id="69c68-158">Valore</span><span class="sxs-lookup"><span data-stu-id="69c68-158">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="69c68-159">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="69c68-159">Link-Id</span></span>                | <span data-ttu-id="69c68-160">46</span><span class="sxs-lookup"><span data-stu-id="69c68-160">46</span></span>                                    |
| <span data-ttu-id="69c68-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="69c68-161">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="69c68-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="69c68-162">System-Only</span></span>            | <span data-ttu-id="69c68-163">Falso</span><span class="sxs-lookup"><span data-stu-id="69c68-163">False</span></span>                                 |
| <span data-ttu-id="69c68-164">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="69c68-164">Is-Single-Valued</span></span>       | <span data-ttu-id="69c68-165">Vero</span><span class="sxs-lookup"><span data-stu-id="69c68-165">True</span></span>                                  |
| <span data-ttu-id="69c68-166">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="69c68-166">Is Indexed</span></span>             | <span data-ttu-id="69c68-167">Falso</span><span class="sxs-lookup"><span data-stu-id="69c68-167">False</span></span>                                 |
| <span data-ttu-id="69c68-168">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="69c68-168">In Global Catalog</span></span>      | <span data-ttu-id="69c68-169">Falso</span><span class="sxs-lookup"><span data-stu-id="69c68-169">False</span></span>                                 |
| <span data-ttu-id="69c68-170">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="69c68-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="69c68-171">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="69c68-171">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="69c68-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="69c68-172">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="69c68-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="69c68-173">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="69c68-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="69c68-174">Search-Flags</span></span>           | <span data-ttu-id="69c68-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="69c68-175">0x00000000</span></span>                            |
| <span data-ttu-id="69c68-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="69c68-176">System-Flags</span></span>           | <span data-ttu-id="69c68-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="69c68-177">0x00000010</span></span>                            |
| <span data-ttu-id="69c68-178">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="69c68-178">Classes used in</span></span>        | [<span data-ttu-id="69c68-179">**Subnet**</span><span class="sxs-lookup"><span data-stu-id="69c68-179">**Subnet**</span></span>](c-subnet.md)<br/> |



## <a name="adam"></a><span data-ttu-id="69c68-180">ADAM</span><span class="sxs-lookup"><span data-stu-id="69c68-180">ADAM</span></span>



| <span data-ttu-id="69c68-181">Voce</span><span class="sxs-lookup"><span data-stu-id="69c68-181">Entry</span></span> | <span data-ttu-id="69c68-182">Valore</span><span class="sxs-lookup"><span data-stu-id="69c68-182">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="69c68-183">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="69c68-183">Link-Id</span></span>                | <span data-ttu-id="69c68-184">46</span><span class="sxs-lookup"><span data-stu-id="69c68-184">46</span></span>                                    |
| <span data-ttu-id="69c68-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="69c68-185">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="69c68-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="69c68-186">System-Only</span></span>            | <span data-ttu-id="69c68-187">Falso</span><span class="sxs-lookup"><span data-stu-id="69c68-187">False</span></span>                                 |
| <span data-ttu-id="69c68-188">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="69c68-188">Is-Single-Valued</span></span>       | <span data-ttu-id="69c68-189">Vero</span><span class="sxs-lookup"><span data-stu-id="69c68-189">True</span></span>                                  |
| <span data-ttu-id="69c68-190">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="69c68-190">Is Indexed</span></span>             | <span data-ttu-id="69c68-191">Falso</span><span class="sxs-lookup"><span data-stu-id="69c68-191">False</span></span>                                 |
| <span data-ttu-id="69c68-192">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="69c68-192">In Global Catalog</span></span>      | <span data-ttu-id="69c68-193">Falso</span><span class="sxs-lookup"><span data-stu-id="69c68-193">False</span></span>                                 |
| <span data-ttu-id="69c68-194">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="69c68-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="69c68-195">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="69c68-195">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="69c68-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="69c68-196">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="69c68-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="69c68-197">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="69c68-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="69c68-198">Search-Flags</span></span>           | <span data-ttu-id="69c68-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="69c68-199">0x00000000</span></span>                            |
| <span data-ttu-id="69c68-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="69c68-200">System-Flags</span></span>           | <span data-ttu-id="69c68-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="69c68-201">0x00000010</span></span>                            |
| <span data-ttu-id="69c68-202">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="69c68-202">Classes used in</span></span>        | [<span data-ttu-id="69c68-203">**Subnet**</span><span class="sxs-lookup"><span data-stu-id="69c68-203">**Subnet**</span></span>](c-subnet.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="69c68-204">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="69c68-204">Windows Server 2003 R2</span></span>



| <span data-ttu-id="69c68-205">Voce</span><span class="sxs-lookup"><span data-stu-id="69c68-205">Entry</span></span> | <span data-ttu-id="69c68-206">Valore</span><span class="sxs-lookup"><span data-stu-id="69c68-206">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="69c68-207">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="69c68-207">Link-Id</span></span>                | <span data-ttu-id="69c68-208">46</span><span class="sxs-lookup"><span data-stu-id="69c68-208">46</span></span>                                    |
| <span data-ttu-id="69c68-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="69c68-209">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="69c68-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="69c68-210">System-Only</span></span>            | <span data-ttu-id="69c68-211">Falso</span><span class="sxs-lookup"><span data-stu-id="69c68-211">False</span></span>                                 |
| <span data-ttu-id="69c68-212">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="69c68-212">Is-Single-Valued</span></span>       | <span data-ttu-id="69c68-213">Vero</span><span class="sxs-lookup"><span data-stu-id="69c68-213">True</span></span>                                  |
| <span data-ttu-id="69c68-214">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="69c68-214">Is Indexed</span></span>             | <span data-ttu-id="69c68-215">Falso</span><span class="sxs-lookup"><span data-stu-id="69c68-215">False</span></span>                                 |
| <span data-ttu-id="69c68-216">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="69c68-216">In Global Catalog</span></span>      | <span data-ttu-id="69c68-217">Falso</span><span class="sxs-lookup"><span data-stu-id="69c68-217">False</span></span>                                 |
| <span data-ttu-id="69c68-218">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="69c68-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="69c68-219">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="69c68-219">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="69c68-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="69c68-220">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="69c68-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="69c68-221">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="69c68-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="69c68-222">Search-Flags</span></span>           | <span data-ttu-id="69c68-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="69c68-223">0x00000000</span></span>                            |
| <span data-ttu-id="69c68-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="69c68-224">System-Flags</span></span>           | <span data-ttu-id="69c68-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="69c68-225">0x00000010</span></span>                            |
| <span data-ttu-id="69c68-226">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="69c68-226">Classes used in</span></span>        | [<span data-ttu-id="69c68-227">**Subnet**</span><span class="sxs-lookup"><span data-stu-id="69c68-227">**Subnet**</span></span>](c-subnet.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="69c68-228">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="69c68-228">Windows Server 2008</span></span>



| <span data-ttu-id="69c68-229">Voce</span><span class="sxs-lookup"><span data-stu-id="69c68-229">Entry</span></span> | <span data-ttu-id="69c68-230">Valore</span><span class="sxs-lookup"><span data-stu-id="69c68-230">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="69c68-231">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="69c68-231">Link-Id</span></span>                | <span data-ttu-id="69c68-232">46</span><span class="sxs-lookup"><span data-stu-id="69c68-232">46</span></span>                                    |
| <span data-ttu-id="69c68-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="69c68-233">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="69c68-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="69c68-234">System-Only</span></span>            | <span data-ttu-id="69c68-235">Falso</span><span class="sxs-lookup"><span data-stu-id="69c68-235">False</span></span>                                 |
| <span data-ttu-id="69c68-236">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="69c68-236">Is-Single-Valued</span></span>       | <span data-ttu-id="69c68-237">Vero</span><span class="sxs-lookup"><span data-stu-id="69c68-237">True</span></span>                                  |
| <span data-ttu-id="69c68-238">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="69c68-238">Is Indexed</span></span>             | <span data-ttu-id="69c68-239">Falso</span><span class="sxs-lookup"><span data-stu-id="69c68-239">False</span></span>                                 |
| <span data-ttu-id="69c68-240">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="69c68-240">In Global Catalog</span></span>      | <span data-ttu-id="69c68-241">Falso</span><span class="sxs-lookup"><span data-stu-id="69c68-241">False</span></span>                                 |
| <span data-ttu-id="69c68-242">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="69c68-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="69c68-243">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="69c68-243">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="69c68-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="69c68-244">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="69c68-245">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="69c68-245">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="69c68-246">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="69c68-246">Search-Flags</span></span>           | <span data-ttu-id="69c68-247">0x00000000</span><span class="sxs-lookup"><span data-stu-id="69c68-247">0x00000000</span></span>                            |
| <span data-ttu-id="69c68-248">System-Flags</span><span class="sxs-lookup"><span data-stu-id="69c68-248">System-Flags</span></span>           | <span data-ttu-id="69c68-249">0x00000010</span><span class="sxs-lookup"><span data-stu-id="69c68-249">0x00000010</span></span>                            |
| <span data-ttu-id="69c68-250">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="69c68-250">Classes used in</span></span>        | [<span data-ttu-id="69c68-251">**Subnet**</span><span class="sxs-lookup"><span data-stu-id="69c68-251">**Subnet**</span></span>](c-subnet.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="69c68-252">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="69c68-252">Windows Server 2008 R2</span></span>



| <span data-ttu-id="69c68-253">Voce</span><span class="sxs-lookup"><span data-stu-id="69c68-253">Entry</span></span> | <span data-ttu-id="69c68-254">Valore</span><span class="sxs-lookup"><span data-stu-id="69c68-254">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="69c68-255">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="69c68-255">Link-Id</span></span>                | <span data-ttu-id="69c68-256">46</span><span class="sxs-lookup"><span data-stu-id="69c68-256">46</span></span>                                    |
| <span data-ttu-id="69c68-257">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="69c68-257">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="69c68-258">System-Only</span><span class="sxs-lookup"><span data-stu-id="69c68-258">System-Only</span></span>            | <span data-ttu-id="69c68-259">Falso</span><span class="sxs-lookup"><span data-stu-id="69c68-259">False</span></span>                                 |
| <span data-ttu-id="69c68-260">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="69c68-260">Is-Single-Valued</span></span>       | <span data-ttu-id="69c68-261">Vero</span><span class="sxs-lookup"><span data-stu-id="69c68-261">True</span></span>                                  |
| <span data-ttu-id="69c68-262">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="69c68-262">Is Indexed</span></span>             | <span data-ttu-id="69c68-263">Falso</span><span class="sxs-lookup"><span data-stu-id="69c68-263">False</span></span>                                 |
| <span data-ttu-id="69c68-264">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="69c68-264">In Global Catalog</span></span>      | <span data-ttu-id="69c68-265">Falso</span><span class="sxs-lookup"><span data-stu-id="69c68-265">False</span></span>                                 |
| <span data-ttu-id="69c68-266">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="69c68-266">NT-Security-Descriptor</span></span> | <span data-ttu-id="69c68-267">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="69c68-267">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="69c68-268">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="69c68-268">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="69c68-269">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="69c68-269">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="69c68-270">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="69c68-270">Search-Flags</span></span>           | <span data-ttu-id="69c68-271">0x00000000</span><span class="sxs-lookup"><span data-stu-id="69c68-271">0x00000000</span></span>                            |
| <span data-ttu-id="69c68-272">System-Flags</span><span class="sxs-lookup"><span data-stu-id="69c68-272">System-Flags</span></span>           | <span data-ttu-id="69c68-273">0x00000010</span><span class="sxs-lookup"><span data-stu-id="69c68-273">0x00000010</span></span>                            |
| <span data-ttu-id="69c68-274">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="69c68-274">Classes used in</span></span>        | [<span data-ttu-id="69c68-275">**Subnet**</span><span class="sxs-lookup"><span data-stu-id="69c68-275">**Subnet**</span></span>](c-subnet.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="69c68-276">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="69c68-276">Windows Server 2012</span></span>



| <span data-ttu-id="69c68-277">Voce</span><span class="sxs-lookup"><span data-stu-id="69c68-277">Entry</span></span> | <span data-ttu-id="69c68-278">Valore</span><span class="sxs-lookup"><span data-stu-id="69c68-278">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="69c68-279">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="69c68-279">Link-Id</span></span>                | <span data-ttu-id="69c68-280">46</span><span class="sxs-lookup"><span data-stu-id="69c68-280">46</span></span>                                    |
| <span data-ttu-id="69c68-281">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="69c68-281">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="69c68-282">System-Only</span><span class="sxs-lookup"><span data-stu-id="69c68-282">System-Only</span></span>            | <span data-ttu-id="69c68-283">Falso</span><span class="sxs-lookup"><span data-stu-id="69c68-283">False</span></span>                                 |
| <span data-ttu-id="69c68-284">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="69c68-284">Is-Single-Valued</span></span>       | <span data-ttu-id="69c68-285">Vero</span><span class="sxs-lookup"><span data-stu-id="69c68-285">True</span></span>                                  |
| <span data-ttu-id="69c68-286">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="69c68-286">Is Indexed</span></span>             | <span data-ttu-id="69c68-287">Falso</span><span class="sxs-lookup"><span data-stu-id="69c68-287">False</span></span>                                 |
| <span data-ttu-id="69c68-288">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="69c68-288">In Global Catalog</span></span>      | <span data-ttu-id="69c68-289">Falso</span><span class="sxs-lookup"><span data-stu-id="69c68-289">False</span></span>                                 |
| <span data-ttu-id="69c68-290">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="69c68-290">NT-Security-Descriptor</span></span> | <span data-ttu-id="69c68-291">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="69c68-291">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="69c68-292">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="69c68-292">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="69c68-293">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="69c68-293">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="69c68-294">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="69c68-294">Search-Flags</span></span>           | <span data-ttu-id="69c68-295">0x00000000</span><span class="sxs-lookup"><span data-stu-id="69c68-295">0x00000000</span></span>                            |
| <span data-ttu-id="69c68-296">System-Flags</span><span class="sxs-lookup"><span data-stu-id="69c68-296">System-Flags</span></span>           | <span data-ttu-id="69c68-297">0x00000010</span><span class="sxs-lookup"><span data-stu-id="69c68-297">0x00000010</span></span>                            |
| <span data-ttu-id="69c68-298">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="69c68-298">Classes used in</span></span>        | [<span data-ttu-id="69c68-299">**Subnet**</span><span class="sxs-lookup"><span data-stu-id="69c68-299">**Subnet**</span></span>](c-subnet.md)<br/> |



 

 





