---
title: Attributo REPL-Property-meta-data
description: Tiene traccia delle informazioni interne sullo stato di replica per gli oggetti DS. Le informazioni possono essere estratte in formato pubblico tramite l'API pubblica DsReplicaGetInfo (). Presente in tutti gli oggetti DS.
ms.assetid: 5776208c-8138-4b0a-855a-8bddcbd2e532
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo REPL-Property-meta-data
- Schema AD dell'attributo replPropertyMetaData
topic_type:
- apiref
api_name:
- Repl-Property-Meta-Data
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7639d9bca600457d519862e1f57d9ee698d2a155
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744906"
---
# <a name="repl-property-meta-data-attribute"></a><span data-ttu-id="592d8-107">Attributo REPL-Property-meta-data</span><span class="sxs-lookup"><span data-stu-id="592d8-107">Repl-Property-Meta-Data attribute</span></span>

<span data-ttu-id="592d8-108">Tiene traccia delle informazioni interne sullo stato di replica per gli oggetti DS.</span><span class="sxs-lookup"><span data-stu-id="592d8-108">Tracks internal replication state information for DS objects.</span></span> <span data-ttu-id="592d8-109">Le informazioni possono essere estratte in formato pubblico tramite l'API pubblica DsReplicaGetInfo ().</span><span class="sxs-lookup"><span data-stu-id="592d8-109">Information here can be extracted in public form through the public API DsReplicaGetInfo().</span></span> <span data-ttu-id="592d8-110">Presente in tutti gli oggetti DS.</span><span class="sxs-lookup"><span data-stu-id="592d8-110">Present on all DS objects.</span></span>



| <span data-ttu-id="592d8-111">Voce</span><span class="sxs-lookup"><span data-stu-id="592d8-111">Entry</span></span> | <span data-ttu-id="592d8-112">Valore</span><span class="sxs-lookup"><span data-stu-id="592d8-112">Value</span></span> |
|-------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="592d8-113">CN</span><span class="sxs-lookup"><span data-stu-id="592d8-113">CN</span></span>                | <span data-ttu-id="592d8-114">REPL-Property-meta-dati</span><span class="sxs-lookup"><span data-stu-id="592d8-114">Repl-Property-Meta-Data</span></span>                                                      |
| <span data-ttu-id="592d8-115">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="592d8-115">Ldap-Display-Name</span></span> | <span data-ttu-id="592d8-116">replPropertyMetaData</span><span class="sxs-lookup"><span data-stu-id="592d8-116">replPropertyMetaData</span></span>                                                         |
| <span data-ttu-id="592d8-117">Dimensione</span><span class="sxs-lookup"><span data-stu-id="592d8-117">Size</span></span>              | <span data-ttu-id="592d8-118">La lunghezza è proporzionale al numero di attributi replicabili sull'oggetto.</span><span class="sxs-lookup"><span data-stu-id="592d8-118">Length is proportional to the number of replicable attributes on the object.</span></span> |
| <span data-ttu-id="592d8-119">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="592d8-119">Update Privilege</span></span>  | <span data-ttu-id="592d8-120">Questo valore viene impostato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="592d8-120">This value is set by the system.</span></span>                                             |
| <span data-ttu-id="592d8-121">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="592d8-121">Update Frequency</span></span>  | <span data-ttu-id="592d8-122">Modifiche in risposta a tutte le modifiche di replica nell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="592d8-122">Changes in response to any replicating changes in the object.</span></span>                |
| <span data-ttu-id="592d8-123">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="592d8-123">Attribute-Id</span></span>      | <span data-ttu-id="592d8-124">1.2.840.113556.1.4.3</span><span class="sxs-lookup"><span data-stu-id="592d8-124">1.2.840.113556.1.4.3</span></span>                                                         |
| <span data-ttu-id="592d8-125">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="592d8-125">System-Id-Guid</span></span>    | <span data-ttu-id="592d8-126">281416c0-1968-11d0-a28f-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="592d8-126">281416c0-1968-11d0-a28f-00aa003049e2</span></span>                                         |
| <span data-ttu-id="592d8-127">Sintassi</span><span class="sxs-lookup"><span data-stu-id="592d8-127">Syntax</span></span>            | [<span data-ttu-id="592d8-128">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="592d8-128">**Object(Replica-Link)**</span></span>](s-object-replica-link.md)                        |



## <a name="implementations"></a><span data-ttu-id="592d8-129">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="592d8-129">Implementations</span></span>

-   [<span data-ttu-id="592d8-130">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="592d8-130">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="592d8-131">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="592d8-131">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="592d8-132">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="592d8-132">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="592d8-133">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="592d8-133">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="592d8-134">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="592d8-134">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="592d8-135">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="592d8-135">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="592d8-136">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="592d8-136">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="592d8-137">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="592d8-137">Windows 2000 Server</span></span>



| <span data-ttu-id="592d8-138">Voce</span><span class="sxs-lookup"><span data-stu-id="592d8-138">Entry</span></span> | <span data-ttu-id="592d8-139">Valore</span><span class="sxs-lookup"><span data-stu-id="592d8-139">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="592d8-140">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="592d8-140">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="592d8-141">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="592d8-141">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="592d8-142">System-Only</span><span class="sxs-lookup"><span data-stu-id="592d8-142">System-Only</span></span>            | <span data-ttu-id="592d8-143">Vero</span><span class="sxs-lookup"><span data-stu-id="592d8-143">True</span></span>                            |
| <span data-ttu-id="592d8-144">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="592d8-144">Is-Single-Valued</span></span>       | <span data-ttu-id="592d8-145">Vero</span><span class="sxs-lookup"><span data-stu-id="592d8-145">True</span></span>                            |
| <span data-ttu-id="592d8-146">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="592d8-146">Is Indexed</span></span>             | <span data-ttu-id="592d8-147">Falso</span><span class="sxs-lookup"><span data-stu-id="592d8-147">False</span></span>                           |
| <span data-ttu-id="592d8-148">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="592d8-148">In Global Catalog</span></span>      | <span data-ttu-id="592d8-149">Vero</span><span class="sxs-lookup"><span data-stu-id="592d8-149">True</span></span>                            |
| <span data-ttu-id="592d8-150">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="592d8-150">NT-Security-Descriptor</span></span> | <span data-ttu-id="592d8-151">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="592d8-151">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="592d8-152">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="592d8-152">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="592d8-153">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="592d8-153">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="592d8-154">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="592d8-154">Search-Flags</span></span>           | <span data-ttu-id="592d8-155">0x00000008</span><span class="sxs-lookup"><span data-stu-id="592d8-155">0x00000008</span></span>                      |
| <span data-ttu-id="592d8-156">System-Flags</span><span class="sxs-lookup"><span data-stu-id="592d8-156">System-Flags</span></span>           | <span data-ttu-id="592d8-157">0x00000013</span><span class="sxs-lookup"><span data-stu-id="592d8-157">0x00000013</span></span>                      |
| <span data-ttu-id="592d8-158">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="592d8-158">Classes used in</span></span>        | [<span data-ttu-id="592d8-159">**In alto**</span><span class="sxs-lookup"><span data-stu-id="592d8-159">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="592d8-160">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="592d8-160">Windows Server 2003</span></span>



| <span data-ttu-id="592d8-161">Voce</span><span class="sxs-lookup"><span data-stu-id="592d8-161">Entry</span></span> | <span data-ttu-id="592d8-162">Valore</span><span class="sxs-lookup"><span data-stu-id="592d8-162">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="592d8-163">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="592d8-163">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="592d8-164">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="592d8-164">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="592d8-165">System-Only</span><span class="sxs-lookup"><span data-stu-id="592d8-165">System-Only</span></span>            | <span data-ttu-id="592d8-166">Vero</span><span class="sxs-lookup"><span data-stu-id="592d8-166">True</span></span>                            |
| <span data-ttu-id="592d8-167">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="592d8-167">Is-Single-Valued</span></span>       | <span data-ttu-id="592d8-168">Vero</span><span class="sxs-lookup"><span data-stu-id="592d8-168">True</span></span>                            |
| <span data-ttu-id="592d8-169">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="592d8-169">Is Indexed</span></span>             | <span data-ttu-id="592d8-170">Falso</span><span class="sxs-lookup"><span data-stu-id="592d8-170">False</span></span>                           |
| <span data-ttu-id="592d8-171">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="592d8-171">In Global Catalog</span></span>      | <span data-ttu-id="592d8-172">Vero</span><span class="sxs-lookup"><span data-stu-id="592d8-172">True</span></span>                            |
| <span data-ttu-id="592d8-173">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="592d8-173">NT-Security-Descriptor</span></span> | <span data-ttu-id="592d8-174">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="592d8-174">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="592d8-175">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="592d8-175">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="592d8-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="592d8-176">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="592d8-177">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="592d8-177">Search-Flags</span></span>           | <span data-ttu-id="592d8-178">0x00000008</span><span class="sxs-lookup"><span data-stu-id="592d8-178">0x00000008</span></span>                      |
| <span data-ttu-id="592d8-179">System-Flags</span><span class="sxs-lookup"><span data-stu-id="592d8-179">System-Flags</span></span>           | <span data-ttu-id="592d8-180">0x0000001B</span><span class="sxs-lookup"><span data-stu-id="592d8-180">0x0000001B</span></span>                      |
| <span data-ttu-id="592d8-181">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="592d8-181">Classes used in</span></span>        | [<span data-ttu-id="592d8-182">**In alto**</span><span class="sxs-lookup"><span data-stu-id="592d8-182">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="592d8-183">ADAM</span><span class="sxs-lookup"><span data-stu-id="592d8-183">ADAM</span></span>



| <span data-ttu-id="592d8-184">Voce</span><span class="sxs-lookup"><span data-stu-id="592d8-184">Entry</span></span> | <span data-ttu-id="592d8-185">Valore</span><span class="sxs-lookup"><span data-stu-id="592d8-185">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="592d8-186">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="592d8-186">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="592d8-187">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="592d8-187">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="592d8-188">System-Only</span><span class="sxs-lookup"><span data-stu-id="592d8-188">System-Only</span></span>            | <span data-ttu-id="592d8-189">Vero</span><span class="sxs-lookup"><span data-stu-id="592d8-189">True</span></span>                            |
| <span data-ttu-id="592d8-190">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="592d8-190">Is-Single-Valued</span></span>       | <span data-ttu-id="592d8-191">Vero</span><span class="sxs-lookup"><span data-stu-id="592d8-191">True</span></span>                            |
| <span data-ttu-id="592d8-192">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="592d8-192">Is Indexed</span></span>             | <span data-ttu-id="592d8-193">Falso</span><span class="sxs-lookup"><span data-stu-id="592d8-193">False</span></span>                           |
| <span data-ttu-id="592d8-194">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="592d8-194">In Global Catalog</span></span>      | <span data-ttu-id="592d8-195">Vero</span><span class="sxs-lookup"><span data-stu-id="592d8-195">True</span></span>                            |
| <span data-ttu-id="592d8-196">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="592d8-196">NT-Security-Descriptor</span></span> | <span data-ttu-id="592d8-197">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="592d8-197">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="592d8-198">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="592d8-198">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="592d8-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="592d8-199">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="592d8-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="592d8-200">Search-Flags</span></span>           | <span data-ttu-id="592d8-201">0x00000008</span><span class="sxs-lookup"><span data-stu-id="592d8-201">0x00000008</span></span>                      |
| <span data-ttu-id="592d8-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="592d8-202">System-Flags</span></span>           | <span data-ttu-id="592d8-203">0x0000001B</span><span class="sxs-lookup"><span data-stu-id="592d8-203">0x0000001B</span></span>                      |
| <span data-ttu-id="592d8-204">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="592d8-204">Classes used in</span></span>        | [<span data-ttu-id="592d8-205">**In alto**</span><span class="sxs-lookup"><span data-stu-id="592d8-205">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="592d8-206">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="592d8-206">Windows Server 2003 R2</span></span>



| <span data-ttu-id="592d8-207">Voce</span><span class="sxs-lookup"><span data-stu-id="592d8-207">Entry</span></span> | <span data-ttu-id="592d8-208">Valore</span><span class="sxs-lookup"><span data-stu-id="592d8-208">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="592d8-209">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="592d8-209">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="592d8-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="592d8-210">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="592d8-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="592d8-211">System-Only</span></span>            | <span data-ttu-id="592d8-212">Vero</span><span class="sxs-lookup"><span data-stu-id="592d8-212">True</span></span>                            |
| <span data-ttu-id="592d8-213">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="592d8-213">Is-Single-Valued</span></span>       | <span data-ttu-id="592d8-214">Vero</span><span class="sxs-lookup"><span data-stu-id="592d8-214">True</span></span>                            |
| <span data-ttu-id="592d8-215">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="592d8-215">Is Indexed</span></span>             | <span data-ttu-id="592d8-216">Falso</span><span class="sxs-lookup"><span data-stu-id="592d8-216">False</span></span>                           |
| <span data-ttu-id="592d8-217">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="592d8-217">In Global Catalog</span></span>      | <span data-ttu-id="592d8-218">Vero</span><span class="sxs-lookup"><span data-stu-id="592d8-218">True</span></span>                            |
| <span data-ttu-id="592d8-219">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="592d8-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="592d8-220">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="592d8-220">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="592d8-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="592d8-221">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="592d8-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="592d8-222">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="592d8-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="592d8-223">Search-Flags</span></span>           | <span data-ttu-id="592d8-224">0x00000008</span><span class="sxs-lookup"><span data-stu-id="592d8-224">0x00000008</span></span>                      |
| <span data-ttu-id="592d8-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="592d8-225">System-Flags</span></span>           | <span data-ttu-id="592d8-226">0x0000001B</span><span class="sxs-lookup"><span data-stu-id="592d8-226">0x0000001B</span></span>                      |
| <span data-ttu-id="592d8-227">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="592d8-227">Classes used in</span></span>        | [<span data-ttu-id="592d8-228">**In alto**</span><span class="sxs-lookup"><span data-stu-id="592d8-228">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="592d8-229">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="592d8-229">Windows Server 2008</span></span>



| <span data-ttu-id="592d8-230">Voce</span><span class="sxs-lookup"><span data-stu-id="592d8-230">Entry</span></span> | <span data-ttu-id="592d8-231">Valore</span><span class="sxs-lookup"><span data-stu-id="592d8-231">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="592d8-232">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="592d8-232">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="592d8-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="592d8-233">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="592d8-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="592d8-234">System-Only</span></span>            | <span data-ttu-id="592d8-235">Vero</span><span class="sxs-lookup"><span data-stu-id="592d8-235">True</span></span>                            |
| <span data-ttu-id="592d8-236">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="592d8-236">Is-Single-Valued</span></span>       | <span data-ttu-id="592d8-237">Vero</span><span class="sxs-lookup"><span data-stu-id="592d8-237">True</span></span>                            |
| <span data-ttu-id="592d8-238">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="592d8-238">Is Indexed</span></span>             | <span data-ttu-id="592d8-239">Falso</span><span class="sxs-lookup"><span data-stu-id="592d8-239">False</span></span>                           |
| <span data-ttu-id="592d8-240">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="592d8-240">In Global Catalog</span></span>      | <span data-ttu-id="592d8-241">Vero</span><span class="sxs-lookup"><span data-stu-id="592d8-241">True</span></span>                            |
| <span data-ttu-id="592d8-242">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="592d8-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="592d8-243">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="592d8-243">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="592d8-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="592d8-244">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="592d8-245">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="592d8-245">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="592d8-246">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="592d8-246">Search-Flags</span></span>           | <span data-ttu-id="592d8-247">0x00000008</span><span class="sxs-lookup"><span data-stu-id="592d8-247">0x00000008</span></span>                      |
| <span data-ttu-id="592d8-248">System-Flags</span><span class="sxs-lookup"><span data-stu-id="592d8-248">System-Flags</span></span>           | <span data-ttu-id="592d8-249">0x0000001B</span><span class="sxs-lookup"><span data-stu-id="592d8-249">0x0000001B</span></span>                      |
| <span data-ttu-id="592d8-250">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="592d8-250">Classes used in</span></span>        | [<span data-ttu-id="592d8-251">**In alto**</span><span class="sxs-lookup"><span data-stu-id="592d8-251">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="592d8-252">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="592d8-252">Windows Server 2008 R2</span></span>



| <span data-ttu-id="592d8-253">Voce</span><span class="sxs-lookup"><span data-stu-id="592d8-253">Entry</span></span> | <span data-ttu-id="592d8-254">Valore</span><span class="sxs-lookup"><span data-stu-id="592d8-254">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="592d8-255">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="592d8-255">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="592d8-256">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="592d8-256">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="592d8-257">System-Only</span><span class="sxs-lookup"><span data-stu-id="592d8-257">System-Only</span></span>            | <span data-ttu-id="592d8-258">Vero</span><span class="sxs-lookup"><span data-stu-id="592d8-258">True</span></span>                            |
| <span data-ttu-id="592d8-259">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="592d8-259">Is-Single-Valued</span></span>       | <span data-ttu-id="592d8-260">Vero</span><span class="sxs-lookup"><span data-stu-id="592d8-260">True</span></span>                            |
| <span data-ttu-id="592d8-261">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="592d8-261">Is Indexed</span></span>             | <span data-ttu-id="592d8-262">Falso</span><span class="sxs-lookup"><span data-stu-id="592d8-262">False</span></span>                           |
| <span data-ttu-id="592d8-263">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="592d8-263">In Global Catalog</span></span>      | <span data-ttu-id="592d8-264">Vero</span><span class="sxs-lookup"><span data-stu-id="592d8-264">True</span></span>                            |
| <span data-ttu-id="592d8-265">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="592d8-265">NT-Security-Descriptor</span></span> | <span data-ttu-id="592d8-266">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="592d8-266">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="592d8-267">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="592d8-267">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="592d8-268">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="592d8-268">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="592d8-269">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="592d8-269">Search-Flags</span></span>           | <span data-ttu-id="592d8-270">0x00000008</span><span class="sxs-lookup"><span data-stu-id="592d8-270">0x00000008</span></span>                      |
| <span data-ttu-id="592d8-271">System-Flags</span><span class="sxs-lookup"><span data-stu-id="592d8-271">System-Flags</span></span>           | <span data-ttu-id="592d8-272">0x0000001B</span><span class="sxs-lookup"><span data-stu-id="592d8-272">0x0000001B</span></span>                      |
| <span data-ttu-id="592d8-273">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="592d8-273">Classes used in</span></span>        | [<span data-ttu-id="592d8-274">**In alto**</span><span class="sxs-lookup"><span data-stu-id="592d8-274">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="592d8-275">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="592d8-275">Windows Server 2012</span></span>



| <span data-ttu-id="592d8-276">Voce</span><span class="sxs-lookup"><span data-stu-id="592d8-276">Entry</span></span> | <span data-ttu-id="592d8-277">Valore</span><span class="sxs-lookup"><span data-stu-id="592d8-277">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="592d8-278">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="592d8-278">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="592d8-279">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="592d8-279">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="592d8-280">System-Only</span><span class="sxs-lookup"><span data-stu-id="592d8-280">System-Only</span></span>            | <span data-ttu-id="592d8-281">Vero</span><span class="sxs-lookup"><span data-stu-id="592d8-281">True</span></span>                            |
| <span data-ttu-id="592d8-282">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="592d8-282">Is-Single-Valued</span></span>       | <span data-ttu-id="592d8-283">Vero</span><span class="sxs-lookup"><span data-stu-id="592d8-283">True</span></span>                            |
| <span data-ttu-id="592d8-284">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="592d8-284">Is Indexed</span></span>             | <span data-ttu-id="592d8-285">Falso</span><span class="sxs-lookup"><span data-stu-id="592d8-285">False</span></span>                           |
| <span data-ttu-id="592d8-286">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="592d8-286">In Global Catalog</span></span>      | <span data-ttu-id="592d8-287">Vero</span><span class="sxs-lookup"><span data-stu-id="592d8-287">True</span></span>                            |
| <span data-ttu-id="592d8-288">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="592d8-288">NT-Security-Descriptor</span></span> | <span data-ttu-id="592d8-289">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="592d8-289">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="592d8-290">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="592d8-290">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="592d8-291">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="592d8-291">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="592d8-292">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="592d8-292">Search-Flags</span></span>           | <span data-ttu-id="592d8-293">0x00000008</span><span class="sxs-lookup"><span data-stu-id="592d8-293">0x00000008</span></span>                      |
| <span data-ttu-id="592d8-294">System-Flags</span><span class="sxs-lookup"><span data-stu-id="592d8-294">System-Flags</span></span>           | <span data-ttu-id="592d8-295">0x0000001B</span><span class="sxs-lookup"><span data-stu-id="592d8-295">0x0000001B</span></span>                      |
| <span data-ttu-id="592d8-296">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="592d8-296">Classes used in</span></span>        | [<span data-ttu-id="592d8-297">**In alto**</span><span class="sxs-lookup"><span data-stu-id="592d8-297">**Top**</span></span>](c-top.md)<br/> |



 

 





