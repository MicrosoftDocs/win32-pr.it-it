---
title: FRS-attributo filtro file
description: Elenco di estensioni di file escluse dalla replica file.
ms.assetid: 094a393a-9e1a-4da8-a38a-161102f164fd
ms.tgt_platform: multiple
keywords:
- FRS-file-filtro attributo AD schema
- Schema AD dell'attributo fRSFileFilter
topic_type:
- apiref
api_name:
- FRS-File-Filter
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 234cf7d6e56e84c2ed9578fc56036e581a2f0ad2
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "106302919"
---
# <a name="frs-file-filter-attribute"></a><span data-ttu-id="bbe3e-105">FRS-attributo filtro file</span><span class="sxs-lookup"><span data-stu-id="bbe3e-105">FRS-File-Filter attribute</span></span>

<span data-ttu-id="bbe3e-106">Elenco di estensioni di file escluse dalla replica file.</span><span class="sxs-lookup"><span data-stu-id="bbe3e-106">A list of file name extensions excluded from file replication.</span></span>



| <span data-ttu-id="bbe3e-107">Voce</span><span class="sxs-lookup"><span data-stu-id="bbe3e-107">Entry</span></span> | <span data-ttu-id="bbe3e-108">Valore</span><span class="sxs-lookup"><span data-stu-id="bbe3e-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="bbe3e-109">CN</span><span class="sxs-lookup"><span data-stu-id="bbe3e-109">CN</span></span>                | <span data-ttu-id="bbe3e-110">FRS-filtro file</span><span class="sxs-lookup"><span data-stu-id="bbe3e-110">FRS-File-Filter</span></span>                             |
| <span data-ttu-id="bbe3e-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="bbe3e-111">Ldap-Display-Name</span></span> | <span data-ttu-id="bbe3e-112">fRSFileFilter</span><span class="sxs-lookup"><span data-stu-id="bbe3e-112">fRSFileFilter</span></span>                               |
| <span data-ttu-id="bbe3e-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="bbe3e-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="bbe3e-114">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="bbe3e-114">Update Privilege</span></span>  | <span data-ttu-id="bbe3e-115">Amministratore di dominio</span><span class="sxs-lookup"><span data-stu-id="bbe3e-115">Domain administrator</span></span>                        |
| <span data-ttu-id="bbe3e-116">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="bbe3e-116">Update Frequency</span></span>  | <span data-ttu-id="bbe3e-117">Quando la replica è impostata.</span><span class="sxs-lookup"><span data-stu-id="bbe3e-117">When replication is setup.</span></span>                  |
| <span data-ttu-id="bbe3e-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="bbe3e-118">Attribute-Id</span></span>      | <span data-ttu-id="bbe3e-119">1.2.840.113556.1.4.483</span><span class="sxs-lookup"><span data-stu-id="bbe3e-119">1.2.840.113556.1.4.483</span></span>                      |
| <span data-ttu-id="bbe3e-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="bbe3e-120">System-Id-Guid</span></span>    | <span data-ttu-id="bbe3e-121">1be8f170-a9ff-11d0-afe2-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="bbe3e-121">1be8f170-a9ff-11d0-afe2-00c04fd930c9</span></span>        |
| <span data-ttu-id="bbe3e-122">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bbe3e-122">Syntax</span></span>            | [<span data-ttu-id="bbe3e-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="bbe3e-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="bbe3e-124">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="bbe3e-124">Implementations</span></span>

-   [<span data-ttu-id="bbe3e-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="bbe3e-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="bbe3e-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="bbe3e-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="bbe3e-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="bbe3e-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="bbe3e-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="bbe3e-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="bbe3e-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="bbe3e-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="bbe3e-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="bbe3e-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="bbe3e-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="bbe3e-131">Windows 2000 Server</span></span>



| <span data-ttu-id="bbe3e-132">Voce</span><span class="sxs-lookup"><span data-stu-id="bbe3e-132">Entry</span></span> | <span data-ttu-id="bbe3e-133">Valore</span><span class="sxs-lookup"><span data-stu-id="bbe3e-133">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="bbe3e-134">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="bbe3e-134">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="bbe3e-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bbe3e-135">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="bbe3e-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="bbe3e-136">System-Only</span></span>            | <span data-ttu-id="bbe3e-137">Falso</span><span class="sxs-lookup"><span data-stu-id="bbe3e-137">False</span></span>                                                     |
| <span data-ttu-id="bbe3e-138">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="bbe3e-138">Is-Single-Valued</span></span>       | <span data-ttu-id="bbe3e-139">Vero</span><span class="sxs-lookup"><span data-stu-id="bbe3e-139">True</span></span>                                                      |
| <span data-ttu-id="bbe3e-140">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="bbe3e-140">Is Indexed</span></span>             | <span data-ttu-id="bbe3e-141">Falso</span><span class="sxs-lookup"><span data-stu-id="bbe3e-141">False</span></span>                                                     |
| <span data-ttu-id="bbe3e-142">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="bbe3e-142">In Global Catalog</span></span>      | <span data-ttu-id="bbe3e-143">Falso</span><span class="sxs-lookup"><span data-stu-id="bbe3e-143">False</span></span>                                                     |
| <span data-ttu-id="bbe3e-144">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="bbe3e-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="bbe3e-145">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="bbe3e-145">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="bbe3e-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bbe3e-146">Range-Lower</span></span>            | <span data-ttu-id="bbe3e-147">0</span><span class="sxs-lookup"><span data-stu-id="bbe3e-147">0</span></span>                                                         |
| <span data-ttu-id="bbe3e-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bbe3e-148">Range-Upper</span></span>            | <span data-ttu-id="bbe3e-149">2048</span><span class="sxs-lookup"><span data-stu-id="bbe3e-149">2048</span></span>                                                      |
| <span data-ttu-id="bbe3e-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bbe3e-150">Search-Flags</span></span>           | <span data-ttu-id="bbe3e-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bbe3e-151">0x00000000</span></span>                                                |
| <span data-ttu-id="bbe3e-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bbe3e-152">System-Flags</span></span>           | <span data-ttu-id="bbe3e-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bbe3e-153">0x00000010</span></span>                                                |
| <span data-ttu-id="bbe3e-154">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="bbe3e-154">Classes used in</span></span>        | [<span data-ttu-id="bbe3e-155">**NTFRS-set di repliche**</span><span class="sxs-lookup"><span data-stu-id="bbe3e-155">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="bbe3e-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="bbe3e-156">Windows Server 2003</span></span>



| <span data-ttu-id="bbe3e-157">Voce</span><span class="sxs-lookup"><span data-stu-id="bbe3e-157">Entry</span></span> | <span data-ttu-id="bbe3e-158">Valore</span><span class="sxs-lookup"><span data-stu-id="bbe3e-158">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="bbe3e-159">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="bbe3e-159">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="bbe3e-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bbe3e-160">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="bbe3e-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="bbe3e-161">System-Only</span></span>            | <span data-ttu-id="bbe3e-162">Falso</span><span class="sxs-lookup"><span data-stu-id="bbe3e-162">False</span></span>                                                     |
| <span data-ttu-id="bbe3e-163">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="bbe3e-163">Is-Single-Valued</span></span>       | <span data-ttu-id="bbe3e-164">Vero</span><span class="sxs-lookup"><span data-stu-id="bbe3e-164">True</span></span>                                                      |
| <span data-ttu-id="bbe3e-165">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="bbe3e-165">Is Indexed</span></span>             | <span data-ttu-id="bbe3e-166">Falso</span><span class="sxs-lookup"><span data-stu-id="bbe3e-166">False</span></span>                                                     |
| <span data-ttu-id="bbe3e-167">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="bbe3e-167">In Global Catalog</span></span>      | <span data-ttu-id="bbe3e-168">Falso</span><span class="sxs-lookup"><span data-stu-id="bbe3e-168">False</span></span>                                                     |
| <span data-ttu-id="bbe3e-169">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="bbe3e-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="bbe3e-170">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="bbe3e-170">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="bbe3e-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bbe3e-171">Range-Lower</span></span>            | <span data-ttu-id="bbe3e-172">0</span><span class="sxs-lookup"><span data-stu-id="bbe3e-172">0</span></span>                                                         |
| <span data-ttu-id="bbe3e-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bbe3e-173">Range-Upper</span></span>            | <span data-ttu-id="bbe3e-174">2048</span><span class="sxs-lookup"><span data-stu-id="bbe3e-174">2048</span></span>                                                      |
| <span data-ttu-id="bbe3e-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bbe3e-175">Search-Flags</span></span>           | <span data-ttu-id="bbe3e-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bbe3e-176">0x00000000</span></span>                                                |
| <span data-ttu-id="bbe3e-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bbe3e-177">System-Flags</span></span>           | <span data-ttu-id="bbe3e-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bbe3e-178">0x00000010</span></span>                                                |
| <span data-ttu-id="bbe3e-179">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="bbe3e-179">Classes used in</span></span>        | [<span data-ttu-id="bbe3e-180">**NTFRS-set di repliche**</span><span class="sxs-lookup"><span data-stu-id="bbe3e-180">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="bbe3e-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="bbe3e-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="bbe3e-182">Voce</span><span class="sxs-lookup"><span data-stu-id="bbe3e-182">Entry</span></span> | <span data-ttu-id="bbe3e-183">Valore</span><span class="sxs-lookup"><span data-stu-id="bbe3e-183">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="bbe3e-184">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="bbe3e-184">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="bbe3e-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bbe3e-185">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="bbe3e-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="bbe3e-186">System-Only</span></span>            | <span data-ttu-id="bbe3e-187">Falso</span><span class="sxs-lookup"><span data-stu-id="bbe3e-187">False</span></span>                                                     |
| <span data-ttu-id="bbe3e-188">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="bbe3e-188">Is-Single-Valued</span></span>       | <span data-ttu-id="bbe3e-189">Vero</span><span class="sxs-lookup"><span data-stu-id="bbe3e-189">True</span></span>                                                      |
| <span data-ttu-id="bbe3e-190">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="bbe3e-190">Is Indexed</span></span>             | <span data-ttu-id="bbe3e-191">Falso</span><span class="sxs-lookup"><span data-stu-id="bbe3e-191">False</span></span>                                                     |
| <span data-ttu-id="bbe3e-192">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="bbe3e-192">In Global Catalog</span></span>      | <span data-ttu-id="bbe3e-193">Falso</span><span class="sxs-lookup"><span data-stu-id="bbe3e-193">False</span></span>                                                     |
| <span data-ttu-id="bbe3e-194">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="bbe3e-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="bbe3e-195">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="bbe3e-195">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="bbe3e-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bbe3e-196">Range-Lower</span></span>            | <span data-ttu-id="bbe3e-197">0</span><span class="sxs-lookup"><span data-stu-id="bbe3e-197">0</span></span>                                                         |
| <span data-ttu-id="bbe3e-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bbe3e-198">Range-Upper</span></span>            | <span data-ttu-id="bbe3e-199">2048</span><span class="sxs-lookup"><span data-stu-id="bbe3e-199">2048</span></span>                                                      |
| <span data-ttu-id="bbe3e-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bbe3e-200">Search-Flags</span></span>           | <span data-ttu-id="bbe3e-201">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bbe3e-201">0x00000000</span></span>                                                |
| <span data-ttu-id="bbe3e-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bbe3e-202">System-Flags</span></span>           | <span data-ttu-id="bbe3e-203">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bbe3e-203">0x00000010</span></span>                                                |
| <span data-ttu-id="bbe3e-204">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="bbe3e-204">Classes used in</span></span>        | [<span data-ttu-id="bbe3e-205">**NTFRS-set di repliche**</span><span class="sxs-lookup"><span data-stu-id="bbe3e-205">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="bbe3e-206">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bbe3e-206">Windows Server 2008</span></span>



| <span data-ttu-id="bbe3e-207">Voce</span><span class="sxs-lookup"><span data-stu-id="bbe3e-207">Entry</span></span> | <span data-ttu-id="bbe3e-208">Valore</span><span class="sxs-lookup"><span data-stu-id="bbe3e-208">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="bbe3e-209">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="bbe3e-209">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="bbe3e-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bbe3e-210">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="bbe3e-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="bbe3e-211">System-Only</span></span>            | <span data-ttu-id="bbe3e-212">Falso</span><span class="sxs-lookup"><span data-stu-id="bbe3e-212">False</span></span>                                                     |
| <span data-ttu-id="bbe3e-213">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="bbe3e-213">Is-Single-Valued</span></span>       | <span data-ttu-id="bbe3e-214">Vero</span><span class="sxs-lookup"><span data-stu-id="bbe3e-214">True</span></span>                                                      |
| <span data-ttu-id="bbe3e-215">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="bbe3e-215">Is Indexed</span></span>             | <span data-ttu-id="bbe3e-216">Falso</span><span class="sxs-lookup"><span data-stu-id="bbe3e-216">False</span></span>                                                     |
| <span data-ttu-id="bbe3e-217">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="bbe3e-217">In Global Catalog</span></span>      | <span data-ttu-id="bbe3e-218">Falso</span><span class="sxs-lookup"><span data-stu-id="bbe3e-218">False</span></span>                                                     |
| <span data-ttu-id="bbe3e-219">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="bbe3e-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="bbe3e-220">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="bbe3e-220">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="bbe3e-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bbe3e-221">Range-Lower</span></span>            | <span data-ttu-id="bbe3e-222">0</span><span class="sxs-lookup"><span data-stu-id="bbe3e-222">0</span></span>                                                         |
| <span data-ttu-id="bbe3e-223">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bbe3e-223">Range-Upper</span></span>            | <span data-ttu-id="bbe3e-224">2048</span><span class="sxs-lookup"><span data-stu-id="bbe3e-224">2048</span></span>                                                      |
| <span data-ttu-id="bbe3e-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bbe3e-225">Search-Flags</span></span>           | <span data-ttu-id="bbe3e-226">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bbe3e-226">0x00000000</span></span>                                                |
| <span data-ttu-id="bbe3e-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bbe3e-227">System-Flags</span></span>           | <span data-ttu-id="bbe3e-228">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bbe3e-228">0x00000010</span></span>                                                |
| <span data-ttu-id="bbe3e-229">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="bbe3e-229">Classes used in</span></span>        | [<span data-ttu-id="bbe3e-230">**NTFRS-set di repliche**</span><span class="sxs-lookup"><span data-stu-id="bbe3e-230">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="bbe3e-231">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="bbe3e-231">Windows Server 2008 R2</span></span>



| <span data-ttu-id="bbe3e-232">Voce</span><span class="sxs-lookup"><span data-stu-id="bbe3e-232">Entry</span></span> | <span data-ttu-id="bbe3e-233">Valore</span><span class="sxs-lookup"><span data-stu-id="bbe3e-233">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="bbe3e-234">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="bbe3e-234">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="bbe3e-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bbe3e-235">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="bbe3e-236">System-Only</span><span class="sxs-lookup"><span data-stu-id="bbe3e-236">System-Only</span></span>            | <span data-ttu-id="bbe3e-237">Falso</span><span class="sxs-lookup"><span data-stu-id="bbe3e-237">False</span></span>                                                     |
| <span data-ttu-id="bbe3e-238">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="bbe3e-238">Is-Single-Valued</span></span>       | <span data-ttu-id="bbe3e-239">Vero</span><span class="sxs-lookup"><span data-stu-id="bbe3e-239">True</span></span>                                                      |
| <span data-ttu-id="bbe3e-240">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="bbe3e-240">Is Indexed</span></span>             | <span data-ttu-id="bbe3e-241">Falso</span><span class="sxs-lookup"><span data-stu-id="bbe3e-241">False</span></span>                                                     |
| <span data-ttu-id="bbe3e-242">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="bbe3e-242">In Global Catalog</span></span>      | <span data-ttu-id="bbe3e-243">Falso</span><span class="sxs-lookup"><span data-stu-id="bbe3e-243">False</span></span>                                                     |
| <span data-ttu-id="bbe3e-244">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="bbe3e-244">NT-Security-Descriptor</span></span> | <span data-ttu-id="bbe3e-245">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="bbe3e-245">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="bbe3e-246">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bbe3e-246">Range-Lower</span></span>            | <span data-ttu-id="bbe3e-247">0</span><span class="sxs-lookup"><span data-stu-id="bbe3e-247">0</span></span>                                                         |
| <span data-ttu-id="bbe3e-248">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bbe3e-248">Range-Upper</span></span>            | <span data-ttu-id="bbe3e-249">2048</span><span class="sxs-lookup"><span data-stu-id="bbe3e-249">2048</span></span>                                                      |
| <span data-ttu-id="bbe3e-250">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bbe3e-250">Search-Flags</span></span>           | <span data-ttu-id="bbe3e-251">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bbe3e-251">0x00000000</span></span>                                                |
| <span data-ttu-id="bbe3e-252">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bbe3e-252">System-Flags</span></span>           | <span data-ttu-id="bbe3e-253">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bbe3e-253">0x00000010</span></span>                                                |
| <span data-ttu-id="bbe3e-254">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="bbe3e-254">Classes used in</span></span>        | [<span data-ttu-id="bbe3e-255">**NTFRS-set di repliche**</span><span class="sxs-lookup"><span data-stu-id="bbe3e-255">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="bbe3e-256">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="bbe3e-256">Windows Server 2012</span></span>



| <span data-ttu-id="bbe3e-257">Voce</span><span class="sxs-lookup"><span data-stu-id="bbe3e-257">Entry</span></span> | <span data-ttu-id="bbe3e-258">Valore</span><span class="sxs-lookup"><span data-stu-id="bbe3e-258">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="bbe3e-259">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="bbe3e-259">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="bbe3e-260">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bbe3e-260">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="bbe3e-261">System-Only</span><span class="sxs-lookup"><span data-stu-id="bbe3e-261">System-Only</span></span>            | <span data-ttu-id="bbe3e-262">Falso</span><span class="sxs-lookup"><span data-stu-id="bbe3e-262">False</span></span>                                                     |
| <span data-ttu-id="bbe3e-263">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="bbe3e-263">Is-Single-Valued</span></span>       | <span data-ttu-id="bbe3e-264">Vero</span><span class="sxs-lookup"><span data-stu-id="bbe3e-264">True</span></span>                                                      |
| <span data-ttu-id="bbe3e-265">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="bbe3e-265">Is Indexed</span></span>             | <span data-ttu-id="bbe3e-266">Falso</span><span class="sxs-lookup"><span data-stu-id="bbe3e-266">False</span></span>                                                     |
| <span data-ttu-id="bbe3e-267">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="bbe3e-267">In Global Catalog</span></span>      | <span data-ttu-id="bbe3e-268">Falso</span><span class="sxs-lookup"><span data-stu-id="bbe3e-268">False</span></span>                                                     |
| <span data-ttu-id="bbe3e-269">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="bbe3e-269">NT-Security-Descriptor</span></span> | <span data-ttu-id="bbe3e-270">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="bbe3e-270">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="bbe3e-271">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bbe3e-271">Range-Lower</span></span>            | <span data-ttu-id="bbe3e-272">0</span><span class="sxs-lookup"><span data-stu-id="bbe3e-272">0</span></span>                                                         |
| <span data-ttu-id="bbe3e-273">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bbe3e-273">Range-Upper</span></span>            | <span data-ttu-id="bbe3e-274">2048</span><span class="sxs-lookup"><span data-stu-id="bbe3e-274">2048</span></span>                                                      |
| <span data-ttu-id="bbe3e-275">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bbe3e-275">Search-Flags</span></span>           | <span data-ttu-id="bbe3e-276">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bbe3e-276">0x00000000</span></span>                                                |
| <span data-ttu-id="bbe3e-277">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bbe3e-277">System-Flags</span></span>           | <span data-ttu-id="bbe3e-278">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bbe3e-278">0x00000010</span></span>                                                |
| <span data-ttu-id="bbe3e-279">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="bbe3e-279">Classes used in</span></span>        | [<span data-ttu-id="bbe3e-280">**NTFRS-set di repliche**</span><span class="sxs-lookup"><span data-stu-id="bbe3e-280">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



 

 





