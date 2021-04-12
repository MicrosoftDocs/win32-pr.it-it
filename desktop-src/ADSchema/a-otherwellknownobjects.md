---
title: Attributo other-well-known-Objects
description: Contiene un elenco di contenitori per GUID e nome distinto. Questo consente il recupero di un oggetto dopo lo spostamento usando solo il GUID e il nome di dominio. Ogni volta che l'oggetto viene spostato, il sistema aggiorna automaticamente il nome distinto.
ms.assetid: 2f33c4ac-235c-47a1-9340-5b90f7edb73b
ms.tgt_platform: multiple
keywords:
- Altri attributi-well-known-Object-schema AD
- Schema AD dell'attributo otherWellKnownObjects archiviato nel
topic_type:
- apiref
api_name:
- Other-Well-Known-Objects
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d38b4f4b86f90368859f9fb966031f539f0399f
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104480272"
---
# <a name="other-well-known-objects-attribute"></a><span data-ttu-id="39996-107">Attributo other-well-known-Objects</span><span class="sxs-lookup"><span data-stu-id="39996-107">Other-Well-Known-Objects attribute</span></span>

<span data-ttu-id="39996-108">Contiene un elenco di contenitori per GUID e nome distinto.</span><span class="sxs-lookup"><span data-stu-id="39996-108">Contains a list of containers by GUID and Distinguished Name.</span></span> <span data-ttu-id="39996-109">Questo consente il recupero di un oggetto dopo lo spostamento usando solo il GUID e il nome di dominio.</span><span class="sxs-lookup"><span data-stu-id="39996-109">This permits retrieving an object after it has been moved by using just the GUID and the domain name.</span></span> <span data-ttu-id="39996-110">Ogni volta che l'oggetto viene spostato, il sistema aggiorna automaticamente il nome distinto.</span><span class="sxs-lookup"><span data-stu-id="39996-110">Whenever the object is moved, the system automatically updates the Distinguished Name.</span></span>



| <span data-ttu-id="39996-111">Voce</span><span class="sxs-lookup"><span data-stu-id="39996-111">Entry</span></span> | <span data-ttu-id="39996-112">Valore</span><span class="sxs-lookup"><span data-stu-id="39996-112">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39996-113">CN</span><span class="sxs-lookup"><span data-stu-id="39996-113">CN</span></span>                | <span data-ttu-id="39996-114">Altri oggetti-well-known</span><span class="sxs-lookup"><span data-stu-id="39996-114">Other-Well-Known-Objects</span></span>                                                                                                                                                                                      |
| <span data-ttu-id="39996-115">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="39996-115">Ldap-Display-Name</span></span> | <span data-ttu-id="39996-116">otherWellKnownObjects archiviato nel</span><span class="sxs-lookup"><span data-stu-id="39996-116">otherWellKnownObjects</span></span>                                                                                                                                                                                         |
| <span data-ttu-id="39996-117">Dimensione</span><span class="sxs-lookup"><span data-stu-id="39996-117">Size</span></span>              | <span data-ttu-id="39996-118">Esempio per il recupero del contenitore degli utenti nel dominio Microsoft: LDAP://(WKGUID = a9d1ca15768811d1aded00c04fd8d5cd, DC = Microsoft, DC = com).</span><span class="sxs-lookup"><span data-stu-id="39996-118">Sample for retrieving the Users container in the microsoft domain: LDAP://(WKGUID=a9d1ca15768811d1aded00c04fd8d5cd,dc=microsoft,dc=com).</span></span> <span data-ttu-id="39996-119">Nota: le parentesi angolari sono sostituite da parentesi per evitare conflitti XML.</span><span class="sxs-lookup"><span data-stu-id="39996-119">NOTE: Angle brackets replaced by parentheses to avoid XML conflicts.</span></span> |
| <span data-ttu-id="39996-120">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="39996-120">Update Privilege</span></span>  | <span data-ttu-id="39996-121">Amministratore schema</span><span class="sxs-lookup"><span data-stu-id="39996-121">Schema administrator</span></span>                                                                                                                                                                                          |
| <span data-ttu-id="39996-122">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="39996-122">Update Frequency</span></span>  | <span data-ttu-id="39996-123">Ogni volta che l'oggetto viene spostato.</span><span class="sxs-lookup"><span data-stu-id="39996-123">Whenever the object is moved.</span></span>                                                                                                                                                                                 |
| <span data-ttu-id="39996-124">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="39996-124">Attribute-Id</span></span>      | <span data-ttu-id="39996-125">1.2.840.113556.1.4.1359</span><span class="sxs-lookup"><span data-stu-id="39996-125">1.2.840.113556.1.4.1359</span></span>                                                                                                                                                                                       |
| <span data-ttu-id="39996-126">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="39996-126">System-Id-Guid</span></span>    | <span data-ttu-id="39996-127">1ea64e5d-ac0f-11d2-90df-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="39996-127">1ea64e5d-ac0f-11d2-90df-00c04fd91ab1</span></span>                                                                                                                                                                          |
| <span data-ttu-id="39996-128">Sintassi</span><span class="sxs-lookup"><span data-stu-id="39996-128">Syntax</span></span>            | [<span data-ttu-id="39996-129">**Object(DN-Binary)**</span><span class="sxs-lookup"><span data-stu-id="39996-129">**Object(DN-Binary)**</span></span>](s-object-dn-binary.md)                                                                                                                                                               |



## <a name="implementations"></a><span data-ttu-id="39996-130">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="39996-130">Implementations</span></span>

-   [<span data-ttu-id="39996-131">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="39996-131">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="39996-132">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="39996-132">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="39996-133">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="39996-133">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="39996-134">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="39996-134">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="39996-135">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="39996-135">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="39996-136">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="39996-136">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="39996-137">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="39996-137">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="39996-138">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="39996-138">Windows 2000 Server</span></span>



| <span data-ttu-id="39996-139">Voce</span><span class="sxs-lookup"><span data-stu-id="39996-139">Entry</span></span> | <span data-ttu-id="39996-140">Valore</span><span class="sxs-lookup"><span data-stu-id="39996-140">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="39996-141">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="39996-141">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="39996-142">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="39996-142">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="39996-143">System-Only</span><span class="sxs-lookup"><span data-stu-id="39996-143">System-Only</span></span>            | <span data-ttu-id="39996-144">Falso</span><span class="sxs-lookup"><span data-stu-id="39996-144">False</span></span>                           |
| <span data-ttu-id="39996-145">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="39996-145">Is-Single-Valued</span></span>       | <span data-ttu-id="39996-146">Falso</span><span class="sxs-lookup"><span data-stu-id="39996-146">False</span></span>                           |
| <span data-ttu-id="39996-147">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="39996-147">Is Indexed</span></span>             | <span data-ttu-id="39996-148">Falso</span><span class="sxs-lookup"><span data-stu-id="39996-148">False</span></span>                           |
| <span data-ttu-id="39996-149">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="39996-149">In Global Catalog</span></span>      | <span data-ttu-id="39996-150">Falso</span><span class="sxs-lookup"><span data-stu-id="39996-150">False</span></span>                           |
| <span data-ttu-id="39996-151">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="39996-151">NT-Security-Descriptor</span></span> | <span data-ttu-id="39996-152">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="39996-152">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="39996-153">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="39996-153">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="39996-154">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="39996-154">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="39996-155">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="39996-155">Search-Flags</span></span>           | <span data-ttu-id="39996-156">0x00000000</span><span class="sxs-lookup"><span data-stu-id="39996-156">0x00000000</span></span>                      |
| <span data-ttu-id="39996-157">System-Flags</span><span class="sxs-lookup"><span data-stu-id="39996-157">System-Flags</span></span>           | <span data-ttu-id="39996-158">0x00000010</span><span class="sxs-lookup"><span data-stu-id="39996-158">0x00000010</span></span>                      |
| <span data-ttu-id="39996-159">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="39996-159">Classes used in</span></span>        | [<span data-ttu-id="39996-160">**In alto**</span><span class="sxs-lookup"><span data-stu-id="39996-160">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="39996-161">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="39996-161">Windows Server 2003</span></span>



| <span data-ttu-id="39996-162">Voce</span><span class="sxs-lookup"><span data-stu-id="39996-162">Entry</span></span> | <span data-ttu-id="39996-163">Valore</span><span class="sxs-lookup"><span data-stu-id="39996-163">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="39996-164">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="39996-164">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="39996-165">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="39996-165">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="39996-166">System-Only</span><span class="sxs-lookup"><span data-stu-id="39996-166">System-Only</span></span>            | <span data-ttu-id="39996-167">Falso</span><span class="sxs-lookup"><span data-stu-id="39996-167">False</span></span>                           |
| <span data-ttu-id="39996-168">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="39996-168">Is-Single-Valued</span></span>       | <span data-ttu-id="39996-169">Falso</span><span class="sxs-lookup"><span data-stu-id="39996-169">False</span></span>                           |
| <span data-ttu-id="39996-170">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="39996-170">Is Indexed</span></span>             | <span data-ttu-id="39996-171">Falso</span><span class="sxs-lookup"><span data-stu-id="39996-171">False</span></span>                           |
| <span data-ttu-id="39996-172">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="39996-172">In Global Catalog</span></span>      | <span data-ttu-id="39996-173">Falso</span><span class="sxs-lookup"><span data-stu-id="39996-173">False</span></span>                           |
| <span data-ttu-id="39996-174">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="39996-174">NT-Security-Descriptor</span></span> | <span data-ttu-id="39996-175">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="39996-175">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="39996-176">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="39996-176">Range-Lower</span></span>            | <span data-ttu-id="39996-177">16</span><span class="sxs-lookup"><span data-stu-id="39996-177">16</span></span>                              |
| <span data-ttu-id="39996-178">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="39996-178">Range-Upper</span></span>            | <span data-ttu-id="39996-179">16</span><span class="sxs-lookup"><span data-stu-id="39996-179">16</span></span>                              |
| <span data-ttu-id="39996-180">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="39996-180">Search-Flags</span></span>           | <span data-ttu-id="39996-181">0x00000000</span><span class="sxs-lookup"><span data-stu-id="39996-181">0x00000000</span></span>                      |
| <span data-ttu-id="39996-182">System-Flags</span><span class="sxs-lookup"><span data-stu-id="39996-182">System-Flags</span></span>           | <span data-ttu-id="39996-183">0x00000010</span><span class="sxs-lookup"><span data-stu-id="39996-183">0x00000010</span></span>                      |
| <span data-ttu-id="39996-184">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="39996-184">Classes used in</span></span>        | [<span data-ttu-id="39996-185">**In alto**</span><span class="sxs-lookup"><span data-stu-id="39996-185">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="39996-186">ADAM</span><span class="sxs-lookup"><span data-stu-id="39996-186">ADAM</span></span>



| <span data-ttu-id="39996-187">Voce</span><span class="sxs-lookup"><span data-stu-id="39996-187">Entry</span></span> | <span data-ttu-id="39996-188">Valore</span><span class="sxs-lookup"><span data-stu-id="39996-188">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="39996-189">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="39996-189">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="39996-190">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="39996-190">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="39996-191">System-Only</span><span class="sxs-lookup"><span data-stu-id="39996-191">System-Only</span></span>            | <span data-ttu-id="39996-192">Falso</span><span class="sxs-lookup"><span data-stu-id="39996-192">False</span></span>                           |
| <span data-ttu-id="39996-193">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="39996-193">Is-Single-Valued</span></span>       | <span data-ttu-id="39996-194">Falso</span><span class="sxs-lookup"><span data-stu-id="39996-194">False</span></span>                           |
| <span data-ttu-id="39996-195">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="39996-195">Is Indexed</span></span>             | <span data-ttu-id="39996-196">Falso</span><span class="sxs-lookup"><span data-stu-id="39996-196">False</span></span>                           |
| <span data-ttu-id="39996-197">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="39996-197">In Global Catalog</span></span>      | <span data-ttu-id="39996-198">Falso</span><span class="sxs-lookup"><span data-stu-id="39996-198">False</span></span>                           |
| <span data-ttu-id="39996-199">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="39996-199">NT-Security-Descriptor</span></span> | <span data-ttu-id="39996-200">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="39996-200">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="39996-201">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="39996-201">Range-Lower</span></span>            | <span data-ttu-id="39996-202">16</span><span class="sxs-lookup"><span data-stu-id="39996-202">16</span></span>                              |
| <span data-ttu-id="39996-203">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="39996-203">Range-Upper</span></span>            | <span data-ttu-id="39996-204">16</span><span class="sxs-lookup"><span data-stu-id="39996-204">16</span></span>                              |
| <span data-ttu-id="39996-205">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="39996-205">Search-Flags</span></span>           | <span data-ttu-id="39996-206">0x00000000</span><span class="sxs-lookup"><span data-stu-id="39996-206">0x00000000</span></span>                      |
| <span data-ttu-id="39996-207">System-Flags</span><span class="sxs-lookup"><span data-stu-id="39996-207">System-Flags</span></span>           | <span data-ttu-id="39996-208">0x00000010</span><span class="sxs-lookup"><span data-stu-id="39996-208">0x00000010</span></span>                      |
| <span data-ttu-id="39996-209">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="39996-209">Classes used in</span></span>        | [<span data-ttu-id="39996-210">**In alto**</span><span class="sxs-lookup"><span data-stu-id="39996-210">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="39996-211">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="39996-211">Windows Server 2003 R2</span></span>



| <span data-ttu-id="39996-212">Voce</span><span class="sxs-lookup"><span data-stu-id="39996-212">Entry</span></span> | <span data-ttu-id="39996-213">Valore</span><span class="sxs-lookup"><span data-stu-id="39996-213">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="39996-214">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="39996-214">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="39996-215">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="39996-215">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="39996-216">System-Only</span><span class="sxs-lookup"><span data-stu-id="39996-216">System-Only</span></span>            | <span data-ttu-id="39996-217">Falso</span><span class="sxs-lookup"><span data-stu-id="39996-217">False</span></span>                           |
| <span data-ttu-id="39996-218">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="39996-218">Is-Single-Valued</span></span>       | <span data-ttu-id="39996-219">Falso</span><span class="sxs-lookup"><span data-stu-id="39996-219">False</span></span>                           |
| <span data-ttu-id="39996-220">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="39996-220">Is Indexed</span></span>             | <span data-ttu-id="39996-221">Falso</span><span class="sxs-lookup"><span data-stu-id="39996-221">False</span></span>                           |
| <span data-ttu-id="39996-222">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="39996-222">In Global Catalog</span></span>      | <span data-ttu-id="39996-223">Falso</span><span class="sxs-lookup"><span data-stu-id="39996-223">False</span></span>                           |
| <span data-ttu-id="39996-224">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="39996-224">NT-Security-Descriptor</span></span> | <span data-ttu-id="39996-225">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="39996-225">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="39996-226">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="39996-226">Range-Lower</span></span>            | <span data-ttu-id="39996-227">16</span><span class="sxs-lookup"><span data-stu-id="39996-227">16</span></span>                              |
| <span data-ttu-id="39996-228">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="39996-228">Range-Upper</span></span>            | <span data-ttu-id="39996-229">16</span><span class="sxs-lookup"><span data-stu-id="39996-229">16</span></span>                              |
| <span data-ttu-id="39996-230">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="39996-230">Search-Flags</span></span>           | <span data-ttu-id="39996-231">0x00000000</span><span class="sxs-lookup"><span data-stu-id="39996-231">0x00000000</span></span>                      |
| <span data-ttu-id="39996-232">System-Flags</span><span class="sxs-lookup"><span data-stu-id="39996-232">System-Flags</span></span>           | <span data-ttu-id="39996-233">0x00000010</span><span class="sxs-lookup"><span data-stu-id="39996-233">0x00000010</span></span>                      |
| <span data-ttu-id="39996-234">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="39996-234">Classes used in</span></span>        | [<span data-ttu-id="39996-235">**In alto**</span><span class="sxs-lookup"><span data-stu-id="39996-235">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="39996-236">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="39996-236">Windows Server 2008</span></span>



| <span data-ttu-id="39996-237">Voce</span><span class="sxs-lookup"><span data-stu-id="39996-237">Entry</span></span> | <span data-ttu-id="39996-238">Valore</span><span class="sxs-lookup"><span data-stu-id="39996-238">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="39996-239">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="39996-239">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="39996-240">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="39996-240">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="39996-241">System-Only</span><span class="sxs-lookup"><span data-stu-id="39996-241">System-Only</span></span>            | <span data-ttu-id="39996-242">Falso</span><span class="sxs-lookup"><span data-stu-id="39996-242">False</span></span>                           |
| <span data-ttu-id="39996-243">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="39996-243">Is-Single-Valued</span></span>       | <span data-ttu-id="39996-244">Falso</span><span class="sxs-lookup"><span data-stu-id="39996-244">False</span></span>                           |
| <span data-ttu-id="39996-245">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="39996-245">Is Indexed</span></span>             | <span data-ttu-id="39996-246">Falso</span><span class="sxs-lookup"><span data-stu-id="39996-246">False</span></span>                           |
| <span data-ttu-id="39996-247">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="39996-247">In Global Catalog</span></span>      | <span data-ttu-id="39996-248">Falso</span><span class="sxs-lookup"><span data-stu-id="39996-248">False</span></span>                           |
| <span data-ttu-id="39996-249">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="39996-249">NT-Security-Descriptor</span></span> | <span data-ttu-id="39996-250">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="39996-250">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="39996-251">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="39996-251">Range-Lower</span></span>            | <span data-ttu-id="39996-252">16</span><span class="sxs-lookup"><span data-stu-id="39996-252">16</span></span>                              |
| <span data-ttu-id="39996-253">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="39996-253">Range-Upper</span></span>            | <span data-ttu-id="39996-254">16</span><span class="sxs-lookup"><span data-stu-id="39996-254">16</span></span>                              |
| <span data-ttu-id="39996-255">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="39996-255">Search-Flags</span></span>           | <span data-ttu-id="39996-256">0x00000000</span><span class="sxs-lookup"><span data-stu-id="39996-256">0x00000000</span></span>                      |
| <span data-ttu-id="39996-257">System-Flags</span><span class="sxs-lookup"><span data-stu-id="39996-257">System-Flags</span></span>           | <span data-ttu-id="39996-258">0x00000010</span><span class="sxs-lookup"><span data-stu-id="39996-258">0x00000010</span></span>                      |
| <span data-ttu-id="39996-259">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="39996-259">Classes used in</span></span>        | [<span data-ttu-id="39996-260">**In alto**</span><span class="sxs-lookup"><span data-stu-id="39996-260">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="39996-261">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="39996-261">Windows Server 2008 R2</span></span>



| <span data-ttu-id="39996-262">Voce</span><span class="sxs-lookup"><span data-stu-id="39996-262">Entry</span></span> | <span data-ttu-id="39996-263">Valore</span><span class="sxs-lookup"><span data-stu-id="39996-263">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="39996-264">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="39996-264">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="39996-265">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="39996-265">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="39996-266">System-Only</span><span class="sxs-lookup"><span data-stu-id="39996-266">System-Only</span></span>            | <span data-ttu-id="39996-267">Falso</span><span class="sxs-lookup"><span data-stu-id="39996-267">False</span></span>                           |
| <span data-ttu-id="39996-268">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="39996-268">Is-Single-Valued</span></span>       | <span data-ttu-id="39996-269">Falso</span><span class="sxs-lookup"><span data-stu-id="39996-269">False</span></span>                           |
| <span data-ttu-id="39996-270">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="39996-270">Is Indexed</span></span>             | <span data-ttu-id="39996-271">Falso</span><span class="sxs-lookup"><span data-stu-id="39996-271">False</span></span>                           |
| <span data-ttu-id="39996-272">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="39996-272">In Global Catalog</span></span>      | <span data-ttu-id="39996-273">Falso</span><span class="sxs-lookup"><span data-stu-id="39996-273">False</span></span>                           |
| <span data-ttu-id="39996-274">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="39996-274">NT-Security-Descriptor</span></span> | <span data-ttu-id="39996-275">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="39996-275">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="39996-276">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="39996-276">Range-Lower</span></span>            | <span data-ttu-id="39996-277">16</span><span class="sxs-lookup"><span data-stu-id="39996-277">16</span></span>                              |
| <span data-ttu-id="39996-278">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="39996-278">Range-Upper</span></span>            | <span data-ttu-id="39996-279">16</span><span class="sxs-lookup"><span data-stu-id="39996-279">16</span></span>                              |
| <span data-ttu-id="39996-280">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="39996-280">Search-Flags</span></span>           | <span data-ttu-id="39996-281">0x00000000</span><span class="sxs-lookup"><span data-stu-id="39996-281">0x00000000</span></span>                      |
| <span data-ttu-id="39996-282">System-Flags</span><span class="sxs-lookup"><span data-stu-id="39996-282">System-Flags</span></span>           | <span data-ttu-id="39996-283">0x00000010</span><span class="sxs-lookup"><span data-stu-id="39996-283">0x00000010</span></span>                      |
| <span data-ttu-id="39996-284">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="39996-284">Classes used in</span></span>        | [<span data-ttu-id="39996-285">**In alto**</span><span class="sxs-lookup"><span data-stu-id="39996-285">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="39996-286">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="39996-286">Windows Server 2012</span></span>



| <span data-ttu-id="39996-287">Voce</span><span class="sxs-lookup"><span data-stu-id="39996-287">Entry</span></span> | <span data-ttu-id="39996-288">Valore</span><span class="sxs-lookup"><span data-stu-id="39996-288">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="39996-289">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="39996-289">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="39996-290">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="39996-290">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="39996-291">System-Only</span><span class="sxs-lookup"><span data-stu-id="39996-291">System-Only</span></span>            | <span data-ttu-id="39996-292">Falso</span><span class="sxs-lookup"><span data-stu-id="39996-292">False</span></span>                           |
| <span data-ttu-id="39996-293">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="39996-293">Is-Single-Valued</span></span>       | <span data-ttu-id="39996-294">Falso</span><span class="sxs-lookup"><span data-stu-id="39996-294">False</span></span>                           |
| <span data-ttu-id="39996-295">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="39996-295">Is Indexed</span></span>             | <span data-ttu-id="39996-296">Falso</span><span class="sxs-lookup"><span data-stu-id="39996-296">False</span></span>                           |
| <span data-ttu-id="39996-297">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="39996-297">In Global Catalog</span></span>      | <span data-ttu-id="39996-298">Falso</span><span class="sxs-lookup"><span data-stu-id="39996-298">False</span></span>                           |
| <span data-ttu-id="39996-299">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="39996-299">NT-Security-Descriptor</span></span> | <span data-ttu-id="39996-300">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="39996-300">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="39996-301">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="39996-301">Range-Lower</span></span>            | <span data-ttu-id="39996-302">16</span><span class="sxs-lookup"><span data-stu-id="39996-302">16</span></span>                              |
| <span data-ttu-id="39996-303">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="39996-303">Range-Upper</span></span>            | <span data-ttu-id="39996-304">16</span><span class="sxs-lookup"><span data-stu-id="39996-304">16</span></span>                              |
| <span data-ttu-id="39996-305">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="39996-305">Search-Flags</span></span>           | <span data-ttu-id="39996-306">0x00000000</span><span class="sxs-lookup"><span data-stu-id="39996-306">0x00000000</span></span>                      |
| <span data-ttu-id="39996-307">System-Flags</span><span class="sxs-lookup"><span data-stu-id="39996-307">System-Flags</span></span>           | <span data-ttu-id="39996-308">0x00000010</span><span class="sxs-lookup"><span data-stu-id="39996-308">0x00000010</span></span>                      |
| <span data-ttu-id="39996-309">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="39996-309">Classes used in</span></span>        | [<span data-ttu-id="39996-310">**In alto**</span><span class="sxs-lookup"><span data-stu-id="39996-310">**Top**</span></span>](c-top.md)<br/> |



 

 





