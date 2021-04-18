---
title: Extended-chars-consentito attributo
description: Indica se i caratteri estesi sono consentiti nel valore di questo attributo. Si applica solo agli attributi di stringa IA5, numeric, Printable e Teletex.
ms.assetid: aeacb5ef-9af2-498b-ae53-b3095de0d0c6
ms.tgt_platform: multiple
keywords:
- Extended-chars-schema di AD attribute consentito
- Schema AD dell'attributo extendedCharsAllowed
topic_type:
- apiref
api_name:
- Extended-Chars-Allowed
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e26194232387f27f3177f13edeab90efc97a4bb3
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "106302926"
---
# <a name="extended-chars-allowed-attribute"></a><span data-ttu-id="2037c-106">Extended-chars-consentito attributo</span><span class="sxs-lookup"><span data-stu-id="2037c-106">Extended-Chars-Allowed attribute</span></span>

<span data-ttu-id="2037c-107">Indica se i caratteri estesi sono consentiti nel valore di questo attributo.</span><span class="sxs-lookup"><span data-stu-id="2037c-107">Indicates whether extended characters are allowed in the value of this attribute.</span></span> <span data-ttu-id="2037c-108">Si applica solo agli attributi di stringa IA5, numeric, Printable e Teletex.</span><span class="sxs-lookup"><span data-stu-id="2037c-108">Only applies to IA5, Numeric, Printable, and Teletex string attributes.</span></span>



| <span data-ttu-id="2037c-109">Voce</span><span class="sxs-lookup"><span data-stu-id="2037c-109">Entry</span></span> | <span data-ttu-id="2037c-110">Valore</span><span class="sxs-lookup"><span data-stu-id="2037c-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="2037c-111">CN</span><span class="sxs-lookup"><span data-stu-id="2037c-111">CN</span></span>                | <span data-ttu-id="2037c-112">Caratteri estesi-consentiti</span><span class="sxs-lookup"><span data-stu-id="2037c-112">Extended-Chars-Allowed</span></span>               |
| <span data-ttu-id="2037c-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="2037c-113">Ldap-Display-Name</span></span> | <span data-ttu-id="2037c-114">extendedCharsAllowed</span><span class="sxs-lookup"><span data-stu-id="2037c-114">extendedCharsAllowed</span></span>                 |
| <span data-ttu-id="2037c-115">Dimensione</span><span class="sxs-lookup"><span data-stu-id="2037c-115">Size</span></span>              | \-                                   |
| <span data-ttu-id="2037c-116">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="2037c-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="2037c-117">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="2037c-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="2037c-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="2037c-118">Attribute-Id</span></span>      | <span data-ttu-id="2037c-119">1.2.840.113556.1.2.380</span><span class="sxs-lookup"><span data-stu-id="2037c-119">1.2.840.113556.1.2.380</span></span>               |
| <span data-ttu-id="2037c-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="2037c-120">System-Id-Guid</span></span>    | <span data-ttu-id="2037c-121">bf967966-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="2037c-121">bf967966-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="2037c-122">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2037c-122">Syntax</span></span>            | [<span data-ttu-id="2037c-123">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="2037c-123">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="2037c-124">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="2037c-124">Implementations</span></span>

-   [<span data-ttu-id="2037c-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="2037c-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="2037c-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="2037c-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="2037c-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="2037c-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="2037c-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="2037c-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="2037c-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="2037c-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="2037c-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="2037c-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="2037c-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="2037c-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="2037c-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2037c-132">Windows 2000 Server</span></span>



| <span data-ttu-id="2037c-133">Voce</span><span class="sxs-lookup"><span data-stu-id="2037c-133">Entry</span></span> | <span data-ttu-id="2037c-134">Valore</span><span class="sxs-lookup"><span data-stu-id="2037c-134">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="2037c-135">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="2037c-135">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="2037c-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2037c-136">MAPI-Id</span></span>                | <span data-ttu-id="2037c-137">0x80A7</span><span class="sxs-lookup"><span data-stu-id="2037c-137">0x80A7</span></span>                                                   |
| <span data-ttu-id="2037c-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="2037c-138">System-Only</span></span>            | <span data-ttu-id="2037c-139">Vero</span><span class="sxs-lookup"><span data-stu-id="2037c-139">True</span></span>                                                     |
| <span data-ttu-id="2037c-140">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="2037c-140">Is-Single-Valued</span></span>       | <span data-ttu-id="2037c-141">Vero</span><span class="sxs-lookup"><span data-stu-id="2037c-141">True</span></span>                                                     |
| <span data-ttu-id="2037c-142">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="2037c-142">Is Indexed</span></span>             | <span data-ttu-id="2037c-143">Falso</span><span class="sxs-lookup"><span data-stu-id="2037c-143">False</span></span>                                                    |
| <span data-ttu-id="2037c-144">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="2037c-144">In Global Catalog</span></span>      | <span data-ttu-id="2037c-145">Falso</span><span class="sxs-lookup"><span data-stu-id="2037c-145">False</span></span>                                                    |
| <span data-ttu-id="2037c-146">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="2037c-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="2037c-147">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="2037c-147">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="2037c-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2037c-148">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="2037c-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2037c-149">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="2037c-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2037c-150">Search-Flags</span></span>           | <span data-ttu-id="2037c-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2037c-151">0x00000000</span></span>                                               |
| <span data-ttu-id="2037c-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2037c-152">System-Flags</span></span>           | <span data-ttu-id="2037c-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2037c-153">0x00000010</span></span>                                               |
| <span data-ttu-id="2037c-154">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="2037c-154">Classes used in</span></span>        | [<span data-ttu-id="2037c-155">**Attribute-schema**</span><span class="sxs-lookup"><span data-stu-id="2037c-155">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="2037c-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2037c-156">Windows Server 2003</span></span>



| <span data-ttu-id="2037c-157">Voce</span><span class="sxs-lookup"><span data-stu-id="2037c-157">Entry</span></span> | <span data-ttu-id="2037c-158">Valore</span><span class="sxs-lookup"><span data-stu-id="2037c-158">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="2037c-159">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="2037c-159">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="2037c-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2037c-160">MAPI-Id</span></span>                | <span data-ttu-id="2037c-161">0x80A7</span><span class="sxs-lookup"><span data-stu-id="2037c-161">0x80A7</span></span>                                                   |
| <span data-ttu-id="2037c-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="2037c-162">System-Only</span></span>            | <span data-ttu-id="2037c-163">Falso</span><span class="sxs-lookup"><span data-stu-id="2037c-163">False</span></span>                                                    |
| <span data-ttu-id="2037c-164">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="2037c-164">Is-Single-Valued</span></span>       | <span data-ttu-id="2037c-165">Vero</span><span class="sxs-lookup"><span data-stu-id="2037c-165">True</span></span>                                                     |
| <span data-ttu-id="2037c-166">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="2037c-166">Is Indexed</span></span>             | <span data-ttu-id="2037c-167">Falso</span><span class="sxs-lookup"><span data-stu-id="2037c-167">False</span></span>                                                    |
| <span data-ttu-id="2037c-168">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="2037c-168">In Global Catalog</span></span>      | <span data-ttu-id="2037c-169">Falso</span><span class="sxs-lookup"><span data-stu-id="2037c-169">False</span></span>                                                    |
| <span data-ttu-id="2037c-170">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="2037c-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="2037c-171">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="2037c-171">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="2037c-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2037c-172">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="2037c-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2037c-173">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="2037c-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2037c-174">Search-Flags</span></span>           | <span data-ttu-id="2037c-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2037c-175">0x00000000</span></span>                                               |
| <span data-ttu-id="2037c-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2037c-176">System-Flags</span></span>           | <span data-ttu-id="2037c-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2037c-177">0x00000010</span></span>                                               |
| <span data-ttu-id="2037c-178">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="2037c-178">Classes used in</span></span>        | [<span data-ttu-id="2037c-179">**Attribute-schema**</span><span class="sxs-lookup"><span data-stu-id="2037c-179">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="2037c-180">ADAM</span><span class="sxs-lookup"><span data-stu-id="2037c-180">ADAM</span></span>



| <span data-ttu-id="2037c-181">Voce</span><span class="sxs-lookup"><span data-stu-id="2037c-181">Entry</span></span> | <span data-ttu-id="2037c-182">Valore</span><span class="sxs-lookup"><span data-stu-id="2037c-182">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="2037c-183">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="2037c-183">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="2037c-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2037c-184">MAPI-Id</span></span>                | <span data-ttu-id="2037c-185">0x80A7</span><span class="sxs-lookup"><span data-stu-id="2037c-185">0x80A7</span></span>                                                   |
| <span data-ttu-id="2037c-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="2037c-186">System-Only</span></span>            | <span data-ttu-id="2037c-187">Falso</span><span class="sxs-lookup"><span data-stu-id="2037c-187">False</span></span>                                                    |
| <span data-ttu-id="2037c-188">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="2037c-188">Is-Single-Valued</span></span>       | <span data-ttu-id="2037c-189">Vero</span><span class="sxs-lookup"><span data-stu-id="2037c-189">True</span></span>                                                     |
| <span data-ttu-id="2037c-190">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="2037c-190">Is Indexed</span></span>             | <span data-ttu-id="2037c-191">Falso</span><span class="sxs-lookup"><span data-stu-id="2037c-191">False</span></span>                                                    |
| <span data-ttu-id="2037c-192">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="2037c-192">In Global Catalog</span></span>      | <span data-ttu-id="2037c-193">Falso</span><span class="sxs-lookup"><span data-stu-id="2037c-193">False</span></span>                                                    |
| <span data-ttu-id="2037c-194">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="2037c-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="2037c-195">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="2037c-195">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="2037c-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2037c-196">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="2037c-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2037c-197">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="2037c-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2037c-198">Search-Flags</span></span>           | <span data-ttu-id="2037c-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2037c-199">0x00000000</span></span>                                               |
| <span data-ttu-id="2037c-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2037c-200">System-Flags</span></span>           | <span data-ttu-id="2037c-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2037c-201">0x00000010</span></span>                                               |
| <span data-ttu-id="2037c-202">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="2037c-202">Classes used in</span></span>        | [<span data-ttu-id="2037c-203">**Attribute-schema**</span><span class="sxs-lookup"><span data-stu-id="2037c-203">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="2037c-204">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="2037c-204">Windows Server 2003 R2</span></span>



| <span data-ttu-id="2037c-205">Voce</span><span class="sxs-lookup"><span data-stu-id="2037c-205">Entry</span></span> | <span data-ttu-id="2037c-206">Valore</span><span class="sxs-lookup"><span data-stu-id="2037c-206">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="2037c-207">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="2037c-207">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="2037c-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2037c-208">MAPI-Id</span></span>                | <span data-ttu-id="2037c-209">0x80A7</span><span class="sxs-lookup"><span data-stu-id="2037c-209">0x80A7</span></span>                                                   |
| <span data-ttu-id="2037c-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="2037c-210">System-Only</span></span>            | <span data-ttu-id="2037c-211">Falso</span><span class="sxs-lookup"><span data-stu-id="2037c-211">False</span></span>                                                    |
| <span data-ttu-id="2037c-212">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="2037c-212">Is-Single-Valued</span></span>       | <span data-ttu-id="2037c-213">Vero</span><span class="sxs-lookup"><span data-stu-id="2037c-213">True</span></span>                                                     |
| <span data-ttu-id="2037c-214">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="2037c-214">Is Indexed</span></span>             | <span data-ttu-id="2037c-215">Falso</span><span class="sxs-lookup"><span data-stu-id="2037c-215">False</span></span>                                                    |
| <span data-ttu-id="2037c-216">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="2037c-216">In Global Catalog</span></span>      | <span data-ttu-id="2037c-217">Falso</span><span class="sxs-lookup"><span data-stu-id="2037c-217">False</span></span>                                                    |
| <span data-ttu-id="2037c-218">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="2037c-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="2037c-219">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="2037c-219">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="2037c-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2037c-220">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="2037c-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2037c-221">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="2037c-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2037c-222">Search-Flags</span></span>           | <span data-ttu-id="2037c-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2037c-223">0x00000000</span></span>                                               |
| <span data-ttu-id="2037c-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2037c-224">System-Flags</span></span>           | <span data-ttu-id="2037c-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2037c-225">0x00000010</span></span>                                               |
| <span data-ttu-id="2037c-226">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="2037c-226">Classes used in</span></span>        | [<span data-ttu-id="2037c-227">**Attribute-schema**</span><span class="sxs-lookup"><span data-stu-id="2037c-227">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="2037c-228">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2037c-228">Windows Server 2008</span></span>



| <span data-ttu-id="2037c-229">Voce</span><span class="sxs-lookup"><span data-stu-id="2037c-229">Entry</span></span> | <span data-ttu-id="2037c-230">Valore</span><span class="sxs-lookup"><span data-stu-id="2037c-230">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="2037c-231">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="2037c-231">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="2037c-232">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2037c-232">MAPI-Id</span></span>                | <span data-ttu-id="2037c-233">0x80A7</span><span class="sxs-lookup"><span data-stu-id="2037c-233">0x80A7</span></span>                                                   |
| <span data-ttu-id="2037c-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="2037c-234">System-Only</span></span>            | <span data-ttu-id="2037c-235">Falso</span><span class="sxs-lookup"><span data-stu-id="2037c-235">False</span></span>                                                    |
| <span data-ttu-id="2037c-236">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="2037c-236">Is-Single-Valued</span></span>       | <span data-ttu-id="2037c-237">Vero</span><span class="sxs-lookup"><span data-stu-id="2037c-237">True</span></span>                                                     |
| <span data-ttu-id="2037c-238">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="2037c-238">Is Indexed</span></span>             | <span data-ttu-id="2037c-239">Falso</span><span class="sxs-lookup"><span data-stu-id="2037c-239">False</span></span>                                                    |
| <span data-ttu-id="2037c-240">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="2037c-240">In Global Catalog</span></span>      | <span data-ttu-id="2037c-241">Falso</span><span class="sxs-lookup"><span data-stu-id="2037c-241">False</span></span>                                                    |
| <span data-ttu-id="2037c-242">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="2037c-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="2037c-243">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="2037c-243">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="2037c-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2037c-244">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="2037c-245">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2037c-245">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="2037c-246">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2037c-246">Search-Flags</span></span>           | <span data-ttu-id="2037c-247">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2037c-247">0x00000000</span></span>                                               |
| <span data-ttu-id="2037c-248">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2037c-248">System-Flags</span></span>           | <span data-ttu-id="2037c-249">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2037c-249">0x00000010</span></span>                                               |
| <span data-ttu-id="2037c-250">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="2037c-250">Classes used in</span></span>        | [<span data-ttu-id="2037c-251">**Attribute-schema**</span><span class="sxs-lookup"><span data-stu-id="2037c-251">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="2037c-252">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2037c-252">Windows Server 2008 R2</span></span>



| <span data-ttu-id="2037c-253">Voce</span><span class="sxs-lookup"><span data-stu-id="2037c-253">Entry</span></span> | <span data-ttu-id="2037c-254">Valore</span><span class="sxs-lookup"><span data-stu-id="2037c-254">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="2037c-255">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="2037c-255">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="2037c-256">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2037c-256">MAPI-Id</span></span>                | <span data-ttu-id="2037c-257">0x80A7</span><span class="sxs-lookup"><span data-stu-id="2037c-257">0x80A7</span></span>                                                   |
| <span data-ttu-id="2037c-258">System-Only</span><span class="sxs-lookup"><span data-stu-id="2037c-258">System-Only</span></span>            | <span data-ttu-id="2037c-259">Falso</span><span class="sxs-lookup"><span data-stu-id="2037c-259">False</span></span>                                                    |
| <span data-ttu-id="2037c-260">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="2037c-260">Is-Single-Valued</span></span>       | <span data-ttu-id="2037c-261">Vero</span><span class="sxs-lookup"><span data-stu-id="2037c-261">True</span></span>                                                     |
| <span data-ttu-id="2037c-262">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="2037c-262">Is Indexed</span></span>             | <span data-ttu-id="2037c-263">Falso</span><span class="sxs-lookup"><span data-stu-id="2037c-263">False</span></span>                                                    |
| <span data-ttu-id="2037c-264">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="2037c-264">In Global Catalog</span></span>      | <span data-ttu-id="2037c-265">Falso</span><span class="sxs-lookup"><span data-stu-id="2037c-265">False</span></span>                                                    |
| <span data-ttu-id="2037c-266">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="2037c-266">NT-Security-Descriptor</span></span> | <span data-ttu-id="2037c-267">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="2037c-267">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="2037c-268">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2037c-268">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="2037c-269">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2037c-269">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="2037c-270">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2037c-270">Search-Flags</span></span>           | <span data-ttu-id="2037c-271">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2037c-271">0x00000000</span></span>                                               |
| <span data-ttu-id="2037c-272">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2037c-272">System-Flags</span></span>           | <span data-ttu-id="2037c-273">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2037c-273">0x00000010</span></span>                                               |
| <span data-ttu-id="2037c-274">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="2037c-274">Classes used in</span></span>        | [<span data-ttu-id="2037c-275">**Attribute-schema**</span><span class="sxs-lookup"><span data-stu-id="2037c-275">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="2037c-276">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2037c-276">Windows Server 2012</span></span>



| <span data-ttu-id="2037c-277">Voce</span><span class="sxs-lookup"><span data-stu-id="2037c-277">Entry</span></span> | <span data-ttu-id="2037c-278">Valore</span><span class="sxs-lookup"><span data-stu-id="2037c-278">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="2037c-279">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="2037c-279">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="2037c-280">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2037c-280">MAPI-Id</span></span>                | <span data-ttu-id="2037c-281">0x80A7</span><span class="sxs-lookup"><span data-stu-id="2037c-281">0x80A7</span></span>                                                   |
| <span data-ttu-id="2037c-282">System-Only</span><span class="sxs-lookup"><span data-stu-id="2037c-282">System-Only</span></span>            | <span data-ttu-id="2037c-283">Falso</span><span class="sxs-lookup"><span data-stu-id="2037c-283">False</span></span>                                                    |
| <span data-ttu-id="2037c-284">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="2037c-284">Is-Single-Valued</span></span>       | <span data-ttu-id="2037c-285">Vero</span><span class="sxs-lookup"><span data-stu-id="2037c-285">True</span></span>                                                     |
| <span data-ttu-id="2037c-286">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="2037c-286">Is Indexed</span></span>             | <span data-ttu-id="2037c-287">Falso</span><span class="sxs-lookup"><span data-stu-id="2037c-287">False</span></span>                                                    |
| <span data-ttu-id="2037c-288">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="2037c-288">In Global Catalog</span></span>      | <span data-ttu-id="2037c-289">Falso</span><span class="sxs-lookup"><span data-stu-id="2037c-289">False</span></span>                                                    |
| <span data-ttu-id="2037c-290">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="2037c-290">NT-Security-Descriptor</span></span> | <span data-ttu-id="2037c-291">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="2037c-291">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="2037c-292">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2037c-292">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="2037c-293">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2037c-293">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="2037c-294">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2037c-294">Search-Flags</span></span>           | <span data-ttu-id="2037c-295">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2037c-295">0x00000000</span></span>                                               |
| <span data-ttu-id="2037c-296">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2037c-296">System-Flags</span></span>           | <span data-ttu-id="2037c-297">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2037c-297">0x00000010</span></span>                                               |
| <span data-ttu-id="2037c-298">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="2037c-298">Classes used in</span></span>        | [<span data-ttu-id="2037c-299">**Attribute-schema**</span><span class="sxs-lookup"><span data-stu-id="2037c-299">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



 

 





