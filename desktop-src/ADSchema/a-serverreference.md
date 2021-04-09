---
title: Attributo Server-Reference
description: Disponibile in un oggetto computer del sito. Contiene il nome distinto del controller di dominio nel contesto dei nomi di dominio.
ms.assetid: 6c0ebe85-b4ed-4284-ad96-0b711d5acce7
ms.tgt_platform: multiple
keywords:
- Schema AD Server-Reference attribute
- Schema AD dell'attributo serverReference
topic_type:
- apiref
api_name:
- Server-Reference
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83fed3b44feeaccb87cb1f55435bbac915c1c262
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103875533"
---
# <a name="server-reference-attribute"></a><span data-ttu-id="d7e60-106">Attributo Server-Reference</span><span class="sxs-lookup"><span data-stu-id="d7e60-106">Server-Reference attribute</span></span>

<span data-ttu-id="d7e60-107">Disponibile in un oggetto computer del sito.</span><span class="sxs-lookup"><span data-stu-id="d7e60-107">Found in a site computer object.</span></span> <span data-ttu-id="d7e60-108">Contiene il nome distinto del controller di dominio nel contesto dei nomi di dominio.</span><span class="sxs-lookup"><span data-stu-id="d7e60-108">Contains the distinguished name of the domain controller in the domain naming context.</span></span>



| <span data-ttu-id="d7e60-109">Voce</span><span class="sxs-lookup"><span data-stu-id="d7e60-109">Entry</span></span> | <span data-ttu-id="d7e60-110">Valore</span><span class="sxs-lookup"><span data-stu-id="d7e60-110">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="d7e60-111">CN</span><span class="sxs-lookup"><span data-stu-id="d7e60-111">CN</span></span>                | <span data-ttu-id="d7e60-112">Server-Reference</span><span class="sxs-lookup"><span data-stu-id="d7e60-112">Server-Reference</span></span>                        |
| <span data-ttu-id="d7e60-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="d7e60-113">Ldap-Display-Name</span></span> | <span data-ttu-id="d7e60-114">serverReference</span><span class="sxs-lookup"><span data-stu-id="d7e60-114">serverReference</span></span>                         |
| <span data-ttu-id="d7e60-115">Dimensione</span><span class="sxs-lookup"><span data-stu-id="d7e60-115">Size</span></span>              | \-                                      |
| <span data-ttu-id="d7e60-116">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="d7e60-116">Update Privilege</span></span>  | <span data-ttu-id="d7e60-117">Questo valore viene impostato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="d7e60-117">This value is set by the system.</span></span>        |
| <span data-ttu-id="d7e60-118">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="d7e60-118">Update Frequency</span></span>  | <span data-ttu-id="d7e60-119">Ogni volta che viene creato un sito.</span><span class="sxs-lookup"><span data-stu-id="d7e60-119">Whenever a site is created.</span></span>             |
| <span data-ttu-id="d7e60-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="d7e60-120">Attribute-Id</span></span>      | <span data-ttu-id="d7e60-121">1.2.840.113556.1.4.515</span><span class="sxs-lookup"><span data-stu-id="d7e60-121">1.2.840.113556.1.4.515</span></span>                  |
| <span data-ttu-id="d7e60-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="d7e60-122">System-Id-Guid</span></span>    | <span data-ttu-id="d7e60-123">26d9736d-6070-11d1-a9c6-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="d7e60-123">26d9736d-6070-11d1-a9c6-0000f80367c1</span></span>    |
| <span data-ttu-id="d7e60-124">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d7e60-124">Syntax</span></span>            | [<span data-ttu-id="d7e60-125">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="d7e60-125">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="d7e60-126">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="d7e60-126">Implementations</span></span>

-   [<span data-ttu-id="d7e60-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="d7e60-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="d7e60-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="d7e60-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="d7e60-129">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="d7e60-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="d7e60-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="d7e60-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="d7e60-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="d7e60-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="d7e60-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="d7e60-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="d7e60-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="d7e60-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="d7e60-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d7e60-134">Windows 2000 Server</span></span>



| <span data-ttu-id="d7e60-135">Voce</span><span class="sxs-lookup"><span data-stu-id="d7e60-135">Entry</span></span> | <span data-ttu-id="d7e60-136">Valore</span><span class="sxs-lookup"><span data-stu-id="d7e60-136">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7e60-137">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="d7e60-137">Link-Id</span></span>                | <span data-ttu-id="d7e60-138">94</span><span class="sxs-lookup"><span data-stu-id="d7e60-138">94</span></span>                                                                                                                              |
| <span data-ttu-id="d7e60-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d7e60-139">MAPI-Id</span></span>                | \-                                                                                                                              |
| <span data-ttu-id="d7e60-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="d7e60-140">System-Only</span></span>            | <span data-ttu-id="d7e60-141">Falso</span><span class="sxs-lookup"><span data-stu-id="d7e60-141">False</span></span>                                                                                                                           |
| <span data-ttu-id="d7e60-142">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="d7e60-142">Is-Single-Valued</span></span>       | <span data-ttu-id="d7e60-143">Vero</span><span class="sxs-lookup"><span data-stu-id="d7e60-143">True</span></span>                                                                                                                            |
| <span data-ttu-id="d7e60-144">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="d7e60-144">Is Indexed</span></span>             | <span data-ttu-id="d7e60-145">Falso</span><span class="sxs-lookup"><span data-stu-id="d7e60-145">False</span></span>                                                                                                                           |
| <span data-ttu-id="d7e60-146">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="d7e60-146">In Global Catalog</span></span>      | <span data-ttu-id="d7e60-147">Falso</span><span class="sxs-lookup"><span data-stu-id="d7e60-147">False</span></span>                                                                                                                           |
| <span data-ttu-id="d7e60-148">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="d7e60-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="d7e60-149">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="d7e60-149">O:BAG:BAD:S:</span></span>                                                                                                                    |
| <span data-ttu-id="d7e60-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d7e60-150">Range-Lower</span></span>            | \-                                                                                                                              |
| <span data-ttu-id="d7e60-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d7e60-151">Range-Upper</span></span>            | \-                                                                                                                              |
| <span data-ttu-id="d7e60-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d7e60-152">Search-Flags</span></span>           | <span data-ttu-id="d7e60-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d7e60-153">0x00000000</span></span>                                                                                                                      |
| <span data-ttu-id="d7e60-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d7e60-154">System-Flags</span></span>           | <span data-ttu-id="d7e60-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d7e60-155">0x00000010</span></span>                                                                                                                      |
| <span data-ttu-id="d7e60-156">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="d7e60-156">Classes used in</span></span>        | [<span data-ttu-id="d7e60-157">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="d7e60-157">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> [<span data-ttu-id="d7e60-158">**Membro NTFRS**</span><span class="sxs-lookup"><span data-stu-id="d7e60-158">**NTFRS-Member**</span></span>](c-ntfrsmember.md)<br/> [<span data-ttu-id="d7e60-159">**Server**</span><span class="sxs-lookup"><span data-stu-id="d7e60-159">**Server**</span></span>](c-server.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="d7e60-160">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d7e60-160">Windows Server 2003</span></span>



| <span data-ttu-id="d7e60-161">Voce</span><span class="sxs-lookup"><span data-stu-id="d7e60-161">Entry</span></span> | <span data-ttu-id="d7e60-162">Valore</span><span class="sxs-lookup"><span data-stu-id="d7e60-162">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7e60-163">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="d7e60-163">Link-Id</span></span>                | <span data-ttu-id="d7e60-164">94</span><span class="sxs-lookup"><span data-stu-id="d7e60-164">94</span></span>                                                                                                                              |
| <span data-ttu-id="d7e60-165">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d7e60-165">MAPI-Id</span></span>                | \-                                                                                                                              |
| <span data-ttu-id="d7e60-166">System-Only</span><span class="sxs-lookup"><span data-stu-id="d7e60-166">System-Only</span></span>            | <span data-ttu-id="d7e60-167">Falso</span><span class="sxs-lookup"><span data-stu-id="d7e60-167">False</span></span>                                                                                                                           |
| <span data-ttu-id="d7e60-168">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="d7e60-168">Is-Single-Valued</span></span>       | <span data-ttu-id="d7e60-169">Vero</span><span class="sxs-lookup"><span data-stu-id="d7e60-169">True</span></span>                                                                                                                            |
| <span data-ttu-id="d7e60-170">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="d7e60-170">Is Indexed</span></span>             | <span data-ttu-id="d7e60-171">Falso</span><span class="sxs-lookup"><span data-stu-id="d7e60-171">False</span></span>                                                                                                                           |
| <span data-ttu-id="d7e60-172">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="d7e60-172">In Global Catalog</span></span>      | <span data-ttu-id="d7e60-173">Falso</span><span class="sxs-lookup"><span data-stu-id="d7e60-173">False</span></span>                                                                                                                           |
| <span data-ttu-id="d7e60-174">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="d7e60-174">NT-Security-Descriptor</span></span> | <span data-ttu-id="d7e60-175">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="d7e60-175">O:BAG:BAD:S:</span></span>                                                                                                                    |
| <span data-ttu-id="d7e60-176">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d7e60-176">Range-Lower</span></span>            | \-                                                                                                                              |
| <span data-ttu-id="d7e60-177">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d7e60-177">Range-Upper</span></span>            | \-                                                                                                                              |
| <span data-ttu-id="d7e60-178">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d7e60-178">Search-Flags</span></span>           | <span data-ttu-id="d7e60-179">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d7e60-179">0x00000000</span></span>                                                                                                                      |
| <span data-ttu-id="d7e60-180">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d7e60-180">System-Flags</span></span>           | <span data-ttu-id="d7e60-181">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d7e60-181">0x00000010</span></span>                                                                                                                      |
| <span data-ttu-id="d7e60-182">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="d7e60-182">Classes used in</span></span>        | [<span data-ttu-id="d7e60-183">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="d7e60-183">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> [<span data-ttu-id="d7e60-184">**Membro NTFRS**</span><span class="sxs-lookup"><span data-stu-id="d7e60-184">**NTFRS-Member**</span></span>](c-ntfrsmember.md)<br/> [<span data-ttu-id="d7e60-185">**Server**</span><span class="sxs-lookup"><span data-stu-id="d7e60-185">**Server**</span></span>](c-server.md)<br/> |



## <a name="adam"></a><span data-ttu-id="d7e60-186">ADAM</span><span class="sxs-lookup"><span data-stu-id="d7e60-186">ADAM</span></span>



| <span data-ttu-id="d7e60-187">Voce</span><span class="sxs-lookup"><span data-stu-id="d7e60-187">Entry</span></span> | <span data-ttu-id="d7e60-188">Valore</span><span class="sxs-lookup"><span data-stu-id="d7e60-188">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="d7e60-189">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="d7e60-189">Link-Id</span></span>                | <span data-ttu-id="d7e60-190">94</span><span class="sxs-lookup"><span data-stu-id="d7e60-190">94</span></span>                                                                             |
| <span data-ttu-id="d7e60-191">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d7e60-191">MAPI-Id</span></span>                | \-                                                                             |
| <span data-ttu-id="d7e60-192">System-Only</span><span class="sxs-lookup"><span data-stu-id="d7e60-192">System-Only</span></span>            | <span data-ttu-id="d7e60-193">Falso</span><span class="sxs-lookup"><span data-stu-id="d7e60-193">False</span></span>                                                                          |
| <span data-ttu-id="d7e60-194">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="d7e60-194">Is-Single-Valued</span></span>       | <span data-ttu-id="d7e60-195">Vero</span><span class="sxs-lookup"><span data-stu-id="d7e60-195">True</span></span>                                                                           |
| <span data-ttu-id="d7e60-196">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="d7e60-196">Is Indexed</span></span>             | <span data-ttu-id="d7e60-197">Falso</span><span class="sxs-lookup"><span data-stu-id="d7e60-197">False</span></span>                                                                          |
| <span data-ttu-id="d7e60-198">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="d7e60-198">In Global Catalog</span></span>      | <span data-ttu-id="d7e60-199">Falso</span><span class="sxs-lookup"><span data-stu-id="d7e60-199">False</span></span>                                                                          |
| <span data-ttu-id="d7e60-200">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="d7e60-200">NT-Security-Descriptor</span></span> | <span data-ttu-id="d7e60-201">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="d7e60-201">O:BAG:BAD:S:</span></span>                                                                   |
| <span data-ttu-id="d7e60-202">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d7e60-202">Range-Lower</span></span>            | \-                                                                             |
| <span data-ttu-id="d7e60-203">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d7e60-203">Range-Upper</span></span>            | \-                                                                             |
| <span data-ttu-id="d7e60-204">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d7e60-204">Search-Flags</span></span>           | <span data-ttu-id="d7e60-205">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d7e60-205">0x00000000</span></span>                                                                     |
| <span data-ttu-id="d7e60-206">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d7e60-206">System-Flags</span></span>           | <span data-ttu-id="d7e60-207">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d7e60-207">0x00000010</span></span>                                                                     |
| <span data-ttu-id="d7e60-208">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="d7e60-208">Classes used in</span></span>        | [<span data-ttu-id="d7e60-209">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="d7e60-209">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> [<span data-ttu-id="d7e60-210">**Server**</span><span class="sxs-lookup"><span data-stu-id="d7e60-210">**Server**</span></span>](c-server.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="d7e60-211">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="d7e60-211">Windows Server 2003 R2</span></span>



| <span data-ttu-id="d7e60-212">Voce</span><span class="sxs-lookup"><span data-stu-id="d7e60-212">Entry</span></span> | <span data-ttu-id="d7e60-213">Valore</span><span class="sxs-lookup"><span data-stu-id="d7e60-213">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7e60-214">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="d7e60-214">Link-Id</span></span>                | <span data-ttu-id="d7e60-215">94</span><span class="sxs-lookup"><span data-stu-id="d7e60-215">94</span></span>                                                                                                                              |
| <span data-ttu-id="d7e60-216">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d7e60-216">MAPI-Id</span></span>                | \-                                                                                                                              |
| <span data-ttu-id="d7e60-217">System-Only</span><span class="sxs-lookup"><span data-stu-id="d7e60-217">System-Only</span></span>            | <span data-ttu-id="d7e60-218">Falso</span><span class="sxs-lookup"><span data-stu-id="d7e60-218">False</span></span>                                                                                                                           |
| <span data-ttu-id="d7e60-219">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="d7e60-219">Is-Single-Valued</span></span>       | <span data-ttu-id="d7e60-220">Vero</span><span class="sxs-lookup"><span data-stu-id="d7e60-220">True</span></span>                                                                                                                            |
| <span data-ttu-id="d7e60-221">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="d7e60-221">Is Indexed</span></span>             | <span data-ttu-id="d7e60-222">Falso</span><span class="sxs-lookup"><span data-stu-id="d7e60-222">False</span></span>                                                                                                                           |
| <span data-ttu-id="d7e60-223">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="d7e60-223">In Global Catalog</span></span>      | <span data-ttu-id="d7e60-224">Falso</span><span class="sxs-lookup"><span data-stu-id="d7e60-224">False</span></span>                                                                                                                           |
| <span data-ttu-id="d7e60-225">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="d7e60-225">NT-Security-Descriptor</span></span> | <span data-ttu-id="d7e60-226">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="d7e60-226">O:BAG:BAD:S:</span></span>                                                                                                                    |
| <span data-ttu-id="d7e60-227">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d7e60-227">Range-Lower</span></span>            | \-                                                                                                                              |
| <span data-ttu-id="d7e60-228">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d7e60-228">Range-Upper</span></span>            | \-                                                                                                                              |
| <span data-ttu-id="d7e60-229">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d7e60-229">Search-Flags</span></span>           | <span data-ttu-id="d7e60-230">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d7e60-230">0x00000000</span></span>                                                                                                                      |
| <span data-ttu-id="d7e60-231">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d7e60-231">System-Flags</span></span>           | <span data-ttu-id="d7e60-232">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d7e60-232">0x00000010</span></span>                                                                                                                      |
| <span data-ttu-id="d7e60-233">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="d7e60-233">Classes used in</span></span>        | [<span data-ttu-id="d7e60-234">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="d7e60-234">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> [<span data-ttu-id="d7e60-235">**Membro NTFRS**</span><span class="sxs-lookup"><span data-stu-id="d7e60-235">**NTFRS-Member**</span></span>](c-ntfrsmember.md)<br/> [<span data-ttu-id="d7e60-236">**Server**</span><span class="sxs-lookup"><span data-stu-id="d7e60-236">**Server**</span></span>](c-server.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="d7e60-237">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d7e60-237">Windows Server 2008</span></span>



| <span data-ttu-id="d7e60-238">Voce</span><span class="sxs-lookup"><span data-stu-id="d7e60-238">Entry</span></span> | <span data-ttu-id="d7e60-239">Valore</span><span class="sxs-lookup"><span data-stu-id="d7e60-239">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7e60-240">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="d7e60-240">Link-Id</span></span>                | <span data-ttu-id="d7e60-241">94</span><span class="sxs-lookup"><span data-stu-id="d7e60-241">94</span></span>                                                                                                                              |
| <span data-ttu-id="d7e60-242">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d7e60-242">MAPI-Id</span></span>                | \-                                                                                                                              |
| <span data-ttu-id="d7e60-243">System-Only</span><span class="sxs-lookup"><span data-stu-id="d7e60-243">System-Only</span></span>            | <span data-ttu-id="d7e60-244">Falso</span><span class="sxs-lookup"><span data-stu-id="d7e60-244">False</span></span>                                                                                                                           |
| <span data-ttu-id="d7e60-245">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="d7e60-245">Is-Single-Valued</span></span>       | <span data-ttu-id="d7e60-246">Vero</span><span class="sxs-lookup"><span data-stu-id="d7e60-246">True</span></span>                                                                                                                            |
| <span data-ttu-id="d7e60-247">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="d7e60-247">Is Indexed</span></span>             | <span data-ttu-id="d7e60-248">Falso</span><span class="sxs-lookup"><span data-stu-id="d7e60-248">False</span></span>                                                                                                                           |
| <span data-ttu-id="d7e60-249">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="d7e60-249">In Global Catalog</span></span>      | <span data-ttu-id="d7e60-250">Falso</span><span class="sxs-lookup"><span data-stu-id="d7e60-250">False</span></span>                                                                                                                           |
| <span data-ttu-id="d7e60-251">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="d7e60-251">NT-Security-Descriptor</span></span> | <span data-ttu-id="d7e60-252">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="d7e60-252">O:BAG:BAD:S:</span></span>                                                                                                                    |
| <span data-ttu-id="d7e60-253">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d7e60-253">Range-Lower</span></span>            | \-                                                                                                                              |
| <span data-ttu-id="d7e60-254">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d7e60-254">Range-Upper</span></span>            | \-                                                                                                                              |
| <span data-ttu-id="d7e60-255">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d7e60-255">Search-Flags</span></span>           | <span data-ttu-id="d7e60-256">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d7e60-256">0x00000000</span></span>                                                                                                                      |
| <span data-ttu-id="d7e60-257">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d7e60-257">System-Flags</span></span>           | <span data-ttu-id="d7e60-258">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d7e60-258">0x00000010</span></span>                                                                                                                      |
| <span data-ttu-id="d7e60-259">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="d7e60-259">Classes used in</span></span>        | [<span data-ttu-id="d7e60-260">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="d7e60-260">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> [<span data-ttu-id="d7e60-261">**Membro NTFRS**</span><span class="sxs-lookup"><span data-stu-id="d7e60-261">**NTFRS-Member**</span></span>](c-ntfrsmember.md)<br/> [<span data-ttu-id="d7e60-262">**Server**</span><span class="sxs-lookup"><span data-stu-id="d7e60-262">**Server**</span></span>](c-server.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="d7e60-263">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d7e60-263">Windows Server 2008 R2</span></span>



| <span data-ttu-id="d7e60-264">Voce</span><span class="sxs-lookup"><span data-stu-id="d7e60-264">Entry</span></span> | <span data-ttu-id="d7e60-265">Valore</span><span class="sxs-lookup"><span data-stu-id="d7e60-265">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7e60-266">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="d7e60-266">Link-Id</span></span>                | <span data-ttu-id="d7e60-267">94</span><span class="sxs-lookup"><span data-stu-id="d7e60-267">94</span></span>                                                                                                                              |
| <span data-ttu-id="d7e60-268">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d7e60-268">MAPI-Id</span></span>                | \-                                                                                                                              |
| <span data-ttu-id="d7e60-269">System-Only</span><span class="sxs-lookup"><span data-stu-id="d7e60-269">System-Only</span></span>            | <span data-ttu-id="d7e60-270">Falso</span><span class="sxs-lookup"><span data-stu-id="d7e60-270">False</span></span>                                                                                                                           |
| <span data-ttu-id="d7e60-271">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="d7e60-271">Is-Single-Valued</span></span>       | <span data-ttu-id="d7e60-272">Vero</span><span class="sxs-lookup"><span data-stu-id="d7e60-272">True</span></span>                                                                                                                            |
| <span data-ttu-id="d7e60-273">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="d7e60-273">Is Indexed</span></span>             | <span data-ttu-id="d7e60-274">Falso</span><span class="sxs-lookup"><span data-stu-id="d7e60-274">False</span></span>                                                                                                                           |
| <span data-ttu-id="d7e60-275">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="d7e60-275">In Global Catalog</span></span>      | <span data-ttu-id="d7e60-276">Falso</span><span class="sxs-lookup"><span data-stu-id="d7e60-276">False</span></span>                                                                                                                           |
| <span data-ttu-id="d7e60-277">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="d7e60-277">NT-Security-Descriptor</span></span> | <span data-ttu-id="d7e60-278">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="d7e60-278">O:BAG:BAD:S:</span></span>                                                                                                                    |
| <span data-ttu-id="d7e60-279">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d7e60-279">Range-Lower</span></span>            | \-                                                                                                                              |
| <span data-ttu-id="d7e60-280">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d7e60-280">Range-Upper</span></span>            | \-                                                                                                                              |
| <span data-ttu-id="d7e60-281">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d7e60-281">Search-Flags</span></span>           | <span data-ttu-id="d7e60-282">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d7e60-282">0x00000000</span></span>                                                                                                                      |
| <span data-ttu-id="d7e60-283">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d7e60-283">System-Flags</span></span>           | <span data-ttu-id="d7e60-284">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d7e60-284">0x00000010</span></span>                                                                                                                      |
| <span data-ttu-id="d7e60-285">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="d7e60-285">Classes used in</span></span>        | [<span data-ttu-id="d7e60-286">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="d7e60-286">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> [<span data-ttu-id="d7e60-287">**Membro NTFRS**</span><span class="sxs-lookup"><span data-stu-id="d7e60-287">**NTFRS-Member**</span></span>](c-ntfrsmember.md)<br/> [<span data-ttu-id="d7e60-288">**Server**</span><span class="sxs-lookup"><span data-stu-id="d7e60-288">**Server**</span></span>](c-server.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="d7e60-289">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d7e60-289">Windows Server 2012</span></span>



| <span data-ttu-id="d7e60-290">Voce</span><span class="sxs-lookup"><span data-stu-id="d7e60-290">Entry</span></span> | <span data-ttu-id="d7e60-291">Valore</span><span class="sxs-lookup"><span data-stu-id="d7e60-291">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7e60-292">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="d7e60-292">Link-Id</span></span>                | <span data-ttu-id="d7e60-293">94</span><span class="sxs-lookup"><span data-stu-id="d7e60-293">94</span></span>                                                                                                                              |
| <span data-ttu-id="d7e60-294">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d7e60-294">MAPI-Id</span></span>                | \-                                                                                                                              |
| <span data-ttu-id="d7e60-295">System-Only</span><span class="sxs-lookup"><span data-stu-id="d7e60-295">System-Only</span></span>            | <span data-ttu-id="d7e60-296">Falso</span><span class="sxs-lookup"><span data-stu-id="d7e60-296">False</span></span>                                                                                                                           |
| <span data-ttu-id="d7e60-297">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="d7e60-297">Is-Single-Valued</span></span>       | <span data-ttu-id="d7e60-298">Vero</span><span class="sxs-lookup"><span data-stu-id="d7e60-298">True</span></span>                                                                                                                            |
| <span data-ttu-id="d7e60-299">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="d7e60-299">Is Indexed</span></span>             | <span data-ttu-id="d7e60-300">Falso</span><span class="sxs-lookup"><span data-stu-id="d7e60-300">False</span></span>                                                                                                                           |
| <span data-ttu-id="d7e60-301">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="d7e60-301">In Global Catalog</span></span>      | <span data-ttu-id="d7e60-302">Falso</span><span class="sxs-lookup"><span data-stu-id="d7e60-302">False</span></span>                                                                                                                           |
| <span data-ttu-id="d7e60-303">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="d7e60-303">NT-Security-Descriptor</span></span> | <span data-ttu-id="d7e60-304">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="d7e60-304">O:BAG:BAD:S:</span></span>                                                                                                                    |
| <span data-ttu-id="d7e60-305">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d7e60-305">Range-Lower</span></span>            | \-                                                                                                                              |
| <span data-ttu-id="d7e60-306">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d7e60-306">Range-Upper</span></span>            | \-                                                                                                                              |
| <span data-ttu-id="d7e60-307">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d7e60-307">Search-Flags</span></span>           | <span data-ttu-id="d7e60-308">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d7e60-308">0x00000000</span></span>                                                                                                                      |
| <span data-ttu-id="d7e60-309">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d7e60-309">System-Flags</span></span>           | <span data-ttu-id="d7e60-310">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d7e60-310">0x00000010</span></span>                                                                                                                      |
| <span data-ttu-id="d7e60-311">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="d7e60-311">Classes used in</span></span>        | [<span data-ttu-id="d7e60-312">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="d7e60-312">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> [<span data-ttu-id="d7e60-313">**Membro NTFRS**</span><span class="sxs-lookup"><span data-stu-id="d7e60-313">**NTFRS-Member**</span></span>](c-ntfrsmember.md)<br/> [<span data-ttu-id="d7e60-314">**Server**</span><span class="sxs-lookup"><span data-stu-id="d7e60-314">**Server**</span></span>](c-server.md)<br/> |



 

 





