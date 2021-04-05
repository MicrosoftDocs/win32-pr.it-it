---
title: Object-Class-Category-attributo
description: Questo attributo contiene il tipo di classe, ad esempio abstract, ausiliario o strutturato.
ms.assetid: 0698392d-991e-4a3c-b734-54d025a38d50
ms.tgt_platform: multiple
keywords:
- Oggetto-classe-schema AD attributo di categoria
- Schema AD dell'attributo objectClassCategory
topic_type:
- apiref
api_name:
- Object-Class-Category
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 397bb50e0af0c9dcddcc535d0bcddb1c8d525cfc
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103965208"
---
# <a name="object-class-category-attribute"></a><span data-ttu-id="008ea-105">Object-Class-Category-attributo</span><span class="sxs-lookup"><span data-stu-id="008ea-105">Object-Class-Category attribute</span></span>

<span data-ttu-id="008ea-106">Questo attributo contiene il tipo di classe, ad esempio abstract, ausiliario o strutturato.</span><span class="sxs-lookup"><span data-stu-id="008ea-106">This attribute contains the class type, such as abstract, auxiliary, or structured.</span></span>



| <span data-ttu-id="008ea-107">Voce</span><span class="sxs-lookup"><span data-stu-id="008ea-107">Entry</span></span> | <span data-ttu-id="008ea-108">Valore</span><span class="sxs-lookup"><span data-stu-id="008ea-108">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="008ea-109">CN</span><span class="sxs-lookup"><span data-stu-id="008ea-109">CN</span></span>                | <span data-ttu-id="008ea-110">Classe Object-Category</span><span class="sxs-lookup"><span data-stu-id="008ea-110">Object-Class-Category</span></span>                                                           |
| <span data-ttu-id="008ea-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="008ea-111">Ldap-Display-Name</span></span> | <span data-ttu-id="008ea-112">objectClassCategory</span><span class="sxs-lookup"><span data-stu-id="008ea-112">objectClassCategory</span></span>                                                             |
| <span data-ttu-id="008ea-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="008ea-113">Size</span></span>              | <span data-ttu-id="008ea-114">4 byte.</span><span class="sxs-lookup"><span data-stu-id="008ea-114">4 bytes.</span></span> <span data-ttu-id="008ea-115">Strutturale 1, abstract 2, ausiliario 3.</span><span class="sxs-lookup"><span data-stu-id="008ea-115">Structural 1, abstract 2, auxiliary 3.</span></span> <span data-ttu-id="008ea-116">Non usare la classe 88, 0.</span><span class="sxs-lookup"><span data-stu-id="008ea-116">Class 88, 0 should not be used.</span></span> |
| <span data-ttu-id="008ea-117">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="008ea-117">Update Privilege</span></span>  | <span data-ttu-id="008ea-118">Il valore verrà impostato dalla finestra di progettazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="008ea-118">The designer of the object would set this value.</span></span>                                |
| <span data-ttu-id="008ea-119">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="008ea-119">Update Frequency</span></span>  | <span data-ttu-id="008ea-120">Questo valore non deve mai cambiare.</span><span class="sxs-lookup"><span data-stu-id="008ea-120">This value should never change.</span></span>                                                 |
| <span data-ttu-id="008ea-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="008ea-121">Attribute-Id</span></span>      | <span data-ttu-id="008ea-122">1.2.840.113556.1.2.370</span><span class="sxs-lookup"><span data-stu-id="008ea-122">1.2.840.113556.1.2.370</span></span>                                                          |
| <span data-ttu-id="008ea-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="008ea-123">System-Id-Guid</span></span>    | <span data-ttu-id="008ea-124">bf9679e6-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="008ea-124">bf9679e6-0de6-11d0-a285-00aa003049e2</span></span>                                            |
| <span data-ttu-id="008ea-125">Sintassi</span><span class="sxs-lookup"><span data-stu-id="008ea-125">Syntax</span></span>            | [<span data-ttu-id="008ea-126">**Enumerazione**</span><span class="sxs-lookup"><span data-stu-id="008ea-126">**Enumeration**</span></span>](s-enumeration.md)                                            |



## <a name="implementations"></a><span data-ttu-id="008ea-127">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="008ea-127">Implementations</span></span>

-   [<span data-ttu-id="008ea-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="008ea-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="008ea-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="008ea-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="008ea-130">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="008ea-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="008ea-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="008ea-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="008ea-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="008ea-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="008ea-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="008ea-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="008ea-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="008ea-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="008ea-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="008ea-135">Windows 2000 Server</span></span>



| <span data-ttu-id="008ea-136">Voce</span><span class="sxs-lookup"><span data-stu-id="008ea-136">Entry</span></span> | <span data-ttu-id="008ea-137">Valore</span><span class="sxs-lookup"><span data-stu-id="008ea-137">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="008ea-138">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="008ea-138">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="008ea-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="008ea-139">MAPI-Id</span></span>                | <span data-ttu-id="008ea-140">0x80F6</span><span class="sxs-lookup"><span data-stu-id="008ea-140">0x80F6</span></span>                                           |
| <span data-ttu-id="008ea-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="008ea-141">System-Only</span></span>            | <span data-ttu-id="008ea-142">Vero</span><span class="sxs-lookup"><span data-stu-id="008ea-142">True</span></span>                                             |
| <span data-ttu-id="008ea-143">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="008ea-143">Is-Single-Valued</span></span>       | <span data-ttu-id="008ea-144">Vero</span><span class="sxs-lookup"><span data-stu-id="008ea-144">True</span></span>                                             |
| <span data-ttu-id="008ea-145">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="008ea-145">Is Indexed</span></span>             | <span data-ttu-id="008ea-146">Falso</span><span class="sxs-lookup"><span data-stu-id="008ea-146">False</span></span>                                            |
| <span data-ttu-id="008ea-147">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="008ea-147">In Global Catalog</span></span>      | <span data-ttu-id="008ea-148">Falso</span><span class="sxs-lookup"><span data-stu-id="008ea-148">False</span></span>                                            |
| <span data-ttu-id="008ea-149">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="008ea-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="008ea-150">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="008ea-150">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="008ea-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="008ea-151">Range-Lower</span></span>            | <span data-ttu-id="008ea-152">0</span><span class="sxs-lookup"><span data-stu-id="008ea-152">0</span></span>                                                |
| <span data-ttu-id="008ea-153">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="008ea-153">Range-Upper</span></span>            | <span data-ttu-id="008ea-154">3</span><span class="sxs-lookup"><span data-stu-id="008ea-154">3</span></span>                                                |
| <span data-ttu-id="008ea-155">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="008ea-155">Search-Flags</span></span>           | <span data-ttu-id="008ea-156">0x00000000</span><span class="sxs-lookup"><span data-stu-id="008ea-156">0x00000000</span></span>                                       |
| <span data-ttu-id="008ea-157">System-Flags</span><span class="sxs-lookup"><span data-stu-id="008ea-157">System-Flags</span></span>           | <span data-ttu-id="008ea-158">0x00000010</span><span class="sxs-lookup"><span data-stu-id="008ea-158">0x00000010</span></span>                                       |
| <span data-ttu-id="008ea-159">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="008ea-159">Classes used in</span></span>        | [<span data-ttu-id="008ea-160">**Classe-schema**</span><span class="sxs-lookup"><span data-stu-id="008ea-160">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="008ea-161">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="008ea-161">Windows Server 2003</span></span>



| <span data-ttu-id="008ea-162">Voce</span><span class="sxs-lookup"><span data-stu-id="008ea-162">Entry</span></span> | <span data-ttu-id="008ea-163">Valore</span><span class="sxs-lookup"><span data-stu-id="008ea-163">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="008ea-164">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="008ea-164">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="008ea-165">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="008ea-165">MAPI-Id</span></span>                | <span data-ttu-id="008ea-166">0x80F6</span><span class="sxs-lookup"><span data-stu-id="008ea-166">0x80F6</span></span>                                           |
| <span data-ttu-id="008ea-167">System-Only</span><span class="sxs-lookup"><span data-stu-id="008ea-167">System-Only</span></span>            | <span data-ttu-id="008ea-168">Vero</span><span class="sxs-lookup"><span data-stu-id="008ea-168">True</span></span>                                             |
| <span data-ttu-id="008ea-169">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="008ea-169">Is-Single-Valued</span></span>       | <span data-ttu-id="008ea-170">Vero</span><span class="sxs-lookup"><span data-stu-id="008ea-170">True</span></span>                                             |
| <span data-ttu-id="008ea-171">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="008ea-171">Is Indexed</span></span>             | <span data-ttu-id="008ea-172">Falso</span><span class="sxs-lookup"><span data-stu-id="008ea-172">False</span></span>                                            |
| <span data-ttu-id="008ea-173">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="008ea-173">In Global Catalog</span></span>      | <span data-ttu-id="008ea-174">Falso</span><span class="sxs-lookup"><span data-stu-id="008ea-174">False</span></span>                                            |
| <span data-ttu-id="008ea-175">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="008ea-175">NT-Security-Descriptor</span></span> | <span data-ttu-id="008ea-176">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="008ea-176">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="008ea-177">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="008ea-177">Range-Lower</span></span>            | <span data-ttu-id="008ea-178">0</span><span class="sxs-lookup"><span data-stu-id="008ea-178">0</span></span>                                                |
| <span data-ttu-id="008ea-179">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="008ea-179">Range-Upper</span></span>            | <span data-ttu-id="008ea-180">3</span><span class="sxs-lookup"><span data-stu-id="008ea-180">3</span></span>                                                |
| <span data-ttu-id="008ea-181">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="008ea-181">Search-Flags</span></span>           | <span data-ttu-id="008ea-182">0x00000000</span><span class="sxs-lookup"><span data-stu-id="008ea-182">0x00000000</span></span>                                       |
| <span data-ttu-id="008ea-183">System-Flags</span><span class="sxs-lookup"><span data-stu-id="008ea-183">System-Flags</span></span>           | <span data-ttu-id="008ea-184">0x00000010</span><span class="sxs-lookup"><span data-stu-id="008ea-184">0x00000010</span></span>                                       |
| <span data-ttu-id="008ea-185">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="008ea-185">Classes used in</span></span>        | [<span data-ttu-id="008ea-186">**Classe-schema**</span><span class="sxs-lookup"><span data-stu-id="008ea-186">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="008ea-187">ADAM</span><span class="sxs-lookup"><span data-stu-id="008ea-187">ADAM</span></span>



| <span data-ttu-id="008ea-188">Voce</span><span class="sxs-lookup"><span data-stu-id="008ea-188">Entry</span></span> | <span data-ttu-id="008ea-189">Valore</span><span class="sxs-lookup"><span data-stu-id="008ea-189">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="008ea-190">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="008ea-190">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="008ea-191">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="008ea-191">MAPI-Id</span></span>                | <span data-ttu-id="008ea-192">0x80F6</span><span class="sxs-lookup"><span data-stu-id="008ea-192">0x80F6</span></span>                                           |
| <span data-ttu-id="008ea-193">System-Only</span><span class="sxs-lookup"><span data-stu-id="008ea-193">System-Only</span></span>            | <span data-ttu-id="008ea-194">Vero</span><span class="sxs-lookup"><span data-stu-id="008ea-194">True</span></span>                                             |
| <span data-ttu-id="008ea-195">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="008ea-195">Is-Single-Valued</span></span>       | <span data-ttu-id="008ea-196">Vero</span><span class="sxs-lookup"><span data-stu-id="008ea-196">True</span></span>                                             |
| <span data-ttu-id="008ea-197">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="008ea-197">Is Indexed</span></span>             | <span data-ttu-id="008ea-198">Falso</span><span class="sxs-lookup"><span data-stu-id="008ea-198">False</span></span>                                            |
| <span data-ttu-id="008ea-199">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="008ea-199">In Global Catalog</span></span>      | <span data-ttu-id="008ea-200">Falso</span><span class="sxs-lookup"><span data-stu-id="008ea-200">False</span></span>                                            |
| <span data-ttu-id="008ea-201">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="008ea-201">NT-Security-Descriptor</span></span> | <span data-ttu-id="008ea-202">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="008ea-202">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="008ea-203">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="008ea-203">Range-Lower</span></span>            | <span data-ttu-id="008ea-204">0</span><span class="sxs-lookup"><span data-stu-id="008ea-204">0</span></span>                                                |
| <span data-ttu-id="008ea-205">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="008ea-205">Range-Upper</span></span>            | <span data-ttu-id="008ea-206">3</span><span class="sxs-lookup"><span data-stu-id="008ea-206">3</span></span>                                                |
| <span data-ttu-id="008ea-207">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="008ea-207">Search-Flags</span></span>           | <span data-ttu-id="008ea-208">0x00000000</span><span class="sxs-lookup"><span data-stu-id="008ea-208">0x00000000</span></span>                                       |
| <span data-ttu-id="008ea-209">System-Flags</span><span class="sxs-lookup"><span data-stu-id="008ea-209">System-Flags</span></span>           | <span data-ttu-id="008ea-210">0x00000010</span><span class="sxs-lookup"><span data-stu-id="008ea-210">0x00000010</span></span>                                       |
| <span data-ttu-id="008ea-211">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="008ea-211">Classes used in</span></span>        | [<span data-ttu-id="008ea-212">**Classe-schema**</span><span class="sxs-lookup"><span data-stu-id="008ea-212">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="008ea-213">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="008ea-213">Windows Server 2003 R2</span></span>



| <span data-ttu-id="008ea-214">Voce</span><span class="sxs-lookup"><span data-stu-id="008ea-214">Entry</span></span> | <span data-ttu-id="008ea-215">Valore</span><span class="sxs-lookup"><span data-stu-id="008ea-215">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="008ea-216">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="008ea-216">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="008ea-217">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="008ea-217">MAPI-Id</span></span>                | <span data-ttu-id="008ea-218">0x80F6</span><span class="sxs-lookup"><span data-stu-id="008ea-218">0x80F6</span></span>                                           |
| <span data-ttu-id="008ea-219">System-Only</span><span class="sxs-lookup"><span data-stu-id="008ea-219">System-Only</span></span>            | <span data-ttu-id="008ea-220">Vero</span><span class="sxs-lookup"><span data-stu-id="008ea-220">True</span></span>                                             |
| <span data-ttu-id="008ea-221">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="008ea-221">Is-Single-Valued</span></span>       | <span data-ttu-id="008ea-222">Vero</span><span class="sxs-lookup"><span data-stu-id="008ea-222">True</span></span>                                             |
| <span data-ttu-id="008ea-223">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="008ea-223">Is Indexed</span></span>             | <span data-ttu-id="008ea-224">Falso</span><span class="sxs-lookup"><span data-stu-id="008ea-224">False</span></span>                                            |
| <span data-ttu-id="008ea-225">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="008ea-225">In Global Catalog</span></span>      | <span data-ttu-id="008ea-226">Falso</span><span class="sxs-lookup"><span data-stu-id="008ea-226">False</span></span>                                            |
| <span data-ttu-id="008ea-227">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="008ea-227">NT-Security-Descriptor</span></span> | <span data-ttu-id="008ea-228">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="008ea-228">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="008ea-229">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="008ea-229">Range-Lower</span></span>            | <span data-ttu-id="008ea-230">0</span><span class="sxs-lookup"><span data-stu-id="008ea-230">0</span></span>                                                |
| <span data-ttu-id="008ea-231">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="008ea-231">Range-Upper</span></span>            | <span data-ttu-id="008ea-232">3</span><span class="sxs-lookup"><span data-stu-id="008ea-232">3</span></span>                                                |
| <span data-ttu-id="008ea-233">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="008ea-233">Search-Flags</span></span>           | <span data-ttu-id="008ea-234">0x00000000</span><span class="sxs-lookup"><span data-stu-id="008ea-234">0x00000000</span></span>                                       |
| <span data-ttu-id="008ea-235">System-Flags</span><span class="sxs-lookup"><span data-stu-id="008ea-235">System-Flags</span></span>           | <span data-ttu-id="008ea-236">0x00000010</span><span class="sxs-lookup"><span data-stu-id="008ea-236">0x00000010</span></span>                                       |
| <span data-ttu-id="008ea-237">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="008ea-237">Classes used in</span></span>        | [<span data-ttu-id="008ea-238">**Classe-schema**</span><span class="sxs-lookup"><span data-stu-id="008ea-238">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="008ea-239">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="008ea-239">Windows Server 2008</span></span>



| <span data-ttu-id="008ea-240">Voce</span><span class="sxs-lookup"><span data-stu-id="008ea-240">Entry</span></span> | <span data-ttu-id="008ea-241">Valore</span><span class="sxs-lookup"><span data-stu-id="008ea-241">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="008ea-242">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="008ea-242">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="008ea-243">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="008ea-243">MAPI-Id</span></span>                | <span data-ttu-id="008ea-244">0x80F6</span><span class="sxs-lookup"><span data-stu-id="008ea-244">0x80F6</span></span>                                           |
| <span data-ttu-id="008ea-245">System-Only</span><span class="sxs-lookup"><span data-stu-id="008ea-245">System-Only</span></span>            | <span data-ttu-id="008ea-246">Vero</span><span class="sxs-lookup"><span data-stu-id="008ea-246">True</span></span>                                             |
| <span data-ttu-id="008ea-247">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="008ea-247">Is-Single-Valued</span></span>       | <span data-ttu-id="008ea-248">Vero</span><span class="sxs-lookup"><span data-stu-id="008ea-248">True</span></span>                                             |
| <span data-ttu-id="008ea-249">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="008ea-249">Is Indexed</span></span>             | <span data-ttu-id="008ea-250">Falso</span><span class="sxs-lookup"><span data-stu-id="008ea-250">False</span></span>                                            |
| <span data-ttu-id="008ea-251">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="008ea-251">In Global Catalog</span></span>      | <span data-ttu-id="008ea-252">Falso</span><span class="sxs-lookup"><span data-stu-id="008ea-252">False</span></span>                                            |
| <span data-ttu-id="008ea-253">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="008ea-253">NT-Security-Descriptor</span></span> | <span data-ttu-id="008ea-254">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="008ea-254">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="008ea-255">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="008ea-255">Range-Lower</span></span>            | <span data-ttu-id="008ea-256">0</span><span class="sxs-lookup"><span data-stu-id="008ea-256">0</span></span>                                                |
| <span data-ttu-id="008ea-257">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="008ea-257">Range-Upper</span></span>            | <span data-ttu-id="008ea-258">3</span><span class="sxs-lookup"><span data-stu-id="008ea-258">3</span></span>                                                |
| <span data-ttu-id="008ea-259">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="008ea-259">Search-Flags</span></span>           | <span data-ttu-id="008ea-260">0x00000000</span><span class="sxs-lookup"><span data-stu-id="008ea-260">0x00000000</span></span>                                       |
| <span data-ttu-id="008ea-261">System-Flags</span><span class="sxs-lookup"><span data-stu-id="008ea-261">System-Flags</span></span>           | <span data-ttu-id="008ea-262">0x00000010</span><span class="sxs-lookup"><span data-stu-id="008ea-262">0x00000010</span></span>                                       |
| <span data-ttu-id="008ea-263">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="008ea-263">Classes used in</span></span>        | [<span data-ttu-id="008ea-264">**Classe-schema**</span><span class="sxs-lookup"><span data-stu-id="008ea-264">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="008ea-265">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="008ea-265">Windows Server 2008 R2</span></span>



| <span data-ttu-id="008ea-266">Voce</span><span class="sxs-lookup"><span data-stu-id="008ea-266">Entry</span></span> | <span data-ttu-id="008ea-267">Valore</span><span class="sxs-lookup"><span data-stu-id="008ea-267">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="008ea-268">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="008ea-268">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="008ea-269">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="008ea-269">MAPI-Id</span></span>                | <span data-ttu-id="008ea-270">0x80F6</span><span class="sxs-lookup"><span data-stu-id="008ea-270">0x80F6</span></span>                                           |
| <span data-ttu-id="008ea-271">System-Only</span><span class="sxs-lookup"><span data-stu-id="008ea-271">System-Only</span></span>            | <span data-ttu-id="008ea-272">Vero</span><span class="sxs-lookup"><span data-stu-id="008ea-272">True</span></span>                                             |
| <span data-ttu-id="008ea-273">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="008ea-273">Is-Single-Valued</span></span>       | <span data-ttu-id="008ea-274">Vero</span><span class="sxs-lookup"><span data-stu-id="008ea-274">True</span></span>                                             |
| <span data-ttu-id="008ea-275">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="008ea-275">Is Indexed</span></span>             | <span data-ttu-id="008ea-276">Falso</span><span class="sxs-lookup"><span data-stu-id="008ea-276">False</span></span>                                            |
| <span data-ttu-id="008ea-277">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="008ea-277">In Global Catalog</span></span>      | <span data-ttu-id="008ea-278">Falso</span><span class="sxs-lookup"><span data-stu-id="008ea-278">False</span></span>                                            |
| <span data-ttu-id="008ea-279">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="008ea-279">NT-Security-Descriptor</span></span> | <span data-ttu-id="008ea-280">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="008ea-280">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="008ea-281">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="008ea-281">Range-Lower</span></span>            | <span data-ttu-id="008ea-282">0</span><span class="sxs-lookup"><span data-stu-id="008ea-282">0</span></span>                                                |
| <span data-ttu-id="008ea-283">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="008ea-283">Range-Upper</span></span>            | <span data-ttu-id="008ea-284">3</span><span class="sxs-lookup"><span data-stu-id="008ea-284">3</span></span>                                                |
| <span data-ttu-id="008ea-285">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="008ea-285">Search-Flags</span></span>           | <span data-ttu-id="008ea-286">0x00000000</span><span class="sxs-lookup"><span data-stu-id="008ea-286">0x00000000</span></span>                                       |
| <span data-ttu-id="008ea-287">System-Flags</span><span class="sxs-lookup"><span data-stu-id="008ea-287">System-Flags</span></span>           | <span data-ttu-id="008ea-288">0x00000010</span><span class="sxs-lookup"><span data-stu-id="008ea-288">0x00000010</span></span>                                       |
| <span data-ttu-id="008ea-289">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="008ea-289">Classes used in</span></span>        | [<span data-ttu-id="008ea-290">**Classe-schema**</span><span class="sxs-lookup"><span data-stu-id="008ea-290">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="008ea-291">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="008ea-291">Windows Server 2012</span></span>



| <span data-ttu-id="008ea-292">Voce</span><span class="sxs-lookup"><span data-stu-id="008ea-292">Entry</span></span> | <span data-ttu-id="008ea-293">Valore</span><span class="sxs-lookup"><span data-stu-id="008ea-293">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="008ea-294">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="008ea-294">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="008ea-295">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="008ea-295">MAPI-Id</span></span>                | <span data-ttu-id="008ea-296">0x80F6</span><span class="sxs-lookup"><span data-stu-id="008ea-296">0x80F6</span></span>                                           |
| <span data-ttu-id="008ea-297">System-Only</span><span class="sxs-lookup"><span data-stu-id="008ea-297">System-Only</span></span>            | <span data-ttu-id="008ea-298">Vero</span><span class="sxs-lookup"><span data-stu-id="008ea-298">True</span></span>                                             |
| <span data-ttu-id="008ea-299">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="008ea-299">Is-Single-Valued</span></span>       | <span data-ttu-id="008ea-300">Vero</span><span class="sxs-lookup"><span data-stu-id="008ea-300">True</span></span>                                             |
| <span data-ttu-id="008ea-301">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="008ea-301">Is Indexed</span></span>             | <span data-ttu-id="008ea-302">Falso</span><span class="sxs-lookup"><span data-stu-id="008ea-302">False</span></span>                                            |
| <span data-ttu-id="008ea-303">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="008ea-303">In Global Catalog</span></span>      | <span data-ttu-id="008ea-304">Falso</span><span class="sxs-lookup"><span data-stu-id="008ea-304">False</span></span>                                            |
| <span data-ttu-id="008ea-305">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="008ea-305">NT-Security-Descriptor</span></span> | <span data-ttu-id="008ea-306">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="008ea-306">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="008ea-307">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="008ea-307">Range-Lower</span></span>            | <span data-ttu-id="008ea-308">0</span><span class="sxs-lookup"><span data-stu-id="008ea-308">0</span></span>                                                |
| <span data-ttu-id="008ea-309">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="008ea-309">Range-Upper</span></span>            | <span data-ttu-id="008ea-310">3</span><span class="sxs-lookup"><span data-stu-id="008ea-310">3</span></span>                                                |
| <span data-ttu-id="008ea-311">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="008ea-311">Search-Flags</span></span>           | <span data-ttu-id="008ea-312">0x00000000</span><span class="sxs-lookup"><span data-stu-id="008ea-312">0x00000000</span></span>                                       |
| <span data-ttu-id="008ea-313">System-Flags</span><span class="sxs-lookup"><span data-stu-id="008ea-313">System-Flags</span></span>           | <span data-ttu-id="008ea-314">0x00000010</span><span class="sxs-lookup"><span data-stu-id="008ea-314">0x00000010</span></span>                                       |
| <span data-ttu-id="008ea-315">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="008ea-315">Classes used in</span></span>        | [<span data-ttu-id="008ea-316">**Classe-schema**</span><span class="sxs-lookup"><span data-stu-id="008ea-316">**Class-Schema**</span></span>](c-classschema.md)<br/> |



 

 





