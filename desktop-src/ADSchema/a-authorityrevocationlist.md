---
title: Attributo Authority-revoche-List
description: Certificato incrociato, elenco di revoche di certificati.
ms.assetid: a9bc7ed3-4600-41a7-bbe5-4ec546a421fa
ms.tgt_platform: multiple
keywords:
- Authority-revoca-elencare l'attributo schema AD
- Schema AD dell'attributo authorityRevocationList
topic_type:
- apiref
api_name:
- Authority-Revocation-List
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fccc08cfb43bf4175bb51f2324e22c247d01f042
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104123186"
---
# <a name="authority-revocation-list-attribute"></a><span data-ttu-id="c3196-105">Attributo Authority-revoche-List</span><span class="sxs-lookup"><span data-stu-id="c3196-105">Authority-Revocation-List attribute</span></span>

<span data-ttu-id="c3196-106">Certificato incrociato, elenco di revoche di certificati.</span><span class="sxs-lookup"><span data-stu-id="c3196-106">Cross certificate, Certificate Revocation List.</span></span>



| <span data-ttu-id="c3196-107">Voce</span><span class="sxs-lookup"><span data-stu-id="c3196-107">Entry</span></span> | <span data-ttu-id="c3196-108">Valore</span><span class="sxs-lookup"><span data-stu-id="c3196-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="c3196-109">CN</span><span class="sxs-lookup"><span data-stu-id="c3196-109">CN</span></span>                | <span data-ttu-id="c3196-110">Elenco di revoche di autorità</span><span class="sxs-lookup"><span data-stu-id="c3196-110">Authority-Revocation-List</span></span>                             |
| <span data-ttu-id="c3196-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="c3196-111">Ldap-Display-Name</span></span> | <span data-ttu-id="c3196-112">authorityRevocationList</span><span class="sxs-lookup"><span data-stu-id="c3196-112">authorityRevocationList</span></span>                               |
| <span data-ttu-id="c3196-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="c3196-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="c3196-114">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="c3196-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="c3196-115">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="c3196-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="c3196-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c3196-116">Attribute-Id</span></span>      | <span data-ttu-id="c3196-117">2.5.4.38</span><span class="sxs-lookup"><span data-stu-id="c3196-117">2.5.4.38</span></span>                                              |
| <span data-ttu-id="c3196-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="c3196-118">System-Id-Guid</span></span>    | <span data-ttu-id="c3196-119">1677578d-47f3-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="c3196-119">1677578d-47f3-11d1-a9c3-0000f80367c1</span></span>                  |
| <span data-ttu-id="c3196-120">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c3196-120">Syntax</span></span>            | [<span data-ttu-id="c3196-121">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="c3196-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="c3196-122">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="c3196-122">Implementations</span></span>

-   [<span data-ttu-id="c3196-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="c3196-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="c3196-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c3196-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c3196-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c3196-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c3196-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c3196-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c3196-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c3196-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c3196-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c3196-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="c3196-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c3196-129">Windows 2000 Server</span></span>



| <span data-ttu-id="c3196-130">Voce</span><span class="sxs-lookup"><span data-stu-id="c3196-130">Entry</span></span> | <span data-ttu-id="c3196-131">Valore</span><span class="sxs-lookup"><span data-stu-id="c3196-131">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3196-132">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="c3196-132">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="c3196-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c3196-133">MAPI-Id</span></span>                | <span data-ttu-id="c3196-134">0x8026</span><span class="sxs-lookup"><span data-stu-id="c3196-134">0x8026</span></span>                                                                                                                                     |
| <span data-ttu-id="c3196-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="c3196-135">System-Only</span></span>            | <span data-ttu-id="c3196-136">Falso</span><span class="sxs-lookup"><span data-stu-id="c3196-136">False</span></span>                                                                                                                                      |
| <span data-ttu-id="c3196-137">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="c3196-137">Is-Single-Valued</span></span>       | <span data-ttu-id="c3196-138">Falso</span><span class="sxs-lookup"><span data-stu-id="c3196-138">False</span></span>                                                                                                                                      |
| <span data-ttu-id="c3196-139">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="c3196-139">Is Indexed</span></span>             | <span data-ttu-id="c3196-140">Falso</span><span class="sxs-lookup"><span data-stu-id="c3196-140">False</span></span>                                                                                                                                      |
| <span data-ttu-id="c3196-141">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="c3196-141">In Global Catalog</span></span>      | <span data-ttu-id="c3196-142">Falso</span><span class="sxs-lookup"><span data-stu-id="c3196-142">False</span></span>                                                                                                                                      |
| <span data-ttu-id="c3196-143">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="c3196-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="c3196-144">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="c3196-144">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="c3196-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c3196-145">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="c3196-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c3196-146">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="c3196-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c3196-147">Search-Flags</span></span>           | <span data-ttu-id="c3196-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c3196-148">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="c3196-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c3196-149">System-Flags</span></span>           | <span data-ttu-id="c3196-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c3196-150">0x00000010</span></span>                                                                                                                                 |
| <span data-ttu-id="c3196-151">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="c3196-151">Classes used in</span></span>        | [<span data-ttu-id="c3196-152">**Autorità di certificazione**</span><span class="sxs-lookup"><span data-stu-id="c3196-152">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="c3196-153">**CRL-punto di distribuzione**</span><span class="sxs-lookup"><span data-stu-id="c3196-153">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="c3196-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c3196-154">Windows Server 2003</span></span>



| <span data-ttu-id="c3196-155">Voce</span><span class="sxs-lookup"><span data-stu-id="c3196-155">Entry</span></span> | <span data-ttu-id="c3196-156">Valore</span><span class="sxs-lookup"><span data-stu-id="c3196-156">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3196-157">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="c3196-157">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="c3196-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c3196-158">MAPI-Id</span></span>                | <span data-ttu-id="c3196-159">0x8026</span><span class="sxs-lookup"><span data-stu-id="c3196-159">0x8026</span></span>                                                                                                                                     |
| <span data-ttu-id="c3196-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="c3196-160">System-Only</span></span>            | <span data-ttu-id="c3196-161">Falso</span><span class="sxs-lookup"><span data-stu-id="c3196-161">False</span></span>                                                                                                                                      |
| <span data-ttu-id="c3196-162">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="c3196-162">Is-Single-Valued</span></span>       | <span data-ttu-id="c3196-163">Falso</span><span class="sxs-lookup"><span data-stu-id="c3196-163">False</span></span>                                                                                                                                      |
| <span data-ttu-id="c3196-164">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="c3196-164">Is Indexed</span></span>             | <span data-ttu-id="c3196-165">Falso</span><span class="sxs-lookup"><span data-stu-id="c3196-165">False</span></span>                                                                                                                                      |
| <span data-ttu-id="c3196-166">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="c3196-166">In Global Catalog</span></span>      | <span data-ttu-id="c3196-167">Falso</span><span class="sxs-lookup"><span data-stu-id="c3196-167">False</span></span>                                                                                                                                      |
| <span data-ttu-id="c3196-168">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="c3196-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="c3196-169">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="c3196-169">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="c3196-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c3196-170">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="c3196-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c3196-171">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="c3196-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c3196-172">Search-Flags</span></span>           | <span data-ttu-id="c3196-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c3196-173">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="c3196-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c3196-174">System-Flags</span></span>           | <span data-ttu-id="c3196-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c3196-175">0x00000010</span></span>                                                                                                                                 |
| <span data-ttu-id="c3196-176">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="c3196-176">Classes used in</span></span>        | [<span data-ttu-id="c3196-177">**Autorità di certificazione**</span><span class="sxs-lookup"><span data-stu-id="c3196-177">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="c3196-178">**CRL-punto di distribuzione**</span><span class="sxs-lookup"><span data-stu-id="c3196-178">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c3196-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c3196-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c3196-180">Voce</span><span class="sxs-lookup"><span data-stu-id="c3196-180">Entry</span></span> | <span data-ttu-id="c3196-181">Valore</span><span class="sxs-lookup"><span data-stu-id="c3196-181">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3196-182">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="c3196-182">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="c3196-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c3196-183">MAPI-Id</span></span>                | <span data-ttu-id="c3196-184">0x8026</span><span class="sxs-lookup"><span data-stu-id="c3196-184">0x8026</span></span>                                                                                                                                     |
| <span data-ttu-id="c3196-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="c3196-185">System-Only</span></span>            | <span data-ttu-id="c3196-186">Falso</span><span class="sxs-lookup"><span data-stu-id="c3196-186">False</span></span>                                                                                                                                      |
| <span data-ttu-id="c3196-187">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="c3196-187">Is-Single-Valued</span></span>       | <span data-ttu-id="c3196-188">Falso</span><span class="sxs-lookup"><span data-stu-id="c3196-188">False</span></span>                                                                                                                                      |
| <span data-ttu-id="c3196-189">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="c3196-189">Is Indexed</span></span>             | <span data-ttu-id="c3196-190">Falso</span><span class="sxs-lookup"><span data-stu-id="c3196-190">False</span></span>                                                                                                                                      |
| <span data-ttu-id="c3196-191">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="c3196-191">In Global Catalog</span></span>      | <span data-ttu-id="c3196-192">Falso</span><span class="sxs-lookup"><span data-stu-id="c3196-192">False</span></span>                                                                                                                                      |
| <span data-ttu-id="c3196-193">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="c3196-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="c3196-194">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="c3196-194">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="c3196-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c3196-195">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="c3196-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c3196-196">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="c3196-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c3196-197">Search-Flags</span></span>           | <span data-ttu-id="c3196-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c3196-198">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="c3196-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c3196-199">System-Flags</span></span>           | <span data-ttu-id="c3196-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c3196-200">0x00000010</span></span>                                                                                                                                 |
| <span data-ttu-id="c3196-201">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="c3196-201">Classes used in</span></span>        | [<span data-ttu-id="c3196-202">**Autorità di certificazione**</span><span class="sxs-lookup"><span data-stu-id="c3196-202">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="c3196-203">**CRL-punto di distribuzione**</span><span class="sxs-lookup"><span data-stu-id="c3196-203">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c3196-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c3196-204">Windows Server 2008</span></span>



| <span data-ttu-id="c3196-205">Voce</span><span class="sxs-lookup"><span data-stu-id="c3196-205">Entry</span></span> | <span data-ttu-id="c3196-206">Valore</span><span class="sxs-lookup"><span data-stu-id="c3196-206">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3196-207">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="c3196-207">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="c3196-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c3196-208">MAPI-Id</span></span>                | <span data-ttu-id="c3196-209">0x8026</span><span class="sxs-lookup"><span data-stu-id="c3196-209">0x8026</span></span>                                                                                                                                     |
| <span data-ttu-id="c3196-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="c3196-210">System-Only</span></span>            | <span data-ttu-id="c3196-211">Falso</span><span class="sxs-lookup"><span data-stu-id="c3196-211">False</span></span>                                                                                                                                      |
| <span data-ttu-id="c3196-212">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="c3196-212">Is-Single-Valued</span></span>       | <span data-ttu-id="c3196-213">Falso</span><span class="sxs-lookup"><span data-stu-id="c3196-213">False</span></span>                                                                                                                                      |
| <span data-ttu-id="c3196-214">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="c3196-214">Is Indexed</span></span>             | <span data-ttu-id="c3196-215">Falso</span><span class="sxs-lookup"><span data-stu-id="c3196-215">False</span></span>                                                                                                                                      |
| <span data-ttu-id="c3196-216">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="c3196-216">In Global Catalog</span></span>      | <span data-ttu-id="c3196-217">Falso</span><span class="sxs-lookup"><span data-stu-id="c3196-217">False</span></span>                                                                                                                                      |
| <span data-ttu-id="c3196-218">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="c3196-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="c3196-219">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="c3196-219">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="c3196-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c3196-220">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="c3196-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c3196-221">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="c3196-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c3196-222">Search-Flags</span></span>           | <span data-ttu-id="c3196-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c3196-223">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="c3196-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c3196-224">System-Flags</span></span>           | <span data-ttu-id="c3196-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c3196-225">0x00000010</span></span>                                                                                                                                 |
| <span data-ttu-id="c3196-226">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="c3196-226">Classes used in</span></span>        | [<span data-ttu-id="c3196-227">**Autorità di certificazione**</span><span class="sxs-lookup"><span data-stu-id="c3196-227">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="c3196-228">**CRL-punto di distribuzione**</span><span class="sxs-lookup"><span data-stu-id="c3196-228">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c3196-229">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c3196-229">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c3196-230">Voce</span><span class="sxs-lookup"><span data-stu-id="c3196-230">Entry</span></span> | <span data-ttu-id="c3196-231">Valore</span><span class="sxs-lookup"><span data-stu-id="c3196-231">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3196-232">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="c3196-232">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="c3196-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c3196-233">MAPI-Id</span></span>                | <span data-ttu-id="c3196-234">0x8026</span><span class="sxs-lookup"><span data-stu-id="c3196-234">0x8026</span></span>                                                                                                                                     |
| <span data-ttu-id="c3196-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="c3196-235">System-Only</span></span>            | <span data-ttu-id="c3196-236">Falso</span><span class="sxs-lookup"><span data-stu-id="c3196-236">False</span></span>                                                                                                                                      |
| <span data-ttu-id="c3196-237">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="c3196-237">Is-Single-Valued</span></span>       | <span data-ttu-id="c3196-238">Falso</span><span class="sxs-lookup"><span data-stu-id="c3196-238">False</span></span>                                                                                                                                      |
| <span data-ttu-id="c3196-239">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="c3196-239">Is Indexed</span></span>             | <span data-ttu-id="c3196-240">Falso</span><span class="sxs-lookup"><span data-stu-id="c3196-240">False</span></span>                                                                                                                                      |
| <span data-ttu-id="c3196-241">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="c3196-241">In Global Catalog</span></span>      | <span data-ttu-id="c3196-242">Falso</span><span class="sxs-lookup"><span data-stu-id="c3196-242">False</span></span>                                                                                                                                      |
| <span data-ttu-id="c3196-243">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="c3196-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="c3196-244">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="c3196-244">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="c3196-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c3196-245">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="c3196-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c3196-246">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="c3196-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c3196-247">Search-Flags</span></span>           | <span data-ttu-id="c3196-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c3196-248">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="c3196-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c3196-249">System-Flags</span></span>           | <span data-ttu-id="c3196-250">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c3196-250">0x00000010</span></span>                                                                                                                                 |
| <span data-ttu-id="c3196-251">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="c3196-251">Classes used in</span></span>        | [<span data-ttu-id="c3196-252">**Autorità di certificazione**</span><span class="sxs-lookup"><span data-stu-id="c3196-252">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="c3196-253">**CRL-punto di distribuzione**</span><span class="sxs-lookup"><span data-stu-id="c3196-253">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c3196-254">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c3196-254">Windows Server 2012</span></span>



| <span data-ttu-id="c3196-255">Voce</span><span class="sxs-lookup"><span data-stu-id="c3196-255">Entry</span></span> | <span data-ttu-id="c3196-256">Valore</span><span class="sxs-lookup"><span data-stu-id="c3196-256">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3196-257">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="c3196-257">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="c3196-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c3196-258">MAPI-Id</span></span>                | <span data-ttu-id="c3196-259">0x8026</span><span class="sxs-lookup"><span data-stu-id="c3196-259">0x8026</span></span>                                                                                                                                     |
| <span data-ttu-id="c3196-260">System-Only</span><span class="sxs-lookup"><span data-stu-id="c3196-260">System-Only</span></span>            | <span data-ttu-id="c3196-261">Falso</span><span class="sxs-lookup"><span data-stu-id="c3196-261">False</span></span>                                                                                                                                      |
| <span data-ttu-id="c3196-262">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="c3196-262">Is-Single-Valued</span></span>       | <span data-ttu-id="c3196-263">Falso</span><span class="sxs-lookup"><span data-stu-id="c3196-263">False</span></span>                                                                                                                                      |
| <span data-ttu-id="c3196-264">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="c3196-264">Is Indexed</span></span>             | <span data-ttu-id="c3196-265">Falso</span><span class="sxs-lookup"><span data-stu-id="c3196-265">False</span></span>                                                                                                                                      |
| <span data-ttu-id="c3196-266">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="c3196-266">In Global Catalog</span></span>      | <span data-ttu-id="c3196-267">Falso</span><span class="sxs-lookup"><span data-stu-id="c3196-267">False</span></span>                                                                                                                                      |
| <span data-ttu-id="c3196-268">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="c3196-268">NT-Security-Descriptor</span></span> | <span data-ttu-id="c3196-269">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="c3196-269">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="c3196-270">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c3196-270">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="c3196-271">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c3196-271">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="c3196-272">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c3196-272">Search-Flags</span></span>           | <span data-ttu-id="c3196-273">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c3196-273">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="c3196-274">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c3196-274">System-Flags</span></span>           | <span data-ttu-id="c3196-275">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c3196-275">0x00000010</span></span>                                                                                                                                 |
| <span data-ttu-id="c3196-276">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="c3196-276">Classes used in</span></span>        | [<span data-ttu-id="c3196-277">**Autorità di certificazione**</span><span class="sxs-lookup"><span data-stu-id="c3196-277">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="c3196-278">**CRL-punto di distribuzione**</span><span class="sxs-lookup"><span data-stu-id="c3196-278">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



 

 





