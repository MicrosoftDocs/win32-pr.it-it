---
title: Attributo Retired-REPL-DSA-Signatures
description: Tiene traccia delle identità di replica DS precedenti di un determinato controller di dominio.
ms.assetid: 82e8b222-5635-41ad-b2ab-386c9e6aa280
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo Retired-REPL-DSA-Signatures
- Schema AD dell'attributo retiredReplDSASignatures
topic_type:
- apiref
api_name:
- Retired-Repl-DSA-Signatures
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a9a4cb4030a8d3aa24244bc2e7a2702e83686fc
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104401010"
---
# <a name="retired-repl-dsa-signatures-attribute"></a><span data-ttu-id="827fc-105">Attributo Retired-REPL-DSA-Signatures</span><span class="sxs-lookup"><span data-stu-id="827fc-105">Retired-Repl-DSA-Signatures attribute</span></span>

<span data-ttu-id="827fc-106">Tiene traccia delle identità di replica DS precedenti di un determinato controller di dominio.</span><span class="sxs-lookup"><span data-stu-id="827fc-106">Tracks the past DS replication identities of a given DC.</span></span>



| <span data-ttu-id="827fc-107">Voce</span><span class="sxs-lookup"><span data-stu-id="827fc-107">Entry</span></span> | <span data-ttu-id="827fc-108">Valore</span><span class="sxs-lookup"><span data-stu-id="827fc-108">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="827fc-109">CN</span><span class="sxs-lookup"><span data-stu-id="827fc-109">CN</span></span>                | <span data-ttu-id="827fc-110">Retired-REPL-DSA-firme</span><span class="sxs-lookup"><span data-stu-id="827fc-110">Retired-Repl-DSA-Signatures</span></span>                                                         |
| <span data-ttu-id="827fc-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="827fc-111">Ldap-Display-Name</span></span> | <span data-ttu-id="827fc-112">retiredReplDSASignatures</span><span class="sxs-lookup"><span data-stu-id="827fc-112">retiredReplDSASignatures</span></span>                                                            |
| <span data-ttu-id="827fc-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="827fc-113">Size</span></span>              | <span data-ttu-id="827fc-114">La lunghezza è proporzionale al numero di volte in cui il controller di dominio è stato ripristinato dal backup.</span><span class="sxs-lookup"><span data-stu-id="827fc-114">Length is proportional to the number of times the DC has been restored from backup.</span></span> |
| <span data-ttu-id="827fc-115">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="827fc-115">Update Privilege</span></span>  | <span data-ttu-id="827fc-116">Questo valore viene impostato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="827fc-116">This value is set by the system.</span></span>                                                    |
| <span data-ttu-id="827fc-117">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="827fc-117">Update Frequency</span></span>  | \-                                                                                  |
| <span data-ttu-id="827fc-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="827fc-118">Attribute-Id</span></span>      | <span data-ttu-id="827fc-119">1.2.840.113556.1.4.673</span><span class="sxs-lookup"><span data-stu-id="827fc-119">1.2.840.113556.1.4.673</span></span>                                                              |
| <span data-ttu-id="827fc-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="827fc-120">System-Id-Guid</span></span>    | <span data-ttu-id="827fc-121">7bfdcb7f-4807-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="827fc-121">7bfdcb7f-4807-11d1-a9c3-0000f80367c1</span></span>                                                |
| <span data-ttu-id="827fc-122">Sintassi</span><span class="sxs-lookup"><span data-stu-id="827fc-122">Syntax</span></span>            | [<span data-ttu-id="827fc-123">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="827fc-123">**Object(Replica-Link)**</span></span>](s-object-replica-link.md)                               |



## <a name="implementations"></a><span data-ttu-id="827fc-124">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="827fc-124">Implementations</span></span>

-   [<span data-ttu-id="827fc-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="827fc-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="827fc-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="827fc-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="827fc-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="827fc-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="827fc-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="827fc-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="827fc-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="827fc-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="827fc-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="827fc-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="827fc-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="827fc-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="827fc-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="827fc-132">Windows 2000 Server</span></span>



| <span data-ttu-id="827fc-133">Voce</span><span class="sxs-lookup"><span data-stu-id="827fc-133">Entry</span></span> | <span data-ttu-id="827fc-134">Valore</span><span class="sxs-lookup"><span data-stu-id="827fc-134">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="827fc-135">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="827fc-135">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="827fc-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="827fc-136">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="827fc-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="827fc-137">System-Only</span></span>            | <span data-ttu-id="827fc-138">Vero</span><span class="sxs-lookup"><span data-stu-id="827fc-138">True</span></span>                                     |
| <span data-ttu-id="827fc-139">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="827fc-139">Is-Single-Valued</span></span>       | <span data-ttu-id="827fc-140">Vero</span><span class="sxs-lookup"><span data-stu-id="827fc-140">True</span></span>                                     |
| <span data-ttu-id="827fc-141">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="827fc-141">Is Indexed</span></span>             | <span data-ttu-id="827fc-142">Falso</span><span class="sxs-lookup"><span data-stu-id="827fc-142">False</span></span>                                    |
| <span data-ttu-id="827fc-143">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="827fc-143">In Global Catalog</span></span>      | <span data-ttu-id="827fc-144">Falso</span><span class="sxs-lookup"><span data-stu-id="827fc-144">False</span></span>                                    |
| <span data-ttu-id="827fc-145">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="827fc-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="827fc-146">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="827fc-146">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="827fc-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="827fc-147">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="827fc-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="827fc-148">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="827fc-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="827fc-149">Search-Flags</span></span>           | <span data-ttu-id="827fc-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="827fc-150">0x00000000</span></span>                               |
| <span data-ttu-id="827fc-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="827fc-151">System-Flags</span></span>           | <span data-ttu-id="827fc-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="827fc-152">0x00000010</span></span>                               |
| <span data-ttu-id="827fc-153">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="827fc-153">Classes used in</span></span>        | [<span data-ttu-id="827fc-154">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="827fc-154">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="827fc-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="827fc-155">Windows Server 2003</span></span>



| <span data-ttu-id="827fc-156">Voce</span><span class="sxs-lookup"><span data-stu-id="827fc-156">Entry</span></span> | <span data-ttu-id="827fc-157">Valore</span><span class="sxs-lookup"><span data-stu-id="827fc-157">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="827fc-158">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="827fc-158">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="827fc-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="827fc-159">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="827fc-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="827fc-160">System-Only</span></span>            | <span data-ttu-id="827fc-161">Vero</span><span class="sxs-lookup"><span data-stu-id="827fc-161">True</span></span>                                     |
| <span data-ttu-id="827fc-162">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="827fc-162">Is-Single-Valued</span></span>       | <span data-ttu-id="827fc-163">Vero</span><span class="sxs-lookup"><span data-stu-id="827fc-163">True</span></span>                                     |
| <span data-ttu-id="827fc-164">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="827fc-164">Is Indexed</span></span>             | <span data-ttu-id="827fc-165">Falso</span><span class="sxs-lookup"><span data-stu-id="827fc-165">False</span></span>                                    |
| <span data-ttu-id="827fc-166">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="827fc-166">In Global Catalog</span></span>      | <span data-ttu-id="827fc-167">Falso</span><span class="sxs-lookup"><span data-stu-id="827fc-167">False</span></span>                                    |
| <span data-ttu-id="827fc-168">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="827fc-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="827fc-169">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="827fc-169">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="827fc-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="827fc-170">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="827fc-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="827fc-171">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="827fc-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="827fc-172">Search-Flags</span></span>           | <span data-ttu-id="827fc-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="827fc-173">0x00000000</span></span>                               |
| <span data-ttu-id="827fc-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="827fc-174">System-Flags</span></span>           | <span data-ttu-id="827fc-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="827fc-175">0x00000010</span></span>                               |
| <span data-ttu-id="827fc-176">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="827fc-176">Classes used in</span></span>        | [<span data-ttu-id="827fc-177">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="827fc-177">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="adam"></a><span data-ttu-id="827fc-178">ADAM</span><span class="sxs-lookup"><span data-stu-id="827fc-178">ADAM</span></span>



| <span data-ttu-id="827fc-179">Voce</span><span class="sxs-lookup"><span data-stu-id="827fc-179">Entry</span></span> | <span data-ttu-id="827fc-180">Valore</span><span class="sxs-lookup"><span data-stu-id="827fc-180">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="827fc-181">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="827fc-181">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="827fc-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="827fc-182">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="827fc-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="827fc-183">System-Only</span></span>            | <span data-ttu-id="827fc-184">Vero</span><span class="sxs-lookup"><span data-stu-id="827fc-184">True</span></span>                                     |
| <span data-ttu-id="827fc-185">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="827fc-185">Is-Single-Valued</span></span>       | <span data-ttu-id="827fc-186">Vero</span><span class="sxs-lookup"><span data-stu-id="827fc-186">True</span></span>                                     |
| <span data-ttu-id="827fc-187">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="827fc-187">Is Indexed</span></span>             | <span data-ttu-id="827fc-188">Falso</span><span class="sxs-lookup"><span data-stu-id="827fc-188">False</span></span>                                    |
| <span data-ttu-id="827fc-189">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="827fc-189">In Global Catalog</span></span>      | <span data-ttu-id="827fc-190">Falso</span><span class="sxs-lookup"><span data-stu-id="827fc-190">False</span></span>                                    |
| <span data-ttu-id="827fc-191">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="827fc-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="827fc-192">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="827fc-192">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="827fc-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="827fc-193">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="827fc-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="827fc-194">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="827fc-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="827fc-195">Search-Flags</span></span>           | <span data-ttu-id="827fc-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="827fc-196">0x00000000</span></span>                               |
| <span data-ttu-id="827fc-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="827fc-197">System-Flags</span></span>           | <span data-ttu-id="827fc-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="827fc-198">0x00000010</span></span>                               |
| <span data-ttu-id="827fc-199">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="827fc-199">Classes used in</span></span>        | [<span data-ttu-id="827fc-200">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="827fc-200">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="827fc-201">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="827fc-201">Windows Server 2003 R2</span></span>



| <span data-ttu-id="827fc-202">Voce</span><span class="sxs-lookup"><span data-stu-id="827fc-202">Entry</span></span> | <span data-ttu-id="827fc-203">Valore</span><span class="sxs-lookup"><span data-stu-id="827fc-203">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="827fc-204">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="827fc-204">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="827fc-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="827fc-205">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="827fc-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="827fc-206">System-Only</span></span>            | <span data-ttu-id="827fc-207">Vero</span><span class="sxs-lookup"><span data-stu-id="827fc-207">True</span></span>                                     |
| <span data-ttu-id="827fc-208">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="827fc-208">Is-Single-Valued</span></span>       | <span data-ttu-id="827fc-209">Vero</span><span class="sxs-lookup"><span data-stu-id="827fc-209">True</span></span>                                     |
| <span data-ttu-id="827fc-210">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="827fc-210">Is Indexed</span></span>             | <span data-ttu-id="827fc-211">Falso</span><span class="sxs-lookup"><span data-stu-id="827fc-211">False</span></span>                                    |
| <span data-ttu-id="827fc-212">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="827fc-212">In Global Catalog</span></span>      | <span data-ttu-id="827fc-213">Falso</span><span class="sxs-lookup"><span data-stu-id="827fc-213">False</span></span>                                    |
| <span data-ttu-id="827fc-214">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="827fc-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="827fc-215">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="827fc-215">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="827fc-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="827fc-216">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="827fc-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="827fc-217">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="827fc-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="827fc-218">Search-Flags</span></span>           | <span data-ttu-id="827fc-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="827fc-219">0x00000000</span></span>                               |
| <span data-ttu-id="827fc-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="827fc-220">System-Flags</span></span>           | <span data-ttu-id="827fc-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="827fc-221">0x00000010</span></span>                               |
| <span data-ttu-id="827fc-222">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="827fc-222">Classes used in</span></span>        | [<span data-ttu-id="827fc-223">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="827fc-223">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="827fc-224">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="827fc-224">Windows Server 2008</span></span>



| <span data-ttu-id="827fc-225">Voce</span><span class="sxs-lookup"><span data-stu-id="827fc-225">Entry</span></span> | <span data-ttu-id="827fc-226">Valore</span><span class="sxs-lookup"><span data-stu-id="827fc-226">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="827fc-227">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="827fc-227">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="827fc-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="827fc-228">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="827fc-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="827fc-229">System-Only</span></span>            | <span data-ttu-id="827fc-230">Vero</span><span class="sxs-lookup"><span data-stu-id="827fc-230">True</span></span>                                     |
| <span data-ttu-id="827fc-231">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="827fc-231">Is-Single-Valued</span></span>       | <span data-ttu-id="827fc-232">Vero</span><span class="sxs-lookup"><span data-stu-id="827fc-232">True</span></span>                                     |
| <span data-ttu-id="827fc-233">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="827fc-233">Is Indexed</span></span>             | <span data-ttu-id="827fc-234">Falso</span><span class="sxs-lookup"><span data-stu-id="827fc-234">False</span></span>                                    |
| <span data-ttu-id="827fc-235">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="827fc-235">In Global Catalog</span></span>      | <span data-ttu-id="827fc-236">Falso</span><span class="sxs-lookup"><span data-stu-id="827fc-236">False</span></span>                                    |
| <span data-ttu-id="827fc-237">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="827fc-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="827fc-238">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="827fc-238">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="827fc-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="827fc-239">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="827fc-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="827fc-240">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="827fc-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="827fc-241">Search-Flags</span></span>           | <span data-ttu-id="827fc-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="827fc-242">0x00000000</span></span>                               |
| <span data-ttu-id="827fc-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="827fc-243">System-Flags</span></span>           | <span data-ttu-id="827fc-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="827fc-244">0x00000010</span></span>                               |
| <span data-ttu-id="827fc-245">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="827fc-245">Classes used in</span></span>        | [<span data-ttu-id="827fc-246">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="827fc-246">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="827fc-247">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="827fc-247">Windows Server 2008 R2</span></span>



| <span data-ttu-id="827fc-248">Voce</span><span class="sxs-lookup"><span data-stu-id="827fc-248">Entry</span></span> | <span data-ttu-id="827fc-249">Valore</span><span class="sxs-lookup"><span data-stu-id="827fc-249">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="827fc-250">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="827fc-250">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="827fc-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="827fc-251">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="827fc-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="827fc-252">System-Only</span></span>            | <span data-ttu-id="827fc-253">Vero</span><span class="sxs-lookup"><span data-stu-id="827fc-253">True</span></span>                                     |
| <span data-ttu-id="827fc-254">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="827fc-254">Is-Single-Valued</span></span>       | <span data-ttu-id="827fc-255">Vero</span><span class="sxs-lookup"><span data-stu-id="827fc-255">True</span></span>                                     |
| <span data-ttu-id="827fc-256">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="827fc-256">Is Indexed</span></span>             | <span data-ttu-id="827fc-257">Falso</span><span class="sxs-lookup"><span data-stu-id="827fc-257">False</span></span>                                    |
| <span data-ttu-id="827fc-258">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="827fc-258">In Global Catalog</span></span>      | <span data-ttu-id="827fc-259">Falso</span><span class="sxs-lookup"><span data-stu-id="827fc-259">False</span></span>                                    |
| <span data-ttu-id="827fc-260">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="827fc-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="827fc-261">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="827fc-261">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="827fc-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="827fc-262">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="827fc-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="827fc-263">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="827fc-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="827fc-264">Search-Flags</span></span>           | <span data-ttu-id="827fc-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="827fc-265">0x00000000</span></span>                               |
| <span data-ttu-id="827fc-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="827fc-266">System-Flags</span></span>           | <span data-ttu-id="827fc-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="827fc-267">0x00000010</span></span>                               |
| <span data-ttu-id="827fc-268">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="827fc-268">Classes used in</span></span>        | [<span data-ttu-id="827fc-269">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="827fc-269">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="827fc-270">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="827fc-270">Windows Server 2012</span></span>



| <span data-ttu-id="827fc-271">Voce</span><span class="sxs-lookup"><span data-stu-id="827fc-271">Entry</span></span> | <span data-ttu-id="827fc-272">Valore</span><span class="sxs-lookup"><span data-stu-id="827fc-272">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="827fc-273">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="827fc-273">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="827fc-274">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="827fc-274">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="827fc-275">System-Only</span><span class="sxs-lookup"><span data-stu-id="827fc-275">System-Only</span></span>            | <span data-ttu-id="827fc-276">Vero</span><span class="sxs-lookup"><span data-stu-id="827fc-276">True</span></span>                                     |
| <span data-ttu-id="827fc-277">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="827fc-277">Is-Single-Valued</span></span>       | <span data-ttu-id="827fc-278">Vero</span><span class="sxs-lookup"><span data-stu-id="827fc-278">True</span></span>                                     |
| <span data-ttu-id="827fc-279">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="827fc-279">Is Indexed</span></span>             | <span data-ttu-id="827fc-280">Falso</span><span class="sxs-lookup"><span data-stu-id="827fc-280">False</span></span>                                    |
| <span data-ttu-id="827fc-281">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="827fc-281">In Global Catalog</span></span>      | <span data-ttu-id="827fc-282">Falso</span><span class="sxs-lookup"><span data-stu-id="827fc-282">False</span></span>                                    |
| <span data-ttu-id="827fc-283">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="827fc-283">NT-Security-Descriptor</span></span> | <span data-ttu-id="827fc-284">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="827fc-284">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="827fc-285">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="827fc-285">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="827fc-286">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="827fc-286">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="827fc-287">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="827fc-287">Search-Flags</span></span>           | <span data-ttu-id="827fc-288">0x00000000</span><span class="sxs-lookup"><span data-stu-id="827fc-288">0x00000000</span></span>                               |
| <span data-ttu-id="827fc-289">System-Flags</span><span class="sxs-lookup"><span data-stu-id="827fc-289">System-Flags</span></span>           | <span data-ttu-id="827fc-290">0x00000010</span><span class="sxs-lookup"><span data-stu-id="827fc-290">0x00000010</span></span>                               |
| <span data-ttu-id="827fc-291">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="827fc-291">Classes used in</span></span>        | [<span data-ttu-id="827fc-292">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="827fc-292">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



 

 





