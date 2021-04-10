---
title: Attributo del generatore di topologia tra siti
description: Questo attributo verrà utilizzato per supportare il failover del computer designato come quello che esegue la generazione della topologia tra siti in un sito specifico.
ms.assetid: 077f4331-ead9-4f17-942e-d55cf253d03b
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo del generatore di topologia tra siti
- Schema AD dell'attributo interSiteTopologyGenerator
topic_type:
- apiref
api_name:
- Inter-Site-Topology-Generator
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7df7b354d05e882373715e4c49498c9daff41652
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104122002"
---
# <a name="inter-site-topology-generator-attribute"></a><span data-ttu-id="d2048-105">Attributo del generatore di topologia tra siti</span><span class="sxs-lookup"><span data-stu-id="d2048-105">Inter-Site-Topology-Generator attribute</span></span>

<span data-ttu-id="d2048-106">Questo attributo verrà utilizzato per supportare il failover del computer designato come quello che esegue la generazione della topologia tra siti in un sito specifico.</span><span class="sxs-lookup"><span data-stu-id="d2048-106">This attribute will be used to support failover for the computer designated as the one that runs Knowledge Consistency Checker inter-site topology generation in a given site.</span></span>



| <span data-ttu-id="d2048-107">Voce</span><span class="sxs-lookup"><span data-stu-id="d2048-107">Entry</span></span> | <span data-ttu-id="d2048-108">Valore</span><span class="sxs-lookup"><span data-stu-id="d2048-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="d2048-109">CN</span><span class="sxs-lookup"><span data-stu-id="d2048-109">CN</span></span>                | <span data-ttu-id="d2048-110">Generatore di topologia tra siti</span><span class="sxs-lookup"><span data-stu-id="d2048-110">Inter-Site-Topology-Generator</span></span>           |
| <span data-ttu-id="d2048-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="d2048-111">Ldap-Display-Name</span></span> | <span data-ttu-id="d2048-112">interSiteTopologyGenerator</span><span class="sxs-lookup"><span data-stu-id="d2048-112">interSiteTopologyGenerator</span></span>              |
| <span data-ttu-id="d2048-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="d2048-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="d2048-114">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="d2048-114">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="d2048-115">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="d2048-115">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="d2048-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="d2048-116">Attribute-Id</span></span>      | <span data-ttu-id="d2048-117">1.2.840.113556.1.4.1246</span><span class="sxs-lookup"><span data-stu-id="d2048-117">1.2.840.113556.1.4.1246</span></span>                 |
| <span data-ttu-id="d2048-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="d2048-118">System-Id-Guid</span></span>    | <span data-ttu-id="d2048-119">b7c69e5e-2cc7-11d2-854e-00a0c983f608</span><span class="sxs-lookup"><span data-stu-id="d2048-119">b7c69e5e-2cc7-11d2-854e-00a0c983f608</span></span>    |
| <span data-ttu-id="d2048-120">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d2048-120">Syntax</span></span>            | [<span data-ttu-id="d2048-121">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="d2048-121">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="d2048-122">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="d2048-122">Implementations</span></span>

-   [<span data-ttu-id="d2048-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="d2048-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="d2048-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="d2048-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="d2048-125">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="d2048-125">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="d2048-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="d2048-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="d2048-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="d2048-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="d2048-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="d2048-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="d2048-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="d2048-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="d2048-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d2048-130">Windows 2000 Server</span></span>



| <span data-ttu-id="d2048-131">Voce</span><span class="sxs-lookup"><span data-stu-id="d2048-131">Entry</span></span> | <span data-ttu-id="d2048-132">Valore</span><span class="sxs-lookup"><span data-stu-id="d2048-132">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="d2048-133">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="d2048-133">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="d2048-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d2048-134">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="d2048-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="d2048-135">System-Only</span></span>            | <span data-ttu-id="d2048-136">Falso</span><span class="sxs-lookup"><span data-stu-id="d2048-136">False</span></span>                                                       |
| <span data-ttu-id="d2048-137">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="d2048-137">Is-Single-Valued</span></span>       | <span data-ttu-id="d2048-138">Vero</span><span class="sxs-lookup"><span data-stu-id="d2048-138">True</span></span>                                                        |
| <span data-ttu-id="d2048-139">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="d2048-139">Is Indexed</span></span>             | <span data-ttu-id="d2048-140">Falso</span><span class="sxs-lookup"><span data-stu-id="d2048-140">False</span></span>                                                       |
| <span data-ttu-id="d2048-141">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="d2048-141">In Global Catalog</span></span>      | <span data-ttu-id="d2048-142">Falso</span><span class="sxs-lookup"><span data-stu-id="d2048-142">False</span></span>                                                       |
| <span data-ttu-id="d2048-143">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="d2048-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="d2048-144">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="d2048-144">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="d2048-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d2048-145">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="d2048-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d2048-146">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="d2048-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d2048-147">Search-Flags</span></span>           | <span data-ttu-id="d2048-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d2048-148">0x00000000</span></span>                                                  |
| <span data-ttu-id="d2048-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d2048-149">System-Flags</span></span>           | <span data-ttu-id="d2048-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d2048-150">0x00000010</span></span>                                                  |
| <span data-ttu-id="d2048-151">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="d2048-151">Classes used in</span></span>        | [<span data-ttu-id="d2048-152">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="d2048-152">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="d2048-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d2048-153">Windows Server 2003</span></span>



| <span data-ttu-id="d2048-154">Voce</span><span class="sxs-lookup"><span data-stu-id="d2048-154">Entry</span></span> | <span data-ttu-id="d2048-155">Valore</span><span class="sxs-lookup"><span data-stu-id="d2048-155">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="d2048-156">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="d2048-156">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="d2048-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d2048-157">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="d2048-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="d2048-158">System-Only</span></span>            | <span data-ttu-id="d2048-159">Falso</span><span class="sxs-lookup"><span data-stu-id="d2048-159">False</span></span>                                                       |
| <span data-ttu-id="d2048-160">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="d2048-160">Is-Single-Valued</span></span>       | <span data-ttu-id="d2048-161">Vero</span><span class="sxs-lookup"><span data-stu-id="d2048-161">True</span></span>                                                        |
| <span data-ttu-id="d2048-162">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="d2048-162">Is Indexed</span></span>             | <span data-ttu-id="d2048-163">Falso</span><span class="sxs-lookup"><span data-stu-id="d2048-163">False</span></span>                                                       |
| <span data-ttu-id="d2048-164">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="d2048-164">In Global Catalog</span></span>      | <span data-ttu-id="d2048-165">Falso</span><span class="sxs-lookup"><span data-stu-id="d2048-165">False</span></span>                                                       |
| <span data-ttu-id="d2048-166">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="d2048-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="d2048-167">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="d2048-167">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="d2048-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d2048-168">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="d2048-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d2048-169">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="d2048-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d2048-170">Search-Flags</span></span>           | <span data-ttu-id="d2048-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d2048-171">0x00000000</span></span>                                                  |
| <span data-ttu-id="d2048-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d2048-172">System-Flags</span></span>           | <span data-ttu-id="d2048-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d2048-173">0x00000010</span></span>                                                  |
| <span data-ttu-id="d2048-174">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="d2048-174">Classes used in</span></span>        | [<span data-ttu-id="d2048-175">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="d2048-175">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="adam"></a><span data-ttu-id="d2048-176">ADAM</span><span class="sxs-lookup"><span data-stu-id="d2048-176">ADAM</span></span>



| <span data-ttu-id="d2048-177">Voce</span><span class="sxs-lookup"><span data-stu-id="d2048-177">Entry</span></span> | <span data-ttu-id="d2048-178">Valore</span><span class="sxs-lookup"><span data-stu-id="d2048-178">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="d2048-179">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="d2048-179">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="d2048-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d2048-180">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="d2048-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="d2048-181">System-Only</span></span>            | <span data-ttu-id="d2048-182">Falso</span><span class="sxs-lookup"><span data-stu-id="d2048-182">False</span></span>                                                       |
| <span data-ttu-id="d2048-183">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="d2048-183">Is-Single-Valued</span></span>       | <span data-ttu-id="d2048-184">Vero</span><span class="sxs-lookup"><span data-stu-id="d2048-184">True</span></span>                                                        |
| <span data-ttu-id="d2048-185">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="d2048-185">Is Indexed</span></span>             | <span data-ttu-id="d2048-186">Falso</span><span class="sxs-lookup"><span data-stu-id="d2048-186">False</span></span>                                                       |
| <span data-ttu-id="d2048-187">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="d2048-187">In Global Catalog</span></span>      | <span data-ttu-id="d2048-188">Falso</span><span class="sxs-lookup"><span data-stu-id="d2048-188">False</span></span>                                                       |
| <span data-ttu-id="d2048-189">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="d2048-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="d2048-190">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="d2048-190">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="d2048-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d2048-191">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="d2048-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d2048-192">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="d2048-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d2048-193">Search-Flags</span></span>           | <span data-ttu-id="d2048-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d2048-194">0x00000000</span></span>                                                  |
| <span data-ttu-id="d2048-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d2048-195">System-Flags</span></span>           | <span data-ttu-id="d2048-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d2048-196">0x00000010</span></span>                                                  |
| <span data-ttu-id="d2048-197">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="d2048-197">Classes used in</span></span>        | [<span data-ttu-id="d2048-198">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="d2048-198">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="d2048-199">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="d2048-199">Windows Server 2003 R2</span></span>



| <span data-ttu-id="d2048-200">Voce</span><span class="sxs-lookup"><span data-stu-id="d2048-200">Entry</span></span> | <span data-ttu-id="d2048-201">Valore</span><span class="sxs-lookup"><span data-stu-id="d2048-201">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="d2048-202">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="d2048-202">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="d2048-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d2048-203">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="d2048-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="d2048-204">System-Only</span></span>            | <span data-ttu-id="d2048-205">Falso</span><span class="sxs-lookup"><span data-stu-id="d2048-205">False</span></span>                                                       |
| <span data-ttu-id="d2048-206">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="d2048-206">Is-Single-Valued</span></span>       | <span data-ttu-id="d2048-207">Vero</span><span class="sxs-lookup"><span data-stu-id="d2048-207">True</span></span>                                                        |
| <span data-ttu-id="d2048-208">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="d2048-208">Is Indexed</span></span>             | <span data-ttu-id="d2048-209">Falso</span><span class="sxs-lookup"><span data-stu-id="d2048-209">False</span></span>                                                       |
| <span data-ttu-id="d2048-210">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="d2048-210">In Global Catalog</span></span>      | <span data-ttu-id="d2048-211">Falso</span><span class="sxs-lookup"><span data-stu-id="d2048-211">False</span></span>                                                       |
| <span data-ttu-id="d2048-212">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="d2048-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="d2048-213">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="d2048-213">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="d2048-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d2048-214">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="d2048-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d2048-215">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="d2048-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d2048-216">Search-Flags</span></span>           | <span data-ttu-id="d2048-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d2048-217">0x00000000</span></span>                                                  |
| <span data-ttu-id="d2048-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d2048-218">System-Flags</span></span>           | <span data-ttu-id="d2048-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d2048-219">0x00000010</span></span>                                                  |
| <span data-ttu-id="d2048-220">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="d2048-220">Classes used in</span></span>        | [<span data-ttu-id="d2048-221">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="d2048-221">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="d2048-222">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d2048-222">Windows Server 2008</span></span>



| <span data-ttu-id="d2048-223">Voce</span><span class="sxs-lookup"><span data-stu-id="d2048-223">Entry</span></span> | <span data-ttu-id="d2048-224">Valore</span><span class="sxs-lookup"><span data-stu-id="d2048-224">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="d2048-225">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="d2048-225">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="d2048-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d2048-226">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="d2048-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="d2048-227">System-Only</span></span>            | <span data-ttu-id="d2048-228">Falso</span><span class="sxs-lookup"><span data-stu-id="d2048-228">False</span></span>                                                       |
| <span data-ttu-id="d2048-229">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="d2048-229">Is-Single-Valued</span></span>       | <span data-ttu-id="d2048-230">Vero</span><span class="sxs-lookup"><span data-stu-id="d2048-230">True</span></span>                                                        |
| <span data-ttu-id="d2048-231">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="d2048-231">Is Indexed</span></span>             | <span data-ttu-id="d2048-232">Falso</span><span class="sxs-lookup"><span data-stu-id="d2048-232">False</span></span>                                                       |
| <span data-ttu-id="d2048-233">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="d2048-233">In Global Catalog</span></span>      | <span data-ttu-id="d2048-234">Falso</span><span class="sxs-lookup"><span data-stu-id="d2048-234">False</span></span>                                                       |
| <span data-ttu-id="d2048-235">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="d2048-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="d2048-236">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="d2048-236">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="d2048-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d2048-237">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="d2048-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d2048-238">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="d2048-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d2048-239">Search-Flags</span></span>           | <span data-ttu-id="d2048-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d2048-240">0x00000000</span></span>                                                  |
| <span data-ttu-id="d2048-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d2048-241">System-Flags</span></span>           | <span data-ttu-id="d2048-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d2048-242">0x00000010</span></span>                                                  |
| <span data-ttu-id="d2048-243">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="d2048-243">Classes used in</span></span>        | [<span data-ttu-id="d2048-244">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="d2048-244">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="d2048-245">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d2048-245">Windows Server 2008 R2</span></span>



| <span data-ttu-id="d2048-246">Voce</span><span class="sxs-lookup"><span data-stu-id="d2048-246">Entry</span></span> | <span data-ttu-id="d2048-247">Valore</span><span class="sxs-lookup"><span data-stu-id="d2048-247">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="d2048-248">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="d2048-248">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="d2048-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d2048-249">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="d2048-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="d2048-250">System-Only</span></span>            | <span data-ttu-id="d2048-251">Falso</span><span class="sxs-lookup"><span data-stu-id="d2048-251">False</span></span>                                                       |
| <span data-ttu-id="d2048-252">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="d2048-252">Is-Single-Valued</span></span>       | <span data-ttu-id="d2048-253">Vero</span><span class="sxs-lookup"><span data-stu-id="d2048-253">True</span></span>                                                        |
| <span data-ttu-id="d2048-254">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="d2048-254">Is Indexed</span></span>             | <span data-ttu-id="d2048-255">Falso</span><span class="sxs-lookup"><span data-stu-id="d2048-255">False</span></span>                                                       |
| <span data-ttu-id="d2048-256">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="d2048-256">In Global Catalog</span></span>      | <span data-ttu-id="d2048-257">Falso</span><span class="sxs-lookup"><span data-stu-id="d2048-257">False</span></span>                                                       |
| <span data-ttu-id="d2048-258">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="d2048-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="d2048-259">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="d2048-259">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="d2048-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d2048-260">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="d2048-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d2048-261">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="d2048-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d2048-262">Search-Flags</span></span>           | <span data-ttu-id="d2048-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d2048-263">0x00000000</span></span>                                                  |
| <span data-ttu-id="d2048-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d2048-264">System-Flags</span></span>           | <span data-ttu-id="d2048-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d2048-265">0x00000010</span></span>                                                  |
| <span data-ttu-id="d2048-266">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="d2048-266">Classes used in</span></span>        | [<span data-ttu-id="d2048-267">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="d2048-267">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="d2048-268">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d2048-268">Windows Server 2012</span></span>



| <span data-ttu-id="d2048-269">Voce</span><span class="sxs-lookup"><span data-stu-id="d2048-269">Entry</span></span> | <span data-ttu-id="d2048-270">Valore</span><span class="sxs-lookup"><span data-stu-id="d2048-270">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="d2048-271">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="d2048-271">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="d2048-272">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d2048-272">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="d2048-273">System-Only</span><span class="sxs-lookup"><span data-stu-id="d2048-273">System-Only</span></span>            | <span data-ttu-id="d2048-274">Falso</span><span class="sxs-lookup"><span data-stu-id="d2048-274">False</span></span>                                                       |
| <span data-ttu-id="d2048-275">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="d2048-275">Is-Single-Valued</span></span>       | <span data-ttu-id="d2048-276">Vero</span><span class="sxs-lookup"><span data-stu-id="d2048-276">True</span></span>                                                        |
| <span data-ttu-id="d2048-277">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="d2048-277">Is Indexed</span></span>             | <span data-ttu-id="d2048-278">Falso</span><span class="sxs-lookup"><span data-stu-id="d2048-278">False</span></span>                                                       |
| <span data-ttu-id="d2048-279">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="d2048-279">In Global Catalog</span></span>      | <span data-ttu-id="d2048-280">Falso</span><span class="sxs-lookup"><span data-stu-id="d2048-280">False</span></span>                                                       |
| <span data-ttu-id="d2048-281">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="d2048-281">NT-Security-Descriptor</span></span> | <span data-ttu-id="d2048-282">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="d2048-282">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="d2048-283">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d2048-283">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="d2048-284">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d2048-284">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="d2048-285">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d2048-285">Search-Flags</span></span>           | <span data-ttu-id="d2048-286">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d2048-286">0x00000000</span></span>                                                  |
| <span data-ttu-id="d2048-287">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d2048-287">System-Flags</span></span>           | <span data-ttu-id="d2048-288">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d2048-288">0x00000010</span></span>                                                  |
| <span data-ttu-id="d2048-289">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="d2048-289">Classes used in</span></span>        | [<span data-ttu-id="d2048-290">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="d2048-290">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



 

 





