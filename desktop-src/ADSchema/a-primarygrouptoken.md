---
title: Primary-Group-token-attributo
description: Attributo calcolato utilizzato per recuperare l'elenco di appartenenze di un gruppo, ad esempio gli utenti di dominio. L'appartenenza completa di tali gruppi non viene archiviata in modo esplicito per motivi di scalabilità.
ms.assetid: b23d3b7f-074b-4f1b-bc06-b22738a8a79e
ms.tgt_platform: multiple
keywords:
- Primary-Group-token attributo AD schema
- Schema AD dell'attributo primaryGroupToken
topic_type:
- apiref
api_name:
- Primary-Group-Token
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b237ab5998ca3f38f2d07128b36d9337c96935d
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104122390"
---
# <a name="primary-group-token-attribute"></a><span data-ttu-id="362ae-106">Primary-Group-token-attributo</span><span class="sxs-lookup"><span data-stu-id="362ae-106">Primary-Group-Token attribute</span></span>

<span data-ttu-id="362ae-107">Attributo calcolato utilizzato per recuperare l'elenco di appartenenze di un gruppo, ad esempio gli utenti di dominio.</span><span class="sxs-lookup"><span data-stu-id="362ae-107">A computed attribute that is used in retrieving the membership list of a group, such as Domain Users.</span></span> <span data-ttu-id="362ae-108">L'appartenenza completa di tali gruppi non viene archiviata in modo esplicito per motivi di scalabilità.</span><span class="sxs-lookup"><span data-stu-id="362ae-108">The complete membership of such groups is not stored explicitly for scaling reasons.</span></span>



| <span data-ttu-id="362ae-109">Voce</span><span class="sxs-lookup"><span data-stu-id="362ae-109">Entry</span></span> | <span data-ttu-id="362ae-110">Valore</span><span class="sxs-lookup"><span data-stu-id="362ae-110">Value</span></span> |
|-------------------|--------------------------------------------|
| <span data-ttu-id="362ae-111">CN</span><span class="sxs-lookup"><span data-stu-id="362ae-111">CN</span></span>                | <span data-ttu-id="362ae-112">Primary-Group-token</span><span class="sxs-lookup"><span data-stu-id="362ae-112">Primary-Group-Token</span></span>                        |
| <span data-ttu-id="362ae-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="362ae-113">Ldap-Display-Name</span></span> | <span data-ttu-id="362ae-114">primaryGroupToken</span><span class="sxs-lookup"><span data-stu-id="362ae-114">primaryGroupToken</span></span>                          |
| <span data-ttu-id="362ae-115">Dimensione</span><span class="sxs-lookup"><span data-stu-id="362ae-115">Size</span></span>              | <span data-ttu-id="362ae-116">4 byte</span><span class="sxs-lookup"><span data-stu-id="362ae-116">4 bytes</span></span>                                    |
| <span data-ttu-id="362ae-117">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="362ae-117">Update Privilege</span></span>  | <span data-ttu-id="362ae-118">Questo valore viene impostato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="362ae-118">This value is set by the system.</span></span>           |
| <span data-ttu-id="362ae-119">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="362ae-119">Update Frequency</span></span>  | <span data-ttu-id="362ae-120">Quando viene modificato un gruppo primario di oggetti.</span><span class="sxs-lookup"><span data-stu-id="362ae-120">Whenever an objects primary group changes.</span></span> |
| <span data-ttu-id="362ae-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="362ae-121">Attribute-Id</span></span>      | <span data-ttu-id="362ae-122">1.2.840.113556.1.4.1412</span><span class="sxs-lookup"><span data-stu-id="362ae-122">1.2.840.113556.1.4.1412</span></span>                    |
| <span data-ttu-id="362ae-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="362ae-123">System-Id-Guid</span></span>    | <span data-ttu-id="362ae-124">c0ed8738-7efd-4481-84d9-66d2db8be369</span><span class="sxs-lookup"><span data-stu-id="362ae-124">c0ed8738-7efd-4481-84d9-66d2db8be369</span></span>       |
| <span data-ttu-id="362ae-125">Sintassi</span><span class="sxs-lookup"><span data-stu-id="362ae-125">Syntax</span></span>            | [<span data-ttu-id="362ae-126">**Enumerazione**</span><span class="sxs-lookup"><span data-stu-id="362ae-126">**Enumeration**</span></span>](s-enumeration.md)       |



## <a name="implementations"></a><span data-ttu-id="362ae-127">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="362ae-127">Implementations</span></span>

-   [<span data-ttu-id="362ae-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="362ae-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="362ae-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="362ae-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="362ae-130">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="362ae-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="362ae-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="362ae-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="362ae-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="362ae-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="362ae-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="362ae-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="362ae-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="362ae-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="362ae-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="362ae-135">Windows 2000 Server</span></span>



| <span data-ttu-id="362ae-136">Voce</span><span class="sxs-lookup"><span data-stu-id="362ae-136">Entry</span></span> | <span data-ttu-id="362ae-137">Valore</span><span class="sxs-lookup"><span data-stu-id="362ae-137">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="362ae-138">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="362ae-138">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="362ae-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="362ae-139">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="362ae-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="362ae-140">System-Only</span></span>            | <span data-ttu-id="362ae-141">Vero</span><span class="sxs-lookup"><span data-stu-id="362ae-141">True</span></span>                                |
| <span data-ttu-id="362ae-142">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="362ae-142">Is-Single-Valued</span></span>       | <span data-ttu-id="362ae-143">Vero</span><span class="sxs-lookup"><span data-stu-id="362ae-143">True</span></span>                                |
| <span data-ttu-id="362ae-144">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="362ae-144">Is Indexed</span></span>             | <span data-ttu-id="362ae-145">Falso</span><span class="sxs-lookup"><span data-stu-id="362ae-145">False</span></span>                               |
| <span data-ttu-id="362ae-146">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="362ae-146">In Global Catalog</span></span>      | <span data-ttu-id="362ae-147">Falso</span><span class="sxs-lookup"><span data-stu-id="362ae-147">False</span></span>                               |
| <span data-ttu-id="362ae-148">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="362ae-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="362ae-149">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="362ae-149">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="362ae-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="362ae-150">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="362ae-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="362ae-151">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="362ae-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="362ae-152">Search-Flags</span></span>           | <span data-ttu-id="362ae-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="362ae-153">0x00000000</span></span>                          |
| <span data-ttu-id="362ae-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="362ae-154">System-Flags</span></span>           | <span data-ttu-id="362ae-155">0x00000014</span><span class="sxs-lookup"><span data-stu-id="362ae-155">0x00000014</span></span>                          |
| <span data-ttu-id="362ae-156">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="362ae-156">Classes used in</span></span>        | [<span data-ttu-id="362ae-157">**Group**</span><span class="sxs-lookup"><span data-stu-id="362ae-157">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="362ae-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="362ae-158">Windows Server 2003</span></span>



| <span data-ttu-id="362ae-159">Voce</span><span class="sxs-lookup"><span data-stu-id="362ae-159">Entry</span></span> | <span data-ttu-id="362ae-160">Valore</span><span class="sxs-lookup"><span data-stu-id="362ae-160">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="362ae-161">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="362ae-161">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="362ae-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="362ae-162">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="362ae-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="362ae-163">System-Only</span></span>            | <span data-ttu-id="362ae-164">Vero</span><span class="sxs-lookup"><span data-stu-id="362ae-164">True</span></span>                                |
| <span data-ttu-id="362ae-165">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="362ae-165">Is-Single-Valued</span></span>       | <span data-ttu-id="362ae-166">Vero</span><span class="sxs-lookup"><span data-stu-id="362ae-166">True</span></span>                                |
| <span data-ttu-id="362ae-167">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="362ae-167">Is Indexed</span></span>             | <span data-ttu-id="362ae-168">Falso</span><span class="sxs-lookup"><span data-stu-id="362ae-168">False</span></span>                               |
| <span data-ttu-id="362ae-169">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="362ae-169">In Global Catalog</span></span>      | <span data-ttu-id="362ae-170">Falso</span><span class="sxs-lookup"><span data-stu-id="362ae-170">False</span></span>                               |
| <span data-ttu-id="362ae-171">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="362ae-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="362ae-172">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="362ae-172">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="362ae-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="362ae-173">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="362ae-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="362ae-174">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="362ae-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="362ae-175">Search-Flags</span></span>           | <span data-ttu-id="362ae-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="362ae-176">0x00000000</span></span>                          |
| <span data-ttu-id="362ae-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="362ae-177">System-Flags</span></span>           | <span data-ttu-id="362ae-178">0x00000014</span><span class="sxs-lookup"><span data-stu-id="362ae-178">0x00000014</span></span>                          |
| <span data-ttu-id="362ae-179">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="362ae-179">Classes used in</span></span>        | [<span data-ttu-id="362ae-180">**Group**</span><span class="sxs-lookup"><span data-stu-id="362ae-180">**Group**</span></span>](c-group.md)<br/> |



## <a name="adam"></a><span data-ttu-id="362ae-181">ADAM</span><span class="sxs-lookup"><span data-stu-id="362ae-181">ADAM</span></span>



| <span data-ttu-id="362ae-182">Voce</span><span class="sxs-lookup"><span data-stu-id="362ae-182">Entry</span></span> | <span data-ttu-id="362ae-183">Valore</span><span class="sxs-lookup"><span data-stu-id="362ae-183">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="362ae-184">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="362ae-184">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="362ae-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="362ae-185">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="362ae-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="362ae-186">System-Only</span></span>            | <span data-ttu-id="362ae-187">Vero</span><span class="sxs-lookup"><span data-stu-id="362ae-187">True</span></span>                                |
| <span data-ttu-id="362ae-188">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="362ae-188">Is-Single-Valued</span></span>       | <span data-ttu-id="362ae-189">Vero</span><span class="sxs-lookup"><span data-stu-id="362ae-189">True</span></span>                                |
| <span data-ttu-id="362ae-190">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="362ae-190">Is Indexed</span></span>             | <span data-ttu-id="362ae-191">Falso</span><span class="sxs-lookup"><span data-stu-id="362ae-191">False</span></span>                               |
| <span data-ttu-id="362ae-192">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="362ae-192">In Global Catalog</span></span>      | <span data-ttu-id="362ae-193">Falso</span><span class="sxs-lookup"><span data-stu-id="362ae-193">False</span></span>                               |
| <span data-ttu-id="362ae-194">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="362ae-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="362ae-195">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="362ae-195">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="362ae-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="362ae-196">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="362ae-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="362ae-197">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="362ae-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="362ae-198">Search-Flags</span></span>           | <span data-ttu-id="362ae-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="362ae-199">0x00000000</span></span>                          |
| <span data-ttu-id="362ae-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="362ae-200">System-Flags</span></span>           | <span data-ttu-id="362ae-201">0x00000014</span><span class="sxs-lookup"><span data-stu-id="362ae-201">0x00000014</span></span>                          |
| <span data-ttu-id="362ae-202">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="362ae-202">Classes used in</span></span>        | [<span data-ttu-id="362ae-203">**Group**</span><span class="sxs-lookup"><span data-stu-id="362ae-203">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="362ae-204">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="362ae-204">Windows Server 2003 R2</span></span>



| <span data-ttu-id="362ae-205">Voce</span><span class="sxs-lookup"><span data-stu-id="362ae-205">Entry</span></span> | <span data-ttu-id="362ae-206">Valore</span><span class="sxs-lookup"><span data-stu-id="362ae-206">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="362ae-207">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="362ae-207">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="362ae-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="362ae-208">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="362ae-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="362ae-209">System-Only</span></span>            | <span data-ttu-id="362ae-210">Vero</span><span class="sxs-lookup"><span data-stu-id="362ae-210">True</span></span>                                |
| <span data-ttu-id="362ae-211">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="362ae-211">Is-Single-Valued</span></span>       | <span data-ttu-id="362ae-212">Vero</span><span class="sxs-lookup"><span data-stu-id="362ae-212">True</span></span>                                |
| <span data-ttu-id="362ae-213">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="362ae-213">Is Indexed</span></span>             | <span data-ttu-id="362ae-214">Falso</span><span class="sxs-lookup"><span data-stu-id="362ae-214">False</span></span>                               |
| <span data-ttu-id="362ae-215">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="362ae-215">In Global Catalog</span></span>      | <span data-ttu-id="362ae-216">Falso</span><span class="sxs-lookup"><span data-stu-id="362ae-216">False</span></span>                               |
| <span data-ttu-id="362ae-217">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="362ae-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="362ae-218">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="362ae-218">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="362ae-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="362ae-219">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="362ae-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="362ae-220">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="362ae-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="362ae-221">Search-Flags</span></span>           | <span data-ttu-id="362ae-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="362ae-222">0x00000000</span></span>                          |
| <span data-ttu-id="362ae-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="362ae-223">System-Flags</span></span>           | <span data-ttu-id="362ae-224">0x00000014</span><span class="sxs-lookup"><span data-stu-id="362ae-224">0x00000014</span></span>                          |
| <span data-ttu-id="362ae-225">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="362ae-225">Classes used in</span></span>        | [<span data-ttu-id="362ae-226">**Group**</span><span class="sxs-lookup"><span data-stu-id="362ae-226">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="362ae-227">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="362ae-227">Windows Server 2008</span></span>



| <span data-ttu-id="362ae-228">Voce</span><span class="sxs-lookup"><span data-stu-id="362ae-228">Entry</span></span> | <span data-ttu-id="362ae-229">Valore</span><span class="sxs-lookup"><span data-stu-id="362ae-229">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="362ae-230">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="362ae-230">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="362ae-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="362ae-231">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="362ae-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="362ae-232">System-Only</span></span>            | <span data-ttu-id="362ae-233">Vero</span><span class="sxs-lookup"><span data-stu-id="362ae-233">True</span></span>                                |
| <span data-ttu-id="362ae-234">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="362ae-234">Is-Single-Valued</span></span>       | <span data-ttu-id="362ae-235">Vero</span><span class="sxs-lookup"><span data-stu-id="362ae-235">True</span></span>                                |
| <span data-ttu-id="362ae-236">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="362ae-236">Is Indexed</span></span>             | <span data-ttu-id="362ae-237">Falso</span><span class="sxs-lookup"><span data-stu-id="362ae-237">False</span></span>                               |
| <span data-ttu-id="362ae-238">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="362ae-238">In Global Catalog</span></span>      | <span data-ttu-id="362ae-239">Falso</span><span class="sxs-lookup"><span data-stu-id="362ae-239">False</span></span>                               |
| <span data-ttu-id="362ae-240">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="362ae-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="362ae-241">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="362ae-241">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="362ae-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="362ae-242">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="362ae-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="362ae-243">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="362ae-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="362ae-244">Search-Flags</span></span>           | <span data-ttu-id="362ae-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="362ae-245">0x00000000</span></span>                          |
| <span data-ttu-id="362ae-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="362ae-246">System-Flags</span></span>           | <span data-ttu-id="362ae-247">0x00000014</span><span class="sxs-lookup"><span data-stu-id="362ae-247">0x00000014</span></span>                          |
| <span data-ttu-id="362ae-248">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="362ae-248">Classes used in</span></span>        | [<span data-ttu-id="362ae-249">**Group**</span><span class="sxs-lookup"><span data-stu-id="362ae-249">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="362ae-250">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="362ae-250">Windows Server 2008 R2</span></span>



| <span data-ttu-id="362ae-251">Voce</span><span class="sxs-lookup"><span data-stu-id="362ae-251">Entry</span></span> | <span data-ttu-id="362ae-252">Valore</span><span class="sxs-lookup"><span data-stu-id="362ae-252">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="362ae-253">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="362ae-253">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="362ae-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="362ae-254">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="362ae-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="362ae-255">System-Only</span></span>            | <span data-ttu-id="362ae-256">Vero</span><span class="sxs-lookup"><span data-stu-id="362ae-256">True</span></span>                                |
| <span data-ttu-id="362ae-257">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="362ae-257">Is-Single-Valued</span></span>       | <span data-ttu-id="362ae-258">Vero</span><span class="sxs-lookup"><span data-stu-id="362ae-258">True</span></span>                                |
| <span data-ttu-id="362ae-259">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="362ae-259">Is Indexed</span></span>             | <span data-ttu-id="362ae-260">Falso</span><span class="sxs-lookup"><span data-stu-id="362ae-260">False</span></span>                               |
| <span data-ttu-id="362ae-261">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="362ae-261">In Global Catalog</span></span>      | <span data-ttu-id="362ae-262">Falso</span><span class="sxs-lookup"><span data-stu-id="362ae-262">False</span></span>                               |
| <span data-ttu-id="362ae-263">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="362ae-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="362ae-264">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="362ae-264">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="362ae-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="362ae-265">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="362ae-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="362ae-266">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="362ae-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="362ae-267">Search-Flags</span></span>           | <span data-ttu-id="362ae-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="362ae-268">0x00000000</span></span>                          |
| <span data-ttu-id="362ae-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="362ae-269">System-Flags</span></span>           | <span data-ttu-id="362ae-270">0x00000014</span><span class="sxs-lookup"><span data-stu-id="362ae-270">0x00000014</span></span>                          |
| <span data-ttu-id="362ae-271">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="362ae-271">Classes used in</span></span>        | [<span data-ttu-id="362ae-272">**Group**</span><span class="sxs-lookup"><span data-stu-id="362ae-272">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="362ae-273">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="362ae-273">Windows Server 2012</span></span>



| <span data-ttu-id="362ae-274">Voce</span><span class="sxs-lookup"><span data-stu-id="362ae-274">Entry</span></span> | <span data-ttu-id="362ae-275">Valore</span><span class="sxs-lookup"><span data-stu-id="362ae-275">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="362ae-276">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="362ae-276">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="362ae-277">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="362ae-277">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="362ae-278">System-Only</span><span class="sxs-lookup"><span data-stu-id="362ae-278">System-Only</span></span>            | <span data-ttu-id="362ae-279">Vero</span><span class="sxs-lookup"><span data-stu-id="362ae-279">True</span></span>                                |
| <span data-ttu-id="362ae-280">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="362ae-280">Is-Single-Valued</span></span>       | <span data-ttu-id="362ae-281">Vero</span><span class="sxs-lookup"><span data-stu-id="362ae-281">True</span></span>                                |
| <span data-ttu-id="362ae-282">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="362ae-282">Is Indexed</span></span>             | <span data-ttu-id="362ae-283">Falso</span><span class="sxs-lookup"><span data-stu-id="362ae-283">False</span></span>                               |
| <span data-ttu-id="362ae-284">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="362ae-284">In Global Catalog</span></span>      | <span data-ttu-id="362ae-285">Falso</span><span class="sxs-lookup"><span data-stu-id="362ae-285">False</span></span>                               |
| <span data-ttu-id="362ae-286">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="362ae-286">NT-Security-Descriptor</span></span> | <span data-ttu-id="362ae-287">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="362ae-287">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="362ae-288">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="362ae-288">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="362ae-289">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="362ae-289">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="362ae-290">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="362ae-290">Search-Flags</span></span>           | <span data-ttu-id="362ae-291">0x00000000</span><span class="sxs-lookup"><span data-stu-id="362ae-291">0x00000000</span></span>                          |
| <span data-ttu-id="362ae-292">System-Flags</span><span class="sxs-lookup"><span data-stu-id="362ae-292">System-Flags</span></span>           | <span data-ttu-id="362ae-293">0x00000014</span><span class="sxs-lookup"><span data-stu-id="362ae-293">0x00000014</span></span>                          |
| <span data-ttu-id="362ae-294">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="362ae-294">Classes used in</span></span>        | [<span data-ttu-id="362ae-295">**Group**</span><span class="sxs-lookup"><span data-stu-id="362ae-295">**Group**</span></span>](c-group.md)<br/> |



 

 





