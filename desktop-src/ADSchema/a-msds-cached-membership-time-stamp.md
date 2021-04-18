---
title: attributo per MS-DS-Cached-Membership-Time-Stamp
description: L'attributo ms-DS-Cached-Membership-Time-Stamp viene usato dalla gestione degli account di sicurezza per l'espansione del gruppo durante la valutazione del token.
ms.assetid: cb096f79-a57b-4001-b197-e75522904734
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo ms-DS-Cached-Membership-Time-Stamp
- msDS-Cached-Membership-Time-Stamp attributo AD schema
topic_type:
- apiref
api_name:
- ms-DS-Cached-Membership-Time-Stamp
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 403e87288d906587a11f2a140a9f447ce8236aca
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "106303278"
---
# <a name="ms-ds-cached-membership-time-stamp-attribute"></a><span data-ttu-id="6db47-105">attributo per MS-DS-Cached-Membership-Time-Stamp</span><span class="sxs-lookup"><span data-stu-id="6db47-105">ms-DS-Cached-Membership-Time-Stamp attribute</span></span>

<span data-ttu-id="6db47-106">L'attributo **ms-DS-Cached-Membership-Time-Stamp** viene usato dalla gestione degli account di sicurezza per l'espansione del gruppo durante la valutazione del token.</span><span class="sxs-lookup"><span data-stu-id="6db47-106">The **ms-DS-Cached-Membership-Time-Stamp** attribute is used by the Security Accounts Manager for group expansion during token evaluation.</span></span>



| <span data-ttu-id="6db47-107">Voce</span><span class="sxs-lookup"><span data-stu-id="6db47-107">Entry</span></span> | <span data-ttu-id="6db47-108">Valore</span><span class="sxs-lookup"><span data-stu-id="6db47-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="6db47-109">CN</span><span class="sxs-lookup"><span data-stu-id="6db47-109">CN</span></span>                | <span data-ttu-id="6db47-110">ms-DS-cache-Membership-timestamp</span><span class="sxs-lookup"><span data-stu-id="6db47-110">ms-DS-Cached-Membership-Time-Stamp</span></span>   |
| <span data-ttu-id="6db47-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="6db47-111">Ldap-Display-Name</span></span> | <span data-ttu-id="6db47-112">msDS-Cached-Membership-timestamp</span><span class="sxs-lookup"><span data-stu-id="6db47-112">msDS-Cached-Membership-Time-Stamp</span></span>    |
| <span data-ttu-id="6db47-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="6db47-113">Size</span></span>              | <span data-ttu-id="6db47-114">8 byte</span><span class="sxs-lookup"><span data-stu-id="6db47-114">8 bytes</span></span>                              |
| <span data-ttu-id="6db47-115">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="6db47-115">Update Privilege</span></span>  | <span data-ttu-id="6db47-116">Questo valore viene impostato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="6db47-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="6db47-117">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="6db47-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="6db47-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="6db47-118">Attribute-Id</span></span>      | <span data-ttu-id="6db47-119">1.2.840.113556.1.4.1442</span><span class="sxs-lookup"><span data-stu-id="6db47-119">1.2.840.113556.1.4.1442</span></span>              |
| <span data-ttu-id="6db47-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="6db47-120">System-Id-Guid</span></span>    | <span data-ttu-id="6db47-121">3566bf1f-beee-4dcb-8abe-ef89fcfec6c1</span><span class="sxs-lookup"><span data-stu-id="6db47-121">3566bf1f-beee-4dcb-8abe-ef89fcfec6c1</span></span> |
| <span data-ttu-id="6db47-122">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6db47-122">Syntax</span></span>            | [<span data-ttu-id="6db47-123">**Interval**</span><span class="sxs-lookup"><span data-stu-id="6db47-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="6db47-124">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="6db47-124">Implementations</span></span>

-   [<span data-ttu-id="6db47-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="6db47-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="6db47-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="6db47-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="6db47-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="6db47-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="6db47-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="6db47-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="6db47-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="6db47-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="6db47-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6db47-130">Windows Server 2003</span></span>



| <span data-ttu-id="6db47-131">Voce</span><span class="sxs-lookup"><span data-stu-id="6db47-131">Entry</span></span> | <span data-ttu-id="6db47-132">Valore</span><span class="sxs-lookup"><span data-stu-id="6db47-132">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="6db47-133">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="6db47-133">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="6db47-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6db47-134">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="6db47-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="6db47-135">System-Only</span></span>            | <span data-ttu-id="6db47-136">Falso</span><span class="sxs-lookup"><span data-stu-id="6db47-136">False</span></span>                             |
| <span data-ttu-id="6db47-137">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="6db47-137">Is-Single-Valued</span></span>       | <span data-ttu-id="6db47-138">Vero</span><span class="sxs-lookup"><span data-stu-id="6db47-138">True</span></span>                              |
| <span data-ttu-id="6db47-139">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="6db47-139">Is Indexed</span></span>             | <span data-ttu-id="6db47-140">Vero</span><span class="sxs-lookup"><span data-stu-id="6db47-140">True</span></span>                              |
| <span data-ttu-id="6db47-141">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="6db47-141">In Global Catalog</span></span>      | <span data-ttu-id="6db47-142">Falso</span><span class="sxs-lookup"><span data-stu-id="6db47-142">False</span></span>                             |
| <span data-ttu-id="6db47-143">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="6db47-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="6db47-144">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="6db47-144">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="6db47-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6db47-145">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="6db47-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6db47-146">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="6db47-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6db47-147">Search-Flags</span></span>           | <span data-ttu-id="6db47-148">0x00000001</span><span class="sxs-lookup"><span data-stu-id="6db47-148">0x00000001</span></span>                        |
| <span data-ttu-id="6db47-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6db47-149">System-Flags</span></span>           | <span data-ttu-id="6db47-150">0x00000011</span><span class="sxs-lookup"><span data-stu-id="6db47-150">0x00000011</span></span>                        |
| <span data-ttu-id="6db47-151">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="6db47-151">Classes used in</span></span>        | [<span data-ttu-id="6db47-152">**Utente**</span><span class="sxs-lookup"><span data-stu-id="6db47-152">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="6db47-153">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="6db47-153">Windows Server 2003 R2</span></span>



| <span data-ttu-id="6db47-154">Voce</span><span class="sxs-lookup"><span data-stu-id="6db47-154">Entry</span></span> | <span data-ttu-id="6db47-155">Valore</span><span class="sxs-lookup"><span data-stu-id="6db47-155">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="6db47-156">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="6db47-156">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="6db47-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6db47-157">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="6db47-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="6db47-158">System-Only</span></span>            | <span data-ttu-id="6db47-159">Falso</span><span class="sxs-lookup"><span data-stu-id="6db47-159">False</span></span>                             |
| <span data-ttu-id="6db47-160">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="6db47-160">Is-Single-Valued</span></span>       | <span data-ttu-id="6db47-161">Vero</span><span class="sxs-lookup"><span data-stu-id="6db47-161">True</span></span>                              |
| <span data-ttu-id="6db47-162">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="6db47-162">Is Indexed</span></span>             | <span data-ttu-id="6db47-163">Vero</span><span class="sxs-lookup"><span data-stu-id="6db47-163">True</span></span>                              |
| <span data-ttu-id="6db47-164">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="6db47-164">In Global Catalog</span></span>      | <span data-ttu-id="6db47-165">Falso</span><span class="sxs-lookup"><span data-stu-id="6db47-165">False</span></span>                             |
| <span data-ttu-id="6db47-166">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="6db47-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="6db47-167">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="6db47-167">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="6db47-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6db47-168">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="6db47-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6db47-169">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="6db47-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6db47-170">Search-Flags</span></span>           | <span data-ttu-id="6db47-171">0x00000001</span><span class="sxs-lookup"><span data-stu-id="6db47-171">0x00000001</span></span>                        |
| <span data-ttu-id="6db47-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6db47-172">System-Flags</span></span>           | <span data-ttu-id="6db47-173">0x00000011</span><span class="sxs-lookup"><span data-stu-id="6db47-173">0x00000011</span></span>                        |
| <span data-ttu-id="6db47-174">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="6db47-174">Classes used in</span></span>        | [<span data-ttu-id="6db47-175">**Utente**</span><span class="sxs-lookup"><span data-stu-id="6db47-175">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="6db47-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6db47-176">Windows Server 2008</span></span>



| <span data-ttu-id="6db47-177">Voce</span><span class="sxs-lookup"><span data-stu-id="6db47-177">Entry</span></span> | <span data-ttu-id="6db47-178">Valore</span><span class="sxs-lookup"><span data-stu-id="6db47-178">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="6db47-179">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="6db47-179">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="6db47-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6db47-180">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="6db47-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="6db47-181">System-Only</span></span>            | <span data-ttu-id="6db47-182">Falso</span><span class="sxs-lookup"><span data-stu-id="6db47-182">False</span></span>                             |
| <span data-ttu-id="6db47-183">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="6db47-183">Is-Single-Valued</span></span>       | <span data-ttu-id="6db47-184">Vero</span><span class="sxs-lookup"><span data-stu-id="6db47-184">True</span></span>                              |
| <span data-ttu-id="6db47-185">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="6db47-185">Is Indexed</span></span>             | <span data-ttu-id="6db47-186">Vero</span><span class="sxs-lookup"><span data-stu-id="6db47-186">True</span></span>                              |
| <span data-ttu-id="6db47-187">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="6db47-187">In Global Catalog</span></span>      | <span data-ttu-id="6db47-188">Falso</span><span class="sxs-lookup"><span data-stu-id="6db47-188">False</span></span>                             |
| <span data-ttu-id="6db47-189">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="6db47-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="6db47-190">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="6db47-190">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="6db47-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6db47-191">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="6db47-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6db47-192">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="6db47-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6db47-193">Search-Flags</span></span>           | <span data-ttu-id="6db47-194">0x00000001</span><span class="sxs-lookup"><span data-stu-id="6db47-194">0x00000001</span></span>                        |
| <span data-ttu-id="6db47-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6db47-195">System-Flags</span></span>           | <span data-ttu-id="6db47-196">0x00000011</span><span class="sxs-lookup"><span data-stu-id="6db47-196">0x00000011</span></span>                        |
| <span data-ttu-id="6db47-197">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="6db47-197">Classes used in</span></span>        | [<span data-ttu-id="6db47-198">**Utente**</span><span class="sxs-lookup"><span data-stu-id="6db47-198">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="6db47-199">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6db47-199">Windows Server 2008 R2</span></span>



| <span data-ttu-id="6db47-200">Voce</span><span class="sxs-lookup"><span data-stu-id="6db47-200">Entry</span></span> | <span data-ttu-id="6db47-201">Valore</span><span class="sxs-lookup"><span data-stu-id="6db47-201">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="6db47-202">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="6db47-202">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="6db47-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6db47-203">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="6db47-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="6db47-204">System-Only</span></span>            | <span data-ttu-id="6db47-205">Falso</span><span class="sxs-lookup"><span data-stu-id="6db47-205">False</span></span>                             |
| <span data-ttu-id="6db47-206">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="6db47-206">Is-Single-Valued</span></span>       | <span data-ttu-id="6db47-207">Vero</span><span class="sxs-lookup"><span data-stu-id="6db47-207">True</span></span>                              |
| <span data-ttu-id="6db47-208">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="6db47-208">Is Indexed</span></span>             | <span data-ttu-id="6db47-209">Vero</span><span class="sxs-lookup"><span data-stu-id="6db47-209">True</span></span>                              |
| <span data-ttu-id="6db47-210">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="6db47-210">In Global Catalog</span></span>      | <span data-ttu-id="6db47-211">Falso</span><span class="sxs-lookup"><span data-stu-id="6db47-211">False</span></span>                             |
| <span data-ttu-id="6db47-212">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="6db47-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="6db47-213">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="6db47-213">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="6db47-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6db47-214">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="6db47-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6db47-215">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="6db47-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6db47-216">Search-Flags</span></span>           | <span data-ttu-id="6db47-217">0x00000001</span><span class="sxs-lookup"><span data-stu-id="6db47-217">0x00000001</span></span>                        |
| <span data-ttu-id="6db47-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6db47-218">System-Flags</span></span>           | <span data-ttu-id="6db47-219">0x00000011</span><span class="sxs-lookup"><span data-stu-id="6db47-219">0x00000011</span></span>                        |
| <span data-ttu-id="6db47-220">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="6db47-220">Classes used in</span></span>        | [<span data-ttu-id="6db47-221">**Utente**</span><span class="sxs-lookup"><span data-stu-id="6db47-221">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="6db47-222">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6db47-222">Windows Server 2012</span></span>



| <span data-ttu-id="6db47-223">Voce</span><span class="sxs-lookup"><span data-stu-id="6db47-223">Entry</span></span> | <span data-ttu-id="6db47-224">Valore</span><span class="sxs-lookup"><span data-stu-id="6db47-224">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="6db47-225">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="6db47-225">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="6db47-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6db47-226">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="6db47-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="6db47-227">System-Only</span></span>            | <span data-ttu-id="6db47-228">Falso</span><span class="sxs-lookup"><span data-stu-id="6db47-228">False</span></span>                             |
| <span data-ttu-id="6db47-229">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="6db47-229">Is-Single-Valued</span></span>       | <span data-ttu-id="6db47-230">Vero</span><span class="sxs-lookup"><span data-stu-id="6db47-230">True</span></span>                              |
| <span data-ttu-id="6db47-231">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="6db47-231">Is Indexed</span></span>             | <span data-ttu-id="6db47-232">Vero</span><span class="sxs-lookup"><span data-stu-id="6db47-232">True</span></span>                              |
| <span data-ttu-id="6db47-233">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="6db47-233">In Global Catalog</span></span>      | <span data-ttu-id="6db47-234">Falso</span><span class="sxs-lookup"><span data-stu-id="6db47-234">False</span></span>                             |
| <span data-ttu-id="6db47-235">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="6db47-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="6db47-236">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="6db47-236">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="6db47-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6db47-237">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="6db47-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6db47-238">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="6db47-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6db47-239">Search-Flags</span></span>           | <span data-ttu-id="6db47-240">0x00000001</span><span class="sxs-lookup"><span data-stu-id="6db47-240">0x00000001</span></span>                        |
| <span data-ttu-id="6db47-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6db47-241">System-Flags</span></span>           | <span data-ttu-id="6db47-242">0x00000011</span><span class="sxs-lookup"><span data-stu-id="6db47-242">0x00000011</span></span>                        |
| <span data-ttu-id="6db47-243">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="6db47-243">Classes used in</span></span>        | [<span data-ttu-id="6db47-244">**Utente**</span><span class="sxs-lookup"><span data-stu-id="6db47-244">**User**</span></span>](c-user.md)<br/> |



 

 





