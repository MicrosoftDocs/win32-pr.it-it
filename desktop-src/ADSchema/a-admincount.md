---
title: Attributo Admin-Count
description: Indica che per un determinato oggetto sono stati modificati gli ACL a un valore più sicuro dal sistema perché era un membro di uno dei gruppi amministrativi (direttamente o in modo transitivo).
ms.assetid: b2384ada-a792-42fa-be64-291d23e00887
ms.tgt_platform: multiple
keywords:
- Schema AD Admin-Count attribute
- Schema AD dell'attributo adminCount
topic_type:
- apiref
api_name:
- Admin-Count
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e95b953aebaa39bb3fc3e4c9cf96632f32a37850
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103745306"
---
# <a name="admin-count-attribute"></a><span data-ttu-id="852e6-105">Attributo Admin-Count</span><span class="sxs-lookup"><span data-stu-id="852e6-105">Admin-Count attribute</span></span>

<span data-ttu-id="852e6-106">Indica che per un determinato oggetto sono stati modificati gli ACL a un valore più sicuro dal sistema perché era un membro di uno dei gruppi amministrativi (direttamente o in modo transitivo).</span><span class="sxs-lookup"><span data-stu-id="852e6-106">Indicates that a given object has had its ACLs changed to a more secure value by the system because it was a member of one of the administrative groups (directly or transitively).</span></span>



| <span data-ttu-id="852e6-107">Voce</span><span class="sxs-lookup"><span data-stu-id="852e6-107">Entry</span></span> | <span data-ttu-id="852e6-108">Valore</span><span class="sxs-lookup"><span data-stu-id="852e6-108">Value</span></span> |
|-------------------|-----------------------------------------------------|
| <span data-ttu-id="852e6-109">CN</span><span class="sxs-lookup"><span data-stu-id="852e6-109">CN</span></span>                | <span data-ttu-id="852e6-110">Admin-Count</span><span class="sxs-lookup"><span data-stu-id="852e6-110">Admin-Count</span></span>                                         |
| <span data-ttu-id="852e6-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="852e6-111">Ldap-Display-Name</span></span> | <span data-ttu-id="852e6-112">adminCount</span><span class="sxs-lookup"><span data-stu-id="852e6-112">adminCount</span></span>                                          |
| <span data-ttu-id="852e6-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="852e6-113">Size</span></span>              | <span data-ttu-id="852e6-114">4 byte</span><span class="sxs-lookup"><span data-stu-id="852e6-114">4 bytes</span></span>                                             |
| <span data-ttu-id="852e6-115">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="852e6-115">Update Privilege</span></span>  | <span data-ttu-id="852e6-116">Questo valore viene impostato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="852e6-116">This value is set by the system.</span></span>                    |
| <span data-ttu-id="852e6-117">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="852e6-117">Update Frequency</span></span>  | <span data-ttu-id="852e6-118">Quando un oggetto viene aggiunto a un gruppo amministrativo.</span><span class="sxs-lookup"><span data-stu-id="852e6-118">When an object is added to an administrative group.</span></span> |
| <span data-ttu-id="852e6-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="852e6-119">Attribute-Id</span></span>      | <span data-ttu-id="852e6-120">1.2.840.113556.1.4.150</span><span class="sxs-lookup"><span data-stu-id="852e6-120">1.2.840.113556.1.4.150</span></span>                              |
| <span data-ttu-id="852e6-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="852e6-121">System-Id-Guid</span></span>    | <span data-ttu-id="852e6-122">bf967918-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="852e6-122">bf967918-0de6-11d0-a285-00aa003049e2</span></span>                |
| <span data-ttu-id="852e6-123">Sintassi</span><span class="sxs-lookup"><span data-stu-id="852e6-123">Syntax</span></span>            | [<span data-ttu-id="852e6-124">**Enumerazione**</span><span class="sxs-lookup"><span data-stu-id="852e6-124">**Enumeration**</span></span>](s-enumeration.md)                |



## <a name="implementations"></a><span data-ttu-id="852e6-125">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="852e6-125">Implementations</span></span>

-   [<span data-ttu-id="852e6-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="852e6-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="852e6-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="852e6-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="852e6-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="852e6-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="852e6-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="852e6-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="852e6-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="852e6-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="852e6-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="852e6-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="852e6-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="852e6-132">Windows 2000 Server</span></span>



| <span data-ttu-id="852e6-133">Voce</span><span class="sxs-lookup"><span data-stu-id="852e6-133">Entry</span></span> | <span data-ttu-id="852e6-134">Valore</span><span class="sxs-lookup"><span data-stu-id="852e6-134">Value</span></span> |
|------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="852e6-135">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="852e6-135">Link-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="852e6-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="852e6-136">MAPI-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="852e6-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="852e6-137">System-Only</span></span>            | <span data-ttu-id="852e6-138">Falso</span><span class="sxs-lookup"><span data-stu-id="852e6-138">False</span></span>                                                                 |
| <span data-ttu-id="852e6-139">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="852e6-139">Is-Single-Valued</span></span>       | <span data-ttu-id="852e6-140">Vero</span><span class="sxs-lookup"><span data-stu-id="852e6-140">True</span></span>                                                                  |
| <span data-ttu-id="852e6-141">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="852e6-141">Is Indexed</span></span>             | <span data-ttu-id="852e6-142">Falso</span><span class="sxs-lookup"><span data-stu-id="852e6-142">False</span></span>                                                                 |
| <span data-ttu-id="852e6-143">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="852e6-143">In Global Catalog</span></span>      | <span data-ttu-id="852e6-144">Falso</span><span class="sxs-lookup"><span data-stu-id="852e6-144">False</span></span>                                                                 |
| <span data-ttu-id="852e6-145">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="852e6-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="852e6-146">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="852e6-146">O:BAG:BAD:S:</span></span>                                                          |
| <span data-ttu-id="852e6-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="852e6-147">Range-Lower</span></span>            | \-                                                                    |
| <span data-ttu-id="852e6-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="852e6-148">Range-Upper</span></span>            | \-                                                                    |
| <span data-ttu-id="852e6-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="852e6-149">Search-Flags</span></span>           | <span data-ttu-id="852e6-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="852e6-150">0x00000000</span></span>                                                            |
| <span data-ttu-id="852e6-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="852e6-151">System-Flags</span></span>           | <span data-ttu-id="852e6-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="852e6-152">0x00000010</span></span>                                                            |
| <span data-ttu-id="852e6-153">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="852e6-153">Classes used in</span></span>        | [<span data-ttu-id="852e6-154">**Group**</span><span class="sxs-lookup"><span data-stu-id="852e6-154">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="852e6-155">**Utente**</span><span class="sxs-lookup"><span data-stu-id="852e6-155">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="852e6-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="852e6-156">Windows Server 2003</span></span>



| <span data-ttu-id="852e6-157">Voce</span><span class="sxs-lookup"><span data-stu-id="852e6-157">Entry</span></span> | <span data-ttu-id="852e6-158">Valore</span><span class="sxs-lookup"><span data-stu-id="852e6-158">Value</span></span> |
|------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="852e6-159">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="852e6-159">Link-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="852e6-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="852e6-160">MAPI-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="852e6-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="852e6-161">System-Only</span></span>            | <span data-ttu-id="852e6-162">Falso</span><span class="sxs-lookup"><span data-stu-id="852e6-162">False</span></span>                                                                 |
| <span data-ttu-id="852e6-163">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="852e6-163">Is-Single-Valued</span></span>       | <span data-ttu-id="852e6-164">Vero</span><span class="sxs-lookup"><span data-stu-id="852e6-164">True</span></span>                                                                  |
| <span data-ttu-id="852e6-165">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="852e6-165">Is Indexed</span></span>             | <span data-ttu-id="852e6-166">Falso</span><span class="sxs-lookup"><span data-stu-id="852e6-166">False</span></span>                                                                 |
| <span data-ttu-id="852e6-167">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="852e6-167">In Global Catalog</span></span>      | <span data-ttu-id="852e6-168">Falso</span><span class="sxs-lookup"><span data-stu-id="852e6-168">False</span></span>                                                                 |
| <span data-ttu-id="852e6-169">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="852e6-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="852e6-170">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="852e6-170">O:BAG:BAD:S:</span></span>                                                          |
| <span data-ttu-id="852e6-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="852e6-171">Range-Lower</span></span>            | \-                                                                    |
| <span data-ttu-id="852e6-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="852e6-172">Range-Upper</span></span>            | \-                                                                    |
| <span data-ttu-id="852e6-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="852e6-173">Search-Flags</span></span>           | <span data-ttu-id="852e6-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="852e6-174">0x00000000</span></span>                                                            |
| <span data-ttu-id="852e6-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="852e6-175">System-Flags</span></span>           | <span data-ttu-id="852e6-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="852e6-176">0x00000010</span></span>                                                            |
| <span data-ttu-id="852e6-177">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="852e6-177">Classes used in</span></span>        | [<span data-ttu-id="852e6-178">**Group**</span><span class="sxs-lookup"><span data-stu-id="852e6-178">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="852e6-179">**Utente**</span><span class="sxs-lookup"><span data-stu-id="852e6-179">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="852e6-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="852e6-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="852e6-181">Voce</span><span class="sxs-lookup"><span data-stu-id="852e6-181">Entry</span></span> | <span data-ttu-id="852e6-182">Valore</span><span class="sxs-lookup"><span data-stu-id="852e6-182">Value</span></span> |
|------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="852e6-183">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="852e6-183">Link-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="852e6-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="852e6-184">MAPI-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="852e6-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="852e6-185">System-Only</span></span>            | <span data-ttu-id="852e6-186">Falso</span><span class="sxs-lookup"><span data-stu-id="852e6-186">False</span></span>                                                                 |
| <span data-ttu-id="852e6-187">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="852e6-187">Is-Single-Valued</span></span>       | <span data-ttu-id="852e6-188">Vero</span><span class="sxs-lookup"><span data-stu-id="852e6-188">True</span></span>                                                                  |
| <span data-ttu-id="852e6-189">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="852e6-189">Is Indexed</span></span>             | <span data-ttu-id="852e6-190">Falso</span><span class="sxs-lookup"><span data-stu-id="852e6-190">False</span></span>                                                                 |
| <span data-ttu-id="852e6-191">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="852e6-191">In Global Catalog</span></span>      | <span data-ttu-id="852e6-192">Falso</span><span class="sxs-lookup"><span data-stu-id="852e6-192">False</span></span>                                                                 |
| <span data-ttu-id="852e6-193">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="852e6-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="852e6-194">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="852e6-194">O:BAG:BAD:S:</span></span>                                                          |
| <span data-ttu-id="852e6-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="852e6-195">Range-Lower</span></span>            | \-                                                                    |
| <span data-ttu-id="852e6-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="852e6-196">Range-Upper</span></span>            | \-                                                                    |
| <span data-ttu-id="852e6-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="852e6-197">Search-Flags</span></span>           | <span data-ttu-id="852e6-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="852e6-198">0x00000000</span></span>                                                            |
| <span data-ttu-id="852e6-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="852e6-199">System-Flags</span></span>           | <span data-ttu-id="852e6-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="852e6-200">0x00000010</span></span>                                                            |
| <span data-ttu-id="852e6-201">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="852e6-201">Classes used in</span></span>        | [<span data-ttu-id="852e6-202">**Group**</span><span class="sxs-lookup"><span data-stu-id="852e6-202">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="852e6-203">**Utente**</span><span class="sxs-lookup"><span data-stu-id="852e6-203">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="852e6-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="852e6-204">Windows Server 2008</span></span>



| <span data-ttu-id="852e6-205">Voce</span><span class="sxs-lookup"><span data-stu-id="852e6-205">Entry</span></span> | <span data-ttu-id="852e6-206">Valore</span><span class="sxs-lookup"><span data-stu-id="852e6-206">Value</span></span> |
|------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="852e6-207">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="852e6-207">Link-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="852e6-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="852e6-208">MAPI-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="852e6-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="852e6-209">System-Only</span></span>            | <span data-ttu-id="852e6-210">Falso</span><span class="sxs-lookup"><span data-stu-id="852e6-210">False</span></span>                                                                 |
| <span data-ttu-id="852e6-211">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="852e6-211">Is-Single-Valued</span></span>       | <span data-ttu-id="852e6-212">Vero</span><span class="sxs-lookup"><span data-stu-id="852e6-212">True</span></span>                                                                  |
| <span data-ttu-id="852e6-213">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="852e6-213">Is Indexed</span></span>             | <span data-ttu-id="852e6-214">Falso</span><span class="sxs-lookup"><span data-stu-id="852e6-214">False</span></span>                                                                 |
| <span data-ttu-id="852e6-215">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="852e6-215">In Global Catalog</span></span>      | <span data-ttu-id="852e6-216">Falso</span><span class="sxs-lookup"><span data-stu-id="852e6-216">False</span></span>                                                                 |
| <span data-ttu-id="852e6-217">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="852e6-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="852e6-218">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="852e6-218">O:BAG:BAD:S:</span></span>                                                          |
| <span data-ttu-id="852e6-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="852e6-219">Range-Lower</span></span>            | \-                                                                    |
| <span data-ttu-id="852e6-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="852e6-220">Range-Upper</span></span>            | \-                                                                    |
| <span data-ttu-id="852e6-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="852e6-221">Search-Flags</span></span>           | <span data-ttu-id="852e6-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="852e6-222">0x00000000</span></span>                                                            |
| <span data-ttu-id="852e6-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="852e6-223">System-Flags</span></span>           | <span data-ttu-id="852e6-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="852e6-224">0x00000010</span></span>                                                            |
| <span data-ttu-id="852e6-225">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="852e6-225">Classes used in</span></span>        | [<span data-ttu-id="852e6-226">**Group**</span><span class="sxs-lookup"><span data-stu-id="852e6-226">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="852e6-227">**Utente**</span><span class="sxs-lookup"><span data-stu-id="852e6-227">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="852e6-228">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="852e6-228">Windows Server 2008 R2</span></span>



| <span data-ttu-id="852e6-229">Voce</span><span class="sxs-lookup"><span data-stu-id="852e6-229">Entry</span></span> | <span data-ttu-id="852e6-230">Valore</span><span class="sxs-lookup"><span data-stu-id="852e6-230">Value</span></span> |
|------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="852e6-231">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="852e6-231">Link-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="852e6-232">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="852e6-232">MAPI-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="852e6-233">System-Only</span><span class="sxs-lookup"><span data-stu-id="852e6-233">System-Only</span></span>            | <span data-ttu-id="852e6-234">Falso</span><span class="sxs-lookup"><span data-stu-id="852e6-234">False</span></span>                                                                 |
| <span data-ttu-id="852e6-235">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="852e6-235">Is-Single-Valued</span></span>       | <span data-ttu-id="852e6-236">Vero</span><span class="sxs-lookup"><span data-stu-id="852e6-236">True</span></span>                                                                  |
| <span data-ttu-id="852e6-237">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="852e6-237">Is Indexed</span></span>             | <span data-ttu-id="852e6-238">Falso</span><span class="sxs-lookup"><span data-stu-id="852e6-238">False</span></span>                                                                 |
| <span data-ttu-id="852e6-239">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="852e6-239">In Global Catalog</span></span>      | <span data-ttu-id="852e6-240">Falso</span><span class="sxs-lookup"><span data-stu-id="852e6-240">False</span></span>                                                                 |
| <span data-ttu-id="852e6-241">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="852e6-241">NT-Security-Descriptor</span></span> | <span data-ttu-id="852e6-242">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="852e6-242">O:BAG:BAD:S:</span></span>                                                          |
| <span data-ttu-id="852e6-243">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="852e6-243">Range-Lower</span></span>            | \-                                                                    |
| <span data-ttu-id="852e6-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="852e6-244">Range-Upper</span></span>            | \-                                                                    |
| <span data-ttu-id="852e6-245">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="852e6-245">Search-Flags</span></span>           | <span data-ttu-id="852e6-246">0x00000000</span><span class="sxs-lookup"><span data-stu-id="852e6-246">0x00000000</span></span>                                                            |
| <span data-ttu-id="852e6-247">System-Flags</span><span class="sxs-lookup"><span data-stu-id="852e6-247">System-Flags</span></span>           | <span data-ttu-id="852e6-248">0x00000010</span><span class="sxs-lookup"><span data-stu-id="852e6-248">0x00000010</span></span>                                                            |
| <span data-ttu-id="852e6-249">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="852e6-249">Classes used in</span></span>        | [<span data-ttu-id="852e6-250">**Group**</span><span class="sxs-lookup"><span data-stu-id="852e6-250">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="852e6-251">**Utente**</span><span class="sxs-lookup"><span data-stu-id="852e6-251">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="852e6-252">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="852e6-252">Windows Server 2012</span></span>



| <span data-ttu-id="852e6-253">Voce</span><span class="sxs-lookup"><span data-stu-id="852e6-253">Entry</span></span> | <span data-ttu-id="852e6-254">Valore</span><span class="sxs-lookup"><span data-stu-id="852e6-254">Value</span></span> |
|------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="852e6-255">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="852e6-255">Link-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="852e6-256">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="852e6-256">MAPI-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="852e6-257">System-Only</span><span class="sxs-lookup"><span data-stu-id="852e6-257">System-Only</span></span>            | <span data-ttu-id="852e6-258">Falso</span><span class="sxs-lookup"><span data-stu-id="852e6-258">False</span></span>                                                                 |
| <span data-ttu-id="852e6-259">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="852e6-259">Is-Single-Valued</span></span>       | <span data-ttu-id="852e6-260">Vero</span><span class="sxs-lookup"><span data-stu-id="852e6-260">True</span></span>                                                                  |
| <span data-ttu-id="852e6-261">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="852e6-261">Is Indexed</span></span>             | <span data-ttu-id="852e6-262">Falso</span><span class="sxs-lookup"><span data-stu-id="852e6-262">False</span></span>                                                                 |
| <span data-ttu-id="852e6-263">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="852e6-263">In Global Catalog</span></span>      | <span data-ttu-id="852e6-264">Falso</span><span class="sxs-lookup"><span data-stu-id="852e6-264">False</span></span>                                                                 |
| <span data-ttu-id="852e6-265">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="852e6-265">NT-Security-Descriptor</span></span> | <span data-ttu-id="852e6-266">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="852e6-266">O:BAG:BAD:S:</span></span>                                                          |
| <span data-ttu-id="852e6-267">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="852e6-267">Range-Lower</span></span>            | \-                                                                    |
| <span data-ttu-id="852e6-268">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="852e6-268">Range-Upper</span></span>            | \-                                                                    |
| <span data-ttu-id="852e6-269">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="852e6-269">Search-Flags</span></span>           | <span data-ttu-id="852e6-270">0x00000000</span><span class="sxs-lookup"><span data-stu-id="852e6-270">0x00000000</span></span>                                                            |
| <span data-ttu-id="852e6-271">System-Flags</span><span class="sxs-lookup"><span data-stu-id="852e6-271">System-Flags</span></span>           | <span data-ttu-id="852e6-272">0x00000010</span><span class="sxs-lookup"><span data-stu-id="852e6-272">0x00000010</span></span>                                                            |
| <span data-ttu-id="852e6-273">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="852e6-273">Classes used in</span></span>        | [<span data-ttu-id="852e6-274">**Group**</span><span class="sxs-lookup"><span data-stu-id="852e6-274">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="852e6-275">**Utente**</span><span class="sxs-lookup"><span data-stu-id="852e6-275">**User**</span></span>](c-user.md)<br/> |



 

 





