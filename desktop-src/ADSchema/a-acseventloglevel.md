---
title: ACS-attributo a livello di log eventi
description: Livello di registrazione RSVP.
ms.assetid: 2f3c645d-a064-40fb-965c-388b2fac61bc
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo ACS-Event-a livello di log
- Schema AD dell'attributo aCSEventLogLevel
topic_type:
- apiref
api_name:
- ACS-Event-Log-Level
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62bb5701f665a3685845368eb2adc72fc33d10bd
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744426"
---
# <a name="acs-event-log-level-attribute"></a><span data-ttu-id="9d006-105">ACS-attributo a livello di log eventi</span><span class="sxs-lookup"><span data-stu-id="9d006-105">ACS-Event-Log-Level attribute</span></span>

<span data-ttu-id="9d006-106">Livello di registrazione RSVP.</span><span class="sxs-lookup"><span data-stu-id="9d006-106">RSVP logging level.</span></span>



| <span data-ttu-id="9d006-107">Voce</span><span class="sxs-lookup"><span data-stu-id="9d006-107">Entry</span></span> | <span data-ttu-id="9d006-108">Valore</span><span class="sxs-lookup"><span data-stu-id="9d006-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="9d006-109">CN</span><span class="sxs-lookup"><span data-stu-id="9d006-109">CN</span></span>                | <span data-ttu-id="9d006-110">ACS-a livello di registro eventi</span><span class="sxs-lookup"><span data-stu-id="9d006-110">ACS-Event-Log-Level</span></span>                     |
| <span data-ttu-id="9d006-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="9d006-111">Ldap-Display-Name</span></span> | <span data-ttu-id="9d006-112">aCSEventLogLevel</span><span class="sxs-lookup"><span data-stu-id="9d006-112">aCSEventLogLevel</span></span>                        |
| <span data-ttu-id="9d006-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="9d006-113">Size</span></span>              | <span data-ttu-id="9d006-114">i valori di 4 byte possono essere 0, 1, 2 e 3.</span><span class="sxs-lookup"><span data-stu-id="9d006-114">4 bytes can have values 0, 1, 2, and 3.</span></span> |
| <span data-ttu-id="9d006-115">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="9d006-115">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="9d006-116">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="9d006-116">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="9d006-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="9d006-117">Attribute-Id</span></span>      | <span data-ttu-id="9d006-118">1.2.840.113556.1.4.769</span><span class="sxs-lookup"><span data-stu-id="9d006-118">1.2.840.113556.1.4.769</span></span>                  |
| <span data-ttu-id="9d006-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="9d006-119">System-Id-Guid</span></span>    | <span data-ttu-id="9d006-120">7f561286-5301-11d1-a9c5-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="9d006-120">7f561286-5301-11d1-a9c5-0000f80367c1</span></span>    |
| <span data-ttu-id="9d006-121">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9d006-121">Syntax</span></span>            | [<span data-ttu-id="9d006-122">**Enumerazione**</span><span class="sxs-lookup"><span data-stu-id="9d006-122">**Enumeration**</span></span>](s-enumeration.md)    |



## <a name="implementations"></a><span data-ttu-id="9d006-123">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="9d006-123">Implementations</span></span>

-   [<span data-ttu-id="9d006-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="9d006-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="9d006-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="9d006-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="9d006-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="9d006-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="9d006-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="9d006-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="9d006-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="9d006-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="9d006-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="9d006-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="9d006-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9d006-130">Windows 2000 Server</span></span>



| <span data-ttu-id="9d006-131">Voce</span><span class="sxs-lookup"><span data-stu-id="9d006-131">Entry</span></span> | <span data-ttu-id="9d006-132">Valore</span><span class="sxs-lookup"><span data-stu-id="9d006-132">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="9d006-133">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="9d006-133">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="9d006-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9d006-134">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="9d006-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="9d006-135">System-Only</span></span>            | <span data-ttu-id="9d006-136">Falso</span><span class="sxs-lookup"><span data-stu-id="9d006-136">False</span></span>                                        |
| <span data-ttu-id="9d006-137">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="9d006-137">Is-Single-Valued</span></span>       | <span data-ttu-id="9d006-138">Vero</span><span class="sxs-lookup"><span data-stu-id="9d006-138">True</span></span>                                         |
| <span data-ttu-id="9d006-139">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="9d006-139">Is Indexed</span></span>             | <span data-ttu-id="9d006-140">Falso</span><span class="sxs-lookup"><span data-stu-id="9d006-140">False</span></span>                                        |
| <span data-ttu-id="9d006-141">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="9d006-141">In Global Catalog</span></span>      | <span data-ttu-id="9d006-142">Falso</span><span class="sxs-lookup"><span data-stu-id="9d006-142">False</span></span>                                        |
| <span data-ttu-id="9d006-143">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="9d006-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="9d006-144">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="9d006-144">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="9d006-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9d006-145">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="9d006-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9d006-146">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="9d006-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9d006-147">Search-Flags</span></span>           | <span data-ttu-id="9d006-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9d006-148">0x00000000</span></span>                                   |
| <span data-ttu-id="9d006-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9d006-149">System-Flags</span></span>           | <span data-ttu-id="9d006-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9d006-150">0x00000010</span></span>                                   |
| <span data-ttu-id="9d006-151">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="9d006-151">Classes used in</span></span>        | [<span data-ttu-id="9d006-152">**ACS-subnet**</span><span class="sxs-lookup"><span data-stu-id="9d006-152">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="9d006-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9d006-153">Windows Server 2003</span></span>



| <span data-ttu-id="9d006-154">Voce</span><span class="sxs-lookup"><span data-stu-id="9d006-154">Entry</span></span> | <span data-ttu-id="9d006-155">Valore</span><span class="sxs-lookup"><span data-stu-id="9d006-155">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="9d006-156">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="9d006-156">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="9d006-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9d006-157">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="9d006-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="9d006-158">System-Only</span></span>            | <span data-ttu-id="9d006-159">Falso</span><span class="sxs-lookup"><span data-stu-id="9d006-159">False</span></span>                                        |
| <span data-ttu-id="9d006-160">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="9d006-160">Is-Single-Valued</span></span>       | <span data-ttu-id="9d006-161">Vero</span><span class="sxs-lookup"><span data-stu-id="9d006-161">True</span></span>                                         |
| <span data-ttu-id="9d006-162">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="9d006-162">Is Indexed</span></span>             | <span data-ttu-id="9d006-163">Falso</span><span class="sxs-lookup"><span data-stu-id="9d006-163">False</span></span>                                        |
| <span data-ttu-id="9d006-164">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="9d006-164">In Global Catalog</span></span>      | <span data-ttu-id="9d006-165">Falso</span><span class="sxs-lookup"><span data-stu-id="9d006-165">False</span></span>                                        |
| <span data-ttu-id="9d006-166">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="9d006-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="9d006-167">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="9d006-167">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="9d006-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9d006-168">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="9d006-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9d006-169">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="9d006-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9d006-170">Search-Flags</span></span>           | <span data-ttu-id="9d006-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9d006-171">0x00000000</span></span>                                   |
| <span data-ttu-id="9d006-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9d006-172">System-Flags</span></span>           | <span data-ttu-id="9d006-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9d006-173">0x00000010</span></span>                                   |
| <span data-ttu-id="9d006-174">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="9d006-174">Classes used in</span></span>        | [<span data-ttu-id="9d006-175">**ACS-subnet**</span><span class="sxs-lookup"><span data-stu-id="9d006-175">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="9d006-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="9d006-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="9d006-177">Voce</span><span class="sxs-lookup"><span data-stu-id="9d006-177">Entry</span></span> | <span data-ttu-id="9d006-178">Valore</span><span class="sxs-lookup"><span data-stu-id="9d006-178">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="9d006-179">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="9d006-179">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="9d006-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9d006-180">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="9d006-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="9d006-181">System-Only</span></span>            | <span data-ttu-id="9d006-182">Falso</span><span class="sxs-lookup"><span data-stu-id="9d006-182">False</span></span>                                        |
| <span data-ttu-id="9d006-183">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="9d006-183">Is-Single-Valued</span></span>       | <span data-ttu-id="9d006-184">Vero</span><span class="sxs-lookup"><span data-stu-id="9d006-184">True</span></span>                                         |
| <span data-ttu-id="9d006-185">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="9d006-185">Is Indexed</span></span>             | <span data-ttu-id="9d006-186">Falso</span><span class="sxs-lookup"><span data-stu-id="9d006-186">False</span></span>                                        |
| <span data-ttu-id="9d006-187">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="9d006-187">In Global Catalog</span></span>      | <span data-ttu-id="9d006-188">Falso</span><span class="sxs-lookup"><span data-stu-id="9d006-188">False</span></span>                                        |
| <span data-ttu-id="9d006-189">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="9d006-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="9d006-190">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="9d006-190">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="9d006-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9d006-191">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="9d006-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9d006-192">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="9d006-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9d006-193">Search-Flags</span></span>           | <span data-ttu-id="9d006-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9d006-194">0x00000000</span></span>                                   |
| <span data-ttu-id="9d006-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9d006-195">System-Flags</span></span>           | <span data-ttu-id="9d006-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9d006-196">0x00000010</span></span>                                   |
| <span data-ttu-id="9d006-197">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="9d006-197">Classes used in</span></span>        | [<span data-ttu-id="9d006-198">**ACS-subnet**</span><span class="sxs-lookup"><span data-stu-id="9d006-198">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="9d006-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9d006-199">Windows Server 2008</span></span>



| <span data-ttu-id="9d006-200">Voce</span><span class="sxs-lookup"><span data-stu-id="9d006-200">Entry</span></span> | <span data-ttu-id="9d006-201">Valore</span><span class="sxs-lookup"><span data-stu-id="9d006-201">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="9d006-202">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="9d006-202">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="9d006-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9d006-203">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="9d006-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="9d006-204">System-Only</span></span>            | <span data-ttu-id="9d006-205">Falso</span><span class="sxs-lookup"><span data-stu-id="9d006-205">False</span></span>                                        |
| <span data-ttu-id="9d006-206">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="9d006-206">Is-Single-Valued</span></span>       | <span data-ttu-id="9d006-207">Vero</span><span class="sxs-lookup"><span data-stu-id="9d006-207">True</span></span>                                         |
| <span data-ttu-id="9d006-208">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="9d006-208">Is Indexed</span></span>             | <span data-ttu-id="9d006-209">Falso</span><span class="sxs-lookup"><span data-stu-id="9d006-209">False</span></span>                                        |
| <span data-ttu-id="9d006-210">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="9d006-210">In Global Catalog</span></span>      | <span data-ttu-id="9d006-211">Falso</span><span class="sxs-lookup"><span data-stu-id="9d006-211">False</span></span>                                        |
| <span data-ttu-id="9d006-212">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="9d006-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="9d006-213">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="9d006-213">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="9d006-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9d006-214">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="9d006-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9d006-215">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="9d006-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9d006-216">Search-Flags</span></span>           | <span data-ttu-id="9d006-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9d006-217">0x00000000</span></span>                                   |
| <span data-ttu-id="9d006-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9d006-218">System-Flags</span></span>           | <span data-ttu-id="9d006-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9d006-219">0x00000010</span></span>                                   |
| <span data-ttu-id="9d006-220">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="9d006-220">Classes used in</span></span>        | [<span data-ttu-id="9d006-221">**ACS-subnet**</span><span class="sxs-lookup"><span data-stu-id="9d006-221">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="9d006-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9d006-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="9d006-223">Voce</span><span class="sxs-lookup"><span data-stu-id="9d006-223">Entry</span></span> | <span data-ttu-id="9d006-224">Valore</span><span class="sxs-lookup"><span data-stu-id="9d006-224">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="9d006-225">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="9d006-225">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="9d006-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9d006-226">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="9d006-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="9d006-227">System-Only</span></span>            | <span data-ttu-id="9d006-228">Falso</span><span class="sxs-lookup"><span data-stu-id="9d006-228">False</span></span>                                        |
| <span data-ttu-id="9d006-229">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="9d006-229">Is-Single-Valued</span></span>       | <span data-ttu-id="9d006-230">Vero</span><span class="sxs-lookup"><span data-stu-id="9d006-230">True</span></span>                                         |
| <span data-ttu-id="9d006-231">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="9d006-231">Is Indexed</span></span>             | <span data-ttu-id="9d006-232">Falso</span><span class="sxs-lookup"><span data-stu-id="9d006-232">False</span></span>                                        |
| <span data-ttu-id="9d006-233">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="9d006-233">In Global Catalog</span></span>      | <span data-ttu-id="9d006-234">Falso</span><span class="sxs-lookup"><span data-stu-id="9d006-234">False</span></span>                                        |
| <span data-ttu-id="9d006-235">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="9d006-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="9d006-236">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="9d006-236">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="9d006-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9d006-237">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="9d006-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9d006-238">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="9d006-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9d006-239">Search-Flags</span></span>           | <span data-ttu-id="9d006-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9d006-240">0x00000000</span></span>                                   |
| <span data-ttu-id="9d006-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9d006-241">System-Flags</span></span>           | <span data-ttu-id="9d006-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9d006-242">0x00000010</span></span>                                   |
| <span data-ttu-id="9d006-243">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="9d006-243">Classes used in</span></span>        | [<span data-ttu-id="9d006-244">**ACS-subnet**</span><span class="sxs-lookup"><span data-stu-id="9d006-244">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="9d006-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9d006-245">Windows Server 2012</span></span>



| <span data-ttu-id="9d006-246">Voce</span><span class="sxs-lookup"><span data-stu-id="9d006-246">Entry</span></span> | <span data-ttu-id="9d006-247">Valore</span><span class="sxs-lookup"><span data-stu-id="9d006-247">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="9d006-248">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="9d006-248">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="9d006-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9d006-249">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="9d006-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="9d006-250">System-Only</span></span>            | <span data-ttu-id="9d006-251">Falso</span><span class="sxs-lookup"><span data-stu-id="9d006-251">False</span></span>                                        |
| <span data-ttu-id="9d006-252">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="9d006-252">Is-Single-Valued</span></span>       | <span data-ttu-id="9d006-253">Vero</span><span class="sxs-lookup"><span data-stu-id="9d006-253">True</span></span>                                         |
| <span data-ttu-id="9d006-254">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="9d006-254">Is Indexed</span></span>             | <span data-ttu-id="9d006-255">Falso</span><span class="sxs-lookup"><span data-stu-id="9d006-255">False</span></span>                                        |
| <span data-ttu-id="9d006-256">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="9d006-256">In Global Catalog</span></span>      | <span data-ttu-id="9d006-257">Falso</span><span class="sxs-lookup"><span data-stu-id="9d006-257">False</span></span>                                        |
| <span data-ttu-id="9d006-258">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="9d006-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="9d006-259">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="9d006-259">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="9d006-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9d006-260">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="9d006-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9d006-261">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="9d006-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9d006-262">Search-Flags</span></span>           | <span data-ttu-id="9d006-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9d006-263">0x00000000</span></span>                                   |
| <span data-ttu-id="9d006-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9d006-264">System-Flags</span></span>           | <span data-ttu-id="9d006-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9d006-265">0x00000010</span></span>                                   |
| <span data-ttu-id="9d006-266">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="9d006-266">Classes used in</span></span>        | [<span data-ttu-id="9d006-267">**ACS-subnet**</span><span class="sxs-lookup"><span data-stu-id="9d006-267">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



 

 





