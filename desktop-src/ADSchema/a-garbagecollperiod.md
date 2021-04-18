---
title: Garbage-Coll-period (attributo)
description: Questo attributo si trova nel servizio directory CN, CN Windows NT, CN Services, CN Configuration,... oggetto. Rappresenta il tempo, in ore, tra l'esecuzione di DS Garbage Collection.
ms.assetid: 982a75f9-04b5-489e-99b3-a9fd3fb280c8
ms.tgt_platform: multiple
keywords:
- Schema di AD dell'attributo Garbage-Coll-period
- Schema AD dell'attributo garbageCollPeriod
topic_type:
- apiref
api_name:
- Garbage-Coll-Period
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64890df97cf4c131ad0dcdbed8cb80bf20b66a83
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "106302906"
---
# <a name="garbage-coll-period-attribute"></a><span data-ttu-id="bd728-106">Garbage-Coll-period (attributo)</span><span class="sxs-lookup"><span data-stu-id="bd728-106">Garbage-Coll-Period attribute</span></span>

<span data-ttu-id="bd728-107">Questo attributo si trova nel CN = Directory Service, CN = Windows NT, CN = Services, CN = Configuration,... oggetto.</span><span class="sxs-lookup"><span data-stu-id="bd728-107">This attribute is located on the CN=Directory Service,CN=Windows NT,CN=Services,CN=Configuration,... object.</span></span> <span data-ttu-id="bd728-108">Rappresenta il tempo, in ore, tra l'esecuzione di DS Garbage Collection.</span><span class="sxs-lookup"><span data-stu-id="bd728-108">It represents the time, in hours, between DS garbage collection runs.</span></span>



| <span data-ttu-id="bd728-109">Voce</span><span class="sxs-lookup"><span data-stu-id="bd728-109">Entry</span></span> | <span data-ttu-id="bd728-110">Valore</span><span class="sxs-lookup"><span data-stu-id="bd728-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="bd728-111">CN</span><span class="sxs-lookup"><span data-stu-id="bd728-111">CN</span></span>                | <span data-ttu-id="bd728-112">Garbage-Coll-period</span><span class="sxs-lookup"><span data-stu-id="bd728-112">Garbage-Coll-Period</span></span>                  |
| <span data-ttu-id="bd728-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="bd728-113">Ldap-Display-Name</span></span> | <span data-ttu-id="bd728-114">garbageCollPeriod</span><span class="sxs-lookup"><span data-stu-id="bd728-114">garbageCollPeriod</span></span>                    |
| <span data-ttu-id="bd728-115">Dimensione</span><span class="sxs-lookup"><span data-stu-id="bd728-115">Size</span></span>              | <span data-ttu-id="bd728-116">4 byte</span><span class="sxs-lookup"><span data-stu-id="bd728-116">4 bytes</span></span>                              |
| <span data-ttu-id="bd728-117">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="bd728-117">Update Privilege</span></span>  | <span data-ttu-id="bd728-118">Amministratore di dominio</span><span class="sxs-lookup"><span data-stu-id="bd728-118">Domain administrator</span></span>                 |
| <span data-ttu-id="bd728-119">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="bd728-119">Update Frequency</span></span>  | <span data-ttu-id="bd728-120">Molto raro.</span><span class="sxs-lookup"><span data-stu-id="bd728-120">Very rare.</span></span>                           |
| <span data-ttu-id="bd728-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="bd728-121">Attribute-Id</span></span>      | <span data-ttu-id="bd728-122">1.2.840.113556.1.2.301</span><span class="sxs-lookup"><span data-stu-id="bd728-122">1.2.840.113556.1.2.301</span></span>               |
| <span data-ttu-id="bd728-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="bd728-123">System-Id-Guid</span></span>    | <span data-ttu-id="bd728-124">5fd424a1-1262-11d0-a060-00aa006c33ed</span><span class="sxs-lookup"><span data-stu-id="bd728-124">5fd424a1-1262-11d0-a060-00aa006c33ed</span></span> |
| <span data-ttu-id="bd728-125">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bd728-125">Syntax</span></span>            | [<span data-ttu-id="bd728-126">**Enumerazione**</span><span class="sxs-lookup"><span data-stu-id="bd728-126">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="bd728-127">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="bd728-127">Implementations</span></span>

-   [<span data-ttu-id="bd728-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="bd728-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="bd728-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="bd728-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="bd728-130">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="bd728-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="bd728-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="bd728-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="bd728-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="bd728-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="bd728-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="bd728-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="bd728-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="bd728-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="bd728-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="bd728-135">Windows 2000 Server</span></span>



| <span data-ttu-id="bd728-136">Voce</span><span class="sxs-lookup"><span data-stu-id="bd728-136">Entry</span></span> | <span data-ttu-id="bd728-137">Valore</span><span class="sxs-lookup"><span data-stu-id="bd728-137">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd728-138">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="bd728-138">Link-Id</span></span>                | \-                                                                                                    |
| <span data-ttu-id="bd728-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bd728-139">MAPI-Id</span></span>                | <span data-ttu-id="bd728-140">0x80AF</span><span class="sxs-lookup"><span data-stu-id="bd728-140">0x80AF</span></span>                                                                                                |
| <span data-ttu-id="bd728-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="bd728-141">System-Only</span></span>            | <span data-ttu-id="bd728-142">Falso</span><span class="sxs-lookup"><span data-stu-id="bd728-142">False</span></span>                                                                                                 |
| <span data-ttu-id="bd728-143">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="bd728-143">Is-Single-Valued</span></span>       | <span data-ttu-id="bd728-144">Vero</span><span class="sxs-lookup"><span data-stu-id="bd728-144">True</span></span>                                                                                                  |
| <span data-ttu-id="bd728-145">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="bd728-145">Is Indexed</span></span>             | <span data-ttu-id="bd728-146">Falso</span><span class="sxs-lookup"><span data-stu-id="bd728-146">False</span></span>                                                                                                 |
| <span data-ttu-id="bd728-147">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="bd728-147">In Global Catalog</span></span>      | <span data-ttu-id="bd728-148">Falso</span><span class="sxs-lookup"><span data-stu-id="bd728-148">False</span></span>                                                                                                 |
| <span data-ttu-id="bd728-149">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="bd728-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="bd728-150">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="bd728-150">O:BAG:BAD:S:</span></span>                                                                                          |
| <span data-ttu-id="bd728-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bd728-151">Range-Lower</span></span>            | \-                                                                                                    |
| <span data-ttu-id="bd728-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bd728-152">Range-Upper</span></span>            | \-                                                                                                    |
| <span data-ttu-id="bd728-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bd728-153">Search-Flags</span></span>           | <span data-ttu-id="bd728-154">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bd728-154">0x00000000</span></span>                                                                                            |
| <span data-ttu-id="bd728-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bd728-155">System-Flags</span></span>           | <span data-ttu-id="bd728-156">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bd728-156">0x00000010</span></span>                                                                                            |
| <span data-ttu-id="bd728-157">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="bd728-157">Classes used in</span></span>        | [<span data-ttu-id="bd728-158">**Destinatario posta**</span><span class="sxs-lookup"><span data-stu-id="bd728-158">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> [<span data-ttu-id="bd728-159">**NTDS-Service**</span><span class="sxs-lookup"><span data-stu-id="bd728-159">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="bd728-160">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="bd728-160">Windows Server 2003</span></span>



| <span data-ttu-id="bd728-161">Voce</span><span class="sxs-lookup"><span data-stu-id="bd728-161">Entry</span></span> | <span data-ttu-id="bd728-162">Valore</span><span class="sxs-lookup"><span data-stu-id="bd728-162">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd728-163">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="bd728-163">Link-Id</span></span>                | \-                                                                                                    |
| <span data-ttu-id="bd728-164">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bd728-164">MAPI-Id</span></span>                | <span data-ttu-id="bd728-165">0x80AF</span><span class="sxs-lookup"><span data-stu-id="bd728-165">0x80AF</span></span>                                                                                                |
| <span data-ttu-id="bd728-166">System-Only</span><span class="sxs-lookup"><span data-stu-id="bd728-166">System-Only</span></span>            | <span data-ttu-id="bd728-167">Falso</span><span class="sxs-lookup"><span data-stu-id="bd728-167">False</span></span>                                                                                                 |
| <span data-ttu-id="bd728-168">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="bd728-168">Is-Single-Valued</span></span>       | <span data-ttu-id="bd728-169">Vero</span><span class="sxs-lookup"><span data-stu-id="bd728-169">True</span></span>                                                                                                  |
| <span data-ttu-id="bd728-170">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="bd728-170">Is Indexed</span></span>             | <span data-ttu-id="bd728-171">Falso</span><span class="sxs-lookup"><span data-stu-id="bd728-171">False</span></span>                                                                                                 |
| <span data-ttu-id="bd728-172">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="bd728-172">In Global Catalog</span></span>      | <span data-ttu-id="bd728-173">Falso</span><span class="sxs-lookup"><span data-stu-id="bd728-173">False</span></span>                                                                                                 |
| <span data-ttu-id="bd728-174">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="bd728-174">NT-Security-Descriptor</span></span> | <span data-ttu-id="bd728-175">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="bd728-175">O:BAG:BAD:S:</span></span>                                                                                          |
| <span data-ttu-id="bd728-176">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bd728-176">Range-Lower</span></span>            | \-                                                                                                    |
| <span data-ttu-id="bd728-177">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bd728-177">Range-Upper</span></span>            | \-                                                                                                    |
| <span data-ttu-id="bd728-178">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bd728-178">Search-Flags</span></span>           | <span data-ttu-id="bd728-179">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bd728-179">0x00000000</span></span>                                                                                            |
| <span data-ttu-id="bd728-180">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bd728-180">System-Flags</span></span>           | <span data-ttu-id="bd728-181">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bd728-181">0x00000010</span></span>                                                                                            |
| <span data-ttu-id="bd728-182">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="bd728-182">Classes used in</span></span>        | [<span data-ttu-id="bd728-183">**Destinatario posta**</span><span class="sxs-lookup"><span data-stu-id="bd728-183">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> [<span data-ttu-id="bd728-184">**NTDS-Service**</span><span class="sxs-lookup"><span data-stu-id="bd728-184">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="adam"></a><span data-ttu-id="bd728-185">ADAM</span><span class="sxs-lookup"><span data-stu-id="bd728-185">ADAM</span></span>



| <span data-ttu-id="bd728-186">Voce</span><span class="sxs-lookup"><span data-stu-id="bd728-186">Entry</span></span> | <span data-ttu-id="bd728-187">Valore</span><span class="sxs-lookup"><span data-stu-id="bd728-187">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="bd728-188">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="bd728-188">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="bd728-189">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bd728-189">MAPI-Id</span></span>                | <span data-ttu-id="bd728-190">0x80AF</span><span class="sxs-lookup"><span data-stu-id="bd728-190">0x80AF</span></span>                                           |
| <span data-ttu-id="bd728-191">System-Only</span><span class="sxs-lookup"><span data-stu-id="bd728-191">System-Only</span></span>            | <span data-ttu-id="bd728-192">Falso</span><span class="sxs-lookup"><span data-stu-id="bd728-192">False</span></span>                                            |
| <span data-ttu-id="bd728-193">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="bd728-193">Is-Single-Valued</span></span>       | <span data-ttu-id="bd728-194">Vero</span><span class="sxs-lookup"><span data-stu-id="bd728-194">True</span></span>                                             |
| <span data-ttu-id="bd728-195">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="bd728-195">Is Indexed</span></span>             | <span data-ttu-id="bd728-196">Falso</span><span class="sxs-lookup"><span data-stu-id="bd728-196">False</span></span>                                            |
| <span data-ttu-id="bd728-197">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="bd728-197">In Global Catalog</span></span>      | <span data-ttu-id="bd728-198">Falso</span><span class="sxs-lookup"><span data-stu-id="bd728-198">False</span></span>                                            |
| <span data-ttu-id="bd728-199">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="bd728-199">NT-Security-Descriptor</span></span> | <span data-ttu-id="bd728-200">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="bd728-200">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="bd728-201">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bd728-201">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="bd728-202">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bd728-202">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="bd728-203">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bd728-203">Search-Flags</span></span>           | <span data-ttu-id="bd728-204">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bd728-204">0x00000000</span></span>                                       |
| <span data-ttu-id="bd728-205">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bd728-205">System-Flags</span></span>           | <span data-ttu-id="bd728-206">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bd728-206">0x00000010</span></span>                                       |
| <span data-ttu-id="bd728-207">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="bd728-207">Classes used in</span></span>        | [<span data-ttu-id="bd728-208">**NTDS-Service**</span><span class="sxs-lookup"><span data-stu-id="bd728-208">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="bd728-209">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="bd728-209">Windows Server 2003 R2</span></span>



| <span data-ttu-id="bd728-210">Voce</span><span class="sxs-lookup"><span data-stu-id="bd728-210">Entry</span></span> | <span data-ttu-id="bd728-211">Valore</span><span class="sxs-lookup"><span data-stu-id="bd728-211">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd728-212">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="bd728-212">Link-Id</span></span>                | \-                                                                                                    |
| <span data-ttu-id="bd728-213">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bd728-213">MAPI-Id</span></span>                | <span data-ttu-id="bd728-214">0x80AF</span><span class="sxs-lookup"><span data-stu-id="bd728-214">0x80AF</span></span>                                                                                                |
| <span data-ttu-id="bd728-215">System-Only</span><span class="sxs-lookup"><span data-stu-id="bd728-215">System-Only</span></span>            | <span data-ttu-id="bd728-216">Falso</span><span class="sxs-lookup"><span data-stu-id="bd728-216">False</span></span>                                                                                                 |
| <span data-ttu-id="bd728-217">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="bd728-217">Is-Single-Valued</span></span>       | <span data-ttu-id="bd728-218">Vero</span><span class="sxs-lookup"><span data-stu-id="bd728-218">True</span></span>                                                                                                  |
| <span data-ttu-id="bd728-219">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="bd728-219">Is Indexed</span></span>             | <span data-ttu-id="bd728-220">Falso</span><span class="sxs-lookup"><span data-stu-id="bd728-220">False</span></span>                                                                                                 |
| <span data-ttu-id="bd728-221">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="bd728-221">In Global Catalog</span></span>      | <span data-ttu-id="bd728-222">Falso</span><span class="sxs-lookup"><span data-stu-id="bd728-222">False</span></span>                                                                                                 |
| <span data-ttu-id="bd728-223">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="bd728-223">NT-Security-Descriptor</span></span> | <span data-ttu-id="bd728-224">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="bd728-224">O:BAG:BAD:S:</span></span>                                                                                          |
| <span data-ttu-id="bd728-225">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bd728-225">Range-Lower</span></span>            | \-                                                                                                    |
| <span data-ttu-id="bd728-226">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bd728-226">Range-Upper</span></span>            | \-                                                                                                    |
| <span data-ttu-id="bd728-227">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bd728-227">Search-Flags</span></span>           | <span data-ttu-id="bd728-228">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bd728-228">0x00000000</span></span>                                                                                            |
| <span data-ttu-id="bd728-229">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bd728-229">System-Flags</span></span>           | <span data-ttu-id="bd728-230">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bd728-230">0x00000010</span></span>                                                                                            |
| <span data-ttu-id="bd728-231">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="bd728-231">Classes used in</span></span>        | [<span data-ttu-id="bd728-232">**Destinatario posta**</span><span class="sxs-lookup"><span data-stu-id="bd728-232">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> [<span data-ttu-id="bd728-233">**NTDS-Service**</span><span class="sxs-lookup"><span data-stu-id="bd728-233">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="bd728-234">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bd728-234">Windows Server 2008</span></span>



| <span data-ttu-id="bd728-235">Voce</span><span class="sxs-lookup"><span data-stu-id="bd728-235">Entry</span></span> | <span data-ttu-id="bd728-236">Valore</span><span class="sxs-lookup"><span data-stu-id="bd728-236">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd728-237">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="bd728-237">Link-Id</span></span>                | \-                                                                                                    |
| <span data-ttu-id="bd728-238">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bd728-238">MAPI-Id</span></span>                | <span data-ttu-id="bd728-239">0x80AF</span><span class="sxs-lookup"><span data-stu-id="bd728-239">0x80AF</span></span>                                                                                                |
| <span data-ttu-id="bd728-240">System-Only</span><span class="sxs-lookup"><span data-stu-id="bd728-240">System-Only</span></span>            | <span data-ttu-id="bd728-241">Falso</span><span class="sxs-lookup"><span data-stu-id="bd728-241">False</span></span>                                                                                                 |
| <span data-ttu-id="bd728-242">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="bd728-242">Is-Single-Valued</span></span>       | <span data-ttu-id="bd728-243">Vero</span><span class="sxs-lookup"><span data-stu-id="bd728-243">True</span></span>                                                                                                  |
| <span data-ttu-id="bd728-244">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="bd728-244">Is Indexed</span></span>             | <span data-ttu-id="bd728-245">Falso</span><span class="sxs-lookup"><span data-stu-id="bd728-245">False</span></span>                                                                                                 |
| <span data-ttu-id="bd728-246">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="bd728-246">In Global Catalog</span></span>      | <span data-ttu-id="bd728-247">Falso</span><span class="sxs-lookup"><span data-stu-id="bd728-247">False</span></span>                                                                                                 |
| <span data-ttu-id="bd728-248">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="bd728-248">NT-Security-Descriptor</span></span> | <span data-ttu-id="bd728-249">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="bd728-249">O:BAG:BAD:S:</span></span>                                                                                          |
| <span data-ttu-id="bd728-250">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bd728-250">Range-Lower</span></span>            | \-                                                                                                    |
| <span data-ttu-id="bd728-251">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bd728-251">Range-Upper</span></span>            | \-                                                                                                    |
| <span data-ttu-id="bd728-252">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bd728-252">Search-Flags</span></span>           | <span data-ttu-id="bd728-253">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bd728-253">0x00000000</span></span>                                                                                            |
| <span data-ttu-id="bd728-254">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bd728-254">System-Flags</span></span>           | <span data-ttu-id="bd728-255">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bd728-255">0x00000010</span></span>                                                                                            |
| <span data-ttu-id="bd728-256">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="bd728-256">Classes used in</span></span>        | [<span data-ttu-id="bd728-257">**Destinatario posta**</span><span class="sxs-lookup"><span data-stu-id="bd728-257">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> [<span data-ttu-id="bd728-258">**NTDS-Service**</span><span class="sxs-lookup"><span data-stu-id="bd728-258">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="bd728-259">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="bd728-259">Windows Server 2008 R2</span></span>



| <span data-ttu-id="bd728-260">Voce</span><span class="sxs-lookup"><span data-stu-id="bd728-260">Entry</span></span> | <span data-ttu-id="bd728-261">Valore</span><span class="sxs-lookup"><span data-stu-id="bd728-261">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd728-262">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="bd728-262">Link-Id</span></span>                | \-                                                                                                    |
| <span data-ttu-id="bd728-263">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bd728-263">MAPI-Id</span></span>                | <span data-ttu-id="bd728-264">0x80AF</span><span class="sxs-lookup"><span data-stu-id="bd728-264">0x80AF</span></span>                                                                                                |
| <span data-ttu-id="bd728-265">System-Only</span><span class="sxs-lookup"><span data-stu-id="bd728-265">System-Only</span></span>            | <span data-ttu-id="bd728-266">Falso</span><span class="sxs-lookup"><span data-stu-id="bd728-266">False</span></span>                                                                                                 |
| <span data-ttu-id="bd728-267">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="bd728-267">Is-Single-Valued</span></span>       | <span data-ttu-id="bd728-268">Vero</span><span class="sxs-lookup"><span data-stu-id="bd728-268">True</span></span>                                                                                                  |
| <span data-ttu-id="bd728-269">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="bd728-269">Is Indexed</span></span>             | <span data-ttu-id="bd728-270">Falso</span><span class="sxs-lookup"><span data-stu-id="bd728-270">False</span></span>                                                                                                 |
| <span data-ttu-id="bd728-271">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="bd728-271">In Global Catalog</span></span>      | <span data-ttu-id="bd728-272">Falso</span><span class="sxs-lookup"><span data-stu-id="bd728-272">False</span></span>                                                                                                 |
| <span data-ttu-id="bd728-273">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="bd728-273">NT-Security-Descriptor</span></span> | <span data-ttu-id="bd728-274">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="bd728-274">O:BAG:BAD:S:</span></span>                                                                                          |
| <span data-ttu-id="bd728-275">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bd728-275">Range-Lower</span></span>            | \-                                                                                                    |
| <span data-ttu-id="bd728-276">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bd728-276">Range-Upper</span></span>            | \-                                                                                                    |
| <span data-ttu-id="bd728-277">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bd728-277">Search-Flags</span></span>           | <span data-ttu-id="bd728-278">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bd728-278">0x00000000</span></span>                                                                                            |
| <span data-ttu-id="bd728-279">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bd728-279">System-Flags</span></span>           | <span data-ttu-id="bd728-280">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bd728-280">0x00000010</span></span>                                                                                            |
| <span data-ttu-id="bd728-281">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="bd728-281">Classes used in</span></span>        | [<span data-ttu-id="bd728-282">**Destinatario posta**</span><span class="sxs-lookup"><span data-stu-id="bd728-282">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> [<span data-ttu-id="bd728-283">**NTDS-Service**</span><span class="sxs-lookup"><span data-stu-id="bd728-283">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="bd728-284">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="bd728-284">Windows Server 2012</span></span>



| <span data-ttu-id="bd728-285">Voce</span><span class="sxs-lookup"><span data-stu-id="bd728-285">Entry</span></span> | <span data-ttu-id="bd728-286">Valore</span><span class="sxs-lookup"><span data-stu-id="bd728-286">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd728-287">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="bd728-287">Link-Id</span></span>                | \-                                                                                                    |
| <span data-ttu-id="bd728-288">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bd728-288">MAPI-Id</span></span>                | <span data-ttu-id="bd728-289">0x80AF</span><span class="sxs-lookup"><span data-stu-id="bd728-289">0x80AF</span></span>                                                                                                |
| <span data-ttu-id="bd728-290">System-Only</span><span class="sxs-lookup"><span data-stu-id="bd728-290">System-Only</span></span>            | <span data-ttu-id="bd728-291">Falso</span><span class="sxs-lookup"><span data-stu-id="bd728-291">False</span></span>                                                                                                 |
| <span data-ttu-id="bd728-292">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="bd728-292">Is-Single-Valued</span></span>       | <span data-ttu-id="bd728-293">Vero</span><span class="sxs-lookup"><span data-stu-id="bd728-293">True</span></span>                                                                                                  |
| <span data-ttu-id="bd728-294">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="bd728-294">Is Indexed</span></span>             | <span data-ttu-id="bd728-295">Falso</span><span class="sxs-lookup"><span data-stu-id="bd728-295">False</span></span>                                                                                                 |
| <span data-ttu-id="bd728-296">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="bd728-296">In Global Catalog</span></span>      | <span data-ttu-id="bd728-297">Falso</span><span class="sxs-lookup"><span data-stu-id="bd728-297">False</span></span>                                                                                                 |
| <span data-ttu-id="bd728-298">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="bd728-298">NT-Security-Descriptor</span></span> | <span data-ttu-id="bd728-299">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="bd728-299">O:BAG:BAD:S:</span></span>                                                                                          |
| <span data-ttu-id="bd728-300">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bd728-300">Range-Lower</span></span>            | \-                                                                                                    |
| <span data-ttu-id="bd728-301">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bd728-301">Range-Upper</span></span>            | \-                                                                                                    |
| <span data-ttu-id="bd728-302">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bd728-302">Search-Flags</span></span>           | <span data-ttu-id="bd728-303">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bd728-303">0x00000000</span></span>                                                                                            |
| <span data-ttu-id="bd728-304">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bd728-304">System-Flags</span></span>           | <span data-ttu-id="bd728-305">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bd728-305">0x00000010</span></span>                                                                                            |
| <span data-ttu-id="bd728-306">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="bd728-306">Classes used in</span></span>        | [<span data-ttu-id="bd728-307">**Destinatario posta**</span><span class="sxs-lookup"><span data-stu-id="bd728-307">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> [<span data-ttu-id="bd728-308">**NTDS-Service**</span><span class="sxs-lookup"><span data-stu-id="bd728-308">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



 

 





