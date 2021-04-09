---
title: Attributo GPC-WQL-Filter
description: Utilizzato per archiviare una stringa che contiene un GUID per il filtro e un percorso dello spazio dei nomi WMI.
ms.assetid: ea76239b-79e2-49b2-a848-a924450d332a
ms.tgt_platform: multiple
keywords:
- GPC-WQL-filtrare l'attributo AD schema
- Schema AD dell'attributo gPCWQLFilter
topic_type:
- apiref
api_name:
- GPC-WQL-Filter
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c9a6b8d3715c1692e93579d3c94cdfa44f4192e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103875474"
---
# <a name="gpc-wql-filter-attribute"></a><span data-ttu-id="d2647-105">Attributo GPC-WQL-Filter</span><span class="sxs-lookup"><span data-stu-id="d2647-105">GPC-WQL-Filter attribute</span></span>

<span data-ttu-id="d2647-106">Utilizzato per archiviare una stringa che contiene un GUID per il filtro e un percorso dello spazio dei nomi WMI.</span><span class="sxs-lookup"><span data-stu-id="d2647-106">Used to store a string that contains a GUID for the filter and a WMI namespace path.</span></span>



| <span data-ttu-id="d2647-107">Voce</span><span class="sxs-lookup"><span data-stu-id="d2647-107">Entry</span></span> | <span data-ttu-id="d2647-108">Valore</span><span class="sxs-lookup"><span data-stu-id="d2647-108">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="d2647-109">CN</span><span class="sxs-lookup"><span data-stu-id="d2647-109">CN</span></span>                | <span data-ttu-id="d2647-110">GPC-WQL-filtro</span><span class="sxs-lookup"><span data-stu-id="d2647-110">GPC-WQL-Filter</span></span>                                                                  |
| <span data-ttu-id="d2647-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="d2647-111">Ldap-Display-Name</span></span> | <span data-ttu-id="d2647-112">gPCWQLFilter</span><span class="sxs-lookup"><span data-stu-id="d2647-112">gPCWQLFilter</span></span>                                                                    |
| <span data-ttu-id="d2647-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="d2647-113">Size</span></span>              | \-                                                                              |
| <span data-ttu-id="d2647-114">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="d2647-114">Update Privilege</span></span>  | <span data-ttu-id="d2647-115">Amministratore di dominio</span><span class="sxs-lookup"><span data-stu-id="d2647-115">Domain administrator</span></span>                                                            |
| <span data-ttu-id="d2647-116">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="d2647-116">Update Frequency</span></span>  | <span data-ttu-id="d2647-117">Solo quando l'amministratore modifica la proprietà Filter nell'interfaccia utente di Criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="d2647-117">Only when the administrator changes the filter property in the Group Policy UI.</span></span> |
| <span data-ttu-id="d2647-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="d2647-118">Attribute-Id</span></span>      | <span data-ttu-id="d2647-119">1.2.840.113556.1.4.1694</span><span class="sxs-lookup"><span data-stu-id="d2647-119">1.2.840.113556.1.4.1694</span></span>                                                         |
| <span data-ttu-id="d2647-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="d2647-120">System-Id-Guid</span></span>    | <span data-ttu-id="d2647-121">7bd4c7a6-1add-4436-8c04-3999a880154c</span><span class="sxs-lookup"><span data-stu-id="d2647-121">7bd4c7a6-1add-4436-8c04-3999a880154c</span></span>                                            |
| <span data-ttu-id="d2647-122">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d2647-122">Syntax</span></span>            | [<span data-ttu-id="d2647-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="d2647-123">**String(Unicode)**</span></span>](s-string-unicode.md)                                     |



## <a name="implementations"></a><span data-ttu-id="d2647-124">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="d2647-124">Implementations</span></span>

-   [<span data-ttu-id="d2647-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="d2647-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="d2647-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="d2647-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="d2647-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="d2647-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="d2647-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="d2647-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="d2647-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="d2647-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="d2647-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d2647-130">Windows Server 2003</span></span>



| <span data-ttu-id="d2647-131">Voce</span><span class="sxs-lookup"><span data-stu-id="d2647-131">Entry</span></span> | <span data-ttu-id="d2647-132">Valore</span><span class="sxs-lookup"><span data-stu-id="d2647-132">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="d2647-133">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="d2647-133">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="d2647-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d2647-134">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="d2647-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="d2647-135">System-Only</span></span>            | <span data-ttu-id="d2647-136">Falso</span><span class="sxs-lookup"><span data-stu-id="d2647-136">False</span></span>                                                               |
| <span data-ttu-id="d2647-137">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="d2647-137">Is-Single-Valued</span></span>       | <span data-ttu-id="d2647-138">Vero</span><span class="sxs-lookup"><span data-stu-id="d2647-138">True</span></span>                                                                |
| <span data-ttu-id="d2647-139">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="d2647-139">Is Indexed</span></span>             | <span data-ttu-id="d2647-140">Falso</span><span class="sxs-lookup"><span data-stu-id="d2647-140">False</span></span>                                                               |
| <span data-ttu-id="d2647-141">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="d2647-141">In Global Catalog</span></span>      | <span data-ttu-id="d2647-142">Falso</span><span class="sxs-lookup"><span data-stu-id="d2647-142">False</span></span>                                                               |
| <span data-ttu-id="d2647-143">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="d2647-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="d2647-144">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="d2647-144">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="d2647-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d2647-145">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="d2647-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d2647-146">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="d2647-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d2647-147">Search-Flags</span></span>           | <span data-ttu-id="d2647-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d2647-148">0x00000000</span></span>                                                          |
| <span data-ttu-id="d2647-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d2647-149">System-Flags</span></span>           | <span data-ttu-id="d2647-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d2647-150">0x00000010</span></span>                                                          |
| <span data-ttu-id="d2647-151">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="d2647-151">Classes used in</span></span>        | [<span data-ttu-id="d2647-152">**Gruppo-criteri-contenitore**</span><span class="sxs-lookup"><span data-stu-id="d2647-152">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="d2647-153">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="d2647-153">Windows Server 2003 R2</span></span>



| <span data-ttu-id="d2647-154">Voce</span><span class="sxs-lookup"><span data-stu-id="d2647-154">Entry</span></span> | <span data-ttu-id="d2647-155">Valore</span><span class="sxs-lookup"><span data-stu-id="d2647-155">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="d2647-156">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="d2647-156">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="d2647-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d2647-157">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="d2647-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="d2647-158">System-Only</span></span>            | <span data-ttu-id="d2647-159">Falso</span><span class="sxs-lookup"><span data-stu-id="d2647-159">False</span></span>                                                               |
| <span data-ttu-id="d2647-160">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="d2647-160">Is-Single-Valued</span></span>       | <span data-ttu-id="d2647-161">Vero</span><span class="sxs-lookup"><span data-stu-id="d2647-161">True</span></span>                                                                |
| <span data-ttu-id="d2647-162">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="d2647-162">Is Indexed</span></span>             | <span data-ttu-id="d2647-163">Falso</span><span class="sxs-lookup"><span data-stu-id="d2647-163">False</span></span>                                                               |
| <span data-ttu-id="d2647-164">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="d2647-164">In Global Catalog</span></span>      | <span data-ttu-id="d2647-165">Falso</span><span class="sxs-lookup"><span data-stu-id="d2647-165">False</span></span>                                                               |
| <span data-ttu-id="d2647-166">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="d2647-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="d2647-167">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="d2647-167">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="d2647-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d2647-168">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="d2647-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d2647-169">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="d2647-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d2647-170">Search-Flags</span></span>           | <span data-ttu-id="d2647-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d2647-171">0x00000000</span></span>                                                          |
| <span data-ttu-id="d2647-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d2647-172">System-Flags</span></span>           | <span data-ttu-id="d2647-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d2647-173">0x00000010</span></span>                                                          |
| <span data-ttu-id="d2647-174">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="d2647-174">Classes used in</span></span>        | [<span data-ttu-id="d2647-175">**Gruppo-criteri-contenitore**</span><span class="sxs-lookup"><span data-stu-id="d2647-175">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="d2647-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d2647-176">Windows Server 2008</span></span>



| <span data-ttu-id="d2647-177">Voce</span><span class="sxs-lookup"><span data-stu-id="d2647-177">Entry</span></span> | <span data-ttu-id="d2647-178">Valore</span><span class="sxs-lookup"><span data-stu-id="d2647-178">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="d2647-179">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="d2647-179">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="d2647-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d2647-180">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="d2647-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="d2647-181">System-Only</span></span>            | <span data-ttu-id="d2647-182">Falso</span><span class="sxs-lookup"><span data-stu-id="d2647-182">False</span></span>                                                               |
| <span data-ttu-id="d2647-183">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="d2647-183">Is-Single-Valued</span></span>       | <span data-ttu-id="d2647-184">Vero</span><span class="sxs-lookup"><span data-stu-id="d2647-184">True</span></span>                                                                |
| <span data-ttu-id="d2647-185">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="d2647-185">Is Indexed</span></span>             | <span data-ttu-id="d2647-186">Falso</span><span class="sxs-lookup"><span data-stu-id="d2647-186">False</span></span>                                                               |
| <span data-ttu-id="d2647-187">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="d2647-187">In Global Catalog</span></span>      | <span data-ttu-id="d2647-188">Falso</span><span class="sxs-lookup"><span data-stu-id="d2647-188">False</span></span>                                                               |
| <span data-ttu-id="d2647-189">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="d2647-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="d2647-190">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="d2647-190">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="d2647-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d2647-191">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="d2647-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d2647-192">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="d2647-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d2647-193">Search-Flags</span></span>           | <span data-ttu-id="d2647-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d2647-194">0x00000000</span></span>                                                          |
| <span data-ttu-id="d2647-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d2647-195">System-Flags</span></span>           | <span data-ttu-id="d2647-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d2647-196">0x00000010</span></span>                                                          |
| <span data-ttu-id="d2647-197">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="d2647-197">Classes used in</span></span>        | [<span data-ttu-id="d2647-198">**Gruppo-criteri-contenitore**</span><span class="sxs-lookup"><span data-stu-id="d2647-198">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="d2647-199">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d2647-199">Windows Server 2008 R2</span></span>



| <span data-ttu-id="d2647-200">Voce</span><span class="sxs-lookup"><span data-stu-id="d2647-200">Entry</span></span> | <span data-ttu-id="d2647-201">Valore</span><span class="sxs-lookup"><span data-stu-id="d2647-201">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="d2647-202">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="d2647-202">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="d2647-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d2647-203">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="d2647-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="d2647-204">System-Only</span></span>            | <span data-ttu-id="d2647-205">Falso</span><span class="sxs-lookup"><span data-stu-id="d2647-205">False</span></span>                                                               |
| <span data-ttu-id="d2647-206">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="d2647-206">Is-Single-Valued</span></span>       | <span data-ttu-id="d2647-207">Vero</span><span class="sxs-lookup"><span data-stu-id="d2647-207">True</span></span>                                                                |
| <span data-ttu-id="d2647-208">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="d2647-208">Is Indexed</span></span>             | <span data-ttu-id="d2647-209">Falso</span><span class="sxs-lookup"><span data-stu-id="d2647-209">False</span></span>                                                               |
| <span data-ttu-id="d2647-210">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="d2647-210">In Global Catalog</span></span>      | <span data-ttu-id="d2647-211">Falso</span><span class="sxs-lookup"><span data-stu-id="d2647-211">False</span></span>                                                               |
| <span data-ttu-id="d2647-212">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="d2647-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="d2647-213">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="d2647-213">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="d2647-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d2647-214">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="d2647-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d2647-215">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="d2647-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d2647-216">Search-Flags</span></span>           | <span data-ttu-id="d2647-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d2647-217">0x00000000</span></span>                                                          |
| <span data-ttu-id="d2647-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d2647-218">System-Flags</span></span>           | <span data-ttu-id="d2647-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d2647-219">0x00000010</span></span>                                                          |
| <span data-ttu-id="d2647-220">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="d2647-220">Classes used in</span></span>        | [<span data-ttu-id="d2647-221">**Gruppo-criteri-contenitore**</span><span class="sxs-lookup"><span data-stu-id="d2647-221">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="d2647-222">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d2647-222">Windows Server 2012</span></span>



| <span data-ttu-id="d2647-223">Voce</span><span class="sxs-lookup"><span data-stu-id="d2647-223">Entry</span></span> | <span data-ttu-id="d2647-224">Valore</span><span class="sxs-lookup"><span data-stu-id="d2647-224">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="d2647-225">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="d2647-225">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="d2647-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d2647-226">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="d2647-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="d2647-227">System-Only</span></span>            | <span data-ttu-id="d2647-228">Falso</span><span class="sxs-lookup"><span data-stu-id="d2647-228">False</span></span>                                                               |
| <span data-ttu-id="d2647-229">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="d2647-229">Is-Single-Valued</span></span>       | <span data-ttu-id="d2647-230">Vero</span><span class="sxs-lookup"><span data-stu-id="d2647-230">True</span></span>                                                                |
| <span data-ttu-id="d2647-231">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="d2647-231">Is Indexed</span></span>             | <span data-ttu-id="d2647-232">Falso</span><span class="sxs-lookup"><span data-stu-id="d2647-232">False</span></span>                                                               |
| <span data-ttu-id="d2647-233">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="d2647-233">In Global Catalog</span></span>      | <span data-ttu-id="d2647-234">Falso</span><span class="sxs-lookup"><span data-stu-id="d2647-234">False</span></span>                                                               |
| <span data-ttu-id="d2647-235">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="d2647-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="d2647-236">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="d2647-236">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="d2647-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d2647-237">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="d2647-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d2647-238">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="d2647-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d2647-239">Search-Flags</span></span>           | <span data-ttu-id="d2647-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d2647-240">0x00000000</span></span>                                                          |
| <span data-ttu-id="d2647-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d2647-241">System-Flags</span></span>           | <span data-ttu-id="d2647-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d2647-242">0x00000010</span></span>                                                          |
| <span data-ttu-id="d2647-243">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="d2647-243">Classes used in</span></span>        | [<span data-ttu-id="d2647-244">**Gruppo-criteri-contenitore**</span><span class="sxs-lookup"><span data-stu-id="d2647-244">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



 

 





