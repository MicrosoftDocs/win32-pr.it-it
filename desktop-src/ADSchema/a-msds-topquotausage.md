---
title: attributo ms-DS-Top-quota-Usage
description: Elenco di utenti con quota superiore attualmente presenti nel database di directory, ordinati in base alla riduzione dell'utilizzo della quota.
ms.assetid: c52db8c8-233c-495f-b3fe-edbe1d723677
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo ms-DS-Top-quota-Usage
- attributo msDS-TopQuotaUsage-schema AD
topic_type:
- apiref
api_name:
- ms-DS-Top-Quota-Usage
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4db787c0360eff64c726ec680c9fd2a18da1e8d1
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "106303489"
---
# <a name="ms-ds-top-quota-usage-attribute"></a><span data-ttu-id="4c28c-105">attributo ms-DS-Top-quota-Usage</span><span class="sxs-lookup"><span data-stu-id="4c28c-105">ms-DS-Top-Quota-Usage attribute</span></span>

<span data-ttu-id="4c28c-106">Elenco di utenti con quota superiore attualmente presenti nel database di directory, ordinati in base alla riduzione dell'utilizzo della quota.</span><span class="sxs-lookup"><span data-stu-id="4c28c-106">The list of top quota users currently in the directory database, ordered by decreasing quota usage.</span></span>



| <span data-ttu-id="4c28c-107">Voce</span><span class="sxs-lookup"><span data-stu-id="4c28c-107">Entry</span></span> | <span data-ttu-id="4c28c-108">Valore</span><span class="sxs-lookup"><span data-stu-id="4c28c-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="4c28c-109">CN</span><span class="sxs-lookup"><span data-stu-id="4c28c-109">CN</span></span>                | <span data-ttu-id="4c28c-110">ms-DS-Top-quota-utilizzo</span><span class="sxs-lookup"><span data-stu-id="4c28c-110">ms-DS-Top-Quota-Usage</span></span>                       |
| <span data-ttu-id="4c28c-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="4c28c-111">Ldap-Display-Name</span></span> | <span data-ttu-id="4c28c-112">msDS-TopQuotaUsage</span><span class="sxs-lookup"><span data-stu-id="4c28c-112">msDS-TopQuotaUsage</span></span>                          |
| <span data-ttu-id="4c28c-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="4c28c-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="4c28c-114">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="4c28c-114">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="4c28c-115">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="4c28c-115">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="4c28c-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="4c28c-116">Attribute-Id</span></span>      | <span data-ttu-id="4c28c-117">1.2.840.113556.1.4.1850</span><span class="sxs-lookup"><span data-stu-id="4c28c-117">1.2.840.113556.1.4.1850</span></span>                     |
| <span data-ttu-id="4c28c-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="4c28c-118">System-Id-Guid</span></span>    | <span data-ttu-id="4c28c-119">7b7cce4f-f1f5-4bb6-b7eb-23504af19e75</span><span class="sxs-lookup"><span data-stu-id="4c28c-119">7b7cce4f-f1f5-4bb6-b7eb-23504af19e75</span></span>        |
| <span data-ttu-id="4c28c-120">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4c28c-120">Syntax</span></span>            | [<span data-ttu-id="4c28c-121">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="4c28c-121">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="4c28c-122">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="4c28c-122">Implementations</span></span>

-   [<span data-ttu-id="4c28c-123">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="4c28c-123">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="4c28c-124">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="4c28c-124">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="4c28c-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="4c28c-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="4c28c-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="4c28c-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="4c28c-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="4c28c-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="4c28c-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="4c28c-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="4c28c-129">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4c28c-129">Windows Server 2003</span></span>



| <span data-ttu-id="4c28c-130">Voce</span><span class="sxs-lookup"><span data-stu-id="4c28c-130">Entry</span></span> | <span data-ttu-id="4c28c-131">Valore</span><span class="sxs-lookup"><span data-stu-id="4c28c-131">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="4c28c-132">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="4c28c-132">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="4c28c-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4c28c-133">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="4c28c-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="4c28c-134">System-Only</span></span>            | <span data-ttu-id="4c28c-135">Falso</span><span class="sxs-lookup"><span data-stu-id="4c28c-135">False</span></span>                                                             |
| <span data-ttu-id="4c28c-136">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="4c28c-136">Is-Single-Valued</span></span>       | <span data-ttu-id="4c28c-137">Falso</span><span class="sxs-lookup"><span data-stu-id="4c28c-137">False</span></span>                                                             |
| <span data-ttu-id="4c28c-138">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="4c28c-138">Is Indexed</span></span>             | <span data-ttu-id="4c28c-139">Falso</span><span class="sxs-lookup"><span data-stu-id="4c28c-139">False</span></span>                                                             |
| <span data-ttu-id="4c28c-140">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="4c28c-140">In Global Catalog</span></span>      | <span data-ttu-id="4c28c-141">Falso</span><span class="sxs-lookup"><span data-stu-id="4c28c-141">False</span></span>                                                             |
| <span data-ttu-id="4c28c-142">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="4c28c-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="4c28c-143">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="4c28c-143">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="4c28c-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4c28c-144">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="4c28c-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4c28c-145">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="4c28c-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4c28c-146">Search-Flags</span></span>           | <span data-ttu-id="4c28c-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4c28c-147">0x00000000</span></span>                                                        |
| <span data-ttu-id="4c28c-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4c28c-148">System-Flags</span></span>           | <span data-ttu-id="4c28c-149">0x00000014</span><span class="sxs-lookup"><span data-stu-id="4c28c-149">0x00000014</span></span>                                                        |
| <span data-ttu-id="4c28c-150">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="4c28c-150">Classes used in</span></span>        | [<span data-ttu-id="4c28c-151">**ms-DS-quota-contenitore**</span><span class="sxs-lookup"><span data-stu-id="4c28c-151">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="adam"></a><span data-ttu-id="4c28c-152">ADAM</span><span class="sxs-lookup"><span data-stu-id="4c28c-152">ADAM</span></span>



| <span data-ttu-id="4c28c-153">Voce</span><span class="sxs-lookup"><span data-stu-id="4c28c-153">Entry</span></span> | <span data-ttu-id="4c28c-154">Valore</span><span class="sxs-lookup"><span data-stu-id="4c28c-154">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="4c28c-155">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="4c28c-155">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="4c28c-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4c28c-156">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="4c28c-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="4c28c-157">System-Only</span></span>            | <span data-ttu-id="4c28c-158">Falso</span><span class="sxs-lookup"><span data-stu-id="4c28c-158">False</span></span>                                                             |
| <span data-ttu-id="4c28c-159">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="4c28c-159">Is-Single-Valued</span></span>       | <span data-ttu-id="4c28c-160">Falso</span><span class="sxs-lookup"><span data-stu-id="4c28c-160">False</span></span>                                                             |
| <span data-ttu-id="4c28c-161">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="4c28c-161">Is Indexed</span></span>             | <span data-ttu-id="4c28c-162">Falso</span><span class="sxs-lookup"><span data-stu-id="4c28c-162">False</span></span>                                                             |
| <span data-ttu-id="4c28c-163">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="4c28c-163">In Global Catalog</span></span>      | <span data-ttu-id="4c28c-164">Falso</span><span class="sxs-lookup"><span data-stu-id="4c28c-164">False</span></span>                                                             |
| <span data-ttu-id="4c28c-165">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="4c28c-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="4c28c-166">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="4c28c-166">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="4c28c-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4c28c-167">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="4c28c-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4c28c-168">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="4c28c-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4c28c-169">Search-Flags</span></span>           | <span data-ttu-id="4c28c-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4c28c-170">0x00000000</span></span>                                                        |
| <span data-ttu-id="4c28c-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4c28c-171">System-Flags</span></span>           | <span data-ttu-id="4c28c-172">0x00000014</span><span class="sxs-lookup"><span data-stu-id="4c28c-172">0x00000014</span></span>                                                        |
| <span data-ttu-id="4c28c-173">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="4c28c-173">Classes used in</span></span>        | [<span data-ttu-id="4c28c-174">**ms-DS-quota-contenitore**</span><span class="sxs-lookup"><span data-stu-id="4c28c-174">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="4c28c-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="4c28c-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="4c28c-176">Voce</span><span class="sxs-lookup"><span data-stu-id="4c28c-176">Entry</span></span> | <span data-ttu-id="4c28c-177">Valore</span><span class="sxs-lookup"><span data-stu-id="4c28c-177">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="4c28c-178">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="4c28c-178">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="4c28c-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4c28c-179">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="4c28c-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="4c28c-180">System-Only</span></span>            | <span data-ttu-id="4c28c-181">Falso</span><span class="sxs-lookup"><span data-stu-id="4c28c-181">False</span></span>                                                             |
| <span data-ttu-id="4c28c-182">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="4c28c-182">Is-Single-Valued</span></span>       | <span data-ttu-id="4c28c-183">Falso</span><span class="sxs-lookup"><span data-stu-id="4c28c-183">False</span></span>                                                             |
| <span data-ttu-id="4c28c-184">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="4c28c-184">Is Indexed</span></span>             | <span data-ttu-id="4c28c-185">Falso</span><span class="sxs-lookup"><span data-stu-id="4c28c-185">False</span></span>                                                             |
| <span data-ttu-id="4c28c-186">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="4c28c-186">In Global Catalog</span></span>      | <span data-ttu-id="4c28c-187">Falso</span><span class="sxs-lookup"><span data-stu-id="4c28c-187">False</span></span>                                                             |
| <span data-ttu-id="4c28c-188">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="4c28c-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="4c28c-189">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="4c28c-189">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="4c28c-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4c28c-190">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="4c28c-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4c28c-191">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="4c28c-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4c28c-192">Search-Flags</span></span>           | <span data-ttu-id="4c28c-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4c28c-193">0x00000000</span></span>                                                        |
| <span data-ttu-id="4c28c-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4c28c-194">System-Flags</span></span>           | <span data-ttu-id="4c28c-195">0x00000014</span><span class="sxs-lookup"><span data-stu-id="4c28c-195">0x00000014</span></span>                                                        |
| <span data-ttu-id="4c28c-196">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="4c28c-196">Classes used in</span></span>        | [<span data-ttu-id="4c28c-197">**ms-DS-quota-contenitore**</span><span class="sxs-lookup"><span data-stu-id="4c28c-197">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="4c28c-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4c28c-198">Windows Server 2008</span></span>



| <span data-ttu-id="4c28c-199">Voce</span><span class="sxs-lookup"><span data-stu-id="4c28c-199">Entry</span></span> | <span data-ttu-id="4c28c-200">Valore</span><span class="sxs-lookup"><span data-stu-id="4c28c-200">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="4c28c-201">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="4c28c-201">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="4c28c-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4c28c-202">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="4c28c-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="4c28c-203">System-Only</span></span>            | <span data-ttu-id="4c28c-204">Falso</span><span class="sxs-lookup"><span data-stu-id="4c28c-204">False</span></span>                                                             |
| <span data-ttu-id="4c28c-205">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="4c28c-205">Is-Single-Valued</span></span>       | <span data-ttu-id="4c28c-206">Falso</span><span class="sxs-lookup"><span data-stu-id="4c28c-206">False</span></span>                                                             |
| <span data-ttu-id="4c28c-207">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="4c28c-207">Is Indexed</span></span>             | <span data-ttu-id="4c28c-208">Falso</span><span class="sxs-lookup"><span data-stu-id="4c28c-208">False</span></span>                                                             |
| <span data-ttu-id="4c28c-209">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="4c28c-209">In Global Catalog</span></span>      | <span data-ttu-id="4c28c-210">Falso</span><span class="sxs-lookup"><span data-stu-id="4c28c-210">False</span></span>                                                             |
| <span data-ttu-id="4c28c-211">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="4c28c-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="4c28c-212">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="4c28c-212">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="4c28c-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4c28c-213">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="4c28c-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4c28c-214">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="4c28c-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4c28c-215">Search-Flags</span></span>           | <span data-ttu-id="4c28c-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4c28c-216">0x00000000</span></span>                                                        |
| <span data-ttu-id="4c28c-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4c28c-217">System-Flags</span></span>           | <span data-ttu-id="4c28c-218">0x00000014</span><span class="sxs-lookup"><span data-stu-id="4c28c-218">0x00000014</span></span>                                                        |
| <span data-ttu-id="4c28c-219">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="4c28c-219">Classes used in</span></span>        | [<span data-ttu-id="4c28c-220">**ms-DS-quota-contenitore**</span><span class="sxs-lookup"><span data-stu-id="4c28c-220">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="4c28c-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4c28c-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="4c28c-222">Voce</span><span class="sxs-lookup"><span data-stu-id="4c28c-222">Entry</span></span> | <span data-ttu-id="4c28c-223">Valore</span><span class="sxs-lookup"><span data-stu-id="4c28c-223">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="4c28c-224">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="4c28c-224">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="4c28c-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4c28c-225">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="4c28c-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="4c28c-226">System-Only</span></span>            | <span data-ttu-id="4c28c-227">Falso</span><span class="sxs-lookup"><span data-stu-id="4c28c-227">False</span></span>                                                             |
| <span data-ttu-id="4c28c-228">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="4c28c-228">Is-Single-Valued</span></span>       | <span data-ttu-id="4c28c-229">Falso</span><span class="sxs-lookup"><span data-stu-id="4c28c-229">False</span></span>                                                             |
| <span data-ttu-id="4c28c-230">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="4c28c-230">Is Indexed</span></span>             | <span data-ttu-id="4c28c-231">Falso</span><span class="sxs-lookup"><span data-stu-id="4c28c-231">False</span></span>                                                             |
| <span data-ttu-id="4c28c-232">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="4c28c-232">In Global Catalog</span></span>      | <span data-ttu-id="4c28c-233">Falso</span><span class="sxs-lookup"><span data-stu-id="4c28c-233">False</span></span>                                                             |
| <span data-ttu-id="4c28c-234">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="4c28c-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="4c28c-235">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="4c28c-235">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="4c28c-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4c28c-236">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="4c28c-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4c28c-237">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="4c28c-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4c28c-238">Search-Flags</span></span>           | <span data-ttu-id="4c28c-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4c28c-239">0x00000000</span></span>                                                        |
| <span data-ttu-id="4c28c-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4c28c-240">System-Flags</span></span>           | <span data-ttu-id="4c28c-241">0x00000014</span><span class="sxs-lookup"><span data-stu-id="4c28c-241">0x00000014</span></span>                                                        |
| <span data-ttu-id="4c28c-242">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="4c28c-242">Classes used in</span></span>        | [<span data-ttu-id="4c28c-243">**ms-DS-quota-contenitore**</span><span class="sxs-lookup"><span data-stu-id="4c28c-243">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="4c28c-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4c28c-244">Windows Server 2012</span></span>



| <span data-ttu-id="4c28c-245">Voce</span><span class="sxs-lookup"><span data-stu-id="4c28c-245">Entry</span></span> | <span data-ttu-id="4c28c-246">Valore</span><span class="sxs-lookup"><span data-stu-id="4c28c-246">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="4c28c-247">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="4c28c-247">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="4c28c-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4c28c-248">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="4c28c-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="4c28c-249">System-Only</span></span>            | <span data-ttu-id="4c28c-250">Falso</span><span class="sxs-lookup"><span data-stu-id="4c28c-250">False</span></span>                                                             |
| <span data-ttu-id="4c28c-251">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="4c28c-251">Is-Single-Valued</span></span>       | <span data-ttu-id="4c28c-252">Falso</span><span class="sxs-lookup"><span data-stu-id="4c28c-252">False</span></span>                                                             |
| <span data-ttu-id="4c28c-253">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="4c28c-253">Is Indexed</span></span>             | <span data-ttu-id="4c28c-254">Falso</span><span class="sxs-lookup"><span data-stu-id="4c28c-254">False</span></span>                                                             |
| <span data-ttu-id="4c28c-255">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="4c28c-255">In Global Catalog</span></span>      | <span data-ttu-id="4c28c-256">Falso</span><span class="sxs-lookup"><span data-stu-id="4c28c-256">False</span></span>                                                             |
| <span data-ttu-id="4c28c-257">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="4c28c-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="4c28c-258">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="4c28c-258">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="4c28c-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4c28c-259">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="4c28c-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4c28c-260">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="4c28c-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4c28c-261">Search-Flags</span></span>           | <span data-ttu-id="4c28c-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4c28c-262">0x00000000</span></span>                                                        |
| <span data-ttu-id="4c28c-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4c28c-263">System-Flags</span></span>           | <span data-ttu-id="4c28c-264">0x00000014</span><span class="sxs-lookup"><span data-stu-id="4c28c-264">0x00000014</span></span>                                                        |
| <span data-ttu-id="4c28c-265">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="4c28c-265">Classes used in</span></span>        | [<span data-ttu-id="4c28c-266">**ms-DS-quota-contenitore**</span><span class="sxs-lookup"><span data-stu-id="4c28c-266">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



 

 





