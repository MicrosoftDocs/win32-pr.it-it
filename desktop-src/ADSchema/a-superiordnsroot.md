---
title: Superior-DNS-attributo radice
description: Si tratta di un attributo di sistema usato per la generazione dei riferimenti.
ms.assetid: 421f8315-26e2-457d-ae76-868b7fc6551a
ms.tgt_platform: multiple
keywords:
- Superiore-DNS-schema AD attributo radice
- Schema AD dell'attributo superiorDNSRoot
topic_type:
- apiref
api_name:
- Superior-DNS-Root
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6561839cf5137968adbac628ad6046b8b86dab85
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "106303358"
---
# <a name="superior-dns-root-attribute"></a><span data-ttu-id="e4ba6-105">Superior-DNS-attributo radice</span><span class="sxs-lookup"><span data-stu-id="e4ba6-105">Superior-DNS-Root attribute</span></span>

<span data-ttu-id="e4ba6-106">Si tratta di un attributo di sistema usato per la generazione dei riferimenti.</span><span class="sxs-lookup"><span data-stu-id="e4ba6-106">This is a system attribute that is used for referrals generation.</span></span>



| <span data-ttu-id="e4ba6-107">Voce</span><span class="sxs-lookup"><span data-stu-id="e4ba6-107">Entry</span></span> | <span data-ttu-id="e4ba6-108">Valore</span><span class="sxs-lookup"><span data-stu-id="e4ba6-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="e4ba6-109">CN</span><span class="sxs-lookup"><span data-stu-id="e4ba6-109">CN</span></span>                | <span data-ttu-id="e4ba6-110">Superiore-DNS-radice</span><span class="sxs-lookup"><span data-stu-id="e4ba6-110">Superior-DNS-Root</span></span>                           |
| <span data-ttu-id="e4ba6-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="e4ba6-111">Ldap-Display-Name</span></span> | <span data-ttu-id="e4ba6-112">superiorDNSRoot</span><span class="sxs-lookup"><span data-stu-id="e4ba6-112">superiorDNSRoot</span></span>                             |
| <span data-ttu-id="e4ba6-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="e4ba6-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="e4ba6-114">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="e4ba6-114">Update Privilege</span></span>  | <span data-ttu-id="e4ba6-115">Questo valore viene impostato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="e4ba6-115">This value is set by the system.</span></span>            |
| <span data-ttu-id="e4ba6-116">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="e4ba6-116">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="e4ba6-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e4ba6-117">Attribute-Id</span></span>      | <span data-ttu-id="e4ba6-118">1.2.840.113556.1.4.532</span><span class="sxs-lookup"><span data-stu-id="e4ba6-118">1.2.840.113556.1.4.532</span></span>                      |
| <span data-ttu-id="e4ba6-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="e4ba6-119">System-Id-Guid</span></span>    | <span data-ttu-id="e4ba6-120">5245801d-ca6a-11d0-afff-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="e4ba6-120">5245801d-ca6a-11d0-afff-0000f80367c1</span></span>        |
| <span data-ttu-id="e4ba6-121">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e4ba6-121">Syntax</span></span>            | [<span data-ttu-id="e4ba6-122">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="e4ba6-122">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="e4ba6-123">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="e4ba6-123">Implementations</span></span>

-   [<span data-ttu-id="e4ba6-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="e4ba6-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="e4ba6-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e4ba6-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e4ba6-126">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="e4ba6-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="e4ba6-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e4ba6-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e4ba6-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e4ba6-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e4ba6-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e4ba6-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e4ba6-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e4ba6-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="e4ba6-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e4ba6-131">Windows 2000 Server</span></span>



| <span data-ttu-id="e4ba6-132">Voce</span><span class="sxs-lookup"><span data-stu-id="e4ba6-132">Entry</span></span> | <span data-ttu-id="e4ba6-133">Valore</span><span class="sxs-lookup"><span data-stu-id="e4ba6-133">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="e4ba6-134">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="e4ba6-134">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="e4ba6-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e4ba6-135">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="e4ba6-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="e4ba6-136">System-Only</span></span>            | <span data-ttu-id="e4ba6-137">Falso</span><span class="sxs-lookup"><span data-stu-id="e4ba6-137">False</span></span>                                      |
| <span data-ttu-id="e4ba6-138">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="e4ba6-138">Is-Single-Valued</span></span>       | <span data-ttu-id="e4ba6-139">Vero</span><span class="sxs-lookup"><span data-stu-id="e4ba6-139">True</span></span>                                       |
| <span data-ttu-id="e4ba6-140">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="e4ba6-140">Is Indexed</span></span>             | <span data-ttu-id="e4ba6-141">Falso</span><span class="sxs-lookup"><span data-stu-id="e4ba6-141">False</span></span>                                      |
| <span data-ttu-id="e4ba6-142">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="e4ba6-142">In Global Catalog</span></span>      | <span data-ttu-id="e4ba6-143">Falso</span><span class="sxs-lookup"><span data-stu-id="e4ba6-143">False</span></span>                                      |
| <span data-ttu-id="e4ba6-144">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="e4ba6-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="e4ba6-145">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="e4ba6-145">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="e4ba6-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e4ba6-146">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="e4ba6-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e4ba6-147">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="e4ba6-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e4ba6-148">Search-Flags</span></span>           | <span data-ttu-id="e4ba6-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e4ba6-149">0x00000000</span></span>                                 |
| <span data-ttu-id="e4ba6-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e4ba6-150">System-Flags</span></span>           | <span data-ttu-id="e4ba6-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e4ba6-151">0x00000010</span></span>                                 |
| <span data-ttu-id="e4ba6-152">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="e4ba6-152">Classes used in</span></span>        | [<span data-ttu-id="e4ba6-153">**Riferimento incrociato**</span><span class="sxs-lookup"><span data-stu-id="e4ba6-153">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="e4ba6-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e4ba6-154">Windows Server 2003</span></span>



| <span data-ttu-id="e4ba6-155">Voce</span><span class="sxs-lookup"><span data-stu-id="e4ba6-155">Entry</span></span> | <span data-ttu-id="e4ba6-156">Valore</span><span class="sxs-lookup"><span data-stu-id="e4ba6-156">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="e4ba6-157">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="e4ba6-157">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="e4ba6-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e4ba6-158">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="e4ba6-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="e4ba6-159">System-Only</span></span>            | <span data-ttu-id="e4ba6-160">Falso</span><span class="sxs-lookup"><span data-stu-id="e4ba6-160">False</span></span>                                      |
| <span data-ttu-id="e4ba6-161">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="e4ba6-161">Is-Single-Valued</span></span>       | <span data-ttu-id="e4ba6-162">Vero</span><span class="sxs-lookup"><span data-stu-id="e4ba6-162">True</span></span>                                       |
| <span data-ttu-id="e4ba6-163">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="e4ba6-163">Is Indexed</span></span>             | <span data-ttu-id="e4ba6-164">Falso</span><span class="sxs-lookup"><span data-stu-id="e4ba6-164">False</span></span>                                      |
| <span data-ttu-id="e4ba6-165">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="e4ba6-165">In Global Catalog</span></span>      | <span data-ttu-id="e4ba6-166">Falso</span><span class="sxs-lookup"><span data-stu-id="e4ba6-166">False</span></span>                                      |
| <span data-ttu-id="e4ba6-167">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="e4ba6-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="e4ba6-168">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="e4ba6-168">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="e4ba6-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e4ba6-169">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="e4ba6-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e4ba6-170">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="e4ba6-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e4ba6-171">Search-Flags</span></span>           | <span data-ttu-id="e4ba6-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e4ba6-172">0x00000000</span></span>                                 |
| <span data-ttu-id="e4ba6-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e4ba6-173">System-Flags</span></span>           | <span data-ttu-id="e4ba6-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e4ba6-174">0x00000010</span></span>                                 |
| <span data-ttu-id="e4ba6-175">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="e4ba6-175">Classes used in</span></span>        | [<span data-ttu-id="e4ba6-176">**Riferimento incrociato**</span><span class="sxs-lookup"><span data-stu-id="e4ba6-176">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="adam"></a><span data-ttu-id="e4ba6-177">ADAM</span><span class="sxs-lookup"><span data-stu-id="e4ba6-177">ADAM</span></span>



| <span data-ttu-id="e4ba6-178">Voce</span><span class="sxs-lookup"><span data-stu-id="e4ba6-178">Entry</span></span> | <span data-ttu-id="e4ba6-179">Valore</span><span class="sxs-lookup"><span data-stu-id="e4ba6-179">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="e4ba6-180">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="e4ba6-180">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="e4ba6-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e4ba6-181">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="e4ba6-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="e4ba6-182">System-Only</span></span>            | <span data-ttu-id="e4ba6-183">Falso</span><span class="sxs-lookup"><span data-stu-id="e4ba6-183">False</span></span>                                      |
| <span data-ttu-id="e4ba6-184">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="e4ba6-184">Is-Single-Valued</span></span>       | <span data-ttu-id="e4ba6-185">Vero</span><span class="sxs-lookup"><span data-stu-id="e4ba6-185">True</span></span>                                       |
| <span data-ttu-id="e4ba6-186">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="e4ba6-186">Is Indexed</span></span>             | <span data-ttu-id="e4ba6-187">Falso</span><span class="sxs-lookup"><span data-stu-id="e4ba6-187">False</span></span>                                      |
| <span data-ttu-id="e4ba6-188">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="e4ba6-188">In Global Catalog</span></span>      | <span data-ttu-id="e4ba6-189">Falso</span><span class="sxs-lookup"><span data-stu-id="e4ba6-189">False</span></span>                                      |
| <span data-ttu-id="e4ba6-190">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="e4ba6-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="e4ba6-191">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="e4ba6-191">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="e4ba6-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e4ba6-192">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="e4ba6-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e4ba6-193">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="e4ba6-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e4ba6-194">Search-Flags</span></span>           | <span data-ttu-id="e4ba6-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e4ba6-195">0x00000000</span></span>                                 |
| <span data-ttu-id="e4ba6-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e4ba6-196">System-Flags</span></span>           | <span data-ttu-id="e4ba6-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e4ba6-197">0x00000010</span></span>                                 |
| <span data-ttu-id="e4ba6-198">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="e4ba6-198">Classes used in</span></span>        | [<span data-ttu-id="e4ba6-199">**Riferimento incrociato**</span><span class="sxs-lookup"><span data-stu-id="e4ba6-199">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e4ba6-200">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e4ba6-200">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e4ba6-201">Voce</span><span class="sxs-lookup"><span data-stu-id="e4ba6-201">Entry</span></span> | <span data-ttu-id="e4ba6-202">Valore</span><span class="sxs-lookup"><span data-stu-id="e4ba6-202">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="e4ba6-203">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="e4ba6-203">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="e4ba6-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e4ba6-204">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="e4ba6-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="e4ba6-205">System-Only</span></span>            | <span data-ttu-id="e4ba6-206">Falso</span><span class="sxs-lookup"><span data-stu-id="e4ba6-206">False</span></span>                                      |
| <span data-ttu-id="e4ba6-207">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="e4ba6-207">Is-Single-Valued</span></span>       | <span data-ttu-id="e4ba6-208">Vero</span><span class="sxs-lookup"><span data-stu-id="e4ba6-208">True</span></span>                                       |
| <span data-ttu-id="e4ba6-209">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="e4ba6-209">Is Indexed</span></span>             | <span data-ttu-id="e4ba6-210">Falso</span><span class="sxs-lookup"><span data-stu-id="e4ba6-210">False</span></span>                                      |
| <span data-ttu-id="e4ba6-211">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="e4ba6-211">In Global Catalog</span></span>      | <span data-ttu-id="e4ba6-212">Falso</span><span class="sxs-lookup"><span data-stu-id="e4ba6-212">False</span></span>                                      |
| <span data-ttu-id="e4ba6-213">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="e4ba6-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="e4ba6-214">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="e4ba6-214">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="e4ba6-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e4ba6-215">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="e4ba6-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e4ba6-216">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="e4ba6-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e4ba6-217">Search-Flags</span></span>           | <span data-ttu-id="e4ba6-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e4ba6-218">0x00000000</span></span>                                 |
| <span data-ttu-id="e4ba6-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e4ba6-219">System-Flags</span></span>           | <span data-ttu-id="e4ba6-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e4ba6-220">0x00000010</span></span>                                 |
| <span data-ttu-id="e4ba6-221">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="e4ba6-221">Classes used in</span></span>        | [<span data-ttu-id="e4ba6-222">**Riferimento incrociato**</span><span class="sxs-lookup"><span data-stu-id="e4ba6-222">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="e4ba6-223">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e4ba6-223">Windows Server 2008</span></span>



| <span data-ttu-id="e4ba6-224">Voce</span><span class="sxs-lookup"><span data-stu-id="e4ba6-224">Entry</span></span> | <span data-ttu-id="e4ba6-225">Valore</span><span class="sxs-lookup"><span data-stu-id="e4ba6-225">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="e4ba6-226">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="e4ba6-226">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="e4ba6-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e4ba6-227">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="e4ba6-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="e4ba6-228">System-Only</span></span>            | <span data-ttu-id="e4ba6-229">Falso</span><span class="sxs-lookup"><span data-stu-id="e4ba6-229">False</span></span>                                      |
| <span data-ttu-id="e4ba6-230">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="e4ba6-230">Is-Single-Valued</span></span>       | <span data-ttu-id="e4ba6-231">Vero</span><span class="sxs-lookup"><span data-stu-id="e4ba6-231">True</span></span>                                       |
| <span data-ttu-id="e4ba6-232">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="e4ba6-232">Is Indexed</span></span>             | <span data-ttu-id="e4ba6-233">Falso</span><span class="sxs-lookup"><span data-stu-id="e4ba6-233">False</span></span>                                      |
| <span data-ttu-id="e4ba6-234">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="e4ba6-234">In Global Catalog</span></span>      | <span data-ttu-id="e4ba6-235">Falso</span><span class="sxs-lookup"><span data-stu-id="e4ba6-235">False</span></span>                                      |
| <span data-ttu-id="e4ba6-236">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="e4ba6-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="e4ba6-237">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="e4ba6-237">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="e4ba6-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e4ba6-238">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="e4ba6-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e4ba6-239">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="e4ba6-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e4ba6-240">Search-Flags</span></span>           | <span data-ttu-id="e4ba6-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e4ba6-241">0x00000000</span></span>                                 |
| <span data-ttu-id="e4ba6-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e4ba6-242">System-Flags</span></span>           | <span data-ttu-id="e4ba6-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e4ba6-243">0x00000010</span></span>                                 |
| <span data-ttu-id="e4ba6-244">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="e4ba6-244">Classes used in</span></span>        | [<span data-ttu-id="e4ba6-245">**Riferimento incrociato**</span><span class="sxs-lookup"><span data-stu-id="e4ba6-245">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e4ba6-246">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e4ba6-246">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e4ba6-247">Voce</span><span class="sxs-lookup"><span data-stu-id="e4ba6-247">Entry</span></span> | <span data-ttu-id="e4ba6-248">Valore</span><span class="sxs-lookup"><span data-stu-id="e4ba6-248">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="e4ba6-249">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="e4ba6-249">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="e4ba6-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e4ba6-250">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="e4ba6-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="e4ba6-251">System-Only</span></span>            | <span data-ttu-id="e4ba6-252">Falso</span><span class="sxs-lookup"><span data-stu-id="e4ba6-252">False</span></span>                                      |
| <span data-ttu-id="e4ba6-253">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="e4ba6-253">Is-Single-Valued</span></span>       | <span data-ttu-id="e4ba6-254">Vero</span><span class="sxs-lookup"><span data-stu-id="e4ba6-254">True</span></span>                                       |
| <span data-ttu-id="e4ba6-255">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="e4ba6-255">Is Indexed</span></span>             | <span data-ttu-id="e4ba6-256">Falso</span><span class="sxs-lookup"><span data-stu-id="e4ba6-256">False</span></span>                                      |
| <span data-ttu-id="e4ba6-257">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="e4ba6-257">In Global Catalog</span></span>      | <span data-ttu-id="e4ba6-258">Falso</span><span class="sxs-lookup"><span data-stu-id="e4ba6-258">False</span></span>                                      |
| <span data-ttu-id="e4ba6-259">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="e4ba6-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="e4ba6-260">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="e4ba6-260">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="e4ba6-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e4ba6-261">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="e4ba6-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e4ba6-262">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="e4ba6-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e4ba6-263">Search-Flags</span></span>           | <span data-ttu-id="e4ba6-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e4ba6-264">0x00000000</span></span>                                 |
| <span data-ttu-id="e4ba6-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e4ba6-265">System-Flags</span></span>           | <span data-ttu-id="e4ba6-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e4ba6-266">0x00000010</span></span>                                 |
| <span data-ttu-id="e4ba6-267">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="e4ba6-267">Classes used in</span></span>        | [<span data-ttu-id="e4ba6-268">**Riferimento incrociato**</span><span class="sxs-lookup"><span data-stu-id="e4ba6-268">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e4ba6-269">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e4ba6-269">Windows Server 2012</span></span>



| <span data-ttu-id="e4ba6-270">Voce</span><span class="sxs-lookup"><span data-stu-id="e4ba6-270">Entry</span></span> | <span data-ttu-id="e4ba6-271">Valore</span><span class="sxs-lookup"><span data-stu-id="e4ba6-271">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="e4ba6-272">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="e4ba6-272">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="e4ba6-273">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e4ba6-273">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="e4ba6-274">System-Only</span><span class="sxs-lookup"><span data-stu-id="e4ba6-274">System-Only</span></span>            | <span data-ttu-id="e4ba6-275">Falso</span><span class="sxs-lookup"><span data-stu-id="e4ba6-275">False</span></span>                                      |
| <span data-ttu-id="e4ba6-276">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="e4ba6-276">Is-Single-Valued</span></span>       | <span data-ttu-id="e4ba6-277">Vero</span><span class="sxs-lookup"><span data-stu-id="e4ba6-277">True</span></span>                                       |
| <span data-ttu-id="e4ba6-278">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="e4ba6-278">Is Indexed</span></span>             | <span data-ttu-id="e4ba6-279">Falso</span><span class="sxs-lookup"><span data-stu-id="e4ba6-279">False</span></span>                                      |
| <span data-ttu-id="e4ba6-280">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="e4ba6-280">In Global Catalog</span></span>      | <span data-ttu-id="e4ba6-281">Falso</span><span class="sxs-lookup"><span data-stu-id="e4ba6-281">False</span></span>                                      |
| <span data-ttu-id="e4ba6-282">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="e4ba6-282">NT-Security-Descriptor</span></span> | <span data-ttu-id="e4ba6-283">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="e4ba6-283">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="e4ba6-284">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e4ba6-284">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="e4ba6-285">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e4ba6-285">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="e4ba6-286">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e4ba6-286">Search-Flags</span></span>           | <span data-ttu-id="e4ba6-287">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e4ba6-287">0x00000000</span></span>                                 |
| <span data-ttu-id="e4ba6-288">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e4ba6-288">System-Flags</span></span>           | <span data-ttu-id="e4ba6-289">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e4ba6-289">0x00000010</span></span>                                 |
| <span data-ttu-id="e4ba6-290">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="e4ba6-290">Classes used in</span></span>        | [<span data-ttu-id="e4ba6-291">**Riferimento incrociato**</span><span class="sxs-lookup"><span data-stu-id="e4ba6-291">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



 

 





