---
title: attributo ms-DS-Preferred-GC-site
description: L'attributo ms-DS-Preferred-GC-site viene usato dalla gestione degli account di sicurezza per l'espansione del gruppo durante la valutazione del token.
ms.assetid: f42d3787-4063-4804-a7b5-4798516ad47e
ms.tgt_platform: multiple
keywords:
- Schema di AD per l'attributo del sito ms-DS-Preferred-GC
- msDS-Preferred-GC-site attributo AD schema
topic_type:
- apiref
api_name:
- ms-DS-Preferred-GC-Site
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 172e12758ba0b365fa195cb4e1384c161cea3d14
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104225265"
---
# <a name="ms-ds-preferred-gc-site-attribute"></a><span data-ttu-id="36c45-105">attributo ms-DS-Preferred-GC-site</span><span class="sxs-lookup"><span data-stu-id="36c45-105">ms-DS-Preferred-GC-Site attribute</span></span>

<span data-ttu-id="36c45-106">L'attributo **ms-DS-Preferred-GC-site** viene usato dalla gestione degli account di sicurezza per l'espansione del gruppo durante la valutazione del token.</span><span class="sxs-lookup"><span data-stu-id="36c45-106">The **ms-DS-Preferred-GC-Site** attribute is used by the Security Accounts Manager for group expansion during token evaluation.</span></span>



| <span data-ttu-id="36c45-107">Voce</span><span class="sxs-lookup"><span data-stu-id="36c45-107">Entry</span></span> | <span data-ttu-id="36c45-108">Valore</span><span class="sxs-lookup"><span data-stu-id="36c45-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="36c45-109">CN</span><span class="sxs-lookup"><span data-stu-id="36c45-109">CN</span></span>                | <span data-ttu-id="36c45-110">ms-DS-preferito-GC-sito</span><span class="sxs-lookup"><span data-stu-id="36c45-110">ms-DS-Preferred-GC-Site</span></span>                 |
| <span data-ttu-id="36c45-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="36c45-111">Ldap-Display-Name</span></span> | <span data-ttu-id="36c45-112">msDS-Preferred-GC-site</span><span class="sxs-lookup"><span data-stu-id="36c45-112">msDS-Preferred-GC-Site</span></span>                  |
| <span data-ttu-id="36c45-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="36c45-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="36c45-114">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="36c45-114">Update Privilege</span></span>  | <span data-ttu-id="36c45-115">Amministratore di dominio</span><span class="sxs-lookup"><span data-stu-id="36c45-115">Domain administrator</span></span>                    |
| <span data-ttu-id="36c45-116">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="36c45-116">Update Frequency</span></span>  | <span data-ttu-id="36c45-117">A discrezione dell'amministratore.</span><span class="sxs-lookup"><span data-stu-id="36c45-117">At the administrator's discretion.</span></span>      |
| <span data-ttu-id="36c45-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="36c45-118">Attribute-Id</span></span>      | <span data-ttu-id="36c45-119">1.2.840.113556.1.4.1444</span><span class="sxs-lookup"><span data-stu-id="36c45-119">1.2.840.113556.1.4.1444</span></span>                 |
| <span data-ttu-id="36c45-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="36c45-120">System-Id-Guid</span></span>    | <span data-ttu-id="36c45-121">d921b50a-0ab2-42cd-87f6-09cf83a91854</span><span class="sxs-lookup"><span data-stu-id="36c45-121">d921b50a-0ab2-42cd-87f6-09cf83a91854</span></span>    |
| <span data-ttu-id="36c45-122">Sintassi</span><span class="sxs-lookup"><span data-stu-id="36c45-122">Syntax</span></span>            | [<span data-ttu-id="36c45-123">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="36c45-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="36c45-124">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="36c45-124">Implementations</span></span>

-   [<span data-ttu-id="36c45-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="36c45-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="36c45-126">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="36c45-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="36c45-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="36c45-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="36c45-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="36c45-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="36c45-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="36c45-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="36c45-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="36c45-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="36c45-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="36c45-131">Windows Server 2003</span></span>



| <span data-ttu-id="36c45-132">Voce</span><span class="sxs-lookup"><span data-stu-id="36c45-132">Entry</span></span> | <span data-ttu-id="36c45-133">Valore</span><span class="sxs-lookup"><span data-stu-id="36c45-133">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="36c45-134">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="36c45-134">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="36c45-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="36c45-135">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="36c45-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="36c45-136">System-Only</span></span>            | <span data-ttu-id="36c45-137">Falso</span><span class="sxs-lookup"><span data-stu-id="36c45-137">False</span></span>                                                       |
| <span data-ttu-id="36c45-138">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="36c45-138">Is-Single-Valued</span></span>       | <span data-ttu-id="36c45-139">Vero</span><span class="sxs-lookup"><span data-stu-id="36c45-139">True</span></span>                                                        |
| <span data-ttu-id="36c45-140">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="36c45-140">Is Indexed</span></span>             | <span data-ttu-id="36c45-141">Falso</span><span class="sxs-lookup"><span data-stu-id="36c45-141">False</span></span>                                                       |
| <span data-ttu-id="36c45-142">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="36c45-142">In Global Catalog</span></span>      | <span data-ttu-id="36c45-143">Falso</span><span class="sxs-lookup"><span data-stu-id="36c45-143">False</span></span>                                                       |
| <span data-ttu-id="36c45-144">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="36c45-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="36c45-145">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="36c45-145">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="36c45-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="36c45-146">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="36c45-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="36c45-147">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="36c45-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="36c45-148">Search-Flags</span></span>           | <span data-ttu-id="36c45-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="36c45-149">0x00000000</span></span>                                                  |
| <span data-ttu-id="36c45-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="36c45-150">System-Flags</span></span>           | <span data-ttu-id="36c45-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="36c45-151">0x00000010</span></span>                                                  |
| <span data-ttu-id="36c45-152">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="36c45-152">Classes used in</span></span>        | [<span data-ttu-id="36c45-153">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="36c45-153">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="adam"></a><span data-ttu-id="36c45-154">ADAM</span><span class="sxs-lookup"><span data-stu-id="36c45-154">ADAM</span></span>



| <span data-ttu-id="36c45-155">Voce</span><span class="sxs-lookup"><span data-stu-id="36c45-155">Entry</span></span> | <span data-ttu-id="36c45-156">Valore</span><span class="sxs-lookup"><span data-stu-id="36c45-156">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="36c45-157">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="36c45-157">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="36c45-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="36c45-158">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="36c45-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="36c45-159">System-Only</span></span>            | <span data-ttu-id="36c45-160">Falso</span><span class="sxs-lookup"><span data-stu-id="36c45-160">False</span></span>                                                       |
| <span data-ttu-id="36c45-161">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="36c45-161">Is-Single-Valued</span></span>       | <span data-ttu-id="36c45-162">Vero</span><span class="sxs-lookup"><span data-stu-id="36c45-162">True</span></span>                                                        |
| <span data-ttu-id="36c45-163">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="36c45-163">Is Indexed</span></span>             | <span data-ttu-id="36c45-164">Falso</span><span class="sxs-lookup"><span data-stu-id="36c45-164">False</span></span>                                                       |
| <span data-ttu-id="36c45-165">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="36c45-165">In Global Catalog</span></span>      | <span data-ttu-id="36c45-166">Falso</span><span class="sxs-lookup"><span data-stu-id="36c45-166">False</span></span>                                                       |
| <span data-ttu-id="36c45-167">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="36c45-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="36c45-168">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="36c45-168">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="36c45-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="36c45-169">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="36c45-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="36c45-170">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="36c45-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="36c45-171">Search-Flags</span></span>           | <span data-ttu-id="36c45-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="36c45-172">0x00000000</span></span>                                                  |
| <span data-ttu-id="36c45-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="36c45-173">System-Flags</span></span>           | <span data-ttu-id="36c45-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="36c45-174">0x00000010</span></span>                                                  |
| <span data-ttu-id="36c45-175">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="36c45-175">Classes used in</span></span>        | [<span data-ttu-id="36c45-176">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="36c45-176">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="36c45-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="36c45-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="36c45-178">Voce</span><span class="sxs-lookup"><span data-stu-id="36c45-178">Entry</span></span> | <span data-ttu-id="36c45-179">Valore</span><span class="sxs-lookup"><span data-stu-id="36c45-179">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="36c45-180">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="36c45-180">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="36c45-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="36c45-181">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="36c45-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="36c45-182">System-Only</span></span>            | <span data-ttu-id="36c45-183">Falso</span><span class="sxs-lookup"><span data-stu-id="36c45-183">False</span></span>                                                       |
| <span data-ttu-id="36c45-184">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="36c45-184">Is-Single-Valued</span></span>       | <span data-ttu-id="36c45-185">Vero</span><span class="sxs-lookup"><span data-stu-id="36c45-185">True</span></span>                                                        |
| <span data-ttu-id="36c45-186">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="36c45-186">Is Indexed</span></span>             | <span data-ttu-id="36c45-187">Falso</span><span class="sxs-lookup"><span data-stu-id="36c45-187">False</span></span>                                                       |
| <span data-ttu-id="36c45-188">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="36c45-188">In Global Catalog</span></span>      | <span data-ttu-id="36c45-189">Falso</span><span class="sxs-lookup"><span data-stu-id="36c45-189">False</span></span>                                                       |
| <span data-ttu-id="36c45-190">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="36c45-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="36c45-191">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="36c45-191">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="36c45-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="36c45-192">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="36c45-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="36c45-193">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="36c45-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="36c45-194">Search-Flags</span></span>           | <span data-ttu-id="36c45-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="36c45-195">0x00000000</span></span>                                                  |
| <span data-ttu-id="36c45-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="36c45-196">System-Flags</span></span>           | <span data-ttu-id="36c45-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="36c45-197">0x00000010</span></span>                                                  |
| <span data-ttu-id="36c45-198">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="36c45-198">Classes used in</span></span>        | [<span data-ttu-id="36c45-199">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="36c45-199">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="36c45-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="36c45-200">Windows Server 2008</span></span>



| <span data-ttu-id="36c45-201">Voce</span><span class="sxs-lookup"><span data-stu-id="36c45-201">Entry</span></span> | <span data-ttu-id="36c45-202">Valore</span><span class="sxs-lookup"><span data-stu-id="36c45-202">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="36c45-203">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="36c45-203">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="36c45-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="36c45-204">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="36c45-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="36c45-205">System-Only</span></span>            | <span data-ttu-id="36c45-206">Falso</span><span class="sxs-lookup"><span data-stu-id="36c45-206">False</span></span>                                                       |
| <span data-ttu-id="36c45-207">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="36c45-207">Is-Single-Valued</span></span>       | <span data-ttu-id="36c45-208">Vero</span><span class="sxs-lookup"><span data-stu-id="36c45-208">True</span></span>                                                        |
| <span data-ttu-id="36c45-209">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="36c45-209">Is Indexed</span></span>             | <span data-ttu-id="36c45-210">Falso</span><span class="sxs-lookup"><span data-stu-id="36c45-210">False</span></span>                                                       |
| <span data-ttu-id="36c45-211">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="36c45-211">In Global Catalog</span></span>      | <span data-ttu-id="36c45-212">Falso</span><span class="sxs-lookup"><span data-stu-id="36c45-212">False</span></span>                                                       |
| <span data-ttu-id="36c45-213">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="36c45-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="36c45-214">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="36c45-214">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="36c45-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="36c45-215">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="36c45-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="36c45-216">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="36c45-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="36c45-217">Search-Flags</span></span>           | <span data-ttu-id="36c45-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="36c45-218">0x00000000</span></span>                                                  |
| <span data-ttu-id="36c45-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="36c45-219">System-Flags</span></span>           | <span data-ttu-id="36c45-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="36c45-220">0x00000010</span></span>                                                  |
| <span data-ttu-id="36c45-221">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="36c45-221">Classes used in</span></span>        | [<span data-ttu-id="36c45-222">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="36c45-222">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="36c45-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="36c45-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="36c45-224">Voce</span><span class="sxs-lookup"><span data-stu-id="36c45-224">Entry</span></span> | <span data-ttu-id="36c45-225">Valore</span><span class="sxs-lookup"><span data-stu-id="36c45-225">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="36c45-226">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="36c45-226">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="36c45-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="36c45-227">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="36c45-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="36c45-228">System-Only</span></span>            | <span data-ttu-id="36c45-229">Falso</span><span class="sxs-lookup"><span data-stu-id="36c45-229">False</span></span>                                                       |
| <span data-ttu-id="36c45-230">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="36c45-230">Is-Single-Valued</span></span>       | <span data-ttu-id="36c45-231">Vero</span><span class="sxs-lookup"><span data-stu-id="36c45-231">True</span></span>                                                        |
| <span data-ttu-id="36c45-232">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="36c45-232">Is Indexed</span></span>             | <span data-ttu-id="36c45-233">Falso</span><span class="sxs-lookup"><span data-stu-id="36c45-233">False</span></span>                                                       |
| <span data-ttu-id="36c45-234">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="36c45-234">In Global Catalog</span></span>      | <span data-ttu-id="36c45-235">Falso</span><span class="sxs-lookup"><span data-stu-id="36c45-235">False</span></span>                                                       |
| <span data-ttu-id="36c45-236">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="36c45-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="36c45-237">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="36c45-237">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="36c45-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="36c45-238">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="36c45-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="36c45-239">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="36c45-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="36c45-240">Search-Flags</span></span>           | <span data-ttu-id="36c45-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="36c45-241">0x00000000</span></span>                                                  |
| <span data-ttu-id="36c45-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="36c45-242">System-Flags</span></span>           | <span data-ttu-id="36c45-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="36c45-243">0x00000010</span></span>                                                  |
| <span data-ttu-id="36c45-244">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="36c45-244">Classes used in</span></span>        | [<span data-ttu-id="36c45-245">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="36c45-245">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="36c45-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="36c45-246">Windows Server 2012</span></span>



| <span data-ttu-id="36c45-247">Voce</span><span class="sxs-lookup"><span data-stu-id="36c45-247">Entry</span></span> | <span data-ttu-id="36c45-248">Valore</span><span class="sxs-lookup"><span data-stu-id="36c45-248">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="36c45-249">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="36c45-249">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="36c45-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="36c45-250">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="36c45-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="36c45-251">System-Only</span></span>            | <span data-ttu-id="36c45-252">Falso</span><span class="sxs-lookup"><span data-stu-id="36c45-252">False</span></span>                                                       |
| <span data-ttu-id="36c45-253">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="36c45-253">Is-Single-Valued</span></span>       | <span data-ttu-id="36c45-254">Vero</span><span class="sxs-lookup"><span data-stu-id="36c45-254">True</span></span>                                                        |
| <span data-ttu-id="36c45-255">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="36c45-255">Is Indexed</span></span>             | <span data-ttu-id="36c45-256">Falso</span><span class="sxs-lookup"><span data-stu-id="36c45-256">False</span></span>                                                       |
| <span data-ttu-id="36c45-257">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="36c45-257">In Global Catalog</span></span>      | <span data-ttu-id="36c45-258">Falso</span><span class="sxs-lookup"><span data-stu-id="36c45-258">False</span></span>                                                       |
| <span data-ttu-id="36c45-259">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="36c45-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="36c45-260">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="36c45-260">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="36c45-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="36c45-261">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="36c45-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="36c45-262">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="36c45-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="36c45-263">Search-Flags</span></span>           | <span data-ttu-id="36c45-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="36c45-264">0x00000000</span></span>                                                  |
| <span data-ttu-id="36c45-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="36c45-265">System-Flags</span></span>           | <span data-ttu-id="36c45-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="36c45-266">0x00000010</span></span>                                                  |
| <span data-ttu-id="36c45-267">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="36c45-267">Classes used in</span></span>        | [<span data-ttu-id="36c45-268">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="36c45-268">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



 

 





