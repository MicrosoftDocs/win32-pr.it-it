---
title: attributo ms-DS-Site-Affinity
description: L'attributo ms-DS-Site-Affinity viene utilizzato da Gestione account di sicurezza per l'espansione del gruppo durante la valutazione del token.
ms.assetid: c05df70a-adbb-48e0-bdcd-c1d83a2e43bd
ms.tgt_platform: multiple
keywords:
- Schema AD per l'attributo ms-DS-Site-Affinity
- attributo msDS-site-Affinity AD schema
topic_type:
- apiref
api_name:
- ms-DS-Site-Affinity
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5dd3ed17b07c73d9e7a6a2d93d93463e1dea40fc
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103875681"
---
# <a name="ms-ds-site-affinity-attribute"></a><span data-ttu-id="9d98d-105">attributo ms-DS-Site-Affinity</span><span class="sxs-lookup"><span data-stu-id="9d98d-105">ms-DS-Site-Affinity attribute</span></span>

<span data-ttu-id="9d98d-106">L'attributo **ms-DS-Site-Affinity** viene utilizzato da Gestione account di sicurezza per l'espansione del gruppo durante la valutazione del token.</span><span class="sxs-lookup"><span data-stu-id="9d98d-106">The **ms-DS-Site-Affinity** attribute is used by the Security Accounts Manager for group expansion during token evaluation.</span></span>



| <span data-ttu-id="9d98d-107">Voce</span><span class="sxs-lookup"><span data-stu-id="9d98d-107">Entry</span></span> | <span data-ttu-id="9d98d-108">Valore</span><span class="sxs-lookup"><span data-stu-id="9d98d-108">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9d98d-109">CN</span><span class="sxs-lookup"><span data-stu-id="9d98d-109">CN</span></span>                | <span data-ttu-id="9d98d-110">ms-DS-Site-affinità</span><span class="sxs-lookup"><span data-stu-id="9d98d-110">ms-DS-Site-Affinity</span></span>                                                                     |
| <span data-ttu-id="9d98d-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="9d98d-111">Ldap-Display-Name</span></span> | <span data-ttu-id="9d98d-112">msDS-site-affinità</span><span class="sxs-lookup"><span data-stu-id="9d98d-112">msDS-Site-Affinity</span></span>                                                                      |
| <span data-ttu-id="9d98d-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="9d98d-113">Size</span></span>              | <span data-ttu-id="9d98d-114">BLOB binario a più valori, dove ogni valore è sizeof (GUID) + sizeof ( \_ Integer grande).</span><span class="sxs-lookup"><span data-stu-id="9d98d-114">Multiple-valued binary BLOB, where each value is sizeof(GUID) + sizeof(LARGE\_INTEGER).</span></span> |
| <span data-ttu-id="9d98d-115">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="9d98d-115">Update Privilege</span></span>  | \-                                                                                      |
| <span data-ttu-id="9d98d-116">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="9d98d-116">Update Frequency</span></span>  | <span data-ttu-id="9d98d-117">Per impostazione predefinita, una volta ogni tre mesi.</span><span class="sxs-lookup"><span data-stu-id="9d98d-117">By default once every three months.</span></span>                                                     |
| <span data-ttu-id="9d98d-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="9d98d-118">Attribute-Id</span></span>      | <span data-ttu-id="9d98d-119">1.2.840.113556.1.4.1443</span><span class="sxs-lookup"><span data-stu-id="9d98d-119">1.2.840.113556.1.4.1443</span></span>                                                                 |
| <span data-ttu-id="9d98d-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="9d98d-120">System-Id-Guid</span></span>    | <span data-ttu-id="9d98d-121">c17c5602-bcb7-46f0-9656-6370ca884b72</span><span class="sxs-lookup"><span data-stu-id="9d98d-121">c17c5602-bcb7-46f0-9656-6370ca884b72</span></span>                                                    |
| <span data-ttu-id="9d98d-122">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9d98d-122">Syntax</span></span>            | [<span data-ttu-id="9d98d-123">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="9d98d-123">**Object(Replica-Link)**</span></span>](s-object-replica-link.md)                                   |



## <a name="implementations"></a><span data-ttu-id="9d98d-124">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="9d98d-124">Implementations</span></span>

-   [<span data-ttu-id="9d98d-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="9d98d-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="9d98d-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="9d98d-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="9d98d-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="9d98d-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="9d98d-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="9d98d-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="9d98d-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="9d98d-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="9d98d-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9d98d-130">Windows Server 2003</span></span>



| <span data-ttu-id="9d98d-131">Voce</span><span class="sxs-lookup"><span data-stu-id="9d98d-131">Entry</span></span> | <span data-ttu-id="9d98d-132">Valore</span><span class="sxs-lookup"><span data-stu-id="9d98d-132">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="9d98d-133">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="9d98d-133">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="9d98d-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9d98d-134">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="9d98d-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="9d98d-135">System-Only</span></span>            | <span data-ttu-id="9d98d-136">Falso</span><span class="sxs-lookup"><span data-stu-id="9d98d-136">False</span></span>                             |
| <span data-ttu-id="9d98d-137">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="9d98d-137">Is-Single-Valued</span></span>       | <span data-ttu-id="9d98d-138">Falso</span><span class="sxs-lookup"><span data-stu-id="9d98d-138">False</span></span>                             |
| <span data-ttu-id="9d98d-139">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="9d98d-139">Is Indexed</span></span>             | <span data-ttu-id="9d98d-140">Vero</span><span class="sxs-lookup"><span data-stu-id="9d98d-140">True</span></span>                              |
| <span data-ttu-id="9d98d-141">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="9d98d-141">In Global Catalog</span></span>      | <span data-ttu-id="9d98d-142">Falso</span><span class="sxs-lookup"><span data-stu-id="9d98d-142">False</span></span>                             |
| <span data-ttu-id="9d98d-143">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="9d98d-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="9d98d-144">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="9d98d-144">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="9d98d-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9d98d-145">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="9d98d-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9d98d-146">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="9d98d-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9d98d-147">Search-Flags</span></span>           | <span data-ttu-id="9d98d-148">0x00000001</span><span class="sxs-lookup"><span data-stu-id="9d98d-148">0x00000001</span></span>                        |
| <span data-ttu-id="9d98d-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9d98d-149">System-Flags</span></span>           | <span data-ttu-id="9d98d-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9d98d-150">0x00000010</span></span>                        |
| <span data-ttu-id="9d98d-151">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="9d98d-151">Classes used in</span></span>        | [<span data-ttu-id="9d98d-152">**Utente**</span><span class="sxs-lookup"><span data-stu-id="9d98d-152">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="9d98d-153">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="9d98d-153">Windows Server 2003 R2</span></span>



| <span data-ttu-id="9d98d-154">Voce</span><span class="sxs-lookup"><span data-stu-id="9d98d-154">Entry</span></span> | <span data-ttu-id="9d98d-155">Valore</span><span class="sxs-lookup"><span data-stu-id="9d98d-155">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="9d98d-156">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="9d98d-156">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="9d98d-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9d98d-157">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="9d98d-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="9d98d-158">System-Only</span></span>            | <span data-ttu-id="9d98d-159">Falso</span><span class="sxs-lookup"><span data-stu-id="9d98d-159">False</span></span>                             |
| <span data-ttu-id="9d98d-160">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="9d98d-160">Is-Single-Valued</span></span>       | <span data-ttu-id="9d98d-161">Falso</span><span class="sxs-lookup"><span data-stu-id="9d98d-161">False</span></span>                             |
| <span data-ttu-id="9d98d-162">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="9d98d-162">Is Indexed</span></span>             | <span data-ttu-id="9d98d-163">Vero</span><span class="sxs-lookup"><span data-stu-id="9d98d-163">True</span></span>                              |
| <span data-ttu-id="9d98d-164">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="9d98d-164">In Global Catalog</span></span>      | <span data-ttu-id="9d98d-165">Falso</span><span class="sxs-lookup"><span data-stu-id="9d98d-165">False</span></span>                             |
| <span data-ttu-id="9d98d-166">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="9d98d-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="9d98d-167">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="9d98d-167">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="9d98d-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9d98d-168">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="9d98d-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9d98d-169">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="9d98d-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9d98d-170">Search-Flags</span></span>           | <span data-ttu-id="9d98d-171">0x00000001</span><span class="sxs-lookup"><span data-stu-id="9d98d-171">0x00000001</span></span>                        |
| <span data-ttu-id="9d98d-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9d98d-172">System-Flags</span></span>           | <span data-ttu-id="9d98d-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9d98d-173">0x00000010</span></span>                        |
| <span data-ttu-id="9d98d-174">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="9d98d-174">Classes used in</span></span>        | [<span data-ttu-id="9d98d-175">**Utente**</span><span class="sxs-lookup"><span data-stu-id="9d98d-175">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="9d98d-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9d98d-176">Windows Server 2008</span></span>



| <span data-ttu-id="9d98d-177">Voce</span><span class="sxs-lookup"><span data-stu-id="9d98d-177">Entry</span></span> | <span data-ttu-id="9d98d-178">Valore</span><span class="sxs-lookup"><span data-stu-id="9d98d-178">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="9d98d-179">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="9d98d-179">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="9d98d-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9d98d-180">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="9d98d-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="9d98d-181">System-Only</span></span>            | <span data-ttu-id="9d98d-182">Falso</span><span class="sxs-lookup"><span data-stu-id="9d98d-182">False</span></span>                             |
| <span data-ttu-id="9d98d-183">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="9d98d-183">Is-Single-Valued</span></span>       | <span data-ttu-id="9d98d-184">Falso</span><span class="sxs-lookup"><span data-stu-id="9d98d-184">False</span></span>                             |
| <span data-ttu-id="9d98d-185">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="9d98d-185">Is Indexed</span></span>             | <span data-ttu-id="9d98d-186">Vero</span><span class="sxs-lookup"><span data-stu-id="9d98d-186">True</span></span>                              |
| <span data-ttu-id="9d98d-187">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="9d98d-187">In Global Catalog</span></span>      | <span data-ttu-id="9d98d-188">Falso</span><span class="sxs-lookup"><span data-stu-id="9d98d-188">False</span></span>                             |
| <span data-ttu-id="9d98d-189">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="9d98d-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="9d98d-190">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="9d98d-190">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="9d98d-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9d98d-191">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="9d98d-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9d98d-192">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="9d98d-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9d98d-193">Search-Flags</span></span>           | <span data-ttu-id="9d98d-194">0x00000001</span><span class="sxs-lookup"><span data-stu-id="9d98d-194">0x00000001</span></span>                        |
| <span data-ttu-id="9d98d-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9d98d-195">System-Flags</span></span>           | <span data-ttu-id="9d98d-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9d98d-196">0x00000010</span></span>                        |
| <span data-ttu-id="9d98d-197">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="9d98d-197">Classes used in</span></span>        | [<span data-ttu-id="9d98d-198">**Utente**</span><span class="sxs-lookup"><span data-stu-id="9d98d-198">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="9d98d-199">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9d98d-199">Windows Server 2008 R2</span></span>



| <span data-ttu-id="9d98d-200">Voce</span><span class="sxs-lookup"><span data-stu-id="9d98d-200">Entry</span></span> | <span data-ttu-id="9d98d-201">Valore</span><span class="sxs-lookup"><span data-stu-id="9d98d-201">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="9d98d-202">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="9d98d-202">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="9d98d-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9d98d-203">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="9d98d-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="9d98d-204">System-Only</span></span>            | <span data-ttu-id="9d98d-205">Falso</span><span class="sxs-lookup"><span data-stu-id="9d98d-205">False</span></span>                             |
| <span data-ttu-id="9d98d-206">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="9d98d-206">Is-Single-Valued</span></span>       | <span data-ttu-id="9d98d-207">Falso</span><span class="sxs-lookup"><span data-stu-id="9d98d-207">False</span></span>                             |
| <span data-ttu-id="9d98d-208">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="9d98d-208">Is Indexed</span></span>             | <span data-ttu-id="9d98d-209">Vero</span><span class="sxs-lookup"><span data-stu-id="9d98d-209">True</span></span>                              |
| <span data-ttu-id="9d98d-210">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="9d98d-210">In Global Catalog</span></span>      | <span data-ttu-id="9d98d-211">Falso</span><span class="sxs-lookup"><span data-stu-id="9d98d-211">False</span></span>                             |
| <span data-ttu-id="9d98d-212">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="9d98d-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="9d98d-213">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="9d98d-213">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="9d98d-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9d98d-214">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="9d98d-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9d98d-215">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="9d98d-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9d98d-216">Search-Flags</span></span>           | <span data-ttu-id="9d98d-217">0x00000001</span><span class="sxs-lookup"><span data-stu-id="9d98d-217">0x00000001</span></span>                        |
| <span data-ttu-id="9d98d-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9d98d-218">System-Flags</span></span>           | <span data-ttu-id="9d98d-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9d98d-219">0x00000010</span></span>                        |
| <span data-ttu-id="9d98d-220">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="9d98d-220">Classes used in</span></span>        | [<span data-ttu-id="9d98d-221">**Utente**</span><span class="sxs-lookup"><span data-stu-id="9d98d-221">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="9d98d-222">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9d98d-222">Windows Server 2012</span></span>



| <span data-ttu-id="9d98d-223">Voce</span><span class="sxs-lookup"><span data-stu-id="9d98d-223">Entry</span></span> | <span data-ttu-id="9d98d-224">Valore</span><span class="sxs-lookup"><span data-stu-id="9d98d-224">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="9d98d-225">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="9d98d-225">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="9d98d-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9d98d-226">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="9d98d-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="9d98d-227">System-Only</span></span>            | <span data-ttu-id="9d98d-228">Falso</span><span class="sxs-lookup"><span data-stu-id="9d98d-228">False</span></span>                             |
| <span data-ttu-id="9d98d-229">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="9d98d-229">Is-Single-Valued</span></span>       | <span data-ttu-id="9d98d-230">Falso</span><span class="sxs-lookup"><span data-stu-id="9d98d-230">False</span></span>                             |
| <span data-ttu-id="9d98d-231">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="9d98d-231">Is Indexed</span></span>             | <span data-ttu-id="9d98d-232">Vero</span><span class="sxs-lookup"><span data-stu-id="9d98d-232">True</span></span>                              |
| <span data-ttu-id="9d98d-233">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="9d98d-233">In Global Catalog</span></span>      | <span data-ttu-id="9d98d-234">Falso</span><span class="sxs-lookup"><span data-stu-id="9d98d-234">False</span></span>                             |
| <span data-ttu-id="9d98d-235">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="9d98d-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="9d98d-236">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="9d98d-236">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="9d98d-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9d98d-237">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="9d98d-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9d98d-238">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="9d98d-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9d98d-239">Search-Flags</span></span>           | <span data-ttu-id="9d98d-240">0x00000001</span><span class="sxs-lookup"><span data-stu-id="9d98d-240">0x00000001</span></span>                        |
| <span data-ttu-id="9d98d-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9d98d-241">System-Flags</span></span>           | <span data-ttu-id="9d98d-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9d98d-242">0x00000010</span></span>                        |
| <span data-ttu-id="9d98d-243">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="9d98d-243">Classes used in</span></span>        | [<span data-ttu-id="9d98d-244">**Utente**</span><span class="sxs-lookup"><span data-stu-id="9d98d-244">**User**</span></span>](c-user.md)<br/> |



 

 





