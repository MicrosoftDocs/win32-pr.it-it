---
title: attributo ms-DS-DnsRootAlias
description: Utilizzato per archiviare l'alias di dominio.
ms.assetid: 36b64363-947f-4af9-947f-eefead55bb02
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo ms-DS-DnsRootAlias
- attributo msDS-DnsRootAlias-schema AD
topic_type:
- apiref
api_name:
- ms-DS-DnsRootAlias
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f0b20b9316aaa9e68ab1ed907135c5640c1480f
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103745170"
---
# <a name="ms-ds-dnsrootalias-attribute"></a><span data-ttu-id="ece05-105">attributo ms-DS-DnsRootAlias</span><span class="sxs-lookup"><span data-stu-id="ece05-105">ms-DS-DnsRootAlias attribute</span></span>

<span data-ttu-id="ece05-106">Utilizzato per archiviare l'alias di dominio.</span><span class="sxs-lookup"><span data-stu-id="ece05-106">Used to store the domain alias.</span></span>



| <span data-ttu-id="ece05-107">Voce</span><span class="sxs-lookup"><span data-stu-id="ece05-107">Entry</span></span> | <span data-ttu-id="ece05-108">Valore</span><span class="sxs-lookup"><span data-stu-id="ece05-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="ece05-109">CN</span><span class="sxs-lookup"><span data-stu-id="ece05-109">CN</span></span>                | <span data-ttu-id="ece05-110">ms-DS-DnsRootAlias</span><span class="sxs-lookup"><span data-stu-id="ece05-110">ms-DS-DnsRootAlias</span></span>                          |
| <span data-ttu-id="ece05-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="ece05-111">Ldap-Display-Name</span></span> | <span data-ttu-id="ece05-112">msDS-DnsRootAlias</span><span class="sxs-lookup"><span data-stu-id="ece05-112">msDS-DnsRootAlias</span></span>                           |
| <span data-ttu-id="ece05-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="ece05-113">Size</span></span>              | <span data-ttu-id="ece05-114">Dimensioni massime di 255 byte.</span><span class="sxs-lookup"><span data-stu-id="ece05-114">Maximum size 255 bytes.</span></span>                     |
| <span data-ttu-id="ece05-115">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="ece05-115">Update Privilege</span></span>  | <span data-ttu-id="ece05-116">Questo valore viene impostato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="ece05-116">This value is set by the system.</span></span>            |
| <span data-ttu-id="ece05-117">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="ece05-117">Update Frequency</span></span>  | <span data-ttu-id="ece05-118">Solo durante la ristrutturazione del dominio.</span><span class="sxs-lookup"><span data-stu-id="ece05-118">Only during domain restructure.</span></span>             |
| <span data-ttu-id="ece05-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ece05-119">Attribute-Id</span></span>      | <span data-ttu-id="ece05-120">1.2.840.113556.1.4.1719</span><span class="sxs-lookup"><span data-stu-id="ece05-120">1.2.840.113556.1.4.1719</span></span>                     |
| <span data-ttu-id="ece05-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="ece05-121">System-Id-Guid</span></span>    | <span data-ttu-id="ece05-122">2143acca-eead-4d29-b591-85fa49ce9173</span><span class="sxs-lookup"><span data-stu-id="ece05-122">2143acca-eead-4d29-b591-85fa49ce9173</span></span>        |
| <span data-ttu-id="ece05-123">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ece05-123">Syntax</span></span>            | [<span data-ttu-id="ece05-124">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="ece05-124">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="ece05-125">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="ece05-125">Implementations</span></span>

-   [<span data-ttu-id="ece05-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ece05-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ece05-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="ece05-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="ece05-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ece05-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ece05-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ece05-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ece05-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ece05-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ece05-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ece05-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="ece05-132">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ece05-132">Windows Server 2003</span></span>



| <span data-ttu-id="ece05-133">Voce</span><span class="sxs-lookup"><span data-stu-id="ece05-133">Entry</span></span> | <span data-ttu-id="ece05-134">Valore</span><span class="sxs-lookup"><span data-stu-id="ece05-134">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="ece05-135">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="ece05-135">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="ece05-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ece05-136">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="ece05-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="ece05-137">System-Only</span></span>            | <span data-ttu-id="ece05-138">Falso</span><span class="sxs-lookup"><span data-stu-id="ece05-138">False</span></span>                                      |
| <span data-ttu-id="ece05-139">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="ece05-139">Is-Single-Valued</span></span>       | <span data-ttu-id="ece05-140">Vero</span><span class="sxs-lookup"><span data-stu-id="ece05-140">True</span></span>                                       |
| <span data-ttu-id="ece05-141">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="ece05-141">Is Indexed</span></span>             | <span data-ttu-id="ece05-142">Falso</span><span class="sxs-lookup"><span data-stu-id="ece05-142">False</span></span>                                      |
| <span data-ttu-id="ece05-143">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="ece05-143">In Global Catalog</span></span>      | <span data-ttu-id="ece05-144">Falso</span><span class="sxs-lookup"><span data-stu-id="ece05-144">False</span></span>                                      |
| <span data-ttu-id="ece05-145">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="ece05-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="ece05-146">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="ece05-146">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="ece05-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ece05-147">Range-Lower</span></span>            | <span data-ttu-id="ece05-148">0</span><span class="sxs-lookup"><span data-stu-id="ece05-148">0</span></span>                                          |
| <span data-ttu-id="ece05-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ece05-149">Range-Upper</span></span>            | <span data-ttu-id="ece05-150">255</span><span class="sxs-lookup"><span data-stu-id="ece05-150">255</span></span>                                        |
| <span data-ttu-id="ece05-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ece05-151">Search-Flags</span></span>           | <span data-ttu-id="ece05-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ece05-152">0x00000000</span></span>                                 |
| <span data-ttu-id="ece05-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ece05-153">System-Flags</span></span>           | <span data-ttu-id="ece05-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ece05-154">0x00000010</span></span>                                 |
| <span data-ttu-id="ece05-155">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="ece05-155">Classes used in</span></span>        | [<span data-ttu-id="ece05-156">**Riferimento incrociato**</span><span class="sxs-lookup"><span data-stu-id="ece05-156">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="adam"></a><span data-ttu-id="ece05-157">ADAM</span><span class="sxs-lookup"><span data-stu-id="ece05-157">ADAM</span></span>



| <span data-ttu-id="ece05-158">Voce</span><span class="sxs-lookup"><span data-stu-id="ece05-158">Entry</span></span> | <span data-ttu-id="ece05-159">Valore</span><span class="sxs-lookup"><span data-stu-id="ece05-159">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="ece05-160">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="ece05-160">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="ece05-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ece05-161">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="ece05-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="ece05-162">System-Only</span></span>            | <span data-ttu-id="ece05-163">Falso</span><span class="sxs-lookup"><span data-stu-id="ece05-163">False</span></span>                                      |
| <span data-ttu-id="ece05-164">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="ece05-164">Is-Single-Valued</span></span>       | <span data-ttu-id="ece05-165">Vero</span><span class="sxs-lookup"><span data-stu-id="ece05-165">True</span></span>                                       |
| <span data-ttu-id="ece05-166">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="ece05-166">Is Indexed</span></span>             | <span data-ttu-id="ece05-167">Falso</span><span class="sxs-lookup"><span data-stu-id="ece05-167">False</span></span>                                      |
| <span data-ttu-id="ece05-168">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="ece05-168">In Global Catalog</span></span>      | <span data-ttu-id="ece05-169">Falso</span><span class="sxs-lookup"><span data-stu-id="ece05-169">False</span></span>                                      |
| <span data-ttu-id="ece05-170">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="ece05-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="ece05-171">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="ece05-171">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="ece05-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ece05-172">Range-Lower</span></span>            | <span data-ttu-id="ece05-173">0</span><span class="sxs-lookup"><span data-stu-id="ece05-173">0</span></span>                                          |
| <span data-ttu-id="ece05-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ece05-174">Range-Upper</span></span>            | <span data-ttu-id="ece05-175">255</span><span class="sxs-lookup"><span data-stu-id="ece05-175">255</span></span>                                        |
| <span data-ttu-id="ece05-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ece05-176">Search-Flags</span></span>           | <span data-ttu-id="ece05-177">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ece05-177">0x00000000</span></span>                                 |
| <span data-ttu-id="ece05-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ece05-178">System-Flags</span></span>           | <span data-ttu-id="ece05-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ece05-179">0x00000010</span></span>                                 |
| <span data-ttu-id="ece05-180">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="ece05-180">Classes used in</span></span>        | [<span data-ttu-id="ece05-181">**Riferimento incrociato**</span><span class="sxs-lookup"><span data-stu-id="ece05-181">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ece05-182">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ece05-182">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ece05-183">Voce</span><span class="sxs-lookup"><span data-stu-id="ece05-183">Entry</span></span> | <span data-ttu-id="ece05-184">Valore</span><span class="sxs-lookup"><span data-stu-id="ece05-184">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="ece05-185">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="ece05-185">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="ece05-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ece05-186">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="ece05-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="ece05-187">System-Only</span></span>            | <span data-ttu-id="ece05-188">Falso</span><span class="sxs-lookup"><span data-stu-id="ece05-188">False</span></span>                                      |
| <span data-ttu-id="ece05-189">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="ece05-189">Is-Single-Valued</span></span>       | <span data-ttu-id="ece05-190">Vero</span><span class="sxs-lookup"><span data-stu-id="ece05-190">True</span></span>                                       |
| <span data-ttu-id="ece05-191">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="ece05-191">Is Indexed</span></span>             | <span data-ttu-id="ece05-192">Falso</span><span class="sxs-lookup"><span data-stu-id="ece05-192">False</span></span>                                      |
| <span data-ttu-id="ece05-193">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="ece05-193">In Global Catalog</span></span>      | <span data-ttu-id="ece05-194">Falso</span><span class="sxs-lookup"><span data-stu-id="ece05-194">False</span></span>                                      |
| <span data-ttu-id="ece05-195">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="ece05-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="ece05-196">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="ece05-196">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="ece05-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ece05-197">Range-Lower</span></span>            | <span data-ttu-id="ece05-198">0</span><span class="sxs-lookup"><span data-stu-id="ece05-198">0</span></span>                                          |
| <span data-ttu-id="ece05-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ece05-199">Range-Upper</span></span>            | <span data-ttu-id="ece05-200">255</span><span class="sxs-lookup"><span data-stu-id="ece05-200">255</span></span>                                        |
| <span data-ttu-id="ece05-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ece05-201">Search-Flags</span></span>           | <span data-ttu-id="ece05-202">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ece05-202">0x00000000</span></span>                                 |
| <span data-ttu-id="ece05-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ece05-203">System-Flags</span></span>           | <span data-ttu-id="ece05-204">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ece05-204">0x00000010</span></span>                                 |
| <span data-ttu-id="ece05-205">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="ece05-205">Classes used in</span></span>        | [<span data-ttu-id="ece05-206">**Riferimento incrociato**</span><span class="sxs-lookup"><span data-stu-id="ece05-206">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ece05-207">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ece05-207">Windows Server 2008</span></span>



| <span data-ttu-id="ece05-208">Voce</span><span class="sxs-lookup"><span data-stu-id="ece05-208">Entry</span></span> | <span data-ttu-id="ece05-209">Valore</span><span class="sxs-lookup"><span data-stu-id="ece05-209">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="ece05-210">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="ece05-210">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="ece05-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ece05-211">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="ece05-212">System-Only</span><span class="sxs-lookup"><span data-stu-id="ece05-212">System-Only</span></span>            | <span data-ttu-id="ece05-213">Falso</span><span class="sxs-lookup"><span data-stu-id="ece05-213">False</span></span>                                      |
| <span data-ttu-id="ece05-214">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="ece05-214">Is-Single-Valued</span></span>       | <span data-ttu-id="ece05-215">Vero</span><span class="sxs-lookup"><span data-stu-id="ece05-215">True</span></span>                                       |
| <span data-ttu-id="ece05-216">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="ece05-216">Is Indexed</span></span>             | <span data-ttu-id="ece05-217">Falso</span><span class="sxs-lookup"><span data-stu-id="ece05-217">False</span></span>                                      |
| <span data-ttu-id="ece05-218">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="ece05-218">In Global Catalog</span></span>      | <span data-ttu-id="ece05-219">Falso</span><span class="sxs-lookup"><span data-stu-id="ece05-219">False</span></span>                                      |
| <span data-ttu-id="ece05-220">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="ece05-220">NT-Security-Descriptor</span></span> | <span data-ttu-id="ece05-221">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="ece05-221">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="ece05-222">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ece05-222">Range-Lower</span></span>            | <span data-ttu-id="ece05-223">0</span><span class="sxs-lookup"><span data-stu-id="ece05-223">0</span></span>                                          |
| <span data-ttu-id="ece05-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ece05-224">Range-Upper</span></span>            | <span data-ttu-id="ece05-225">255</span><span class="sxs-lookup"><span data-stu-id="ece05-225">255</span></span>                                        |
| <span data-ttu-id="ece05-226">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ece05-226">Search-Flags</span></span>           | <span data-ttu-id="ece05-227">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ece05-227">0x00000000</span></span>                                 |
| <span data-ttu-id="ece05-228">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ece05-228">System-Flags</span></span>           | <span data-ttu-id="ece05-229">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ece05-229">0x00000010</span></span>                                 |
| <span data-ttu-id="ece05-230">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="ece05-230">Classes used in</span></span>        | [<span data-ttu-id="ece05-231">**Riferimento incrociato**</span><span class="sxs-lookup"><span data-stu-id="ece05-231">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ece05-232">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ece05-232">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ece05-233">Voce</span><span class="sxs-lookup"><span data-stu-id="ece05-233">Entry</span></span> | <span data-ttu-id="ece05-234">Valore</span><span class="sxs-lookup"><span data-stu-id="ece05-234">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="ece05-235">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="ece05-235">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="ece05-236">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ece05-236">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="ece05-237">System-Only</span><span class="sxs-lookup"><span data-stu-id="ece05-237">System-Only</span></span>            | <span data-ttu-id="ece05-238">Falso</span><span class="sxs-lookup"><span data-stu-id="ece05-238">False</span></span>                                      |
| <span data-ttu-id="ece05-239">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="ece05-239">Is-Single-Valued</span></span>       | <span data-ttu-id="ece05-240">Vero</span><span class="sxs-lookup"><span data-stu-id="ece05-240">True</span></span>                                       |
| <span data-ttu-id="ece05-241">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="ece05-241">Is Indexed</span></span>             | <span data-ttu-id="ece05-242">Falso</span><span class="sxs-lookup"><span data-stu-id="ece05-242">False</span></span>                                      |
| <span data-ttu-id="ece05-243">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="ece05-243">In Global Catalog</span></span>      | <span data-ttu-id="ece05-244">Falso</span><span class="sxs-lookup"><span data-stu-id="ece05-244">False</span></span>                                      |
| <span data-ttu-id="ece05-245">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="ece05-245">NT-Security-Descriptor</span></span> | <span data-ttu-id="ece05-246">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="ece05-246">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="ece05-247">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ece05-247">Range-Lower</span></span>            | <span data-ttu-id="ece05-248">0</span><span class="sxs-lookup"><span data-stu-id="ece05-248">0</span></span>                                          |
| <span data-ttu-id="ece05-249">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ece05-249">Range-Upper</span></span>            | <span data-ttu-id="ece05-250">255</span><span class="sxs-lookup"><span data-stu-id="ece05-250">255</span></span>                                        |
| <span data-ttu-id="ece05-251">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ece05-251">Search-Flags</span></span>           | <span data-ttu-id="ece05-252">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ece05-252">0x00000000</span></span>                                 |
| <span data-ttu-id="ece05-253">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ece05-253">System-Flags</span></span>           | <span data-ttu-id="ece05-254">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ece05-254">0x00000010</span></span>                                 |
| <span data-ttu-id="ece05-255">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="ece05-255">Classes used in</span></span>        | [<span data-ttu-id="ece05-256">**Riferimento incrociato**</span><span class="sxs-lookup"><span data-stu-id="ece05-256">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ece05-257">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ece05-257">Windows Server 2012</span></span>



| <span data-ttu-id="ece05-258">Voce</span><span class="sxs-lookup"><span data-stu-id="ece05-258">Entry</span></span> | <span data-ttu-id="ece05-259">Valore</span><span class="sxs-lookup"><span data-stu-id="ece05-259">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="ece05-260">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="ece05-260">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="ece05-261">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ece05-261">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="ece05-262">System-Only</span><span class="sxs-lookup"><span data-stu-id="ece05-262">System-Only</span></span>            | <span data-ttu-id="ece05-263">Falso</span><span class="sxs-lookup"><span data-stu-id="ece05-263">False</span></span>                                      |
| <span data-ttu-id="ece05-264">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="ece05-264">Is-Single-Valued</span></span>       | <span data-ttu-id="ece05-265">Vero</span><span class="sxs-lookup"><span data-stu-id="ece05-265">True</span></span>                                       |
| <span data-ttu-id="ece05-266">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="ece05-266">Is Indexed</span></span>             | <span data-ttu-id="ece05-267">Falso</span><span class="sxs-lookup"><span data-stu-id="ece05-267">False</span></span>                                      |
| <span data-ttu-id="ece05-268">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="ece05-268">In Global Catalog</span></span>      | <span data-ttu-id="ece05-269">Falso</span><span class="sxs-lookup"><span data-stu-id="ece05-269">False</span></span>                                      |
| <span data-ttu-id="ece05-270">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="ece05-270">NT-Security-Descriptor</span></span> | <span data-ttu-id="ece05-271">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="ece05-271">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="ece05-272">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ece05-272">Range-Lower</span></span>            | <span data-ttu-id="ece05-273">0</span><span class="sxs-lookup"><span data-stu-id="ece05-273">0</span></span>                                          |
| <span data-ttu-id="ece05-274">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ece05-274">Range-Upper</span></span>            | <span data-ttu-id="ece05-275">255</span><span class="sxs-lookup"><span data-stu-id="ece05-275">255</span></span>                                        |
| <span data-ttu-id="ece05-276">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ece05-276">Search-Flags</span></span>           | <span data-ttu-id="ece05-277">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ece05-277">0x00000000</span></span>                                 |
| <span data-ttu-id="ece05-278">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ece05-278">System-Flags</span></span>           | <span data-ttu-id="ece05-279">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ece05-279">0x00000010</span></span>                                 |
| <span data-ttu-id="ece05-280">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="ece05-280">Classes used in</span></span>        | [<span data-ttu-id="ece05-281">**Riferimento incrociato**</span><span class="sxs-lookup"><span data-stu-id="ece05-281">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



 

 





