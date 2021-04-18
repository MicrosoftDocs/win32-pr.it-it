---
title: attributo ms-FRS-Hub-member
description: L'attributo ms-FRS-Hub-Member viene usato per registrare le impostazioni di topologia NTFRS preferite.
ms.assetid: df8623e0-745a-46f8-a696-8f6e7014fd2b
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo ms-FRS-Hub-member
- msFRS-Hub-schema AD attributo membro
topic_type:
- apiref
api_name:
- ms-FRS-Hub-Member
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56a211c5951ac589d00c4b8c92c031c80b2d1415
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "106303233"
---
# <a name="ms-frs-hub-member-attribute"></a><span data-ttu-id="bafe3-105">attributo ms-FRS-Hub-member</span><span class="sxs-lookup"><span data-stu-id="bafe3-105">ms-FRS-Hub-Member attribute</span></span>

<span data-ttu-id="bafe3-106">L'attributo **MS-FRS-Hub-member** viene usato per registrare le impostazioni di topologia NTFRS preferite.</span><span class="sxs-lookup"><span data-stu-id="bafe3-106">The **ms-FRS-Hub-Member** attribute is used to record the preferred NTFRS topology settings.</span></span> <span data-ttu-id="bafe3-107">Quando un membro FRS viene aggiunto o eliminato a un set di repliche, viene fatto riferimento a questi attributi e vengono apportate modifiche appropriate alle connessioni tra il resto dei membri FRS nel set di repliche.</span><span class="sxs-lookup"><span data-stu-id="bafe3-107">When an FRS member gets added or deleted to a replica set, these attributes are referred and appropriate adjustments are made to the connections between the rest of the FRS members in the replica set.</span></span>



| <span data-ttu-id="bafe3-108">Voce</span><span class="sxs-lookup"><span data-stu-id="bafe3-108">Entry</span></span> | <span data-ttu-id="bafe3-109">Valore</span><span class="sxs-lookup"><span data-stu-id="bafe3-109">Value</span></span> |
|-------------------|--------------------------------------------------------------------|
| <span data-ttu-id="bafe3-110">CN</span><span class="sxs-lookup"><span data-stu-id="bafe3-110">CN</span></span>                | <span data-ttu-id="bafe3-111">MS-FRS-Hub-membro</span><span class="sxs-lookup"><span data-stu-id="bafe3-111">ms-FRS-Hub-Member</span></span>                                                  |
| <span data-ttu-id="bafe3-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="bafe3-112">Ldap-Display-Name</span></span> | <span data-ttu-id="bafe3-113">msFRS-Hub-membro</span><span class="sxs-lookup"><span data-stu-id="bafe3-113">msFRS-Hub-Member</span></span>                                                   |
| <span data-ttu-id="bafe3-114">Dimensione</span><span class="sxs-lookup"><span data-stu-id="bafe3-114">Size</span></span>              | \-                                                                 |
| <span data-ttu-id="bafe3-115">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="bafe3-115">Update Privilege</span></span>  | <span data-ttu-id="bafe3-116">Amministratore di dominio</span><span class="sxs-lookup"><span data-stu-id="bafe3-116">Domain administrator</span></span>                                               |
| <span data-ttu-id="bafe3-117">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="bafe3-117">Update Frequency</span></span>  | <span data-ttu-id="bafe3-118">Quando viene creato il set di repliche o la topologia preferita viene modificata.</span><span class="sxs-lookup"><span data-stu-id="bafe3-118">When the replica set is created or the preferred topology changes.</span></span> |
| <span data-ttu-id="bafe3-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="bafe3-119">Attribute-Id</span></span>      | <span data-ttu-id="bafe3-120">1.2.840.113556.1.4.1693</span><span class="sxs-lookup"><span data-stu-id="bafe3-120">1.2.840.113556.1.4.1693</span></span>                                            |
| <span data-ttu-id="bafe3-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="bafe3-121">System-Id-Guid</span></span>    | <span data-ttu-id="bafe3-122">5643ff81-35b6-4ca9-9512-baf0bd0a2772</span><span class="sxs-lookup"><span data-stu-id="bafe3-122">5643ff81-35b6-4ca9-9512-baf0bd0a2772</span></span>                               |
| <span data-ttu-id="bafe3-123">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bafe3-123">Syntax</span></span>            | [<span data-ttu-id="bafe3-124">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="bafe3-124">**Object(DS-DN)**</span></span>](s-object-ds-dn.md)                            |



## <a name="implementations"></a><span data-ttu-id="bafe3-125">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="bafe3-125">Implementations</span></span>

-   [<span data-ttu-id="bafe3-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="bafe3-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="bafe3-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="bafe3-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="bafe3-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="bafe3-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="bafe3-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="bafe3-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="bafe3-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="bafe3-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="bafe3-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="bafe3-131">Windows Server 2003</span></span>



| <span data-ttu-id="bafe3-132">Voce</span><span class="sxs-lookup"><span data-stu-id="bafe3-132">Entry</span></span> | <span data-ttu-id="bafe3-133">Valore</span><span class="sxs-lookup"><span data-stu-id="bafe3-133">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="bafe3-134">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="bafe3-134">Link-Id</span></span>                | <span data-ttu-id="bafe3-135">1046</span><span class="sxs-lookup"><span data-stu-id="bafe3-135">1046</span></span>                                                      |
| <span data-ttu-id="bafe3-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bafe3-136">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="bafe3-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="bafe3-137">System-Only</span></span>            | <span data-ttu-id="bafe3-138">Falso</span><span class="sxs-lookup"><span data-stu-id="bafe3-138">False</span></span>                                                     |
| <span data-ttu-id="bafe3-139">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="bafe3-139">Is-Single-Valued</span></span>       | <span data-ttu-id="bafe3-140">Vero</span><span class="sxs-lookup"><span data-stu-id="bafe3-140">True</span></span>                                                      |
| <span data-ttu-id="bafe3-141">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="bafe3-141">Is Indexed</span></span>             | <span data-ttu-id="bafe3-142">Falso</span><span class="sxs-lookup"><span data-stu-id="bafe3-142">False</span></span>                                                     |
| <span data-ttu-id="bafe3-143">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="bafe3-143">In Global Catalog</span></span>      | <span data-ttu-id="bafe3-144">Falso</span><span class="sxs-lookup"><span data-stu-id="bafe3-144">False</span></span>                                                     |
| <span data-ttu-id="bafe3-145">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="bafe3-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="bafe3-146">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="bafe3-146">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="bafe3-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bafe3-147">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="bafe3-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bafe3-148">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="bafe3-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bafe3-149">Search-Flags</span></span>           | <span data-ttu-id="bafe3-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bafe3-150">0x00000000</span></span>                                                |
| <span data-ttu-id="bafe3-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bafe3-151">System-Flags</span></span>           | <span data-ttu-id="bafe3-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bafe3-152">0x00000000</span></span>                                                |
| <span data-ttu-id="bafe3-153">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="bafe3-153">Classes used in</span></span>        | [<span data-ttu-id="bafe3-154">**NTFRS-set di repliche**</span><span class="sxs-lookup"><span data-stu-id="bafe3-154">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="bafe3-155">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="bafe3-155">Windows Server 2003 R2</span></span>



| <span data-ttu-id="bafe3-156">Voce</span><span class="sxs-lookup"><span data-stu-id="bafe3-156">Entry</span></span> | <span data-ttu-id="bafe3-157">Valore</span><span class="sxs-lookup"><span data-stu-id="bafe3-157">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="bafe3-158">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="bafe3-158">Link-Id</span></span>                | <span data-ttu-id="bafe3-159">1046</span><span class="sxs-lookup"><span data-stu-id="bafe3-159">1046</span></span>                                                      |
| <span data-ttu-id="bafe3-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bafe3-160">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="bafe3-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="bafe3-161">System-Only</span></span>            | <span data-ttu-id="bafe3-162">Falso</span><span class="sxs-lookup"><span data-stu-id="bafe3-162">False</span></span>                                                     |
| <span data-ttu-id="bafe3-163">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="bafe3-163">Is-Single-Valued</span></span>       | <span data-ttu-id="bafe3-164">Vero</span><span class="sxs-lookup"><span data-stu-id="bafe3-164">True</span></span>                                                      |
| <span data-ttu-id="bafe3-165">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="bafe3-165">Is Indexed</span></span>             | <span data-ttu-id="bafe3-166">Falso</span><span class="sxs-lookup"><span data-stu-id="bafe3-166">False</span></span>                                                     |
| <span data-ttu-id="bafe3-167">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="bafe3-167">In Global Catalog</span></span>      | <span data-ttu-id="bafe3-168">Falso</span><span class="sxs-lookup"><span data-stu-id="bafe3-168">False</span></span>                                                     |
| <span data-ttu-id="bafe3-169">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="bafe3-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="bafe3-170">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="bafe3-170">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="bafe3-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bafe3-171">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="bafe3-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bafe3-172">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="bafe3-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bafe3-173">Search-Flags</span></span>           | <span data-ttu-id="bafe3-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bafe3-174">0x00000000</span></span>                                                |
| <span data-ttu-id="bafe3-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bafe3-175">System-Flags</span></span>           | <span data-ttu-id="bafe3-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bafe3-176">0x00000000</span></span>                                                |
| <span data-ttu-id="bafe3-177">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="bafe3-177">Classes used in</span></span>        | [<span data-ttu-id="bafe3-178">**NTFRS-set di repliche**</span><span class="sxs-lookup"><span data-stu-id="bafe3-178">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="bafe3-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bafe3-179">Windows Server 2008</span></span>



| <span data-ttu-id="bafe3-180">Voce</span><span class="sxs-lookup"><span data-stu-id="bafe3-180">Entry</span></span> | <span data-ttu-id="bafe3-181">Valore</span><span class="sxs-lookup"><span data-stu-id="bafe3-181">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="bafe3-182">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="bafe3-182">Link-Id</span></span>                | <span data-ttu-id="bafe3-183">1046</span><span class="sxs-lookup"><span data-stu-id="bafe3-183">1046</span></span>                                                      |
| <span data-ttu-id="bafe3-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bafe3-184">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="bafe3-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="bafe3-185">System-Only</span></span>            | <span data-ttu-id="bafe3-186">Falso</span><span class="sxs-lookup"><span data-stu-id="bafe3-186">False</span></span>                                                     |
| <span data-ttu-id="bafe3-187">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="bafe3-187">Is-Single-Valued</span></span>       | <span data-ttu-id="bafe3-188">Vero</span><span class="sxs-lookup"><span data-stu-id="bafe3-188">True</span></span>                                                      |
| <span data-ttu-id="bafe3-189">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="bafe3-189">Is Indexed</span></span>             | <span data-ttu-id="bafe3-190">Falso</span><span class="sxs-lookup"><span data-stu-id="bafe3-190">False</span></span>                                                     |
| <span data-ttu-id="bafe3-191">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="bafe3-191">In Global Catalog</span></span>      | <span data-ttu-id="bafe3-192">Falso</span><span class="sxs-lookup"><span data-stu-id="bafe3-192">False</span></span>                                                     |
| <span data-ttu-id="bafe3-193">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="bafe3-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="bafe3-194">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="bafe3-194">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="bafe3-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bafe3-195">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="bafe3-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bafe3-196">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="bafe3-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bafe3-197">Search-Flags</span></span>           | <span data-ttu-id="bafe3-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bafe3-198">0x00000000</span></span>                                                |
| <span data-ttu-id="bafe3-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bafe3-199">System-Flags</span></span>           | <span data-ttu-id="bafe3-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bafe3-200">0x00000000</span></span>                                                |
| <span data-ttu-id="bafe3-201">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="bafe3-201">Classes used in</span></span>        | [<span data-ttu-id="bafe3-202">**NTFRS-set di repliche**</span><span class="sxs-lookup"><span data-stu-id="bafe3-202">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="bafe3-203">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="bafe3-203">Windows Server 2008 R2</span></span>



| <span data-ttu-id="bafe3-204">Voce</span><span class="sxs-lookup"><span data-stu-id="bafe3-204">Entry</span></span> | <span data-ttu-id="bafe3-205">Valore</span><span class="sxs-lookup"><span data-stu-id="bafe3-205">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="bafe3-206">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="bafe3-206">Link-Id</span></span>                | <span data-ttu-id="bafe3-207">1046</span><span class="sxs-lookup"><span data-stu-id="bafe3-207">1046</span></span>                                                      |
| <span data-ttu-id="bafe3-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bafe3-208">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="bafe3-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="bafe3-209">System-Only</span></span>            | <span data-ttu-id="bafe3-210">Falso</span><span class="sxs-lookup"><span data-stu-id="bafe3-210">False</span></span>                                                     |
| <span data-ttu-id="bafe3-211">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="bafe3-211">Is-Single-Valued</span></span>       | <span data-ttu-id="bafe3-212">Vero</span><span class="sxs-lookup"><span data-stu-id="bafe3-212">True</span></span>                                                      |
| <span data-ttu-id="bafe3-213">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="bafe3-213">Is Indexed</span></span>             | <span data-ttu-id="bafe3-214">Falso</span><span class="sxs-lookup"><span data-stu-id="bafe3-214">False</span></span>                                                     |
| <span data-ttu-id="bafe3-215">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="bafe3-215">In Global Catalog</span></span>      | <span data-ttu-id="bafe3-216">Falso</span><span class="sxs-lookup"><span data-stu-id="bafe3-216">False</span></span>                                                     |
| <span data-ttu-id="bafe3-217">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="bafe3-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="bafe3-218">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="bafe3-218">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="bafe3-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bafe3-219">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="bafe3-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bafe3-220">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="bafe3-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bafe3-221">Search-Flags</span></span>           | <span data-ttu-id="bafe3-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bafe3-222">0x00000000</span></span>                                                |
| <span data-ttu-id="bafe3-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bafe3-223">System-Flags</span></span>           | <span data-ttu-id="bafe3-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bafe3-224">0x00000000</span></span>                                                |
| <span data-ttu-id="bafe3-225">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="bafe3-225">Classes used in</span></span>        | [<span data-ttu-id="bafe3-226">**NTFRS-set di repliche**</span><span class="sxs-lookup"><span data-stu-id="bafe3-226">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="bafe3-227">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="bafe3-227">Windows Server 2012</span></span>



| <span data-ttu-id="bafe3-228">Voce</span><span class="sxs-lookup"><span data-stu-id="bafe3-228">Entry</span></span> | <span data-ttu-id="bafe3-229">Valore</span><span class="sxs-lookup"><span data-stu-id="bafe3-229">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="bafe3-230">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="bafe3-230">Link-Id</span></span>                | <span data-ttu-id="bafe3-231">1046</span><span class="sxs-lookup"><span data-stu-id="bafe3-231">1046</span></span>                                                      |
| <span data-ttu-id="bafe3-232">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bafe3-232">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="bafe3-233">System-Only</span><span class="sxs-lookup"><span data-stu-id="bafe3-233">System-Only</span></span>            | <span data-ttu-id="bafe3-234">Falso</span><span class="sxs-lookup"><span data-stu-id="bafe3-234">False</span></span>                                                     |
| <span data-ttu-id="bafe3-235">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="bafe3-235">Is-Single-Valued</span></span>       | <span data-ttu-id="bafe3-236">Vero</span><span class="sxs-lookup"><span data-stu-id="bafe3-236">True</span></span>                                                      |
| <span data-ttu-id="bafe3-237">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="bafe3-237">Is Indexed</span></span>             | <span data-ttu-id="bafe3-238">Falso</span><span class="sxs-lookup"><span data-stu-id="bafe3-238">False</span></span>                                                     |
| <span data-ttu-id="bafe3-239">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="bafe3-239">In Global Catalog</span></span>      | <span data-ttu-id="bafe3-240">Falso</span><span class="sxs-lookup"><span data-stu-id="bafe3-240">False</span></span>                                                     |
| <span data-ttu-id="bafe3-241">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="bafe3-241">NT-Security-Descriptor</span></span> | <span data-ttu-id="bafe3-242">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="bafe3-242">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="bafe3-243">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bafe3-243">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="bafe3-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bafe3-244">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="bafe3-245">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bafe3-245">Search-Flags</span></span>           | <span data-ttu-id="bafe3-246">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bafe3-246">0x00000000</span></span>                                                |
| <span data-ttu-id="bafe3-247">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bafe3-247">System-Flags</span></span>           | <span data-ttu-id="bafe3-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bafe3-248">0x00000000</span></span>                                                |
| <span data-ttu-id="bafe3-249">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="bafe3-249">Classes used in</span></span>        | [<span data-ttu-id="bafe3-250">**NTFRS-set di repliche**</span><span class="sxs-lookup"><span data-stu-id="bafe3-250">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="bafe3-251">Commenti</span><span class="sxs-lookup"><span data-stu-id="bafe3-251">Remarks</span></span>

<span data-ttu-id="bafe3-252">Si tratta del nome distinto completo di un oggetto [**membro di NTFRS**](c-ntfrsmember.md) .</span><span class="sxs-lookup"><span data-stu-id="bafe3-252">This is the fully qualified distinguished name of an [**NTFRS-Member**](c-ntfrsmember.md) object.</span></span> <span data-ttu-id="bafe3-253">Il nome distinto è nel formato "CN = *<computerGuid>* , CN = *<Dfs Link Name>* , CN = *<Dfs Root name>* , CN = DFS Volumes, CN = File Replication Service, CN = System, DC =..."</span><span class="sxs-lookup"><span data-stu-id="bafe3-253">The distinguished name is in the format of "CN=*<computerGuid>*, CN=*<Dfs Link Name>*, CN=*<Dfs Root name>*, CN=DFS Volumes, CN=File Replication Service,CN=System, DC=..."</span></span>

 

 





