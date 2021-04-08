---
title: Attributo Must-Contain
description: Elenco di attributi obbligatori per una classe. Questi attributi devono essere specificati quando viene creata un'istanza della classe.
ms.assetid: ad112640-0e99-453a-8eff-f964419d8631
ms.tgt_platform: multiple
keywords:
- Schema AD Must-Contain attribute
- Schema AD dell'attributo mustContain
topic_type:
- apiref
api_name:
- Must-Contain
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d791468691f438d01161f0d6252f7b995fc0f51e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744591"
---
# <a name="must-contain-attribute"></a><span data-ttu-id="6e42f-106">Attributo Must-Contain</span><span class="sxs-lookup"><span data-stu-id="6e42f-106">Must-Contain attribute</span></span>

<span data-ttu-id="6e42f-107">Elenco di attributi obbligatori per una classe.</span><span class="sxs-lookup"><span data-stu-id="6e42f-107">The list of mandatory attributes for a class.</span></span> <span data-ttu-id="6e42f-108">Questi attributi devono essere specificati quando viene creata un'istanza della classe.</span><span class="sxs-lookup"><span data-stu-id="6e42f-108">These attributes must be specified when an instance of the class is created.</span></span>



| <span data-ttu-id="6e42f-109">Voce</span><span class="sxs-lookup"><span data-stu-id="6e42f-109">Entry</span></span> | <span data-ttu-id="6e42f-110">Valore</span><span class="sxs-lookup"><span data-stu-id="6e42f-110">Value</span></span> |
|-------------------|-----------------------------------------------------------------|
| <span data-ttu-id="6e42f-111">CN</span><span class="sxs-lookup"><span data-stu-id="6e42f-111">CN</span></span>                | <span data-ttu-id="6e42f-112">Must-Contain</span><span class="sxs-lookup"><span data-stu-id="6e42f-112">Must-Contain</span></span>                                                    |
| <span data-ttu-id="6e42f-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="6e42f-113">Ldap-Display-Name</span></span> | <span data-ttu-id="6e42f-114">mustContain</span><span class="sxs-lookup"><span data-stu-id="6e42f-114">mustContain</span></span>                                                     |
| <span data-ttu-id="6e42f-115">Dimensione</span><span class="sxs-lookup"><span data-stu-id="6e42f-115">Size</span></span>              | \-                                                              |
| <span data-ttu-id="6e42f-116">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="6e42f-116">Update Privilege</span></span>  | <span data-ttu-id="6e42f-117">Amministratore schema</span><span class="sxs-lookup"><span data-stu-id="6e42f-117">Schema administrator</span></span>                                            |
| <span data-ttu-id="6e42f-118">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="6e42f-118">Update Frequency</span></span>  | \-                                                              |
| <span data-ttu-id="6e42f-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="6e42f-119">Attribute-Id</span></span>      | <span data-ttu-id="6e42f-120">1.2.840.113556.1.2.24</span><span class="sxs-lookup"><span data-stu-id="6e42f-120">1.2.840.113556.1.2.24</span></span>                                           |
| <span data-ttu-id="6e42f-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="6e42f-121">System-Id-Guid</span></span>    | <span data-ttu-id="6e42f-122">bf9679d3-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="6e42f-122">bf9679d3-0de6-11d0-a285-00aa003049e2</span></span>                            |
| <span data-ttu-id="6e42f-123">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6e42f-123">Syntax</span></span>            | [<span data-ttu-id="6e42f-124">**String(Object-Identifier)**</span><span class="sxs-lookup"><span data-stu-id="6e42f-124">**String(Object-Identifier)**</span></span>](s-string-object-identifier.md) |



## <a name="implementations"></a><span data-ttu-id="6e42f-125">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="6e42f-125">Implementations</span></span>

-   [<span data-ttu-id="6e42f-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="6e42f-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="6e42f-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="6e42f-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="6e42f-128">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="6e42f-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="6e42f-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="6e42f-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="6e42f-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="6e42f-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="6e42f-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="6e42f-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="6e42f-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="6e42f-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="6e42f-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6e42f-133">Windows 2000 Server</span></span>



| <span data-ttu-id="6e42f-134">Voce</span><span class="sxs-lookup"><span data-stu-id="6e42f-134">Entry</span></span> | <span data-ttu-id="6e42f-135">Valore</span><span class="sxs-lookup"><span data-stu-id="6e42f-135">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="6e42f-136">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="6e42f-136">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="6e42f-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6e42f-137">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="6e42f-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="6e42f-138">System-Only</span></span>            | <span data-ttu-id="6e42f-139">Falso</span><span class="sxs-lookup"><span data-stu-id="6e42f-139">False</span></span>                                            |
| <span data-ttu-id="6e42f-140">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="6e42f-140">Is-Single-Valued</span></span>       | <span data-ttu-id="6e42f-141">Falso</span><span class="sxs-lookup"><span data-stu-id="6e42f-141">False</span></span>                                            |
| <span data-ttu-id="6e42f-142">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="6e42f-142">Is Indexed</span></span>             | <span data-ttu-id="6e42f-143">Falso</span><span class="sxs-lookup"><span data-stu-id="6e42f-143">False</span></span>                                            |
| <span data-ttu-id="6e42f-144">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="6e42f-144">In Global Catalog</span></span>      | <span data-ttu-id="6e42f-145">Falso</span><span class="sxs-lookup"><span data-stu-id="6e42f-145">False</span></span>                                            |
| <span data-ttu-id="6e42f-146">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="6e42f-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="6e42f-147">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="6e42f-147">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="6e42f-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6e42f-148">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="6e42f-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6e42f-149">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="6e42f-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6e42f-150">Search-Flags</span></span>           | <span data-ttu-id="6e42f-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6e42f-151">0x00000000</span></span>                                       |
| <span data-ttu-id="6e42f-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6e42f-152">System-Flags</span></span>           | <span data-ttu-id="6e42f-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6e42f-153">0x00000010</span></span>                                       |
| <span data-ttu-id="6e42f-154">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="6e42f-154">Classes used in</span></span>        | [<span data-ttu-id="6e42f-155">**Classe-schema**</span><span class="sxs-lookup"><span data-stu-id="6e42f-155">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="6e42f-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6e42f-156">Windows Server 2003</span></span>



| <span data-ttu-id="6e42f-157">Voce</span><span class="sxs-lookup"><span data-stu-id="6e42f-157">Entry</span></span> | <span data-ttu-id="6e42f-158">Valore</span><span class="sxs-lookup"><span data-stu-id="6e42f-158">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="6e42f-159">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="6e42f-159">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="6e42f-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6e42f-160">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="6e42f-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="6e42f-161">System-Only</span></span>            | <span data-ttu-id="6e42f-162">Falso</span><span class="sxs-lookup"><span data-stu-id="6e42f-162">False</span></span>                                            |
| <span data-ttu-id="6e42f-163">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="6e42f-163">Is-Single-Valued</span></span>       | <span data-ttu-id="6e42f-164">Falso</span><span class="sxs-lookup"><span data-stu-id="6e42f-164">False</span></span>                                            |
| <span data-ttu-id="6e42f-165">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="6e42f-165">Is Indexed</span></span>             | <span data-ttu-id="6e42f-166">Falso</span><span class="sxs-lookup"><span data-stu-id="6e42f-166">False</span></span>                                            |
| <span data-ttu-id="6e42f-167">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="6e42f-167">In Global Catalog</span></span>      | <span data-ttu-id="6e42f-168">Falso</span><span class="sxs-lookup"><span data-stu-id="6e42f-168">False</span></span>                                            |
| <span data-ttu-id="6e42f-169">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="6e42f-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="6e42f-170">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="6e42f-170">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="6e42f-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6e42f-171">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="6e42f-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6e42f-172">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="6e42f-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6e42f-173">Search-Flags</span></span>           | <span data-ttu-id="6e42f-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6e42f-174">0x00000000</span></span>                                       |
| <span data-ttu-id="6e42f-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6e42f-175">System-Flags</span></span>           | <span data-ttu-id="6e42f-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6e42f-176">0x00000010</span></span>                                       |
| <span data-ttu-id="6e42f-177">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="6e42f-177">Classes used in</span></span>        | [<span data-ttu-id="6e42f-178">**Classe-schema**</span><span class="sxs-lookup"><span data-stu-id="6e42f-178">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="6e42f-179">ADAM</span><span class="sxs-lookup"><span data-stu-id="6e42f-179">ADAM</span></span>



| <span data-ttu-id="6e42f-180">Voce</span><span class="sxs-lookup"><span data-stu-id="6e42f-180">Entry</span></span> | <span data-ttu-id="6e42f-181">Valore</span><span class="sxs-lookup"><span data-stu-id="6e42f-181">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="6e42f-182">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="6e42f-182">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="6e42f-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6e42f-183">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="6e42f-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="6e42f-184">System-Only</span></span>            | <span data-ttu-id="6e42f-185">Falso</span><span class="sxs-lookup"><span data-stu-id="6e42f-185">False</span></span>                                            |
| <span data-ttu-id="6e42f-186">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="6e42f-186">Is-Single-Valued</span></span>       | <span data-ttu-id="6e42f-187">Falso</span><span class="sxs-lookup"><span data-stu-id="6e42f-187">False</span></span>                                            |
| <span data-ttu-id="6e42f-188">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="6e42f-188">Is Indexed</span></span>             | <span data-ttu-id="6e42f-189">Falso</span><span class="sxs-lookup"><span data-stu-id="6e42f-189">False</span></span>                                            |
| <span data-ttu-id="6e42f-190">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="6e42f-190">In Global Catalog</span></span>      | <span data-ttu-id="6e42f-191">Falso</span><span class="sxs-lookup"><span data-stu-id="6e42f-191">False</span></span>                                            |
| <span data-ttu-id="6e42f-192">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="6e42f-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="6e42f-193">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="6e42f-193">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="6e42f-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6e42f-194">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="6e42f-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6e42f-195">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="6e42f-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6e42f-196">Search-Flags</span></span>           | <span data-ttu-id="6e42f-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6e42f-197">0x00000000</span></span>                                       |
| <span data-ttu-id="6e42f-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6e42f-198">System-Flags</span></span>           | <span data-ttu-id="6e42f-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6e42f-199">0x00000010</span></span>                                       |
| <span data-ttu-id="6e42f-200">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="6e42f-200">Classes used in</span></span>        | [<span data-ttu-id="6e42f-201">**Classe-schema**</span><span class="sxs-lookup"><span data-stu-id="6e42f-201">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="6e42f-202">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="6e42f-202">Windows Server 2003 R2</span></span>



| <span data-ttu-id="6e42f-203">Voce</span><span class="sxs-lookup"><span data-stu-id="6e42f-203">Entry</span></span> | <span data-ttu-id="6e42f-204">Valore</span><span class="sxs-lookup"><span data-stu-id="6e42f-204">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="6e42f-205">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="6e42f-205">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="6e42f-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6e42f-206">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="6e42f-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="6e42f-207">System-Only</span></span>            | <span data-ttu-id="6e42f-208">Falso</span><span class="sxs-lookup"><span data-stu-id="6e42f-208">False</span></span>                                            |
| <span data-ttu-id="6e42f-209">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="6e42f-209">Is-Single-Valued</span></span>       | <span data-ttu-id="6e42f-210">Falso</span><span class="sxs-lookup"><span data-stu-id="6e42f-210">False</span></span>                                            |
| <span data-ttu-id="6e42f-211">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="6e42f-211">Is Indexed</span></span>             | <span data-ttu-id="6e42f-212">Falso</span><span class="sxs-lookup"><span data-stu-id="6e42f-212">False</span></span>                                            |
| <span data-ttu-id="6e42f-213">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="6e42f-213">In Global Catalog</span></span>      | <span data-ttu-id="6e42f-214">Falso</span><span class="sxs-lookup"><span data-stu-id="6e42f-214">False</span></span>                                            |
| <span data-ttu-id="6e42f-215">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="6e42f-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="6e42f-216">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="6e42f-216">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="6e42f-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6e42f-217">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="6e42f-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6e42f-218">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="6e42f-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6e42f-219">Search-Flags</span></span>           | <span data-ttu-id="6e42f-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6e42f-220">0x00000000</span></span>                                       |
| <span data-ttu-id="6e42f-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6e42f-221">System-Flags</span></span>           | <span data-ttu-id="6e42f-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6e42f-222">0x00000010</span></span>                                       |
| <span data-ttu-id="6e42f-223">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="6e42f-223">Classes used in</span></span>        | [<span data-ttu-id="6e42f-224">**Classe-schema**</span><span class="sxs-lookup"><span data-stu-id="6e42f-224">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="6e42f-225">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6e42f-225">Windows Server 2008</span></span>



| <span data-ttu-id="6e42f-226">Voce</span><span class="sxs-lookup"><span data-stu-id="6e42f-226">Entry</span></span> | <span data-ttu-id="6e42f-227">Valore</span><span class="sxs-lookup"><span data-stu-id="6e42f-227">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="6e42f-228">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="6e42f-228">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="6e42f-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6e42f-229">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="6e42f-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="6e42f-230">System-Only</span></span>            | <span data-ttu-id="6e42f-231">Falso</span><span class="sxs-lookup"><span data-stu-id="6e42f-231">False</span></span>                                            |
| <span data-ttu-id="6e42f-232">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="6e42f-232">Is-Single-Valued</span></span>       | <span data-ttu-id="6e42f-233">Falso</span><span class="sxs-lookup"><span data-stu-id="6e42f-233">False</span></span>                                            |
| <span data-ttu-id="6e42f-234">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="6e42f-234">Is Indexed</span></span>             | <span data-ttu-id="6e42f-235">Falso</span><span class="sxs-lookup"><span data-stu-id="6e42f-235">False</span></span>                                            |
| <span data-ttu-id="6e42f-236">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="6e42f-236">In Global Catalog</span></span>      | <span data-ttu-id="6e42f-237">Falso</span><span class="sxs-lookup"><span data-stu-id="6e42f-237">False</span></span>                                            |
| <span data-ttu-id="6e42f-238">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="6e42f-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="6e42f-239">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="6e42f-239">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="6e42f-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6e42f-240">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="6e42f-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6e42f-241">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="6e42f-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6e42f-242">Search-Flags</span></span>           | <span data-ttu-id="6e42f-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6e42f-243">0x00000000</span></span>                                       |
| <span data-ttu-id="6e42f-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6e42f-244">System-Flags</span></span>           | <span data-ttu-id="6e42f-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6e42f-245">0x00000010</span></span>                                       |
| <span data-ttu-id="6e42f-246">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="6e42f-246">Classes used in</span></span>        | [<span data-ttu-id="6e42f-247">**Classe-schema**</span><span class="sxs-lookup"><span data-stu-id="6e42f-247">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="6e42f-248">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6e42f-248">Windows Server 2008 R2</span></span>



| <span data-ttu-id="6e42f-249">Voce</span><span class="sxs-lookup"><span data-stu-id="6e42f-249">Entry</span></span> | <span data-ttu-id="6e42f-250">Valore</span><span class="sxs-lookup"><span data-stu-id="6e42f-250">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="6e42f-251">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="6e42f-251">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="6e42f-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6e42f-252">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="6e42f-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="6e42f-253">System-Only</span></span>            | <span data-ttu-id="6e42f-254">Falso</span><span class="sxs-lookup"><span data-stu-id="6e42f-254">False</span></span>                                            |
| <span data-ttu-id="6e42f-255">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="6e42f-255">Is-Single-Valued</span></span>       | <span data-ttu-id="6e42f-256">Falso</span><span class="sxs-lookup"><span data-stu-id="6e42f-256">False</span></span>                                            |
| <span data-ttu-id="6e42f-257">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="6e42f-257">Is Indexed</span></span>             | <span data-ttu-id="6e42f-258">Falso</span><span class="sxs-lookup"><span data-stu-id="6e42f-258">False</span></span>                                            |
| <span data-ttu-id="6e42f-259">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="6e42f-259">In Global Catalog</span></span>      | <span data-ttu-id="6e42f-260">Falso</span><span class="sxs-lookup"><span data-stu-id="6e42f-260">False</span></span>                                            |
| <span data-ttu-id="6e42f-261">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="6e42f-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="6e42f-262">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="6e42f-262">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="6e42f-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6e42f-263">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="6e42f-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6e42f-264">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="6e42f-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6e42f-265">Search-Flags</span></span>           | <span data-ttu-id="6e42f-266">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6e42f-266">0x00000000</span></span>                                       |
| <span data-ttu-id="6e42f-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6e42f-267">System-Flags</span></span>           | <span data-ttu-id="6e42f-268">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6e42f-268">0x00000010</span></span>                                       |
| <span data-ttu-id="6e42f-269">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="6e42f-269">Classes used in</span></span>        | [<span data-ttu-id="6e42f-270">**Classe-schema**</span><span class="sxs-lookup"><span data-stu-id="6e42f-270">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="6e42f-271">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6e42f-271">Windows Server 2012</span></span>



| <span data-ttu-id="6e42f-272">Voce</span><span class="sxs-lookup"><span data-stu-id="6e42f-272">Entry</span></span> | <span data-ttu-id="6e42f-273">Valore</span><span class="sxs-lookup"><span data-stu-id="6e42f-273">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="6e42f-274">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="6e42f-274">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="6e42f-275">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6e42f-275">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="6e42f-276">System-Only</span><span class="sxs-lookup"><span data-stu-id="6e42f-276">System-Only</span></span>            | <span data-ttu-id="6e42f-277">Falso</span><span class="sxs-lookup"><span data-stu-id="6e42f-277">False</span></span>                                            |
| <span data-ttu-id="6e42f-278">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="6e42f-278">Is-Single-Valued</span></span>       | <span data-ttu-id="6e42f-279">Falso</span><span class="sxs-lookup"><span data-stu-id="6e42f-279">False</span></span>                                            |
| <span data-ttu-id="6e42f-280">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="6e42f-280">Is Indexed</span></span>             | <span data-ttu-id="6e42f-281">Falso</span><span class="sxs-lookup"><span data-stu-id="6e42f-281">False</span></span>                                            |
| <span data-ttu-id="6e42f-282">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="6e42f-282">In Global Catalog</span></span>      | <span data-ttu-id="6e42f-283">Falso</span><span class="sxs-lookup"><span data-stu-id="6e42f-283">False</span></span>                                            |
| <span data-ttu-id="6e42f-284">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="6e42f-284">NT-Security-Descriptor</span></span> | <span data-ttu-id="6e42f-285">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="6e42f-285">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="6e42f-286">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6e42f-286">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="6e42f-287">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6e42f-287">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="6e42f-288">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6e42f-288">Search-Flags</span></span>           | <span data-ttu-id="6e42f-289">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6e42f-289">0x00000000</span></span>                                       |
| <span data-ttu-id="6e42f-290">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6e42f-290">System-Flags</span></span>           | <span data-ttu-id="6e42f-291">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6e42f-291">0x00000010</span></span>                                       |
| <span data-ttu-id="6e42f-292">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="6e42f-292">Classes used in</span></span>        | [<span data-ttu-id="6e42f-293">**Classe-schema**</span><span class="sxs-lookup"><span data-stu-id="6e42f-293">**Class-Schema**</span></span>](c-classschema.md)<br/> |



 

 





