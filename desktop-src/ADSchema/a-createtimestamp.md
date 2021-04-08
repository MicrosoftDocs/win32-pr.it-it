---
title: Attributo Create-Time-Stamp
description: Data di creazione dell'oggetto. Questo valore viene replicato.
ms.assetid: 7b957a44-7185-49fa-a219-7c7f4b3e9fce
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo Create-Time-Stamp
- Schema AD dell'attributo createTimeStamp
topic_type:
- apiref
api_name:
- Create-Time-Stamp
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f66714aeb035667bc858b7a2e888f6334e7d09c7
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103745266"
---
# <a name="create-time-stamp-attribute"></a><span data-ttu-id="fab2d-106">Attributo Create-Time-Stamp</span><span class="sxs-lookup"><span data-stu-id="fab2d-106">Create-Time-Stamp attribute</span></span>

<span data-ttu-id="fab2d-107">Data di creazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="fab2d-107">The date when this object was created.</span></span> <span data-ttu-id="fab2d-108">Questo valore viene replicato.</span><span class="sxs-lookup"><span data-stu-id="fab2d-108">This value is replicated.</span></span>



| <span data-ttu-id="fab2d-109">Voce</span><span class="sxs-lookup"><span data-stu-id="fab2d-109">Entry</span></span> | <span data-ttu-id="fab2d-110">Valore</span><span class="sxs-lookup"><span data-stu-id="fab2d-110">Value</span></span> |
|-------------------|---------------------------------------------------------------|
| <span data-ttu-id="fab2d-111">CN</span><span class="sxs-lookup"><span data-stu-id="fab2d-111">CN</span></span>                | <span data-ttu-id="fab2d-112">Creazione timestamp</span><span class="sxs-lookup"><span data-stu-id="fab2d-112">Create-Time-Stamp</span></span>                                             |
| <span data-ttu-id="fab2d-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="fab2d-113">Ldap-Display-Name</span></span> | <span data-ttu-id="fab2d-114">createTimeStamp</span><span class="sxs-lookup"><span data-stu-id="fab2d-114">createTimeStamp</span></span>                                               |
| <span data-ttu-id="fab2d-115">Dimensione</span><span class="sxs-lookup"><span data-stu-id="fab2d-115">Size</span></span>              | <span data-ttu-id="fab2d-116">8 byte</span><span class="sxs-lookup"><span data-stu-id="fab2d-116">8 bytes</span></span>                                                       |
| <span data-ttu-id="fab2d-117">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="fab2d-117">Update Privilege</span></span>  | <span data-ttu-id="fab2d-118">Questo valore viene impostato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="fab2d-118">This value is set by the system.</span></span>                              |
| <span data-ttu-id="fab2d-119">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="fab2d-119">Update Frequency</span></span>  | <span data-ttu-id="fab2d-120">Quando viene creato l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="fab2d-120">When the object is created.</span></span>                                   |
| <span data-ttu-id="fab2d-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="fab2d-121">Attribute-Id</span></span>      | <span data-ttu-id="fab2d-122">2.5.18.1</span><span class="sxs-lookup"><span data-stu-id="fab2d-122">2.5.18.1</span></span>                                                      |
| <span data-ttu-id="fab2d-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="fab2d-123">System-Id-Guid</span></span>    | <span data-ttu-id="fab2d-124">2df90d73-009f-11d2-aa4c-00c04fd7d83a</span><span class="sxs-lookup"><span data-stu-id="fab2d-124">2df90d73-009f-11d2-aa4c-00c04fd7d83a</span></span>                          |
| <span data-ttu-id="fab2d-125">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fab2d-125">Syntax</span></span>            | [<span data-ttu-id="fab2d-126">**String(Generalized-Time)**</span><span class="sxs-lookup"><span data-stu-id="fab2d-126">**String(Generalized-Time)**</span></span>](s-string-generalized-time.md) |



## <a name="implementations"></a><span data-ttu-id="fab2d-127">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="fab2d-127">Implementations</span></span>

-   [<span data-ttu-id="fab2d-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="fab2d-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="fab2d-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="fab2d-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="fab2d-130">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="fab2d-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="fab2d-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="fab2d-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="fab2d-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="fab2d-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="fab2d-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="fab2d-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="fab2d-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="fab2d-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="fab2d-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="fab2d-135">Windows 2000 Server</span></span>



| <span data-ttu-id="fab2d-136">Voce</span><span class="sxs-lookup"><span data-stu-id="fab2d-136">Entry</span></span> | <span data-ttu-id="fab2d-137">Valore</span><span class="sxs-lookup"><span data-stu-id="fab2d-137">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="fab2d-138">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="fab2d-138">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="fab2d-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fab2d-139">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="fab2d-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="fab2d-140">System-Only</span></span>            | <span data-ttu-id="fab2d-141">Vero</span><span class="sxs-lookup"><span data-stu-id="fab2d-141">True</span></span>                            |
| <span data-ttu-id="fab2d-142">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="fab2d-142">Is-Single-Valued</span></span>       | <span data-ttu-id="fab2d-143">Vero</span><span class="sxs-lookup"><span data-stu-id="fab2d-143">True</span></span>                            |
| <span data-ttu-id="fab2d-144">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="fab2d-144">Is Indexed</span></span>             | <span data-ttu-id="fab2d-145">Falso</span><span class="sxs-lookup"><span data-stu-id="fab2d-145">False</span></span>                           |
| <span data-ttu-id="fab2d-146">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="fab2d-146">In Global Catalog</span></span>      | <span data-ttu-id="fab2d-147">Falso</span><span class="sxs-lookup"><span data-stu-id="fab2d-147">False</span></span>                           |
| <span data-ttu-id="fab2d-148">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="fab2d-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="fab2d-149">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="fab2d-149">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="fab2d-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fab2d-150">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="fab2d-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fab2d-151">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="fab2d-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fab2d-152">Search-Flags</span></span>           | <span data-ttu-id="fab2d-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fab2d-153">0x00000000</span></span>                      |
| <span data-ttu-id="fab2d-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fab2d-154">System-Flags</span></span>           | <span data-ttu-id="fab2d-155">0x08000014</span><span class="sxs-lookup"><span data-stu-id="fab2d-155">0x08000014</span></span>                      |
| <span data-ttu-id="fab2d-156">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="fab2d-156">Classes used in</span></span>        | [<span data-ttu-id="fab2d-157">**In alto**</span><span class="sxs-lookup"><span data-stu-id="fab2d-157">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="fab2d-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="fab2d-158">Windows Server 2003</span></span>



| <span data-ttu-id="fab2d-159">Voce</span><span class="sxs-lookup"><span data-stu-id="fab2d-159">Entry</span></span> | <span data-ttu-id="fab2d-160">Valore</span><span class="sxs-lookup"><span data-stu-id="fab2d-160">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="fab2d-161">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="fab2d-161">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="fab2d-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fab2d-162">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="fab2d-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="fab2d-163">System-Only</span></span>            | <span data-ttu-id="fab2d-164">Vero</span><span class="sxs-lookup"><span data-stu-id="fab2d-164">True</span></span>                            |
| <span data-ttu-id="fab2d-165">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="fab2d-165">Is-Single-Valued</span></span>       | <span data-ttu-id="fab2d-166">Vero</span><span class="sxs-lookup"><span data-stu-id="fab2d-166">True</span></span>                            |
| <span data-ttu-id="fab2d-167">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="fab2d-167">Is Indexed</span></span>             | <span data-ttu-id="fab2d-168">Falso</span><span class="sxs-lookup"><span data-stu-id="fab2d-168">False</span></span>                           |
| <span data-ttu-id="fab2d-169">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="fab2d-169">In Global Catalog</span></span>      | <span data-ttu-id="fab2d-170">Falso</span><span class="sxs-lookup"><span data-stu-id="fab2d-170">False</span></span>                           |
| <span data-ttu-id="fab2d-171">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="fab2d-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="fab2d-172">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="fab2d-172">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="fab2d-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fab2d-173">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="fab2d-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fab2d-174">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="fab2d-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fab2d-175">Search-Flags</span></span>           | <span data-ttu-id="fab2d-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fab2d-176">0x00000000</span></span>                      |
| <span data-ttu-id="fab2d-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fab2d-177">System-Flags</span></span>           | <span data-ttu-id="fab2d-178">0x08000014</span><span class="sxs-lookup"><span data-stu-id="fab2d-178">0x08000014</span></span>                      |
| <span data-ttu-id="fab2d-179">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="fab2d-179">Classes used in</span></span>        | [<span data-ttu-id="fab2d-180">**In alto**</span><span class="sxs-lookup"><span data-stu-id="fab2d-180">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="fab2d-181">ADAM</span><span class="sxs-lookup"><span data-stu-id="fab2d-181">ADAM</span></span>



| <span data-ttu-id="fab2d-182">Voce</span><span class="sxs-lookup"><span data-stu-id="fab2d-182">Entry</span></span> | <span data-ttu-id="fab2d-183">Valore</span><span class="sxs-lookup"><span data-stu-id="fab2d-183">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="fab2d-184">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="fab2d-184">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="fab2d-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fab2d-185">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="fab2d-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="fab2d-186">System-Only</span></span>            | <span data-ttu-id="fab2d-187">Vero</span><span class="sxs-lookup"><span data-stu-id="fab2d-187">True</span></span>                            |
| <span data-ttu-id="fab2d-188">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="fab2d-188">Is-Single-Valued</span></span>       | <span data-ttu-id="fab2d-189">Vero</span><span class="sxs-lookup"><span data-stu-id="fab2d-189">True</span></span>                            |
| <span data-ttu-id="fab2d-190">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="fab2d-190">Is Indexed</span></span>             | <span data-ttu-id="fab2d-191">Falso</span><span class="sxs-lookup"><span data-stu-id="fab2d-191">False</span></span>                           |
| <span data-ttu-id="fab2d-192">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="fab2d-192">In Global Catalog</span></span>      | <span data-ttu-id="fab2d-193">Falso</span><span class="sxs-lookup"><span data-stu-id="fab2d-193">False</span></span>                           |
| <span data-ttu-id="fab2d-194">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="fab2d-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="fab2d-195">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="fab2d-195">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="fab2d-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fab2d-196">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="fab2d-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fab2d-197">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="fab2d-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fab2d-198">Search-Flags</span></span>           | <span data-ttu-id="fab2d-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fab2d-199">0x00000000</span></span>                      |
| <span data-ttu-id="fab2d-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fab2d-200">System-Flags</span></span>           | <span data-ttu-id="fab2d-201">0x08000014</span><span class="sxs-lookup"><span data-stu-id="fab2d-201">0x08000014</span></span>                      |
| <span data-ttu-id="fab2d-202">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="fab2d-202">Classes used in</span></span>        | [<span data-ttu-id="fab2d-203">**In alto**</span><span class="sxs-lookup"><span data-stu-id="fab2d-203">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="fab2d-204">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="fab2d-204">Windows Server 2003 R2</span></span>



| <span data-ttu-id="fab2d-205">Voce</span><span class="sxs-lookup"><span data-stu-id="fab2d-205">Entry</span></span> | <span data-ttu-id="fab2d-206">Valore</span><span class="sxs-lookup"><span data-stu-id="fab2d-206">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="fab2d-207">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="fab2d-207">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="fab2d-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fab2d-208">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="fab2d-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="fab2d-209">System-Only</span></span>            | <span data-ttu-id="fab2d-210">Vero</span><span class="sxs-lookup"><span data-stu-id="fab2d-210">True</span></span>                            |
| <span data-ttu-id="fab2d-211">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="fab2d-211">Is-Single-Valued</span></span>       | <span data-ttu-id="fab2d-212">Vero</span><span class="sxs-lookup"><span data-stu-id="fab2d-212">True</span></span>                            |
| <span data-ttu-id="fab2d-213">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="fab2d-213">Is Indexed</span></span>             | <span data-ttu-id="fab2d-214">Falso</span><span class="sxs-lookup"><span data-stu-id="fab2d-214">False</span></span>                           |
| <span data-ttu-id="fab2d-215">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="fab2d-215">In Global Catalog</span></span>      | <span data-ttu-id="fab2d-216">Falso</span><span class="sxs-lookup"><span data-stu-id="fab2d-216">False</span></span>                           |
| <span data-ttu-id="fab2d-217">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="fab2d-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="fab2d-218">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="fab2d-218">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="fab2d-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fab2d-219">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="fab2d-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fab2d-220">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="fab2d-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fab2d-221">Search-Flags</span></span>           | <span data-ttu-id="fab2d-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fab2d-222">0x00000000</span></span>                      |
| <span data-ttu-id="fab2d-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fab2d-223">System-Flags</span></span>           | <span data-ttu-id="fab2d-224">0x08000014</span><span class="sxs-lookup"><span data-stu-id="fab2d-224">0x08000014</span></span>                      |
| <span data-ttu-id="fab2d-225">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="fab2d-225">Classes used in</span></span>        | [<span data-ttu-id="fab2d-226">**In alto**</span><span class="sxs-lookup"><span data-stu-id="fab2d-226">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="fab2d-227">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fab2d-227">Windows Server 2008</span></span>



| <span data-ttu-id="fab2d-228">Voce</span><span class="sxs-lookup"><span data-stu-id="fab2d-228">Entry</span></span> | <span data-ttu-id="fab2d-229">Valore</span><span class="sxs-lookup"><span data-stu-id="fab2d-229">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="fab2d-230">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="fab2d-230">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="fab2d-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fab2d-231">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="fab2d-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="fab2d-232">System-Only</span></span>            | <span data-ttu-id="fab2d-233">Vero</span><span class="sxs-lookup"><span data-stu-id="fab2d-233">True</span></span>                            |
| <span data-ttu-id="fab2d-234">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="fab2d-234">Is-Single-Valued</span></span>       | <span data-ttu-id="fab2d-235">Vero</span><span class="sxs-lookup"><span data-stu-id="fab2d-235">True</span></span>                            |
| <span data-ttu-id="fab2d-236">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="fab2d-236">Is Indexed</span></span>             | <span data-ttu-id="fab2d-237">Falso</span><span class="sxs-lookup"><span data-stu-id="fab2d-237">False</span></span>                           |
| <span data-ttu-id="fab2d-238">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="fab2d-238">In Global Catalog</span></span>      | <span data-ttu-id="fab2d-239">Falso</span><span class="sxs-lookup"><span data-stu-id="fab2d-239">False</span></span>                           |
| <span data-ttu-id="fab2d-240">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="fab2d-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="fab2d-241">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="fab2d-241">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="fab2d-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fab2d-242">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="fab2d-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fab2d-243">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="fab2d-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fab2d-244">Search-Flags</span></span>           | <span data-ttu-id="fab2d-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fab2d-245">0x00000000</span></span>                      |
| <span data-ttu-id="fab2d-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fab2d-246">System-Flags</span></span>           | <span data-ttu-id="fab2d-247">0x08000014</span><span class="sxs-lookup"><span data-stu-id="fab2d-247">0x08000014</span></span>                      |
| <span data-ttu-id="fab2d-248">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="fab2d-248">Classes used in</span></span>        | [<span data-ttu-id="fab2d-249">**In alto**</span><span class="sxs-lookup"><span data-stu-id="fab2d-249">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="fab2d-250">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="fab2d-250">Windows Server 2008 R2</span></span>



| <span data-ttu-id="fab2d-251">Voce</span><span class="sxs-lookup"><span data-stu-id="fab2d-251">Entry</span></span> | <span data-ttu-id="fab2d-252">Valore</span><span class="sxs-lookup"><span data-stu-id="fab2d-252">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="fab2d-253">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="fab2d-253">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="fab2d-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fab2d-254">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="fab2d-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="fab2d-255">System-Only</span></span>            | <span data-ttu-id="fab2d-256">Vero</span><span class="sxs-lookup"><span data-stu-id="fab2d-256">True</span></span>                            |
| <span data-ttu-id="fab2d-257">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="fab2d-257">Is-Single-Valued</span></span>       | <span data-ttu-id="fab2d-258">Vero</span><span class="sxs-lookup"><span data-stu-id="fab2d-258">True</span></span>                            |
| <span data-ttu-id="fab2d-259">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="fab2d-259">Is Indexed</span></span>             | <span data-ttu-id="fab2d-260">Falso</span><span class="sxs-lookup"><span data-stu-id="fab2d-260">False</span></span>                           |
| <span data-ttu-id="fab2d-261">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="fab2d-261">In Global Catalog</span></span>      | <span data-ttu-id="fab2d-262">Falso</span><span class="sxs-lookup"><span data-stu-id="fab2d-262">False</span></span>                           |
| <span data-ttu-id="fab2d-263">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="fab2d-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="fab2d-264">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="fab2d-264">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="fab2d-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fab2d-265">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="fab2d-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fab2d-266">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="fab2d-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fab2d-267">Search-Flags</span></span>           | <span data-ttu-id="fab2d-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fab2d-268">0x00000000</span></span>                      |
| <span data-ttu-id="fab2d-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fab2d-269">System-Flags</span></span>           | <span data-ttu-id="fab2d-270">0x08000014</span><span class="sxs-lookup"><span data-stu-id="fab2d-270">0x08000014</span></span>                      |
| <span data-ttu-id="fab2d-271">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="fab2d-271">Classes used in</span></span>        | [<span data-ttu-id="fab2d-272">**In alto**</span><span class="sxs-lookup"><span data-stu-id="fab2d-272">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="fab2d-273">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="fab2d-273">Windows Server 2012</span></span>



| <span data-ttu-id="fab2d-274">Voce</span><span class="sxs-lookup"><span data-stu-id="fab2d-274">Entry</span></span> | <span data-ttu-id="fab2d-275">Valore</span><span class="sxs-lookup"><span data-stu-id="fab2d-275">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="fab2d-276">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="fab2d-276">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="fab2d-277">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fab2d-277">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="fab2d-278">System-Only</span><span class="sxs-lookup"><span data-stu-id="fab2d-278">System-Only</span></span>            | <span data-ttu-id="fab2d-279">Vero</span><span class="sxs-lookup"><span data-stu-id="fab2d-279">True</span></span>                            |
| <span data-ttu-id="fab2d-280">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="fab2d-280">Is-Single-Valued</span></span>       | <span data-ttu-id="fab2d-281">Vero</span><span class="sxs-lookup"><span data-stu-id="fab2d-281">True</span></span>                            |
| <span data-ttu-id="fab2d-282">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="fab2d-282">Is Indexed</span></span>             | <span data-ttu-id="fab2d-283">Falso</span><span class="sxs-lookup"><span data-stu-id="fab2d-283">False</span></span>                           |
| <span data-ttu-id="fab2d-284">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="fab2d-284">In Global Catalog</span></span>      | <span data-ttu-id="fab2d-285">Falso</span><span class="sxs-lookup"><span data-stu-id="fab2d-285">False</span></span>                           |
| <span data-ttu-id="fab2d-286">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="fab2d-286">NT-Security-Descriptor</span></span> | <span data-ttu-id="fab2d-287">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="fab2d-287">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="fab2d-288">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fab2d-288">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="fab2d-289">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fab2d-289">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="fab2d-290">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fab2d-290">Search-Flags</span></span>           | <span data-ttu-id="fab2d-291">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fab2d-291">0x00000000</span></span>                      |
| <span data-ttu-id="fab2d-292">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fab2d-292">System-Flags</span></span>           | <span data-ttu-id="fab2d-293">0x08000014</span><span class="sxs-lookup"><span data-stu-id="fab2d-293">0x08000014</span></span>                      |
| <span data-ttu-id="fab2d-294">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="fab2d-294">Classes used in</span></span>        | [<span data-ttu-id="fab2d-295">**In alto**</span><span class="sxs-lookup"><span data-stu-id="fab2d-295">**Top**</span></span>](c-top.md)<br/> |



 

 





