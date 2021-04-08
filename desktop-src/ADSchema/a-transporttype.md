---
title: Attributo Transport-Type
description: Nome distinto per un tipo di trasporto utilizzato per connettere i siti. Questo valore può puntare a un trasporto IP o SMTP.
ms.assetid: aed18e69-3118-4cb8-b959-829106602f95
ms.tgt_platform: multiple
keywords:
- Schema AD Transport-Type attribute
- Schema AD dell'attributo transportType
topic_type:
- apiref
api_name:
- Transport-Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a28c68347deb83d52b78564688a563431609fb81
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103875129"
---
# <a name="transport-type-attribute"></a><span data-ttu-id="d2211-106">Attributo Transport-Type</span><span class="sxs-lookup"><span data-stu-id="d2211-106">Transport-Type attribute</span></span>

<span data-ttu-id="d2211-107">Nome distinto per un tipo di trasporto utilizzato per connettere i siti.</span><span class="sxs-lookup"><span data-stu-id="d2211-107">The distinguished name for a type of transport being used to connect sites together.</span></span> <span data-ttu-id="d2211-108">Questo valore può puntare a un trasporto IP o SMTP.</span><span class="sxs-lookup"><span data-stu-id="d2211-108">This value can point to an IP or SMTP transport.</span></span>



| <span data-ttu-id="d2211-109">Voce</span><span class="sxs-lookup"><span data-stu-id="d2211-109">Entry</span></span> | <span data-ttu-id="d2211-110">Valore</span><span class="sxs-lookup"><span data-stu-id="d2211-110">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="d2211-111">CN</span><span class="sxs-lookup"><span data-stu-id="d2211-111">CN</span></span>                | <span data-ttu-id="d2211-112">Transport-Type</span><span class="sxs-lookup"><span data-stu-id="d2211-112">Transport-Type</span></span>                          |
| <span data-ttu-id="d2211-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="d2211-113">Ldap-Display-Name</span></span> | <span data-ttu-id="d2211-114">transportType</span><span class="sxs-lookup"><span data-stu-id="d2211-114">transportType</span></span>                           |
| <span data-ttu-id="d2211-115">Dimensione</span><span class="sxs-lookup"><span data-stu-id="d2211-115">Size</span></span>              | \-                                      |
| <span data-ttu-id="d2211-116">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="d2211-116">Update Privilege</span></span>  | <span data-ttu-id="d2211-117">Questo valore viene impostato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="d2211-117">This value is set by the system.</span></span>        |
| <span data-ttu-id="d2211-118">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="d2211-118">Update Frequency</span></span>  | <span data-ttu-id="d2211-119">Quando si connettono i siti.</span><span class="sxs-lookup"><span data-stu-id="d2211-119">When connecting sites.</span></span>                  |
| <span data-ttu-id="d2211-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="d2211-120">Attribute-Id</span></span>      | <span data-ttu-id="d2211-121">1.2.840.113556.1.4.791</span><span class="sxs-lookup"><span data-stu-id="d2211-121">1.2.840.113556.1.4.791</span></span>                  |
| <span data-ttu-id="d2211-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="d2211-122">System-Id-Guid</span></span>    | <span data-ttu-id="d2211-123">26d97374-6070-11d1-a9c6-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="d2211-123">26d97374-6070-11d1-a9c6-0000f80367c1</span></span>    |
| <span data-ttu-id="d2211-124">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d2211-124">Syntax</span></span>            | [<span data-ttu-id="d2211-125">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="d2211-125">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="d2211-126">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="d2211-126">Implementations</span></span>

-   [<span data-ttu-id="d2211-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="d2211-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="d2211-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="d2211-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="d2211-129">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="d2211-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="d2211-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="d2211-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="d2211-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="d2211-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="d2211-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="d2211-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="d2211-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="d2211-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="d2211-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d2211-134">Windows 2000 Server</span></span>



| <span data-ttu-id="d2211-135">Voce</span><span class="sxs-lookup"><span data-stu-id="d2211-135">Entry</span></span> | <span data-ttu-id="d2211-136">Valore</span><span class="sxs-lookup"><span data-stu-id="d2211-136">Value</span></span> |
|------------------------|--------------------------------------------------------|
| <span data-ttu-id="d2211-137">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="d2211-137">Link-Id</span></span>                | \-                                                     |
| <span data-ttu-id="d2211-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d2211-138">MAPI-Id</span></span>                | \-                                                     |
| <span data-ttu-id="d2211-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="d2211-139">System-Only</span></span>            | <span data-ttu-id="d2211-140">Falso</span><span class="sxs-lookup"><span data-stu-id="d2211-140">False</span></span>                                                  |
| <span data-ttu-id="d2211-141">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="d2211-141">Is-Single-Valued</span></span>       | <span data-ttu-id="d2211-142">Vero</span><span class="sxs-lookup"><span data-stu-id="d2211-142">True</span></span>                                                   |
| <span data-ttu-id="d2211-143">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="d2211-143">Is Indexed</span></span>             | <span data-ttu-id="d2211-144">Falso</span><span class="sxs-lookup"><span data-stu-id="d2211-144">False</span></span>                                                  |
| <span data-ttu-id="d2211-145">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="d2211-145">In Global Catalog</span></span>      | <span data-ttu-id="d2211-146">Falso</span><span class="sxs-lookup"><span data-stu-id="d2211-146">False</span></span>                                                  |
| <span data-ttu-id="d2211-147">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="d2211-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="d2211-148">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="d2211-148">O:BAG:BAD:S:</span></span>                                           |
| <span data-ttu-id="d2211-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d2211-149">Range-Lower</span></span>            | \-                                                     |
| <span data-ttu-id="d2211-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d2211-150">Range-Upper</span></span>            | \-                                                     |
| <span data-ttu-id="d2211-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d2211-151">Search-Flags</span></span>           | <span data-ttu-id="d2211-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d2211-152">0x00000000</span></span>                                             |
| <span data-ttu-id="d2211-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d2211-153">System-Flags</span></span>           | <span data-ttu-id="d2211-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d2211-154">0x00000010</span></span>                                             |
| <span data-ttu-id="d2211-155">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="d2211-155">Classes used in</span></span>        | [<span data-ttu-id="d2211-156">**NTDS-connessione**</span><span class="sxs-lookup"><span data-stu-id="d2211-156">**NTDS-Connection**</span></span>](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="d2211-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d2211-157">Windows Server 2003</span></span>



| <span data-ttu-id="d2211-158">Voce</span><span class="sxs-lookup"><span data-stu-id="d2211-158">Entry</span></span> | <span data-ttu-id="d2211-159">Valore</span><span class="sxs-lookup"><span data-stu-id="d2211-159">Value</span></span> |
|------------------------|--------------------------------------------------------|
| <span data-ttu-id="d2211-160">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="d2211-160">Link-Id</span></span>                | \-                                                     |
| <span data-ttu-id="d2211-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d2211-161">MAPI-Id</span></span>                | \-                                                     |
| <span data-ttu-id="d2211-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="d2211-162">System-Only</span></span>            | <span data-ttu-id="d2211-163">Falso</span><span class="sxs-lookup"><span data-stu-id="d2211-163">False</span></span>                                                  |
| <span data-ttu-id="d2211-164">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="d2211-164">Is-Single-Valued</span></span>       | <span data-ttu-id="d2211-165">Vero</span><span class="sxs-lookup"><span data-stu-id="d2211-165">True</span></span>                                                   |
| <span data-ttu-id="d2211-166">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="d2211-166">Is Indexed</span></span>             | <span data-ttu-id="d2211-167">Falso</span><span class="sxs-lookup"><span data-stu-id="d2211-167">False</span></span>                                                  |
| <span data-ttu-id="d2211-168">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="d2211-168">In Global Catalog</span></span>      | <span data-ttu-id="d2211-169">Falso</span><span class="sxs-lookup"><span data-stu-id="d2211-169">False</span></span>                                                  |
| <span data-ttu-id="d2211-170">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="d2211-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="d2211-171">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="d2211-171">O:BAG:BAD:S:</span></span>                                           |
| <span data-ttu-id="d2211-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d2211-172">Range-Lower</span></span>            | \-                                                     |
| <span data-ttu-id="d2211-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d2211-173">Range-Upper</span></span>            | \-                                                     |
| <span data-ttu-id="d2211-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d2211-174">Search-Flags</span></span>           | <span data-ttu-id="d2211-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d2211-175">0x00000000</span></span>                                             |
| <span data-ttu-id="d2211-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d2211-176">System-Flags</span></span>           | <span data-ttu-id="d2211-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d2211-177">0x00000010</span></span>                                             |
| <span data-ttu-id="d2211-178">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="d2211-178">Classes used in</span></span>        | [<span data-ttu-id="d2211-179">**NTDS-connessione**</span><span class="sxs-lookup"><span data-stu-id="d2211-179">**NTDS-Connection**</span></span>](c-ntdsconnection.md)<br/> |



## <a name="adam"></a><span data-ttu-id="d2211-180">ADAM</span><span class="sxs-lookup"><span data-stu-id="d2211-180">ADAM</span></span>



| <span data-ttu-id="d2211-181">Voce</span><span class="sxs-lookup"><span data-stu-id="d2211-181">Entry</span></span> | <span data-ttu-id="d2211-182">Valore</span><span class="sxs-lookup"><span data-stu-id="d2211-182">Value</span></span> |
|------------------------|--------------------------------------------------------|
| <span data-ttu-id="d2211-183">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="d2211-183">Link-Id</span></span>                | \-                                                     |
| <span data-ttu-id="d2211-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d2211-184">MAPI-Id</span></span>                | \-                                                     |
| <span data-ttu-id="d2211-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="d2211-185">System-Only</span></span>            | <span data-ttu-id="d2211-186">Falso</span><span class="sxs-lookup"><span data-stu-id="d2211-186">False</span></span>                                                  |
| <span data-ttu-id="d2211-187">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="d2211-187">Is-Single-Valued</span></span>       | <span data-ttu-id="d2211-188">Vero</span><span class="sxs-lookup"><span data-stu-id="d2211-188">True</span></span>                                                   |
| <span data-ttu-id="d2211-189">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="d2211-189">Is Indexed</span></span>             | <span data-ttu-id="d2211-190">Falso</span><span class="sxs-lookup"><span data-stu-id="d2211-190">False</span></span>                                                  |
| <span data-ttu-id="d2211-191">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="d2211-191">In Global Catalog</span></span>      | <span data-ttu-id="d2211-192">Falso</span><span class="sxs-lookup"><span data-stu-id="d2211-192">False</span></span>                                                  |
| <span data-ttu-id="d2211-193">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="d2211-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="d2211-194">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="d2211-194">O:BAG:BAD:S:</span></span>                                           |
| <span data-ttu-id="d2211-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d2211-195">Range-Lower</span></span>            | \-                                                     |
| <span data-ttu-id="d2211-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d2211-196">Range-Upper</span></span>            | \-                                                     |
| <span data-ttu-id="d2211-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d2211-197">Search-Flags</span></span>           | <span data-ttu-id="d2211-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d2211-198">0x00000000</span></span>                                             |
| <span data-ttu-id="d2211-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d2211-199">System-Flags</span></span>           | <span data-ttu-id="d2211-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d2211-200">0x00000010</span></span>                                             |
| <span data-ttu-id="d2211-201">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="d2211-201">Classes used in</span></span>        | [<span data-ttu-id="d2211-202">**NTDS-connessione**</span><span class="sxs-lookup"><span data-stu-id="d2211-202">**NTDS-Connection**</span></span>](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="d2211-203">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="d2211-203">Windows Server 2003 R2</span></span>



| <span data-ttu-id="d2211-204">Voce</span><span class="sxs-lookup"><span data-stu-id="d2211-204">Entry</span></span> | <span data-ttu-id="d2211-205">Valore</span><span class="sxs-lookup"><span data-stu-id="d2211-205">Value</span></span> |
|------------------------|--------------------------------------------------------|
| <span data-ttu-id="d2211-206">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="d2211-206">Link-Id</span></span>                | \-                                                     |
| <span data-ttu-id="d2211-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d2211-207">MAPI-Id</span></span>                | \-                                                     |
| <span data-ttu-id="d2211-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="d2211-208">System-Only</span></span>            | <span data-ttu-id="d2211-209">Falso</span><span class="sxs-lookup"><span data-stu-id="d2211-209">False</span></span>                                                  |
| <span data-ttu-id="d2211-210">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="d2211-210">Is-Single-Valued</span></span>       | <span data-ttu-id="d2211-211">Vero</span><span class="sxs-lookup"><span data-stu-id="d2211-211">True</span></span>                                                   |
| <span data-ttu-id="d2211-212">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="d2211-212">Is Indexed</span></span>             | <span data-ttu-id="d2211-213">Falso</span><span class="sxs-lookup"><span data-stu-id="d2211-213">False</span></span>                                                  |
| <span data-ttu-id="d2211-214">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="d2211-214">In Global Catalog</span></span>      | <span data-ttu-id="d2211-215">Falso</span><span class="sxs-lookup"><span data-stu-id="d2211-215">False</span></span>                                                  |
| <span data-ttu-id="d2211-216">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="d2211-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="d2211-217">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="d2211-217">O:BAG:BAD:S:</span></span>                                           |
| <span data-ttu-id="d2211-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d2211-218">Range-Lower</span></span>            | \-                                                     |
| <span data-ttu-id="d2211-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d2211-219">Range-Upper</span></span>            | \-                                                     |
| <span data-ttu-id="d2211-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d2211-220">Search-Flags</span></span>           | <span data-ttu-id="d2211-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d2211-221">0x00000000</span></span>                                             |
| <span data-ttu-id="d2211-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d2211-222">System-Flags</span></span>           | <span data-ttu-id="d2211-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d2211-223">0x00000010</span></span>                                             |
| <span data-ttu-id="d2211-224">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="d2211-224">Classes used in</span></span>        | [<span data-ttu-id="d2211-225">**NTDS-connessione**</span><span class="sxs-lookup"><span data-stu-id="d2211-225">**NTDS-Connection**</span></span>](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="d2211-226">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d2211-226">Windows Server 2008</span></span>



| <span data-ttu-id="d2211-227">Voce</span><span class="sxs-lookup"><span data-stu-id="d2211-227">Entry</span></span> | <span data-ttu-id="d2211-228">Valore</span><span class="sxs-lookup"><span data-stu-id="d2211-228">Value</span></span> |
|------------------------|--------------------------------------------------------|
| <span data-ttu-id="d2211-229">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="d2211-229">Link-Id</span></span>                | \-                                                     |
| <span data-ttu-id="d2211-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d2211-230">MAPI-Id</span></span>                | \-                                                     |
| <span data-ttu-id="d2211-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="d2211-231">System-Only</span></span>            | <span data-ttu-id="d2211-232">Falso</span><span class="sxs-lookup"><span data-stu-id="d2211-232">False</span></span>                                                  |
| <span data-ttu-id="d2211-233">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="d2211-233">Is-Single-Valued</span></span>       | <span data-ttu-id="d2211-234">Vero</span><span class="sxs-lookup"><span data-stu-id="d2211-234">True</span></span>                                                   |
| <span data-ttu-id="d2211-235">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="d2211-235">Is Indexed</span></span>             | <span data-ttu-id="d2211-236">Falso</span><span class="sxs-lookup"><span data-stu-id="d2211-236">False</span></span>                                                  |
| <span data-ttu-id="d2211-237">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="d2211-237">In Global Catalog</span></span>      | <span data-ttu-id="d2211-238">Falso</span><span class="sxs-lookup"><span data-stu-id="d2211-238">False</span></span>                                                  |
| <span data-ttu-id="d2211-239">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="d2211-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="d2211-240">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="d2211-240">O:BAG:BAD:S:</span></span>                                           |
| <span data-ttu-id="d2211-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d2211-241">Range-Lower</span></span>            | \-                                                     |
| <span data-ttu-id="d2211-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d2211-242">Range-Upper</span></span>            | \-                                                     |
| <span data-ttu-id="d2211-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d2211-243">Search-Flags</span></span>           | <span data-ttu-id="d2211-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d2211-244">0x00000000</span></span>                                             |
| <span data-ttu-id="d2211-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d2211-245">System-Flags</span></span>           | <span data-ttu-id="d2211-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d2211-246">0x00000010</span></span>                                             |
| <span data-ttu-id="d2211-247">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="d2211-247">Classes used in</span></span>        | [<span data-ttu-id="d2211-248">**NTDS-connessione**</span><span class="sxs-lookup"><span data-stu-id="d2211-248">**NTDS-Connection**</span></span>](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="d2211-249">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d2211-249">Windows Server 2008 R2</span></span>



| <span data-ttu-id="d2211-250">Voce</span><span class="sxs-lookup"><span data-stu-id="d2211-250">Entry</span></span> | <span data-ttu-id="d2211-251">Valore</span><span class="sxs-lookup"><span data-stu-id="d2211-251">Value</span></span> |
|------------------------|--------------------------------------------------------|
| <span data-ttu-id="d2211-252">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="d2211-252">Link-Id</span></span>                | \-                                                     |
| <span data-ttu-id="d2211-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d2211-253">MAPI-Id</span></span>                | \-                                                     |
| <span data-ttu-id="d2211-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="d2211-254">System-Only</span></span>            | <span data-ttu-id="d2211-255">Falso</span><span class="sxs-lookup"><span data-stu-id="d2211-255">False</span></span>                                                  |
| <span data-ttu-id="d2211-256">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="d2211-256">Is-Single-Valued</span></span>       | <span data-ttu-id="d2211-257">Vero</span><span class="sxs-lookup"><span data-stu-id="d2211-257">True</span></span>                                                   |
| <span data-ttu-id="d2211-258">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="d2211-258">Is Indexed</span></span>             | <span data-ttu-id="d2211-259">Falso</span><span class="sxs-lookup"><span data-stu-id="d2211-259">False</span></span>                                                  |
| <span data-ttu-id="d2211-260">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="d2211-260">In Global Catalog</span></span>      | <span data-ttu-id="d2211-261">Falso</span><span class="sxs-lookup"><span data-stu-id="d2211-261">False</span></span>                                                  |
| <span data-ttu-id="d2211-262">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="d2211-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="d2211-263">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="d2211-263">O:BAG:BAD:S:</span></span>                                           |
| <span data-ttu-id="d2211-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d2211-264">Range-Lower</span></span>            | \-                                                     |
| <span data-ttu-id="d2211-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d2211-265">Range-Upper</span></span>            | \-                                                     |
| <span data-ttu-id="d2211-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d2211-266">Search-Flags</span></span>           | <span data-ttu-id="d2211-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d2211-267">0x00000000</span></span>                                             |
| <span data-ttu-id="d2211-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d2211-268">System-Flags</span></span>           | <span data-ttu-id="d2211-269">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d2211-269">0x00000010</span></span>                                             |
| <span data-ttu-id="d2211-270">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="d2211-270">Classes used in</span></span>        | [<span data-ttu-id="d2211-271">**NTDS-connessione**</span><span class="sxs-lookup"><span data-stu-id="d2211-271">**NTDS-Connection**</span></span>](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="d2211-272">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d2211-272">Windows Server 2012</span></span>



| <span data-ttu-id="d2211-273">Voce</span><span class="sxs-lookup"><span data-stu-id="d2211-273">Entry</span></span> | <span data-ttu-id="d2211-274">Valore</span><span class="sxs-lookup"><span data-stu-id="d2211-274">Value</span></span> |
|------------------------|--------------------------------------------------------|
| <span data-ttu-id="d2211-275">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="d2211-275">Link-Id</span></span>                | \-                                                     |
| <span data-ttu-id="d2211-276">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d2211-276">MAPI-Id</span></span>                | \-                                                     |
| <span data-ttu-id="d2211-277">System-Only</span><span class="sxs-lookup"><span data-stu-id="d2211-277">System-Only</span></span>            | <span data-ttu-id="d2211-278">Falso</span><span class="sxs-lookup"><span data-stu-id="d2211-278">False</span></span>                                                  |
| <span data-ttu-id="d2211-279">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="d2211-279">Is-Single-Valued</span></span>       | <span data-ttu-id="d2211-280">Vero</span><span class="sxs-lookup"><span data-stu-id="d2211-280">True</span></span>                                                   |
| <span data-ttu-id="d2211-281">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="d2211-281">Is Indexed</span></span>             | <span data-ttu-id="d2211-282">Falso</span><span class="sxs-lookup"><span data-stu-id="d2211-282">False</span></span>                                                  |
| <span data-ttu-id="d2211-283">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="d2211-283">In Global Catalog</span></span>      | <span data-ttu-id="d2211-284">Falso</span><span class="sxs-lookup"><span data-stu-id="d2211-284">False</span></span>                                                  |
| <span data-ttu-id="d2211-285">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="d2211-285">NT-Security-Descriptor</span></span> | <span data-ttu-id="d2211-286">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="d2211-286">O:BAG:BAD:S:</span></span>                                           |
| <span data-ttu-id="d2211-287">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d2211-287">Range-Lower</span></span>            | \-                                                     |
| <span data-ttu-id="d2211-288">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d2211-288">Range-Upper</span></span>            | \-                                                     |
| <span data-ttu-id="d2211-289">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d2211-289">Search-Flags</span></span>           | <span data-ttu-id="d2211-290">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d2211-290">0x00000000</span></span>                                             |
| <span data-ttu-id="d2211-291">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d2211-291">System-Flags</span></span>           | <span data-ttu-id="d2211-292">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d2211-292">0x00000010</span></span>                                             |
| <span data-ttu-id="d2211-293">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="d2211-293">Classes used in</span></span>        | [<span data-ttu-id="d2211-294">**NTDS-connessione**</span><span class="sxs-lookup"><span data-stu-id="d2211-294">**NTDS-Connection**</span></span>](c-ntdsconnection.md)<br/> |



 

 





