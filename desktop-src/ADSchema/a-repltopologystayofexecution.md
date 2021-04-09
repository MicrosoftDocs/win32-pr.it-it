---
title: REPL-topologia-attributo stay-of-Execution
description: Ritardo tra l'eliminazione di un oggetto server e la relativa rimozione definitiva dalla topologia di replica.
ms.assetid: 770231b0-4886-41c2-a3b5-ac488ac09669
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo REPL-topologia-Rest-of-Execution
- Schema AD dell'attributo replTopologyStayOfExecution
topic_type:
- apiref
api_name:
- Repl-Topology-Stay-Of-Execution
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a51c74c477cce926dd18ea17b8df2b1adcf99df1
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744554"
---
# <a name="repl-topology-stay-of-execution-attribute"></a><span data-ttu-id="12eb9-105">REPL-topologia-attributo stay-of-Execution</span><span class="sxs-lookup"><span data-stu-id="12eb9-105">Repl-Topology-Stay-Of-Execution attribute</span></span>

<span data-ttu-id="12eb9-106">Ritardo tra l'eliminazione di un oggetto server e la relativa rimozione definitiva dalla topologia di replica.</span><span class="sxs-lookup"><span data-stu-id="12eb9-106">The delay between deleting a server object and it being permanently removed from the replication topology.</span></span>



| <span data-ttu-id="12eb9-107">Voce</span><span class="sxs-lookup"><span data-stu-id="12eb9-107">Entry</span></span> | <span data-ttu-id="12eb9-108">Valore</span><span class="sxs-lookup"><span data-stu-id="12eb9-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="12eb9-109">CN</span><span class="sxs-lookup"><span data-stu-id="12eb9-109">CN</span></span>                | <span data-ttu-id="12eb9-110">REPL-topologia-permanenza di esecuzione</span><span class="sxs-lookup"><span data-stu-id="12eb9-110">Repl-Topology-Stay-Of-Execution</span></span>      |
| <span data-ttu-id="12eb9-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="12eb9-111">Ldap-Display-Name</span></span> | <span data-ttu-id="12eb9-112">replTopologyStayOfExecution</span><span class="sxs-lookup"><span data-stu-id="12eb9-112">replTopologyStayOfExecution</span></span>          |
| <span data-ttu-id="12eb9-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="12eb9-113">Size</span></span>              | <span data-ttu-id="12eb9-114">4 byte</span><span class="sxs-lookup"><span data-stu-id="12eb9-114">4 bytes</span></span>                              |
| <span data-ttu-id="12eb9-115">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="12eb9-115">Update Privilege</span></span>  | <span data-ttu-id="12eb9-116">Questo valore viene impostato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="12eb9-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="12eb9-117">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="12eb9-117">Update Frequency</span></span>  | <span data-ttu-id="12eb9-118">Ogni volta che un oggetto server viene eliminato.</span><span class="sxs-lookup"><span data-stu-id="12eb9-118">Whenever a server object is deleted.</span></span> |
| <span data-ttu-id="12eb9-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="12eb9-119">Attribute-Id</span></span>      | <span data-ttu-id="12eb9-120">1.2.840.113556.1.4.677</span><span class="sxs-lookup"><span data-stu-id="12eb9-120">1.2.840.113556.1.4.677</span></span>               |
| <span data-ttu-id="12eb9-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="12eb9-121">System-Id-Guid</span></span>    | <span data-ttu-id="12eb9-122">7bfdcb83-4807-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="12eb9-122">7bfdcb83-4807-11d1-a9c3-0000f80367c1</span></span> |
| <span data-ttu-id="12eb9-123">Sintassi</span><span class="sxs-lookup"><span data-stu-id="12eb9-123">Syntax</span></span>            | [<span data-ttu-id="12eb9-124">**Enumerazione**</span><span class="sxs-lookup"><span data-stu-id="12eb9-124">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="12eb9-125">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="12eb9-125">Implementations</span></span>

-   [<span data-ttu-id="12eb9-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="12eb9-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="12eb9-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="12eb9-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="12eb9-128">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="12eb9-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="12eb9-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="12eb9-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="12eb9-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="12eb9-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="12eb9-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="12eb9-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="12eb9-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="12eb9-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="12eb9-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="12eb9-133">Windows 2000 Server</span></span>



| <span data-ttu-id="12eb9-134">Voce</span><span class="sxs-lookup"><span data-stu-id="12eb9-134">Entry</span></span> | <span data-ttu-id="12eb9-135">Valore</span><span class="sxs-lookup"><span data-stu-id="12eb9-135">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="12eb9-136">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="12eb9-136">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="12eb9-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="12eb9-137">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="12eb9-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="12eb9-138">System-Only</span></span>            | <span data-ttu-id="12eb9-139">Falso</span><span class="sxs-lookup"><span data-stu-id="12eb9-139">False</span></span>                                            |
| <span data-ttu-id="12eb9-140">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="12eb9-140">Is-Single-Valued</span></span>       | <span data-ttu-id="12eb9-141">Vero</span><span class="sxs-lookup"><span data-stu-id="12eb9-141">True</span></span>                                             |
| <span data-ttu-id="12eb9-142">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="12eb9-142">Is Indexed</span></span>             | <span data-ttu-id="12eb9-143">Falso</span><span class="sxs-lookup"><span data-stu-id="12eb9-143">False</span></span>                                            |
| <span data-ttu-id="12eb9-144">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="12eb9-144">In Global Catalog</span></span>      | <span data-ttu-id="12eb9-145">Falso</span><span class="sxs-lookup"><span data-stu-id="12eb9-145">False</span></span>                                            |
| <span data-ttu-id="12eb9-146">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="12eb9-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="12eb9-147">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="12eb9-147">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="12eb9-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="12eb9-148">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="12eb9-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="12eb9-149">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="12eb9-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="12eb9-150">Search-Flags</span></span>           | <span data-ttu-id="12eb9-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="12eb9-151">0x00000000</span></span>                                       |
| <span data-ttu-id="12eb9-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="12eb9-152">System-Flags</span></span>           | <span data-ttu-id="12eb9-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="12eb9-153">0x00000010</span></span>                                       |
| <span data-ttu-id="12eb9-154">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="12eb9-154">Classes used in</span></span>        | [<span data-ttu-id="12eb9-155">**NTDS-Service**</span><span class="sxs-lookup"><span data-stu-id="12eb9-155">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="12eb9-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="12eb9-156">Windows Server 2003</span></span>



| <span data-ttu-id="12eb9-157">Voce</span><span class="sxs-lookup"><span data-stu-id="12eb9-157">Entry</span></span> | <span data-ttu-id="12eb9-158">Valore</span><span class="sxs-lookup"><span data-stu-id="12eb9-158">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="12eb9-159">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="12eb9-159">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="12eb9-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="12eb9-160">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="12eb9-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="12eb9-161">System-Only</span></span>            | <span data-ttu-id="12eb9-162">Falso</span><span class="sxs-lookup"><span data-stu-id="12eb9-162">False</span></span>                                            |
| <span data-ttu-id="12eb9-163">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="12eb9-163">Is-Single-Valued</span></span>       | <span data-ttu-id="12eb9-164">Vero</span><span class="sxs-lookup"><span data-stu-id="12eb9-164">True</span></span>                                             |
| <span data-ttu-id="12eb9-165">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="12eb9-165">Is Indexed</span></span>             | <span data-ttu-id="12eb9-166">Falso</span><span class="sxs-lookup"><span data-stu-id="12eb9-166">False</span></span>                                            |
| <span data-ttu-id="12eb9-167">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="12eb9-167">In Global Catalog</span></span>      | <span data-ttu-id="12eb9-168">Falso</span><span class="sxs-lookup"><span data-stu-id="12eb9-168">False</span></span>                                            |
| <span data-ttu-id="12eb9-169">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="12eb9-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="12eb9-170">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="12eb9-170">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="12eb9-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="12eb9-171">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="12eb9-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="12eb9-172">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="12eb9-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="12eb9-173">Search-Flags</span></span>           | <span data-ttu-id="12eb9-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="12eb9-174">0x00000000</span></span>                                       |
| <span data-ttu-id="12eb9-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="12eb9-175">System-Flags</span></span>           | <span data-ttu-id="12eb9-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="12eb9-176">0x00000010</span></span>                                       |
| <span data-ttu-id="12eb9-177">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="12eb9-177">Classes used in</span></span>        | [<span data-ttu-id="12eb9-178">**NTDS-Service**</span><span class="sxs-lookup"><span data-stu-id="12eb9-178">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="adam"></a><span data-ttu-id="12eb9-179">ADAM</span><span class="sxs-lookup"><span data-stu-id="12eb9-179">ADAM</span></span>



| <span data-ttu-id="12eb9-180">Voce</span><span class="sxs-lookup"><span data-stu-id="12eb9-180">Entry</span></span> | <span data-ttu-id="12eb9-181">Valore</span><span class="sxs-lookup"><span data-stu-id="12eb9-181">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="12eb9-182">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="12eb9-182">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="12eb9-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="12eb9-183">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="12eb9-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="12eb9-184">System-Only</span></span>            | <span data-ttu-id="12eb9-185">Falso</span><span class="sxs-lookup"><span data-stu-id="12eb9-185">False</span></span>                                            |
| <span data-ttu-id="12eb9-186">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="12eb9-186">Is-Single-Valued</span></span>       | <span data-ttu-id="12eb9-187">Vero</span><span class="sxs-lookup"><span data-stu-id="12eb9-187">True</span></span>                                             |
| <span data-ttu-id="12eb9-188">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="12eb9-188">Is Indexed</span></span>             | <span data-ttu-id="12eb9-189">Falso</span><span class="sxs-lookup"><span data-stu-id="12eb9-189">False</span></span>                                            |
| <span data-ttu-id="12eb9-190">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="12eb9-190">In Global Catalog</span></span>      | <span data-ttu-id="12eb9-191">Falso</span><span class="sxs-lookup"><span data-stu-id="12eb9-191">False</span></span>                                            |
| <span data-ttu-id="12eb9-192">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="12eb9-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="12eb9-193">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="12eb9-193">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="12eb9-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="12eb9-194">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="12eb9-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="12eb9-195">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="12eb9-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="12eb9-196">Search-Flags</span></span>           | <span data-ttu-id="12eb9-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="12eb9-197">0x00000000</span></span>                                       |
| <span data-ttu-id="12eb9-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="12eb9-198">System-Flags</span></span>           | <span data-ttu-id="12eb9-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="12eb9-199">0x00000010</span></span>                                       |
| <span data-ttu-id="12eb9-200">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="12eb9-200">Classes used in</span></span>        | [<span data-ttu-id="12eb9-201">**NTDS-Service**</span><span class="sxs-lookup"><span data-stu-id="12eb9-201">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="12eb9-202">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="12eb9-202">Windows Server 2003 R2</span></span>



| <span data-ttu-id="12eb9-203">Voce</span><span class="sxs-lookup"><span data-stu-id="12eb9-203">Entry</span></span> | <span data-ttu-id="12eb9-204">Valore</span><span class="sxs-lookup"><span data-stu-id="12eb9-204">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="12eb9-205">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="12eb9-205">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="12eb9-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="12eb9-206">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="12eb9-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="12eb9-207">System-Only</span></span>            | <span data-ttu-id="12eb9-208">Falso</span><span class="sxs-lookup"><span data-stu-id="12eb9-208">False</span></span>                                            |
| <span data-ttu-id="12eb9-209">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="12eb9-209">Is-Single-Valued</span></span>       | <span data-ttu-id="12eb9-210">Vero</span><span class="sxs-lookup"><span data-stu-id="12eb9-210">True</span></span>                                             |
| <span data-ttu-id="12eb9-211">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="12eb9-211">Is Indexed</span></span>             | <span data-ttu-id="12eb9-212">Falso</span><span class="sxs-lookup"><span data-stu-id="12eb9-212">False</span></span>                                            |
| <span data-ttu-id="12eb9-213">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="12eb9-213">In Global Catalog</span></span>      | <span data-ttu-id="12eb9-214">Falso</span><span class="sxs-lookup"><span data-stu-id="12eb9-214">False</span></span>                                            |
| <span data-ttu-id="12eb9-215">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="12eb9-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="12eb9-216">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="12eb9-216">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="12eb9-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="12eb9-217">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="12eb9-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="12eb9-218">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="12eb9-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="12eb9-219">Search-Flags</span></span>           | <span data-ttu-id="12eb9-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="12eb9-220">0x00000000</span></span>                                       |
| <span data-ttu-id="12eb9-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="12eb9-221">System-Flags</span></span>           | <span data-ttu-id="12eb9-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="12eb9-222">0x00000010</span></span>                                       |
| <span data-ttu-id="12eb9-223">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="12eb9-223">Classes used in</span></span>        | [<span data-ttu-id="12eb9-224">**NTDS-Service**</span><span class="sxs-lookup"><span data-stu-id="12eb9-224">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="12eb9-225">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="12eb9-225">Windows Server 2008</span></span>



| <span data-ttu-id="12eb9-226">Voce</span><span class="sxs-lookup"><span data-stu-id="12eb9-226">Entry</span></span> | <span data-ttu-id="12eb9-227">Valore</span><span class="sxs-lookup"><span data-stu-id="12eb9-227">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="12eb9-228">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="12eb9-228">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="12eb9-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="12eb9-229">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="12eb9-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="12eb9-230">System-Only</span></span>            | <span data-ttu-id="12eb9-231">Falso</span><span class="sxs-lookup"><span data-stu-id="12eb9-231">False</span></span>                                            |
| <span data-ttu-id="12eb9-232">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="12eb9-232">Is-Single-Valued</span></span>       | <span data-ttu-id="12eb9-233">Vero</span><span class="sxs-lookup"><span data-stu-id="12eb9-233">True</span></span>                                             |
| <span data-ttu-id="12eb9-234">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="12eb9-234">Is Indexed</span></span>             | <span data-ttu-id="12eb9-235">Falso</span><span class="sxs-lookup"><span data-stu-id="12eb9-235">False</span></span>                                            |
| <span data-ttu-id="12eb9-236">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="12eb9-236">In Global Catalog</span></span>      | <span data-ttu-id="12eb9-237">Falso</span><span class="sxs-lookup"><span data-stu-id="12eb9-237">False</span></span>                                            |
| <span data-ttu-id="12eb9-238">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="12eb9-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="12eb9-239">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="12eb9-239">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="12eb9-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="12eb9-240">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="12eb9-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="12eb9-241">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="12eb9-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="12eb9-242">Search-Flags</span></span>           | <span data-ttu-id="12eb9-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="12eb9-243">0x00000000</span></span>                                       |
| <span data-ttu-id="12eb9-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="12eb9-244">System-Flags</span></span>           | <span data-ttu-id="12eb9-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="12eb9-245">0x00000010</span></span>                                       |
| <span data-ttu-id="12eb9-246">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="12eb9-246">Classes used in</span></span>        | [<span data-ttu-id="12eb9-247">**NTDS-Service**</span><span class="sxs-lookup"><span data-stu-id="12eb9-247">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="12eb9-248">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="12eb9-248">Windows Server 2008 R2</span></span>



| <span data-ttu-id="12eb9-249">Voce</span><span class="sxs-lookup"><span data-stu-id="12eb9-249">Entry</span></span> | <span data-ttu-id="12eb9-250">Valore</span><span class="sxs-lookup"><span data-stu-id="12eb9-250">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="12eb9-251">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="12eb9-251">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="12eb9-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="12eb9-252">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="12eb9-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="12eb9-253">System-Only</span></span>            | <span data-ttu-id="12eb9-254">Falso</span><span class="sxs-lookup"><span data-stu-id="12eb9-254">False</span></span>                                            |
| <span data-ttu-id="12eb9-255">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="12eb9-255">Is-Single-Valued</span></span>       | <span data-ttu-id="12eb9-256">Vero</span><span class="sxs-lookup"><span data-stu-id="12eb9-256">True</span></span>                                             |
| <span data-ttu-id="12eb9-257">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="12eb9-257">Is Indexed</span></span>             | <span data-ttu-id="12eb9-258">Falso</span><span class="sxs-lookup"><span data-stu-id="12eb9-258">False</span></span>                                            |
| <span data-ttu-id="12eb9-259">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="12eb9-259">In Global Catalog</span></span>      | <span data-ttu-id="12eb9-260">Falso</span><span class="sxs-lookup"><span data-stu-id="12eb9-260">False</span></span>                                            |
| <span data-ttu-id="12eb9-261">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="12eb9-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="12eb9-262">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="12eb9-262">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="12eb9-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="12eb9-263">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="12eb9-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="12eb9-264">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="12eb9-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="12eb9-265">Search-Flags</span></span>           | <span data-ttu-id="12eb9-266">0x00000000</span><span class="sxs-lookup"><span data-stu-id="12eb9-266">0x00000000</span></span>                                       |
| <span data-ttu-id="12eb9-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="12eb9-267">System-Flags</span></span>           | <span data-ttu-id="12eb9-268">0x00000010</span><span class="sxs-lookup"><span data-stu-id="12eb9-268">0x00000010</span></span>                                       |
| <span data-ttu-id="12eb9-269">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="12eb9-269">Classes used in</span></span>        | [<span data-ttu-id="12eb9-270">**NTDS-Service**</span><span class="sxs-lookup"><span data-stu-id="12eb9-270">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="12eb9-271">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="12eb9-271">Windows Server 2012</span></span>



| <span data-ttu-id="12eb9-272">Voce</span><span class="sxs-lookup"><span data-stu-id="12eb9-272">Entry</span></span> | <span data-ttu-id="12eb9-273">Valore</span><span class="sxs-lookup"><span data-stu-id="12eb9-273">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="12eb9-274">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="12eb9-274">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="12eb9-275">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="12eb9-275">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="12eb9-276">System-Only</span><span class="sxs-lookup"><span data-stu-id="12eb9-276">System-Only</span></span>            | <span data-ttu-id="12eb9-277">Falso</span><span class="sxs-lookup"><span data-stu-id="12eb9-277">False</span></span>                                            |
| <span data-ttu-id="12eb9-278">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="12eb9-278">Is-Single-Valued</span></span>       | <span data-ttu-id="12eb9-279">Vero</span><span class="sxs-lookup"><span data-stu-id="12eb9-279">True</span></span>                                             |
| <span data-ttu-id="12eb9-280">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="12eb9-280">Is Indexed</span></span>             | <span data-ttu-id="12eb9-281">Falso</span><span class="sxs-lookup"><span data-stu-id="12eb9-281">False</span></span>                                            |
| <span data-ttu-id="12eb9-282">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="12eb9-282">In Global Catalog</span></span>      | <span data-ttu-id="12eb9-283">Falso</span><span class="sxs-lookup"><span data-stu-id="12eb9-283">False</span></span>                                            |
| <span data-ttu-id="12eb9-284">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="12eb9-284">NT-Security-Descriptor</span></span> | <span data-ttu-id="12eb9-285">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="12eb9-285">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="12eb9-286">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="12eb9-286">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="12eb9-287">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="12eb9-287">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="12eb9-288">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="12eb9-288">Search-Flags</span></span>           | <span data-ttu-id="12eb9-289">0x00000000</span><span class="sxs-lookup"><span data-stu-id="12eb9-289">0x00000000</span></span>                                       |
| <span data-ttu-id="12eb9-290">System-Flags</span><span class="sxs-lookup"><span data-stu-id="12eb9-290">System-Flags</span></span>           | <span data-ttu-id="12eb9-291">0x00000010</span><span class="sxs-lookup"><span data-stu-id="12eb9-291">0x00000010</span></span>                                       |
| <span data-ttu-id="12eb9-292">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="12eb9-292">Classes used in</span></span>        | [<span data-ttu-id="12eb9-293">**NTDS-Service**</span><span class="sxs-lookup"><span data-stu-id="12eb9-293">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



 

 





