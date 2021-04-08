---
title: Attributo Trust-Attributes
description: Questo attributo archivia gli attributi di trust per un dominio trusted.
ms.assetid: c85b98a6-4d09-4eb2-821b-58ef558b3460
ms.tgt_platform: multiple
keywords:
- Schema AD Trust-Attributes attribute
- Schema AD dell'attributo trustAttributes
topic_type:
- apiref
api_name:
- Trust-Attributes
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d81dc06f73fbda5dab7ce8d2a07bfc90323d2b29
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744882"
---
# <a name="trust-attributes-attribute"></a><span data-ttu-id="f6f6b-105">Attributo Trust-Attributes</span><span class="sxs-lookup"><span data-stu-id="f6f6b-105">Trust-Attributes attribute</span></span>

<span data-ttu-id="f6f6b-106">Questo attributo archivia gli attributi di trust per un dominio trusted.</span><span class="sxs-lookup"><span data-stu-id="f6f6b-106">This attribute stores the trust attributes for a trusted domain.</span></span> <span data-ttu-id="f6f6b-107">I valori di attributo possibili sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="f6f6b-107">Possible attribute values are as follows:</span></span>

-   <span data-ttu-id="f6f6b-108">\_ \_ \_ Transitività non transitiva dell'attributo trust.</span><span class="sxs-lookup"><span data-stu-id="f6f6b-108">TRUST\_ATTRIBUTE\_NON\_TRANSITIVE Disable transitivity.</span></span>
-   <span data-ttu-id="f6f6b-109">\_ \_ \_ L'attendibilità padre dell'albero degli attributi di attendibilità è impostata sul padre dell'albero dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="f6f6b-109">TRUST\_ATTRIBUTE\_TREE\_PARENT Trust is set to the organization tree parent.</span></span>
-   <span data-ttu-id="f6f6b-110">Trust \_ \_ radice dell'albero degli attributi di attendibilità \_ impostato su un'altra radice dell'albero nell'insieme di strutture.</span><span class="sxs-lookup"><span data-stu-id="f6f6b-110">TRUST\_ATTRIBUTE\_TREE\_ROOT Trust set to another tree root in the forest.</span></span>
-   <span data-ttu-id="f6f6b-111">\_Attributo trust \_ di livello superiore \_ solo collegamento attendibile valido solo per client di livello superiore.</span><span class="sxs-lookup"><span data-stu-id="f6f6b-111">TRUST\_ATTRIBUTE\_UPLEVEL\_ONLY Trusted link valid only for uplevel client.</span></span>



| <span data-ttu-id="f6f6b-112">Voce</span><span class="sxs-lookup"><span data-stu-id="f6f6b-112">Entry</span></span> | <span data-ttu-id="f6f6b-113">Valore</span><span class="sxs-lookup"><span data-stu-id="f6f6b-113">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="f6f6b-114">CN</span><span class="sxs-lookup"><span data-stu-id="f6f6b-114">CN</span></span>                | <span data-ttu-id="f6f6b-115">Trust-Attributes</span><span class="sxs-lookup"><span data-stu-id="f6f6b-115">Trust-Attributes</span></span>                     |
| <span data-ttu-id="f6f6b-116">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="f6f6b-116">Ldap-Display-Name</span></span> | <span data-ttu-id="f6f6b-117">trustAttributes</span><span class="sxs-lookup"><span data-stu-id="f6f6b-117">trustAttributes</span></span>                      |
| <span data-ttu-id="f6f6b-118">Dimensione</span><span class="sxs-lookup"><span data-stu-id="f6f6b-118">Size</span></span>              | \-                                   |
| <span data-ttu-id="f6f6b-119">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="f6f6b-119">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="f6f6b-120">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="f6f6b-120">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="f6f6b-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f6f6b-121">Attribute-Id</span></span>      | <span data-ttu-id="f6f6b-122">1.2.840.113556.1.4.470</span><span class="sxs-lookup"><span data-stu-id="f6f6b-122">1.2.840.113556.1.4.470</span></span>               |
| <span data-ttu-id="f6f6b-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="f6f6b-123">System-Id-Guid</span></span>    | <span data-ttu-id="f6f6b-124">80a67e5a-9f22-11d0-afdd-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="f6f6b-124">80a67e5a-9f22-11d0-afdd-00c04fd930c9</span></span> |
| <span data-ttu-id="f6f6b-125">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f6f6b-125">Syntax</span></span>            | [<span data-ttu-id="f6f6b-126">**Enumerazione**</span><span class="sxs-lookup"><span data-stu-id="f6f6b-126">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="f6f6b-127">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="f6f6b-127">Implementations</span></span>

-   [<span data-ttu-id="f6f6b-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="f6f6b-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="f6f6b-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f6f6b-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f6f6b-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f6f6b-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f6f6b-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f6f6b-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f6f6b-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f6f6b-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f6f6b-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f6f6b-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="f6f6b-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f6f6b-134">Windows 2000 Server</span></span>



| <span data-ttu-id="f6f6b-135">Voce</span><span class="sxs-lookup"><span data-stu-id="f6f6b-135">Entry</span></span> | <span data-ttu-id="f6f6b-136">Valore</span><span class="sxs-lookup"><span data-stu-id="f6f6b-136">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="f6f6b-137">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="f6f6b-137">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="f6f6b-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f6f6b-138">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="f6f6b-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="f6f6b-139">System-Only</span></span>            | <span data-ttu-id="f6f6b-140">Falso</span><span class="sxs-lookup"><span data-stu-id="f6f6b-140">False</span></span>                                                |
| <span data-ttu-id="f6f6b-141">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="f6f6b-141">Is-Single-Valued</span></span>       | <span data-ttu-id="f6f6b-142">Vero</span><span class="sxs-lookup"><span data-stu-id="f6f6b-142">True</span></span>                                                 |
| <span data-ttu-id="f6f6b-143">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="f6f6b-143">Is Indexed</span></span>             | <span data-ttu-id="f6f6b-144">Falso</span><span class="sxs-lookup"><span data-stu-id="f6f6b-144">False</span></span>                                                |
| <span data-ttu-id="f6f6b-145">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="f6f6b-145">In Global Catalog</span></span>      | <span data-ttu-id="f6f6b-146">Falso</span><span class="sxs-lookup"><span data-stu-id="f6f6b-146">False</span></span>                                                |
| <span data-ttu-id="f6f6b-147">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="f6f6b-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="f6f6b-148">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="f6f6b-148">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="f6f6b-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f6f6b-149">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="f6f6b-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f6f6b-150">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="f6f6b-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f6f6b-151">Search-Flags</span></span>           | <span data-ttu-id="f6f6b-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f6f6b-152">0x00000000</span></span>                                           |
| <span data-ttu-id="f6f6b-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f6f6b-153">System-Flags</span></span>           | <span data-ttu-id="f6f6b-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f6f6b-154">0x00000010</span></span>                                           |
| <span data-ttu-id="f6f6b-155">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="f6f6b-155">Classes used in</span></span>        | [<span data-ttu-id="f6f6b-156">**Dominio trusted**</span><span class="sxs-lookup"><span data-stu-id="f6f6b-156">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="f6f6b-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f6f6b-157">Windows Server 2003</span></span>



| <span data-ttu-id="f6f6b-158">Voce</span><span class="sxs-lookup"><span data-stu-id="f6f6b-158">Entry</span></span> | <span data-ttu-id="f6f6b-159">Valore</span><span class="sxs-lookup"><span data-stu-id="f6f6b-159">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="f6f6b-160">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="f6f6b-160">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="f6f6b-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f6f6b-161">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="f6f6b-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="f6f6b-162">System-Only</span></span>            | <span data-ttu-id="f6f6b-163">Falso</span><span class="sxs-lookup"><span data-stu-id="f6f6b-163">False</span></span>                                                |
| <span data-ttu-id="f6f6b-164">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="f6f6b-164">Is-Single-Valued</span></span>       | <span data-ttu-id="f6f6b-165">Vero</span><span class="sxs-lookup"><span data-stu-id="f6f6b-165">True</span></span>                                                 |
| <span data-ttu-id="f6f6b-166">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="f6f6b-166">Is Indexed</span></span>             | <span data-ttu-id="f6f6b-167">Falso</span><span class="sxs-lookup"><span data-stu-id="f6f6b-167">False</span></span>                                                |
| <span data-ttu-id="f6f6b-168">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="f6f6b-168">In Global Catalog</span></span>      | <span data-ttu-id="f6f6b-169">Vero</span><span class="sxs-lookup"><span data-stu-id="f6f6b-169">True</span></span>                                                 |
| <span data-ttu-id="f6f6b-170">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="f6f6b-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="f6f6b-171">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="f6f6b-171">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="f6f6b-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f6f6b-172">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="f6f6b-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f6f6b-173">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="f6f6b-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f6f6b-174">Search-Flags</span></span>           | <span data-ttu-id="f6f6b-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f6f6b-175">0x00000000</span></span>                                           |
| <span data-ttu-id="f6f6b-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f6f6b-176">System-Flags</span></span>           | <span data-ttu-id="f6f6b-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f6f6b-177">0x00000010</span></span>                                           |
| <span data-ttu-id="f6f6b-178">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="f6f6b-178">Classes used in</span></span>        | [<span data-ttu-id="f6f6b-179">**Dominio trusted**</span><span class="sxs-lookup"><span data-stu-id="f6f6b-179">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f6f6b-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f6f6b-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f6f6b-181">Voce</span><span class="sxs-lookup"><span data-stu-id="f6f6b-181">Entry</span></span> | <span data-ttu-id="f6f6b-182">Valore</span><span class="sxs-lookup"><span data-stu-id="f6f6b-182">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="f6f6b-183">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="f6f6b-183">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="f6f6b-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f6f6b-184">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="f6f6b-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="f6f6b-185">System-Only</span></span>            | <span data-ttu-id="f6f6b-186">Falso</span><span class="sxs-lookup"><span data-stu-id="f6f6b-186">False</span></span>                                                |
| <span data-ttu-id="f6f6b-187">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="f6f6b-187">Is-Single-Valued</span></span>       | <span data-ttu-id="f6f6b-188">Vero</span><span class="sxs-lookup"><span data-stu-id="f6f6b-188">True</span></span>                                                 |
| <span data-ttu-id="f6f6b-189">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="f6f6b-189">Is Indexed</span></span>             | <span data-ttu-id="f6f6b-190">Falso</span><span class="sxs-lookup"><span data-stu-id="f6f6b-190">False</span></span>                                                |
| <span data-ttu-id="f6f6b-191">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="f6f6b-191">In Global Catalog</span></span>      | <span data-ttu-id="f6f6b-192">Vero</span><span class="sxs-lookup"><span data-stu-id="f6f6b-192">True</span></span>                                                 |
| <span data-ttu-id="f6f6b-193">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="f6f6b-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="f6f6b-194">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="f6f6b-194">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="f6f6b-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f6f6b-195">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="f6f6b-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f6f6b-196">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="f6f6b-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f6f6b-197">Search-Flags</span></span>           | <span data-ttu-id="f6f6b-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f6f6b-198">0x00000000</span></span>                                           |
| <span data-ttu-id="f6f6b-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f6f6b-199">System-Flags</span></span>           | <span data-ttu-id="f6f6b-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f6f6b-200">0x00000010</span></span>                                           |
| <span data-ttu-id="f6f6b-201">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="f6f6b-201">Classes used in</span></span>        | [<span data-ttu-id="f6f6b-202">**Dominio trusted**</span><span class="sxs-lookup"><span data-stu-id="f6f6b-202">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f6f6b-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f6f6b-203">Windows Server 2008</span></span>



| <span data-ttu-id="f6f6b-204">Voce</span><span class="sxs-lookup"><span data-stu-id="f6f6b-204">Entry</span></span> | <span data-ttu-id="f6f6b-205">Valore</span><span class="sxs-lookup"><span data-stu-id="f6f6b-205">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="f6f6b-206">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="f6f6b-206">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="f6f6b-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f6f6b-207">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="f6f6b-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="f6f6b-208">System-Only</span></span>            | <span data-ttu-id="f6f6b-209">Falso</span><span class="sxs-lookup"><span data-stu-id="f6f6b-209">False</span></span>                                                |
| <span data-ttu-id="f6f6b-210">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="f6f6b-210">Is-Single-Valued</span></span>       | <span data-ttu-id="f6f6b-211">Vero</span><span class="sxs-lookup"><span data-stu-id="f6f6b-211">True</span></span>                                                 |
| <span data-ttu-id="f6f6b-212">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="f6f6b-212">Is Indexed</span></span>             | <span data-ttu-id="f6f6b-213">Falso</span><span class="sxs-lookup"><span data-stu-id="f6f6b-213">False</span></span>                                                |
| <span data-ttu-id="f6f6b-214">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="f6f6b-214">In Global Catalog</span></span>      | <span data-ttu-id="f6f6b-215">Vero</span><span class="sxs-lookup"><span data-stu-id="f6f6b-215">True</span></span>                                                 |
| <span data-ttu-id="f6f6b-216">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="f6f6b-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="f6f6b-217">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="f6f6b-217">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="f6f6b-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f6f6b-218">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="f6f6b-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f6f6b-219">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="f6f6b-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f6f6b-220">Search-Flags</span></span>           | <span data-ttu-id="f6f6b-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f6f6b-221">0x00000000</span></span>                                           |
| <span data-ttu-id="f6f6b-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f6f6b-222">System-Flags</span></span>           | <span data-ttu-id="f6f6b-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f6f6b-223">0x00000010</span></span>                                           |
| <span data-ttu-id="f6f6b-224">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="f6f6b-224">Classes used in</span></span>        | [<span data-ttu-id="f6f6b-225">**Dominio trusted**</span><span class="sxs-lookup"><span data-stu-id="f6f6b-225">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f6f6b-226">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f6f6b-226">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f6f6b-227">Voce</span><span class="sxs-lookup"><span data-stu-id="f6f6b-227">Entry</span></span> | <span data-ttu-id="f6f6b-228">Valore</span><span class="sxs-lookup"><span data-stu-id="f6f6b-228">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="f6f6b-229">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="f6f6b-229">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="f6f6b-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f6f6b-230">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="f6f6b-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="f6f6b-231">System-Only</span></span>            | <span data-ttu-id="f6f6b-232">Falso</span><span class="sxs-lookup"><span data-stu-id="f6f6b-232">False</span></span>                                                |
| <span data-ttu-id="f6f6b-233">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="f6f6b-233">Is-Single-Valued</span></span>       | <span data-ttu-id="f6f6b-234">Vero</span><span class="sxs-lookup"><span data-stu-id="f6f6b-234">True</span></span>                                                 |
| <span data-ttu-id="f6f6b-235">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="f6f6b-235">Is Indexed</span></span>             | <span data-ttu-id="f6f6b-236">Falso</span><span class="sxs-lookup"><span data-stu-id="f6f6b-236">False</span></span>                                                |
| <span data-ttu-id="f6f6b-237">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="f6f6b-237">In Global Catalog</span></span>      | <span data-ttu-id="f6f6b-238">Vero</span><span class="sxs-lookup"><span data-stu-id="f6f6b-238">True</span></span>                                                 |
| <span data-ttu-id="f6f6b-239">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="f6f6b-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="f6f6b-240">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="f6f6b-240">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="f6f6b-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f6f6b-241">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="f6f6b-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f6f6b-242">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="f6f6b-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f6f6b-243">Search-Flags</span></span>           | <span data-ttu-id="f6f6b-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f6f6b-244">0x00000000</span></span>                                           |
| <span data-ttu-id="f6f6b-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f6f6b-245">System-Flags</span></span>           | <span data-ttu-id="f6f6b-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f6f6b-246">0x00000010</span></span>                                           |
| <span data-ttu-id="f6f6b-247">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="f6f6b-247">Classes used in</span></span>        | [<span data-ttu-id="f6f6b-248">**Dominio trusted**</span><span class="sxs-lookup"><span data-stu-id="f6f6b-248">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f6f6b-249">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f6f6b-249">Windows Server 2012</span></span>



| <span data-ttu-id="f6f6b-250">Voce</span><span class="sxs-lookup"><span data-stu-id="f6f6b-250">Entry</span></span> | <span data-ttu-id="f6f6b-251">Valore</span><span class="sxs-lookup"><span data-stu-id="f6f6b-251">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="f6f6b-252">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="f6f6b-252">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="f6f6b-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f6f6b-253">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="f6f6b-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="f6f6b-254">System-Only</span></span>            | <span data-ttu-id="f6f6b-255">Falso</span><span class="sxs-lookup"><span data-stu-id="f6f6b-255">False</span></span>                                                |
| <span data-ttu-id="f6f6b-256">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="f6f6b-256">Is-Single-Valued</span></span>       | <span data-ttu-id="f6f6b-257">Vero</span><span class="sxs-lookup"><span data-stu-id="f6f6b-257">True</span></span>                                                 |
| <span data-ttu-id="f6f6b-258">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="f6f6b-258">Is Indexed</span></span>             | <span data-ttu-id="f6f6b-259">Falso</span><span class="sxs-lookup"><span data-stu-id="f6f6b-259">False</span></span>                                                |
| <span data-ttu-id="f6f6b-260">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="f6f6b-260">In Global Catalog</span></span>      | <span data-ttu-id="f6f6b-261">Vero</span><span class="sxs-lookup"><span data-stu-id="f6f6b-261">True</span></span>                                                 |
| <span data-ttu-id="f6f6b-262">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="f6f6b-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="f6f6b-263">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="f6f6b-263">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="f6f6b-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f6f6b-264">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="f6f6b-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f6f6b-265">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="f6f6b-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f6f6b-266">Search-Flags</span></span>           | <span data-ttu-id="f6f6b-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f6f6b-267">0x00000000</span></span>                                           |
| <span data-ttu-id="f6f6b-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f6f6b-268">System-Flags</span></span>           | <span data-ttu-id="f6f6b-269">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f6f6b-269">0x00000010</span></span>                                           |
| <span data-ttu-id="f6f6b-270">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="f6f6b-270">Classes used in</span></span>        | [<span data-ttu-id="f6f6b-271">**Dominio trusted**</span><span class="sxs-lookup"><span data-stu-id="f6f6b-271">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



 

 





