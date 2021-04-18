---
title: Attributo Search-Flags
description: Contiene un set di flag che specificano le informazioni di ricerca e di indicizzazione per un attributo.
ms.assetid: 55fc4398-25d2-466a-9aa9-fa375d827023
ms.tgt_platform: multiple
keywords:
- Schema AD Search-Flags attribute
- Schema AD dell'attributo searchFlags
topic_type:
- apiref
api_name:
- Search-Flags
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86f615464aa0aed69dd9590f668e37ec8c789c88
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "106303364"
---
# <a name="search-flags-attribute"></a><span data-ttu-id="bed4f-105">Attributo Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bed4f-105">Search-Flags attribute</span></span>

<span data-ttu-id="bed4f-106">Contiene un set di flag che specificano le informazioni di ricerca e di indicizzazione per un attributo.</span><span class="sxs-lookup"><span data-stu-id="bed4f-106">Contains a set of flags that specify search and indexing information for an attribute.</span></span> <span data-ttu-id="bed4f-107">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="bed4f-107">See Remarks.</span></span>



| <span data-ttu-id="bed4f-108">Voce</span><span class="sxs-lookup"><span data-stu-id="bed4f-108">Entry</span></span> | <span data-ttu-id="bed4f-109">Valore</span><span class="sxs-lookup"><span data-stu-id="bed4f-109">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="bed4f-110">CN</span><span class="sxs-lookup"><span data-stu-id="bed4f-110">CN</span></span>                | <span data-ttu-id="bed4f-111">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bed4f-111">Search-Flags</span></span>                         |
| <span data-ttu-id="bed4f-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="bed4f-112">Ldap-Display-Name</span></span> | <span data-ttu-id="bed4f-113">searchFlags</span><span class="sxs-lookup"><span data-stu-id="bed4f-113">searchFlags</span></span>                          |
| <span data-ttu-id="bed4f-114">Dimensione</span><span class="sxs-lookup"><span data-stu-id="bed4f-114">Size</span></span>              | \-                                   |
| <span data-ttu-id="bed4f-115">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="bed4f-115">Update Privilege</span></span>  | <span data-ttu-id="bed4f-116">Amministratore schema</span><span class="sxs-lookup"><span data-stu-id="bed4f-116">Schema administrator</span></span>                 |
| <span data-ttu-id="bed4f-117">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="bed4f-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="bed4f-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="bed4f-118">Attribute-Id</span></span>      | <span data-ttu-id="bed4f-119">1.2.840.113556.1.2.334</span><span class="sxs-lookup"><span data-stu-id="bed4f-119">1.2.840.113556.1.2.334</span></span>               |
| <span data-ttu-id="bed4f-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="bed4f-120">System-Id-Guid</span></span>    | <span data-ttu-id="bed4f-121">bf967a2d-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="bed4f-121">bf967a2d-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="bed4f-122">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bed4f-122">Syntax</span></span>            | [<span data-ttu-id="bed4f-123">**Enumerazione**</span><span class="sxs-lookup"><span data-stu-id="bed4f-123">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="bed4f-124">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="bed4f-124">Implementations</span></span>

-   [<span data-ttu-id="bed4f-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="bed4f-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="bed4f-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="bed4f-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="bed4f-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="bed4f-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="bed4f-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="bed4f-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="bed4f-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="bed4f-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="bed4f-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="bed4f-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="bed4f-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="bed4f-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="bed4f-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="bed4f-132">Windows 2000 Server</span></span>



| <span data-ttu-id="bed4f-133">Voce</span><span class="sxs-lookup"><span data-stu-id="bed4f-133">Entry</span></span> | <span data-ttu-id="bed4f-134">Valore</span><span class="sxs-lookup"><span data-stu-id="bed4f-134">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="bed4f-135">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="bed4f-135">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="bed4f-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bed4f-136">MAPI-Id</span></span>                | <span data-ttu-id="bed4f-137">0x812D</span><span class="sxs-lookup"><span data-stu-id="bed4f-137">0x812D</span></span>                                                   |
| <span data-ttu-id="bed4f-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="bed4f-138">System-Only</span></span>            | <span data-ttu-id="bed4f-139">Falso</span><span class="sxs-lookup"><span data-stu-id="bed4f-139">False</span></span>                                                    |
| <span data-ttu-id="bed4f-140">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="bed4f-140">Is-Single-Valued</span></span>       | <span data-ttu-id="bed4f-141">Vero</span><span class="sxs-lookup"><span data-stu-id="bed4f-141">True</span></span>                                                     |
| <span data-ttu-id="bed4f-142">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="bed4f-142">Is Indexed</span></span>             | <span data-ttu-id="bed4f-143">Falso</span><span class="sxs-lookup"><span data-stu-id="bed4f-143">False</span></span>                                                    |
| <span data-ttu-id="bed4f-144">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="bed4f-144">In Global Catalog</span></span>      | <span data-ttu-id="bed4f-145">Falso</span><span class="sxs-lookup"><span data-stu-id="bed4f-145">False</span></span>                                                    |
| <span data-ttu-id="bed4f-146">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="bed4f-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="bed4f-147">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="bed4f-147">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="bed4f-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bed4f-148">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="bed4f-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bed4f-149">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="bed4f-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bed4f-150">Search-Flags</span></span>           | <span data-ttu-id="bed4f-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bed4f-151">0x00000000</span></span>                                               |
| <span data-ttu-id="bed4f-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bed4f-152">System-Flags</span></span>           | <span data-ttu-id="bed4f-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bed4f-153">0x00000010</span></span>                                               |
| <span data-ttu-id="bed4f-154">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="bed4f-154">Classes used in</span></span>        | [<span data-ttu-id="bed4f-155">**Attribute-schema**</span><span class="sxs-lookup"><span data-stu-id="bed4f-155">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="bed4f-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="bed4f-156">Windows Server 2003</span></span>



| <span data-ttu-id="bed4f-157">Voce</span><span class="sxs-lookup"><span data-stu-id="bed4f-157">Entry</span></span> | <span data-ttu-id="bed4f-158">Valore</span><span class="sxs-lookup"><span data-stu-id="bed4f-158">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="bed4f-159">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="bed4f-159">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="bed4f-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bed4f-160">MAPI-Id</span></span>                | <span data-ttu-id="bed4f-161">0x812D</span><span class="sxs-lookup"><span data-stu-id="bed4f-161">0x812D</span></span>                                                   |
| <span data-ttu-id="bed4f-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="bed4f-162">System-Only</span></span>            | <span data-ttu-id="bed4f-163">Falso</span><span class="sxs-lookup"><span data-stu-id="bed4f-163">False</span></span>                                                    |
| <span data-ttu-id="bed4f-164">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="bed4f-164">Is-Single-Valued</span></span>       | <span data-ttu-id="bed4f-165">Vero</span><span class="sxs-lookup"><span data-stu-id="bed4f-165">True</span></span>                                                     |
| <span data-ttu-id="bed4f-166">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="bed4f-166">Is Indexed</span></span>             | <span data-ttu-id="bed4f-167">Falso</span><span class="sxs-lookup"><span data-stu-id="bed4f-167">False</span></span>                                                    |
| <span data-ttu-id="bed4f-168">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="bed4f-168">In Global Catalog</span></span>      | <span data-ttu-id="bed4f-169">Falso</span><span class="sxs-lookup"><span data-stu-id="bed4f-169">False</span></span>                                                    |
| <span data-ttu-id="bed4f-170">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="bed4f-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="bed4f-171">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="bed4f-171">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="bed4f-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bed4f-172">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="bed4f-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bed4f-173">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="bed4f-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bed4f-174">Search-Flags</span></span>           | <span data-ttu-id="bed4f-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bed4f-175">0x00000000</span></span>                                               |
| <span data-ttu-id="bed4f-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bed4f-176">System-Flags</span></span>           | <span data-ttu-id="bed4f-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bed4f-177">0x00000010</span></span>                                               |
| <span data-ttu-id="bed4f-178">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="bed4f-178">Classes used in</span></span>        | [<span data-ttu-id="bed4f-179">**Attribute-schema**</span><span class="sxs-lookup"><span data-stu-id="bed4f-179">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="bed4f-180">ADAM</span><span class="sxs-lookup"><span data-stu-id="bed4f-180">ADAM</span></span>



| <span data-ttu-id="bed4f-181">Voce</span><span class="sxs-lookup"><span data-stu-id="bed4f-181">Entry</span></span> | <span data-ttu-id="bed4f-182">Valore</span><span class="sxs-lookup"><span data-stu-id="bed4f-182">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="bed4f-183">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="bed4f-183">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="bed4f-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bed4f-184">MAPI-Id</span></span>                | <span data-ttu-id="bed4f-185">0x812D</span><span class="sxs-lookup"><span data-stu-id="bed4f-185">0x812D</span></span>                                                   |
| <span data-ttu-id="bed4f-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="bed4f-186">System-Only</span></span>            | <span data-ttu-id="bed4f-187">Falso</span><span class="sxs-lookup"><span data-stu-id="bed4f-187">False</span></span>                                                    |
| <span data-ttu-id="bed4f-188">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="bed4f-188">Is-Single-Valued</span></span>       | <span data-ttu-id="bed4f-189">Vero</span><span class="sxs-lookup"><span data-stu-id="bed4f-189">True</span></span>                                                     |
| <span data-ttu-id="bed4f-190">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="bed4f-190">Is Indexed</span></span>             | <span data-ttu-id="bed4f-191">Falso</span><span class="sxs-lookup"><span data-stu-id="bed4f-191">False</span></span>                                                    |
| <span data-ttu-id="bed4f-192">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="bed4f-192">In Global Catalog</span></span>      | <span data-ttu-id="bed4f-193">Falso</span><span class="sxs-lookup"><span data-stu-id="bed4f-193">False</span></span>                                                    |
| <span data-ttu-id="bed4f-194">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="bed4f-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="bed4f-195">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="bed4f-195">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="bed4f-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bed4f-196">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="bed4f-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bed4f-197">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="bed4f-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bed4f-198">Search-Flags</span></span>           | <span data-ttu-id="bed4f-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bed4f-199">0x00000000</span></span>                                               |
| <span data-ttu-id="bed4f-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bed4f-200">System-Flags</span></span>           | <span data-ttu-id="bed4f-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bed4f-201">0x00000010</span></span>                                               |
| <span data-ttu-id="bed4f-202">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="bed4f-202">Classes used in</span></span>        | [<span data-ttu-id="bed4f-203">**Attribute-schema**</span><span class="sxs-lookup"><span data-stu-id="bed4f-203">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="bed4f-204">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="bed4f-204">Windows Server 2003 R2</span></span>



| <span data-ttu-id="bed4f-205">Voce</span><span class="sxs-lookup"><span data-stu-id="bed4f-205">Entry</span></span> | <span data-ttu-id="bed4f-206">Valore</span><span class="sxs-lookup"><span data-stu-id="bed4f-206">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="bed4f-207">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="bed4f-207">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="bed4f-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bed4f-208">MAPI-Id</span></span>                | <span data-ttu-id="bed4f-209">0x812D</span><span class="sxs-lookup"><span data-stu-id="bed4f-209">0x812D</span></span>                                                   |
| <span data-ttu-id="bed4f-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="bed4f-210">System-Only</span></span>            | <span data-ttu-id="bed4f-211">Falso</span><span class="sxs-lookup"><span data-stu-id="bed4f-211">False</span></span>                                                    |
| <span data-ttu-id="bed4f-212">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="bed4f-212">Is-Single-Valued</span></span>       | <span data-ttu-id="bed4f-213">Vero</span><span class="sxs-lookup"><span data-stu-id="bed4f-213">True</span></span>                                                     |
| <span data-ttu-id="bed4f-214">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="bed4f-214">Is Indexed</span></span>             | <span data-ttu-id="bed4f-215">Falso</span><span class="sxs-lookup"><span data-stu-id="bed4f-215">False</span></span>                                                    |
| <span data-ttu-id="bed4f-216">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="bed4f-216">In Global Catalog</span></span>      | <span data-ttu-id="bed4f-217">Falso</span><span class="sxs-lookup"><span data-stu-id="bed4f-217">False</span></span>                                                    |
| <span data-ttu-id="bed4f-218">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="bed4f-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="bed4f-219">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="bed4f-219">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="bed4f-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bed4f-220">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="bed4f-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bed4f-221">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="bed4f-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bed4f-222">Search-Flags</span></span>           | <span data-ttu-id="bed4f-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bed4f-223">0x00000000</span></span>                                               |
| <span data-ttu-id="bed4f-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bed4f-224">System-Flags</span></span>           | <span data-ttu-id="bed4f-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bed4f-225">0x00000010</span></span>                                               |
| <span data-ttu-id="bed4f-226">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="bed4f-226">Classes used in</span></span>        | [<span data-ttu-id="bed4f-227">**Attribute-schema**</span><span class="sxs-lookup"><span data-stu-id="bed4f-227">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="bed4f-228">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bed4f-228">Windows Server 2008</span></span>



| <span data-ttu-id="bed4f-229">Voce</span><span class="sxs-lookup"><span data-stu-id="bed4f-229">Entry</span></span> | <span data-ttu-id="bed4f-230">Valore</span><span class="sxs-lookup"><span data-stu-id="bed4f-230">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="bed4f-231">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="bed4f-231">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="bed4f-232">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bed4f-232">MAPI-Id</span></span>                | <span data-ttu-id="bed4f-233">0x812D</span><span class="sxs-lookup"><span data-stu-id="bed4f-233">0x812D</span></span>                                                   |
| <span data-ttu-id="bed4f-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="bed4f-234">System-Only</span></span>            | <span data-ttu-id="bed4f-235">Falso</span><span class="sxs-lookup"><span data-stu-id="bed4f-235">False</span></span>                                                    |
| <span data-ttu-id="bed4f-236">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="bed4f-236">Is-Single-Valued</span></span>       | <span data-ttu-id="bed4f-237">Vero</span><span class="sxs-lookup"><span data-stu-id="bed4f-237">True</span></span>                                                     |
| <span data-ttu-id="bed4f-238">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="bed4f-238">Is Indexed</span></span>             | <span data-ttu-id="bed4f-239">Falso</span><span class="sxs-lookup"><span data-stu-id="bed4f-239">False</span></span>                                                    |
| <span data-ttu-id="bed4f-240">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="bed4f-240">In Global Catalog</span></span>      | <span data-ttu-id="bed4f-241">Falso</span><span class="sxs-lookup"><span data-stu-id="bed4f-241">False</span></span>                                                    |
| <span data-ttu-id="bed4f-242">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="bed4f-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="bed4f-243">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="bed4f-243">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="bed4f-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bed4f-244">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="bed4f-245">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bed4f-245">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="bed4f-246">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bed4f-246">Search-Flags</span></span>           | <span data-ttu-id="bed4f-247">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bed4f-247">0x00000000</span></span>                                               |
| <span data-ttu-id="bed4f-248">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bed4f-248">System-Flags</span></span>           | <span data-ttu-id="bed4f-249">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bed4f-249">0x00000010</span></span>                                               |
| <span data-ttu-id="bed4f-250">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="bed4f-250">Classes used in</span></span>        | [<span data-ttu-id="bed4f-251">**Attribute-schema**</span><span class="sxs-lookup"><span data-stu-id="bed4f-251">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="bed4f-252">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="bed4f-252">Windows Server 2008 R2</span></span>



| <span data-ttu-id="bed4f-253">Voce</span><span class="sxs-lookup"><span data-stu-id="bed4f-253">Entry</span></span> | <span data-ttu-id="bed4f-254">Valore</span><span class="sxs-lookup"><span data-stu-id="bed4f-254">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="bed4f-255">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="bed4f-255">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="bed4f-256">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bed4f-256">MAPI-Id</span></span>                | <span data-ttu-id="bed4f-257">0x812D</span><span class="sxs-lookup"><span data-stu-id="bed4f-257">0x812D</span></span>                                                   |
| <span data-ttu-id="bed4f-258">System-Only</span><span class="sxs-lookup"><span data-stu-id="bed4f-258">System-Only</span></span>            | <span data-ttu-id="bed4f-259">Falso</span><span class="sxs-lookup"><span data-stu-id="bed4f-259">False</span></span>                                                    |
| <span data-ttu-id="bed4f-260">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="bed4f-260">Is-Single-Valued</span></span>       | <span data-ttu-id="bed4f-261">Vero</span><span class="sxs-lookup"><span data-stu-id="bed4f-261">True</span></span>                                                     |
| <span data-ttu-id="bed4f-262">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="bed4f-262">Is Indexed</span></span>             | <span data-ttu-id="bed4f-263">Falso</span><span class="sxs-lookup"><span data-stu-id="bed4f-263">False</span></span>                                                    |
| <span data-ttu-id="bed4f-264">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="bed4f-264">In Global Catalog</span></span>      | <span data-ttu-id="bed4f-265">Falso</span><span class="sxs-lookup"><span data-stu-id="bed4f-265">False</span></span>                                                    |
| <span data-ttu-id="bed4f-266">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="bed4f-266">NT-Security-Descriptor</span></span> | <span data-ttu-id="bed4f-267">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="bed4f-267">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="bed4f-268">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bed4f-268">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="bed4f-269">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bed4f-269">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="bed4f-270">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bed4f-270">Search-Flags</span></span>           | <span data-ttu-id="bed4f-271">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bed4f-271">0x00000000</span></span>                                               |
| <span data-ttu-id="bed4f-272">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bed4f-272">System-Flags</span></span>           | <span data-ttu-id="bed4f-273">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bed4f-273">0x00000010</span></span>                                               |
| <span data-ttu-id="bed4f-274">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="bed4f-274">Classes used in</span></span>        | [<span data-ttu-id="bed4f-275">**Attribute-schema**</span><span class="sxs-lookup"><span data-stu-id="bed4f-275">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="bed4f-276">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="bed4f-276">Windows Server 2012</span></span>



| <span data-ttu-id="bed4f-277">Voce</span><span class="sxs-lookup"><span data-stu-id="bed4f-277">Entry</span></span> | <span data-ttu-id="bed4f-278">Valore</span><span class="sxs-lookup"><span data-stu-id="bed4f-278">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="bed4f-279">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="bed4f-279">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="bed4f-280">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bed4f-280">MAPI-Id</span></span>                | <span data-ttu-id="bed4f-281">0x812D</span><span class="sxs-lookup"><span data-stu-id="bed4f-281">0x812D</span></span>                                                   |
| <span data-ttu-id="bed4f-282">System-Only</span><span class="sxs-lookup"><span data-stu-id="bed4f-282">System-Only</span></span>            | <span data-ttu-id="bed4f-283">Falso</span><span class="sxs-lookup"><span data-stu-id="bed4f-283">False</span></span>                                                    |
| <span data-ttu-id="bed4f-284">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="bed4f-284">Is-Single-Valued</span></span>       | <span data-ttu-id="bed4f-285">Vero</span><span class="sxs-lookup"><span data-stu-id="bed4f-285">True</span></span>                                                     |
| <span data-ttu-id="bed4f-286">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="bed4f-286">Is Indexed</span></span>             | <span data-ttu-id="bed4f-287">Falso</span><span class="sxs-lookup"><span data-stu-id="bed4f-287">False</span></span>                                                    |
| <span data-ttu-id="bed4f-288">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="bed4f-288">In Global Catalog</span></span>      | <span data-ttu-id="bed4f-289">Falso</span><span class="sxs-lookup"><span data-stu-id="bed4f-289">False</span></span>                                                    |
| <span data-ttu-id="bed4f-290">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="bed4f-290">NT-Security-Descriptor</span></span> | <span data-ttu-id="bed4f-291">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="bed4f-291">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="bed4f-292">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bed4f-292">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="bed4f-293">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bed4f-293">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="bed4f-294">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bed4f-294">Search-Flags</span></span>           | <span data-ttu-id="bed4f-295">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bed4f-295">0x00000000</span></span>                                               |
| <span data-ttu-id="bed4f-296">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bed4f-296">System-Flags</span></span>           | <span data-ttu-id="bed4f-297">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bed4f-297">0x00000010</span></span>                                               |
| <span data-ttu-id="bed4f-298">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="bed4f-298">Classes used in</span></span>        | [<span data-ttu-id="bed4f-299">**Attribute-schema**</span><span class="sxs-lookup"><span data-stu-id="bed4f-299">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="bed4f-300">Commenti</span><span class="sxs-lookup"><span data-stu-id="bed4f-300">Remarks</span></span>

<span data-ttu-id="bed4f-301">Questo attributo può essere zero o una combinazione di uno o più dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="bed4f-301">This attribute can be zero or a combination of one or more of the following values.</span></span>



| <span data-ttu-id="bed4f-302">Valore</span><span class="sxs-lookup"><span data-stu-id="bed4f-302">Value</span></span>            | <span data-ttu-id="bed4f-303">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bed4f-303">Description</span></span>                                                                                                                                                                                                                                                                                                                                                               |
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bed4f-304">1 (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="bed4f-304">1 (0x00000001)</span></span>   | <span data-ttu-id="bed4f-305">Creare un indice per l'attributo.</span><span class="sxs-lookup"><span data-stu-id="bed4f-305">Create an index for the attribute.</span></span>                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="bed4f-306">2 (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="bed4f-306">2 (0x00000002)</span></span>   | <span data-ttu-id="bed4f-307">Creare un indice per l'attributo in ogni contenitore.</span><span class="sxs-lookup"><span data-stu-id="bed4f-307">Create an index for the attribute in each container.</span></span>                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="bed4f-308">4 (0x00000004)</span><span class="sxs-lookup"><span data-stu-id="bed4f-308">4 (0x00000004)</span></span>   | <span data-ttu-id="bed4f-309">Aggiungere questo attributo al set di risoluzione dei nomi ambiguo (ANR).</span><span class="sxs-lookup"><span data-stu-id="bed4f-309">Add this attribute to the Ambiguous Name Resolution (ANR) set.</span></span> <span data-ttu-id="bed4f-310">Viene utilizzato per facilitare la ricerca di un oggetto quando vengono fornite solo informazioni parziali.</span><span class="sxs-lookup"><span data-stu-id="bed4f-310">This is used to assist in finding an object when only partial information is given.</span></span> <span data-ttu-id="bed4f-311">Se, ad esempio, il filtro LDAP è (ANR = JEFF), la ricerca troverà ogni oggetto in cui il nome, il cognome, l'indirizzo di posta elettronica o un altro attributo ANR è uguale a JEFF.</span><span class="sxs-lookup"><span data-stu-id="bed4f-311">For example, if the LDAP filter is (ANR=JEFF), the search will find each object where the first name, last name, email address, or other ANR attribute is equal to JEFF.</span></span> <span data-ttu-id="bed4f-312">È necessario impostare il bit 0 per questo indice.</span><span class="sxs-lookup"><span data-stu-id="bed4f-312">Bit 0 must be set for this index take affect.</span></span> |
| <span data-ttu-id="bed4f-313">8 (0x00000008)</span><span class="sxs-lookup"><span data-stu-id="bed4f-313">8 (0x00000008)</span></span>   | <span data-ttu-id="bed4f-314">Mantenere questo attributo nell'oggetto contrassegnato per la rimozione definitiva per gli oggetti eliminati.</span><span class="sxs-lookup"><span data-stu-id="bed4f-314">Preserve this attribute in the tombstone object for deleted objects.</span></span>                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="bed4f-315">16 (0x00000010)</span><span class="sxs-lookup"><span data-stu-id="bed4f-315">16 (0x00000010)</span></span>  | <span data-ttu-id="bed4f-316">Copiare il valore di questo attributo quando l'oggetto viene copiato.</span><span class="sxs-lookup"><span data-stu-id="bed4f-316">Copy the value for this attribute when the object is copied.</span></span>                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="bed4f-317">32 (0x00000020)</span><span class="sxs-lookup"><span data-stu-id="bed4f-317">32 (0x00000020)</span></span>  | <span data-ttu-id="bed4f-318">Creare un indice di tupla per l'attributo.</span><span class="sxs-lookup"><span data-stu-id="bed4f-318">Create a tuple index for the attribute.</span></span> <span data-ttu-id="bed4f-319">Ciò consente di migliorare le ricerche in cui il carattere jolly viene visualizzato all'inizio della stringa di ricerca.</span><span class="sxs-lookup"><span data-stu-id="bed4f-319">This will improve searches where the wildcard appears at the front of the search string.</span></span> <span data-ttu-id="bed4f-320">Ad esempio, (sn = \* mith).</span><span class="sxs-lookup"><span data-stu-id="bed4f-320">For example, (sn=\*mith).</span></span>                                                                                                                                                                                                                |
| <span data-ttu-id="bed4f-321">64 (0x00000040)</span><span class="sxs-lookup"><span data-stu-id="bed4f-321">64(0x00000040)</span></span>   | <span data-ttu-id="bed4f-322">Supportato a partire da ADAM.</span><span class="sxs-lookup"><span data-stu-id="bed4f-322">Supported beginning with ADAM.</span></span> <span data-ttu-id="bed4f-323">Consente di creare un indice per migliorare significativamente le prestazioni VLV sugli attributi arbitrari.</span><span class="sxs-lookup"><span data-stu-id="bed4f-323">Creates an index to greatly help VLV performance on arbitrary attributes.</span></span>                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="bed4f-324">128 (0x00000080)</span><span class="sxs-lookup"><span data-stu-id="bed4f-324">128 (0x00000080)</span></span> | <span data-ttu-id="bed4f-325">Contrassegnare l'attributo come riservato.</span><span class="sxs-lookup"><span data-stu-id="bed4f-325">Mark attribute as confidential.</span></span> <span data-ttu-id="bed4f-326">Ignorato per gli attributi dello schema di base (systemFlags = 0x10).</span><span class="sxs-lookup"><span data-stu-id="bed4f-326">Ignored for base schema attributes (systemFlags=0x10).</span></span>                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="bed4f-327">64 (0x00000040)</span><span class="sxs-lookup"><span data-stu-id="bed4f-327">64 (0x00000040)</span></span>  | <span data-ttu-id="bed4f-328">Supportato a partire da Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="bed4f-328">Supported beginning with Windows Server 2008.</span></span> <span data-ttu-id="bed4f-329">Creare un indice per migliorare le prestazioni di ricerca VLV in questo attributo.</span><span class="sxs-lookup"><span data-stu-id="bed4f-329">Create an index to improve VLV search performance on this attribute.</span></span>                                                                                                                                                                                                                                                        |



 

 

 





