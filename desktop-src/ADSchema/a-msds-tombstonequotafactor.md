---
title: ms-DS-Tombstone-quota-Factor-attributo
description: Fattore percentuale in base al quale il conteggio degli oggetti contrassegnato per la rimozione definitiva deve essere ridotto a scopo di contabilità delle quote.
ms.assetid: 602c2fe0-d3b7-45e8-8ce8-35a7163f7b25
ms.tgt_platform: multiple
keywords:
- Schema AD degli attributi ms-DS-Tombstone-quote-Factor
- attributo msDS-TombstoneQuotaFactor-schema AD
topic_type:
- apiref
api_name:
- ms-DS-Tombstone-Quota-Factor
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a44dd7f648754c2ded7334c9b221022d936ebfb
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104519798"
---
# <a name="ms-ds-tombstone-quota-factor-attribute"></a><span data-ttu-id="2fcdc-105">ms-DS-Tombstone-quota-Factor-attributo</span><span class="sxs-lookup"><span data-stu-id="2fcdc-105">ms-DS-Tombstone-Quota-Factor attribute</span></span>

<span data-ttu-id="2fcdc-106">Fattore percentuale in base al quale il conteggio degli oggetti contrassegnato per la rimozione definitiva deve essere ridotto a scopo di contabilità delle quote.</span><span class="sxs-lookup"><span data-stu-id="2fcdc-106">The percentage factor by which the tombstone object count should be reduced for the purpose of quota accounting.</span></span>



| <span data-ttu-id="2fcdc-107">Voce</span><span class="sxs-lookup"><span data-stu-id="2fcdc-107">Entry</span></span> | <span data-ttu-id="2fcdc-108">Valore</span><span class="sxs-lookup"><span data-stu-id="2fcdc-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="2fcdc-109">CN</span><span class="sxs-lookup"><span data-stu-id="2fcdc-109">CN</span></span>                | <span data-ttu-id="2fcdc-110">ms-DS-Tombstone-quota-fattore</span><span class="sxs-lookup"><span data-stu-id="2fcdc-110">ms-DS-Tombstone-Quota-Factor</span></span>         |
| <span data-ttu-id="2fcdc-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="2fcdc-111">Ldap-Display-Name</span></span> | <span data-ttu-id="2fcdc-112">msDS-TombstoneQuotaFactor</span><span class="sxs-lookup"><span data-stu-id="2fcdc-112">msDS-TombstoneQuotaFactor</span></span>            |
| <span data-ttu-id="2fcdc-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="2fcdc-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="2fcdc-114">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="2fcdc-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="2fcdc-115">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="2fcdc-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="2fcdc-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="2fcdc-116">Attribute-Id</span></span>      | <span data-ttu-id="2fcdc-117">1.2.840.113556.1.4.1847</span><span class="sxs-lookup"><span data-stu-id="2fcdc-117">1.2.840.113556.1.4.1847</span></span>              |
| <span data-ttu-id="2fcdc-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="2fcdc-118">System-Id-Guid</span></span>    | <span data-ttu-id="2fcdc-119">461744d7-f3b6-45ba-8753-fb9552a5df32</span><span class="sxs-lookup"><span data-stu-id="2fcdc-119">461744d7-f3b6-45ba-8753-fb9552a5df32</span></span> |
| <span data-ttu-id="2fcdc-120">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2fcdc-120">Syntax</span></span>            | [<span data-ttu-id="2fcdc-121">**Enumerazione**</span><span class="sxs-lookup"><span data-stu-id="2fcdc-121">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="2fcdc-122">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="2fcdc-122">Implementations</span></span>

-   [<span data-ttu-id="2fcdc-123">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="2fcdc-123">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="2fcdc-124">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="2fcdc-124">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="2fcdc-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="2fcdc-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="2fcdc-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="2fcdc-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="2fcdc-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="2fcdc-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="2fcdc-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="2fcdc-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="2fcdc-129">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2fcdc-129">Windows Server 2003</span></span>



| <span data-ttu-id="2fcdc-130">Voce</span><span class="sxs-lookup"><span data-stu-id="2fcdc-130">Entry</span></span> | <span data-ttu-id="2fcdc-131">Valore</span><span class="sxs-lookup"><span data-stu-id="2fcdc-131">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="2fcdc-132">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="2fcdc-132">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="2fcdc-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2fcdc-133">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="2fcdc-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="2fcdc-134">System-Only</span></span>            | <span data-ttu-id="2fcdc-135">Falso</span><span class="sxs-lookup"><span data-stu-id="2fcdc-135">False</span></span>                                                             |
| <span data-ttu-id="2fcdc-136">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="2fcdc-136">Is-Single-Valued</span></span>       | <span data-ttu-id="2fcdc-137">Vero</span><span class="sxs-lookup"><span data-stu-id="2fcdc-137">True</span></span>                                                              |
| <span data-ttu-id="2fcdc-138">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="2fcdc-138">Is Indexed</span></span>             | <span data-ttu-id="2fcdc-139">Falso</span><span class="sxs-lookup"><span data-stu-id="2fcdc-139">False</span></span>                                                             |
| <span data-ttu-id="2fcdc-140">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="2fcdc-140">In Global Catalog</span></span>      | <span data-ttu-id="2fcdc-141">Falso</span><span class="sxs-lookup"><span data-stu-id="2fcdc-141">False</span></span>                                                             |
| <span data-ttu-id="2fcdc-142">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="2fcdc-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="2fcdc-143">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="2fcdc-143">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="2fcdc-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2fcdc-144">Range-Lower</span></span>            | <span data-ttu-id="2fcdc-145">0</span><span class="sxs-lookup"><span data-stu-id="2fcdc-145">0</span></span>                                                                 |
| <span data-ttu-id="2fcdc-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2fcdc-146">Range-Upper</span></span>            | <span data-ttu-id="2fcdc-147">100</span><span class="sxs-lookup"><span data-stu-id="2fcdc-147">100</span></span>                                                               |
| <span data-ttu-id="2fcdc-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2fcdc-148">Search-Flags</span></span>           | <span data-ttu-id="2fcdc-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2fcdc-149">0x00000000</span></span>                                                        |
| <span data-ttu-id="2fcdc-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2fcdc-150">System-Flags</span></span>           | <span data-ttu-id="2fcdc-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2fcdc-151">0x00000010</span></span>                                                        |
| <span data-ttu-id="2fcdc-152">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="2fcdc-152">Classes used in</span></span>        | [<span data-ttu-id="2fcdc-153">**ms-DS-quota-contenitore**</span><span class="sxs-lookup"><span data-stu-id="2fcdc-153">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="adam"></a><span data-ttu-id="2fcdc-154">ADAM</span><span class="sxs-lookup"><span data-stu-id="2fcdc-154">ADAM</span></span>



| <span data-ttu-id="2fcdc-155">Voce</span><span class="sxs-lookup"><span data-stu-id="2fcdc-155">Entry</span></span> | <span data-ttu-id="2fcdc-156">Valore</span><span class="sxs-lookup"><span data-stu-id="2fcdc-156">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="2fcdc-157">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="2fcdc-157">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="2fcdc-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2fcdc-158">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="2fcdc-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="2fcdc-159">System-Only</span></span>            | <span data-ttu-id="2fcdc-160">Falso</span><span class="sxs-lookup"><span data-stu-id="2fcdc-160">False</span></span>                                                             |
| <span data-ttu-id="2fcdc-161">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="2fcdc-161">Is-Single-Valued</span></span>       | <span data-ttu-id="2fcdc-162">Vero</span><span class="sxs-lookup"><span data-stu-id="2fcdc-162">True</span></span>                                                              |
| <span data-ttu-id="2fcdc-163">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="2fcdc-163">Is Indexed</span></span>             | <span data-ttu-id="2fcdc-164">Falso</span><span class="sxs-lookup"><span data-stu-id="2fcdc-164">False</span></span>                                                             |
| <span data-ttu-id="2fcdc-165">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="2fcdc-165">In Global Catalog</span></span>      | <span data-ttu-id="2fcdc-166">Falso</span><span class="sxs-lookup"><span data-stu-id="2fcdc-166">False</span></span>                                                             |
| <span data-ttu-id="2fcdc-167">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="2fcdc-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="2fcdc-168">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="2fcdc-168">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="2fcdc-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2fcdc-169">Range-Lower</span></span>            | <span data-ttu-id="2fcdc-170">0</span><span class="sxs-lookup"><span data-stu-id="2fcdc-170">0</span></span>                                                                 |
| <span data-ttu-id="2fcdc-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2fcdc-171">Range-Upper</span></span>            | <span data-ttu-id="2fcdc-172">100</span><span class="sxs-lookup"><span data-stu-id="2fcdc-172">100</span></span>                                                               |
| <span data-ttu-id="2fcdc-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2fcdc-173">Search-Flags</span></span>           | <span data-ttu-id="2fcdc-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2fcdc-174">0x00000000</span></span>                                                        |
| <span data-ttu-id="2fcdc-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2fcdc-175">System-Flags</span></span>           | <span data-ttu-id="2fcdc-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2fcdc-176">0x00000010</span></span>                                                        |
| <span data-ttu-id="2fcdc-177">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="2fcdc-177">Classes used in</span></span>        | [<span data-ttu-id="2fcdc-178">**ms-DS-quota-contenitore**</span><span class="sxs-lookup"><span data-stu-id="2fcdc-178">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="2fcdc-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="2fcdc-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="2fcdc-180">Voce</span><span class="sxs-lookup"><span data-stu-id="2fcdc-180">Entry</span></span> | <span data-ttu-id="2fcdc-181">Valore</span><span class="sxs-lookup"><span data-stu-id="2fcdc-181">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="2fcdc-182">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="2fcdc-182">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="2fcdc-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2fcdc-183">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="2fcdc-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="2fcdc-184">System-Only</span></span>            | <span data-ttu-id="2fcdc-185">Falso</span><span class="sxs-lookup"><span data-stu-id="2fcdc-185">False</span></span>                                                             |
| <span data-ttu-id="2fcdc-186">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="2fcdc-186">Is-Single-Valued</span></span>       | <span data-ttu-id="2fcdc-187">Vero</span><span class="sxs-lookup"><span data-stu-id="2fcdc-187">True</span></span>                                                              |
| <span data-ttu-id="2fcdc-188">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="2fcdc-188">Is Indexed</span></span>             | <span data-ttu-id="2fcdc-189">Falso</span><span class="sxs-lookup"><span data-stu-id="2fcdc-189">False</span></span>                                                             |
| <span data-ttu-id="2fcdc-190">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="2fcdc-190">In Global Catalog</span></span>      | <span data-ttu-id="2fcdc-191">Falso</span><span class="sxs-lookup"><span data-stu-id="2fcdc-191">False</span></span>                                                             |
| <span data-ttu-id="2fcdc-192">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="2fcdc-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="2fcdc-193">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="2fcdc-193">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="2fcdc-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2fcdc-194">Range-Lower</span></span>            | <span data-ttu-id="2fcdc-195">0</span><span class="sxs-lookup"><span data-stu-id="2fcdc-195">0</span></span>                                                                 |
| <span data-ttu-id="2fcdc-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2fcdc-196">Range-Upper</span></span>            | <span data-ttu-id="2fcdc-197">100</span><span class="sxs-lookup"><span data-stu-id="2fcdc-197">100</span></span>                                                               |
| <span data-ttu-id="2fcdc-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2fcdc-198">Search-Flags</span></span>           | <span data-ttu-id="2fcdc-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2fcdc-199">0x00000000</span></span>                                                        |
| <span data-ttu-id="2fcdc-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2fcdc-200">System-Flags</span></span>           | <span data-ttu-id="2fcdc-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2fcdc-201">0x00000010</span></span>                                                        |
| <span data-ttu-id="2fcdc-202">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="2fcdc-202">Classes used in</span></span>        | [<span data-ttu-id="2fcdc-203">**ms-DS-quota-contenitore**</span><span class="sxs-lookup"><span data-stu-id="2fcdc-203">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="2fcdc-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2fcdc-204">Windows Server 2008</span></span>



| <span data-ttu-id="2fcdc-205">Voce</span><span class="sxs-lookup"><span data-stu-id="2fcdc-205">Entry</span></span> | <span data-ttu-id="2fcdc-206">Valore</span><span class="sxs-lookup"><span data-stu-id="2fcdc-206">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="2fcdc-207">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="2fcdc-207">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="2fcdc-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2fcdc-208">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="2fcdc-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="2fcdc-209">System-Only</span></span>            | <span data-ttu-id="2fcdc-210">Falso</span><span class="sxs-lookup"><span data-stu-id="2fcdc-210">False</span></span>                                                             |
| <span data-ttu-id="2fcdc-211">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="2fcdc-211">Is-Single-Valued</span></span>       | <span data-ttu-id="2fcdc-212">Vero</span><span class="sxs-lookup"><span data-stu-id="2fcdc-212">True</span></span>                                                              |
| <span data-ttu-id="2fcdc-213">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="2fcdc-213">Is Indexed</span></span>             | <span data-ttu-id="2fcdc-214">Falso</span><span class="sxs-lookup"><span data-stu-id="2fcdc-214">False</span></span>                                                             |
| <span data-ttu-id="2fcdc-215">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="2fcdc-215">In Global Catalog</span></span>      | <span data-ttu-id="2fcdc-216">Falso</span><span class="sxs-lookup"><span data-stu-id="2fcdc-216">False</span></span>                                                             |
| <span data-ttu-id="2fcdc-217">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="2fcdc-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="2fcdc-218">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="2fcdc-218">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="2fcdc-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2fcdc-219">Range-Lower</span></span>            | <span data-ttu-id="2fcdc-220">0</span><span class="sxs-lookup"><span data-stu-id="2fcdc-220">0</span></span>                                                                 |
| <span data-ttu-id="2fcdc-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2fcdc-221">Range-Upper</span></span>            | <span data-ttu-id="2fcdc-222">100</span><span class="sxs-lookup"><span data-stu-id="2fcdc-222">100</span></span>                                                               |
| <span data-ttu-id="2fcdc-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2fcdc-223">Search-Flags</span></span>           | <span data-ttu-id="2fcdc-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2fcdc-224">0x00000000</span></span>                                                        |
| <span data-ttu-id="2fcdc-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2fcdc-225">System-Flags</span></span>           | <span data-ttu-id="2fcdc-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2fcdc-226">0x00000010</span></span>                                                        |
| <span data-ttu-id="2fcdc-227">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="2fcdc-227">Classes used in</span></span>        | [<span data-ttu-id="2fcdc-228">**ms-DS-quota-contenitore**</span><span class="sxs-lookup"><span data-stu-id="2fcdc-228">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="2fcdc-229">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2fcdc-229">Windows Server 2008 R2</span></span>



| <span data-ttu-id="2fcdc-230">Voce</span><span class="sxs-lookup"><span data-stu-id="2fcdc-230">Entry</span></span> | <span data-ttu-id="2fcdc-231">Valore</span><span class="sxs-lookup"><span data-stu-id="2fcdc-231">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="2fcdc-232">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="2fcdc-232">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="2fcdc-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2fcdc-233">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="2fcdc-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="2fcdc-234">System-Only</span></span>            | <span data-ttu-id="2fcdc-235">Falso</span><span class="sxs-lookup"><span data-stu-id="2fcdc-235">False</span></span>                                                             |
| <span data-ttu-id="2fcdc-236">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="2fcdc-236">Is-Single-Valued</span></span>       | <span data-ttu-id="2fcdc-237">Vero</span><span class="sxs-lookup"><span data-stu-id="2fcdc-237">True</span></span>                                                              |
| <span data-ttu-id="2fcdc-238">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="2fcdc-238">Is Indexed</span></span>             | <span data-ttu-id="2fcdc-239">Falso</span><span class="sxs-lookup"><span data-stu-id="2fcdc-239">False</span></span>                                                             |
| <span data-ttu-id="2fcdc-240">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="2fcdc-240">In Global Catalog</span></span>      | <span data-ttu-id="2fcdc-241">Falso</span><span class="sxs-lookup"><span data-stu-id="2fcdc-241">False</span></span>                                                             |
| <span data-ttu-id="2fcdc-242">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="2fcdc-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="2fcdc-243">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="2fcdc-243">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="2fcdc-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2fcdc-244">Range-Lower</span></span>            | <span data-ttu-id="2fcdc-245">0</span><span class="sxs-lookup"><span data-stu-id="2fcdc-245">0</span></span>                                                                 |
| <span data-ttu-id="2fcdc-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2fcdc-246">Range-Upper</span></span>            | <span data-ttu-id="2fcdc-247">100</span><span class="sxs-lookup"><span data-stu-id="2fcdc-247">100</span></span>                                                               |
| <span data-ttu-id="2fcdc-248">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2fcdc-248">Search-Flags</span></span>           | <span data-ttu-id="2fcdc-249">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2fcdc-249">0x00000000</span></span>                                                        |
| <span data-ttu-id="2fcdc-250">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2fcdc-250">System-Flags</span></span>           | <span data-ttu-id="2fcdc-251">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2fcdc-251">0x00000010</span></span>                                                        |
| <span data-ttu-id="2fcdc-252">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="2fcdc-252">Classes used in</span></span>        | [<span data-ttu-id="2fcdc-253">**ms-DS-quota-contenitore**</span><span class="sxs-lookup"><span data-stu-id="2fcdc-253">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="2fcdc-254">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2fcdc-254">Windows Server 2012</span></span>



| <span data-ttu-id="2fcdc-255">Voce</span><span class="sxs-lookup"><span data-stu-id="2fcdc-255">Entry</span></span> | <span data-ttu-id="2fcdc-256">Valore</span><span class="sxs-lookup"><span data-stu-id="2fcdc-256">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="2fcdc-257">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="2fcdc-257">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="2fcdc-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2fcdc-258">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="2fcdc-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="2fcdc-259">System-Only</span></span>            | <span data-ttu-id="2fcdc-260">Falso</span><span class="sxs-lookup"><span data-stu-id="2fcdc-260">False</span></span>                                                             |
| <span data-ttu-id="2fcdc-261">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="2fcdc-261">Is-Single-Valued</span></span>       | <span data-ttu-id="2fcdc-262">Vero</span><span class="sxs-lookup"><span data-stu-id="2fcdc-262">True</span></span>                                                              |
| <span data-ttu-id="2fcdc-263">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="2fcdc-263">Is Indexed</span></span>             | <span data-ttu-id="2fcdc-264">Falso</span><span class="sxs-lookup"><span data-stu-id="2fcdc-264">False</span></span>                                                             |
| <span data-ttu-id="2fcdc-265">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="2fcdc-265">In Global Catalog</span></span>      | <span data-ttu-id="2fcdc-266">Falso</span><span class="sxs-lookup"><span data-stu-id="2fcdc-266">False</span></span>                                                             |
| <span data-ttu-id="2fcdc-267">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="2fcdc-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="2fcdc-268">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="2fcdc-268">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="2fcdc-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2fcdc-269">Range-Lower</span></span>            | <span data-ttu-id="2fcdc-270">0</span><span class="sxs-lookup"><span data-stu-id="2fcdc-270">0</span></span>                                                                 |
| <span data-ttu-id="2fcdc-271">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2fcdc-271">Range-Upper</span></span>            | <span data-ttu-id="2fcdc-272">100</span><span class="sxs-lookup"><span data-stu-id="2fcdc-272">100</span></span>                                                               |
| <span data-ttu-id="2fcdc-273">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2fcdc-273">Search-Flags</span></span>           | <span data-ttu-id="2fcdc-274">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2fcdc-274">0x00000000</span></span>                                                        |
| <span data-ttu-id="2fcdc-275">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2fcdc-275">System-Flags</span></span>           | <span data-ttu-id="2fcdc-276">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2fcdc-276">0x00000010</span></span>                                                        |
| <span data-ttu-id="2fcdc-277">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="2fcdc-277">Classes used in</span></span>        | [<span data-ttu-id="2fcdc-278">**ms-DS-quota-contenitore**</span><span class="sxs-lookup"><span data-stu-id="2fcdc-278">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



 

 





