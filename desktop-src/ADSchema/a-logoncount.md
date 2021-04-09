---
title: Attributo Logon-Count
description: Numero di volte in cui l'account è stato connesso correttamente. Il valore 0 indica che il valore è sconosciuto.
ms.assetid: 8b12bea7-dfc3-46e3-a4a2-92b5f1239b98
ms.tgt_platform: multiple
keywords:
- Schema AD Logon-Count attribute
- Schema AD dell'attributo logonCount
topic_type:
- apiref
api_name:
- Logon-Count
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6ba7865cb3b90f42ede71b169f98f8ce45e722d
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103875454"
---
# <a name="logon-count-attribute"></a><span data-ttu-id="187cb-106">Attributo Logon-Count</span><span class="sxs-lookup"><span data-stu-id="187cb-106">Logon-Count attribute</span></span>

<span data-ttu-id="187cb-107">Numero di volte in cui l'account è stato connesso correttamente.</span><span class="sxs-lookup"><span data-stu-id="187cb-107">The number of times the account has successfully logged on.</span></span> <span data-ttu-id="187cb-108">Il valore 0 indica che il valore è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="187cb-108">A value of 0 indicates that the value is unknown.</span></span>



| <span data-ttu-id="187cb-109">Voce</span><span class="sxs-lookup"><span data-stu-id="187cb-109">Entry</span></span> | <span data-ttu-id="187cb-110">Valore</span><span class="sxs-lookup"><span data-stu-id="187cb-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="187cb-111">CN</span><span class="sxs-lookup"><span data-stu-id="187cb-111">CN</span></span>                | <span data-ttu-id="187cb-112">Logon-Count</span><span class="sxs-lookup"><span data-stu-id="187cb-112">Logon-Count</span></span>                          |
| <span data-ttu-id="187cb-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="187cb-113">Ldap-Display-Name</span></span> | <span data-ttu-id="187cb-114">logonCount</span><span class="sxs-lookup"><span data-stu-id="187cb-114">logonCount</span></span>                           |
| <span data-ttu-id="187cb-115">Dimensione</span><span class="sxs-lookup"><span data-stu-id="187cb-115">Size</span></span>              | <span data-ttu-id="187cb-116">4 byte</span><span class="sxs-lookup"><span data-stu-id="187cb-116">4 bytes</span></span>                              |
| <span data-ttu-id="187cb-117">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="187cb-117">Update Privilege</span></span>  | <span data-ttu-id="187cb-118">Amministratore di dominio</span><span class="sxs-lookup"><span data-stu-id="187cb-118">Domain administrator</span></span>                 |
| <span data-ttu-id="187cb-119">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="187cb-119">Update Frequency</span></span>  | <span data-ttu-id="187cb-120">Ogni volta che l'utente esegue l'accesso.</span><span class="sxs-lookup"><span data-stu-id="187cb-120">Each time the user logs on.</span></span>          |
| <span data-ttu-id="187cb-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="187cb-121">Attribute-Id</span></span>      | <span data-ttu-id="187cb-122">1.2.840.113556.1.4.169</span><span class="sxs-lookup"><span data-stu-id="187cb-122">1.2.840.113556.1.4.169</span></span>               |
| <span data-ttu-id="187cb-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="187cb-123">System-Id-Guid</span></span>    | <span data-ttu-id="187cb-124">bf9679aa-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="187cb-124">bf9679aa-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="187cb-125">Sintassi</span><span class="sxs-lookup"><span data-stu-id="187cb-125">Syntax</span></span>            | [<span data-ttu-id="187cb-126">**Enumerazione**</span><span class="sxs-lookup"><span data-stu-id="187cb-126">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="187cb-127">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="187cb-127">Implementations</span></span>

-   [<span data-ttu-id="187cb-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="187cb-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="187cb-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="187cb-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="187cb-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="187cb-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="187cb-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="187cb-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="187cb-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="187cb-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="187cb-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="187cb-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="187cb-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="187cb-134">Windows 2000 Server</span></span>



| <span data-ttu-id="187cb-135">Voce</span><span class="sxs-lookup"><span data-stu-id="187cb-135">Entry</span></span> | <span data-ttu-id="187cb-136">Valore</span><span class="sxs-lookup"><span data-stu-id="187cb-136">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="187cb-137">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="187cb-137">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="187cb-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="187cb-138">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="187cb-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="187cb-139">System-Only</span></span>            | <span data-ttu-id="187cb-140">Falso</span><span class="sxs-lookup"><span data-stu-id="187cb-140">False</span></span>                             |
| <span data-ttu-id="187cb-141">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="187cb-141">Is-Single-Valued</span></span>       | <span data-ttu-id="187cb-142">Vero</span><span class="sxs-lookup"><span data-stu-id="187cb-142">True</span></span>                              |
| <span data-ttu-id="187cb-143">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="187cb-143">Is Indexed</span></span>             | <span data-ttu-id="187cb-144">Falso</span><span class="sxs-lookup"><span data-stu-id="187cb-144">False</span></span>                             |
| <span data-ttu-id="187cb-145">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="187cb-145">In Global Catalog</span></span>      | <span data-ttu-id="187cb-146">Falso</span><span class="sxs-lookup"><span data-stu-id="187cb-146">False</span></span>                             |
| <span data-ttu-id="187cb-147">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="187cb-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="187cb-148">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="187cb-148">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="187cb-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="187cb-149">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="187cb-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="187cb-150">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="187cb-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="187cb-151">Search-Flags</span></span>           | <span data-ttu-id="187cb-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="187cb-152">0x00000000</span></span>                        |
| <span data-ttu-id="187cb-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="187cb-153">System-Flags</span></span>           | <span data-ttu-id="187cb-154">0x00000011</span><span class="sxs-lookup"><span data-stu-id="187cb-154">0x00000011</span></span>                        |
| <span data-ttu-id="187cb-155">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="187cb-155">Classes used in</span></span>        | [<span data-ttu-id="187cb-156">**Utente**</span><span class="sxs-lookup"><span data-stu-id="187cb-156">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="187cb-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="187cb-157">Windows Server 2003</span></span>



| <span data-ttu-id="187cb-158">Voce</span><span class="sxs-lookup"><span data-stu-id="187cb-158">Entry</span></span> | <span data-ttu-id="187cb-159">Valore</span><span class="sxs-lookup"><span data-stu-id="187cb-159">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="187cb-160">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="187cb-160">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="187cb-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="187cb-161">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="187cb-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="187cb-162">System-Only</span></span>            | <span data-ttu-id="187cb-163">Falso</span><span class="sxs-lookup"><span data-stu-id="187cb-163">False</span></span>                             |
| <span data-ttu-id="187cb-164">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="187cb-164">Is-Single-Valued</span></span>       | <span data-ttu-id="187cb-165">Vero</span><span class="sxs-lookup"><span data-stu-id="187cb-165">True</span></span>                              |
| <span data-ttu-id="187cb-166">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="187cb-166">Is Indexed</span></span>             | <span data-ttu-id="187cb-167">Falso</span><span class="sxs-lookup"><span data-stu-id="187cb-167">False</span></span>                             |
| <span data-ttu-id="187cb-168">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="187cb-168">In Global Catalog</span></span>      | <span data-ttu-id="187cb-169">Falso</span><span class="sxs-lookup"><span data-stu-id="187cb-169">False</span></span>                             |
| <span data-ttu-id="187cb-170">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="187cb-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="187cb-171">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="187cb-171">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="187cb-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="187cb-172">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="187cb-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="187cb-173">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="187cb-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="187cb-174">Search-Flags</span></span>           | <span data-ttu-id="187cb-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="187cb-175">0x00000000</span></span>                        |
| <span data-ttu-id="187cb-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="187cb-176">System-Flags</span></span>           | <span data-ttu-id="187cb-177">0x00000011</span><span class="sxs-lookup"><span data-stu-id="187cb-177">0x00000011</span></span>                        |
| <span data-ttu-id="187cb-178">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="187cb-178">Classes used in</span></span>        | [<span data-ttu-id="187cb-179">**Utente**</span><span class="sxs-lookup"><span data-stu-id="187cb-179">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="187cb-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="187cb-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="187cb-181">Voce</span><span class="sxs-lookup"><span data-stu-id="187cb-181">Entry</span></span> | <span data-ttu-id="187cb-182">Valore</span><span class="sxs-lookup"><span data-stu-id="187cb-182">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="187cb-183">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="187cb-183">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="187cb-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="187cb-184">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="187cb-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="187cb-185">System-Only</span></span>            | <span data-ttu-id="187cb-186">Falso</span><span class="sxs-lookup"><span data-stu-id="187cb-186">False</span></span>                             |
| <span data-ttu-id="187cb-187">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="187cb-187">Is-Single-Valued</span></span>       | <span data-ttu-id="187cb-188">Vero</span><span class="sxs-lookup"><span data-stu-id="187cb-188">True</span></span>                              |
| <span data-ttu-id="187cb-189">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="187cb-189">Is Indexed</span></span>             | <span data-ttu-id="187cb-190">Falso</span><span class="sxs-lookup"><span data-stu-id="187cb-190">False</span></span>                             |
| <span data-ttu-id="187cb-191">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="187cb-191">In Global Catalog</span></span>      | <span data-ttu-id="187cb-192">Falso</span><span class="sxs-lookup"><span data-stu-id="187cb-192">False</span></span>                             |
| <span data-ttu-id="187cb-193">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="187cb-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="187cb-194">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="187cb-194">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="187cb-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="187cb-195">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="187cb-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="187cb-196">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="187cb-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="187cb-197">Search-Flags</span></span>           | <span data-ttu-id="187cb-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="187cb-198">0x00000000</span></span>                        |
| <span data-ttu-id="187cb-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="187cb-199">System-Flags</span></span>           | <span data-ttu-id="187cb-200">0x00000011</span><span class="sxs-lookup"><span data-stu-id="187cb-200">0x00000011</span></span>                        |
| <span data-ttu-id="187cb-201">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="187cb-201">Classes used in</span></span>        | [<span data-ttu-id="187cb-202">**Utente**</span><span class="sxs-lookup"><span data-stu-id="187cb-202">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="187cb-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="187cb-203">Windows Server 2008</span></span>



| <span data-ttu-id="187cb-204">Voce</span><span class="sxs-lookup"><span data-stu-id="187cb-204">Entry</span></span> | <span data-ttu-id="187cb-205">Valore</span><span class="sxs-lookup"><span data-stu-id="187cb-205">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="187cb-206">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="187cb-206">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="187cb-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="187cb-207">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="187cb-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="187cb-208">System-Only</span></span>            | <span data-ttu-id="187cb-209">Falso</span><span class="sxs-lookup"><span data-stu-id="187cb-209">False</span></span>                             |
| <span data-ttu-id="187cb-210">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="187cb-210">Is-Single-Valued</span></span>       | <span data-ttu-id="187cb-211">Vero</span><span class="sxs-lookup"><span data-stu-id="187cb-211">True</span></span>                              |
| <span data-ttu-id="187cb-212">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="187cb-212">Is Indexed</span></span>             | <span data-ttu-id="187cb-213">Falso</span><span class="sxs-lookup"><span data-stu-id="187cb-213">False</span></span>                             |
| <span data-ttu-id="187cb-214">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="187cb-214">In Global Catalog</span></span>      | <span data-ttu-id="187cb-215">Falso</span><span class="sxs-lookup"><span data-stu-id="187cb-215">False</span></span>                             |
| <span data-ttu-id="187cb-216">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="187cb-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="187cb-217">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="187cb-217">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="187cb-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="187cb-218">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="187cb-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="187cb-219">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="187cb-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="187cb-220">Search-Flags</span></span>           | <span data-ttu-id="187cb-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="187cb-221">0x00000000</span></span>                        |
| <span data-ttu-id="187cb-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="187cb-222">System-Flags</span></span>           | <span data-ttu-id="187cb-223">0x00000011</span><span class="sxs-lookup"><span data-stu-id="187cb-223">0x00000011</span></span>                        |
| <span data-ttu-id="187cb-224">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="187cb-224">Classes used in</span></span>        | [<span data-ttu-id="187cb-225">**Utente**</span><span class="sxs-lookup"><span data-stu-id="187cb-225">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="187cb-226">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="187cb-226">Windows Server 2008 R2</span></span>



| <span data-ttu-id="187cb-227">Voce</span><span class="sxs-lookup"><span data-stu-id="187cb-227">Entry</span></span> | <span data-ttu-id="187cb-228">Valore</span><span class="sxs-lookup"><span data-stu-id="187cb-228">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="187cb-229">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="187cb-229">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="187cb-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="187cb-230">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="187cb-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="187cb-231">System-Only</span></span>            | <span data-ttu-id="187cb-232">Falso</span><span class="sxs-lookup"><span data-stu-id="187cb-232">False</span></span>                             |
| <span data-ttu-id="187cb-233">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="187cb-233">Is-Single-Valued</span></span>       | <span data-ttu-id="187cb-234">Vero</span><span class="sxs-lookup"><span data-stu-id="187cb-234">True</span></span>                              |
| <span data-ttu-id="187cb-235">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="187cb-235">Is Indexed</span></span>             | <span data-ttu-id="187cb-236">Falso</span><span class="sxs-lookup"><span data-stu-id="187cb-236">False</span></span>                             |
| <span data-ttu-id="187cb-237">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="187cb-237">In Global Catalog</span></span>      | <span data-ttu-id="187cb-238">Falso</span><span class="sxs-lookup"><span data-stu-id="187cb-238">False</span></span>                             |
| <span data-ttu-id="187cb-239">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="187cb-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="187cb-240">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="187cb-240">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="187cb-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="187cb-241">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="187cb-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="187cb-242">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="187cb-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="187cb-243">Search-Flags</span></span>           | <span data-ttu-id="187cb-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="187cb-244">0x00000000</span></span>                        |
| <span data-ttu-id="187cb-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="187cb-245">System-Flags</span></span>           | <span data-ttu-id="187cb-246">0x00000011</span><span class="sxs-lookup"><span data-stu-id="187cb-246">0x00000011</span></span>                        |
| <span data-ttu-id="187cb-247">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="187cb-247">Classes used in</span></span>        | [<span data-ttu-id="187cb-248">**Utente**</span><span class="sxs-lookup"><span data-stu-id="187cb-248">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="187cb-249">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="187cb-249">Windows Server 2012</span></span>



| <span data-ttu-id="187cb-250">Voce</span><span class="sxs-lookup"><span data-stu-id="187cb-250">Entry</span></span> | <span data-ttu-id="187cb-251">Valore</span><span class="sxs-lookup"><span data-stu-id="187cb-251">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="187cb-252">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="187cb-252">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="187cb-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="187cb-253">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="187cb-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="187cb-254">System-Only</span></span>            | <span data-ttu-id="187cb-255">Falso</span><span class="sxs-lookup"><span data-stu-id="187cb-255">False</span></span>                             |
| <span data-ttu-id="187cb-256">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="187cb-256">Is-Single-Valued</span></span>       | <span data-ttu-id="187cb-257">Vero</span><span class="sxs-lookup"><span data-stu-id="187cb-257">True</span></span>                              |
| <span data-ttu-id="187cb-258">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="187cb-258">Is Indexed</span></span>             | <span data-ttu-id="187cb-259">Falso</span><span class="sxs-lookup"><span data-stu-id="187cb-259">False</span></span>                             |
| <span data-ttu-id="187cb-260">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="187cb-260">In Global Catalog</span></span>      | <span data-ttu-id="187cb-261">Falso</span><span class="sxs-lookup"><span data-stu-id="187cb-261">False</span></span>                             |
| <span data-ttu-id="187cb-262">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="187cb-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="187cb-263">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="187cb-263">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="187cb-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="187cb-264">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="187cb-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="187cb-265">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="187cb-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="187cb-266">Search-Flags</span></span>           | <span data-ttu-id="187cb-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="187cb-267">0x00000000</span></span>                        |
| <span data-ttu-id="187cb-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="187cb-268">System-Flags</span></span>           | <span data-ttu-id="187cb-269">0x00000011</span><span class="sxs-lookup"><span data-stu-id="187cb-269">0x00000011</span></span>                        |
| <span data-ttu-id="187cb-270">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="187cb-270">Classes used in</span></span>        | [<span data-ttu-id="187cb-271">**Utente**</span><span class="sxs-lookup"><span data-stu-id="187cb-271">**User**</span></span>](c-user.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="187cb-272">Commenti</span><span class="sxs-lookup"><span data-stu-id="187cb-272">Remarks</span></span>

<span data-ttu-id="187cb-273">Questo attributo non viene replicato e viene mantenuto in ogni controller di dominio nel dominio.</span><span class="sxs-lookup"><span data-stu-id="187cb-273">This attribute is not replicated and is maintained on each domain controller in the domain.</span></span> <span data-ttu-id="187cb-274">Per ottenere un valore preciso per il numero totale di tentativi di accesso riusciti nel dominio, è necessario eseguire una query su ogni controller di dominio nel dominio e utilizzare la somma dei valori.</span><span class="sxs-lookup"><span data-stu-id="187cb-274">To get an accurate value for the user's total number of successful logon attempts in the domain, each domain controller in the domain must be queried and the sum of the values should be used.</span></span> <span data-ttu-id="187cb-275">Tenere presente che l'attributo non è replicato, pertanto i controller di dominio ritirati potrebbero avere conteggiati anche gli accessi per l'utente e questi non saranno presenti nel conteggio.</span><span class="sxs-lookup"><span data-stu-id="187cb-275">Keep in mind that the attribute is not replicated, therefore domain controllers that are retired may have counted logons for the user as well, and these will be missing from the count.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="187cb-276">A causa della compatibilità con le versioni a 16 bit di LAN Manager, l'attributo ha un limite massimo di 65535.</span><span class="sxs-lookup"><span data-stu-id="187cb-276">Due to compatibility with 16-bit versions of LAN Manager, the attribute has an upper limit of 65535.</span></span> <span data-ttu-id="187cb-277">Una volta raggiunto questo limite, non è possibile utilizzarlo come indicatore dell'attività dell'utente nel controller di dominio.</span><span class="sxs-lookup"><span data-stu-id="187cb-277">After this limit has been reached, you cannot use it as an indicator of user activity on this domain controller.</span></span>

 

 

 





