---
title: attributo ms-DS-has-Domain-NCs
description: Informazioni di replica del servizio directory che illustrano in dettaglio i contesti di denominazione dei domini presenti in un determinato server.
ms.assetid: e5a7c371-5a37-466e-b56f-ee261b48e3b2
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo ms-DS-has-Domain-NCs
- attributo msDS-HasDomainNCs-schema AD
topic_type:
- apiref
api_name:
- ms-DS-Has-Domain-NCs
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83b946286974cc6ba4e6d30484e7768a1daeccb6
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104480097"
---
# <a name="ms-ds-has-domain-ncs-attribute"></a><span data-ttu-id="acd48-105">attributo ms-DS-has-Domain-NCs</span><span class="sxs-lookup"><span data-stu-id="acd48-105">ms-DS-Has-Domain-NCs attribute</span></span>

<span data-ttu-id="acd48-106">Informazioni di replica del servizio directory che illustrano in dettaglio i contesti di denominazione dei domini presenti in un determinato server.</span><span class="sxs-lookup"><span data-stu-id="acd48-106">Directory service replication information that details the domain naming contexts present on a particular server.</span></span>



| <span data-ttu-id="acd48-107">Voce</span><span class="sxs-lookup"><span data-stu-id="acd48-107">Entry</span></span> | <span data-ttu-id="acd48-108">Valore</span><span class="sxs-lookup"><span data-stu-id="acd48-108">Value</span></span> |
|-------------------|-----------------------------------------------------|
| <span data-ttu-id="acd48-109">CN</span><span class="sxs-lookup"><span data-stu-id="acd48-109">CN</span></span>                | <span data-ttu-id="acd48-110">ms-DS-has-Domain-NCs</span><span class="sxs-lookup"><span data-stu-id="acd48-110">ms-DS-Has-Domain-NCs</span></span>                                |
| <span data-ttu-id="acd48-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="acd48-111">Ldap-Display-Name</span></span> | <span data-ttu-id="acd48-112">msDS-HasDomainNCs</span><span class="sxs-lookup"><span data-stu-id="acd48-112">msDS-HasDomainNCs</span></span>                                   |
| <span data-ttu-id="acd48-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="acd48-113">Size</span></span>              | \-                                                  |
| <span data-ttu-id="acd48-114">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="acd48-114">Update Privilege</span></span>  | <span data-ttu-id="acd48-115">Questo valore viene impostato dal sistema</span><span class="sxs-lookup"><span data-stu-id="acd48-115">This value is set by the system</span></span>                     |
| <span data-ttu-id="acd48-116">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="acd48-116">Update Frequency</span></span>  | <span data-ttu-id="acd48-117">Viene impostato da DCPromo e mai modificato successivamente.</span><span class="sxs-lookup"><span data-stu-id="acd48-117">It is set by DCPromo and never modified thereafter.</span></span> |
| <span data-ttu-id="acd48-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="acd48-118">Attribute-Id</span></span>      | <span data-ttu-id="acd48-119">1.2.840.113556.1.4.1820</span><span class="sxs-lookup"><span data-stu-id="acd48-119">1.2.840.113556.1.4.1820</span></span>                             |
| <span data-ttu-id="acd48-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="acd48-120">System-Id-Guid</span></span>    | <span data-ttu-id="acd48-121">6f17e347-a842-4498-b8b3-15e007da4fed</span><span class="sxs-lookup"><span data-stu-id="acd48-121">6f17e347-a842-4498-b8b3-15e007da4fed</span></span>                |
| <span data-ttu-id="acd48-122">Sintassi</span><span class="sxs-lookup"><span data-stu-id="acd48-122">Syntax</span></span>            | [<span data-ttu-id="acd48-123">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="acd48-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md)             |



## <a name="implementations"></a><span data-ttu-id="acd48-124">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="acd48-124">Implementations</span></span>

-   [<span data-ttu-id="acd48-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="acd48-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="acd48-126">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="acd48-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="acd48-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="acd48-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="acd48-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="acd48-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="acd48-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="acd48-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="acd48-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="acd48-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="acd48-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="acd48-131">Windows Server 2003</span></span>



| <span data-ttu-id="acd48-132">Voce</span><span class="sxs-lookup"><span data-stu-id="acd48-132">Entry</span></span> | <span data-ttu-id="acd48-133">Valore</span><span class="sxs-lookup"><span data-stu-id="acd48-133">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="acd48-134">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="acd48-134">Link-Id</span></span>                | <span data-ttu-id="acd48-135">2026</span><span class="sxs-lookup"><span data-stu-id="acd48-135">2026</span></span>                                     |
| <span data-ttu-id="acd48-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="acd48-136">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="acd48-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="acd48-137">System-Only</span></span>            | <span data-ttu-id="acd48-138">Vero</span><span class="sxs-lookup"><span data-stu-id="acd48-138">True</span></span>                                     |
| <span data-ttu-id="acd48-139">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="acd48-139">Is-Single-Valued</span></span>       | <span data-ttu-id="acd48-140">Falso</span><span class="sxs-lookup"><span data-stu-id="acd48-140">False</span></span>                                    |
| <span data-ttu-id="acd48-141">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="acd48-141">Is Indexed</span></span>             | <span data-ttu-id="acd48-142">Falso</span><span class="sxs-lookup"><span data-stu-id="acd48-142">False</span></span>                                    |
| <span data-ttu-id="acd48-143">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="acd48-143">In Global Catalog</span></span>      | <span data-ttu-id="acd48-144">Falso</span><span class="sxs-lookup"><span data-stu-id="acd48-144">False</span></span>                                    |
| <span data-ttu-id="acd48-145">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="acd48-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="acd48-146">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="acd48-146">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="acd48-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="acd48-147">Range-Lower</span></span>            | <span data-ttu-id="acd48-148">4</span><span class="sxs-lookup"><span data-stu-id="acd48-148">4</span></span>                                        |
| <span data-ttu-id="acd48-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="acd48-149">Range-Upper</span></span>            | <span data-ttu-id="acd48-150">4</span><span class="sxs-lookup"><span data-stu-id="acd48-150">4</span></span>                                        |
| <span data-ttu-id="acd48-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="acd48-151">Search-Flags</span></span>           | <span data-ttu-id="acd48-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="acd48-152">0x00000000</span></span>                               |
| <span data-ttu-id="acd48-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="acd48-153">System-Flags</span></span>           | <span data-ttu-id="acd48-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="acd48-154">0x00000010</span></span>                               |
| <span data-ttu-id="acd48-155">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="acd48-155">Classes used in</span></span>        | [<span data-ttu-id="acd48-156">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="acd48-156">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="adam"></a><span data-ttu-id="acd48-157">ADAM</span><span class="sxs-lookup"><span data-stu-id="acd48-157">ADAM</span></span>



| <span data-ttu-id="acd48-158">Voce</span><span class="sxs-lookup"><span data-stu-id="acd48-158">Entry</span></span> | <span data-ttu-id="acd48-159">Valore</span><span class="sxs-lookup"><span data-stu-id="acd48-159">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="acd48-160">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="acd48-160">Link-Id</span></span>                | <span data-ttu-id="acd48-161">2026</span><span class="sxs-lookup"><span data-stu-id="acd48-161">2026</span></span>                                     |
| <span data-ttu-id="acd48-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="acd48-162">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="acd48-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="acd48-163">System-Only</span></span>            | <span data-ttu-id="acd48-164">Vero</span><span class="sxs-lookup"><span data-stu-id="acd48-164">True</span></span>                                     |
| <span data-ttu-id="acd48-165">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="acd48-165">Is-Single-Valued</span></span>       | <span data-ttu-id="acd48-166">Falso</span><span class="sxs-lookup"><span data-stu-id="acd48-166">False</span></span>                                    |
| <span data-ttu-id="acd48-167">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="acd48-167">Is Indexed</span></span>             | <span data-ttu-id="acd48-168">Falso</span><span class="sxs-lookup"><span data-stu-id="acd48-168">False</span></span>                                    |
| <span data-ttu-id="acd48-169">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="acd48-169">In Global Catalog</span></span>      | <span data-ttu-id="acd48-170">Falso</span><span class="sxs-lookup"><span data-stu-id="acd48-170">False</span></span>                                    |
| <span data-ttu-id="acd48-171">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="acd48-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="acd48-172">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="acd48-172">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="acd48-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="acd48-173">Range-Lower</span></span>            | <span data-ttu-id="acd48-174">4</span><span class="sxs-lookup"><span data-stu-id="acd48-174">4</span></span>                                        |
| <span data-ttu-id="acd48-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="acd48-175">Range-Upper</span></span>            | <span data-ttu-id="acd48-176">4</span><span class="sxs-lookup"><span data-stu-id="acd48-176">4</span></span>                                        |
| <span data-ttu-id="acd48-177">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="acd48-177">Search-Flags</span></span>           | <span data-ttu-id="acd48-178">0x00000000</span><span class="sxs-lookup"><span data-stu-id="acd48-178">0x00000000</span></span>                               |
| <span data-ttu-id="acd48-179">System-Flags</span><span class="sxs-lookup"><span data-stu-id="acd48-179">System-Flags</span></span>           | <span data-ttu-id="acd48-180">0x00000010</span><span class="sxs-lookup"><span data-stu-id="acd48-180">0x00000010</span></span>                               |
| <span data-ttu-id="acd48-181">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="acd48-181">Classes used in</span></span>        | [<span data-ttu-id="acd48-182">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="acd48-182">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="acd48-183">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="acd48-183">Windows Server 2003 R2</span></span>



| <span data-ttu-id="acd48-184">Voce</span><span class="sxs-lookup"><span data-stu-id="acd48-184">Entry</span></span> | <span data-ttu-id="acd48-185">Valore</span><span class="sxs-lookup"><span data-stu-id="acd48-185">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="acd48-186">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="acd48-186">Link-Id</span></span>                | <span data-ttu-id="acd48-187">2026</span><span class="sxs-lookup"><span data-stu-id="acd48-187">2026</span></span>                                     |
| <span data-ttu-id="acd48-188">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="acd48-188">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="acd48-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="acd48-189">System-Only</span></span>            | <span data-ttu-id="acd48-190">Vero</span><span class="sxs-lookup"><span data-stu-id="acd48-190">True</span></span>                                     |
| <span data-ttu-id="acd48-191">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="acd48-191">Is-Single-Valued</span></span>       | <span data-ttu-id="acd48-192">Falso</span><span class="sxs-lookup"><span data-stu-id="acd48-192">False</span></span>                                    |
| <span data-ttu-id="acd48-193">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="acd48-193">Is Indexed</span></span>             | <span data-ttu-id="acd48-194">Falso</span><span class="sxs-lookup"><span data-stu-id="acd48-194">False</span></span>                                    |
| <span data-ttu-id="acd48-195">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="acd48-195">In Global Catalog</span></span>      | <span data-ttu-id="acd48-196">Falso</span><span class="sxs-lookup"><span data-stu-id="acd48-196">False</span></span>                                    |
| <span data-ttu-id="acd48-197">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="acd48-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="acd48-198">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="acd48-198">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="acd48-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="acd48-199">Range-Lower</span></span>            | <span data-ttu-id="acd48-200">4</span><span class="sxs-lookup"><span data-stu-id="acd48-200">4</span></span>                                        |
| <span data-ttu-id="acd48-201">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="acd48-201">Range-Upper</span></span>            | <span data-ttu-id="acd48-202">4</span><span class="sxs-lookup"><span data-stu-id="acd48-202">4</span></span>                                        |
| <span data-ttu-id="acd48-203">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="acd48-203">Search-Flags</span></span>           | <span data-ttu-id="acd48-204">0x00000000</span><span class="sxs-lookup"><span data-stu-id="acd48-204">0x00000000</span></span>                               |
| <span data-ttu-id="acd48-205">System-Flags</span><span class="sxs-lookup"><span data-stu-id="acd48-205">System-Flags</span></span>           | <span data-ttu-id="acd48-206">0x00000010</span><span class="sxs-lookup"><span data-stu-id="acd48-206">0x00000010</span></span>                               |
| <span data-ttu-id="acd48-207">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="acd48-207">Classes used in</span></span>        | [<span data-ttu-id="acd48-208">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="acd48-208">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="acd48-209">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="acd48-209">Windows Server 2008</span></span>



| <span data-ttu-id="acd48-210">Voce</span><span class="sxs-lookup"><span data-stu-id="acd48-210">Entry</span></span> | <span data-ttu-id="acd48-211">Valore</span><span class="sxs-lookup"><span data-stu-id="acd48-211">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="acd48-212">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="acd48-212">Link-Id</span></span>                | <span data-ttu-id="acd48-213">2026</span><span class="sxs-lookup"><span data-stu-id="acd48-213">2026</span></span>                                     |
| <span data-ttu-id="acd48-214">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="acd48-214">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="acd48-215">System-Only</span><span class="sxs-lookup"><span data-stu-id="acd48-215">System-Only</span></span>            | <span data-ttu-id="acd48-216">Vero</span><span class="sxs-lookup"><span data-stu-id="acd48-216">True</span></span>                                     |
| <span data-ttu-id="acd48-217">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="acd48-217">Is-Single-Valued</span></span>       | <span data-ttu-id="acd48-218">Falso</span><span class="sxs-lookup"><span data-stu-id="acd48-218">False</span></span>                                    |
| <span data-ttu-id="acd48-219">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="acd48-219">Is Indexed</span></span>             | <span data-ttu-id="acd48-220">Falso</span><span class="sxs-lookup"><span data-stu-id="acd48-220">False</span></span>                                    |
| <span data-ttu-id="acd48-221">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="acd48-221">In Global Catalog</span></span>      | <span data-ttu-id="acd48-222">Falso</span><span class="sxs-lookup"><span data-stu-id="acd48-222">False</span></span>                                    |
| <span data-ttu-id="acd48-223">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="acd48-223">NT-Security-Descriptor</span></span> | <span data-ttu-id="acd48-224">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="acd48-224">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="acd48-225">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="acd48-225">Range-Lower</span></span>            | <span data-ttu-id="acd48-226">4</span><span class="sxs-lookup"><span data-stu-id="acd48-226">4</span></span>                                        |
| <span data-ttu-id="acd48-227">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="acd48-227">Range-Upper</span></span>            | <span data-ttu-id="acd48-228">4</span><span class="sxs-lookup"><span data-stu-id="acd48-228">4</span></span>                                        |
| <span data-ttu-id="acd48-229">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="acd48-229">Search-Flags</span></span>           | <span data-ttu-id="acd48-230">0x00000000</span><span class="sxs-lookup"><span data-stu-id="acd48-230">0x00000000</span></span>                               |
| <span data-ttu-id="acd48-231">System-Flags</span><span class="sxs-lookup"><span data-stu-id="acd48-231">System-Flags</span></span>           | <span data-ttu-id="acd48-232">0x00000010</span><span class="sxs-lookup"><span data-stu-id="acd48-232">0x00000010</span></span>                               |
| <span data-ttu-id="acd48-233">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="acd48-233">Classes used in</span></span>        | [<span data-ttu-id="acd48-234">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="acd48-234">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="acd48-235">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="acd48-235">Windows Server 2008 R2</span></span>



| <span data-ttu-id="acd48-236">Voce</span><span class="sxs-lookup"><span data-stu-id="acd48-236">Entry</span></span> | <span data-ttu-id="acd48-237">Valore</span><span class="sxs-lookup"><span data-stu-id="acd48-237">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="acd48-238">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="acd48-238">Link-Id</span></span>                | <span data-ttu-id="acd48-239">2026</span><span class="sxs-lookup"><span data-stu-id="acd48-239">2026</span></span>                                     |
| <span data-ttu-id="acd48-240">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="acd48-240">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="acd48-241">System-Only</span><span class="sxs-lookup"><span data-stu-id="acd48-241">System-Only</span></span>            | <span data-ttu-id="acd48-242">Vero</span><span class="sxs-lookup"><span data-stu-id="acd48-242">True</span></span>                                     |
| <span data-ttu-id="acd48-243">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="acd48-243">Is-Single-Valued</span></span>       | <span data-ttu-id="acd48-244">Falso</span><span class="sxs-lookup"><span data-stu-id="acd48-244">False</span></span>                                    |
| <span data-ttu-id="acd48-245">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="acd48-245">Is Indexed</span></span>             | <span data-ttu-id="acd48-246">Falso</span><span class="sxs-lookup"><span data-stu-id="acd48-246">False</span></span>                                    |
| <span data-ttu-id="acd48-247">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="acd48-247">In Global Catalog</span></span>      | <span data-ttu-id="acd48-248">Falso</span><span class="sxs-lookup"><span data-stu-id="acd48-248">False</span></span>                                    |
| <span data-ttu-id="acd48-249">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="acd48-249">NT-Security-Descriptor</span></span> | <span data-ttu-id="acd48-250">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="acd48-250">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="acd48-251">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="acd48-251">Range-Lower</span></span>            | <span data-ttu-id="acd48-252">4</span><span class="sxs-lookup"><span data-stu-id="acd48-252">4</span></span>                                        |
| <span data-ttu-id="acd48-253">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="acd48-253">Range-Upper</span></span>            | <span data-ttu-id="acd48-254">4</span><span class="sxs-lookup"><span data-stu-id="acd48-254">4</span></span>                                        |
| <span data-ttu-id="acd48-255">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="acd48-255">Search-Flags</span></span>           | <span data-ttu-id="acd48-256">0x00000000</span><span class="sxs-lookup"><span data-stu-id="acd48-256">0x00000000</span></span>                               |
| <span data-ttu-id="acd48-257">System-Flags</span><span class="sxs-lookup"><span data-stu-id="acd48-257">System-Flags</span></span>           | <span data-ttu-id="acd48-258">0x00000010</span><span class="sxs-lookup"><span data-stu-id="acd48-258">0x00000010</span></span>                               |
| <span data-ttu-id="acd48-259">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="acd48-259">Classes used in</span></span>        | [<span data-ttu-id="acd48-260">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="acd48-260">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="acd48-261">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="acd48-261">Windows Server 2012</span></span>



| <span data-ttu-id="acd48-262">Voce</span><span class="sxs-lookup"><span data-stu-id="acd48-262">Entry</span></span> | <span data-ttu-id="acd48-263">Valore</span><span class="sxs-lookup"><span data-stu-id="acd48-263">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="acd48-264">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="acd48-264">Link-Id</span></span>                | <span data-ttu-id="acd48-265">2026</span><span class="sxs-lookup"><span data-stu-id="acd48-265">2026</span></span>                                     |
| <span data-ttu-id="acd48-266">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="acd48-266">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="acd48-267">System-Only</span><span class="sxs-lookup"><span data-stu-id="acd48-267">System-Only</span></span>            | <span data-ttu-id="acd48-268">Vero</span><span class="sxs-lookup"><span data-stu-id="acd48-268">True</span></span>                                     |
| <span data-ttu-id="acd48-269">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="acd48-269">Is-Single-Valued</span></span>       | <span data-ttu-id="acd48-270">Falso</span><span class="sxs-lookup"><span data-stu-id="acd48-270">False</span></span>                                    |
| <span data-ttu-id="acd48-271">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="acd48-271">Is Indexed</span></span>             | <span data-ttu-id="acd48-272">Falso</span><span class="sxs-lookup"><span data-stu-id="acd48-272">False</span></span>                                    |
| <span data-ttu-id="acd48-273">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="acd48-273">In Global Catalog</span></span>      | <span data-ttu-id="acd48-274">Falso</span><span class="sxs-lookup"><span data-stu-id="acd48-274">False</span></span>                                    |
| <span data-ttu-id="acd48-275">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="acd48-275">NT-Security-Descriptor</span></span> | <span data-ttu-id="acd48-276">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="acd48-276">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="acd48-277">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="acd48-277">Range-Lower</span></span>            | <span data-ttu-id="acd48-278">4</span><span class="sxs-lookup"><span data-stu-id="acd48-278">4</span></span>                                        |
| <span data-ttu-id="acd48-279">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="acd48-279">Range-Upper</span></span>            | <span data-ttu-id="acd48-280">4</span><span class="sxs-lookup"><span data-stu-id="acd48-280">4</span></span>                                        |
| <span data-ttu-id="acd48-281">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="acd48-281">Search-Flags</span></span>           | <span data-ttu-id="acd48-282">0x00000000</span><span class="sxs-lookup"><span data-stu-id="acd48-282">0x00000000</span></span>                               |
| <span data-ttu-id="acd48-283">System-Flags</span><span class="sxs-lookup"><span data-stu-id="acd48-283">System-Flags</span></span>           | <span data-ttu-id="acd48-284">0x00000010</span><span class="sxs-lookup"><span data-stu-id="acd48-284">0x00000010</span></span>                               |
| <span data-ttu-id="acd48-285">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="acd48-285">Classes used in</span></span>        | [<span data-ttu-id="acd48-286">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="acd48-286">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



 

 





