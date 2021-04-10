---
title: Attributo LDAP-IPDeny-List
description: Include un elenco di indirizzi IP binari a cui viene negato l'accesso a un server LDAP.
ms.assetid: 7d554d49-8934-4d71-b32f-8e59c22faf8c
ms.tgt_platform: multiple
keywords:
- LDAP-IPDeny-list-schema AD attributo
- Schema AD dell'attributo lDAPIPDenyList
topic_type:
- apiref
api_name:
- LDAP-IPDeny-List
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43246b5bb5786eefafc8598e9d729d9a2f308e08
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104122589"
---
# <a name="ldap-ipdeny-list-attribute"></a><span data-ttu-id="e3c39-105">Attributo LDAP-IPDeny-List</span><span class="sxs-lookup"><span data-stu-id="e3c39-105">LDAP-IPDeny-List attribute</span></span>

<span data-ttu-id="e3c39-106">Include un elenco di indirizzi IP binari a cui viene negato l'accesso a un server LDAP.</span><span class="sxs-lookup"><span data-stu-id="e3c39-106">Holds a list of binary IP addresses that are denied access to an LDAP server.</span></span>



| <span data-ttu-id="e3c39-107">Voce</span><span class="sxs-lookup"><span data-stu-id="e3c39-107">Entry</span></span> | <span data-ttu-id="e3c39-108">Valore</span><span class="sxs-lookup"><span data-stu-id="e3c39-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="e3c39-109">CN</span><span class="sxs-lookup"><span data-stu-id="e3c39-109">CN</span></span>                | <span data-ttu-id="e3c39-110">LDAP-IPDeny-List</span><span class="sxs-lookup"><span data-stu-id="e3c39-110">LDAP-IPDeny-List</span></span>                                      |
| <span data-ttu-id="e3c39-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="e3c39-111">Ldap-Display-Name</span></span> | <span data-ttu-id="e3c39-112">lDAPIPDenyList</span><span class="sxs-lookup"><span data-stu-id="e3c39-112">lDAPIPDenyList</span></span>                                        |
| <span data-ttu-id="e3c39-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="e3c39-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="e3c39-114">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="e3c39-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="e3c39-115">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="e3c39-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="e3c39-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e3c39-116">Attribute-Id</span></span>      | <span data-ttu-id="e3c39-117">1.2.840.113556.1.4.844</span><span class="sxs-lookup"><span data-stu-id="e3c39-117">1.2.840.113556.1.4.844</span></span>                                |
| <span data-ttu-id="e3c39-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="e3c39-118">System-Id-Guid</span></span>    | <span data-ttu-id="e3c39-119">7359a353-90f7-11d1-aebc-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="e3c39-119">7359a353-90f7-11d1-aebc-0000f80367c1</span></span>                  |
| <span data-ttu-id="e3c39-120">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e3c39-120">Syntax</span></span>            | [<span data-ttu-id="e3c39-121">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="e3c39-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="e3c39-122">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="e3c39-122">Implementations</span></span>

-   [<span data-ttu-id="e3c39-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="e3c39-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="e3c39-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e3c39-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e3c39-125">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="e3c39-125">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="e3c39-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e3c39-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e3c39-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e3c39-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e3c39-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e3c39-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e3c39-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e3c39-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="e3c39-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e3c39-130">Windows 2000 Server</span></span>



| <span data-ttu-id="e3c39-131">Voce</span><span class="sxs-lookup"><span data-stu-id="e3c39-131">Entry</span></span> | <span data-ttu-id="e3c39-132">Valore</span><span class="sxs-lookup"><span data-stu-id="e3c39-132">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="e3c39-133">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="e3c39-133">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="e3c39-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e3c39-134">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="e3c39-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="e3c39-135">System-Only</span></span>            | <span data-ttu-id="e3c39-136">Falso</span><span class="sxs-lookup"><span data-stu-id="e3c39-136">False</span></span>                                            |
| <span data-ttu-id="e3c39-137">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="e3c39-137">Is-Single-Valued</span></span>       | <span data-ttu-id="e3c39-138">Falso</span><span class="sxs-lookup"><span data-stu-id="e3c39-138">False</span></span>                                            |
| <span data-ttu-id="e3c39-139">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="e3c39-139">Is Indexed</span></span>             | <span data-ttu-id="e3c39-140">Falso</span><span class="sxs-lookup"><span data-stu-id="e3c39-140">False</span></span>                                            |
| <span data-ttu-id="e3c39-141">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="e3c39-141">In Global Catalog</span></span>      | <span data-ttu-id="e3c39-142">Falso</span><span class="sxs-lookup"><span data-stu-id="e3c39-142">False</span></span>                                            |
| <span data-ttu-id="e3c39-143">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="e3c39-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="e3c39-144">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="e3c39-144">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="e3c39-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e3c39-145">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="e3c39-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e3c39-146">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="e3c39-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e3c39-147">Search-Flags</span></span>           | <span data-ttu-id="e3c39-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e3c39-148">0x00000000</span></span>                                       |
| <span data-ttu-id="e3c39-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e3c39-149">System-Flags</span></span>           | <span data-ttu-id="e3c39-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e3c39-150">0x00000010</span></span>                                       |
| <span data-ttu-id="e3c39-151">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="e3c39-151">Classes used in</span></span>        | [<span data-ttu-id="e3c39-152">**Query-criteri**</span><span class="sxs-lookup"><span data-stu-id="e3c39-152">**Query-Policy**</span></span>](c-querypolicy.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="e3c39-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e3c39-153">Windows Server 2003</span></span>



| <span data-ttu-id="e3c39-154">Voce</span><span class="sxs-lookup"><span data-stu-id="e3c39-154">Entry</span></span> | <span data-ttu-id="e3c39-155">Valore</span><span class="sxs-lookup"><span data-stu-id="e3c39-155">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="e3c39-156">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="e3c39-156">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="e3c39-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e3c39-157">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="e3c39-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="e3c39-158">System-Only</span></span>            | <span data-ttu-id="e3c39-159">Falso</span><span class="sxs-lookup"><span data-stu-id="e3c39-159">False</span></span>                                            |
| <span data-ttu-id="e3c39-160">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="e3c39-160">Is-Single-Valued</span></span>       | <span data-ttu-id="e3c39-161">Falso</span><span class="sxs-lookup"><span data-stu-id="e3c39-161">False</span></span>                                            |
| <span data-ttu-id="e3c39-162">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="e3c39-162">Is Indexed</span></span>             | <span data-ttu-id="e3c39-163">Falso</span><span class="sxs-lookup"><span data-stu-id="e3c39-163">False</span></span>                                            |
| <span data-ttu-id="e3c39-164">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="e3c39-164">In Global Catalog</span></span>      | <span data-ttu-id="e3c39-165">Falso</span><span class="sxs-lookup"><span data-stu-id="e3c39-165">False</span></span>                                            |
| <span data-ttu-id="e3c39-166">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="e3c39-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="e3c39-167">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="e3c39-167">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="e3c39-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e3c39-168">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="e3c39-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e3c39-169">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="e3c39-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e3c39-170">Search-Flags</span></span>           | <span data-ttu-id="e3c39-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e3c39-171">0x00000000</span></span>                                       |
| <span data-ttu-id="e3c39-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e3c39-172">System-Flags</span></span>           | <span data-ttu-id="e3c39-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e3c39-173">0x00000010</span></span>                                       |
| <span data-ttu-id="e3c39-174">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="e3c39-174">Classes used in</span></span>        | [<span data-ttu-id="e3c39-175">**Query-criteri**</span><span class="sxs-lookup"><span data-stu-id="e3c39-175">**Query-Policy**</span></span>](c-querypolicy.md)<br/> |



## <a name="adam"></a><span data-ttu-id="e3c39-176">ADAM</span><span class="sxs-lookup"><span data-stu-id="e3c39-176">ADAM</span></span>



| <span data-ttu-id="e3c39-177">Voce</span><span class="sxs-lookup"><span data-stu-id="e3c39-177">Entry</span></span> | <span data-ttu-id="e3c39-178">Valore</span><span class="sxs-lookup"><span data-stu-id="e3c39-178">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="e3c39-179">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="e3c39-179">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="e3c39-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e3c39-180">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="e3c39-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="e3c39-181">System-Only</span></span>            | <span data-ttu-id="e3c39-182">Falso</span><span class="sxs-lookup"><span data-stu-id="e3c39-182">False</span></span>                                            |
| <span data-ttu-id="e3c39-183">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="e3c39-183">Is-Single-Valued</span></span>       | <span data-ttu-id="e3c39-184">Falso</span><span class="sxs-lookup"><span data-stu-id="e3c39-184">False</span></span>                                            |
| <span data-ttu-id="e3c39-185">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="e3c39-185">Is Indexed</span></span>             | <span data-ttu-id="e3c39-186">Falso</span><span class="sxs-lookup"><span data-stu-id="e3c39-186">False</span></span>                                            |
| <span data-ttu-id="e3c39-187">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="e3c39-187">In Global Catalog</span></span>      | <span data-ttu-id="e3c39-188">Falso</span><span class="sxs-lookup"><span data-stu-id="e3c39-188">False</span></span>                                            |
| <span data-ttu-id="e3c39-189">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="e3c39-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="e3c39-190">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="e3c39-190">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="e3c39-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e3c39-191">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="e3c39-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e3c39-192">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="e3c39-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e3c39-193">Search-Flags</span></span>           | <span data-ttu-id="e3c39-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e3c39-194">0x00000000</span></span>                                       |
| <span data-ttu-id="e3c39-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e3c39-195">System-Flags</span></span>           | <span data-ttu-id="e3c39-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e3c39-196">0x00000010</span></span>                                       |
| <span data-ttu-id="e3c39-197">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="e3c39-197">Classes used in</span></span>        | [<span data-ttu-id="e3c39-198">**Query-criteri**</span><span class="sxs-lookup"><span data-stu-id="e3c39-198">**Query-Policy**</span></span>](c-querypolicy.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e3c39-199">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e3c39-199">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e3c39-200">Voce</span><span class="sxs-lookup"><span data-stu-id="e3c39-200">Entry</span></span> | <span data-ttu-id="e3c39-201">Valore</span><span class="sxs-lookup"><span data-stu-id="e3c39-201">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="e3c39-202">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="e3c39-202">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="e3c39-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e3c39-203">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="e3c39-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="e3c39-204">System-Only</span></span>            | <span data-ttu-id="e3c39-205">Falso</span><span class="sxs-lookup"><span data-stu-id="e3c39-205">False</span></span>                                            |
| <span data-ttu-id="e3c39-206">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="e3c39-206">Is-Single-Valued</span></span>       | <span data-ttu-id="e3c39-207">Falso</span><span class="sxs-lookup"><span data-stu-id="e3c39-207">False</span></span>                                            |
| <span data-ttu-id="e3c39-208">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="e3c39-208">Is Indexed</span></span>             | <span data-ttu-id="e3c39-209">Falso</span><span class="sxs-lookup"><span data-stu-id="e3c39-209">False</span></span>                                            |
| <span data-ttu-id="e3c39-210">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="e3c39-210">In Global Catalog</span></span>      | <span data-ttu-id="e3c39-211">Falso</span><span class="sxs-lookup"><span data-stu-id="e3c39-211">False</span></span>                                            |
| <span data-ttu-id="e3c39-212">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="e3c39-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="e3c39-213">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="e3c39-213">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="e3c39-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e3c39-214">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="e3c39-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e3c39-215">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="e3c39-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e3c39-216">Search-Flags</span></span>           | <span data-ttu-id="e3c39-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e3c39-217">0x00000000</span></span>                                       |
| <span data-ttu-id="e3c39-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e3c39-218">System-Flags</span></span>           | <span data-ttu-id="e3c39-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e3c39-219">0x00000010</span></span>                                       |
| <span data-ttu-id="e3c39-220">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="e3c39-220">Classes used in</span></span>        | [<span data-ttu-id="e3c39-221">**Query-criteri**</span><span class="sxs-lookup"><span data-stu-id="e3c39-221">**Query-Policy**</span></span>](c-querypolicy.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="e3c39-222">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e3c39-222">Windows Server 2008</span></span>



| <span data-ttu-id="e3c39-223">Voce</span><span class="sxs-lookup"><span data-stu-id="e3c39-223">Entry</span></span> | <span data-ttu-id="e3c39-224">Valore</span><span class="sxs-lookup"><span data-stu-id="e3c39-224">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="e3c39-225">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="e3c39-225">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="e3c39-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e3c39-226">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="e3c39-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="e3c39-227">System-Only</span></span>            | <span data-ttu-id="e3c39-228">Falso</span><span class="sxs-lookup"><span data-stu-id="e3c39-228">False</span></span>                                            |
| <span data-ttu-id="e3c39-229">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="e3c39-229">Is-Single-Valued</span></span>       | <span data-ttu-id="e3c39-230">Falso</span><span class="sxs-lookup"><span data-stu-id="e3c39-230">False</span></span>                                            |
| <span data-ttu-id="e3c39-231">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="e3c39-231">Is Indexed</span></span>             | <span data-ttu-id="e3c39-232">Falso</span><span class="sxs-lookup"><span data-stu-id="e3c39-232">False</span></span>                                            |
| <span data-ttu-id="e3c39-233">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="e3c39-233">In Global Catalog</span></span>      | <span data-ttu-id="e3c39-234">Falso</span><span class="sxs-lookup"><span data-stu-id="e3c39-234">False</span></span>                                            |
| <span data-ttu-id="e3c39-235">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="e3c39-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="e3c39-236">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="e3c39-236">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="e3c39-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e3c39-237">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="e3c39-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e3c39-238">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="e3c39-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e3c39-239">Search-Flags</span></span>           | <span data-ttu-id="e3c39-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e3c39-240">0x00000000</span></span>                                       |
| <span data-ttu-id="e3c39-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e3c39-241">System-Flags</span></span>           | <span data-ttu-id="e3c39-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e3c39-242">0x00000010</span></span>                                       |
| <span data-ttu-id="e3c39-243">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="e3c39-243">Classes used in</span></span>        | [<span data-ttu-id="e3c39-244">**Query-criteri**</span><span class="sxs-lookup"><span data-stu-id="e3c39-244">**Query-Policy**</span></span>](c-querypolicy.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e3c39-245">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e3c39-245">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e3c39-246">Voce</span><span class="sxs-lookup"><span data-stu-id="e3c39-246">Entry</span></span> | <span data-ttu-id="e3c39-247">Valore</span><span class="sxs-lookup"><span data-stu-id="e3c39-247">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="e3c39-248">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="e3c39-248">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="e3c39-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e3c39-249">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="e3c39-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="e3c39-250">System-Only</span></span>            | <span data-ttu-id="e3c39-251">Falso</span><span class="sxs-lookup"><span data-stu-id="e3c39-251">False</span></span>                                            |
| <span data-ttu-id="e3c39-252">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="e3c39-252">Is-Single-Valued</span></span>       | <span data-ttu-id="e3c39-253">Falso</span><span class="sxs-lookup"><span data-stu-id="e3c39-253">False</span></span>                                            |
| <span data-ttu-id="e3c39-254">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="e3c39-254">Is Indexed</span></span>             | <span data-ttu-id="e3c39-255">Falso</span><span class="sxs-lookup"><span data-stu-id="e3c39-255">False</span></span>                                            |
| <span data-ttu-id="e3c39-256">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="e3c39-256">In Global Catalog</span></span>      | <span data-ttu-id="e3c39-257">Falso</span><span class="sxs-lookup"><span data-stu-id="e3c39-257">False</span></span>                                            |
| <span data-ttu-id="e3c39-258">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="e3c39-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="e3c39-259">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="e3c39-259">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="e3c39-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e3c39-260">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="e3c39-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e3c39-261">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="e3c39-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e3c39-262">Search-Flags</span></span>           | <span data-ttu-id="e3c39-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e3c39-263">0x00000000</span></span>                                       |
| <span data-ttu-id="e3c39-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e3c39-264">System-Flags</span></span>           | <span data-ttu-id="e3c39-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e3c39-265">0x00000010</span></span>                                       |
| <span data-ttu-id="e3c39-266">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="e3c39-266">Classes used in</span></span>        | [<span data-ttu-id="e3c39-267">**Query-criteri**</span><span class="sxs-lookup"><span data-stu-id="e3c39-267">**Query-Policy**</span></span>](c-querypolicy.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e3c39-268">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e3c39-268">Windows Server 2012</span></span>



| <span data-ttu-id="e3c39-269">Voce</span><span class="sxs-lookup"><span data-stu-id="e3c39-269">Entry</span></span> | <span data-ttu-id="e3c39-270">Valore</span><span class="sxs-lookup"><span data-stu-id="e3c39-270">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="e3c39-271">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="e3c39-271">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="e3c39-272">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e3c39-272">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="e3c39-273">System-Only</span><span class="sxs-lookup"><span data-stu-id="e3c39-273">System-Only</span></span>            | <span data-ttu-id="e3c39-274">Falso</span><span class="sxs-lookup"><span data-stu-id="e3c39-274">False</span></span>                                            |
| <span data-ttu-id="e3c39-275">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="e3c39-275">Is-Single-Valued</span></span>       | <span data-ttu-id="e3c39-276">Falso</span><span class="sxs-lookup"><span data-stu-id="e3c39-276">False</span></span>                                            |
| <span data-ttu-id="e3c39-277">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="e3c39-277">Is Indexed</span></span>             | <span data-ttu-id="e3c39-278">Falso</span><span class="sxs-lookup"><span data-stu-id="e3c39-278">False</span></span>                                            |
| <span data-ttu-id="e3c39-279">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="e3c39-279">In Global Catalog</span></span>      | <span data-ttu-id="e3c39-280">Falso</span><span class="sxs-lookup"><span data-stu-id="e3c39-280">False</span></span>                                            |
| <span data-ttu-id="e3c39-281">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="e3c39-281">NT-Security-Descriptor</span></span> | <span data-ttu-id="e3c39-282">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="e3c39-282">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="e3c39-283">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e3c39-283">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="e3c39-284">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e3c39-284">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="e3c39-285">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e3c39-285">Search-Flags</span></span>           | <span data-ttu-id="e3c39-286">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e3c39-286">0x00000000</span></span>                                       |
| <span data-ttu-id="e3c39-287">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e3c39-287">System-Flags</span></span>           | <span data-ttu-id="e3c39-288">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e3c39-288">0x00000010</span></span>                                       |
| <span data-ttu-id="e3c39-289">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="e3c39-289">Classes used in</span></span>        | [<span data-ttu-id="e3c39-290">**Query-criteri**</span><span class="sxs-lookup"><span data-stu-id="e3c39-290">**Query-Policy**</span></span>](c-querypolicy.md)<br/> |



 

 





