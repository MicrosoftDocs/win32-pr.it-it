---
title: Attributo Trust-Parent
description: Elemento padre nella gerarchia di trust KERBEROS.
ms.assetid: 738cf509-42a2-40b6-a525-6df34c02d0f0
ms.tgt_platform: multiple
keywords:
- Schema AD Trust-Parent attribute
- Schema AD dell'attributo trustParent
topic_type:
- apiref
api_name:
- Trust-Parent
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1d8be971c7597b14daf7a694e41c9d67714e5f0
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744874"
---
# <a name="trust-parent-attribute"></a><span data-ttu-id="f0035-105">Attributo Trust-Parent</span><span class="sxs-lookup"><span data-stu-id="f0035-105">Trust-Parent attribute</span></span>

<span data-ttu-id="f0035-106">Elemento padre nella gerarchia di trust KERBEROS.</span><span class="sxs-lookup"><span data-stu-id="f0035-106">The parent in KERBEROS trust hierarchy.</span></span>



| <span data-ttu-id="f0035-107">Voce</span><span class="sxs-lookup"><span data-stu-id="f0035-107">Entry</span></span> | <span data-ttu-id="f0035-108">Valore</span><span class="sxs-lookup"><span data-stu-id="f0035-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="f0035-109">CN</span><span class="sxs-lookup"><span data-stu-id="f0035-109">CN</span></span>                | <span data-ttu-id="f0035-110">Trust-Parent</span><span class="sxs-lookup"><span data-stu-id="f0035-110">Trust-Parent</span></span>                            |
| <span data-ttu-id="f0035-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="f0035-111">Ldap-Display-Name</span></span> | <span data-ttu-id="f0035-112">trustParent</span><span class="sxs-lookup"><span data-stu-id="f0035-112">trustParent</span></span>                             |
| <span data-ttu-id="f0035-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="f0035-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="f0035-114">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="f0035-114">Update Privilege</span></span>  | <span data-ttu-id="f0035-115">Questo valore viene impostato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="f0035-115">This value is set by the system.</span></span>        |
| <span data-ttu-id="f0035-116">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="f0035-116">Update Frequency</span></span>  | <span data-ttu-id="f0035-117">Quando viene creato un dominio figlio.</span><span class="sxs-lookup"><span data-stu-id="f0035-117">When a child domain is created.</span></span>         |
| <span data-ttu-id="f0035-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f0035-118">Attribute-Id</span></span>      | <span data-ttu-id="f0035-119">1.2.840.113556.1.4.471</span><span class="sxs-lookup"><span data-stu-id="f0035-119">1.2.840.113556.1.4.471</span></span>                  |
| <span data-ttu-id="f0035-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="f0035-120">System-Id-Guid</span></span>    | <span data-ttu-id="f0035-121">b000ea7a-a086-11d0-afdd-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="f0035-121">b000ea7a-a086-11d0-afdd-00c04fd930c9</span></span>    |
| <span data-ttu-id="f0035-122">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f0035-122">Syntax</span></span>            | [<span data-ttu-id="f0035-123">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="f0035-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="f0035-124">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="f0035-124">Implementations</span></span>

-   [<span data-ttu-id="f0035-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="f0035-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="f0035-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f0035-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f0035-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="f0035-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="f0035-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f0035-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f0035-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f0035-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f0035-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f0035-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f0035-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f0035-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="f0035-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f0035-132">Windows 2000 Server</span></span>



| <span data-ttu-id="f0035-133">Voce</span><span class="sxs-lookup"><span data-stu-id="f0035-133">Entry</span></span> | <span data-ttu-id="f0035-134">Valore</span><span class="sxs-lookup"><span data-stu-id="f0035-134">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="f0035-135">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="f0035-135">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="f0035-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f0035-136">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="f0035-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="f0035-137">System-Only</span></span>            | <span data-ttu-id="f0035-138">Falso</span><span class="sxs-lookup"><span data-stu-id="f0035-138">False</span></span>                                      |
| <span data-ttu-id="f0035-139">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="f0035-139">Is-Single-Valued</span></span>       | <span data-ttu-id="f0035-140">Vero</span><span class="sxs-lookup"><span data-stu-id="f0035-140">True</span></span>                                       |
| <span data-ttu-id="f0035-141">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="f0035-141">Is Indexed</span></span>             | <span data-ttu-id="f0035-142">Falso</span><span class="sxs-lookup"><span data-stu-id="f0035-142">False</span></span>                                      |
| <span data-ttu-id="f0035-143">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="f0035-143">In Global Catalog</span></span>      | <span data-ttu-id="f0035-144">Falso</span><span class="sxs-lookup"><span data-stu-id="f0035-144">False</span></span>                                      |
| <span data-ttu-id="f0035-145">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="f0035-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="f0035-146">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="f0035-146">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="f0035-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f0035-147">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="f0035-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f0035-148">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="f0035-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f0035-149">Search-Flags</span></span>           | <span data-ttu-id="f0035-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f0035-150">0x00000000</span></span>                                 |
| <span data-ttu-id="f0035-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f0035-151">System-Flags</span></span>           | <span data-ttu-id="f0035-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f0035-152">0x00000010</span></span>                                 |
| <span data-ttu-id="f0035-153">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="f0035-153">Classes used in</span></span>        | [<span data-ttu-id="f0035-154">**Riferimento incrociato**</span><span class="sxs-lookup"><span data-stu-id="f0035-154">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="f0035-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f0035-155">Windows Server 2003</span></span>



| <span data-ttu-id="f0035-156">Voce</span><span class="sxs-lookup"><span data-stu-id="f0035-156">Entry</span></span> | <span data-ttu-id="f0035-157">Valore</span><span class="sxs-lookup"><span data-stu-id="f0035-157">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="f0035-158">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="f0035-158">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="f0035-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f0035-159">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="f0035-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="f0035-160">System-Only</span></span>            | <span data-ttu-id="f0035-161">Falso</span><span class="sxs-lookup"><span data-stu-id="f0035-161">False</span></span>                                      |
| <span data-ttu-id="f0035-162">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="f0035-162">Is-Single-Valued</span></span>       | <span data-ttu-id="f0035-163">Vero</span><span class="sxs-lookup"><span data-stu-id="f0035-163">True</span></span>                                       |
| <span data-ttu-id="f0035-164">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="f0035-164">Is Indexed</span></span>             | <span data-ttu-id="f0035-165">Falso</span><span class="sxs-lookup"><span data-stu-id="f0035-165">False</span></span>                                      |
| <span data-ttu-id="f0035-166">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="f0035-166">In Global Catalog</span></span>      | <span data-ttu-id="f0035-167">Falso</span><span class="sxs-lookup"><span data-stu-id="f0035-167">False</span></span>                                      |
| <span data-ttu-id="f0035-168">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="f0035-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="f0035-169">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="f0035-169">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="f0035-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f0035-170">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="f0035-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f0035-171">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="f0035-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f0035-172">Search-Flags</span></span>           | <span data-ttu-id="f0035-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f0035-173">0x00000000</span></span>                                 |
| <span data-ttu-id="f0035-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f0035-174">System-Flags</span></span>           | <span data-ttu-id="f0035-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f0035-175">0x00000010</span></span>                                 |
| <span data-ttu-id="f0035-176">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="f0035-176">Classes used in</span></span>        | [<span data-ttu-id="f0035-177">**Riferimento incrociato**</span><span class="sxs-lookup"><span data-stu-id="f0035-177">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="adam"></a><span data-ttu-id="f0035-178">ADAM</span><span class="sxs-lookup"><span data-stu-id="f0035-178">ADAM</span></span>



| <span data-ttu-id="f0035-179">Voce</span><span class="sxs-lookup"><span data-stu-id="f0035-179">Entry</span></span> | <span data-ttu-id="f0035-180">Valore</span><span class="sxs-lookup"><span data-stu-id="f0035-180">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="f0035-181">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="f0035-181">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="f0035-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f0035-182">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="f0035-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="f0035-183">System-Only</span></span>            | <span data-ttu-id="f0035-184">Falso</span><span class="sxs-lookup"><span data-stu-id="f0035-184">False</span></span>                                      |
| <span data-ttu-id="f0035-185">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="f0035-185">Is-Single-Valued</span></span>       | <span data-ttu-id="f0035-186">Vero</span><span class="sxs-lookup"><span data-stu-id="f0035-186">True</span></span>                                       |
| <span data-ttu-id="f0035-187">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="f0035-187">Is Indexed</span></span>             | <span data-ttu-id="f0035-188">Falso</span><span class="sxs-lookup"><span data-stu-id="f0035-188">False</span></span>                                      |
| <span data-ttu-id="f0035-189">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="f0035-189">In Global Catalog</span></span>      | <span data-ttu-id="f0035-190">Falso</span><span class="sxs-lookup"><span data-stu-id="f0035-190">False</span></span>                                      |
| <span data-ttu-id="f0035-191">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="f0035-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="f0035-192">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="f0035-192">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="f0035-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f0035-193">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="f0035-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f0035-194">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="f0035-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f0035-195">Search-Flags</span></span>           | <span data-ttu-id="f0035-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f0035-196">0x00000000</span></span>                                 |
| <span data-ttu-id="f0035-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f0035-197">System-Flags</span></span>           | <span data-ttu-id="f0035-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f0035-198">0x00000010</span></span>                                 |
| <span data-ttu-id="f0035-199">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="f0035-199">Classes used in</span></span>        | [<span data-ttu-id="f0035-200">**Riferimento incrociato**</span><span class="sxs-lookup"><span data-stu-id="f0035-200">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f0035-201">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f0035-201">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f0035-202">Voce</span><span class="sxs-lookup"><span data-stu-id="f0035-202">Entry</span></span> | <span data-ttu-id="f0035-203">Valore</span><span class="sxs-lookup"><span data-stu-id="f0035-203">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="f0035-204">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="f0035-204">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="f0035-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f0035-205">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="f0035-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="f0035-206">System-Only</span></span>            | <span data-ttu-id="f0035-207">Falso</span><span class="sxs-lookup"><span data-stu-id="f0035-207">False</span></span>                                      |
| <span data-ttu-id="f0035-208">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="f0035-208">Is-Single-Valued</span></span>       | <span data-ttu-id="f0035-209">Vero</span><span class="sxs-lookup"><span data-stu-id="f0035-209">True</span></span>                                       |
| <span data-ttu-id="f0035-210">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="f0035-210">Is Indexed</span></span>             | <span data-ttu-id="f0035-211">Falso</span><span class="sxs-lookup"><span data-stu-id="f0035-211">False</span></span>                                      |
| <span data-ttu-id="f0035-212">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="f0035-212">In Global Catalog</span></span>      | <span data-ttu-id="f0035-213">Falso</span><span class="sxs-lookup"><span data-stu-id="f0035-213">False</span></span>                                      |
| <span data-ttu-id="f0035-214">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="f0035-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="f0035-215">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="f0035-215">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="f0035-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f0035-216">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="f0035-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f0035-217">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="f0035-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f0035-218">Search-Flags</span></span>           | <span data-ttu-id="f0035-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f0035-219">0x00000000</span></span>                                 |
| <span data-ttu-id="f0035-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f0035-220">System-Flags</span></span>           | <span data-ttu-id="f0035-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f0035-221">0x00000010</span></span>                                 |
| <span data-ttu-id="f0035-222">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="f0035-222">Classes used in</span></span>        | [<span data-ttu-id="f0035-223">**Riferimento incrociato**</span><span class="sxs-lookup"><span data-stu-id="f0035-223">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f0035-224">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f0035-224">Windows Server 2008</span></span>



| <span data-ttu-id="f0035-225">Voce</span><span class="sxs-lookup"><span data-stu-id="f0035-225">Entry</span></span> | <span data-ttu-id="f0035-226">Valore</span><span class="sxs-lookup"><span data-stu-id="f0035-226">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="f0035-227">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="f0035-227">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="f0035-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f0035-228">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="f0035-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="f0035-229">System-Only</span></span>            | <span data-ttu-id="f0035-230">Falso</span><span class="sxs-lookup"><span data-stu-id="f0035-230">False</span></span>                                      |
| <span data-ttu-id="f0035-231">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="f0035-231">Is-Single-Valued</span></span>       | <span data-ttu-id="f0035-232">Vero</span><span class="sxs-lookup"><span data-stu-id="f0035-232">True</span></span>                                       |
| <span data-ttu-id="f0035-233">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="f0035-233">Is Indexed</span></span>             | <span data-ttu-id="f0035-234">Falso</span><span class="sxs-lookup"><span data-stu-id="f0035-234">False</span></span>                                      |
| <span data-ttu-id="f0035-235">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="f0035-235">In Global Catalog</span></span>      | <span data-ttu-id="f0035-236">Falso</span><span class="sxs-lookup"><span data-stu-id="f0035-236">False</span></span>                                      |
| <span data-ttu-id="f0035-237">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="f0035-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="f0035-238">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="f0035-238">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="f0035-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f0035-239">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="f0035-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f0035-240">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="f0035-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f0035-241">Search-Flags</span></span>           | <span data-ttu-id="f0035-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f0035-242">0x00000000</span></span>                                 |
| <span data-ttu-id="f0035-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f0035-243">System-Flags</span></span>           | <span data-ttu-id="f0035-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f0035-244">0x00000010</span></span>                                 |
| <span data-ttu-id="f0035-245">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="f0035-245">Classes used in</span></span>        | [<span data-ttu-id="f0035-246">**Riferimento incrociato**</span><span class="sxs-lookup"><span data-stu-id="f0035-246">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f0035-247">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f0035-247">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f0035-248">Voce</span><span class="sxs-lookup"><span data-stu-id="f0035-248">Entry</span></span> | <span data-ttu-id="f0035-249">Valore</span><span class="sxs-lookup"><span data-stu-id="f0035-249">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="f0035-250">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="f0035-250">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="f0035-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f0035-251">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="f0035-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="f0035-252">System-Only</span></span>            | <span data-ttu-id="f0035-253">Falso</span><span class="sxs-lookup"><span data-stu-id="f0035-253">False</span></span>                                      |
| <span data-ttu-id="f0035-254">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="f0035-254">Is-Single-Valued</span></span>       | <span data-ttu-id="f0035-255">Vero</span><span class="sxs-lookup"><span data-stu-id="f0035-255">True</span></span>                                       |
| <span data-ttu-id="f0035-256">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="f0035-256">Is Indexed</span></span>             | <span data-ttu-id="f0035-257">Falso</span><span class="sxs-lookup"><span data-stu-id="f0035-257">False</span></span>                                      |
| <span data-ttu-id="f0035-258">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="f0035-258">In Global Catalog</span></span>      | <span data-ttu-id="f0035-259">Falso</span><span class="sxs-lookup"><span data-stu-id="f0035-259">False</span></span>                                      |
| <span data-ttu-id="f0035-260">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="f0035-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="f0035-261">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="f0035-261">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="f0035-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f0035-262">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="f0035-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f0035-263">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="f0035-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f0035-264">Search-Flags</span></span>           | <span data-ttu-id="f0035-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f0035-265">0x00000000</span></span>                                 |
| <span data-ttu-id="f0035-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f0035-266">System-Flags</span></span>           | <span data-ttu-id="f0035-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f0035-267">0x00000010</span></span>                                 |
| <span data-ttu-id="f0035-268">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="f0035-268">Classes used in</span></span>        | [<span data-ttu-id="f0035-269">**Riferimento incrociato**</span><span class="sxs-lookup"><span data-stu-id="f0035-269">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f0035-270">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f0035-270">Windows Server 2012</span></span>



| <span data-ttu-id="f0035-271">Voce</span><span class="sxs-lookup"><span data-stu-id="f0035-271">Entry</span></span> | <span data-ttu-id="f0035-272">Valore</span><span class="sxs-lookup"><span data-stu-id="f0035-272">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="f0035-273">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="f0035-273">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="f0035-274">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f0035-274">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="f0035-275">System-Only</span><span class="sxs-lookup"><span data-stu-id="f0035-275">System-Only</span></span>            | <span data-ttu-id="f0035-276">Falso</span><span class="sxs-lookup"><span data-stu-id="f0035-276">False</span></span>                                      |
| <span data-ttu-id="f0035-277">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="f0035-277">Is-Single-Valued</span></span>       | <span data-ttu-id="f0035-278">Vero</span><span class="sxs-lookup"><span data-stu-id="f0035-278">True</span></span>                                       |
| <span data-ttu-id="f0035-279">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="f0035-279">Is Indexed</span></span>             | <span data-ttu-id="f0035-280">Falso</span><span class="sxs-lookup"><span data-stu-id="f0035-280">False</span></span>                                      |
| <span data-ttu-id="f0035-281">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="f0035-281">In Global Catalog</span></span>      | <span data-ttu-id="f0035-282">Falso</span><span class="sxs-lookup"><span data-stu-id="f0035-282">False</span></span>                                      |
| <span data-ttu-id="f0035-283">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="f0035-283">NT-Security-Descriptor</span></span> | <span data-ttu-id="f0035-284">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="f0035-284">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="f0035-285">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f0035-285">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="f0035-286">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f0035-286">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="f0035-287">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f0035-287">Search-Flags</span></span>           | <span data-ttu-id="f0035-288">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f0035-288">0x00000000</span></span>                                 |
| <span data-ttu-id="f0035-289">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f0035-289">System-Flags</span></span>           | <span data-ttu-id="f0035-290">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f0035-290">0x00000010</span></span>                                 |
| <span data-ttu-id="f0035-291">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="f0035-291">Classes used in</span></span>        | [<span data-ttu-id="f0035-292">**Riferimento incrociato**</span><span class="sxs-lookup"><span data-stu-id="f0035-292">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



 

 





