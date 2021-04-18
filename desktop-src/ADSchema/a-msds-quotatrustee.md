---
title: ms-DS-quota-attributo trustee
description: SID dell'entità di sicurezza a cui viene assegnata la quota.
ms.assetid: 4da8f731-0a8f-4d8a-a4e7-81ed881a30b5
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo ms-DS-quota-trustee
- attributo msDS-QuotaTrustee-schema AD
topic_type:
- apiref
api_name:
- ms-DS-Quota-Trustee
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7733e74c2f5d381aa6f52ea58bb03c377fab7cbe
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "106303245"
---
# <a name="ms-ds-quota-trustee-attribute"></a><span data-ttu-id="b8bd7-105">ms-DS-quota-attributo trustee</span><span class="sxs-lookup"><span data-stu-id="b8bd7-105">ms-DS-Quota-Trustee attribute</span></span>

<span data-ttu-id="b8bd7-106">SID dell'entità di sicurezza a cui viene assegnata la quota.</span><span class="sxs-lookup"><span data-stu-id="b8bd7-106">The SID of the security principal for which the quota is being assigned.</span></span>



| <span data-ttu-id="b8bd7-107">Voce</span><span class="sxs-lookup"><span data-stu-id="b8bd7-107">Entry</span></span> | <span data-ttu-id="b8bd7-108">Valore</span><span class="sxs-lookup"><span data-stu-id="b8bd7-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="b8bd7-109">CN</span><span class="sxs-lookup"><span data-stu-id="b8bd7-109">CN</span></span>                | <span data-ttu-id="b8bd7-110">ms-DS-quota-fiduciario</span><span class="sxs-lookup"><span data-stu-id="b8bd7-110">ms-DS-Quota-Trustee</span></span>                  |
| <span data-ttu-id="b8bd7-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="b8bd7-111">Ldap-Display-Name</span></span> | <span data-ttu-id="b8bd7-112">msDS-QuotaTrustee</span><span class="sxs-lookup"><span data-stu-id="b8bd7-112">msDS-QuotaTrustee</span></span>                    |
| <span data-ttu-id="b8bd7-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="b8bd7-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="b8bd7-114">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="b8bd7-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="b8bd7-115">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="b8bd7-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="b8bd7-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b8bd7-116">Attribute-Id</span></span>      | <span data-ttu-id="b8bd7-117">1.2.840.113556.1.4.1844</span><span class="sxs-lookup"><span data-stu-id="b8bd7-117">1.2.840.113556.1.4.1844</span></span>              |
| <span data-ttu-id="b8bd7-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="b8bd7-118">System-Id-Guid</span></span>    | <span data-ttu-id="b8bd7-119">16378906-4ea5-49be-a8d1-bfd41dff4f65</span><span class="sxs-lookup"><span data-stu-id="b8bd7-119">16378906-4ea5-49be-a8d1-bfd41dff4f65</span></span> |
| <span data-ttu-id="b8bd7-120">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b8bd7-120">Syntax</span></span>            | [<span data-ttu-id="b8bd7-121">**Stringa (SID)**</span><span class="sxs-lookup"><span data-stu-id="b8bd7-121">**String(Sid)**</span></span>](s-string-sid.md)  |



## <a name="implementations"></a><span data-ttu-id="b8bd7-122">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="b8bd7-122">Implementations</span></span>

-   [<span data-ttu-id="b8bd7-123">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b8bd7-123">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b8bd7-124">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="b8bd7-124">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="b8bd7-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b8bd7-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b8bd7-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b8bd7-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b8bd7-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b8bd7-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b8bd7-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b8bd7-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="b8bd7-129">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b8bd7-129">Windows Server 2003</span></span>



| <span data-ttu-id="b8bd7-130">Voce</span><span class="sxs-lookup"><span data-stu-id="b8bd7-130">Entry</span></span> | <span data-ttu-id="b8bd7-131">Valore</span><span class="sxs-lookup"><span data-stu-id="b8bd7-131">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="b8bd7-132">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="b8bd7-132">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="b8bd7-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b8bd7-133">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="b8bd7-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="b8bd7-134">System-Only</span></span>            | <span data-ttu-id="b8bd7-135">Falso</span><span class="sxs-lookup"><span data-stu-id="b8bd7-135">False</span></span>                                                         |
| <span data-ttu-id="b8bd7-136">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="b8bd7-136">Is-Single-Valued</span></span>       | <span data-ttu-id="b8bd7-137">Vero</span><span class="sxs-lookup"><span data-stu-id="b8bd7-137">True</span></span>                                                          |
| <span data-ttu-id="b8bd7-138">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="b8bd7-138">Is Indexed</span></span>             | <span data-ttu-id="b8bd7-139">Falso</span><span class="sxs-lookup"><span data-stu-id="b8bd7-139">False</span></span>                                                         |
| <span data-ttu-id="b8bd7-140">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="b8bd7-140">In Global Catalog</span></span>      | <span data-ttu-id="b8bd7-141">Falso</span><span class="sxs-lookup"><span data-stu-id="b8bd7-141">False</span></span>                                                         |
| <span data-ttu-id="b8bd7-142">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="b8bd7-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="b8bd7-143">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="b8bd7-143">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="b8bd7-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b8bd7-144">Range-Lower</span></span>            | <span data-ttu-id="b8bd7-145">0</span><span class="sxs-lookup"><span data-stu-id="b8bd7-145">0</span></span>                                                             |
| <span data-ttu-id="b8bd7-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b8bd7-146">Range-Upper</span></span>            | <span data-ttu-id="b8bd7-147">28</span><span class="sxs-lookup"><span data-stu-id="b8bd7-147">28</span></span>                                                            |
| <span data-ttu-id="b8bd7-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b8bd7-148">Search-Flags</span></span>           | <span data-ttu-id="b8bd7-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b8bd7-149">0x00000000</span></span>                                                    |
| <span data-ttu-id="b8bd7-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b8bd7-150">System-Flags</span></span>           | <span data-ttu-id="b8bd7-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b8bd7-151">0x00000010</span></span>                                                    |
| <span data-ttu-id="b8bd7-152">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="b8bd7-152">Classes used in</span></span>        | [<span data-ttu-id="b8bd7-153">**ms-DS-quota-controllo**</span><span class="sxs-lookup"><span data-stu-id="b8bd7-153">**ms-DS-Quota-Control**</span></span>](c-msds-quotacontrol.md)<br/> |



## <a name="adam"></a><span data-ttu-id="b8bd7-154">ADAM</span><span class="sxs-lookup"><span data-stu-id="b8bd7-154">ADAM</span></span>



| <span data-ttu-id="b8bd7-155">Voce</span><span class="sxs-lookup"><span data-stu-id="b8bd7-155">Entry</span></span> | <span data-ttu-id="b8bd7-156">Valore</span><span class="sxs-lookup"><span data-stu-id="b8bd7-156">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="b8bd7-157">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="b8bd7-157">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="b8bd7-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b8bd7-158">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="b8bd7-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="b8bd7-159">System-Only</span></span>            | <span data-ttu-id="b8bd7-160">Falso</span><span class="sxs-lookup"><span data-stu-id="b8bd7-160">False</span></span>                                                         |
| <span data-ttu-id="b8bd7-161">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="b8bd7-161">Is-Single-Valued</span></span>       | <span data-ttu-id="b8bd7-162">Vero</span><span class="sxs-lookup"><span data-stu-id="b8bd7-162">True</span></span>                                                          |
| <span data-ttu-id="b8bd7-163">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="b8bd7-163">Is Indexed</span></span>             | <span data-ttu-id="b8bd7-164">Falso</span><span class="sxs-lookup"><span data-stu-id="b8bd7-164">False</span></span>                                                         |
| <span data-ttu-id="b8bd7-165">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="b8bd7-165">In Global Catalog</span></span>      | <span data-ttu-id="b8bd7-166">Falso</span><span class="sxs-lookup"><span data-stu-id="b8bd7-166">False</span></span>                                                         |
| <span data-ttu-id="b8bd7-167">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="b8bd7-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="b8bd7-168">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="b8bd7-168">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="b8bd7-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b8bd7-169">Range-Lower</span></span>            | <span data-ttu-id="b8bd7-170">0</span><span class="sxs-lookup"><span data-stu-id="b8bd7-170">0</span></span>                                                             |
| <span data-ttu-id="b8bd7-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b8bd7-171">Range-Upper</span></span>            | <span data-ttu-id="b8bd7-172">28</span><span class="sxs-lookup"><span data-stu-id="b8bd7-172">28</span></span>                                                            |
| <span data-ttu-id="b8bd7-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b8bd7-173">Search-Flags</span></span>           | <span data-ttu-id="b8bd7-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b8bd7-174">0x00000000</span></span>                                                    |
| <span data-ttu-id="b8bd7-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b8bd7-175">System-Flags</span></span>           | <span data-ttu-id="b8bd7-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b8bd7-176">0x00000010</span></span>                                                    |
| <span data-ttu-id="b8bd7-177">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="b8bd7-177">Classes used in</span></span>        | [<span data-ttu-id="b8bd7-178">**ms-DS-quota-controllo**</span><span class="sxs-lookup"><span data-stu-id="b8bd7-178">**ms-DS-Quota-Control**</span></span>](c-msds-quotacontrol.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b8bd7-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b8bd7-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b8bd7-180">Voce</span><span class="sxs-lookup"><span data-stu-id="b8bd7-180">Entry</span></span> | <span data-ttu-id="b8bd7-181">Valore</span><span class="sxs-lookup"><span data-stu-id="b8bd7-181">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="b8bd7-182">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="b8bd7-182">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="b8bd7-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b8bd7-183">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="b8bd7-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="b8bd7-184">System-Only</span></span>            | <span data-ttu-id="b8bd7-185">Falso</span><span class="sxs-lookup"><span data-stu-id="b8bd7-185">False</span></span>                                                         |
| <span data-ttu-id="b8bd7-186">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="b8bd7-186">Is-Single-Valued</span></span>       | <span data-ttu-id="b8bd7-187">Vero</span><span class="sxs-lookup"><span data-stu-id="b8bd7-187">True</span></span>                                                          |
| <span data-ttu-id="b8bd7-188">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="b8bd7-188">Is Indexed</span></span>             | <span data-ttu-id="b8bd7-189">Falso</span><span class="sxs-lookup"><span data-stu-id="b8bd7-189">False</span></span>                                                         |
| <span data-ttu-id="b8bd7-190">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="b8bd7-190">In Global Catalog</span></span>      | <span data-ttu-id="b8bd7-191">Falso</span><span class="sxs-lookup"><span data-stu-id="b8bd7-191">False</span></span>                                                         |
| <span data-ttu-id="b8bd7-192">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="b8bd7-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="b8bd7-193">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="b8bd7-193">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="b8bd7-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b8bd7-194">Range-Lower</span></span>            | <span data-ttu-id="b8bd7-195">0</span><span class="sxs-lookup"><span data-stu-id="b8bd7-195">0</span></span>                                                             |
| <span data-ttu-id="b8bd7-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b8bd7-196">Range-Upper</span></span>            | <span data-ttu-id="b8bd7-197">28</span><span class="sxs-lookup"><span data-stu-id="b8bd7-197">28</span></span>                                                            |
| <span data-ttu-id="b8bd7-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b8bd7-198">Search-Flags</span></span>           | <span data-ttu-id="b8bd7-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b8bd7-199">0x00000000</span></span>                                                    |
| <span data-ttu-id="b8bd7-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b8bd7-200">System-Flags</span></span>           | <span data-ttu-id="b8bd7-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b8bd7-201">0x00000010</span></span>                                                    |
| <span data-ttu-id="b8bd7-202">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="b8bd7-202">Classes used in</span></span>        | [<span data-ttu-id="b8bd7-203">**ms-DS-quota-controllo**</span><span class="sxs-lookup"><span data-stu-id="b8bd7-203">**ms-DS-Quota-Control**</span></span>](c-msds-quotacontrol.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b8bd7-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b8bd7-204">Windows Server 2008</span></span>



| <span data-ttu-id="b8bd7-205">Voce</span><span class="sxs-lookup"><span data-stu-id="b8bd7-205">Entry</span></span> | <span data-ttu-id="b8bd7-206">Valore</span><span class="sxs-lookup"><span data-stu-id="b8bd7-206">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="b8bd7-207">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="b8bd7-207">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="b8bd7-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b8bd7-208">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="b8bd7-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="b8bd7-209">System-Only</span></span>            | <span data-ttu-id="b8bd7-210">Falso</span><span class="sxs-lookup"><span data-stu-id="b8bd7-210">False</span></span>                                                         |
| <span data-ttu-id="b8bd7-211">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="b8bd7-211">Is-Single-Valued</span></span>       | <span data-ttu-id="b8bd7-212">Vero</span><span class="sxs-lookup"><span data-stu-id="b8bd7-212">True</span></span>                                                          |
| <span data-ttu-id="b8bd7-213">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="b8bd7-213">Is Indexed</span></span>             | <span data-ttu-id="b8bd7-214">Falso</span><span class="sxs-lookup"><span data-stu-id="b8bd7-214">False</span></span>                                                         |
| <span data-ttu-id="b8bd7-215">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="b8bd7-215">In Global Catalog</span></span>      | <span data-ttu-id="b8bd7-216">Falso</span><span class="sxs-lookup"><span data-stu-id="b8bd7-216">False</span></span>                                                         |
| <span data-ttu-id="b8bd7-217">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="b8bd7-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="b8bd7-218">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="b8bd7-218">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="b8bd7-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b8bd7-219">Range-Lower</span></span>            | <span data-ttu-id="b8bd7-220">0</span><span class="sxs-lookup"><span data-stu-id="b8bd7-220">0</span></span>                                                             |
| <span data-ttu-id="b8bd7-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b8bd7-221">Range-Upper</span></span>            | <span data-ttu-id="b8bd7-222">28</span><span class="sxs-lookup"><span data-stu-id="b8bd7-222">28</span></span>                                                            |
| <span data-ttu-id="b8bd7-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b8bd7-223">Search-Flags</span></span>           | <span data-ttu-id="b8bd7-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b8bd7-224">0x00000000</span></span>                                                    |
| <span data-ttu-id="b8bd7-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b8bd7-225">System-Flags</span></span>           | <span data-ttu-id="b8bd7-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b8bd7-226">0x00000010</span></span>                                                    |
| <span data-ttu-id="b8bd7-227">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="b8bd7-227">Classes used in</span></span>        | [<span data-ttu-id="b8bd7-228">**ms-DS-quota-controllo**</span><span class="sxs-lookup"><span data-stu-id="b8bd7-228">**ms-DS-Quota-Control**</span></span>](c-msds-quotacontrol.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b8bd7-229">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b8bd7-229">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b8bd7-230">Voce</span><span class="sxs-lookup"><span data-stu-id="b8bd7-230">Entry</span></span> | <span data-ttu-id="b8bd7-231">Valore</span><span class="sxs-lookup"><span data-stu-id="b8bd7-231">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="b8bd7-232">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="b8bd7-232">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="b8bd7-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b8bd7-233">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="b8bd7-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="b8bd7-234">System-Only</span></span>            | <span data-ttu-id="b8bd7-235">Falso</span><span class="sxs-lookup"><span data-stu-id="b8bd7-235">False</span></span>                                                         |
| <span data-ttu-id="b8bd7-236">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="b8bd7-236">Is-Single-Valued</span></span>       | <span data-ttu-id="b8bd7-237">Vero</span><span class="sxs-lookup"><span data-stu-id="b8bd7-237">True</span></span>                                                          |
| <span data-ttu-id="b8bd7-238">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="b8bd7-238">Is Indexed</span></span>             | <span data-ttu-id="b8bd7-239">Falso</span><span class="sxs-lookup"><span data-stu-id="b8bd7-239">False</span></span>                                                         |
| <span data-ttu-id="b8bd7-240">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="b8bd7-240">In Global Catalog</span></span>      | <span data-ttu-id="b8bd7-241">Falso</span><span class="sxs-lookup"><span data-stu-id="b8bd7-241">False</span></span>                                                         |
| <span data-ttu-id="b8bd7-242">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="b8bd7-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="b8bd7-243">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="b8bd7-243">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="b8bd7-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b8bd7-244">Range-Lower</span></span>            | <span data-ttu-id="b8bd7-245">0</span><span class="sxs-lookup"><span data-stu-id="b8bd7-245">0</span></span>                                                             |
| <span data-ttu-id="b8bd7-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b8bd7-246">Range-Upper</span></span>            | <span data-ttu-id="b8bd7-247">28</span><span class="sxs-lookup"><span data-stu-id="b8bd7-247">28</span></span>                                                            |
| <span data-ttu-id="b8bd7-248">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b8bd7-248">Search-Flags</span></span>           | <span data-ttu-id="b8bd7-249">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b8bd7-249">0x00000000</span></span>                                                    |
| <span data-ttu-id="b8bd7-250">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b8bd7-250">System-Flags</span></span>           | <span data-ttu-id="b8bd7-251">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b8bd7-251">0x00000010</span></span>                                                    |
| <span data-ttu-id="b8bd7-252">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="b8bd7-252">Classes used in</span></span>        | [<span data-ttu-id="b8bd7-253">**ms-DS-quota-controllo**</span><span class="sxs-lookup"><span data-stu-id="b8bd7-253">**ms-DS-Quota-Control**</span></span>](c-msds-quotacontrol.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b8bd7-254">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b8bd7-254">Windows Server 2012</span></span>



| <span data-ttu-id="b8bd7-255">Voce</span><span class="sxs-lookup"><span data-stu-id="b8bd7-255">Entry</span></span> | <span data-ttu-id="b8bd7-256">Valore</span><span class="sxs-lookup"><span data-stu-id="b8bd7-256">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="b8bd7-257">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="b8bd7-257">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="b8bd7-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b8bd7-258">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="b8bd7-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="b8bd7-259">System-Only</span></span>            | <span data-ttu-id="b8bd7-260">Falso</span><span class="sxs-lookup"><span data-stu-id="b8bd7-260">False</span></span>                                                         |
| <span data-ttu-id="b8bd7-261">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="b8bd7-261">Is-Single-Valued</span></span>       | <span data-ttu-id="b8bd7-262">Vero</span><span class="sxs-lookup"><span data-stu-id="b8bd7-262">True</span></span>                                                          |
| <span data-ttu-id="b8bd7-263">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="b8bd7-263">Is Indexed</span></span>             | <span data-ttu-id="b8bd7-264">Falso</span><span class="sxs-lookup"><span data-stu-id="b8bd7-264">False</span></span>                                                         |
| <span data-ttu-id="b8bd7-265">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="b8bd7-265">In Global Catalog</span></span>      | <span data-ttu-id="b8bd7-266">Falso</span><span class="sxs-lookup"><span data-stu-id="b8bd7-266">False</span></span>                                                         |
| <span data-ttu-id="b8bd7-267">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="b8bd7-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="b8bd7-268">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="b8bd7-268">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="b8bd7-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b8bd7-269">Range-Lower</span></span>            | <span data-ttu-id="b8bd7-270">0</span><span class="sxs-lookup"><span data-stu-id="b8bd7-270">0</span></span>                                                             |
| <span data-ttu-id="b8bd7-271">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b8bd7-271">Range-Upper</span></span>            | <span data-ttu-id="b8bd7-272">28</span><span class="sxs-lookup"><span data-stu-id="b8bd7-272">28</span></span>                                                            |
| <span data-ttu-id="b8bd7-273">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b8bd7-273">Search-Flags</span></span>           | <span data-ttu-id="b8bd7-274">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b8bd7-274">0x00000000</span></span>                                                    |
| <span data-ttu-id="b8bd7-275">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b8bd7-275">System-Flags</span></span>           | <span data-ttu-id="b8bd7-276">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b8bd7-276">0x00000010</span></span>                                                    |
| <span data-ttu-id="b8bd7-277">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="b8bd7-277">Classes used in</span></span>        | [<span data-ttu-id="b8bd7-278">**ms-DS-quota-controllo**</span><span class="sxs-lookup"><span data-stu-id="b8bd7-278">**ms-DS-Quota-Control**</span></span>](c-msds-quotacontrol.md)<br/> |



 

 





