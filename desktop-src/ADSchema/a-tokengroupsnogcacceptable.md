---
title: Token-Groups-No-GC-acceptable (attributo)
description: Questo attributo contiene l'elenco dei SID a causa di un'operazione di espansione dell'appartenenza a un gruppo transitiva su un determinato utente o computer. Non è possibile recuperare i gruppi di token se non è presente un catalogo globale per recuperare le appartenenze inverse transitive.
ms.assetid: 08718c69-6339-40dc-8486-a7cd72028ed1
ms.tgt_platform: multiple
keywords:
- Token-Groups-No-GC-acceptable attribute AD schema
- Schema AD dell'attributo tokenGroupsNoGCAcceptable
topic_type:
- apiref
api_name:
- Token-Groups-No-GC-Acceptable
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a87c4b8996586c8c35ed4c815b954dad02b5db03
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103875130"
---
# <a name="token-groups-no-gc-acceptable-attribute"></a><span data-ttu-id="25173-106">Token-Groups-No-GC-acceptable (attributo)</span><span class="sxs-lookup"><span data-stu-id="25173-106">Token-Groups-No-GC-Acceptable attribute</span></span>

<span data-ttu-id="25173-107">Questo attributo contiene l'elenco dei SID a causa di un'operazione di espansione dell'appartenenza a un gruppo transitiva su un determinato utente o computer.</span><span class="sxs-lookup"><span data-stu-id="25173-107">This attribute contains the list of SIDs due to a transitive group membership expansion operation on a given user or computer.</span></span> <span data-ttu-id="25173-108">Non è possibile recuperare i gruppi di token se non è presente un catalogo globale per recuperare le appartenenze inverse transitive.</span><span class="sxs-lookup"><span data-stu-id="25173-108">Token groups cannot be retrieved if a Global Catalog is not present to retrieve the transitive reverse memberships.</span></span>



| <span data-ttu-id="25173-109">Voce</span><span class="sxs-lookup"><span data-stu-id="25173-109">Entry</span></span> | <span data-ttu-id="25173-110">Valore</span><span class="sxs-lookup"><span data-stu-id="25173-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="25173-111">CN</span><span class="sxs-lookup"><span data-stu-id="25173-111">CN</span></span>                | <span data-ttu-id="25173-112">Token-Groups-No-GC-accettabile</span><span class="sxs-lookup"><span data-stu-id="25173-112">Token-Groups-No-GC-Acceptable</span></span>        |
| <span data-ttu-id="25173-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="25173-113">Ldap-Display-Name</span></span> | <span data-ttu-id="25173-114">tokenGroupsNoGCAcceptable</span><span class="sxs-lookup"><span data-stu-id="25173-114">tokenGroupsNoGCAcceptable</span></span>            |
| <span data-ttu-id="25173-115">Dimensione</span><span class="sxs-lookup"><span data-stu-id="25173-115">Size</span></span>              | \-                                   |
| <span data-ttu-id="25173-116">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="25173-116">Update Privilege</span></span>  | <span data-ttu-id="25173-117">Questo valore viene impostato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="25173-117">The system sets this value.</span></span>          |
| <span data-ttu-id="25173-118">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="25173-118">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="25173-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="25173-119">Attribute-Id</span></span>      | <span data-ttu-id="25173-120">1.2.840.113556.1.4.1303</span><span class="sxs-lookup"><span data-stu-id="25173-120">1.2.840.113556.1.4.1303</span></span>              |
| <span data-ttu-id="25173-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="25173-121">System-Id-Guid</span></span>    | <span data-ttu-id="25173-122">040fc392-33df-11d2-98b2-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="25173-122">040fc392-33df-11d2-98b2-0000f87a57d4</span></span> |
| <span data-ttu-id="25173-123">Sintassi</span><span class="sxs-lookup"><span data-stu-id="25173-123">Syntax</span></span>            | [<span data-ttu-id="25173-124">**Stringa (SID)**</span><span class="sxs-lookup"><span data-stu-id="25173-124">**String(Sid)**</span></span>](s-string-sid.md)  |



## <a name="implementations"></a><span data-ttu-id="25173-125">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="25173-125">Implementations</span></span>

-   [<span data-ttu-id="25173-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="25173-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="25173-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="25173-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="25173-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="25173-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="25173-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="25173-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="25173-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="25173-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="25173-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="25173-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="25173-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="25173-132">Windows 2000 Server</span></span>



| <span data-ttu-id="25173-133">Voce</span><span class="sxs-lookup"><span data-stu-id="25173-133">Entry</span></span> | <span data-ttu-id="25173-134">Valore</span><span class="sxs-lookup"><span data-stu-id="25173-134">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="25173-135">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="25173-135">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="25173-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="25173-136">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="25173-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="25173-137">System-Only</span></span>            | <span data-ttu-id="25173-138">Falso</span><span class="sxs-lookup"><span data-stu-id="25173-138">False</span></span>                                                        |
| <span data-ttu-id="25173-139">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="25173-139">Is-Single-Valued</span></span>       | <span data-ttu-id="25173-140">Falso</span><span class="sxs-lookup"><span data-stu-id="25173-140">False</span></span>                                                        |
| <span data-ttu-id="25173-141">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="25173-141">Is Indexed</span></span>             | <span data-ttu-id="25173-142">Falso</span><span class="sxs-lookup"><span data-stu-id="25173-142">False</span></span>                                                        |
| <span data-ttu-id="25173-143">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="25173-143">In Global Catalog</span></span>      | <span data-ttu-id="25173-144">Falso</span><span class="sxs-lookup"><span data-stu-id="25173-144">False</span></span>                                                        |
| <span data-ttu-id="25173-145">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="25173-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="25173-146">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="25173-146">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="25173-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="25173-147">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="25173-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="25173-148">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="25173-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="25173-149">Search-Flags</span></span>           | <span data-ttu-id="25173-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="25173-150">0x00000000</span></span>                                                   |
| <span data-ttu-id="25173-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="25173-151">System-Flags</span></span>           | <span data-ttu-id="25173-152">0x08000014</span><span class="sxs-lookup"><span data-stu-id="25173-152">0x08000014</span></span>                                                   |
| <span data-ttu-id="25173-153">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="25173-153">Classes used in</span></span>        | [<span data-ttu-id="25173-154">**Entità di sicurezza**</span><span class="sxs-lookup"><span data-stu-id="25173-154">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="25173-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="25173-155">Windows Server 2003</span></span>



| <span data-ttu-id="25173-156">Voce</span><span class="sxs-lookup"><span data-stu-id="25173-156">Entry</span></span> | <span data-ttu-id="25173-157">Valore</span><span class="sxs-lookup"><span data-stu-id="25173-157">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="25173-158">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="25173-158">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="25173-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="25173-159">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="25173-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="25173-160">System-Only</span></span>            | <span data-ttu-id="25173-161">Falso</span><span class="sxs-lookup"><span data-stu-id="25173-161">False</span></span>                                                        |
| <span data-ttu-id="25173-162">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="25173-162">Is-Single-Valued</span></span>       | <span data-ttu-id="25173-163">Falso</span><span class="sxs-lookup"><span data-stu-id="25173-163">False</span></span>                                                        |
| <span data-ttu-id="25173-164">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="25173-164">Is Indexed</span></span>             | <span data-ttu-id="25173-165">Falso</span><span class="sxs-lookup"><span data-stu-id="25173-165">False</span></span>                                                        |
| <span data-ttu-id="25173-166">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="25173-166">In Global Catalog</span></span>      | <span data-ttu-id="25173-167">Falso</span><span class="sxs-lookup"><span data-stu-id="25173-167">False</span></span>                                                        |
| <span data-ttu-id="25173-168">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="25173-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="25173-169">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="25173-169">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="25173-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="25173-170">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="25173-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="25173-171">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="25173-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="25173-172">Search-Flags</span></span>           | <span data-ttu-id="25173-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="25173-173">0x00000000</span></span>                                                   |
| <span data-ttu-id="25173-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="25173-174">System-Flags</span></span>           | <span data-ttu-id="25173-175">0x08000014</span><span class="sxs-lookup"><span data-stu-id="25173-175">0x08000014</span></span>                                                   |
| <span data-ttu-id="25173-176">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="25173-176">Classes used in</span></span>        | [<span data-ttu-id="25173-177">**Entità di sicurezza**</span><span class="sxs-lookup"><span data-stu-id="25173-177">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="25173-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="25173-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="25173-179">Voce</span><span class="sxs-lookup"><span data-stu-id="25173-179">Entry</span></span> | <span data-ttu-id="25173-180">Valore</span><span class="sxs-lookup"><span data-stu-id="25173-180">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="25173-181">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="25173-181">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="25173-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="25173-182">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="25173-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="25173-183">System-Only</span></span>            | <span data-ttu-id="25173-184">Falso</span><span class="sxs-lookup"><span data-stu-id="25173-184">False</span></span>                                                        |
| <span data-ttu-id="25173-185">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="25173-185">Is-Single-Valued</span></span>       | <span data-ttu-id="25173-186">Falso</span><span class="sxs-lookup"><span data-stu-id="25173-186">False</span></span>                                                        |
| <span data-ttu-id="25173-187">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="25173-187">Is Indexed</span></span>             | <span data-ttu-id="25173-188">Falso</span><span class="sxs-lookup"><span data-stu-id="25173-188">False</span></span>                                                        |
| <span data-ttu-id="25173-189">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="25173-189">In Global Catalog</span></span>      | <span data-ttu-id="25173-190">Falso</span><span class="sxs-lookup"><span data-stu-id="25173-190">False</span></span>                                                        |
| <span data-ttu-id="25173-191">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="25173-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="25173-192">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="25173-192">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="25173-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="25173-193">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="25173-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="25173-194">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="25173-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="25173-195">Search-Flags</span></span>           | <span data-ttu-id="25173-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="25173-196">0x00000000</span></span>                                                   |
| <span data-ttu-id="25173-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="25173-197">System-Flags</span></span>           | <span data-ttu-id="25173-198">0x08000014</span><span class="sxs-lookup"><span data-stu-id="25173-198">0x08000014</span></span>                                                   |
| <span data-ttu-id="25173-199">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="25173-199">Classes used in</span></span>        | [<span data-ttu-id="25173-200">**Entità di sicurezza**</span><span class="sxs-lookup"><span data-stu-id="25173-200">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="25173-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="25173-201">Windows Server 2008</span></span>



| <span data-ttu-id="25173-202">Voce</span><span class="sxs-lookup"><span data-stu-id="25173-202">Entry</span></span> | <span data-ttu-id="25173-203">Valore</span><span class="sxs-lookup"><span data-stu-id="25173-203">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="25173-204">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="25173-204">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="25173-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="25173-205">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="25173-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="25173-206">System-Only</span></span>            | <span data-ttu-id="25173-207">Falso</span><span class="sxs-lookup"><span data-stu-id="25173-207">False</span></span>                                                        |
| <span data-ttu-id="25173-208">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="25173-208">Is-Single-Valued</span></span>       | <span data-ttu-id="25173-209">Falso</span><span class="sxs-lookup"><span data-stu-id="25173-209">False</span></span>                                                        |
| <span data-ttu-id="25173-210">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="25173-210">Is Indexed</span></span>             | <span data-ttu-id="25173-211">Falso</span><span class="sxs-lookup"><span data-stu-id="25173-211">False</span></span>                                                        |
| <span data-ttu-id="25173-212">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="25173-212">In Global Catalog</span></span>      | <span data-ttu-id="25173-213">Falso</span><span class="sxs-lookup"><span data-stu-id="25173-213">False</span></span>                                                        |
| <span data-ttu-id="25173-214">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="25173-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="25173-215">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="25173-215">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="25173-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="25173-216">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="25173-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="25173-217">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="25173-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="25173-218">Search-Flags</span></span>           | <span data-ttu-id="25173-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="25173-219">0x00000000</span></span>                                                   |
| <span data-ttu-id="25173-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="25173-220">System-Flags</span></span>           | <span data-ttu-id="25173-221">0x08000014</span><span class="sxs-lookup"><span data-stu-id="25173-221">0x08000014</span></span>                                                   |
| <span data-ttu-id="25173-222">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="25173-222">Classes used in</span></span>        | [<span data-ttu-id="25173-223">**Entità di sicurezza**</span><span class="sxs-lookup"><span data-stu-id="25173-223">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="25173-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="25173-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="25173-225">Voce</span><span class="sxs-lookup"><span data-stu-id="25173-225">Entry</span></span> | <span data-ttu-id="25173-226">Valore</span><span class="sxs-lookup"><span data-stu-id="25173-226">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="25173-227">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="25173-227">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="25173-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="25173-228">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="25173-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="25173-229">System-Only</span></span>            | <span data-ttu-id="25173-230">Falso</span><span class="sxs-lookup"><span data-stu-id="25173-230">False</span></span>                                                        |
| <span data-ttu-id="25173-231">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="25173-231">Is-Single-Valued</span></span>       | <span data-ttu-id="25173-232">Falso</span><span class="sxs-lookup"><span data-stu-id="25173-232">False</span></span>                                                        |
| <span data-ttu-id="25173-233">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="25173-233">Is Indexed</span></span>             | <span data-ttu-id="25173-234">Falso</span><span class="sxs-lookup"><span data-stu-id="25173-234">False</span></span>                                                        |
| <span data-ttu-id="25173-235">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="25173-235">In Global Catalog</span></span>      | <span data-ttu-id="25173-236">Falso</span><span class="sxs-lookup"><span data-stu-id="25173-236">False</span></span>                                                        |
| <span data-ttu-id="25173-237">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="25173-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="25173-238">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="25173-238">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="25173-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="25173-239">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="25173-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="25173-240">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="25173-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="25173-241">Search-Flags</span></span>           | <span data-ttu-id="25173-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="25173-242">0x00000000</span></span>                                                   |
| <span data-ttu-id="25173-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="25173-243">System-Flags</span></span>           | <span data-ttu-id="25173-244">0x08000014</span><span class="sxs-lookup"><span data-stu-id="25173-244">0x08000014</span></span>                                                   |
| <span data-ttu-id="25173-245">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="25173-245">Classes used in</span></span>        | [<span data-ttu-id="25173-246">**Entità di sicurezza**</span><span class="sxs-lookup"><span data-stu-id="25173-246">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="25173-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="25173-247">Windows Server 2012</span></span>



| <span data-ttu-id="25173-248">Voce</span><span class="sxs-lookup"><span data-stu-id="25173-248">Entry</span></span> | <span data-ttu-id="25173-249">Valore</span><span class="sxs-lookup"><span data-stu-id="25173-249">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="25173-250">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="25173-250">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="25173-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="25173-251">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="25173-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="25173-252">System-Only</span></span>            | <span data-ttu-id="25173-253">Falso</span><span class="sxs-lookup"><span data-stu-id="25173-253">False</span></span>                                                        |
| <span data-ttu-id="25173-254">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="25173-254">Is-Single-Valued</span></span>       | <span data-ttu-id="25173-255">Falso</span><span class="sxs-lookup"><span data-stu-id="25173-255">False</span></span>                                                        |
| <span data-ttu-id="25173-256">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="25173-256">Is Indexed</span></span>             | <span data-ttu-id="25173-257">Falso</span><span class="sxs-lookup"><span data-stu-id="25173-257">False</span></span>                                                        |
| <span data-ttu-id="25173-258">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="25173-258">In Global Catalog</span></span>      | <span data-ttu-id="25173-259">Falso</span><span class="sxs-lookup"><span data-stu-id="25173-259">False</span></span>                                                        |
| <span data-ttu-id="25173-260">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="25173-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="25173-261">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="25173-261">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="25173-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="25173-262">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="25173-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="25173-263">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="25173-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="25173-264">Search-Flags</span></span>           | <span data-ttu-id="25173-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="25173-265">0x00000000</span></span>                                                   |
| <span data-ttu-id="25173-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="25173-266">System-Flags</span></span>           | <span data-ttu-id="25173-267">0x08000014</span><span class="sxs-lookup"><span data-stu-id="25173-267">0x08000014</span></span>                                                   |
| <span data-ttu-id="25173-268">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="25173-268">Classes used in</span></span>        | [<span data-ttu-id="25173-269">**Entità di sicurezza**</span><span class="sxs-lookup"><span data-stu-id="25173-269">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



 

 





