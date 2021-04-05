---
title: Obj-Dist-Name (attributo)
description: Uguale al nome distinto per un oggetto. Utilizzato da Exchange.
ms.assetid: 0dc2855c-2707-49d8-80e6-27f163a59bc8
ms.tgt_platform: multiple
keywords:
- Attributo Obj-Dist-Name-schema AD
- Schema AD dell'attributo Distinguishname
topic_type:
- apiref
api_name:
- Obj-Dist-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42cd118f38de78546b7b792bca3c8c9ef6d229cb
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103874910"
---
# <a name="obj-dist-name-attribute"></a><span data-ttu-id="c93a3-106">Obj-Dist-Name (attributo)</span><span class="sxs-lookup"><span data-stu-id="c93a3-106">Obj-Dist-Name attribute</span></span>

<span data-ttu-id="c93a3-107">Uguale al nome distinto per un oggetto.</span><span class="sxs-lookup"><span data-stu-id="c93a3-107">Same as the Distinguished Name for an object.</span></span> <span data-ttu-id="c93a3-108">Utilizzato da Exchange.</span><span class="sxs-lookup"><span data-stu-id="c93a3-108">Used by Exchange.</span></span>



| <span data-ttu-id="c93a3-109">Voce</span><span class="sxs-lookup"><span data-stu-id="c93a3-109">Entry</span></span> | <span data-ttu-id="c93a3-110">Valore</span><span class="sxs-lookup"><span data-stu-id="c93a3-110">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="c93a3-111">CN</span><span class="sxs-lookup"><span data-stu-id="c93a3-111">CN</span></span>                | <span data-ttu-id="c93a3-112">Obj-Dist-Name</span><span class="sxs-lookup"><span data-stu-id="c93a3-112">Obj-Dist-Name</span></span>                           |
| <span data-ttu-id="c93a3-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="c93a3-113">Ldap-Display-Name</span></span> | <span data-ttu-id="c93a3-114">distinguishedName</span><span class="sxs-lookup"><span data-stu-id="c93a3-114">distinguishedName</span></span>                       |
| <span data-ttu-id="c93a3-115">Dimensione</span><span class="sxs-lookup"><span data-stu-id="c93a3-115">Size</span></span>              | \-                                      |
| <span data-ttu-id="c93a3-116">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="c93a3-116">Update Privilege</span></span>  | <span data-ttu-id="c93a3-117">Questo valore viene impostato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="c93a3-117">This value is set by the system.</span></span>        |
| <span data-ttu-id="c93a3-118">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="c93a3-118">Update Frequency</span></span>  | <span data-ttu-id="c93a3-119">Ogni volta che un oggetto viene creato o spostato.</span><span class="sxs-lookup"><span data-stu-id="c93a3-119">Whenever an object is created or moved.</span></span> |
| <span data-ttu-id="c93a3-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c93a3-120">Attribute-Id</span></span>      | <span data-ttu-id="c93a3-121">2.5.4.49</span><span class="sxs-lookup"><span data-stu-id="c93a3-121">2.5.4.49</span></span>                                |
| <span data-ttu-id="c93a3-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="c93a3-122">System-Id-Guid</span></span>    | <span data-ttu-id="c93a3-123">bf9679e4-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="c93a3-123">bf9679e4-0de6-11d0-a285-00aa003049e2</span></span>    |
| <span data-ttu-id="c93a3-124">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c93a3-124">Syntax</span></span>            | [<span data-ttu-id="c93a3-125">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="c93a3-125">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="c93a3-126">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="c93a3-126">Implementations</span></span>

-   [<span data-ttu-id="c93a3-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="c93a3-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="c93a3-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c93a3-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c93a3-129">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="c93a3-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="c93a3-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c93a3-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c93a3-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c93a3-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c93a3-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c93a3-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c93a3-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c93a3-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="c93a3-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c93a3-134">Windows 2000 Server</span></span>



| <span data-ttu-id="c93a3-135">Voce</span><span class="sxs-lookup"><span data-stu-id="c93a3-135">Entry</span></span> | <span data-ttu-id="c93a3-136">Valore</span><span class="sxs-lookup"><span data-stu-id="c93a3-136">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c93a3-137">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="c93a3-137">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="c93a3-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c93a3-138">MAPI-Id</span></span>                | <span data-ttu-id="c93a3-139">0x803C</span><span class="sxs-lookup"><span data-stu-id="c93a3-139">0x803C</span></span>                          |
| <span data-ttu-id="c93a3-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="c93a3-140">System-Only</span></span>            | <span data-ttu-id="c93a3-141">Vero</span><span class="sxs-lookup"><span data-stu-id="c93a3-141">True</span></span>                            |
| <span data-ttu-id="c93a3-142">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="c93a3-142">Is-Single-Valued</span></span>       | <span data-ttu-id="c93a3-143">Vero</span><span class="sxs-lookup"><span data-stu-id="c93a3-143">True</span></span>                            |
| <span data-ttu-id="c93a3-144">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="c93a3-144">Is Indexed</span></span>             | <span data-ttu-id="c93a3-145">Falso</span><span class="sxs-lookup"><span data-stu-id="c93a3-145">False</span></span>                           |
| <span data-ttu-id="c93a3-146">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="c93a3-146">In Global Catalog</span></span>      | <span data-ttu-id="c93a3-147">Vero</span><span class="sxs-lookup"><span data-stu-id="c93a3-147">True</span></span>                            |
| <span data-ttu-id="c93a3-148">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="c93a3-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="c93a3-149">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="c93a3-149">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c93a3-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c93a3-150">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="c93a3-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c93a3-151">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="c93a3-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c93a3-152">Search-Flags</span></span>           | <span data-ttu-id="c93a3-153">0x00000008</span><span class="sxs-lookup"><span data-stu-id="c93a3-153">0x00000008</span></span>                      |
| <span data-ttu-id="c93a3-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c93a3-154">System-Flags</span></span>           | <span data-ttu-id="c93a3-155">0x00000013</span><span class="sxs-lookup"><span data-stu-id="c93a3-155">0x00000013</span></span>                      |
| <span data-ttu-id="c93a3-156">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="c93a3-156">Classes used in</span></span>        | [<span data-ttu-id="c93a3-157">**In alto**</span><span class="sxs-lookup"><span data-stu-id="c93a3-157">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="c93a3-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c93a3-158">Windows Server 2003</span></span>



| <span data-ttu-id="c93a3-159">Voce</span><span class="sxs-lookup"><span data-stu-id="c93a3-159">Entry</span></span> | <span data-ttu-id="c93a3-160">Valore</span><span class="sxs-lookup"><span data-stu-id="c93a3-160">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c93a3-161">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="c93a3-161">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="c93a3-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c93a3-162">MAPI-Id</span></span>                | <span data-ttu-id="c93a3-163">0x803C</span><span class="sxs-lookup"><span data-stu-id="c93a3-163">0x803C</span></span>                          |
| <span data-ttu-id="c93a3-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="c93a3-164">System-Only</span></span>            | <span data-ttu-id="c93a3-165">Vero</span><span class="sxs-lookup"><span data-stu-id="c93a3-165">True</span></span>                            |
| <span data-ttu-id="c93a3-166">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="c93a3-166">Is-Single-Valued</span></span>       | <span data-ttu-id="c93a3-167">Vero</span><span class="sxs-lookup"><span data-stu-id="c93a3-167">True</span></span>                            |
| <span data-ttu-id="c93a3-168">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="c93a3-168">Is Indexed</span></span>             | <span data-ttu-id="c93a3-169">Falso</span><span class="sxs-lookup"><span data-stu-id="c93a3-169">False</span></span>                           |
| <span data-ttu-id="c93a3-170">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="c93a3-170">In Global Catalog</span></span>      | <span data-ttu-id="c93a3-171">Vero</span><span class="sxs-lookup"><span data-stu-id="c93a3-171">True</span></span>                            |
| <span data-ttu-id="c93a3-172">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="c93a3-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="c93a3-173">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="c93a3-173">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c93a3-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c93a3-174">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="c93a3-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c93a3-175">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="c93a3-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c93a3-176">Search-Flags</span></span>           | <span data-ttu-id="c93a3-177">0x00000008</span><span class="sxs-lookup"><span data-stu-id="c93a3-177">0x00000008</span></span>                      |
| <span data-ttu-id="c93a3-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c93a3-178">System-Flags</span></span>           | <span data-ttu-id="c93a3-179">0x00000013</span><span class="sxs-lookup"><span data-stu-id="c93a3-179">0x00000013</span></span>                      |
| <span data-ttu-id="c93a3-180">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="c93a3-180">Classes used in</span></span>        | [<span data-ttu-id="c93a3-181">**In alto**</span><span class="sxs-lookup"><span data-stu-id="c93a3-181">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="c93a3-182">ADAM</span><span class="sxs-lookup"><span data-stu-id="c93a3-182">ADAM</span></span>



| <span data-ttu-id="c93a3-183">Voce</span><span class="sxs-lookup"><span data-stu-id="c93a3-183">Entry</span></span> | <span data-ttu-id="c93a3-184">Valore</span><span class="sxs-lookup"><span data-stu-id="c93a3-184">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c93a3-185">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="c93a3-185">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="c93a3-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c93a3-186">MAPI-Id</span></span>                | <span data-ttu-id="c93a3-187">0x803C</span><span class="sxs-lookup"><span data-stu-id="c93a3-187">0x803C</span></span>                          |
| <span data-ttu-id="c93a3-188">System-Only</span><span class="sxs-lookup"><span data-stu-id="c93a3-188">System-Only</span></span>            | <span data-ttu-id="c93a3-189">Vero</span><span class="sxs-lookup"><span data-stu-id="c93a3-189">True</span></span>                            |
| <span data-ttu-id="c93a3-190">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="c93a3-190">Is-Single-Valued</span></span>       | <span data-ttu-id="c93a3-191">Vero</span><span class="sxs-lookup"><span data-stu-id="c93a3-191">True</span></span>                            |
| <span data-ttu-id="c93a3-192">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="c93a3-192">Is Indexed</span></span>             | <span data-ttu-id="c93a3-193">Falso</span><span class="sxs-lookup"><span data-stu-id="c93a3-193">False</span></span>                           |
| <span data-ttu-id="c93a3-194">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="c93a3-194">In Global Catalog</span></span>      | <span data-ttu-id="c93a3-195">Vero</span><span class="sxs-lookup"><span data-stu-id="c93a3-195">True</span></span>                            |
| <span data-ttu-id="c93a3-196">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="c93a3-196">NT-Security-Descriptor</span></span> | <span data-ttu-id="c93a3-197">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="c93a3-197">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c93a3-198">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c93a3-198">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="c93a3-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c93a3-199">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="c93a3-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c93a3-200">Search-Flags</span></span>           | <span data-ttu-id="c93a3-201">0x00000008</span><span class="sxs-lookup"><span data-stu-id="c93a3-201">0x00000008</span></span>                      |
| <span data-ttu-id="c93a3-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c93a3-202">System-Flags</span></span>           | <span data-ttu-id="c93a3-203">0x00000013</span><span class="sxs-lookup"><span data-stu-id="c93a3-203">0x00000013</span></span>                      |
| <span data-ttu-id="c93a3-204">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="c93a3-204">Classes used in</span></span>        | [<span data-ttu-id="c93a3-205">**In alto**</span><span class="sxs-lookup"><span data-stu-id="c93a3-205">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c93a3-206">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c93a3-206">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c93a3-207">Voce</span><span class="sxs-lookup"><span data-stu-id="c93a3-207">Entry</span></span> | <span data-ttu-id="c93a3-208">Valore</span><span class="sxs-lookup"><span data-stu-id="c93a3-208">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c93a3-209">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="c93a3-209">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="c93a3-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c93a3-210">MAPI-Id</span></span>                | <span data-ttu-id="c93a3-211">0x803C</span><span class="sxs-lookup"><span data-stu-id="c93a3-211">0x803C</span></span>                          |
| <span data-ttu-id="c93a3-212">System-Only</span><span class="sxs-lookup"><span data-stu-id="c93a3-212">System-Only</span></span>            | <span data-ttu-id="c93a3-213">Vero</span><span class="sxs-lookup"><span data-stu-id="c93a3-213">True</span></span>                            |
| <span data-ttu-id="c93a3-214">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="c93a3-214">Is-Single-Valued</span></span>       | <span data-ttu-id="c93a3-215">Vero</span><span class="sxs-lookup"><span data-stu-id="c93a3-215">True</span></span>                            |
| <span data-ttu-id="c93a3-216">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="c93a3-216">Is Indexed</span></span>             | <span data-ttu-id="c93a3-217">Falso</span><span class="sxs-lookup"><span data-stu-id="c93a3-217">False</span></span>                           |
| <span data-ttu-id="c93a3-218">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="c93a3-218">In Global Catalog</span></span>      | <span data-ttu-id="c93a3-219">Vero</span><span class="sxs-lookup"><span data-stu-id="c93a3-219">True</span></span>                            |
| <span data-ttu-id="c93a3-220">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="c93a3-220">NT-Security-Descriptor</span></span> | <span data-ttu-id="c93a3-221">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="c93a3-221">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c93a3-222">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c93a3-222">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="c93a3-223">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c93a3-223">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="c93a3-224">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c93a3-224">Search-Flags</span></span>           | <span data-ttu-id="c93a3-225">0x00000008</span><span class="sxs-lookup"><span data-stu-id="c93a3-225">0x00000008</span></span>                      |
| <span data-ttu-id="c93a3-226">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c93a3-226">System-Flags</span></span>           | <span data-ttu-id="c93a3-227">0x00000013</span><span class="sxs-lookup"><span data-stu-id="c93a3-227">0x00000013</span></span>                      |
| <span data-ttu-id="c93a3-228">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="c93a3-228">Classes used in</span></span>        | [<span data-ttu-id="c93a3-229">**In alto**</span><span class="sxs-lookup"><span data-stu-id="c93a3-229">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c93a3-230">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c93a3-230">Windows Server 2008</span></span>



| <span data-ttu-id="c93a3-231">Voce</span><span class="sxs-lookup"><span data-stu-id="c93a3-231">Entry</span></span> | <span data-ttu-id="c93a3-232">Valore</span><span class="sxs-lookup"><span data-stu-id="c93a3-232">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c93a3-233">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="c93a3-233">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="c93a3-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c93a3-234">MAPI-Id</span></span>                | <span data-ttu-id="c93a3-235">0x803C</span><span class="sxs-lookup"><span data-stu-id="c93a3-235">0x803C</span></span>                          |
| <span data-ttu-id="c93a3-236">System-Only</span><span class="sxs-lookup"><span data-stu-id="c93a3-236">System-Only</span></span>            | <span data-ttu-id="c93a3-237">Vero</span><span class="sxs-lookup"><span data-stu-id="c93a3-237">True</span></span>                            |
| <span data-ttu-id="c93a3-238">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="c93a3-238">Is-Single-Valued</span></span>       | <span data-ttu-id="c93a3-239">Vero</span><span class="sxs-lookup"><span data-stu-id="c93a3-239">True</span></span>                            |
| <span data-ttu-id="c93a3-240">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="c93a3-240">Is Indexed</span></span>             | <span data-ttu-id="c93a3-241">Falso</span><span class="sxs-lookup"><span data-stu-id="c93a3-241">False</span></span>                           |
| <span data-ttu-id="c93a3-242">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="c93a3-242">In Global Catalog</span></span>      | <span data-ttu-id="c93a3-243">Vero</span><span class="sxs-lookup"><span data-stu-id="c93a3-243">True</span></span>                            |
| <span data-ttu-id="c93a3-244">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="c93a3-244">NT-Security-Descriptor</span></span> | <span data-ttu-id="c93a3-245">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="c93a3-245">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c93a3-246">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c93a3-246">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="c93a3-247">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c93a3-247">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="c93a3-248">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c93a3-248">Search-Flags</span></span>           | <span data-ttu-id="c93a3-249">0x00000008</span><span class="sxs-lookup"><span data-stu-id="c93a3-249">0x00000008</span></span>                      |
| <span data-ttu-id="c93a3-250">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c93a3-250">System-Flags</span></span>           | <span data-ttu-id="c93a3-251">0x00000013</span><span class="sxs-lookup"><span data-stu-id="c93a3-251">0x00000013</span></span>                      |
| <span data-ttu-id="c93a3-252">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="c93a3-252">Classes used in</span></span>        | [<span data-ttu-id="c93a3-253">**In alto**</span><span class="sxs-lookup"><span data-stu-id="c93a3-253">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c93a3-254">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c93a3-254">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c93a3-255">Voce</span><span class="sxs-lookup"><span data-stu-id="c93a3-255">Entry</span></span> | <span data-ttu-id="c93a3-256">Valore</span><span class="sxs-lookup"><span data-stu-id="c93a3-256">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c93a3-257">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="c93a3-257">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="c93a3-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c93a3-258">MAPI-Id</span></span>                | <span data-ttu-id="c93a3-259">0x803C</span><span class="sxs-lookup"><span data-stu-id="c93a3-259">0x803C</span></span>                          |
| <span data-ttu-id="c93a3-260">System-Only</span><span class="sxs-lookup"><span data-stu-id="c93a3-260">System-Only</span></span>            | <span data-ttu-id="c93a3-261">Vero</span><span class="sxs-lookup"><span data-stu-id="c93a3-261">True</span></span>                            |
| <span data-ttu-id="c93a3-262">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="c93a3-262">Is-Single-Valued</span></span>       | <span data-ttu-id="c93a3-263">Vero</span><span class="sxs-lookup"><span data-stu-id="c93a3-263">True</span></span>                            |
| <span data-ttu-id="c93a3-264">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="c93a3-264">Is Indexed</span></span>             | <span data-ttu-id="c93a3-265">Falso</span><span class="sxs-lookup"><span data-stu-id="c93a3-265">False</span></span>                           |
| <span data-ttu-id="c93a3-266">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="c93a3-266">In Global Catalog</span></span>      | <span data-ttu-id="c93a3-267">Vero</span><span class="sxs-lookup"><span data-stu-id="c93a3-267">True</span></span>                            |
| <span data-ttu-id="c93a3-268">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="c93a3-268">NT-Security-Descriptor</span></span> | <span data-ttu-id="c93a3-269">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="c93a3-269">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c93a3-270">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c93a3-270">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="c93a3-271">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c93a3-271">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="c93a3-272">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c93a3-272">Search-Flags</span></span>           | <span data-ttu-id="c93a3-273">0x00000008</span><span class="sxs-lookup"><span data-stu-id="c93a3-273">0x00000008</span></span>                      |
| <span data-ttu-id="c93a3-274">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c93a3-274">System-Flags</span></span>           | <span data-ttu-id="c93a3-275">0x00000013</span><span class="sxs-lookup"><span data-stu-id="c93a3-275">0x00000013</span></span>                      |
| <span data-ttu-id="c93a3-276">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="c93a3-276">Classes used in</span></span>        | [<span data-ttu-id="c93a3-277">**In alto**</span><span class="sxs-lookup"><span data-stu-id="c93a3-277">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c93a3-278">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c93a3-278">Windows Server 2012</span></span>



| <span data-ttu-id="c93a3-279">Voce</span><span class="sxs-lookup"><span data-stu-id="c93a3-279">Entry</span></span> | <span data-ttu-id="c93a3-280">Valore</span><span class="sxs-lookup"><span data-stu-id="c93a3-280">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c93a3-281">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="c93a3-281">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="c93a3-282">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c93a3-282">MAPI-Id</span></span>                | <span data-ttu-id="c93a3-283">0x803C</span><span class="sxs-lookup"><span data-stu-id="c93a3-283">0x803C</span></span>                          |
| <span data-ttu-id="c93a3-284">System-Only</span><span class="sxs-lookup"><span data-stu-id="c93a3-284">System-Only</span></span>            | <span data-ttu-id="c93a3-285">Vero</span><span class="sxs-lookup"><span data-stu-id="c93a3-285">True</span></span>                            |
| <span data-ttu-id="c93a3-286">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="c93a3-286">Is-Single-Valued</span></span>       | <span data-ttu-id="c93a3-287">Vero</span><span class="sxs-lookup"><span data-stu-id="c93a3-287">True</span></span>                            |
| <span data-ttu-id="c93a3-288">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="c93a3-288">Is Indexed</span></span>             | <span data-ttu-id="c93a3-289">Falso</span><span class="sxs-lookup"><span data-stu-id="c93a3-289">False</span></span>                           |
| <span data-ttu-id="c93a3-290">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="c93a3-290">In Global Catalog</span></span>      | <span data-ttu-id="c93a3-291">Vero</span><span class="sxs-lookup"><span data-stu-id="c93a3-291">True</span></span>                            |
| <span data-ttu-id="c93a3-292">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="c93a3-292">NT-Security-Descriptor</span></span> | <span data-ttu-id="c93a3-293">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="c93a3-293">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c93a3-294">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c93a3-294">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="c93a3-295">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c93a3-295">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="c93a3-296">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c93a3-296">Search-Flags</span></span>           | <span data-ttu-id="c93a3-297">0x00000008</span><span class="sxs-lookup"><span data-stu-id="c93a3-297">0x00000008</span></span>                      |
| <span data-ttu-id="c93a3-298">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c93a3-298">System-Flags</span></span>           | <span data-ttu-id="c93a3-299">0x00000013</span><span class="sxs-lookup"><span data-stu-id="c93a3-299">0x00000013</span></span>                      |
| <span data-ttu-id="c93a3-300">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="c93a3-300">Classes used in</span></span>        | [<span data-ttu-id="c93a3-301">**In alto**</span><span class="sxs-lookup"><span data-stu-id="c93a3-301">**Top**</span></span>](c-top.md)<br/> |



 

 





