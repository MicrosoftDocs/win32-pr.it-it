---
title: Ultimo-set-time (attributo)
description: Data e ora dell'Ultima modifica del segreto.
ms.assetid: 71245cd4-90d8-4aa1-ad96-d46d6b3a7ad0
ms.tgt_platform: multiple
keywords:
- Ultimo schema AD attribute-set-time
- Schema AD dell'attributo lastSetTime
topic_type:
- apiref
api_name:
- Last-Set-Time
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce123377fac6e67de1ba84b906c9498d0a064936
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104401002"
---
# <a name="last-set-time-attribute"></a><span data-ttu-id="48d70-105">Ultimo-set-time (attributo)</span><span class="sxs-lookup"><span data-stu-id="48d70-105">Last-Set-Time attribute</span></span>

<span data-ttu-id="48d70-106">Data e ora dell'Ultima modifica del segreto.</span><span class="sxs-lookup"><span data-stu-id="48d70-106">The last time the secret was changed.</span></span> <span data-ttu-id="48d70-107">Questo valore viene archiviato come intero grande che rappresenta il numero di intervalli di 100-nanosecondi a partire dal 1 ° gennaio 1601 (UTC).</span><span class="sxs-lookup"><span data-stu-id="48d70-107">This value is stored as a large integer that represents the number of 100-nanosecond intervals since January 1, 1601 (UTC).</span></span>



| <span data-ttu-id="48d70-108">Voce</span><span class="sxs-lookup"><span data-stu-id="48d70-108">Entry</span></span> | <span data-ttu-id="48d70-109">Valore</span><span class="sxs-lookup"><span data-stu-id="48d70-109">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="48d70-110">CN</span><span class="sxs-lookup"><span data-stu-id="48d70-110">CN</span></span>                | <span data-ttu-id="48d70-111">Ora ultimo set</span><span class="sxs-lookup"><span data-stu-id="48d70-111">Last-Set-Time</span></span>                        |
| <span data-ttu-id="48d70-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="48d70-112">Ldap-Display-Name</span></span> | <span data-ttu-id="48d70-113">lastSetTime</span><span class="sxs-lookup"><span data-stu-id="48d70-113">lastSetTime</span></span>                          |
| <span data-ttu-id="48d70-114">Dimensione</span><span class="sxs-lookup"><span data-stu-id="48d70-114">Size</span></span>              | <span data-ttu-id="48d70-115">8 byte</span><span class="sxs-lookup"><span data-stu-id="48d70-115">8 bytes</span></span>                              |
| <span data-ttu-id="48d70-116">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="48d70-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="48d70-117">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="48d70-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="48d70-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="48d70-118">Attribute-Id</span></span>      | <span data-ttu-id="48d70-119">1.2.840.113556.1.4.53</span><span class="sxs-lookup"><span data-stu-id="48d70-119">1.2.840.113556.1.4.53</span></span>                |
| <span data-ttu-id="48d70-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="48d70-120">System-Id-Guid</span></span>    | <span data-ttu-id="48d70-121">bf967998-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="48d70-121">bf967998-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="48d70-122">Sintassi</span><span class="sxs-lookup"><span data-stu-id="48d70-122">Syntax</span></span>            | [<span data-ttu-id="48d70-123">**Interval**</span><span class="sxs-lookup"><span data-stu-id="48d70-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="48d70-124">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="48d70-124">Implementations</span></span>

-   [<span data-ttu-id="48d70-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="48d70-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="48d70-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="48d70-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="48d70-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="48d70-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="48d70-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="48d70-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="48d70-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="48d70-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="48d70-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="48d70-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="48d70-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="48d70-131">Windows 2000 Server</span></span>



| <span data-ttu-id="48d70-132">Voce</span><span class="sxs-lookup"><span data-stu-id="48d70-132">Entry</span></span> | <span data-ttu-id="48d70-133">Valore</span><span class="sxs-lookup"><span data-stu-id="48d70-133">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="48d70-134">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="48d70-134">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="48d70-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="48d70-135">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="48d70-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="48d70-136">System-Only</span></span>            | <span data-ttu-id="48d70-137">Falso</span><span class="sxs-lookup"><span data-stu-id="48d70-137">False</span></span>                                 |
| <span data-ttu-id="48d70-138">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="48d70-138">Is-Single-Valued</span></span>       | <span data-ttu-id="48d70-139">Vero</span><span class="sxs-lookup"><span data-stu-id="48d70-139">True</span></span>                                  |
| <span data-ttu-id="48d70-140">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="48d70-140">Is Indexed</span></span>             | <span data-ttu-id="48d70-141">Falso</span><span class="sxs-lookup"><span data-stu-id="48d70-141">False</span></span>                                 |
| <span data-ttu-id="48d70-142">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="48d70-142">In Global Catalog</span></span>      | <span data-ttu-id="48d70-143">Falso</span><span class="sxs-lookup"><span data-stu-id="48d70-143">False</span></span>                                 |
| <span data-ttu-id="48d70-144">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="48d70-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="48d70-145">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="48d70-145">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="48d70-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="48d70-146">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="48d70-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="48d70-147">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="48d70-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="48d70-148">Search-Flags</span></span>           | <span data-ttu-id="48d70-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="48d70-149">0x00000000</span></span>                            |
| <span data-ttu-id="48d70-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="48d70-150">System-Flags</span></span>           | <span data-ttu-id="48d70-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="48d70-151">0x00000010</span></span>                            |
| <span data-ttu-id="48d70-152">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="48d70-152">Classes used in</span></span>        | [<span data-ttu-id="48d70-153">**Segreto**</span><span class="sxs-lookup"><span data-stu-id="48d70-153">**Secret**</span></span>](c-secret.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="48d70-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="48d70-154">Windows Server 2003</span></span>



| <span data-ttu-id="48d70-155">Voce</span><span class="sxs-lookup"><span data-stu-id="48d70-155">Entry</span></span> | <span data-ttu-id="48d70-156">Valore</span><span class="sxs-lookup"><span data-stu-id="48d70-156">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="48d70-157">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="48d70-157">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="48d70-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="48d70-158">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="48d70-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="48d70-159">System-Only</span></span>            | <span data-ttu-id="48d70-160">Falso</span><span class="sxs-lookup"><span data-stu-id="48d70-160">False</span></span>                                 |
| <span data-ttu-id="48d70-161">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="48d70-161">Is-Single-Valued</span></span>       | <span data-ttu-id="48d70-162">Vero</span><span class="sxs-lookup"><span data-stu-id="48d70-162">True</span></span>                                  |
| <span data-ttu-id="48d70-163">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="48d70-163">Is Indexed</span></span>             | <span data-ttu-id="48d70-164">Falso</span><span class="sxs-lookup"><span data-stu-id="48d70-164">False</span></span>                                 |
| <span data-ttu-id="48d70-165">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="48d70-165">In Global Catalog</span></span>      | <span data-ttu-id="48d70-166">Falso</span><span class="sxs-lookup"><span data-stu-id="48d70-166">False</span></span>                                 |
| <span data-ttu-id="48d70-167">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="48d70-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="48d70-168">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="48d70-168">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="48d70-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="48d70-169">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="48d70-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="48d70-170">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="48d70-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="48d70-171">Search-Flags</span></span>           | <span data-ttu-id="48d70-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="48d70-172">0x00000000</span></span>                            |
| <span data-ttu-id="48d70-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="48d70-173">System-Flags</span></span>           | <span data-ttu-id="48d70-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="48d70-174">0x00000010</span></span>                            |
| <span data-ttu-id="48d70-175">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="48d70-175">Classes used in</span></span>        | [<span data-ttu-id="48d70-176">**Segreto**</span><span class="sxs-lookup"><span data-stu-id="48d70-176">**Secret**</span></span>](c-secret.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="48d70-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="48d70-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="48d70-178">Voce</span><span class="sxs-lookup"><span data-stu-id="48d70-178">Entry</span></span> | <span data-ttu-id="48d70-179">Valore</span><span class="sxs-lookup"><span data-stu-id="48d70-179">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="48d70-180">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="48d70-180">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="48d70-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="48d70-181">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="48d70-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="48d70-182">System-Only</span></span>            | <span data-ttu-id="48d70-183">Falso</span><span class="sxs-lookup"><span data-stu-id="48d70-183">False</span></span>                                 |
| <span data-ttu-id="48d70-184">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="48d70-184">Is-Single-Valued</span></span>       | <span data-ttu-id="48d70-185">Vero</span><span class="sxs-lookup"><span data-stu-id="48d70-185">True</span></span>                                  |
| <span data-ttu-id="48d70-186">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="48d70-186">Is Indexed</span></span>             | <span data-ttu-id="48d70-187">Falso</span><span class="sxs-lookup"><span data-stu-id="48d70-187">False</span></span>                                 |
| <span data-ttu-id="48d70-188">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="48d70-188">In Global Catalog</span></span>      | <span data-ttu-id="48d70-189">Falso</span><span class="sxs-lookup"><span data-stu-id="48d70-189">False</span></span>                                 |
| <span data-ttu-id="48d70-190">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="48d70-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="48d70-191">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="48d70-191">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="48d70-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="48d70-192">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="48d70-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="48d70-193">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="48d70-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="48d70-194">Search-Flags</span></span>           | <span data-ttu-id="48d70-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="48d70-195">0x00000000</span></span>                            |
| <span data-ttu-id="48d70-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="48d70-196">System-Flags</span></span>           | <span data-ttu-id="48d70-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="48d70-197">0x00000010</span></span>                            |
| <span data-ttu-id="48d70-198">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="48d70-198">Classes used in</span></span>        | [<span data-ttu-id="48d70-199">**Segreto**</span><span class="sxs-lookup"><span data-stu-id="48d70-199">**Secret**</span></span>](c-secret.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="48d70-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="48d70-200">Windows Server 2008</span></span>



| <span data-ttu-id="48d70-201">Voce</span><span class="sxs-lookup"><span data-stu-id="48d70-201">Entry</span></span> | <span data-ttu-id="48d70-202">Valore</span><span class="sxs-lookup"><span data-stu-id="48d70-202">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="48d70-203">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="48d70-203">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="48d70-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="48d70-204">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="48d70-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="48d70-205">System-Only</span></span>            | <span data-ttu-id="48d70-206">Falso</span><span class="sxs-lookup"><span data-stu-id="48d70-206">False</span></span>                                 |
| <span data-ttu-id="48d70-207">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="48d70-207">Is-Single-Valued</span></span>       | <span data-ttu-id="48d70-208">Vero</span><span class="sxs-lookup"><span data-stu-id="48d70-208">True</span></span>                                  |
| <span data-ttu-id="48d70-209">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="48d70-209">Is Indexed</span></span>             | <span data-ttu-id="48d70-210">Falso</span><span class="sxs-lookup"><span data-stu-id="48d70-210">False</span></span>                                 |
| <span data-ttu-id="48d70-211">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="48d70-211">In Global Catalog</span></span>      | <span data-ttu-id="48d70-212">Falso</span><span class="sxs-lookup"><span data-stu-id="48d70-212">False</span></span>                                 |
| <span data-ttu-id="48d70-213">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="48d70-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="48d70-214">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="48d70-214">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="48d70-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="48d70-215">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="48d70-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="48d70-216">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="48d70-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="48d70-217">Search-Flags</span></span>           | <span data-ttu-id="48d70-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="48d70-218">0x00000000</span></span>                            |
| <span data-ttu-id="48d70-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="48d70-219">System-Flags</span></span>           | <span data-ttu-id="48d70-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="48d70-220">0x00000010</span></span>                            |
| <span data-ttu-id="48d70-221">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="48d70-221">Classes used in</span></span>        | [<span data-ttu-id="48d70-222">**Segreto**</span><span class="sxs-lookup"><span data-stu-id="48d70-222">**Secret**</span></span>](c-secret.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="48d70-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="48d70-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="48d70-224">Voce</span><span class="sxs-lookup"><span data-stu-id="48d70-224">Entry</span></span> | <span data-ttu-id="48d70-225">Valore</span><span class="sxs-lookup"><span data-stu-id="48d70-225">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="48d70-226">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="48d70-226">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="48d70-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="48d70-227">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="48d70-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="48d70-228">System-Only</span></span>            | <span data-ttu-id="48d70-229">Falso</span><span class="sxs-lookup"><span data-stu-id="48d70-229">False</span></span>                                 |
| <span data-ttu-id="48d70-230">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="48d70-230">Is-Single-Valued</span></span>       | <span data-ttu-id="48d70-231">Vero</span><span class="sxs-lookup"><span data-stu-id="48d70-231">True</span></span>                                  |
| <span data-ttu-id="48d70-232">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="48d70-232">Is Indexed</span></span>             | <span data-ttu-id="48d70-233">Falso</span><span class="sxs-lookup"><span data-stu-id="48d70-233">False</span></span>                                 |
| <span data-ttu-id="48d70-234">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="48d70-234">In Global Catalog</span></span>      | <span data-ttu-id="48d70-235">Falso</span><span class="sxs-lookup"><span data-stu-id="48d70-235">False</span></span>                                 |
| <span data-ttu-id="48d70-236">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="48d70-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="48d70-237">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="48d70-237">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="48d70-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="48d70-238">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="48d70-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="48d70-239">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="48d70-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="48d70-240">Search-Flags</span></span>           | <span data-ttu-id="48d70-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="48d70-241">0x00000000</span></span>                            |
| <span data-ttu-id="48d70-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="48d70-242">System-Flags</span></span>           | <span data-ttu-id="48d70-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="48d70-243">0x00000010</span></span>                            |
| <span data-ttu-id="48d70-244">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="48d70-244">Classes used in</span></span>        | [<span data-ttu-id="48d70-245">**Segreto**</span><span class="sxs-lookup"><span data-stu-id="48d70-245">**Secret**</span></span>](c-secret.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="48d70-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="48d70-246">Windows Server 2012</span></span>



| <span data-ttu-id="48d70-247">Voce</span><span class="sxs-lookup"><span data-stu-id="48d70-247">Entry</span></span> | <span data-ttu-id="48d70-248">Valore</span><span class="sxs-lookup"><span data-stu-id="48d70-248">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="48d70-249">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="48d70-249">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="48d70-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="48d70-250">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="48d70-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="48d70-251">System-Only</span></span>            | <span data-ttu-id="48d70-252">Falso</span><span class="sxs-lookup"><span data-stu-id="48d70-252">False</span></span>                                 |
| <span data-ttu-id="48d70-253">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="48d70-253">Is-Single-Valued</span></span>       | <span data-ttu-id="48d70-254">Vero</span><span class="sxs-lookup"><span data-stu-id="48d70-254">True</span></span>                                  |
| <span data-ttu-id="48d70-255">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="48d70-255">Is Indexed</span></span>             | <span data-ttu-id="48d70-256">Falso</span><span class="sxs-lookup"><span data-stu-id="48d70-256">False</span></span>                                 |
| <span data-ttu-id="48d70-257">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="48d70-257">In Global Catalog</span></span>      | <span data-ttu-id="48d70-258">Falso</span><span class="sxs-lookup"><span data-stu-id="48d70-258">False</span></span>                                 |
| <span data-ttu-id="48d70-259">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="48d70-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="48d70-260">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="48d70-260">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="48d70-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="48d70-261">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="48d70-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="48d70-262">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="48d70-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="48d70-263">Search-Flags</span></span>           | <span data-ttu-id="48d70-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="48d70-264">0x00000000</span></span>                            |
| <span data-ttu-id="48d70-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="48d70-265">System-Flags</span></span>           | <span data-ttu-id="48d70-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="48d70-266">0x00000010</span></span>                            |
| <span data-ttu-id="48d70-267">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="48d70-267">Classes used in</span></span>        | [<span data-ttu-id="48d70-268">**Segreto**</span><span class="sxs-lookup"><span data-stu-id="48d70-268">**Secret**</span></span>](c-secret.md)<br/> |



 

 





