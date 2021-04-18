---
title: Initializes (attributo)
description: Contiene le iniziali per parti del nome completo dell'utente. Questa operazione può essere utilizzata come iniziale intermedia nella Rubrica di Windows.
ms.assetid: 220b4448-5276-4c3f-8a1b-217cec06135a
ms.tgt_platform: multiple
keywords:
- Attributo iniziale-schema AD
- attributo iniziale-schema AD
topic_type:
- apiref
api_name:
- Initials
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 946f6c9633c1126a30ae4898274096a54db9a402
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "106303340"
---
# <a name="initials-attribute"></a><span data-ttu-id="e5cb7-106">Initializes (attributo)</span><span class="sxs-lookup"><span data-stu-id="e5cb7-106">Initials attribute</span></span>

<span data-ttu-id="e5cb7-107">Contiene le iniziali per parti del nome completo dell'utente.</span><span class="sxs-lookup"><span data-stu-id="e5cb7-107">Contains the initials for parts of the user's full name.</span></span> <span data-ttu-id="e5cb7-108">Questa operazione può essere utilizzata come iniziale intermedia nella Rubrica di Windows.</span><span class="sxs-lookup"><span data-stu-id="e5cb7-108">This may be used as the middle initial in the Windows Address Book.</span></span>



| <span data-ttu-id="e5cb7-109">Voce</span><span class="sxs-lookup"><span data-stu-id="e5cb7-109">Entry</span></span> | <span data-ttu-id="e5cb7-110">Valore</span><span class="sxs-lookup"><span data-stu-id="e5cb7-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="e5cb7-111">CN</span><span class="sxs-lookup"><span data-stu-id="e5cb7-111">CN</span></span>                | <span data-ttu-id="e5cb7-112">Iniziali</span><span class="sxs-lookup"><span data-stu-id="e5cb7-112">Initials</span></span>                                    |
| <span data-ttu-id="e5cb7-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="e5cb7-113">Ldap-Display-Name</span></span> | <span data-ttu-id="e5cb7-114">Initials</span><span class="sxs-lookup"><span data-stu-id="e5cb7-114">initials</span></span>                                    |
| <span data-ttu-id="e5cb7-115">Dimensione</span><span class="sxs-lookup"><span data-stu-id="e5cb7-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="e5cb7-116">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="e5cb7-116">Update Privilege</span></span>  | <span data-ttu-id="e5cb7-117">Amministratore di dominio o proprietario dell'account.</span><span class="sxs-lookup"><span data-stu-id="e5cb7-117">Domain administrator or account owner.</span></span>      |
| <span data-ttu-id="e5cb7-118">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="e5cb7-118">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="e5cb7-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e5cb7-119">Attribute-Id</span></span>      | <span data-ttu-id="e5cb7-120">2.5.4.43</span><span class="sxs-lookup"><span data-stu-id="e5cb7-120">2.5.4.43</span></span>                                    |
| <span data-ttu-id="e5cb7-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="e5cb7-121">System-Id-Guid</span></span>    | <span data-ttu-id="e5cb7-122">f0f8ff90-1191-11d0-a060-00aa006c33ed</span><span class="sxs-lookup"><span data-stu-id="e5cb7-122">f0f8ff90-1191-11d0-a060-00aa006c33ed</span></span>        |
| <span data-ttu-id="e5cb7-123">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e5cb7-123">Syntax</span></span>            | [<span data-ttu-id="e5cb7-124">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="e5cb7-124">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="e5cb7-125">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="e5cb7-125">Implementations</span></span>

-   [<span data-ttu-id="e5cb7-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="e5cb7-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="e5cb7-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e5cb7-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e5cb7-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e5cb7-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e5cb7-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e5cb7-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e5cb7-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e5cb7-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e5cb7-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e5cb7-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="e5cb7-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e5cb7-132">Windows 2000 Server</span></span>



| <span data-ttu-id="e5cb7-133">Voce</span><span class="sxs-lookup"><span data-stu-id="e5cb7-133">Entry</span></span> | <span data-ttu-id="e5cb7-134">Valore</span><span class="sxs-lookup"><span data-stu-id="e5cb7-134">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="e5cb7-135">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="e5cb7-135">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="e5cb7-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e5cb7-136">MAPI-Id</span></span>                | <span data-ttu-id="e5cb7-137">0x3A0A</span><span class="sxs-lookup"><span data-stu-id="e5cb7-137">0x3A0A</span></span>                                                             |
| <span data-ttu-id="e5cb7-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="e5cb7-138">System-Only</span></span>            | <span data-ttu-id="e5cb7-139">Falso</span><span class="sxs-lookup"><span data-stu-id="e5cb7-139">False</span></span>                                                              |
| <span data-ttu-id="e5cb7-140">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="e5cb7-140">Is-Single-Valued</span></span>       | <span data-ttu-id="e5cb7-141">Vero</span><span class="sxs-lookup"><span data-stu-id="e5cb7-141">True</span></span>                                                               |
| <span data-ttu-id="e5cb7-142">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="e5cb7-142">Is Indexed</span></span>             | <span data-ttu-id="e5cb7-143">Falso</span><span class="sxs-lookup"><span data-stu-id="e5cb7-143">False</span></span>                                                              |
| <span data-ttu-id="e5cb7-144">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="e5cb7-144">In Global Catalog</span></span>      | <span data-ttu-id="e5cb7-145">Falso</span><span class="sxs-lookup"><span data-stu-id="e5cb7-145">False</span></span>                                                              |
| <span data-ttu-id="e5cb7-146">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="e5cb7-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="e5cb7-147">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="e5cb7-147">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="e5cb7-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e5cb7-148">Range-Lower</span></span>            | <span data-ttu-id="e5cb7-149">1</span><span class="sxs-lookup"><span data-stu-id="e5cb7-149">1</span></span>                                                                  |
| <span data-ttu-id="e5cb7-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e5cb7-150">Range-Upper</span></span>            | <span data-ttu-id="e5cb7-151">6</span><span class="sxs-lookup"><span data-stu-id="e5cb7-151">6</span></span>                                                                  |
| <span data-ttu-id="e5cb7-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e5cb7-152">Search-Flags</span></span>           | <span data-ttu-id="e5cb7-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e5cb7-153">0x00000000</span></span>                                                         |
| <span data-ttu-id="e5cb7-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e5cb7-154">System-Flags</span></span>           | <span data-ttu-id="e5cb7-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e5cb7-155">0x00000010</span></span>                                                         |
| <span data-ttu-id="e5cb7-156">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="e5cb7-156">Classes used in</span></span>        | [<span data-ttu-id="e5cb7-157">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="e5cb7-157">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="e5cb7-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e5cb7-158">Windows Server 2003</span></span>



| <span data-ttu-id="e5cb7-159">Voce</span><span class="sxs-lookup"><span data-stu-id="e5cb7-159">Entry</span></span> | <span data-ttu-id="e5cb7-160">Valore</span><span class="sxs-lookup"><span data-stu-id="e5cb7-160">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5cb7-161">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="e5cb7-161">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="e5cb7-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e5cb7-162">MAPI-Id</span></span>                | <span data-ttu-id="e5cb7-163">0x3A0A</span><span class="sxs-lookup"><span data-stu-id="e5cb7-163">0x3A0A</span></span>                                                                                                                 |
| <span data-ttu-id="e5cb7-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="e5cb7-164">System-Only</span></span>            | <span data-ttu-id="e5cb7-165">Falso</span><span class="sxs-lookup"><span data-stu-id="e5cb7-165">False</span></span>                                                                                                                  |
| <span data-ttu-id="e5cb7-166">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="e5cb7-166">Is-Single-Valued</span></span>       | <span data-ttu-id="e5cb7-167">Vero</span><span class="sxs-lookup"><span data-stu-id="e5cb7-167">True</span></span>                                                                                                                   |
| <span data-ttu-id="e5cb7-168">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="e5cb7-168">Is Indexed</span></span>             | <span data-ttu-id="e5cb7-169">Falso</span><span class="sxs-lookup"><span data-stu-id="e5cb7-169">False</span></span>                                                                                                                  |
| <span data-ttu-id="e5cb7-170">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="e5cb7-170">In Global Catalog</span></span>      | <span data-ttu-id="e5cb7-171">Falso</span><span class="sxs-lookup"><span data-stu-id="e5cb7-171">False</span></span>                                                                                                                  |
| <span data-ttu-id="e5cb7-172">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="e5cb7-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="e5cb7-173">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="e5cb7-173">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="e5cb7-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e5cb7-174">Range-Lower</span></span>            | <span data-ttu-id="e5cb7-175">1</span><span class="sxs-lookup"><span data-stu-id="e5cb7-175">1</span></span>                                                                                                                      |
| <span data-ttu-id="e5cb7-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e5cb7-176">Range-Upper</span></span>            | <span data-ttu-id="e5cb7-177">6</span><span class="sxs-lookup"><span data-stu-id="e5cb7-177">6</span></span>                                                                                                                      |
| <span data-ttu-id="e5cb7-178">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e5cb7-178">Search-Flags</span></span>           | <span data-ttu-id="e5cb7-179">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e5cb7-179">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="e5cb7-180">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e5cb7-180">System-Flags</span></span>           | <span data-ttu-id="e5cb7-181">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e5cb7-181">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="e5cb7-182">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="e5cb7-182">Classes used in</span></span>        | [<span data-ttu-id="e5cb7-183">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="e5cb7-183">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="e5cb7-184">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="e5cb7-184">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e5cb7-185">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e5cb7-185">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e5cb7-186">Voce</span><span class="sxs-lookup"><span data-stu-id="e5cb7-186">Entry</span></span> | <span data-ttu-id="e5cb7-187">Valore</span><span class="sxs-lookup"><span data-stu-id="e5cb7-187">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5cb7-188">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="e5cb7-188">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="e5cb7-189">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e5cb7-189">MAPI-Id</span></span>                | <span data-ttu-id="e5cb7-190">0x3A0A</span><span class="sxs-lookup"><span data-stu-id="e5cb7-190">0x3A0A</span></span>                                                                                                                 |
| <span data-ttu-id="e5cb7-191">System-Only</span><span class="sxs-lookup"><span data-stu-id="e5cb7-191">System-Only</span></span>            | <span data-ttu-id="e5cb7-192">Falso</span><span class="sxs-lookup"><span data-stu-id="e5cb7-192">False</span></span>                                                                                                                  |
| <span data-ttu-id="e5cb7-193">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="e5cb7-193">Is-Single-Valued</span></span>       | <span data-ttu-id="e5cb7-194">Vero</span><span class="sxs-lookup"><span data-stu-id="e5cb7-194">True</span></span>                                                                                                                   |
| <span data-ttu-id="e5cb7-195">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="e5cb7-195">Is Indexed</span></span>             | <span data-ttu-id="e5cb7-196">Falso</span><span class="sxs-lookup"><span data-stu-id="e5cb7-196">False</span></span>                                                                                                                  |
| <span data-ttu-id="e5cb7-197">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="e5cb7-197">In Global Catalog</span></span>      | <span data-ttu-id="e5cb7-198">Falso</span><span class="sxs-lookup"><span data-stu-id="e5cb7-198">False</span></span>                                                                                                                  |
| <span data-ttu-id="e5cb7-199">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="e5cb7-199">NT-Security-Descriptor</span></span> | <span data-ttu-id="e5cb7-200">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="e5cb7-200">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="e5cb7-201">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e5cb7-201">Range-Lower</span></span>            | <span data-ttu-id="e5cb7-202">1</span><span class="sxs-lookup"><span data-stu-id="e5cb7-202">1</span></span>                                                                                                                      |
| <span data-ttu-id="e5cb7-203">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e5cb7-203">Range-Upper</span></span>            | <span data-ttu-id="e5cb7-204">6</span><span class="sxs-lookup"><span data-stu-id="e5cb7-204">6</span></span>                                                                                                                      |
| <span data-ttu-id="e5cb7-205">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e5cb7-205">Search-Flags</span></span>           | <span data-ttu-id="e5cb7-206">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e5cb7-206">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="e5cb7-207">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e5cb7-207">System-Flags</span></span>           | <span data-ttu-id="e5cb7-208">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e5cb7-208">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="e5cb7-209">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="e5cb7-209">Classes used in</span></span>        | [<span data-ttu-id="e5cb7-210">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="e5cb7-210">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="e5cb7-211">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="e5cb7-211">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="e5cb7-212">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e5cb7-212">Windows Server 2008</span></span>



| <span data-ttu-id="e5cb7-213">Voce</span><span class="sxs-lookup"><span data-stu-id="e5cb7-213">Entry</span></span> | <span data-ttu-id="e5cb7-214">Valore</span><span class="sxs-lookup"><span data-stu-id="e5cb7-214">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5cb7-215">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="e5cb7-215">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="e5cb7-216">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e5cb7-216">MAPI-Id</span></span>                | <span data-ttu-id="e5cb7-217">0x3A0A</span><span class="sxs-lookup"><span data-stu-id="e5cb7-217">0x3A0A</span></span>                                                                                                                 |
| <span data-ttu-id="e5cb7-218">System-Only</span><span class="sxs-lookup"><span data-stu-id="e5cb7-218">System-Only</span></span>            | <span data-ttu-id="e5cb7-219">Falso</span><span class="sxs-lookup"><span data-stu-id="e5cb7-219">False</span></span>                                                                                                                  |
| <span data-ttu-id="e5cb7-220">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="e5cb7-220">Is-Single-Valued</span></span>       | <span data-ttu-id="e5cb7-221">Vero</span><span class="sxs-lookup"><span data-stu-id="e5cb7-221">True</span></span>                                                                                                                   |
| <span data-ttu-id="e5cb7-222">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="e5cb7-222">Is Indexed</span></span>             | <span data-ttu-id="e5cb7-223">Falso</span><span class="sxs-lookup"><span data-stu-id="e5cb7-223">False</span></span>                                                                                                                  |
| <span data-ttu-id="e5cb7-224">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="e5cb7-224">In Global Catalog</span></span>      | <span data-ttu-id="e5cb7-225">Falso</span><span class="sxs-lookup"><span data-stu-id="e5cb7-225">False</span></span>                                                                                                                  |
| <span data-ttu-id="e5cb7-226">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="e5cb7-226">NT-Security-Descriptor</span></span> | <span data-ttu-id="e5cb7-227">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="e5cb7-227">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="e5cb7-228">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e5cb7-228">Range-Lower</span></span>            | <span data-ttu-id="e5cb7-229">1</span><span class="sxs-lookup"><span data-stu-id="e5cb7-229">1</span></span>                                                                                                                      |
| <span data-ttu-id="e5cb7-230">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e5cb7-230">Range-Upper</span></span>            | <span data-ttu-id="e5cb7-231">6</span><span class="sxs-lookup"><span data-stu-id="e5cb7-231">6</span></span>                                                                                                                      |
| <span data-ttu-id="e5cb7-232">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e5cb7-232">Search-Flags</span></span>           | <span data-ttu-id="e5cb7-233">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e5cb7-233">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="e5cb7-234">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e5cb7-234">System-Flags</span></span>           | <span data-ttu-id="e5cb7-235">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e5cb7-235">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="e5cb7-236">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="e5cb7-236">Classes used in</span></span>        | [<span data-ttu-id="e5cb7-237">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="e5cb7-237">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="e5cb7-238">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="e5cb7-238">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e5cb7-239">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e5cb7-239">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e5cb7-240">Voce</span><span class="sxs-lookup"><span data-stu-id="e5cb7-240">Entry</span></span> | <span data-ttu-id="e5cb7-241">Valore</span><span class="sxs-lookup"><span data-stu-id="e5cb7-241">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5cb7-242">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="e5cb7-242">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="e5cb7-243">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e5cb7-243">MAPI-Id</span></span>                | <span data-ttu-id="e5cb7-244">0x3A0A</span><span class="sxs-lookup"><span data-stu-id="e5cb7-244">0x3A0A</span></span>                                                                                                                 |
| <span data-ttu-id="e5cb7-245">System-Only</span><span class="sxs-lookup"><span data-stu-id="e5cb7-245">System-Only</span></span>            | <span data-ttu-id="e5cb7-246">Falso</span><span class="sxs-lookup"><span data-stu-id="e5cb7-246">False</span></span>                                                                                                                  |
| <span data-ttu-id="e5cb7-247">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="e5cb7-247">Is-Single-Valued</span></span>       | <span data-ttu-id="e5cb7-248">Vero</span><span class="sxs-lookup"><span data-stu-id="e5cb7-248">True</span></span>                                                                                                                   |
| <span data-ttu-id="e5cb7-249">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="e5cb7-249">Is Indexed</span></span>             | <span data-ttu-id="e5cb7-250">Falso</span><span class="sxs-lookup"><span data-stu-id="e5cb7-250">False</span></span>                                                                                                                  |
| <span data-ttu-id="e5cb7-251">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="e5cb7-251">In Global Catalog</span></span>      | <span data-ttu-id="e5cb7-252">Falso</span><span class="sxs-lookup"><span data-stu-id="e5cb7-252">False</span></span>                                                                                                                  |
| <span data-ttu-id="e5cb7-253">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="e5cb7-253">NT-Security-Descriptor</span></span> | <span data-ttu-id="e5cb7-254">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="e5cb7-254">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="e5cb7-255">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e5cb7-255">Range-Lower</span></span>            | <span data-ttu-id="e5cb7-256">1</span><span class="sxs-lookup"><span data-stu-id="e5cb7-256">1</span></span>                                                                                                                      |
| <span data-ttu-id="e5cb7-257">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e5cb7-257">Range-Upper</span></span>            | <span data-ttu-id="e5cb7-258">6</span><span class="sxs-lookup"><span data-stu-id="e5cb7-258">6</span></span>                                                                                                                      |
| <span data-ttu-id="e5cb7-259">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e5cb7-259">Search-Flags</span></span>           | <span data-ttu-id="e5cb7-260">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e5cb7-260">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="e5cb7-261">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e5cb7-261">System-Flags</span></span>           | <span data-ttu-id="e5cb7-262">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e5cb7-262">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="e5cb7-263">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="e5cb7-263">Classes used in</span></span>        | [<span data-ttu-id="e5cb7-264">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="e5cb7-264">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="e5cb7-265">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="e5cb7-265">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e5cb7-266">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e5cb7-266">Windows Server 2012</span></span>



| <span data-ttu-id="e5cb7-267">Voce</span><span class="sxs-lookup"><span data-stu-id="e5cb7-267">Entry</span></span> | <span data-ttu-id="e5cb7-268">Valore</span><span class="sxs-lookup"><span data-stu-id="e5cb7-268">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5cb7-269">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="e5cb7-269">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="e5cb7-270">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e5cb7-270">MAPI-Id</span></span>                | <span data-ttu-id="e5cb7-271">0x3A0A</span><span class="sxs-lookup"><span data-stu-id="e5cb7-271">0x3A0A</span></span>                                                                                                                 |
| <span data-ttu-id="e5cb7-272">System-Only</span><span class="sxs-lookup"><span data-stu-id="e5cb7-272">System-Only</span></span>            | <span data-ttu-id="e5cb7-273">Falso</span><span class="sxs-lookup"><span data-stu-id="e5cb7-273">False</span></span>                                                                                                                  |
| <span data-ttu-id="e5cb7-274">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="e5cb7-274">Is-Single-Valued</span></span>       | <span data-ttu-id="e5cb7-275">Vero</span><span class="sxs-lookup"><span data-stu-id="e5cb7-275">True</span></span>                                                                                                                   |
| <span data-ttu-id="e5cb7-276">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="e5cb7-276">Is Indexed</span></span>             | <span data-ttu-id="e5cb7-277">Falso</span><span class="sxs-lookup"><span data-stu-id="e5cb7-277">False</span></span>                                                                                                                  |
| <span data-ttu-id="e5cb7-278">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="e5cb7-278">In Global Catalog</span></span>      | <span data-ttu-id="e5cb7-279">Falso</span><span class="sxs-lookup"><span data-stu-id="e5cb7-279">False</span></span>                                                                                                                  |
| <span data-ttu-id="e5cb7-280">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="e5cb7-280">NT-Security-Descriptor</span></span> | <span data-ttu-id="e5cb7-281">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="e5cb7-281">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="e5cb7-282">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e5cb7-282">Range-Lower</span></span>            | <span data-ttu-id="e5cb7-283">1</span><span class="sxs-lookup"><span data-stu-id="e5cb7-283">1</span></span>                                                                                                                      |
| <span data-ttu-id="e5cb7-284">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e5cb7-284">Range-Upper</span></span>            | <span data-ttu-id="e5cb7-285">6</span><span class="sxs-lookup"><span data-stu-id="e5cb7-285">6</span></span>                                                                                                                      |
| <span data-ttu-id="e5cb7-286">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e5cb7-286">Search-Flags</span></span>           | <span data-ttu-id="e5cb7-287">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e5cb7-287">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="e5cb7-288">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e5cb7-288">System-Flags</span></span>           | <span data-ttu-id="e5cb7-289">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e5cb7-289">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="e5cb7-290">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="e5cb7-290">Classes used in</span></span>        | [<span data-ttu-id="e5cb7-291">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="e5cb7-291">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="e5cb7-292">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="e5cb7-292">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



 

 





