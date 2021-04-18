---
title: REPL-UpToDate-Vector-attributo
description: Tiene traccia delle informazioni interne sullo stato della replica per un intero NC. Le informazioni possono essere estratte in formato pubblico tramite l'API DsReplicaGetInfo (). Presente in tutti gli oggetti radice NC.
ms.assetid: f23d94f8-c31b-447f-98c3-c35a4f5f1d43
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo REPL-UpToDate-Vector
- Schema AD dell'attributo dell'replUpToDateVector
topic_type:
- apiref
api_name:
- Repl-UpToDate-Vector
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9263111459d01d99cf5990d1c818b5ff2a7a19be
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "106303374"
---
# <a name="repl-uptodate-vector-attribute"></a><span data-ttu-id="1d7bb-107">REPL-UpToDate-Vector-attributo</span><span class="sxs-lookup"><span data-stu-id="1d7bb-107">Repl-UpToDate-Vector attribute</span></span>

<span data-ttu-id="1d7bb-108">Tiene traccia delle informazioni interne sullo stato della replica per un intero NC.</span><span class="sxs-lookup"><span data-stu-id="1d7bb-108">Tracks internal replication state information for an entire NC.</span></span> <span data-ttu-id="1d7bb-109">Le informazioni possono essere estratte in formato pubblico tramite l'API DsReplicaGetInfo ().</span><span class="sxs-lookup"><span data-stu-id="1d7bb-109">Information here can be extracted in public form through the API DsReplicaGetInfo().</span></span> <span data-ttu-id="1d7bb-110">Presente in tutti gli oggetti radice NC.</span><span class="sxs-lookup"><span data-stu-id="1d7bb-110">Present on all NC root objects.</span></span>



| <span data-ttu-id="1d7bb-111">Voce</span><span class="sxs-lookup"><span data-stu-id="1d7bb-111">Entry</span></span> | <span data-ttu-id="1d7bb-112">Valore</span><span class="sxs-lookup"><span data-stu-id="1d7bb-112">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="1d7bb-113">CN</span><span class="sxs-lookup"><span data-stu-id="1d7bb-113">CN</span></span>                | <span data-ttu-id="1d7bb-114">REPL-UpToDate-Vector</span><span class="sxs-lookup"><span data-stu-id="1d7bb-114">Repl-UpToDate-Vector</span></span>                                                           |
| <span data-ttu-id="1d7bb-115">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="1d7bb-115">Ldap-Display-Name</span></span> | <span data-ttu-id="1d7bb-116">Dell'replUpToDateVector</span><span class="sxs-lookup"><span data-stu-id="1d7bb-116">replUpToDateVector</span></span>                                                             |
| <span data-ttu-id="1d7bb-117">Dimensione</span><span class="sxs-lookup"><span data-stu-id="1d7bb-117">Size</span></span>              | <span data-ttu-id="1d7bb-118">La lunghezza è proporzionale al numero di repliche (passate e presenti) del NC.</span><span class="sxs-lookup"><span data-stu-id="1d7bb-118">Length is proportional to the number of replicas (past and present) of the NC.</span></span> |
| <span data-ttu-id="1d7bb-119">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="1d7bb-119">Update Privilege</span></span>  | <span data-ttu-id="1d7bb-120">Questo valore viene impostato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="1d7bb-120">This value is set by the system.</span></span>                                               |
| <span data-ttu-id="1d7bb-121">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="1d7bb-121">Update Frequency</span></span>  | <span data-ttu-id="1d7bb-122">Modifiche della risposta ai cicli di replica in ingresso completati.</span><span class="sxs-lookup"><span data-stu-id="1d7bb-122">Changes in response to completed inbound replication cycles.</span></span>                   |
| <span data-ttu-id="1d7bb-123">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="1d7bb-123">Attribute-Id</span></span>      | <span data-ttu-id="1d7bb-124">1.2.840.113556.1.4.4</span><span class="sxs-lookup"><span data-stu-id="1d7bb-124">1.2.840.113556.1.4.4</span></span>                                                           |
| <span data-ttu-id="1d7bb-125">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="1d7bb-125">System-Id-Guid</span></span>    | <span data-ttu-id="1d7bb-126">bf967a16-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="1d7bb-126">bf967a16-0de6-11d0-a285-00aa003049e2</span></span>                                           |
| <span data-ttu-id="1d7bb-127">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1d7bb-127">Syntax</span></span>            | [<span data-ttu-id="1d7bb-128">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="1d7bb-128">**Object(Replica-Link)**</span></span>](s-object-replica-link.md)                          |



## <a name="implementations"></a><span data-ttu-id="1d7bb-129">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="1d7bb-129">Implementations</span></span>

-   [<span data-ttu-id="1d7bb-130">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="1d7bb-130">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="1d7bb-131">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="1d7bb-131">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="1d7bb-132">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="1d7bb-132">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="1d7bb-133">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="1d7bb-133">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="1d7bb-134">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="1d7bb-134">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="1d7bb-135">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="1d7bb-135">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="1d7bb-136">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="1d7bb-136">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="1d7bb-137">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1d7bb-137">Windows 2000 Server</span></span>



| <span data-ttu-id="1d7bb-138">Voce</span><span class="sxs-lookup"><span data-stu-id="1d7bb-138">Entry</span></span> | <span data-ttu-id="1d7bb-139">Valore</span><span class="sxs-lookup"><span data-stu-id="1d7bb-139">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="1d7bb-140">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="1d7bb-140">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="1d7bb-141">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1d7bb-141">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="1d7bb-142">System-Only</span><span class="sxs-lookup"><span data-stu-id="1d7bb-142">System-Only</span></span>            | <span data-ttu-id="1d7bb-143">Vero</span><span class="sxs-lookup"><span data-stu-id="1d7bb-143">True</span></span>                            |
| <span data-ttu-id="1d7bb-144">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="1d7bb-144">Is-Single-Valued</span></span>       | <span data-ttu-id="1d7bb-145">Vero</span><span class="sxs-lookup"><span data-stu-id="1d7bb-145">True</span></span>                            |
| <span data-ttu-id="1d7bb-146">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="1d7bb-146">Is Indexed</span></span>             | <span data-ttu-id="1d7bb-147">Falso</span><span class="sxs-lookup"><span data-stu-id="1d7bb-147">False</span></span>                           |
| <span data-ttu-id="1d7bb-148">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="1d7bb-148">In Global Catalog</span></span>      | <span data-ttu-id="1d7bb-149">Vero</span><span class="sxs-lookup"><span data-stu-id="1d7bb-149">True</span></span>                            |
| <span data-ttu-id="1d7bb-150">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="1d7bb-150">NT-Security-Descriptor</span></span> | <span data-ttu-id="1d7bb-151">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="1d7bb-151">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="1d7bb-152">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1d7bb-152">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="1d7bb-153">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1d7bb-153">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="1d7bb-154">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1d7bb-154">Search-Flags</span></span>           | <span data-ttu-id="1d7bb-155">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1d7bb-155">0x00000000</span></span>                      |
| <span data-ttu-id="1d7bb-156">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1d7bb-156">System-Flags</span></span>           | <span data-ttu-id="1d7bb-157">0x00000013</span><span class="sxs-lookup"><span data-stu-id="1d7bb-157">0x00000013</span></span>                      |
| <span data-ttu-id="1d7bb-158">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="1d7bb-158">Classes used in</span></span>        | [<span data-ttu-id="1d7bb-159">**In alto**</span><span class="sxs-lookup"><span data-stu-id="1d7bb-159">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="1d7bb-160">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1d7bb-160">Windows Server 2003</span></span>



| <span data-ttu-id="1d7bb-161">Voce</span><span class="sxs-lookup"><span data-stu-id="1d7bb-161">Entry</span></span> | <span data-ttu-id="1d7bb-162">Valore</span><span class="sxs-lookup"><span data-stu-id="1d7bb-162">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="1d7bb-163">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="1d7bb-163">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="1d7bb-164">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1d7bb-164">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="1d7bb-165">System-Only</span><span class="sxs-lookup"><span data-stu-id="1d7bb-165">System-Only</span></span>            | <span data-ttu-id="1d7bb-166">Vero</span><span class="sxs-lookup"><span data-stu-id="1d7bb-166">True</span></span>                            |
| <span data-ttu-id="1d7bb-167">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="1d7bb-167">Is-Single-Valued</span></span>       | <span data-ttu-id="1d7bb-168">Vero</span><span class="sxs-lookup"><span data-stu-id="1d7bb-168">True</span></span>                            |
| <span data-ttu-id="1d7bb-169">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="1d7bb-169">Is Indexed</span></span>             | <span data-ttu-id="1d7bb-170">Falso</span><span class="sxs-lookup"><span data-stu-id="1d7bb-170">False</span></span>                           |
| <span data-ttu-id="1d7bb-171">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="1d7bb-171">In Global Catalog</span></span>      | <span data-ttu-id="1d7bb-172">Vero</span><span class="sxs-lookup"><span data-stu-id="1d7bb-172">True</span></span>                            |
| <span data-ttu-id="1d7bb-173">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="1d7bb-173">NT-Security-Descriptor</span></span> | <span data-ttu-id="1d7bb-174">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="1d7bb-174">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="1d7bb-175">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1d7bb-175">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="1d7bb-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1d7bb-176">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="1d7bb-177">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1d7bb-177">Search-Flags</span></span>           | <span data-ttu-id="1d7bb-178">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1d7bb-178">0x00000000</span></span>                      |
| <span data-ttu-id="1d7bb-179">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1d7bb-179">System-Flags</span></span>           | <span data-ttu-id="1d7bb-180">0x00000013</span><span class="sxs-lookup"><span data-stu-id="1d7bb-180">0x00000013</span></span>                      |
| <span data-ttu-id="1d7bb-181">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="1d7bb-181">Classes used in</span></span>        | [<span data-ttu-id="1d7bb-182">**In alto**</span><span class="sxs-lookup"><span data-stu-id="1d7bb-182">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="1d7bb-183">ADAM</span><span class="sxs-lookup"><span data-stu-id="1d7bb-183">ADAM</span></span>



| <span data-ttu-id="1d7bb-184">Voce</span><span class="sxs-lookup"><span data-stu-id="1d7bb-184">Entry</span></span> | <span data-ttu-id="1d7bb-185">Valore</span><span class="sxs-lookup"><span data-stu-id="1d7bb-185">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="1d7bb-186">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="1d7bb-186">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="1d7bb-187">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1d7bb-187">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="1d7bb-188">System-Only</span><span class="sxs-lookup"><span data-stu-id="1d7bb-188">System-Only</span></span>            | <span data-ttu-id="1d7bb-189">Vero</span><span class="sxs-lookup"><span data-stu-id="1d7bb-189">True</span></span>                            |
| <span data-ttu-id="1d7bb-190">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="1d7bb-190">Is-Single-Valued</span></span>       | <span data-ttu-id="1d7bb-191">Vero</span><span class="sxs-lookup"><span data-stu-id="1d7bb-191">True</span></span>                            |
| <span data-ttu-id="1d7bb-192">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="1d7bb-192">Is Indexed</span></span>             | <span data-ttu-id="1d7bb-193">Falso</span><span class="sxs-lookup"><span data-stu-id="1d7bb-193">False</span></span>                           |
| <span data-ttu-id="1d7bb-194">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="1d7bb-194">In Global Catalog</span></span>      | <span data-ttu-id="1d7bb-195">Vero</span><span class="sxs-lookup"><span data-stu-id="1d7bb-195">True</span></span>                            |
| <span data-ttu-id="1d7bb-196">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="1d7bb-196">NT-Security-Descriptor</span></span> | <span data-ttu-id="1d7bb-197">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="1d7bb-197">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="1d7bb-198">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1d7bb-198">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="1d7bb-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1d7bb-199">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="1d7bb-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1d7bb-200">Search-Flags</span></span>           | <span data-ttu-id="1d7bb-201">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1d7bb-201">0x00000000</span></span>                      |
| <span data-ttu-id="1d7bb-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1d7bb-202">System-Flags</span></span>           | <span data-ttu-id="1d7bb-203">0x00000013</span><span class="sxs-lookup"><span data-stu-id="1d7bb-203">0x00000013</span></span>                      |
| <span data-ttu-id="1d7bb-204">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="1d7bb-204">Classes used in</span></span>        | [<span data-ttu-id="1d7bb-205">**In alto**</span><span class="sxs-lookup"><span data-stu-id="1d7bb-205">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="1d7bb-206">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="1d7bb-206">Windows Server 2003 R2</span></span>



| <span data-ttu-id="1d7bb-207">Voce</span><span class="sxs-lookup"><span data-stu-id="1d7bb-207">Entry</span></span> | <span data-ttu-id="1d7bb-208">Valore</span><span class="sxs-lookup"><span data-stu-id="1d7bb-208">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="1d7bb-209">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="1d7bb-209">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="1d7bb-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1d7bb-210">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="1d7bb-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="1d7bb-211">System-Only</span></span>            | <span data-ttu-id="1d7bb-212">Vero</span><span class="sxs-lookup"><span data-stu-id="1d7bb-212">True</span></span>                            |
| <span data-ttu-id="1d7bb-213">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="1d7bb-213">Is-Single-Valued</span></span>       | <span data-ttu-id="1d7bb-214">Vero</span><span class="sxs-lookup"><span data-stu-id="1d7bb-214">True</span></span>                            |
| <span data-ttu-id="1d7bb-215">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="1d7bb-215">Is Indexed</span></span>             | <span data-ttu-id="1d7bb-216">Falso</span><span class="sxs-lookup"><span data-stu-id="1d7bb-216">False</span></span>                           |
| <span data-ttu-id="1d7bb-217">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="1d7bb-217">In Global Catalog</span></span>      | <span data-ttu-id="1d7bb-218">Vero</span><span class="sxs-lookup"><span data-stu-id="1d7bb-218">True</span></span>                            |
| <span data-ttu-id="1d7bb-219">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="1d7bb-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="1d7bb-220">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="1d7bb-220">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="1d7bb-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1d7bb-221">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="1d7bb-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1d7bb-222">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="1d7bb-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1d7bb-223">Search-Flags</span></span>           | <span data-ttu-id="1d7bb-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1d7bb-224">0x00000000</span></span>                      |
| <span data-ttu-id="1d7bb-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1d7bb-225">System-Flags</span></span>           | <span data-ttu-id="1d7bb-226">0x00000013</span><span class="sxs-lookup"><span data-stu-id="1d7bb-226">0x00000013</span></span>                      |
| <span data-ttu-id="1d7bb-227">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="1d7bb-227">Classes used in</span></span>        | [<span data-ttu-id="1d7bb-228">**In alto**</span><span class="sxs-lookup"><span data-stu-id="1d7bb-228">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="1d7bb-229">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1d7bb-229">Windows Server 2008</span></span>



| <span data-ttu-id="1d7bb-230">Voce</span><span class="sxs-lookup"><span data-stu-id="1d7bb-230">Entry</span></span> | <span data-ttu-id="1d7bb-231">Valore</span><span class="sxs-lookup"><span data-stu-id="1d7bb-231">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="1d7bb-232">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="1d7bb-232">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="1d7bb-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1d7bb-233">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="1d7bb-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="1d7bb-234">System-Only</span></span>            | <span data-ttu-id="1d7bb-235">Vero</span><span class="sxs-lookup"><span data-stu-id="1d7bb-235">True</span></span>                            |
| <span data-ttu-id="1d7bb-236">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="1d7bb-236">Is-Single-Valued</span></span>       | <span data-ttu-id="1d7bb-237">Vero</span><span class="sxs-lookup"><span data-stu-id="1d7bb-237">True</span></span>                            |
| <span data-ttu-id="1d7bb-238">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="1d7bb-238">Is Indexed</span></span>             | <span data-ttu-id="1d7bb-239">Falso</span><span class="sxs-lookup"><span data-stu-id="1d7bb-239">False</span></span>                           |
| <span data-ttu-id="1d7bb-240">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="1d7bb-240">In Global Catalog</span></span>      | <span data-ttu-id="1d7bb-241">Vero</span><span class="sxs-lookup"><span data-stu-id="1d7bb-241">True</span></span>                            |
| <span data-ttu-id="1d7bb-242">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="1d7bb-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="1d7bb-243">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="1d7bb-243">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="1d7bb-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1d7bb-244">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="1d7bb-245">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1d7bb-245">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="1d7bb-246">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1d7bb-246">Search-Flags</span></span>           | <span data-ttu-id="1d7bb-247">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1d7bb-247">0x00000000</span></span>                      |
| <span data-ttu-id="1d7bb-248">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1d7bb-248">System-Flags</span></span>           | <span data-ttu-id="1d7bb-249">0x00000013</span><span class="sxs-lookup"><span data-stu-id="1d7bb-249">0x00000013</span></span>                      |
| <span data-ttu-id="1d7bb-250">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="1d7bb-250">Classes used in</span></span>        | [<span data-ttu-id="1d7bb-251">**In alto**</span><span class="sxs-lookup"><span data-stu-id="1d7bb-251">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="1d7bb-252">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1d7bb-252">Windows Server 2008 R2</span></span>



| <span data-ttu-id="1d7bb-253">Voce</span><span class="sxs-lookup"><span data-stu-id="1d7bb-253">Entry</span></span> | <span data-ttu-id="1d7bb-254">Valore</span><span class="sxs-lookup"><span data-stu-id="1d7bb-254">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="1d7bb-255">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="1d7bb-255">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="1d7bb-256">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1d7bb-256">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="1d7bb-257">System-Only</span><span class="sxs-lookup"><span data-stu-id="1d7bb-257">System-Only</span></span>            | <span data-ttu-id="1d7bb-258">Vero</span><span class="sxs-lookup"><span data-stu-id="1d7bb-258">True</span></span>                            |
| <span data-ttu-id="1d7bb-259">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="1d7bb-259">Is-Single-Valued</span></span>       | <span data-ttu-id="1d7bb-260">Vero</span><span class="sxs-lookup"><span data-stu-id="1d7bb-260">True</span></span>                            |
| <span data-ttu-id="1d7bb-261">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="1d7bb-261">Is Indexed</span></span>             | <span data-ttu-id="1d7bb-262">Falso</span><span class="sxs-lookup"><span data-stu-id="1d7bb-262">False</span></span>                           |
| <span data-ttu-id="1d7bb-263">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="1d7bb-263">In Global Catalog</span></span>      | <span data-ttu-id="1d7bb-264">Vero</span><span class="sxs-lookup"><span data-stu-id="1d7bb-264">True</span></span>                            |
| <span data-ttu-id="1d7bb-265">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="1d7bb-265">NT-Security-Descriptor</span></span> | <span data-ttu-id="1d7bb-266">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="1d7bb-266">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="1d7bb-267">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1d7bb-267">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="1d7bb-268">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1d7bb-268">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="1d7bb-269">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1d7bb-269">Search-Flags</span></span>           | <span data-ttu-id="1d7bb-270">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1d7bb-270">0x00000000</span></span>                      |
| <span data-ttu-id="1d7bb-271">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1d7bb-271">System-Flags</span></span>           | <span data-ttu-id="1d7bb-272">0x00000013</span><span class="sxs-lookup"><span data-stu-id="1d7bb-272">0x00000013</span></span>                      |
| <span data-ttu-id="1d7bb-273">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="1d7bb-273">Classes used in</span></span>        | [<span data-ttu-id="1d7bb-274">**In alto**</span><span class="sxs-lookup"><span data-stu-id="1d7bb-274">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="1d7bb-275">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1d7bb-275">Windows Server 2012</span></span>



| <span data-ttu-id="1d7bb-276">Voce</span><span class="sxs-lookup"><span data-stu-id="1d7bb-276">Entry</span></span> | <span data-ttu-id="1d7bb-277">Valore</span><span class="sxs-lookup"><span data-stu-id="1d7bb-277">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="1d7bb-278">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="1d7bb-278">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="1d7bb-279">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1d7bb-279">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="1d7bb-280">System-Only</span><span class="sxs-lookup"><span data-stu-id="1d7bb-280">System-Only</span></span>            | <span data-ttu-id="1d7bb-281">Vero</span><span class="sxs-lookup"><span data-stu-id="1d7bb-281">True</span></span>                            |
| <span data-ttu-id="1d7bb-282">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="1d7bb-282">Is-Single-Valued</span></span>       | <span data-ttu-id="1d7bb-283">Vero</span><span class="sxs-lookup"><span data-stu-id="1d7bb-283">True</span></span>                            |
| <span data-ttu-id="1d7bb-284">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="1d7bb-284">Is Indexed</span></span>             | <span data-ttu-id="1d7bb-285">Falso</span><span class="sxs-lookup"><span data-stu-id="1d7bb-285">False</span></span>                           |
| <span data-ttu-id="1d7bb-286">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="1d7bb-286">In Global Catalog</span></span>      | <span data-ttu-id="1d7bb-287">Vero</span><span class="sxs-lookup"><span data-stu-id="1d7bb-287">True</span></span>                            |
| <span data-ttu-id="1d7bb-288">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="1d7bb-288">NT-Security-Descriptor</span></span> | <span data-ttu-id="1d7bb-289">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="1d7bb-289">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="1d7bb-290">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1d7bb-290">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="1d7bb-291">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1d7bb-291">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="1d7bb-292">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1d7bb-292">Search-Flags</span></span>           | <span data-ttu-id="1d7bb-293">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1d7bb-293">0x00000000</span></span>                      |
| <span data-ttu-id="1d7bb-294">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1d7bb-294">System-Flags</span></span>           | <span data-ttu-id="1d7bb-295">0x00000013</span><span class="sxs-lookup"><span data-stu-id="1d7bb-295">0x00000013</span></span>                      |
| <span data-ttu-id="1d7bb-296">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="1d7bb-296">Classes used in</span></span>        | [<span data-ttu-id="1d7bb-297">**In alto**</span><span class="sxs-lookup"><span data-stu-id="1d7bb-297">**Top**</span></span>](c-top.md)<br/> |



 

 





