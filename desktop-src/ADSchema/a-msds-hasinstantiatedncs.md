---
title: attributi ms-DS-has-instantied-NCs
description: Informazioni sullo stato di replica di DS, analoghe a (e un superset di) degli attributi hasMasterNCs e hasPartialReplicaNCs esistenti. Utilizzato da KCC durante la configurazione dei partner di replica.
ms.assetid: 00dda441-e382-4fb2-b735-ae547901c11f
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo di MS-DS-has-instantid-NCs
- attributo msDS-HasInstantiatedNCs-schema AD
topic_type:
- apiref
api_name:
- ms-DS-Has-Instantiated-NCs
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2900d68f82e859bac7ce1dabbfea2d28fd8998b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104480096"
---
# <a name="ms-ds-has-instantiated-ncs-attribute"></a><span data-ttu-id="71997-106">attributi ms-DS-has-instantied-NCs</span><span class="sxs-lookup"><span data-stu-id="71997-106">ms-DS-Has-Instantiated-NCs attribute</span></span>

<span data-ttu-id="71997-107">Informazioni sullo stato di replica di DS, analoghe a (e un superset di) degli attributi hasMasterNCs e hasPartialReplicaNCs esistenti.</span><span class="sxs-lookup"><span data-stu-id="71997-107">DS replication state information, analogous to (and a superset of) the existing attributes hasMasterNCs and hasPartialReplicaNCs.</span></span> <span data-ttu-id="71997-108">Utilizzato da KCC durante la configurazione dei partner di replica.</span><span class="sxs-lookup"><span data-stu-id="71997-108">To be used by the KCC when setting up replication partners.</span></span>



| <span data-ttu-id="71997-109">Voce</span><span class="sxs-lookup"><span data-stu-id="71997-109">Entry</span></span> | <span data-ttu-id="71997-110">Valore</span><span class="sxs-lookup"><span data-stu-id="71997-110">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71997-111">CN</span><span class="sxs-lookup"><span data-stu-id="71997-111">CN</span></span>                | <span data-ttu-id="71997-112">ms-DS-ha-creata un'istanza-NCs</span><span class="sxs-lookup"><span data-stu-id="71997-112">ms-DS-Has-Instantiated-NCs</span></span>                                                                                                                                                                                  |
| <span data-ttu-id="71997-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="71997-113">Ldap-Display-Name</span></span> | <span data-ttu-id="71997-114">msDS-HasInstantiatedNCs</span><span class="sxs-lookup"><span data-stu-id="71997-114">msDS-HasInstantiatedNCs</span></span>                                                                                                                                                                                     |
| <span data-ttu-id="71997-115">Dimensione</span><span class="sxs-lookup"><span data-stu-id="71997-115">Size</span></span>              | <span data-ttu-id="71997-116">4 byte</span><span class="sxs-lookup"><span data-stu-id="71997-116">4 bytes</span></span>                                                                                                                                                                                                     |
| <span data-ttu-id="71997-117">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="71997-117">Update Privilege</span></span>  | <span data-ttu-id="71997-118">Questo valore viene impostato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="71997-118">This value is set by the system.</span></span>                                                                                                                                                                            |
| <span data-ttu-id="71997-119">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="71997-119">Update Frequency</span></span>  | <span data-ttu-id="71997-120">Circa due volte più spesso di hasMasterNCs/hasPartialReplicaNCs.</span><span class="sxs-lookup"><span data-stu-id="71997-120">Roughly twice as often as hasMasterNCs / hasPartialReplicaNCs.</span></span> <span data-ttu-id="71997-121">Questi attributi esistenti vengono aggiornati solo quando il controller di dominio aggiunge o rimuove una partizione, ad esempio in caso di passaggio da un controller di dominio a un GC o viceversa.</span><span class="sxs-lookup"><span data-stu-id="71997-121">These existing attributes are updated only when the DC adds or removes a partition (For example, when changing from DC to GC or vice versa).</span></span> |
| <span data-ttu-id="71997-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="71997-122">Attribute-Id</span></span>      | <span data-ttu-id="71997-123">1.2.840.113556.1.4.1709</span><span class="sxs-lookup"><span data-stu-id="71997-123">1.2.840.113556.1.4.1709</span></span>                                                                                                                                                                                     |
| <span data-ttu-id="71997-124">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="71997-124">System-Id-Guid</span></span>    | <span data-ttu-id="71997-125">11e9a5bc-4517-4049-af9c-51554fb0fc09</span><span class="sxs-lookup"><span data-stu-id="71997-125">11e9a5bc-4517-4049-af9c-51554fb0fc09</span></span>                                                                                                                                                                        |
| <span data-ttu-id="71997-126">Sintassi</span><span class="sxs-lookup"><span data-stu-id="71997-126">Syntax</span></span>            | [<span data-ttu-id="71997-127">**Object(DN-Binary)**</span><span class="sxs-lookup"><span data-stu-id="71997-127">**Object(DN-Binary)**</span></span>](s-object-dn-binary.md)                                                                                                                                                             |



## <a name="implementations"></a><span data-ttu-id="71997-128">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="71997-128">Implementations</span></span>

-   [<span data-ttu-id="71997-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="71997-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="71997-130">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="71997-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="71997-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="71997-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="71997-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="71997-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="71997-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="71997-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="71997-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="71997-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="71997-135">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="71997-135">Windows Server 2003</span></span>



| <span data-ttu-id="71997-136">Voce</span><span class="sxs-lookup"><span data-stu-id="71997-136">Entry</span></span> | <span data-ttu-id="71997-137">Valore</span><span class="sxs-lookup"><span data-stu-id="71997-137">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="71997-138">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="71997-138">Link-Id</span></span>                | <span data-ttu-id="71997-139">2002</span><span class="sxs-lookup"><span data-stu-id="71997-139">2002</span></span>                                     |
| <span data-ttu-id="71997-140">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="71997-140">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="71997-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="71997-141">System-Only</span></span>            | <span data-ttu-id="71997-142">Vero</span><span class="sxs-lookup"><span data-stu-id="71997-142">True</span></span>                                     |
| <span data-ttu-id="71997-143">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="71997-143">Is-Single-Valued</span></span>       | <span data-ttu-id="71997-144">Falso</span><span class="sxs-lookup"><span data-stu-id="71997-144">False</span></span>                                    |
| <span data-ttu-id="71997-145">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="71997-145">Is Indexed</span></span>             | <span data-ttu-id="71997-146">Falso</span><span class="sxs-lookup"><span data-stu-id="71997-146">False</span></span>                                    |
| <span data-ttu-id="71997-147">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="71997-147">In Global Catalog</span></span>      | <span data-ttu-id="71997-148">Falso</span><span class="sxs-lookup"><span data-stu-id="71997-148">False</span></span>                                    |
| <span data-ttu-id="71997-149">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="71997-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="71997-150">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="71997-150">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="71997-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="71997-151">Range-Lower</span></span>            | <span data-ttu-id="71997-152">4</span><span class="sxs-lookup"><span data-stu-id="71997-152">4</span></span>                                        |
| <span data-ttu-id="71997-153">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="71997-153">Range-Upper</span></span>            | <span data-ttu-id="71997-154">4</span><span class="sxs-lookup"><span data-stu-id="71997-154">4</span></span>                                        |
| <span data-ttu-id="71997-155">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="71997-155">Search-Flags</span></span>           | <span data-ttu-id="71997-156">0x00000000</span><span class="sxs-lookup"><span data-stu-id="71997-156">0x00000000</span></span>                               |
| <span data-ttu-id="71997-157">System-Flags</span><span class="sxs-lookup"><span data-stu-id="71997-157">System-Flags</span></span>           | <span data-ttu-id="71997-158">0x00000010</span><span class="sxs-lookup"><span data-stu-id="71997-158">0x00000010</span></span>                               |
| <span data-ttu-id="71997-159">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="71997-159">Classes used in</span></span>        | [<span data-ttu-id="71997-160">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="71997-160">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="adam"></a><span data-ttu-id="71997-161">ADAM</span><span class="sxs-lookup"><span data-stu-id="71997-161">ADAM</span></span>



| <span data-ttu-id="71997-162">Voce</span><span class="sxs-lookup"><span data-stu-id="71997-162">Entry</span></span> | <span data-ttu-id="71997-163">Valore</span><span class="sxs-lookup"><span data-stu-id="71997-163">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="71997-164">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="71997-164">Link-Id</span></span>                | <span data-ttu-id="71997-165">2002</span><span class="sxs-lookup"><span data-stu-id="71997-165">2002</span></span>                                     |
| <span data-ttu-id="71997-166">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="71997-166">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="71997-167">System-Only</span><span class="sxs-lookup"><span data-stu-id="71997-167">System-Only</span></span>            | <span data-ttu-id="71997-168">Vero</span><span class="sxs-lookup"><span data-stu-id="71997-168">True</span></span>                                     |
| <span data-ttu-id="71997-169">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="71997-169">Is-Single-Valued</span></span>       | <span data-ttu-id="71997-170">Falso</span><span class="sxs-lookup"><span data-stu-id="71997-170">False</span></span>                                    |
| <span data-ttu-id="71997-171">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="71997-171">Is Indexed</span></span>             | <span data-ttu-id="71997-172">Falso</span><span class="sxs-lookup"><span data-stu-id="71997-172">False</span></span>                                    |
| <span data-ttu-id="71997-173">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="71997-173">In Global Catalog</span></span>      | <span data-ttu-id="71997-174">Falso</span><span class="sxs-lookup"><span data-stu-id="71997-174">False</span></span>                                    |
| <span data-ttu-id="71997-175">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="71997-175">NT-Security-Descriptor</span></span> | <span data-ttu-id="71997-176">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="71997-176">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="71997-177">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="71997-177">Range-Lower</span></span>            | <span data-ttu-id="71997-178">4</span><span class="sxs-lookup"><span data-stu-id="71997-178">4</span></span>                                        |
| <span data-ttu-id="71997-179">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="71997-179">Range-Upper</span></span>            | <span data-ttu-id="71997-180">4</span><span class="sxs-lookup"><span data-stu-id="71997-180">4</span></span>                                        |
| <span data-ttu-id="71997-181">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="71997-181">Search-Flags</span></span>           | <span data-ttu-id="71997-182">0x00000000</span><span class="sxs-lookup"><span data-stu-id="71997-182">0x00000000</span></span>                               |
| <span data-ttu-id="71997-183">System-Flags</span><span class="sxs-lookup"><span data-stu-id="71997-183">System-Flags</span></span>           | <span data-ttu-id="71997-184">0x00000010</span><span class="sxs-lookup"><span data-stu-id="71997-184">0x00000010</span></span>                               |
| <span data-ttu-id="71997-185">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="71997-185">Classes used in</span></span>        | [<span data-ttu-id="71997-186">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="71997-186">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="71997-187">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="71997-187">Windows Server 2003 R2</span></span>



| <span data-ttu-id="71997-188">Voce</span><span class="sxs-lookup"><span data-stu-id="71997-188">Entry</span></span> | <span data-ttu-id="71997-189">Valore</span><span class="sxs-lookup"><span data-stu-id="71997-189">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="71997-190">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="71997-190">Link-Id</span></span>                | <span data-ttu-id="71997-191">2002</span><span class="sxs-lookup"><span data-stu-id="71997-191">2002</span></span>                                     |
| <span data-ttu-id="71997-192">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="71997-192">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="71997-193">System-Only</span><span class="sxs-lookup"><span data-stu-id="71997-193">System-Only</span></span>            | <span data-ttu-id="71997-194">Vero</span><span class="sxs-lookup"><span data-stu-id="71997-194">True</span></span>                                     |
| <span data-ttu-id="71997-195">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="71997-195">Is-Single-Valued</span></span>       | <span data-ttu-id="71997-196">Falso</span><span class="sxs-lookup"><span data-stu-id="71997-196">False</span></span>                                    |
| <span data-ttu-id="71997-197">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="71997-197">Is Indexed</span></span>             | <span data-ttu-id="71997-198">Falso</span><span class="sxs-lookup"><span data-stu-id="71997-198">False</span></span>                                    |
| <span data-ttu-id="71997-199">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="71997-199">In Global Catalog</span></span>      | <span data-ttu-id="71997-200">Falso</span><span class="sxs-lookup"><span data-stu-id="71997-200">False</span></span>                                    |
| <span data-ttu-id="71997-201">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="71997-201">NT-Security-Descriptor</span></span> | <span data-ttu-id="71997-202">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="71997-202">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="71997-203">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="71997-203">Range-Lower</span></span>            | <span data-ttu-id="71997-204">4</span><span class="sxs-lookup"><span data-stu-id="71997-204">4</span></span>                                        |
| <span data-ttu-id="71997-205">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="71997-205">Range-Upper</span></span>            | <span data-ttu-id="71997-206">4</span><span class="sxs-lookup"><span data-stu-id="71997-206">4</span></span>                                        |
| <span data-ttu-id="71997-207">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="71997-207">Search-Flags</span></span>           | <span data-ttu-id="71997-208">0x00000000</span><span class="sxs-lookup"><span data-stu-id="71997-208">0x00000000</span></span>                               |
| <span data-ttu-id="71997-209">System-Flags</span><span class="sxs-lookup"><span data-stu-id="71997-209">System-Flags</span></span>           | <span data-ttu-id="71997-210">0x00000010</span><span class="sxs-lookup"><span data-stu-id="71997-210">0x00000010</span></span>                               |
| <span data-ttu-id="71997-211">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="71997-211">Classes used in</span></span>        | [<span data-ttu-id="71997-212">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="71997-212">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="71997-213">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="71997-213">Windows Server 2008</span></span>



| <span data-ttu-id="71997-214">Voce</span><span class="sxs-lookup"><span data-stu-id="71997-214">Entry</span></span> | <span data-ttu-id="71997-215">Valore</span><span class="sxs-lookup"><span data-stu-id="71997-215">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="71997-216">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="71997-216">Link-Id</span></span>                | <span data-ttu-id="71997-217">2002</span><span class="sxs-lookup"><span data-stu-id="71997-217">2002</span></span>                                     |
| <span data-ttu-id="71997-218">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="71997-218">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="71997-219">System-Only</span><span class="sxs-lookup"><span data-stu-id="71997-219">System-Only</span></span>            | <span data-ttu-id="71997-220">Vero</span><span class="sxs-lookup"><span data-stu-id="71997-220">True</span></span>                                     |
| <span data-ttu-id="71997-221">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="71997-221">Is-Single-Valued</span></span>       | <span data-ttu-id="71997-222">Falso</span><span class="sxs-lookup"><span data-stu-id="71997-222">False</span></span>                                    |
| <span data-ttu-id="71997-223">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="71997-223">Is Indexed</span></span>             | <span data-ttu-id="71997-224">Falso</span><span class="sxs-lookup"><span data-stu-id="71997-224">False</span></span>                                    |
| <span data-ttu-id="71997-225">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="71997-225">In Global Catalog</span></span>      | <span data-ttu-id="71997-226">Falso</span><span class="sxs-lookup"><span data-stu-id="71997-226">False</span></span>                                    |
| <span data-ttu-id="71997-227">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="71997-227">NT-Security-Descriptor</span></span> | <span data-ttu-id="71997-228">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="71997-228">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="71997-229">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="71997-229">Range-Lower</span></span>            | <span data-ttu-id="71997-230">4</span><span class="sxs-lookup"><span data-stu-id="71997-230">4</span></span>                                        |
| <span data-ttu-id="71997-231">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="71997-231">Range-Upper</span></span>            | <span data-ttu-id="71997-232">4</span><span class="sxs-lookup"><span data-stu-id="71997-232">4</span></span>                                        |
| <span data-ttu-id="71997-233">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="71997-233">Search-Flags</span></span>           | <span data-ttu-id="71997-234">0x00000000</span><span class="sxs-lookup"><span data-stu-id="71997-234">0x00000000</span></span>                               |
| <span data-ttu-id="71997-235">System-Flags</span><span class="sxs-lookup"><span data-stu-id="71997-235">System-Flags</span></span>           | <span data-ttu-id="71997-236">0x00000010</span><span class="sxs-lookup"><span data-stu-id="71997-236">0x00000010</span></span>                               |
| <span data-ttu-id="71997-237">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="71997-237">Classes used in</span></span>        | [<span data-ttu-id="71997-238">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="71997-238">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="71997-239">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="71997-239">Windows Server 2008 R2</span></span>



| <span data-ttu-id="71997-240">Voce</span><span class="sxs-lookup"><span data-stu-id="71997-240">Entry</span></span> | <span data-ttu-id="71997-241">Valore</span><span class="sxs-lookup"><span data-stu-id="71997-241">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="71997-242">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="71997-242">Link-Id</span></span>                | <span data-ttu-id="71997-243">2002</span><span class="sxs-lookup"><span data-stu-id="71997-243">2002</span></span>                                     |
| <span data-ttu-id="71997-244">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="71997-244">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="71997-245">System-Only</span><span class="sxs-lookup"><span data-stu-id="71997-245">System-Only</span></span>            | <span data-ttu-id="71997-246">Vero</span><span class="sxs-lookup"><span data-stu-id="71997-246">True</span></span>                                     |
| <span data-ttu-id="71997-247">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="71997-247">Is-Single-Valued</span></span>       | <span data-ttu-id="71997-248">Falso</span><span class="sxs-lookup"><span data-stu-id="71997-248">False</span></span>                                    |
| <span data-ttu-id="71997-249">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="71997-249">Is Indexed</span></span>             | <span data-ttu-id="71997-250">Falso</span><span class="sxs-lookup"><span data-stu-id="71997-250">False</span></span>                                    |
| <span data-ttu-id="71997-251">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="71997-251">In Global Catalog</span></span>      | <span data-ttu-id="71997-252">Falso</span><span class="sxs-lookup"><span data-stu-id="71997-252">False</span></span>                                    |
| <span data-ttu-id="71997-253">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="71997-253">NT-Security-Descriptor</span></span> | <span data-ttu-id="71997-254">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="71997-254">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="71997-255">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="71997-255">Range-Lower</span></span>            | <span data-ttu-id="71997-256">4</span><span class="sxs-lookup"><span data-stu-id="71997-256">4</span></span>                                        |
| <span data-ttu-id="71997-257">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="71997-257">Range-Upper</span></span>            | <span data-ttu-id="71997-258">4</span><span class="sxs-lookup"><span data-stu-id="71997-258">4</span></span>                                        |
| <span data-ttu-id="71997-259">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="71997-259">Search-Flags</span></span>           | <span data-ttu-id="71997-260">0x00000000</span><span class="sxs-lookup"><span data-stu-id="71997-260">0x00000000</span></span>                               |
| <span data-ttu-id="71997-261">System-Flags</span><span class="sxs-lookup"><span data-stu-id="71997-261">System-Flags</span></span>           | <span data-ttu-id="71997-262">0x00000010</span><span class="sxs-lookup"><span data-stu-id="71997-262">0x00000010</span></span>                               |
| <span data-ttu-id="71997-263">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="71997-263">Classes used in</span></span>        | [<span data-ttu-id="71997-264">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="71997-264">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="71997-265">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="71997-265">Windows Server 2012</span></span>



| <span data-ttu-id="71997-266">Voce</span><span class="sxs-lookup"><span data-stu-id="71997-266">Entry</span></span> | <span data-ttu-id="71997-267">Valore</span><span class="sxs-lookup"><span data-stu-id="71997-267">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="71997-268">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="71997-268">Link-Id</span></span>                | <span data-ttu-id="71997-269">2002</span><span class="sxs-lookup"><span data-stu-id="71997-269">2002</span></span>                                     |
| <span data-ttu-id="71997-270">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="71997-270">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="71997-271">System-Only</span><span class="sxs-lookup"><span data-stu-id="71997-271">System-Only</span></span>            | <span data-ttu-id="71997-272">Vero</span><span class="sxs-lookup"><span data-stu-id="71997-272">True</span></span>                                     |
| <span data-ttu-id="71997-273">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="71997-273">Is-Single-Valued</span></span>       | <span data-ttu-id="71997-274">Falso</span><span class="sxs-lookup"><span data-stu-id="71997-274">False</span></span>                                    |
| <span data-ttu-id="71997-275">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="71997-275">Is Indexed</span></span>             | <span data-ttu-id="71997-276">Falso</span><span class="sxs-lookup"><span data-stu-id="71997-276">False</span></span>                                    |
| <span data-ttu-id="71997-277">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="71997-277">In Global Catalog</span></span>      | <span data-ttu-id="71997-278">Falso</span><span class="sxs-lookup"><span data-stu-id="71997-278">False</span></span>                                    |
| <span data-ttu-id="71997-279">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="71997-279">NT-Security-Descriptor</span></span> | <span data-ttu-id="71997-280">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="71997-280">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="71997-281">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="71997-281">Range-Lower</span></span>            | <span data-ttu-id="71997-282">4</span><span class="sxs-lookup"><span data-stu-id="71997-282">4</span></span>                                        |
| <span data-ttu-id="71997-283">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="71997-283">Range-Upper</span></span>            | <span data-ttu-id="71997-284">4</span><span class="sxs-lookup"><span data-stu-id="71997-284">4</span></span>                                        |
| <span data-ttu-id="71997-285">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="71997-285">Search-Flags</span></span>           | <span data-ttu-id="71997-286">0x00000000</span><span class="sxs-lookup"><span data-stu-id="71997-286">0x00000000</span></span>                               |
| <span data-ttu-id="71997-287">System-Flags</span><span class="sxs-lookup"><span data-stu-id="71997-287">System-Flags</span></span>           | <span data-ttu-id="71997-288">0x00000010</span><span class="sxs-lookup"><span data-stu-id="71997-288">0x00000010</span></span>                               |
| <span data-ttu-id="71997-289">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="71997-289">Classes used in</span></span>        | [<span data-ttu-id="71997-290">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="71997-290">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



 

 





