---
title: Extended-Class-info (attributo)
description: Proprietà multivalore che contiene stringhe che rappresentano informazioni aggiuntive per ogni classe. Ogni valore contiene governsID, lDAPDisplayName e schemaIDGUID della classe.
ms.assetid: f0f07950-28f8-4fe7-b030-1ab7632569e1
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo Extended-info Class
- Schema AD dell'attributo extendedClassInfo
topic_type:
- apiref
api_name:
- Extended-Class-Info
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f1b3320f547a3dbb41a151a33765cf9729e82c6
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104400970"
---
# <a name="extended-class-info-attribute"></a><span data-ttu-id="b5594-106">Extended-Class-info (attributo)</span><span class="sxs-lookup"><span data-stu-id="b5594-106">Extended-Class-Info attribute</span></span>

<span data-ttu-id="b5594-107">Proprietà multivalore che contiene stringhe che rappresentano informazioni aggiuntive per ogni classe.</span><span class="sxs-lookup"><span data-stu-id="b5594-107">A multi-valued property that contains strings that represent additional information for each class.</span></span> <span data-ttu-id="b5594-108">Ogni valore contiene governsID, lDAPDisplayName e schemaIDGUID della classe.</span><span class="sxs-lookup"><span data-stu-id="b5594-108">Each value contains the governsID, lDAPDisplayName, and schemaIDGUID of the class.</span></span>



| <span data-ttu-id="b5594-109">Voce</span><span class="sxs-lookup"><span data-stu-id="b5594-109">Entry</span></span> | <span data-ttu-id="b5594-110">Valore</span><span class="sxs-lookup"><span data-stu-id="b5594-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="b5594-111">CN</span><span class="sxs-lookup"><span data-stu-id="b5594-111">CN</span></span>                | <span data-ttu-id="b5594-112">Extended-Class-info</span><span class="sxs-lookup"><span data-stu-id="b5594-112">Extended-Class-Info</span></span>                         |
| <span data-ttu-id="b5594-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="b5594-113">Ldap-Display-Name</span></span> | <span data-ttu-id="b5594-114">extendedClassInfo</span><span class="sxs-lookup"><span data-stu-id="b5594-114">extendedClassInfo</span></span>                           |
| <span data-ttu-id="b5594-115">Dimensione</span><span class="sxs-lookup"><span data-stu-id="b5594-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="b5594-116">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="b5594-116">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="b5594-117">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="b5594-117">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="b5594-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b5594-118">Attribute-Id</span></span>      | <span data-ttu-id="b5594-119">1.2.840.113556.1.4.908</span><span class="sxs-lookup"><span data-stu-id="b5594-119">1.2.840.113556.1.4.908</span></span>                      |
| <span data-ttu-id="b5594-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="b5594-120">System-Id-Guid</span></span>    | <span data-ttu-id="b5594-121">9a7ad948-ca53-11d1-bbd0-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="b5594-121">9a7ad948-ca53-11d1-bbd0-0080c76670c0</span></span>        |
| <span data-ttu-id="b5594-122">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b5594-122">Syntax</span></span>            | [<span data-ttu-id="b5594-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="b5594-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="b5594-124">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="b5594-124">Implementations</span></span>

-   [<span data-ttu-id="b5594-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="b5594-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="b5594-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b5594-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b5594-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="b5594-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="b5594-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b5594-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b5594-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b5594-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b5594-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b5594-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b5594-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b5594-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="b5594-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b5594-132">Windows 2000 Server</span></span>



| <span data-ttu-id="b5594-133">Voce</span><span class="sxs-lookup"><span data-stu-id="b5594-133">Entry</span></span> | <span data-ttu-id="b5594-134">Valore</span><span class="sxs-lookup"><span data-stu-id="b5594-134">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="b5594-135">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="b5594-135">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="b5594-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b5594-136">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="b5594-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="b5594-137">System-Only</span></span>            | <span data-ttu-id="b5594-138">Vero</span><span class="sxs-lookup"><span data-stu-id="b5594-138">True</span></span>                                        |
| <span data-ttu-id="b5594-139">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="b5594-139">Is-Single-Valued</span></span>       | <span data-ttu-id="b5594-140">Falso</span><span class="sxs-lookup"><span data-stu-id="b5594-140">False</span></span>                                       |
| <span data-ttu-id="b5594-141">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="b5594-141">Is Indexed</span></span>             | <span data-ttu-id="b5594-142">Falso</span><span class="sxs-lookup"><span data-stu-id="b5594-142">False</span></span>                                       |
| <span data-ttu-id="b5594-143">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="b5594-143">In Global Catalog</span></span>      | <span data-ttu-id="b5594-144">Falso</span><span class="sxs-lookup"><span data-stu-id="b5594-144">False</span></span>                                       |
| <span data-ttu-id="b5594-145">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="b5594-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="b5594-146">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="b5594-146">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="b5594-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b5594-147">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="b5594-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b5594-148">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="b5594-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b5594-149">Search-Flags</span></span>           | <span data-ttu-id="b5594-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b5594-150">0x00000000</span></span>                                  |
| <span data-ttu-id="b5594-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b5594-151">System-Flags</span></span>           | <span data-ttu-id="b5594-152">0x08000014</span><span class="sxs-lookup"><span data-stu-id="b5594-152">0x08000014</span></span>                                  |
| <span data-ttu-id="b5594-153">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="b5594-153">Classes used in</span></span>        | [<span data-ttu-id="b5594-154">**Sottoschema**</span><span class="sxs-lookup"><span data-stu-id="b5594-154">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="b5594-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b5594-155">Windows Server 2003</span></span>



| <span data-ttu-id="b5594-156">Voce</span><span class="sxs-lookup"><span data-stu-id="b5594-156">Entry</span></span> | <span data-ttu-id="b5594-157">Valore</span><span class="sxs-lookup"><span data-stu-id="b5594-157">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="b5594-158">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="b5594-158">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="b5594-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b5594-159">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="b5594-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="b5594-160">System-Only</span></span>            | <span data-ttu-id="b5594-161">Vero</span><span class="sxs-lookup"><span data-stu-id="b5594-161">True</span></span>                                        |
| <span data-ttu-id="b5594-162">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="b5594-162">Is-Single-Valued</span></span>       | <span data-ttu-id="b5594-163">Falso</span><span class="sxs-lookup"><span data-stu-id="b5594-163">False</span></span>                                       |
| <span data-ttu-id="b5594-164">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="b5594-164">Is Indexed</span></span>             | <span data-ttu-id="b5594-165">Falso</span><span class="sxs-lookup"><span data-stu-id="b5594-165">False</span></span>                                       |
| <span data-ttu-id="b5594-166">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="b5594-166">In Global Catalog</span></span>      | <span data-ttu-id="b5594-167">Falso</span><span class="sxs-lookup"><span data-stu-id="b5594-167">False</span></span>                                       |
| <span data-ttu-id="b5594-168">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="b5594-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="b5594-169">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="b5594-169">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="b5594-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b5594-170">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="b5594-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b5594-171">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="b5594-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b5594-172">Search-Flags</span></span>           | <span data-ttu-id="b5594-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b5594-173">0x00000000</span></span>                                  |
| <span data-ttu-id="b5594-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b5594-174">System-Flags</span></span>           | <span data-ttu-id="b5594-175">0x08000014</span><span class="sxs-lookup"><span data-stu-id="b5594-175">0x08000014</span></span>                                  |
| <span data-ttu-id="b5594-176">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="b5594-176">Classes used in</span></span>        | [<span data-ttu-id="b5594-177">**Sottoschema**</span><span class="sxs-lookup"><span data-stu-id="b5594-177">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="b5594-178">ADAM</span><span class="sxs-lookup"><span data-stu-id="b5594-178">ADAM</span></span>



| <span data-ttu-id="b5594-179">Voce</span><span class="sxs-lookup"><span data-stu-id="b5594-179">Entry</span></span> | <span data-ttu-id="b5594-180">Valore</span><span class="sxs-lookup"><span data-stu-id="b5594-180">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="b5594-181">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="b5594-181">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="b5594-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b5594-182">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="b5594-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="b5594-183">System-Only</span></span>            | <span data-ttu-id="b5594-184">Vero</span><span class="sxs-lookup"><span data-stu-id="b5594-184">True</span></span>                                        |
| <span data-ttu-id="b5594-185">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="b5594-185">Is-Single-Valued</span></span>       | <span data-ttu-id="b5594-186">Falso</span><span class="sxs-lookup"><span data-stu-id="b5594-186">False</span></span>                                       |
| <span data-ttu-id="b5594-187">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="b5594-187">Is Indexed</span></span>             | <span data-ttu-id="b5594-188">Falso</span><span class="sxs-lookup"><span data-stu-id="b5594-188">False</span></span>                                       |
| <span data-ttu-id="b5594-189">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="b5594-189">In Global Catalog</span></span>      | <span data-ttu-id="b5594-190">Falso</span><span class="sxs-lookup"><span data-stu-id="b5594-190">False</span></span>                                       |
| <span data-ttu-id="b5594-191">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="b5594-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="b5594-192">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="b5594-192">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="b5594-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b5594-193">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="b5594-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b5594-194">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="b5594-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b5594-195">Search-Flags</span></span>           | <span data-ttu-id="b5594-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b5594-196">0x00000000</span></span>                                  |
| <span data-ttu-id="b5594-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b5594-197">System-Flags</span></span>           | <span data-ttu-id="b5594-198">0x08000014</span><span class="sxs-lookup"><span data-stu-id="b5594-198">0x08000014</span></span>                                  |
| <span data-ttu-id="b5594-199">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="b5594-199">Classes used in</span></span>        | [<span data-ttu-id="b5594-200">**Sottoschema**</span><span class="sxs-lookup"><span data-stu-id="b5594-200">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b5594-201">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b5594-201">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b5594-202">Voce</span><span class="sxs-lookup"><span data-stu-id="b5594-202">Entry</span></span> | <span data-ttu-id="b5594-203">Valore</span><span class="sxs-lookup"><span data-stu-id="b5594-203">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="b5594-204">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="b5594-204">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="b5594-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b5594-205">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="b5594-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="b5594-206">System-Only</span></span>            | <span data-ttu-id="b5594-207">Vero</span><span class="sxs-lookup"><span data-stu-id="b5594-207">True</span></span>                                        |
| <span data-ttu-id="b5594-208">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="b5594-208">Is-Single-Valued</span></span>       | <span data-ttu-id="b5594-209">Falso</span><span class="sxs-lookup"><span data-stu-id="b5594-209">False</span></span>                                       |
| <span data-ttu-id="b5594-210">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="b5594-210">Is Indexed</span></span>             | <span data-ttu-id="b5594-211">Falso</span><span class="sxs-lookup"><span data-stu-id="b5594-211">False</span></span>                                       |
| <span data-ttu-id="b5594-212">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="b5594-212">In Global Catalog</span></span>      | <span data-ttu-id="b5594-213">Falso</span><span class="sxs-lookup"><span data-stu-id="b5594-213">False</span></span>                                       |
| <span data-ttu-id="b5594-214">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="b5594-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="b5594-215">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="b5594-215">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="b5594-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b5594-216">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="b5594-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b5594-217">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="b5594-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b5594-218">Search-Flags</span></span>           | <span data-ttu-id="b5594-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b5594-219">0x00000000</span></span>                                  |
| <span data-ttu-id="b5594-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b5594-220">System-Flags</span></span>           | <span data-ttu-id="b5594-221">0x08000014</span><span class="sxs-lookup"><span data-stu-id="b5594-221">0x08000014</span></span>                                  |
| <span data-ttu-id="b5594-222">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="b5594-222">Classes used in</span></span>        | [<span data-ttu-id="b5594-223">**Sottoschema**</span><span class="sxs-lookup"><span data-stu-id="b5594-223">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b5594-224">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b5594-224">Windows Server 2008</span></span>



| <span data-ttu-id="b5594-225">Voce</span><span class="sxs-lookup"><span data-stu-id="b5594-225">Entry</span></span> | <span data-ttu-id="b5594-226">Valore</span><span class="sxs-lookup"><span data-stu-id="b5594-226">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="b5594-227">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="b5594-227">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="b5594-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b5594-228">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="b5594-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="b5594-229">System-Only</span></span>            | <span data-ttu-id="b5594-230">Vero</span><span class="sxs-lookup"><span data-stu-id="b5594-230">True</span></span>                                        |
| <span data-ttu-id="b5594-231">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="b5594-231">Is-Single-Valued</span></span>       | <span data-ttu-id="b5594-232">Falso</span><span class="sxs-lookup"><span data-stu-id="b5594-232">False</span></span>                                       |
| <span data-ttu-id="b5594-233">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="b5594-233">Is Indexed</span></span>             | <span data-ttu-id="b5594-234">Falso</span><span class="sxs-lookup"><span data-stu-id="b5594-234">False</span></span>                                       |
| <span data-ttu-id="b5594-235">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="b5594-235">In Global Catalog</span></span>      | <span data-ttu-id="b5594-236">Falso</span><span class="sxs-lookup"><span data-stu-id="b5594-236">False</span></span>                                       |
| <span data-ttu-id="b5594-237">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="b5594-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="b5594-238">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="b5594-238">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="b5594-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b5594-239">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="b5594-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b5594-240">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="b5594-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b5594-241">Search-Flags</span></span>           | <span data-ttu-id="b5594-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b5594-242">0x00000000</span></span>                                  |
| <span data-ttu-id="b5594-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b5594-243">System-Flags</span></span>           | <span data-ttu-id="b5594-244">0x08000014</span><span class="sxs-lookup"><span data-stu-id="b5594-244">0x08000014</span></span>                                  |
| <span data-ttu-id="b5594-245">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="b5594-245">Classes used in</span></span>        | [<span data-ttu-id="b5594-246">**Sottoschema**</span><span class="sxs-lookup"><span data-stu-id="b5594-246">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b5594-247">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b5594-247">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b5594-248">Voce</span><span class="sxs-lookup"><span data-stu-id="b5594-248">Entry</span></span> | <span data-ttu-id="b5594-249">Valore</span><span class="sxs-lookup"><span data-stu-id="b5594-249">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="b5594-250">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="b5594-250">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="b5594-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b5594-251">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="b5594-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="b5594-252">System-Only</span></span>            | <span data-ttu-id="b5594-253">Vero</span><span class="sxs-lookup"><span data-stu-id="b5594-253">True</span></span>                                        |
| <span data-ttu-id="b5594-254">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="b5594-254">Is-Single-Valued</span></span>       | <span data-ttu-id="b5594-255">Falso</span><span class="sxs-lookup"><span data-stu-id="b5594-255">False</span></span>                                       |
| <span data-ttu-id="b5594-256">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="b5594-256">Is Indexed</span></span>             | <span data-ttu-id="b5594-257">Falso</span><span class="sxs-lookup"><span data-stu-id="b5594-257">False</span></span>                                       |
| <span data-ttu-id="b5594-258">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="b5594-258">In Global Catalog</span></span>      | <span data-ttu-id="b5594-259">Falso</span><span class="sxs-lookup"><span data-stu-id="b5594-259">False</span></span>                                       |
| <span data-ttu-id="b5594-260">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="b5594-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="b5594-261">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="b5594-261">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="b5594-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b5594-262">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="b5594-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b5594-263">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="b5594-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b5594-264">Search-Flags</span></span>           | <span data-ttu-id="b5594-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b5594-265">0x00000000</span></span>                                  |
| <span data-ttu-id="b5594-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b5594-266">System-Flags</span></span>           | <span data-ttu-id="b5594-267">0x08000014</span><span class="sxs-lookup"><span data-stu-id="b5594-267">0x08000014</span></span>                                  |
| <span data-ttu-id="b5594-268">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="b5594-268">Classes used in</span></span>        | [<span data-ttu-id="b5594-269">**Sottoschema**</span><span class="sxs-lookup"><span data-stu-id="b5594-269">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b5594-270">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b5594-270">Windows Server 2012</span></span>



| <span data-ttu-id="b5594-271">Voce</span><span class="sxs-lookup"><span data-stu-id="b5594-271">Entry</span></span> | <span data-ttu-id="b5594-272">Valore</span><span class="sxs-lookup"><span data-stu-id="b5594-272">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="b5594-273">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="b5594-273">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="b5594-274">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b5594-274">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="b5594-275">System-Only</span><span class="sxs-lookup"><span data-stu-id="b5594-275">System-Only</span></span>            | <span data-ttu-id="b5594-276">Vero</span><span class="sxs-lookup"><span data-stu-id="b5594-276">True</span></span>                                        |
| <span data-ttu-id="b5594-277">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="b5594-277">Is-Single-Valued</span></span>       | <span data-ttu-id="b5594-278">Falso</span><span class="sxs-lookup"><span data-stu-id="b5594-278">False</span></span>                                       |
| <span data-ttu-id="b5594-279">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="b5594-279">Is Indexed</span></span>             | <span data-ttu-id="b5594-280">Falso</span><span class="sxs-lookup"><span data-stu-id="b5594-280">False</span></span>                                       |
| <span data-ttu-id="b5594-281">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="b5594-281">In Global Catalog</span></span>      | <span data-ttu-id="b5594-282">Falso</span><span class="sxs-lookup"><span data-stu-id="b5594-282">False</span></span>                                       |
| <span data-ttu-id="b5594-283">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="b5594-283">NT-Security-Descriptor</span></span> | <span data-ttu-id="b5594-284">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="b5594-284">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="b5594-285">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b5594-285">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="b5594-286">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b5594-286">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="b5594-287">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b5594-287">Search-Flags</span></span>           | <span data-ttu-id="b5594-288">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b5594-288">0x00000000</span></span>                                  |
| <span data-ttu-id="b5594-289">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b5594-289">System-Flags</span></span>           | <span data-ttu-id="b5594-290">0x08000014</span><span class="sxs-lookup"><span data-stu-id="b5594-290">0x08000014</span></span>                                  |
| <span data-ttu-id="b5594-291">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="b5594-291">Classes used in</span></span>        | [<span data-ttu-id="b5594-292">**Sottoschema**</span><span class="sxs-lookup"><span data-stu-id="b5594-292">**SubSchema**</span></span>](c-subschema.md)<br/> |



 

 





