---
title: Entry-TTL (attributo)
description: Questo attributo operativo è gestito dal server e sembra essere presente in ogni voce dinamica.
ms.assetid: cac0e52e-243d-4822-9419-2af8b9352cee
ms.tgt_platform: multiple
keywords:
- Entry-TTL attributo AD schema
- Schema AD dell'attributo entryTTL
topic_type:
- apiref
api_name:
- Entry-TTL
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab2dd5e38b22731fee7f957ee8f817537e32c645
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104479712"
---
# <a name="entry-ttl-attribute"></a><span data-ttu-id="4be5b-105">Entry-TTL (attributo)</span><span class="sxs-lookup"><span data-stu-id="4be5b-105">Entry-TTL attribute</span></span>

<span data-ttu-id="4be5b-106">Questo attributo operativo è gestito dal server e sembra essere presente in ogni voce dinamica.</span><span class="sxs-lookup"><span data-stu-id="4be5b-106">This operational attribute is maintained by the server and appears to be present in every dynamic entry.</span></span> <span data-ttu-id="4be5b-107">L'attributo non è presente se la voce non contiene la classe di oggetti dynamicObject.</span><span class="sxs-lookup"><span data-stu-id="4be5b-107">The attribute is not present when the entry does not contain the dynamicObject object class.</span></span> <span data-ttu-id="4be5b-108">Il valore di questo attributo è il tempo, in secondi, in cui la voce continuerà a esistere prima di scomparire dalla directory.</span><span class="sxs-lookup"><span data-stu-id="4be5b-108">The value of this attribute is the time, in seconds, that the entry will continue to exist before disappearing from the directory.</span></span> <span data-ttu-id="4be5b-109">In assenza di operazioni "Refresh", i valori restituiti leggendo l'attributo in due ricerche successive sono garantiti che non aumentano.</span><span class="sxs-lookup"><span data-stu-id="4be5b-109">In the absence of intervening "refresh" operations, the values returned by reading the attribute in two successive searches are guaranteed to be nonincreasing.</span></span> <span data-ttu-id="4be5b-110">Il valore minimo consentito è 0, che indica che la voce può scomparire senza preavviso.</span><span class="sxs-lookup"><span data-stu-id="4be5b-110">The smallest permissible value is 0, indicating that the entry may disappear without warning.</span></span> <span data-ttu-id="4be5b-111">L'attributo è contrassegnato come nessuna modifica da parte dell'utente perché può essere modificato solo tramite l'operazione di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="4be5b-111">The attribute is marked NO-USER-MODIFICATION because it may only be changed by using the refresh operation.</span></span>



| <span data-ttu-id="4be5b-112">Voce</span><span class="sxs-lookup"><span data-stu-id="4be5b-112">Entry</span></span> | <span data-ttu-id="4be5b-113">Valore</span><span class="sxs-lookup"><span data-stu-id="4be5b-113">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="4be5b-114">CN</span><span class="sxs-lookup"><span data-stu-id="4be5b-114">CN</span></span>                | <span data-ttu-id="4be5b-115">Voce-TTL</span><span class="sxs-lookup"><span data-stu-id="4be5b-115">Entry-TTL</span></span>                                   |
| <span data-ttu-id="4be5b-116">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="4be5b-116">Ldap-Display-Name</span></span> | <span data-ttu-id="4be5b-117">entryTTL</span><span class="sxs-lookup"><span data-stu-id="4be5b-117">entryTTL</span></span>                                    |
| <span data-ttu-id="4be5b-118">Dimensione</span><span class="sxs-lookup"><span data-stu-id="4be5b-118">Size</span></span>              | <span data-ttu-id="4be5b-119">4 byte.</span><span class="sxs-lookup"><span data-stu-id="4be5b-119">4 bytes.</span></span> <span data-ttu-id="4be5b-120">Massimo = 1 anno, valore predefinito = 1 giorno.</span><span class="sxs-lookup"><span data-stu-id="4be5b-120">Maximum = 1 year, default = 1 day.</span></span> |
| <span data-ttu-id="4be5b-121">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="4be5b-121">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="4be5b-122">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="4be5b-122">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="4be5b-123">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="4be5b-123">Attribute-Id</span></span>      | <span data-ttu-id="4be5b-124">1.3.6.1.4.1.1466.101.119.3</span><span class="sxs-lookup"><span data-stu-id="4be5b-124">1.3.6.1.4.1.1466.101.119.3</span></span>                  |
| <span data-ttu-id="4be5b-125">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="4be5b-125">System-Id-Guid</span></span>    | <span data-ttu-id="4be5b-126">d213decc-d81a-4384-AAC2-dcfcfd631cf8</span><span class="sxs-lookup"><span data-stu-id="4be5b-126">d213decc-d81a-4384-aac2-dcfcfd631cf8</span></span>        |
| <span data-ttu-id="4be5b-127">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4be5b-127">Syntax</span></span>            | [<span data-ttu-id="4be5b-128">**Enumerazione**</span><span class="sxs-lookup"><span data-stu-id="4be5b-128">**Enumeration**</span></span>](s-enumeration.md)        |



## <a name="implementations"></a><span data-ttu-id="4be5b-129">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="4be5b-129">Implementations</span></span>

-   [<span data-ttu-id="4be5b-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="4be5b-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="4be5b-131">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="4be5b-131">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="4be5b-132">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="4be5b-132">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="4be5b-133">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="4be5b-133">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="4be5b-134">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="4be5b-134">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="4be5b-135">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="4be5b-135">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="4be5b-136">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4be5b-136">Windows Server 2003</span></span>



| <span data-ttu-id="4be5b-137">Voce</span><span class="sxs-lookup"><span data-stu-id="4be5b-137">Entry</span></span> | <span data-ttu-id="4be5b-138">Valore</span><span class="sxs-lookup"><span data-stu-id="4be5b-138">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="4be5b-139">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="4be5b-139">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="4be5b-140">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4be5b-140">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="4be5b-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="4be5b-141">System-Only</span></span>            | <span data-ttu-id="4be5b-142">Falso</span><span class="sxs-lookup"><span data-stu-id="4be5b-142">False</span></span>                                                |
| <span data-ttu-id="4be5b-143">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="4be5b-143">Is-Single-Valued</span></span>       | <span data-ttu-id="4be5b-144">Vero</span><span class="sxs-lookup"><span data-stu-id="4be5b-144">True</span></span>                                                 |
| <span data-ttu-id="4be5b-145">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="4be5b-145">Is Indexed</span></span>             | <span data-ttu-id="4be5b-146">Falso</span><span class="sxs-lookup"><span data-stu-id="4be5b-146">False</span></span>                                                |
| <span data-ttu-id="4be5b-147">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="4be5b-147">In Global Catalog</span></span>      | <span data-ttu-id="4be5b-148">Falso</span><span class="sxs-lookup"><span data-stu-id="4be5b-148">False</span></span>                                                |
| <span data-ttu-id="4be5b-149">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="4be5b-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="4be5b-150">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="4be5b-150">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="4be5b-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4be5b-151">Range-Lower</span></span>            | <span data-ttu-id="4be5b-152">0</span><span class="sxs-lookup"><span data-stu-id="4be5b-152">0</span></span>                                                    |
| <span data-ttu-id="4be5b-153">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4be5b-153">Range-Upper</span></span>            | <span data-ttu-id="4be5b-154">31557600</span><span class="sxs-lookup"><span data-stu-id="4be5b-154">31557600</span></span>                                             |
| <span data-ttu-id="4be5b-155">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4be5b-155">Search-Flags</span></span>           | <span data-ttu-id="4be5b-156">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4be5b-156">0x00000000</span></span>                                           |
| <span data-ttu-id="4be5b-157">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4be5b-157">System-Flags</span></span>           | <span data-ttu-id="4be5b-158">0x00000014</span><span class="sxs-lookup"><span data-stu-id="4be5b-158">0x00000014</span></span>                                           |
| <span data-ttu-id="4be5b-159">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="4be5b-159">Classes used in</span></span>        | [<span data-ttu-id="4be5b-160">**Oggetto dinamico**</span><span class="sxs-lookup"><span data-stu-id="4be5b-160">**Dynamic-Object**</span></span>](c-dynamicobject.md)<br/> |



## <a name="adam"></a><span data-ttu-id="4be5b-161">ADAM</span><span class="sxs-lookup"><span data-stu-id="4be5b-161">ADAM</span></span>



| <span data-ttu-id="4be5b-162">Voce</span><span class="sxs-lookup"><span data-stu-id="4be5b-162">Entry</span></span> | <span data-ttu-id="4be5b-163">Valore</span><span class="sxs-lookup"><span data-stu-id="4be5b-163">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="4be5b-164">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="4be5b-164">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="4be5b-165">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4be5b-165">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="4be5b-166">System-Only</span><span class="sxs-lookup"><span data-stu-id="4be5b-166">System-Only</span></span>            | <span data-ttu-id="4be5b-167">Falso</span><span class="sxs-lookup"><span data-stu-id="4be5b-167">False</span></span>                                                |
| <span data-ttu-id="4be5b-168">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="4be5b-168">Is-Single-Valued</span></span>       | <span data-ttu-id="4be5b-169">Vero</span><span class="sxs-lookup"><span data-stu-id="4be5b-169">True</span></span>                                                 |
| <span data-ttu-id="4be5b-170">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="4be5b-170">Is Indexed</span></span>             | <span data-ttu-id="4be5b-171">Falso</span><span class="sxs-lookup"><span data-stu-id="4be5b-171">False</span></span>                                                |
| <span data-ttu-id="4be5b-172">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="4be5b-172">In Global Catalog</span></span>      | <span data-ttu-id="4be5b-173">Falso</span><span class="sxs-lookup"><span data-stu-id="4be5b-173">False</span></span>                                                |
| <span data-ttu-id="4be5b-174">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="4be5b-174">NT-Security-Descriptor</span></span> | <span data-ttu-id="4be5b-175">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="4be5b-175">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="4be5b-176">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4be5b-176">Range-Lower</span></span>            | <span data-ttu-id="4be5b-177">0</span><span class="sxs-lookup"><span data-stu-id="4be5b-177">0</span></span>                                                    |
| <span data-ttu-id="4be5b-178">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4be5b-178">Range-Upper</span></span>            | <span data-ttu-id="4be5b-179">31557600</span><span class="sxs-lookup"><span data-stu-id="4be5b-179">31557600</span></span>                                             |
| <span data-ttu-id="4be5b-180">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4be5b-180">Search-Flags</span></span>           | <span data-ttu-id="4be5b-181">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4be5b-181">0x00000000</span></span>                                           |
| <span data-ttu-id="4be5b-182">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4be5b-182">System-Flags</span></span>           | <span data-ttu-id="4be5b-183">0x00000014</span><span class="sxs-lookup"><span data-stu-id="4be5b-183">0x00000014</span></span>                                           |
| <span data-ttu-id="4be5b-184">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="4be5b-184">Classes used in</span></span>        | [<span data-ttu-id="4be5b-185">**Oggetto dinamico**</span><span class="sxs-lookup"><span data-stu-id="4be5b-185">**Dynamic-Object**</span></span>](c-dynamicobject.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="4be5b-186">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="4be5b-186">Windows Server 2003 R2</span></span>



| <span data-ttu-id="4be5b-187">Voce</span><span class="sxs-lookup"><span data-stu-id="4be5b-187">Entry</span></span> | <span data-ttu-id="4be5b-188">Valore</span><span class="sxs-lookup"><span data-stu-id="4be5b-188">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="4be5b-189">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="4be5b-189">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="4be5b-190">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4be5b-190">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="4be5b-191">System-Only</span><span class="sxs-lookup"><span data-stu-id="4be5b-191">System-Only</span></span>            | <span data-ttu-id="4be5b-192">Falso</span><span class="sxs-lookup"><span data-stu-id="4be5b-192">False</span></span>                                                |
| <span data-ttu-id="4be5b-193">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="4be5b-193">Is-Single-Valued</span></span>       | <span data-ttu-id="4be5b-194">Vero</span><span class="sxs-lookup"><span data-stu-id="4be5b-194">True</span></span>                                                 |
| <span data-ttu-id="4be5b-195">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="4be5b-195">Is Indexed</span></span>             | <span data-ttu-id="4be5b-196">Falso</span><span class="sxs-lookup"><span data-stu-id="4be5b-196">False</span></span>                                                |
| <span data-ttu-id="4be5b-197">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="4be5b-197">In Global Catalog</span></span>      | <span data-ttu-id="4be5b-198">Falso</span><span class="sxs-lookup"><span data-stu-id="4be5b-198">False</span></span>                                                |
| <span data-ttu-id="4be5b-199">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="4be5b-199">NT-Security-Descriptor</span></span> | <span data-ttu-id="4be5b-200">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="4be5b-200">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="4be5b-201">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4be5b-201">Range-Lower</span></span>            | <span data-ttu-id="4be5b-202">0</span><span class="sxs-lookup"><span data-stu-id="4be5b-202">0</span></span>                                                    |
| <span data-ttu-id="4be5b-203">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4be5b-203">Range-Upper</span></span>            | <span data-ttu-id="4be5b-204">31557600</span><span class="sxs-lookup"><span data-stu-id="4be5b-204">31557600</span></span>                                             |
| <span data-ttu-id="4be5b-205">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4be5b-205">Search-Flags</span></span>           | <span data-ttu-id="4be5b-206">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4be5b-206">0x00000000</span></span>                                           |
| <span data-ttu-id="4be5b-207">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4be5b-207">System-Flags</span></span>           | <span data-ttu-id="4be5b-208">0x00000014</span><span class="sxs-lookup"><span data-stu-id="4be5b-208">0x00000014</span></span>                                           |
| <span data-ttu-id="4be5b-209">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="4be5b-209">Classes used in</span></span>        | [<span data-ttu-id="4be5b-210">**Oggetto dinamico**</span><span class="sxs-lookup"><span data-stu-id="4be5b-210">**Dynamic-Object**</span></span>](c-dynamicobject.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="4be5b-211">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4be5b-211">Windows Server 2008</span></span>



| <span data-ttu-id="4be5b-212">Voce</span><span class="sxs-lookup"><span data-stu-id="4be5b-212">Entry</span></span> | <span data-ttu-id="4be5b-213">Valore</span><span class="sxs-lookup"><span data-stu-id="4be5b-213">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="4be5b-214">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="4be5b-214">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="4be5b-215">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4be5b-215">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="4be5b-216">System-Only</span><span class="sxs-lookup"><span data-stu-id="4be5b-216">System-Only</span></span>            | <span data-ttu-id="4be5b-217">Falso</span><span class="sxs-lookup"><span data-stu-id="4be5b-217">False</span></span>                                                |
| <span data-ttu-id="4be5b-218">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="4be5b-218">Is-Single-Valued</span></span>       | <span data-ttu-id="4be5b-219">Vero</span><span class="sxs-lookup"><span data-stu-id="4be5b-219">True</span></span>                                                 |
| <span data-ttu-id="4be5b-220">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="4be5b-220">Is Indexed</span></span>             | <span data-ttu-id="4be5b-221">Falso</span><span class="sxs-lookup"><span data-stu-id="4be5b-221">False</span></span>                                                |
| <span data-ttu-id="4be5b-222">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="4be5b-222">In Global Catalog</span></span>      | <span data-ttu-id="4be5b-223">Falso</span><span class="sxs-lookup"><span data-stu-id="4be5b-223">False</span></span>                                                |
| <span data-ttu-id="4be5b-224">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="4be5b-224">NT-Security-Descriptor</span></span> | <span data-ttu-id="4be5b-225">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="4be5b-225">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="4be5b-226">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4be5b-226">Range-Lower</span></span>            | <span data-ttu-id="4be5b-227">0</span><span class="sxs-lookup"><span data-stu-id="4be5b-227">0</span></span>                                                    |
| <span data-ttu-id="4be5b-228">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4be5b-228">Range-Upper</span></span>            | <span data-ttu-id="4be5b-229">31557600</span><span class="sxs-lookup"><span data-stu-id="4be5b-229">31557600</span></span>                                             |
| <span data-ttu-id="4be5b-230">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4be5b-230">Search-Flags</span></span>           | <span data-ttu-id="4be5b-231">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4be5b-231">0x00000000</span></span>                                           |
| <span data-ttu-id="4be5b-232">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4be5b-232">System-Flags</span></span>           | <span data-ttu-id="4be5b-233">0x00000014</span><span class="sxs-lookup"><span data-stu-id="4be5b-233">0x00000014</span></span>                                           |
| <span data-ttu-id="4be5b-234">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="4be5b-234">Classes used in</span></span>        | [<span data-ttu-id="4be5b-235">**Oggetto dinamico**</span><span class="sxs-lookup"><span data-stu-id="4be5b-235">**Dynamic-Object**</span></span>](c-dynamicobject.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="4be5b-236">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4be5b-236">Windows Server 2008 R2</span></span>



| <span data-ttu-id="4be5b-237">Voce</span><span class="sxs-lookup"><span data-stu-id="4be5b-237">Entry</span></span> | <span data-ttu-id="4be5b-238">Valore</span><span class="sxs-lookup"><span data-stu-id="4be5b-238">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="4be5b-239">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="4be5b-239">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="4be5b-240">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4be5b-240">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="4be5b-241">System-Only</span><span class="sxs-lookup"><span data-stu-id="4be5b-241">System-Only</span></span>            | <span data-ttu-id="4be5b-242">Falso</span><span class="sxs-lookup"><span data-stu-id="4be5b-242">False</span></span>                                                |
| <span data-ttu-id="4be5b-243">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="4be5b-243">Is-Single-Valued</span></span>       | <span data-ttu-id="4be5b-244">Vero</span><span class="sxs-lookup"><span data-stu-id="4be5b-244">True</span></span>                                                 |
| <span data-ttu-id="4be5b-245">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="4be5b-245">Is Indexed</span></span>             | <span data-ttu-id="4be5b-246">Falso</span><span class="sxs-lookup"><span data-stu-id="4be5b-246">False</span></span>                                                |
| <span data-ttu-id="4be5b-247">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="4be5b-247">In Global Catalog</span></span>      | <span data-ttu-id="4be5b-248">Falso</span><span class="sxs-lookup"><span data-stu-id="4be5b-248">False</span></span>                                                |
| <span data-ttu-id="4be5b-249">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="4be5b-249">NT-Security-Descriptor</span></span> | <span data-ttu-id="4be5b-250">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="4be5b-250">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="4be5b-251">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4be5b-251">Range-Lower</span></span>            | <span data-ttu-id="4be5b-252">0</span><span class="sxs-lookup"><span data-stu-id="4be5b-252">0</span></span>                                                    |
| <span data-ttu-id="4be5b-253">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4be5b-253">Range-Upper</span></span>            | <span data-ttu-id="4be5b-254">31557600</span><span class="sxs-lookup"><span data-stu-id="4be5b-254">31557600</span></span>                                             |
| <span data-ttu-id="4be5b-255">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4be5b-255">Search-Flags</span></span>           | <span data-ttu-id="4be5b-256">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4be5b-256">0x00000000</span></span>                                           |
| <span data-ttu-id="4be5b-257">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4be5b-257">System-Flags</span></span>           | <span data-ttu-id="4be5b-258">0x00000014</span><span class="sxs-lookup"><span data-stu-id="4be5b-258">0x00000014</span></span>                                           |
| <span data-ttu-id="4be5b-259">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="4be5b-259">Classes used in</span></span>        | [<span data-ttu-id="4be5b-260">**Oggetto dinamico**</span><span class="sxs-lookup"><span data-stu-id="4be5b-260">**Dynamic-Object**</span></span>](c-dynamicobject.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="4be5b-261">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4be5b-261">Windows Server 2012</span></span>



| <span data-ttu-id="4be5b-262">Voce</span><span class="sxs-lookup"><span data-stu-id="4be5b-262">Entry</span></span> | <span data-ttu-id="4be5b-263">Valore</span><span class="sxs-lookup"><span data-stu-id="4be5b-263">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="4be5b-264">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="4be5b-264">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="4be5b-265">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4be5b-265">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="4be5b-266">System-Only</span><span class="sxs-lookup"><span data-stu-id="4be5b-266">System-Only</span></span>            | <span data-ttu-id="4be5b-267">Falso</span><span class="sxs-lookup"><span data-stu-id="4be5b-267">False</span></span>                                                |
| <span data-ttu-id="4be5b-268">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="4be5b-268">Is-Single-Valued</span></span>       | <span data-ttu-id="4be5b-269">Vero</span><span class="sxs-lookup"><span data-stu-id="4be5b-269">True</span></span>                                                 |
| <span data-ttu-id="4be5b-270">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="4be5b-270">Is Indexed</span></span>             | <span data-ttu-id="4be5b-271">Falso</span><span class="sxs-lookup"><span data-stu-id="4be5b-271">False</span></span>                                                |
| <span data-ttu-id="4be5b-272">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="4be5b-272">In Global Catalog</span></span>      | <span data-ttu-id="4be5b-273">Falso</span><span class="sxs-lookup"><span data-stu-id="4be5b-273">False</span></span>                                                |
| <span data-ttu-id="4be5b-274">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="4be5b-274">NT-Security-Descriptor</span></span> | <span data-ttu-id="4be5b-275">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="4be5b-275">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="4be5b-276">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4be5b-276">Range-Lower</span></span>            | <span data-ttu-id="4be5b-277">0</span><span class="sxs-lookup"><span data-stu-id="4be5b-277">0</span></span>                                                    |
| <span data-ttu-id="4be5b-278">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4be5b-278">Range-Upper</span></span>            | <span data-ttu-id="4be5b-279">31557600</span><span class="sxs-lookup"><span data-stu-id="4be5b-279">31557600</span></span>                                             |
| <span data-ttu-id="4be5b-280">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4be5b-280">Search-Flags</span></span>           | <span data-ttu-id="4be5b-281">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4be5b-281">0x00000000</span></span>                                           |
| <span data-ttu-id="4be5b-282">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4be5b-282">System-Flags</span></span>           | <span data-ttu-id="4be5b-283">0x00000014</span><span class="sxs-lookup"><span data-stu-id="4be5b-283">0x00000014</span></span>                                           |
| <span data-ttu-id="4be5b-284">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="4be5b-284">Classes used in</span></span>        | [<span data-ttu-id="4be5b-285">**Oggetto dinamico**</span><span class="sxs-lookup"><span data-stu-id="4be5b-285">**Dynamic-Object**</span></span>](c-dynamicobject.md)<br/> |



 

 





