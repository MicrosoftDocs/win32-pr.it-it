---
title: Attributo Link-ID
description: Intero che indica che l'attributo è un attributo collegato. Un numero intero pari è un collegamento in avanti e un intero dispari è un collegamento a ritroso.
ms.assetid: 73851839-f70c-40c6-976c-0bf727083791
ms.tgt_platform: multiple
keywords:
- Schema di AD dell'attributo Link-ID
- Schema AD dell'attributo linkID
topic_type:
- apiref
api_name:
- Link-ID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a64ad1d26ce5510ac5643419ade46d0565df6487
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104519902"
---
# <a name="link-id-attribute"></a><span data-ttu-id="d65a5-106">Attributo Link-ID</span><span class="sxs-lookup"><span data-stu-id="d65a5-106">Link-ID attribute</span></span>

<span data-ttu-id="d65a5-107">Intero che indica che l'attributo è un attributo collegato.</span><span class="sxs-lookup"><span data-stu-id="d65a5-107">An integer that indicates that the attribute is a linked attribute.</span></span> <span data-ttu-id="d65a5-108">Un numero intero pari è un collegamento in avanti e un intero dispari è un collegamento a ritroso.</span><span class="sxs-lookup"><span data-stu-id="d65a5-108">An even integer is a forward link and an odd integer is a backward link.</span></span>



| <span data-ttu-id="d65a5-109">Voce</span><span class="sxs-lookup"><span data-stu-id="d65a5-109">Entry</span></span> | <span data-ttu-id="d65a5-110">Valore</span><span class="sxs-lookup"><span data-stu-id="d65a5-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="d65a5-111">CN</span><span class="sxs-lookup"><span data-stu-id="d65a5-111">CN</span></span>                | <span data-ttu-id="d65a5-112">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="d65a5-112">Link-ID</span></span>                              |
| <span data-ttu-id="d65a5-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="d65a5-113">Ldap-Display-Name</span></span> | <span data-ttu-id="d65a5-114">linkID</span><span class="sxs-lookup"><span data-stu-id="d65a5-114">linkID</span></span>                               |
| <span data-ttu-id="d65a5-115">Dimensione</span><span class="sxs-lookup"><span data-stu-id="d65a5-115">Size</span></span>              | \-                                   |
| <span data-ttu-id="d65a5-116">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="d65a5-116">Update Privilege</span></span>  | <span data-ttu-id="d65a5-117">Amministratore schema</span><span class="sxs-lookup"><span data-stu-id="d65a5-117">Schema administrator</span></span>                 |
| <span data-ttu-id="d65a5-118">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="d65a5-118">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="d65a5-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="d65a5-119">Attribute-Id</span></span>      | <span data-ttu-id="d65a5-120">1.2.840.113556.1.2.50</span><span class="sxs-lookup"><span data-stu-id="d65a5-120">1.2.840.113556.1.2.50</span></span>                |
| <span data-ttu-id="d65a5-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="d65a5-121">System-Id-Guid</span></span>    | <span data-ttu-id="d65a5-122">bf96799b-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="d65a5-122">bf96799b-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="d65a5-123">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d65a5-123">Syntax</span></span>            | [<span data-ttu-id="d65a5-124">**Enumerazione**</span><span class="sxs-lookup"><span data-stu-id="d65a5-124">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="d65a5-125">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="d65a5-125">Implementations</span></span>

-   [<span data-ttu-id="d65a5-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="d65a5-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="d65a5-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="d65a5-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="d65a5-128">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="d65a5-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="d65a5-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="d65a5-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="d65a5-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="d65a5-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="d65a5-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="d65a5-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="d65a5-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="d65a5-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="d65a5-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d65a5-133">Windows 2000 Server</span></span>



| <span data-ttu-id="d65a5-134">Voce</span><span class="sxs-lookup"><span data-stu-id="d65a5-134">Entry</span></span> | <span data-ttu-id="d65a5-135">Valore</span><span class="sxs-lookup"><span data-stu-id="d65a5-135">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="d65a5-136">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="d65a5-136">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="d65a5-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d65a5-137">MAPI-Id</span></span>                | <span data-ttu-id="d65a5-138">0x80C5</span><span class="sxs-lookup"><span data-stu-id="d65a5-138">0x80C5</span></span>                                                   |
| <span data-ttu-id="d65a5-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="d65a5-139">System-Only</span></span>            | <span data-ttu-id="d65a5-140">Vero</span><span class="sxs-lookup"><span data-stu-id="d65a5-140">True</span></span>                                                     |
| <span data-ttu-id="d65a5-141">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="d65a5-141">Is-Single-Valued</span></span>       | <span data-ttu-id="d65a5-142">Vero</span><span class="sxs-lookup"><span data-stu-id="d65a5-142">True</span></span>                                                     |
| <span data-ttu-id="d65a5-143">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="d65a5-143">Is Indexed</span></span>             | <span data-ttu-id="d65a5-144">Falso</span><span class="sxs-lookup"><span data-stu-id="d65a5-144">False</span></span>                                                    |
| <span data-ttu-id="d65a5-145">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="d65a5-145">In Global Catalog</span></span>      | <span data-ttu-id="d65a5-146">Falso</span><span class="sxs-lookup"><span data-stu-id="d65a5-146">False</span></span>                                                    |
| <span data-ttu-id="d65a5-147">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="d65a5-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="d65a5-148">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="d65a5-148">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="d65a5-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d65a5-149">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="d65a5-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d65a5-150">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="d65a5-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d65a5-151">Search-Flags</span></span>           | <span data-ttu-id="d65a5-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d65a5-152">0x00000000</span></span>                                               |
| <span data-ttu-id="d65a5-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d65a5-153">System-Flags</span></span>           | <span data-ttu-id="d65a5-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d65a5-154">0x00000010</span></span>                                               |
| <span data-ttu-id="d65a5-155">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="d65a5-155">Classes used in</span></span>        | [<span data-ttu-id="d65a5-156">**Attribute-schema**</span><span class="sxs-lookup"><span data-stu-id="d65a5-156">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="d65a5-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d65a5-157">Windows Server 2003</span></span>



| <span data-ttu-id="d65a5-158">Voce</span><span class="sxs-lookup"><span data-stu-id="d65a5-158">Entry</span></span> | <span data-ttu-id="d65a5-159">Valore</span><span class="sxs-lookup"><span data-stu-id="d65a5-159">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="d65a5-160">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="d65a5-160">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="d65a5-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d65a5-161">MAPI-Id</span></span>                | <span data-ttu-id="d65a5-162">0x80C5</span><span class="sxs-lookup"><span data-stu-id="d65a5-162">0x80C5</span></span>                                                   |
| <span data-ttu-id="d65a5-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="d65a5-163">System-Only</span></span>            | <span data-ttu-id="d65a5-164">Vero</span><span class="sxs-lookup"><span data-stu-id="d65a5-164">True</span></span>                                                     |
| <span data-ttu-id="d65a5-165">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="d65a5-165">Is-Single-Valued</span></span>       | <span data-ttu-id="d65a5-166">Vero</span><span class="sxs-lookup"><span data-stu-id="d65a5-166">True</span></span>                                                     |
| <span data-ttu-id="d65a5-167">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="d65a5-167">Is Indexed</span></span>             | <span data-ttu-id="d65a5-168">Falso</span><span class="sxs-lookup"><span data-stu-id="d65a5-168">False</span></span>                                                    |
| <span data-ttu-id="d65a5-169">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="d65a5-169">In Global Catalog</span></span>      | <span data-ttu-id="d65a5-170">Falso</span><span class="sxs-lookup"><span data-stu-id="d65a5-170">False</span></span>                                                    |
| <span data-ttu-id="d65a5-171">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="d65a5-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="d65a5-172">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="d65a5-172">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="d65a5-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d65a5-173">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="d65a5-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d65a5-174">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="d65a5-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d65a5-175">Search-Flags</span></span>           | <span data-ttu-id="d65a5-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d65a5-176">0x00000000</span></span>                                               |
| <span data-ttu-id="d65a5-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d65a5-177">System-Flags</span></span>           | <span data-ttu-id="d65a5-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d65a5-178">0x00000010</span></span>                                               |
| <span data-ttu-id="d65a5-179">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="d65a5-179">Classes used in</span></span>        | [<span data-ttu-id="d65a5-180">**Attribute-schema**</span><span class="sxs-lookup"><span data-stu-id="d65a5-180">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="d65a5-181">ADAM</span><span class="sxs-lookup"><span data-stu-id="d65a5-181">ADAM</span></span>



| <span data-ttu-id="d65a5-182">Voce</span><span class="sxs-lookup"><span data-stu-id="d65a5-182">Entry</span></span> | <span data-ttu-id="d65a5-183">Valore</span><span class="sxs-lookup"><span data-stu-id="d65a5-183">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="d65a5-184">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="d65a5-184">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="d65a5-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d65a5-185">MAPI-Id</span></span>                | <span data-ttu-id="d65a5-186">0x80C5</span><span class="sxs-lookup"><span data-stu-id="d65a5-186">0x80C5</span></span>                                                   |
| <span data-ttu-id="d65a5-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="d65a5-187">System-Only</span></span>            | <span data-ttu-id="d65a5-188">Vero</span><span class="sxs-lookup"><span data-stu-id="d65a5-188">True</span></span>                                                     |
| <span data-ttu-id="d65a5-189">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="d65a5-189">Is-Single-Valued</span></span>       | <span data-ttu-id="d65a5-190">Vero</span><span class="sxs-lookup"><span data-stu-id="d65a5-190">True</span></span>                                                     |
| <span data-ttu-id="d65a5-191">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="d65a5-191">Is Indexed</span></span>             | <span data-ttu-id="d65a5-192">Falso</span><span class="sxs-lookup"><span data-stu-id="d65a5-192">False</span></span>                                                    |
| <span data-ttu-id="d65a5-193">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="d65a5-193">In Global Catalog</span></span>      | <span data-ttu-id="d65a5-194">Falso</span><span class="sxs-lookup"><span data-stu-id="d65a5-194">False</span></span>                                                    |
| <span data-ttu-id="d65a5-195">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="d65a5-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="d65a5-196">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="d65a5-196">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="d65a5-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d65a5-197">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="d65a5-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d65a5-198">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="d65a5-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d65a5-199">Search-Flags</span></span>           | <span data-ttu-id="d65a5-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d65a5-200">0x00000000</span></span>                                               |
| <span data-ttu-id="d65a5-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d65a5-201">System-Flags</span></span>           | <span data-ttu-id="d65a5-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d65a5-202">0x00000010</span></span>                                               |
| <span data-ttu-id="d65a5-203">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="d65a5-203">Classes used in</span></span>        | [<span data-ttu-id="d65a5-204">**Attribute-schema**</span><span class="sxs-lookup"><span data-stu-id="d65a5-204">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="d65a5-205">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="d65a5-205">Windows Server 2003 R2</span></span>



| <span data-ttu-id="d65a5-206">Voce</span><span class="sxs-lookup"><span data-stu-id="d65a5-206">Entry</span></span> | <span data-ttu-id="d65a5-207">Valore</span><span class="sxs-lookup"><span data-stu-id="d65a5-207">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="d65a5-208">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="d65a5-208">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="d65a5-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d65a5-209">MAPI-Id</span></span>                | <span data-ttu-id="d65a5-210">0x80C5</span><span class="sxs-lookup"><span data-stu-id="d65a5-210">0x80C5</span></span>                                                   |
| <span data-ttu-id="d65a5-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="d65a5-211">System-Only</span></span>            | <span data-ttu-id="d65a5-212">Vero</span><span class="sxs-lookup"><span data-stu-id="d65a5-212">True</span></span>                                                     |
| <span data-ttu-id="d65a5-213">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="d65a5-213">Is-Single-Valued</span></span>       | <span data-ttu-id="d65a5-214">Vero</span><span class="sxs-lookup"><span data-stu-id="d65a5-214">True</span></span>                                                     |
| <span data-ttu-id="d65a5-215">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="d65a5-215">Is Indexed</span></span>             | <span data-ttu-id="d65a5-216">Falso</span><span class="sxs-lookup"><span data-stu-id="d65a5-216">False</span></span>                                                    |
| <span data-ttu-id="d65a5-217">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="d65a5-217">In Global Catalog</span></span>      | <span data-ttu-id="d65a5-218">Falso</span><span class="sxs-lookup"><span data-stu-id="d65a5-218">False</span></span>                                                    |
| <span data-ttu-id="d65a5-219">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="d65a5-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="d65a5-220">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="d65a5-220">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="d65a5-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d65a5-221">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="d65a5-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d65a5-222">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="d65a5-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d65a5-223">Search-Flags</span></span>           | <span data-ttu-id="d65a5-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d65a5-224">0x00000000</span></span>                                               |
| <span data-ttu-id="d65a5-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d65a5-225">System-Flags</span></span>           | <span data-ttu-id="d65a5-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d65a5-226">0x00000010</span></span>                                               |
| <span data-ttu-id="d65a5-227">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="d65a5-227">Classes used in</span></span>        | [<span data-ttu-id="d65a5-228">**Attribute-schema**</span><span class="sxs-lookup"><span data-stu-id="d65a5-228">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="d65a5-229">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d65a5-229">Windows Server 2008</span></span>



| <span data-ttu-id="d65a5-230">Voce</span><span class="sxs-lookup"><span data-stu-id="d65a5-230">Entry</span></span> | <span data-ttu-id="d65a5-231">Valore</span><span class="sxs-lookup"><span data-stu-id="d65a5-231">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="d65a5-232">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="d65a5-232">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="d65a5-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d65a5-233">MAPI-Id</span></span>                | <span data-ttu-id="d65a5-234">0x80C5</span><span class="sxs-lookup"><span data-stu-id="d65a5-234">0x80C5</span></span>                                                   |
| <span data-ttu-id="d65a5-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="d65a5-235">System-Only</span></span>            | <span data-ttu-id="d65a5-236">Vero</span><span class="sxs-lookup"><span data-stu-id="d65a5-236">True</span></span>                                                     |
| <span data-ttu-id="d65a5-237">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="d65a5-237">Is-Single-Valued</span></span>       | <span data-ttu-id="d65a5-238">Vero</span><span class="sxs-lookup"><span data-stu-id="d65a5-238">True</span></span>                                                     |
| <span data-ttu-id="d65a5-239">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="d65a5-239">Is Indexed</span></span>             | <span data-ttu-id="d65a5-240">Falso</span><span class="sxs-lookup"><span data-stu-id="d65a5-240">False</span></span>                                                    |
| <span data-ttu-id="d65a5-241">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="d65a5-241">In Global Catalog</span></span>      | <span data-ttu-id="d65a5-242">Falso</span><span class="sxs-lookup"><span data-stu-id="d65a5-242">False</span></span>                                                    |
| <span data-ttu-id="d65a5-243">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="d65a5-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="d65a5-244">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="d65a5-244">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="d65a5-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d65a5-245">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="d65a5-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d65a5-246">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="d65a5-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d65a5-247">Search-Flags</span></span>           | <span data-ttu-id="d65a5-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d65a5-248">0x00000000</span></span>                                               |
| <span data-ttu-id="d65a5-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d65a5-249">System-Flags</span></span>           | <span data-ttu-id="d65a5-250">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d65a5-250">0x00000010</span></span>                                               |
| <span data-ttu-id="d65a5-251">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="d65a5-251">Classes used in</span></span>        | [<span data-ttu-id="d65a5-252">**Attribute-schema**</span><span class="sxs-lookup"><span data-stu-id="d65a5-252">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="d65a5-253">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d65a5-253">Windows Server 2008 R2</span></span>



| <span data-ttu-id="d65a5-254">Voce</span><span class="sxs-lookup"><span data-stu-id="d65a5-254">Entry</span></span> | <span data-ttu-id="d65a5-255">Valore</span><span class="sxs-lookup"><span data-stu-id="d65a5-255">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="d65a5-256">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="d65a5-256">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="d65a5-257">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d65a5-257">MAPI-Id</span></span>                | <span data-ttu-id="d65a5-258">0x80C5</span><span class="sxs-lookup"><span data-stu-id="d65a5-258">0x80C5</span></span>                                                   |
| <span data-ttu-id="d65a5-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="d65a5-259">System-Only</span></span>            | <span data-ttu-id="d65a5-260">Vero</span><span class="sxs-lookup"><span data-stu-id="d65a5-260">True</span></span>                                                     |
| <span data-ttu-id="d65a5-261">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="d65a5-261">Is-Single-Valued</span></span>       | <span data-ttu-id="d65a5-262">Vero</span><span class="sxs-lookup"><span data-stu-id="d65a5-262">True</span></span>                                                     |
| <span data-ttu-id="d65a5-263">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="d65a5-263">Is Indexed</span></span>             | <span data-ttu-id="d65a5-264">Falso</span><span class="sxs-lookup"><span data-stu-id="d65a5-264">False</span></span>                                                    |
| <span data-ttu-id="d65a5-265">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="d65a5-265">In Global Catalog</span></span>      | <span data-ttu-id="d65a5-266">Falso</span><span class="sxs-lookup"><span data-stu-id="d65a5-266">False</span></span>                                                    |
| <span data-ttu-id="d65a5-267">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="d65a5-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="d65a5-268">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="d65a5-268">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="d65a5-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d65a5-269">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="d65a5-270">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d65a5-270">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="d65a5-271">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d65a5-271">Search-Flags</span></span>           | <span data-ttu-id="d65a5-272">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d65a5-272">0x00000000</span></span>                                               |
| <span data-ttu-id="d65a5-273">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d65a5-273">System-Flags</span></span>           | <span data-ttu-id="d65a5-274">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d65a5-274">0x00000010</span></span>                                               |
| <span data-ttu-id="d65a5-275">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="d65a5-275">Classes used in</span></span>        | [<span data-ttu-id="d65a5-276">**Attribute-schema**</span><span class="sxs-lookup"><span data-stu-id="d65a5-276">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="d65a5-277">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d65a5-277">Windows Server 2012</span></span>



| <span data-ttu-id="d65a5-278">Voce</span><span class="sxs-lookup"><span data-stu-id="d65a5-278">Entry</span></span> | <span data-ttu-id="d65a5-279">Valore</span><span class="sxs-lookup"><span data-stu-id="d65a5-279">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="d65a5-280">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="d65a5-280">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="d65a5-281">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d65a5-281">MAPI-Id</span></span>                | <span data-ttu-id="d65a5-282">0x80C5</span><span class="sxs-lookup"><span data-stu-id="d65a5-282">0x80C5</span></span>                                                   |
| <span data-ttu-id="d65a5-283">System-Only</span><span class="sxs-lookup"><span data-stu-id="d65a5-283">System-Only</span></span>            | <span data-ttu-id="d65a5-284">Vero</span><span class="sxs-lookup"><span data-stu-id="d65a5-284">True</span></span>                                                     |
| <span data-ttu-id="d65a5-285">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="d65a5-285">Is-Single-Valued</span></span>       | <span data-ttu-id="d65a5-286">Vero</span><span class="sxs-lookup"><span data-stu-id="d65a5-286">True</span></span>                                                     |
| <span data-ttu-id="d65a5-287">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="d65a5-287">Is Indexed</span></span>             | <span data-ttu-id="d65a5-288">Falso</span><span class="sxs-lookup"><span data-stu-id="d65a5-288">False</span></span>                                                    |
| <span data-ttu-id="d65a5-289">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="d65a5-289">In Global Catalog</span></span>      | <span data-ttu-id="d65a5-290">Falso</span><span class="sxs-lookup"><span data-stu-id="d65a5-290">False</span></span>                                                    |
| <span data-ttu-id="d65a5-291">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="d65a5-291">NT-Security-Descriptor</span></span> | <span data-ttu-id="d65a5-292">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="d65a5-292">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="d65a5-293">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d65a5-293">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="d65a5-294">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d65a5-294">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="d65a5-295">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d65a5-295">Search-Flags</span></span>           | <span data-ttu-id="d65a5-296">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d65a5-296">0x00000000</span></span>                                               |
| <span data-ttu-id="d65a5-297">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d65a5-297">System-Flags</span></span>           | <span data-ttu-id="d65a5-298">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d65a5-298">0x00000010</span></span>                                               |
| <span data-ttu-id="d65a5-299">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="d65a5-299">Classes used in</span></span>        | [<span data-ttu-id="d65a5-300">**Attribute-schema**</span><span class="sxs-lookup"><span data-stu-id="d65a5-300">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



 

 





