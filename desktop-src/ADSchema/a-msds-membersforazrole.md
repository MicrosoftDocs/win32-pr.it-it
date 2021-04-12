---
title: attributo ms-DS-members-for-AZ-Role
description: Elenco di utenti o gruppi di applicazioni membro collegati a AZ-Role.
ms.assetid: c1234443-fd25-4ed8-a8ee-9853810ebe7d
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo ms-DS-members-for-AZ-Role
- attributo msDS-MembersForAzRole-schema AD
topic_type:
- apiref
api_name:
- ms-DS-Members-For-Az-Role
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b19203e5c44d0389e64531867444d1bb2865196
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104480376"
---
# <a name="ms-ds-members-for-az-role-attribute"></a><span data-ttu-id="74450-105">attributo ms-DS-members-for-AZ-Role</span><span class="sxs-lookup"><span data-stu-id="74450-105">ms-DS-Members-For-Az-Role attribute</span></span>

<span data-ttu-id="74450-106">Elenco di utenti o gruppi di applicazioni membro collegati a AZ-Role.</span><span class="sxs-lookup"><span data-stu-id="74450-106">List of member application groups or users linked to Az-Role.</span></span>



| <span data-ttu-id="74450-107">Voce</span><span class="sxs-lookup"><span data-stu-id="74450-107">Entry</span></span> | <span data-ttu-id="74450-108">Valore</span><span class="sxs-lookup"><span data-stu-id="74450-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="74450-109">CN</span><span class="sxs-lookup"><span data-stu-id="74450-109">CN</span></span>                | <span data-ttu-id="74450-110">ms-DS-members-for-AZ-Role</span><span class="sxs-lookup"><span data-stu-id="74450-110">ms-DS-Members-For-Az-Role</span></span>               |
| <span data-ttu-id="74450-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="74450-111">Ldap-Display-Name</span></span> | <span data-ttu-id="74450-112">msDS-MembersForAzRole</span><span class="sxs-lookup"><span data-stu-id="74450-112">msDS-MembersForAzRole</span></span>                   |
| <span data-ttu-id="74450-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="74450-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="74450-114">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="74450-114">Update Privilege</span></span>  | <span data-ttu-id="74450-115">Amministratore di AzRoles</span><span class="sxs-lookup"><span data-stu-id="74450-115">AzRoles admin</span></span>                           |
| <span data-ttu-id="74450-116">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="74450-116">Update Frequency</span></span>  | <span data-ttu-id="74450-117">Durante l'inizializzazione o la modifica dei criteri.</span><span class="sxs-lookup"><span data-stu-id="74450-117">During initialization or policy change.</span></span> |
| <span data-ttu-id="74450-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="74450-118">Attribute-Id</span></span>      | <span data-ttu-id="74450-119">1.2.840.113556.1.4.1806</span><span class="sxs-lookup"><span data-stu-id="74450-119">1.2.840.113556.1.4.1806</span></span>                 |
| <span data-ttu-id="74450-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="74450-120">System-Id-Guid</span></span>    | <span data-ttu-id="74450-121">cbf7e6cd-85a4-4314-8939-8bfe80597835</span><span class="sxs-lookup"><span data-stu-id="74450-121">cbf7e6cd-85a4-4314-8939-8bfe80597835</span></span>    |
| <span data-ttu-id="74450-122">Sintassi</span><span class="sxs-lookup"><span data-stu-id="74450-122">Syntax</span></span>            | [<span data-ttu-id="74450-123">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="74450-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="74450-124">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="74450-124">Implementations</span></span>

-   [<span data-ttu-id="74450-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="74450-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="74450-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="74450-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="74450-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="74450-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="74450-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="74450-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="74450-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="74450-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="74450-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="74450-130">Windows Server 2003</span></span>



| <span data-ttu-id="74450-131">Voce</span><span class="sxs-lookup"><span data-stu-id="74450-131">Entry</span></span> | <span data-ttu-id="74450-132">Valore</span><span class="sxs-lookup"><span data-stu-id="74450-132">Value</span></span> |
|------------------------|---------------------------------------------------|
| <span data-ttu-id="74450-133">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="74450-133">Link-Id</span></span>                | <span data-ttu-id="74450-134">2016</span><span class="sxs-lookup"><span data-stu-id="74450-134">2016</span></span>                                              |
| <span data-ttu-id="74450-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="74450-135">MAPI-Id</span></span>                | \-                                                |
| <span data-ttu-id="74450-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="74450-136">System-Only</span></span>            | <span data-ttu-id="74450-137">Falso</span><span class="sxs-lookup"><span data-stu-id="74450-137">False</span></span>                                             |
| <span data-ttu-id="74450-138">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="74450-138">Is-Single-Valued</span></span>       | <span data-ttu-id="74450-139">Falso</span><span class="sxs-lookup"><span data-stu-id="74450-139">False</span></span>                                             |
| <span data-ttu-id="74450-140">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="74450-140">Is Indexed</span></span>             | <span data-ttu-id="74450-141">Falso</span><span class="sxs-lookup"><span data-stu-id="74450-141">False</span></span>                                             |
| <span data-ttu-id="74450-142">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="74450-142">In Global Catalog</span></span>      | <span data-ttu-id="74450-143">Falso</span><span class="sxs-lookup"><span data-stu-id="74450-143">False</span></span>                                             |
| <span data-ttu-id="74450-144">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="74450-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="74450-145">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="74450-145">O:BAG:BAD:S:</span></span>                                      |
| <span data-ttu-id="74450-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="74450-146">Range-Lower</span></span>            | \-                                                |
| <span data-ttu-id="74450-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="74450-147">Range-Upper</span></span>            | \-                                                |
| <span data-ttu-id="74450-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="74450-148">Search-Flags</span></span>           | <span data-ttu-id="74450-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="74450-149">0x00000000</span></span>                                        |
| <span data-ttu-id="74450-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="74450-150">System-Flags</span></span>           | <span data-ttu-id="74450-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="74450-151">0x00000010</span></span>                                        |
| <span data-ttu-id="74450-152">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="74450-152">Classes used in</span></span>        | [<span data-ttu-id="74450-153">**ms-DS-AZ-Role**</span><span class="sxs-lookup"><span data-stu-id="74450-153">**ms-DS-Az-Role**</span></span>](c-msds-azrole.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="74450-154">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="74450-154">Windows Server 2003 R2</span></span>



| <span data-ttu-id="74450-155">Voce</span><span class="sxs-lookup"><span data-stu-id="74450-155">Entry</span></span> | <span data-ttu-id="74450-156">Valore</span><span class="sxs-lookup"><span data-stu-id="74450-156">Value</span></span> |
|------------------------|---------------------------------------------------|
| <span data-ttu-id="74450-157">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="74450-157">Link-Id</span></span>                | <span data-ttu-id="74450-158">2016</span><span class="sxs-lookup"><span data-stu-id="74450-158">2016</span></span>                                              |
| <span data-ttu-id="74450-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="74450-159">MAPI-Id</span></span>                | \-                                                |
| <span data-ttu-id="74450-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="74450-160">System-Only</span></span>            | <span data-ttu-id="74450-161">Falso</span><span class="sxs-lookup"><span data-stu-id="74450-161">False</span></span>                                             |
| <span data-ttu-id="74450-162">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="74450-162">Is-Single-Valued</span></span>       | <span data-ttu-id="74450-163">Falso</span><span class="sxs-lookup"><span data-stu-id="74450-163">False</span></span>                                             |
| <span data-ttu-id="74450-164">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="74450-164">Is Indexed</span></span>             | <span data-ttu-id="74450-165">Falso</span><span class="sxs-lookup"><span data-stu-id="74450-165">False</span></span>                                             |
| <span data-ttu-id="74450-166">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="74450-166">In Global Catalog</span></span>      | <span data-ttu-id="74450-167">Falso</span><span class="sxs-lookup"><span data-stu-id="74450-167">False</span></span>                                             |
| <span data-ttu-id="74450-168">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="74450-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="74450-169">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="74450-169">O:BAG:BAD:S:</span></span>                                      |
| <span data-ttu-id="74450-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="74450-170">Range-Lower</span></span>            | \-                                                |
| <span data-ttu-id="74450-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="74450-171">Range-Upper</span></span>            | \-                                                |
| <span data-ttu-id="74450-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="74450-172">Search-Flags</span></span>           | <span data-ttu-id="74450-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="74450-173">0x00000000</span></span>                                        |
| <span data-ttu-id="74450-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="74450-174">System-Flags</span></span>           | <span data-ttu-id="74450-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="74450-175">0x00000010</span></span>                                        |
| <span data-ttu-id="74450-176">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="74450-176">Classes used in</span></span>        | [<span data-ttu-id="74450-177">**ms-DS-AZ-Role**</span><span class="sxs-lookup"><span data-stu-id="74450-177">**ms-DS-Az-Role**</span></span>](c-msds-azrole.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="74450-178">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="74450-178">Windows Server 2008</span></span>



| <span data-ttu-id="74450-179">Voce</span><span class="sxs-lookup"><span data-stu-id="74450-179">Entry</span></span> | <span data-ttu-id="74450-180">Valore</span><span class="sxs-lookup"><span data-stu-id="74450-180">Value</span></span> |
|------------------------|---------------------------------------------------|
| <span data-ttu-id="74450-181">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="74450-181">Link-Id</span></span>                | <span data-ttu-id="74450-182">2016</span><span class="sxs-lookup"><span data-stu-id="74450-182">2016</span></span>                                              |
| <span data-ttu-id="74450-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="74450-183">MAPI-Id</span></span>                | \-                                                |
| <span data-ttu-id="74450-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="74450-184">System-Only</span></span>            | <span data-ttu-id="74450-185">Falso</span><span class="sxs-lookup"><span data-stu-id="74450-185">False</span></span>                                             |
| <span data-ttu-id="74450-186">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="74450-186">Is-Single-Valued</span></span>       | <span data-ttu-id="74450-187">Falso</span><span class="sxs-lookup"><span data-stu-id="74450-187">False</span></span>                                             |
| <span data-ttu-id="74450-188">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="74450-188">Is Indexed</span></span>             | <span data-ttu-id="74450-189">Falso</span><span class="sxs-lookup"><span data-stu-id="74450-189">False</span></span>                                             |
| <span data-ttu-id="74450-190">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="74450-190">In Global Catalog</span></span>      | <span data-ttu-id="74450-191">Falso</span><span class="sxs-lookup"><span data-stu-id="74450-191">False</span></span>                                             |
| <span data-ttu-id="74450-192">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="74450-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="74450-193">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="74450-193">O:BAG:BAD:S:</span></span>                                      |
| <span data-ttu-id="74450-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="74450-194">Range-Lower</span></span>            | \-                                                |
| <span data-ttu-id="74450-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="74450-195">Range-Upper</span></span>            | \-                                                |
| <span data-ttu-id="74450-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="74450-196">Search-Flags</span></span>           | <span data-ttu-id="74450-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="74450-197">0x00000000</span></span>                                        |
| <span data-ttu-id="74450-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="74450-198">System-Flags</span></span>           | <span data-ttu-id="74450-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="74450-199">0x00000010</span></span>                                        |
| <span data-ttu-id="74450-200">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="74450-200">Classes used in</span></span>        | [<span data-ttu-id="74450-201">**ms-DS-AZ-Role**</span><span class="sxs-lookup"><span data-stu-id="74450-201">**ms-DS-Az-Role**</span></span>](c-msds-azrole.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="74450-202">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="74450-202">Windows Server 2008 R2</span></span>



| <span data-ttu-id="74450-203">Voce</span><span class="sxs-lookup"><span data-stu-id="74450-203">Entry</span></span> | <span data-ttu-id="74450-204">Valore</span><span class="sxs-lookup"><span data-stu-id="74450-204">Value</span></span> |
|------------------------|---------------------------------------------------|
| <span data-ttu-id="74450-205">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="74450-205">Link-Id</span></span>                | <span data-ttu-id="74450-206">2016</span><span class="sxs-lookup"><span data-stu-id="74450-206">2016</span></span>                                              |
| <span data-ttu-id="74450-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="74450-207">MAPI-Id</span></span>                | \-                                                |
| <span data-ttu-id="74450-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="74450-208">System-Only</span></span>            | <span data-ttu-id="74450-209">Falso</span><span class="sxs-lookup"><span data-stu-id="74450-209">False</span></span>                                             |
| <span data-ttu-id="74450-210">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="74450-210">Is-Single-Valued</span></span>       | <span data-ttu-id="74450-211">Falso</span><span class="sxs-lookup"><span data-stu-id="74450-211">False</span></span>                                             |
| <span data-ttu-id="74450-212">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="74450-212">Is Indexed</span></span>             | <span data-ttu-id="74450-213">Falso</span><span class="sxs-lookup"><span data-stu-id="74450-213">False</span></span>                                             |
| <span data-ttu-id="74450-214">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="74450-214">In Global Catalog</span></span>      | <span data-ttu-id="74450-215">Falso</span><span class="sxs-lookup"><span data-stu-id="74450-215">False</span></span>                                             |
| <span data-ttu-id="74450-216">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="74450-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="74450-217">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="74450-217">O:BAG:BAD:S:</span></span>                                      |
| <span data-ttu-id="74450-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="74450-218">Range-Lower</span></span>            | \-                                                |
| <span data-ttu-id="74450-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="74450-219">Range-Upper</span></span>            | \-                                                |
| <span data-ttu-id="74450-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="74450-220">Search-Flags</span></span>           | <span data-ttu-id="74450-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="74450-221">0x00000000</span></span>                                        |
| <span data-ttu-id="74450-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="74450-222">System-Flags</span></span>           | <span data-ttu-id="74450-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="74450-223">0x00000010</span></span>                                        |
| <span data-ttu-id="74450-224">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="74450-224">Classes used in</span></span>        | [<span data-ttu-id="74450-225">**ms-DS-AZ-Role**</span><span class="sxs-lookup"><span data-stu-id="74450-225">**ms-DS-Az-Role**</span></span>](c-msds-azrole.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="74450-226">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="74450-226">Windows Server 2012</span></span>



| <span data-ttu-id="74450-227">Voce</span><span class="sxs-lookup"><span data-stu-id="74450-227">Entry</span></span> | <span data-ttu-id="74450-228">Valore</span><span class="sxs-lookup"><span data-stu-id="74450-228">Value</span></span> |
|------------------------|---------------------------------------------------|
| <span data-ttu-id="74450-229">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="74450-229">Link-Id</span></span>                | <span data-ttu-id="74450-230">2016</span><span class="sxs-lookup"><span data-stu-id="74450-230">2016</span></span>                                              |
| <span data-ttu-id="74450-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="74450-231">MAPI-Id</span></span>                | \-                                                |
| <span data-ttu-id="74450-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="74450-232">System-Only</span></span>            | <span data-ttu-id="74450-233">Falso</span><span class="sxs-lookup"><span data-stu-id="74450-233">False</span></span>                                             |
| <span data-ttu-id="74450-234">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="74450-234">Is-Single-Valued</span></span>       | <span data-ttu-id="74450-235">Falso</span><span class="sxs-lookup"><span data-stu-id="74450-235">False</span></span>                                             |
| <span data-ttu-id="74450-236">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="74450-236">Is Indexed</span></span>             | <span data-ttu-id="74450-237">Falso</span><span class="sxs-lookup"><span data-stu-id="74450-237">False</span></span>                                             |
| <span data-ttu-id="74450-238">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="74450-238">In Global Catalog</span></span>      | <span data-ttu-id="74450-239">Falso</span><span class="sxs-lookup"><span data-stu-id="74450-239">False</span></span>                                             |
| <span data-ttu-id="74450-240">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="74450-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="74450-241">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="74450-241">O:BAG:BAD:S:</span></span>                                      |
| <span data-ttu-id="74450-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="74450-242">Range-Lower</span></span>            | \-                                                |
| <span data-ttu-id="74450-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="74450-243">Range-Upper</span></span>            | \-                                                |
| <span data-ttu-id="74450-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="74450-244">Search-Flags</span></span>           | <span data-ttu-id="74450-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="74450-245">0x00000000</span></span>                                        |
| <span data-ttu-id="74450-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="74450-246">System-Flags</span></span>           | <span data-ttu-id="74450-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="74450-247">0x00000010</span></span>                                        |
| <span data-ttu-id="74450-248">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="74450-248">Classes used in</span></span>        | [<span data-ttu-id="74450-249">**ms-DS-AZ-Role**</span><span class="sxs-lookup"><span data-stu-id="74450-249">**ms-DS-Az-Role**</span></span>](c-msds-azrole.md)<br/> |



 

 





