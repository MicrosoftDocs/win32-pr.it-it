---
title: attributo ms-DS-ReplicationEpoch
description: Viene usato per mantenere il periodo in cui vengono replicati tutti i controller di dominio. Epoch è il periodo di tempo in cui un dominio ha un nome specifico. Una nuova Epoch viene avviata quando si verifica una modifica del nome di dominio.
ms.assetid: d8a3c4fd-f416-483f-820f-7b3182d0bfc3
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo ms-DS-ReplicationEpoch
- attributo msDS-ReplicationEpoch-schema AD
topic_type:
- apiref
api_name:
- ms-DS-ReplicationEpoch
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef9aaefefe5cd1ae269508390ae13f67037fdb8a
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104519806"
---
# <a name="ms-ds-replicationepoch-attribute"></a><span data-ttu-id="f29fd-107">attributo ms-DS-ReplicationEpoch</span><span class="sxs-lookup"><span data-stu-id="f29fd-107">ms-DS-ReplicationEpoch attribute</span></span>

<span data-ttu-id="f29fd-108">Viene usato per mantenere il periodo in cui vengono replicati tutti i controller di dominio.</span><span class="sxs-lookup"><span data-stu-id="f29fd-108">This is used to hold the epoch under which all the DCs are replicating.</span></span> <span data-ttu-id="f29fd-109">Epoch è il periodo di tempo in cui un dominio ha un nome specifico.</span><span class="sxs-lookup"><span data-stu-id="f29fd-109">An epoch is the period of time in which a domain has a specific name.</span></span> <span data-ttu-id="f29fd-110">Una nuova Epoch viene avviata quando si verifica una modifica del nome di dominio.</span><span class="sxs-lookup"><span data-stu-id="f29fd-110">A new epoch starts when a domain name change occurs.</span></span>



| <span data-ttu-id="f29fd-111">Voce</span><span class="sxs-lookup"><span data-stu-id="f29fd-111">Entry</span></span> | <span data-ttu-id="f29fd-112">Valore</span><span class="sxs-lookup"><span data-stu-id="f29fd-112">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="f29fd-113">CN</span><span class="sxs-lookup"><span data-stu-id="f29fd-113">CN</span></span>                | <span data-ttu-id="f29fd-114">ms-DS-ReplicationEpoch</span><span class="sxs-lookup"><span data-stu-id="f29fd-114">ms-DS-ReplicationEpoch</span></span>               |
| <span data-ttu-id="f29fd-115">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="f29fd-115">Ldap-Display-Name</span></span> | <span data-ttu-id="f29fd-116">msDS-ReplicationEpoch</span><span class="sxs-lookup"><span data-stu-id="f29fd-116">msDS-ReplicationEpoch</span></span>                |
| <span data-ttu-id="f29fd-117">Dimensione</span><span class="sxs-lookup"><span data-stu-id="f29fd-117">Size</span></span>              | \-                                   |
| <span data-ttu-id="f29fd-118">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="f29fd-118">Update Privilege</span></span>  | <span data-ttu-id="f29fd-119">Questo valore viene impostato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="f29fd-119">This value is set by the system.</span></span>     |
| <span data-ttu-id="f29fd-120">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="f29fd-120">Update Frequency</span></span>  | <span data-ttu-id="f29fd-121">Solo durante la ristrutturazione del dominio.</span><span class="sxs-lookup"><span data-stu-id="f29fd-121">Only during domain restructure.</span></span>      |
| <span data-ttu-id="f29fd-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f29fd-122">Attribute-Id</span></span>      | <span data-ttu-id="f29fd-123">1.2.840.113556.1.4.1720</span><span class="sxs-lookup"><span data-stu-id="f29fd-123">1.2.840.113556.1.4.1720</span></span>              |
| <span data-ttu-id="f29fd-124">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="f29fd-124">System-Id-Guid</span></span>    | <span data-ttu-id="f29fd-125">08e3aa79-eb1c-45b5-af7b-8f94246c8e41</span><span class="sxs-lookup"><span data-stu-id="f29fd-125">08e3aa79-eb1c-45b5-af7b-8f94246c8e41</span></span> |
| <span data-ttu-id="f29fd-126">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f29fd-126">Syntax</span></span>            | [<span data-ttu-id="f29fd-127">**Enumerazione**</span><span class="sxs-lookup"><span data-stu-id="f29fd-127">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="f29fd-128">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="f29fd-128">Implementations</span></span>

-   [<span data-ttu-id="f29fd-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f29fd-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f29fd-130">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="f29fd-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="f29fd-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f29fd-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f29fd-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f29fd-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f29fd-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f29fd-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f29fd-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f29fd-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="f29fd-135">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f29fd-135">Windows Server 2003</span></span>



| <span data-ttu-id="f29fd-136">Voce</span><span class="sxs-lookup"><span data-stu-id="f29fd-136">Entry</span></span> | <span data-ttu-id="f29fd-137">Valore</span><span class="sxs-lookup"><span data-stu-id="f29fd-137">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="f29fd-138">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="f29fd-138">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="f29fd-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f29fd-139">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="f29fd-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="f29fd-140">System-Only</span></span>            | <span data-ttu-id="f29fd-141">Falso</span><span class="sxs-lookup"><span data-stu-id="f29fd-141">False</span></span>                                    |
| <span data-ttu-id="f29fd-142">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="f29fd-142">Is-Single-Valued</span></span>       | <span data-ttu-id="f29fd-143">Vero</span><span class="sxs-lookup"><span data-stu-id="f29fd-143">True</span></span>                                     |
| <span data-ttu-id="f29fd-144">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="f29fd-144">Is Indexed</span></span>             | <span data-ttu-id="f29fd-145">Falso</span><span class="sxs-lookup"><span data-stu-id="f29fd-145">False</span></span>                                    |
| <span data-ttu-id="f29fd-146">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="f29fd-146">In Global Catalog</span></span>      | <span data-ttu-id="f29fd-147">Falso</span><span class="sxs-lookup"><span data-stu-id="f29fd-147">False</span></span>                                    |
| <span data-ttu-id="f29fd-148">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="f29fd-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="f29fd-149">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="f29fd-149">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="f29fd-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f29fd-150">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="f29fd-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f29fd-151">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="f29fd-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f29fd-152">Search-Flags</span></span>           | <span data-ttu-id="f29fd-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f29fd-153">0x00000000</span></span>                               |
| <span data-ttu-id="f29fd-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f29fd-154">System-Flags</span></span>           | <span data-ttu-id="f29fd-155">0x00000011</span><span class="sxs-lookup"><span data-stu-id="f29fd-155">0x00000011</span></span>                               |
| <span data-ttu-id="f29fd-156">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="f29fd-156">Classes used in</span></span>        | [<span data-ttu-id="f29fd-157">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="f29fd-157">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="adam"></a><span data-ttu-id="f29fd-158">ADAM</span><span class="sxs-lookup"><span data-stu-id="f29fd-158">ADAM</span></span>



| <span data-ttu-id="f29fd-159">Voce</span><span class="sxs-lookup"><span data-stu-id="f29fd-159">Entry</span></span> | <span data-ttu-id="f29fd-160">Valore</span><span class="sxs-lookup"><span data-stu-id="f29fd-160">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="f29fd-161">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="f29fd-161">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="f29fd-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f29fd-162">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="f29fd-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="f29fd-163">System-Only</span></span>            | <span data-ttu-id="f29fd-164">Falso</span><span class="sxs-lookup"><span data-stu-id="f29fd-164">False</span></span>                                    |
| <span data-ttu-id="f29fd-165">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="f29fd-165">Is-Single-Valued</span></span>       | <span data-ttu-id="f29fd-166">Vero</span><span class="sxs-lookup"><span data-stu-id="f29fd-166">True</span></span>                                     |
| <span data-ttu-id="f29fd-167">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="f29fd-167">Is Indexed</span></span>             | <span data-ttu-id="f29fd-168">Falso</span><span class="sxs-lookup"><span data-stu-id="f29fd-168">False</span></span>                                    |
| <span data-ttu-id="f29fd-169">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="f29fd-169">In Global Catalog</span></span>      | <span data-ttu-id="f29fd-170">Falso</span><span class="sxs-lookup"><span data-stu-id="f29fd-170">False</span></span>                                    |
| <span data-ttu-id="f29fd-171">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="f29fd-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="f29fd-172">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="f29fd-172">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="f29fd-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f29fd-173">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="f29fd-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f29fd-174">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="f29fd-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f29fd-175">Search-Flags</span></span>           | <span data-ttu-id="f29fd-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f29fd-176">0x00000000</span></span>                               |
| <span data-ttu-id="f29fd-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f29fd-177">System-Flags</span></span>           | <span data-ttu-id="f29fd-178">0x00000011</span><span class="sxs-lookup"><span data-stu-id="f29fd-178">0x00000011</span></span>                               |
| <span data-ttu-id="f29fd-179">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="f29fd-179">Classes used in</span></span>        | [<span data-ttu-id="f29fd-180">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="f29fd-180">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f29fd-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f29fd-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f29fd-182">Voce</span><span class="sxs-lookup"><span data-stu-id="f29fd-182">Entry</span></span> | <span data-ttu-id="f29fd-183">Valore</span><span class="sxs-lookup"><span data-stu-id="f29fd-183">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="f29fd-184">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="f29fd-184">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="f29fd-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f29fd-185">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="f29fd-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="f29fd-186">System-Only</span></span>            | <span data-ttu-id="f29fd-187">Falso</span><span class="sxs-lookup"><span data-stu-id="f29fd-187">False</span></span>                                    |
| <span data-ttu-id="f29fd-188">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="f29fd-188">Is-Single-Valued</span></span>       | <span data-ttu-id="f29fd-189">Vero</span><span class="sxs-lookup"><span data-stu-id="f29fd-189">True</span></span>                                     |
| <span data-ttu-id="f29fd-190">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="f29fd-190">Is Indexed</span></span>             | <span data-ttu-id="f29fd-191">Falso</span><span class="sxs-lookup"><span data-stu-id="f29fd-191">False</span></span>                                    |
| <span data-ttu-id="f29fd-192">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="f29fd-192">In Global Catalog</span></span>      | <span data-ttu-id="f29fd-193">Falso</span><span class="sxs-lookup"><span data-stu-id="f29fd-193">False</span></span>                                    |
| <span data-ttu-id="f29fd-194">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="f29fd-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="f29fd-195">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="f29fd-195">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="f29fd-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f29fd-196">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="f29fd-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f29fd-197">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="f29fd-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f29fd-198">Search-Flags</span></span>           | <span data-ttu-id="f29fd-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f29fd-199">0x00000000</span></span>                               |
| <span data-ttu-id="f29fd-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f29fd-200">System-Flags</span></span>           | <span data-ttu-id="f29fd-201">0x00000011</span><span class="sxs-lookup"><span data-stu-id="f29fd-201">0x00000011</span></span>                               |
| <span data-ttu-id="f29fd-202">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="f29fd-202">Classes used in</span></span>        | [<span data-ttu-id="f29fd-203">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="f29fd-203">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f29fd-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f29fd-204">Windows Server 2008</span></span>



| <span data-ttu-id="f29fd-205">Voce</span><span class="sxs-lookup"><span data-stu-id="f29fd-205">Entry</span></span> | <span data-ttu-id="f29fd-206">Valore</span><span class="sxs-lookup"><span data-stu-id="f29fd-206">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="f29fd-207">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="f29fd-207">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="f29fd-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f29fd-208">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="f29fd-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="f29fd-209">System-Only</span></span>            | <span data-ttu-id="f29fd-210">Falso</span><span class="sxs-lookup"><span data-stu-id="f29fd-210">False</span></span>                                    |
| <span data-ttu-id="f29fd-211">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="f29fd-211">Is-Single-Valued</span></span>       | <span data-ttu-id="f29fd-212">Vero</span><span class="sxs-lookup"><span data-stu-id="f29fd-212">True</span></span>                                     |
| <span data-ttu-id="f29fd-213">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="f29fd-213">Is Indexed</span></span>             | <span data-ttu-id="f29fd-214">Falso</span><span class="sxs-lookup"><span data-stu-id="f29fd-214">False</span></span>                                    |
| <span data-ttu-id="f29fd-215">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="f29fd-215">In Global Catalog</span></span>      | <span data-ttu-id="f29fd-216">Falso</span><span class="sxs-lookup"><span data-stu-id="f29fd-216">False</span></span>                                    |
| <span data-ttu-id="f29fd-217">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="f29fd-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="f29fd-218">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="f29fd-218">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="f29fd-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f29fd-219">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="f29fd-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f29fd-220">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="f29fd-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f29fd-221">Search-Flags</span></span>           | <span data-ttu-id="f29fd-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f29fd-222">0x00000000</span></span>                               |
| <span data-ttu-id="f29fd-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f29fd-223">System-Flags</span></span>           | <span data-ttu-id="f29fd-224">0x00000011</span><span class="sxs-lookup"><span data-stu-id="f29fd-224">0x00000011</span></span>                               |
| <span data-ttu-id="f29fd-225">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="f29fd-225">Classes used in</span></span>        | [<span data-ttu-id="f29fd-226">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="f29fd-226">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f29fd-227">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f29fd-227">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f29fd-228">Voce</span><span class="sxs-lookup"><span data-stu-id="f29fd-228">Entry</span></span> | <span data-ttu-id="f29fd-229">Valore</span><span class="sxs-lookup"><span data-stu-id="f29fd-229">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="f29fd-230">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="f29fd-230">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="f29fd-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f29fd-231">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="f29fd-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="f29fd-232">System-Only</span></span>            | <span data-ttu-id="f29fd-233">Falso</span><span class="sxs-lookup"><span data-stu-id="f29fd-233">False</span></span>                                    |
| <span data-ttu-id="f29fd-234">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="f29fd-234">Is-Single-Valued</span></span>       | <span data-ttu-id="f29fd-235">Vero</span><span class="sxs-lookup"><span data-stu-id="f29fd-235">True</span></span>                                     |
| <span data-ttu-id="f29fd-236">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="f29fd-236">Is Indexed</span></span>             | <span data-ttu-id="f29fd-237">Falso</span><span class="sxs-lookup"><span data-stu-id="f29fd-237">False</span></span>                                    |
| <span data-ttu-id="f29fd-238">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="f29fd-238">In Global Catalog</span></span>      | <span data-ttu-id="f29fd-239">Falso</span><span class="sxs-lookup"><span data-stu-id="f29fd-239">False</span></span>                                    |
| <span data-ttu-id="f29fd-240">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="f29fd-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="f29fd-241">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="f29fd-241">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="f29fd-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f29fd-242">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="f29fd-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f29fd-243">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="f29fd-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f29fd-244">Search-Flags</span></span>           | <span data-ttu-id="f29fd-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f29fd-245">0x00000000</span></span>                               |
| <span data-ttu-id="f29fd-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f29fd-246">System-Flags</span></span>           | <span data-ttu-id="f29fd-247">0x00000011</span><span class="sxs-lookup"><span data-stu-id="f29fd-247">0x00000011</span></span>                               |
| <span data-ttu-id="f29fd-248">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="f29fd-248">Classes used in</span></span>        | [<span data-ttu-id="f29fd-249">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="f29fd-249">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f29fd-250">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f29fd-250">Windows Server 2012</span></span>



| <span data-ttu-id="f29fd-251">Voce</span><span class="sxs-lookup"><span data-stu-id="f29fd-251">Entry</span></span> | <span data-ttu-id="f29fd-252">Valore</span><span class="sxs-lookup"><span data-stu-id="f29fd-252">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="f29fd-253">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="f29fd-253">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="f29fd-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f29fd-254">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="f29fd-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="f29fd-255">System-Only</span></span>            | <span data-ttu-id="f29fd-256">Falso</span><span class="sxs-lookup"><span data-stu-id="f29fd-256">False</span></span>                                    |
| <span data-ttu-id="f29fd-257">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="f29fd-257">Is-Single-Valued</span></span>       | <span data-ttu-id="f29fd-258">Vero</span><span class="sxs-lookup"><span data-stu-id="f29fd-258">True</span></span>                                     |
| <span data-ttu-id="f29fd-259">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="f29fd-259">Is Indexed</span></span>             | <span data-ttu-id="f29fd-260">Falso</span><span class="sxs-lookup"><span data-stu-id="f29fd-260">False</span></span>                                    |
| <span data-ttu-id="f29fd-261">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="f29fd-261">In Global Catalog</span></span>      | <span data-ttu-id="f29fd-262">Falso</span><span class="sxs-lookup"><span data-stu-id="f29fd-262">False</span></span>                                    |
| <span data-ttu-id="f29fd-263">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="f29fd-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="f29fd-264">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="f29fd-264">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="f29fd-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f29fd-265">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="f29fd-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f29fd-266">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="f29fd-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f29fd-267">Search-Flags</span></span>           | <span data-ttu-id="f29fd-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f29fd-268">0x00000000</span></span>                               |
| <span data-ttu-id="f29fd-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f29fd-269">System-Flags</span></span>           | <span data-ttu-id="f29fd-270">0x00000011</span><span class="sxs-lookup"><span data-stu-id="f29fd-270">0x00000011</span></span>                               |
| <span data-ttu-id="f29fd-271">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="f29fd-271">Classes used in</span></span>        | [<span data-ttu-id="f29fd-272">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="f29fd-272">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



 

 





