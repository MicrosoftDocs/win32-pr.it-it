---
title: Attributo MS-DS-per-User-Trust-tombstones-quota
description: Consente di applicare una quota per utente per l'eliminazione di oggetti Trusted-Domain quando l'autorizzazione è basata sulla corrispondenza del SID dell'utente.
ms.assetid: 4db98754-a2d1-43a4-b9cb-0e3fcbbf3ed9
ms.tgt_platform: multiple
keywords:
- MS-DS-per-User-Trust-tombstones-schema AD dell'attributo quota
- attributo msDS-PerUserTrustTombstonesQuota-schema AD
topic_type:
- apiref
api_name:
- MS-DS-Per-User-Trust-Tombstones-Quota
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c94bb62b822552a863df99dac83e98462514c42
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "106303248"
---
# <a name="ms-ds-per-user-trust-tombstones-quota-attribute"></a><span data-ttu-id="99052-105">Attributo MS-DS-per-User-Trust-tombstones-quota</span><span class="sxs-lookup"><span data-stu-id="99052-105">MS-DS-Per-User-Trust-Tombstones-Quota attribute</span></span>

<span data-ttu-id="99052-106">Consente di applicare una quota per utente per l'eliminazione di oggetti Trusted-Domain quando l'autorizzazione è basata sulla corrispondenza del SID dell'utente.</span><span class="sxs-lookup"><span data-stu-id="99052-106">Used to enforce a per-user quota for deleting Trusted-Domain objects when authorization is based on matching the user's SID.</span></span>



| <span data-ttu-id="99052-107">Voce</span><span class="sxs-lookup"><span data-stu-id="99052-107">Entry</span></span> | <span data-ttu-id="99052-108">Valore</span><span class="sxs-lookup"><span data-stu-id="99052-108">Value</span></span> |
|-------------------|-------------------------------------------|
| <span data-ttu-id="99052-109">CN</span><span class="sxs-lookup"><span data-stu-id="99052-109">CN</span></span>                | <span data-ttu-id="99052-110">MS-DS-per utente-Trust-Tombstone-quota</span><span class="sxs-lookup"><span data-stu-id="99052-110">MS-DS-Per-User-Trust-Tombstones-Quota</span></span>     |
| <span data-ttu-id="99052-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="99052-111">Ldap-Display-Name</span></span> | <span data-ttu-id="99052-112">msDS-PerUserTrustTombstonesQuota</span><span class="sxs-lookup"><span data-stu-id="99052-112">msDS-PerUserTrustTombstonesQuota</span></span>          |
| <span data-ttu-id="99052-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="99052-113">Size</span></span>              | \-                                        |
| <span data-ttu-id="99052-114">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="99052-114">Update Privilege</span></span>  | <span data-ttu-id="99052-115">Amministratore di dominio</span><span class="sxs-lookup"><span data-stu-id="99052-115">Domain administrator</span></span>                      |
| <span data-ttu-id="99052-116">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="99052-116">Update Frequency</span></span>  | <span data-ttu-id="99052-117">Alla creazione della foresta e, successivamente, raramente.</span><span class="sxs-lookup"><span data-stu-id="99052-117">At forest creation and rarely after that.</span></span> |
| <span data-ttu-id="99052-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="99052-118">Attribute-Id</span></span>      | <span data-ttu-id="99052-119">1.2.840.113556.1.4.1790</span><span class="sxs-lookup"><span data-stu-id="99052-119">1.2.840.113556.1.4.1790</span></span>                   |
| <span data-ttu-id="99052-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="99052-120">System-Id-Guid</span></span>    | <span data-ttu-id="99052-121">8b70a6c6-50f9-4fa3-a71e-1ce03040449b</span><span class="sxs-lookup"><span data-stu-id="99052-121">8b70a6c6-50f9-4fa3-a71e-1ce03040449b</span></span>      |
| <span data-ttu-id="99052-122">Sintassi</span><span class="sxs-lookup"><span data-stu-id="99052-122">Syntax</span></span>            | [<span data-ttu-id="99052-123">**Enumerazione**</span><span class="sxs-lookup"><span data-stu-id="99052-123">**Enumeration**</span></span>](s-enumeration.md)      |



## <a name="implementations"></a><span data-ttu-id="99052-124">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="99052-124">Implementations</span></span>

-   [<span data-ttu-id="99052-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="99052-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="99052-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="99052-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="99052-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="99052-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="99052-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="99052-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="99052-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="99052-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="99052-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="99052-130">Windows Server 2003</span></span>



| <span data-ttu-id="99052-131">Voce</span><span class="sxs-lookup"><span data-stu-id="99052-131">Entry</span></span> | <span data-ttu-id="99052-132">Valore</span><span class="sxs-lookup"><span data-stu-id="99052-132">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="99052-133">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="99052-133">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="99052-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="99052-134">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="99052-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="99052-135">System-Only</span></span>            | <span data-ttu-id="99052-136">Falso</span><span class="sxs-lookup"><span data-stu-id="99052-136">False</span></span>                                        |
| <span data-ttu-id="99052-137">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="99052-137">Is-Single-Valued</span></span>       | <span data-ttu-id="99052-138">Vero</span><span class="sxs-lookup"><span data-stu-id="99052-138">True</span></span>                                         |
| <span data-ttu-id="99052-139">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="99052-139">Is Indexed</span></span>             | <span data-ttu-id="99052-140">Falso</span><span class="sxs-lookup"><span data-stu-id="99052-140">False</span></span>                                        |
| <span data-ttu-id="99052-141">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="99052-141">In Global Catalog</span></span>      | <span data-ttu-id="99052-142">Falso</span><span class="sxs-lookup"><span data-stu-id="99052-142">False</span></span>                                        |
| <span data-ttu-id="99052-143">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="99052-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="99052-144">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="99052-144">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="99052-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="99052-145">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="99052-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="99052-146">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="99052-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="99052-147">Search-Flags</span></span>           | <span data-ttu-id="99052-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="99052-148">0x00000000</span></span>                                   |
| <span data-ttu-id="99052-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="99052-149">System-Flags</span></span>           | <span data-ttu-id="99052-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="99052-150">0x00000010</span></span>                                   |
| <span data-ttu-id="99052-151">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="99052-151">Classes used in</span></span>        | [<span data-ttu-id="99052-152">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="99052-152">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="99052-153">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="99052-153">Windows Server 2003 R2</span></span>



| <span data-ttu-id="99052-154">Voce</span><span class="sxs-lookup"><span data-stu-id="99052-154">Entry</span></span> | <span data-ttu-id="99052-155">Valore</span><span class="sxs-lookup"><span data-stu-id="99052-155">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="99052-156">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="99052-156">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="99052-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="99052-157">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="99052-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="99052-158">System-Only</span></span>            | <span data-ttu-id="99052-159">Falso</span><span class="sxs-lookup"><span data-stu-id="99052-159">False</span></span>                                        |
| <span data-ttu-id="99052-160">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="99052-160">Is-Single-Valued</span></span>       | <span data-ttu-id="99052-161">Vero</span><span class="sxs-lookup"><span data-stu-id="99052-161">True</span></span>                                         |
| <span data-ttu-id="99052-162">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="99052-162">Is Indexed</span></span>             | <span data-ttu-id="99052-163">Falso</span><span class="sxs-lookup"><span data-stu-id="99052-163">False</span></span>                                        |
| <span data-ttu-id="99052-164">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="99052-164">In Global Catalog</span></span>      | <span data-ttu-id="99052-165">Falso</span><span class="sxs-lookup"><span data-stu-id="99052-165">False</span></span>                                        |
| <span data-ttu-id="99052-166">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="99052-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="99052-167">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="99052-167">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="99052-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="99052-168">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="99052-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="99052-169">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="99052-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="99052-170">Search-Flags</span></span>           | <span data-ttu-id="99052-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="99052-171">0x00000000</span></span>                                   |
| <span data-ttu-id="99052-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="99052-172">System-Flags</span></span>           | <span data-ttu-id="99052-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="99052-173">0x00000010</span></span>                                   |
| <span data-ttu-id="99052-174">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="99052-174">Classes used in</span></span>        | [<span data-ttu-id="99052-175">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="99052-175">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="99052-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="99052-176">Windows Server 2008</span></span>



| <span data-ttu-id="99052-177">Voce</span><span class="sxs-lookup"><span data-stu-id="99052-177">Entry</span></span> | <span data-ttu-id="99052-178">Valore</span><span class="sxs-lookup"><span data-stu-id="99052-178">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="99052-179">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="99052-179">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="99052-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="99052-180">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="99052-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="99052-181">System-Only</span></span>            | <span data-ttu-id="99052-182">Falso</span><span class="sxs-lookup"><span data-stu-id="99052-182">False</span></span>                                        |
| <span data-ttu-id="99052-183">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="99052-183">Is-Single-Valued</span></span>       | <span data-ttu-id="99052-184">Vero</span><span class="sxs-lookup"><span data-stu-id="99052-184">True</span></span>                                         |
| <span data-ttu-id="99052-185">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="99052-185">Is Indexed</span></span>             | <span data-ttu-id="99052-186">Falso</span><span class="sxs-lookup"><span data-stu-id="99052-186">False</span></span>                                        |
| <span data-ttu-id="99052-187">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="99052-187">In Global Catalog</span></span>      | <span data-ttu-id="99052-188">Falso</span><span class="sxs-lookup"><span data-stu-id="99052-188">False</span></span>                                        |
| <span data-ttu-id="99052-189">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="99052-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="99052-190">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="99052-190">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="99052-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="99052-191">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="99052-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="99052-192">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="99052-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="99052-193">Search-Flags</span></span>           | <span data-ttu-id="99052-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="99052-194">0x00000000</span></span>                                   |
| <span data-ttu-id="99052-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="99052-195">System-Flags</span></span>           | <span data-ttu-id="99052-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="99052-196">0x00000010</span></span>                                   |
| <span data-ttu-id="99052-197">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="99052-197">Classes used in</span></span>        | [<span data-ttu-id="99052-198">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="99052-198">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="99052-199">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="99052-199">Windows Server 2008 R2</span></span>



| <span data-ttu-id="99052-200">Voce</span><span class="sxs-lookup"><span data-stu-id="99052-200">Entry</span></span> | <span data-ttu-id="99052-201">Valore</span><span class="sxs-lookup"><span data-stu-id="99052-201">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="99052-202">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="99052-202">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="99052-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="99052-203">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="99052-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="99052-204">System-Only</span></span>            | <span data-ttu-id="99052-205">Falso</span><span class="sxs-lookup"><span data-stu-id="99052-205">False</span></span>                                        |
| <span data-ttu-id="99052-206">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="99052-206">Is-Single-Valued</span></span>       | <span data-ttu-id="99052-207">Vero</span><span class="sxs-lookup"><span data-stu-id="99052-207">True</span></span>                                         |
| <span data-ttu-id="99052-208">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="99052-208">Is Indexed</span></span>             | <span data-ttu-id="99052-209">Falso</span><span class="sxs-lookup"><span data-stu-id="99052-209">False</span></span>                                        |
| <span data-ttu-id="99052-210">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="99052-210">In Global Catalog</span></span>      | <span data-ttu-id="99052-211">Falso</span><span class="sxs-lookup"><span data-stu-id="99052-211">False</span></span>                                        |
| <span data-ttu-id="99052-212">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="99052-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="99052-213">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="99052-213">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="99052-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="99052-214">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="99052-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="99052-215">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="99052-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="99052-216">Search-Flags</span></span>           | <span data-ttu-id="99052-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="99052-217">0x00000000</span></span>                                   |
| <span data-ttu-id="99052-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="99052-218">System-Flags</span></span>           | <span data-ttu-id="99052-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="99052-219">0x00000010</span></span>                                   |
| <span data-ttu-id="99052-220">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="99052-220">Classes used in</span></span>        | [<span data-ttu-id="99052-221">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="99052-221">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="99052-222">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="99052-222">Windows Server 2012</span></span>



| <span data-ttu-id="99052-223">Voce</span><span class="sxs-lookup"><span data-stu-id="99052-223">Entry</span></span> | <span data-ttu-id="99052-224">Valore</span><span class="sxs-lookup"><span data-stu-id="99052-224">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="99052-225">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="99052-225">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="99052-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="99052-226">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="99052-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="99052-227">System-Only</span></span>            | <span data-ttu-id="99052-228">Falso</span><span class="sxs-lookup"><span data-stu-id="99052-228">False</span></span>                                        |
| <span data-ttu-id="99052-229">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="99052-229">Is-Single-Valued</span></span>       | <span data-ttu-id="99052-230">Vero</span><span class="sxs-lookup"><span data-stu-id="99052-230">True</span></span>                                         |
| <span data-ttu-id="99052-231">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="99052-231">Is Indexed</span></span>             | <span data-ttu-id="99052-232">Falso</span><span class="sxs-lookup"><span data-stu-id="99052-232">False</span></span>                                        |
| <span data-ttu-id="99052-233">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="99052-233">In Global Catalog</span></span>      | <span data-ttu-id="99052-234">Falso</span><span class="sxs-lookup"><span data-stu-id="99052-234">False</span></span>                                        |
| <span data-ttu-id="99052-235">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="99052-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="99052-236">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="99052-236">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="99052-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="99052-237">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="99052-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="99052-238">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="99052-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="99052-239">Search-Flags</span></span>           | <span data-ttu-id="99052-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="99052-240">0x00000000</span></span>                                   |
| <span data-ttu-id="99052-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="99052-241">System-Flags</span></span>           | <span data-ttu-id="99052-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="99052-242">0x00000010</span></span>                                   |
| <span data-ttu-id="99052-243">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="99052-243">Classes used in</span></span>        | [<span data-ttu-id="99052-244">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="99052-244">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



 

 





