---
title: Attributo per il GUID
description: Avvio senza dischi di un GUID del computer. Corrisponde all'indirizzo MAC della scheda di rete del computer.
ms.assetid: 60ce0482-79a3-499a-9607-f1f496e297d0
ms.tgt_platform: multiple
keywords:
- Schema di AD per l'attributo-GUID
- Schema AD dell'attributo netbootGUID
topic_type:
- apiref
api_name:
- Netboot-GUID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7c09d6f9139580ad329b47f13999d348abf5a87
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103875614"
---
# <a name="netboot-guid-attribute"></a><span data-ttu-id="13999-106">Attributo per il GUID</span><span class="sxs-lookup"><span data-stu-id="13999-106">Netboot-GUID attribute</span></span>

<span data-ttu-id="13999-107">Avvio senza dischi: GUID a bordo di un computer.</span><span class="sxs-lookup"><span data-stu-id="13999-107">Diskless boot: A computer's on-board GUID.</span></span> <span data-ttu-id="13999-108">Corrisponde all'indirizzo MAC della scheda di rete del computer.</span><span class="sxs-lookup"><span data-stu-id="13999-108">Corresponds to the computer's network card MAC address.</span></span>



| <span data-ttu-id="13999-109">Voce</span><span class="sxs-lookup"><span data-stu-id="13999-109">Entry</span></span> | <span data-ttu-id="13999-110">Valore</span><span class="sxs-lookup"><span data-stu-id="13999-110">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="13999-111">CN</span><span class="sxs-lookup"><span data-stu-id="13999-111">CN</span></span>                | <span data-ttu-id="13999-112">-GUID</span><span class="sxs-lookup"><span data-stu-id="13999-112">Netboot-GUID</span></span>                                          |
| <span data-ttu-id="13999-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="13999-113">Ldap-Display-Name</span></span> | <span data-ttu-id="13999-114">netbootGUID</span><span class="sxs-lookup"><span data-stu-id="13999-114">netbootGUID</span></span>                                           |
| <span data-ttu-id="13999-115">Dimensione</span><span class="sxs-lookup"><span data-stu-id="13999-115">Size</span></span>              | \-                                                    |
| <span data-ttu-id="13999-116">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="13999-116">Update Privilege</span></span>  | <span data-ttu-id="13999-117">Questo valore viene impostato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="13999-117">This value is set by the system.</span></span>                      |
| <span data-ttu-id="13999-118">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="13999-118">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="13999-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="13999-119">Attribute-Id</span></span>      | <span data-ttu-id="13999-120">1.2.840.113556.1.4.359</span><span class="sxs-lookup"><span data-stu-id="13999-120">1.2.840.113556.1.4.359</span></span>                                |
| <span data-ttu-id="13999-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="13999-121">System-Id-Guid</span></span>    | <span data-ttu-id="13999-122">3e978921-8c01-11d0-afda-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="13999-122">3e978921-8c01-11d0-afda-00c04fd930c9</span></span>                  |
| <span data-ttu-id="13999-123">Sintassi</span><span class="sxs-lookup"><span data-stu-id="13999-123">Syntax</span></span>            | [<span data-ttu-id="13999-124">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="13999-124">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="13999-125">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="13999-125">Implementations</span></span>

-   [<span data-ttu-id="13999-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="13999-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="13999-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="13999-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="13999-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="13999-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="13999-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="13999-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="13999-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="13999-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="13999-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="13999-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="13999-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="13999-132">Windows 2000 Server</span></span>



| <span data-ttu-id="13999-133">Voce</span><span class="sxs-lookup"><span data-stu-id="13999-133">Entry</span></span> | <span data-ttu-id="13999-134">Valore</span><span class="sxs-lookup"><span data-stu-id="13999-134">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="13999-135">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="13999-135">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="13999-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="13999-136">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="13999-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="13999-137">System-Only</span></span>            | <span data-ttu-id="13999-138">Falso</span><span class="sxs-lookup"><span data-stu-id="13999-138">False</span></span>                                     |
| <span data-ttu-id="13999-139">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="13999-139">Is-Single-Valued</span></span>       | <span data-ttu-id="13999-140">Vero</span><span class="sxs-lookup"><span data-stu-id="13999-140">True</span></span>                                      |
| <span data-ttu-id="13999-141">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="13999-141">Is Indexed</span></span>             | <span data-ttu-id="13999-142">Vero</span><span class="sxs-lookup"><span data-stu-id="13999-142">True</span></span>                                      |
| <span data-ttu-id="13999-143">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="13999-143">In Global Catalog</span></span>      | <span data-ttu-id="13999-144">Vero</span><span class="sxs-lookup"><span data-stu-id="13999-144">True</span></span>                                      |
| <span data-ttu-id="13999-145">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="13999-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="13999-146">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="13999-146">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="13999-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="13999-147">Range-Lower</span></span>            | <span data-ttu-id="13999-148">16</span><span class="sxs-lookup"><span data-stu-id="13999-148">16</span></span>                                        |
| <span data-ttu-id="13999-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="13999-149">Range-Upper</span></span>            | <span data-ttu-id="13999-150">16</span><span class="sxs-lookup"><span data-stu-id="13999-150">16</span></span>                                        |
| <span data-ttu-id="13999-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="13999-151">Search-Flags</span></span>           | <span data-ttu-id="13999-152">0x00000001</span><span class="sxs-lookup"><span data-stu-id="13999-152">0x00000001</span></span>                                |
| <span data-ttu-id="13999-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="13999-153">System-Flags</span></span>           | <span data-ttu-id="13999-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="13999-154">0x00000010</span></span>                                |
| <span data-ttu-id="13999-155">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="13999-155">Classes used in</span></span>        | [<span data-ttu-id="13999-156">**Computer**</span><span class="sxs-lookup"><span data-stu-id="13999-156">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="13999-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="13999-157">Windows Server 2003</span></span>



| <span data-ttu-id="13999-158">Voce</span><span class="sxs-lookup"><span data-stu-id="13999-158">Entry</span></span> | <span data-ttu-id="13999-159">Valore</span><span class="sxs-lookup"><span data-stu-id="13999-159">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="13999-160">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="13999-160">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="13999-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="13999-161">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="13999-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="13999-162">System-Only</span></span>            | <span data-ttu-id="13999-163">Falso</span><span class="sxs-lookup"><span data-stu-id="13999-163">False</span></span>                                     |
| <span data-ttu-id="13999-164">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="13999-164">Is-Single-Valued</span></span>       | <span data-ttu-id="13999-165">Vero</span><span class="sxs-lookup"><span data-stu-id="13999-165">True</span></span>                                      |
| <span data-ttu-id="13999-166">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="13999-166">Is Indexed</span></span>             | <span data-ttu-id="13999-167">Vero</span><span class="sxs-lookup"><span data-stu-id="13999-167">True</span></span>                                      |
| <span data-ttu-id="13999-168">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="13999-168">In Global Catalog</span></span>      | <span data-ttu-id="13999-169">Vero</span><span class="sxs-lookup"><span data-stu-id="13999-169">True</span></span>                                      |
| <span data-ttu-id="13999-170">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="13999-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="13999-171">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="13999-171">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="13999-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="13999-172">Range-Lower</span></span>            | <span data-ttu-id="13999-173">16</span><span class="sxs-lookup"><span data-stu-id="13999-173">16</span></span>                                        |
| <span data-ttu-id="13999-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="13999-174">Range-Upper</span></span>            | <span data-ttu-id="13999-175">16</span><span class="sxs-lookup"><span data-stu-id="13999-175">16</span></span>                                        |
| <span data-ttu-id="13999-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="13999-176">Search-Flags</span></span>           | <span data-ttu-id="13999-177">0x00000001</span><span class="sxs-lookup"><span data-stu-id="13999-177">0x00000001</span></span>                                |
| <span data-ttu-id="13999-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="13999-178">System-Flags</span></span>           | <span data-ttu-id="13999-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="13999-179">0x00000010</span></span>                                |
| <span data-ttu-id="13999-180">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="13999-180">Classes used in</span></span>        | [<span data-ttu-id="13999-181">**Computer**</span><span class="sxs-lookup"><span data-stu-id="13999-181">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="13999-182">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="13999-182">Windows Server 2003 R2</span></span>



| <span data-ttu-id="13999-183">Voce</span><span class="sxs-lookup"><span data-stu-id="13999-183">Entry</span></span> | <span data-ttu-id="13999-184">Valore</span><span class="sxs-lookup"><span data-stu-id="13999-184">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="13999-185">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="13999-185">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="13999-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="13999-186">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="13999-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="13999-187">System-Only</span></span>            | <span data-ttu-id="13999-188">Falso</span><span class="sxs-lookup"><span data-stu-id="13999-188">False</span></span>                                     |
| <span data-ttu-id="13999-189">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="13999-189">Is-Single-Valued</span></span>       | <span data-ttu-id="13999-190">Vero</span><span class="sxs-lookup"><span data-stu-id="13999-190">True</span></span>                                      |
| <span data-ttu-id="13999-191">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="13999-191">Is Indexed</span></span>             | <span data-ttu-id="13999-192">Vero</span><span class="sxs-lookup"><span data-stu-id="13999-192">True</span></span>                                      |
| <span data-ttu-id="13999-193">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="13999-193">In Global Catalog</span></span>      | <span data-ttu-id="13999-194">Vero</span><span class="sxs-lookup"><span data-stu-id="13999-194">True</span></span>                                      |
| <span data-ttu-id="13999-195">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="13999-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="13999-196">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="13999-196">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="13999-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="13999-197">Range-Lower</span></span>            | <span data-ttu-id="13999-198">16</span><span class="sxs-lookup"><span data-stu-id="13999-198">16</span></span>                                        |
| <span data-ttu-id="13999-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="13999-199">Range-Upper</span></span>            | <span data-ttu-id="13999-200">16</span><span class="sxs-lookup"><span data-stu-id="13999-200">16</span></span>                                        |
| <span data-ttu-id="13999-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="13999-201">Search-Flags</span></span>           | <span data-ttu-id="13999-202">0x00000001</span><span class="sxs-lookup"><span data-stu-id="13999-202">0x00000001</span></span>                                |
| <span data-ttu-id="13999-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="13999-203">System-Flags</span></span>           | <span data-ttu-id="13999-204">0x00000010</span><span class="sxs-lookup"><span data-stu-id="13999-204">0x00000010</span></span>                                |
| <span data-ttu-id="13999-205">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="13999-205">Classes used in</span></span>        | [<span data-ttu-id="13999-206">**Computer**</span><span class="sxs-lookup"><span data-stu-id="13999-206">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="13999-207">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="13999-207">Windows Server 2008</span></span>



| <span data-ttu-id="13999-208">Voce</span><span class="sxs-lookup"><span data-stu-id="13999-208">Entry</span></span> | <span data-ttu-id="13999-209">Valore</span><span class="sxs-lookup"><span data-stu-id="13999-209">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="13999-210">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="13999-210">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="13999-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="13999-211">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="13999-212">System-Only</span><span class="sxs-lookup"><span data-stu-id="13999-212">System-Only</span></span>            | <span data-ttu-id="13999-213">Falso</span><span class="sxs-lookup"><span data-stu-id="13999-213">False</span></span>                                     |
| <span data-ttu-id="13999-214">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="13999-214">Is-Single-Valued</span></span>       | <span data-ttu-id="13999-215">Vero</span><span class="sxs-lookup"><span data-stu-id="13999-215">True</span></span>                                      |
| <span data-ttu-id="13999-216">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="13999-216">Is Indexed</span></span>             | <span data-ttu-id="13999-217">Vero</span><span class="sxs-lookup"><span data-stu-id="13999-217">True</span></span>                                      |
| <span data-ttu-id="13999-218">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="13999-218">In Global Catalog</span></span>      | <span data-ttu-id="13999-219">Vero</span><span class="sxs-lookup"><span data-stu-id="13999-219">True</span></span>                                      |
| <span data-ttu-id="13999-220">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="13999-220">NT-Security-Descriptor</span></span> | <span data-ttu-id="13999-221">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="13999-221">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="13999-222">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="13999-222">Range-Lower</span></span>            | <span data-ttu-id="13999-223">16</span><span class="sxs-lookup"><span data-stu-id="13999-223">16</span></span>                                        |
| <span data-ttu-id="13999-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="13999-224">Range-Upper</span></span>            | <span data-ttu-id="13999-225">16</span><span class="sxs-lookup"><span data-stu-id="13999-225">16</span></span>                                        |
| <span data-ttu-id="13999-226">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="13999-226">Search-Flags</span></span>           | <span data-ttu-id="13999-227">0x00000001</span><span class="sxs-lookup"><span data-stu-id="13999-227">0x00000001</span></span>                                |
| <span data-ttu-id="13999-228">System-Flags</span><span class="sxs-lookup"><span data-stu-id="13999-228">System-Flags</span></span>           | <span data-ttu-id="13999-229">0x00000010</span><span class="sxs-lookup"><span data-stu-id="13999-229">0x00000010</span></span>                                |
| <span data-ttu-id="13999-230">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="13999-230">Classes used in</span></span>        | [<span data-ttu-id="13999-231">**Computer**</span><span class="sxs-lookup"><span data-stu-id="13999-231">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="13999-232">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="13999-232">Windows Server 2008 R2</span></span>



| <span data-ttu-id="13999-233">Voce</span><span class="sxs-lookup"><span data-stu-id="13999-233">Entry</span></span> | <span data-ttu-id="13999-234">Valore</span><span class="sxs-lookup"><span data-stu-id="13999-234">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="13999-235">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="13999-235">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="13999-236">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="13999-236">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="13999-237">System-Only</span><span class="sxs-lookup"><span data-stu-id="13999-237">System-Only</span></span>            | <span data-ttu-id="13999-238">Falso</span><span class="sxs-lookup"><span data-stu-id="13999-238">False</span></span>                                     |
| <span data-ttu-id="13999-239">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="13999-239">Is-Single-Valued</span></span>       | <span data-ttu-id="13999-240">Vero</span><span class="sxs-lookup"><span data-stu-id="13999-240">True</span></span>                                      |
| <span data-ttu-id="13999-241">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="13999-241">Is Indexed</span></span>             | <span data-ttu-id="13999-242">Vero</span><span class="sxs-lookup"><span data-stu-id="13999-242">True</span></span>                                      |
| <span data-ttu-id="13999-243">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="13999-243">In Global Catalog</span></span>      | <span data-ttu-id="13999-244">Vero</span><span class="sxs-lookup"><span data-stu-id="13999-244">True</span></span>                                      |
| <span data-ttu-id="13999-245">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="13999-245">NT-Security-Descriptor</span></span> | <span data-ttu-id="13999-246">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="13999-246">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="13999-247">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="13999-247">Range-Lower</span></span>            | <span data-ttu-id="13999-248">16</span><span class="sxs-lookup"><span data-stu-id="13999-248">16</span></span>                                        |
| <span data-ttu-id="13999-249">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="13999-249">Range-Upper</span></span>            | <span data-ttu-id="13999-250">16</span><span class="sxs-lookup"><span data-stu-id="13999-250">16</span></span>                                        |
| <span data-ttu-id="13999-251">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="13999-251">Search-Flags</span></span>           | <span data-ttu-id="13999-252">0x00000001</span><span class="sxs-lookup"><span data-stu-id="13999-252">0x00000001</span></span>                                |
| <span data-ttu-id="13999-253">System-Flags</span><span class="sxs-lookup"><span data-stu-id="13999-253">System-Flags</span></span>           | <span data-ttu-id="13999-254">0x00000010</span><span class="sxs-lookup"><span data-stu-id="13999-254">0x00000010</span></span>                                |
| <span data-ttu-id="13999-255">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="13999-255">Classes used in</span></span>        | [<span data-ttu-id="13999-256">**Computer**</span><span class="sxs-lookup"><span data-stu-id="13999-256">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="13999-257">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="13999-257">Windows Server 2012</span></span>



| <span data-ttu-id="13999-258">Voce</span><span class="sxs-lookup"><span data-stu-id="13999-258">Entry</span></span> | <span data-ttu-id="13999-259">Valore</span><span class="sxs-lookup"><span data-stu-id="13999-259">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="13999-260">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="13999-260">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="13999-261">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="13999-261">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="13999-262">System-Only</span><span class="sxs-lookup"><span data-stu-id="13999-262">System-Only</span></span>            | <span data-ttu-id="13999-263">Falso</span><span class="sxs-lookup"><span data-stu-id="13999-263">False</span></span>                                     |
| <span data-ttu-id="13999-264">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="13999-264">Is-Single-Valued</span></span>       | <span data-ttu-id="13999-265">Vero</span><span class="sxs-lookup"><span data-stu-id="13999-265">True</span></span>                                      |
| <span data-ttu-id="13999-266">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="13999-266">Is Indexed</span></span>             | <span data-ttu-id="13999-267">Vero</span><span class="sxs-lookup"><span data-stu-id="13999-267">True</span></span>                                      |
| <span data-ttu-id="13999-268">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="13999-268">In Global Catalog</span></span>      | <span data-ttu-id="13999-269">Vero</span><span class="sxs-lookup"><span data-stu-id="13999-269">True</span></span>                                      |
| <span data-ttu-id="13999-270">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="13999-270">NT-Security-Descriptor</span></span> | <span data-ttu-id="13999-271">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="13999-271">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="13999-272">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="13999-272">Range-Lower</span></span>            | <span data-ttu-id="13999-273">16</span><span class="sxs-lookup"><span data-stu-id="13999-273">16</span></span>                                        |
| <span data-ttu-id="13999-274">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="13999-274">Range-Upper</span></span>            | <span data-ttu-id="13999-275">16</span><span class="sxs-lookup"><span data-stu-id="13999-275">16</span></span>                                        |
| <span data-ttu-id="13999-276">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="13999-276">Search-Flags</span></span>           | <span data-ttu-id="13999-277">0x00000001</span><span class="sxs-lookup"><span data-stu-id="13999-277">0x00000001</span></span>                                |
| <span data-ttu-id="13999-278">System-Flags</span><span class="sxs-lookup"><span data-stu-id="13999-278">System-Flags</span></span>           | <span data-ttu-id="13999-279">0x00000010</span><span class="sxs-lookup"><span data-stu-id="13999-279">0x00000010</span></span>                                |
| <span data-ttu-id="13999-280">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="13999-280">Classes used in</span></span>        | [<span data-ttu-id="13999-281">**Computer**</span><span class="sxs-lookup"><span data-stu-id="13999-281">**Computer**</span></span>](c-computer.md)<br/> |



 

 





