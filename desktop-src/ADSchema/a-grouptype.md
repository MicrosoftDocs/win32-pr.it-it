---
title: Attributo Group-Type
description: Contiene un set di flag che definiscono il tipo e l'ambito di un oggetto gruppo.
ms.assetid: cd37ed2f-8503-4227-b0d2-c8135605cb84
ms.tgt_platform: multiple
keywords:
- Schema AD Group-Type attribute
- Schema AD dell'attributo groupType
topic_type:
- apiref
api_name:
- Group-Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e1db8f102e7e56b38d15d74fedb7c5a5366ee47
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "106302895"
---
# <a name="group-type-attribute"></a><span data-ttu-id="bfca9-105">Attributo Group-Type</span><span class="sxs-lookup"><span data-stu-id="bfca9-105">Group-Type attribute</span></span>

<span data-ttu-id="bfca9-106">Contiene un set di flag che definiscono il tipo e l'ambito di un oggetto gruppo.</span><span class="sxs-lookup"><span data-stu-id="bfca9-106">Contains a set of flags that define the type and scope of a group object.</span></span> <span data-ttu-id="bfca9-107">Per i valori possibili per questo attributo, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="bfca9-107">For the possible values for this attribute, see Remarks.</span></span>



| <span data-ttu-id="bfca9-108">Voce</span><span class="sxs-lookup"><span data-stu-id="bfca9-108">Entry</span></span> | <span data-ttu-id="bfca9-109">Valore</span><span class="sxs-lookup"><span data-stu-id="bfca9-109">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="bfca9-110">CN</span><span class="sxs-lookup"><span data-stu-id="bfca9-110">CN</span></span>                | <span data-ttu-id="bfca9-111">Group-Type</span><span class="sxs-lookup"><span data-stu-id="bfca9-111">Group-Type</span></span>                           |
| <span data-ttu-id="bfca9-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="bfca9-112">Ldap-Display-Name</span></span> | <span data-ttu-id="bfca9-113">groupType</span><span class="sxs-lookup"><span data-stu-id="bfca9-113">groupType</span></span>                            |
| <span data-ttu-id="bfca9-114">Dimensione</span><span class="sxs-lookup"><span data-stu-id="bfca9-114">Size</span></span>              | \-                                   |
| <span data-ttu-id="bfca9-115">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="bfca9-115">Update Privilege</span></span>  | <span data-ttu-id="bfca9-116">Amministratore di dominio</span><span class="sxs-lookup"><span data-stu-id="bfca9-116">Domain administrator</span></span>                 |
| <span data-ttu-id="bfca9-117">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="bfca9-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="bfca9-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="bfca9-118">Attribute-Id</span></span>      | <span data-ttu-id="bfca9-119">1.2.840.113556.1.4.750</span><span class="sxs-lookup"><span data-stu-id="bfca9-119">1.2.840.113556.1.4.750</span></span>               |
| <span data-ttu-id="bfca9-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="bfca9-120">System-Id-Guid</span></span>    | <span data-ttu-id="bfca9-121">9a9a021e-4a5b-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="bfca9-121">9a9a021e-4a5b-11d1-a9c3-0000f80367c1</span></span> |
| <span data-ttu-id="bfca9-122">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bfca9-122">Syntax</span></span>            | [<span data-ttu-id="bfca9-123">**Enumerazione**</span><span class="sxs-lookup"><span data-stu-id="bfca9-123">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="bfca9-124">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="bfca9-124">Implementations</span></span>

-   [<span data-ttu-id="bfca9-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="bfca9-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="bfca9-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="bfca9-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="bfca9-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="bfca9-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="bfca9-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="bfca9-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="bfca9-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="bfca9-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="bfca9-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="bfca9-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="bfca9-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="bfca9-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="bfca9-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="bfca9-132">Windows 2000 Server</span></span>



| <span data-ttu-id="bfca9-133">Voce</span><span class="sxs-lookup"><span data-stu-id="bfca9-133">Entry</span></span> | <span data-ttu-id="bfca9-134">Valore</span><span class="sxs-lookup"><span data-stu-id="bfca9-134">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="bfca9-135">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="bfca9-135">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="bfca9-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bfca9-136">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="bfca9-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="bfca9-137">System-Only</span></span>            | <span data-ttu-id="bfca9-138">Falso</span><span class="sxs-lookup"><span data-stu-id="bfca9-138">False</span></span>                               |
| <span data-ttu-id="bfca9-139">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="bfca9-139">Is-Single-Valued</span></span>       | <span data-ttu-id="bfca9-140">Vero</span><span class="sxs-lookup"><span data-stu-id="bfca9-140">True</span></span>                                |
| <span data-ttu-id="bfca9-141">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="bfca9-141">Is Indexed</span></span>             | <span data-ttu-id="bfca9-142">Vero</span><span class="sxs-lookup"><span data-stu-id="bfca9-142">True</span></span>                                |
| <span data-ttu-id="bfca9-143">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="bfca9-143">In Global Catalog</span></span>      | <span data-ttu-id="bfca9-144">Vero</span><span class="sxs-lookup"><span data-stu-id="bfca9-144">True</span></span>                                |
| <span data-ttu-id="bfca9-145">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="bfca9-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="bfca9-146">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="bfca9-146">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="bfca9-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bfca9-147">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="bfca9-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bfca9-148">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="bfca9-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bfca9-149">Search-Flags</span></span>           | <span data-ttu-id="bfca9-150">0x00000009</span><span class="sxs-lookup"><span data-stu-id="bfca9-150">0x00000009</span></span>                          |
| <span data-ttu-id="bfca9-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bfca9-151">System-Flags</span></span>           | <span data-ttu-id="bfca9-152">0x00000012</span><span class="sxs-lookup"><span data-stu-id="bfca9-152">0x00000012</span></span>                          |
| <span data-ttu-id="bfca9-153">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="bfca9-153">Classes used in</span></span>        | [<span data-ttu-id="bfca9-154">**Group**</span><span class="sxs-lookup"><span data-stu-id="bfca9-154">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="bfca9-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="bfca9-155">Windows Server 2003</span></span>



| <span data-ttu-id="bfca9-156">Voce</span><span class="sxs-lookup"><span data-stu-id="bfca9-156">Entry</span></span> | <span data-ttu-id="bfca9-157">Valore</span><span class="sxs-lookup"><span data-stu-id="bfca9-157">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="bfca9-158">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="bfca9-158">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="bfca9-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bfca9-159">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="bfca9-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="bfca9-160">System-Only</span></span>            | <span data-ttu-id="bfca9-161">Falso</span><span class="sxs-lookup"><span data-stu-id="bfca9-161">False</span></span>                               |
| <span data-ttu-id="bfca9-162">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="bfca9-162">Is-Single-Valued</span></span>       | <span data-ttu-id="bfca9-163">Vero</span><span class="sxs-lookup"><span data-stu-id="bfca9-163">True</span></span>                                |
| <span data-ttu-id="bfca9-164">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="bfca9-164">Is Indexed</span></span>             | <span data-ttu-id="bfca9-165">Vero</span><span class="sxs-lookup"><span data-stu-id="bfca9-165">True</span></span>                                |
| <span data-ttu-id="bfca9-166">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="bfca9-166">In Global Catalog</span></span>      | <span data-ttu-id="bfca9-167">Vero</span><span class="sxs-lookup"><span data-stu-id="bfca9-167">True</span></span>                                |
| <span data-ttu-id="bfca9-168">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="bfca9-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="bfca9-169">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="bfca9-169">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="bfca9-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bfca9-170">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="bfca9-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bfca9-171">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="bfca9-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bfca9-172">Search-Flags</span></span>           | <span data-ttu-id="bfca9-173">0x00000009</span><span class="sxs-lookup"><span data-stu-id="bfca9-173">0x00000009</span></span>                          |
| <span data-ttu-id="bfca9-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bfca9-174">System-Flags</span></span>           | <span data-ttu-id="bfca9-175">0x00000012</span><span class="sxs-lookup"><span data-stu-id="bfca9-175">0x00000012</span></span>                          |
| <span data-ttu-id="bfca9-176">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="bfca9-176">Classes used in</span></span>        | [<span data-ttu-id="bfca9-177">**Group**</span><span class="sxs-lookup"><span data-stu-id="bfca9-177">**Group**</span></span>](c-group.md)<br/> |



## <a name="adam"></a><span data-ttu-id="bfca9-178">ADAM</span><span class="sxs-lookup"><span data-stu-id="bfca9-178">ADAM</span></span>



| <span data-ttu-id="bfca9-179">Voce</span><span class="sxs-lookup"><span data-stu-id="bfca9-179">Entry</span></span> | <span data-ttu-id="bfca9-180">Valore</span><span class="sxs-lookup"><span data-stu-id="bfca9-180">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="bfca9-181">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="bfca9-181">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="bfca9-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bfca9-182">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="bfca9-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="bfca9-183">System-Only</span></span>            | <span data-ttu-id="bfca9-184">Falso</span><span class="sxs-lookup"><span data-stu-id="bfca9-184">False</span></span>                               |
| <span data-ttu-id="bfca9-185">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="bfca9-185">Is-Single-Valued</span></span>       | <span data-ttu-id="bfca9-186">Vero</span><span class="sxs-lookup"><span data-stu-id="bfca9-186">True</span></span>                                |
| <span data-ttu-id="bfca9-187">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="bfca9-187">Is Indexed</span></span>             | <span data-ttu-id="bfca9-188">Vero</span><span class="sxs-lookup"><span data-stu-id="bfca9-188">True</span></span>                                |
| <span data-ttu-id="bfca9-189">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="bfca9-189">In Global Catalog</span></span>      | <span data-ttu-id="bfca9-190">Vero</span><span class="sxs-lookup"><span data-stu-id="bfca9-190">True</span></span>                                |
| <span data-ttu-id="bfca9-191">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="bfca9-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="bfca9-192">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="bfca9-192">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="bfca9-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bfca9-193">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="bfca9-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bfca9-194">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="bfca9-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bfca9-195">Search-Flags</span></span>           | <span data-ttu-id="bfca9-196">0x00000009</span><span class="sxs-lookup"><span data-stu-id="bfca9-196">0x00000009</span></span>                          |
| <span data-ttu-id="bfca9-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bfca9-197">System-Flags</span></span>           | <span data-ttu-id="bfca9-198">0x00000012</span><span class="sxs-lookup"><span data-stu-id="bfca9-198">0x00000012</span></span>                          |
| <span data-ttu-id="bfca9-199">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="bfca9-199">Classes used in</span></span>        | [<span data-ttu-id="bfca9-200">**Group**</span><span class="sxs-lookup"><span data-stu-id="bfca9-200">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="bfca9-201">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="bfca9-201">Windows Server 2003 R2</span></span>



| <span data-ttu-id="bfca9-202">Voce</span><span class="sxs-lookup"><span data-stu-id="bfca9-202">Entry</span></span> | <span data-ttu-id="bfca9-203">Valore</span><span class="sxs-lookup"><span data-stu-id="bfca9-203">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="bfca9-204">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="bfca9-204">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="bfca9-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bfca9-205">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="bfca9-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="bfca9-206">System-Only</span></span>            | <span data-ttu-id="bfca9-207">Falso</span><span class="sxs-lookup"><span data-stu-id="bfca9-207">False</span></span>                               |
| <span data-ttu-id="bfca9-208">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="bfca9-208">Is-Single-Valued</span></span>       | <span data-ttu-id="bfca9-209">Vero</span><span class="sxs-lookup"><span data-stu-id="bfca9-209">True</span></span>                                |
| <span data-ttu-id="bfca9-210">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="bfca9-210">Is Indexed</span></span>             | <span data-ttu-id="bfca9-211">Vero</span><span class="sxs-lookup"><span data-stu-id="bfca9-211">True</span></span>                                |
| <span data-ttu-id="bfca9-212">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="bfca9-212">In Global Catalog</span></span>      | <span data-ttu-id="bfca9-213">Vero</span><span class="sxs-lookup"><span data-stu-id="bfca9-213">True</span></span>                                |
| <span data-ttu-id="bfca9-214">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="bfca9-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="bfca9-215">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="bfca9-215">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="bfca9-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bfca9-216">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="bfca9-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bfca9-217">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="bfca9-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bfca9-218">Search-Flags</span></span>           | <span data-ttu-id="bfca9-219">0x00000009</span><span class="sxs-lookup"><span data-stu-id="bfca9-219">0x00000009</span></span>                          |
| <span data-ttu-id="bfca9-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bfca9-220">System-Flags</span></span>           | <span data-ttu-id="bfca9-221">0x00000012</span><span class="sxs-lookup"><span data-stu-id="bfca9-221">0x00000012</span></span>                          |
| <span data-ttu-id="bfca9-222">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="bfca9-222">Classes used in</span></span>        | [<span data-ttu-id="bfca9-223">**Group**</span><span class="sxs-lookup"><span data-stu-id="bfca9-223">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="bfca9-224">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bfca9-224">Windows Server 2008</span></span>



| <span data-ttu-id="bfca9-225">Voce</span><span class="sxs-lookup"><span data-stu-id="bfca9-225">Entry</span></span> | <span data-ttu-id="bfca9-226">Valore</span><span class="sxs-lookup"><span data-stu-id="bfca9-226">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="bfca9-227">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="bfca9-227">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="bfca9-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bfca9-228">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="bfca9-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="bfca9-229">System-Only</span></span>            | <span data-ttu-id="bfca9-230">Falso</span><span class="sxs-lookup"><span data-stu-id="bfca9-230">False</span></span>                               |
| <span data-ttu-id="bfca9-231">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="bfca9-231">Is-Single-Valued</span></span>       | <span data-ttu-id="bfca9-232">Vero</span><span class="sxs-lookup"><span data-stu-id="bfca9-232">True</span></span>                                |
| <span data-ttu-id="bfca9-233">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="bfca9-233">Is Indexed</span></span>             | <span data-ttu-id="bfca9-234">Vero</span><span class="sxs-lookup"><span data-stu-id="bfca9-234">True</span></span>                                |
| <span data-ttu-id="bfca9-235">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="bfca9-235">In Global Catalog</span></span>      | <span data-ttu-id="bfca9-236">Vero</span><span class="sxs-lookup"><span data-stu-id="bfca9-236">True</span></span>                                |
| <span data-ttu-id="bfca9-237">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="bfca9-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="bfca9-238">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="bfca9-238">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="bfca9-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bfca9-239">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="bfca9-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bfca9-240">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="bfca9-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bfca9-241">Search-Flags</span></span>           | <span data-ttu-id="bfca9-242">0x00000009</span><span class="sxs-lookup"><span data-stu-id="bfca9-242">0x00000009</span></span>                          |
| <span data-ttu-id="bfca9-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bfca9-243">System-Flags</span></span>           | <span data-ttu-id="bfca9-244">0x00000012</span><span class="sxs-lookup"><span data-stu-id="bfca9-244">0x00000012</span></span>                          |
| <span data-ttu-id="bfca9-245">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="bfca9-245">Classes used in</span></span>        | [<span data-ttu-id="bfca9-246">**Group**</span><span class="sxs-lookup"><span data-stu-id="bfca9-246">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="bfca9-247">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="bfca9-247">Windows Server 2008 R2</span></span>



| <span data-ttu-id="bfca9-248">Voce</span><span class="sxs-lookup"><span data-stu-id="bfca9-248">Entry</span></span> | <span data-ttu-id="bfca9-249">Valore</span><span class="sxs-lookup"><span data-stu-id="bfca9-249">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="bfca9-250">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="bfca9-250">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="bfca9-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bfca9-251">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="bfca9-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="bfca9-252">System-Only</span></span>            | <span data-ttu-id="bfca9-253">Falso</span><span class="sxs-lookup"><span data-stu-id="bfca9-253">False</span></span>                               |
| <span data-ttu-id="bfca9-254">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="bfca9-254">Is-Single-Valued</span></span>       | <span data-ttu-id="bfca9-255">Vero</span><span class="sxs-lookup"><span data-stu-id="bfca9-255">True</span></span>                                |
| <span data-ttu-id="bfca9-256">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="bfca9-256">Is Indexed</span></span>             | <span data-ttu-id="bfca9-257">Vero</span><span class="sxs-lookup"><span data-stu-id="bfca9-257">True</span></span>                                |
| <span data-ttu-id="bfca9-258">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="bfca9-258">In Global Catalog</span></span>      | <span data-ttu-id="bfca9-259">Vero</span><span class="sxs-lookup"><span data-stu-id="bfca9-259">True</span></span>                                |
| <span data-ttu-id="bfca9-260">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="bfca9-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="bfca9-261">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="bfca9-261">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="bfca9-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bfca9-262">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="bfca9-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bfca9-263">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="bfca9-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bfca9-264">Search-Flags</span></span>           | <span data-ttu-id="bfca9-265">0x00000009</span><span class="sxs-lookup"><span data-stu-id="bfca9-265">0x00000009</span></span>                          |
| <span data-ttu-id="bfca9-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bfca9-266">System-Flags</span></span>           | <span data-ttu-id="bfca9-267">0x00000012</span><span class="sxs-lookup"><span data-stu-id="bfca9-267">0x00000012</span></span>                          |
| <span data-ttu-id="bfca9-268">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="bfca9-268">Classes used in</span></span>        | [<span data-ttu-id="bfca9-269">**Group**</span><span class="sxs-lookup"><span data-stu-id="bfca9-269">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="bfca9-270">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="bfca9-270">Windows Server 2012</span></span>



| <span data-ttu-id="bfca9-271">Voce</span><span class="sxs-lookup"><span data-stu-id="bfca9-271">Entry</span></span> | <span data-ttu-id="bfca9-272">Valore</span><span class="sxs-lookup"><span data-stu-id="bfca9-272">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="bfca9-273">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="bfca9-273">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="bfca9-274">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bfca9-274">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="bfca9-275">System-Only</span><span class="sxs-lookup"><span data-stu-id="bfca9-275">System-Only</span></span>            | <span data-ttu-id="bfca9-276">Falso</span><span class="sxs-lookup"><span data-stu-id="bfca9-276">False</span></span>                               |
| <span data-ttu-id="bfca9-277">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="bfca9-277">Is-Single-Valued</span></span>       | <span data-ttu-id="bfca9-278">Vero</span><span class="sxs-lookup"><span data-stu-id="bfca9-278">True</span></span>                                |
| <span data-ttu-id="bfca9-279">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="bfca9-279">Is Indexed</span></span>             | <span data-ttu-id="bfca9-280">Vero</span><span class="sxs-lookup"><span data-stu-id="bfca9-280">True</span></span>                                |
| <span data-ttu-id="bfca9-281">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="bfca9-281">In Global Catalog</span></span>      | <span data-ttu-id="bfca9-282">Vero</span><span class="sxs-lookup"><span data-stu-id="bfca9-282">True</span></span>                                |
| <span data-ttu-id="bfca9-283">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="bfca9-283">NT-Security-Descriptor</span></span> | <span data-ttu-id="bfca9-284">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="bfca9-284">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="bfca9-285">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bfca9-285">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="bfca9-286">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bfca9-286">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="bfca9-287">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bfca9-287">Search-Flags</span></span>           | <span data-ttu-id="bfca9-288">0x00000009</span><span class="sxs-lookup"><span data-stu-id="bfca9-288">0x00000009</span></span>                          |
| <span data-ttu-id="bfca9-289">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bfca9-289">System-Flags</span></span>           | <span data-ttu-id="bfca9-290">0x00000012</span><span class="sxs-lookup"><span data-stu-id="bfca9-290">0x00000012</span></span>                          |
| <span data-ttu-id="bfca9-291">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="bfca9-291">Classes used in</span></span>        | [<span data-ttu-id="bfca9-292">**Group**</span><span class="sxs-lookup"><span data-stu-id="bfca9-292">**Group**</span></span>](c-group.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="bfca9-293">Commenti</span><span class="sxs-lookup"><span data-stu-id="bfca9-293">Remarks</span></span>

<span data-ttu-id="bfca9-294">Questo attributo può essere zero o una combinazione di uno o più dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="bfca9-294">This attribute can be zero or a combination of one or more of the following values.</span></span>



| <span data-ttu-id="bfca9-295">Valore</span><span class="sxs-lookup"><span data-stu-id="bfca9-295">Value</span></span>                   | <span data-ttu-id="bfca9-296">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bfca9-296">Description</span></span>                                                                                  |
|-------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="bfca9-297">1 (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="bfca9-297">1 (0x00000001)</span></span>          | <span data-ttu-id="bfca9-298">Specifica un gruppo creato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="bfca9-298">Specifies a group that is created by the system.</span></span>                                             |
| <span data-ttu-id="bfca9-299">2 (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="bfca9-299">2 (0x00000002)</span></span>          | <span data-ttu-id="bfca9-300">Specifica un gruppo con ambito globale.</span><span class="sxs-lookup"><span data-stu-id="bfca9-300">Specifies a group with global scope.</span></span>                                                         |
| <span data-ttu-id="bfca9-301">4 (0x00000004)</span><span class="sxs-lookup"><span data-stu-id="bfca9-301">4 (0x00000004)</span></span>          | <span data-ttu-id="bfca9-302">Specifica un gruppo con ambito locale di dominio.</span><span class="sxs-lookup"><span data-stu-id="bfca9-302">Specifies a group with domain local scope.</span></span>                                                   |
| <span data-ttu-id="bfca9-303">8 (0x00000008)</span><span class="sxs-lookup"><span data-stu-id="bfca9-303">8 (0x00000008)</span></span>          | <span data-ttu-id="bfca9-304">Specifica un gruppo con ambito universale.</span><span class="sxs-lookup"><span data-stu-id="bfca9-304">Specifies a group with universal scope.</span></span>                                                      |
| <span data-ttu-id="bfca9-305">16 (0x00000010)</span><span class="sxs-lookup"><span data-stu-id="bfca9-305">16 (0x00000010)</span></span>         | <span data-ttu-id="bfca9-306">Specifica un \_ gruppo App Basic per gestione autorizzazioni di Windows Server.</span><span class="sxs-lookup"><span data-stu-id="bfca9-306">Specifies an APP\_BASIC group for Windows Server Authorization Manager.</span></span>                      |
| <span data-ttu-id="bfca9-307">32 (0x00000020)</span><span class="sxs-lookup"><span data-stu-id="bfca9-307">32 (0x00000020)</span></span>         | <span data-ttu-id="bfca9-308">Specifica un \_ gruppo di query app per gestione autorizzazioni di Windows Server.</span><span class="sxs-lookup"><span data-stu-id="bfca9-308">Specifies an APP\_QUERY group for Windows Server Authorization Manager.</span></span>                      |
| <span data-ttu-id="bfca9-309">2147483648 (0x80000000)</span><span class="sxs-lookup"><span data-stu-id="bfca9-309">2147483648 (0x80000000)</span></span> | <span data-ttu-id="bfca9-310">Specifica un gruppo di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="bfca9-310">Specifies a security group.</span></span> <span data-ttu-id="bfca9-311">Se questo flag non è impostato, il gruppo è un gruppo di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="bfca9-311">If this flag is not set, then the group is a distribution group.</span></span> |



 

<span data-ttu-id="bfca9-312">Per ulteriori informazioni sul tipo di gruppo e sull'ambito, vedere gli argomenti [tipi](/previous-versions/windows/it-pro/windows-server-2003/cc781446(v=ws.10)) di gruppo e [ambito del gruppo](/previous-versions/windows/it-pro/windows-server-2003/cc755692(v=ws.10)) in Microsoft TechNet.</span><span class="sxs-lookup"><span data-stu-id="bfca9-312">For more information about group type and scope, see the [Group types](/previous-versions/windows/it-pro/windows-server-2003/cc781446(v=ws.10)) and [Group scope](/previous-versions/windows/it-pro/windows-server-2003/cc755692(v=ws.10)) topics on Microsoft TechNet.</span></span>

 

