---
title: attributo ms-DS-non membri
description: Questo attributo ha lo stesso scopo dell'attributo non di sicurezza-membro, ma con le regole di ambito applicate.
ms.assetid: 11d3d030-3643-4ed2-a52e-a57f32e9597f
ms.tgt_platform: multiple
keywords:
- attributo ms-DS-non membri-schema AD
- attributo msDS-Nonmembers-schema AD
topic_type:
- apiref
api_name:
- ms-DS-Non-Members
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca8ca19af90f2f534f974863aa7d766f6be4624b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103875381"
---
# <a name="ms-ds-non-members-attribute"></a><span data-ttu-id="ae9c4-105">attributo ms-DS-non membri</span><span class="sxs-lookup"><span data-stu-id="ae9c4-105">ms-DS-Non-Members attribute</span></span>

<span data-ttu-id="ae9c4-106">Questo attributo ha lo stesso scopo dell'attributo non di sicurezza-membro, ma con le regole di ambito applicate.</span><span class="sxs-lookup"><span data-stu-id="ae9c4-106">This attribute serves the same purpose as the Non-Security-Member attribute but with scoping rules applied.</span></span>



| <span data-ttu-id="ae9c4-107">Voce</span><span class="sxs-lookup"><span data-stu-id="ae9c4-107">Entry</span></span> | <span data-ttu-id="ae9c4-108">Valore</span><span class="sxs-lookup"><span data-stu-id="ae9c4-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="ae9c4-109">CN</span><span class="sxs-lookup"><span data-stu-id="ae9c4-109">CN</span></span>                | <span data-ttu-id="ae9c4-110">ms-DS-non membri</span><span class="sxs-lookup"><span data-stu-id="ae9c4-110">ms-DS-Non-Members</span></span>                       |
| <span data-ttu-id="ae9c4-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="ae9c4-111">Ldap-Display-Name</span></span> | <span data-ttu-id="ae9c4-112">msDS-non membri</span><span class="sxs-lookup"><span data-stu-id="ae9c4-112">msDS-NonMembers</span></span>                         |
| <span data-ttu-id="ae9c4-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="ae9c4-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="ae9c4-114">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="ae9c4-114">Update Privilege</span></span>  | <span data-ttu-id="ae9c4-115">Amministratore di AzRoles</span><span class="sxs-lookup"><span data-stu-id="ae9c4-115">AzRoles Admin</span></span>                           |
| <span data-ttu-id="ae9c4-116">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="ae9c4-116">Update Frequency</span></span>  | <span data-ttu-id="ae9c4-117">Durante l'inizializzazione e la modifica dei criteri.</span><span class="sxs-lookup"><span data-stu-id="ae9c4-117">At initialization and policy change.</span></span>    |
| <span data-ttu-id="ae9c4-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ae9c4-118">Attribute-Id</span></span>      | <span data-ttu-id="ae9c4-119">1.2.840.113556.1.4.1793</span><span class="sxs-lookup"><span data-stu-id="ae9c4-119">1.2.840.113556.1.4.1793</span></span>                 |
| <span data-ttu-id="ae9c4-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="ae9c4-120">System-Id-Guid</span></span>    | <span data-ttu-id="ae9c4-121">cafcb1de-f23c-46b5-adf7-1e64957bd5db</span><span class="sxs-lookup"><span data-stu-id="ae9c4-121">cafcb1de-f23c-46b5-adf7-1e64957bd5db</span></span>    |
| <span data-ttu-id="ae9c4-122">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ae9c4-122">Syntax</span></span>            | [<span data-ttu-id="ae9c4-123">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="ae9c4-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="ae9c4-124">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="ae9c4-124">Implementations</span></span>

-   [<span data-ttu-id="ae9c4-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ae9c4-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ae9c4-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ae9c4-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ae9c4-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ae9c4-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ae9c4-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ae9c4-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ae9c4-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ae9c4-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="ae9c4-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ae9c4-130">Windows Server 2003</span></span>



| <span data-ttu-id="ae9c4-131">Voce</span><span class="sxs-lookup"><span data-stu-id="ae9c4-131">Entry</span></span> | <span data-ttu-id="ae9c4-132">Valore</span><span class="sxs-lookup"><span data-stu-id="ae9c4-132">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="ae9c4-133">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="ae9c4-133">Link-Id</span></span>                | <span data-ttu-id="ae9c4-134">2014</span><span class="sxs-lookup"><span data-stu-id="ae9c4-134">2014</span></span>                                |
| <span data-ttu-id="ae9c4-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ae9c4-135">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="ae9c4-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="ae9c4-136">System-Only</span></span>            | <span data-ttu-id="ae9c4-137">Falso</span><span class="sxs-lookup"><span data-stu-id="ae9c4-137">False</span></span>                               |
| <span data-ttu-id="ae9c4-138">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="ae9c4-138">Is-Single-Valued</span></span>       | <span data-ttu-id="ae9c4-139">Falso</span><span class="sxs-lookup"><span data-stu-id="ae9c4-139">False</span></span>                               |
| <span data-ttu-id="ae9c4-140">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="ae9c4-140">Is Indexed</span></span>             | <span data-ttu-id="ae9c4-141">Falso</span><span class="sxs-lookup"><span data-stu-id="ae9c4-141">False</span></span>                               |
| <span data-ttu-id="ae9c4-142">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="ae9c4-142">In Global Catalog</span></span>      | <span data-ttu-id="ae9c4-143">Falso</span><span class="sxs-lookup"><span data-stu-id="ae9c4-143">False</span></span>                               |
| <span data-ttu-id="ae9c4-144">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="ae9c4-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="ae9c4-145">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="ae9c4-145">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="ae9c4-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ae9c4-146">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="ae9c4-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ae9c4-147">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="ae9c4-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ae9c4-148">Search-Flags</span></span>           | <span data-ttu-id="ae9c4-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ae9c4-149">0x00000000</span></span>                          |
| <span data-ttu-id="ae9c4-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ae9c4-150">System-Flags</span></span>           | <span data-ttu-id="ae9c4-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ae9c4-151">0x00000010</span></span>                          |
| <span data-ttu-id="ae9c4-152">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="ae9c4-152">Classes used in</span></span>        | [<span data-ttu-id="ae9c4-153">**Group**</span><span class="sxs-lookup"><span data-stu-id="ae9c4-153">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ae9c4-154">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ae9c4-154">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ae9c4-155">Voce</span><span class="sxs-lookup"><span data-stu-id="ae9c4-155">Entry</span></span> | <span data-ttu-id="ae9c4-156">Valore</span><span class="sxs-lookup"><span data-stu-id="ae9c4-156">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="ae9c4-157">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="ae9c4-157">Link-Id</span></span>                | <span data-ttu-id="ae9c4-158">2014</span><span class="sxs-lookup"><span data-stu-id="ae9c4-158">2014</span></span>                                |
| <span data-ttu-id="ae9c4-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ae9c4-159">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="ae9c4-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="ae9c4-160">System-Only</span></span>            | <span data-ttu-id="ae9c4-161">Falso</span><span class="sxs-lookup"><span data-stu-id="ae9c4-161">False</span></span>                               |
| <span data-ttu-id="ae9c4-162">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="ae9c4-162">Is-Single-Valued</span></span>       | <span data-ttu-id="ae9c4-163">Falso</span><span class="sxs-lookup"><span data-stu-id="ae9c4-163">False</span></span>                               |
| <span data-ttu-id="ae9c4-164">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="ae9c4-164">Is Indexed</span></span>             | <span data-ttu-id="ae9c4-165">Falso</span><span class="sxs-lookup"><span data-stu-id="ae9c4-165">False</span></span>                               |
| <span data-ttu-id="ae9c4-166">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="ae9c4-166">In Global Catalog</span></span>      | <span data-ttu-id="ae9c4-167">Falso</span><span class="sxs-lookup"><span data-stu-id="ae9c4-167">False</span></span>                               |
| <span data-ttu-id="ae9c4-168">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="ae9c4-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="ae9c4-169">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="ae9c4-169">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="ae9c4-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ae9c4-170">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="ae9c4-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ae9c4-171">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="ae9c4-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ae9c4-172">Search-Flags</span></span>           | <span data-ttu-id="ae9c4-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ae9c4-173">0x00000000</span></span>                          |
| <span data-ttu-id="ae9c4-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ae9c4-174">System-Flags</span></span>           | <span data-ttu-id="ae9c4-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ae9c4-175">0x00000010</span></span>                          |
| <span data-ttu-id="ae9c4-176">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="ae9c4-176">Classes used in</span></span>        | [<span data-ttu-id="ae9c4-177">**Group**</span><span class="sxs-lookup"><span data-stu-id="ae9c4-177">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ae9c4-178">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ae9c4-178">Windows Server 2008</span></span>



| <span data-ttu-id="ae9c4-179">Voce</span><span class="sxs-lookup"><span data-stu-id="ae9c4-179">Entry</span></span> | <span data-ttu-id="ae9c4-180">Valore</span><span class="sxs-lookup"><span data-stu-id="ae9c4-180">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="ae9c4-181">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="ae9c4-181">Link-Id</span></span>                | <span data-ttu-id="ae9c4-182">2014</span><span class="sxs-lookup"><span data-stu-id="ae9c4-182">2014</span></span>                                |
| <span data-ttu-id="ae9c4-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ae9c4-183">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="ae9c4-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="ae9c4-184">System-Only</span></span>            | <span data-ttu-id="ae9c4-185">Falso</span><span class="sxs-lookup"><span data-stu-id="ae9c4-185">False</span></span>                               |
| <span data-ttu-id="ae9c4-186">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="ae9c4-186">Is-Single-Valued</span></span>       | <span data-ttu-id="ae9c4-187">Falso</span><span class="sxs-lookup"><span data-stu-id="ae9c4-187">False</span></span>                               |
| <span data-ttu-id="ae9c4-188">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="ae9c4-188">Is Indexed</span></span>             | <span data-ttu-id="ae9c4-189">Falso</span><span class="sxs-lookup"><span data-stu-id="ae9c4-189">False</span></span>                               |
| <span data-ttu-id="ae9c4-190">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="ae9c4-190">In Global Catalog</span></span>      | <span data-ttu-id="ae9c4-191">Falso</span><span class="sxs-lookup"><span data-stu-id="ae9c4-191">False</span></span>                               |
| <span data-ttu-id="ae9c4-192">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="ae9c4-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="ae9c4-193">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="ae9c4-193">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="ae9c4-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ae9c4-194">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="ae9c4-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ae9c4-195">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="ae9c4-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ae9c4-196">Search-Flags</span></span>           | <span data-ttu-id="ae9c4-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ae9c4-197">0x00000000</span></span>                          |
| <span data-ttu-id="ae9c4-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ae9c4-198">System-Flags</span></span>           | <span data-ttu-id="ae9c4-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ae9c4-199">0x00000010</span></span>                          |
| <span data-ttu-id="ae9c4-200">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="ae9c4-200">Classes used in</span></span>        | [<span data-ttu-id="ae9c4-201">**Group**</span><span class="sxs-lookup"><span data-stu-id="ae9c4-201">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ae9c4-202">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ae9c4-202">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ae9c4-203">Voce</span><span class="sxs-lookup"><span data-stu-id="ae9c4-203">Entry</span></span> | <span data-ttu-id="ae9c4-204">Valore</span><span class="sxs-lookup"><span data-stu-id="ae9c4-204">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="ae9c4-205">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="ae9c4-205">Link-Id</span></span>                | <span data-ttu-id="ae9c4-206">2014</span><span class="sxs-lookup"><span data-stu-id="ae9c4-206">2014</span></span>                                |
| <span data-ttu-id="ae9c4-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ae9c4-207">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="ae9c4-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="ae9c4-208">System-Only</span></span>            | <span data-ttu-id="ae9c4-209">Falso</span><span class="sxs-lookup"><span data-stu-id="ae9c4-209">False</span></span>                               |
| <span data-ttu-id="ae9c4-210">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="ae9c4-210">Is-Single-Valued</span></span>       | <span data-ttu-id="ae9c4-211">Falso</span><span class="sxs-lookup"><span data-stu-id="ae9c4-211">False</span></span>                               |
| <span data-ttu-id="ae9c4-212">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="ae9c4-212">Is Indexed</span></span>             | <span data-ttu-id="ae9c4-213">Falso</span><span class="sxs-lookup"><span data-stu-id="ae9c4-213">False</span></span>                               |
| <span data-ttu-id="ae9c4-214">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="ae9c4-214">In Global Catalog</span></span>      | <span data-ttu-id="ae9c4-215">Falso</span><span class="sxs-lookup"><span data-stu-id="ae9c4-215">False</span></span>                               |
| <span data-ttu-id="ae9c4-216">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="ae9c4-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="ae9c4-217">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="ae9c4-217">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="ae9c4-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ae9c4-218">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="ae9c4-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ae9c4-219">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="ae9c4-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ae9c4-220">Search-Flags</span></span>           | <span data-ttu-id="ae9c4-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ae9c4-221">0x00000000</span></span>                          |
| <span data-ttu-id="ae9c4-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ae9c4-222">System-Flags</span></span>           | <span data-ttu-id="ae9c4-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ae9c4-223">0x00000010</span></span>                          |
| <span data-ttu-id="ae9c4-224">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="ae9c4-224">Classes used in</span></span>        | [<span data-ttu-id="ae9c4-225">**Group**</span><span class="sxs-lookup"><span data-stu-id="ae9c4-225">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ae9c4-226">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ae9c4-226">Windows Server 2012</span></span>



| <span data-ttu-id="ae9c4-227">Voce</span><span class="sxs-lookup"><span data-stu-id="ae9c4-227">Entry</span></span> | <span data-ttu-id="ae9c4-228">Valore</span><span class="sxs-lookup"><span data-stu-id="ae9c4-228">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="ae9c4-229">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="ae9c4-229">Link-Id</span></span>                | <span data-ttu-id="ae9c4-230">2014</span><span class="sxs-lookup"><span data-stu-id="ae9c4-230">2014</span></span>                                |
| <span data-ttu-id="ae9c4-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ae9c4-231">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="ae9c4-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="ae9c4-232">System-Only</span></span>            | <span data-ttu-id="ae9c4-233">Falso</span><span class="sxs-lookup"><span data-stu-id="ae9c4-233">False</span></span>                               |
| <span data-ttu-id="ae9c4-234">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="ae9c4-234">Is-Single-Valued</span></span>       | <span data-ttu-id="ae9c4-235">Falso</span><span class="sxs-lookup"><span data-stu-id="ae9c4-235">False</span></span>                               |
| <span data-ttu-id="ae9c4-236">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="ae9c4-236">Is Indexed</span></span>             | <span data-ttu-id="ae9c4-237">Falso</span><span class="sxs-lookup"><span data-stu-id="ae9c4-237">False</span></span>                               |
| <span data-ttu-id="ae9c4-238">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="ae9c4-238">In Global Catalog</span></span>      | <span data-ttu-id="ae9c4-239">Falso</span><span class="sxs-lookup"><span data-stu-id="ae9c4-239">False</span></span>                               |
| <span data-ttu-id="ae9c4-240">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="ae9c4-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="ae9c4-241">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="ae9c4-241">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="ae9c4-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ae9c4-242">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="ae9c4-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ae9c4-243">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="ae9c4-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ae9c4-244">Search-Flags</span></span>           | <span data-ttu-id="ae9c4-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ae9c4-245">0x00000000</span></span>                          |
| <span data-ttu-id="ae9c4-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ae9c4-246">System-Flags</span></span>           | <span data-ttu-id="ae9c4-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ae9c4-247">0x00000010</span></span>                          |
| <span data-ttu-id="ae9c4-248">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="ae9c4-248">Classes used in</span></span>        | [<span data-ttu-id="ae9c4-249">**Group**</span><span class="sxs-lookup"><span data-stu-id="ae9c4-249">**Group**</span></span>](c-group.md)<br/> |



 

 





