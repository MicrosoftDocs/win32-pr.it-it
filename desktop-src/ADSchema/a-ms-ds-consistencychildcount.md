---
title: Attributo MS-DS-coerenza-figlio-conteggio
description: Questo attributo viene utilizzato per verificare la coerenza tra la directory e un altro oggetto, database o applicazione, confrontando un conteggio di oggetti figlio.
ms.assetid: f7d6e8f0-963b-45a9-86af-8e51d6de32bb
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo MS-DS-coerenza-figlio-conteggio
- Schema AD dell'attributo mS-DS-ConsistencyChildCount
topic_type:
- apiref
api_name:
- MS-DS-Consistency-Child-Count
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b9c46d1c4519550a91d92d0a82f726a20572490
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104122111"
---
# <a name="ms-ds-consistency-child-count-attribute"></a><span data-ttu-id="7f8f4-105">Attributo MS-DS-coerenza-figlio-conteggio</span><span class="sxs-lookup"><span data-stu-id="7f8f4-105">MS-DS-Consistency-Child-Count attribute</span></span>

<span data-ttu-id="7f8f4-106">Questo attributo viene utilizzato per verificare la coerenza tra la directory e un altro oggetto, database o applicazione, confrontando un conteggio di oggetti figlio.</span><span class="sxs-lookup"><span data-stu-id="7f8f4-106">This attribute is used to check consistency between the directory and another object, database, or application, by comparing a count of child objects.</span></span>



| <span data-ttu-id="7f8f4-107">Voce</span><span class="sxs-lookup"><span data-stu-id="7f8f4-107">Entry</span></span> | <span data-ttu-id="7f8f4-108">Valore</span><span class="sxs-lookup"><span data-stu-id="7f8f4-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="7f8f4-109">CN</span><span class="sxs-lookup"><span data-stu-id="7f8f4-109">CN</span></span>                | <span data-ttu-id="7f8f4-110">MS-DS-coerenza-figlio-conteggio</span><span class="sxs-lookup"><span data-stu-id="7f8f4-110">MS-DS-Consistency-Child-Count</span></span>        |
| <span data-ttu-id="7f8f4-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="7f8f4-111">Ldap-Display-Name</span></span> | <span data-ttu-id="7f8f4-112">mS-DS-ConsistencyChildCount</span><span class="sxs-lookup"><span data-stu-id="7f8f4-112">mS-DS-ConsistencyChildCount</span></span>          |
| <span data-ttu-id="7f8f4-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="7f8f4-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="7f8f4-114">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="7f8f4-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="7f8f4-115">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="7f8f4-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="7f8f4-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="7f8f4-116">Attribute-Id</span></span>      | <span data-ttu-id="7f8f4-117">1.2.840.113556.1.4.1361</span><span class="sxs-lookup"><span data-stu-id="7f8f4-117">1.2.840.113556.1.4.1361</span></span>              |
| <span data-ttu-id="7f8f4-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="7f8f4-118">System-Id-Guid</span></span>    | <span data-ttu-id="7f8f4-119">178b7bc2-b63a-11d2-90e1-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="7f8f4-119">178b7bc2-b63a-11d2-90e1-00c04fd91ab1</span></span> |
| <span data-ttu-id="7f8f4-120">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7f8f4-120">Syntax</span></span>            | [<span data-ttu-id="7f8f4-121">**Enumerazione**</span><span class="sxs-lookup"><span data-stu-id="7f8f4-121">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="7f8f4-122">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="7f8f4-122">Implementations</span></span>

-   [<span data-ttu-id="7f8f4-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="7f8f4-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="7f8f4-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="7f8f4-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="7f8f4-125">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="7f8f4-125">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="7f8f4-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="7f8f4-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="7f8f4-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="7f8f4-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="7f8f4-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="7f8f4-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="7f8f4-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="7f8f4-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="7f8f4-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7f8f4-130">Windows 2000 Server</span></span>



| <span data-ttu-id="7f8f4-131">Voce</span><span class="sxs-lookup"><span data-stu-id="7f8f4-131">Entry</span></span> | <span data-ttu-id="7f8f4-132">Valore</span><span class="sxs-lookup"><span data-stu-id="7f8f4-132">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="7f8f4-133">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="7f8f4-133">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="7f8f4-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7f8f4-134">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="7f8f4-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="7f8f4-135">System-Only</span></span>            | <span data-ttu-id="7f8f4-136">Falso</span><span class="sxs-lookup"><span data-stu-id="7f8f4-136">False</span></span>                           |
| <span data-ttu-id="7f8f4-137">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="7f8f4-137">Is-Single-Valued</span></span>       | <span data-ttu-id="7f8f4-138">Vero</span><span class="sxs-lookup"><span data-stu-id="7f8f4-138">True</span></span>                            |
| <span data-ttu-id="7f8f4-139">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="7f8f4-139">Is Indexed</span></span>             | <span data-ttu-id="7f8f4-140">Falso</span><span class="sxs-lookup"><span data-stu-id="7f8f4-140">False</span></span>                           |
| <span data-ttu-id="7f8f4-141">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="7f8f4-141">In Global Catalog</span></span>      | <span data-ttu-id="7f8f4-142">Falso</span><span class="sxs-lookup"><span data-stu-id="7f8f4-142">False</span></span>                           |
| <span data-ttu-id="7f8f4-143">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="7f8f4-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="7f8f4-144">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="7f8f4-144">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="7f8f4-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7f8f4-145">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="7f8f4-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7f8f4-146">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="7f8f4-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7f8f4-147">Search-Flags</span></span>           | <span data-ttu-id="7f8f4-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7f8f4-148">0x00000000</span></span>                      |
| <span data-ttu-id="7f8f4-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7f8f4-149">System-Flags</span></span>           | <span data-ttu-id="7f8f4-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7f8f4-150">0x00000010</span></span>                      |
| <span data-ttu-id="7f8f4-151">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="7f8f4-151">Classes used in</span></span>        | [<span data-ttu-id="7f8f4-152">**In alto**</span><span class="sxs-lookup"><span data-stu-id="7f8f4-152">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="7f8f4-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7f8f4-153">Windows Server 2003</span></span>



| <span data-ttu-id="7f8f4-154">Voce</span><span class="sxs-lookup"><span data-stu-id="7f8f4-154">Entry</span></span> | <span data-ttu-id="7f8f4-155">Valore</span><span class="sxs-lookup"><span data-stu-id="7f8f4-155">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="7f8f4-156">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="7f8f4-156">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="7f8f4-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7f8f4-157">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="7f8f4-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="7f8f4-158">System-Only</span></span>            | <span data-ttu-id="7f8f4-159">Falso</span><span class="sxs-lookup"><span data-stu-id="7f8f4-159">False</span></span>                           |
| <span data-ttu-id="7f8f4-160">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="7f8f4-160">Is-Single-Valued</span></span>       | <span data-ttu-id="7f8f4-161">Vero</span><span class="sxs-lookup"><span data-stu-id="7f8f4-161">True</span></span>                            |
| <span data-ttu-id="7f8f4-162">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="7f8f4-162">Is Indexed</span></span>             | <span data-ttu-id="7f8f4-163">Falso</span><span class="sxs-lookup"><span data-stu-id="7f8f4-163">False</span></span>                           |
| <span data-ttu-id="7f8f4-164">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="7f8f4-164">In Global Catalog</span></span>      | <span data-ttu-id="7f8f4-165">Falso</span><span class="sxs-lookup"><span data-stu-id="7f8f4-165">False</span></span>                           |
| <span data-ttu-id="7f8f4-166">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="7f8f4-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="7f8f4-167">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="7f8f4-167">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="7f8f4-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7f8f4-168">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="7f8f4-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7f8f4-169">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="7f8f4-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7f8f4-170">Search-Flags</span></span>           | <span data-ttu-id="7f8f4-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7f8f4-171">0x00000000</span></span>                      |
| <span data-ttu-id="7f8f4-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7f8f4-172">System-Flags</span></span>           | <span data-ttu-id="7f8f4-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7f8f4-173">0x00000010</span></span>                      |
| <span data-ttu-id="7f8f4-174">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="7f8f4-174">Classes used in</span></span>        | [<span data-ttu-id="7f8f4-175">**In alto**</span><span class="sxs-lookup"><span data-stu-id="7f8f4-175">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="7f8f4-176">ADAM</span><span class="sxs-lookup"><span data-stu-id="7f8f4-176">ADAM</span></span>



| <span data-ttu-id="7f8f4-177">Voce</span><span class="sxs-lookup"><span data-stu-id="7f8f4-177">Entry</span></span> | <span data-ttu-id="7f8f4-178">Valore</span><span class="sxs-lookup"><span data-stu-id="7f8f4-178">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="7f8f4-179">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="7f8f4-179">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="7f8f4-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7f8f4-180">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="7f8f4-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="7f8f4-181">System-Only</span></span>            | <span data-ttu-id="7f8f4-182">Falso</span><span class="sxs-lookup"><span data-stu-id="7f8f4-182">False</span></span>                           |
| <span data-ttu-id="7f8f4-183">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="7f8f4-183">Is-Single-Valued</span></span>       | <span data-ttu-id="7f8f4-184">Vero</span><span class="sxs-lookup"><span data-stu-id="7f8f4-184">True</span></span>                            |
| <span data-ttu-id="7f8f4-185">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="7f8f4-185">Is Indexed</span></span>             | <span data-ttu-id="7f8f4-186">Falso</span><span class="sxs-lookup"><span data-stu-id="7f8f4-186">False</span></span>                           |
| <span data-ttu-id="7f8f4-187">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="7f8f4-187">In Global Catalog</span></span>      | <span data-ttu-id="7f8f4-188">Falso</span><span class="sxs-lookup"><span data-stu-id="7f8f4-188">False</span></span>                           |
| <span data-ttu-id="7f8f4-189">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="7f8f4-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="7f8f4-190">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="7f8f4-190">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="7f8f4-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7f8f4-191">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="7f8f4-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7f8f4-192">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="7f8f4-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7f8f4-193">Search-Flags</span></span>           | <span data-ttu-id="7f8f4-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7f8f4-194">0x00000000</span></span>                      |
| <span data-ttu-id="7f8f4-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7f8f4-195">System-Flags</span></span>           | <span data-ttu-id="7f8f4-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7f8f4-196">0x00000010</span></span>                      |
| <span data-ttu-id="7f8f4-197">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="7f8f4-197">Classes used in</span></span>        | [<span data-ttu-id="7f8f4-198">**In alto**</span><span class="sxs-lookup"><span data-stu-id="7f8f4-198">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="7f8f4-199">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="7f8f4-199">Windows Server 2003 R2</span></span>



| <span data-ttu-id="7f8f4-200">Voce</span><span class="sxs-lookup"><span data-stu-id="7f8f4-200">Entry</span></span> | <span data-ttu-id="7f8f4-201">Valore</span><span class="sxs-lookup"><span data-stu-id="7f8f4-201">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="7f8f4-202">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="7f8f4-202">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="7f8f4-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7f8f4-203">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="7f8f4-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="7f8f4-204">System-Only</span></span>            | <span data-ttu-id="7f8f4-205">Falso</span><span class="sxs-lookup"><span data-stu-id="7f8f4-205">False</span></span>                           |
| <span data-ttu-id="7f8f4-206">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="7f8f4-206">Is-Single-Valued</span></span>       | <span data-ttu-id="7f8f4-207">Vero</span><span class="sxs-lookup"><span data-stu-id="7f8f4-207">True</span></span>                            |
| <span data-ttu-id="7f8f4-208">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="7f8f4-208">Is Indexed</span></span>             | <span data-ttu-id="7f8f4-209">Falso</span><span class="sxs-lookup"><span data-stu-id="7f8f4-209">False</span></span>                           |
| <span data-ttu-id="7f8f4-210">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="7f8f4-210">In Global Catalog</span></span>      | <span data-ttu-id="7f8f4-211">Falso</span><span class="sxs-lookup"><span data-stu-id="7f8f4-211">False</span></span>                           |
| <span data-ttu-id="7f8f4-212">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="7f8f4-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="7f8f4-213">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="7f8f4-213">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="7f8f4-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7f8f4-214">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="7f8f4-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7f8f4-215">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="7f8f4-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7f8f4-216">Search-Flags</span></span>           | <span data-ttu-id="7f8f4-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7f8f4-217">0x00000000</span></span>                      |
| <span data-ttu-id="7f8f4-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7f8f4-218">System-Flags</span></span>           | <span data-ttu-id="7f8f4-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7f8f4-219">0x00000010</span></span>                      |
| <span data-ttu-id="7f8f4-220">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="7f8f4-220">Classes used in</span></span>        | [<span data-ttu-id="7f8f4-221">**In alto**</span><span class="sxs-lookup"><span data-stu-id="7f8f4-221">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="7f8f4-222">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7f8f4-222">Windows Server 2008</span></span>



| <span data-ttu-id="7f8f4-223">Voce</span><span class="sxs-lookup"><span data-stu-id="7f8f4-223">Entry</span></span> | <span data-ttu-id="7f8f4-224">Valore</span><span class="sxs-lookup"><span data-stu-id="7f8f4-224">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="7f8f4-225">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="7f8f4-225">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="7f8f4-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7f8f4-226">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="7f8f4-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="7f8f4-227">System-Only</span></span>            | <span data-ttu-id="7f8f4-228">Falso</span><span class="sxs-lookup"><span data-stu-id="7f8f4-228">False</span></span>                           |
| <span data-ttu-id="7f8f4-229">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="7f8f4-229">Is-Single-Valued</span></span>       | <span data-ttu-id="7f8f4-230">Vero</span><span class="sxs-lookup"><span data-stu-id="7f8f4-230">True</span></span>                            |
| <span data-ttu-id="7f8f4-231">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="7f8f4-231">Is Indexed</span></span>             | <span data-ttu-id="7f8f4-232">Falso</span><span class="sxs-lookup"><span data-stu-id="7f8f4-232">False</span></span>                           |
| <span data-ttu-id="7f8f4-233">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="7f8f4-233">In Global Catalog</span></span>      | <span data-ttu-id="7f8f4-234">Falso</span><span class="sxs-lookup"><span data-stu-id="7f8f4-234">False</span></span>                           |
| <span data-ttu-id="7f8f4-235">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="7f8f4-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="7f8f4-236">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="7f8f4-236">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="7f8f4-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7f8f4-237">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="7f8f4-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7f8f4-238">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="7f8f4-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7f8f4-239">Search-Flags</span></span>           | <span data-ttu-id="7f8f4-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7f8f4-240">0x00000000</span></span>                      |
| <span data-ttu-id="7f8f4-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7f8f4-241">System-Flags</span></span>           | <span data-ttu-id="7f8f4-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7f8f4-242">0x00000010</span></span>                      |
| <span data-ttu-id="7f8f4-243">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="7f8f4-243">Classes used in</span></span>        | [<span data-ttu-id="7f8f4-244">**In alto**</span><span class="sxs-lookup"><span data-stu-id="7f8f4-244">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="7f8f4-245">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7f8f4-245">Windows Server 2008 R2</span></span>



| <span data-ttu-id="7f8f4-246">Voce</span><span class="sxs-lookup"><span data-stu-id="7f8f4-246">Entry</span></span> | <span data-ttu-id="7f8f4-247">Valore</span><span class="sxs-lookup"><span data-stu-id="7f8f4-247">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="7f8f4-248">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="7f8f4-248">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="7f8f4-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7f8f4-249">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="7f8f4-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="7f8f4-250">System-Only</span></span>            | <span data-ttu-id="7f8f4-251">Falso</span><span class="sxs-lookup"><span data-stu-id="7f8f4-251">False</span></span>                           |
| <span data-ttu-id="7f8f4-252">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="7f8f4-252">Is-Single-Valued</span></span>       | <span data-ttu-id="7f8f4-253">Vero</span><span class="sxs-lookup"><span data-stu-id="7f8f4-253">True</span></span>                            |
| <span data-ttu-id="7f8f4-254">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="7f8f4-254">Is Indexed</span></span>             | <span data-ttu-id="7f8f4-255">Falso</span><span class="sxs-lookup"><span data-stu-id="7f8f4-255">False</span></span>                           |
| <span data-ttu-id="7f8f4-256">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="7f8f4-256">In Global Catalog</span></span>      | <span data-ttu-id="7f8f4-257">Falso</span><span class="sxs-lookup"><span data-stu-id="7f8f4-257">False</span></span>                           |
| <span data-ttu-id="7f8f4-258">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="7f8f4-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="7f8f4-259">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="7f8f4-259">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="7f8f4-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7f8f4-260">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="7f8f4-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7f8f4-261">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="7f8f4-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7f8f4-262">Search-Flags</span></span>           | <span data-ttu-id="7f8f4-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7f8f4-263">0x00000000</span></span>                      |
| <span data-ttu-id="7f8f4-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7f8f4-264">System-Flags</span></span>           | <span data-ttu-id="7f8f4-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7f8f4-265">0x00000010</span></span>                      |
| <span data-ttu-id="7f8f4-266">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="7f8f4-266">Classes used in</span></span>        | [<span data-ttu-id="7f8f4-267">**In alto**</span><span class="sxs-lookup"><span data-stu-id="7f8f4-267">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="7f8f4-268">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7f8f4-268">Windows Server 2012</span></span>



| <span data-ttu-id="7f8f4-269">Voce</span><span class="sxs-lookup"><span data-stu-id="7f8f4-269">Entry</span></span> | <span data-ttu-id="7f8f4-270">Valore</span><span class="sxs-lookup"><span data-stu-id="7f8f4-270">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="7f8f4-271">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="7f8f4-271">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="7f8f4-272">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7f8f4-272">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="7f8f4-273">System-Only</span><span class="sxs-lookup"><span data-stu-id="7f8f4-273">System-Only</span></span>            | <span data-ttu-id="7f8f4-274">Falso</span><span class="sxs-lookup"><span data-stu-id="7f8f4-274">False</span></span>                           |
| <span data-ttu-id="7f8f4-275">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="7f8f4-275">Is-Single-Valued</span></span>       | <span data-ttu-id="7f8f4-276">Vero</span><span class="sxs-lookup"><span data-stu-id="7f8f4-276">True</span></span>                            |
| <span data-ttu-id="7f8f4-277">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="7f8f4-277">Is Indexed</span></span>             | <span data-ttu-id="7f8f4-278">Falso</span><span class="sxs-lookup"><span data-stu-id="7f8f4-278">False</span></span>                           |
| <span data-ttu-id="7f8f4-279">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="7f8f4-279">In Global Catalog</span></span>      | <span data-ttu-id="7f8f4-280">Falso</span><span class="sxs-lookup"><span data-stu-id="7f8f4-280">False</span></span>                           |
| <span data-ttu-id="7f8f4-281">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="7f8f4-281">NT-Security-Descriptor</span></span> | <span data-ttu-id="7f8f4-282">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="7f8f4-282">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="7f8f4-283">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7f8f4-283">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="7f8f4-284">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7f8f4-284">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="7f8f4-285">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7f8f4-285">Search-Flags</span></span>           | <span data-ttu-id="7f8f4-286">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7f8f4-286">0x00000000</span></span>                      |
| <span data-ttu-id="7f8f4-287">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7f8f4-287">System-Flags</span></span>           | <span data-ttu-id="7f8f4-288">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7f8f4-288">0x00000010</span></span>                      |
| <span data-ttu-id="7f8f4-289">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="7f8f4-289">Classes used in</span></span>        | [<span data-ttu-id="7f8f4-290">**In alto**</span><span class="sxs-lookup"><span data-stu-id="7f8f4-290">**Top**</span></span>](c-top.md)<br/> |



 

 





