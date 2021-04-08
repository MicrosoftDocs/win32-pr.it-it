---
title: attributo ms-DS-Trust-Forest-Trust-Info
description: Contiene informazioni sull'attendibilità della foresta (un BLOB binario) utilizzato dal sistema per un oggetto Trusted-Domain.
ms.assetid: 60944ff6-d2b1-4f53-8557-7d79a7d9df51
ms.tgt_platform: multiple
keywords:
- Schema di AD dell'attributo ms-DS-Trust-Forest-Trust-Info
- attributo msDS-TrustForestTrustInfo-schema AD
topic_type:
- apiref
api_name:
- ms-DS-Trust-Forest-Trust-Info
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e259abaeae4d99b80b8ff6a390901f1c9f51e6a
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744679"
---
# <a name="ms-ds-trust-forest-trust-info-attribute"></a><span data-ttu-id="b1668-105">attributo ms-DS-Trust-Forest-Trust-Info</span><span class="sxs-lookup"><span data-stu-id="b1668-105">ms-DS-Trust-Forest-Trust-Info attribute</span></span>

<span data-ttu-id="b1668-106">Contiene informazioni sull'attendibilità della foresta (un BLOB binario) utilizzato dal sistema per un oggetto Trusted-Domain.</span><span class="sxs-lookup"><span data-stu-id="b1668-106">Contains forest trust information (a binary BLOB) that is used by the system for a Trusted-Domain object.</span></span>



| <span data-ttu-id="b1668-107">Voce</span><span class="sxs-lookup"><span data-stu-id="b1668-107">Entry</span></span> | <span data-ttu-id="b1668-108">Valore</span><span class="sxs-lookup"><span data-stu-id="b1668-108">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1668-109">CN</span><span class="sxs-lookup"><span data-stu-id="b1668-109">CN</span></span>                | <span data-ttu-id="b1668-110">ms-DS-Trust-Forest-Trust-Info</span><span class="sxs-lookup"><span data-stu-id="b1668-110">ms-DS-Trust-Forest-Trust-Info</span></span>                                                                                      |
| <span data-ttu-id="b1668-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="b1668-111">Ldap-Display-Name</span></span> | <span data-ttu-id="b1668-112">msDS-TrustForestTrustInfo</span><span class="sxs-lookup"><span data-stu-id="b1668-112">msDS-TrustForestTrustInfo</span></span>                                                                                          |
| <span data-ttu-id="b1668-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="b1668-113">Size</span></span>              | \-                                                                                                                 |
| <span data-ttu-id="b1668-114">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="b1668-114">Update Privilege</span></span>  | \-                                                                                                                 |
| <span data-ttu-id="b1668-115">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="b1668-115">Update Frequency</span></span>  | <span data-ttu-id="b1668-116">Solo quando la relazione di trust tra le foreste cambia.</span><span class="sxs-lookup"><span data-stu-id="b1668-116">Only when trust relationship between forests changes.</span></span> <span data-ttu-id="b1668-117">Questo problema può verificarsi se la topologia di una foresta trusted viene modificata.</span><span class="sxs-lookup"><span data-stu-id="b1668-117">This can happen if the topology of a trusted forest changes.</span></span> |
| <span data-ttu-id="b1668-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b1668-118">Attribute-Id</span></span>      | <span data-ttu-id="b1668-119">1.2.840.113556.1.4.1702</span><span class="sxs-lookup"><span data-stu-id="b1668-119">1.2.840.113556.1.4.1702</span></span>                                                                                            |
| <span data-ttu-id="b1668-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="b1668-120">System-Id-Guid</span></span>    | <span data-ttu-id="b1668-121">29cc866e-49d3-4969-942e-1dbc0925d183</span><span class="sxs-lookup"><span data-stu-id="b1668-121">29cc866e-49d3-4969-942e-1dbc0925d183</span></span>                                                                               |
| <span data-ttu-id="b1668-122">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b1668-122">Syntax</span></span>            | [<span data-ttu-id="b1668-123">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="b1668-123">**Object(Replica-Link)**</span></span>](s-object-replica-link.md)                                                              |



## <a name="implementations"></a><span data-ttu-id="b1668-124">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="b1668-124">Implementations</span></span>

-   [<span data-ttu-id="b1668-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b1668-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b1668-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b1668-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b1668-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b1668-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b1668-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b1668-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b1668-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b1668-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="b1668-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b1668-130">Windows Server 2003</span></span>



| <span data-ttu-id="b1668-131">Voce</span><span class="sxs-lookup"><span data-stu-id="b1668-131">Entry</span></span> | <span data-ttu-id="b1668-132">Valore</span><span class="sxs-lookup"><span data-stu-id="b1668-132">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="b1668-133">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="b1668-133">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b1668-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b1668-134">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b1668-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="b1668-135">System-Only</span></span>            | <span data-ttu-id="b1668-136">Falso</span><span class="sxs-lookup"><span data-stu-id="b1668-136">False</span></span>                                                |
| <span data-ttu-id="b1668-137">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="b1668-137">Is-Single-Valued</span></span>       | <span data-ttu-id="b1668-138">Vero</span><span class="sxs-lookup"><span data-stu-id="b1668-138">True</span></span>                                                 |
| <span data-ttu-id="b1668-139">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="b1668-139">Is Indexed</span></span>             | <span data-ttu-id="b1668-140">Falso</span><span class="sxs-lookup"><span data-stu-id="b1668-140">False</span></span>                                                |
| <span data-ttu-id="b1668-141">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="b1668-141">In Global Catalog</span></span>      | <span data-ttu-id="b1668-142">Vero</span><span class="sxs-lookup"><span data-stu-id="b1668-142">True</span></span>                                                 |
| <span data-ttu-id="b1668-143">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="b1668-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="b1668-144">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="b1668-144">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="b1668-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b1668-145">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="b1668-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b1668-146">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="b1668-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b1668-147">Search-Flags</span></span>           | <span data-ttu-id="b1668-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b1668-148">0x00000000</span></span>                                           |
| <span data-ttu-id="b1668-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b1668-149">System-Flags</span></span>           | <span data-ttu-id="b1668-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b1668-150">0x00000010</span></span>                                           |
| <span data-ttu-id="b1668-151">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="b1668-151">Classes used in</span></span>        | [<span data-ttu-id="b1668-152">**Dominio trusted**</span><span class="sxs-lookup"><span data-stu-id="b1668-152">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b1668-153">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b1668-153">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b1668-154">Voce</span><span class="sxs-lookup"><span data-stu-id="b1668-154">Entry</span></span> | <span data-ttu-id="b1668-155">Valore</span><span class="sxs-lookup"><span data-stu-id="b1668-155">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="b1668-156">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="b1668-156">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b1668-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b1668-157">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b1668-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="b1668-158">System-Only</span></span>            | <span data-ttu-id="b1668-159">Falso</span><span class="sxs-lookup"><span data-stu-id="b1668-159">False</span></span>                                                |
| <span data-ttu-id="b1668-160">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="b1668-160">Is-Single-Valued</span></span>       | <span data-ttu-id="b1668-161">Vero</span><span class="sxs-lookup"><span data-stu-id="b1668-161">True</span></span>                                                 |
| <span data-ttu-id="b1668-162">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="b1668-162">Is Indexed</span></span>             | <span data-ttu-id="b1668-163">Falso</span><span class="sxs-lookup"><span data-stu-id="b1668-163">False</span></span>                                                |
| <span data-ttu-id="b1668-164">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="b1668-164">In Global Catalog</span></span>      | <span data-ttu-id="b1668-165">Vero</span><span class="sxs-lookup"><span data-stu-id="b1668-165">True</span></span>                                                 |
| <span data-ttu-id="b1668-166">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="b1668-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="b1668-167">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="b1668-167">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="b1668-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b1668-168">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="b1668-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b1668-169">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="b1668-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b1668-170">Search-Flags</span></span>           | <span data-ttu-id="b1668-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b1668-171">0x00000000</span></span>                                           |
| <span data-ttu-id="b1668-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b1668-172">System-Flags</span></span>           | <span data-ttu-id="b1668-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b1668-173">0x00000010</span></span>                                           |
| <span data-ttu-id="b1668-174">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="b1668-174">Classes used in</span></span>        | [<span data-ttu-id="b1668-175">**Dominio trusted**</span><span class="sxs-lookup"><span data-stu-id="b1668-175">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b1668-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b1668-176">Windows Server 2008</span></span>



| <span data-ttu-id="b1668-177">Voce</span><span class="sxs-lookup"><span data-stu-id="b1668-177">Entry</span></span> | <span data-ttu-id="b1668-178">Valore</span><span class="sxs-lookup"><span data-stu-id="b1668-178">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="b1668-179">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="b1668-179">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b1668-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b1668-180">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b1668-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="b1668-181">System-Only</span></span>            | <span data-ttu-id="b1668-182">Falso</span><span class="sxs-lookup"><span data-stu-id="b1668-182">False</span></span>                                                |
| <span data-ttu-id="b1668-183">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="b1668-183">Is-Single-Valued</span></span>       | <span data-ttu-id="b1668-184">Vero</span><span class="sxs-lookup"><span data-stu-id="b1668-184">True</span></span>                                                 |
| <span data-ttu-id="b1668-185">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="b1668-185">Is Indexed</span></span>             | <span data-ttu-id="b1668-186">Falso</span><span class="sxs-lookup"><span data-stu-id="b1668-186">False</span></span>                                                |
| <span data-ttu-id="b1668-187">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="b1668-187">In Global Catalog</span></span>      | <span data-ttu-id="b1668-188">Vero</span><span class="sxs-lookup"><span data-stu-id="b1668-188">True</span></span>                                                 |
| <span data-ttu-id="b1668-189">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="b1668-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="b1668-190">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="b1668-190">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="b1668-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b1668-191">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="b1668-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b1668-192">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="b1668-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b1668-193">Search-Flags</span></span>           | <span data-ttu-id="b1668-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b1668-194">0x00000000</span></span>                                           |
| <span data-ttu-id="b1668-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b1668-195">System-Flags</span></span>           | <span data-ttu-id="b1668-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b1668-196">0x00000010</span></span>                                           |
| <span data-ttu-id="b1668-197">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="b1668-197">Classes used in</span></span>        | [<span data-ttu-id="b1668-198">**Dominio trusted**</span><span class="sxs-lookup"><span data-stu-id="b1668-198">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b1668-199">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b1668-199">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b1668-200">Voce</span><span class="sxs-lookup"><span data-stu-id="b1668-200">Entry</span></span> | <span data-ttu-id="b1668-201">Valore</span><span class="sxs-lookup"><span data-stu-id="b1668-201">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="b1668-202">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="b1668-202">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b1668-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b1668-203">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b1668-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="b1668-204">System-Only</span></span>            | <span data-ttu-id="b1668-205">Falso</span><span class="sxs-lookup"><span data-stu-id="b1668-205">False</span></span>                                                |
| <span data-ttu-id="b1668-206">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="b1668-206">Is-Single-Valued</span></span>       | <span data-ttu-id="b1668-207">Vero</span><span class="sxs-lookup"><span data-stu-id="b1668-207">True</span></span>                                                 |
| <span data-ttu-id="b1668-208">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="b1668-208">Is Indexed</span></span>             | <span data-ttu-id="b1668-209">Falso</span><span class="sxs-lookup"><span data-stu-id="b1668-209">False</span></span>                                                |
| <span data-ttu-id="b1668-210">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="b1668-210">In Global Catalog</span></span>      | <span data-ttu-id="b1668-211">Vero</span><span class="sxs-lookup"><span data-stu-id="b1668-211">True</span></span>                                                 |
| <span data-ttu-id="b1668-212">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="b1668-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="b1668-213">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="b1668-213">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="b1668-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b1668-214">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="b1668-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b1668-215">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="b1668-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b1668-216">Search-Flags</span></span>           | <span data-ttu-id="b1668-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b1668-217">0x00000000</span></span>                                           |
| <span data-ttu-id="b1668-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b1668-218">System-Flags</span></span>           | <span data-ttu-id="b1668-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b1668-219">0x00000010</span></span>                                           |
| <span data-ttu-id="b1668-220">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="b1668-220">Classes used in</span></span>        | [<span data-ttu-id="b1668-221">**Dominio trusted**</span><span class="sxs-lookup"><span data-stu-id="b1668-221">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b1668-222">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b1668-222">Windows Server 2012</span></span>



| <span data-ttu-id="b1668-223">Voce</span><span class="sxs-lookup"><span data-stu-id="b1668-223">Entry</span></span> | <span data-ttu-id="b1668-224">Valore</span><span class="sxs-lookup"><span data-stu-id="b1668-224">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="b1668-225">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="b1668-225">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b1668-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b1668-226">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b1668-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="b1668-227">System-Only</span></span>            | <span data-ttu-id="b1668-228">Falso</span><span class="sxs-lookup"><span data-stu-id="b1668-228">False</span></span>                                                |
| <span data-ttu-id="b1668-229">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="b1668-229">Is-Single-Valued</span></span>       | <span data-ttu-id="b1668-230">Vero</span><span class="sxs-lookup"><span data-stu-id="b1668-230">True</span></span>                                                 |
| <span data-ttu-id="b1668-231">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="b1668-231">Is Indexed</span></span>             | <span data-ttu-id="b1668-232">Falso</span><span class="sxs-lookup"><span data-stu-id="b1668-232">False</span></span>                                                |
| <span data-ttu-id="b1668-233">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="b1668-233">In Global Catalog</span></span>      | <span data-ttu-id="b1668-234">Vero</span><span class="sxs-lookup"><span data-stu-id="b1668-234">True</span></span>                                                 |
| <span data-ttu-id="b1668-235">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="b1668-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="b1668-236">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="b1668-236">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="b1668-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b1668-237">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="b1668-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b1668-238">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="b1668-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b1668-239">Search-Flags</span></span>           | <span data-ttu-id="b1668-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b1668-240">0x00000000</span></span>                                           |
| <span data-ttu-id="b1668-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b1668-241">System-Flags</span></span>           | <span data-ttu-id="b1668-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b1668-242">0x00000010</span></span>                                           |
| <span data-ttu-id="b1668-243">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="b1668-243">Classes used in</span></span>        | [<span data-ttu-id="b1668-244">**Dominio trusted**</span><span class="sxs-lookup"><span data-stu-id="b1668-244">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



 

 





