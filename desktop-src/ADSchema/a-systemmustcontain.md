---
title: Attributo System-must-contain
description: Elenco di attributi obbligatori per una classe. Questi attributi devono essere specificati quando viene creata un'istanza della classe. L'elenco di attributi può essere modificato solo dal sistema.
ms.assetid: 5131bd16-1a8d-4d4a-98e4-6140438c6517
ms.tgt_platform: multiple
keywords:
- Attributo System-must-contain-schema AD
- Schema AD dell'attributo systemMustContain
topic_type:
- apiref
api_name:
- System-Must-Contain
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f8d36419ca7e6cd24422645579fb7f9ecc69457
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104519966"
---
# <a name="system-must-contain-attribute"></a><span data-ttu-id="78d94-107">Attributo System-must-contain</span><span class="sxs-lookup"><span data-stu-id="78d94-107">System-Must-Contain attribute</span></span>

<span data-ttu-id="78d94-108">Elenco di attributi obbligatori per una classe.</span><span class="sxs-lookup"><span data-stu-id="78d94-108">The list of mandatory attributes for a class.</span></span> <span data-ttu-id="78d94-109">Questi attributi devono essere specificati quando viene creata un'istanza della classe.</span><span class="sxs-lookup"><span data-stu-id="78d94-109">These attributes must be specified when an instance of the class is created.</span></span> <span data-ttu-id="78d94-110">L'elenco di attributi può essere modificato solo dal sistema.</span><span class="sxs-lookup"><span data-stu-id="78d94-110">The list of attributes can only be modified by the system.</span></span>



| <span data-ttu-id="78d94-111">Voce</span><span class="sxs-lookup"><span data-stu-id="78d94-111">Entry</span></span> | <span data-ttu-id="78d94-112">Valore</span><span class="sxs-lookup"><span data-stu-id="78d94-112">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="78d94-113">CN</span><span class="sxs-lookup"><span data-stu-id="78d94-113">CN</span></span>                | <span data-ttu-id="78d94-114">System-must-contain</span><span class="sxs-lookup"><span data-stu-id="78d94-114">System-Must-Contain</span></span>                                                           |
| <span data-ttu-id="78d94-115">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="78d94-115">Ldap-Display-Name</span></span> | <span data-ttu-id="78d94-116">systemMustContain</span><span class="sxs-lookup"><span data-stu-id="78d94-116">systemMustContain</span></span>                                                             |
| <span data-ttu-id="78d94-117">Dimensione</span><span class="sxs-lookup"><span data-stu-id="78d94-117">Size</span></span>              | \-                                                                            |
| <span data-ttu-id="78d94-118">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="78d94-118">Update Privilege</span></span>  | <span data-ttu-id="78d94-119">Amministratore schema</span><span class="sxs-lookup"><span data-stu-id="78d94-119">Schema administrator</span></span>                                                          |
| <span data-ttu-id="78d94-120">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="78d94-120">Update Frequency</span></span>  | <span data-ttu-id="78d94-121">Quando la classe viene creata o viene aggiunto un nuovo attributo obbligatorio alla classe.</span><span class="sxs-lookup"><span data-stu-id="78d94-121">When the class is created or a new mandatory attribute is added to the class.</span></span> |
| <span data-ttu-id="78d94-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="78d94-122">Attribute-Id</span></span>      | <span data-ttu-id="78d94-123">1.2.840.113556.1.4.197</span><span class="sxs-lookup"><span data-stu-id="78d94-123">1.2.840.113556.1.4.197</span></span>                                                        |
| <span data-ttu-id="78d94-124">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="78d94-124">System-Id-Guid</span></span>    | <span data-ttu-id="78d94-125">bf967a45-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="78d94-125">bf967a45-0de6-11d0-a285-00aa003049e2</span></span>                                          |
| <span data-ttu-id="78d94-126">Sintassi</span><span class="sxs-lookup"><span data-stu-id="78d94-126">Syntax</span></span>            | [<span data-ttu-id="78d94-127">**String(Object-Identifier)**</span><span class="sxs-lookup"><span data-stu-id="78d94-127">**String(Object-Identifier)**</span></span>](s-string-object-identifier.md)               |



## <a name="implementations"></a><span data-ttu-id="78d94-128">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="78d94-128">Implementations</span></span>

-   [<span data-ttu-id="78d94-129">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="78d94-129">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="78d94-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="78d94-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="78d94-131">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="78d94-131">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="78d94-132">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="78d94-132">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="78d94-133">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="78d94-133">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="78d94-134">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="78d94-134">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="78d94-135">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="78d94-135">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="78d94-136">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="78d94-136">Windows 2000 Server</span></span>



| <span data-ttu-id="78d94-137">Voce</span><span class="sxs-lookup"><span data-stu-id="78d94-137">Entry</span></span> | <span data-ttu-id="78d94-138">Valore</span><span class="sxs-lookup"><span data-stu-id="78d94-138">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="78d94-139">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="78d94-139">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="78d94-140">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="78d94-140">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="78d94-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="78d94-141">System-Only</span></span>            | <span data-ttu-id="78d94-142">Vero</span><span class="sxs-lookup"><span data-stu-id="78d94-142">True</span></span>                                             |
| <span data-ttu-id="78d94-143">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="78d94-143">Is-Single-Valued</span></span>       | <span data-ttu-id="78d94-144">Falso</span><span class="sxs-lookup"><span data-stu-id="78d94-144">False</span></span>                                            |
| <span data-ttu-id="78d94-145">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="78d94-145">Is Indexed</span></span>             | <span data-ttu-id="78d94-146">Falso</span><span class="sxs-lookup"><span data-stu-id="78d94-146">False</span></span>                                            |
| <span data-ttu-id="78d94-147">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="78d94-147">In Global Catalog</span></span>      | <span data-ttu-id="78d94-148">Falso</span><span class="sxs-lookup"><span data-stu-id="78d94-148">False</span></span>                                            |
| <span data-ttu-id="78d94-149">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="78d94-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="78d94-150">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="78d94-150">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="78d94-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="78d94-151">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="78d94-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="78d94-152">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="78d94-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="78d94-153">Search-Flags</span></span>           | <span data-ttu-id="78d94-154">0x00000000</span><span class="sxs-lookup"><span data-stu-id="78d94-154">0x00000000</span></span>                                       |
| <span data-ttu-id="78d94-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="78d94-155">System-Flags</span></span>           | <span data-ttu-id="78d94-156">0x00000010</span><span class="sxs-lookup"><span data-stu-id="78d94-156">0x00000010</span></span>                                       |
| <span data-ttu-id="78d94-157">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="78d94-157">Classes used in</span></span>        | [<span data-ttu-id="78d94-158">**Classe-schema**</span><span class="sxs-lookup"><span data-stu-id="78d94-158">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="78d94-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="78d94-159">Windows Server 2003</span></span>



| <span data-ttu-id="78d94-160">Voce</span><span class="sxs-lookup"><span data-stu-id="78d94-160">Entry</span></span> | <span data-ttu-id="78d94-161">Valore</span><span class="sxs-lookup"><span data-stu-id="78d94-161">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="78d94-162">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="78d94-162">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="78d94-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="78d94-163">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="78d94-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="78d94-164">System-Only</span></span>            | <span data-ttu-id="78d94-165">Vero</span><span class="sxs-lookup"><span data-stu-id="78d94-165">True</span></span>                                             |
| <span data-ttu-id="78d94-166">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="78d94-166">Is-Single-Valued</span></span>       | <span data-ttu-id="78d94-167">Falso</span><span class="sxs-lookup"><span data-stu-id="78d94-167">False</span></span>                                            |
| <span data-ttu-id="78d94-168">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="78d94-168">Is Indexed</span></span>             | <span data-ttu-id="78d94-169">Falso</span><span class="sxs-lookup"><span data-stu-id="78d94-169">False</span></span>                                            |
| <span data-ttu-id="78d94-170">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="78d94-170">In Global Catalog</span></span>      | <span data-ttu-id="78d94-171">Falso</span><span class="sxs-lookup"><span data-stu-id="78d94-171">False</span></span>                                            |
| <span data-ttu-id="78d94-172">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="78d94-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="78d94-173">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="78d94-173">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="78d94-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="78d94-174">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="78d94-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="78d94-175">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="78d94-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="78d94-176">Search-Flags</span></span>           | <span data-ttu-id="78d94-177">0x00000000</span><span class="sxs-lookup"><span data-stu-id="78d94-177">0x00000000</span></span>                                       |
| <span data-ttu-id="78d94-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="78d94-178">System-Flags</span></span>           | <span data-ttu-id="78d94-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="78d94-179">0x00000010</span></span>                                       |
| <span data-ttu-id="78d94-180">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="78d94-180">Classes used in</span></span>        | [<span data-ttu-id="78d94-181">**Classe-schema**</span><span class="sxs-lookup"><span data-stu-id="78d94-181">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="78d94-182">ADAM</span><span class="sxs-lookup"><span data-stu-id="78d94-182">ADAM</span></span>



| <span data-ttu-id="78d94-183">Voce</span><span class="sxs-lookup"><span data-stu-id="78d94-183">Entry</span></span> | <span data-ttu-id="78d94-184">Valore</span><span class="sxs-lookup"><span data-stu-id="78d94-184">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="78d94-185">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="78d94-185">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="78d94-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="78d94-186">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="78d94-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="78d94-187">System-Only</span></span>            | <span data-ttu-id="78d94-188">Vero</span><span class="sxs-lookup"><span data-stu-id="78d94-188">True</span></span>                                             |
| <span data-ttu-id="78d94-189">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="78d94-189">Is-Single-Valued</span></span>       | <span data-ttu-id="78d94-190">Falso</span><span class="sxs-lookup"><span data-stu-id="78d94-190">False</span></span>                                            |
| <span data-ttu-id="78d94-191">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="78d94-191">Is Indexed</span></span>             | <span data-ttu-id="78d94-192">Falso</span><span class="sxs-lookup"><span data-stu-id="78d94-192">False</span></span>                                            |
| <span data-ttu-id="78d94-193">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="78d94-193">In Global Catalog</span></span>      | <span data-ttu-id="78d94-194">Falso</span><span class="sxs-lookup"><span data-stu-id="78d94-194">False</span></span>                                            |
| <span data-ttu-id="78d94-195">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="78d94-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="78d94-196">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="78d94-196">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="78d94-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="78d94-197">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="78d94-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="78d94-198">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="78d94-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="78d94-199">Search-Flags</span></span>           | <span data-ttu-id="78d94-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="78d94-200">0x00000000</span></span>                                       |
| <span data-ttu-id="78d94-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="78d94-201">System-Flags</span></span>           | <span data-ttu-id="78d94-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="78d94-202">0x00000010</span></span>                                       |
| <span data-ttu-id="78d94-203">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="78d94-203">Classes used in</span></span>        | [<span data-ttu-id="78d94-204">**Classe-schema**</span><span class="sxs-lookup"><span data-stu-id="78d94-204">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="78d94-205">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="78d94-205">Windows Server 2003 R2</span></span>



| <span data-ttu-id="78d94-206">Voce</span><span class="sxs-lookup"><span data-stu-id="78d94-206">Entry</span></span> | <span data-ttu-id="78d94-207">Valore</span><span class="sxs-lookup"><span data-stu-id="78d94-207">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="78d94-208">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="78d94-208">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="78d94-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="78d94-209">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="78d94-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="78d94-210">System-Only</span></span>            | <span data-ttu-id="78d94-211">Vero</span><span class="sxs-lookup"><span data-stu-id="78d94-211">True</span></span>                                             |
| <span data-ttu-id="78d94-212">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="78d94-212">Is-Single-Valued</span></span>       | <span data-ttu-id="78d94-213">Falso</span><span class="sxs-lookup"><span data-stu-id="78d94-213">False</span></span>                                            |
| <span data-ttu-id="78d94-214">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="78d94-214">Is Indexed</span></span>             | <span data-ttu-id="78d94-215">Falso</span><span class="sxs-lookup"><span data-stu-id="78d94-215">False</span></span>                                            |
| <span data-ttu-id="78d94-216">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="78d94-216">In Global Catalog</span></span>      | <span data-ttu-id="78d94-217">Falso</span><span class="sxs-lookup"><span data-stu-id="78d94-217">False</span></span>                                            |
| <span data-ttu-id="78d94-218">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="78d94-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="78d94-219">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="78d94-219">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="78d94-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="78d94-220">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="78d94-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="78d94-221">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="78d94-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="78d94-222">Search-Flags</span></span>           | <span data-ttu-id="78d94-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="78d94-223">0x00000000</span></span>                                       |
| <span data-ttu-id="78d94-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="78d94-224">System-Flags</span></span>           | <span data-ttu-id="78d94-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="78d94-225">0x00000010</span></span>                                       |
| <span data-ttu-id="78d94-226">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="78d94-226">Classes used in</span></span>        | [<span data-ttu-id="78d94-227">**Classe-schema**</span><span class="sxs-lookup"><span data-stu-id="78d94-227">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="78d94-228">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="78d94-228">Windows Server 2008</span></span>



| <span data-ttu-id="78d94-229">Voce</span><span class="sxs-lookup"><span data-stu-id="78d94-229">Entry</span></span> | <span data-ttu-id="78d94-230">Valore</span><span class="sxs-lookup"><span data-stu-id="78d94-230">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="78d94-231">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="78d94-231">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="78d94-232">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="78d94-232">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="78d94-233">System-Only</span><span class="sxs-lookup"><span data-stu-id="78d94-233">System-Only</span></span>            | <span data-ttu-id="78d94-234">Vero</span><span class="sxs-lookup"><span data-stu-id="78d94-234">True</span></span>                                             |
| <span data-ttu-id="78d94-235">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="78d94-235">Is-Single-Valued</span></span>       | <span data-ttu-id="78d94-236">Falso</span><span class="sxs-lookup"><span data-stu-id="78d94-236">False</span></span>                                            |
| <span data-ttu-id="78d94-237">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="78d94-237">Is Indexed</span></span>             | <span data-ttu-id="78d94-238">Falso</span><span class="sxs-lookup"><span data-stu-id="78d94-238">False</span></span>                                            |
| <span data-ttu-id="78d94-239">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="78d94-239">In Global Catalog</span></span>      | <span data-ttu-id="78d94-240">Falso</span><span class="sxs-lookup"><span data-stu-id="78d94-240">False</span></span>                                            |
| <span data-ttu-id="78d94-241">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="78d94-241">NT-Security-Descriptor</span></span> | <span data-ttu-id="78d94-242">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="78d94-242">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="78d94-243">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="78d94-243">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="78d94-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="78d94-244">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="78d94-245">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="78d94-245">Search-Flags</span></span>           | <span data-ttu-id="78d94-246">0x00000000</span><span class="sxs-lookup"><span data-stu-id="78d94-246">0x00000000</span></span>                                       |
| <span data-ttu-id="78d94-247">System-Flags</span><span class="sxs-lookup"><span data-stu-id="78d94-247">System-Flags</span></span>           | <span data-ttu-id="78d94-248">0x00000010</span><span class="sxs-lookup"><span data-stu-id="78d94-248">0x00000010</span></span>                                       |
| <span data-ttu-id="78d94-249">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="78d94-249">Classes used in</span></span>        | [<span data-ttu-id="78d94-250">**Classe-schema**</span><span class="sxs-lookup"><span data-stu-id="78d94-250">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="78d94-251">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="78d94-251">Windows Server 2008 R2</span></span>



| <span data-ttu-id="78d94-252">Voce</span><span class="sxs-lookup"><span data-stu-id="78d94-252">Entry</span></span> | <span data-ttu-id="78d94-253">Valore</span><span class="sxs-lookup"><span data-stu-id="78d94-253">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="78d94-254">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="78d94-254">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="78d94-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="78d94-255">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="78d94-256">System-Only</span><span class="sxs-lookup"><span data-stu-id="78d94-256">System-Only</span></span>            | <span data-ttu-id="78d94-257">Vero</span><span class="sxs-lookup"><span data-stu-id="78d94-257">True</span></span>                                             |
| <span data-ttu-id="78d94-258">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="78d94-258">Is-Single-Valued</span></span>       | <span data-ttu-id="78d94-259">Falso</span><span class="sxs-lookup"><span data-stu-id="78d94-259">False</span></span>                                            |
| <span data-ttu-id="78d94-260">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="78d94-260">Is Indexed</span></span>             | <span data-ttu-id="78d94-261">Falso</span><span class="sxs-lookup"><span data-stu-id="78d94-261">False</span></span>                                            |
| <span data-ttu-id="78d94-262">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="78d94-262">In Global Catalog</span></span>      | <span data-ttu-id="78d94-263">Falso</span><span class="sxs-lookup"><span data-stu-id="78d94-263">False</span></span>                                            |
| <span data-ttu-id="78d94-264">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="78d94-264">NT-Security-Descriptor</span></span> | <span data-ttu-id="78d94-265">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="78d94-265">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="78d94-266">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="78d94-266">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="78d94-267">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="78d94-267">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="78d94-268">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="78d94-268">Search-Flags</span></span>           | <span data-ttu-id="78d94-269">0x00000000</span><span class="sxs-lookup"><span data-stu-id="78d94-269">0x00000000</span></span>                                       |
| <span data-ttu-id="78d94-270">System-Flags</span><span class="sxs-lookup"><span data-stu-id="78d94-270">System-Flags</span></span>           | <span data-ttu-id="78d94-271">0x00000010</span><span class="sxs-lookup"><span data-stu-id="78d94-271">0x00000010</span></span>                                       |
| <span data-ttu-id="78d94-272">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="78d94-272">Classes used in</span></span>        | [<span data-ttu-id="78d94-273">**Classe-schema**</span><span class="sxs-lookup"><span data-stu-id="78d94-273">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="78d94-274">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="78d94-274">Windows Server 2012</span></span>



| <span data-ttu-id="78d94-275">Voce</span><span class="sxs-lookup"><span data-stu-id="78d94-275">Entry</span></span> | <span data-ttu-id="78d94-276">Valore</span><span class="sxs-lookup"><span data-stu-id="78d94-276">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="78d94-277">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="78d94-277">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="78d94-278">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="78d94-278">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="78d94-279">System-Only</span><span class="sxs-lookup"><span data-stu-id="78d94-279">System-Only</span></span>            | <span data-ttu-id="78d94-280">Vero</span><span class="sxs-lookup"><span data-stu-id="78d94-280">True</span></span>                                             |
| <span data-ttu-id="78d94-281">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="78d94-281">Is-Single-Valued</span></span>       | <span data-ttu-id="78d94-282">Falso</span><span class="sxs-lookup"><span data-stu-id="78d94-282">False</span></span>                                            |
| <span data-ttu-id="78d94-283">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="78d94-283">Is Indexed</span></span>             | <span data-ttu-id="78d94-284">Falso</span><span class="sxs-lookup"><span data-stu-id="78d94-284">False</span></span>                                            |
| <span data-ttu-id="78d94-285">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="78d94-285">In Global Catalog</span></span>      | <span data-ttu-id="78d94-286">Falso</span><span class="sxs-lookup"><span data-stu-id="78d94-286">False</span></span>                                            |
| <span data-ttu-id="78d94-287">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="78d94-287">NT-Security-Descriptor</span></span> | <span data-ttu-id="78d94-288">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="78d94-288">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="78d94-289">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="78d94-289">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="78d94-290">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="78d94-290">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="78d94-291">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="78d94-291">Search-Flags</span></span>           | <span data-ttu-id="78d94-292">0x00000000</span><span class="sxs-lookup"><span data-stu-id="78d94-292">0x00000000</span></span>                                       |
| <span data-ttu-id="78d94-293">System-Flags</span><span class="sxs-lookup"><span data-stu-id="78d94-293">System-Flags</span></span>           | <span data-ttu-id="78d94-294">0x00000010</span><span class="sxs-lookup"><span data-stu-id="78d94-294">0x00000010</span></span>                                       |
| <span data-ttu-id="78d94-295">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="78d94-295">Classes used in</span></span>        | [<span data-ttu-id="78d94-296">**Classe-schema**</span><span class="sxs-lookup"><span data-stu-id="78d94-296">**Class-Schema**</span></span>](c-classschema.md)<br/> |



 

 





