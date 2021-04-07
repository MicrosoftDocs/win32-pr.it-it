---
title: Attributo Object-Classes
description: Proprietà con più valori che contiene stringhe che rappresentano ogni classe nello schema. Ogni valore contiene governsID, lDAPDisplayName, mustContain, mayContain e così via.
ms.assetid: 7e3eda48-8e64-4a52-8d92-7a0d37e513ef
ms.tgt_platform: multiple
keywords:
- Schema AD Object-Classes attribute
- Schema AD dell'attributo objectClasses
topic_type:
- apiref
api_name:
- Object-Classes
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b799c725790115152ac70c0214d82a8c242ea600
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103875606"
---
# <a name="object-classes-attribute"></a><span data-ttu-id="0c5be-106">Attributo Object-Classes</span><span class="sxs-lookup"><span data-stu-id="0c5be-106">Object-Classes attribute</span></span>

<span data-ttu-id="0c5be-107">Proprietà con più valori che contiene stringhe che rappresentano ogni classe nello schema.</span><span class="sxs-lookup"><span data-stu-id="0c5be-107">A multiple-valued property that contains strings that represent each class in the schema.</span></span> <span data-ttu-id="0c5be-108">Ogni valore contiene governsID, lDAPDisplayName, mustContain, mayContain e così via.</span><span class="sxs-lookup"><span data-stu-id="0c5be-108">Each value contains the governsID, lDAPDisplayName, mustContain, mayContain, and so on.</span></span>



| <span data-ttu-id="0c5be-109">Voce</span><span class="sxs-lookup"><span data-stu-id="0c5be-109">Entry</span></span> | <span data-ttu-id="0c5be-110">Valore</span><span class="sxs-lookup"><span data-stu-id="0c5be-110">Value</span></span> |
|-------------------|--------------------------------------------------|
| <span data-ttu-id="0c5be-111">CN</span><span class="sxs-lookup"><span data-stu-id="0c5be-111">CN</span></span>                | <span data-ttu-id="0c5be-112">Object-Classes</span><span class="sxs-lookup"><span data-stu-id="0c5be-112">Object-Classes</span></span>                                   |
| <span data-ttu-id="0c5be-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="0c5be-113">Ldap-Display-Name</span></span> | <span data-ttu-id="0c5be-114">objectClasses</span><span class="sxs-lookup"><span data-stu-id="0c5be-114">objectClasses</span></span>                                    |
| <span data-ttu-id="0c5be-115">Dimensione</span><span class="sxs-lookup"><span data-stu-id="0c5be-115">Size</span></span>              | <span data-ttu-id="0c5be-116">Circa 20 byte in media per nome di classe.</span><span class="sxs-lookup"><span data-stu-id="0c5be-116">About 20 bytes on average per class name.</span></span>        |
| <span data-ttu-id="0c5be-117">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="0c5be-117">Update Privilege</span></span>  | <span data-ttu-id="0c5be-118">Il valore verrà impostato dalla finestra di progettazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="0c5be-118">The designer of the object would set this value.</span></span> |
| <span data-ttu-id="0c5be-119">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="0c5be-119">Update Frequency</span></span>  | <span data-ttu-id="0c5be-120">Ogni volta che viene modificata la progettazione della classe.</span><span class="sxs-lookup"><span data-stu-id="0c5be-120">Whenever the design of the class changes.</span></span>        |
| <span data-ttu-id="0c5be-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="0c5be-121">Attribute-Id</span></span>      | <span data-ttu-id="0c5be-122">2.5.21.6</span><span class="sxs-lookup"><span data-stu-id="0c5be-122">2.5.21.6</span></span>                                         |
| <span data-ttu-id="0c5be-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="0c5be-123">System-Id-Guid</span></span>    | <span data-ttu-id="0c5be-124">9a7ad94b-ca53-11d1-bbd0-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="0c5be-124">9a7ad94b-ca53-11d1-bbd0-0080c76670c0</span></span>             |
| <span data-ttu-id="0c5be-125">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0c5be-125">Syntax</span></span>            | [<span data-ttu-id="0c5be-126">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="0c5be-126">**String(Unicode)**</span></span>](s-string-unicode.md)      |



## <a name="implementations"></a><span data-ttu-id="0c5be-127">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="0c5be-127">Implementations</span></span>

-   [<span data-ttu-id="0c5be-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="0c5be-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="0c5be-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="0c5be-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="0c5be-130">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="0c5be-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="0c5be-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="0c5be-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="0c5be-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="0c5be-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="0c5be-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="0c5be-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="0c5be-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="0c5be-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="0c5be-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0c5be-135">Windows 2000 Server</span></span>



| <span data-ttu-id="0c5be-136">Voce</span><span class="sxs-lookup"><span data-stu-id="0c5be-136">Entry</span></span> | <span data-ttu-id="0c5be-137">Valore</span><span class="sxs-lookup"><span data-stu-id="0c5be-137">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="0c5be-138">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="0c5be-138">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="0c5be-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0c5be-139">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="0c5be-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="0c5be-140">System-Only</span></span>            | <span data-ttu-id="0c5be-141">Vero</span><span class="sxs-lookup"><span data-stu-id="0c5be-141">True</span></span>                                        |
| <span data-ttu-id="0c5be-142">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="0c5be-142">Is-Single-Valued</span></span>       | <span data-ttu-id="0c5be-143">Falso</span><span class="sxs-lookup"><span data-stu-id="0c5be-143">False</span></span>                                       |
| <span data-ttu-id="0c5be-144">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="0c5be-144">Is Indexed</span></span>             | <span data-ttu-id="0c5be-145">Falso</span><span class="sxs-lookup"><span data-stu-id="0c5be-145">False</span></span>                                       |
| <span data-ttu-id="0c5be-146">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="0c5be-146">In Global Catalog</span></span>      | <span data-ttu-id="0c5be-147">Falso</span><span class="sxs-lookup"><span data-stu-id="0c5be-147">False</span></span>                                       |
| <span data-ttu-id="0c5be-148">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="0c5be-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="0c5be-149">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="0c5be-149">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="0c5be-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0c5be-150">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="0c5be-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0c5be-151">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="0c5be-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0c5be-152">Search-Flags</span></span>           | <span data-ttu-id="0c5be-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0c5be-153">0x00000000</span></span>                                  |
| <span data-ttu-id="0c5be-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0c5be-154">System-Flags</span></span>           | <span data-ttu-id="0c5be-155">0x08000014</span><span class="sxs-lookup"><span data-stu-id="0c5be-155">0x08000014</span></span>                                  |
| <span data-ttu-id="0c5be-156">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="0c5be-156">Classes used in</span></span>        | [<span data-ttu-id="0c5be-157">**Sottoschema**</span><span class="sxs-lookup"><span data-stu-id="0c5be-157">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="0c5be-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0c5be-158">Windows Server 2003</span></span>



| <span data-ttu-id="0c5be-159">Voce</span><span class="sxs-lookup"><span data-stu-id="0c5be-159">Entry</span></span> | <span data-ttu-id="0c5be-160">Valore</span><span class="sxs-lookup"><span data-stu-id="0c5be-160">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="0c5be-161">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="0c5be-161">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="0c5be-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0c5be-162">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="0c5be-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="0c5be-163">System-Only</span></span>            | <span data-ttu-id="0c5be-164">Vero</span><span class="sxs-lookup"><span data-stu-id="0c5be-164">True</span></span>                                        |
| <span data-ttu-id="0c5be-165">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="0c5be-165">Is-Single-Valued</span></span>       | <span data-ttu-id="0c5be-166">Falso</span><span class="sxs-lookup"><span data-stu-id="0c5be-166">False</span></span>                                       |
| <span data-ttu-id="0c5be-167">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="0c5be-167">Is Indexed</span></span>             | <span data-ttu-id="0c5be-168">Falso</span><span class="sxs-lookup"><span data-stu-id="0c5be-168">False</span></span>                                       |
| <span data-ttu-id="0c5be-169">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="0c5be-169">In Global Catalog</span></span>      | <span data-ttu-id="0c5be-170">Falso</span><span class="sxs-lookup"><span data-stu-id="0c5be-170">False</span></span>                                       |
| <span data-ttu-id="0c5be-171">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="0c5be-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="0c5be-172">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="0c5be-172">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="0c5be-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0c5be-173">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="0c5be-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0c5be-174">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="0c5be-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0c5be-175">Search-Flags</span></span>           | <span data-ttu-id="0c5be-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0c5be-176">0x00000000</span></span>                                  |
| <span data-ttu-id="0c5be-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0c5be-177">System-Flags</span></span>           | <span data-ttu-id="0c5be-178">0x08000014</span><span class="sxs-lookup"><span data-stu-id="0c5be-178">0x08000014</span></span>                                  |
| <span data-ttu-id="0c5be-179">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="0c5be-179">Classes used in</span></span>        | [<span data-ttu-id="0c5be-180">**Sottoschema**</span><span class="sxs-lookup"><span data-stu-id="0c5be-180">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="0c5be-181">ADAM</span><span class="sxs-lookup"><span data-stu-id="0c5be-181">ADAM</span></span>



| <span data-ttu-id="0c5be-182">Voce</span><span class="sxs-lookup"><span data-stu-id="0c5be-182">Entry</span></span> | <span data-ttu-id="0c5be-183">Valore</span><span class="sxs-lookup"><span data-stu-id="0c5be-183">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="0c5be-184">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="0c5be-184">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="0c5be-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0c5be-185">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="0c5be-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="0c5be-186">System-Only</span></span>            | <span data-ttu-id="0c5be-187">Vero</span><span class="sxs-lookup"><span data-stu-id="0c5be-187">True</span></span>                                        |
| <span data-ttu-id="0c5be-188">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="0c5be-188">Is-Single-Valued</span></span>       | <span data-ttu-id="0c5be-189">Falso</span><span class="sxs-lookup"><span data-stu-id="0c5be-189">False</span></span>                                       |
| <span data-ttu-id="0c5be-190">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="0c5be-190">Is Indexed</span></span>             | <span data-ttu-id="0c5be-191">Falso</span><span class="sxs-lookup"><span data-stu-id="0c5be-191">False</span></span>                                       |
| <span data-ttu-id="0c5be-192">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="0c5be-192">In Global Catalog</span></span>      | <span data-ttu-id="0c5be-193">Falso</span><span class="sxs-lookup"><span data-stu-id="0c5be-193">False</span></span>                                       |
| <span data-ttu-id="0c5be-194">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="0c5be-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="0c5be-195">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="0c5be-195">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="0c5be-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0c5be-196">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="0c5be-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0c5be-197">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="0c5be-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0c5be-198">Search-Flags</span></span>           | <span data-ttu-id="0c5be-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0c5be-199">0x00000000</span></span>                                  |
| <span data-ttu-id="0c5be-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0c5be-200">System-Flags</span></span>           | <span data-ttu-id="0c5be-201">0x08000014</span><span class="sxs-lookup"><span data-stu-id="0c5be-201">0x08000014</span></span>                                  |
| <span data-ttu-id="0c5be-202">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="0c5be-202">Classes used in</span></span>        | [<span data-ttu-id="0c5be-203">**Sottoschema**</span><span class="sxs-lookup"><span data-stu-id="0c5be-203">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="0c5be-204">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="0c5be-204">Windows Server 2003 R2</span></span>



| <span data-ttu-id="0c5be-205">Voce</span><span class="sxs-lookup"><span data-stu-id="0c5be-205">Entry</span></span> | <span data-ttu-id="0c5be-206">Valore</span><span class="sxs-lookup"><span data-stu-id="0c5be-206">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="0c5be-207">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="0c5be-207">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="0c5be-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0c5be-208">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="0c5be-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="0c5be-209">System-Only</span></span>            | <span data-ttu-id="0c5be-210">Vero</span><span class="sxs-lookup"><span data-stu-id="0c5be-210">True</span></span>                                        |
| <span data-ttu-id="0c5be-211">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="0c5be-211">Is-Single-Valued</span></span>       | <span data-ttu-id="0c5be-212">Falso</span><span class="sxs-lookup"><span data-stu-id="0c5be-212">False</span></span>                                       |
| <span data-ttu-id="0c5be-213">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="0c5be-213">Is Indexed</span></span>             | <span data-ttu-id="0c5be-214">Falso</span><span class="sxs-lookup"><span data-stu-id="0c5be-214">False</span></span>                                       |
| <span data-ttu-id="0c5be-215">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="0c5be-215">In Global Catalog</span></span>      | <span data-ttu-id="0c5be-216">Falso</span><span class="sxs-lookup"><span data-stu-id="0c5be-216">False</span></span>                                       |
| <span data-ttu-id="0c5be-217">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="0c5be-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="0c5be-218">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="0c5be-218">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="0c5be-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0c5be-219">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="0c5be-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0c5be-220">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="0c5be-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0c5be-221">Search-Flags</span></span>           | <span data-ttu-id="0c5be-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0c5be-222">0x00000000</span></span>                                  |
| <span data-ttu-id="0c5be-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0c5be-223">System-Flags</span></span>           | <span data-ttu-id="0c5be-224">0x08000014</span><span class="sxs-lookup"><span data-stu-id="0c5be-224">0x08000014</span></span>                                  |
| <span data-ttu-id="0c5be-225">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="0c5be-225">Classes used in</span></span>        | [<span data-ttu-id="0c5be-226">**Sottoschema**</span><span class="sxs-lookup"><span data-stu-id="0c5be-226">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="0c5be-227">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0c5be-227">Windows Server 2008</span></span>



| <span data-ttu-id="0c5be-228">Voce</span><span class="sxs-lookup"><span data-stu-id="0c5be-228">Entry</span></span> | <span data-ttu-id="0c5be-229">Valore</span><span class="sxs-lookup"><span data-stu-id="0c5be-229">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="0c5be-230">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="0c5be-230">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="0c5be-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0c5be-231">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="0c5be-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="0c5be-232">System-Only</span></span>            | <span data-ttu-id="0c5be-233">Vero</span><span class="sxs-lookup"><span data-stu-id="0c5be-233">True</span></span>                                        |
| <span data-ttu-id="0c5be-234">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="0c5be-234">Is-Single-Valued</span></span>       | <span data-ttu-id="0c5be-235">Falso</span><span class="sxs-lookup"><span data-stu-id="0c5be-235">False</span></span>                                       |
| <span data-ttu-id="0c5be-236">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="0c5be-236">Is Indexed</span></span>             | <span data-ttu-id="0c5be-237">Falso</span><span class="sxs-lookup"><span data-stu-id="0c5be-237">False</span></span>                                       |
| <span data-ttu-id="0c5be-238">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="0c5be-238">In Global Catalog</span></span>      | <span data-ttu-id="0c5be-239">Falso</span><span class="sxs-lookup"><span data-stu-id="0c5be-239">False</span></span>                                       |
| <span data-ttu-id="0c5be-240">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="0c5be-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="0c5be-241">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="0c5be-241">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="0c5be-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0c5be-242">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="0c5be-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0c5be-243">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="0c5be-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0c5be-244">Search-Flags</span></span>           | <span data-ttu-id="0c5be-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0c5be-245">0x00000000</span></span>                                  |
| <span data-ttu-id="0c5be-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0c5be-246">System-Flags</span></span>           | <span data-ttu-id="0c5be-247">0x08000014</span><span class="sxs-lookup"><span data-stu-id="0c5be-247">0x08000014</span></span>                                  |
| <span data-ttu-id="0c5be-248">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="0c5be-248">Classes used in</span></span>        | [<span data-ttu-id="0c5be-249">**Sottoschema**</span><span class="sxs-lookup"><span data-stu-id="0c5be-249">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="0c5be-250">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="0c5be-250">Windows Server 2008 R2</span></span>



| <span data-ttu-id="0c5be-251">Voce</span><span class="sxs-lookup"><span data-stu-id="0c5be-251">Entry</span></span> | <span data-ttu-id="0c5be-252">Valore</span><span class="sxs-lookup"><span data-stu-id="0c5be-252">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="0c5be-253">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="0c5be-253">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="0c5be-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0c5be-254">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="0c5be-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="0c5be-255">System-Only</span></span>            | <span data-ttu-id="0c5be-256">Vero</span><span class="sxs-lookup"><span data-stu-id="0c5be-256">True</span></span>                                        |
| <span data-ttu-id="0c5be-257">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="0c5be-257">Is-Single-Valued</span></span>       | <span data-ttu-id="0c5be-258">Falso</span><span class="sxs-lookup"><span data-stu-id="0c5be-258">False</span></span>                                       |
| <span data-ttu-id="0c5be-259">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="0c5be-259">Is Indexed</span></span>             | <span data-ttu-id="0c5be-260">Falso</span><span class="sxs-lookup"><span data-stu-id="0c5be-260">False</span></span>                                       |
| <span data-ttu-id="0c5be-261">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="0c5be-261">In Global Catalog</span></span>      | <span data-ttu-id="0c5be-262">Falso</span><span class="sxs-lookup"><span data-stu-id="0c5be-262">False</span></span>                                       |
| <span data-ttu-id="0c5be-263">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="0c5be-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="0c5be-264">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="0c5be-264">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="0c5be-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0c5be-265">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="0c5be-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0c5be-266">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="0c5be-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0c5be-267">Search-Flags</span></span>           | <span data-ttu-id="0c5be-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0c5be-268">0x00000000</span></span>                                  |
| <span data-ttu-id="0c5be-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0c5be-269">System-Flags</span></span>           | <span data-ttu-id="0c5be-270">0x08000014</span><span class="sxs-lookup"><span data-stu-id="0c5be-270">0x08000014</span></span>                                  |
| <span data-ttu-id="0c5be-271">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="0c5be-271">Classes used in</span></span>        | [<span data-ttu-id="0c5be-272">**Sottoschema**</span><span class="sxs-lookup"><span data-stu-id="0c5be-272">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="0c5be-273">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0c5be-273">Windows Server 2012</span></span>



| <span data-ttu-id="0c5be-274">Voce</span><span class="sxs-lookup"><span data-stu-id="0c5be-274">Entry</span></span> | <span data-ttu-id="0c5be-275">Valore</span><span class="sxs-lookup"><span data-stu-id="0c5be-275">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="0c5be-276">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="0c5be-276">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="0c5be-277">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0c5be-277">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="0c5be-278">System-Only</span><span class="sxs-lookup"><span data-stu-id="0c5be-278">System-Only</span></span>            | <span data-ttu-id="0c5be-279">Vero</span><span class="sxs-lookup"><span data-stu-id="0c5be-279">True</span></span>                                        |
| <span data-ttu-id="0c5be-280">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="0c5be-280">Is-Single-Valued</span></span>       | <span data-ttu-id="0c5be-281">Falso</span><span class="sxs-lookup"><span data-stu-id="0c5be-281">False</span></span>                                       |
| <span data-ttu-id="0c5be-282">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="0c5be-282">Is Indexed</span></span>             | <span data-ttu-id="0c5be-283">Falso</span><span class="sxs-lookup"><span data-stu-id="0c5be-283">False</span></span>                                       |
| <span data-ttu-id="0c5be-284">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="0c5be-284">In Global Catalog</span></span>      | <span data-ttu-id="0c5be-285">Falso</span><span class="sxs-lookup"><span data-stu-id="0c5be-285">False</span></span>                                       |
| <span data-ttu-id="0c5be-286">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="0c5be-286">NT-Security-Descriptor</span></span> | <span data-ttu-id="0c5be-287">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="0c5be-287">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="0c5be-288">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0c5be-288">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="0c5be-289">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0c5be-289">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="0c5be-290">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0c5be-290">Search-Flags</span></span>           | <span data-ttu-id="0c5be-291">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0c5be-291">0x00000000</span></span>                                  |
| <span data-ttu-id="0c5be-292">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0c5be-292">System-Flags</span></span>           | <span data-ttu-id="0c5be-293">0x08000014</span><span class="sxs-lookup"><span data-stu-id="0c5be-293">0x08000014</span></span>                                  |
| <span data-ttu-id="0c5be-294">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="0c5be-294">Classes used in</span></span>        | [<span data-ttu-id="0c5be-295">**Sottoschema**</span><span class="sxs-lookup"><span data-stu-id="0c5be-295">**SubSchema**</span></span>](c-subschema.md)<br/> |



 

 





