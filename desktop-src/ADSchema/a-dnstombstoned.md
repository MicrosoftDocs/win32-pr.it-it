---
title: Attributo DNS-Tombstoned
description: True se l'oggetto è stato contrassegnato per la rimozione definitiva. Questo attributo esiste per semplificare e velocizzare la ricerca dei record contrassegnati per la rimozione definitiva. Gli oggetti contrassegnati per la rimozione definitiva sono oggetti eliminati, ma non ancora rimossi dalla directory.
ms.assetid: d876a6d7-d5bc-4fe2-af03-1fff3381708f
ms.tgt_platform: multiple
keywords:
- Schema AD DNS-Tombstoned attribute
- Schema AD dell'attributo dNSTombstoned
topic_type:
- apiref
api_name:
- DNS-Tombstoned
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0dba61706861b808f28d7f6874a9bfd93d4152c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103874993"
---
# <a name="dns-tombstoned-attribute"></a><span data-ttu-id="c3b43-107">Attributo DNS-Tombstoned</span><span class="sxs-lookup"><span data-stu-id="c3b43-107">DNS-Tombstoned attribute</span></span>

<span data-ttu-id="c3b43-108">True se l'oggetto è stato contrassegnato per la rimozione definitiva.</span><span class="sxs-lookup"><span data-stu-id="c3b43-108">True if this object has been tombstoned.</span></span> <span data-ttu-id="c3b43-109">Questo attributo esiste per semplificare e velocizzare la ricerca dei record contrassegnati per la rimozione definitiva.</span><span class="sxs-lookup"><span data-stu-id="c3b43-109">This attribute exists to make searching for tombstoned records easier and faster.</span></span> <span data-ttu-id="c3b43-110">Gli oggetti contrassegnati per la rimozione definitiva sono oggetti eliminati, ma non ancora rimossi dalla directory.</span><span class="sxs-lookup"><span data-stu-id="c3b43-110">Tombstoned objects are objects that have been deleted but not yet removed from the directory.</span></span>



| <span data-ttu-id="c3b43-111">Voce</span><span class="sxs-lookup"><span data-stu-id="c3b43-111">Entry</span></span> | <span data-ttu-id="c3b43-112">Valore</span><span class="sxs-lookup"><span data-stu-id="c3b43-112">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="c3b43-113">CN</span><span class="sxs-lookup"><span data-stu-id="c3b43-113">CN</span></span>                | <span data-ttu-id="c3b43-114">DNS-Tombstoned</span><span class="sxs-lookup"><span data-stu-id="c3b43-114">DNS-Tombstoned</span></span>                       |
| <span data-ttu-id="c3b43-115">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="c3b43-115">Ldap-Display-Name</span></span> | <span data-ttu-id="c3b43-116">dNSTombstoned</span><span class="sxs-lookup"><span data-stu-id="c3b43-116">dNSTombstoned</span></span>                        |
| <span data-ttu-id="c3b43-117">Dimensione</span><span class="sxs-lookup"><span data-stu-id="c3b43-117">Size</span></span>              | <span data-ttu-id="c3b43-118">4 byte</span><span class="sxs-lookup"><span data-stu-id="c3b43-118">4 bytes</span></span>                              |
| <span data-ttu-id="c3b43-119">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="c3b43-119">Update Privilege</span></span>  | <span data-ttu-id="c3b43-120">Questo valore viene impostato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="c3b43-120">This value is set by the system.</span></span>     |
| <span data-ttu-id="c3b43-121">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="c3b43-121">Update Frequency</span></span>  | <span data-ttu-id="c3b43-122">Ogni volta che un oggetto viene eliminato.</span><span class="sxs-lookup"><span data-stu-id="c3b43-122">Whenever an object is deleted.</span></span>       |
| <span data-ttu-id="c3b43-123">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c3b43-123">Attribute-Id</span></span>      | <span data-ttu-id="c3b43-124">1.2.840.113556.1.4.1414</span><span class="sxs-lookup"><span data-stu-id="c3b43-124">1.2.840.113556.1.4.1414</span></span>              |
| <span data-ttu-id="c3b43-125">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="c3b43-125">System-Id-Guid</span></span>    | <span data-ttu-id="c3b43-126">d5eb2eb7-be4e-463b-a214-634a44d7392e</span><span class="sxs-lookup"><span data-stu-id="c3b43-126">d5eb2eb7-be4e-463b-a214-634a44d7392e</span></span> |
| <span data-ttu-id="c3b43-127">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c3b43-127">Syntax</span></span>            | [<span data-ttu-id="c3b43-128">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="c3b43-128">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="c3b43-129">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="c3b43-129">Implementations</span></span>

-   [<span data-ttu-id="c3b43-130">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="c3b43-130">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="c3b43-131">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c3b43-131">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c3b43-132">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c3b43-132">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c3b43-133">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c3b43-133">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c3b43-134">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c3b43-134">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c3b43-135">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c3b43-135">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="c3b43-136">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c3b43-136">Windows 2000 Server</span></span>



| <span data-ttu-id="c3b43-137">Voce</span><span class="sxs-lookup"><span data-stu-id="c3b43-137">Entry</span></span> | <span data-ttu-id="c3b43-138">Valore</span><span class="sxs-lookup"><span data-stu-id="c3b43-138">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="c3b43-139">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="c3b43-139">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="c3b43-140">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c3b43-140">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="c3b43-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="c3b43-141">System-Only</span></span>            | <span data-ttu-id="c3b43-142">Falso</span><span class="sxs-lookup"><span data-stu-id="c3b43-142">False</span></span>                                    |
| <span data-ttu-id="c3b43-143">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="c3b43-143">Is-Single-Valued</span></span>       | <span data-ttu-id="c3b43-144">Vero</span><span class="sxs-lookup"><span data-stu-id="c3b43-144">True</span></span>                                     |
| <span data-ttu-id="c3b43-145">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="c3b43-145">Is Indexed</span></span>             | <span data-ttu-id="c3b43-146">Vero</span><span class="sxs-lookup"><span data-stu-id="c3b43-146">True</span></span>                                     |
| <span data-ttu-id="c3b43-147">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="c3b43-147">In Global Catalog</span></span>      | <span data-ttu-id="c3b43-148">Falso</span><span class="sxs-lookup"><span data-stu-id="c3b43-148">False</span></span>                                    |
| <span data-ttu-id="c3b43-149">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="c3b43-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="c3b43-150">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="c3b43-150">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="c3b43-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c3b43-151">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="c3b43-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c3b43-152">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="c3b43-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c3b43-153">Search-Flags</span></span>           | <span data-ttu-id="c3b43-154">0x00000001</span><span class="sxs-lookup"><span data-stu-id="c3b43-154">0x00000001</span></span>                               |
| <span data-ttu-id="c3b43-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c3b43-155">System-Flags</span></span>           | <span data-ttu-id="c3b43-156">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c3b43-156">0x00000010</span></span>                               |
| <span data-ttu-id="c3b43-157">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="c3b43-157">Classes used in</span></span>        | [<span data-ttu-id="c3b43-158">**DNS-nodo**</span><span class="sxs-lookup"><span data-stu-id="c3b43-158">**Dns-Node**</span></span>](c-dnsnode.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="c3b43-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c3b43-159">Windows Server 2003</span></span>



| <span data-ttu-id="c3b43-160">Voce</span><span class="sxs-lookup"><span data-stu-id="c3b43-160">Entry</span></span> | <span data-ttu-id="c3b43-161">Valore</span><span class="sxs-lookup"><span data-stu-id="c3b43-161">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="c3b43-162">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="c3b43-162">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="c3b43-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c3b43-163">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="c3b43-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="c3b43-164">System-Only</span></span>            | <span data-ttu-id="c3b43-165">Falso</span><span class="sxs-lookup"><span data-stu-id="c3b43-165">False</span></span>                                    |
| <span data-ttu-id="c3b43-166">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="c3b43-166">Is-Single-Valued</span></span>       | <span data-ttu-id="c3b43-167">Vero</span><span class="sxs-lookup"><span data-stu-id="c3b43-167">True</span></span>                                     |
| <span data-ttu-id="c3b43-168">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="c3b43-168">Is Indexed</span></span>             | <span data-ttu-id="c3b43-169">Vero</span><span class="sxs-lookup"><span data-stu-id="c3b43-169">True</span></span>                                     |
| <span data-ttu-id="c3b43-170">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="c3b43-170">In Global Catalog</span></span>      | <span data-ttu-id="c3b43-171">Falso</span><span class="sxs-lookup"><span data-stu-id="c3b43-171">False</span></span>                                    |
| <span data-ttu-id="c3b43-172">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="c3b43-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="c3b43-173">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="c3b43-173">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="c3b43-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c3b43-174">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="c3b43-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c3b43-175">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="c3b43-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c3b43-176">Search-Flags</span></span>           | <span data-ttu-id="c3b43-177">0x00000001</span><span class="sxs-lookup"><span data-stu-id="c3b43-177">0x00000001</span></span>                               |
| <span data-ttu-id="c3b43-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c3b43-178">System-Flags</span></span>           | <span data-ttu-id="c3b43-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c3b43-179">0x00000010</span></span>                               |
| <span data-ttu-id="c3b43-180">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="c3b43-180">Classes used in</span></span>        | [<span data-ttu-id="c3b43-181">**DNS-nodo**</span><span class="sxs-lookup"><span data-stu-id="c3b43-181">**Dns-Node**</span></span>](c-dnsnode.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c3b43-182">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c3b43-182">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c3b43-183">Voce</span><span class="sxs-lookup"><span data-stu-id="c3b43-183">Entry</span></span> | <span data-ttu-id="c3b43-184">Valore</span><span class="sxs-lookup"><span data-stu-id="c3b43-184">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="c3b43-185">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="c3b43-185">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="c3b43-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c3b43-186">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="c3b43-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="c3b43-187">System-Only</span></span>            | <span data-ttu-id="c3b43-188">Falso</span><span class="sxs-lookup"><span data-stu-id="c3b43-188">False</span></span>                                    |
| <span data-ttu-id="c3b43-189">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="c3b43-189">Is-Single-Valued</span></span>       | <span data-ttu-id="c3b43-190">Vero</span><span class="sxs-lookup"><span data-stu-id="c3b43-190">True</span></span>                                     |
| <span data-ttu-id="c3b43-191">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="c3b43-191">Is Indexed</span></span>             | <span data-ttu-id="c3b43-192">Vero</span><span class="sxs-lookup"><span data-stu-id="c3b43-192">True</span></span>                                     |
| <span data-ttu-id="c3b43-193">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="c3b43-193">In Global Catalog</span></span>      | <span data-ttu-id="c3b43-194">Falso</span><span class="sxs-lookup"><span data-stu-id="c3b43-194">False</span></span>                                    |
| <span data-ttu-id="c3b43-195">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="c3b43-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="c3b43-196">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="c3b43-196">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="c3b43-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c3b43-197">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="c3b43-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c3b43-198">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="c3b43-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c3b43-199">Search-Flags</span></span>           | <span data-ttu-id="c3b43-200">0x00000001</span><span class="sxs-lookup"><span data-stu-id="c3b43-200">0x00000001</span></span>                               |
| <span data-ttu-id="c3b43-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c3b43-201">System-Flags</span></span>           | <span data-ttu-id="c3b43-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c3b43-202">0x00000010</span></span>                               |
| <span data-ttu-id="c3b43-203">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="c3b43-203">Classes used in</span></span>        | [<span data-ttu-id="c3b43-204">**DNS-nodo**</span><span class="sxs-lookup"><span data-stu-id="c3b43-204">**Dns-Node**</span></span>](c-dnsnode.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c3b43-205">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c3b43-205">Windows Server 2008</span></span>



| <span data-ttu-id="c3b43-206">Voce</span><span class="sxs-lookup"><span data-stu-id="c3b43-206">Entry</span></span> | <span data-ttu-id="c3b43-207">Valore</span><span class="sxs-lookup"><span data-stu-id="c3b43-207">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="c3b43-208">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="c3b43-208">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="c3b43-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c3b43-209">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="c3b43-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="c3b43-210">System-Only</span></span>            | <span data-ttu-id="c3b43-211">Falso</span><span class="sxs-lookup"><span data-stu-id="c3b43-211">False</span></span>                                    |
| <span data-ttu-id="c3b43-212">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="c3b43-212">Is-Single-Valued</span></span>       | <span data-ttu-id="c3b43-213">Vero</span><span class="sxs-lookup"><span data-stu-id="c3b43-213">True</span></span>                                     |
| <span data-ttu-id="c3b43-214">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="c3b43-214">Is Indexed</span></span>             | <span data-ttu-id="c3b43-215">Vero</span><span class="sxs-lookup"><span data-stu-id="c3b43-215">True</span></span>                                     |
| <span data-ttu-id="c3b43-216">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="c3b43-216">In Global Catalog</span></span>      | <span data-ttu-id="c3b43-217">Falso</span><span class="sxs-lookup"><span data-stu-id="c3b43-217">False</span></span>                                    |
| <span data-ttu-id="c3b43-218">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="c3b43-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="c3b43-219">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="c3b43-219">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="c3b43-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c3b43-220">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="c3b43-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c3b43-221">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="c3b43-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c3b43-222">Search-Flags</span></span>           | <span data-ttu-id="c3b43-223">0x00000001</span><span class="sxs-lookup"><span data-stu-id="c3b43-223">0x00000001</span></span>                               |
| <span data-ttu-id="c3b43-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c3b43-224">System-Flags</span></span>           | <span data-ttu-id="c3b43-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c3b43-225">0x00000010</span></span>                               |
| <span data-ttu-id="c3b43-226">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="c3b43-226">Classes used in</span></span>        | [<span data-ttu-id="c3b43-227">**DNS-nodo**</span><span class="sxs-lookup"><span data-stu-id="c3b43-227">**Dns-Node**</span></span>](c-dnsnode.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c3b43-228">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c3b43-228">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c3b43-229">Voce</span><span class="sxs-lookup"><span data-stu-id="c3b43-229">Entry</span></span> | <span data-ttu-id="c3b43-230">Valore</span><span class="sxs-lookup"><span data-stu-id="c3b43-230">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="c3b43-231">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="c3b43-231">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="c3b43-232">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c3b43-232">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="c3b43-233">System-Only</span><span class="sxs-lookup"><span data-stu-id="c3b43-233">System-Only</span></span>            | <span data-ttu-id="c3b43-234">Falso</span><span class="sxs-lookup"><span data-stu-id="c3b43-234">False</span></span>                                    |
| <span data-ttu-id="c3b43-235">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="c3b43-235">Is-Single-Valued</span></span>       | <span data-ttu-id="c3b43-236">Vero</span><span class="sxs-lookup"><span data-stu-id="c3b43-236">True</span></span>                                     |
| <span data-ttu-id="c3b43-237">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="c3b43-237">Is Indexed</span></span>             | <span data-ttu-id="c3b43-238">Vero</span><span class="sxs-lookup"><span data-stu-id="c3b43-238">True</span></span>                                     |
| <span data-ttu-id="c3b43-239">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="c3b43-239">In Global Catalog</span></span>      | <span data-ttu-id="c3b43-240">Falso</span><span class="sxs-lookup"><span data-stu-id="c3b43-240">False</span></span>                                    |
| <span data-ttu-id="c3b43-241">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="c3b43-241">NT-Security-Descriptor</span></span> | <span data-ttu-id="c3b43-242">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="c3b43-242">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="c3b43-243">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c3b43-243">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="c3b43-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c3b43-244">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="c3b43-245">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c3b43-245">Search-Flags</span></span>           | <span data-ttu-id="c3b43-246">0x00000001</span><span class="sxs-lookup"><span data-stu-id="c3b43-246">0x00000001</span></span>                               |
| <span data-ttu-id="c3b43-247">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c3b43-247">System-Flags</span></span>           | <span data-ttu-id="c3b43-248">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c3b43-248">0x00000010</span></span>                               |
| <span data-ttu-id="c3b43-249">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="c3b43-249">Classes used in</span></span>        | [<span data-ttu-id="c3b43-250">**DNS-nodo**</span><span class="sxs-lookup"><span data-stu-id="c3b43-250">**Dns-Node**</span></span>](c-dnsnode.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c3b43-251">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c3b43-251">Windows Server 2012</span></span>



| <span data-ttu-id="c3b43-252">Voce</span><span class="sxs-lookup"><span data-stu-id="c3b43-252">Entry</span></span> | <span data-ttu-id="c3b43-253">Valore</span><span class="sxs-lookup"><span data-stu-id="c3b43-253">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="c3b43-254">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="c3b43-254">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="c3b43-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c3b43-255">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="c3b43-256">System-Only</span><span class="sxs-lookup"><span data-stu-id="c3b43-256">System-Only</span></span>            | <span data-ttu-id="c3b43-257">Falso</span><span class="sxs-lookup"><span data-stu-id="c3b43-257">False</span></span>                                    |
| <span data-ttu-id="c3b43-258">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="c3b43-258">Is-Single-Valued</span></span>       | <span data-ttu-id="c3b43-259">Vero</span><span class="sxs-lookup"><span data-stu-id="c3b43-259">True</span></span>                                     |
| <span data-ttu-id="c3b43-260">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="c3b43-260">Is Indexed</span></span>             | <span data-ttu-id="c3b43-261">Vero</span><span class="sxs-lookup"><span data-stu-id="c3b43-261">True</span></span>                                     |
| <span data-ttu-id="c3b43-262">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="c3b43-262">In Global Catalog</span></span>      | <span data-ttu-id="c3b43-263">Falso</span><span class="sxs-lookup"><span data-stu-id="c3b43-263">False</span></span>                                    |
| <span data-ttu-id="c3b43-264">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="c3b43-264">NT-Security-Descriptor</span></span> | <span data-ttu-id="c3b43-265">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="c3b43-265">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="c3b43-266">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c3b43-266">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="c3b43-267">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c3b43-267">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="c3b43-268">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c3b43-268">Search-Flags</span></span>           | <span data-ttu-id="c3b43-269">0x00000001</span><span class="sxs-lookup"><span data-stu-id="c3b43-269">0x00000001</span></span>                               |
| <span data-ttu-id="c3b43-270">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c3b43-270">System-Flags</span></span>           | <span data-ttu-id="c3b43-271">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c3b43-271">0x00000010</span></span>                               |
| <span data-ttu-id="c3b43-272">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="c3b43-272">Classes used in</span></span>        | [<span data-ttu-id="c3b43-273">**DNS-nodo**</span><span class="sxs-lookup"><span data-stu-id="c3b43-273">**Dns-Node**</span></span>](c-dnsnode.md)<br/> |



 

 





