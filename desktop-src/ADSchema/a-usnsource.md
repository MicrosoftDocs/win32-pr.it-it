---
title: Attributo USN-Source
description: Valore dell'attributo USN-Changed dell'oggetto dalla directory remota che ha replicato la modifica nel server locale.
ms.assetid: b307f84a-3ab1-4bfa-afc2-e74055f2a652
ms.tgt_platform: multiple
keywords:
- Schema AD USN-Source attribute
- Schema AD dell'attributo uSNSource
topic_type:
- apiref
api_name:
- USN-Source
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0998ffb73fc02511d77440550c8c669b35a98563
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104400976"
---
# <a name="usn-source-attribute"></a><span data-ttu-id="9c5f0-105">Attributo USN-Source</span><span class="sxs-lookup"><span data-stu-id="9c5f0-105">USN-Source attribute</span></span>

<span data-ttu-id="9c5f0-106">Valore dell'attributo [**USN-changed**](a-usnchanged.md) dell'oggetto dalla directory remota che ha replicato la modifica nel server locale.</span><span class="sxs-lookup"><span data-stu-id="9c5f0-106">Value of the [**USN-Changed**](a-usnchanged.md) attribute of the object from the remote directory that replicated the change to the local server.</span></span>



| <span data-ttu-id="9c5f0-107">Voce</span><span class="sxs-lookup"><span data-stu-id="9c5f0-107">Entry</span></span> | <span data-ttu-id="9c5f0-108">Valore</span><span class="sxs-lookup"><span data-stu-id="9c5f0-108">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c5f0-109">CN</span><span class="sxs-lookup"><span data-stu-id="9c5f0-109">CN</span></span>                | <span data-ttu-id="9c5f0-110">USN-Source</span><span class="sxs-lookup"><span data-stu-id="9c5f0-110">USN-Source</span></span>                                                                                          |
| <span data-ttu-id="9c5f0-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="9c5f0-111">Ldap-Display-Name</span></span> | <span data-ttu-id="9c5f0-112">uSNSource</span><span class="sxs-lookup"><span data-stu-id="9c5f0-112">uSNSource</span></span>                                                                                           |
| <span data-ttu-id="9c5f0-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="9c5f0-113">Size</span></span>              | <span data-ttu-id="9c5f0-114">8 byte</span><span class="sxs-lookup"><span data-stu-id="9c5f0-114">8 bytes</span></span>                                                                                             |
| <span data-ttu-id="9c5f0-115">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="9c5f0-115">Update Privilege</span></span>  | <span data-ttu-id="9c5f0-116">Questo valore viene impostato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="9c5f0-116">This value is set by the system.</span></span>                                                                    |
| <span data-ttu-id="9c5f0-117">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="9c5f0-117">Update Frequency</span></span>  | <span data-ttu-id="9c5f0-118">Quando l'oggetto viene modificato in una directory remota che ha replicato la modifica alla directory locale.</span><span class="sxs-lookup"><span data-stu-id="9c5f0-118">When the object is changed on a remote directory that replicated the change to the local directory.</span></span> |
| <span data-ttu-id="9c5f0-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="9c5f0-119">Attribute-Id</span></span>      | <span data-ttu-id="9c5f0-120">1.2.840.113556.1.4.896</span><span class="sxs-lookup"><span data-stu-id="9c5f0-120">1.2.840.113556.1.4.896</span></span>                                                                              |
| <span data-ttu-id="9c5f0-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="9c5f0-121">System-Id-Guid</span></span>    | <span data-ttu-id="9c5f0-122">167758ad-47f3-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="9c5f0-122">167758ad-47f3-11d1-a9c3-0000f80367c1</span></span>                                                                |
| <span data-ttu-id="9c5f0-123">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9c5f0-123">Syntax</span></span>            | [<span data-ttu-id="9c5f0-124">**Interval**</span><span class="sxs-lookup"><span data-stu-id="9c5f0-124">**Interval**</span></span>](s-interval.md)                                                                      |



## <a name="implementations"></a><span data-ttu-id="9c5f0-125">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="9c5f0-125">Implementations</span></span>

-   [<span data-ttu-id="9c5f0-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="9c5f0-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="9c5f0-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="9c5f0-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="9c5f0-128">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="9c5f0-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="9c5f0-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="9c5f0-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="9c5f0-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="9c5f0-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="9c5f0-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="9c5f0-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="9c5f0-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="9c5f0-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="9c5f0-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9c5f0-133">Windows 2000 Server</span></span>



| <span data-ttu-id="9c5f0-134">Voce</span><span class="sxs-lookup"><span data-stu-id="9c5f0-134">Entry</span></span> | <span data-ttu-id="9c5f0-135">Valore</span><span class="sxs-lookup"><span data-stu-id="9c5f0-135">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="9c5f0-136">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="9c5f0-136">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="9c5f0-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9c5f0-137">MAPI-Id</span></span>                | <span data-ttu-id="9c5f0-138">0x8157</span><span class="sxs-lookup"><span data-stu-id="9c5f0-138">0x8157</span></span>                          |
| <span data-ttu-id="9c5f0-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="9c5f0-139">System-Only</span></span>            | <span data-ttu-id="9c5f0-140">Falso</span><span class="sxs-lookup"><span data-stu-id="9c5f0-140">False</span></span>                           |
| <span data-ttu-id="9c5f0-141">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="9c5f0-141">Is-Single-Valued</span></span>       | <span data-ttu-id="9c5f0-142">Vero</span><span class="sxs-lookup"><span data-stu-id="9c5f0-142">True</span></span>                            |
| <span data-ttu-id="9c5f0-143">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="9c5f0-143">Is Indexed</span></span>             | <span data-ttu-id="9c5f0-144">Falso</span><span class="sxs-lookup"><span data-stu-id="9c5f0-144">False</span></span>                           |
| <span data-ttu-id="9c5f0-145">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="9c5f0-145">In Global Catalog</span></span>      | <span data-ttu-id="9c5f0-146">Falso</span><span class="sxs-lookup"><span data-stu-id="9c5f0-146">False</span></span>                           |
| <span data-ttu-id="9c5f0-147">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="9c5f0-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="9c5f0-148">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="9c5f0-148">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="9c5f0-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9c5f0-149">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="9c5f0-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9c5f0-150">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="9c5f0-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9c5f0-151">Search-Flags</span></span>           | <span data-ttu-id="9c5f0-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9c5f0-152">0x00000000</span></span>                      |
| <span data-ttu-id="9c5f0-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9c5f0-153">System-Flags</span></span>           | <span data-ttu-id="9c5f0-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9c5f0-154">0x00000010</span></span>                      |
| <span data-ttu-id="9c5f0-155">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="9c5f0-155">Classes used in</span></span>        | [<span data-ttu-id="9c5f0-156">**In alto**</span><span class="sxs-lookup"><span data-stu-id="9c5f0-156">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="9c5f0-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9c5f0-157">Windows Server 2003</span></span>



| <span data-ttu-id="9c5f0-158">Voce</span><span class="sxs-lookup"><span data-stu-id="9c5f0-158">Entry</span></span> | <span data-ttu-id="9c5f0-159">Valore</span><span class="sxs-lookup"><span data-stu-id="9c5f0-159">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="9c5f0-160">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="9c5f0-160">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="9c5f0-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9c5f0-161">MAPI-Id</span></span>                | <span data-ttu-id="9c5f0-162">0x8157</span><span class="sxs-lookup"><span data-stu-id="9c5f0-162">0x8157</span></span>                          |
| <span data-ttu-id="9c5f0-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="9c5f0-163">System-Only</span></span>            | <span data-ttu-id="9c5f0-164">Falso</span><span class="sxs-lookup"><span data-stu-id="9c5f0-164">False</span></span>                           |
| <span data-ttu-id="9c5f0-165">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="9c5f0-165">Is-Single-Valued</span></span>       | <span data-ttu-id="9c5f0-166">Vero</span><span class="sxs-lookup"><span data-stu-id="9c5f0-166">True</span></span>                            |
| <span data-ttu-id="9c5f0-167">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="9c5f0-167">Is Indexed</span></span>             | <span data-ttu-id="9c5f0-168">Falso</span><span class="sxs-lookup"><span data-stu-id="9c5f0-168">False</span></span>                           |
| <span data-ttu-id="9c5f0-169">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="9c5f0-169">In Global Catalog</span></span>      | <span data-ttu-id="9c5f0-170">Falso</span><span class="sxs-lookup"><span data-stu-id="9c5f0-170">False</span></span>                           |
| <span data-ttu-id="9c5f0-171">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="9c5f0-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="9c5f0-172">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="9c5f0-172">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="9c5f0-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9c5f0-173">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="9c5f0-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9c5f0-174">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="9c5f0-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9c5f0-175">Search-Flags</span></span>           | <span data-ttu-id="9c5f0-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9c5f0-176">0x00000000</span></span>                      |
| <span data-ttu-id="9c5f0-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9c5f0-177">System-Flags</span></span>           | <span data-ttu-id="9c5f0-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9c5f0-178">0x00000010</span></span>                      |
| <span data-ttu-id="9c5f0-179">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="9c5f0-179">Classes used in</span></span>        | [<span data-ttu-id="9c5f0-180">**In alto**</span><span class="sxs-lookup"><span data-stu-id="9c5f0-180">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="9c5f0-181">ADAM</span><span class="sxs-lookup"><span data-stu-id="9c5f0-181">ADAM</span></span>



| <span data-ttu-id="9c5f0-182">Voce</span><span class="sxs-lookup"><span data-stu-id="9c5f0-182">Entry</span></span> | <span data-ttu-id="9c5f0-183">Valore</span><span class="sxs-lookup"><span data-stu-id="9c5f0-183">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="9c5f0-184">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="9c5f0-184">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="9c5f0-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9c5f0-185">MAPI-Id</span></span>                | <span data-ttu-id="9c5f0-186">0x8157</span><span class="sxs-lookup"><span data-stu-id="9c5f0-186">0x8157</span></span>                          |
| <span data-ttu-id="9c5f0-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="9c5f0-187">System-Only</span></span>            | <span data-ttu-id="9c5f0-188">Falso</span><span class="sxs-lookup"><span data-stu-id="9c5f0-188">False</span></span>                           |
| <span data-ttu-id="9c5f0-189">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="9c5f0-189">Is-Single-Valued</span></span>       | <span data-ttu-id="9c5f0-190">Vero</span><span class="sxs-lookup"><span data-stu-id="9c5f0-190">True</span></span>                            |
| <span data-ttu-id="9c5f0-191">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="9c5f0-191">Is Indexed</span></span>             | <span data-ttu-id="9c5f0-192">Falso</span><span class="sxs-lookup"><span data-stu-id="9c5f0-192">False</span></span>                           |
| <span data-ttu-id="9c5f0-193">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="9c5f0-193">In Global Catalog</span></span>      | <span data-ttu-id="9c5f0-194">Falso</span><span class="sxs-lookup"><span data-stu-id="9c5f0-194">False</span></span>                           |
| <span data-ttu-id="9c5f0-195">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="9c5f0-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="9c5f0-196">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="9c5f0-196">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="9c5f0-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9c5f0-197">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="9c5f0-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9c5f0-198">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="9c5f0-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9c5f0-199">Search-Flags</span></span>           | <span data-ttu-id="9c5f0-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9c5f0-200">0x00000000</span></span>                      |
| <span data-ttu-id="9c5f0-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9c5f0-201">System-Flags</span></span>           | <span data-ttu-id="9c5f0-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9c5f0-202">0x00000010</span></span>                      |
| <span data-ttu-id="9c5f0-203">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="9c5f0-203">Classes used in</span></span>        | [<span data-ttu-id="9c5f0-204">**In alto**</span><span class="sxs-lookup"><span data-stu-id="9c5f0-204">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="9c5f0-205">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="9c5f0-205">Windows Server 2003 R2</span></span>



| <span data-ttu-id="9c5f0-206">Voce</span><span class="sxs-lookup"><span data-stu-id="9c5f0-206">Entry</span></span> | <span data-ttu-id="9c5f0-207">Valore</span><span class="sxs-lookup"><span data-stu-id="9c5f0-207">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="9c5f0-208">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="9c5f0-208">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="9c5f0-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9c5f0-209">MAPI-Id</span></span>                | <span data-ttu-id="9c5f0-210">0x8157</span><span class="sxs-lookup"><span data-stu-id="9c5f0-210">0x8157</span></span>                          |
| <span data-ttu-id="9c5f0-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="9c5f0-211">System-Only</span></span>            | <span data-ttu-id="9c5f0-212">Falso</span><span class="sxs-lookup"><span data-stu-id="9c5f0-212">False</span></span>                           |
| <span data-ttu-id="9c5f0-213">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="9c5f0-213">Is-Single-Valued</span></span>       | <span data-ttu-id="9c5f0-214">Vero</span><span class="sxs-lookup"><span data-stu-id="9c5f0-214">True</span></span>                            |
| <span data-ttu-id="9c5f0-215">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="9c5f0-215">Is Indexed</span></span>             | <span data-ttu-id="9c5f0-216">Falso</span><span class="sxs-lookup"><span data-stu-id="9c5f0-216">False</span></span>                           |
| <span data-ttu-id="9c5f0-217">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="9c5f0-217">In Global Catalog</span></span>      | <span data-ttu-id="9c5f0-218">Falso</span><span class="sxs-lookup"><span data-stu-id="9c5f0-218">False</span></span>                           |
| <span data-ttu-id="9c5f0-219">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="9c5f0-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="9c5f0-220">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="9c5f0-220">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="9c5f0-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9c5f0-221">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="9c5f0-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9c5f0-222">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="9c5f0-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9c5f0-223">Search-Flags</span></span>           | <span data-ttu-id="9c5f0-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9c5f0-224">0x00000000</span></span>                      |
| <span data-ttu-id="9c5f0-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9c5f0-225">System-Flags</span></span>           | <span data-ttu-id="9c5f0-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9c5f0-226">0x00000010</span></span>                      |
| <span data-ttu-id="9c5f0-227">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="9c5f0-227">Classes used in</span></span>        | [<span data-ttu-id="9c5f0-228">**In alto**</span><span class="sxs-lookup"><span data-stu-id="9c5f0-228">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="9c5f0-229">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9c5f0-229">Windows Server 2008</span></span>



| <span data-ttu-id="9c5f0-230">Voce</span><span class="sxs-lookup"><span data-stu-id="9c5f0-230">Entry</span></span> | <span data-ttu-id="9c5f0-231">Valore</span><span class="sxs-lookup"><span data-stu-id="9c5f0-231">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="9c5f0-232">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="9c5f0-232">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="9c5f0-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9c5f0-233">MAPI-Id</span></span>                | <span data-ttu-id="9c5f0-234">0x8157</span><span class="sxs-lookup"><span data-stu-id="9c5f0-234">0x8157</span></span>                          |
| <span data-ttu-id="9c5f0-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="9c5f0-235">System-Only</span></span>            | <span data-ttu-id="9c5f0-236">Falso</span><span class="sxs-lookup"><span data-stu-id="9c5f0-236">False</span></span>                           |
| <span data-ttu-id="9c5f0-237">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="9c5f0-237">Is-Single-Valued</span></span>       | <span data-ttu-id="9c5f0-238">Vero</span><span class="sxs-lookup"><span data-stu-id="9c5f0-238">True</span></span>                            |
| <span data-ttu-id="9c5f0-239">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="9c5f0-239">Is Indexed</span></span>             | <span data-ttu-id="9c5f0-240">Falso</span><span class="sxs-lookup"><span data-stu-id="9c5f0-240">False</span></span>                           |
| <span data-ttu-id="9c5f0-241">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="9c5f0-241">In Global Catalog</span></span>      | <span data-ttu-id="9c5f0-242">Falso</span><span class="sxs-lookup"><span data-stu-id="9c5f0-242">False</span></span>                           |
| <span data-ttu-id="9c5f0-243">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="9c5f0-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="9c5f0-244">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="9c5f0-244">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="9c5f0-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9c5f0-245">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="9c5f0-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9c5f0-246">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="9c5f0-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9c5f0-247">Search-Flags</span></span>           | <span data-ttu-id="9c5f0-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9c5f0-248">0x00000000</span></span>                      |
| <span data-ttu-id="9c5f0-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9c5f0-249">System-Flags</span></span>           | <span data-ttu-id="9c5f0-250">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9c5f0-250">0x00000010</span></span>                      |
| <span data-ttu-id="9c5f0-251">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="9c5f0-251">Classes used in</span></span>        | [<span data-ttu-id="9c5f0-252">**In alto**</span><span class="sxs-lookup"><span data-stu-id="9c5f0-252">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="9c5f0-253">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9c5f0-253">Windows Server 2008 R2</span></span>



| <span data-ttu-id="9c5f0-254">Voce</span><span class="sxs-lookup"><span data-stu-id="9c5f0-254">Entry</span></span> | <span data-ttu-id="9c5f0-255">Valore</span><span class="sxs-lookup"><span data-stu-id="9c5f0-255">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="9c5f0-256">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="9c5f0-256">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="9c5f0-257">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9c5f0-257">MAPI-Id</span></span>                | <span data-ttu-id="9c5f0-258">0x8157</span><span class="sxs-lookup"><span data-stu-id="9c5f0-258">0x8157</span></span>                          |
| <span data-ttu-id="9c5f0-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="9c5f0-259">System-Only</span></span>            | <span data-ttu-id="9c5f0-260">Falso</span><span class="sxs-lookup"><span data-stu-id="9c5f0-260">False</span></span>                           |
| <span data-ttu-id="9c5f0-261">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="9c5f0-261">Is-Single-Valued</span></span>       | <span data-ttu-id="9c5f0-262">Vero</span><span class="sxs-lookup"><span data-stu-id="9c5f0-262">True</span></span>                            |
| <span data-ttu-id="9c5f0-263">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="9c5f0-263">Is Indexed</span></span>             | <span data-ttu-id="9c5f0-264">Falso</span><span class="sxs-lookup"><span data-stu-id="9c5f0-264">False</span></span>                           |
| <span data-ttu-id="9c5f0-265">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="9c5f0-265">In Global Catalog</span></span>      | <span data-ttu-id="9c5f0-266">Falso</span><span class="sxs-lookup"><span data-stu-id="9c5f0-266">False</span></span>                           |
| <span data-ttu-id="9c5f0-267">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="9c5f0-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="9c5f0-268">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="9c5f0-268">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="9c5f0-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9c5f0-269">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="9c5f0-270">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9c5f0-270">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="9c5f0-271">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9c5f0-271">Search-Flags</span></span>           | <span data-ttu-id="9c5f0-272">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9c5f0-272">0x00000000</span></span>                      |
| <span data-ttu-id="9c5f0-273">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9c5f0-273">System-Flags</span></span>           | <span data-ttu-id="9c5f0-274">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9c5f0-274">0x00000010</span></span>                      |
| <span data-ttu-id="9c5f0-275">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="9c5f0-275">Classes used in</span></span>        | [<span data-ttu-id="9c5f0-276">**In alto**</span><span class="sxs-lookup"><span data-stu-id="9c5f0-276">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="9c5f0-277">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9c5f0-277">Windows Server 2012</span></span>



| <span data-ttu-id="9c5f0-278">Voce</span><span class="sxs-lookup"><span data-stu-id="9c5f0-278">Entry</span></span> | <span data-ttu-id="9c5f0-279">Valore</span><span class="sxs-lookup"><span data-stu-id="9c5f0-279">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="9c5f0-280">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="9c5f0-280">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="9c5f0-281">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9c5f0-281">MAPI-Id</span></span>                | <span data-ttu-id="9c5f0-282">0x8157</span><span class="sxs-lookup"><span data-stu-id="9c5f0-282">0x8157</span></span>                          |
| <span data-ttu-id="9c5f0-283">System-Only</span><span class="sxs-lookup"><span data-stu-id="9c5f0-283">System-Only</span></span>            | <span data-ttu-id="9c5f0-284">Falso</span><span class="sxs-lookup"><span data-stu-id="9c5f0-284">False</span></span>                           |
| <span data-ttu-id="9c5f0-285">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="9c5f0-285">Is-Single-Valued</span></span>       | <span data-ttu-id="9c5f0-286">Vero</span><span class="sxs-lookup"><span data-stu-id="9c5f0-286">True</span></span>                            |
| <span data-ttu-id="9c5f0-287">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="9c5f0-287">Is Indexed</span></span>             | <span data-ttu-id="9c5f0-288">Falso</span><span class="sxs-lookup"><span data-stu-id="9c5f0-288">False</span></span>                           |
| <span data-ttu-id="9c5f0-289">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="9c5f0-289">In Global Catalog</span></span>      | <span data-ttu-id="9c5f0-290">Falso</span><span class="sxs-lookup"><span data-stu-id="9c5f0-290">False</span></span>                           |
| <span data-ttu-id="9c5f0-291">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="9c5f0-291">NT-Security-Descriptor</span></span> | <span data-ttu-id="9c5f0-292">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="9c5f0-292">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="9c5f0-293">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9c5f0-293">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="9c5f0-294">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9c5f0-294">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="9c5f0-295">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9c5f0-295">Search-Flags</span></span>           | <span data-ttu-id="9c5f0-296">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9c5f0-296">0x00000000</span></span>                      |
| <span data-ttu-id="9c5f0-297">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9c5f0-297">System-Flags</span></span>           | <span data-ttu-id="9c5f0-298">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9c5f0-298">0x00000010</span></span>                      |
| <span data-ttu-id="9c5f0-299">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="9c5f0-299">Classes used in</span></span>        | [<span data-ttu-id="9c5f0-300">**In alto**</span><span class="sxs-lookup"><span data-stu-id="9c5f0-300">**Top**</span></span>](c-top.md)<br/> |



 

 





