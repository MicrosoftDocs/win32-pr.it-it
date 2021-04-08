---
title: Site-GUID (attributo)
description: Identificatore univoco per un sito.
ms.assetid: 1baa967e-5aa3-495f-aa4f-14eac74f70e4
ms.tgt_platform: multiple
keywords:
- Attributo site-GUID-schema AD
- Schema AD dell'attributo siteGUID
topic_type:
- apiref
api_name:
- Site-GUID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3932eb2ced2fe14480010c1120266619cc34456
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103965193"
---
# <a name="site-guid-attribute"></a><span data-ttu-id="ef6cd-105">Site-GUID (attributo)</span><span class="sxs-lookup"><span data-stu-id="ef6cd-105">Site-GUID attribute</span></span>

<span data-ttu-id="ef6cd-106">Identificatore univoco per un sito.</span><span class="sxs-lookup"><span data-stu-id="ef6cd-106">The unique identifier for a site.</span></span>



| <span data-ttu-id="ef6cd-107">Voce</span><span class="sxs-lookup"><span data-stu-id="ef6cd-107">Entry</span></span> | <span data-ttu-id="ef6cd-108">Valore</span><span class="sxs-lookup"><span data-stu-id="ef6cd-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="ef6cd-109">CN</span><span class="sxs-lookup"><span data-stu-id="ef6cd-109">CN</span></span>                | <span data-ttu-id="ef6cd-110">GUID sito</span><span class="sxs-lookup"><span data-stu-id="ef6cd-110">Site-GUID</span></span>                                             |
| <span data-ttu-id="ef6cd-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="ef6cd-111">Ldap-Display-Name</span></span> | <span data-ttu-id="ef6cd-112">siteGUID</span><span class="sxs-lookup"><span data-stu-id="ef6cd-112">siteGUID</span></span>                                              |
| <span data-ttu-id="ef6cd-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="ef6cd-113">Size</span></span>              | <span data-ttu-id="ef6cd-114">16 byte</span><span class="sxs-lookup"><span data-stu-id="ef6cd-114">16 bytes</span></span>                                              |
| <span data-ttu-id="ef6cd-115">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="ef6cd-115">Update Privilege</span></span>  | <span data-ttu-id="ef6cd-116">Questo valore viene impostato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="ef6cd-116">This value is set by the system.</span></span>                      |
| <span data-ttu-id="ef6cd-117">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="ef6cd-117">Update Frequency</span></span>  | <span data-ttu-id="ef6cd-118">Ogni volta che viene creato un nuovo sito.</span><span class="sxs-lookup"><span data-stu-id="ef6cd-118">Whenever a new site is created.</span></span>                       |
| <span data-ttu-id="ef6cd-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ef6cd-119">Attribute-Id</span></span>      | <span data-ttu-id="ef6cd-120">1.2.840.113556.1.4.362</span><span class="sxs-lookup"><span data-stu-id="ef6cd-120">1.2.840.113556.1.4.362</span></span>                                |
| <span data-ttu-id="ef6cd-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="ef6cd-121">System-Id-Guid</span></span>    | <span data-ttu-id="ef6cd-122">3e978924-8c01-11d0-afda-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="ef6cd-122">3e978924-8c01-11d0-afda-00c04fd930c9</span></span>                  |
| <span data-ttu-id="ef6cd-123">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ef6cd-123">Syntax</span></span>            | [<span data-ttu-id="ef6cd-124">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="ef6cd-124">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="ef6cd-125">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="ef6cd-125">Implementations</span></span>

-   [<span data-ttu-id="ef6cd-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="ef6cd-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="ef6cd-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ef6cd-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ef6cd-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ef6cd-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ef6cd-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ef6cd-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ef6cd-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ef6cd-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ef6cd-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ef6cd-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="ef6cd-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ef6cd-132">Windows 2000 Server</span></span>



| <span data-ttu-id="ef6cd-133">Voce</span><span class="sxs-lookup"><span data-stu-id="ef6cd-133">Entry</span></span> | <span data-ttu-id="ef6cd-134">Valore</span><span class="sxs-lookup"><span data-stu-id="ef6cd-134">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="ef6cd-135">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="ef6cd-135">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="ef6cd-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ef6cd-136">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="ef6cd-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="ef6cd-137">System-Only</span></span>            | <span data-ttu-id="ef6cd-138">Falso</span><span class="sxs-lookup"><span data-stu-id="ef6cd-138">False</span></span>                                     |
| <span data-ttu-id="ef6cd-139">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="ef6cd-139">Is-Single-Valued</span></span>       | <span data-ttu-id="ef6cd-140">Vero</span><span class="sxs-lookup"><span data-stu-id="ef6cd-140">True</span></span>                                      |
| <span data-ttu-id="ef6cd-141">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="ef6cd-141">Is Indexed</span></span>             | <span data-ttu-id="ef6cd-142">Falso</span><span class="sxs-lookup"><span data-stu-id="ef6cd-142">False</span></span>                                     |
| <span data-ttu-id="ef6cd-143">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="ef6cd-143">In Global Catalog</span></span>      | <span data-ttu-id="ef6cd-144">Falso</span><span class="sxs-lookup"><span data-stu-id="ef6cd-144">False</span></span>                                     |
| <span data-ttu-id="ef6cd-145">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="ef6cd-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="ef6cd-146">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="ef6cd-146">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="ef6cd-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ef6cd-147">Range-Lower</span></span>            | <span data-ttu-id="ef6cd-148">16</span><span class="sxs-lookup"><span data-stu-id="ef6cd-148">16</span></span>                                        |
| <span data-ttu-id="ef6cd-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ef6cd-149">Range-Upper</span></span>            | <span data-ttu-id="ef6cd-150">16</span><span class="sxs-lookup"><span data-stu-id="ef6cd-150">16</span></span>                                        |
| <span data-ttu-id="ef6cd-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ef6cd-151">Search-Flags</span></span>           | <span data-ttu-id="ef6cd-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ef6cd-152">0x00000000</span></span>                                |
| <span data-ttu-id="ef6cd-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ef6cd-153">System-Flags</span></span>           | <span data-ttu-id="ef6cd-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ef6cd-154">0x00000010</span></span>                                |
| <span data-ttu-id="ef6cd-155">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="ef6cd-155">Classes used in</span></span>        | [<span data-ttu-id="ef6cd-156">**Computer**</span><span class="sxs-lookup"><span data-stu-id="ef6cd-156">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="ef6cd-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ef6cd-157">Windows Server 2003</span></span>



| <span data-ttu-id="ef6cd-158">Voce</span><span class="sxs-lookup"><span data-stu-id="ef6cd-158">Entry</span></span> | <span data-ttu-id="ef6cd-159">Valore</span><span class="sxs-lookup"><span data-stu-id="ef6cd-159">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="ef6cd-160">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="ef6cd-160">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="ef6cd-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ef6cd-161">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="ef6cd-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="ef6cd-162">System-Only</span></span>            | <span data-ttu-id="ef6cd-163">Falso</span><span class="sxs-lookup"><span data-stu-id="ef6cd-163">False</span></span>                                     |
| <span data-ttu-id="ef6cd-164">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="ef6cd-164">Is-Single-Valued</span></span>       | <span data-ttu-id="ef6cd-165">Vero</span><span class="sxs-lookup"><span data-stu-id="ef6cd-165">True</span></span>                                      |
| <span data-ttu-id="ef6cd-166">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="ef6cd-166">Is Indexed</span></span>             | <span data-ttu-id="ef6cd-167">Falso</span><span class="sxs-lookup"><span data-stu-id="ef6cd-167">False</span></span>                                     |
| <span data-ttu-id="ef6cd-168">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="ef6cd-168">In Global Catalog</span></span>      | <span data-ttu-id="ef6cd-169">Falso</span><span class="sxs-lookup"><span data-stu-id="ef6cd-169">False</span></span>                                     |
| <span data-ttu-id="ef6cd-170">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="ef6cd-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="ef6cd-171">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="ef6cd-171">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="ef6cd-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ef6cd-172">Range-Lower</span></span>            | <span data-ttu-id="ef6cd-173">16</span><span class="sxs-lookup"><span data-stu-id="ef6cd-173">16</span></span>                                        |
| <span data-ttu-id="ef6cd-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ef6cd-174">Range-Upper</span></span>            | <span data-ttu-id="ef6cd-175">16</span><span class="sxs-lookup"><span data-stu-id="ef6cd-175">16</span></span>                                        |
| <span data-ttu-id="ef6cd-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ef6cd-176">Search-Flags</span></span>           | <span data-ttu-id="ef6cd-177">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ef6cd-177">0x00000000</span></span>                                |
| <span data-ttu-id="ef6cd-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ef6cd-178">System-Flags</span></span>           | <span data-ttu-id="ef6cd-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ef6cd-179">0x00000010</span></span>                                |
| <span data-ttu-id="ef6cd-180">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="ef6cd-180">Classes used in</span></span>        | [<span data-ttu-id="ef6cd-181">**Computer**</span><span class="sxs-lookup"><span data-stu-id="ef6cd-181">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ef6cd-182">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ef6cd-182">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ef6cd-183">Voce</span><span class="sxs-lookup"><span data-stu-id="ef6cd-183">Entry</span></span> | <span data-ttu-id="ef6cd-184">Valore</span><span class="sxs-lookup"><span data-stu-id="ef6cd-184">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="ef6cd-185">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="ef6cd-185">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="ef6cd-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ef6cd-186">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="ef6cd-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="ef6cd-187">System-Only</span></span>            | <span data-ttu-id="ef6cd-188">Falso</span><span class="sxs-lookup"><span data-stu-id="ef6cd-188">False</span></span>                                     |
| <span data-ttu-id="ef6cd-189">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="ef6cd-189">Is-Single-Valued</span></span>       | <span data-ttu-id="ef6cd-190">Vero</span><span class="sxs-lookup"><span data-stu-id="ef6cd-190">True</span></span>                                      |
| <span data-ttu-id="ef6cd-191">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="ef6cd-191">Is Indexed</span></span>             | <span data-ttu-id="ef6cd-192">Falso</span><span class="sxs-lookup"><span data-stu-id="ef6cd-192">False</span></span>                                     |
| <span data-ttu-id="ef6cd-193">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="ef6cd-193">In Global Catalog</span></span>      | <span data-ttu-id="ef6cd-194">Falso</span><span class="sxs-lookup"><span data-stu-id="ef6cd-194">False</span></span>                                     |
| <span data-ttu-id="ef6cd-195">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="ef6cd-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="ef6cd-196">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="ef6cd-196">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="ef6cd-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ef6cd-197">Range-Lower</span></span>            | <span data-ttu-id="ef6cd-198">16</span><span class="sxs-lookup"><span data-stu-id="ef6cd-198">16</span></span>                                        |
| <span data-ttu-id="ef6cd-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ef6cd-199">Range-Upper</span></span>            | <span data-ttu-id="ef6cd-200">16</span><span class="sxs-lookup"><span data-stu-id="ef6cd-200">16</span></span>                                        |
| <span data-ttu-id="ef6cd-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ef6cd-201">Search-Flags</span></span>           | <span data-ttu-id="ef6cd-202">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ef6cd-202">0x00000000</span></span>                                |
| <span data-ttu-id="ef6cd-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ef6cd-203">System-Flags</span></span>           | <span data-ttu-id="ef6cd-204">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ef6cd-204">0x00000010</span></span>                                |
| <span data-ttu-id="ef6cd-205">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="ef6cd-205">Classes used in</span></span>        | [<span data-ttu-id="ef6cd-206">**Computer**</span><span class="sxs-lookup"><span data-stu-id="ef6cd-206">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ef6cd-207">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ef6cd-207">Windows Server 2008</span></span>



| <span data-ttu-id="ef6cd-208">Voce</span><span class="sxs-lookup"><span data-stu-id="ef6cd-208">Entry</span></span> | <span data-ttu-id="ef6cd-209">Valore</span><span class="sxs-lookup"><span data-stu-id="ef6cd-209">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="ef6cd-210">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="ef6cd-210">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="ef6cd-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ef6cd-211">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="ef6cd-212">System-Only</span><span class="sxs-lookup"><span data-stu-id="ef6cd-212">System-Only</span></span>            | <span data-ttu-id="ef6cd-213">Falso</span><span class="sxs-lookup"><span data-stu-id="ef6cd-213">False</span></span>                                     |
| <span data-ttu-id="ef6cd-214">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="ef6cd-214">Is-Single-Valued</span></span>       | <span data-ttu-id="ef6cd-215">Vero</span><span class="sxs-lookup"><span data-stu-id="ef6cd-215">True</span></span>                                      |
| <span data-ttu-id="ef6cd-216">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="ef6cd-216">Is Indexed</span></span>             | <span data-ttu-id="ef6cd-217">Falso</span><span class="sxs-lookup"><span data-stu-id="ef6cd-217">False</span></span>                                     |
| <span data-ttu-id="ef6cd-218">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="ef6cd-218">In Global Catalog</span></span>      | <span data-ttu-id="ef6cd-219">Falso</span><span class="sxs-lookup"><span data-stu-id="ef6cd-219">False</span></span>                                     |
| <span data-ttu-id="ef6cd-220">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="ef6cd-220">NT-Security-Descriptor</span></span> | <span data-ttu-id="ef6cd-221">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="ef6cd-221">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="ef6cd-222">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ef6cd-222">Range-Lower</span></span>            | <span data-ttu-id="ef6cd-223">16</span><span class="sxs-lookup"><span data-stu-id="ef6cd-223">16</span></span>                                        |
| <span data-ttu-id="ef6cd-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ef6cd-224">Range-Upper</span></span>            | <span data-ttu-id="ef6cd-225">16</span><span class="sxs-lookup"><span data-stu-id="ef6cd-225">16</span></span>                                        |
| <span data-ttu-id="ef6cd-226">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ef6cd-226">Search-Flags</span></span>           | <span data-ttu-id="ef6cd-227">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ef6cd-227">0x00000000</span></span>                                |
| <span data-ttu-id="ef6cd-228">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ef6cd-228">System-Flags</span></span>           | <span data-ttu-id="ef6cd-229">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ef6cd-229">0x00000010</span></span>                                |
| <span data-ttu-id="ef6cd-230">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="ef6cd-230">Classes used in</span></span>        | [<span data-ttu-id="ef6cd-231">**Computer**</span><span class="sxs-lookup"><span data-stu-id="ef6cd-231">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ef6cd-232">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ef6cd-232">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ef6cd-233">Voce</span><span class="sxs-lookup"><span data-stu-id="ef6cd-233">Entry</span></span> | <span data-ttu-id="ef6cd-234">Valore</span><span class="sxs-lookup"><span data-stu-id="ef6cd-234">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="ef6cd-235">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="ef6cd-235">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="ef6cd-236">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ef6cd-236">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="ef6cd-237">System-Only</span><span class="sxs-lookup"><span data-stu-id="ef6cd-237">System-Only</span></span>            | <span data-ttu-id="ef6cd-238">Falso</span><span class="sxs-lookup"><span data-stu-id="ef6cd-238">False</span></span>                                     |
| <span data-ttu-id="ef6cd-239">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="ef6cd-239">Is-Single-Valued</span></span>       | <span data-ttu-id="ef6cd-240">Vero</span><span class="sxs-lookup"><span data-stu-id="ef6cd-240">True</span></span>                                      |
| <span data-ttu-id="ef6cd-241">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="ef6cd-241">Is Indexed</span></span>             | <span data-ttu-id="ef6cd-242">Falso</span><span class="sxs-lookup"><span data-stu-id="ef6cd-242">False</span></span>                                     |
| <span data-ttu-id="ef6cd-243">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="ef6cd-243">In Global Catalog</span></span>      | <span data-ttu-id="ef6cd-244">Falso</span><span class="sxs-lookup"><span data-stu-id="ef6cd-244">False</span></span>                                     |
| <span data-ttu-id="ef6cd-245">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="ef6cd-245">NT-Security-Descriptor</span></span> | <span data-ttu-id="ef6cd-246">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="ef6cd-246">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="ef6cd-247">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ef6cd-247">Range-Lower</span></span>            | <span data-ttu-id="ef6cd-248">16</span><span class="sxs-lookup"><span data-stu-id="ef6cd-248">16</span></span>                                        |
| <span data-ttu-id="ef6cd-249">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ef6cd-249">Range-Upper</span></span>            | <span data-ttu-id="ef6cd-250">16</span><span class="sxs-lookup"><span data-stu-id="ef6cd-250">16</span></span>                                        |
| <span data-ttu-id="ef6cd-251">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ef6cd-251">Search-Flags</span></span>           | <span data-ttu-id="ef6cd-252">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ef6cd-252">0x00000000</span></span>                                |
| <span data-ttu-id="ef6cd-253">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ef6cd-253">System-Flags</span></span>           | <span data-ttu-id="ef6cd-254">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ef6cd-254">0x00000010</span></span>                                |
| <span data-ttu-id="ef6cd-255">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="ef6cd-255">Classes used in</span></span>        | [<span data-ttu-id="ef6cd-256">**Computer**</span><span class="sxs-lookup"><span data-stu-id="ef6cd-256">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ef6cd-257">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ef6cd-257">Windows Server 2012</span></span>



| <span data-ttu-id="ef6cd-258">Voce</span><span class="sxs-lookup"><span data-stu-id="ef6cd-258">Entry</span></span> | <span data-ttu-id="ef6cd-259">Valore</span><span class="sxs-lookup"><span data-stu-id="ef6cd-259">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="ef6cd-260">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="ef6cd-260">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="ef6cd-261">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ef6cd-261">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="ef6cd-262">System-Only</span><span class="sxs-lookup"><span data-stu-id="ef6cd-262">System-Only</span></span>            | <span data-ttu-id="ef6cd-263">Falso</span><span class="sxs-lookup"><span data-stu-id="ef6cd-263">False</span></span>                                     |
| <span data-ttu-id="ef6cd-264">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="ef6cd-264">Is-Single-Valued</span></span>       | <span data-ttu-id="ef6cd-265">Vero</span><span class="sxs-lookup"><span data-stu-id="ef6cd-265">True</span></span>                                      |
| <span data-ttu-id="ef6cd-266">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="ef6cd-266">Is Indexed</span></span>             | <span data-ttu-id="ef6cd-267">Falso</span><span class="sxs-lookup"><span data-stu-id="ef6cd-267">False</span></span>                                     |
| <span data-ttu-id="ef6cd-268">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="ef6cd-268">In Global Catalog</span></span>      | <span data-ttu-id="ef6cd-269">Falso</span><span class="sxs-lookup"><span data-stu-id="ef6cd-269">False</span></span>                                     |
| <span data-ttu-id="ef6cd-270">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="ef6cd-270">NT-Security-Descriptor</span></span> | <span data-ttu-id="ef6cd-271">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="ef6cd-271">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="ef6cd-272">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ef6cd-272">Range-Lower</span></span>            | <span data-ttu-id="ef6cd-273">16</span><span class="sxs-lookup"><span data-stu-id="ef6cd-273">16</span></span>                                        |
| <span data-ttu-id="ef6cd-274">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ef6cd-274">Range-Upper</span></span>            | <span data-ttu-id="ef6cd-275">16</span><span class="sxs-lookup"><span data-stu-id="ef6cd-275">16</span></span>                                        |
| <span data-ttu-id="ef6cd-276">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ef6cd-276">Search-Flags</span></span>           | <span data-ttu-id="ef6cd-277">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ef6cd-277">0x00000000</span></span>                                |
| <span data-ttu-id="ef6cd-278">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ef6cd-278">System-Flags</span></span>           | <span data-ttu-id="ef6cd-279">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ef6cd-279">0x00000010</span></span>                                |
| <span data-ttu-id="ef6cd-280">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="ef6cd-280">Classes used in</span></span>        | [<span data-ttu-id="ef6cd-281">**Computer**</span><span class="sxs-lookup"><span data-stu-id="ef6cd-281">**Computer**</span></span>](c-computer.md)<br/> |



 

 





