---
title: attributo ms-DS-has-Master-NCs
description: Contiene i contesti di denominazione contenuti in un controller di dominio. Questo attributo è deprecato con-Master-NCs.
ms.assetid: 5325db42-afd7-472c-8797-447e752a3907
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo ms-DS-has-Master-NCs
- attributo msDS-hasMasterNCs-schema AD
topic_type:
- apiref
api_name:
- ms-DS-Has-Master-NCs
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24507460eaa7653cfc2c98d3772942de9936162c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103875718"
---
# <a name="ms-ds-has-master-ncs-attribute"></a><span data-ttu-id="c9ee1-106">attributo ms-DS-has-Master-NCs</span><span class="sxs-lookup"><span data-stu-id="c9ee1-106">ms-DS-Has-Master-NCs attribute</span></span>

<span data-ttu-id="c9ee1-107">Contiene i contesti di denominazione contenuti in un controller di dominio.</span><span class="sxs-lookup"><span data-stu-id="c9ee1-107">Contains the naming contexts held by a domain controller.</span></span> <span data-ttu-id="c9ee1-108">Questo attributo è deprecato con-Master-NCs.</span><span class="sxs-lookup"><span data-stu-id="c9ee1-108">This attribute deprecates has-Master-NCs.</span></span>



| <span data-ttu-id="c9ee1-109">Voce</span><span class="sxs-lookup"><span data-stu-id="c9ee1-109">Entry</span></span> | <span data-ttu-id="c9ee1-110">Valore</span><span class="sxs-lookup"><span data-stu-id="c9ee1-110">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="c9ee1-111">CN</span><span class="sxs-lookup"><span data-stu-id="c9ee1-111">CN</span></span>                | <span data-ttu-id="c9ee1-112">ms-DS-has-Master-NCs</span><span class="sxs-lookup"><span data-stu-id="c9ee1-112">ms-DS-Has-Master-NCs</span></span>                    |
| <span data-ttu-id="c9ee1-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="c9ee1-113">Ldap-Display-Name</span></span> | <span data-ttu-id="c9ee1-114">msDS-hasMasterNCs</span><span class="sxs-lookup"><span data-stu-id="c9ee1-114">msDS-hasMasterNCs</span></span>                       |
| <span data-ttu-id="c9ee1-115">Dimensione</span><span class="sxs-lookup"><span data-stu-id="c9ee1-115">Size</span></span>              | \-                                      |
| <span data-ttu-id="c9ee1-116">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="c9ee1-116">Update Privilege</span></span>  | <span data-ttu-id="c9ee1-117">Questo valore viene impostato dal sistema</span><span class="sxs-lookup"><span data-stu-id="c9ee1-117">This value is set by the system</span></span>         |
| <span data-ttu-id="c9ee1-118">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="c9ee1-118">Update Frequency</span></span>  | <span data-ttu-id="c9ee1-119">Ogni volta che viene creato un nuovo NC.</span><span class="sxs-lookup"><span data-stu-id="c9ee1-119">Each time a new NC is created.</span></span>          |
| <span data-ttu-id="c9ee1-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c9ee1-120">Attribute-Id</span></span>      | <span data-ttu-id="c9ee1-121">1.2.840.113556.1.4.1836</span><span class="sxs-lookup"><span data-stu-id="c9ee1-121">1.2.840.113556.1.4.1836</span></span>                 |
| <span data-ttu-id="c9ee1-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="c9ee1-122">System-Id-Guid</span></span>    | <span data-ttu-id="c9ee1-123">ae2de0e2-59d7-4d47-8d47-ed4dfe4357ad</span><span class="sxs-lookup"><span data-stu-id="c9ee1-123">ae2de0e2-59d7-4d47-8d47-ed4dfe4357ad</span></span>    |
| <span data-ttu-id="c9ee1-124">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c9ee1-124">Syntax</span></span>            | [<span data-ttu-id="c9ee1-125">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="c9ee1-125">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="c9ee1-126">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="c9ee1-126">Implementations</span></span>

-   [<span data-ttu-id="c9ee1-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c9ee1-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c9ee1-128">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="c9ee1-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="c9ee1-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c9ee1-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c9ee1-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c9ee1-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c9ee1-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c9ee1-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c9ee1-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c9ee1-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="c9ee1-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c9ee1-133">Windows Server 2003</span></span>



| <span data-ttu-id="c9ee1-134">Voce</span><span class="sxs-lookup"><span data-stu-id="c9ee1-134">Entry</span></span> | <span data-ttu-id="c9ee1-135">Valore</span><span class="sxs-lookup"><span data-stu-id="c9ee1-135">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="c9ee1-136">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="c9ee1-136">Link-Id</span></span>                | <span data-ttu-id="c9ee1-137">2036</span><span class="sxs-lookup"><span data-stu-id="c9ee1-137">2036</span></span>                                     |
| <span data-ttu-id="c9ee1-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c9ee1-138">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="c9ee1-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="c9ee1-139">System-Only</span></span>            | <span data-ttu-id="c9ee1-140">Vero</span><span class="sxs-lookup"><span data-stu-id="c9ee1-140">True</span></span>                                     |
| <span data-ttu-id="c9ee1-141">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="c9ee1-141">Is-Single-Valued</span></span>       | <span data-ttu-id="c9ee1-142">Falso</span><span class="sxs-lookup"><span data-stu-id="c9ee1-142">False</span></span>                                    |
| <span data-ttu-id="c9ee1-143">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="c9ee1-143">Is Indexed</span></span>             | <span data-ttu-id="c9ee1-144">Falso</span><span class="sxs-lookup"><span data-stu-id="c9ee1-144">False</span></span>                                    |
| <span data-ttu-id="c9ee1-145">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="c9ee1-145">In Global Catalog</span></span>      | <span data-ttu-id="c9ee1-146">Falso</span><span class="sxs-lookup"><span data-stu-id="c9ee1-146">False</span></span>                                    |
| <span data-ttu-id="c9ee1-147">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="c9ee1-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="c9ee1-148">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="c9ee1-148">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="c9ee1-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c9ee1-149">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="c9ee1-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c9ee1-150">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="c9ee1-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c9ee1-151">Search-Flags</span></span>           | <span data-ttu-id="c9ee1-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c9ee1-152">0x00000000</span></span>                               |
| <span data-ttu-id="c9ee1-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c9ee1-153">System-Flags</span></span>           | <span data-ttu-id="c9ee1-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c9ee1-154">0x00000010</span></span>                               |
| <span data-ttu-id="c9ee1-155">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="c9ee1-155">Classes used in</span></span>        | [<span data-ttu-id="c9ee1-156">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="c9ee1-156">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="adam"></a><span data-ttu-id="c9ee1-157">ADAM</span><span class="sxs-lookup"><span data-stu-id="c9ee1-157">ADAM</span></span>



| <span data-ttu-id="c9ee1-158">Voce</span><span class="sxs-lookup"><span data-stu-id="c9ee1-158">Entry</span></span> | <span data-ttu-id="c9ee1-159">Valore</span><span class="sxs-lookup"><span data-stu-id="c9ee1-159">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="c9ee1-160">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="c9ee1-160">Link-Id</span></span>                | <span data-ttu-id="c9ee1-161">2036</span><span class="sxs-lookup"><span data-stu-id="c9ee1-161">2036</span></span>                                     |
| <span data-ttu-id="c9ee1-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c9ee1-162">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="c9ee1-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="c9ee1-163">System-Only</span></span>            | <span data-ttu-id="c9ee1-164">Vero</span><span class="sxs-lookup"><span data-stu-id="c9ee1-164">True</span></span>                                     |
| <span data-ttu-id="c9ee1-165">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="c9ee1-165">Is-Single-Valued</span></span>       | <span data-ttu-id="c9ee1-166">Falso</span><span class="sxs-lookup"><span data-stu-id="c9ee1-166">False</span></span>                                    |
| <span data-ttu-id="c9ee1-167">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="c9ee1-167">Is Indexed</span></span>             | <span data-ttu-id="c9ee1-168">Falso</span><span class="sxs-lookup"><span data-stu-id="c9ee1-168">False</span></span>                                    |
| <span data-ttu-id="c9ee1-169">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="c9ee1-169">In Global Catalog</span></span>      | <span data-ttu-id="c9ee1-170">Falso</span><span class="sxs-lookup"><span data-stu-id="c9ee1-170">False</span></span>                                    |
| <span data-ttu-id="c9ee1-171">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="c9ee1-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="c9ee1-172">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="c9ee1-172">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="c9ee1-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c9ee1-173">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="c9ee1-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c9ee1-174">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="c9ee1-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c9ee1-175">Search-Flags</span></span>           | <span data-ttu-id="c9ee1-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c9ee1-176">0x00000000</span></span>                               |
| <span data-ttu-id="c9ee1-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c9ee1-177">System-Flags</span></span>           | <span data-ttu-id="c9ee1-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c9ee1-178">0x00000010</span></span>                               |
| <span data-ttu-id="c9ee1-179">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="c9ee1-179">Classes used in</span></span>        | [<span data-ttu-id="c9ee1-180">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="c9ee1-180">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c9ee1-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c9ee1-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c9ee1-182">Voce</span><span class="sxs-lookup"><span data-stu-id="c9ee1-182">Entry</span></span> | <span data-ttu-id="c9ee1-183">Valore</span><span class="sxs-lookup"><span data-stu-id="c9ee1-183">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="c9ee1-184">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="c9ee1-184">Link-Id</span></span>                | <span data-ttu-id="c9ee1-185">2036</span><span class="sxs-lookup"><span data-stu-id="c9ee1-185">2036</span></span>                                     |
| <span data-ttu-id="c9ee1-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c9ee1-186">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="c9ee1-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="c9ee1-187">System-Only</span></span>            | <span data-ttu-id="c9ee1-188">Vero</span><span class="sxs-lookup"><span data-stu-id="c9ee1-188">True</span></span>                                     |
| <span data-ttu-id="c9ee1-189">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="c9ee1-189">Is-Single-Valued</span></span>       | <span data-ttu-id="c9ee1-190">Falso</span><span class="sxs-lookup"><span data-stu-id="c9ee1-190">False</span></span>                                    |
| <span data-ttu-id="c9ee1-191">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="c9ee1-191">Is Indexed</span></span>             | <span data-ttu-id="c9ee1-192">Falso</span><span class="sxs-lookup"><span data-stu-id="c9ee1-192">False</span></span>                                    |
| <span data-ttu-id="c9ee1-193">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="c9ee1-193">In Global Catalog</span></span>      | <span data-ttu-id="c9ee1-194">Falso</span><span class="sxs-lookup"><span data-stu-id="c9ee1-194">False</span></span>                                    |
| <span data-ttu-id="c9ee1-195">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="c9ee1-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="c9ee1-196">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="c9ee1-196">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="c9ee1-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c9ee1-197">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="c9ee1-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c9ee1-198">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="c9ee1-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c9ee1-199">Search-Flags</span></span>           | <span data-ttu-id="c9ee1-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c9ee1-200">0x00000000</span></span>                               |
| <span data-ttu-id="c9ee1-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c9ee1-201">System-Flags</span></span>           | <span data-ttu-id="c9ee1-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c9ee1-202">0x00000010</span></span>                               |
| <span data-ttu-id="c9ee1-203">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="c9ee1-203">Classes used in</span></span>        | [<span data-ttu-id="c9ee1-204">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="c9ee1-204">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c9ee1-205">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c9ee1-205">Windows Server 2008</span></span>



| <span data-ttu-id="c9ee1-206">Voce</span><span class="sxs-lookup"><span data-stu-id="c9ee1-206">Entry</span></span> | <span data-ttu-id="c9ee1-207">Valore</span><span class="sxs-lookup"><span data-stu-id="c9ee1-207">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="c9ee1-208">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="c9ee1-208">Link-Id</span></span>                | <span data-ttu-id="c9ee1-209">2036</span><span class="sxs-lookup"><span data-stu-id="c9ee1-209">2036</span></span>                                     |
| <span data-ttu-id="c9ee1-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c9ee1-210">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="c9ee1-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="c9ee1-211">System-Only</span></span>            | <span data-ttu-id="c9ee1-212">Vero</span><span class="sxs-lookup"><span data-stu-id="c9ee1-212">True</span></span>                                     |
| <span data-ttu-id="c9ee1-213">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="c9ee1-213">Is-Single-Valued</span></span>       | <span data-ttu-id="c9ee1-214">Falso</span><span class="sxs-lookup"><span data-stu-id="c9ee1-214">False</span></span>                                    |
| <span data-ttu-id="c9ee1-215">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="c9ee1-215">Is Indexed</span></span>             | <span data-ttu-id="c9ee1-216">Falso</span><span class="sxs-lookup"><span data-stu-id="c9ee1-216">False</span></span>                                    |
| <span data-ttu-id="c9ee1-217">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="c9ee1-217">In Global Catalog</span></span>      | <span data-ttu-id="c9ee1-218">Falso</span><span class="sxs-lookup"><span data-stu-id="c9ee1-218">False</span></span>                                    |
| <span data-ttu-id="c9ee1-219">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="c9ee1-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="c9ee1-220">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="c9ee1-220">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="c9ee1-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c9ee1-221">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="c9ee1-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c9ee1-222">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="c9ee1-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c9ee1-223">Search-Flags</span></span>           | <span data-ttu-id="c9ee1-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c9ee1-224">0x00000000</span></span>                               |
| <span data-ttu-id="c9ee1-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c9ee1-225">System-Flags</span></span>           | <span data-ttu-id="c9ee1-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c9ee1-226">0x00000010</span></span>                               |
| <span data-ttu-id="c9ee1-227">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="c9ee1-227">Classes used in</span></span>        | [<span data-ttu-id="c9ee1-228">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="c9ee1-228">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c9ee1-229">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c9ee1-229">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c9ee1-230">Voce</span><span class="sxs-lookup"><span data-stu-id="c9ee1-230">Entry</span></span> | <span data-ttu-id="c9ee1-231">Valore</span><span class="sxs-lookup"><span data-stu-id="c9ee1-231">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="c9ee1-232">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="c9ee1-232">Link-Id</span></span>                | <span data-ttu-id="c9ee1-233">2036</span><span class="sxs-lookup"><span data-stu-id="c9ee1-233">2036</span></span>                                     |
| <span data-ttu-id="c9ee1-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c9ee1-234">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="c9ee1-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="c9ee1-235">System-Only</span></span>            | <span data-ttu-id="c9ee1-236">Vero</span><span class="sxs-lookup"><span data-stu-id="c9ee1-236">True</span></span>                                     |
| <span data-ttu-id="c9ee1-237">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="c9ee1-237">Is-Single-Valued</span></span>       | <span data-ttu-id="c9ee1-238">Falso</span><span class="sxs-lookup"><span data-stu-id="c9ee1-238">False</span></span>                                    |
| <span data-ttu-id="c9ee1-239">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="c9ee1-239">Is Indexed</span></span>             | <span data-ttu-id="c9ee1-240">Falso</span><span class="sxs-lookup"><span data-stu-id="c9ee1-240">False</span></span>                                    |
| <span data-ttu-id="c9ee1-241">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="c9ee1-241">In Global Catalog</span></span>      | <span data-ttu-id="c9ee1-242">Falso</span><span class="sxs-lookup"><span data-stu-id="c9ee1-242">False</span></span>                                    |
| <span data-ttu-id="c9ee1-243">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="c9ee1-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="c9ee1-244">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="c9ee1-244">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="c9ee1-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c9ee1-245">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="c9ee1-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c9ee1-246">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="c9ee1-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c9ee1-247">Search-Flags</span></span>           | <span data-ttu-id="c9ee1-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c9ee1-248">0x00000000</span></span>                               |
| <span data-ttu-id="c9ee1-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c9ee1-249">System-Flags</span></span>           | <span data-ttu-id="c9ee1-250">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c9ee1-250">0x00000010</span></span>                               |
| <span data-ttu-id="c9ee1-251">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="c9ee1-251">Classes used in</span></span>        | [<span data-ttu-id="c9ee1-252">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="c9ee1-252">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c9ee1-253">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c9ee1-253">Windows Server 2012</span></span>



| <span data-ttu-id="c9ee1-254">Voce</span><span class="sxs-lookup"><span data-stu-id="c9ee1-254">Entry</span></span> | <span data-ttu-id="c9ee1-255">Valore</span><span class="sxs-lookup"><span data-stu-id="c9ee1-255">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="c9ee1-256">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="c9ee1-256">Link-Id</span></span>                | <span data-ttu-id="c9ee1-257">2036</span><span class="sxs-lookup"><span data-stu-id="c9ee1-257">2036</span></span>                                     |
| <span data-ttu-id="c9ee1-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c9ee1-258">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="c9ee1-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="c9ee1-259">System-Only</span></span>            | <span data-ttu-id="c9ee1-260">Vero</span><span class="sxs-lookup"><span data-stu-id="c9ee1-260">True</span></span>                                     |
| <span data-ttu-id="c9ee1-261">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="c9ee1-261">Is-Single-Valued</span></span>       | <span data-ttu-id="c9ee1-262">Falso</span><span class="sxs-lookup"><span data-stu-id="c9ee1-262">False</span></span>                                    |
| <span data-ttu-id="c9ee1-263">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="c9ee1-263">Is Indexed</span></span>             | <span data-ttu-id="c9ee1-264">Falso</span><span class="sxs-lookup"><span data-stu-id="c9ee1-264">False</span></span>                                    |
| <span data-ttu-id="c9ee1-265">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="c9ee1-265">In Global Catalog</span></span>      | <span data-ttu-id="c9ee1-266">Falso</span><span class="sxs-lookup"><span data-stu-id="c9ee1-266">False</span></span>                                    |
| <span data-ttu-id="c9ee1-267">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="c9ee1-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="c9ee1-268">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="c9ee1-268">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="c9ee1-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c9ee1-269">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="c9ee1-270">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c9ee1-270">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="c9ee1-271">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c9ee1-271">Search-Flags</span></span>           | <span data-ttu-id="c9ee1-272">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c9ee1-272">0x00000000</span></span>                               |
| <span data-ttu-id="c9ee1-273">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c9ee1-273">System-Flags</span></span>           | <span data-ttu-id="c9ee1-274">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c9ee1-274">0x00000010</span></span>                               |
| <span data-ttu-id="c9ee1-275">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="c9ee1-275">Classes used in</span></span>        | [<span data-ttu-id="c9ee1-276">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="c9ee1-276">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



 

 





