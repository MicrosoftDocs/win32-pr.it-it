---
title: Attributo Rights-Guid
description: GUID utilizzato per rappresentare un diritto esteso all'interno di una voce di controllo di accesso.
ms.assetid: 6f3a654e-fead-41e7-8383-6dade1a2747e
ms.tgt_platform: multiple
keywords:
- Schema AD Rights-Guid attribute
- Schema AD dell'attributo rightsGuid
topic_type:
- apiref
api_name:
- Rights-Guid
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4da47ec8e4736dd13b6ba39da0208aed505aa8a9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104122691"
---
# <a name="rights-guid-attribute"></a><span data-ttu-id="b0121-105">Attributo Rights-Guid</span><span class="sxs-lookup"><span data-stu-id="b0121-105">Rights-Guid attribute</span></span>

<span data-ttu-id="b0121-106">GUID utilizzato per rappresentare un diritto esteso all'interno di una voce di controllo di accesso.</span><span class="sxs-lookup"><span data-stu-id="b0121-106">The GUID used to represent an extended right within an access control entry.</span></span>



| <span data-ttu-id="b0121-107">Voce</span><span class="sxs-lookup"><span data-stu-id="b0121-107">Entry</span></span> | <span data-ttu-id="b0121-108">Valore</span><span class="sxs-lookup"><span data-stu-id="b0121-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="b0121-109">CN</span><span class="sxs-lookup"><span data-stu-id="b0121-109">CN</span></span>                | <span data-ttu-id="b0121-110">Rights-Guid</span><span class="sxs-lookup"><span data-stu-id="b0121-110">Rights-Guid</span></span>                                 |
| <span data-ttu-id="b0121-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="b0121-111">Ldap-Display-Name</span></span> | <span data-ttu-id="b0121-112">rightsGuid</span><span class="sxs-lookup"><span data-stu-id="b0121-112">rightsGuid</span></span>                                  |
| <span data-ttu-id="b0121-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="b0121-113">Size</span></span>              | <span data-ttu-id="b0121-114">16 byte</span><span class="sxs-lookup"><span data-stu-id="b0121-114">16 bytes</span></span>                                    |
| <span data-ttu-id="b0121-115">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="b0121-115">Update Privilege</span></span>  | <span data-ttu-id="b0121-116">Questo valore viene impostato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="b0121-116">This value is set by the system.</span></span>            |
| <span data-ttu-id="b0121-117">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="b0121-117">Update Frequency</span></span>  | <span data-ttu-id="b0121-118">Quando viene creato un nuovo diritto esteso.</span><span class="sxs-lookup"><span data-stu-id="b0121-118">When a new extended right is created.</span></span>       |
| <span data-ttu-id="b0121-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b0121-119">Attribute-Id</span></span>      | <span data-ttu-id="b0121-120">1.2.840.113556.1.4.340</span><span class="sxs-lookup"><span data-stu-id="b0121-120">1.2.840.113556.1.4.340</span></span>                      |
| <span data-ttu-id="b0121-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="b0121-121">System-Id-Guid</span></span>    | <span data-ttu-id="b0121-122">8297931c-86d3-11d0-afda-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="b0121-122">8297931c-86d3-11d0-afda-00c04fd930c9</span></span>        |
| <span data-ttu-id="b0121-123">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b0121-123">Syntax</span></span>            | [<span data-ttu-id="b0121-124">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="b0121-124">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="b0121-125">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="b0121-125">Implementations</span></span>

-   [<span data-ttu-id="b0121-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="b0121-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="b0121-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b0121-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b0121-128">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="b0121-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="b0121-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b0121-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b0121-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b0121-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b0121-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b0121-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b0121-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b0121-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="b0121-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b0121-133">Windows 2000 Server</span></span>



| <span data-ttu-id="b0121-134">Voce</span><span class="sxs-lookup"><span data-stu-id="b0121-134">Entry</span></span> | <span data-ttu-id="b0121-135">Valore</span><span class="sxs-lookup"><span data-stu-id="b0121-135">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="b0121-136">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="b0121-136">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="b0121-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b0121-137">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="b0121-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="b0121-138">System-Only</span></span>            | <span data-ttu-id="b0121-139">Falso</span><span class="sxs-lookup"><span data-stu-id="b0121-139">False</span></span>                                                           |
| <span data-ttu-id="b0121-140">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="b0121-140">Is-Single-Valued</span></span>       | <span data-ttu-id="b0121-141">Vero</span><span class="sxs-lookup"><span data-stu-id="b0121-141">True</span></span>                                                            |
| <span data-ttu-id="b0121-142">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="b0121-142">Is Indexed</span></span>             | <span data-ttu-id="b0121-143">Falso</span><span class="sxs-lookup"><span data-stu-id="b0121-143">False</span></span>                                                           |
| <span data-ttu-id="b0121-144">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="b0121-144">In Global Catalog</span></span>      | <span data-ttu-id="b0121-145">Falso</span><span class="sxs-lookup"><span data-stu-id="b0121-145">False</span></span>                                                           |
| <span data-ttu-id="b0121-146">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="b0121-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="b0121-147">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="b0121-147">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="b0121-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b0121-148">Range-Lower</span></span>            | <span data-ttu-id="b0121-149">36</span><span class="sxs-lookup"><span data-stu-id="b0121-149">36</span></span>                                                              |
| <span data-ttu-id="b0121-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b0121-150">Range-Upper</span></span>            | <span data-ttu-id="b0121-151">36</span><span class="sxs-lookup"><span data-stu-id="b0121-151">36</span></span>                                                              |
| <span data-ttu-id="b0121-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b0121-152">Search-Flags</span></span>           | <span data-ttu-id="b0121-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b0121-153">0x00000000</span></span>                                                      |
| <span data-ttu-id="b0121-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b0121-154">System-Flags</span></span>           | <span data-ttu-id="b0121-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b0121-155">0x00000010</span></span>                                                      |
| <span data-ttu-id="b0121-156">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="b0121-156">Classes used in</span></span>        | [<span data-ttu-id="b0121-157">**Controllo-accesso-a destra**</span><span class="sxs-lookup"><span data-stu-id="b0121-157">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="b0121-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b0121-158">Windows Server 2003</span></span>



| <span data-ttu-id="b0121-159">Voce</span><span class="sxs-lookup"><span data-stu-id="b0121-159">Entry</span></span> | <span data-ttu-id="b0121-160">Valore</span><span class="sxs-lookup"><span data-stu-id="b0121-160">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="b0121-161">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="b0121-161">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="b0121-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b0121-162">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="b0121-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="b0121-163">System-Only</span></span>            | <span data-ttu-id="b0121-164">Falso</span><span class="sxs-lookup"><span data-stu-id="b0121-164">False</span></span>                                                           |
| <span data-ttu-id="b0121-165">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="b0121-165">Is-Single-Valued</span></span>       | <span data-ttu-id="b0121-166">Vero</span><span class="sxs-lookup"><span data-stu-id="b0121-166">True</span></span>                                                            |
| <span data-ttu-id="b0121-167">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="b0121-167">Is Indexed</span></span>             | <span data-ttu-id="b0121-168">Falso</span><span class="sxs-lookup"><span data-stu-id="b0121-168">False</span></span>                                                           |
| <span data-ttu-id="b0121-169">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="b0121-169">In Global Catalog</span></span>      | <span data-ttu-id="b0121-170">Falso</span><span class="sxs-lookup"><span data-stu-id="b0121-170">False</span></span>                                                           |
| <span data-ttu-id="b0121-171">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="b0121-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="b0121-172">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="b0121-172">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="b0121-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b0121-173">Range-Lower</span></span>            | <span data-ttu-id="b0121-174">36</span><span class="sxs-lookup"><span data-stu-id="b0121-174">36</span></span>                                                              |
| <span data-ttu-id="b0121-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b0121-175">Range-Upper</span></span>            | <span data-ttu-id="b0121-176">36</span><span class="sxs-lookup"><span data-stu-id="b0121-176">36</span></span>                                                              |
| <span data-ttu-id="b0121-177">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b0121-177">Search-Flags</span></span>           | <span data-ttu-id="b0121-178">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b0121-178">0x00000000</span></span>                                                      |
| <span data-ttu-id="b0121-179">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b0121-179">System-Flags</span></span>           | <span data-ttu-id="b0121-180">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b0121-180">0x00000010</span></span>                                                      |
| <span data-ttu-id="b0121-181">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="b0121-181">Classes used in</span></span>        | [<span data-ttu-id="b0121-182">**Controllo-accesso-a destra**</span><span class="sxs-lookup"><span data-stu-id="b0121-182">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="adam"></a><span data-ttu-id="b0121-183">ADAM</span><span class="sxs-lookup"><span data-stu-id="b0121-183">ADAM</span></span>



| <span data-ttu-id="b0121-184">Voce</span><span class="sxs-lookup"><span data-stu-id="b0121-184">Entry</span></span> | <span data-ttu-id="b0121-185">Valore</span><span class="sxs-lookup"><span data-stu-id="b0121-185">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="b0121-186">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="b0121-186">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="b0121-187">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b0121-187">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="b0121-188">System-Only</span><span class="sxs-lookup"><span data-stu-id="b0121-188">System-Only</span></span>            | <span data-ttu-id="b0121-189">Falso</span><span class="sxs-lookup"><span data-stu-id="b0121-189">False</span></span>                                                           |
| <span data-ttu-id="b0121-190">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="b0121-190">Is-Single-Valued</span></span>       | <span data-ttu-id="b0121-191">Vero</span><span class="sxs-lookup"><span data-stu-id="b0121-191">True</span></span>                                                            |
| <span data-ttu-id="b0121-192">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="b0121-192">Is Indexed</span></span>             | <span data-ttu-id="b0121-193">Falso</span><span class="sxs-lookup"><span data-stu-id="b0121-193">False</span></span>                                                           |
| <span data-ttu-id="b0121-194">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="b0121-194">In Global Catalog</span></span>      | <span data-ttu-id="b0121-195">Falso</span><span class="sxs-lookup"><span data-stu-id="b0121-195">False</span></span>                                                           |
| <span data-ttu-id="b0121-196">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="b0121-196">NT-Security-Descriptor</span></span> | <span data-ttu-id="b0121-197">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="b0121-197">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="b0121-198">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b0121-198">Range-Lower</span></span>            | <span data-ttu-id="b0121-199">36</span><span class="sxs-lookup"><span data-stu-id="b0121-199">36</span></span>                                                              |
| <span data-ttu-id="b0121-200">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b0121-200">Range-Upper</span></span>            | <span data-ttu-id="b0121-201">36</span><span class="sxs-lookup"><span data-stu-id="b0121-201">36</span></span>                                                              |
| <span data-ttu-id="b0121-202">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b0121-202">Search-Flags</span></span>           | <span data-ttu-id="b0121-203">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b0121-203">0x00000000</span></span>                                                      |
| <span data-ttu-id="b0121-204">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b0121-204">System-Flags</span></span>           | <span data-ttu-id="b0121-205">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b0121-205">0x00000010</span></span>                                                      |
| <span data-ttu-id="b0121-206">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="b0121-206">Classes used in</span></span>        | [<span data-ttu-id="b0121-207">**Controllo-accesso-a destra**</span><span class="sxs-lookup"><span data-stu-id="b0121-207">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b0121-208">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b0121-208">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b0121-209">Voce</span><span class="sxs-lookup"><span data-stu-id="b0121-209">Entry</span></span> | <span data-ttu-id="b0121-210">Valore</span><span class="sxs-lookup"><span data-stu-id="b0121-210">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="b0121-211">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="b0121-211">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="b0121-212">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b0121-212">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="b0121-213">System-Only</span><span class="sxs-lookup"><span data-stu-id="b0121-213">System-Only</span></span>            | <span data-ttu-id="b0121-214">Falso</span><span class="sxs-lookup"><span data-stu-id="b0121-214">False</span></span>                                                           |
| <span data-ttu-id="b0121-215">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="b0121-215">Is-Single-Valued</span></span>       | <span data-ttu-id="b0121-216">Vero</span><span class="sxs-lookup"><span data-stu-id="b0121-216">True</span></span>                                                            |
| <span data-ttu-id="b0121-217">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="b0121-217">Is Indexed</span></span>             | <span data-ttu-id="b0121-218">Falso</span><span class="sxs-lookup"><span data-stu-id="b0121-218">False</span></span>                                                           |
| <span data-ttu-id="b0121-219">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="b0121-219">In Global Catalog</span></span>      | <span data-ttu-id="b0121-220">Falso</span><span class="sxs-lookup"><span data-stu-id="b0121-220">False</span></span>                                                           |
| <span data-ttu-id="b0121-221">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="b0121-221">NT-Security-Descriptor</span></span> | <span data-ttu-id="b0121-222">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="b0121-222">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="b0121-223">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b0121-223">Range-Lower</span></span>            | <span data-ttu-id="b0121-224">36</span><span class="sxs-lookup"><span data-stu-id="b0121-224">36</span></span>                                                              |
| <span data-ttu-id="b0121-225">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b0121-225">Range-Upper</span></span>            | <span data-ttu-id="b0121-226">36</span><span class="sxs-lookup"><span data-stu-id="b0121-226">36</span></span>                                                              |
| <span data-ttu-id="b0121-227">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b0121-227">Search-Flags</span></span>           | <span data-ttu-id="b0121-228">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b0121-228">0x00000000</span></span>                                                      |
| <span data-ttu-id="b0121-229">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b0121-229">System-Flags</span></span>           | <span data-ttu-id="b0121-230">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b0121-230">0x00000010</span></span>                                                      |
| <span data-ttu-id="b0121-231">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="b0121-231">Classes used in</span></span>        | [<span data-ttu-id="b0121-232">**Controllo-accesso-a destra**</span><span class="sxs-lookup"><span data-stu-id="b0121-232">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b0121-233">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b0121-233">Windows Server 2008</span></span>



| <span data-ttu-id="b0121-234">Voce</span><span class="sxs-lookup"><span data-stu-id="b0121-234">Entry</span></span> | <span data-ttu-id="b0121-235">Valore</span><span class="sxs-lookup"><span data-stu-id="b0121-235">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="b0121-236">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="b0121-236">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="b0121-237">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b0121-237">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="b0121-238">System-Only</span><span class="sxs-lookup"><span data-stu-id="b0121-238">System-Only</span></span>            | <span data-ttu-id="b0121-239">Falso</span><span class="sxs-lookup"><span data-stu-id="b0121-239">False</span></span>                                                           |
| <span data-ttu-id="b0121-240">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="b0121-240">Is-Single-Valued</span></span>       | <span data-ttu-id="b0121-241">Vero</span><span class="sxs-lookup"><span data-stu-id="b0121-241">True</span></span>                                                            |
| <span data-ttu-id="b0121-242">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="b0121-242">Is Indexed</span></span>             | <span data-ttu-id="b0121-243">Falso</span><span class="sxs-lookup"><span data-stu-id="b0121-243">False</span></span>                                                           |
| <span data-ttu-id="b0121-244">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="b0121-244">In Global Catalog</span></span>      | <span data-ttu-id="b0121-245">Falso</span><span class="sxs-lookup"><span data-stu-id="b0121-245">False</span></span>                                                           |
| <span data-ttu-id="b0121-246">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="b0121-246">NT-Security-Descriptor</span></span> | <span data-ttu-id="b0121-247">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="b0121-247">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="b0121-248">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b0121-248">Range-Lower</span></span>            | <span data-ttu-id="b0121-249">36</span><span class="sxs-lookup"><span data-stu-id="b0121-249">36</span></span>                                                              |
| <span data-ttu-id="b0121-250">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b0121-250">Range-Upper</span></span>            | <span data-ttu-id="b0121-251">36</span><span class="sxs-lookup"><span data-stu-id="b0121-251">36</span></span>                                                              |
| <span data-ttu-id="b0121-252">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b0121-252">Search-Flags</span></span>           | <span data-ttu-id="b0121-253">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b0121-253">0x00000000</span></span>                                                      |
| <span data-ttu-id="b0121-254">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b0121-254">System-Flags</span></span>           | <span data-ttu-id="b0121-255">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b0121-255">0x00000010</span></span>                                                      |
| <span data-ttu-id="b0121-256">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="b0121-256">Classes used in</span></span>        | [<span data-ttu-id="b0121-257">**Controllo-accesso-a destra**</span><span class="sxs-lookup"><span data-stu-id="b0121-257">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b0121-258">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b0121-258">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b0121-259">Voce</span><span class="sxs-lookup"><span data-stu-id="b0121-259">Entry</span></span> | <span data-ttu-id="b0121-260">Valore</span><span class="sxs-lookup"><span data-stu-id="b0121-260">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="b0121-261">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="b0121-261">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="b0121-262">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b0121-262">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="b0121-263">System-Only</span><span class="sxs-lookup"><span data-stu-id="b0121-263">System-Only</span></span>            | <span data-ttu-id="b0121-264">Falso</span><span class="sxs-lookup"><span data-stu-id="b0121-264">False</span></span>                                                           |
| <span data-ttu-id="b0121-265">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="b0121-265">Is-Single-Valued</span></span>       | <span data-ttu-id="b0121-266">Vero</span><span class="sxs-lookup"><span data-stu-id="b0121-266">True</span></span>                                                            |
| <span data-ttu-id="b0121-267">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="b0121-267">Is Indexed</span></span>             | <span data-ttu-id="b0121-268">Falso</span><span class="sxs-lookup"><span data-stu-id="b0121-268">False</span></span>                                                           |
| <span data-ttu-id="b0121-269">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="b0121-269">In Global Catalog</span></span>      | <span data-ttu-id="b0121-270">Falso</span><span class="sxs-lookup"><span data-stu-id="b0121-270">False</span></span>                                                           |
| <span data-ttu-id="b0121-271">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="b0121-271">NT-Security-Descriptor</span></span> | <span data-ttu-id="b0121-272">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="b0121-272">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="b0121-273">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b0121-273">Range-Lower</span></span>            | <span data-ttu-id="b0121-274">36</span><span class="sxs-lookup"><span data-stu-id="b0121-274">36</span></span>                                                              |
| <span data-ttu-id="b0121-275">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b0121-275">Range-Upper</span></span>            | <span data-ttu-id="b0121-276">36</span><span class="sxs-lookup"><span data-stu-id="b0121-276">36</span></span>                                                              |
| <span data-ttu-id="b0121-277">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b0121-277">Search-Flags</span></span>           | <span data-ttu-id="b0121-278">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b0121-278">0x00000000</span></span>                                                      |
| <span data-ttu-id="b0121-279">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b0121-279">System-Flags</span></span>           | <span data-ttu-id="b0121-280">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b0121-280">0x00000010</span></span>                                                      |
| <span data-ttu-id="b0121-281">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="b0121-281">Classes used in</span></span>        | [<span data-ttu-id="b0121-282">**Controllo-accesso-a destra**</span><span class="sxs-lookup"><span data-stu-id="b0121-282">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b0121-283">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b0121-283">Windows Server 2012</span></span>



| <span data-ttu-id="b0121-284">Voce</span><span class="sxs-lookup"><span data-stu-id="b0121-284">Entry</span></span> | <span data-ttu-id="b0121-285">Valore</span><span class="sxs-lookup"><span data-stu-id="b0121-285">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="b0121-286">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="b0121-286">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="b0121-287">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b0121-287">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="b0121-288">System-Only</span><span class="sxs-lookup"><span data-stu-id="b0121-288">System-Only</span></span>            | <span data-ttu-id="b0121-289">Falso</span><span class="sxs-lookup"><span data-stu-id="b0121-289">False</span></span>                                                           |
| <span data-ttu-id="b0121-290">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="b0121-290">Is-Single-Valued</span></span>       | <span data-ttu-id="b0121-291">Vero</span><span class="sxs-lookup"><span data-stu-id="b0121-291">True</span></span>                                                            |
| <span data-ttu-id="b0121-292">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="b0121-292">Is Indexed</span></span>             | <span data-ttu-id="b0121-293">Falso</span><span class="sxs-lookup"><span data-stu-id="b0121-293">False</span></span>                                                           |
| <span data-ttu-id="b0121-294">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="b0121-294">In Global Catalog</span></span>      | <span data-ttu-id="b0121-295">Falso</span><span class="sxs-lookup"><span data-stu-id="b0121-295">False</span></span>                                                           |
| <span data-ttu-id="b0121-296">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="b0121-296">NT-Security-Descriptor</span></span> | <span data-ttu-id="b0121-297">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="b0121-297">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="b0121-298">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b0121-298">Range-Lower</span></span>            | <span data-ttu-id="b0121-299">36</span><span class="sxs-lookup"><span data-stu-id="b0121-299">36</span></span>                                                              |
| <span data-ttu-id="b0121-300">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b0121-300">Range-Upper</span></span>            | <span data-ttu-id="b0121-301">36</span><span class="sxs-lookup"><span data-stu-id="b0121-301">36</span></span>                                                              |
| <span data-ttu-id="b0121-302">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b0121-302">Search-Flags</span></span>           | <span data-ttu-id="b0121-303">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b0121-303">0x00000000</span></span>                                                      |
| <span data-ttu-id="b0121-304">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b0121-304">System-Flags</span></span>           | <span data-ttu-id="b0121-305">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b0121-305">0x00000010</span></span>                                                      |
| <span data-ttu-id="b0121-306">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="b0121-306">Classes used in</span></span>        | [<span data-ttu-id="b0121-307">**Controllo-accesso-a destra**</span><span class="sxs-lookup"><span data-stu-id="b0121-307">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



 

 





