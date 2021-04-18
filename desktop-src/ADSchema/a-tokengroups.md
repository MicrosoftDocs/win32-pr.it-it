---
title: Attributo Token-Groups
description: Attributo calcolato che contiene l'elenco di SID a causa di un'operazione di espansione dell'appartenenza a un gruppo transitiva su un determinato utente o computer. Non è possibile recuperare i gruppi di token se non è presente alcun catalogo globale per recuperare le appartenenze inverse transitive.
ms.assetid: bb430c9f-20b7-4f21-804d-fbd4864b6505
ms.tgt_platform: multiple
keywords:
- Schema AD Token-Groups attribute
- Schema AD dell'attributo tokenGroups
topic_type:
- apiref
api_name:
- Token-Groups
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5342d1ff2bf549796340532b0514d5c5b060c2c1
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "106303114"
---
# <a name="token-groups-attribute"></a><span data-ttu-id="27064-106">Attributo Token-Groups</span><span class="sxs-lookup"><span data-stu-id="27064-106">Token-Groups attribute</span></span>

<span data-ttu-id="27064-107">Attributo calcolato che contiene l'elenco di SID a causa di un'operazione di espansione dell'appartenenza a un gruppo transitiva su un determinato utente o computer.</span><span class="sxs-lookup"><span data-stu-id="27064-107">A computed attribute that contains the list of SIDs due to a transitive group membership expansion operation on a given user or computer.</span></span> <span data-ttu-id="27064-108">Non è possibile recuperare i gruppi di token se non è presente alcun catalogo globale per recuperare le appartenenze inverse transitive.</span><span class="sxs-lookup"><span data-stu-id="27064-108">Token Groups cannot be retrieved if no Global Catalog is present to retrieve the transitive reverse memberships.</span></span>



| <span data-ttu-id="27064-109">Voce</span><span class="sxs-lookup"><span data-stu-id="27064-109">Entry</span></span> | <span data-ttu-id="27064-110">Valore</span><span class="sxs-lookup"><span data-stu-id="27064-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="27064-111">CN</span><span class="sxs-lookup"><span data-stu-id="27064-111">CN</span></span>                | <span data-ttu-id="27064-112">Token-Groups</span><span class="sxs-lookup"><span data-stu-id="27064-112">Token-Groups</span></span>                         |
| <span data-ttu-id="27064-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="27064-113">Ldap-Display-Name</span></span> | <span data-ttu-id="27064-114">tokenGroups</span><span class="sxs-lookup"><span data-stu-id="27064-114">tokenGroups</span></span>                          |
| <span data-ttu-id="27064-115">Dimensione</span><span class="sxs-lookup"><span data-stu-id="27064-115">Size</span></span>              | \-                                   |
| <span data-ttu-id="27064-116">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="27064-116">Update Privilege</span></span>  | <span data-ttu-id="27064-117">Questo valore viene impostato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="27064-117">This value is set by the system.</span></span>     |
| <span data-ttu-id="27064-118">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="27064-118">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="27064-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="27064-119">Attribute-Id</span></span>      | <span data-ttu-id="27064-120">1.2.840.113556.1.4.1301</span><span class="sxs-lookup"><span data-stu-id="27064-120">1.2.840.113556.1.4.1301</span></span>              |
| <span data-ttu-id="27064-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="27064-121">System-Id-Guid</span></span>    | <span data-ttu-id="27064-122">b7c69e6d-2cc7-11d2-854e-00a0c983f608</span><span class="sxs-lookup"><span data-stu-id="27064-122">b7c69e6d-2cc7-11d2-854e-00a0c983f608</span></span> |
| <span data-ttu-id="27064-123">Sintassi</span><span class="sxs-lookup"><span data-stu-id="27064-123">Syntax</span></span>            | [<span data-ttu-id="27064-124">**Stringa (SID)**</span><span class="sxs-lookup"><span data-stu-id="27064-124">**String(Sid)**</span></span>](s-string-sid.md)  |



## <a name="implementations"></a><span data-ttu-id="27064-125">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="27064-125">Implementations</span></span>

-   [<span data-ttu-id="27064-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="27064-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="27064-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="27064-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="27064-128">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="27064-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="27064-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="27064-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="27064-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="27064-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="27064-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="27064-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="27064-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="27064-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="27064-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="27064-133">Windows 2000 Server</span></span>



| <span data-ttu-id="27064-134">Voce</span><span class="sxs-lookup"><span data-stu-id="27064-134">Entry</span></span> | <span data-ttu-id="27064-135">Valore</span><span class="sxs-lookup"><span data-stu-id="27064-135">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="27064-136">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="27064-136">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="27064-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="27064-137">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="27064-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="27064-138">System-Only</span></span>            | <span data-ttu-id="27064-139">Falso</span><span class="sxs-lookup"><span data-stu-id="27064-139">False</span></span>                                                        |
| <span data-ttu-id="27064-140">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="27064-140">Is-Single-Valued</span></span>       | <span data-ttu-id="27064-141">Falso</span><span class="sxs-lookup"><span data-stu-id="27064-141">False</span></span>                                                        |
| <span data-ttu-id="27064-142">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="27064-142">Is Indexed</span></span>             | <span data-ttu-id="27064-143">Falso</span><span class="sxs-lookup"><span data-stu-id="27064-143">False</span></span>                                                        |
| <span data-ttu-id="27064-144">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="27064-144">In Global Catalog</span></span>      | <span data-ttu-id="27064-145">Falso</span><span class="sxs-lookup"><span data-stu-id="27064-145">False</span></span>                                                        |
| <span data-ttu-id="27064-146">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="27064-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="27064-147">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="27064-147">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="27064-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="27064-148">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="27064-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="27064-149">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="27064-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="27064-150">Search-Flags</span></span>           | <span data-ttu-id="27064-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="27064-151">0x00000000</span></span>                                                   |
| <span data-ttu-id="27064-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="27064-152">System-Flags</span></span>           | <span data-ttu-id="27064-153">0x08000014</span><span class="sxs-lookup"><span data-stu-id="27064-153">0x08000014</span></span>                                                   |
| <span data-ttu-id="27064-154">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="27064-154">Classes used in</span></span>        | [<span data-ttu-id="27064-155">**Entità di sicurezza**</span><span class="sxs-lookup"><span data-stu-id="27064-155">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="27064-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="27064-156">Windows Server 2003</span></span>



| <span data-ttu-id="27064-157">Voce</span><span class="sxs-lookup"><span data-stu-id="27064-157">Entry</span></span> | <span data-ttu-id="27064-158">Valore</span><span class="sxs-lookup"><span data-stu-id="27064-158">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="27064-159">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="27064-159">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="27064-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="27064-160">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="27064-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="27064-161">System-Only</span></span>            | <span data-ttu-id="27064-162">Falso</span><span class="sxs-lookup"><span data-stu-id="27064-162">False</span></span>                                                        |
| <span data-ttu-id="27064-163">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="27064-163">Is-Single-Valued</span></span>       | <span data-ttu-id="27064-164">Falso</span><span class="sxs-lookup"><span data-stu-id="27064-164">False</span></span>                                                        |
| <span data-ttu-id="27064-165">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="27064-165">Is Indexed</span></span>             | <span data-ttu-id="27064-166">Falso</span><span class="sxs-lookup"><span data-stu-id="27064-166">False</span></span>                                                        |
| <span data-ttu-id="27064-167">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="27064-167">In Global Catalog</span></span>      | <span data-ttu-id="27064-168">Falso</span><span class="sxs-lookup"><span data-stu-id="27064-168">False</span></span>                                                        |
| <span data-ttu-id="27064-169">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="27064-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="27064-170">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="27064-170">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="27064-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="27064-171">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="27064-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="27064-172">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="27064-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="27064-173">Search-Flags</span></span>           | <span data-ttu-id="27064-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="27064-174">0x00000000</span></span>                                                   |
| <span data-ttu-id="27064-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="27064-175">System-Flags</span></span>           | <span data-ttu-id="27064-176">0x08000014</span><span class="sxs-lookup"><span data-stu-id="27064-176">0x08000014</span></span>                                                   |
| <span data-ttu-id="27064-177">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="27064-177">Classes used in</span></span>        | [<span data-ttu-id="27064-178">**Entità di sicurezza**</span><span class="sxs-lookup"><span data-stu-id="27064-178">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="adam"></a><span data-ttu-id="27064-179">ADAM</span><span class="sxs-lookup"><span data-stu-id="27064-179">ADAM</span></span>



| <span data-ttu-id="27064-180">Voce</span><span class="sxs-lookup"><span data-stu-id="27064-180">Entry</span></span> | <span data-ttu-id="27064-181">Valore</span><span class="sxs-lookup"><span data-stu-id="27064-181">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="27064-182">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="27064-182">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="27064-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="27064-183">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="27064-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="27064-184">System-Only</span></span>            | <span data-ttu-id="27064-185">Falso</span><span class="sxs-lookup"><span data-stu-id="27064-185">False</span></span>                                                        |
| <span data-ttu-id="27064-186">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="27064-186">Is-Single-Valued</span></span>       | <span data-ttu-id="27064-187">Falso</span><span class="sxs-lookup"><span data-stu-id="27064-187">False</span></span>                                                        |
| <span data-ttu-id="27064-188">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="27064-188">Is Indexed</span></span>             | <span data-ttu-id="27064-189">Falso</span><span class="sxs-lookup"><span data-stu-id="27064-189">False</span></span>                                                        |
| <span data-ttu-id="27064-190">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="27064-190">In Global Catalog</span></span>      | <span data-ttu-id="27064-191">Falso</span><span class="sxs-lookup"><span data-stu-id="27064-191">False</span></span>                                                        |
| <span data-ttu-id="27064-192">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="27064-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="27064-193">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="27064-193">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="27064-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="27064-194">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="27064-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="27064-195">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="27064-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="27064-196">Search-Flags</span></span>           | <span data-ttu-id="27064-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="27064-197">0x00000000</span></span>                                                   |
| <span data-ttu-id="27064-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="27064-198">System-Flags</span></span>           | <span data-ttu-id="27064-199">0x08000014</span><span class="sxs-lookup"><span data-stu-id="27064-199">0x08000014</span></span>                                                   |
| <span data-ttu-id="27064-200">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="27064-200">Classes used in</span></span>        | [<span data-ttu-id="27064-201">**Entità di sicurezza**</span><span class="sxs-lookup"><span data-stu-id="27064-201">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="27064-202">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="27064-202">Windows Server 2003 R2</span></span>



| <span data-ttu-id="27064-203">Voce</span><span class="sxs-lookup"><span data-stu-id="27064-203">Entry</span></span> | <span data-ttu-id="27064-204">Valore</span><span class="sxs-lookup"><span data-stu-id="27064-204">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="27064-205">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="27064-205">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="27064-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="27064-206">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="27064-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="27064-207">System-Only</span></span>            | <span data-ttu-id="27064-208">Falso</span><span class="sxs-lookup"><span data-stu-id="27064-208">False</span></span>                                                        |
| <span data-ttu-id="27064-209">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="27064-209">Is-Single-Valued</span></span>       | <span data-ttu-id="27064-210">Falso</span><span class="sxs-lookup"><span data-stu-id="27064-210">False</span></span>                                                        |
| <span data-ttu-id="27064-211">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="27064-211">Is Indexed</span></span>             | <span data-ttu-id="27064-212">Falso</span><span class="sxs-lookup"><span data-stu-id="27064-212">False</span></span>                                                        |
| <span data-ttu-id="27064-213">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="27064-213">In Global Catalog</span></span>      | <span data-ttu-id="27064-214">Falso</span><span class="sxs-lookup"><span data-stu-id="27064-214">False</span></span>                                                        |
| <span data-ttu-id="27064-215">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="27064-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="27064-216">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="27064-216">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="27064-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="27064-217">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="27064-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="27064-218">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="27064-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="27064-219">Search-Flags</span></span>           | <span data-ttu-id="27064-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="27064-220">0x00000000</span></span>                                                   |
| <span data-ttu-id="27064-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="27064-221">System-Flags</span></span>           | <span data-ttu-id="27064-222">0x08000014</span><span class="sxs-lookup"><span data-stu-id="27064-222">0x08000014</span></span>                                                   |
| <span data-ttu-id="27064-223">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="27064-223">Classes used in</span></span>        | [<span data-ttu-id="27064-224">**Entità di sicurezza**</span><span class="sxs-lookup"><span data-stu-id="27064-224">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="27064-225">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="27064-225">Windows Server 2008</span></span>



| <span data-ttu-id="27064-226">Voce</span><span class="sxs-lookup"><span data-stu-id="27064-226">Entry</span></span> | <span data-ttu-id="27064-227">Valore</span><span class="sxs-lookup"><span data-stu-id="27064-227">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="27064-228">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="27064-228">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="27064-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="27064-229">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="27064-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="27064-230">System-Only</span></span>            | <span data-ttu-id="27064-231">Falso</span><span class="sxs-lookup"><span data-stu-id="27064-231">False</span></span>                                                        |
| <span data-ttu-id="27064-232">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="27064-232">Is-Single-Valued</span></span>       | <span data-ttu-id="27064-233">Falso</span><span class="sxs-lookup"><span data-stu-id="27064-233">False</span></span>                                                        |
| <span data-ttu-id="27064-234">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="27064-234">Is Indexed</span></span>             | <span data-ttu-id="27064-235">Falso</span><span class="sxs-lookup"><span data-stu-id="27064-235">False</span></span>                                                        |
| <span data-ttu-id="27064-236">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="27064-236">In Global Catalog</span></span>      | <span data-ttu-id="27064-237">Falso</span><span class="sxs-lookup"><span data-stu-id="27064-237">False</span></span>                                                        |
| <span data-ttu-id="27064-238">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="27064-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="27064-239">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="27064-239">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="27064-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="27064-240">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="27064-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="27064-241">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="27064-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="27064-242">Search-Flags</span></span>           | <span data-ttu-id="27064-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="27064-243">0x00000000</span></span>                                                   |
| <span data-ttu-id="27064-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="27064-244">System-Flags</span></span>           | <span data-ttu-id="27064-245">0x08000014</span><span class="sxs-lookup"><span data-stu-id="27064-245">0x08000014</span></span>                                                   |
| <span data-ttu-id="27064-246">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="27064-246">Classes used in</span></span>        | [<span data-ttu-id="27064-247">**Entità di sicurezza**</span><span class="sxs-lookup"><span data-stu-id="27064-247">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="27064-248">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="27064-248">Windows Server 2008 R2</span></span>



| <span data-ttu-id="27064-249">Voce</span><span class="sxs-lookup"><span data-stu-id="27064-249">Entry</span></span> | <span data-ttu-id="27064-250">Valore</span><span class="sxs-lookup"><span data-stu-id="27064-250">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="27064-251">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="27064-251">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="27064-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="27064-252">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="27064-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="27064-253">System-Only</span></span>            | <span data-ttu-id="27064-254">Falso</span><span class="sxs-lookup"><span data-stu-id="27064-254">False</span></span>                                                        |
| <span data-ttu-id="27064-255">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="27064-255">Is-Single-Valued</span></span>       | <span data-ttu-id="27064-256">Falso</span><span class="sxs-lookup"><span data-stu-id="27064-256">False</span></span>                                                        |
| <span data-ttu-id="27064-257">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="27064-257">Is Indexed</span></span>             | <span data-ttu-id="27064-258">Falso</span><span class="sxs-lookup"><span data-stu-id="27064-258">False</span></span>                                                        |
| <span data-ttu-id="27064-259">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="27064-259">In Global Catalog</span></span>      | <span data-ttu-id="27064-260">Falso</span><span class="sxs-lookup"><span data-stu-id="27064-260">False</span></span>                                                        |
| <span data-ttu-id="27064-261">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="27064-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="27064-262">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="27064-262">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="27064-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="27064-263">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="27064-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="27064-264">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="27064-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="27064-265">Search-Flags</span></span>           | <span data-ttu-id="27064-266">0x00000000</span><span class="sxs-lookup"><span data-stu-id="27064-266">0x00000000</span></span>                                                   |
| <span data-ttu-id="27064-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="27064-267">System-Flags</span></span>           | <span data-ttu-id="27064-268">0x08000014</span><span class="sxs-lookup"><span data-stu-id="27064-268">0x08000014</span></span>                                                   |
| <span data-ttu-id="27064-269">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="27064-269">Classes used in</span></span>        | [<span data-ttu-id="27064-270">**Entità di sicurezza**</span><span class="sxs-lookup"><span data-stu-id="27064-270">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="27064-271">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="27064-271">Windows Server 2012</span></span>



| <span data-ttu-id="27064-272">Voce</span><span class="sxs-lookup"><span data-stu-id="27064-272">Entry</span></span> | <span data-ttu-id="27064-273">Valore</span><span class="sxs-lookup"><span data-stu-id="27064-273">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="27064-274">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="27064-274">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="27064-275">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="27064-275">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="27064-276">System-Only</span><span class="sxs-lookup"><span data-stu-id="27064-276">System-Only</span></span>            | <span data-ttu-id="27064-277">Falso</span><span class="sxs-lookup"><span data-stu-id="27064-277">False</span></span>                                                        |
| <span data-ttu-id="27064-278">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="27064-278">Is-Single-Valued</span></span>       | <span data-ttu-id="27064-279">Falso</span><span class="sxs-lookup"><span data-stu-id="27064-279">False</span></span>                                                        |
| <span data-ttu-id="27064-280">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="27064-280">Is Indexed</span></span>             | <span data-ttu-id="27064-281">Falso</span><span class="sxs-lookup"><span data-stu-id="27064-281">False</span></span>                                                        |
| <span data-ttu-id="27064-282">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="27064-282">In Global Catalog</span></span>      | <span data-ttu-id="27064-283">Falso</span><span class="sxs-lookup"><span data-stu-id="27064-283">False</span></span>                                                        |
| <span data-ttu-id="27064-284">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="27064-284">NT-Security-Descriptor</span></span> | <span data-ttu-id="27064-285">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="27064-285">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="27064-286">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="27064-286">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="27064-287">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="27064-287">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="27064-288">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="27064-288">Search-Flags</span></span>           | <span data-ttu-id="27064-289">0x00000000</span><span class="sxs-lookup"><span data-stu-id="27064-289">0x00000000</span></span>                                                   |
| <span data-ttu-id="27064-290">System-Flags</span><span class="sxs-lookup"><span data-stu-id="27064-290">System-Flags</span></span>           | <span data-ttu-id="27064-291">0x08000014</span><span class="sxs-lookup"><span data-stu-id="27064-291">0x08000014</span></span>                                                   |
| <span data-ttu-id="27064-292">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="27064-292">Classes used in</span></span>        | [<span data-ttu-id="27064-293">**Entità di sicurezza**</span><span class="sxs-lookup"><span data-stu-id="27064-293">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



 

 





