---
title: System-classe ausiliaria-attributo
description: Elenco di classi ausiliarie che non possono essere modificate dall'utente.
ms.assetid: 6d629925-7321-4f3a-bf4c-4adf0d33c946
ms.tgt_platform: multiple
keywords:
- Schema di AD Attribute di classe ausiliario di sistema
- Schema AD dell'attributo systemAuxiliaryClass
topic_type:
- apiref
api_name:
- System-Auxiliary-Class
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebe70899ba2bda8fe98b38228cb661e7a773ec1d
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "106303119"
---
# <a name="system-auxiliary-class-attribute"></a><span data-ttu-id="7c447-105">System-classe ausiliaria-attributo</span><span class="sxs-lookup"><span data-stu-id="7c447-105">System-Auxiliary-Class attribute</span></span>

<span data-ttu-id="7c447-106">Elenco di classi ausiliarie che non possono essere modificate dall'utente.</span><span class="sxs-lookup"><span data-stu-id="7c447-106">A list of auxiliary classes that cannot be modified by the user.</span></span>



| <span data-ttu-id="7c447-107">Voce</span><span class="sxs-lookup"><span data-stu-id="7c447-107">Entry</span></span> | <span data-ttu-id="7c447-108">Valore</span><span class="sxs-lookup"><span data-stu-id="7c447-108">Value</span></span> |
|-------------------|--------------------------------------------------------------------|
| <span data-ttu-id="7c447-109">CN</span><span class="sxs-lookup"><span data-stu-id="7c447-109">CN</span></span>                | <span data-ttu-id="7c447-110">System-ausiliari-classe</span><span class="sxs-lookup"><span data-stu-id="7c447-110">System-Auxiliary-Class</span></span>                                             |
| <span data-ttu-id="7c447-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="7c447-111">Ldap-Display-Name</span></span> | <span data-ttu-id="7c447-112">systemAuxiliaryClass</span><span class="sxs-lookup"><span data-stu-id="7c447-112">systemAuxiliaryClass</span></span>                                               |
| <span data-ttu-id="7c447-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="7c447-113">Size</span></span>              | \-                                                                 |
| <span data-ttu-id="7c447-114">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="7c447-114">Update Privilege</span></span>  | <span data-ttu-id="7c447-115">Amministratore schema</span><span class="sxs-lookup"><span data-stu-id="7c447-115">Schema administrator</span></span>                                               |
| <span data-ttu-id="7c447-116">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="7c447-116">Update Frequency</span></span>  | <span data-ttu-id="7c447-117">Quando viene creata la classe o viene aggiunta una nuova classe ausiliaria.</span><span class="sxs-lookup"><span data-stu-id="7c447-117">When the class is created or a new auxiliary class is added to it.</span></span> |
| <span data-ttu-id="7c447-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="7c447-118">Attribute-Id</span></span>      | <span data-ttu-id="7c447-119">1.2.840.113556.1.4.198</span><span class="sxs-lookup"><span data-stu-id="7c447-119">1.2.840.113556.1.4.198</span></span>                                             |
| <span data-ttu-id="7c447-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="7c447-120">System-Id-Guid</span></span>    | <span data-ttu-id="7c447-121">bf967a43-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="7c447-121">bf967a43-0de6-11d0-a285-00aa003049e2</span></span>                               |
| <span data-ttu-id="7c447-122">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7c447-122">Syntax</span></span>            | [<span data-ttu-id="7c447-123">**String(Object-Identifier)**</span><span class="sxs-lookup"><span data-stu-id="7c447-123">**String(Object-Identifier)**</span></span>](s-string-object-identifier.md)    |



## <a name="implementations"></a><span data-ttu-id="7c447-124">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="7c447-124">Implementations</span></span>

-   [<span data-ttu-id="7c447-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="7c447-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="7c447-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="7c447-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="7c447-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="7c447-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="7c447-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="7c447-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="7c447-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="7c447-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="7c447-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="7c447-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="7c447-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="7c447-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="7c447-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7c447-132">Windows 2000 Server</span></span>



| <span data-ttu-id="7c447-133">Voce</span><span class="sxs-lookup"><span data-stu-id="7c447-133">Entry</span></span> | <span data-ttu-id="7c447-134">Valore</span><span class="sxs-lookup"><span data-stu-id="7c447-134">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="7c447-135">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="7c447-135">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="7c447-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7c447-136">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="7c447-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="7c447-137">System-Only</span></span>            | <span data-ttu-id="7c447-138">Vero</span><span class="sxs-lookup"><span data-stu-id="7c447-138">True</span></span>                                             |
| <span data-ttu-id="7c447-139">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="7c447-139">Is-Single-Valued</span></span>       | <span data-ttu-id="7c447-140">Falso</span><span class="sxs-lookup"><span data-stu-id="7c447-140">False</span></span>                                            |
| <span data-ttu-id="7c447-141">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="7c447-141">Is Indexed</span></span>             | <span data-ttu-id="7c447-142">Falso</span><span class="sxs-lookup"><span data-stu-id="7c447-142">False</span></span>                                            |
| <span data-ttu-id="7c447-143">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="7c447-143">In Global Catalog</span></span>      | <span data-ttu-id="7c447-144">Falso</span><span class="sxs-lookup"><span data-stu-id="7c447-144">False</span></span>                                            |
| <span data-ttu-id="7c447-145">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="7c447-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="7c447-146">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="7c447-146">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="7c447-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7c447-147">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="7c447-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7c447-148">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="7c447-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7c447-149">Search-Flags</span></span>           | <span data-ttu-id="7c447-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7c447-150">0x00000000</span></span>                                       |
| <span data-ttu-id="7c447-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7c447-151">System-Flags</span></span>           | <span data-ttu-id="7c447-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7c447-152">0x00000010</span></span>                                       |
| <span data-ttu-id="7c447-153">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="7c447-153">Classes used in</span></span>        | [<span data-ttu-id="7c447-154">**Classe-schema**</span><span class="sxs-lookup"><span data-stu-id="7c447-154">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="7c447-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7c447-155">Windows Server 2003</span></span>



| <span data-ttu-id="7c447-156">Voce</span><span class="sxs-lookup"><span data-stu-id="7c447-156">Entry</span></span> | <span data-ttu-id="7c447-157">Valore</span><span class="sxs-lookup"><span data-stu-id="7c447-157">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="7c447-158">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="7c447-158">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="7c447-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7c447-159">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="7c447-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="7c447-160">System-Only</span></span>            | <span data-ttu-id="7c447-161">Vero</span><span class="sxs-lookup"><span data-stu-id="7c447-161">True</span></span>                                             |
| <span data-ttu-id="7c447-162">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="7c447-162">Is-Single-Valued</span></span>       | <span data-ttu-id="7c447-163">Falso</span><span class="sxs-lookup"><span data-stu-id="7c447-163">False</span></span>                                            |
| <span data-ttu-id="7c447-164">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="7c447-164">Is Indexed</span></span>             | <span data-ttu-id="7c447-165">Falso</span><span class="sxs-lookup"><span data-stu-id="7c447-165">False</span></span>                                            |
| <span data-ttu-id="7c447-166">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="7c447-166">In Global Catalog</span></span>      | <span data-ttu-id="7c447-167">Falso</span><span class="sxs-lookup"><span data-stu-id="7c447-167">False</span></span>                                            |
| <span data-ttu-id="7c447-168">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="7c447-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="7c447-169">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="7c447-169">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="7c447-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7c447-170">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="7c447-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7c447-171">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="7c447-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7c447-172">Search-Flags</span></span>           | <span data-ttu-id="7c447-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7c447-173">0x00000000</span></span>                                       |
| <span data-ttu-id="7c447-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7c447-174">System-Flags</span></span>           | <span data-ttu-id="7c447-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7c447-175">0x00000010</span></span>                                       |
| <span data-ttu-id="7c447-176">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="7c447-176">Classes used in</span></span>        | [<span data-ttu-id="7c447-177">**Classe-schema**</span><span class="sxs-lookup"><span data-stu-id="7c447-177">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="7c447-178">ADAM</span><span class="sxs-lookup"><span data-stu-id="7c447-178">ADAM</span></span>



| <span data-ttu-id="7c447-179">Voce</span><span class="sxs-lookup"><span data-stu-id="7c447-179">Entry</span></span> | <span data-ttu-id="7c447-180">Valore</span><span class="sxs-lookup"><span data-stu-id="7c447-180">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="7c447-181">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="7c447-181">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="7c447-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7c447-182">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="7c447-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="7c447-183">System-Only</span></span>            | <span data-ttu-id="7c447-184">Vero</span><span class="sxs-lookup"><span data-stu-id="7c447-184">True</span></span>                                             |
| <span data-ttu-id="7c447-185">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="7c447-185">Is-Single-Valued</span></span>       | <span data-ttu-id="7c447-186">Falso</span><span class="sxs-lookup"><span data-stu-id="7c447-186">False</span></span>                                            |
| <span data-ttu-id="7c447-187">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="7c447-187">Is Indexed</span></span>             | <span data-ttu-id="7c447-188">Falso</span><span class="sxs-lookup"><span data-stu-id="7c447-188">False</span></span>                                            |
| <span data-ttu-id="7c447-189">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="7c447-189">In Global Catalog</span></span>      | <span data-ttu-id="7c447-190">Falso</span><span class="sxs-lookup"><span data-stu-id="7c447-190">False</span></span>                                            |
| <span data-ttu-id="7c447-191">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="7c447-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="7c447-192">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="7c447-192">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="7c447-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7c447-193">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="7c447-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7c447-194">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="7c447-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7c447-195">Search-Flags</span></span>           | <span data-ttu-id="7c447-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7c447-196">0x00000000</span></span>                                       |
| <span data-ttu-id="7c447-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7c447-197">System-Flags</span></span>           | <span data-ttu-id="7c447-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7c447-198">0x00000010</span></span>                                       |
| <span data-ttu-id="7c447-199">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="7c447-199">Classes used in</span></span>        | [<span data-ttu-id="7c447-200">**Classe-schema**</span><span class="sxs-lookup"><span data-stu-id="7c447-200">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="7c447-201">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="7c447-201">Windows Server 2003 R2</span></span>



| <span data-ttu-id="7c447-202">Voce</span><span class="sxs-lookup"><span data-stu-id="7c447-202">Entry</span></span> | <span data-ttu-id="7c447-203">Valore</span><span class="sxs-lookup"><span data-stu-id="7c447-203">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="7c447-204">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="7c447-204">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="7c447-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7c447-205">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="7c447-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="7c447-206">System-Only</span></span>            | <span data-ttu-id="7c447-207">Vero</span><span class="sxs-lookup"><span data-stu-id="7c447-207">True</span></span>                                             |
| <span data-ttu-id="7c447-208">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="7c447-208">Is-Single-Valued</span></span>       | <span data-ttu-id="7c447-209">Falso</span><span class="sxs-lookup"><span data-stu-id="7c447-209">False</span></span>                                            |
| <span data-ttu-id="7c447-210">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="7c447-210">Is Indexed</span></span>             | <span data-ttu-id="7c447-211">Falso</span><span class="sxs-lookup"><span data-stu-id="7c447-211">False</span></span>                                            |
| <span data-ttu-id="7c447-212">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="7c447-212">In Global Catalog</span></span>      | <span data-ttu-id="7c447-213">Falso</span><span class="sxs-lookup"><span data-stu-id="7c447-213">False</span></span>                                            |
| <span data-ttu-id="7c447-214">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="7c447-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="7c447-215">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="7c447-215">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="7c447-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7c447-216">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="7c447-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7c447-217">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="7c447-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7c447-218">Search-Flags</span></span>           | <span data-ttu-id="7c447-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7c447-219">0x00000000</span></span>                                       |
| <span data-ttu-id="7c447-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7c447-220">System-Flags</span></span>           | <span data-ttu-id="7c447-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7c447-221">0x00000010</span></span>                                       |
| <span data-ttu-id="7c447-222">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="7c447-222">Classes used in</span></span>        | [<span data-ttu-id="7c447-223">**Classe-schema**</span><span class="sxs-lookup"><span data-stu-id="7c447-223">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="7c447-224">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7c447-224">Windows Server 2008</span></span>



| <span data-ttu-id="7c447-225">Voce</span><span class="sxs-lookup"><span data-stu-id="7c447-225">Entry</span></span> | <span data-ttu-id="7c447-226">Valore</span><span class="sxs-lookup"><span data-stu-id="7c447-226">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="7c447-227">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="7c447-227">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="7c447-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7c447-228">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="7c447-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="7c447-229">System-Only</span></span>            | <span data-ttu-id="7c447-230">Vero</span><span class="sxs-lookup"><span data-stu-id="7c447-230">True</span></span>                                             |
| <span data-ttu-id="7c447-231">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="7c447-231">Is-Single-Valued</span></span>       | <span data-ttu-id="7c447-232">Falso</span><span class="sxs-lookup"><span data-stu-id="7c447-232">False</span></span>                                            |
| <span data-ttu-id="7c447-233">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="7c447-233">Is Indexed</span></span>             | <span data-ttu-id="7c447-234">Falso</span><span class="sxs-lookup"><span data-stu-id="7c447-234">False</span></span>                                            |
| <span data-ttu-id="7c447-235">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="7c447-235">In Global Catalog</span></span>      | <span data-ttu-id="7c447-236">Falso</span><span class="sxs-lookup"><span data-stu-id="7c447-236">False</span></span>                                            |
| <span data-ttu-id="7c447-237">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="7c447-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="7c447-238">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="7c447-238">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="7c447-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7c447-239">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="7c447-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7c447-240">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="7c447-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7c447-241">Search-Flags</span></span>           | <span data-ttu-id="7c447-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7c447-242">0x00000000</span></span>                                       |
| <span data-ttu-id="7c447-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7c447-243">System-Flags</span></span>           | <span data-ttu-id="7c447-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7c447-244">0x00000010</span></span>                                       |
| <span data-ttu-id="7c447-245">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="7c447-245">Classes used in</span></span>        | [<span data-ttu-id="7c447-246">**Classe-schema**</span><span class="sxs-lookup"><span data-stu-id="7c447-246">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="7c447-247">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7c447-247">Windows Server 2008 R2</span></span>



| <span data-ttu-id="7c447-248">Voce</span><span class="sxs-lookup"><span data-stu-id="7c447-248">Entry</span></span> | <span data-ttu-id="7c447-249">Valore</span><span class="sxs-lookup"><span data-stu-id="7c447-249">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="7c447-250">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="7c447-250">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="7c447-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7c447-251">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="7c447-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="7c447-252">System-Only</span></span>            | <span data-ttu-id="7c447-253">Vero</span><span class="sxs-lookup"><span data-stu-id="7c447-253">True</span></span>                                             |
| <span data-ttu-id="7c447-254">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="7c447-254">Is-Single-Valued</span></span>       | <span data-ttu-id="7c447-255">Falso</span><span class="sxs-lookup"><span data-stu-id="7c447-255">False</span></span>                                            |
| <span data-ttu-id="7c447-256">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="7c447-256">Is Indexed</span></span>             | <span data-ttu-id="7c447-257">Falso</span><span class="sxs-lookup"><span data-stu-id="7c447-257">False</span></span>                                            |
| <span data-ttu-id="7c447-258">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="7c447-258">In Global Catalog</span></span>      | <span data-ttu-id="7c447-259">Falso</span><span class="sxs-lookup"><span data-stu-id="7c447-259">False</span></span>                                            |
| <span data-ttu-id="7c447-260">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="7c447-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="7c447-261">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="7c447-261">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="7c447-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7c447-262">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="7c447-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7c447-263">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="7c447-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7c447-264">Search-Flags</span></span>           | <span data-ttu-id="7c447-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7c447-265">0x00000000</span></span>                                       |
| <span data-ttu-id="7c447-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7c447-266">System-Flags</span></span>           | <span data-ttu-id="7c447-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7c447-267">0x00000010</span></span>                                       |
| <span data-ttu-id="7c447-268">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="7c447-268">Classes used in</span></span>        | [<span data-ttu-id="7c447-269">**Classe-schema**</span><span class="sxs-lookup"><span data-stu-id="7c447-269">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="7c447-270">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7c447-270">Windows Server 2012</span></span>



| <span data-ttu-id="7c447-271">Voce</span><span class="sxs-lookup"><span data-stu-id="7c447-271">Entry</span></span> | <span data-ttu-id="7c447-272">Valore</span><span class="sxs-lookup"><span data-stu-id="7c447-272">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="7c447-273">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="7c447-273">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="7c447-274">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7c447-274">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="7c447-275">System-Only</span><span class="sxs-lookup"><span data-stu-id="7c447-275">System-Only</span></span>            | <span data-ttu-id="7c447-276">Vero</span><span class="sxs-lookup"><span data-stu-id="7c447-276">True</span></span>                                             |
| <span data-ttu-id="7c447-277">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="7c447-277">Is-Single-Valued</span></span>       | <span data-ttu-id="7c447-278">Falso</span><span class="sxs-lookup"><span data-stu-id="7c447-278">False</span></span>                                            |
| <span data-ttu-id="7c447-279">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="7c447-279">Is Indexed</span></span>             | <span data-ttu-id="7c447-280">Falso</span><span class="sxs-lookup"><span data-stu-id="7c447-280">False</span></span>                                            |
| <span data-ttu-id="7c447-281">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="7c447-281">In Global Catalog</span></span>      | <span data-ttu-id="7c447-282">Falso</span><span class="sxs-lookup"><span data-stu-id="7c447-282">False</span></span>                                            |
| <span data-ttu-id="7c447-283">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="7c447-283">NT-Security-Descriptor</span></span> | <span data-ttu-id="7c447-284">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="7c447-284">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="7c447-285">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7c447-285">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="7c447-286">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7c447-286">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="7c447-287">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7c447-287">Search-Flags</span></span>           | <span data-ttu-id="7c447-288">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7c447-288">0x00000000</span></span>                                       |
| <span data-ttu-id="7c447-289">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7c447-289">System-Flags</span></span>           | <span data-ttu-id="7c447-290">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7c447-290">0x00000010</span></span>                                       |
| <span data-ttu-id="7c447-291">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="7c447-291">Classes used in</span></span>        | [<span data-ttu-id="7c447-292">**Classe-schema**</span><span class="sxs-lookup"><span data-stu-id="7c447-292">**Class-Schema**</span></span>](c-classschema.md)<br/> |



 

 





