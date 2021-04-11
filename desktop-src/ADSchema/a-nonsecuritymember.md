---
title: Attributo non di sicurezza-membro
description: Membri non di sicurezza di un gruppo. Utilizzato per gli elenchi di distribuzione di Exchange.
ms.assetid: 0db135e4-dcba-4afb-a174-3c7b2b40688e
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo non di sicurezza-membro
- Schema AD dell'attributo nonSecurityMember
topic_type:
- apiref
api_name:
- Non-Security-Member
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a04919d9d538ff4da97d73e79d14e9a2706032b8
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103965353"
---
# <a name="non-security-member-attribute"></a><span data-ttu-id="e8169-106">Attributo non di sicurezza-membro</span><span class="sxs-lookup"><span data-stu-id="e8169-106">Non-Security-Member attribute</span></span>

<span data-ttu-id="e8169-107">Membri non di sicurezza di un gruppo.</span><span class="sxs-lookup"><span data-stu-id="e8169-107">Nonsecurity members of a group.</span></span> <span data-ttu-id="e8169-108">Utilizzato per gli elenchi di distribuzione di Exchange.</span><span class="sxs-lookup"><span data-stu-id="e8169-108">Used for Exchange distribution lists.</span></span>



| <span data-ttu-id="e8169-109">Voce</span><span class="sxs-lookup"><span data-stu-id="e8169-109">Entry</span></span> | <span data-ttu-id="e8169-110">Valore</span><span class="sxs-lookup"><span data-stu-id="e8169-110">Value</span></span> |
|-------------------|--------------------------------------------------|
| <span data-ttu-id="e8169-111">CN</span><span class="sxs-lookup"><span data-stu-id="e8169-111">CN</span></span>                | <span data-ttu-id="e8169-112">Membro non di sicurezza</span><span class="sxs-lookup"><span data-stu-id="e8169-112">Non-Security-Member</span></span>                              |
| <span data-ttu-id="e8169-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="e8169-113">Ldap-Display-Name</span></span> | <span data-ttu-id="e8169-114">nonSecurityMember</span><span class="sxs-lookup"><span data-stu-id="e8169-114">nonSecurityMember</span></span>                                |
| <span data-ttu-id="e8169-115">Dimensione</span><span class="sxs-lookup"><span data-stu-id="e8169-115">Size</span></span>              | \-                                               |
| <span data-ttu-id="e8169-116">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="e8169-116">Update Privilege</span></span>  | <span data-ttu-id="e8169-117">Amministratore di dominio</span><span class="sxs-lookup"><span data-stu-id="e8169-117">Domain administrator</span></span>                             |
| <span data-ttu-id="e8169-118">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="e8169-118">Update Frequency</span></span>  | <span data-ttu-id="e8169-119">Ogni volta che un utente viene aggiunto o rimosso dal DL.</span><span class="sxs-lookup"><span data-stu-id="e8169-119">Whenever a user is added or removed from the DL.</span></span> |
| <span data-ttu-id="e8169-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e8169-120">Attribute-Id</span></span>      | <span data-ttu-id="e8169-121">1.2.840.113556.1.4.530</span><span class="sxs-lookup"><span data-stu-id="e8169-121">1.2.840.113556.1.4.530</span></span>                           |
| <span data-ttu-id="e8169-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="e8169-122">System-Id-Guid</span></span>    | <span data-ttu-id="e8169-123">52458018-ca6a-11D0-AFFF-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="e8169-123">52458018-ca6a-11d0-afff-0000f80367c1</span></span>             |
| <span data-ttu-id="e8169-124">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e8169-124">Syntax</span></span>            | [<span data-ttu-id="e8169-125">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="e8169-125">**Object(DS-DN)**</span></span>](s-object-ds-dn.md)          |



## <a name="implementations"></a><span data-ttu-id="e8169-126">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="e8169-126">Implementations</span></span>

-   [<span data-ttu-id="e8169-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="e8169-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="e8169-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e8169-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e8169-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e8169-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e8169-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e8169-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e8169-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e8169-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e8169-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e8169-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="e8169-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e8169-133">Windows 2000 Server</span></span>



| <span data-ttu-id="e8169-134">Voce</span><span class="sxs-lookup"><span data-stu-id="e8169-134">Entry</span></span> | <span data-ttu-id="e8169-135">Valore</span><span class="sxs-lookup"><span data-stu-id="e8169-135">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="e8169-136">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="e8169-136">Link-Id</span></span>                | <span data-ttu-id="e8169-137">50</span><span class="sxs-lookup"><span data-stu-id="e8169-137">50</span></span>                                  |
| <span data-ttu-id="e8169-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e8169-138">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="e8169-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="e8169-139">System-Only</span></span>            | <span data-ttu-id="e8169-140">Falso</span><span class="sxs-lookup"><span data-stu-id="e8169-140">False</span></span>                               |
| <span data-ttu-id="e8169-141">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="e8169-141">Is-Single-Valued</span></span>       | <span data-ttu-id="e8169-142">Falso</span><span class="sxs-lookup"><span data-stu-id="e8169-142">False</span></span>                               |
| <span data-ttu-id="e8169-143">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="e8169-143">Is Indexed</span></span>             | <span data-ttu-id="e8169-144">Falso</span><span class="sxs-lookup"><span data-stu-id="e8169-144">False</span></span>                               |
| <span data-ttu-id="e8169-145">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="e8169-145">In Global Catalog</span></span>      | <span data-ttu-id="e8169-146">Falso</span><span class="sxs-lookup"><span data-stu-id="e8169-146">False</span></span>                               |
| <span data-ttu-id="e8169-147">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="e8169-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="e8169-148">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="e8169-148">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="e8169-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e8169-149">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="e8169-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e8169-150">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="e8169-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e8169-151">Search-Flags</span></span>           | <span data-ttu-id="e8169-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e8169-152">0x00000000</span></span>                          |
| <span data-ttu-id="e8169-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e8169-153">System-Flags</span></span>           | <span data-ttu-id="e8169-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e8169-154">0x00000010</span></span>                          |
| <span data-ttu-id="e8169-155">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="e8169-155">Classes used in</span></span>        | [<span data-ttu-id="e8169-156">**Group**</span><span class="sxs-lookup"><span data-stu-id="e8169-156">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="e8169-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e8169-157">Windows Server 2003</span></span>



| <span data-ttu-id="e8169-158">Voce</span><span class="sxs-lookup"><span data-stu-id="e8169-158">Entry</span></span> | <span data-ttu-id="e8169-159">Valore</span><span class="sxs-lookup"><span data-stu-id="e8169-159">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="e8169-160">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="e8169-160">Link-Id</span></span>                | <span data-ttu-id="e8169-161">50</span><span class="sxs-lookup"><span data-stu-id="e8169-161">50</span></span>                                  |
| <span data-ttu-id="e8169-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e8169-162">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="e8169-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="e8169-163">System-Only</span></span>            | <span data-ttu-id="e8169-164">Falso</span><span class="sxs-lookup"><span data-stu-id="e8169-164">False</span></span>                               |
| <span data-ttu-id="e8169-165">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="e8169-165">Is-Single-Valued</span></span>       | <span data-ttu-id="e8169-166">Falso</span><span class="sxs-lookup"><span data-stu-id="e8169-166">False</span></span>                               |
| <span data-ttu-id="e8169-167">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="e8169-167">Is Indexed</span></span>             | <span data-ttu-id="e8169-168">Falso</span><span class="sxs-lookup"><span data-stu-id="e8169-168">False</span></span>                               |
| <span data-ttu-id="e8169-169">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="e8169-169">In Global Catalog</span></span>      | <span data-ttu-id="e8169-170">Falso</span><span class="sxs-lookup"><span data-stu-id="e8169-170">False</span></span>                               |
| <span data-ttu-id="e8169-171">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="e8169-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="e8169-172">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="e8169-172">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="e8169-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e8169-173">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="e8169-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e8169-174">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="e8169-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e8169-175">Search-Flags</span></span>           | <span data-ttu-id="e8169-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e8169-176">0x00000000</span></span>                          |
| <span data-ttu-id="e8169-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e8169-177">System-Flags</span></span>           | <span data-ttu-id="e8169-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e8169-178">0x00000010</span></span>                          |
| <span data-ttu-id="e8169-179">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="e8169-179">Classes used in</span></span>        | [<span data-ttu-id="e8169-180">**Group**</span><span class="sxs-lookup"><span data-stu-id="e8169-180">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e8169-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e8169-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e8169-182">Voce</span><span class="sxs-lookup"><span data-stu-id="e8169-182">Entry</span></span> | <span data-ttu-id="e8169-183">Valore</span><span class="sxs-lookup"><span data-stu-id="e8169-183">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="e8169-184">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="e8169-184">Link-Id</span></span>                | <span data-ttu-id="e8169-185">50</span><span class="sxs-lookup"><span data-stu-id="e8169-185">50</span></span>                                  |
| <span data-ttu-id="e8169-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e8169-186">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="e8169-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="e8169-187">System-Only</span></span>            | <span data-ttu-id="e8169-188">Falso</span><span class="sxs-lookup"><span data-stu-id="e8169-188">False</span></span>                               |
| <span data-ttu-id="e8169-189">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="e8169-189">Is-Single-Valued</span></span>       | <span data-ttu-id="e8169-190">Falso</span><span class="sxs-lookup"><span data-stu-id="e8169-190">False</span></span>                               |
| <span data-ttu-id="e8169-191">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="e8169-191">Is Indexed</span></span>             | <span data-ttu-id="e8169-192">Falso</span><span class="sxs-lookup"><span data-stu-id="e8169-192">False</span></span>                               |
| <span data-ttu-id="e8169-193">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="e8169-193">In Global Catalog</span></span>      | <span data-ttu-id="e8169-194">Falso</span><span class="sxs-lookup"><span data-stu-id="e8169-194">False</span></span>                               |
| <span data-ttu-id="e8169-195">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="e8169-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="e8169-196">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="e8169-196">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="e8169-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e8169-197">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="e8169-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e8169-198">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="e8169-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e8169-199">Search-Flags</span></span>           | <span data-ttu-id="e8169-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e8169-200">0x00000000</span></span>                          |
| <span data-ttu-id="e8169-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e8169-201">System-Flags</span></span>           | <span data-ttu-id="e8169-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e8169-202">0x00000010</span></span>                          |
| <span data-ttu-id="e8169-203">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="e8169-203">Classes used in</span></span>        | [<span data-ttu-id="e8169-204">**Group**</span><span class="sxs-lookup"><span data-stu-id="e8169-204">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="e8169-205">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e8169-205">Windows Server 2008</span></span>



| <span data-ttu-id="e8169-206">Voce</span><span class="sxs-lookup"><span data-stu-id="e8169-206">Entry</span></span> | <span data-ttu-id="e8169-207">Valore</span><span class="sxs-lookup"><span data-stu-id="e8169-207">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="e8169-208">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="e8169-208">Link-Id</span></span>                | <span data-ttu-id="e8169-209">50</span><span class="sxs-lookup"><span data-stu-id="e8169-209">50</span></span>                                  |
| <span data-ttu-id="e8169-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e8169-210">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="e8169-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="e8169-211">System-Only</span></span>            | <span data-ttu-id="e8169-212">Falso</span><span class="sxs-lookup"><span data-stu-id="e8169-212">False</span></span>                               |
| <span data-ttu-id="e8169-213">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="e8169-213">Is-Single-Valued</span></span>       | <span data-ttu-id="e8169-214">Falso</span><span class="sxs-lookup"><span data-stu-id="e8169-214">False</span></span>                               |
| <span data-ttu-id="e8169-215">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="e8169-215">Is Indexed</span></span>             | <span data-ttu-id="e8169-216">Falso</span><span class="sxs-lookup"><span data-stu-id="e8169-216">False</span></span>                               |
| <span data-ttu-id="e8169-217">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="e8169-217">In Global Catalog</span></span>      | <span data-ttu-id="e8169-218">Falso</span><span class="sxs-lookup"><span data-stu-id="e8169-218">False</span></span>                               |
| <span data-ttu-id="e8169-219">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="e8169-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="e8169-220">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="e8169-220">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="e8169-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e8169-221">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="e8169-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e8169-222">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="e8169-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e8169-223">Search-Flags</span></span>           | <span data-ttu-id="e8169-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e8169-224">0x00000000</span></span>                          |
| <span data-ttu-id="e8169-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e8169-225">System-Flags</span></span>           | <span data-ttu-id="e8169-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e8169-226">0x00000010</span></span>                          |
| <span data-ttu-id="e8169-227">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="e8169-227">Classes used in</span></span>        | [<span data-ttu-id="e8169-228">**Group**</span><span class="sxs-lookup"><span data-stu-id="e8169-228">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e8169-229">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e8169-229">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e8169-230">Voce</span><span class="sxs-lookup"><span data-stu-id="e8169-230">Entry</span></span> | <span data-ttu-id="e8169-231">Valore</span><span class="sxs-lookup"><span data-stu-id="e8169-231">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="e8169-232">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="e8169-232">Link-Id</span></span>                | <span data-ttu-id="e8169-233">50</span><span class="sxs-lookup"><span data-stu-id="e8169-233">50</span></span>                                  |
| <span data-ttu-id="e8169-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e8169-234">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="e8169-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="e8169-235">System-Only</span></span>            | <span data-ttu-id="e8169-236">Falso</span><span class="sxs-lookup"><span data-stu-id="e8169-236">False</span></span>                               |
| <span data-ttu-id="e8169-237">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="e8169-237">Is-Single-Valued</span></span>       | <span data-ttu-id="e8169-238">Falso</span><span class="sxs-lookup"><span data-stu-id="e8169-238">False</span></span>                               |
| <span data-ttu-id="e8169-239">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="e8169-239">Is Indexed</span></span>             | <span data-ttu-id="e8169-240">Falso</span><span class="sxs-lookup"><span data-stu-id="e8169-240">False</span></span>                               |
| <span data-ttu-id="e8169-241">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="e8169-241">In Global Catalog</span></span>      | <span data-ttu-id="e8169-242">Falso</span><span class="sxs-lookup"><span data-stu-id="e8169-242">False</span></span>                               |
| <span data-ttu-id="e8169-243">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="e8169-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="e8169-244">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="e8169-244">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="e8169-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e8169-245">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="e8169-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e8169-246">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="e8169-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e8169-247">Search-Flags</span></span>           | <span data-ttu-id="e8169-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e8169-248">0x00000000</span></span>                          |
| <span data-ttu-id="e8169-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e8169-249">System-Flags</span></span>           | <span data-ttu-id="e8169-250">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e8169-250">0x00000010</span></span>                          |
| <span data-ttu-id="e8169-251">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="e8169-251">Classes used in</span></span>        | [<span data-ttu-id="e8169-252">**Group**</span><span class="sxs-lookup"><span data-stu-id="e8169-252">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e8169-253">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e8169-253">Windows Server 2012</span></span>



| <span data-ttu-id="e8169-254">Voce</span><span class="sxs-lookup"><span data-stu-id="e8169-254">Entry</span></span> | <span data-ttu-id="e8169-255">Valore</span><span class="sxs-lookup"><span data-stu-id="e8169-255">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="e8169-256">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="e8169-256">Link-Id</span></span>                | <span data-ttu-id="e8169-257">50</span><span class="sxs-lookup"><span data-stu-id="e8169-257">50</span></span>                                  |
| <span data-ttu-id="e8169-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e8169-258">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="e8169-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="e8169-259">System-Only</span></span>            | <span data-ttu-id="e8169-260">Falso</span><span class="sxs-lookup"><span data-stu-id="e8169-260">False</span></span>                               |
| <span data-ttu-id="e8169-261">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="e8169-261">Is-Single-Valued</span></span>       | <span data-ttu-id="e8169-262">Falso</span><span class="sxs-lookup"><span data-stu-id="e8169-262">False</span></span>                               |
| <span data-ttu-id="e8169-263">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="e8169-263">Is Indexed</span></span>             | <span data-ttu-id="e8169-264">Falso</span><span class="sxs-lookup"><span data-stu-id="e8169-264">False</span></span>                               |
| <span data-ttu-id="e8169-265">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="e8169-265">In Global Catalog</span></span>      | <span data-ttu-id="e8169-266">Falso</span><span class="sxs-lookup"><span data-stu-id="e8169-266">False</span></span>                               |
| <span data-ttu-id="e8169-267">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="e8169-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="e8169-268">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="e8169-268">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="e8169-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e8169-269">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="e8169-270">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e8169-270">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="e8169-271">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e8169-271">Search-Flags</span></span>           | <span data-ttu-id="e8169-272">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e8169-272">0x00000000</span></span>                          |
| <span data-ttu-id="e8169-273">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e8169-273">System-Flags</span></span>           | <span data-ttu-id="e8169-274">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e8169-274">0x00000010</span></span>                          |
| <span data-ttu-id="e8169-275">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="e8169-275">Classes used in</span></span>        | [<span data-ttu-id="e8169-276">**Group**</span><span class="sxs-lookup"><span data-stu-id="e8169-276">**Group**</span></span>](c-group.md)<br/> |



 

 





