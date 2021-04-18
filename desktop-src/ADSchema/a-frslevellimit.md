---
title: Attributo a livello di servizio FRS
description: Limitare la profondità dell'albero di directory per la replica dei file.
ms.assetid: e2916cbd-1ce7-4ff7-82a2-5fbdae3c6a1b
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo per il limite di livello FRS
- Schema AD dell'attributo fRSLevelLimit
topic_type:
- apiref
api_name:
- FRS-Level-Limit
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c587565eb10014ef638a2320dd9229d8409ba06
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "106302917"
---
# <a name="frs-level-limit-attribute"></a><span data-ttu-id="05972-105">Attributo a livello di servizio FRS</span><span class="sxs-lookup"><span data-stu-id="05972-105">FRS-Level-Limit attribute</span></span>

<span data-ttu-id="05972-106">Limitare la profondità dell'albero di directory per la replica dei file.</span><span class="sxs-lookup"><span data-stu-id="05972-106">Limit depth of directory tree to replicate for file replication.</span></span>



| <span data-ttu-id="05972-107">Voce</span><span class="sxs-lookup"><span data-stu-id="05972-107">Entry</span></span> | <span data-ttu-id="05972-108">Valore</span><span class="sxs-lookup"><span data-stu-id="05972-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="05972-109">CN</span><span class="sxs-lookup"><span data-stu-id="05972-109">CN</span></span>                | <span data-ttu-id="05972-110">Limite di livello FRS</span><span class="sxs-lookup"><span data-stu-id="05972-110">FRS-Level-Limit</span></span>                      |
| <span data-ttu-id="05972-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="05972-111">Ldap-Display-Name</span></span> | <span data-ttu-id="05972-112">fRSLevelLimit</span><span class="sxs-lookup"><span data-stu-id="05972-112">fRSLevelLimit</span></span>                        |
| <span data-ttu-id="05972-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="05972-113">Size</span></span>              | <span data-ttu-id="05972-114">4 byte</span><span class="sxs-lookup"><span data-stu-id="05972-114">4 bytes</span></span>                              |
| <span data-ttu-id="05972-115">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="05972-115">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="05972-116">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="05972-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="05972-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="05972-117">Attribute-Id</span></span>      | <span data-ttu-id="05972-118">1.2.840.113556.1.4.534</span><span class="sxs-lookup"><span data-stu-id="05972-118">1.2.840.113556.1.4.534</span></span>               |
| <span data-ttu-id="05972-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="05972-119">System-Id-Guid</span></span>    | <span data-ttu-id="05972-120">5245801e-ca6a-11d0-afff-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="05972-120">5245801e-ca6a-11d0-afff-0000f80367c1</span></span> |
| <span data-ttu-id="05972-121">Sintassi</span><span class="sxs-lookup"><span data-stu-id="05972-121">Syntax</span></span>            | [<span data-ttu-id="05972-122">**Enumerazione**</span><span class="sxs-lookup"><span data-stu-id="05972-122">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="05972-123">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="05972-123">Implementations</span></span>

-   [<span data-ttu-id="05972-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="05972-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="05972-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="05972-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="05972-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="05972-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="05972-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="05972-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="05972-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="05972-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="05972-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="05972-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="05972-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="05972-130">Windows 2000 Server</span></span>



| <span data-ttu-id="05972-131">Voce</span><span class="sxs-lookup"><span data-stu-id="05972-131">Entry</span></span> | <span data-ttu-id="05972-132">Valore</span><span class="sxs-lookup"><span data-stu-id="05972-132">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="05972-133">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="05972-133">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="05972-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="05972-134">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="05972-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="05972-135">System-Only</span></span>            | <span data-ttu-id="05972-136">Falso</span><span class="sxs-lookup"><span data-stu-id="05972-136">False</span></span>                                                     |
| <span data-ttu-id="05972-137">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="05972-137">Is-Single-Valued</span></span>       | <span data-ttu-id="05972-138">Vero</span><span class="sxs-lookup"><span data-stu-id="05972-138">True</span></span>                                                      |
| <span data-ttu-id="05972-139">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="05972-139">Is Indexed</span></span>             | <span data-ttu-id="05972-140">Falso</span><span class="sxs-lookup"><span data-stu-id="05972-140">False</span></span>                                                     |
| <span data-ttu-id="05972-141">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="05972-141">In Global Catalog</span></span>      | <span data-ttu-id="05972-142">Falso</span><span class="sxs-lookup"><span data-stu-id="05972-142">False</span></span>                                                     |
| <span data-ttu-id="05972-143">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="05972-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="05972-144">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="05972-144">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="05972-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="05972-145">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="05972-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="05972-146">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="05972-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="05972-147">Search-Flags</span></span>           | <span data-ttu-id="05972-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="05972-148">0x00000000</span></span>                                                |
| <span data-ttu-id="05972-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="05972-149">System-Flags</span></span>           | <span data-ttu-id="05972-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="05972-150">0x00000010</span></span>                                                |
| <span data-ttu-id="05972-151">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="05972-151">Classes used in</span></span>        | [<span data-ttu-id="05972-152">**NTFRS-set di repliche**</span><span class="sxs-lookup"><span data-stu-id="05972-152">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="05972-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="05972-153">Windows Server 2003</span></span>



| <span data-ttu-id="05972-154">Voce</span><span class="sxs-lookup"><span data-stu-id="05972-154">Entry</span></span> | <span data-ttu-id="05972-155">Valore</span><span class="sxs-lookup"><span data-stu-id="05972-155">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="05972-156">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="05972-156">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="05972-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="05972-157">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="05972-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="05972-158">System-Only</span></span>            | <span data-ttu-id="05972-159">Falso</span><span class="sxs-lookup"><span data-stu-id="05972-159">False</span></span>                                                     |
| <span data-ttu-id="05972-160">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="05972-160">Is-Single-Valued</span></span>       | <span data-ttu-id="05972-161">Vero</span><span class="sxs-lookup"><span data-stu-id="05972-161">True</span></span>                                                      |
| <span data-ttu-id="05972-162">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="05972-162">Is Indexed</span></span>             | <span data-ttu-id="05972-163">Falso</span><span class="sxs-lookup"><span data-stu-id="05972-163">False</span></span>                                                     |
| <span data-ttu-id="05972-164">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="05972-164">In Global Catalog</span></span>      | <span data-ttu-id="05972-165">Falso</span><span class="sxs-lookup"><span data-stu-id="05972-165">False</span></span>                                                     |
| <span data-ttu-id="05972-166">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="05972-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="05972-167">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="05972-167">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="05972-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="05972-168">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="05972-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="05972-169">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="05972-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="05972-170">Search-Flags</span></span>           | <span data-ttu-id="05972-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="05972-171">0x00000000</span></span>                                                |
| <span data-ttu-id="05972-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="05972-172">System-Flags</span></span>           | <span data-ttu-id="05972-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="05972-173">0x00000010</span></span>                                                |
| <span data-ttu-id="05972-174">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="05972-174">Classes used in</span></span>        | [<span data-ttu-id="05972-175">**NTFRS-set di repliche**</span><span class="sxs-lookup"><span data-stu-id="05972-175">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="05972-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="05972-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="05972-177">Voce</span><span class="sxs-lookup"><span data-stu-id="05972-177">Entry</span></span> | <span data-ttu-id="05972-178">Valore</span><span class="sxs-lookup"><span data-stu-id="05972-178">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="05972-179">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="05972-179">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="05972-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="05972-180">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="05972-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="05972-181">System-Only</span></span>            | <span data-ttu-id="05972-182">Falso</span><span class="sxs-lookup"><span data-stu-id="05972-182">False</span></span>                                                     |
| <span data-ttu-id="05972-183">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="05972-183">Is-Single-Valued</span></span>       | <span data-ttu-id="05972-184">Vero</span><span class="sxs-lookup"><span data-stu-id="05972-184">True</span></span>                                                      |
| <span data-ttu-id="05972-185">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="05972-185">Is Indexed</span></span>             | <span data-ttu-id="05972-186">Falso</span><span class="sxs-lookup"><span data-stu-id="05972-186">False</span></span>                                                     |
| <span data-ttu-id="05972-187">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="05972-187">In Global Catalog</span></span>      | <span data-ttu-id="05972-188">Falso</span><span class="sxs-lookup"><span data-stu-id="05972-188">False</span></span>                                                     |
| <span data-ttu-id="05972-189">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="05972-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="05972-190">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="05972-190">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="05972-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="05972-191">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="05972-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="05972-192">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="05972-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="05972-193">Search-Flags</span></span>           | <span data-ttu-id="05972-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="05972-194">0x00000000</span></span>                                                |
| <span data-ttu-id="05972-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="05972-195">System-Flags</span></span>           | <span data-ttu-id="05972-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="05972-196">0x00000010</span></span>                                                |
| <span data-ttu-id="05972-197">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="05972-197">Classes used in</span></span>        | [<span data-ttu-id="05972-198">**NTFRS-set di repliche**</span><span class="sxs-lookup"><span data-stu-id="05972-198">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="05972-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="05972-199">Windows Server 2008</span></span>



| <span data-ttu-id="05972-200">Voce</span><span class="sxs-lookup"><span data-stu-id="05972-200">Entry</span></span> | <span data-ttu-id="05972-201">Valore</span><span class="sxs-lookup"><span data-stu-id="05972-201">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="05972-202">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="05972-202">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="05972-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="05972-203">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="05972-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="05972-204">System-Only</span></span>            | <span data-ttu-id="05972-205">Falso</span><span class="sxs-lookup"><span data-stu-id="05972-205">False</span></span>                                                     |
| <span data-ttu-id="05972-206">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="05972-206">Is-Single-Valued</span></span>       | <span data-ttu-id="05972-207">Vero</span><span class="sxs-lookup"><span data-stu-id="05972-207">True</span></span>                                                      |
| <span data-ttu-id="05972-208">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="05972-208">Is Indexed</span></span>             | <span data-ttu-id="05972-209">Falso</span><span class="sxs-lookup"><span data-stu-id="05972-209">False</span></span>                                                     |
| <span data-ttu-id="05972-210">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="05972-210">In Global Catalog</span></span>      | <span data-ttu-id="05972-211">Falso</span><span class="sxs-lookup"><span data-stu-id="05972-211">False</span></span>                                                     |
| <span data-ttu-id="05972-212">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="05972-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="05972-213">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="05972-213">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="05972-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="05972-214">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="05972-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="05972-215">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="05972-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="05972-216">Search-Flags</span></span>           | <span data-ttu-id="05972-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="05972-217">0x00000000</span></span>                                                |
| <span data-ttu-id="05972-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="05972-218">System-Flags</span></span>           | <span data-ttu-id="05972-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="05972-219">0x00000010</span></span>                                                |
| <span data-ttu-id="05972-220">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="05972-220">Classes used in</span></span>        | [<span data-ttu-id="05972-221">**NTFRS-set di repliche**</span><span class="sxs-lookup"><span data-stu-id="05972-221">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="05972-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="05972-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="05972-223">Voce</span><span class="sxs-lookup"><span data-stu-id="05972-223">Entry</span></span> | <span data-ttu-id="05972-224">Valore</span><span class="sxs-lookup"><span data-stu-id="05972-224">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="05972-225">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="05972-225">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="05972-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="05972-226">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="05972-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="05972-227">System-Only</span></span>            | <span data-ttu-id="05972-228">Falso</span><span class="sxs-lookup"><span data-stu-id="05972-228">False</span></span>                                                     |
| <span data-ttu-id="05972-229">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="05972-229">Is-Single-Valued</span></span>       | <span data-ttu-id="05972-230">Vero</span><span class="sxs-lookup"><span data-stu-id="05972-230">True</span></span>                                                      |
| <span data-ttu-id="05972-231">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="05972-231">Is Indexed</span></span>             | <span data-ttu-id="05972-232">Falso</span><span class="sxs-lookup"><span data-stu-id="05972-232">False</span></span>                                                     |
| <span data-ttu-id="05972-233">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="05972-233">In Global Catalog</span></span>      | <span data-ttu-id="05972-234">Falso</span><span class="sxs-lookup"><span data-stu-id="05972-234">False</span></span>                                                     |
| <span data-ttu-id="05972-235">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="05972-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="05972-236">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="05972-236">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="05972-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="05972-237">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="05972-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="05972-238">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="05972-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="05972-239">Search-Flags</span></span>           | <span data-ttu-id="05972-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="05972-240">0x00000000</span></span>                                                |
| <span data-ttu-id="05972-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="05972-241">System-Flags</span></span>           | <span data-ttu-id="05972-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="05972-242">0x00000010</span></span>                                                |
| <span data-ttu-id="05972-243">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="05972-243">Classes used in</span></span>        | [<span data-ttu-id="05972-244">**NTFRS-set di repliche**</span><span class="sxs-lookup"><span data-stu-id="05972-244">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="05972-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="05972-245">Windows Server 2012</span></span>



| <span data-ttu-id="05972-246">Voce</span><span class="sxs-lookup"><span data-stu-id="05972-246">Entry</span></span> | <span data-ttu-id="05972-247">Valore</span><span class="sxs-lookup"><span data-stu-id="05972-247">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="05972-248">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="05972-248">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="05972-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="05972-249">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="05972-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="05972-250">System-Only</span></span>            | <span data-ttu-id="05972-251">Falso</span><span class="sxs-lookup"><span data-stu-id="05972-251">False</span></span>                                                     |
| <span data-ttu-id="05972-252">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="05972-252">Is-Single-Valued</span></span>       | <span data-ttu-id="05972-253">Vero</span><span class="sxs-lookup"><span data-stu-id="05972-253">True</span></span>                                                      |
| <span data-ttu-id="05972-254">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="05972-254">Is Indexed</span></span>             | <span data-ttu-id="05972-255">Falso</span><span class="sxs-lookup"><span data-stu-id="05972-255">False</span></span>                                                     |
| <span data-ttu-id="05972-256">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="05972-256">In Global Catalog</span></span>      | <span data-ttu-id="05972-257">Falso</span><span class="sxs-lookup"><span data-stu-id="05972-257">False</span></span>                                                     |
| <span data-ttu-id="05972-258">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="05972-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="05972-259">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="05972-259">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="05972-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="05972-260">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="05972-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="05972-261">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="05972-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="05972-262">Search-Flags</span></span>           | <span data-ttu-id="05972-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="05972-263">0x00000000</span></span>                                                |
| <span data-ttu-id="05972-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="05972-264">System-Flags</span></span>           | <span data-ttu-id="05972-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="05972-265">0x00000010</span></span>                                                |
| <span data-ttu-id="05972-266">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="05972-266">Classes used in</span></span>        | [<span data-ttu-id="05972-267">**NTFRS-set di repliche**</span><span class="sxs-lookup"><span data-stu-id="05972-267">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



 

 





