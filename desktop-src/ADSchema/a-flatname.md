---
title: Attributo Flat-Name
description: Per i domini Windows NT, il nome Flat è il nome NetBIOS. Per i collegamenti con non \ 8211; Domini di Windows NT, il nome Flat è il nome di identificazione del dominio o è NULL.
ms.assetid: ec368657-a0e7-4416-ab80-1d18d98bbcfa
ms.tgt_platform: multiple
keywords:
- Schema AD Flat-Name attribute
- Schema AD dell'attributo flatName
topic_type:
- apiref
api_name:
- Flat-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 373ee0736c051932fdb6dd20701f0c5ec353ad3b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104479792"
---
# <a name="flat-name-attribute"></a><span data-ttu-id="341b8-106">Attributo Flat-Name</span><span class="sxs-lookup"><span data-stu-id="341b8-106">Flat-Name attribute</span></span>

<span data-ttu-id="341b8-107">Per i domini Windows NT, il nome Flat è il nome NetBIOS.</span><span class="sxs-lookup"><span data-stu-id="341b8-107">For Windows NT domains, the flat name is the NetBIOS name.</span></span> <span data-ttu-id="341b8-108">Per i collegamenti con domini non Windows NT, il nome Flat è il nome di identificazione del dominio o è **null**.</span><span class="sxs-lookup"><span data-stu-id="341b8-108">For links with non Windows NT domains, the flat name is the identifying name of that domain, or it is **NULL**.</span></span>



| <span data-ttu-id="341b8-109">Voce</span><span class="sxs-lookup"><span data-stu-id="341b8-109">Entry</span></span> | <span data-ttu-id="341b8-110">Valore</span><span class="sxs-lookup"><span data-stu-id="341b8-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="341b8-111">CN</span><span class="sxs-lookup"><span data-stu-id="341b8-111">CN</span></span>                | <span data-ttu-id="341b8-112">Flat-Name</span><span class="sxs-lookup"><span data-stu-id="341b8-112">Flat-Name</span></span>                                   |
| <span data-ttu-id="341b8-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="341b8-113">Ldap-Display-Name</span></span> | <span data-ttu-id="341b8-114">flatName</span><span class="sxs-lookup"><span data-stu-id="341b8-114">flatName</span></span>                                    |
| <span data-ttu-id="341b8-115">Dimensione</span><span class="sxs-lookup"><span data-stu-id="341b8-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="341b8-116">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="341b8-116">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="341b8-117">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="341b8-117">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="341b8-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="341b8-118">Attribute-Id</span></span>      | <span data-ttu-id="341b8-119">1.2.840.113556.1.4.511</span><span class="sxs-lookup"><span data-stu-id="341b8-119">1.2.840.113556.1.4.511</span></span>                      |
| <span data-ttu-id="341b8-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="341b8-120">System-Id-Guid</span></span>    | <span data-ttu-id="341b8-121">b7b13117-b82e-11d0-afee-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="341b8-121">b7b13117-b82e-11d0-afee-0000f80367c1</span></span>        |
| <span data-ttu-id="341b8-122">Sintassi</span><span class="sxs-lookup"><span data-stu-id="341b8-122">Syntax</span></span>            | [<span data-ttu-id="341b8-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="341b8-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="341b8-124">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="341b8-124">Implementations</span></span>

-   [<span data-ttu-id="341b8-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="341b8-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="341b8-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="341b8-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="341b8-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="341b8-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="341b8-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="341b8-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="341b8-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="341b8-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="341b8-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="341b8-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="341b8-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="341b8-131">Windows 2000 Server</span></span>



| <span data-ttu-id="341b8-132">Voce</span><span class="sxs-lookup"><span data-stu-id="341b8-132">Entry</span></span> | <span data-ttu-id="341b8-133">Valore</span><span class="sxs-lookup"><span data-stu-id="341b8-133">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="341b8-134">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="341b8-134">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="341b8-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="341b8-135">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="341b8-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="341b8-136">System-Only</span></span>            | <span data-ttu-id="341b8-137">Falso</span><span class="sxs-lookup"><span data-stu-id="341b8-137">False</span></span>                                                |
| <span data-ttu-id="341b8-138">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="341b8-138">Is-Single-Valued</span></span>       | <span data-ttu-id="341b8-139">Vero</span><span class="sxs-lookup"><span data-stu-id="341b8-139">True</span></span>                                                 |
| <span data-ttu-id="341b8-140">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="341b8-140">Is Indexed</span></span>             | <span data-ttu-id="341b8-141">Vero</span><span class="sxs-lookup"><span data-stu-id="341b8-141">True</span></span>                                                 |
| <span data-ttu-id="341b8-142">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="341b8-142">In Global Catalog</span></span>      | <span data-ttu-id="341b8-143">Falso</span><span class="sxs-lookup"><span data-stu-id="341b8-143">False</span></span>                                                |
| <span data-ttu-id="341b8-144">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="341b8-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="341b8-145">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="341b8-145">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="341b8-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="341b8-146">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="341b8-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="341b8-147">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="341b8-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="341b8-148">Search-Flags</span></span>           | <span data-ttu-id="341b8-149">0x00000001</span><span class="sxs-lookup"><span data-stu-id="341b8-149">0x00000001</span></span>                                           |
| <span data-ttu-id="341b8-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="341b8-150">System-Flags</span></span>           | <span data-ttu-id="341b8-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="341b8-151">0x00000010</span></span>                                           |
| <span data-ttu-id="341b8-152">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="341b8-152">Classes used in</span></span>        | [<span data-ttu-id="341b8-153">**Dominio trusted**</span><span class="sxs-lookup"><span data-stu-id="341b8-153">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="341b8-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="341b8-154">Windows Server 2003</span></span>



| <span data-ttu-id="341b8-155">Voce</span><span class="sxs-lookup"><span data-stu-id="341b8-155">Entry</span></span> | <span data-ttu-id="341b8-156">Valore</span><span class="sxs-lookup"><span data-stu-id="341b8-156">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="341b8-157">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="341b8-157">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="341b8-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="341b8-158">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="341b8-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="341b8-159">System-Only</span></span>            | <span data-ttu-id="341b8-160">Falso</span><span class="sxs-lookup"><span data-stu-id="341b8-160">False</span></span>                                                |
| <span data-ttu-id="341b8-161">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="341b8-161">Is-Single-Valued</span></span>       | <span data-ttu-id="341b8-162">Vero</span><span class="sxs-lookup"><span data-stu-id="341b8-162">True</span></span>                                                 |
| <span data-ttu-id="341b8-163">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="341b8-163">Is Indexed</span></span>             | <span data-ttu-id="341b8-164">Vero</span><span class="sxs-lookup"><span data-stu-id="341b8-164">True</span></span>                                                 |
| <span data-ttu-id="341b8-165">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="341b8-165">In Global Catalog</span></span>      | <span data-ttu-id="341b8-166">Falso</span><span class="sxs-lookup"><span data-stu-id="341b8-166">False</span></span>                                                |
| <span data-ttu-id="341b8-167">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="341b8-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="341b8-168">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="341b8-168">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="341b8-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="341b8-169">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="341b8-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="341b8-170">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="341b8-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="341b8-171">Search-Flags</span></span>           | <span data-ttu-id="341b8-172">0x00000001</span><span class="sxs-lookup"><span data-stu-id="341b8-172">0x00000001</span></span>                                           |
| <span data-ttu-id="341b8-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="341b8-173">System-Flags</span></span>           | <span data-ttu-id="341b8-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="341b8-174">0x00000010</span></span>                                           |
| <span data-ttu-id="341b8-175">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="341b8-175">Classes used in</span></span>        | [<span data-ttu-id="341b8-176">**Dominio trusted**</span><span class="sxs-lookup"><span data-stu-id="341b8-176">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="341b8-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="341b8-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="341b8-178">Voce</span><span class="sxs-lookup"><span data-stu-id="341b8-178">Entry</span></span> | <span data-ttu-id="341b8-179">Valore</span><span class="sxs-lookup"><span data-stu-id="341b8-179">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="341b8-180">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="341b8-180">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="341b8-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="341b8-181">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="341b8-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="341b8-182">System-Only</span></span>            | <span data-ttu-id="341b8-183">Falso</span><span class="sxs-lookup"><span data-stu-id="341b8-183">False</span></span>                                                |
| <span data-ttu-id="341b8-184">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="341b8-184">Is-Single-Valued</span></span>       | <span data-ttu-id="341b8-185">Vero</span><span class="sxs-lookup"><span data-stu-id="341b8-185">True</span></span>                                                 |
| <span data-ttu-id="341b8-186">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="341b8-186">Is Indexed</span></span>             | <span data-ttu-id="341b8-187">Vero</span><span class="sxs-lookup"><span data-stu-id="341b8-187">True</span></span>                                                 |
| <span data-ttu-id="341b8-188">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="341b8-188">In Global Catalog</span></span>      | <span data-ttu-id="341b8-189">Falso</span><span class="sxs-lookup"><span data-stu-id="341b8-189">False</span></span>                                                |
| <span data-ttu-id="341b8-190">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="341b8-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="341b8-191">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="341b8-191">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="341b8-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="341b8-192">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="341b8-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="341b8-193">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="341b8-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="341b8-194">Search-Flags</span></span>           | <span data-ttu-id="341b8-195">0x00000001</span><span class="sxs-lookup"><span data-stu-id="341b8-195">0x00000001</span></span>                                           |
| <span data-ttu-id="341b8-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="341b8-196">System-Flags</span></span>           | <span data-ttu-id="341b8-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="341b8-197">0x00000010</span></span>                                           |
| <span data-ttu-id="341b8-198">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="341b8-198">Classes used in</span></span>        | [<span data-ttu-id="341b8-199">**Dominio trusted**</span><span class="sxs-lookup"><span data-stu-id="341b8-199">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="341b8-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="341b8-200">Windows Server 2008</span></span>



| <span data-ttu-id="341b8-201">Voce</span><span class="sxs-lookup"><span data-stu-id="341b8-201">Entry</span></span> | <span data-ttu-id="341b8-202">Valore</span><span class="sxs-lookup"><span data-stu-id="341b8-202">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="341b8-203">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="341b8-203">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="341b8-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="341b8-204">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="341b8-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="341b8-205">System-Only</span></span>            | <span data-ttu-id="341b8-206">Falso</span><span class="sxs-lookup"><span data-stu-id="341b8-206">False</span></span>                                                |
| <span data-ttu-id="341b8-207">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="341b8-207">Is-Single-Valued</span></span>       | <span data-ttu-id="341b8-208">Vero</span><span class="sxs-lookup"><span data-stu-id="341b8-208">True</span></span>                                                 |
| <span data-ttu-id="341b8-209">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="341b8-209">Is Indexed</span></span>             | <span data-ttu-id="341b8-210">Vero</span><span class="sxs-lookup"><span data-stu-id="341b8-210">True</span></span>                                                 |
| <span data-ttu-id="341b8-211">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="341b8-211">In Global Catalog</span></span>      | <span data-ttu-id="341b8-212">Falso</span><span class="sxs-lookup"><span data-stu-id="341b8-212">False</span></span>                                                |
| <span data-ttu-id="341b8-213">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="341b8-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="341b8-214">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="341b8-214">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="341b8-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="341b8-215">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="341b8-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="341b8-216">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="341b8-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="341b8-217">Search-Flags</span></span>           | <span data-ttu-id="341b8-218">0x00000001</span><span class="sxs-lookup"><span data-stu-id="341b8-218">0x00000001</span></span>                                           |
| <span data-ttu-id="341b8-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="341b8-219">System-Flags</span></span>           | <span data-ttu-id="341b8-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="341b8-220">0x00000010</span></span>                                           |
| <span data-ttu-id="341b8-221">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="341b8-221">Classes used in</span></span>        | [<span data-ttu-id="341b8-222">**Dominio trusted**</span><span class="sxs-lookup"><span data-stu-id="341b8-222">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="341b8-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="341b8-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="341b8-224">Voce</span><span class="sxs-lookup"><span data-stu-id="341b8-224">Entry</span></span> | <span data-ttu-id="341b8-225">Valore</span><span class="sxs-lookup"><span data-stu-id="341b8-225">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="341b8-226">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="341b8-226">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="341b8-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="341b8-227">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="341b8-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="341b8-228">System-Only</span></span>            | <span data-ttu-id="341b8-229">Falso</span><span class="sxs-lookup"><span data-stu-id="341b8-229">False</span></span>                                                |
| <span data-ttu-id="341b8-230">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="341b8-230">Is-Single-Valued</span></span>       | <span data-ttu-id="341b8-231">Vero</span><span class="sxs-lookup"><span data-stu-id="341b8-231">True</span></span>                                                 |
| <span data-ttu-id="341b8-232">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="341b8-232">Is Indexed</span></span>             | <span data-ttu-id="341b8-233">Vero</span><span class="sxs-lookup"><span data-stu-id="341b8-233">True</span></span>                                                 |
| <span data-ttu-id="341b8-234">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="341b8-234">In Global Catalog</span></span>      | <span data-ttu-id="341b8-235">Falso</span><span class="sxs-lookup"><span data-stu-id="341b8-235">False</span></span>                                                |
| <span data-ttu-id="341b8-236">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="341b8-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="341b8-237">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="341b8-237">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="341b8-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="341b8-238">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="341b8-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="341b8-239">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="341b8-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="341b8-240">Search-Flags</span></span>           | <span data-ttu-id="341b8-241">0x00000001</span><span class="sxs-lookup"><span data-stu-id="341b8-241">0x00000001</span></span>                                           |
| <span data-ttu-id="341b8-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="341b8-242">System-Flags</span></span>           | <span data-ttu-id="341b8-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="341b8-243">0x00000010</span></span>                                           |
| <span data-ttu-id="341b8-244">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="341b8-244">Classes used in</span></span>        | [<span data-ttu-id="341b8-245">**Dominio trusted**</span><span class="sxs-lookup"><span data-stu-id="341b8-245">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="341b8-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="341b8-246">Windows Server 2012</span></span>



| <span data-ttu-id="341b8-247">Voce</span><span class="sxs-lookup"><span data-stu-id="341b8-247">Entry</span></span> | <span data-ttu-id="341b8-248">Valore</span><span class="sxs-lookup"><span data-stu-id="341b8-248">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="341b8-249">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="341b8-249">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="341b8-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="341b8-250">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="341b8-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="341b8-251">System-Only</span></span>            | <span data-ttu-id="341b8-252">Falso</span><span class="sxs-lookup"><span data-stu-id="341b8-252">False</span></span>                                                |
| <span data-ttu-id="341b8-253">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="341b8-253">Is-Single-Valued</span></span>       | <span data-ttu-id="341b8-254">Vero</span><span class="sxs-lookup"><span data-stu-id="341b8-254">True</span></span>                                                 |
| <span data-ttu-id="341b8-255">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="341b8-255">Is Indexed</span></span>             | <span data-ttu-id="341b8-256">Vero</span><span class="sxs-lookup"><span data-stu-id="341b8-256">True</span></span>                                                 |
| <span data-ttu-id="341b8-257">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="341b8-257">In Global Catalog</span></span>      | <span data-ttu-id="341b8-258">Falso</span><span class="sxs-lookup"><span data-stu-id="341b8-258">False</span></span>                                                |
| <span data-ttu-id="341b8-259">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="341b8-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="341b8-260">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="341b8-260">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="341b8-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="341b8-261">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="341b8-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="341b8-262">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="341b8-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="341b8-263">Search-Flags</span></span>           | <span data-ttu-id="341b8-264">0x00000001</span><span class="sxs-lookup"><span data-stu-id="341b8-264">0x00000001</span></span>                                           |
| <span data-ttu-id="341b8-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="341b8-265">System-Flags</span></span>           | <span data-ttu-id="341b8-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="341b8-266">0x00000010</span></span>                                           |
| <span data-ttu-id="341b8-267">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="341b8-267">Classes used in</span></span>        | [<span data-ttu-id="341b8-268">**Dominio trusted**</span><span class="sxs-lookup"><span data-stu-id="341b8-268">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



 

 





