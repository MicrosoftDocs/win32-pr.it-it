---
title: Attributo Instance-Type
description: Bit che determina il modo in cui viene creata un'istanza dell'oggetto in un determinato server.
ms.assetid: ed77c302-3d80-4292-8e48-bfc6cb5079ee
ms.tgt_platform: multiple
keywords:
- Schema AD Instance-Type attribute
- Schema AD dell'attributo instanceType
topic_type:
- apiref
api_name:
- Instance-Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e31eec3c5a7a189f4623e8e77badb3b1e83e0cd4
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744834"
---
# <a name="instance-type-attribute"></a><span data-ttu-id="72ecc-105">Attributo Instance-Type</span><span class="sxs-lookup"><span data-stu-id="72ecc-105">Instance-Type attribute</span></span>

<span data-ttu-id="72ecc-106">Bit che determina il modo in cui viene creata un'istanza dell'oggetto in un determinato server.</span><span class="sxs-lookup"><span data-stu-id="72ecc-106">A bitfield that dictates how the object is instantiated on a particular server.</span></span> <span data-ttu-id="72ecc-107">Il valore di questo attributo può variare in repliche diverse anche se le repliche sono sincronizzate.</span><span class="sxs-lookup"><span data-stu-id="72ecc-107">The value of this attribute can differ on different replicas even if the replicas are in sync.</span></span>

<span data-ttu-id="72ecc-108">Questo attributo può essere zero o una combinazione di uno o più dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="72ecc-108">This attribute can be zero or a combination of one or more of the following values.</span></span>

| <span data-ttu-id="72ecc-109">Valore</span><span class="sxs-lookup"><span data-stu-id="72ecc-109">Value</span></span>      | <span data-ttu-id="72ecc-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="72ecc-110">Description</span></span>                                                                                        |
|------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72ecc-111">0x00000001</span><span class="sxs-lookup"><span data-stu-id="72ecc-111">0x00000001</span></span> | <span data-ttu-id="72ecc-112">Intestazione del contesto dei nomi.</span><span class="sxs-lookup"><span data-stu-id="72ecc-112">The head of naming context.</span></span>                                                                        |
| <span data-ttu-id="72ecc-113">0x00000002</span><span class="sxs-lookup"><span data-stu-id="72ecc-113">0x00000002</span></span> | <span data-ttu-id="72ecc-114">Non è stata creata un'istanza della replica.</span><span class="sxs-lookup"><span data-stu-id="72ecc-114">This replica is not instantiated.</span></span>                                                                  |
| <span data-ttu-id="72ecc-115">0x00000004</span><span class="sxs-lookup"><span data-stu-id="72ecc-115">0x00000004</span></span> | <span data-ttu-id="72ecc-116">L'oggetto è scrivibile in questa directory.</span><span class="sxs-lookup"><span data-stu-id="72ecc-116">The object is writable on this directory.</span></span>                                                          |
| <span data-ttu-id="72ecc-117">0x00000008</span><span class="sxs-lookup"><span data-stu-id="72ecc-117">0x00000008</span></span> | <span data-ttu-id="72ecc-118">Viene mantenuto il contesto di denominazione sopra questo in questa directory.</span><span class="sxs-lookup"><span data-stu-id="72ecc-118">The naming context above this one on this directory is held.</span></span>                                       |
| <span data-ttu-id="72ecc-119">0x00000010</span><span class="sxs-lookup"><span data-stu-id="72ecc-119">0x00000010</span></span> | <span data-ttu-id="72ecc-120">Il contesto dei nomi è in corso di costruzione per la prima volta tramite la replica.</span><span class="sxs-lookup"><span data-stu-id="72ecc-120">The naming context is in the process of being constructed for the first time by using replication.</span></span> |
| <span data-ttu-id="72ecc-121">0x00000020</span><span class="sxs-lookup"><span data-stu-id="72ecc-121">0x00000020</span></span> | <span data-ttu-id="72ecc-122">Il contesto dei nomi è in corso di rimozione dal DSA locale.</span><span class="sxs-lookup"><span data-stu-id="72ecc-122">The naming context is in the process of being removed from the local DSA.</span></span>                          |



 



| <span data-ttu-id="72ecc-123">Voce</span><span class="sxs-lookup"><span data-stu-id="72ecc-123">Entry</span></span> | <span data-ttu-id="72ecc-124">Valore</span><span class="sxs-lookup"><span data-stu-id="72ecc-124">Value</span></span> |
|-------------------|------------------------------------------------|
| <span data-ttu-id="72ecc-125">CN</span><span class="sxs-lookup"><span data-stu-id="72ecc-125">CN</span></span>                | <span data-ttu-id="72ecc-126">Instance-Type</span><span class="sxs-lookup"><span data-stu-id="72ecc-126">Instance-Type</span></span>                                  |
| <span data-ttu-id="72ecc-127">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="72ecc-127">Ldap-Display-Name</span></span> | <span data-ttu-id="72ecc-128">instanceType</span><span class="sxs-lookup"><span data-stu-id="72ecc-128">instanceType</span></span>                                   |
| <span data-ttu-id="72ecc-129">Dimensione</span><span class="sxs-lookup"><span data-stu-id="72ecc-129">Size</span></span>              | <span data-ttu-id="72ecc-130">4 byte.</span><span class="sxs-lookup"><span data-stu-id="72ecc-130">4 bytes.</span></span>                                       |
| <span data-ttu-id="72ecc-131">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="72ecc-131">Update Privilege</span></span>  | <span data-ttu-id="72ecc-132">Questo valore viene impostato dall'amministratore dello schema.</span><span class="sxs-lookup"><span data-stu-id="72ecc-132">This value is set by the schema administrator.</span></span> |
| <span data-ttu-id="72ecc-133">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="72ecc-133">Update Frequency</span></span>  | <span data-ttu-id="72ecc-134">Quando viene creato l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="72ecc-134">When the object is created.</span></span>                    |
| <span data-ttu-id="72ecc-135">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="72ecc-135">Attribute-Id</span></span>      | <span data-ttu-id="72ecc-136">1.2.840.113556.1.2.1</span><span class="sxs-lookup"><span data-stu-id="72ecc-136">1.2.840.113556.1.2.1</span></span>                           |
| <span data-ttu-id="72ecc-137">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="72ecc-137">System-Id-Guid</span></span>    | <span data-ttu-id="72ecc-138">bf96798c-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="72ecc-138">bf96798c-0de6-11d0-a285-00aa003049e2</span></span>           |
| <span data-ttu-id="72ecc-139">Sintassi</span><span class="sxs-lookup"><span data-stu-id="72ecc-139">Syntax</span></span>            | [<span data-ttu-id="72ecc-140">**Enumerazione**</span><span class="sxs-lookup"><span data-stu-id="72ecc-140">**Enumeration**</span></span>](s-enumeration.md)           |



## <a name="implementations"></a><span data-ttu-id="72ecc-141">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="72ecc-141">Implementations</span></span>

-   [<span data-ttu-id="72ecc-142">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="72ecc-142">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="72ecc-143">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="72ecc-143">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="72ecc-144">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="72ecc-144">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="72ecc-145">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="72ecc-145">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="72ecc-146">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="72ecc-146">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="72ecc-147">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="72ecc-147">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="72ecc-148">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="72ecc-148">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="72ecc-149">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="72ecc-149">Windows 2000 Server</span></span>



| <span data-ttu-id="72ecc-150">Voce</span><span class="sxs-lookup"><span data-stu-id="72ecc-150">Entry</span></span> | <span data-ttu-id="72ecc-151">Valore</span><span class="sxs-lookup"><span data-stu-id="72ecc-151">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="72ecc-152">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="72ecc-152">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="72ecc-153">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="72ecc-153">MAPI-Id</span></span>                | <span data-ttu-id="72ecc-154">0x80BD</span><span class="sxs-lookup"><span data-stu-id="72ecc-154">0x80BD</span></span>                          |
| <span data-ttu-id="72ecc-155">System-Only</span><span class="sxs-lookup"><span data-stu-id="72ecc-155">System-Only</span></span>            | <span data-ttu-id="72ecc-156">Vero</span><span class="sxs-lookup"><span data-stu-id="72ecc-156">True</span></span>                            |
| <span data-ttu-id="72ecc-157">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="72ecc-157">Is-Single-Valued</span></span>       | <span data-ttu-id="72ecc-158">Vero</span><span class="sxs-lookup"><span data-stu-id="72ecc-158">True</span></span>                            |
| <span data-ttu-id="72ecc-159">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="72ecc-159">Is Indexed</span></span>             | <span data-ttu-id="72ecc-160">Falso</span><span class="sxs-lookup"><span data-stu-id="72ecc-160">False</span></span>                           |
| <span data-ttu-id="72ecc-161">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="72ecc-161">In Global Catalog</span></span>      | <span data-ttu-id="72ecc-162">Vero</span><span class="sxs-lookup"><span data-stu-id="72ecc-162">True</span></span>                            |
| <span data-ttu-id="72ecc-163">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="72ecc-163">NT-Security-Descriptor</span></span> | <span data-ttu-id="72ecc-164">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="72ecc-164">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="72ecc-165">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="72ecc-165">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="72ecc-166">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="72ecc-166">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="72ecc-167">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="72ecc-167">Search-Flags</span></span>           | <span data-ttu-id="72ecc-168">0x00000008</span><span class="sxs-lookup"><span data-stu-id="72ecc-168">0x00000008</span></span>                      |
| <span data-ttu-id="72ecc-169">System-Flags</span><span class="sxs-lookup"><span data-stu-id="72ecc-169">System-Flags</span></span>           | <span data-ttu-id="72ecc-170">0x00000012</span><span class="sxs-lookup"><span data-stu-id="72ecc-170">0x00000012</span></span>                      |
| <span data-ttu-id="72ecc-171">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="72ecc-171">Classes used in</span></span>        | [<span data-ttu-id="72ecc-172">**In alto**</span><span class="sxs-lookup"><span data-stu-id="72ecc-172">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="72ecc-173">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="72ecc-173">Windows Server 2003</span></span>



| <span data-ttu-id="72ecc-174">Voce</span><span class="sxs-lookup"><span data-stu-id="72ecc-174">Entry</span></span> | <span data-ttu-id="72ecc-175">Valore</span><span class="sxs-lookup"><span data-stu-id="72ecc-175">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="72ecc-176">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="72ecc-176">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="72ecc-177">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="72ecc-177">MAPI-Id</span></span>                | <span data-ttu-id="72ecc-178">0x80BD</span><span class="sxs-lookup"><span data-stu-id="72ecc-178">0x80BD</span></span>                          |
| <span data-ttu-id="72ecc-179">System-Only</span><span class="sxs-lookup"><span data-stu-id="72ecc-179">System-Only</span></span>            | <span data-ttu-id="72ecc-180">Vero</span><span class="sxs-lookup"><span data-stu-id="72ecc-180">True</span></span>                            |
| <span data-ttu-id="72ecc-181">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="72ecc-181">Is-Single-Valued</span></span>       | <span data-ttu-id="72ecc-182">Vero</span><span class="sxs-lookup"><span data-stu-id="72ecc-182">True</span></span>                            |
| <span data-ttu-id="72ecc-183">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="72ecc-183">Is Indexed</span></span>             | <span data-ttu-id="72ecc-184">Falso</span><span class="sxs-lookup"><span data-stu-id="72ecc-184">False</span></span>                           |
| <span data-ttu-id="72ecc-185">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="72ecc-185">In Global Catalog</span></span>      | <span data-ttu-id="72ecc-186">Vero</span><span class="sxs-lookup"><span data-stu-id="72ecc-186">True</span></span>                            |
| <span data-ttu-id="72ecc-187">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="72ecc-187">NT-Security-Descriptor</span></span> | <span data-ttu-id="72ecc-188">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="72ecc-188">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="72ecc-189">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="72ecc-189">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="72ecc-190">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="72ecc-190">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="72ecc-191">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="72ecc-191">Search-Flags</span></span>           | <span data-ttu-id="72ecc-192">0x00000008</span><span class="sxs-lookup"><span data-stu-id="72ecc-192">0x00000008</span></span>                      |
| <span data-ttu-id="72ecc-193">System-Flags</span><span class="sxs-lookup"><span data-stu-id="72ecc-193">System-Flags</span></span>           | <span data-ttu-id="72ecc-194">0x00000012</span><span class="sxs-lookup"><span data-stu-id="72ecc-194">0x00000012</span></span>                      |
| <span data-ttu-id="72ecc-195">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="72ecc-195">Classes used in</span></span>        | [<span data-ttu-id="72ecc-196">**In alto**</span><span class="sxs-lookup"><span data-stu-id="72ecc-196">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="72ecc-197">ADAM</span><span class="sxs-lookup"><span data-stu-id="72ecc-197">ADAM</span></span>



| <span data-ttu-id="72ecc-198">Voce</span><span class="sxs-lookup"><span data-stu-id="72ecc-198">Entry</span></span> | <span data-ttu-id="72ecc-199">Valore</span><span class="sxs-lookup"><span data-stu-id="72ecc-199">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="72ecc-200">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="72ecc-200">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="72ecc-201">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="72ecc-201">MAPI-Id</span></span>                | <span data-ttu-id="72ecc-202">0x80BD</span><span class="sxs-lookup"><span data-stu-id="72ecc-202">0x80BD</span></span>                          |
| <span data-ttu-id="72ecc-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="72ecc-203">System-Only</span></span>            | <span data-ttu-id="72ecc-204">Vero</span><span class="sxs-lookup"><span data-stu-id="72ecc-204">True</span></span>                            |
| <span data-ttu-id="72ecc-205">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="72ecc-205">Is-Single-Valued</span></span>       | <span data-ttu-id="72ecc-206">Vero</span><span class="sxs-lookup"><span data-stu-id="72ecc-206">True</span></span>                            |
| <span data-ttu-id="72ecc-207">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="72ecc-207">Is Indexed</span></span>             | <span data-ttu-id="72ecc-208">Falso</span><span class="sxs-lookup"><span data-stu-id="72ecc-208">False</span></span>                           |
| <span data-ttu-id="72ecc-209">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="72ecc-209">In Global Catalog</span></span>      | <span data-ttu-id="72ecc-210">Vero</span><span class="sxs-lookup"><span data-stu-id="72ecc-210">True</span></span>                            |
| <span data-ttu-id="72ecc-211">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="72ecc-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="72ecc-212">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="72ecc-212">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="72ecc-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="72ecc-213">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="72ecc-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="72ecc-214">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="72ecc-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="72ecc-215">Search-Flags</span></span>           | <span data-ttu-id="72ecc-216">0x00000008</span><span class="sxs-lookup"><span data-stu-id="72ecc-216">0x00000008</span></span>                      |
| <span data-ttu-id="72ecc-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="72ecc-217">System-Flags</span></span>           | <span data-ttu-id="72ecc-218">0x00000012</span><span class="sxs-lookup"><span data-stu-id="72ecc-218">0x00000012</span></span>                      |
| <span data-ttu-id="72ecc-219">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="72ecc-219">Classes used in</span></span>        | [<span data-ttu-id="72ecc-220">**In alto**</span><span class="sxs-lookup"><span data-stu-id="72ecc-220">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="72ecc-221">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="72ecc-221">Windows Server 2003 R2</span></span>



| <span data-ttu-id="72ecc-222">Voce</span><span class="sxs-lookup"><span data-stu-id="72ecc-222">Entry</span></span> | <span data-ttu-id="72ecc-223">Valore</span><span class="sxs-lookup"><span data-stu-id="72ecc-223">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="72ecc-224">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="72ecc-224">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="72ecc-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="72ecc-225">MAPI-Id</span></span>                | <span data-ttu-id="72ecc-226">0x80BD</span><span class="sxs-lookup"><span data-stu-id="72ecc-226">0x80BD</span></span>                          |
| <span data-ttu-id="72ecc-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="72ecc-227">System-Only</span></span>            | <span data-ttu-id="72ecc-228">Vero</span><span class="sxs-lookup"><span data-stu-id="72ecc-228">True</span></span>                            |
| <span data-ttu-id="72ecc-229">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="72ecc-229">Is-Single-Valued</span></span>       | <span data-ttu-id="72ecc-230">Vero</span><span class="sxs-lookup"><span data-stu-id="72ecc-230">True</span></span>                            |
| <span data-ttu-id="72ecc-231">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="72ecc-231">Is Indexed</span></span>             | <span data-ttu-id="72ecc-232">Falso</span><span class="sxs-lookup"><span data-stu-id="72ecc-232">False</span></span>                           |
| <span data-ttu-id="72ecc-233">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="72ecc-233">In Global Catalog</span></span>      | <span data-ttu-id="72ecc-234">Vero</span><span class="sxs-lookup"><span data-stu-id="72ecc-234">True</span></span>                            |
| <span data-ttu-id="72ecc-235">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="72ecc-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="72ecc-236">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="72ecc-236">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="72ecc-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="72ecc-237">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="72ecc-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="72ecc-238">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="72ecc-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="72ecc-239">Search-Flags</span></span>           | <span data-ttu-id="72ecc-240">0x00000008</span><span class="sxs-lookup"><span data-stu-id="72ecc-240">0x00000008</span></span>                      |
| <span data-ttu-id="72ecc-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="72ecc-241">System-Flags</span></span>           | <span data-ttu-id="72ecc-242">0x00000012</span><span class="sxs-lookup"><span data-stu-id="72ecc-242">0x00000012</span></span>                      |
| <span data-ttu-id="72ecc-243">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="72ecc-243">Classes used in</span></span>        | [<span data-ttu-id="72ecc-244">**In alto**</span><span class="sxs-lookup"><span data-stu-id="72ecc-244">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="72ecc-245">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="72ecc-245">Windows Server 2008</span></span>



| <span data-ttu-id="72ecc-246">Voce</span><span class="sxs-lookup"><span data-stu-id="72ecc-246">Entry</span></span> | <span data-ttu-id="72ecc-247">Valore</span><span class="sxs-lookup"><span data-stu-id="72ecc-247">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="72ecc-248">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="72ecc-248">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="72ecc-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="72ecc-249">MAPI-Id</span></span>                | <span data-ttu-id="72ecc-250">0x80BD</span><span class="sxs-lookup"><span data-stu-id="72ecc-250">0x80BD</span></span>                          |
| <span data-ttu-id="72ecc-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="72ecc-251">System-Only</span></span>            | <span data-ttu-id="72ecc-252">Vero</span><span class="sxs-lookup"><span data-stu-id="72ecc-252">True</span></span>                            |
| <span data-ttu-id="72ecc-253">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="72ecc-253">Is-Single-Valued</span></span>       | <span data-ttu-id="72ecc-254">Vero</span><span class="sxs-lookup"><span data-stu-id="72ecc-254">True</span></span>                            |
| <span data-ttu-id="72ecc-255">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="72ecc-255">Is Indexed</span></span>             | <span data-ttu-id="72ecc-256">Falso</span><span class="sxs-lookup"><span data-stu-id="72ecc-256">False</span></span>                           |
| <span data-ttu-id="72ecc-257">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="72ecc-257">In Global Catalog</span></span>      | <span data-ttu-id="72ecc-258">Vero</span><span class="sxs-lookup"><span data-stu-id="72ecc-258">True</span></span>                            |
| <span data-ttu-id="72ecc-259">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="72ecc-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="72ecc-260">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="72ecc-260">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="72ecc-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="72ecc-261">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="72ecc-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="72ecc-262">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="72ecc-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="72ecc-263">Search-Flags</span></span>           | <span data-ttu-id="72ecc-264">0x00000008</span><span class="sxs-lookup"><span data-stu-id="72ecc-264">0x00000008</span></span>                      |
| <span data-ttu-id="72ecc-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="72ecc-265">System-Flags</span></span>           | <span data-ttu-id="72ecc-266">0x00000012</span><span class="sxs-lookup"><span data-stu-id="72ecc-266">0x00000012</span></span>                      |
| <span data-ttu-id="72ecc-267">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="72ecc-267">Classes used in</span></span>        | [<span data-ttu-id="72ecc-268">**In alto**</span><span class="sxs-lookup"><span data-stu-id="72ecc-268">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="72ecc-269">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="72ecc-269">Windows Server 2008 R2</span></span>



| <span data-ttu-id="72ecc-270">Voce</span><span class="sxs-lookup"><span data-stu-id="72ecc-270">Entry</span></span> | <span data-ttu-id="72ecc-271">Valore</span><span class="sxs-lookup"><span data-stu-id="72ecc-271">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="72ecc-272">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="72ecc-272">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="72ecc-273">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="72ecc-273">MAPI-Id</span></span>                | <span data-ttu-id="72ecc-274">0x80BD</span><span class="sxs-lookup"><span data-stu-id="72ecc-274">0x80BD</span></span>                          |
| <span data-ttu-id="72ecc-275">System-Only</span><span class="sxs-lookup"><span data-stu-id="72ecc-275">System-Only</span></span>            | <span data-ttu-id="72ecc-276">Vero</span><span class="sxs-lookup"><span data-stu-id="72ecc-276">True</span></span>                            |
| <span data-ttu-id="72ecc-277">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="72ecc-277">Is-Single-Valued</span></span>       | <span data-ttu-id="72ecc-278">Vero</span><span class="sxs-lookup"><span data-stu-id="72ecc-278">True</span></span>                            |
| <span data-ttu-id="72ecc-279">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="72ecc-279">Is Indexed</span></span>             | <span data-ttu-id="72ecc-280">Falso</span><span class="sxs-lookup"><span data-stu-id="72ecc-280">False</span></span>                           |
| <span data-ttu-id="72ecc-281">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="72ecc-281">In Global Catalog</span></span>      | <span data-ttu-id="72ecc-282">Vero</span><span class="sxs-lookup"><span data-stu-id="72ecc-282">True</span></span>                            |
| <span data-ttu-id="72ecc-283">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="72ecc-283">NT-Security-Descriptor</span></span> | <span data-ttu-id="72ecc-284">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="72ecc-284">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="72ecc-285">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="72ecc-285">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="72ecc-286">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="72ecc-286">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="72ecc-287">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="72ecc-287">Search-Flags</span></span>           | <span data-ttu-id="72ecc-288">0x00000008</span><span class="sxs-lookup"><span data-stu-id="72ecc-288">0x00000008</span></span>                      |
| <span data-ttu-id="72ecc-289">System-Flags</span><span class="sxs-lookup"><span data-stu-id="72ecc-289">System-Flags</span></span>           | <span data-ttu-id="72ecc-290">0x00000012</span><span class="sxs-lookup"><span data-stu-id="72ecc-290">0x00000012</span></span>                      |
| <span data-ttu-id="72ecc-291">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="72ecc-291">Classes used in</span></span>        | [<span data-ttu-id="72ecc-292">**In alto**</span><span class="sxs-lookup"><span data-stu-id="72ecc-292">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="72ecc-293">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="72ecc-293">Windows Server 2012</span></span>



| <span data-ttu-id="72ecc-294">Voce</span><span class="sxs-lookup"><span data-stu-id="72ecc-294">Entry</span></span> | <span data-ttu-id="72ecc-295">Valore</span><span class="sxs-lookup"><span data-stu-id="72ecc-295">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="72ecc-296">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="72ecc-296">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="72ecc-297">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="72ecc-297">MAPI-Id</span></span>                | <span data-ttu-id="72ecc-298">0x80BD</span><span class="sxs-lookup"><span data-stu-id="72ecc-298">0x80BD</span></span>                          |
| <span data-ttu-id="72ecc-299">System-Only</span><span class="sxs-lookup"><span data-stu-id="72ecc-299">System-Only</span></span>            | <span data-ttu-id="72ecc-300">Vero</span><span class="sxs-lookup"><span data-stu-id="72ecc-300">True</span></span>                            |
| <span data-ttu-id="72ecc-301">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="72ecc-301">Is-Single-Valued</span></span>       | <span data-ttu-id="72ecc-302">Vero</span><span class="sxs-lookup"><span data-stu-id="72ecc-302">True</span></span>                            |
| <span data-ttu-id="72ecc-303">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="72ecc-303">Is Indexed</span></span>             | <span data-ttu-id="72ecc-304">Falso</span><span class="sxs-lookup"><span data-stu-id="72ecc-304">False</span></span>                           |
| <span data-ttu-id="72ecc-305">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="72ecc-305">In Global Catalog</span></span>      | <span data-ttu-id="72ecc-306">Vero</span><span class="sxs-lookup"><span data-stu-id="72ecc-306">True</span></span>                            |
| <span data-ttu-id="72ecc-307">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="72ecc-307">NT-Security-Descriptor</span></span> | <span data-ttu-id="72ecc-308">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="72ecc-308">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="72ecc-309">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="72ecc-309">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="72ecc-310">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="72ecc-310">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="72ecc-311">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="72ecc-311">Search-Flags</span></span>           | <span data-ttu-id="72ecc-312">0x00000008</span><span class="sxs-lookup"><span data-stu-id="72ecc-312">0x00000008</span></span>                      |
| <span data-ttu-id="72ecc-313">System-Flags</span><span class="sxs-lookup"><span data-stu-id="72ecc-313">System-Flags</span></span>           | <span data-ttu-id="72ecc-314">0x00000012</span><span class="sxs-lookup"><span data-stu-id="72ecc-314">0x00000012</span></span>                      |
| <span data-ttu-id="72ecc-315">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="72ecc-315">Classes used in</span></span>        | [<span data-ttu-id="72ecc-316">**In alto**</span><span class="sxs-lookup"><span data-stu-id="72ecc-316">**Top**</span></span>](c-top.md)<br/> |



 

 





