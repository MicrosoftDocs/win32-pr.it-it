---
title: attributo ms-DS-REPL-attribute-meta-data
description: Elenco di metadati per ogni attributo replicato. I metadati indicano che l'attributo è stato modificato per ultimo.
ms.assetid: 07cfd323-eb90-4715-9307-583cf7e9f63e
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo ms-DS-REPL-attribute-meta-data
- attributo msDS-ReplAttributeMetaData-schema AD
topic_type:
- apiref
api_name:
- ms-DS-Repl-Attribute-Meta-Data
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2edc991ead7104d8b9b4c023882d39adf1d53446
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "106303244"
---
# <a name="ms-ds-repl-attribute-meta-data-attribute"></a><span data-ttu-id="a882f-106">attributo ms-DS-REPL-attribute-meta-data</span><span class="sxs-lookup"><span data-stu-id="a882f-106">ms-DS-Repl-Attribute-Meta-Data attribute</span></span>

<span data-ttu-id="a882f-107">Elenco di metadati per ogni attributo replicato.</span><span class="sxs-lookup"><span data-stu-id="a882f-107">A list of metadata for each replicated attribute.</span></span> <span data-ttu-id="a882f-108">I metadati indicano che l'attributo è stato modificato per ultimo.</span><span class="sxs-lookup"><span data-stu-id="a882f-108">The metadata indicates who changed the attribute last.</span></span>



| <span data-ttu-id="a882f-109">Voce</span><span class="sxs-lookup"><span data-stu-id="a882f-109">Entry</span></span> | <span data-ttu-id="a882f-110">Valore</span><span class="sxs-lookup"><span data-stu-id="a882f-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="a882f-111">CN</span><span class="sxs-lookup"><span data-stu-id="a882f-111">CN</span></span>                | <span data-ttu-id="a882f-112">ms-DS-REPL-attribute-meta-data</span><span class="sxs-lookup"><span data-stu-id="a882f-112">ms-DS-Repl-Attribute-Meta-Data</span></span>              |
| <span data-ttu-id="a882f-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="a882f-113">Ldap-Display-Name</span></span> | <span data-ttu-id="a882f-114">msDS-ReplAttributeMetaData</span><span class="sxs-lookup"><span data-stu-id="a882f-114">msDS-ReplAttributeMetaData</span></span>                  |
| <span data-ttu-id="a882f-115">Dimensione</span><span class="sxs-lookup"><span data-stu-id="a882f-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="a882f-116">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="a882f-116">Update Privilege</span></span>  | <span data-ttu-id="a882f-117">Questo valore viene impostato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="a882f-117">This value is set by the system.</span></span>            |
| <span data-ttu-id="a882f-118">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="a882f-118">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="a882f-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a882f-119">Attribute-Id</span></span>      | <span data-ttu-id="a882f-120">1.2.840.113556.1.4.1707</span><span class="sxs-lookup"><span data-stu-id="a882f-120">1.2.840.113556.1.4.1707</span></span>                     |
| <span data-ttu-id="a882f-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="a882f-121">System-Id-Guid</span></span>    | <span data-ttu-id="a882f-122">d7c53242-724e-4c39-9d4c-2df8c9d66c7a</span><span class="sxs-lookup"><span data-stu-id="a882f-122">d7c53242-724e-4c39-9d4c-2df8c9d66c7a</span></span>        |
| <span data-ttu-id="a882f-123">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a882f-123">Syntax</span></span>            | [<span data-ttu-id="a882f-124">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="a882f-124">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="a882f-125">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="a882f-125">Implementations</span></span>

-   [<span data-ttu-id="a882f-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a882f-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a882f-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="a882f-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="a882f-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a882f-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a882f-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a882f-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a882f-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a882f-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a882f-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a882f-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="a882f-132">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a882f-132">Windows Server 2003</span></span>



| <span data-ttu-id="a882f-133">Voce</span><span class="sxs-lookup"><span data-stu-id="a882f-133">Entry</span></span> | <span data-ttu-id="a882f-134">Valore</span><span class="sxs-lookup"><span data-stu-id="a882f-134">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a882f-135">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="a882f-135">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="a882f-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a882f-136">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="a882f-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="a882f-137">System-Only</span></span>            | <span data-ttu-id="a882f-138">Falso</span><span class="sxs-lookup"><span data-stu-id="a882f-138">False</span></span>                           |
| <span data-ttu-id="a882f-139">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="a882f-139">Is-Single-Valued</span></span>       | <span data-ttu-id="a882f-140">Falso</span><span class="sxs-lookup"><span data-stu-id="a882f-140">False</span></span>                           |
| <span data-ttu-id="a882f-141">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="a882f-141">Is Indexed</span></span>             | <span data-ttu-id="a882f-142">Falso</span><span class="sxs-lookup"><span data-stu-id="a882f-142">False</span></span>                           |
| <span data-ttu-id="a882f-143">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="a882f-143">In Global Catalog</span></span>      | <span data-ttu-id="a882f-144">Falso</span><span class="sxs-lookup"><span data-stu-id="a882f-144">False</span></span>                           |
| <span data-ttu-id="a882f-145">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="a882f-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="a882f-146">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="a882f-146">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a882f-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a882f-147">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a882f-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a882f-148">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a882f-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a882f-149">Search-Flags</span></span>           | <span data-ttu-id="a882f-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a882f-150">0x00000000</span></span>                      |
| <span data-ttu-id="a882f-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a882f-151">System-Flags</span></span>           | <span data-ttu-id="a882f-152">0x00000014</span><span class="sxs-lookup"><span data-stu-id="a882f-152">0x00000014</span></span>                      |
| <span data-ttu-id="a882f-153">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="a882f-153">Classes used in</span></span>        | [<span data-ttu-id="a882f-154">**In alto**</span><span class="sxs-lookup"><span data-stu-id="a882f-154">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="a882f-155">ADAM</span><span class="sxs-lookup"><span data-stu-id="a882f-155">ADAM</span></span>



| <span data-ttu-id="a882f-156">Voce</span><span class="sxs-lookup"><span data-stu-id="a882f-156">Entry</span></span> | <span data-ttu-id="a882f-157">Valore</span><span class="sxs-lookup"><span data-stu-id="a882f-157">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a882f-158">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="a882f-158">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="a882f-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a882f-159">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="a882f-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="a882f-160">System-Only</span></span>            | <span data-ttu-id="a882f-161">Falso</span><span class="sxs-lookup"><span data-stu-id="a882f-161">False</span></span>                           |
| <span data-ttu-id="a882f-162">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="a882f-162">Is-Single-Valued</span></span>       | <span data-ttu-id="a882f-163">Falso</span><span class="sxs-lookup"><span data-stu-id="a882f-163">False</span></span>                           |
| <span data-ttu-id="a882f-164">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="a882f-164">Is Indexed</span></span>             | <span data-ttu-id="a882f-165">Falso</span><span class="sxs-lookup"><span data-stu-id="a882f-165">False</span></span>                           |
| <span data-ttu-id="a882f-166">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="a882f-166">In Global Catalog</span></span>      | <span data-ttu-id="a882f-167">Falso</span><span class="sxs-lookup"><span data-stu-id="a882f-167">False</span></span>                           |
| <span data-ttu-id="a882f-168">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="a882f-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="a882f-169">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="a882f-169">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a882f-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a882f-170">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a882f-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a882f-171">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a882f-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a882f-172">Search-Flags</span></span>           | <span data-ttu-id="a882f-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a882f-173">0x00000000</span></span>                      |
| <span data-ttu-id="a882f-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a882f-174">System-Flags</span></span>           | <span data-ttu-id="a882f-175">0x00000014</span><span class="sxs-lookup"><span data-stu-id="a882f-175">0x00000014</span></span>                      |
| <span data-ttu-id="a882f-176">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="a882f-176">Classes used in</span></span>        | [<span data-ttu-id="a882f-177">**In alto**</span><span class="sxs-lookup"><span data-stu-id="a882f-177">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a882f-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a882f-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a882f-179">Voce</span><span class="sxs-lookup"><span data-stu-id="a882f-179">Entry</span></span> | <span data-ttu-id="a882f-180">Valore</span><span class="sxs-lookup"><span data-stu-id="a882f-180">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a882f-181">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="a882f-181">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="a882f-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a882f-182">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="a882f-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="a882f-183">System-Only</span></span>            | <span data-ttu-id="a882f-184">Falso</span><span class="sxs-lookup"><span data-stu-id="a882f-184">False</span></span>                           |
| <span data-ttu-id="a882f-185">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="a882f-185">Is-Single-Valued</span></span>       | <span data-ttu-id="a882f-186">Falso</span><span class="sxs-lookup"><span data-stu-id="a882f-186">False</span></span>                           |
| <span data-ttu-id="a882f-187">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="a882f-187">Is Indexed</span></span>             | <span data-ttu-id="a882f-188">Falso</span><span class="sxs-lookup"><span data-stu-id="a882f-188">False</span></span>                           |
| <span data-ttu-id="a882f-189">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="a882f-189">In Global Catalog</span></span>      | <span data-ttu-id="a882f-190">Falso</span><span class="sxs-lookup"><span data-stu-id="a882f-190">False</span></span>                           |
| <span data-ttu-id="a882f-191">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="a882f-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="a882f-192">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="a882f-192">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a882f-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a882f-193">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a882f-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a882f-194">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a882f-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a882f-195">Search-Flags</span></span>           | <span data-ttu-id="a882f-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a882f-196">0x00000000</span></span>                      |
| <span data-ttu-id="a882f-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a882f-197">System-Flags</span></span>           | <span data-ttu-id="a882f-198">0x00000014</span><span class="sxs-lookup"><span data-stu-id="a882f-198">0x00000014</span></span>                      |
| <span data-ttu-id="a882f-199">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="a882f-199">Classes used in</span></span>        | [<span data-ttu-id="a882f-200">**In alto**</span><span class="sxs-lookup"><span data-stu-id="a882f-200">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a882f-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a882f-201">Windows Server 2008</span></span>



| <span data-ttu-id="a882f-202">Voce</span><span class="sxs-lookup"><span data-stu-id="a882f-202">Entry</span></span> | <span data-ttu-id="a882f-203">Valore</span><span class="sxs-lookup"><span data-stu-id="a882f-203">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a882f-204">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="a882f-204">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="a882f-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a882f-205">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="a882f-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="a882f-206">System-Only</span></span>            | <span data-ttu-id="a882f-207">Falso</span><span class="sxs-lookup"><span data-stu-id="a882f-207">False</span></span>                           |
| <span data-ttu-id="a882f-208">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="a882f-208">Is-Single-Valued</span></span>       | <span data-ttu-id="a882f-209">Falso</span><span class="sxs-lookup"><span data-stu-id="a882f-209">False</span></span>                           |
| <span data-ttu-id="a882f-210">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="a882f-210">Is Indexed</span></span>             | <span data-ttu-id="a882f-211">Falso</span><span class="sxs-lookup"><span data-stu-id="a882f-211">False</span></span>                           |
| <span data-ttu-id="a882f-212">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="a882f-212">In Global Catalog</span></span>      | <span data-ttu-id="a882f-213">Falso</span><span class="sxs-lookup"><span data-stu-id="a882f-213">False</span></span>                           |
| <span data-ttu-id="a882f-214">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="a882f-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="a882f-215">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="a882f-215">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a882f-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a882f-216">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a882f-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a882f-217">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a882f-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a882f-218">Search-Flags</span></span>           | <span data-ttu-id="a882f-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a882f-219">0x00000000</span></span>                      |
| <span data-ttu-id="a882f-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a882f-220">System-Flags</span></span>           | <span data-ttu-id="a882f-221">0x00000014</span><span class="sxs-lookup"><span data-stu-id="a882f-221">0x00000014</span></span>                      |
| <span data-ttu-id="a882f-222">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="a882f-222">Classes used in</span></span>        | [<span data-ttu-id="a882f-223">**In alto**</span><span class="sxs-lookup"><span data-stu-id="a882f-223">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a882f-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a882f-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a882f-225">Voce</span><span class="sxs-lookup"><span data-stu-id="a882f-225">Entry</span></span> | <span data-ttu-id="a882f-226">Valore</span><span class="sxs-lookup"><span data-stu-id="a882f-226">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a882f-227">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="a882f-227">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="a882f-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a882f-228">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="a882f-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="a882f-229">System-Only</span></span>            | <span data-ttu-id="a882f-230">Falso</span><span class="sxs-lookup"><span data-stu-id="a882f-230">False</span></span>                           |
| <span data-ttu-id="a882f-231">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="a882f-231">Is-Single-Valued</span></span>       | <span data-ttu-id="a882f-232">Falso</span><span class="sxs-lookup"><span data-stu-id="a882f-232">False</span></span>                           |
| <span data-ttu-id="a882f-233">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="a882f-233">Is Indexed</span></span>             | <span data-ttu-id="a882f-234">Falso</span><span class="sxs-lookup"><span data-stu-id="a882f-234">False</span></span>                           |
| <span data-ttu-id="a882f-235">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="a882f-235">In Global Catalog</span></span>      | <span data-ttu-id="a882f-236">Falso</span><span class="sxs-lookup"><span data-stu-id="a882f-236">False</span></span>                           |
| <span data-ttu-id="a882f-237">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="a882f-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="a882f-238">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="a882f-238">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a882f-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a882f-239">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a882f-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a882f-240">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a882f-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a882f-241">Search-Flags</span></span>           | <span data-ttu-id="a882f-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a882f-242">0x00000000</span></span>                      |
| <span data-ttu-id="a882f-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a882f-243">System-Flags</span></span>           | <span data-ttu-id="a882f-244">0x00000014</span><span class="sxs-lookup"><span data-stu-id="a882f-244">0x00000014</span></span>                      |
| <span data-ttu-id="a882f-245">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="a882f-245">Classes used in</span></span>        | [<span data-ttu-id="a882f-246">**In alto**</span><span class="sxs-lookup"><span data-stu-id="a882f-246">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a882f-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a882f-247">Windows Server 2012</span></span>



| <span data-ttu-id="a882f-248">Voce</span><span class="sxs-lookup"><span data-stu-id="a882f-248">Entry</span></span> | <span data-ttu-id="a882f-249">Valore</span><span class="sxs-lookup"><span data-stu-id="a882f-249">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a882f-250">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="a882f-250">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="a882f-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a882f-251">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="a882f-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="a882f-252">System-Only</span></span>            | <span data-ttu-id="a882f-253">Falso</span><span class="sxs-lookup"><span data-stu-id="a882f-253">False</span></span>                           |
| <span data-ttu-id="a882f-254">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="a882f-254">Is-Single-Valued</span></span>       | <span data-ttu-id="a882f-255">Falso</span><span class="sxs-lookup"><span data-stu-id="a882f-255">False</span></span>                           |
| <span data-ttu-id="a882f-256">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="a882f-256">Is Indexed</span></span>             | <span data-ttu-id="a882f-257">Falso</span><span class="sxs-lookup"><span data-stu-id="a882f-257">False</span></span>                           |
| <span data-ttu-id="a882f-258">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="a882f-258">In Global Catalog</span></span>      | <span data-ttu-id="a882f-259">Falso</span><span class="sxs-lookup"><span data-stu-id="a882f-259">False</span></span>                           |
| <span data-ttu-id="a882f-260">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="a882f-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="a882f-261">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="a882f-261">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a882f-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a882f-262">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a882f-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a882f-263">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a882f-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a882f-264">Search-Flags</span></span>           | <span data-ttu-id="a882f-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a882f-265">0x00000000</span></span>                      |
| <span data-ttu-id="a882f-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a882f-266">System-Flags</span></span>           | <span data-ttu-id="a882f-267">0x00000014</span><span class="sxs-lookup"><span data-stu-id="a882f-267">0x00000014</span></span>                      |
| <span data-ttu-id="a882f-268">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="a882f-268">Classes used in</span></span>        | [<span data-ttu-id="a882f-269">**In alto**</span><span class="sxs-lookup"><span data-stu-id="a882f-269">**Top**</span></span>](c-top.md)<br/> |



 

 





