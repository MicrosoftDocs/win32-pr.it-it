---
title: Attributo RDN-att-ID
description: RDN per l'attributo utilizzato per assegnare un nome a una classe.
ms.assetid: 793199c4-6c5e-481f-8f73-bd59375ab51b
ms.tgt_platform: multiple
keywords:
- RDN-att-ID attributo AD schema
- Schema AD dell'attributo rDNAttID
topic_type:
- apiref
api_name:
- RDN-Att-ID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43b5fb573d289b71bb459cd8595b5df5115f42bf
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "106303147"
---
# <a name="rdn-att-id-attribute"></a><span data-ttu-id="a4217-105">Attributo RDN-att-ID</span><span class="sxs-lookup"><span data-stu-id="a4217-105">RDN-Att-ID attribute</span></span>

<span data-ttu-id="a4217-106">RDN per l'attributo utilizzato per assegnare un nome a una classe.</span><span class="sxs-lookup"><span data-stu-id="a4217-106">The RDN for the attribute that is used to name a class.</span></span>



| <span data-ttu-id="a4217-107">Voce</span><span class="sxs-lookup"><span data-stu-id="a4217-107">Entry</span></span> | <span data-ttu-id="a4217-108">Valore</span><span class="sxs-lookup"><span data-stu-id="a4217-108">Value</span></span> |
|-------------------|-----------------------------------------------------------------|
| <span data-ttu-id="a4217-109">CN</span><span class="sxs-lookup"><span data-stu-id="a4217-109">CN</span></span>                | <span data-ttu-id="a4217-110">RDN-att-ID</span><span class="sxs-lookup"><span data-stu-id="a4217-110">RDN-Att-ID</span></span>                                                      |
| <span data-ttu-id="a4217-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="a4217-111">Ldap-Display-Name</span></span> | <span data-ttu-id="a4217-112">rDNAttID</span><span class="sxs-lookup"><span data-stu-id="a4217-112">rDNAttID</span></span>                                                        |
| <span data-ttu-id="a4217-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="a4217-113">Size</span></span>              | \-                                                              |
| <span data-ttu-id="a4217-114">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="a4217-114">Update Privilege</span></span>  | <span data-ttu-id="a4217-115">Amministratore schema</span><span class="sxs-lookup"><span data-stu-id="a4217-115">Schema administrator</span></span>                                            |
| <span data-ttu-id="a4217-116">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="a4217-116">Update Frequency</span></span>  | \-                                                              |
| <span data-ttu-id="a4217-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a4217-117">Attribute-Id</span></span>      | <span data-ttu-id="a4217-118">1.2.840.113556.1.2.26</span><span class="sxs-lookup"><span data-stu-id="a4217-118">1.2.840.113556.1.2.26</span></span>                                           |
| <span data-ttu-id="a4217-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="a4217-119">System-Id-Guid</span></span>    | <span data-ttu-id="a4217-120">bf967a0f-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="a4217-120">bf967a0f-0de6-11d0-a285-00aa003049e2</span></span>                            |
| <span data-ttu-id="a4217-121">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a4217-121">Syntax</span></span>            | [<span data-ttu-id="a4217-122">**String(Object-Identifier)**</span><span class="sxs-lookup"><span data-stu-id="a4217-122">**String(Object-Identifier)**</span></span>](s-string-object-identifier.md) |



## <a name="implementations"></a><span data-ttu-id="a4217-123">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="a4217-123">Implementations</span></span>

-   [<span data-ttu-id="a4217-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="a4217-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="a4217-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a4217-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a4217-126">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="a4217-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="a4217-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a4217-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a4217-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a4217-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a4217-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a4217-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a4217-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a4217-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="a4217-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a4217-131">Windows 2000 Server</span></span>



| <span data-ttu-id="a4217-132">Voce</span><span class="sxs-lookup"><span data-stu-id="a4217-132">Entry</span></span> | <span data-ttu-id="a4217-133">Valore</span><span class="sxs-lookup"><span data-stu-id="a4217-133">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="a4217-134">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="a4217-134">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="a4217-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a4217-135">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="a4217-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="a4217-136">System-Only</span></span>            | <span data-ttu-id="a4217-137">Vero</span><span class="sxs-lookup"><span data-stu-id="a4217-137">True</span></span>                                             |
| <span data-ttu-id="a4217-138">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="a4217-138">Is-Single-Valued</span></span>       | <span data-ttu-id="a4217-139">Vero</span><span class="sxs-lookup"><span data-stu-id="a4217-139">True</span></span>                                             |
| <span data-ttu-id="a4217-140">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="a4217-140">Is Indexed</span></span>             | <span data-ttu-id="a4217-141">Falso</span><span class="sxs-lookup"><span data-stu-id="a4217-141">False</span></span>                                            |
| <span data-ttu-id="a4217-142">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="a4217-142">In Global Catalog</span></span>      | <span data-ttu-id="a4217-143">Falso</span><span class="sxs-lookup"><span data-stu-id="a4217-143">False</span></span>                                            |
| <span data-ttu-id="a4217-144">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="a4217-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="a4217-145">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="a4217-145">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="a4217-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a4217-146">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="a4217-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a4217-147">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="a4217-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a4217-148">Search-Flags</span></span>           | <span data-ttu-id="a4217-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a4217-149">0x00000000</span></span>                                       |
| <span data-ttu-id="a4217-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a4217-150">System-Flags</span></span>           | <span data-ttu-id="a4217-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a4217-151">0x00000010</span></span>                                       |
| <span data-ttu-id="a4217-152">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="a4217-152">Classes used in</span></span>        | [<span data-ttu-id="a4217-153">**Classe-schema**</span><span class="sxs-lookup"><span data-stu-id="a4217-153">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="a4217-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a4217-154">Windows Server 2003</span></span>



| <span data-ttu-id="a4217-155">Voce</span><span class="sxs-lookup"><span data-stu-id="a4217-155">Entry</span></span> | <span data-ttu-id="a4217-156">Valore</span><span class="sxs-lookup"><span data-stu-id="a4217-156">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="a4217-157">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="a4217-157">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="a4217-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a4217-158">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="a4217-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="a4217-159">System-Only</span></span>            | <span data-ttu-id="a4217-160">Vero</span><span class="sxs-lookup"><span data-stu-id="a4217-160">True</span></span>                                             |
| <span data-ttu-id="a4217-161">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="a4217-161">Is-Single-Valued</span></span>       | <span data-ttu-id="a4217-162">Vero</span><span class="sxs-lookup"><span data-stu-id="a4217-162">True</span></span>                                             |
| <span data-ttu-id="a4217-163">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="a4217-163">Is Indexed</span></span>             | <span data-ttu-id="a4217-164">Falso</span><span class="sxs-lookup"><span data-stu-id="a4217-164">False</span></span>                                            |
| <span data-ttu-id="a4217-165">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="a4217-165">In Global Catalog</span></span>      | <span data-ttu-id="a4217-166">Falso</span><span class="sxs-lookup"><span data-stu-id="a4217-166">False</span></span>                                            |
| <span data-ttu-id="a4217-167">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="a4217-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="a4217-168">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="a4217-168">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="a4217-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a4217-169">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="a4217-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a4217-170">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="a4217-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a4217-171">Search-Flags</span></span>           | <span data-ttu-id="a4217-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a4217-172">0x00000000</span></span>                                       |
| <span data-ttu-id="a4217-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a4217-173">System-Flags</span></span>           | <span data-ttu-id="a4217-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a4217-174">0x00000010</span></span>                                       |
| <span data-ttu-id="a4217-175">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="a4217-175">Classes used in</span></span>        | [<span data-ttu-id="a4217-176">**Classe-schema**</span><span class="sxs-lookup"><span data-stu-id="a4217-176">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="a4217-177">ADAM</span><span class="sxs-lookup"><span data-stu-id="a4217-177">ADAM</span></span>



| <span data-ttu-id="a4217-178">Voce</span><span class="sxs-lookup"><span data-stu-id="a4217-178">Entry</span></span> | <span data-ttu-id="a4217-179">Valore</span><span class="sxs-lookup"><span data-stu-id="a4217-179">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="a4217-180">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="a4217-180">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="a4217-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a4217-181">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="a4217-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="a4217-182">System-Only</span></span>            | <span data-ttu-id="a4217-183">Vero</span><span class="sxs-lookup"><span data-stu-id="a4217-183">True</span></span>                                             |
| <span data-ttu-id="a4217-184">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="a4217-184">Is-Single-Valued</span></span>       | <span data-ttu-id="a4217-185">Vero</span><span class="sxs-lookup"><span data-stu-id="a4217-185">True</span></span>                                             |
| <span data-ttu-id="a4217-186">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="a4217-186">Is Indexed</span></span>             | <span data-ttu-id="a4217-187">Falso</span><span class="sxs-lookup"><span data-stu-id="a4217-187">False</span></span>                                            |
| <span data-ttu-id="a4217-188">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="a4217-188">In Global Catalog</span></span>      | <span data-ttu-id="a4217-189">Falso</span><span class="sxs-lookup"><span data-stu-id="a4217-189">False</span></span>                                            |
| <span data-ttu-id="a4217-190">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="a4217-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="a4217-191">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="a4217-191">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="a4217-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a4217-192">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="a4217-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a4217-193">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="a4217-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a4217-194">Search-Flags</span></span>           | <span data-ttu-id="a4217-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a4217-195">0x00000000</span></span>                                       |
| <span data-ttu-id="a4217-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a4217-196">System-Flags</span></span>           | <span data-ttu-id="a4217-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a4217-197">0x00000010</span></span>                                       |
| <span data-ttu-id="a4217-198">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="a4217-198">Classes used in</span></span>        | [<span data-ttu-id="a4217-199">**Classe-schema**</span><span class="sxs-lookup"><span data-stu-id="a4217-199">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a4217-200">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a4217-200">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a4217-201">Voce</span><span class="sxs-lookup"><span data-stu-id="a4217-201">Entry</span></span> | <span data-ttu-id="a4217-202">Valore</span><span class="sxs-lookup"><span data-stu-id="a4217-202">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="a4217-203">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="a4217-203">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="a4217-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a4217-204">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="a4217-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="a4217-205">System-Only</span></span>            | <span data-ttu-id="a4217-206">Vero</span><span class="sxs-lookup"><span data-stu-id="a4217-206">True</span></span>                                             |
| <span data-ttu-id="a4217-207">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="a4217-207">Is-Single-Valued</span></span>       | <span data-ttu-id="a4217-208">Vero</span><span class="sxs-lookup"><span data-stu-id="a4217-208">True</span></span>                                             |
| <span data-ttu-id="a4217-209">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="a4217-209">Is Indexed</span></span>             | <span data-ttu-id="a4217-210">Falso</span><span class="sxs-lookup"><span data-stu-id="a4217-210">False</span></span>                                            |
| <span data-ttu-id="a4217-211">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="a4217-211">In Global Catalog</span></span>      | <span data-ttu-id="a4217-212">Falso</span><span class="sxs-lookup"><span data-stu-id="a4217-212">False</span></span>                                            |
| <span data-ttu-id="a4217-213">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="a4217-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="a4217-214">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="a4217-214">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="a4217-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a4217-215">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="a4217-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a4217-216">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="a4217-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a4217-217">Search-Flags</span></span>           | <span data-ttu-id="a4217-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a4217-218">0x00000000</span></span>                                       |
| <span data-ttu-id="a4217-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a4217-219">System-Flags</span></span>           | <span data-ttu-id="a4217-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a4217-220">0x00000010</span></span>                                       |
| <span data-ttu-id="a4217-221">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="a4217-221">Classes used in</span></span>        | [<span data-ttu-id="a4217-222">**Classe-schema**</span><span class="sxs-lookup"><span data-stu-id="a4217-222">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a4217-223">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a4217-223">Windows Server 2008</span></span>



| <span data-ttu-id="a4217-224">Voce</span><span class="sxs-lookup"><span data-stu-id="a4217-224">Entry</span></span> | <span data-ttu-id="a4217-225">Valore</span><span class="sxs-lookup"><span data-stu-id="a4217-225">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="a4217-226">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="a4217-226">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="a4217-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a4217-227">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="a4217-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="a4217-228">System-Only</span></span>            | <span data-ttu-id="a4217-229">Vero</span><span class="sxs-lookup"><span data-stu-id="a4217-229">True</span></span>                                             |
| <span data-ttu-id="a4217-230">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="a4217-230">Is-Single-Valued</span></span>       | <span data-ttu-id="a4217-231">Vero</span><span class="sxs-lookup"><span data-stu-id="a4217-231">True</span></span>                                             |
| <span data-ttu-id="a4217-232">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="a4217-232">Is Indexed</span></span>             | <span data-ttu-id="a4217-233">Falso</span><span class="sxs-lookup"><span data-stu-id="a4217-233">False</span></span>                                            |
| <span data-ttu-id="a4217-234">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="a4217-234">In Global Catalog</span></span>      | <span data-ttu-id="a4217-235">Falso</span><span class="sxs-lookup"><span data-stu-id="a4217-235">False</span></span>                                            |
| <span data-ttu-id="a4217-236">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="a4217-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="a4217-237">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="a4217-237">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="a4217-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a4217-238">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="a4217-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a4217-239">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="a4217-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a4217-240">Search-Flags</span></span>           | <span data-ttu-id="a4217-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a4217-241">0x00000000</span></span>                                       |
| <span data-ttu-id="a4217-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a4217-242">System-Flags</span></span>           | <span data-ttu-id="a4217-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a4217-243">0x00000010</span></span>                                       |
| <span data-ttu-id="a4217-244">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="a4217-244">Classes used in</span></span>        | [<span data-ttu-id="a4217-245">**Classe-schema**</span><span class="sxs-lookup"><span data-stu-id="a4217-245">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a4217-246">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a4217-246">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a4217-247">Voce</span><span class="sxs-lookup"><span data-stu-id="a4217-247">Entry</span></span> | <span data-ttu-id="a4217-248">Valore</span><span class="sxs-lookup"><span data-stu-id="a4217-248">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="a4217-249">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="a4217-249">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="a4217-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a4217-250">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="a4217-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="a4217-251">System-Only</span></span>            | <span data-ttu-id="a4217-252">Vero</span><span class="sxs-lookup"><span data-stu-id="a4217-252">True</span></span>                                             |
| <span data-ttu-id="a4217-253">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="a4217-253">Is-Single-Valued</span></span>       | <span data-ttu-id="a4217-254">Vero</span><span class="sxs-lookup"><span data-stu-id="a4217-254">True</span></span>                                             |
| <span data-ttu-id="a4217-255">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="a4217-255">Is Indexed</span></span>             | <span data-ttu-id="a4217-256">Falso</span><span class="sxs-lookup"><span data-stu-id="a4217-256">False</span></span>                                            |
| <span data-ttu-id="a4217-257">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="a4217-257">In Global Catalog</span></span>      | <span data-ttu-id="a4217-258">Falso</span><span class="sxs-lookup"><span data-stu-id="a4217-258">False</span></span>                                            |
| <span data-ttu-id="a4217-259">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="a4217-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="a4217-260">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="a4217-260">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="a4217-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a4217-261">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="a4217-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a4217-262">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="a4217-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a4217-263">Search-Flags</span></span>           | <span data-ttu-id="a4217-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a4217-264">0x00000000</span></span>                                       |
| <span data-ttu-id="a4217-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a4217-265">System-Flags</span></span>           | <span data-ttu-id="a4217-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a4217-266">0x00000010</span></span>                                       |
| <span data-ttu-id="a4217-267">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="a4217-267">Classes used in</span></span>        | [<span data-ttu-id="a4217-268">**Classe-schema**</span><span class="sxs-lookup"><span data-stu-id="a4217-268">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a4217-269">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a4217-269">Windows Server 2012</span></span>



| <span data-ttu-id="a4217-270">Voce</span><span class="sxs-lookup"><span data-stu-id="a4217-270">Entry</span></span> | <span data-ttu-id="a4217-271">Valore</span><span class="sxs-lookup"><span data-stu-id="a4217-271">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="a4217-272">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="a4217-272">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="a4217-273">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a4217-273">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="a4217-274">System-Only</span><span class="sxs-lookup"><span data-stu-id="a4217-274">System-Only</span></span>            | <span data-ttu-id="a4217-275">Vero</span><span class="sxs-lookup"><span data-stu-id="a4217-275">True</span></span>                                             |
| <span data-ttu-id="a4217-276">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="a4217-276">Is-Single-Valued</span></span>       | <span data-ttu-id="a4217-277">Vero</span><span class="sxs-lookup"><span data-stu-id="a4217-277">True</span></span>                                             |
| <span data-ttu-id="a4217-278">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="a4217-278">Is Indexed</span></span>             | <span data-ttu-id="a4217-279">Falso</span><span class="sxs-lookup"><span data-stu-id="a4217-279">False</span></span>                                            |
| <span data-ttu-id="a4217-280">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="a4217-280">In Global Catalog</span></span>      | <span data-ttu-id="a4217-281">Falso</span><span class="sxs-lookup"><span data-stu-id="a4217-281">False</span></span>                                            |
| <span data-ttu-id="a4217-282">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="a4217-282">NT-Security-Descriptor</span></span> | <span data-ttu-id="a4217-283">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="a4217-283">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="a4217-284">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a4217-284">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="a4217-285">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a4217-285">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="a4217-286">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a4217-286">Search-Flags</span></span>           | <span data-ttu-id="a4217-287">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a4217-287">0x00000000</span></span>                                       |
| <span data-ttu-id="a4217-288">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a4217-288">System-Flags</span></span>           | <span data-ttu-id="a4217-289">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a4217-289">0x00000010</span></span>                                       |
| <span data-ttu-id="a4217-290">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="a4217-290">Classes used in</span></span>        | [<span data-ttu-id="a4217-291">**Classe-schema**</span><span class="sxs-lookup"><span data-stu-id="a4217-291">**Class-Schema**</span></span>](c-classschema.md)<br/> |



 

 





