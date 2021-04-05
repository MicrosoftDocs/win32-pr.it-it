---
title: Attributo MS-DS-coerenza-GUID
description: Questo attributo viene utilizzato per verificare la coerenza tra la directory e un altro oggetto, database o applicazione, confrontando i GUID.
ms.assetid: 1372f46a-5569-4b06-9803-7d3862cdb745
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo MS-DS-coerenza-GUID
- Schema AD dell'attributo mS-DS-ConsistencyGuid
topic_type:
- apiref
api_name:
- MS-DS-Consistency-Guid
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8fdbea1e9fba4ac28f968fdd61a054f55fe47deb
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103875438"
---
# <a name="ms-ds-consistency-guid-attribute"></a><span data-ttu-id="db096-105">Attributo MS-DS-coerenza-GUID</span><span class="sxs-lookup"><span data-stu-id="db096-105">MS-DS-Consistency-Guid attribute</span></span>

<span data-ttu-id="db096-106">Questo attributo viene utilizzato per verificare la coerenza tra la directory e un altro oggetto, database o applicazione, confrontando i GUID.</span><span class="sxs-lookup"><span data-stu-id="db096-106">This attribute is used to check consistency between the directory and another object, database, or application, by comparing GUIDs.</span></span>



| <span data-ttu-id="db096-107">Voce</span><span class="sxs-lookup"><span data-stu-id="db096-107">Entry</span></span> | <span data-ttu-id="db096-108">Valore</span><span class="sxs-lookup"><span data-stu-id="db096-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="db096-109">CN</span><span class="sxs-lookup"><span data-stu-id="db096-109">CN</span></span>                | <span data-ttu-id="db096-110">MS-DS-Consistency-Guid</span><span class="sxs-lookup"><span data-stu-id="db096-110">MS-DS-Consistency-Guid</span></span>                                |
| <span data-ttu-id="db096-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="db096-111">Ldap-Display-Name</span></span> | <span data-ttu-id="db096-112">mS-DS-ConsistencyGuid</span><span class="sxs-lookup"><span data-stu-id="db096-112">mS-DS-ConsistencyGuid</span></span>                                 |
| <span data-ttu-id="db096-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="db096-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="db096-114">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="db096-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="db096-115">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="db096-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="db096-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="db096-116">Attribute-Id</span></span>      | <span data-ttu-id="db096-117">1.2.840.113556.1.4.1360</span><span class="sxs-lookup"><span data-stu-id="db096-117">1.2.840.113556.1.4.1360</span></span>                               |
| <span data-ttu-id="db096-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="db096-118">System-Id-Guid</span></span>    | <span data-ttu-id="db096-119">23773dc2-b63a-11d2-90e1-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="db096-119">23773dc2-b63a-11d2-90e1-00c04fd91ab1</span></span>                  |
| <span data-ttu-id="db096-120">Sintassi</span><span class="sxs-lookup"><span data-stu-id="db096-120">Syntax</span></span>            | [<span data-ttu-id="db096-121">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="db096-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="db096-122">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="db096-122">Implementations</span></span>

-   [<span data-ttu-id="db096-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="db096-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="db096-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="db096-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="db096-125">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="db096-125">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="db096-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="db096-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="db096-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="db096-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="db096-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="db096-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="db096-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="db096-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="db096-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="db096-130">Windows 2000 Server</span></span>



| <span data-ttu-id="db096-131">Voce</span><span class="sxs-lookup"><span data-stu-id="db096-131">Entry</span></span> | <span data-ttu-id="db096-132">Valore</span><span class="sxs-lookup"><span data-stu-id="db096-132">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="db096-133">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="db096-133">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="db096-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="db096-134">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="db096-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="db096-135">System-Only</span></span>            | <span data-ttu-id="db096-136">Falso</span><span class="sxs-lookup"><span data-stu-id="db096-136">False</span></span>                           |
| <span data-ttu-id="db096-137">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="db096-137">Is-Single-Valued</span></span>       | <span data-ttu-id="db096-138">Vero</span><span class="sxs-lookup"><span data-stu-id="db096-138">True</span></span>                            |
| <span data-ttu-id="db096-139">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="db096-139">Is Indexed</span></span>             | <span data-ttu-id="db096-140">Falso</span><span class="sxs-lookup"><span data-stu-id="db096-140">False</span></span>                           |
| <span data-ttu-id="db096-141">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="db096-141">In Global Catalog</span></span>      | <span data-ttu-id="db096-142">Falso</span><span class="sxs-lookup"><span data-stu-id="db096-142">False</span></span>                           |
| <span data-ttu-id="db096-143">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="db096-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="db096-144">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="db096-144">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="db096-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="db096-145">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="db096-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="db096-146">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="db096-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="db096-147">Search-Flags</span></span>           | <span data-ttu-id="db096-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="db096-148">0x00000000</span></span>                      |
| <span data-ttu-id="db096-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="db096-149">System-Flags</span></span>           | <span data-ttu-id="db096-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="db096-150">0x00000010</span></span>                      |
| <span data-ttu-id="db096-151">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="db096-151">Classes used in</span></span>        | [<span data-ttu-id="db096-152">**In alto**</span><span class="sxs-lookup"><span data-stu-id="db096-152">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="db096-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="db096-153">Windows Server 2003</span></span>



| <span data-ttu-id="db096-154">Voce</span><span class="sxs-lookup"><span data-stu-id="db096-154">Entry</span></span> | <span data-ttu-id="db096-155">Valore</span><span class="sxs-lookup"><span data-stu-id="db096-155">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="db096-156">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="db096-156">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="db096-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="db096-157">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="db096-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="db096-158">System-Only</span></span>            | <span data-ttu-id="db096-159">Falso</span><span class="sxs-lookup"><span data-stu-id="db096-159">False</span></span>                           |
| <span data-ttu-id="db096-160">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="db096-160">Is-Single-Valued</span></span>       | <span data-ttu-id="db096-161">Vero</span><span class="sxs-lookup"><span data-stu-id="db096-161">True</span></span>                            |
| <span data-ttu-id="db096-162">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="db096-162">Is Indexed</span></span>             | <span data-ttu-id="db096-163">Falso</span><span class="sxs-lookup"><span data-stu-id="db096-163">False</span></span>                           |
| <span data-ttu-id="db096-164">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="db096-164">In Global Catalog</span></span>      | <span data-ttu-id="db096-165">Falso</span><span class="sxs-lookup"><span data-stu-id="db096-165">False</span></span>                           |
| <span data-ttu-id="db096-166">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="db096-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="db096-167">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="db096-167">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="db096-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="db096-168">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="db096-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="db096-169">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="db096-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="db096-170">Search-Flags</span></span>           | <span data-ttu-id="db096-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="db096-171">0x00000000</span></span>                      |
| <span data-ttu-id="db096-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="db096-172">System-Flags</span></span>           | <span data-ttu-id="db096-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="db096-173">0x00000010</span></span>                      |
| <span data-ttu-id="db096-174">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="db096-174">Classes used in</span></span>        | [<span data-ttu-id="db096-175">**In alto**</span><span class="sxs-lookup"><span data-stu-id="db096-175">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="db096-176">ADAM</span><span class="sxs-lookup"><span data-stu-id="db096-176">ADAM</span></span>



| <span data-ttu-id="db096-177">Voce</span><span class="sxs-lookup"><span data-stu-id="db096-177">Entry</span></span> | <span data-ttu-id="db096-178">Valore</span><span class="sxs-lookup"><span data-stu-id="db096-178">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="db096-179">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="db096-179">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="db096-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="db096-180">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="db096-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="db096-181">System-Only</span></span>            | <span data-ttu-id="db096-182">Falso</span><span class="sxs-lookup"><span data-stu-id="db096-182">False</span></span>                           |
| <span data-ttu-id="db096-183">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="db096-183">Is-Single-Valued</span></span>       | <span data-ttu-id="db096-184">Vero</span><span class="sxs-lookup"><span data-stu-id="db096-184">True</span></span>                            |
| <span data-ttu-id="db096-185">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="db096-185">Is Indexed</span></span>             | <span data-ttu-id="db096-186">Falso</span><span class="sxs-lookup"><span data-stu-id="db096-186">False</span></span>                           |
| <span data-ttu-id="db096-187">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="db096-187">In Global Catalog</span></span>      | <span data-ttu-id="db096-188">Falso</span><span class="sxs-lookup"><span data-stu-id="db096-188">False</span></span>                           |
| <span data-ttu-id="db096-189">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="db096-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="db096-190">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="db096-190">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="db096-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="db096-191">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="db096-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="db096-192">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="db096-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="db096-193">Search-Flags</span></span>           | <span data-ttu-id="db096-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="db096-194">0x00000000</span></span>                      |
| <span data-ttu-id="db096-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="db096-195">System-Flags</span></span>           | <span data-ttu-id="db096-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="db096-196">0x00000010</span></span>                      |
| <span data-ttu-id="db096-197">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="db096-197">Classes used in</span></span>        | [<span data-ttu-id="db096-198">**In alto**</span><span class="sxs-lookup"><span data-stu-id="db096-198">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="db096-199">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="db096-199">Windows Server 2003 R2</span></span>



| <span data-ttu-id="db096-200">Voce</span><span class="sxs-lookup"><span data-stu-id="db096-200">Entry</span></span> | <span data-ttu-id="db096-201">Valore</span><span class="sxs-lookup"><span data-stu-id="db096-201">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="db096-202">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="db096-202">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="db096-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="db096-203">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="db096-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="db096-204">System-Only</span></span>            | <span data-ttu-id="db096-205">Falso</span><span class="sxs-lookup"><span data-stu-id="db096-205">False</span></span>                           |
| <span data-ttu-id="db096-206">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="db096-206">Is-Single-Valued</span></span>       | <span data-ttu-id="db096-207">Vero</span><span class="sxs-lookup"><span data-stu-id="db096-207">True</span></span>                            |
| <span data-ttu-id="db096-208">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="db096-208">Is Indexed</span></span>             | <span data-ttu-id="db096-209">Falso</span><span class="sxs-lookup"><span data-stu-id="db096-209">False</span></span>                           |
| <span data-ttu-id="db096-210">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="db096-210">In Global Catalog</span></span>      | <span data-ttu-id="db096-211">Falso</span><span class="sxs-lookup"><span data-stu-id="db096-211">False</span></span>                           |
| <span data-ttu-id="db096-212">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="db096-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="db096-213">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="db096-213">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="db096-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="db096-214">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="db096-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="db096-215">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="db096-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="db096-216">Search-Flags</span></span>           | <span data-ttu-id="db096-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="db096-217">0x00000000</span></span>                      |
| <span data-ttu-id="db096-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="db096-218">System-Flags</span></span>           | <span data-ttu-id="db096-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="db096-219">0x00000010</span></span>                      |
| <span data-ttu-id="db096-220">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="db096-220">Classes used in</span></span>        | [<span data-ttu-id="db096-221">**In alto**</span><span class="sxs-lookup"><span data-stu-id="db096-221">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="db096-222">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="db096-222">Windows Server 2008</span></span>



| <span data-ttu-id="db096-223">Voce</span><span class="sxs-lookup"><span data-stu-id="db096-223">Entry</span></span> | <span data-ttu-id="db096-224">Valore</span><span class="sxs-lookup"><span data-stu-id="db096-224">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="db096-225">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="db096-225">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="db096-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="db096-226">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="db096-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="db096-227">System-Only</span></span>            | <span data-ttu-id="db096-228">Falso</span><span class="sxs-lookup"><span data-stu-id="db096-228">False</span></span>                           |
| <span data-ttu-id="db096-229">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="db096-229">Is-Single-Valued</span></span>       | <span data-ttu-id="db096-230">Vero</span><span class="sxs-lookup"><span data-stu-id="db096-230">True</span></span>                            |
| <span data-ttu-id="db096-231">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="db096-231">Is Indexed</span></span>             | <span data-ttu-id="db096-232">Falso</span><span class="sxs-lookup"><span data-stu-id="db096-232">False</span></span>                           |
| <span data-ttu-id="db096-233">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="db096-233">In Global Catalog</span></span>      | <span data-ttu-id="db096-234">Falso</span><span class="sxs-lookup"><span data-stu-id="db096-234">False</span></span>                           |
| <span data-ttu-id="db096-235">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="db096-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="db096-236">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="db096-236">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="db096-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="db096-237">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="db096-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="db096-238">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="db096-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="db096-239">Search-Flags</span></span>           | <span data-ttu-id="db096-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="db096-240">0x00000000</span></span>                      |
| <span data-ttu-id="db096-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="db096-241">System-Flags</span></span>           | <span data-ttu-id="db096-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="db096-242">0x00000010</span></span>                      |
| <span data-ttu-id="db096-243">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="db096-243">Classes used in</span></span>        | [<span data-ttu-id="db096-244">**In alto**</span><span class="sxs-lookup"><span data-stu-id="db096-244">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="db096-245">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="db096-245">Windows Server 2008 R2</span></span>



| <span data-ttu-id="db096-246">Voce</span><span class="sxs-lookup"><span data-stu-id="db096-246">Entry</span></span> | <span data-ttu-id="db096-247">Valore</span><span class="sxs-lookup"><span data-stu-id="db096-247">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="db096-248">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="db096-248">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="db096-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="db096-249">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="db096-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="db096-250">System-Only</span></span>            | <span data-ttu-id="db096-251">Falso</span><span class="sxs-lookup"><span data-stu-id="db096-251">False</span></span>                           |
| <span data-ttu-id="db096-252">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="db096-252">Is-Single-Valued</span></span>       | <span data-ttu-id="db096-253">Vero</span><span class="sxs-lookup"><span data-stu-id="db096-253">True</span></span>                            |
| <span data-ttu-id="db096-254">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="db096-254">Is Indexed</span></span>             | <span data-ttu-id="db096-255">Falso</span><span class="sxs-lookup"><span data-stu-id="db096-255">False</span></span>                           |
| <span data-ttu-id="db096-256">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="db096-256">In Global Catalog</span></span>      | <span data-ttu-id="db096-257">Falso</span><span class="sxs-lookup"><span data-stu-id="db096-257">False</span></span>                           |
| <span data-ttu-id="db096-258">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="db096-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="db096-259">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="db096-259">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="db096-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="db096-260">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="db096-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="db096-261">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="db096-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="db096-262">Search-Flags</span></span>           | <span data-ttu-id="db096-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="db096-263">0x00000000</span></span>                      |
| <span data-ttu-id="db096-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="db096-264">System-Flags</span></span>           | <span data-ttu-id="db096-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="db096-265">0x00000010</span></span>                      |
| <span data-ttu-id="db096-266">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="db096-266">Classes used in</span></span>        | [<span data-ttu-id="db096-267">**In alto**</span><span class="sxs-lookup"><span data-stu-id="db096-267">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="db096-268">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="db096-268">Windows Server 2012</span></span>



| <span data-ttu-id="db096-269">Voce</span><span class="sxs-lookup"><span data-stu-id="db096-269">Entry</span></span> | <span data-ttu-id="db096-270">Valore</span><span class="sxs-lookup"><span data-stu-id="db096-270">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="db096-271">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="db096-271">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="db096-272">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="db096-272">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="db096-273">System-Only</span><span class="sxs-lookup"><span data-stu-id="db096-273">System-Only</span></span>            | <span data-ttu-id="db096-274">Falso</span><span class="sxs-lookup"><span data-stu-id="db096-274">False</span></span>                           |
| <span data-ttu-id="db096-275">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="db096-275">Is-Single-Valued</span></span>       | <span data-ttu-id="db096-276">Vero</span><span class="sxs-lookup"><span data-stu-id="db096-276">True</span></span>                            |
| <span data-ttu-id="db096-277">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="db096-277">Is Indexed</span></span>             | <span data-ttu-id="db096-278">Falso</span><span class="sxs-lookup"><span data-stu-id="db096-278">False</span></span>                           |
| <span data-ttu-id="db096-279">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="db096-279">In Global Catalog</span></span>      | <span data-ttu-id="db096-280">Falso</span><span class="sxs-lookup"><span data-stu-id="db096-280">False</span></span>                           |
| <span data-ttu-id="db096-281">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="db096-281">NT-Security-Descriptor</span></span> | <span data-ttu-id="db096-282">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="db096-282">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="db096-283">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="db096-283">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="db096-284">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="db096-284">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="db096-285">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="db096-285">Search-Flags</span></span>           | <span data-ttu-id="db096-286">0x00000000</span><span class="sxs-lookup"><span data-stu-id="db096-286">0x00000000</span></span>                      |
| <span data-ttu-id="db096-287">System-Flags</span><span class="sxs-lookup"><span data-stu-id="db096-287">System-Flags</span></span>           | <span data-ttu-id="db096-288">0x00000010</span><span class="sxs-lookup"><span data-stu-id="db096-288">0x00000010</span></span>                      |
| <span data-ttu-id="db096-289">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="db096-289">Classes used in</span></span>        | [<span data-ttu-id="db096-290">**In alto**</span><span class="sxs-lookup"><span data-stu-id="db096-290">**Top**</span></span>](c-top.md)<br/> |



 

 





