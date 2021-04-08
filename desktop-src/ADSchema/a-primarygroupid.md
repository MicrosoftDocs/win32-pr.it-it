---
title: Attributo Primary-Group-ID
description: Contiene l'identificatore relativo (RID) per il gruppo primario dell'utente. Per impostazione predefinita, si tratta del RID per il gruppo Domain Users.
ms.assetid: 80803734-f7dd-4348-a110-ca6b8bccb60b
ms.tgt_platform: multiple
keywords:
- Primary-Group-ID attributo AD schema
- Schema AD dell'attributo primaryGroupID
topic_type:
- apiref
api_name:
- Primary-Group-ID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad2b6237ff6e49a01da3b960b58103ae10dca7b2
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744959"
---
# <a name="primary-group-id-attribute"></a><span data-ttu-id="29389-106">Attributo Primary-Group-ID</span><span class="sxs-lookup"><span data-stu-id="29389-106">Primary-Group-ID attribute</span></span>

<span data-ttu-id="29389-107">Contiene l'identificatore relativo (RID) per il gruppo primario dell'utente.</span><span class="sxs-lookup"><span data-stu-id="29389-107">Contains the relative identifier (RID) for the primary group of the user.</span></span> <span data-ttu-id="29389-108">Per impostazione predefinita, si tratta del RID per il gruppo Domain Users.</span><span class="sxs-lookup"><span data-stu-id="29389-108">By default, this is the RID for the Domain Users group.</span></span>



| <span data-ttu-id="29389-109">Voce</span><span class="sxs-lookup"><span data-stu-id="29389-109">Entry</span></span> | <span data-ttu-id="29389-110">Valore</span><span class="sxs-lookup"><span data-stu-id="29389-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="29389-111">CN</span><span class="sxs-lookup"><span data-stu-id="29389-111">CN</span></span>                | <span data-ttu-id="29389-112">Primary-Group-ID</span><span class="sxs-lookup"><span data-stu-id="29389-112">Primary-Group-ID</span></span>                     |
| <span data-ttu-id="29389-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="29389-113">Ldap-Display-Name</span></span> | <span data-ttu-id="29389-114">primaryGroupID</span><span class="sxs-lookup"><span data-stu-id="29389-114">primaryGroupID</span></span>                       |
| <span data-ttu-id="29389-115">Dimensione</span><span class="sxs-lookup"><span data-stu-id="29389-115">Size</span></span>              | <span data-ttu-id="29389-116">4 byte</span><span class="sxs-lookup"><span data-stu-id="29389-116">4 bytes</span></span>                              |
| <span data-ttu-id="29389-117">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="29389-117">Update Privilege</span></span>  | <span data-ttu-id="29389-118">Questo valore viene impostato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="29389-118">This value is set by the system.</span></span>     |
| <span data-ttu-id="29389-119">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="29389-119">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="29389-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="29389-120">Attribute-Id</span></span>      | <span data-ttu-id="29389-121">1.2.840.113556.1.4.98</span><span class="sxs-lookup"><span data-stu-id="29389-121">1.2.840.113556.1.4.98</span></span>                |
| <span data-ttu-id="29389-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="29389-122">System-Id-Guid</span></span>    | <span data-ttu-id="29389-123">bf967a00-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="29389-123">bf967a00-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="29389-124">Sintassi</span><span class="sxs-lookup"><span data-stu-id="29389-124">Syntax</span></span>            | [<span data-ttu-id="29389-125">**Enumerazione**</span><span class="sxs-lookup"><span data-stu-id="29389-125">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="29389-126">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="29389-126">Implementations</span></span>

-   [<span data-ttu-id="29389-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="29389-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="29389-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="29389-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="29389-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="29389-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="29389-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="29389-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="29389-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="29389-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="29389-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="29389-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="29389-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="29389-133">Windows 2000 Server</span></span>



| <span data-ttu-id="29389-134">Voce</span><span class="sxs-lookup"><span data-stu-id="29389-134">Entry</span></span> | <span data-ttu-id="29389-135">Valore</span><span class="sxs-lookup"><span data-stu-id="29389-135">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="29389-136">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="29389-136">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="29389-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="29389-137">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="29389-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="29389-138">System-Only</span></span>            | <span data-ttu-id="29389-139">Falso</span><span class="sxs-lookup"><span data-stu-id="29389-139">False</span></span>                             |
| <span data-ttu-id="29389-140">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="29389-140">Is-Single-Valued</span></span>       | <span data-ttu-id="29389-141">Vero</span><span class="sxs-lookup"><span data-stu-id="29389-141">True</span></span>                              |
| <span data-ttu-id="29389-142">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="29389-142">Is Indexed</span></span>             | <span data-ttu-id="29389-143">Vero</span><span class="sxs-lookup"><span data-stu-id="29389-143">True</span></span>                              |
| <span data-ttu-id="29389-144">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="29389-144">In Global Catalog</span></span>      | <span data-ttu-id="29389-145">Vero</span><span class="sxs-lookup"><span data-stu-id="29389-145">True</span></span>                              |
| <span data-ttu-id="29389-146">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="29389-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="29389-147">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="29389-147">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="29389-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="29389-148">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="29389-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="29389-149">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="29389-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="29389-150">Search-Flags</span></span>           | <span data-ttu-id="29389-151">0x00000011</span><span class="sxs-lookup"><span data-stu-id="29389-151">0x00000011</span></span>                        |
| <span data-ttu-id="29389-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="29389-152">System-Flags</span></span>           | <span data-ttu-id="29389-153">0x00000012</span><span class="sxs-lookup"><span data-stu-id="29389-153">0x00000012</span></span>                        |
| <span data-ttu-id="29389-154">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="29389-154">Classes used in</span></span>        | [<span data-ttu-id="29389-155">**Utente**</span><span class="sxs-lookup"><span data-stu-id="29389-155">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="29389-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="29389-156">Windows Server 2003</span></span>



| <span data-ttu-id="29389-157">Voce</span><span class="sxs-lookup"><span data-stu-id="29389-157">Entry</span></span> | <span data-ttu-id="29389-158">Valore</span><span class="sxs-lookup"><span data-stu-id="29389-158">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="29389-159">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="29389-159">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="29389-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="29389-160">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="29389-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="29389-161">System-Only</span></span>            | <span data-ttu-id="29389-162">Falso</span><span class="sxs-lookup"><span data-stu-id="29389-162">False</span></span>                             |
| <span data-ttu-id="29389-163">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="29389-163">Is-Single-Valued</span></span>       | <span data-ttu-id="29389-164">Vero</span><span class="sxs-lookup"><span data-stu-id="29389-164">True</span></span>                              |
| <span data-ttu-id="29389-165">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="29389-165">Is Indexed</span></span>             | <span data-ttu-id="29389-166">Vero</span><span class="sxs-lookup"><span data-stu-id="29389-166">True</span></span>                              |
| <span data-ttu-id="29389-167">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="29389-167">In Global Catalog</span></span>      | <span data-ttu-id="29389-168">Vero</span><span class="sxs-lookup"><span data-stu-id="29389-168">True</span></span>                              |
| <span data-ttu-id="29389-169">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="29389-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="29389-170">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="29389-170">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="29389-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="29389-171">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="29389-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="29389-172">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="29389-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="29389-173">Search-Flags</span></span>           | <span data-ttu-id="29389-174">0x00000011</span><span class="sxs-lookup"><span data-stu-id="29389-174">0x00000011</span></span>                        |
| <span data-ttu-id="29389-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="29389-175">System-Flags</span></span>           | <span data-ttu-id="29389-176">0x00000012</span><span class="sxs-lookup"><span data-stu-id="29389-176">0x00000012</span></span>                        |
| <span data-ttu-id="29389-177">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="29389-177">Classes used in</span></span>        | [<span data-ttu-id="29389-178">**Utente**</span><span class="sxs-lookup"><span data-stu-id="29389-178">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="29389-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="29389-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="29389-180">Voce</span><span class="sxs-lookup"><span data-stu-id="29389-180">Entry</span></span> | <span data-ttu-id="29389-181">Valore</span><span class="sxs-lookup"><span data-stu-id="29389-181">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="29389-182">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="29389-182">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="29389-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="29389-183">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="29389-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="29389-184">System-Only</span></span>            | <span data-ttu-id="29389-185">Falso</span><span class="sxs-lookup"><span data-stu-id="29389-185">False</span></span>                             |
| <span data-ttu-id="29389-186">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="29389-186">Is-Single-Valued</span></span>       | <span data-ttu-id="29389-187">Vero</span><span class="sxs-lookup"><span data-stu-id="29389-187">True</span></span>                              |
| <span data-ttu-id="29389-188">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="29389-188">Is Indexed</span></span>             | <span data-ttu-id="29389-189">Vero</span><span class="sxs-lookup"><span data-stu-id="29389-189">True</span></span>                              |
| <span data-ttu-id="29389-190">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="29389-190">In Global Catalog</span></span>      | <span data-ttu-id="29389-191">Vero</span><span class="sxs-lookup"><span data-stu-id="29389-191">True</span></span>                              |
| <span data-ttu-id="29389-192">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="29389-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="29389-193">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="29389-193">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="29389-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="29389-194">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="29389-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="29389-195">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="29389-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="29389-196">Search-Flags</span></span>           | <span data-ttu-id="29389-197">0x00000011</span><span class="sxs-lookup"><span data-stu-id="29389-197">0x00000011</span></span>                        |
| <span data-ttu-id="29389-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="29389-198">System-Flags</span></span>           | <span data-ttu-id="29389-199">0x00000012</span><span class="sxs-lookup"><span data-stu-id="29389-199">0x00000012</span></span>                        |
| <span data-ttu-id="29389-200">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="29389-200">Classes used in</span></span>        | [<span data-ttu-id="29389-201">**Utente**</span><span class="sxs-lookup"><span data-stu-id="29389-201">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="29389-202">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="29389-202">Windows Server 2008</span></span>



| <span data-ttu-id="29389-203">Voce</span><span class="sxs-lookup"><span data-stu-id="29389-203">Entry</span></span> | <span data-ttu-id="29389-204">Valore</span><span class="sxs-lookup"><span data-stu-id="29389-204">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="29389-205">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="29389-205">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="29389-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="29389-206">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="29389-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="29389-207">System-Only</span></span>            | <span data-ttu-id="29389-208">Falso</span><span class="sxs-lookup"><span data-stu-id="29389-208">False</span></span>                             |
| <span data-ttu-id="29389-209">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="29389-209">Is-Single-Valued</span></span>       | <span data-ttu-id="29389-210">Vero</span><span class="sxs-lookup"><span data-stu-id="29389-210">True</span></span>                              |
| <span data-ttu-id="29389-211">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="29389-211">Is Indexed</span></span>             | <span data-ttu-id="29389-212">Vero</span><span class="sxs-lookup"><span data-stu-id="29389-212">True</span></span>                              |
| <span data-ttu-id="29389-213">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="29389-213">In Global Catalog</span></span>      | <span data-ttu-id="29389-214">Vero</span><span class="sxs-lookup"><span data-stu-id="29389-214">True</span></span>                              |
| <span data-ttu-id="29389-215">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="29389-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="29389-216">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="29389-216">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="29389-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="29389-217">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="29389-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="29389-218">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="29389-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="29389-219">Search-Flags</span></span>           | <span data-ttu-id="29389-220">0x00000011</span><span class="sxs-lookup"><span data-stu-id="29389-220">0x00000011</span></span>                        |
| <span data-ttu-id="29389-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="29389-221">System-Flags</span></span>           | <span data-ttu-id="29389-222">0x00000012</span><span class="sxs-lookup"><span data-stu-id="29389-222">0x00000012</span></span>                        |
| <span data-ttu-id="29389-223">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="29389-223">Classes used in</span></span>        | [<span data-ttu-id="29389-224">**Utente**</span><span class="sxs-lookup"><span data-stu-id="29389-224">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="29389-225">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="29389-225">Windows Server 2008 R2</span></span>



| <span data-ttu-id="29389-226">Voce</span><span class="sxs-lookup"><span data-stu-id="29389-226">Entry</span></span> | <span data-ttu-id="29389-227">Valore</span><span class="sxs-lookup"><span data-stu-id="29389-227">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="29389-228">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="29389-228">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="29389-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="29389-229">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="29389-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="29389-230">System-Only</span></span>            | <span data-ttu-id="29389-231">Falso</span><span class="sxs-lookup"><span data-stu-id="29389-231">False</span></span>                             |
| <span data-ttu-id="29389-232">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="29389-232">Is-Single-Valued</span></span>       | <span data-ttu-id="29389-233">Vero</span><span class="sxs-lookup"><span data-stu-id="29389-233">True</span></span>                              |
| <span data-ttu-id="29389-234">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="29389-234">Is Indexed</span></span>             | <span data-ttu-id="29389-235">Vero</span><span class="sxs-lookup"><span data-stu-id="29389-235">True</span></span>                              |
| <span data-ttu-id="29389-236">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="29389-236">In Global Catalog</span></span>      | <span data-ttu-id="29389-237">Vero</span><span class="sxs-lookup"><span data-stu-id="29389-237">True</span></span>                              |
| <span data-ttu-id="29389-238">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="29389-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="29389-239">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="29389-239">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="29389-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="29389-240">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="29389-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="29389-241">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="29389-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="29389-242">Search-Flags</span></span>           | <span data-ttu-id="29389-243">0x00000011</span><span class="sxs-lookup"><span data-stu-id="29389-243">0x00000011</span></span>                        |
| <span data-ttu-id="29389-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="29389-244">System-Flags</span></span>           | <span data-ttu-id="29389-245">0x00000012</span><span class="sxs-lookup"><span data-stu-id="29389-245">0x00000012</span></span>                        |
| <span data-ttu-id="29389-246">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="29389-246">Classes used in</span></span>        | [<span data-ttu-id="29389-247">**Utente**</span><span class="sxs-lookup"><span data-stu-id="29389-247">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="29389-248">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="29389-248">Windows Server 2012</span></span>



| <span data-ttu-id="29389-249">Voce</span><span class="sxs-lookup"><span data-stu-id="29389-249">Entry</span></span> | <span data-ttu-id="29389-250">Valore</span><span class="sxs-lookup"><span data-stu-id="29389-250">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="29389-251">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="29389-251">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="29389-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="29389-252">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="29389-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="29389-253">System-Only</span></span>            | <span data-ttu-id="29389-254">Falso</span><span class="sxs-lookup"><span data-stu-id="29389-254">False</span></span>                             |
| <span data-ttu-id="29389-255">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="29389-255">Is-Single-Valued</span></span>       | <span data-ttu-id="29389-256">Vero</span><span class="sxs-lookup"><span data-stu-id="29389-256">True</span></span>                              |
| <span data-ttu-id="29389-257">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="29389-257">Is Indexed</span></span>             | <span data-ttu-id="29389-258">Vero</span><span class="sxs-lookup"><span data-stu-id="29389-258">True</span></span>                              |
| <span data-ttu-id="29389-259">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="29389-259">In Global Catalog</span></span>      | <span data-ttu-id="29389-260">Vero</span><span class="sxs-lookup"><span data-stu-id="29389-260">True</span></span>                              |
| <span data-ttu-id="29389-261">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="29389-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="29389-262">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="29389-262">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="29389-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="29389-263">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="29389-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="29389-264">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="29389-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="29389-265">Search-Flags</span></span>           | <span data-ttu-id="29389-266">0x00000011</span><span class="sxs-lookup"><span data-stu-id="29389-266">0x00000011</span></span>                        |
| <span data-ttu-id="29389-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="29389-267">System-Flags</span></span>           | <span data-ttu-id="29389-268">0x00000012</span><span class="sxs-lookup"><span data-stu-id="29389-268">0x00000012</span></span>                        |
| <span data-ttu-id="29389-269">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="29389-269">Classes used in</span></span>        | [<span data-ttu-id="29389-270">**Utente**</span><span class="sxs-lookup"><span data-stu-id="29389-270">**User**</span></span>](c-user.md)<br/> |



 

 





