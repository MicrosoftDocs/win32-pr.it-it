---
title: Attributo FRS-Time-Last-Command
description: Ora in cui è stato eseguito l'ultimo comando.
ms.assetid: 262d410b-406a-4d4f-91f3-9986e867a4a5
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo FRS-Time-Last-Command
- Schema AD dell'attributo fRSTimeLastCommand
topic_type:
- apiref
api_name:
- FRS-Time-Last-Command
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7c81979b060d8f452441406af062cb26b307311
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "106302910"
---
# <a name="frs-time-last-command-attribute"></a><span data-ttu-id="55f0b-105">Attributo FRS-Time-Last-Command</span><span class="sxs-lookup"><span data-stu-id="55f0b-105">FRS-Time-Last-Command attribute</span></span>

<span data-ttu-id="55f0b-106">Ora in cui è stato eseguito l'ultimo comando.</span><span class="sxs-lookup"><span data-stu-id="55f0b-106">The time in which the last command was executed.</span></span>



| <span data-ttu-id="55f0b-107">Voce</span><span class="sxs-lookup"><span data-stu-id="55f0b-107">Entry</span></span> | <span data-ttu-id="55f0b-108">Valore</span><span class="sxs-lookup"><span data-stu-id="55f0b-108">Value</span></span> |
|-------------------|---------------------------------------------------------------|
| <span data-ttu-id="55f0b-109">CN</span><span class="sxs-lookup"><span data-stu-id="55f0b-109">CN</span></span>                | <span data-ttu-id="55f0b-110">FRS-ora-ultimo comando</span><span class="sxs-lookup"><span data-stu-id="55f0b-110">FRS-Time-Last-Command</span></span>                                         |
| <span data-ttu-id="55f0b-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="55f0b-111">Ldap-Display-Name</span></span> | <span data-ttu-id="55f0b-112">fRSTimeLastCommand</span><span class="sxs-lookup"><span data-stu-id="55f0b-112">fRSTimeLastCommand</span></span>                                            |
| <span data-ttu-id="55f0b-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="55f0b-113">Size</span></span>              | \-                                                            |
| <span data-ttu-id="55f0b-114">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="55f0b-114">Update Privilege</span></span>  | \-                                                            |
| <span data-ttu-id="55f0b-115">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="55f0b-115">Update Frequency</span></span>  | \-                                                            |
| <span data-ttu-id="55f0b-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="55f0b-116">Attribute-Id</span></span>      | <span data-ttu-id="55f0b-117">1.2.840.113556.1.4.880</span><span class="sxs-lookup"><span data-stu-id="55f0b-117">1.2.840.113556.1.4.880</span></span>                                        |
| <span data-ttu-id="55f0b-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="55f0b-118">System-Id-Guid</span></span>    | <span data-ttu-id="55f0b-119">2a132583-9373-11d1-aebc-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="55f0b-119">2a132583-9373-11d1-aebc-0000f80367c1</span></span>                          |
| <span data-ttu-id="55f0b-120">Sintassi</span><span class="sxs-lookup"><span data-stu-id="55f0b-120">Syntax</span></span>            | [<span data-ttu-id="55f0b-121">**String(Generalized-Time)**</span><span class="sxs-lookup"><span data-stu-id="55f0b-121">**String(Generalized-Time)**</span></span>](s-string-generalized-time.md) |



## <a name="implementations"></a><span data-ttu-id="55f0b-122">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="55f0b-122">Implementations</span></span>

-   [<span data-ttu-id="55f0b-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="55f0b-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="55f0b-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="55f0b-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="55f0b-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="55f0b-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="55f0b-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="55f0b-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="55f0b-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="55f0b-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="55f0b-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="55f0b-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="55f0b-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="55f0b-129">Windows 2000 Server</span></span>



| <span data-ttu-id="55f0b-130">Voce</span><span class="sxs-lookup"><span data-stu-id="55f0b-130">Entry</span></span> | <span data-ttu-id="55f0b-131">Valore</span><span class="sxs-lookup"><span data-stu-id="55f0b-131">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="55f0b-132">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="55f0b-132">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="55f0b-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="55f0b-133">MAPI-Id</span></span>                | \-                                                       |
| <span data-ttu-id="55f0b-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="55f0b-134">System-Only</span></span>            | <span data-ttu-id="55f0b-135">Falso</span><span class="sxs-lookup"><span data-stu-id="55f0b-135">False</span></span>                                                    |
| <span data-ttu-id="55f0b-136">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="55f0b-136">Is-Single-Valued</span></span>       | <span data-ttu-id="55f0b-137">Vero</span><span class="sxs-lookup"><span data-stu-id="55f0b-137">True</span></span>                                                     |
| <span data-ttu-id="55f0b-138">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="55f0b-138">Is Indexed</span></span>             | <span data-ttu-id="55f0b-139">Falso</span><span class="sxs-lookup"><span data-stu-id="55f0b-139">False</span></span>                                                    |
| <span data-ttu-id="55f0b-140">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="55f0b-140">In Global Catalog</span></span>      | <span data-ttu-id="55f0b-141">Falso</span><span class="sxs-lookup"><span data-stu-id="55f0b-141">False</span></span>                                                    |
| <span data-ttu-id="55f0b-142">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="55f0b-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="55f0b-143">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="55f0b-143">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="55f0b-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="55f0b-144">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="55f0b-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="55f0b-145">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="55f0b-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="55f0b-146">Search-Flags</span></span>           | <span data-ttu-id="55f0b-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="55f0b-147">0x00000000</span></span>                                               |
| <span data-ttu-id="55f0b-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="55f0b-148">System-Flags</span></span>           | <span data-ttu-id="55f0b-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="55f0b-149">0x00000010</span></span>                                               |
| <span data-ttu-id="55f0b-150">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="55f0b-150">Classes used in</span></span>        | [<span data-ttu-id="55f0b-151">**Sottoscrittore NTFRS**</span><span class="sxs-lookup"><span data-stu-id="55f0b-151">**NTFRS-Subscriber**</span></span>](c-ntfrssubscriber.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="55f0b-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="55f0b-152">Windows Server 2003</span></span>



| <span data-ttu-id="55f0b-153">Voce</span><span class="sxs-lookup"><span data-stu-id="55f0b-153">Entry</span></span> | <span data-ttu-id="55f0b-154">Valore</span><span class="sxs-lookup"><span data-stu-id="55f0b-154">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="55f0b-155">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="55f0b-155">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="55f0b-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="55f0b-156">MAPI-Id</span></span>                | \-                                                       |
| <span data-ttu-id="55f0b-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="55f0b-157">System-Only</span></span>            | <span data-ttu-id="55f0b-158">Falso</span><span class="sxs-lookup"><span data-stu-id="55f0b-158">False</span></span>                                                    |
| <span data-ttu-id="55f0b-159">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="55f0b-159">Is-Single-Valued</span></span>       | <span data-ttu-id="55f0b-160">Vero</span><span class="sxs-lookup"><span data-stu-id="55f0b-160">True</span></span>                                                     |
| <span data-ttu-id="55f0b-161">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="55f0b-161">Is Indexed</span></span>             | <span data-ttu-id="55f0b-162">Falso</span><span class="sxs-lookup"><span data-stu-id="55f0b-162">False</span></span>                                                    |
| <span data-ttu-id="55f0b-163">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="55f0b-163">In Global Catalog</span></span>      | <span data-ttu-id="55f0b-164">Falso</span><span class="sxs-lookup"><span data-stu-id="55f0b-164">False</span></span>                                                    |
| <span data-ttu-id="55f0b-165">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="55f0b-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="55f0b-166">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="55f0b-166">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="55f0b-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="55f0b-167">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="55f0b-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="55f0b-168">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="55f0b-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="55f0b-169">Search-Flags</span></span>           | <span data-ttu-id="55f0b-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="55f0b-170">0x00000000</span></span>                                               |
| <span data-ttu-id="55f0b-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="55f0b-171">System-Flags</span></span>           | <span data-ttu-id="55f0b-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="55f0b-172">0x00000010</span></span>                                               |
| <span data-ttu-id="55f0b-173">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="55f0b-173">Classes used in</span></span>        | [<span data-ttu-id="55f0b-174">**Sottoscrittore NTFRS**</span><span class="sxs-lookup"><span data-stu-id="55f0b-174">**NTFRS-Subscriber**</span></span>](c-ntfrssubscriber.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="55f0b-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="55f0b-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="55f0b-176">Voce</span><span class="sxs-lookup"><span data-stu-id="55f0b-176">Entry</span></span> | <span data-ttu-id="55f0b-177">Valore</span><span class="sxs-lookup"><span data-stu-id="55f0b-177">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="55f0b-178">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="55f0b-178">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="55f0b-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="55f0b-179">MAPI-Id</span></span>                | \-                                                       |
| <span data-ttu-id="55f0b-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="55f0b-180">System-Only</span></span>            | <span data-ttu-id="55f0b-181">Falso</span><span class="sxs-lookup"><span data-stu-id="55f0b-181">False</span></span>                                                    |
| <span data-ttu-id="55f0b-182">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="55f0b-182">Is-Single-Valued</span></span>       | <span data-ttu-id="55f0b-183">Vero</span><span class="sxs-lookup"><span data-stu-id="55f0b-183">True</span></span>                                                     |
| <span data-ttu-id="55f0b-184">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="55f0b-184">Is Indexed</span></span>             | <span data-ttu-id="55f0b-185">Falso</span><span class="sxs-lookup"><span data-stu-id="55f0b-185">False</span></span>                                                    |
| <span data-ttu-id="55f0b-186">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="55f0b-186">In Global Catalog</span></span>      | <span data-ttu-id="55f0b-187">Falso</span><span class="sxs-lookup"><span data-stu-id="55f0b-187">False</span></span>                                                    |
| <span data-ttu-id="55f0b-188">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="55f0b-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="55f0b-189">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="55f0b-189">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="55f0b-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="55f0b-190">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="55f0b-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="55f0b-191">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="55f0b-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="55f0b-192">Search-Flags</span></span>           | <span data-ttu-id="55f0b-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="55f0b-193">0x00000000</span></span>                                               |
| <span data-ttu-id="55f0b-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="55f0b-194">System-Flags</span></span>           | <span data-ttu-id="55f0b-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="55f0b-195">0x00000010</span></span>                                               |
| <span data-ttu-id="55f0b-196">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="55f0b-196">Classes used in</span></span>        | [<span data-ttu-id="55f0b-197">**Sottoscrittore NTFRS**</span><span class="sxs-lookup"><span data-stu-id="55f0b-197">**NTFRS-Subscriber**</span></span>](c-ntfrssubscriber.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="55f0b-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="55f0b-198">Windows Server 2008</span></span>



| <span data-ttu-id="55f0b-199">Voce</span><span class="sxs-lookup"><span data-stu-id="55f0b-199">Entry</span></span> | <span data-ttu-id="55f0b-200">Valore</span><span class="sxs-lookup"><span data-stu-id="55f0b-200">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="55f0b-201">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="55f0b-201">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="55f0b-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="55f0b-202">MAPI-Id</span></span>                | \-                                                       |
| <span data-ttu-id="55f0b-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="55f0b-203">System-Only</span></span>            | <span data-ttu-id="55f0b-204">Falso</span><span class="sxs-lookup"><span data-stu-id="55f0b-204">False</span></span>                                                    |
| <span data-ttu-id="55f0b-205">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="55f0b-205">Is-Single-Valued</span></span>       | <span data-ttu-id="55f0b-206">Vero</span><span class="sxs-lookup"><span data-stu-id="55f0b-206">True</span></span>                                                     |
| <span data-ttu-id="55f0b-207">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="55f0b-207">Is Indexed</span></span>             | <span data-ttu-id="55f0b-208">Falso</span><span class="sxs-lookup"><span data-stu-id="55f0b-208">False</span></span>                                                    |
| <span data-ttu-id="55f0b-209">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="55f0b-209">In Global Catalog</span></span>      | <span data-ttu-id="55f0b-210">Falso</span><span class="sxs-lookup"><span data-stu-id="55f0b-210">False</span></span>                                                    |
| <span data-ttu-id="55f0b-211">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="55f0b-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="55f0b-212">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="55f0b-212">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="55f0b-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="55f0b-213">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="55f0b-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="55f0b-214">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="55f0b-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="55f0b-215">Search-Flags</span></span>           | <span data-ttu-id="55f0b-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="55f0b-216">0x00000000</span></span>                                               |
| <span data-ttu-id="55f0b-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="55f0b-217">System-Flags</span></span>           | <span data-ttu-id="55f0b-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="55f0b-218">0x00000010</span></span>                                               |
| <span data-ttu-id="55f0b-219">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="55f0b-219">Classes used in</span></span>        | [<span data-ttu-id="55f0b-220">**Sottoscrittore NTFRS**</span><span class="sxs-lookup"><span data-stu-id="55f0b-220">**NTFRS-Subscriber**</span></span>](c-ntfrssubscriber.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="55f0b-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="55f0b-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="55f0b-222">Voce</span><span class="sxs-lookup"><span data-stu-id="55f0b-222">Entry</span></span> | <span data-ttu-id="55f0b-223">Valore</span><span class="sxs-lookup"><span data-stu-id="55f0b-223">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="55f0b-224">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="55f0b-224">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="55f0b-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="55f0b-225">MAPI-Id</span></span>                | \-                                                       |
| <span data-ttu-id="55f0b-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="55f0b-226">System-Only</span></span>            | <span data-ttu-id="55f0b-227">Falso</span><span class="sxs-lookup"><span data-stu-id="55f0b-227">False</span></span>                                                    |
| <span data-ttu-id="55f0b-228">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="55f0b-228">Is-Single-Valued</span></span>       | <span data-ttu-id="55f0b-229">Vero</span><span class="sxs-lookup"><span data-stu-id="55f0b-229">True</span></span>                                                     |
| <span data-ttu-id="55f0b-230">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="55f0b-230">Is Indexed</span></span>             | <span data-ttu-id="55f0b-231">Falso</span><span class="sxs-lookup"><span data-stu-id="55f0b-231">False</span></span>                                                    |
| <span data-ttu-id="55f0b-232">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="55f0b-232">In Global Catalog</span></span>      | <span data-ttu-id="55f0b-233">Falso</span><span class="sxs-lookup"><span data-stu-id="55f0b-233">False</span></span>                                                    |
| <span data-ttu-id="55f0b-234">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="55f0b-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="55f0b-235">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="55f0b-235">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="55f0b-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="55f0b-236">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="55f0b-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="55f0b-237">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="55f0b-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="55f0b-238">Search-Flags</span></span>           | <span data-ttu-id="55f0b-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="55f0b-239">0x00000000</span></span>                                               |
| <span data-ttu-id="55f0b-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="55f0b-240">System-Flags</span></span>           | <span data-ttu-id="55f0b-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="55f0b-241">0x00000010</span></span>                                               |
| <span data-ttu-id="55f0b-242">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="55f0b-242">Classes used in</span></span>        | [<span data-ttu-id="55f0b-243">**Sottoscrittore NTFRS**</span><span class="sxs-lookup"><span data-stu-id="55f0b-243">**NTFRS-Subscriber**</span></span>](c-ntfrssubscriber.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="55f0b-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="55f0b-244">Windows Server 2012</span></span>



| <span data-ttu-id="55f0b-245">Voce</span><span class="sxs-lookup"><span data-stu-id="55f0b-245">Entry</span></span> | <span data-ttu-id="55f0b-246">Valore</span><span class="sxs-lookup"><span data-stu-id="55f0b-246">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="55f0b-247">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="55f0b-247">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="55f0b-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="55f0b-248">MAPI-Id</span></span>                | \-                                                       |
| <span data-ttu-id="55f0b-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="55f0b-249">System-Only</span></span>            | <span data-ttu-id="55f0b-250">Falso</span><span class="sxs-lookup"><span data-stu-id="55f0b-250">False</span></span>                                                    |
| <span data-ttu-id="55f0b-251">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="55f0b-251">Is-Single-Valued</span></span>       | <span data-ttu-id="55f0b-252">Vero</span><span class="sxs-lookup"><span data-stu-id="55f0b-252">True</span></span>                                                     |
| <span data-ttu-id="55f0b-253">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="55f0b-253">Is Indexed</span></span>             | <span data-ttu-id="55f0b-254">Falso</span><span class="sxs-lookup"><span data-stu-id="55f0b-254">False</span></span>                                                    |
| <span data-ttu-id="55f0b-255">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="55f0b-255">In Global Catalog</span></span>      | <span data-ttu-id="55f0b-256">Falso</span><span class="sxs-lookup"><span data-stu-id="55f0b-256">False</span></span>                                                    |
| <span data-ttu-id="55f0b-257">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="55f0b-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="55f0b-258">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="55f0b-258">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="55f0b-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="55f0b-259">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="55f0b-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="55f0b-260">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="55f0b-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="55f0b-261">Search-Flags</span></span>           | <span data-ttu-id="55f0b-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="55f0b-262">0x00000000</span></span>                                               |
| <span data-ttu-id="55f0b-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="55f0b-263">System-Flags</span></span>           | <span data-ttu-id="55f0b-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="55f0b-264">0x00000010</span></span>                                               |
| <span data-ttu-id="55f0b-265">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="55f0b-265">Classes used in</span></span>        | [<span data-ttu-id="55f0b-266">**Sottoscrittore NTFRS**</span><span class="sxs-lookup"><span data-stu-id="55f0b-266">**NTFRS-Subscriber**</span></span>](c-ntfrssubscriber.md)<br/> |



 

 





