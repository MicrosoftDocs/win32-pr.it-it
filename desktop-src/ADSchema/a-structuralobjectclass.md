---
title: Strutturale-oggetto-classe attributo
description: Questo attributo costruito archivia un elenco di classi contenute in una gerarchia di classi, incluse le classi astratte. Questo elenco contiene classi ausiliarie collegate in modo dinamico.
ms.assetid: f7311cb9-4816-4caa-9cae-cbcd61b93d27
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo strutturale-classe Object
- Schema AD dell'attributo structuralObjectClass
topic_type:
- apiref
api_name:
- Structural-Object-Class
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cdcc236c0c65aa365400894dd6ccfb845af04b55
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "106303359"
---
# <a name="structural-object-class-attribute"></a><span data-ttu-id="676fc-106">Strutturale-oggetto-classe attributo</span><span class="sxs-lookup"><span data-stu-id="676fc-106">Structural-Object-Class attribute</span></span>

<span data-ttu-id="676fc-107">Questo attributo costruito archivia un elenco di classi contenute in una gerarchia di classi, incluse le classi astratte.</span><span class="sxs-lookup"><span data-stu-id="676fc-107">This constructed attribute stores a list of classes contained in a class hierarchy, including abstract classes.</span></span> <span data-ttu-id="676fc-108">Questo elenco contiene classi ausiliarie collegate in modo dinamico.</span><span class="sxs-lookup"><span data-stu-id="676fc-108">This list does contain dynamically linked auxiliary classes.</span></span>



| <span data-ttu-id="676fc-109">Voce</span><span class="sxs-lookup"><span data-stu-id="676fc-109">Entry</span></span> | <span data-ttu-id="676fc-110">Valore</span><span class="sxs-lookup"><span data-stu-id="676fc-110">Value</span></span> |
|-------------------|-----------------------------------------------------------------|
| <span data-ttu-id="676fc-111">CN</span><span class="sxs-lookup"><span data-stu-id="676fc-111">CN</span></span>                | <span data-ttu-id="676fc-112">Classe strutturale-oggetto</span><span class="sxs-lookup"><span data-stu-id="676fc-112">Structural-Object-Class</span></span>                                         |
| <span data-ttu-id="676fc-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="676fc-113">Ldap-Display-Name</span></span> | <span data-ttu-id="676fc-114">structuralObjectClass</span><span class="sxs-lookup"><span data-stu-id="676fc-114">structuralObjectClass</span></span>                                           |
| <span data-ttu-id="676fc-115">Dimensione</span><span class="sxs-lookup"><span data-stu-id="676fc-115">Size</span></span>              | \-                                                              |
| <span data-ttu-id="676fc-116">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="676fc-116">Update Privilege</span></span>  | <span data-ttu-id="676fc-117">Questo valore viene impostato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="676fc-117">This value is set by the system.</span></span>                                |
| <span data-ttu-id="676fc-118">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="676fc-118">Update Frequency</span></span>  | <span data-ttu-id="676fc-119">Al momento della creazione della classe.</span><span class="sxs-lookup"><span data-stu-id="676fc-119">At class creation.</span></span>                                              |
| <span data-ttu-id="676fc-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="676fc-120">Attribute-Id</span></span>      | <span data-ttu-id="676fc-121">2.5.21.9</span><span class="sxs-lookup"><span data-stu-id="676fc-121">2.5.21.9</span></span>                                                        |
| <span data-ttu-id="676fc-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="676fc-122">System-Id-Guid</span></span>    | <span data-ttu-id="676fc-123">3860949f-f6a8-4b38-9950-81ecb6bc2982</span><span class="sxs-lookup"><span data-stu-id="676fc-123">3860949f-f6a8-4b38-9950-81ecb6bc2982</span></span>                            |
| <span data-ttu-id="676fc-124">Sintassi</span><span class="sxs-lookup"><span data-stu-id="676fc-124">Syntax</span></span>            | [<span data-ttu-id="676fc-125">**String(Object-Identifier)**</span><span class="sxs-lookup"><span data-stu-id="676fc-125">**String(Object-Identifier)**</span></span>](s-string-object-identifier.md) |



## <a name="implementations"></a><span data-ttu-id="676fc-126">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="676fc-126">Implementations</span></span>

-   [<span data-ttu-id="676fc-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="676fc-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="676fc-128">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="676fc-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="676fc-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="676fc-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="676fc-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="676fc-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="676fc-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="676fc-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="676fc-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="676fc-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="676fc-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="676fc-133">Windows Server 2003</span></span>



| <span data-ttu-id="676fc-134">Voce</span><span class="sxs-lookup"><span data-stu-id="676fc-134">Entry</span></span> | <span data-ttu-id="676fc-135">Valore</span><span class="sxs-lookup"><span data-stu-id="676fc-135">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="676fc-136">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="676fc-136">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="676fc-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="676fc-137">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="676fc-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="676fc-138">System-Only</span></span>            | <span data-ttu-id="676fc-139">Falso</span><span class="sxs-lookup"><span data-stu-id="676fc-139">False</span></span>                           |
| <span data-ttu-id="676fc-140">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="676fc-140">Is-Single-Valued</span></span>       | <span data-ttu-id="676fc-141">Falso</span><span class="sxs-lookup"><span data-stu-id="676fc-141">False</span></span>                           |
| <span data-ttu-id="676fc-142">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="676fc-142">Is Indexed</span></span>             | <span data-ttu-id="676fc-143">Falso</span><span class="sxs-lookup"><span data-stu-id="676fc-143">False</span></span>                           |
| <span data-ttu-id="676fc-144">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="676fc-144">In Global Catalog</span></span>      | <span data-ttu-id="676fc-145">Falso</span><span class="sxs-lookup"><span data-stu-id="676fc-145">False</span></span>                           |
| <span data-ttu-id="676fc-146">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="676fc-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="676fc-147">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="676fc-147">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="676fc-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="676fc-148">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="676fc-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="676fc-149">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="676fc-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="676fc-150">Search-Flags</span></span>           | <span data-ttu-id="676fc-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="676fc-151">0x00000000</span></span>                      |
| <span data-ttu-id="676fc-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="676fc-152">System-Flags</span></span>           | <span data-ttu-id="676fc-153">0x00000014</span><span class="sxs-lookup"><span data-stu-id="676fc-153">0x00000014</span></span>                      |
| <span data-ttu-id="676fc-154">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="676fc-154">Classes used in</span></span>        | [<span data-ttu-id="676fc-155">**In alto**</span><span class="sxs-lookup"><span data-stu-id="676fc-155">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="676fc-156">ADAM</span><span class="sxs-lookup"><span data-stu-id="676fc-156">ADAM</span></span>



| <span data-ttu-id="676fc-157">Voce</span><span class="sxs-lookup"><span data-stu-id="676fc-157">Entry</span></span> | <span data-ttu-id="676fc-158">Valore</span><span class="sxs-lookup"><span data-stu-id="676fc-158">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="676fc-159">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="676fc-159">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="676fc-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="676fc-160">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="676fc-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="676fc-161">System-Only</span></span>            | <span data-ttu-id="676fc-162">Falso</span><span class="sxs-lookup"><span data-stu-id="676fc-162">False</span></span>                           |
| <span data-ttu-id="676fc-163">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="676fc-163">Is-Single-Valued</span></span>       | <span data-ttu-id="676fc-164">Falso</span><span class="sxs-lookup"><span data-stu-id="676fc-164">False</span></span>                           |
| <span data-ttu-id="676fc-165">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="676fc-165">Is Indexed</span></span>             | <span data-ttu-id="676fc-166">Falso</span><span class="sxs-lookup"><span data-stu-id="676fc-166">False</span></span>                           |
| <span data-ttu-id="676fc-167">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="676fc-167">In Global Catalog</span></span>      | <span data-ttu-id="676fc-168">Falso</span><span class="sxs-lookup"><span data-stu-id="676fc-168">False</span></span>                           |
| <span data-ttu-id="676fc-169">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="676fc-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="676fc-170">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="676fc-170">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="676fc-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="676fc-171">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="676fc-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="676fc-172">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="676fc-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="676fc-173">Search-Flags</span></span>           | <span data-ttu-id="676fc-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="676fc-174">0x00000000</span></span>                      |
| <span data-ttu-id="676fc-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="676fc-175">System-Flags</span></span>           | <span data-ttu-id="676fc-176">0x00000014</span><span class="sxs-lookup"><span data-stu-id="676fc-176">0x00000014</span></span>                      |
| <span data-ttu-id="676fc-177">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="676fc-177">Classes used in</span></span>        | [<span data-ttu-id="676fc-178">**In alto**</span><span class="sxs-lookup"><span data-stu-id="676fc-178">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="676fc-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="676fc-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="676fc-180">Voce</span><span class="sxs-lookup"><span data-stu-id="676fc-180">Entry</span></span> | <span data-ttu-id="676fc-181">Valore</span><span class="sxs-lookup"><span data-stu-id="676fc-181">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="676fc-182">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="676fc-182">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="676fc-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="676fc-183">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="676fc-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="676fc-184">System-Only</span></span>            | <span data-ttu-id="676fc-185">Falso</span><span class="sxs-lookup"><span data-stu-id="676fc-185">False</span></span>                           |
| <span data-ttu-id="676fc-186">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="676fc-186">Is-Single-Valued</span></span>       | <span data-ttu-id="676fc-187">Falso</span><span class="sxs-lookup"><span data-stu-id="676fc-187">False</span></span>                           |
| <span data-ttu-id="676fc-188">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="676fc-188">Is Indexed</span></span>             | <span data-ttu-id="676fc-189">Falso</span><span class="sxs-lookup"><span data-stu-id="676fc-189">False</span></span>                           |
| <span data-ttu-id="676fc-190">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="676fc-190">In Global Catalog</span></span>      | <span data-ttu-id="676fc-191">Falso</span><span class="sxs-lookup"><span data-stu-id="676fc-191">False</span></span>                           |
| <span data-ttu-id="676fc-192">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="676fc-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="676fc-193">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="676fc-193">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="676fc-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="676fc-194">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="676fc-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="676fc-195">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="676fc-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="676fc-196">Search-Flags</span></span>           | <span data-ttu-id="676fc-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="676fc-197">0x00000000</span></span>                      |
| <span data-ttu-id="676fc-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="676fc-198">System-Flags</span></span>           | <span data-ttu-id="676fc-199">0x00000014</span><span class="sxs-lookup"><span data-stu-id="676fc-199">0x00000014</span></span>                      |
| <span data-ttu-id="676fc-200">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="676fc-200">Classes used in</span></span>        | [<span data-ttu-id="676fc-201">**In alto**</span><span class="sxs-lookup"><span data-stu-id="676fc-201">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="676fc-202">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="676fc-202">Windows Server 2008</span></span>



| <span data-ttu-id="676fc-203">Voce</span><span class="sxs-lookup"><span data-stu-id="676fc-203">Entry</span></span> | <span data-ttu-id="676fc-204">Valore</span><span class="sxs-lookup"><span data-stu-id="676fc-204">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="676fc-205">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="676fc-205">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="676fc-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="676fc-206">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="676fc-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="676fc-207">System-Only</span></span>            | <span data-ttu-id="676fc-208">Falso</span><span class="sxs-lookup"><span data-stu-id="676fc-208">False</span></span>                           |
| <span data-ttu-id="676fc-209">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="676fc-209">Is-Single-Valued</span></span>       | <span data-ttu-id="676fc-210">Falso</span><span class="sxs-lookup"><span data-stu-id="676fc-210">False</span></span>                           |
| <span data-ttu-id="676fc-211">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="676fc-211">Is Indexed</span></span>             | <span data-ttu-id="676fc-212">Falso</span><span class="sxs-lookup"><span data-stu-id="676fc-212">False</span></span>                           |
| <span data-ttu-id="676fc-213">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="676fc-213">In Global Catalog</span></span>      | <span data-ttu-id="676fc-214">Falso</span><span class="sxs-lookup"><span data-stu-id="676fc-214">False</span></span>                           |
| <span data-ttu-id="676fc-215">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="676fc-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="676fc-216">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="676fc-216">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="676fc-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="676fc-217">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="676fc-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="676fc-218">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="676fc-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="676fc-219">Search-Flags</span></span>           | <span data-ttu-id="676fc-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="676fc-220">0x00000000</span></span>                      |
| <span data-ttu-id="676fc-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="676fc-221">System-Flags</span></span>           | <span data-ttu-id="676fc-222">0x00000014</span><span class="sxs-lookup"><span data-stu-id="676fc-222">0x00000014</span></span>                      |
| <span data-ttu-id="676fc-223">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="676fc-223">Classes used in</span></span>        | [<span data-ttu-id="676fc-224">**In alto**</span><span class="sxs-lookup"><span data-stu-id="676fc-224">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="676fc-225">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="676fc-225">Windows Server 2008 R2</span></span>



| <span data-ttu-id="676fc-226">Voce</span><span class="sxs-lookup"><span data-stu-id="676fc-226">Entry</span></span> | <span data-ttu-id="676fc-227">Valore</span><span class="sxs-lookup"><span data-stu-id="676fc-227">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="676fc-228">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="676fc-228">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="676fc-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="676fc-229">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="676fc-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="676fc-230">System-Only</span></span>            | <span data-ttu-id="676fc-231">Falso</span><span class="sxs-lookup"><span data-stu-id="676fc-231">False</span></span>                           |
| <span data-ttu-id="676fc-232">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="676fc-232">Is-Single-Valued</span></span>       | <span data-ttu-id="676fc-233">Falso</span><span class="sxs-lookup"><span data-stu-id="676fc-233">False</span></span>                           |
| <span data-ttu-id="676fc-234">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="676fc-234">Is Indexed</span></span>             | <span data-ttu-id="676fc-235">Falso</span><span class="sxs-lookup"><span data-stu-id="676fc-235">False</span></span>                           |
| <span data-ttu-id="676fc-236">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="676fc-236">In Global Catalog</span></span>      | <span data-ttu-id="676fc-237">Falso</span><span class="sxs-lookup"><span data-stu-id="676fc-237">False</span></span>                           |
| <span data-ttu-id="676fc-238">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="676fc-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="676fc-239">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="676fc-239">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="676fc-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="676fc-240">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="676fc-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="676fc-241">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="676fc-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="676fc-242">Search-Flags</span></span>           | <span data-ttu-id="676fc-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="676fc-243">0x00000000</span></span>                      |
| <span data-ttu-id="676fc-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="676fc-244">System-Flags</span></span>           | <span data-ttu-id="676fc-245">0x00000014</span><span class="sxs-lookup"><span data-stu-id="676fc-245">0x00000014</span></span>                      |
| <span data-ttu-id="676fc-246">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="676fc-246">Classes used in</span></span>        | [<span data-ttu-id="676fc-247">**In alto**</span><span class="sxs-lookup"><span data-stu-id="676fc-247">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="676fc-248">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="676fc-248">Windows Server 2012</span></span>



| <span data-ttu-id="676fc-249">Voce</span><span class="sxs-lookup"><span data-stu-id="676fc-249">Entry</span></span> | <span data-ttu-id="676fc-250">Valore</span><span class="sxs-lookup"><span data-stu-id="676fc-250">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="676fc-251">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="676fc-251">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="676fc-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="676fc-252">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="676fc-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="676fc-253">System-Only</span></span>            | <span data-ttu-id="676fc-254">Falso</span><span class="sxs-lookup"><span data-stu-id="676fc-254">False</span></span>                           |
| <span data-ttu-id="676fc-255">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="676fc-255">Is-Single-Valued</span></span>       | <span data-ttu-id="676fc-256">Falso</span><span class="sxs-lookup"><span data-stu-id="676fc-256">False</span></span>                           |
| <span data-ttu-id="676fc-257">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="676fc-257">Is Indexed</span></span>             | <span data-ttu-id="676fc-258">Falso</span><span class="sxs-lookup"><span data-stu-id="676fc-258">False</span></span>                           |
| <span data-ttu-id="676fc-259">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="676fc-259">In Global Catalog</span></span>      | <span data-ttu-id="676fc-260">Falso</span><span class="sxs-lookup"><span data-stu-id="676fc-260">False</span></span>                           |
| <span data-ttu-id="676fc-261">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="676fc-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="676fc-262">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="676fc-262">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="676fc-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="676fc-263">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="676fc-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="676fc-264">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="676fc-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="676fc-265">Search-Flags</span></span>           | <span data-ttu-id="676fc-266">0x00000000</span><span class="sxs-lookup"><span data-stu-id="676fc-266">0x00000000</span></span>                      |
| <span data-ttu-id="676fc-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="676fc-267">System-Flags</span></span>           | <span data-ttu-id="676fc-268">0x00000014</span><span class="sxs-lookup"><span data-stu-id="676fc-268">0x00000014</span></span>                      |
| <span data-ttu-id="676fc-269">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="676fc-269">Classes used in</span></span>        | [<span data-ttu-id="676fc-270">**In alto**</span><span class="sxs-lookup"><span data-stu-id="676fc-270">**Top**</span></span>](c-top.md)<br/> |



 

 





