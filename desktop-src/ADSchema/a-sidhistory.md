---
title: Attributo SID-History
description: Contiene i SID precedenti utilizzati per l'oggetto se l'oggetto è stato spostato da un altro dominio.
ms.assetid: d738002b-fc05-4c60-aaf9-b83be61ed5a9
ms.tgt_platform: multiple
keywords:
- Schema AD SID-History attribute
- Schema AD dell'attributo sIDHistory
topic_type:
- apiref
api_name:
- SID-History
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16474a6463fc99e7ed2c1d2b1a2cdbf6ea9b6614
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104479921"
---
# <a name="sid-history-attribute"></a><span data-ttu-id="690da-105">Attributo SID-History</span><span class="sxs-lookup"><span data-stu-id="690da-105">SID-History attribute</span></span>

<span data-ttu-id="690da-106">Contiene i SID precedenti utilizzati per l'oggetto se l'oggetto è stato spostato da un altro dominio.</span><span class="sxs-lookup"><span data-stu-id="690da-106">Contains previous SIDs used for the object if the object was moved from another domain.</span></span> <span data-ttu-id="690da-107">Ogni volta che un oggetto viene spostato da un dominio a un altro, viene creato un nuovo SID e il nuovo SID diventa objectSID.</span><span class="sxs-lookup"><span data-stu-id="690da-107">Whenever an object is moved from one domain to another, a new SID is created and that new SID becomes the objectSID.</span></span> <span data-ttu-id="690da-108">Il SID precedente viene aggiunto alla proprietà sIDHistory.</span><span class="sxs-lookup"><span data-stu-id="690da-108">The previous SID is added to the sIDHistory property.</span></span>



| <span data-ttu-id="690da-109">Voce</span><span class="sxs-lookup"><span data-stu-id="690da-109">Entry</span></span> | <span data-ttu-id="690da-110">Valore</span><span class="sxs-lookup"><span data-stu-id="690da-110">Value</span></span> |
|-------------------|------------------------------------------------|
| <span data-ttu-id="690da-111">CN</span><span class="sxs-lookup"><span data-stu-id="690da-111">CN</span></span>                | <span data-ttu-id="690da-112">SID-History</span><span class="sxs-lookup"><span data-stu-id="690da-112">SID-History</span></span>                                    |
| <span data-ttu-id="690da-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="690da-113">Ldap-Display-Name</span></span> | <span data-ttu-id="690da-114">sIDHistory</span><span class="sxs-lookup"><span data-stu-id="690da-114">sIDHistory</span></span>                                     |
| <span data-ttu-id="690da-115">Dimensione</span><span class="sxs-lookup"><span data-stu-id="690da-115">Size</span></span>              | \-                                             |
| <span data-ttu-id="690da-116">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="690da-116">Update Privilege</span></span>  | <span data-ttu-id="690da-117">Questo valore viene impostato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="690da-117">This value is set by the system.</span></span>               |
| <span data-ttu-id="690da-118">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="690da-118">Update Frequency</span></span>  | <span data-ttu-id="690da-119">Ogni volta che l'oggetto viene spostato in un nuovo dominio.</span><span class="sxs-lookup"><span data-stu-id="690da-119">Each time the object is moved to a new domain.</span></span> |
| <span data-ttu-id="690da-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="690da-120">Attribute-Id</span></span>      | <span data-ttu-id="690da-121">1.2.840.113556.1.4.609</span><span class="sxs-lookup"><span data-stu-id="690da-121">1.2.840.113556.1.4.609</span></span>                         |
| <span data-ttu-id="690da-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="690da-122">System-Id-Guid</span></span>    | <span data-ttu-id="690da-123">17eb4278-d167-11d0-b002-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="690da-123">17eb4278-d167-11d0-b002-0000f80367c1</span></span>           |
| <span data-ttu-id="690da-124">Sintassi</span><span class="sxs-lookup"><span data-stu-id="690da-124">Syntax</span></span>            | [<span data-ttu-id="690da-125">**Stringa (SID)**</span><span class="sxs-lookup"><span data-stu-id="690da-125">**String(Sid)**</span></span>](s-string-sid.md)            |



## <a name="implementations"></a><span data-ttu-id="690da-126">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="690da-126">Implementations</span></span>

-   [<span data-ttu-id="690da-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="690da-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="690da-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="690da-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="690da-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="690da-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="690da-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="690da-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="690da-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="690da-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="690da-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="690da-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="690da-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="690da-133">Windows 2000 Server</span></span>



| <span data-ttu-id="690da-134">Voce</span><span class="sxs-lookup"><span data-stu-id="690da-134">Entry</span></span> | <span data-ttu-id="690da-135">Valore</span><span class="sxs-lookup"><span data-stu-id="690da-135">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="690da-136">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="690da-136">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="690da-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="690da-137">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="690da-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="690da-138">System-Only</span></span>            | <span data-ttu-id="690da-139">Vero</span><span class="sxs-lookup"><span data-stu-id="690da-139">True</span></span>                                                         |
| <span data-ttu-id="690da-140">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="690da-140">Is-Single-Valued</span></span>       | <span data-ttu-id="690da-141">Falso</span><span class="sxs-lookup"><span data-stu-id="690da-141">False</span></span>                                                        |
| <span data-ttu-id="690da-142">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="690da-142">Is Indexed</span></span>             | <span data-ttu-id="690da-143">Vero</span><span class="sxs-lookup"><span data-stu-id="690da-143">True</span></span>                                                         |
| <span data-ttu-id="690da-144">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="690da-144">In Global Catalog</span></span>      | <span data-ttu-id="690da-145">Vero</span><span class="sxs-lookup"><span data-stu-id="690da-145">True</span></span>                                                         |
| <span data-ttu-id="690da-146">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="690da-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="690da-147">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="690da-147">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="690da-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="690da-148">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="690da-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="690da-149">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="690da-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="690da-150">Search-Flags</span></span>           | <span data-ttu-id="690da-151">0x00000001</span><span class="sxs-lookup"><span data-stu-id="690da-151">0x00000001</span></span>                                                   |
| <span data-ttu-id="690da-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="690da-152">System-Flags</span></span>           | <span data-ttu-id="690da-153">0x00000012</span><span class="sxs-lookup"><span data-stu-id="690da-153">0x00000012</span></span>                                                   |
| <span data-ttu-id="690da-154">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="690da-154">Classes used in</span></span>        | [<span data-ttu-id="690da-155">**Entità di sicurezza**</span><span class="sxs-lookup"><span data-stu-id="690da-155">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="690da-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="690da-156">Windows Server 2003</span></span>



| <span data-ttu-id="690da-157">Voce</span><span class="sxs-lookup"><span data-stu-id="690da-157">Entry</span></span> | <span data-ttu-id="690da-158">Valore</span><span class="sxs-lookup"><span data-stu-id="690da-158">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="690da-159">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="690da-159">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="690da-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="690da-160">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="690da-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="690da-161">System-Only</span></span>            | <span data-ttu-id="690da-162">Falso</span><span class="sxs-lookup"><span data-stu-id="690da-162">False</span></span>                                                        |
| <span data-ttu-id="690da-163">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="690da-163">Is-Single-Valued</span></span>       | <span data-ttu-id="690da-164">Falso</span><span class="sxs-lookup"><span data-stu-id="690da-164">False</span></span>                                                        |
| <span data-ttu-id="690da-165">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="690da-165">Is Indexed</span></span>             | <span data-ttu-id="690da-166">Vero</span><span class="sxs-lookup"><span data-stu-id="690da-166">True</span></span>                                                         |
| <span data-ttu-id="690da-167">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="690da-167">In Global Catalog</span></span>      | <span data-ttu-id="690da-168">Vero</span><span class="sxs-lookup"><span data-stu-id="690da-168">True</span></span>                                                         |
| <span data-ttu-id="690da-169">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="690da-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="690da-170">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="690da-170">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="690da-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="690da-171">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="690da-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="690da-172">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="690da-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="690da-173">Search-Flags</span></span>           | <span data-ttu-id="690da-174">0x00000001</span><span class="sxs-lookup"><span data-stu-id="690da-174">0x00000001</span></span>                                                   |
| <span data-ttu-id="690da-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="690da-175">System-Flags</span></span>           | <span data-ttu-id="690da-176">0x00000012</span><span class="sxs-lookup"><span data-stu-id="690da-176">0x00000012</span></span>                                                   |
| <span data-ttu-id="690da-177">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="690da-177">Classes used in</span></span>        | [<span data-ttu-id="690da-178">**Entità di sicurezza**</span><span class="sxs-lookup"><span data-stu-id="690da-178">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="690da-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="690da-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="690da-180">Voce</span><span class="sxs-lookup"><span data-stu-id="690da-180">Entry</span></span> | <span data-ttu-id="690da-181">Valore</span><span class="sxs-lookup"><span data-stu-id="690da-181">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="690da-182">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="690da-182">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="690da-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="690da-183">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="690da-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="690da-184">System-Only</span></span>            | <span data-ttu-id="690da-185">Falso</span><span class="sxs-lookup"><span data-stu-id="690da-185">False</span></span>                                                        |
| <span data-ttu-id="690da-186">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="690da-186">Is-Single-Valued</span></span>       | <span data-ttu-id="690da-187">Falso</span><span class="sxs-lookup"><span data-stu-id="690da-187">False</span></span>                                                        |
| <span data-ttu-id="690da-188">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="690da-188">Is Indexed</span></span>             | <span data-ttu-id="690da-189">Vero</span><span class="sxs-lookup"><span data-stu-id="690da-189">True</span></span>                                                         |
| <span data-ttu-id="690da-190">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="690da-190">In Global Catalog</span></span>      | <span data-ttu-id="690da-191">Vero</span><span class="sxs-lookup"><span data-stu-id="690da-191">True</span></span>                                                         |
| <span data-ttu-id="690da-192">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="690da-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="690da-193">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="690da-193">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="690da-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="690da-194">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="690da-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="690da-195">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="690da-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="690da-196">Search-Flags</span></span>           | <span data-ttu-id="690da-197">0x00000001</span><span class="sxs-lookup"><span data-stu-id="690da-197">0x00000001</span></span>                                                   |
| <span data-ttu-id="690da-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="690da-198">System-Flags</span></span>           | <span data-ttu-id="690da-199">0x00000012</span><span class="sxs-lookup"><span data-stu-id="690da-199">0x00000012</span></span>                                                   |
| <span data-ttu-id="690da-200">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="690da-200">Classes used in</span></span>        | [<span data-ttu-id="690da-201">**Entità di sicurezza**</span><span class="sxs-lookup"><span data-stu-id="690da-201">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="690da-202">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="690da-202">Windows Server 2008</span></span>



| <span data-ttu-id="690da-203">Voce</span><span class="sxs-lookup"><span data-stu-id="690da-203">Entry</span></span> | <span data-ttu-id="690da-204">Valore</span><span class="sxs-lookup"><span data-stu-id="690da-204">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="690da-205">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="690da-205">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="690da-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="690da-206">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="690da-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="690da-207">System-Only</span></span>            | <span data-ttu-id="690da-208">Falso</span><span class="sxs-lookup"><span data-stu-id="690da-208">False</span></span>                                                        |
| <span data-ttu-id="690da-209">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="690da-209">Is-Single-Valued</span></span>       | <span data-ttu-id="690da-210">Falso</span><span class="sxs-lookup"><span data-stu-id="690da-210">False</span></span>                                                        |
| <span data-ttu-id="690da-211">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="690da-211">Is Indexed</span></span>             | <span data-ttu-id="690da-212">Vero</span><span class="sxs-lookup"><span data-stu-id="690da-212">True</span></span>                                                         |
| <span data-ttu-id="690da-213">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="690da-213">In Global Catalog</span></span>      | <span data-ttu-id="690da-214">Vero</span><span class="sxs-lookup"><span data-stu-id="690da-214">True</span></span>                                                         |
| <span data-ttu-id="690da-215">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="690da-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="690da-216">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="690da-216">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="690da-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="690da-217">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="690da-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="690da-218">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="690da-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="690da-219">Search-Flags</span></span>           | <span data-ttu-id="690da-220">0x00000001</span><span class="sxs-lookup"><span data-stu-id="690da-220">0x00000001</span></span>                                                   |
| <span data-ttu-id="690da-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="690da-221">System-Flags</span></span>           | <span data-ttu-id="690da-222">0x00000012</span><span class="sxs-lookup"><span data-stu-id="690da-222">0x00000012</span></span>                                                   |
| <span data-ttu-id="690da-223">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="690da-223">Classes used in</span></span>        | [<span data-ttu-id="690da-224">**Entità di sicurezza**</span><span class="sxs-lookup"><span data-stu-id="690da-224">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="690da-225">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="690da-225">Windows Server 2008 R2</span></span>



| <span data-ttu-id="690da-226">Voce</span><span class="sxs-lookup"><span data-stu-id="690da-226">Entry</span></span> | <span data-ttu-id="690da-227">Valore</span><span class="sxs-lookup"><span data-stu-id="690da-227">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="690da-228">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="690da-228">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="690da-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="690da-229">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="690da-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="690da-230">System-Only</span></span>            | <span data-ttu-id="690da-231">Falso</span><span class="sxs-lookup"><span data-stu-id="690da-231">False</span></span>                                                        |
| <span data-ttu-id="690da-232">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="690da-232">Is-Single-Valued</span></span>       | <span data-ttu-id="690da-233">Falso</span><span class="sxs-lookup"><span data-stu-id="690da-233">False</span></span>                                                        |
| <span data-ttu-id="690da-234">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="690da-234">Is Indexed</span></span>             | <span data-ttu-id="690da-235">Vero</span><span class="sxs-lookup"><span data-stu-id="690da-235">True</span></span>                                                         |
| <span data-ttu-id="690da-236">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="690da-236">In Global Catalog</span></span>      | <span data-ttu-id="690da-237">Vero</span><span class="sxs-lookup"><span data-stu-id="690da-237">True</span></span>                                                         |
| <span data-ttu-id="690da-238">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="690da-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="690da-239">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="690da-239">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="690da-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="690da-240">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="690da-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="690da-241">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="690da-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="690da-242">Search-Flags</span></span>           | <span data-ttu-id="690da-243">0x00000001</span><span class="sxs-lookup"><span data-stu-id="690da-243">0x00000001</span></span>                                                   |
| <span data-ttu-id="690da-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="690da-244">System-Flags</span></span>           | <span data-ttu-id="690da-245">0x00000012</span><span class="sxs-lookup"><span data-stu-id="690da-245">0x00000012</span></span>                                                   |
| <span data-ttu-id="690da-246">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="690da-246">Classes used in</span></span>        | [<span data-ttu-id="690da-247">**Entità di sicurezza**</span><span class="sxs-lookup"><span data-stu-id="690da-247">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="690da-248">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="690da-248">Windows Server 2012</span></span>



| <span data-ttu-id="690da-249">Voce</span><span class="sxs-lookup"><span data-stu-id="690da-249">Entry</span></span> | <span data-ttu-id="690da-250">Valore</span><span class="sxs-lookup"><span data-stu-id="690da-250">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="690da-251">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="690da-251">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="690da-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="690da-252">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="690da-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="690da-253">System-Only</span></span>            | <span data-ttu-id="690da-254">Falso</span><span class="sxs-lookup"><span data-stu-id="690da-254">False</span></span>                                                        |
| <span data-ttu-id="690da-255">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="690da-255">Is-Single-Valued</span></span>       | <span data-ttu-id="690da-256">Falso</span><span class="sxs-lookup"><span data-stu-id="690da-256">False</span></span>                                                        |
| <span data-ttu-id="690da-257">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="690da-257">Is Indexed</span></span>             | <span data-ttu-id="690da-258">Vero</span><span class="sxs-lookup"><span data-stu-id="690da-258">True</span></span>                                                         |
| <span data-ttu-id="690da-259">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="690da-259">In Global Catalog</span></span>      | <span data-ttu-id="690da-260">Vero</span><span class="sxs-lookup"><span data-stu-id="690da-260">True</span></span>                                                         |
| <span data-ttu-id="690da-261">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="690da-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="690da-262">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="690da-262">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="690da-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="690da-263">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="690da-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="690da-264">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="690da-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="690da-265">Search-Flags</span></span>           | <span data-ttu-id="690da-266">0x00000001</span><span class="sxs-lookup"><span data-stu-id="690da-266">0x00000001</span></span>                                                   |
| <span data-ttu-id="690da-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="690da-267">System-Flags</span></span>           | <span data-ttu-id="690da-268">0x00000012</span><span class="sxs-lookup"><span data-stu-id="690da-268">0x00000012</span></span>                                                   |
| <span data-ttu-id="690da-269">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="690da-269">Classes used in</span></span>        | [<span data-ttu-id="690da-270">**Entità di sicurezza**</span><span class="sxs-lookup"><span data-stu-id="690da-270">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



 

 





