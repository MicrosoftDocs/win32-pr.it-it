---
title: Attributo Dns-Record
description: Utilizzato per archiviare i record di risorse DNS binarie sugli oggetti DNS.
ms.assetid: 2d5a17da-0efc-450e-b247-3ab6d2de3a5d
ms.tgt_platform: multiple
keywords:
- Schema AD Dns-Record attribute
- Schema AD dell'attributo dnsRecord
topic_type:
- apiref
api_name:
- Dns-Record
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 013fa5ef4a9fcec151f996c347cdfd525438aa7d
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104123069"
---
# <a name="dns-record-attribute"></a><span data-ttu-id="5d21e-105">Attributo Dns-Record</span><span class="sxs-lookup"><span data-stu-id="5d21e-105">Dns-Record attribute</span></span>

<span data-ttu-id="5d21e-106">Utilizzato per archiviare i record di risorse DNS binarie sugli oggetti DNS.</span><span class="sxs-lookup"><span data-stu-id="5d21e-106">Used to store binary DNS resource records on DNS objects.</span></span>



| <span data-ttu-id="5d21e-107">Voce</span><span class="sxs-lookup"><span data-stu-id="5d21e-107">Entry</span></span> | <span data-ttu-id="5d21e-108">Valore</span><span class="sxs-lookup"><span data-stu-id="5d21e-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="5d21e-109">CN</span><span class="sxs-lookup"><span data-stu-id="5d21e-109">CN</span></span>                | <span data-ttu-id="5d21e-110">Dns-Record</span><span class="sxs-lookup"><span data-stu-id="5d21e-110">Dns-Record</span></span>                                            |
| <span data-ttu-id="5d21e-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="5d21e-111">Ldap-Display-Name</span></span> | <span data-ttu-id="5d21e-112">dnsRecord</span><span class="sxs-lookup"><span data-stu-id="5d21e-112">dnsRecord</span></span>                                             |
| <span data-ttu-id="5d21e-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="5d21e-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="5d21e-114">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="5d21e-114">Update Privilege</span></span>  | <span data-ttu-id="5d21e-115">Questo valore viene impostato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="5d21e-115">This value is set by the system.</span></span>                      |
| <span data-ttu-id="5d21e-116">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="5d21e-116">Update Frequency</span></span>  | <span data-ttu-id="5d21e-117">Ogni volta che i record di risorse DNS cambiano.</span><span class="sxs-lookup"><span data-stu-id="5d21e-117">Whenever DNS resource records change.</span></span>                 |
| <span data-ttu-id="5d21e-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="5d21e-118">Attribute-Id</span></span>      | <span data-ttu-id="5d21e-119">1.2.840.113556.1.4.382</span><span class="sxs-lookup"><span data-stu-id="5d21e-119">1.2.840.113556.1.4.382</span></span>                                |
| <span data-ttu-id="5d21e-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="5d21e-120">System-Id-Guid</span></span>    | <span data-ttu-id="5d21e-121">e0fa1e69-9b45-11d0-afdd-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="5d21e-121">e0fa1e69-9b45-11d0-afdd-00c04fd930c9</span></span>                  |
| <span data-ttu-id="5d21e-122">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5d21e-122">Syntax</span></span>            | [<span data-ttu-id="5d21e-123">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="5d21e-123">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="5d21e-124">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="5d21e-124">Implementations</span></span>

-   [<span data-ttu-id="5d21e-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="5d21e-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="5d21e-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="5d21e-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="5d21e-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="5d21e-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="5d21e-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="5d21e-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="5d21e-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="5d21e-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="5d21e-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="5d21e-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="5d21e-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5d21e-131">Windows 2000 Server</span></span>



| <span data-ttu-id="5d21e-132">Voce</span><span class="sxs-lookup"><span data-stu-id="5d21e-132">Entry</span></span> | <span data-ttu-id="5d21e-133">Valore</span><span class="sxs-lookup"><span data-stu-id="5d21e-133">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="5d21e-134">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="5d21e-134">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="5d21e-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5d21e-135">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="5d21e-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="5d21e-136">System-Only</span></span>            | <span data-ttu-id="5d21e-137">Falso</span><span class="sxs-lookup"><span data-stu-id="5d21e-137">False</span></span>                                    |
| <span data-ttu-id="5d21e-138">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="5d21e-138">Is-Single-Valued</span></span>       | <span data-ttu-id="5d21e-139">Falso</span><span class="sxs-lookup"><span data-stu-id="5d21e-139">False</span></span>                                    |
| <span data-ttu-id="5d21e-140">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="5d21e-140">Is Indexed</span></span>             | <span data-ttu-id="5d21e-141">Falso</span><span class="sxs-lookup"><span data-stu-id="5d21e-141">False</span></span>                                    |
| <span data-ttu-id="5d21e-142">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="5d21e-142">In Global Catalog</span></span>      | <span data-ttu-id="5d21e-143">Falso</span><span class="sxs-lookup"><span data-stu-id="5d21e-143">False</span></span>                                    |
| <span data-ttu-id="5d21e-144">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="5d21e-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="5d21e-145">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="5d21e-145">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="5d21e-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5d21e-146">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="5d21e-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5d21e-147">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="5d21e-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5d21e-148">Search-Flags</span></span>           | <span data-ttu-id="5d21e-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5d21e-149">0x00000000</span></span>                               |
| <span data-ttu-id="5d21e-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5d21e-150">System-Flags</span></span>           | <span data-ttu-id="5d21e-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5d21e-151">0x00000010</span></span>                               |
| <span data-ttu-id="5d21e-152">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="5d21e-152">Classes used in</span></span>        | [<span data-ttu-id="5d21e-153">**DNS-nodo**</span><span class="sxs-lookup"><span data-stu-id="5d21e-153">**Dns-Node**</span></span>](c-dnsnode.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="5d21e-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5d21e-154">Windows Server 2003</span></span>



| <span data-ttu-id="5d21e-155">Voce</span><span class="sxs-lookup"><span data-stu-id="5d21e-155">Entry</span></span> | <span data-ttu-id="5d21e-156">Valore</span><span class="sxs-lookup"><span data-stu-id="5d21e-156">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="5d21e-157">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="5d21e-157">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="5d21e-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5d21e-158">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="5d21e-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="5d21e-159">System-Only</span></span>            | <span data-ttu-id="5d21e-160">Falso</span><span class="sxs-lookup"><span data-stu-id="5d21e-160">False</span></span>                                    |
| <span data-ttu-id="5d21e-161">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="5d21e-161">Is-Single-Valued</span></span>       | <span data-ttu-id="5d21e-162">Falso</span><span class="sxs-lookup"><span data-stu-id="5d21e-162">False</span></span>                                    |
| <span data-ttu-id="5d21e-163">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="5d21e-163">Is Indexed</span></span>             | <span data-ttu-id="5d21e-164">Falso</span><span class="sxs-lookup"><span data-stu-id="5d21e-164">False</span></span>                                    |
| <span data-ttu-id="5d21e-165">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="5d21e-165">In Global Catalog</span></span>      | <span data-ttu-id="5d21e-166">Falso</span><span class="sxs-lookup"><span data-stu-id="5d21e-166">False</span></span>                                    |
| <span data-ttu-id="5d21e-167">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="5d21e-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="5d21e-168">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="5d21e-168">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="5d21e-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5d21e-169">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="5d21e-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5d21e-170">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="5d21e-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5d21e-171">Search-Flags</span></span>           | <span data-ttu-id="5d21e-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5d21e-172">0x00000000</span></span>                               |
| <span data-ttu-id="5d21e-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5d21e-173">System-Flags</span></span>           | <span data-ttu-id="5d21e-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5d21e-174">0x00000010</span></span>                               |
| <span data-ttu-id="5d21e-175">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="5d21e-175">Classes used in</span></span>        | [<span data-ttu-id="5d21e-176">**DNS-nodo**</span><span class="sxs-lookup"><span data-stu-id="5d21e-176">**Dns-Node**</span></span>](c-dnsnode.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="5d21e-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="5d21e-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="5d21e-178">Voce</span><span class="sxs-lookup"><span data-stu-id="5d21e-178">Entry</span></span> | <span data-ttu-id="5d21e-179">Valore</span><span class="sxs-lookup"><span data-stu-id="5d21e-179">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="5d21e-180">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="5d21e-180">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="5d21e-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5d21e-181">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="5d21e-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="5d21e-182">System-Only</span></span>            | <span data-ttu-id="5d21e-183">Falso</span><span class="sxs-lookup"><span data-stu-id="5d21e-183">False</span></span>                                    |
| <span data-ttu-id="5d21e-184">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="5d21e-184">Is-Single-Valued</span></span>       | <span data-ttu-id="5d21e-185">Falso</span><span class="sxs-lookup"><span data-stu-id="5d21e-185">False</span></span>                                    |
| <span data-ttu-id="5d21e-186">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="5d21e-186">Is Indexed</span></span>             | <span data-ttu-id="5d21e-187">Falso</span><span class="sxs-lookup"><span data-stu-id="5d21e-187">False</span></span>                                    |
| <span data-ttu-id="5d21e-188">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="5d21e-188">In Global Catalog</span></span>      | <span data-ttu-id="5d21e-189">Falso</span><span class="sxs-lookup"><span data-stu-id="5d21e-189">False</span></span>                                    |
| <span data-ttu-id="5d21e-190">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="5d21e-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="5d21e-191">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="5d21e-191">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="5d21e-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5d21e-192">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="5d21e-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5d21e-193">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="5d21e-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5d21e-194">Search-Flags</span></span>           | <span data-ttu-id="5d21e-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5d21e-195">0x00000000</span></span>                               |
| <span data-ttu-id="5d21e-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5d21e-196">System-Flags</span></span>           | <span data-ttu-id="5d21e-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5d21e-197">0x00000010</span></span>                               |
| <span data-ttu-id="5d21e-198">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="5d21e-198">Classes used in</span></span>        | [<span data-ttu-id="5d21e-199">**DNS-nodo**</span><span class="sxs-lookup"><span data-stu-id="5d21e-199">**Dns-Node**</span></span>](c-dnsnode.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="5d21e-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5d21e-200">Windows Server 2008</span></span>



| <span data-ttu-id="5d21e-201">Voce</span><span class="sxs-lookup"><span data-stu-id="5d21e-201">Entry</span></span> | <span data-ttu-id="5d21e-202">Valore</span><span class="sxs-lookup"><span data-stu-id="5d21e-202">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="5d21e-203">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="5d21e-203">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="5d21e-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5d21e-204">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="5d21e-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="5d21e-205">System-Only</span></span>            | <span data-ttu-id="5d21e-206">Falso</span><span class="sxs-lookup"><span data-stu-id="5d21e-206">False</span></span>                                    |
| <span data-ttu-id="5d21e-207">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="5d21e-207">Is-Single-Valued</span></span>       | <span data-ttu-id="5d21e-208">Falso</span><span class="sxs-lookup"><span data-stu-id="5d21e-208">False</span></span>                                    |
| <span data-ttu-id="5d21e-209">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="5d21e-209">Is Indexed</span></span>             | <span data-ttu-id="5d21e-210">Falso</span><span class="sxs-lookup"><span data-stu-id="5d21e-210">False</span></span>                                    |
| <span data-ttu-id="5d21e-211">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="5d21e-211">In Global Catalog</span></span>      | <span data-ttu-id="5d21e-212">Falso</span><span class="sxs-lookup"><span data-stu-id="5d21e-212">False</span></span>                                    |
| <span data-ttu-id="5d21e-213">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="5d21e-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="5d21e-214">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="5d21e-214">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="5d21e-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5d21e-215">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="5d21e-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5d21e-216">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="5d21e-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5d21e-217">Search-Flags</span></span>           | <span data-ttu-id="5d21e-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5d21e-218">0x00000000</span></span>                               |
| <span data-ttu-id="5d21e-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5d21e-219">System-Flags</span></span>           | <span data-ttu-id="5d21e-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5d21e-220">0x00000010</span></span>                               |
| <span data-ttu-id="5d21e-221">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="5d21e-221">Classes used in</span></span>        | [<span data-ttu-id="5d21e-222">**DNS-nodo**</span><span class="sxs-lookup"><span data-stu-id="5d21e-222">**Dns-Node**</span></span>](c-dnsnode.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="5d21e-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5d21e-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="5d21e-224">Voce</span><span class="sxs-lookup"><span data-stu-id="5d21e-224">Entry</span></span> | <span data-ttu-id="5d21e-225">Valore</span><span class="sxs-lookup"><span data-stu-id="5d21e-225">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="5d21e-226">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="5d21e-226">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="5d21e-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5d21e-227">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="5d21e-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="5d21e-228">System-Only</span></span>            | <span data-ttu-id="5d21e-229">Falso</span><span class="sxs-lookup"><span data-stu-id="5d21e-229">False</span></span>                                    |
| <span data-ttu-id="5d21e-230">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="5d21e-230">Is-Single-Valued</span></span>       | <span data-ttu-id="5d21e-231">Falso</span><span class="sxs-lookup"><span data-stu-id="5d21e-231">False</span></span>                                    |
| <span data-ttu-id="5d21e-232">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="5d21e-232">Is Indexed</span></span>             | <span data-ttu-id="5d21e-233">Falso</span><span class="sxs-lookup"><span data-stu-id="5d21e-233">False</span></span>                                    |
| <span data-ttu-id="5d21e-234">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="5d21e-234">In Global Catalog</span></span>      | <span data-ttu-id="5d21e-235">Falso</span><span class="sxs-lookup"><span data-stu-id="5d21e-235">False</span></span>                                    |
| <span data-ttu-id="5d21e-236">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="5d21e-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="5d21e-237">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="5d21e-237">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="5d21e-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5d21e-238">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="5d21e-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5d21e-239">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="5d21e-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5d21e-240">Search-Flags</span></span>           | <span data-ttu-id="5d21e-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5d21e-241">0x00000000</span></span>                               |
| <span data-ttu-id="5d21e-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5d21e-242">System-Flags</span></span>           | <span data-ttu-id="5d21e-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5d21e-243">0x00000010</span></span>                               |
| <span data-ttu-id="5d21e-244">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="5d21e-244">Classes used in</span></span>        | [<span data-ttu-id="5d21e-245">**DNS-nodo**</span><span class="sxs-lookup"><span data-stu-id="5d21e-245">**Dns-Node**</span></span>](c-dnsnode.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="5d21e-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5d21e-246">Windows Server 2012</span></span>



| <span data-ttu-id="5d21e-247">Voce</span><span class="sxs-lookup"><span data-stu-id="5d21e-247">Entry</span></span> | <span data-ttu-id="5d21e-248">Valore</span><span class="sxs-lookup"><span data-stu-id="5d21e-248">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="5d21e-249">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="5d21e-249">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="5d21e-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5d21e-250">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="5d21e-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="5d21e-251">System-Only</span></span>            | <span data-ttu-id="5d21e-252">Falso</span><span class="sxs-lookup"><span data-stu-id="5d21e-252">False</span></span>                                    |
| <span data-ttu-id="5d21e-253">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="5d21e-253">Is-Single-Valued</span></span>       | <span data-ttu-id="5d21e-254">Falso</span><span class="sxs-lookup"><span data-stu-id="5d21e-254">False</span></span>                                    |
| <span data-ttu-id="5d21e-255">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="5d21e-255">Is Indexed</span></span>             | <span data-ttu-id="5d21e-256">Falso</span><span class="sxs-lookup"><span data-stu-id="5d21e-256">False</span></span>                                    |
| <span data-ttu-id="5d21e-257">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="5d21e-257">In Global Catalog</span></span>      | <span data-ttu-id="5d21e-258">Falso</span><span class="sxs-lookup"><span data-stu-id="5d21e-258">False</span></span>                                    |
| <span data-ttu-id="5d21e-259">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="5d21e-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="5d21e-260">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="5d21e-260">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="5d21e-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5d21e-261">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="5d21e-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5d21e-262">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="5d21e-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5d21e-263">Search-Flags</span></span>           | <span data-ttu-id="5d21e-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5d21e-264">0x00000000</span></span>                               |
| <span data-ttu-id="5d21e-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5d21e-265">System-Flags</span></span>           | <span data-ttu-id="5d21e-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5d21e-266">0x00000010</span></span>                               |
| <span data-ttu-id="5d21e-267">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="5d21e-267">Classes used in</span></span>        | [<span data-ttu-id="5d21e-268">**DNS-nodo**</span><span class="sxs-lookup"><span data-stu-id="5d21e-268">**Dns-Node**</span></span>](c-dnsnode.md)<br/> |



 

 





