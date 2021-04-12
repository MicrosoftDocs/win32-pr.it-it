---
title: MS-DS-replicates-NC-Reason (attributo)
description: Attributo dell'oggetto ntdsConnection che indica perché, o se il KCC Mostra che la connessione è utile nella topologia di replica. È a più valori e ha la sintassi binaria DistName +, dove la parte binaria è un bit di dimensioni int.
ms.assetid: ba66e346-d288-4c0b-b41e-599c3f8e8405
ms.tgt_platform: multiple
keywords:
- MS-DS-replicas-schema AD dell'attributo NC-Reason
- Schema AD dell'attributo mS-DS-ReplicatesNCReason
topic_type:
- apiref
api_name:
- MS-DS-Replicates-NC-Reason
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a45c587ef82773b5e7fd310e8e8591f18ad27ab
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104400964"
---
# <a name="ms-ds-replicates-nc-reason-attribute"></a><span data-ttu-id="f87ad-106">MS-DS-replicates-NC-Reason (attributo)</span><span class="sxs-lookup"><span data-stu-id="f87ad-106">MS-DS-Replicates-NC-Reason attribute</span></span>

<span data-ttu-id="f87ad-107">Attributo dell'oggetto ntdsConnection che indica perché, o se il KCC Mostra che la connessione è utile nella topologia di replica.</span><span class="sxs-lookup"><span data-stu-id="f87ad-107">Attribute of ntdsConnection object that indicates why (or whether) the KCC shows the connection is useful in the replication topology.</span></span> <span data-ttu-id="f87ad-108">È a più valori e ha la sintassi binaria DistName +, dove la parte binaria è un bit di dimensioni int.</span><span class="sxs-lookup"><span data-stu-id="f87ad-108">Is multiple-valued and has DistName+Binary syntax, where the binary part is an int-size bitfield.</span></span>



| <span data-ttu-id="f87ad-109">Voce</span><span class="sxs-lookup"><span data-stu-id="f87ad-109">Entry</span></span> | <span data-ttu-id="f87ad-110">Valore</span><span class="sxs-lookup"><span data-stu-id="f87ad-110">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f87ad-111">CN</span><span class="sxs-lookup"><span data-stu-id="f87ad-111">CN</span></span>                | <span data-ttu-id="f87ad-112">MS-DS-replicas-NC-Reason</span><span class="sxs-lookup"><span data-stu-id="f87ad-112">MS-DS-Replicates-NC-Reason</span></span>                                                                                                                 |
| <span data-ttu-id="f87ad-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="f87ad-113">Ldap-Display-Name</span></span> | <span data-ttu-id="f87ad-114">mS-DS-ReplicatesNCReason</span><span class="sxs-lookup"><span data-stu-id="f87ad-114">mS-DS-ReplicatesNCReason</span></span>                                                                                                                   |
| <span data-ttu-id="f87ad-115">Dimensione</span><span class="sxs-lookup"><span data-stu-id="f87ad-115">Size</span></span>              | <span data-ttu-id="f87ad-116">Valore per la parte binaria: 0 = nessun \_ motivo, 1 = \_ topologia GC, 2 = \_ topologia ad anello, 4 = riduzione della \_ topologia degli hop \_ , 8 = \_ topologia di server non aggiornati \_ .</span><span class="sxs-lookup"><span data-stu-id="f87ad-116">Value for binary portion: 0 = NO\_REASON,1 = GC\_TOPOLOGY, 2 = RING\_TOPOLOGY, 4 = MINIMIZE\_HOPS\_TOPOLOGY, 8 = STALE\_SERVERS\_TOPOLOGY.</span></span> |
| <span data-ttu-id="f87ad-117">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="f87ad-117">Update Privilege</span></span>  | <span data-ttu-id="f87ad-118">Questo valore viene impostato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="f87ad-118">This value is set by the system.</span></span>                                                                                                           |
| <span data-ttu-id="f87ad-119">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="f87ad-119">Update Frequency</span></span>  | <span data-ttu-id="f87ad-120">Può cambiare in risposta alle modifiche nella topologia di rete.</span><span class="sxs-lookup"><span data-stu-id="f87ad-120">Can change in response to changes in the network topology.</span></span>                                                                                 |
| <span data-ttu-id="f87ad-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f87ad-121">Attribute-Id</span></span>      | <span data-ttu-id="f87ad-122">1.2.840.113556.1.4.1408</span><span class="sxs-lookup"><span data-stu-id="f87ad-122">1.2.840.113556.1.4.1408</span></span>                                                                                                                    |
| <span data-ttu-id="f87ad-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="f87ad-123">System-Id-Guid</span></span>    | <span data-ttu-id="f87ad-124">0ea12b84-08b3-11d3-91bc-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="f87ad-124">0ea12b84-08b3-11d3-91bc-0000f87a57d4</span></span>                                                                                                       |
| <span data-ttu-id="f87ad-125">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f87ad-125">Syntax</span></span>            | [<span data-ttu-id="f87ad-126">**Object(DN-Binary)**</span><span class="sxs-lookup"><span data-stu-id="f87ad-126">**Object(DN-Binary)**</span></span>](s-object-dn-binary.md)                                                                                            |



## <a name="implementations"></a><span data-ttu-id="f87ad-127">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="f87ad-127">Implementations</span></span>

-   [<span data-ttu-id="f87ad-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="f87ad-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="f87ad-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f87ad-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f87ad-130">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="f87ad-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="f87ad-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f87ad-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f87ad-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f87ad-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f87ad-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f87ad-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f87ad-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f87ad-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="f87ad-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f87ad-135">Windows 2000 Server</span></span>



| <span data-ttu-id="f87ad-136">Voce</span><span class="sxs-lookup"><span data-stu-id="f87ad-136">Entry</span></span> | <span data-ttu-id="f87ad-137">Valore</span><span class="sxs-lookup"><span data-stu-id="f87ad-137">Value</span></span> |
|------------------------|--------------------------------------------------------|
| <span data-ttu-id="f87ad-138">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="f87ad-138">Link-Id</span></span>                | \-                                                     |
| <span data-ttu-id="f87ad-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f87ad-139">MAPI-Id</span></span>                | \-                                                     |
| <span data-ttu-id="f87ad-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="f87ad-140">System-Only</span></span>            | <span data-ttu-id="f87ad-141">Falso</span><span class="sxs-lookup"><span data-stu-id="f87ad-141">False</span></span>                                                  |
| <span data-ttu-id="f87ad-142">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="f87ad-142">Is-Single-Valued</span></span>       | <span data-ttu-id="f87ad-143">Falso</span><span class="sxs-lookup"><span data-stu-id="f87ad-143">False</span></span>                                                  |
| <span data-ttu-id="f87ad-144">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="f87ad-144">Is Indexed</span></span>             | <span data-ttu-id="f87ad-145">Falso</span><span class="sxs-lookup"><span data-stu-id="f87ad-145">False</span></span>                                                  |
| <span data-ttu-id="f87ad-146">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="f87ad-146">In Global Catalog</span></span>      | <span data-ttu-id="f87ad-147">Falso</span><span class="sxs-lookup"><span data-stu-id="f87ad-147">False</span></span>                                                  |
| <span data-ttu-id="f87ad-148">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="f87ad-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="f87ad-149">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="f87ad-149">O:BAG:BAD:S:</span></span>                                           |
| <span data-ttu-id="f87ad-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f87ad-150">Range-Lower</span></span>            | \-                                                     |
| <span data-ttu-id="f87ad-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f87ad-151">Range-Upper</span></span>            | \-                                                     |
| <span data-ttu-id="f87ad-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f87ad-152">Search-Flags</span></span>           | <span data-ttu-id="f87ad-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f87ad-153">0x00000000</span></span>                                             |
| <span data-ttu-id="f87ad-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f87ad-154">System-Flags</span></span>           | <span data-ttu-id="f87ad-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f87ad-155">0x00000010</span></span>                                             |
| <span data-ttu-id="f87ad-156">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="f87ad-156">Classes used in</span></span>        | [<span data-ttu-id="f87ad-157">**NTDS-connessione**</span><span class="sxs-lookup"><span data-stu-id="f87ad-157">**NTDS-Connection**</span></span>](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="f87ad-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f87ad-158">Windows Server 2003</span></span>



| <span data-ttu-id="f87ad-159">Voce</span><span class="sxs-lookup"><span data-stu-id="f87ad-159">Entry</span></span> | <span data-ttu-id="f87ad-160">Valore</span><span class="sxs-lookup"><span data-stu-id="f87ad-160">Value</span></span> |
|------------------------|--------------------------------------------------------|
| <span data-ttu-id="f87ad-161">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="f87ad-161">Link-Id</span></span>                | \-                                                     |
| <span data-ttu-id="f87ad-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f87ad-162">MAPI-Id</span></span>                | \-                                                     |
| <span data-ttu-id="f87ad-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="f87ad-163">System-Only</span></span>            | <span data-ttu-id="f87ad-164">Falso</span><span class="sxs-lookup"><span data-stu-id="f87ad-164">False</span></span>                                                  |
| <span data-ttu-id="f87ad-165">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="f87ad-165">Is-Single-Valued</span></span>       | <span data-ttu-id="f87ad-166">Falso</span><span class="sxs-lookup"><span data-stu-id="f87ad-166">False</span></span>                                                  |
| <span data-ttu-id="f87ad-167">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="f87ad-167">Is Indexed</span></span>             | <span data-ttu-id="f87ad-168">Falso</span><span class="sxs-lookup"><span data-stu-id="f87ad-168">False</span></span>                                                  |
| <span data-ttu-id="f87ad-169">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="f87ad-169">In Global Catalog</span></span>      | <span data-ttu-id="f87ad-170">Falso</span><span class="sxs-lookup"><span data-stu-id="f87ad-170">False</span></span>                                                  |
| <span data-ttu-id="f87ad-171">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="f87ad-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="f87ad-172">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="f87ad-172">O:BAG:BAD:S:</span></span>                                           |
| <span data-ttu-id="f87ad-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f87ad-173">Range-Lower</span></span>            | \-                                                     |
| <span data-ttu-id="f87ad-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f87ad-174">Range-Upper</span></span>            | \-                                                     |
| <span data-ttu-id="f87ad-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f87ad-175">Search-Flags</span></span>           | <span data-ttu-id="f87ad-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f87ad-176">0x00000000</span></span>                                             |
| <span data-ttu-id="f87ad-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f87ad-177">System-Flags</span></span>           | <span data-ttu-id="f87ad-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f87ad-178">0x00000010</span></span>                                             |
| <span data-ttu-id="f87ad-179">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="f87ad-179">Classes used in</span></span>        | [<span data-ttu-id="f87ad-180">**NTDS-connessione**</span><span class="sxs-lookup"><span data-stu-id="f87ad-180">**NTDS-Connection**</span></span>](c-ntdsconnection.md)<br/> |



## <a name="adam"></a><span data-ttu-id="f87ad-181">ADAM</span><span class="sxs-lookup"><span data-stu-id="f87ad-181">ADAM</span></span>



| <span data-ttu-id="f87ad-182">Voce</span><span class="sxs-lookup"><span data-stu-id="f87ad-182">Entry</span></span> | <span data-ttu-id="f87ad-183">Valore</span><span class="sxs-lookup"><span data-stu-id="f87ad-183">Value</span></span> |
|------------------------|--------------------------------------------------------|
| <span data-ttu-id="f87ad-184">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="f87ad-184">Link-Id</span></span>                | \-                                                     |
| <span data-ttu-id="f87ad-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f87ad-185">MAPI-Id</span></span>                | \-                                                     |
| <span data-ttu-id="f87ad-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="f87ad-186">System-Only</span></span>            | <span data-ttu-id="f87ad-187">Falso</span><span class="sxs-lookup"><span data-stu-id="f87ad-187">False</span></span>                                                  |
| <span data-ttu-id="f87ad-188">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="f87ad-188">Is-Single-Valued</span></span>       | <span data-ttu-id="f87ad-189">Falso</span><span class="sxs-lookup"><span data-stu-id="f87ad-189">False</span></span>                                                  |
| <span data-ttu-id="f87ad-190">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="f87ad-190">Is Indexed</span></span>             | <span data-ttu-id="f87ad-191">Falso</span><span class="sxs-lookup"><span data-stu-id="f87ad-191">False</span></span>                                                  |
| <span data-ttu-id="f87ad-192">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="f87ad-192">In Global Catalog</span></span>      | <span data-ttu-id="f87ad-193">Falso</span><span class="sxs-lookup"><span data-stu-id="f87ad-193">False</span></span>                                                  |
| <span data-ttu-id="f87ad-194">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="f87ad-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="f87ad-195">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="f87ad-195">O:BAG:BAD:S:</span></span>                                           |
| <span data-ttu-id="f87ad-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f87ad-196">Range-Lower</span></span>            | \-                                                     |
| <span data-ttu-id="f87ad-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f87ad-197">Range-Upper</span></span>            | \-                                                     |
| <span data-ttu-id="f87ad-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f87ad-198">Search-Flags</span></span>           | <span data-ttu-id="f87ad-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f87ad-199">0x00000000</span></span>                                             |
| <span data-ttu-id="f87ad-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f87ad-200">System-Flags</span></span>           | <span data-ttu-id="f87ad-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f87ad-201">0x00000010</span></span>                                             |
| <span data-ttu-id="f87ad-202">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="f87ad-202">Classes used in</span></span>        | [<span data-ttu-id="f87ad-203">**NTDS-connessione**</span><span class="sxs-lookup"><span data-stu-id="f87ad-203">**NTDS-Connection**</span></span>](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f87ad-204">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f87ad-204">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f87ad-205">Voce</span><span class="sxs-lookup"><span data-stu-id="f87ad-205">Entry</span></span> | <span data-ttu-id="f87ad-206">Valore</span><span class="sxs-lookup"><span data-stu-id="f87ad-206">Value</span></span> |
|------------------------|--------------------------------------------------------|
| <span data-ttu-id="f87ad-207">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="f87ad-207">Link-Id</span></span>                | \-                                                     |
| <span data-ttu-id="f87ad-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f87ad-208">MAPI-Id</span></span>                | \-                                                     |
| <span data-ttu-id="f87ad-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="f87ad-209">System-Only</span></span>            | <span data-ttu-id="f87ad-210">Falso</span><span class="sxs-lookup"><span data-stu-id="f87ad-210">False</span></span>                                                  |
| <span data-ttu-id="f87ad-211">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="f87ad-211">Is-Single-Valued</span></span>       | <span data-ttu-id="f87ad-212">Falso</span><span class="sxs-lookup"><span data-stu-id="f87ad-212">False</span></span>                                                  |
| <span data-ttu-id="f87ad-213">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="f87ad-213">Is Indexed</span></span>             | <span data-ttu-id="f87ad-214">Falso</span><span class="sxs-lookup"><span data-stu-id="f87ad-214">False</span></span>                                                  |
| <span data-ttu-id="f87ad-215">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="f87ad-215">In Global Catalog</span></span>      | <span data-ttu-id="f87ad-216">Falso</span><span class="sxs-lookup"><span data-stu-id="f87ad-216">False</span></span>                                                  |
| <span data-ttu-id="f87ad-217">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="f87ad-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="f87ad-218">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="f87ad-218">O:BAG:BAD:S:</span></span>                                           |
| <span data-ttu-id="f87ad-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f87ad-219">Range-Lower</span></span>            | \-                                                     |
| <span data-ttu-id="f87ad-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f87ad-220">Range-Upper</span></span>            | \-                                                     |
| <span data-ttu-id="f87ad-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f87ad-221">Search-Flags</span></span>           | <span data-ttu-id="f87ad-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f87ad-222">0x00000000</span></span>                                             |
| <span data-ttu-id="f87ad-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f87ad-223">System-Flags</span></span>           | <span data-ttu-id="f87ad-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f87ad-224">0x00000010</span></span>                                             |
| <span data-ttu-id="f87ad-225">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="f87ad-225">Classes used in</span></span>        | [<span data-ttu-id="f87ad-226">**NTDS-connessione**</span><span class="sxs-lookup"><span data-stu-id="f87ad-226">**NTDS-Connection**</span></span>](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f87ad-227">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f87ad-227">Windows Server 2008</span></span>



| <span data-ttu-id="f87ad-228">Voce</span><span class="sxs-lookup"><span data-stu-id="f87ad-228">Entry</span></span> | <span data-ttu-id="f87ad-229">Valore</span><span class="sxs-lookup"><span data-stu-id="f87ad-229">Value</span></span> |
|------------------------|--------------------------------------------------------|
| <span data-ttu-id="f87ad-230">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="f87ad-230">Link-Id</span></span>                | \-                                                     |
| <span data-ttu-id="f87ad-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f87ad-231">MAPI-Id</span></span>                | \-                                                     |
| <span data-ttu-id="f87ad-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="f87ad-232">System-Only</span></span>            | <span data-ttu-id="f87ad-233">Falso</span><span class="sxs-lookup"><span data-stu-id="f87ad-233">False</span></span>                                                  |
| <span data-ttu-id="f87ad-234">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="f87ad-234">Is-Single-Valued</span></span>       | <span data-ttu-id="f87ad-235">Falso</span><span class="sxs-lookup"><span data-stu-id="f87ad-235">False</span></span>                                                  |
| <span data-ttu-id="f87ad-236">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="f87ad-236">Is Indexed</span></span>             | <span data-ttu-id="f87ad-237">Falso</span><span class="sxs-lookup"><span data-stu-id="f87ad-237">False</span></span>                                                  |
| <span data-ttu-id="f87ad-238">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="f87ad-238">In Global Catalog</span></span>      | <span data-ttu-id="f87ad-239">Falso</span><span class="sxs-lookup"><span data-stu-id="f87ad-239">False</span></span>                                                  |
| <span data-ttu-id="f87ad-240">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="f87ad-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="f87ad-241">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="f87ad-241">O:BAG:BAD:S:</span></span>                                           |
| <span data-ttu-id="f87ad-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f87ad-242">Range-Lower</span></span>            | \-                                                     |
| <span data-ttu-id="f87ad-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f87ad-243">Range-Upper</span></span>            | \-                                                     |
| <span data-ttu-id="f87ad-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f87ad-244">Search-Flags</span></span>           | <span data-ttu-id="f87ad-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f87ad-245">0x00000000</span></span>                                             |
| <span data-ttu-id="f87ad-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f87ad-246">System-Flags</span></span>           | <span data-ttu-id="f87ad-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f87ad-247">0x00000010</span></span>                                             |
| <span data-ttu-id="f87ad-248">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="f87ad-248">Classes used in</span></span>        | [<span data-ttu-id="f87ad-249">**NTDS-connessione**</span><span class="sxs-lookup"><span data-stu-id="f87ad-249">**NTDS-Connection**</span></span>](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f87ad-250">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f87ad-250">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f87ad-251">Voce</span><span class="sxs-lookup"><span data-stu-id="f87ad-251">Entry</span></span> | <span data-ttu-id="f87ad-252">Valore</span><span class="sxs-lookup"><span data-stu-id="f87ad-252">Value</span></span> |
|------------------------|--------------------------------------------------------|
| <span data-ttu-id="f87ad-253">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="f87ad-253">Link-Id</span></span>                | \-                                                     |
| <span data-ttu-id="f87ad-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f87ad-254">MAPI-Id</span></span>                | \-                                                     |
| <span data-ttu-id="f87ad-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="f87ad-255">System-Only</span></span>            | <span data-ttu-id="f87ad-256">Falso</span><span class="sxs-lookup"><span data-stu-id="f87ad-256">False</span></span>                                                  |
| <span data-ttu-id="f87ad-257">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="f87ad-257">Is-Single-Valued</span></span>       | <span data-ttu-id="f87ad-258">Falso</span><span class="sxs-lookup"><span data-stu-id="f87ad-258">False</span></span>                                                  |
| <span data-ttu-id="f87ad-259">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="f87ad-259">Is Indexed</span></span>             | <span data-ttu-id="f87ad-260">Falso</span><span class="sxs-lookup"><span data-stu-id="f87ad-260">False</span></span>                                                  |
| <span data-ttu-id="f87ad-261">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="f87ad-261">In Global Catalog</span></span>      | <span data-ttu-id="f87ad-262">Falso</span><span class="sxs-lookup"><span data-stu-id="f87ad-262">False</span></span>                                                  |
| <span data-ttu-id="f87ad-263">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="f87ad-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="f87ad-264">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="f87ad-264">O:BAG:BAD:S:</span></span>                                           |
| <span data-ttu-id="f87ad-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f87ad-265">Range-Lower</span></span>            | \-                                                     |
| <span data-ttu-id="f87ad-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f87ad-266">Range-Upper</span></span>            | \-                                                     |
| <span data-ttu-id="f87ad-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f87ad-267">Search-Flags</span></span>           | <span data-ttu-id="f87ad-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f87ad-268">0x00000000</span></span>                                             |
| <span data-ttu-id="f87ad-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f87ad-269">System-Flags</span></span>           | <span data-ttu-id="f87ad-270">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f87ad-270">0x00000010</span></span>                                             |
| <span data-ttu-id="f87ad-271">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="f87ad-271">Classes used in</span></span>        | [<span data-ttu-id="f87ad-272">**NTDS-connessione**</span><span class="sxs-lookup"><span data-stu-id="f87ad-272">**NTDS-Connection**</span></span>](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f87ad-273">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f87ad-273">Windows Server 2012</span></span>



| <span data-ttu-id="f87ad-274">Voce</span><span class="sxs-lookup"><span data-stu-id="f87ad-274">Entry</span></span> | <span data-ttu-id="f87ad-275">Valore</span><span class="sxs-lookup"><span data-stu-id="f87ad-275">Value</span></span> |
|------------------------|--------------------------------------------------------|
| <span data-ttu-id="f87ad-276">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="f87ad-276">Link-Id</span></span>                | \-                                                     |
| <span data-ttu-id="f87ad-277">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f87ad-277">MAPI-Id</span></span>                | \-                                                     |
| <span data-ttu-id="f87ad-278">System-Only</span><span class="sxs-lookup"><span data-stu-id="f87ad-278">System-Only</span></span>            | <span data-ttu-id="f87ad-279">Falso</span><span class="sxs-lookup"><span data-stu-id="f87ad-279">False</span></span>                                                  |
| <span data-ttu-id="f87ad-280">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="f87ad-280">Is-Single-Valued</span></span>       | <span data-ttu-id="f87ad-281">Falso</span><span class="sxs-lookup"><span data-stu-id="f87ad-281">False</span></span>                                                  |
| <span data-ttu-id="f87ad-282">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="f87ad-282">Is Indexed</span></span>             | <span data-ttu-id="f87ad-283">Falso</span><span class="sxs-lookup"><span data-stu-id="f87ad-283">False</span></span>                                                  |
| <span data-ttu-id="f87ad-284">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="f87ad-284">In Global Catalog</span></span>      | <span data-ttu-id="f87ad-285">Falso</span><span class="sxs-lookup"><span data-stu-id="f87ad-285">False</span></span>                                                  |
| <span data-ttu-id="f87ad-286">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="f87ad-286">NT-Security-Descriptor</span></span> | <span data-ttu-id="f87ad-287">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="f87ad-287">O:BAG:BAD:S:</span></span>                                           |
| <span data-ttu-id="f87ad-288">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f87ad-288">Range-Lower</span></span>            | \-                                                     |
| <span data-ttu-id="f87ad-289">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f87ad-289">Range-Upper</span></span>            | \-                                                     |
| <span data-ttu-id="f87ad-290">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f87ad-290">Search-Flags</span></span>           | <span data-ttu-id="f87ad-291">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f87ad-291">0x00000000</span></span>                                             |
| <span data-ttu-id="f87ad-292">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f87ad-292">System-Flags</span></span>           | <span data-ttu-id="f87ad-293">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f87ad-293">0x00000010</span></span>                                             |
| <span data-ttu-id="f87ad-294">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="f87ad-294">Classes used in</span></span>        | [<span data-ttu-id="f87ad-295">**NTDS-connessione**</span><span class="sxs-lookup"><span data-stu-id="f87ad-295">**NTDS-Connection**</span></span>](c-ntdsconnection.md)<br/> |



 

 





