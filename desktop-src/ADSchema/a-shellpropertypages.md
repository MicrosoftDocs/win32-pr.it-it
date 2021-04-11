---
title: Attributo Shell-Property-Pages
description: Numero di ordine e GUID delle pagine delle proprietà per la gestione di oggetti Active Directory. È possibile accedere a queste pagine delle proprietà dalla shell di Windows. Per ulteriori informazioni, vedere il documento estensione dell'interfaccia utente per gli oggetti directory.
ms.assetid: e0edd91b-bdb6-47aa-9be2-8a23a89adb26
ms.tgt_platform: multiple
keywords:
- Shell-Property-Pages attributo schema AD
- Schema AD dell'attributo shellPropertyPages
topic_type:
- apiref
api_name:
- Shell-Property-Pages
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: befad2334a754843fa0ae412565db8c82260f7cd
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104122334"
---
# <a name="shell-property-pages-attribute"></a><span data-ttu-id="3c0cc-107">Attributo Shell-Property-Pages</span><span class="sxs-lookup"><span data-stu-id="3c0cc-107">Shell-Property-Pages attribute</span></span>

<span data-ttu-id="3c0cc-108">Numero di ordine e GUID delle pagine delle proprietà per la gestione di oggetti Active Directory.</span><span class="sxs-lookup"><span data-stu-id="3c0cc-108">The order number and GUID of property pages for managing Active Directory objects.</span></span> <span data-ttu-id="3c0cc-109">È possibile accedere a queste pagine delle proprietà dalla shell di Windows.</span><span class="sxs-lookup"><span data-stu-id="3c0cc-109">These property pages can be accessed from the Windows shell.</span></span> <span data-ttu-id="3c0cc-110">Per ulteriori informazioni, vedere il documento estensione dell'interfaccia utente per gli oggetti directory.</span><span class="sxs-lookup"><span data-stu-id="3c0cc-110">For more information see the document, Extending the User Interface for Directory Objects.</span></span>



| <span data-ttu-id="3c0cc-111">Voce</span><span class="sxs-lookup"><span data-stu-id="3c0cc-111">Entry</span></span> | <span data-ttu-id="3c0cc-112">Valore</span><span class="sxs-lookup"><span data-stu-id="3c0cc-112">Value</span></span> |
|-------------------|------------------------------------------------|
| <span data-ttu-id="3c0cc-113">CN</span><span class="sxs-lookup"><span data-stu-id="3c0cc-113">CN</span></span>                | <span data-ttu-id="3c0cc-114">Shell-proprietà-pagine</span><span class="sxs-lookup"><span data-stu-id="3c0cc-114">Shell-Property-Pages</span></span>                           |
| <span data-ttu-id="3c0cc-115">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="3c0cc-115">Ldap-Display-Name</span></span> | <span data-ttu-id="3c0cc-116">shellPropertyPages</span><span class="sxs-lookup"><span data-stu-id="3c0cc-116">shellPropertyPages</span></span>                             |
| <span data-ttu-id="3c0cc-117">Dimensione</span><span class="sxs-lookup"><span data-stu-id="3c0cc-117">Size</span></span>              | \-                                             |
| <span data-ttu-id="3c0cc-118">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="3c0cc-118">Update Privilege</span></span>  | <span data-ttu-id="3c0cc-119">Amministratore di dominio o sviluppatore di applicazioni.</span><span class="sxs-lookup"><span data-stu-id="3c0cc-119">Domain administrator or application developer.</span></span> |
| <span data-ttu-id="3c0cc-120">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="3c0cc-120">Update Frequency</span></span>  | <span data-ttu-id="3c0cc-121">Ogni volta che viene aggiunta o rimossa una pagina delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="3c0cc-121">Whenever a property page is added or removed.</span></span>  |
| <span data-ttu-id="3c0cc-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="3c0cc-122">Attribute-Id</span></span>      | <span data-ttu-id="3c0cc-123">1.2.840.113556.1.4.563</span><span class="sxs-lookup"><span data-stu-id="3c0cc-123">1.2.840.113556.1.4.563</span></span>                         |
| <span data-ttu-id="3c0cc-124">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="3c0cc-124">System-Id-Guid</span></span>    | <span data-ttu-id="3c0cc-125">52458039-ca6a-11D0-AFFF-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="3c0cc-125">52458039-ca6a-11d0-afff-0000f80367c1</span></span>           |
| <span data-ttu-id="3c0cc-126">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3c0cc-126">Syntax</span></span>            | [<span data-ttu-id="3c0cc-127">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="3c0cc-127">**String(Unicode)**</span></span>](s-string-unicode.md)    |



## <a name="implementations"></a><span data-ttu-id="3c0cc-128">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="3c0cc-128">Implementations</span></span>

-   [<span data-ttu-id="3c0cc-129">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="3c0cc-129">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="3c0cc-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="3c0cc-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="3c0cc-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="3c0cc-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="3c0cc-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="3c0cc-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="3c0cc-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="3c0cc-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="3c0cc-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="3c0cc-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="3c0cc-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="3c0cc-135">Windows 2000 Server</span></span>



| <span data-ttu-id="3c0cc-136">Voce</span><span class="sxs-lookup"><span data-stu-id="3c0cc-136">Entry</span></span> | <span data-ttu-id="3c0cc-137">Valore</span><span class="sxs-lookup"><span data-stu-id="3c0cc-137">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="3c0cc-138">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="3c0cc-138">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="3c0cc-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3c0cc-139">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="3c0cc-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="3c0cc-140">System-Only</span></span>            | <span data-ttu-id="3c0cc-141">Falso</span><span class="sxs-lookup"><span data-stu-id="3c0cc-141">False</span></span>                                                      |
| <span data-ttu-id="3c0cc-142">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="3c0cc-142">Is-Single-Valued</span></span>       | <span data-ttu-id="3c0cc-143">Falso</span><span class="sxs-lookup"><span data-stu-id="3c0cc-143">False</span></span>                                                      |
| <span data-ttu-id="3c0cc-144">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="3c0cc-144">Is Indexed</span></span>             | <span data-ttu-id="3c0cc-145">Falso</span><span class="sxs-lookup"><span data-stu-id="3c0cc-145">False</span></span>                                                      |
| <span data-ttu-id="3c0cc-146">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="3c0cc-146">In Global Catalog</span></span>      | <span data-ttu-id="3c0cc-147">Falso</span><span class="sxs-lookup"><span data-stu-id="3c0cc-147">False</span></span>                                                      |
| <span data-ttu-id="3c0cc-148">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="3c0cc-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="3c0cc-149">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="3c0cc-149">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="3c0cc-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3c0cc-150">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="3c0cc-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3c0cc-151">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="3c0cc-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3c0cc-152">Search-Flags</span></span>           | <span data-ttu-id="3c0cc-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3c0cc-153">0x00000000</span></span>                                                 |
| <span data-ttu-id="3c0cc-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3c0cc-154">System-Flags</span></span>           | <span data-ttu-id="3c0cc-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3c0cc-155">0x00000010</span></span>                                                 |
| <span data-ttu-id="3c0cc-156">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="3c0cc-156">Classes used in</span></span>        | [<span data-ttu-id="3c0cc-157">**Display-specifier**</span><span class="sxs-lookup"><span data-stu-id="3c0cc-157">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="3c0cc-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3c0cc-158">Windows Server 2003</span></span>



| <span data-ttu-id="3c0cc-159">Voce</span><span class="sxs-lookup"><span data-stu-id="3c0cc-159">Entry</span></span> | <span data-ttu-id="3c0cc-160">Valore</span><span class="sxs-lookup"><span data-stu-id="3c0cc-160">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="3c0cc-161">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="3c0cc-161">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="3c0cc-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3c0cc-162">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="3c0cc-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="3c0cc-163">System-Only</span></span>            | <span data-ttu-id="3c0cc-164">Falso</span><span class="sxs-lookup"><span data-stu-id="3c0cc-164">False</span></span>                                                      |
| <span data-ttu-id="3c0cc-165">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="3c0cc-165">Is-Single-Valued</span></span>       | <span data-ttu-id="3c0cc-166">Falso</span><span class="sxs-lookup"><span data-stu-id="3c0cc-166">False</span></span>                                                      |
| <span data-ttu-id="3c0cc-167">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="3c0cc-167">Is Indexed</span></span>             | <span data-ttu-id="3c0cc-168">Falso</span><span class="sxs-lookup"><span data-stu-id="3c0cc-168">False</span></span>                                                      |
| <span data-ttu-id="3c0cc-169">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="3c0cc-169">In Global Catalog</span></span>      | <span data-ttu-id="3c0cc-170">Falso</span><span class="sxs-lookup"><span data-stu-id="3c0cc-170">False</span></span>                                                      |
| <span data-ttu-id="3c0cc-171">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="3c0cc-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="3c0cc-172">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="3c0cc-172">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="3c0cc-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3c0cc-173">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="3c0cc-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3c0cc-174">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="3c0cc-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3c0cc-175">Search-Flags</span></span>           | <span data-ttu-id="3c0cc-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3c0cc-176">0x00000000</span></span>                                                 |
| <span data-ttu-id="3c0cc-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3c0cc-177">System-Flags</span></span>           | <span data-ttu-id="3c0cc-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3c0cc-178">0x00000010</span></span>                                                 |
| <span data-ttu-id="3c0cc-179">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="3c0cc-179">Classes used in</span></span>        | [<span data-ttu-id="3c0cc-180">**Display-specifier**</span><span class="sxs-lookup"><span data-stu-id="3c0cc-180">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="3c0cc-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="3c0cc-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="3c0cc-182">Voce</span><span class="sxs-lookup"><span data-stu-id="3c0cc-182">Entry</span></span> | <span data-ttu-id="3c0cc-183">Valore</span><span class="sxs-lookup"><span data-stu-id="3c0cc-183">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="3c0cc-184">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="3c0cc-184">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="3c0cc-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3c0cc-185">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="3c0cc-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="3c0cc-186">System-Only</span></span>            | <span data-ttu-id="3c0cc-187">Falso</span><span class="sxs-lookup"><span data-stu-id="3c0cc-187">False</span></span>                                                      |
| <span data-ttu-id="3c0cc-188">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="3c0cc-188">Is-Single-Valued</span></span>       | <span data-ttu-id="3c0cc-189">Falso</span><span class="sxs-lookup"><span data-stu-id="3c0cc-189">False</span></span>                                                      |
| <span data-ttu-id="3c0cc-190">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="3c0cc-190">Is Indexed</span></span>             | <span data-ttu-id="3c0cc-191">Falso</span><span class="sxs-lookup"><span data-stu-id="3c0cc-191">False</span></span>                                                      |
| <span data-ttu-id="3c0cc-192">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="3c0cc-192">In Global Catalog</span></span>      | <span data-ttu-id="3c0cc-193">Falso</span><span class="sxs-lookup"><span data-stu-id="3c0cc-193">False</span></span>                                                      |
| <span data-ttu-id="3c0cc-194">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="3c0cc-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="3c0cc-195">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="3c0cc-195">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="3c0cc-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3c0cc-196">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="3c0cc-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3c0cc-197">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="3c0cc-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3c0cc-198">Search-Flags</span></span>           | <span data-ttu-id="3c0cc-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3c0cc-199">0x00000000</span></span>                                                 |
| <span data-ttu-id="3c0cc-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3c0cc-200">System-Flags</span></span>           | <span data-ttu-id="3c0cc-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3c0cc-201">0x00000010</span></span>                                                 |
| <span data-ttu-id="3c0cc-202">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="3c0cc-202">Classes used in</span></span>        | [<span data-ttu-id="3c0cc-203">**Display-specifier**</span><span class="sxs-lookup"><span data-stu-id="3c0cc-203">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="3c0cc-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3c0cc-204">Windows Server 2008</span></span>



| <span data-ttu-id="3c0cc-205">Voce</span><span class="sxs-lookup"><span data-stu-id="3c0cc-205">Entry</span></span> | <span data-ttu-id="3c0cc-206">Valore</span><span class="sxs-lookup"><span data-stu-id="3c0cc-206">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="3c0cc-207">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="3c0cc-207">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="3c0cc-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3c0cc-208">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="3c0cc-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="3c0cc-209">System-Only</span></span>            | <span data-ttu-id="3c0cc-210">Falso</span><span class="sxs-lookup"><span data-stu-id="3c0cc-210">False</span></span>                                                      |
| <span data-ttu-id="3c0cc-211">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="3c0cc-211">Is-Single-Valued</span></span>       | <span data-ttu-id="3c0cc-212">Falso</span><span class="sxs-lookup"><span data-stu-id="3c0cc-212">False</span></span>                                                      |
| <span data-ttu-id="3c0cc-213">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="3c0cc-213">Is Indexed</span></span>             | <span data-ttu-id="3c0cc-214">Falso</span><span class="sxs-lookup"><span data-stu-id="3c0cc-214">False</span></span>                                                      |
| <span data-ttu-id="3c0cc-215">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="3c0cc-215">In Global Catalog</span></span>      | <span data-ttu-id="3c0cc-216">Falso</span><span class="sxs-lookup"><span data-stu-id="3c0cc-216">False</span></span>                                                      |
| <span data-ttu-id="3c0cc-217">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="3c0cc-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="3c0cc-218">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="3c0cc-218">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="3c0cc-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3c0cc-219">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="3c0cc-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3c0cc-220">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="3c0cc-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3c0cc-221">Search-Flags</span></span>           | <span data-ttu-id="3c0cc-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3c0cc-222">0x00000000</span></span>                                                 |
| <span data-ttu-id="3c0cc-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3c0cc-223">System-Flags</span></span>           | <span data-ttu-id="3c0cc-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3c0cc-224">0x00000010</span></span>                                                 |
| <span data-ttu-id="3c0cc-225">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="3c0cc-225">Classes used in</span></span>        | [<span data-ttu-id="3c0cc-226">**Display-specifier**</span><span class="sxs-lookup"><span data-stu-id="3c0cc-226">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="3c0cc-227">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3c0cc-227">Windows Server 2008 R2</span></span>



| <span data-ttu-id="3c0cc-228">Voce</span><span class="sxs-lookup"><span data-stu-id="3c0cc-228">Entry</span></span> | <span data-ttu-id="3c0cc-229">Valore</span><span class="sxs-lookup"><span data-stu-id="3c0cc-229">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="3c0cc-230">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="3c0cc-230">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="3c0cc-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3c0cc-231">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="3c0cc-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="3c0cc-232">System-Only</span></span>            | <span data-ttu-id="3c0cc-233">Falso</span><span class="sxs-lookup"><span data-stu-id="3c0cc-233">False</span></span>                                                      |
| <span data-ttu-id="3c0cc-234">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="3c0cc-234">Is-Single-Valued</span></span>       | <span data-ttu-id="3c0cc-235">Falso</span><span class="sxs-lookup"><span data-stu-id="3c0cc-235">False</span></span>                                                      |
| <span data-ttu-id="3c0cc-236">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="3c0cc-236">Is Indexed</span></span>             | <span data-ttu-id="3c0cc-237">Falso</span><span class="sxs-lookup"><span data-stu-id="3c0cc-237">False</span></span>                                                      |
| <span data-ttu-id="3c0cc-238">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="3c0cc-238">In Global Catalog</span></span>      | <span data-ttu-id="3c0cc-239">Falso</span><span class="sxs-lookup"><span data-stu-id="3c0cc-239">False</span></span>                                                      |
| <span data-ttu-id="3c0cc-240">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="3c0cc-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="3c0cc-241">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="3c0cc-241">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="3c0cc-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3c0cc-242">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="3c0cc-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3c0cc-243">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="3c0cc-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3c0cc-244">Search-Flags</span></span>           | <span data-ttu-id="3c0cc-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3c0cc-245">0x00000000</span></span>                                                 |
| <span data-ttu-id="3c0cc-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3c0cc-246">System-Flags</span></span>           | <span data-ttu-id="3c0cc-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3c0cc-247">0x00000010</span></span>                                                 |
| <span data-ttu-id="3c0cc-248">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="3c0cc-248">Classes used in</span></span>        | [<span data-ttu-id="3c0cc-249">**Display-specifier**</span><span class="sxs-lookup"><span data-stu-id="3c0cc-249">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="3c0cc-250">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3c0cc-250">Windows Server 2012</span></span>



| <span data-ttu-id="3c0cc-251">Voce</span><span class="sxs-lookup"><span data-stu-id="3c0cc-251">Entry</span></span> | <span data-ttu-id="3c0cc-252">Valore</span><span class="sxs-lookup"><span data-stu-id="3c0cc-252">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="3c0cc-253">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="3c0cc-253">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="3c0cc-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3c0cc-254">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="3c0cc-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="3c0cc-255">System-Only</span></span>            | <span data-ttu-id="3c0cc-256">Falso</span><span class="sxs-lookup"><span data-stu-id="3c0cc-256">False</span></span>                                                      |
| <span data-ttu-id="3c0cc-257">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="3c0cc-257">Is-Single-Valued</span></span>       | <span data-ttu-id="3c0cc-258">Falso</span><span class="sxs-lookup"><span data-stu-id="3c0cc-258">False</span></span>                                                      |
| <span data-ttu-id="3c0cc-259">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="3c0cc-259">Is Indexed</span></span>             | <span data-ttu-id="3c0cc-260">Falso</span><span class="sxs-lookup"><span data-stu-id="3c0cc-260">False</span></span>                                                      |
| <span data-ttu-id="3c0cc-261">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="3c0cc-261">In Global Catalog</span></span>      | <span data-ttu-id="3c0cc-262">Falso</span><span class="sxs-lookup"><span data-stu-id="3c0cc-262">False</span></span>                                                      |
| <span data-ttu-id="3c0cc-263">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="3c0cc-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="3c0cc-264">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="3c0cc-264">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="3c0cc-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3c0cc-265">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="3c0cc-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3c0cc-266">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="3c0cc-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3c0cc-267">Search-Flags</span></span>           | <span data-ttu-id="3c0cc-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3c0cc-268">0x00000000</span></span>                                                 |
| <span data-ttu-id="3c0cc-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3c0cc-269">System-Flags</span></span>           | <span data-ttu-id="3c0cc-270">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3c0cc-270">0x00000010</span></span>                                                 |
| <span data-ttu-id="3c0cc-271">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="3c0cc-271">Classes used in</span></span>        | [<span data-ttu-id="3c0cc-272">**Display-specifier**</span><span class="sxs-lookup"><span data-stu-id="3c0cc-272">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



 

 





