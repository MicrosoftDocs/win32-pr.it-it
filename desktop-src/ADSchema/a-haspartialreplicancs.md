---
title: Con attributo-partial-replica-NCs
description: Di pari livello a ha-Master-NCs. Has-partial-replica-NCs riflette il nome distinto per tutti gli altri domini di dominio che sono stati replicati in un catalogo globale.
ms.assetid: 2501bbb3-74b5-4604-b0c0-8653fc092e1c
ms.tgt_platform: multiple
keywords:
- Con lo schema AD dell'attributo-partial-replica-NCs
- Schema AD dell'attributo hasPartialReplicaNCs
topic_type:
- apiref
api_name:
- Has-Partial-Replica-NCs
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f284df094c909b01b88a4853ed7c4a41dee9f31a
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744218"
---
# <a name="has-partial-replica-ncs-attribute"></a><span data-ttu-id="f9a71-106">Con attributo-partial-replica-NCs</span><span class="sxs-lookup"><span data-stu-id="f9a71-106">Has-Partial-Replica-NCs attribute</span></span>

<span data-ttu-id="f9a71-107">Di pari livello a ha-Master-NCs.</span><span class="sxs-lookup"><span data-stu-id="f9a71-107">Sibling to Has-Master-NCs.</span></span> <span data-ttu-id="f9a71-108">Has-partial-replica-NCs riflette il nome distinto per tutti gli altri domini di dominio che sono stati replicati in un catalogo globale.</span><span class="sxs-lookup"><span data-stu-id="f9a71-108">Has-Partial-Replica-NCs reflects the distinguished name for all other-domain NCs that have been replicated into a global catalog.</span></span>



| <span data-ttu-id="f9a71-109">Voce</span><span class="sxs-lookup"><span data-stu-id="f9a71-109">Entry</span></span> | <span data-ttu-id="f9a71-110">Valore</span><span class="sxs-lookup"><span data-stu-id="f9a71-110">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="f9a71-111">CN</span><span class="sxs-lookup"><span data-stu-id="f9a71-111">CN</span></span>                | <span data-ttu-id="f9a71-112">Has-partial-replica-NCs</span><span class="sxs-lookup"><span data-stu-id="f9a71-112">Has-Partial-Replica-NCs</span></span>                 |
| <span data-ttu-id="f9a71-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="f9a71-113">Ldap-Display-Name</span></span> | <span data-ttu-id="f9a71-114">hasPartialReplicaNCs</span><span class="sxs-lookup"><span data-stu-id="f9a71-114">hasPartialReplicaNCs</span></span>                    |
| <span data-ttu-id="f9a71-115">Dimensione</span><span class="sxs-lookup"><span data-stu-id="f9a71-115">Size</span></span>              | \-                                      |
| <span data-ttu-id="f9a71-116">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="f9a71-116">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="f9a71-117">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="f9a71-117">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="f9a71-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f9a71-118">Attribute-Id</span></span>      | <span data-ttu-id="f9a71-119">1.2.840.113556.1.2.15</span><span class="sxs-lookup"><span data-stu-id="f9a71-119">1.2.840.113556.1.2.15</span></span>                   |
| <span data-ttu-id="f9a71-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="f9a71-120">System-Id-Guid</span></span>    | <span data-ttu-id="f9a71-121">bf967981-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="f9a71-121">bf967981-0de6-11d0-a285-00aa003049e2</span></span>    |
| <span data-ttu-id="f9a71-122">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f9a71-122">Syntax</span></span>            | [<span data-ttu-id="f9a71-123">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="f9a71-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="f9a71-124">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="f9a71-124">Implementations</span></span>

-   [<span data-ttu-id="f9a71-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="f9a71-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="f9a71-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f9a71-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f9a71-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="f9a71-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="f9a71-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f9a71-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f9a71-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f9a71-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f9a71-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f9a71-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f9a71-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f9a71-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="f9a71-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f9a71-132">Windows 2000 Server</span></span>



| <span data-ttu-id="f9a71-133">Voce</span><span class="sxs-lookup"><span data-stu-id="f9a71-133">Entry</span></span> | <span data-ttu-id="f9a71-134">Valore</span><span class="sxs-lookup"><span data-stu-id="f9a71-134">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="f9a71-135">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="f9a71-135">Link-Id</span></span>                | <span data-ttu-id="f9a71-136">74</span><span class="sxs-lookup"><span data-stu-id="f9a71-136">74</span></span>                                       |
| <span data-ttu-id="f9a71-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f9a71-137">MAPI-Id</span></span>                | <span data-ttu-id="f9a71-138">0x80B5</span><span class="sxs-lookup"><span data-stu-id="f9a71-138">0x80B5</span></span>                                   |
| <span data-ttu-id="f9a71-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="f9a71-139">System-Only</span></span>            | <span data-ttu-id="f9a71-140">Vero</span><span class="sxs-lookup"><span data-stu-id="f9a71-140">True</span></span>                                     |
| <span data-ttu-id="f9a71-141">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="f9a71-141">Is-Single-Valued</span></span>       | <span data-ttu-id="f9a71-142">Falso</span><span class="sxs-lookup"><span data-stu-id="f9a71-142">False</span></span>                                    |
| <span data-ttu-id="f9a71-143">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="f9a71-143">Is Indexed</span></span>             | <span data-ttu-id="f9a71-144">Falso</span><span class="sxs-lookup"><span data-stu-id="f9a71-144">False</span></span>                                    |
| <span data-ttu-id="f9a71-145">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="f9a71-145">In Global Catalog</span></span>      | <span data-ttu-id="f9a71-146">Falso</span><span class="sxs-lookup"><span data-stu-id="f9a71-146">False</span></span>                                    |
| <span data-ttu-id="f9a71-147">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="f9a71-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="f9a71-148">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="f9a71-148">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="f9a71-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f9a71-149">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="f9a71-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f9a71-150">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="f9a71-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f9a71-151">Search-Flags</span></span>           | <span data-ttu-id="f9a71-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f9a71-152">0x00000000</span></span>                               |
| <span data-ttu-id="f9a71-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f9a71-153">System-Flags</span></span>           | <span data-ttu-id="f9a71-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f9a71-154">0x00000010</span></span>                               |
| <span data-ttu-id="f9a71-155">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="f9a71-155">Classes used in</span></span>        | [<span data-ttu-id="f9a71-156">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="f9a71-156">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="f9a71-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f9a71-157">Windows Server 2003</span></span>



| <span data-ttu-id="f9a71-158">Voce</span><span class="sxs-lookup"><span data-stu-id="f9a71-158">Entry</span></span> | <span data-ttu-id="f9a71-159">Valore</span><span class="sxs-lookup"><span data-stu-id="f9a71-159">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="f9a71-160">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="f9a71-160">Link-Id</span></span>                | <span data-ttu-id="f9a71-161">74</span><span class="sxs-lookup"><span data-stu-id="f9a71-161">74</span></span>                                       |
| <span data-ttu-id="f9a71-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f9a71-162">MAPI-Id</span></span>                | <span data-ttu-id="f9a71-163">0x80B5</span><span class="sxs-lookup"><span data-stu-id="f9a71-163">0x80B5</span></span>                                   |
| <span data-ttu-id="f9a71-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="f9a71-164">System-Only</span></span>            | <span data-ttu-id="f9a71-165">Vero</span><span class="sxs-lookup"><span data-stu-id="f9a71-165">True</span></span>                                     |
| <span data-ttu-id="f9a71-166">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="f9a71-166">Is-Single-Valued</span></span>       | <span data-ttu-id="f9a71-167">Falso</span><span class="sxs-lookup"><span data-stu-id="f9a71-167">False</span></span>                                    |
| <span data-ttu-id="f9a71-168">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="f9a71-168">Is Indexed</span></span>             | <span data-ttu-id="f9a71-169">Falso</span><span class="sxs-lookup"><span data-stu-id="f9a71-169">False</span></span>                                    |
| <span data-ttu-id="f9a71-170">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="f9a71-170">In Global Catalog</span></span>      | <span data-ttu-id="f9a71-171">Falso</span><span class="sxs-lookup"><span data-stu-id="f9a71-171">False</span></span>                                    |
| <span data-ttu-id="f9a71-172">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="f9a71-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="f9a71-173">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="f9a71-173">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="f9a71-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f9a71-174">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="f9a71-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f9a71-175">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="f9a71-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f9a71-176">Search-Flags</span></span>           | <span data-ttu-id="f9a71-177">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f9a71-177">0x00000000</span></span>                               |
| <span data-ttu-id="f9a71-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f9a71-178">System-Flags</span></span>           | <span data-ttu-id="f9a71-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f9a71-179">0x00000010</span></span>                               |
| <span data-ttu-id="f9a71-180">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="f9a71-180">Classes used in</span></span>        | [<span data-ttu-id="f9a71-181">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="f9a71-181">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="adam"></a><span data-ttu-id="f9a71-182">ADAM</span><span class="sxs-lookup"><span data-stu-id="f9a71-182">ADAM</span></span>



| <span data-ttu-id="f9a71-183">Voce</span><span class="sxs-lookup"><span data-stu-id="f9a71-183">Entry</span></span> | <span data-ttu-id="f9a71-184">Valore</span><span class="sxs-lookup"><span data-stu-id="f9a71-184">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="f9a71-185">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="f9a71-185">Link-Id</span></span>                | <span data-ttu-id="f9a71-186">74</span><span class="sxs-lookup"><span data-stu-id="f9a71-186">74</span></span>                                       |
| <span data-ttu-id="f9a71-187">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f9a71-187">MAPI-Id</span></span>                | <span data-ttu-id="f9a71-188">0x80B5</span><span class="sxs-lookup"><span data-stu-id="f9a71-188">0x80B5</span></span>                                   |
| <span data-ttu-id="f9a71-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="f9a71-189">System-Only</span></span>            | <span data-ttu-id="f9a71-190">Vero</span><span class="sxs-lookup"><span data-stu-id="f9a71-190">True</span></span>                                     |
| <span data-ttu-id="f9a71-191">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="f9a71-191">Is-Single-Valued</span></span>       | <span data-ttu-id="f9a71-192">Falso</span><span class="sxs-lookup"><span data-stu-id="f9a71-192">False</span></span>                                    |
| <span data-ttu-id="f9a71-193">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="f9a71-193">Is Indexed</span></span>             | <span data-ttu-id="f9a71-194">Falso</span><span class="sxs-lookup"><span data-stu-id="f9a71-194">False</span></span>                                    |
| <span data-ttu-id="f9a71-195">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="f9a71-195">In Global Catalog</span></span>      | <span data-ttu-id="f9a71-196">Falso</span><span class="sxs-lookup"><span data-stu-id="f9a71-196">False</span></span>                                    |
| <span data-ttu-id="f9a71-197">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="f9a71-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="f9a71-198">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="f9a71-198">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="f9a71-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f9a71-199">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="f9a71-200">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f9a71-200">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="f9a71-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f9a71-201">Search-Flags</span></span>           | <span data-ttu-id="f9a71-202">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f9a71-202">0x00000000</span></span>                               |
| <span data-ttu-id="f9a71-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f9a71-203">System-Flags</span></span>           | <span data-ttu-id="f9a71-204">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f9a71-204">0x00000010</span></span>                               |
| <span data-ttu-id="f9a71-205">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="f9a71-205">Classes used in</span></span>        | [<span data-ttu-id="f9a71-206">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="f9a71-206">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f9a71-207">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f9a71-207">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f9a71-208">Voce</span><span class="sxs-lookup"><span data-stu-id="f9a71-208">Entry</span></span> | <span data-ttu-id="f9a71-209">Valore</span><span class="sxs-lookup"><span data-stu-id="f9a71-209">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="f9a71-210">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="f9a71-210">Link-Id</span></span>                | <span data-ttu-id="f9a71-211">74</span><span class="sxs-lookup"><span data-stu-id="f9a71-211">74</span></span>                                       |
| <span data-ttu-id="f9a71-212">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f9a71-212">MAPI-Id</span></span>                | <span data-ttu-id="f9a71-213">0x80B5</span><span class="sxs-lookup"><span data-stu-id="f9a71-213">0x80B5</span></span>                                   |
| <span data-ttu-id="f9a71-214">System-Only</span><span class="sxs-lookup"><span data-stu-id="f9a71-214">System-Only</span></span>            | <span data-ttu-id="f9a71-215">Vero</span><span class="sxs-lookup"><span data-stu-id="f9a71-215">True</span></span>                                     |
| <span data-ttu-id="f9a71-216">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="f9a71-216">Is-Single-Valued</span></span>       | <span data-ttu-id="f9a71-217">Falso</span><span class="sxs-lookup"><span data-stu-id="f9a71-217">False</span></span>                                    |
| <span data-ttu-id="f9a71-218">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="f9a71-218">Is Indexed</span></span>             | <span data-ttu-id="f9a71-219">Falso</span><span class="sxs-lookup"><span data-stu-id="f9a71-219">False</span></span>                                    |
| <span data-ttu-id="f9a71-220">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="f9a71-220">In Global Catalog</span></span>      | <span data-ttu-id="f9a71-221">Falso</span><span class="sxs-lookup"><span data-stu-id="f9a71-221">False</span></span>                                    |
| <span data-ttu-id="f9a71-222">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="f9a71-222">NT-Security-Descriptor</span></span> | <span data-ttu-id="f9a71-223">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="f9a71-223">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="f9a71-224">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f9a71-224">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="f9a71-225">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f9a71-225">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="f9a71-226">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f9a71-226">Search-Flags</span></span>           | <span data-ttu-id="f9a71-227">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f9a71-227">0x00000000</span></span>                               |
| <span data-ttu-id="f9a71-228">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f9a71-228">System-Flags</span></span>           | <span data-ttu-id="f9a71-229">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f9a71-229">0x00000010</span></span>                               |
| <span data-ttu-id="f9a71-230">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="f9a71-230">Classes used in</span></span>        | [<span data-ttu-id="f9a71-231">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="f9a71-231">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f9a71-232">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f9a71-232">Windows Server 2008</span></span>



| <span data-ttu-id="f9a71-233">Voce</span><span class="sxs-lookup"><span data-stu-id="f9a71-233">Entry</span></span> | <span data-ttu-id="f9a71-234">Valore</span><span class="sxs-lookup"><span data-stu-id="f9a71-234">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="f9a71-235">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="f9a71-235">Link-Id</span></span>                | <span data-ttu-id="f9a71-236">74</span><span class="sxs-lookup"><span data-stu-id="f9a71-236">74</span></span>                                       |
| <span data-ttu-id="f9a71-237">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f9a71-237">MAPI-Id</span></span>                | <span data-ttu-id="f9a71-238">0x80B5</span><span class="sxs-lookup"><span data-stu-id="f9a71-238">0x80B5</span></span>                                   |
| <span data-ttu-id="f9a71-239">System-Only</span><span class="sxs-lookup"><span data-stu-id="f9a71-239">System-Only</span></span>            | <span data-ttu-id="f9a71-240">Vero</span><span class="sxs-lookup"><span data-stu-id="f9a71-240">True</span></span>                                     |
| <span data-ttu-id="f9a71-241">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="f9a71-241">Is-Single-Valued</span></span>       | <span data-ttu-id="f9a71-242">Falso</span><span class="sxs-lookup"><span data-stu-id="f9a71-242">False</span></span>                                    |
| <span data-ttu-id="f9a71-243">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="f9a71-243">Is Indexed</span></span>             | <span data-ttu-id="f9a71-244">Falso</span><span class="sxs-lookup"><span data-stu-id="f9a71-244">False</span></span>                                    |
| <span data-ttu-id="f9a71-245">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="f9a71-245">In Global Catalog</span></span>      | <span data-ttu-id="f9a71-246">Falso</span><span class="sxs-lookup"><span data-stu-id="f9a71-246">False</span></span>                                    |
| <span data-ttu-id="f9a71-247">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="f9a71-247">NT-Security-Descriptor</span></span> | <span data-ttu-id="f9a71-248">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="f9a71-248">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="f9a71-249">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f9a71-249">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="f9a71-250">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f9a71-250">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="f9a71-251">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f9a71-251">Search-Flags</span></span>           | <span data-ttu-id="f9a71-252">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f9a71-252">0x00000000</span></span>                               |
| <span data-ttu-id="f9a71-253">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f9a71-253">System-Flags</span></span>           | <span data-ttu-id="f9a71-254">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f9a71-254">0x00000010</span></span>                               |
| <span data-ttu-id="f9a71-255">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="f9a71-255">Classes used in</span></span>        | [<span data-ttu-id="f9a71-256">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="f9a71-256">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f9a71-257">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f9a71-257">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f9a71-258">Voce</span><span class="sxs-lookup"><span data-stu-id="f9a71-258">Entry</span></span> | <span data-ttu-id="f9a71-259">Valore</span><span class="sxs-lookup"><span data-stu-id="f9a71-259">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="f9a71-260">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="f9a71-260">Link-Id</span></span>                | <span data-ttu-id="f9a71-261">74</span><span class="sxs-lookup"><span data-stu-id="f9a71-261">74</span></span>                                       |
| <span data-ttu-id="f9a71-262">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f9a71-262">MAPI-Id</span></span>                | <span data-ttu-id="f9a71-263">0x80B5</span><span class="sxs-lookup"><span data-stu-id="f9a71-263">0x80B5</span></span>                                   |
| <span data-ttu-id="f9a71-264">System-Only</span><span class="sxs-lookup"><span data-stu-id="f9a71-264">System-Only</span></span>            | <span data-ttu-id="f9a71-265">Vero</span><span class="sxs-lookup"><span data-stu-id="f9a71-265">True</span></span>                                     |
| <span data-ttu-id="f9a71-266">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="f9a71-266">Is-Single-Valued</span></span>       | <span data-ttu-id="f9a71-267">Falso</span><span class="sxs-lookup"><span data-stu-id="f9a71-267">False</span></span>                                    |
| <span data-ttu-id="f9a71-268">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="f9a71-268">Is Indexed</span></span>             | <span data-ttu-id="f9a71-269">Falso</span><span class="sxs-lookup"><span data-stu-id="f9a71-269">False</span></span>                                    |
| <span data-ttu-id="f9a71-270">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="f9a71-270">In Global Catalog</span></span>      | <span data-ttu-id="f9a71-271">Falso</span><span class="sxs-lookup"><span data-stu-id="f9a71-271">False</span></span>                                    |
| <span data-ttu-id="f9a71-272">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="f9a71-272">NT-Security-Descriptor</span></span> | <span data-ttu-id="f9a71-273">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="f9a71-273">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="f9a71-274">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f9a71-274">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="f9a71-275">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f9a71-275">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="f9a71-276">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f9a71-276">Search-Flags</span></span>           | <span data-ttu-id="f9a71-277">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f9a71-277">0x00000000</span></span>                               |
| <span data-ttu-id="f9a71-278">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f9a71-278">System-Flags</span></span>           | <span data-ttu-id="f9a71-279">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f9a71-279">0x00000010</span></span>                               |
| <span data-ttu-id="f9a71-280">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="f9a71-280">Classes used in</span></span>        | [<span data-ttu-id="f9a71-281">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="f9a71-281">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f9a71-282">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f9a71-282">Windows Server 2012</span></span>



| <span data-ttu-id="f9a71-283">Voce</span><span class="sxs-lookup"><span data-stu-id="f9a71-283">Entry</span></span> | <span data-ttu-id="f9a71-284">Valore</span><span class="sxs-lookup"><span data-stu-id="f9a71-284">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="f9a71-285">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="f9a71-285">Link-Id</span></span>                | <span data-ttu-id="f9a71-286">74</span><span class="sxs-lookup"><span data-stu-id="f9a71-286">74</span></span>                                       |
| <span data-ttu-id="f9a71-287">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f9a71-287">MAPI-Id</span></span>                | <span data-ttu-id="f9a71-288">0x80B5</span><span class="sxs-lookup"><span data-stu-id="f9a71-288">0x80B5</span></span>                                   |
| <span data-ttu-id="f9a71-289">System-Only</span><span class="sxs-lookup"><span data-stu-id="f9a71-289">System-Only</span></span>            | <span data-ttu-id="f9a71-290">Vero</span><span class="sxs-lookup"><span data-stu-id="f9a71-290">True</span></span>                                     |
| <span data-ttu-id="f9a71-291">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="f9a71-291">Is-Single-Valued</span></span>       | <span data-ttu-id="f9a71-292">Falso</span><span class="sxs-lookup"><span data-stu-id="f9a71-292">False</span></span>                                    |
| <span data-ttu-id="f9a71-293">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="f9a71-293">Is Indexed</span></span>             | <span data-ttu-id="f9a71-294">Falso</span><span class="sxs-lookup"><span data-stu-id="f9a71-294">False</span></span>                                    |
| <span data-ttu-id="f9a71-295">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="f9a71-295">In Global Catalog</span></span>      | <span data-ttu-id="f9a71-296">Falso</span><span class="sxs-lookup"><span data-stu-id="f9a71-296">False</span></span>                                    |
| <span data-ttu-id="f9a71-297">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="f9a71-297">NT-Security-Descriptor</span></span> | <span data-ttu-id="f9a71-298">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="f9a71-298">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="f9a71-299">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f9a71-299">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="f9a71-300">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f9a71-300">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="f9a71-301">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f9a71-301">Search-Flags</span></span>           | <span data-ttu-id="f9a71-302">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f9a71-302">0x00000000</span></span>                               |
| <span data-ttu-id="f9a71-303">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f9a71-303">System-Flags</span></span>           | <span data-ttu-id="f9a71-304">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f9a71-304">0x00000010</span></span>                               |
| <span data-ttu-id="f9a71-305">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="f9a71-305">Classes used in</span></span>        | [<span data-ttu-id="f9a71-306">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="f9a71-306">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



 

 





