---
title: Attributo Managed-Objects
description: Contiene l'elenco di oggetti gestiti dall'utente. Gli oggetti elencati sono quelli la cui proprietà managedBy è impostata su questo utente. Ogni elemento nell'elenco è un riferimento collegato all'oggetto gestito.
ms.assetid: 59b76431-03a5-4839-8800-ef03d26b66cc
ms.tgt_platform: multiple
keywords:
- Schema AD Managed-Objects attribute
- Schema AD dell'attributo managedObjects
topic_type:
- apiref
api_name:
- Managed-Objects
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48c7bc489d11c99f8790426a531e09a20f133476
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "106303002"
---
# <a name="managed-objects-attribute"></a><span data-ttu-id="8723d-107">Attributo Managed-Objects</span><span class="sxs-lookup"><span data-stu-id="8723d-107">Managed-Objects attribute</span></span>

<span data-ttu-id="8723d-108">Contiene l'elenco di oggetti gestiti dall'utente.</span><span class="sxs-lookup"><span data-stu-id="8723d-108">Contains the list of objects that are managed by the user.</span></span> <span data-ttu-id="8723d-109">Gli oggetti elencati sono quelli la cui proprietà managedBy è impostata su questo utente.</span><span class="sxs-lookup"><span data-stu-id="8723d-109">The objects listed are those that have the property managedBy property set to this user.</span></span> <span data-ttu-id="8723d-110">Ogni elemento nell'elenco è un riferimento collegato all'oggetto gestito.</span><span class="sxs-lookup"><span data-stu-id="8723d-110">Each item in the list is a linked reference to the managed object.</span></span>



| <span data-ttu-id="8723d-111">Voce</span><span class="sxs-lookup"><span data-stu-id="8723d-111">Entry</span></span> | <span data-ttu-id="8723d-112">Valore</span><span class="sxs-lookup"><span data-stu-id="8723d-112">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8723d-113">CN</span><span class="sxs-lookup"><span data-stu-id="8723d-113">CN</span></span>                | <span data-ttu-id="8723d-114">Managed-Objects</span><span class="sxs-lookup"><span data-stu-id="8723d-114">Managed-Objects</span></span>                                                                    |
| <span data-ttu-id="8723d-115">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="8723d-115">Ldap-Display-Name</span></span> | <span data-ttu-id="8723d-116">managedObjects</span><span class="sxs-lookup"><span data-stu-id="8723d-116">managedObjects</span></span>                                                                     |
| <span data-ttu-id="8723d-117">Dimensione</span><span class="sxs-lookup"><span data-stu-id="8723d-117">Size</span></span>              | \-                                                                                 |
| <span data-ttu-id="8723d-118">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="8723d-118">Update Privilege</span></span>  | <span data-ttu-id="8723d-119">Questo valore viene impostato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="8723d-119">This value is set by the system.</span></span>                                                   |
| <span data-ttu-id="8723d-120">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="8723d-120">Update Frequency</span></span>  | <span data-ttu-id="8723d-121">Quando viene creato il record degli utenti e ogni volta che è necessario modificare gli oggetti gestiti.</span><span class="sxs-lookup"><span data-stu-id="8723d-121">When the users record is created and whenever the managed objects needs to change.</span></span> |
| <span data-ttu-id="8723d-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="8723d-122">Attribute-Id</span></span>      | <span data-ttu-id="8723d-123">1.2.840.113556.1.4.654</span><span class="sxs-lookup"><span data-stu-id="8723d-123">1.2.840.113556.1.4.654</span></span>                                                             |
| <span data-ttu-id="8723d-124">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="8723d-124">System-Id-Guid</span></span>    | <span data-ttu-id="8723d-125">0296c124-40da-11d1-a9c0-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="8723d-125">0296c124-40da-11d1-a9c0-0000f80367c1</span></span>                                               |
| <span data-ttu-id="8723d-126">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8723d-126">Syntax</span></span>            | [<span data-ttu-id="8723d-127">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="8723d-127">**Object(DS-DN)**</span></span>](s-object-ds-dn.md)                                            |



## <a name="implementations"></a><span data-ttu-id="8723d-128">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="8723d-128">Implementations</span></span>

-   [<span data-ttu-id="8723d-129">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="8723d-129">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="8723d-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="8723d-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="8723d-131">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="8723d-131">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="8723d-132">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="8723d-132">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="8723d-133">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="8723d-133">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="8723d-134">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="8723d-134">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="8723d-135">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="8723d-135">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="8723d-136">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8723d-136">Windows 2000 Server</span></span>



| <span data-ttu-id="8723d-137">Voce</span><span class="sxs-lookup"><span data-stu-id="8723d-137">Entry</span></span> | <span data-ttu-id="8723d-138">Valore</span><span class="sxs-lookup"><span data-stu-id="8723d-138">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="8723d-139">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="8723d-139">Link-Id</span></span>                | <span data-ttu-id="8723d-140">73</span><span class="sxs-lookup"><span data-stu-id="8723d-140">73</span></span>                              |
| <span data-ttu-id="8723d-141">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8723d-141">MAPI-Id</span></span>                | <span data-ttu-id="8723d-142">0x8024</span><span class="sxs-lookup"><span data-stu-id="8723d-142">0x8024</span></span>                          |
| <span data-ttu-id="8723d-143">System-Only</span><span class="sxs-lookup"><span data-stu-id="8723d-143">System-Only</span></span>            | <span data-ttu-id="8723d-144">Vero</span><span class="sxs-lookup"><span data-stu-id="8723d-144">True</span></span>                            |
| <span data-ttu-id="8723d-145">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="8723d-145">Is-Single-Valued</span></span>       | <span data-ttu-id="8723d-146">Falso</span><span class="sxs-lookup"><span data-stu-id="8723d-146">False</span></span>                           |
| <span data-ttu-id="8723d-147">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="8723d-147">Is Indexed</span></span>             | <span data-ttu-id="8723d-148">Falso</span><span class="sxs-lookup"><span data-stu-id="8723d-148">False</span></span>                           |
| <span data-ttu-id="8723d-149">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="8723d-149">In Global Catalog</span></span>      | <span data-ttu-id="8723d-150">Falso</span><span class="sxs-lookup"><span data-stu-id="8723d-150">False</span></span>                           |
| <span data-ttu-id="8723d-151">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="8723d-151">NT-Security-Descriptor</span></span> | <span data-ttu-id="8723d-152">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="8723d-152">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="8723d-153">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8723d-153">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="8723d-154">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8723d-154">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="8723d-155">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8723d-155">Search-Flags</span></span>           | <span data-ttu-id="8723d-156">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8723d-156">0x00000000</span></span>                      |
| <span data-ttu-id="8723d-157">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8723d-157">System-Flags</span></span>           | <span data-ttu-id="8723d-158">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8723d-158">0x00000010</span></span>                      |
| <span data-ttu-id="8723d-159">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="8723d-159">Classes used in</span></span>        | [<span data-ttu-id="8723d-160">**In alto**</span><span class="sxs-lookup"><span data-stu-id="8723d-160">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="8723d-161">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8723d-161">Windows Server 2003</span></span>



| <span data-ttu-id="8723d-162">Voce</span><span class="sxs-lookup"><span data-stu-id="8723d-162">Entry</span></span> | <span data-ttu-id="8723d-163">Valore</span><span class="sxs-lookup"><span data-stu-id="8723d-163">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="8723d-164">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="8723d-164">Link-Id</span></span>                | <span data-ttu-id="8723d-165">73</span><span class="sxs-lookup"><span data-stu-id="8723d-165">73</span></span>                              |
| <span data-ttu-id="8723d-166">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8723d-166">MAPI-Id</span></span>                | <span data-ttu-id="8723d-167">0x8024</span><span class="sxs-lookup"><span data-stu-id="8723d-167">0x8024</span></span>                          |
| <span data-ttu-id="8723d-168">System-Only</span><span class="sxs-lookup"><span data-stu-id="8723d-168">System-Only</span></span>            | <span data-ttu-id="8723d-169">Vero</span><span class="sxs-lookup"><span data-stu-id="8723d-169">True</span></span>                            |
| <span data-ttu-id="8723d-170">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="8723d-170">Is-Single-Valued</span></span>       | <span data-ttu-id="8723d-171">Falso</span><span class="sxs-lookup"><span data-stu-id="8723d-171">False</span></span>                           |
| <span data-ttu-id="8723d-172">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="8723d-172">Is Indexed</span></span>             | <span data-ttu-id="8723d-173">Falso</span><span class="sxs-lookup"><span data-stu-id="8723d-173">False</span></span>                           |
| <span data-ttu-id="8723d-174">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="8723d-174">In Global Catalog</span></span>      | <span data-ttu-id="8723d-175">Falso</span><span class="sxs-lookup"><span data-stu-id="8723d-175">False</span></span>                           |
| <span data-ttu-id="8723d-176">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="8723d-176">NT-Security-Descriptor</span></span> | <span data-ttu-id="8723d-177">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="8723d-177">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="8723d-178">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8723d-178">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="8723d-179">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8723d-179">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="8723d-180">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8723d-180">Search-Flags</span></span>           | <span data-ttu-id="8723d-181">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8723d-181">0x00000000</span></span>                      |
| <span data-ttu-id="8723d-182">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8723d-182">System-Flags</span></span>           | <span data-ttu-id="8723d-183">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8723d-183">0x00000010</span></span>                      |
| <span data-ttu-id="8723d-184">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="8723d-184">Classes used in</span></span>        | [<span data-ttu-id="8723d-185">**In alto**</span><span class="sxs-lookup"><span data-stu-id="8723d-185">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="8723d-186">ADAM</span><span class="sxs-lookup"><span data-stu-id="8723d-186">ADAM</span></span>



| <span data-ttu-id="8723d-187">Voce</span><span class="sxs-lookup"><span data-stu-id="8723d-187">Entry</span></span> | <span data-ttu-id="8723d-188">Valore</span><span class="sxs-lookup"><span data-stu-id="8723d-188">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="8723d-189">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="8723d-189">Link-Id</span></span>                | <span data-ttu-id="8723d-190">73</span><span class="sxs-lookup"><span data-stu-id="8723d-190">73</span></span>                              |
| <span data-ttu-id="8723d-191">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8723d-191">MAPI-Id</span></span>                | <span data-ttu-id="8723d-192">0x8024</span><span class="sxs-lookup"><span data-stu-id="8723d-192">0x8024</span></span>                          |
| <span data-ttu-id="8723d-193">System-Only</span><span class="sxs-lookup"><span data-stu-id="8723d-193">System-Only</span></span>            | <span data-ttu-id="8723d-194">Vero</span><span class="sxs-lookup"><span data-stu-id="8723d-194">True</span></span>                            |
| <span data-ttu-id="8723d-195">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="8723d-195">Is-Single-Valued</span></span>       | <span data-ttu-id="8723d-196">Falso</span><span class="sxs-lookup"><span data-stu-id="8723d-196">False</span></span>                           |
| <span data-ttu-id="8723d-197">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="8723d-197">Is Indexed</span></span>             | <span data-ttu-id="8723d-198">Falso</span><span class="sxs-lookup"><span data-stu-id="8723d-198">False</span></span>                           |
| <span data-ttu-id="8723d-199">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="8723d-199">In Global Catalog</span></span>      | <span data-ttu-id="8723d-200">Falso</span><span class="sxs-lookup"><span data-stu-id="8723d-200">False</span></span>                           |
| <span data-ttu-id="8723d-201">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="8723d-201">NT-Security-Descriptor</span></span> | <span data-ttu-id="8723d-202">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="8723d-202">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="8723d-203">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8723d-203">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="8723d-204">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8723d-204">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="8723d-205">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8723d-205">Search-Flags</span></span>           | <span data-ttu-id="8723d-206">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8723d-206">0x00000000</span></span>                      |
| <span data-ttu-id="8723d-207">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8723d-207">System-Flags</span></span>           | <span data-ttu-id="8723d-208">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8723d-208">0x00000010</span></span>                      |
| <span data-ttu-id="8723d-209">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="8723d-209">Classes used in</span></span>        | [<span data-ttu-id="8723d-210">**In alto**</span><span class="sxs-lookup"><span data-stu-id="8723d-210">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="8723d-211">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="8723d-211">Windows Server 2003 R2</span></span>



| <span data-ttu-id="8723d-212">Voce</span><span class="sxs-lookup"><span data-stu-id="8723d-212">Entry</span></span> | <span data-ttu-id="8723d-213">Valore</span><span class="sxs-lookup"><span data-stu-id="8723d-213">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="8723d-214">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="8723d-214">Link-Id</span></span>                | <span data-ttu-id="8723d-215">73</span><span class="sxs-lookup"><span data-stu-id="8723d-215">73</span></span>                              |
| <span data-ttu-id="8723d-216">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8723d-216">MAPI-Id</span></span>                | <span data-ttu-id="8723d-217">0x8024</span><span class="sxs-lookup"><span data-stu-id="8723d-217">0x8024</span></span>                          |
| <span data-ttu-id="8723d-218">System-Only</span><span class="sxs-lookup"><span data-stu-id="8723d-218">System-Only</span></span>            | <span data-ttu-id="8723d-219">Vero</span><span class="sxs-lookup"><span data-stu-id="8723d-219">True</span></span>                            |
| <span data-ttu-id="8723d-220">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="8723d-220">Is-Single-Valued</span></span>       | <span data-ttu-id="8723d-221">Falso</span><span class="sxs-lookup"><span data-stu-id="8723d-221">False</span></span>                           |
| <span data-ttu-id="8723d-222">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="8723d-222">Is Indexed</span></span>             | <span data-ttu-id="8723d-223">Falso</span><span class="sxs-lookup"><span data-stu-id="8723d-223">False</span></span>                           |
| <span data-ttu-id="8723d-224">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="8723d-224">In Global Catalog</span></span>      | <span data-ttu-id="8723d-225">Falso</span><span class="sxs-lookup"><span data-stu-id="8723d-225">False</span></span>                           |
| <span data-ttu-id="8723d-226">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="8723d-226">NT-Security-Descriptor</span></span> | <span data-ttu-id="8723d-227">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="8723d-227">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="8723d-228">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8723d-228">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="8723d-229">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8723d-229">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="8723d-230">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8723d-230">Search-Flags</span></span>           | <span data-ttu-id="8723d-231">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8723d-231">0x00000000</span></span>                      |
| <span data-ttu-id="8723d-232">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8723d-232">System-Flags</span></span>           | <span data-ttu-id="8723d-233">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8723d-233">0x00000010</span></span>                      |
| <span data-ttu-id="8723d-234">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="8723d-234">Classes used in</span></span>        | [<span data-ttu-id="8723d-235">**In alto**</span><span class="sxs-lookup"><span data-stu-id="8723d-235">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="8723d-236">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8723d-236">Windows Server 2008</span></span>



| <span data-ttu-id="8723d-237">Voce</span><span class="sxs-lookup"><span data-stu-id="8723d-237">Entry</span></span> | <span data-ttu-id="8723d-238">Valore</span><span class="sxs-lookup"><span data-stu-id="8723d-238">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="8723d-239">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="8723d-239">Link-Id</span></span>                | <span data-ttu-id="8723d-240">73</span><span class="sxs-lookup"><span data-stu-id="8723d-240">73</span></span>                              |
| <span data-ttu-id="8723d-241">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8723d-241">MAPI-Id</span></span>                | <span data-ttu-id="8723d-242">0x8024</span><span class="sxs-lookup"><span data-stu-id="8723d-242">0x8024</span></span>                          |
| <span data-ttu-id="8723d-243">System-Only</span><span class="sxs-lookup"><span data-stu-id="8723d-243">System-Only</span></span>            | <span data-ttu-id="8723d-244">Vero</span><span class="sxs-lookup"><span data-stu-id="8723d-244">True</span></span>                            |
| <span data-ttu-id="8723d-245">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="8723d-245">Is-Single-Valued</span></span>       | <span data-ttu-id="8723d-246">Falso</span><span class="sxs-lookup"><span data-stu-id="8723d-246">False</span></span>                           |
| <span data-ttu-id="8723d-247">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="8723d-247">Is Indexed</span></span>             | <span data-ttu-id="8723d-248">Falso</span><span class="sxs-lookup"><span data-stu-id="8723d-248">False</span></span>                           |
| <span data-ttu-id="8723d-249">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="8723d-249">In Global Catalog</span></span>      | <span data-ttu-id="8723d-250">Falso</span><span class="sxs-lookup"><span data-stu-id="8723d-250">False</span></span>                           |
| <span data-ttu-id="8723d-251">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="8723d-251">NT-Security-Descriptor</span></span> | <span data-ttu-id="8723d-252">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="8723d-252">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="8723d-253">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8723d-253">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="8723d-254">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8723d-254">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="8723d-255">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8723d-255">Search-Flags</span></span>           | <span data-ttu-id="8723d-256">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8723d-256">0x00000000</span></span>                      |
| <span data-ttu-id="8723d-257">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8723d-257">System-Flags</span></span>           | <span data-ttu-id="8723d-258">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8723d-258">0x00000010</span></span>                      |
| <span data-ttu-id="8723d-259">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="8723d-259">Classes used in</span></span>        | [<span data-ttu-id="8723d-260">**In alto**</span><span class="sxs-lookup"><span data-stu-id="8723d-260">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="8723d-261">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8723d-261">Windows Server 2008 R2</span></span>



| <span data-ttu-id="8723d-262">Voce</span><span class="sxs-lookup"><span data-stu-id="8723d-262">Entry</span></span> | <span data-ttu-id="8723d-263">Valore</span><span class="sxs-lookup"><span data-stu-id="8723d-263">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="8723d-264">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="8723d-264">Link-Id</span></span>                | <span data-ttu-id="8723d-265">73</span><span class="sxs-lookup"><span data-stu-id="8723d-265">73</span></span>                              |
| <span data-ttu-id="8723d-266">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8723d-266">MAPI-Id</span></span>                | <span data-ttu-id="8723d-267">0x8024</span><span class="sxs-lookup"><span data-stu-id="8723d-267">0x8024</span></span>                          |
| <span data-ttu-id="8723d-268">System-Only</span><span class="sxs-lookup"><span data-stu-id="8723d-268">System-Only</span></span>            | <span data-ttu-id="8723d-269">Vero</span><span class="sxs-lookup"><span data-stu-id="8723d-269">True</span></span>                            |
| <span data-ttu-id="8723d-270">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="8723d-270">Is-Single-Valued</span></span>       | <span data-ttu-id="8723d-271">Falso</span><span class="sxs-lookup"><span data-stu-id="8723d-271">False</span></span>                           |
| <span data-ttu-id="8723d-272">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="8723d-272">Is Indexed</span></span>             | <span data-ttu-id="8723d-273">Falso</span><span class="sxs-lookup"><span data-stu-id="8723d-273">False</span></span>                           |
| <span data-ttu-id="8723d-274">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="8723d-274">In Global Catalog</span></span>      | <span data-ttu-id="8723d-275">Falso</span><span class="sxs-lookup"><span data-stu-id="8723d-275">False</span></span>                           |
| <span data-ttu-id="8723d-276">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="8723d-276">NT-Security-Descriptor</span></span> | <span data-ttu-id="8723d-277">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="8723d-277">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="8723d-278">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8723d-278">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="8723d-279">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8723d-279">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="8723d-280">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8723d-280">Search-Flags</span></span>           | <span data-ttu-id="8723d-281">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8723d-281">0x00000000</span></span>                      |
| <span data-ttu-id="8723d-282">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8723d-282">System-Flags</span></span>           | <span data-ttu-id="8723d-283">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8723d-283">0x00000010</span></span>                      |
| <span data-ttu-id="8723d-284">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="8723d-284">Classes used in</span></span>        | [<span data-ttu-id="8723d-285">**In alto**</span><span class="sxs-lookup"><span data-stu-id="8723d-285">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="8723d-286">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8723d-286">Windows Server 2012</span></span>



| <span data-ttu-id="8723d-287">Voce</span><span class="sxs-lookup"><span data-stu-id="8723d-287">Entry</span></span> | <span data-ttu-id="8723d-288">Valore</span><span class="sxs-lookup"><span data-stu-id="8723d-288">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="8723d-289">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="8723d-289">Link-Id</span></span>                | <span data-ttu-id="8723d-290">73</span><span class="sxs-lookup"><span data-stu-id="8723d-290">73</span></span>                              |
| <span data-ttu-id="8723d-291">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8723d-291">MAPI-Id</span></span>                | <span data-ttu-id="8723d-292">0x8024</span><span class="sxs-lookup"><span data-stu-id="8723d-292">0x8024</span></span>                          |
| <span data-ttu-id="8723d-293">System-Only</span><span class="sxs-lookup"><span data-stu-id="8723d-293">System-Only</span></span>            | <span data-ttu-id="8723d-294">Vero</span><span class="sxs-lookup"><span data-stu-id="8723d-294">True</span></span>                            |
| <span data-ttu-id="8723d-295">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="8723d-295">Is-Single-Valued</span></span>       | <span data-ttu-id="8723d-296">Falso</span><span class="sxs-lookup"><span data-stu-id="8723d-296">False</span></span>                           |
| <span data-ttu-id="8723d-297">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="8723d-297">Is Indexed</span></span>             | <span data-ttu-id="8723d-298">Falso</span><span class="sxs-lookup"><span data-stu-id="8723d-298">False</span></span>                           |
| <span data-ttu-id="8723d-299">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="8723d-299">In Global Catalog</span></span>      | <span data-ttu-id="8723d-300">Falso</span><span class="sxs-lookup"><span data-stu-id="8723d-300">False</span></span>                           |
| <span data-ttu-id="8723d-301">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="8723d-301">NT-Security-Descriptor</span></span> | <span data-ttu-id="8723d-302">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="8723d-302">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="8723d-303">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8723d-303">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="8723d-304">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8723d-304">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="8723d-305">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8723d-305">Search-Flags</span></span>           | <span data-ttu-id="8723d-306">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8723d-306">0x00000000</span></span>                      |
| <span data-ttu-id="8723d-307">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8723d-307">System-Flags</span></span>           | <span data-ttu-id="8723d-308">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8723d-308">0x00000010</span></span>                      |
| <span data-ttu-id="8723d-309">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="8723d-309">Classes used in</span></span>        | [<span data-ttu-id="8723d-310">**In alto**</span><span class="sxs-lookup"><span data-stu-id="8723d-310">**Top**</span></span>](c-top.md)<br/> |



 

 





