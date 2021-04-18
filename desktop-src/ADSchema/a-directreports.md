---
title: Attributo Reports
description: Contiene l'elenco di utenti che riportano direttamente all'utente. Gli utenti elencati come report sono quelli per i quali la proprietà Gestione proprietà è impostata su questo utente. Ogni elemento nell'elenco è un riferimento collegato all'oggetto che rappresenta l'utente.
ms.assetid: 369fc457-685c-4875-aed3-0a246a219512
ms.tgt_platform: multiple
keywords:
- Attributo di AD schema di report
- Schema AD dell'attributo directReports
topic_type:
- apiref
api_name:
- Reports
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ef5a555b7c1d48fdb337f2c876abf3f15ae8daa
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "106303577"
---
# <a name="reports-attribute"></a><span data-ttu-id="b3270-107">Attributo Reports</span><span class="sxs-lookup"><span data-stu-id="b3270-107">Reports attribute</span></span>

<span data-ttu-id="b3270-108">Contiene l'elenco di utenti che riportano direttamente all'utente.</span><span class="sxs-lookup"><span data-stu-id="b3270-108">Contains the list of users that directly report to the user.</span></span> <span data-ttu-id="b3270-109">Gli utenti elencati come report sono quelli per i quali la proprietà Gestione proprietà è impostata su questo utente.</span><span class="sxs-lookup"><span data-stu-id="b3270-109">The users listed as reports are those that have the property manager property set to this user.</span></span> <span data-ttu-id="b3270-110">Ogni elemento nell'elenco è un riferimento collegato all'oggetto che rappresenta l'utente.</span><span class="sxs-lookup"><span data-stu-id="b3270-110">Each item in the list is a linked reference to the object that represents the user.</span></span>



| <span data-ttu-id="b3270-111">Voce</span><span class="sxs-lookup"><span data-stu-id="b3270-111">Entry</span></span> | <span data-ttu-id="b3270-112">Valore</span><span class="sxs-lookup"><span data-stu-id="b3270-112">Value</span></span> |
|-------------------|-------------------------------------------------|
| <span data-ttu-id="b3270-113">CN</span><span class="sxs-lookup"><span data-stu-id="b3270-113">CN</span></span>                | <span data-ttu-id="b3270-114">Report</span><span class="sxs-lookup"><span data-stu-id="b3270-114">Reports</span></span>                                         |
| <span data-ttu-id="b3270-115">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="b3270-115">Ldap-Display-Name</span></span> | <span data-ttu-id="b3270-116">directReports</span><span class="sxs-lookup"><span data-stu-id="b3270-116">directReports</span></span>                                   |
| <span data-ttu-id="b3270-117">Dimensione</span><span class="sxs-lookup"><span data-stu-id="b3270-117">Size</span></span>              | \-                                              |
| <span data-ttu-id="b3270-118">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="b3270-118">Update Privilege</span></span>  | <span data-ttu-id="b3270-119">Questo valore viene impostato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="b3270-119">This value is set by the system.</span></span>                |
| <span data-ttu-id="b3270-120">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="b3270-120">Update Frequency</span></span>  | <span data-ttu-id="b3270-121">Ogni volta che viene modificato il report diretto per un utente.</span><span class="sxs-lookup"><span data-stu-id="b3270-121">Whenever the direct reports for a user changes.</span></span> |
| <span data-ttu-id="b3270-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b3270-122">Attribute-Id</span></span>      | <span data-ttu-id="b3270-123">1.2.840.113556.1.2.436</span><span class="sxs-lookup"><span data-stu-id="b3270-123">1.2.840.113556.1.2.436</span></span>                          |
| <span data-ttu-id="b3270-124">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="b3270-124">System-Id-Guid</span></span>    | <span data-ttu-id="b3270-125">bf967a1c-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="b3270-125">bf967a1c-0de6-11d0-a285-00aa003049e2</span></span>            |
| <span data-ttu-id="b3270-126">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b3270-126">Syntax</span></span>            | [<span data-ttu-id="b3270-127">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="b3270-127">**Object(DS-DN)**</span></span>](s-object-ds-dn.md)         |



## <a name="implementations"></a><span data-ttu-id="b3270-128">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="b3270-128">Implementations</span></span>

-   [<span data-ttu-id="b3270-129">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="b3270-129">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="b3270-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b3270-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b3270-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b3270-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b3270-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b3270-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b3270-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b3270-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b3270-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b3270-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="b3270-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b3270-135">Windows 2000 Server</span></span>



| <span data-ttu-id="b3270-136">Voce</span><span class="sxs-lookup"><span data-stu-id="b3270-136">Entry</span></span> | <span data-ttu-id="b3270-137">Valore</span><span class="sxs-lookup"><span data-stu-id="b3270-137">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b3270-138">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="b3270-138">Link-Id</span></span>                | <span data-ttu-id="b3270-139">43</span><span class="sxs-lookup"><span data-stu-id="b3270-139">43</span></span>                              |
| <span data-ttu-id="b3270-140">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b3270-140">MAPI-Id</span></span>                | <span data-ttu-id="b3270-141">0x800E</span><span class="sxs-lookup"><span data-stu-id="b3270-141">0x800E</span></span>                          |
| <span data-ttu-id="b3270-142">System-Only</span><span class="sxs-lookup"><span data-stu-id="b3270-142">System-Only</span></span>            | <span data-ttu-id="b3270-143">Vero</span><span class="sxs-lookup"><span data-stu-id="b3270-143">True</span></span>                            |
| <span data-ttu-id="b3270-144">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="b3270-144">Is-Single-Valued</span></span>       | <span data-ttu-id="b3270-145">Falso</span><span class="sxs-lookup"><span data-stu-id="b3270-145">False</span></span>                           |
| <span data-ttu-id="b3270-146">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="b3270-146">Is Indexed</span></span>             | <span data-ttu-id="b3270-147">Falso</span><span class="sxs-lookup"><span data-stu-id="b3270-147">False</span></span>                           |
| <span data-ttu-id="b3270-148">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="b3270-148">In Global Catalog</span></span>      | <span data-ttu-id="b3270-149">Falso</span><span class="sxs-lookup"><span data-stu-id="b3270-149">False</span></span>                           |
| <span data-ttu-id="b3270-150">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="b3270-150">NT-Security-Descriptor</span></span> | <span data-ttu-id="b3270-151">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="b3270-151">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b3270-152">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b3270-152">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b3270-153">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b3270-153">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b3270-154">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b3270-154">Search-Flags</span></span>           | <span data-ttu-id="b3270-155">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b3270-155">0x00000000</span></span>                      |
| <span data-ttu-id="b3270-156">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b3270-156">System-Flags</span></span>           | <span data-ttu-id="b3270-157">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b3270-157">0x00000010</span></span>                      |
| <span data-ttu-id="b3270-158">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="b3270-158">Classes used in</span></span>        | [<span data-ttu-id="b3270-159">**In alto**</span><span class="sxs-lookup"><span data-stu-id="b3270-159">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="b3270-160">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b3270-160">Windows Server 2003</span></span>



| <span data-ttu-id="b3270-161">Voce</span><span class="sxs-lookup"><span data-stu-id="b3270-161">Entry</span></span> | <span data-ttu-id="b3270-162">Valore</span><span class="sxs-lookup"><span data-stu-id="b3270-162">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b3270-163">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="b3270-163">Link-Id</span></span>                | <span data-ttu-id="b3270-164">43</span><span class="sxs-lookup"><span data-stu-id="b3270-164">43</span></span>                              |
| <span data-ttu-id="b3270-165">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b3270-165">MAPI-Id</span></span>                | <span data-ttu-id="b3270-166">0x800E</span><span class="sxs-lookup"><span data-stu-id="b3270-166">0x800E</span></span>                          |
| <span data-ttu-id="b3270-167">System-Only</span><span class="sxs-lookup"><span data-stu-id="b3270-167">System-Only</span></span>            | <span data-ttu-id="b3270-168">Vero</span><span class="sxs-lookup"><span data-stu-id="b3270-168">True</span></span>                            |
| <span data-ttu-id="b3270-169">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="b3270-169">Is-Single-Valued</span></span>       | <span data-ttu-id="b3270-170">Falso</span><span class="sxs-lookup"><span data-stu-id="b3270-170">False</span></span>                           |
| <span data-ttu-id="b3270-171">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="b3270-171">Is Indexed</span></span>             | <span data-ttu-id="b3270-172">Falso</span><span class="sxs-lookup"><span data-stu-id="b3270-172">False</span></span>                           |
| <span data-ttu-id="b3270-173">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="b3270-173">In Global Catalog</span></span>      | <span data-ttu-id="b3270-174">Falso</span><span class="sxs-lookup"><span data-stu-id="b3270-174">False</span></span>                           |
| <span data-ttu-id="b3270-175">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="b3270-175">NT-Security-Descriptor</span></span> | <span data-ttu-id="b3270-176">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="b3270-176">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b3270-177">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b3270-177">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b3270-178">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b3270-178">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b3270-179">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b3270-179">Search-Flags</span></span>           | <span data-ttu-id="b3270-180">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b3270-180">0x00000000</span></span>                      |
| <span data-ttu-id="b3270-181">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b3270-181">System-Flags</span></span>           | <span data-ttu-id="b3270-182">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b3270-182">0x00000010</span></span>                      |
| <span data-ttu-id="b3270-183">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="b3270-183">Classes used in</span></span>        | [<span data-ttu-id="b3270-184">**In alto**</span><span class="sxs-lookup"><span data-stu-id="b3270-184">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b3270-185">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b3270-185">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b3270-186">Voce</span><span class="sxs-lookup"><span data-stu-id="b3270-186">Entry</span></span> | <span data-ttu-id="b3270-187">Valore</span><span class="sxs-lookup"><span data-stu-id="b3270-187">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b3270-188">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="b3270-188">Link-Id</span></span>                | <span data-ttu-id="b3270-189">43</span><span class="sxs-lookup"><span data-stu-id="b3270-189">43</span></span>                              |
| <span data-ttu-id="b3270-190">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b3270-190">MAPI-Id</span></span>                | <span data-ttu-id="b3270-191">0x800E</span><span class="sxs-lookup"><span data-stu-id="b3270-191">0x800E</span></span>                          |
| <span data-ttu-id="b3270-192">System-Only</span><span class="sxs-lookup"><span data-stu-id="b3270-192">System-Only</span></span>            | <span data-ttu-id="b3270-193">Vero</span><span class="sxs-lookup"><span data-stu-id="b3270-193">True</span></span>                            |
| <span data-ttu-id="b3270-194">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="b3270-194">Is-Single-Valued</span></span>       | <span data-ttu-id="b3270-195">Falso</span><span class="sxs-lookup"><span data-stu-id="b3270-195">False</span></span>                           |
| <span data-ttu-id="b3270-196">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="b3270-196">Is Indexed</span></span>             | <span data-ttu-id="b3270-197">Falso</span><span class="sxs-lookup"><span data-stu-id="b3270-197">False</span></span>                           |
| <span data-ttu-id="b3270-198">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="b3270-198">In Global Catalog</span></span>      | <span data-ttu-id="b3270-199">Falso</span><span class="sxs-lookup"><span data-stu-id="b3270-199">False</span></span>                           |
| <span data-ttu-id="b3270-200">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="b3270-200">NT-Security-Descriptor</span></span> | <span data-ttu-id="b3270-201">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="b3270-201">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b3270-202">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b3270-202">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b3270-203">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b3270-203">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b3270-204">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b3270-204">Search-Flags</span></span>           | <span data-ttu-id="b3270-205">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b3270-205">0x00000000</span></span>                      |
| <span data-ttu-id="b3270-206">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b3270-206">System-Flags</span></span>           | <span data-ttu-id="b3270-207">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b3270-207">0x00000010</span></span>                      |
| <span data-ttu-id="b3270-208">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="b3270-208">Classes used in</span></span>        | [<span data-ttu-id="b3270-209">**In alto**</span><span class="sxs-lookup"><span data-stu-id="b3270-209">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b3270-210">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b3270-210">Windows Server 2008</span></span>



| <span data-ttu-id="b3270-211">Voce</span><span class="sxs-lookup"><span data-stu-id="b3270-211">Entry</span></span> | <span data-ttu-id="b3270-212">Valore</span><span class="sxs-lookup"><span data-stu-id="b3270-212">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b3270-213">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="b3270-213">Link-Id</span></span>                | <span data-ttu-id="b3270-214">43</span><span class="sxs-lookup"><span data-stu-id="b3270-214">43</span></span>                              |
| <span data-ttu-id="b3270-215">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b3270-215">MAPI-Id</span></span>                | <span data-ttu-id="b3270-216">0x800E</span><span class="sxs-lookup"><span data-stu-id="b3270-216">0x800E</span></span>                          |
| <span data-ttu-id="b3270-217">System-Only</span><span class="sxs-lookup"><span data-stu-id="b3270-217">System-Only</span></span>            | <span data-ttu-id="b3270-218">Vero</span><span class="sxs-lookup"><span data-stu-id="b3270-218">True</span></span>                            |
| <span data-ttu-id="b3270-219">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="b3270-219">Is-Single-Valued</span></span>       | <span data-ttu-id="b3270-220">Falso</span><span class="sxs-lookup"><span data-stu-id="b3270-220">False</span></span>                           |
| <span data-ttu-id="b3270-221">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="b3270-221">Is Indexed</span></span>             | <span data-ttu-id="b3270-222">Falso</span><span class="sxs-lookup"><span data-stu-id="b3270-222">False</span></span>                           |
| <span data-ttu-id="b3270-223">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="b3270-223">In Global Catalog</span></span>      | <span data-ttu-id="b3270-224">Falso</span><span class="sxs-lookup"><span data-stu-id="b3270-224">False</span></span>                           |
| <span data-ttu-id="b3270-225">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="b3270-225">NT-Security-Descriptor</span></span> | <span data-ttu-id="b3270-226">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="b3270-226">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b3270-227">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b3270-227">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b3270-228">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b3270-228">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b3270-229">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b3270-229">Search-Flags</span></span>           | <span data-ttu-id="b3270-230">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b3270-230">0x00000000</span></span>                      |
| <span data-ttu-id="b3270-231">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b3270-231">System-Flags</span></span>           | <span data-ttu-id="b3270-232">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b3270-232">0x00000010</span></span>                      |
| <span data-ttu-id="b3270-233">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="b3270-233">Classes used in</span></span>        | [<span data-ttu-id="b3270-234">**In alto**</span><span class="sxs-lookup"><span data-stu-id="b3270-234">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b3270-235">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b3270-235">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b3270-236">Voce</span><span class="sxs-lookup"><span data-stu-id="b3270-236">Entry</span></span> | <span data-ttu-id="b3270-237">Valore</span><span class="sxs-lookup"><span data-stu-id="b3270-237">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b3270-238">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="b3270-238">Link-Id</span></span>                | <span data-ttu-id="b3270-239">43</span><span class="sxs-lookup"><span data-stu-id="b3270-239">43</span></span>                              |
| <span data-ttu-id="b3270-240">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b3270-240">MAPI-Id</span></span>                | <span data-ttu-id="b3270-241">0x800E</span><span class="sxs-lookup"><span data-stu-id="b3270-241">0x800E</span></span>                          |
| <span data-ttu-id="b3270-242">System-Only</span><span class="sxs-lookup"><span data-stu-id="b3270-242">System-Only</span></span>            | <span data-ttu-id="b3270-243">Vero</span><span class="sxs-lookup"><span data-stu-id="b3270-243">True</span></span>                            |
| <span data-ttu-id="b3270-244">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="b3270-244">Is-Single-Valued</span></span>       | <span data-ttu-id="b3270-245">Falso</span><span class="sxs-lookup"><span data-stu-id="b3270-245">False</span></span>                           |
| <span data-ttu-id="b3270-246">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="b3270-246">Is Indexed</span></span>             | <span data-ttu-id="b3270-247">Falso</span><span class="sxs-lookup"><span data-stu-id="b3270-247">False</span></span>                           |
| <span data-ttu-id="b3270-248">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="b3270-248">In Global Catalog</span></span>      | <span data-ttu-id="b3270-249">Falso</span><span class="sxs-lookup"><span data-stu-id="b3270-249">False</span></span>                           |
| <span data-ttu-id="b3270-250">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="b3270-250">NT-Security-Descriptor</span></span> | <span data-ttu-id="b3270-251">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="b3270-251">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b3270-252">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b3270-252">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b3270-253">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b3270-253">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b3270-254">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b3270-254">Search-Flags</span></span>           | <span data-ttu-id="b3270-255">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b3270-255">0x00000000</span></span>                      |
| <span data-ttu-id="b3270-256">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b3270-256">System-Flags</span></span>           | <span data-ttu-id="b3270-257">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b3270-257">0x00000010</span></span>                      |
| <span data-ttu-id="b3270-258">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="b3270-258">Classes used in</span></span>        | [<span data-ttu-id="b3270-259">**In alto**</span><span class="sxs-lookup"><span data-stu-id="b3270-259">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b3270-260">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b3270-260">Windows Server 2012</span></span>



| <span data-ttu-id="b3270-261">Voce</span><span class="sxs-lookup"><span data-stu-id="b3270-261">Entry</span></span> | <span data-ttu-id="b3270-262">Valore</span><span class="sxs-lookup"><span data-stu-id="b3270-262">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b3270-263">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="b3270-263">Link-Id</span></span>                | <span data-ttu-id="b3270-264">43</span><span class="sxs-lookup"><span data-stu-id="b3270-264">43</span></span>                              |
| <span data-ttu-id="b3270-265">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b3270-265">MAPI-Id</span></span>                | <span data-ttu-id="b3270-266">0x800E</span><span class="sxs-lookup"><span data-stu-id="b3270-266">0x800E</span></span>                          |
| <span data-ttu-id="b3270-267">System-Only</span><span class="sxs-lookup"><span data-stu-id="b3270-267">System-Only</span></span>            | <span data-ttu-id="b3270-268">Vero</span><span class="sxs-lookup"><span data-stu-id="b3270-268">True</span></span>                            |
| <span data-ttu-id="b3270-269">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="b3270-269">Is-Single-Valued</span></span>       | <span data-ttu-id="b3270-270">Falso</span><span class="sxs-lookup"><span data-stu-id="b3270-270">False</span></span>                           |
| <span data-ttu-id="b3270-271">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="b3270-271">Is Indexed</span></span>             | <span data-ttu-id="b3270-272">Falso</span><span class="sxs-lookup"><span data-stu-id="b3270-272">False</span></span>                           |
| <span data-ttu-id="b3270-273">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="b3270-273">In Global Catalog</span></span>      | <span data-ttu-id="b3270-274">Falso</span><span class="sxs-lookup"><span data-stu-id="b3270-274">False</span></span>                           |
| <span data-ttu-id="b3270-275">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="b3270-275">NT-Security-Descriptor</span></span> | <span data-ttu-id="b3270-276">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="b3270-276">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b3270-277">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b3270-277">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b3270-278">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b3270-278">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b3270-279">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b3270-279">Search-Flags</span></span>           | <span data-ttu-id="b3270-280">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b3270-280">0x00000000</span></span>                      |
| <span data-ttu-id="b3270-281">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b3270-281">System-Flags</span></span>           | <span data-ttu-id="b3270-282">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b3270-282">0x00000010</span></span>                      |
| <span data-ttu-id="b3270-283">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="b3270-283">Classes used in</span></span>        | [<span data-ttu-id="b3270-284">**In alto**</span><span class="sxs-lookup"><span data-stu-id="b3270-284">**Top**</span></span>](c-top.md)<br/> |



 

 





