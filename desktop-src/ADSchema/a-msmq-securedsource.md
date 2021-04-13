---
title: MSMQ-protetto-attributo di origine
description: Questo fa parte di un oggetto MSMQ, viene impostato chiamando l'API su MQCreateQueue o MQSetProperties. Controlla se MSMQ accetta messaggi solo da un'origine protetta (ad esempio, HTTPS) per questa coda.
ms.assetid: 780d164f-c7fa-4c65-b46e-3a67ead92163
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo di origine protetto MSMQ
- Schema AD MSMQ-SecuredSource attribute
topic_type:
- apiref
api_name:
- MSMQ-Secured-Source
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5dd005cedcd650aa0604a85e78a46d10f1e01b0
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104519766"
---
# <a name="msmq-secured-source-attribute"></a><span data-ttu-id="81769-106">MSMQ-protetto-attributo di origine</span><span class="sxs-lookup"><span data-stu-id="81769-106">MSMQ-Secured-Source attribute</span></span>

<span data-ttu-id="81769-107">Questo fa parte di un oggetto MSMQ, viene impostato chiamando l'API su MQCreateQueue o MQSetProperties.</span><span class="sxs-lookup"><span data-stu-id="81769-107">This is part of an MSMQ object, it is set by calling API to MQCreateQueue or MQSetProperties.</span></span> <span data-ttu-id="81769-108">Controlla se MSMQ accetta messaggi solo da un'origine protetta (ad esempio, HTTPS) per questa coda.</span><span class="sxs-lookup"><span data-stu-id="81769-108">It controls whether MSMQ accepts messages only from a secured source (for example, https) for this queue.</span></span>



| <span data-ttu-id="81769-109">Voce</span><span class="sxs-lookup"><span data-stu-id="81769-109">Entry</span></span> | <span data-ttu-id="81769-110">Valore</span><span class="sxs-lookup"><span data-stu-id="81769-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="81769-111">CN</span><span class="sxs-lookup"><span data-stu-id="81769-111">CN</span></span>                | <span data-ttu-id="81769-112">MSMQ-protetto-origine</span><span class="sxs-lookup"><span data-stu-id="81769-112">MSMQ-Secured-Source</span></span>                  |
| <span data-ttu-id="81769-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="81769-113">Ldap-Display-Name</span></span> | <span data-ttu-id="81769-114">MSMQ-SecuredSource</span><span class="sxs-lookup"><span data-stu-id="81769-114">MSMQ-SecuredSource</span></span>                   |
| <span data-ttu-id="81769-115">Dimensione</span><span class="sxs-lookup"><span data-stu-id="81769-115">Size</span></span>              | <span data-ttu-id="81769-116">4 byte</span><span class="sxs-lookup"><span data-stu-id="81769-116">4 bytes</span></span>                              |
| <span data-ttu-id="81769-117">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="81769-117">Update Privilege</span></span>  | <span data-ttu-id="81769-118">Proprietario della coda.</span><span class="sxs-lookup"><span data-stu-id="81769-118">The queue owner.</span></span>                     |
| <span data-ttu-id="81769-119">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="81769-119">Update Frequency</span></span>  | <span data-ttu-id="81769-120">Quando viene creata una coda.</span><span class="sxs-lookup"><span data-stu-id="81769-120">When a queue is created.</span></span>             |
| <span data-ttu-id="81769-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="81769-121">Attribute-Id</span></span>      | <span data-ttu-id="81769-122">1.2.840.113556.1.4.1713</span><span class="sxs-lookup"><span data-stu-id="81769-122">1.2.840.113556.1.4.1713</span></span>              |
| <span data-ttu-id="81769-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="81769-123">System-Id-Guid</span></span>    | <span data-ttu-id="81769-124">8bf0221b-7a06-4d63-91f0-1499941813d3</span><span class="sxs-lookup"><span data-stu-id="81769-124">8bf0221b-7a06-4d63-91f0-1499941813d3</span></span> |
| <span data-ttu-id="81769-125">Sintassi</span><span class="sxs-lookup"><span data-stu-id="81769-125">Syntax</span></span>            | [<span data-ttu-id="81769-126">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="81769-126">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="81769-127">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="81769-127">Implementations</span></span>

-   [<span data-ttu-id="81769-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="81769-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="81769-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="81769-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="81769-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="81769-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="81769-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="81769-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="81769-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="81769-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="81769-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="81769-133">Windows Server 2003</span></span>



| <span data-ttu-id="81769-134">Voce</span><span class="sxs-lookup"><span data-stu-id="81769-134">Entry</span></span> | <span data-ttu-id="81769-135">Valore</span><span class="sxs-lookup"><span data-stu-id="81769-135">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="81769-136">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="81769-136">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="81769-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="81769-137">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="81769-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="81769-138">System-Only</span></span>            | <span data-ttu-id="81769-139">Falso</span><span class="sxs-lookup"><span data-stu-id="81769-139">False</span></span>                                        |
| <span data-ttu-id="81769-140">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="81769-140">Is-Single-Valued</span></span>       | <span data-ttu-id="81769-141">Vero</span><span class="sxs-lookup"><span data-stu-id="81769-141">True</span></span>                                         |
| <span data-ttu-id="81769-142">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="81769-142">Is Indexed</span></span>             | <span data-ttu-id="81769-143">Falso</span><span class="sxs-lookup"><span data-stu-id="81769-143">False</span></span>                                        |
| <span data-ttu-id="81769-144">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="81769-144">In Global Catalog</span></span>      | <span data-ttu-id="81769-145">Vero</span><span class="sxs-lookup"><span data-stu-id="81769-145">True</span></span>                                         |
| <span data-ttu-id="81769-146">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="81769-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="81769-147">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="81769-147">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="81769-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="81769-148">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="81769-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="81769-149">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="81769-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="81769-150">Search-Flags</span></span>           | <span data-ttu-id="81769-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="81769-151">0x00000000</span></span>                                   |
| <span data-ttu-id="81769-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="81769-152">System-Flags</span></span>           | <span data-ttu-id="81769-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="81769-153">0x00000010</span></span>                                   |
| <span data-ttu-id="81769-154">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="81769-154">Classes used in</span></span>        | [<span data-ttu-id="81769-155">**Coda MSMQ**</span><span class="sxs-lookup"><span data-stu-id="81769-155">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="81769-156">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="81769-156">Windows Server 2003 R2</span></span>



| <span data-ttu-id="81769-157">Voce</span><span class="sxs-lookup"><span data-stu-id="81769-157">Entry</span></span> | <span data-ttu-id="81769-158">Valore</span><span class="sxs-lookup"><span data-stu-id="81769-158">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="81769-159">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="81769-159">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="81769-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="81769-160">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="81769-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="81769-161">System-Only</span></span>            | <span data-ttu-id="81769-162">Falso</span><span class="sxs-lookup"><span data-stu-id="81769-162">False</span></span>                                        |
| <span data-ttu-id="81769-163">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="81769-163">Is-Single-Valued</span></span>       | <span data-ttu-id="81769-164">Vero</span><span class="sxs-lookup"><span data-stu-id="81769-164">True</span></span>                                         |
| <span data-ttu-id="81769-165">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="81769-165">Is Indexed</span></span>             | <span data-ttu-id="81769-166">Falso</span><span class="sxs-lookup"><span data-stu-id="81769-166">False</span></span>                                        |
| <span data-ttu-id="81769-167">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="81769-167">In Global Catalog</span></span>      | <span data-ttu-id="81769-168">Vero</span><span class="sxs-lookup"><span data-stu-id="81769-168">True</span></span>                                         |
| <span data-ttu-id="81769-169">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="81769-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="81769-170">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="81769-170">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="81769-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="81769-171">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="81769-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="81769-172">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="81769-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="81769-173">Search-Flags</span></span>           | <span data-ttu-id="81769-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="81769-174">0x00000000</span></span>                                   |
| <span data-ttu-id="81769-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="81769-175">System-Flags</span></span>           | <span data-ttu-id="81769-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="81769-176">0x00000010</span></span>                                   |
| <span data-ttu-id="81769-177">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="81769-177">Classes used in</span></span>        | [<span data-ttu-id="81769-178">**Coda MSMQ**</span><span class="sxs-lookup"><span data-stu-id="81769-178">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="81769-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="81769-179">Windows Server 2008</span></span>



| <span data-ttu-id="81769-180">Voce</span><span class="sxs-lookup"><span data-stu-id="81769-180">Entry</span></span> | <span data-ttu-id="81769-181">Valore</span><span class="sxs-lookup"><span data-stu-id="81769-181">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="81769-182">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="81769-182">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="81769-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="81769-183">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="81769-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="81769-184">System-Only</span></span>            | <span data-ttu-id="81769-185">Falso</span><span class="sxs-lookup"><span data-stu-id="81769-185">False</span></span>                                        |
| <span data-ttu-id="81769-186">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="81769-186">Is-Single-Valued</span></span>       | <span data-ttu-id="81769-187">Vero</span><span class="sxs-lookup"><span data-stu-id="81769-187">True</span></span>                                         |
| <span data-ttu-id="81769-188">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="81769-188">Is Indexed</span></span>             | <span data-ttu-id="81769-189">Falso</span><span class="sxs-lookup"><span data-stu-id="81769-189">False</span></span>                                        |
| <span data-ttu-id="81769-190">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="81769-190">In Global Catalog</span></span>      | <span data-ttu-id="81769-191">Vero</span><span class="sxs-lookup"><span data-stu-id="81769-191">True</span></span>                                         |
| <span data-ttu-id="81769-192">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="81769-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="81769-193">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="81769-193">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="81769-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="81769-194">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="81769-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="81769-195">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="81769-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="81769-196">Search-Flags</span></span>           | <span data-ttu-id="81769-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="81769-197">0x00000000</span></span>                                   |
| <span data-ttu-id="81769-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="81769-198">System-Flags</span></span>           | <span data-ttu-id="81769-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="81769-199">0x00000010</span></span>                                   |
| <span data-ttu-id="81769-200">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="81769-200">Classes used in</span></span>        | [<span data-ttu-id="81769-201">**Coda MSMQ**</span><span class="sxs-lookup"><span data-stu-id="81769-201">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="81769-202">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="81769-202">Windows Server 2008 R2</span></span>



| <span data-ttu-id="81769-203">Voce</span><span class="sxs-lookup"><span data-stu-id="81769-203">Entry</span></span> | <span data-ttu-id="81769-204">Valore</span><span class="sxs-lookup"><span data-stu-id="81769-204">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="81769-205">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="81769-205">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="81769-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="81769-206">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="81769-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="81769-207">System-Only</span></span>            | <span data-ttu-id="81769-208">Falso</span><span class="sxs-lookup"><span data-stu-id="81769-208">False</span></span>                                        |
| <span data-ttu-id="81769-209">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="81769-209">Is-Single-Valued</span></span>       | <span data-ttu-id="81769-210">Vero</span><span class="sxs-lookup"><span data-stu-id="81769-210">True</span></span>                                         |
| <span data-ttu-id="81769-211">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="81769-211">Is Indexed</span></span>             | <span data-ttu-id="81769-212">Falso</span><span class="sxs-lookup"><span data-stu-id="81769-212">False</span></span>                                        |
| <span data-ttu-id="81769-213">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="81769-213">In Global Catalog</span></span>      | <span data-ttu-id="81769-214">Vero</span><span class="sxs-lookup"><span data-stu-id="81769-214">True</span></span>                                         |
| <span data-ttu-id="81769-215">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="81769-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="81769-216">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="81769-216">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="81769-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="81769-217">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="81769-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="81769-218">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="81769-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="81769-219">Search-Flags</span></span>           | <span data-ttu-id="81769-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="81769-220">0x00000000</span></span>                                   |
| <span data-ttu-id="81769-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="81769-221">System-Flags</span></span>           | <span data-ttu-id="81769-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="81769-222">0x00000010</span></span>                                   |
| <span data-ttu-id="81769-223">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="81769-223">Classes used in</span></span>        | [<span data-ttu-id="81769-224">**Coda MSMQ**</span><span class="sxs-lookup"><span data-stu-id="81769-224">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="81769-225">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="81769-225">Windows Server 2012</span></span>



| <span data-ttu-id="81769-226">Voce</span><span class="sxs-lookup"><span data-stu-id="81769-226">Entry</span></span> | <span data-ttu-id="81769-227">Valore</span><span class="sxs-lookup"><span data-stu-id="81769-227">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="81769-228">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="81769-228">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="81769-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="81769-229">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="81769-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="81769-230">System-Only</span></span>            | <span data-ttu-id="81769-231">Falso</span><span class="sxs-lookup"><span data-stu-id="81769-231">False</span></span>                                        |
| <span data-ttu-id="81769-232">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="81769-232">Is-Single-Valued</span></span>       | <span data-ttu-id="81769-233">Vero</span><span class="sxs-lookup"><span data-stu-id="81769-233">True</span></span>                                         |
| <span data-ttu-id="81769-234">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="81769-234">Is Indexed</span></span>             | <span data-ttu-id="81769-235">Falso</span><span class="sxs-lookup"><span data-stu-id="81769-235">False</span></span>                                        |
| <span data-ttu-id="81769-236">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="81769-236">In Global Catalog</span></span>      | <span data-ttu-id="81769-237">Vero</span><span class="sxs-lookup"><span data-stu-id="81769-237">True</span></span>                                         |
| <span data-ttu-id="81769-238">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="81769-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="81769-239">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="81769-239">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="81769-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="81769-240">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="81769-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="81769-241">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="81769-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="81769-242">Search-Flags</span></span>           | <span data-ttu-id="81769-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="81769-243">0x00000000</span></span>                                   |
| <span data-ttu-id="81769-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="81769-244">System-Flags</span></span>           | <span data-ttu-id="81769-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="81769-245">0x00000010</span></span>                                   |
| <span data-ttu-id="81769-246">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="81769-246">Classes used in</span></span>        | [<span data-ttu-id="81769-247">**Coda MSMQ**</span><span class="sxs-lookup"><span data-stu-id="81769-247">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



 

 





