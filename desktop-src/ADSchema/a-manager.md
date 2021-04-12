---
title: Gestore (attributo)
description: Contiene il nome distinto dell'utente che corrisponde al responsabile dell'utente. L'oggetto utente del Manager contiene una proprietà directReports che contiene riferimenti a tutti gli oggetti utente che hanno le proprietà Manager impostate su questo nome distinto.
ms.assetid: 40743784-a99c-4ec0-9140-9f865c073244
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo Manager
- Schema AD dell'attributo Manager
topic_type:
- apiref
api_name:
- Manager
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f42c659a436f9798861f5c37df19f8d10db91127
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104401000"
---
# <a name="manager-attribute"></a><span data-ttu-id="1a90f-106">Gestore (attributo)</span><span class="sxs-lookup"><span data-stu-id="1a90f-106">Manager attribute</span></span>

<span data-ttu-id="1a90f-107">Contiene il nome distinto dell'utente che corrisponde al responsabile dell'utente.</span><span class="sxs-lookup"><span data-stu-id="1a90f-107">Contains the distinguished name of the user who is the user's manager.</span></span> <span data-ttu-id="1a90f-108">L'oggetto utente del Manager contiene una proprietà directReports che contiene riferimenti a tutti gli oggetti utente che hanno le proprietà Manager impostate su questo nome distinto.</span><span class="sxs-lookup"><span data-stu-id="1a90f-108">The manager's user object contains a directReports property that contains references to all user objects that have their manager properties set to this distinguished name.</span></span>



| <span data-ttu-id="1a90f-109">Voce</span><span class="sxs-lookup"><span data-stu-id="1a90f-109">Entry</span></span> | <span data-ttu-id="1a90f-110">Valore</span><span class="sxs-lookup"><span data-stu-id="1a90f-110">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="1a90f-111">CN</span><span class="sxs-lookup"><span data-stu-id="1a90f-111">CN</span></span>                | <span data-ttu-id="1a90f-112">Manager</span><span class="sxs-lookup"><span data-stu-id="1a90f-112">Manager</span></span>                                                                     |
| <span data-ttu-id="1a90f-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="1a90f-113">Ldap-Display-Name</span></span> | <span data-ttu-id="1a90f-114">manager</span><span class="sxs-lookup"><span data-stu-id="1a90f-114">manager</span></span>                                                                     |
| <span data-ttu-id="1a90f-115">Dimensione</span><span class="sxs-lookup"><span data-stu-id="1a90f-115">Size</span></span>              | \-                                                                          |
| <span data-ttu-id="1a90f-116">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="1a90f-116">Update Privilege</span></span>  | <span data-ttu-id="1a90f-117">Amministratore di dominio o proprietario dell'account.</span><span class="sxs-lookup"><span data-stu-id="1a90f-117">Domain administrator or account owner.</span></span>                                      |
| <span data-ttu-id="1a90f-118">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="1a90f-118">Update Frequency</span></span>  | <span data-ttu-id="1a90f-119">Quando il record dell'utente viene creato e ogni volta che il responsabile deve cambiare.</span><span class="sxs-lookup"><span data-stu-id="1a90f-119">When the user's record is created and whenever the manager needs to change.</span></span> |
| <span data-ttu-id="1a90f-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="1a90f-120">Attribute-Id</span></span>      | <span data-ttu-id="1a90f-121">0.9.2342.19200300.100.1.10</span><span class="sxs-lookup"><span data-stu-id="1a90f-121">0.9.2342.19200300.100.1.10</span></span>                                                  |
| <span data-ttu-id="1a90f-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="1a90f-122">System-Id-Guid</span></span>    | <span data-ttu-id="1a90f-123">bf9679b5-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="1a90f-123">bf9679b5-0de6-11d0-a285-00aa003049e2</span></span>                                        |
| <span data-ttu-id="1a90f-124">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1a90f-124">Syntax</span></span>            | [<span data-ttu-id="1a90f-125">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="1a90f-125">**Object(DS-DN)**</span></span>](s-object-ds-dn.md)                                     |



## <a name="implementations"></a><span data-ttu-id="1a90f-126">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="1a90f-126">Implementations</span></span>

-   [<span data-ttu-id="1a90f-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="1a90f-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="1a90f-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="1a90f-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="1a90f-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="1a90f-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="1a90f-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="1a90f-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="1a90f-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="1a90f-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="1a90f-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="1a90f-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="1a90f-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1a90f-133">Windows 2000 Server</span></span>



| <span data-ttu-id="1a90f-134">Voce</span><span class="sxs-lookup"><span data-stu-id="1a90f-134">Entry</span></span> | <span data-ttu-id="1a90f-135">Valore</span><span class="sxs-lookup"><span data-stu-id="1a90f-135">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="1a90f-136">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="1a90f-136">Link-Id</span></span>                | <span data-ttu-id="1a90f-137">42</span><span class="sxs-lookup"><span data-stu-id="1a90f-137">42</span></span>                                                                 |
| <span data-ttu-id="1a90f-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1a90f-138">MAPI-Id</span></span>                | <span data-ttu-id="1a90f-139">0x8005</span><span class="sxs-lookup"><span data-stu-id="1a90f-139">0x8005</span></span>                                                             |
| <span data-ttu-id="1a90f-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="1a90f-140">System-Only</span></span>            | <span data-ttu-id="1a90f-141">Falso</span><span class="sxs-lookup"><span data-stu-id="1a90f-141">False</span></span>                                                              |
| <span data-ttu-id="1a90f-142">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="1a90f-142">Is-Single-Valued</span></span>       | <span data-ttu-id="1a90f-143">Vero</span><span class="sxs-lookup"><span data-stu-id="1a90f-143">True</span></span>                                                               |
| <span data-ttu-id="1a90f-144">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="1a90f-144">Is Indexed</span></span>             | <span data-ttu-id="1a90f-145">Falso</span><span class="sxs-lookup"><span data-stu-id="1a90f-145">False</span></span>                                                              |
| <span data-ttu-id="1a90f-146">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="1a90f-146">In Global Catalog</span></span>      | <span data-ttu-id="1a90f-147">Vero</span><span class="sxs-lookup"><span data-stu-id="1a90f-147">True</span></span>                                                               |
| <span data-ttu-id="1a90f-148">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="1a90f-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="1a90f-149">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="1a90f-149">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="1a90f-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1a90f-150">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="1a90f-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1a90f-151">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="1a90f-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1a90f-152">Search-Flags</span></span>           | <span data-ttu-id="1a90f-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1a90f-153">0x00000010</span></span>                                                         |
| <span data-ttu-id="1a90f-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1a90f-154">System-Flags</span></span>           | <span data-ttu-id="1a90f-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1a90f-155">0x00000010</span></span>                                                         |
| <span data-ttu-id="1a90f-156">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="1a90f-156">Classes used in</span></span>        | [<span data-ttu-id="1a90f-157">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="1a90f-157">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="1a90f-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1a90f-158">Windows Server 2003</span></span>



| <span data-ttu-id="1a90f-159">Voce</span><span class="sxs-lookup"><span data-stu-id="1a90f-159">Entry</span></span> | <span data-ttu-id="1a90f-160">Valore</span><span class="sxs-lookup"><span data-stu-id="1a90f-160">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a90f-161">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="1a90f-161">Link-Id</span></span>                | <span data-ttu-id="1a90f-162">42</span><span class="sxs-lookup"><span data-stu-id="1a90f-162">42</span></span>                                                                                                                     |
| <span data-ttu-id="1a90f-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1a90f-163">MAPI-Id</span></span>                | <span data-ttu-id="1a90f-164">0x8005</span><span class="sxs-lookup"><span data-stu-id="1a90f-164">0x8005</span></span>                                                                                                                 |
| <span data-ttu-id="1a90f-165">System-Only</span><span class="sxs-lookup"><span data-stu-id="1a90f-165">System-Only</span></span>            | <span data-ttu-id="1a90f-166">Falso</span><span class="sxs-lookup"><span data-stu-id="1a90f-166">False</span></span>                                                                                                                  |
| <span data-ttu-id="1a90f-167">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="1a90f-167">Is-Single-Valued</span></span>       | <span data-ttu-id="1a90f-168">Vero</span><span class="sxs-lookup"><span data-stu-id="1a90f-168">True</span></span>                                                                                                                   |
| <span data-ttu-id="1a90f-169">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="1a90f-169">Is Indexed</span></span>             | <span data-ttu-id="1a90f-170">Falso</span><span class="sxs-lookup"><span data-stu-id="1a90f-170">False</span></span>                                                                                                                  |
| <span data-ttu-id="1a90f-171">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="1a90f-171">In Global Catalog</span></span>      | <span data-ttu-id="1a90f-172">Vero</span><span class="sxs-lookup"><span data-stu-id="1a90f-172">True</span></span>                                                                                                                   |
| <span data-ttu-id="1a90f-173">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="1a90f-173">NT-Security-Descriptor</span></span> | <span data-ttu-id="1a90f-174">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="1a90f-174">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="1a90f-175">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1a90f-175">Range-Lower</span></span>            | \-                                                                                                                     |
| <span data-ttu-id="1a90f-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1a90f-176">Range-Upper</span></span>            | \-                                                                                                                     |
| <span data-ttu-id="1a90f-177">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1a90f-177">Search-Flags</span></span>           | <span data-ttu-id="1a90f-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1a90f-178">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="1a90f-179">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1a90f-179">System-Flags</span></span>           | <span data-ttu-id="1a90f-180">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1a90f-180">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="1a90f-181">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="1a90f-181">Classes used in</span></span>        | [<span data-ttu-id="1a90f-182">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="1a90f-182">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="1a90f-183">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="1a90f-183">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="1a90f-184">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="1a90f-184">Windows Server 2003 R2</span></span>



| <span data-ttu-id="1a90f-185">Voce</span><span class="sxs-lookup"><span data-stu-id="1a90f-185">Entry</span></span> | <span data-ttu-id="1a90f-186">Valore</span><span class="sxs-lookup"><span data-stu-id="1a90f-186">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a90f-187">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="1a90f-187">Link-Id</span></span>                | <span data-ttu-id="1a90f-188">42</span><span class="sxs-lookup"><span data-stu-id="1a90f-188">42</span></span>                                                                                                                     |
| <span data-ttu-id="1a90f-189">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1a90f-189">MAPI-Id</span></span>                | <span data-ttu-id="1a90f-190">0x8005</span><span class="sxs-lookup"><span data-stu-id="1a90f-190">0x8005</span></span>                                                                                                                 |
| <span data-ttu-id="1a90f-191">System-Only</span><span class="sxs-lookup"><span data-stu-id="1a90f-191">System-Only</span></span>            | <span data-ttu-id="1a90f-192">Falso</span><span class="sxs-lookup"><span data-stu-id="1a90f-192">False</span></span>                                                                                                                  |
| <span data-ttu-id="1a90f-193">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="1a90f-193">Is-Single-Valued</span></span>       | <span data-ttu-id="1a90f-194">Vero</span><span class="sxs-lookup"><span data-stu-id="1a90f-194">True</span></span>                                                                                                                   |
| <span data-ttu-id="1a90f-195">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="1a90f-195">Is Indexed</span></span>             | <span data-ttu-id="1a90f-196">Falso</span><span class="sxs-lookup"><span data-stu-id="1a90f-196">False</span></span>                                                                                                                  |
| <span data-ttu-id="1a90f-197">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="1a90f-197">In Global Catalog</span></span>      | <span data-ttu-id="1a90f-198">Vero</span><span class="sxs-lookup"><span data-stu-id="1a90f-198">True</span></span>                                                                                                                   |
| <span data-ttu-id="1a90f-199">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="1a90f-199">NT-Security-Descriptor</span></span> | <span data-ttu-id="1a90f-200">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="1a90f-200">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="1a90f-201">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1a90f-201">Range-Lower</span></span>            | \-                                                                                                                     |
| <span data-ttu-id="1a90f-202">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1a90f-202">Range-Upper</span></span>            | \-                                                                                                                     |
| <span data-ttu-id="1a90f-203">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1a90f-203">Search-Flags</span></span>           | <span data-ttu-id="1a90f-204">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1a90f-204">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="1a90f-205">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1a90f-205">System-Flags</span></span>           | <span data-ttu-id="1a90f-206">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1a90f-206">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="1a90f-207">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="1a90f-207">Classes used in</span></span>        | [<span data-ttu-id="1a90f-208">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="1a90f-208">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="1a90f-209">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="1a90f-209">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="1a90f-210">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1a90f-210">Windows Server 2008</span></span>



| <span data-ttu-id="1a90f-211">Voce</span><span class="sxs-lookup"><span data-stu-id="1a90f-211">Entry</span></span> | <span data-ttu-id="1a90f-212">Valore</span><span class="sxs-lookup"><span data-stu-id="1a90f-212">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a90f-213">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="1a90f-213">Link-Id</span></span>                | <span data-ttu-id="1a90f-214">42</span><span class="sxs-lookup"><span data-stu-id="1a90f-214">42</span></span>                                                                                                                     |
| <span data-ttu-id="1a90f-215">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1a90f-215">MAPI-Id</span></span>                | <span data-ttu-id="1a90f-216">0x8005</span><span class="sxs-lookup"><span data-stu-id="1a90f-216">0x8005</span></span>                                                                                                                 |
| <span data-ttu-id="1a90f-217">System-Only</span><span class="sxs-lookup"><span data-stu-id="1a90f-217">System-Only</span></span>            | <span data-ttu-id="1a90f-218">Falso</span><span class="sxs-lookup"><span data-stu-id="1a90f-218">False</span></span>                                                                                                                  |
| <span data-ttu-id="1a90f-219">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="1a90f-219">Is-Single-Valued</span></span>       | <span data-ttu-id="1a90f-220">Vero</span><span class="sxs-lookup"><span data-stu-id="1a90f-220">True</span></span>                                                                                                                   |
| <span data-ttu-id="1a90f-221">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="1a90f-221">Is Indexed</span></span>             | <span data-ttu-id="1a90f-222">Falso</span><span class="sxs-lookup"><span data-stu-id="1a90f-222">False</span></span>                                                                                                                  |
| <span data-ttu-id="1a90f-223">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="1a90f-223">In Global Catalog</span></span>      | <span data-ttu-id="1a90f-224">Vero</span><span class="sxs-lookup"><span data-stu-id="1a90f-224">True</span></span>                                                                                                                   |
| <span data-ttu-id="1a90f-225">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="1a90f-225">NT-Security-Descriptor</span></span> | <span data-ttu-id="1a90f-226">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="1a90f-226">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="1a90f-227">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1a90f-227">Range-Lower</span></span>            | \-                                                                                                                     |
| <span data-ttu-id="1a90f-228">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1a90f-228">Range-Upper</span></span>            | \-                                                                                                                     |
| <span data-ttu-id="1a90f-229">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1a90f-229">Search-Flags</span></span>           | <span data-ttu-id="1a90f-230">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1a90f-230">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="1a90f-231">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1a90f-231">System-Flags</span></span>           | <span data-ttu-id="1a90f-232">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1a90f-232">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="1a90f-233">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="1a90f-233">Classes used in</span></span>        | [<span data-ttu-id="1a90f-234">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="1a90f-234">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="1a90f-235">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="1a90f-235">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="1a90f-236">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1a90f-236">Windows Server 2008 R2</span></span>



| <span data-ttu-id="1a90f-237">Voce</span><span class="sxs-lookup"><span data-stu-id="1a90f-237">Entry</span></span> | <span data-ttu-id="1a90f-238">Valore</span><span class="sxs-lookup"><span data-stu-id="1a90f-238">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a90f-239">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="1a90f-239">Link-Id</span></span>                | <span data-ttu-id="1a90f-240">42</span><span class="sxs-lookup"><span data-stu-id="1a90f-240">42</span></span>                                                                                                                     |
| <span data-ttu-id="1a90f-241">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1a90f-241">MAPI-Id</span></span>                | <span data-ttu-id="1a90f-242">0x8005</span><span class="sxs-lookup"><span data-stu-id="1a90f-242">0x8005</span></span>                                                                                                                 |
| <span data-ttu-id="1a90f-243">System-Only</span><span class="sxs-lookup"><span data-stu-id="1a90f-243">System-Only</span></span>            | <span data-ttu-id="1a90f-244">Falso</span><span class="sxs-lookup"><span data-stu-id="1a90f-244">False</span></span>                                                                                                                  |
| <span data-ttu-id="1a90f-245">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="1a90f-245">Is-Single-Valued</span></span>       | <span data-ttu-id="1a90f-246">Vero</span><span class="sxs-lookup"><span data-stu-id="1a90f-246">True</span></span>                                                                                                                   |
| <span data-ttu-id="1a90f-247">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="1a90f-247">Is Indexed</span></span>             | <span data-ttu-id="1a90f-248">Falso</span><span class="sxs-lookup"><span data-stu-id="1a90f-248">False</span></span>                                                                                                                  |
| <span data-ttu-id="1a90f-249">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="1a90f-249">In Global Catalog</span></span>      | <span data-ttu-id="1a90f-250">Vero</span><span class="sxs-lookup"><span data-stu-id="1a90f-250">True</span></span>                                                                                                                   |
| <span data-ttu-id="1a90f-251">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="1a90f-251">NT-Security-Descriptor</span></span> | <span data-ttu-id="1a90f-252">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="1a90f-252">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="1a90f-253">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1a90f-253">Range-Lower</span></span>            | \-                                                                                                                     |
| <span data-ttu-id="1a90f-254">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1a90f-254">Range-Upper</span></span>            | \-                                                                                                                     |
| <span data-ttu-id="1a90f-255">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1a90f-255">Search-Flags</span></span>           | <span data-ttu-id="1a90f-256">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1a90f-256">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="1a90f-257">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1a90f-257">System-Flags</span></span>           | <span data-ttu-id="1a90f-258">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1a90f-258">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="1a90f-259">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="1a90f-259">Classes used in</span></span>        | [<span data-ttu-id="1a90f-260">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="1a90f-260">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="1a90f-261">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="1a90f-261">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="1a90f-262">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1a90f-262">Windows Server 2012</span></span>



| <span data-ttu-id="1a90f-263">Voce</span><span class="sxs-lookup"><span data-stu-id="1a90f-263">Entry</span></span> | <span data-ttu-id="1a90f-264">Valore</span><span class="sxs-lookup"><span data-stu-id="1a90f-264">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a90f-265">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="1a90f-265">Link-Id</span></span>                | <span data-ttu-id="1a90f-266">42</span><span class="sxs-lookup"><span data-stu-id="1a90f-266">42</span></span>                                                                                                                     |
| <span data-ttu-id="1a90f-267">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1a90f-267">MAPI-Id</span></span>                | <span data-ttu-id="1a90f-268">0x8005</span><span class="sxs-lookup"><span data-stu-id="1a90f-268">0x8005</span></span>                                                                                                                 |
| <span data-ttu-id="1a90f-269">System-Only</span><span class="sxs-lookup"><span data-stu-id="1a90f-269">System-Only</span></span>            | <span data-ttu-id="1a90f-270">Falso</span><span class="sxs-lookup"><span data-stu-id="1a90f-270">False</span></span>                                                                                                                  |
| <span data-ttu-id="1a90f-271">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="1a90f-271">Is-Single-Valued</span></span>       | <span data-ttu-id="1a90f-272">Vero</span><span class="sxs-lookup"><span data-stu-id="1a90f-272">True</span></span>                                                                                                                   |
| <span data-ttu-id="1a90f-273">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="1a90f-273">Is Indexed</span></span>             | <span data-ttu-id="1a90f-274">Falso</span><span class="sxs-lookup"><span data-stu-id="1a90f-274">False</span></span>                                                                                                                  |
| <span data-ttu-id="1a90f-275">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="1a90f-275">In Global Catalog</span></span>      | <span data-ttu-id="1a90f-276">Vero</span><span class="sxs-lookup"><span data-stu-id="1a90f-276">True</span></span>                                                                                                                   |
| <span data-ttu-id="1a90f-277">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="1a90f-277">NT-Security-Descriptor</span></span> | <span data-ttu-id="1a90f-278">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="1a90f-278">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="1a90f-279">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1a90f-279">Range-Lower</span></span>            | \-                                                                                                                     |
| <span data-ttu-id="1a90f-280">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1a90f-280">Range-Upper</span></span>            | \-                                                                                                                     |
| <span data-ttu-id="1a90f-281">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1a90f-281">Search-Flags</span></span>           | <span data-ttu-id="1a90f-282">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1a90f-282">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="1a90f-283">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1a90f-283">System-Flags</span></span>           | <span data-ttu-id="1a90f-284">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1a90f-284">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="1a90f-285">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="1a90f-285">Classes used in</span></span>        | [<span data-ttu-id="1a90f-286">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="1a90f-286">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="1a90f-287">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="1a90f-287">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



 

 





