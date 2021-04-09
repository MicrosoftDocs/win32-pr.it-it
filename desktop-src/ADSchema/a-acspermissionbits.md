---
title: ACS-autorizzazione-bits (attributo)
description: Consente l'origine del flusso multicast per un determinato utente.
ms.assetid: c7e7866d-b906-4a64-bd51-4e9cc7b8fb86
ms.tgt_platform: multiple
keywords:
- ACS-autorizzazione-bits attributo AD schema
- Schema AD dell'attributo aCSPermissionBits
topic_type:
- apiref
api_name:
- ACS-Permission-Bits
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a27370178dd46fd50df44b1226686db5a70a846
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104122199"
---
# <a name="acs-permission-bits-attribute"></a><span data-ttu-id="c6a5b-105">ACS-autorizzazione-bits (attributo)</span><span class="sxs-lookup"><span data-stu-id="c6a5b-105">ACS-Permission-Bits attribute</span></span>

<span data-ttu-id="c6a5b-106">Consente l'origine del flusso multicast per un determinato utente.</span><span class="sxs-lookup"><span data-stu-id="c6a5b-106">Allows multicast flow origination for a given user.</span></span>



| <span data-ttu-id="c6a5b-107">Voce</span><span class="sxs-lookup"><span data-stu-id="c6a5b-107">Entry</span></span> | <span data-ttu-id="c6a5b-108">Valore</span><span class="sxs-lookup"><span data-stu-id="c6a5b-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="c6a5b-109">CN</span><span class="sxs-lookup"><span data-stu-id="c6a5b-109">CN</span></span>                | <span data-ttu-id="c6a5b-110">ACS-autorizzazioni-BITS</span><span class="sxs-lookup"><span data-stu-id="c6a5b-110">ACS-Permission-Bits</span></span>                  |
| <span data-ttu-id="c6a5b-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="c6a5b-111">Ldap-Display-Name</span></span> | <span data-ttu-id="c6a5b-112">aCSPermissionBits</span><span class="sxs-lookup"><span data-stu-id="c6a5b-112">aCSPermissionBits</span></span>                    |
| <span data-ttu-id="c6a5b-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="c6a5b-113">Size</span></span>              | <span data-ttu-id="c6a5b-114">8 byte</span><span class="sxs-lookup"><span data-stu-id="c6a5b-114">8 bytes</span></span>                              |
| <span data-ttu-id="c6a5b-115">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="c6a5b-115">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="c6a5b-116">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="c6a5b-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="c6a5b-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c6a5b-117">Attribute-Id</span></span>      | <span data-ttu-id="c6a5b-118">1.2.840.113556.1.4.765</span><span class="sxs-lookup"><span data-stu-id="c6a5b-118">1.2.840.113556.1.4.765</span></span>               |
| <span data-ttu-id="c6a5b-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="c6a5b-119">System-Id-Guid</span></span>    | <span data-ttu-id="c6a5b-120">7f561282-5301-11d1-a9c5-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="c6a5b-120">7f561282-5301-11d1-a9c5-0000f80367c1</span></span> |
| <span data-ttu-id="c6a5b-121">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c6a5b-121">Syntax</span></span>            | [<span data-ttu-id="c6a5b-122">**Interval**</span><span class="sxs-lookup"><span data-stu-id="c6a5b-122">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="c6a5b-123">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="c6a5b-123">Implementations</span></span>

-   [<span data-ttu-id="c6a5b-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="c6a5b-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="c6a5b-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c6a5b-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c6a5b-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c6a5b-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c6a5b-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c6a5b-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c6a5b-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c6a5b-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c6a5b-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c6a5b-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="c6a5b-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c6a5b-130">Windows 2000 Server</span></span>



| <span data-ttu-id="c6a5b-131">Voce</span><span class="sxs-lookup"><span data-stu-id="c6a5b-131">Entry</span></span> | <span data-ttu-id="c6a5b-132">Valore</span><span class="sxs-lookup"><span data-stu-id="c6a5b-132">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="c6a5b-133">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="c6a5b-133">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="c6a5b-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c6a5b-134">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="c6a5b-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="c6a5b-135">System-Only</span></span>            | <span data-ttu-id="c6a5b-136">Falso</span><span class="sxs-lookup"><span data-stu-id="c6a5b-136">False</span></span>                                        |
| <span data-ttu-id="c6a5b-137">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="c6a5b-137">Is-Single-Valued</span></span>       | <span data-ttu-id="c6a5b-138">Vero</span><span class="sxs-lookup"><span data-stu-id="c6a5b-138">True</span></span>                                         |
| <span data-ttu-id="c6a5b-139">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="c6a5b-139">Is Indexed</span></span>             | <span data-ttu-id="c6a5b-140">Falso</span><span class="sxs-lookup"><span data-stu-id="c6a5b-140">False</span></span>                                        |
| <span data-ttu-id="c6a5b-141">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="c6a5b-141">In Global Catalog</span></span>      | <span data-ttu-id="c6a5b-142">Falso</span><span class="sxs-lookup"><span data-stu-id="c6a5b-142">False</span></span>                                        |
| <span data-ttu-id="c6a5b-143">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="c6a5b-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="c6a5b-144">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="c6a5b-144">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="c6a5b-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c6a5b-145">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="c6a5b-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c6a5b-146">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="c6a5b-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c6a5b-147">Search-Flags</span></span>           | <span data-ttu-id="c6a5b-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c6a5b-148">0x00000000</span></span>                                   |
| <span data-ttu-id="c6a5b-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c6a5b-149">System-Flags</span></span>           | <span data-ttu-id="c6a5b-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c6a5b-150">0x00000010</span></span>                                   |
| <span data-ttu-id="c6a5b-151">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="c6a5b-151">Classes used in</span></span>        | [<span data-ttu-id="c6a5b-152">**ACS-criteri**</span><span class="sxs-lookup"><span data-stu-id="c6a5b-152">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="c6a5b-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c6a5b-153">Windows Server 2003</span></span>



| <span data-ttu-id="c6a5b-154">Voce</span><span class="sxs-lookup"><span data-stu-id="c6a5b-154">Entry</span></span> | <span data-ttu-id="c6a5b-155">Valore</span><span class="sxs-lookup"><span data-stu-id="c6a5b-155">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="c6a5b-156">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="c6a5b-156">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="c6a5b-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c6a5b-157">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="c6a5b-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="c6a5b-158">System-Only</span></span>            | <span data-ttu-id="c6a5b-159">Falso</span><span class="sxs-lookup"><span data-stu-id="c6a5b-159">False</span></span>                                        |
| <span data-ttu-id="c6a5b-160">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="c6a5b-160">Is-Single-Valued</span></span>       | <span data-ttu-id="c6a5b-161">Vero</span><span class="sxs-lookup"><span data-stu-id="c6a5b-161">True</span></span>                                         |
| <span data-ttu-id="c6a5b-162">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="c6a5b-162">Is Indexed</span></span>             | <span data-ttu-id="c6a5b-163">Falso</span><span class="sxs-lookup"><span data-stu-id="c6a5b-163">False</span></span>                                        |
| <span data-ttu-id="c6a5b-164">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="c6a5b-164">In Global Catalog</span></span>      | <span data-ttu-id="c6a5b-165">Falso</span><span class="sxs-lookup"><span data-stu-id="c6a5b-165">False</span></span>                                        |
| <span data-ttu-id="c6a5b-166">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="c6a5b-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="c6a5b-167">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="c6a5b-167">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="c6a5b-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c6a5b-168">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="c6a5b-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c6a5b-169">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="c6a5b-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c6a5b-170">Search-Flags</span></span>           | <span data-ttu-id="c6a5b-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c6a5b-171">0x00000000</span></span>                                   |
| <span data-ttu-id="c6a5b-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c6a5b-172">System-Flags</span></span>           | <span data-ttu-id="c6a5b-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c6a5b-173">0x00000010</span></span>                                   |
| <span data-ttu-id="c6a5b-174">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="c6a5b-174">Classes used in</span></span>        | [<span data-ttu-id="c6a5b-175">**ACS-criteri**</span><span class="sxs-lookup"><span data-stu-id="c6a5b-175">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c6a5b-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c6a5b-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c6a5b-177">Voce</span><span class="sxs-lookup"><span data-stu-id="c6a5b-177">Entry</span></span> | <span data-ttu-id="c6a5b-178">Valore</span><span class="sxs-lookup"><span data-stu-id="c6a5b-178">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="c6a5b-179">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="c6a5b-179">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="c6a5b-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c6a5b-180">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="c6a5b-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="c6a5b-181">System-Only</span></span>            | <span data-ttu-id="c6a5b-182">Falso</span><span class="sxs-lookup"><span data-stu-id="c6a5b-182">False</span></span>                                        |
| <span data-ttu-id="c6a5b-183">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="c6a5b-183">Is-Single-Valued</span></span>       | <span data-ttu-id="c6a5b-184">Vero</span><span class="sxs-lookup"><span data-stu-id="c6a5b-184">True</span></span>                                         |
| <span data-ttu-id="c6a5b-185">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="c6a5b-185">Is Indexed</span></span>             | <span data-ttu-id="c6a5b-186">Falso</span><span class="sxs-lookup"><span data-stu-id="c6a5b-186">False</span></span>                                        |
| <span data-ttu-id="c6a5b-187">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="c6a5b-187">In Global Catalog</span></span>      | <span data-ttu-id="c6a5b-188">Falso</span><span class="sxs-lookup"><span data-stu-id="c6a5b-188">False</span></span>                                        |
| <span data-ttu-id="c6a5b-189">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="c6a5b-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="c6a5b-190">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="c6a5b-190">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="c6a5b-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c6a5b-191">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="c6a5b-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c6a5b-192">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="c6a5b-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c6a5b-193">Search-Flags</span></span>           | <span data-ttu-id="c6a5b-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c6a5b-194">0x00000000</span></span>                                   |
| <span data-ttu-id="c6a5b-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c6a5b-195">System-Flags</span></span>           | <span data-ttu-id="c6a5b-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c6a5b-196">0x00000010</span></span>                                   |
| <span data-ttu-id="c6a5b-197">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="c6a5b-197">Classes used in</span></span>        | [<span data-ttu-id="c6a5b-198">**ACS-criteri**</span><span class="sxs-lookup"><span data-stu-id="c6a5b-198">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c6a5b-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c6a5b-199">Windows Server 2008</span></span>



| <span data-ttu-id="c6a5b-200">Voce</span><span class="sxs-lookup"><span data-stu-id="c6a5b-200">Entry</span></span> | <span data-ttu-id="c6a5b-201">Valore</span><span class="sxs-lookup"><span data-stu-id="c6a5b-201">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="c6a5b-202">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="c6a5b-202">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="c6a5b-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c6a5b-203">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="c6a5b-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="c6a5b-204">System-Only</span></span>            | <span data-ttu-id="c6a5b-205">Falso</span><span class="sxs-lookup"><span data-stu-id="c6a5b-205">False</span></span>                                        |
| <span data-ttu-id="c6a5b-206">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="c6a5b-206">Is-Single-Valued</span></span>       | <span data-ttu-id="c6a5b-207">Vero</span><span class="sxs-lookup"><span data-stu-id="c6a5b-207">True</span></span>                                         |
| <span data-ttu-id="c6a5b-208">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="c6a5b-208">Is Indexed</span></span>             | <span data-ttu-id="c6a5b-209">Falso</span><span class="sxs-lookup"><span data-stu-id="c6a5b-209">False</span></span>                                        |
| <span data-ttu-id="c6a5b-210">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="c6a5b-210">In Global Catalog</span></span>      | <span data-ttu-id="c6a5b-211">Falso</span><span class="sxs-lookup"><span data-stu-id="c6a5b-211">False</span></span>                                        |
| <span data-ttu-id="c6a5b-212">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="c6a5b-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="c6a5b-213">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="c6a5b-213">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="c6a5b-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c6a5b-214">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="c6a5b-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c6a5b-215">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="c6a5b-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c6a5b-216">Search-Flags</span></span>           | <span data-ttu-id="c6a5b-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c6a5b-217">0x00000000</span></span>                                   |
| <span data-ttu-id="c6a5b-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c6a5b-218">System-Flags</span></span>           | <span data-ttu-id="c6a5b-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c6a5b-219">0x00000010</span></span>                                   |
| <span data-ttu-id="c6a5b-220">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="c6a5b-220">Classes used in</span></span>        | [<span data-ttu-id="c6a5b-221">**ACS-criteri**</span><span class="sxs-lookup"><span data-stu-id="c6a5b-221">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c6a5b-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c6a5b-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c6a5b-223">Voce</span><span class="sxs-lookup"><span data-stu-id="c6a5b-223">Entry</span></span> | <span data-ttu-id="c6a5b-224">Valore</span><span class="sxs-lookup"><span data-stu-id="c6a5b-224">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="c6a5b-225">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="c6a5b-225">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="c6a5b-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c6a5b-226">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="c6a5b-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="c6a5b-227">System-Only</span></span>            | <span data-ttu-id="c6a5b-228">Falso</span><span class="sxs-lookup"><span data-stu-id="c6a5b-228">False</span></span>                                        |
| <span data-ttu-id="c6a5b-229">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="c6a5b-229">Is-Single-Valued</span></span>       | <span data-ttu-id="c6a5b-230">Vero</span><span class="sxs-lookup"><span data-stu-id="c6a5b-230">True</span></span>                                         |
| <span data-ttu-id="c6a5b-231">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="c6a5b-231">Is Indexed</span></span>             | <span data-ttu-id="c6a5b-232">Falso</span><span class="sxs-lookup"><span data-stu-id="c6a5b-232">False</span></span>                                        |
| <span data-ttu-id="c6a5b-233">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="c6a5b-233">In Global Catalog</span></span>      | <span data-ttu-id="c6a5b-234">Falso</span><span class="sxs-lookup"><span data-stu-id="c6a5b-234">False</span></span>                                        |
| <span data-ttu-id="c6a5b-235">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="c6a5b-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="c6a5b-236">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="c6a5b-236">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="c6a5b-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c6a5b-237">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="c6a5b-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c6a5b-238">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="c6a5b-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c6a5b-239">Search-Flags</span></span>           | <span data-ttu-id="c6a5b-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c6a5b-240">0x00000000</span></span>                                   |
| <span data-ttu-id="c6a5b-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c6a5b-241">System-Flags</span></span>           | <span data-ttu-id="c6a5b-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c6a5b-242">0x00000010</span></span>                                   |
| <span data-ttu-id="c6a5b-243">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="c6a5b-243">Classes used in</span></span>        | [<span data-ttu-id="c6a5b-244">**ACS-criteri**</span><span class="sxs-lookup"><span data-stu-id="c6a5b-244">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c6a5b-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c6a5b-245">Windows Server 2012</span></span>



| <span data-ttu-id="c6a5b-246">Voce</span><span class="sxs-lookup"><span data-stu-id="c6a5b-246">Entry</span></span> | <span data-ttu-id="c6a5b-247">Valore</span><span class="sxs-lookup"><span data-stu-id="c6a5b-247">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="c6a5b-248">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="c6a5b-248">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="c6a5b-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c6a5b-249">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="c6a5b-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="c6a5b-250">System-Only</span></span>            | <span data-ttu-id="c6a5b-251">Falso</span><span class="sxs-lookup"><span data-stu-id="c6a5b-251">False</span></span>                                        |
| <span data-ttu-id="c6a5b-252">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="c6a5b-252">Is-Single-Valued</span></span>       | <span data-ttu-id="c6a5b-253">Vero</span><span class="sxs-lookup"><span data-stu-id="c6a5b-253">True</span></span>                                         |
| <span data-ttu-id="c6a5b-254">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="c6a5b-254">Is Indexed</span></span>             | <span data-ttu-id="c6a5b-255">Falso</span><span class="sxs-lookup"><span data-stu-id="c6a5b-255">False</span></span>                                        |
| <span data-ttu-id="c6a5b-256">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="c6a5b-256">In Global Catalog</span></span>      | <span data-ttu-id="c6a5b-257">Falso</span><span class="sxs-lookup"><span data-stu-id="c6a5b-257">False</span></span>                                        |
| <span data-ttu-id="c6a5b-258">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="c6a5b-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="c6a5b-259">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="c6a5b-259">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="c6a5b-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c6a5b-260">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="c6a5b-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c6a5b-261">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="c6a5b-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c6a5b-262">Search-Flags</span></span>           | <span data-ttu-id="c6a5b-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c6a5b-263">0x00000000</span></span>                                   |
| <span data-ttu-id="c6a5b-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c6a5b-264">System-Flags</span></span>           | <span data-ttu-id="c6a5b-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c6a5b-265">0x00000010</span></span>                                   |
| <span data-ttu-id="c6a5b-266">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="c6a5b-266">Classes used in</span></span>        | [<span data-ttu-id="c6a5b-267">**ACS-criteri**</span><span class="sxs-lookup"><span data-stu-id="c6a5b-267">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



 

 





