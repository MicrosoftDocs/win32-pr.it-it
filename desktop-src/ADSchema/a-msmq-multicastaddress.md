---
title: MSMQ-multicast-address-attributo
description: Questo fa parte di un oggetto MSMQ, viene impostato chiamando l'API su MQCreateQueue o MQSetProperties. Controlla se MSMQ accetterà messaggi da un indirizzo multicast.
ms.assetid: 65622cc9-81d9-42c6-b208-cac703f32244
ms.tgt_platform: multiple
keywords:
- MSMQ-multicast-address-schema AD
- Schema AD MSMQ-MulticastAddress attribute
topic_type:
- apiref
api_name:
- MSMQ-Multicast-Address
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a1b90543c40e22d8dd5fdc2b3e5195bd9382357
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104519773"
---
# <a name="msmq-multicast-address-attribute"></a><span data-ttu-id="341d6-106">MSMQ-multicast-address-attributo</span><span class="sxs-lookup"><span data-stu-id="341d6-106">MSMQ-Multicast-Address attribute</span></span>

<span data-ttu-id="341d6-107">Questo fa parte di un oggetto MSMQ, viene impostato chiamando l'API su MQCreateQueue o MQSetProperties.</span><span class="sxs-lookup"><span data-stu-id="341d6-107">This is part of an MSMQ object, it is set by calling API to MQCreateQueue or MQSetProperties.</span></span> <span data-ttu-id="341d6-108">Controlla se MSMQ accetterà messaggi da un indirizzo multicast.</span><span class="sxs-lookup"><span data-stu-id="341d6-108">It controls whether MSMQ will accept messages from a multicast address.</span></span>



| <span data-ttu-id="341d6-109">Voce</span><span class="sxs-lookup"><span data-stu-id="341d6-109">Entry</span></span> | <span data-ttu-id="341d6-110">Valore</span><span class="sxs-lookup"><span data-stu-id="341d6-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="341d6-111">CN</span><span class="sxs-lookup"><span data-stu-id="341d6-111">CN</span></span>                | <span data-ttu-id="341d6-112">MSMQ-multicast-address</span><span class="sxs-lookup"><span data-stu-id="341d6-112">MSMQ-Multicast-Address</span></span>                      |
| <span data-ttu-id="341d6-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="341d6-113">Ldap-Display-Name</span></span> | <span data-ttu-id="341d6-114">MSMQ-MulticastAddress</span><span class="sxs-lookup"><span data-stu-id="341d6-114">MSMQ-MulticastAddress</span></span>                       |
| <span data-ttu-id="341d6-115">Dimensione</span><span class="sxs-lookup"><span data-stu-id="341d6-115">Size</span></span>              | <span data-ttu-id="341d6-116">4 byte</span><span class="sxs-lookup"><span data-stu-id="341d6-116">4 bytes</span></span>                                     |
| <span data-ttu-id="341d6-117">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="341d6-117">Update Privilege</span></span>  | <span data-ttu-id="341d6-118">Proprietario della coda.</span><span class="sxs-lookup"><span data-stu-id="341d6-118">The queue owner.</span></span>                            |
| <span data-ttu-id="341d6-119">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="341d6-119">Update Frequency</span></span>  | <span data-ttu-id="341d6-120">Quando viene creata una coda.</span><span class="sxs-lookup"><span data-stu-id="341d6-120">When a queue is created.</span></span>                    |
| <span data-ttu-id="341d6-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="341d6-121">Attribute-Id</span></span>      | <span data-ttu-id="341d6-122">1.2.840.113556.1.4.1714</span><span class="sxs-lookup"><span data-stu-id="341d6-122">1.2.840.113556.1.4.1714</span></span>                     |
| <span data-ttu-id="341d6-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="341d6-123">System-Id-Guid</span></span>    | <span data-ttu-id="341d6-124">1d2f4412-f10d-4337-9b48-6e5b125cd265</span><span class="sxs-lookup"><span data-stu-id="341d6-124">1d2f4412-f10d-4337-9b48-6e5b125cd265</span></span>        |
| <span data-ttu-id="341d6-125">Sintassi</span><span class="sxs-lookup"><span data-stu-id="341d6-125">Syntax</span></span>            | [<span data-ttu-id="341d6-126">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="341d6-126">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="341d6-127">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="341d6-127">Implementations</span></span>

-   [<span data-ttu-id="341d6-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="341d6-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="341d6-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="341d6-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="341d6-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="341d6-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="341d6-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="341d6-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="341d6-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="341d6-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="341d6-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="341d6-133">Windows Server 2003</span></span>



| <span data-ttu-id="341d6-134">Voce</span><span class="sxs-lookup"><span data-stu-id="341d6-134">Entry</span></span> | <span data-ttu-id="341d6-135">Valore</span><span class="sxs-lookup"><span data-stu-id="341d6-135">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="341d6-136">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="341d6-136">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="341d6-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="341d6-137">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="341d6-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="341d6-138">System-Only</span></span>            | <span data-ttu-id="341d6-139">Falso</span><span class="sxs-lookup"><span data-stu-id="341d6-139">False</span></span>                                        |
| <span data-ttu-id="341d6-140">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="341d6-140">Is-Single-Valued</span></span>       | <span data-ttu-id="341d6-141">Vero</span><span class="sxs-lookup"><span data-stu-id="341d6-141">True</span></span>                                         |
| <span data-ttu-id="341d6-142">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="341d6-142">Is Indexed</span></span>             | <span data-ttu-id="341d6-143">Falso</span><span class="sxs-lookup"><span data-stu-id="341d6-143">False</span></span>                                        |
| <span data-ttu-id="341d6-144">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="341d6-144">In Global Catalog</span></span>      | <span data-ttu-id="341d6-145">Vero</span><span class="sxs-lookup"><span data-stu-id="341d6-145">True</span></span>                                         |
| <span data-ttu-id="341d6-146">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="341d6-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="341d6-147">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="341d6-147">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="341d6-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="341d6-148">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="341d6-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="341d6-149">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="341d6-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="341d6-150">Search-Flags</span></span>           | <span data-ttu-id="341d6-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="341d6-151">0x00000000</span></span>                                   |
| <span data-ttu-id="341d6-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="341d6-152">System-Flags</span></span>           | <span data-ttu-id="341d6-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="341d6-153">0x00000010</span></span>                                   |
| <span data-ttu-id="341d6-154">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="341d6-154">Classes used in</span></span>        | [<span data-ttu-id="341d6-155">**Coda MSMQ**</span><span class="sxs-lookup"><span data-stu-id="341d6-155">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="341d6-156">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="341d6-156">Windows Server 2003 R2</span></span>



| <span data-ttu-id="341d6-157">Voce</span><span class="sxs-lookup"><span data-stu-id="341d6-157">Entry</span></span> | <span data-ttu-id="341d6-158">Valore</span><span class="sxs-lookup"><span data-stu-id="341d6-158">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="341d6-159">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="341d6-159">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="341d6-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="341d6-160">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="341d6-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="341d6-161">System-Only</span></span>            | <span data-ttu-id="341d6-162">Falso</span><span class="sxs-lookup"><span data-stu-id="341d6-162">False</span></span>                                        |
| <span data-ttu-id="341d6-163">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="341d6-163">Is-Single-Valued</span></span>       | <span data-ttu-id="341d6-164">Vero</span><span class="sxs-lookup"><span data-stu-id="341d6-164">True</span></span>                                         |
| <span data-ttu-id="341d6-165">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="341d6-165">Is Indexed</span></span>             | <span data-ttu-id="341d6-166">Falso</span><span class="sxs-lookup"><span data-stu-id="341d6-166">False</span></span>                                        |
| <span data-ttu-id="341d6-167">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="341d6-167">In Global Catalog</span></span>      | <span data-ttu-id="341d6-168">Vero</span><span class="sxs-lookup"><span data-stu-id="341d6-168">True</span></span>                                         |
| <span data-ttu-id="341d6-169">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="341d6-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="341d6-170">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="341d6-170">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="341d6-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="341d6-171">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="341d6-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="341d6-172">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="341d6-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="341d6-173">Search-Flags</span></span>           | <span data-ttu-id="341d6-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="341d6-174">0x00000000</span></span>                                   |
| <span data-ttu-id="341d6-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="341d6-175">System-Flags</span></span>           | <span data-ttu-id="341d6-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="341d6-176">0x00000010</span></span>                                   |
| <span data-ttu-id="341d6-177">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="341d6-177">Classes used in</span></span>        | [<span data-ttu-id="341d6-178">**Coda MSMQ**</span><span class="sxs-lookup"><span data-stu-id="341d6-178">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="341d6-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="341d6-179">Windows Server 2008</span></span>



| <span data-ttu-id="341d6-180">Voce</span><span class="sxs-lookup"><span data-stu-id="341d6-180">Entry</span></span> | <span data-ttu-id="341d6-181">Valore</span><span class="sxs-lookup"><span data-stu-id="341d6-181">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="341d6-182">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="341d6-182">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="341d6-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="341d6-183">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="341d6-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="341d6-184">System-Only</span></span>            | <span data-ttu-id="341d6-185">Falso</span><span class="sxs-lookup"><span data-stu-id="341d6-185">False</span></span>                                        |
| <span data-ttu-id="341d6-186">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="341d6-186">Is-Single-Valued</span></span>       | <span data-ttu-id="341d6-187">Vero</span><span class="sxs-lookup"><span data-stu-id="341d6-187">True</span></span>                                         |
| <span data-ttu-id="341d6-188">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="341d6-188">Is Indexed</span></span>             | <span data-ttu-id="341d6-189">Falso</span><span class="sxs-lookup"><span data-stu-id="341d6-189">False</span></span>                                        |
| <span data-ttu-id="341d6-190">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="341d6-190">In Global Catalog</span></span>      | <span data-ttu-id="341d6-191">Vero</span><span class="sxs-lookup"><span data-stu-id="341d6-191">True</span></span>                                         |
| <span data-ttu-id="341d6-192">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="341d6-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="341d6-193">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="341d6-193">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="341d6-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="341d6-194">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="341d6-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="341d6-195">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="341d6-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="341d6-196">Search-Flags</span></span>           | <span data-ttu-id="341d6-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="341d6-197">0x00000000</span></span>                                   |
| <span data-ttu-id="341d6-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="341d6-198">System-Flags</span></span>           | <span data-ttu-id="341d6-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="341d6-199">0x00000010</span></span>                                   |
| <span data-ttu-id="341d6-200">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="341d6-200">Classes used in</span></span>        | [<span data-ttu-id="341d6-201">**Coda MSMQ**</span><span class="sxs-lookup"><span data-stu-id="341d6-201">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="341d6-202">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="341d6-202">Windows Server 2008 R2</span></span>



| <span data-ttu-id="341d6-203">Voce</span><span class="sxs-lookup"><span data-stu-id="341d6-203">Entry</span></span> | <span data-ttu-id="341d6-204">Valore</span><span class="sxs-lookup"><span data-stu-id="341d6-204">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="341d6-205">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="341d6-205">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="341d6-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="341d6-206">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="341d6-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="341d6-207">System-Only</span></span>            | <span data-ttu-id="341d6-208">Falso</span><span class="sxs-lookup"><span data-stu-id="341d6-208">False</span></span>                                        |
| <span data-ttu-id="341d6-209">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="341d6-209">Is-Single-Valued</span></span>       | <span data-ttu-id="341d6-210">Vero</span><span class="sxs-lookup"><span data-stu-id="341d6-210">True</span></span>                                         |
| <span data-ttu-id="341d6-211">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="341d6-211">Is Indexed</span></span>             | <span data-ttu-id="341d6-212">Falso</span><span class="sxs-lookup"><span data-stu-id="341d6-212">False</span></span>                                        |
| <span data-ttu-id="341d6-213">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="341d6-213">In Global Catalog</span></span>      | <span data-ttu-id="341d6-214">Vero</span><span class="sxs-lookup"><span data-stu-id="341d6-214">True</span></span>                                         |
| <span data-ttu-id="341d6-215">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="341d6-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="341d6-216">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="341d6-216">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="341d6-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="341d6-217">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="341d6-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="341d6-218">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="341d6-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="341d6-219">Search-Flags</span></span>           | <span data-ttu-id="341d6-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="341d6-220">0x00000000</span></span>                                   |
| <span data-ttu-id="341d6-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="341d6-221">System-Flags</span></span>           | <span data-ttu-id="341d6-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="341d6-222">0x00000010</span></span>                                   |
| <span data-ttu-id="341d6-223">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="341d6-223">Classes used in</span></span>        | [<span data-ttu-id="341d6-224">**Coda MSMQ**</span><span class="sxs-lookup"><span data-stu-id="341d6-224">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="341d6-225">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="341d6-225">Windows Server 2012</span></span>



| <span data-ttu-id="341d6-226">Voce</span><span class="sxs-lookup"><span data-stu-id="341d6-226">Entry</span></span> | <span data-ttu-id="341d6-227">Valore</span><span class="sxs-lookup"><span data-stu-id="341d6-227">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="341d6-228">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="341d6-228">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="341d6-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="341d6-229">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="341d6-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="341d6-230">System-Only</span></span>            | <span data-ttu-id="341d6-231">Falso</span><span class="sxs-lookup"><span data-stu-id="341d6-231">False</span></span>                                        |
| <span data-ttu-id="341d6-232">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="341d6-232">Is-Single-Valued</span></span>       | <span data-ttu-id="341d6-233">Vero</span><span class="sxs-lookup"><span data-stu-id="341d6-233">True</span></span>                                         |
| <span data-ttu-id="341d6-234">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="341d6-234">Is Indexed</span></span>             | <span data-ttu-id="341d6-235">Falso</span><span class="sxs-lookup"><span data-stu-id="341d6-235">False</span></span>                                        |
| <span data-ttu-id="341d6-236">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="341d6-236">In Global Catalog</span></span>      | <span data-ttu-id="341d6-237">Vero</span><span class="sxs-lookup"><span data-stu-id="341d6-237">True</span></span>                                         |
| <span data-ttu-id="341d6-238">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="341d6-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="341d6-239">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="341d6-239">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="341d6-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="341d6-240">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="341d6-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="341d6-241">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="341d6-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="341d6-242">Search-Flags</span></span>           | <span data-ttu-id="341d6-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="341d6-243">0x00000000</span></span>                                   |
| <span data-ttu-id="341d6-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="341d6-244">System-Flags</span></span>           | <span data-ttu-id="341d6-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="341d6-245">0x00000010</span></span>                                   |
| <span data-ttu-id="341d6-246">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="341d6-246">Classes used in</span></span>        | [<span data-ttu-id="341d6-247">**Coda MSMQ**</span><span class="sxs-lookup"><span data-stu-id="341d6-247">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



 

 





