---
title: Attributo Applies-To
description: Contiene l'elenco di classi di oggetti a cui si applica il diritto esteso. Nell'elenco una classe di oggetti è rappresentata dalla proprietà schemaIDGUID per il relativo oggetto schemaClass.
ms.assetid: 8333e508-627c-42ce-865b-db061a5603db
ms.tgt_platform: multiple
keywords:
- Schema AD Applies-To attribute
- Schema AD dell'attributo appliesTo
topic_type:
- apiref
api_name:
- Applies-To
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37b96a2690f420259b038b54b6d2b070b41f56d4
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104123198"
---
# <a name="applies-to-attribute"></a><span data-ttu-id="4055c-106">Attributo Applies-To</span><span class="sxs-lookup"><span data-stu-id="4055c-106">Applies-To attribute</span></span>

<span data-ttu-id="4055c-107">Contiene l'elenco di classi di oggetti a cui si applica il diritto esteso.</span><span class="sxs-lookup"><span data-stu-id="4055c-107">Contains the list of object classes that the extended right applies to.</span></span> <span data-ttu-id="4055c-108">Nell'elenco una classe di oggetti è rappresentata dalla proprietà schemaIDGUID per il relativo oggetto schemaClass.</span><span class="sxs-lookup"><span data-stu-id="4055c-108">In the list, an object class is represented by the schemaIDGUID property for its schemaClass object.</span></span>



| <span data-ttu-id="4055c-109">Voce</span><span class="sxs-lookup"><span data-stu-id="4055c-109">Entry</span></span> | <span data-ttu-id="4055c-110">Valore</span><span class="sxs-lookup"><span data-stu-id="4055c-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="4055c-111">CN</span><span class="sxs-lookup"><span data-stu-id="4055c-111">CN</span></span>                | <span data-ttu-id="4055c-112">Applies-To</span><span class="sxs-lookup"><span data-stu-id="4055c-112">Applies-To</span></span>                                  |
| <span data-ttu-id="4055c-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="4055c-113">Ldap-Display-Name</span></span> | <span data-ttu-id="4055c-114">appliesTo</span><span class="sxs-lookup"><span data-stu-id="4055c-114">appliesTo</span></span>                                   |
| <span data-ttu-id="4055c-115">Dimensione</span><span class="sxs-lookup"><span data-stu-id="4055c-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="4055c-116">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="4055c-116">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="4055c-117">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="4055c-117">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="4055c-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="4055c-118">Attribute-Id</span></span>      | <span data-ttu-id="4055c-119">1.2.840.113556.1.4.341</span><span class="sxs-lookup"><span data-stu-id="4055c-119">1.2.840.113556.1.4.341</span></span>                      |
| <span data-ttu-id="4055c-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="4055c-120">System-Id-Guid</span></span>    | <span data-ttu-id="4055c-121">8297931d-86d3-11d0-afda-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="4055c-121">8297931d-86d3-11d0-afda-00c04fd930c9</span></span>        |
| <span data-ttu-id="4055c-122">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4055c-122">Syntax</span></span>            | [<span data-ttu-id="4055c-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="4055c-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="4055c-124">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="4055c-124">Implementations</span></span>

-   [<span data-ttu-id="4055c-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="4055c-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="4055c-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="4055c-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="4055c-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="4055c-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="4055c-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="4055c-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="4055c-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="4055c-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="4055c-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="4055c-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="4055c-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="4055c-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="4055c-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4055c-132">Windows 2000 Server</span></span>



| <span data-ttu-id="4055c-133">Voce</span><span class="sxs-lookup"><span data-stu-id="4055c-133">Entry</span></span> | <span data-ttu-id="4055c-134">Valore</span><span class="sxs-lookup"><span data-stu-id="4055c-134">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="4055c-135">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="4055c-135">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="4055c-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4055c-136">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="4055c-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="4055c-137">System-Only</span></span>            | <span data-ttu-id="4055c-138">Falso</span><span class="sxs-lookup"><span data-stu-id="4055c-138">False</span></span>                                                           |
| <span data-ttu-id="4055c-139">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="4055c-139">Is-Single-Valued</span></span>       | <span data-ttu-id="4055c-140">Falso</span><span class="sxs-lookup"><span data-stu-id="4055c-140">False</span></span>                                                           |
| <span data-ttu-id="4055c-141">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="4055c-141">Is Indexed</span></span>             | <span data-ttu-id="4055c-142">Falso</span><span class="sxs-lookup"><span data-stu-id="4055c-142">False</span></span>                                                           |
| <span data-ttu-id="4055c-143">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="4055c-143">In Global Catalog</span></span>      | <span data-ttu-id="4055c-144">Falso</span><span class="sxs-lookup"><span data-stu-id="4055c-144">False</span></span>                                                           |
| <span data-ttu-id="4055c-145">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="4055c-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="4055c-146">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="4055c-146">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="4055c-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4055c-147">Range-Lower</span></span>            | <span data-ttu-id="4055c-148">36</span><span class="sxs-lookup"><span data-stu-id="4055c-148">36</span></span>                                                              |
| <span data-ttu-id="4055c-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4055c-149">Range-Upper</span></span>            | <span data-ttu-id="4055c-150">36</span><span class="sxs-lookup"><span data-stu-id="4055c-150">36</span></span>                                                              |
| <span data-ttu-id="4055c-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4055c-151">Search-Flags</span></span>           | <span data-ttu-id="4055c-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4055c-152">0x00000000</span></span>                                                      |
| <span data-ttu-id="4055c-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4055c-153">System-Flags</span></span>           | <span data-ttu-id="4055c-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4055c-154">0x00000010</span></span>                                                      |
| <span data-ttu-id="4055c-155">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="4055c-155">Classes used in</span></span>        | [<span data-ttu-id="4055c-156">**Controllo-accesso-a destra**</span><span class="sxs-lookup"><span data-stu-id="4055c-156">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="4055c-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4055c-157">Windows Server 2003</span></span>



| <span data-ttu-id="4055c-158">Voce</span><span class="sxs-lookup"><span data-stu-id="4055c-158">Entry</span></span> | <span data-ttu-id="4055c-159">Valore</span><span class="sxs-lookup"><span data-stu-id="4055c-159">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="4055c-160">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="4055c-160">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="4055c-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4055c-161">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="4055c-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="4055c-162">System-Only</span></span>            | <span data-ttu-id="4055c-163">Falso</span><span class="sxs-lookup"><span data-stu-id="4055c-163">False</span></span>                                                           |
| <span data-ttu-id="4055c-164">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="4055c-164">Is-Single-Valued</span></span>       | <span data-ttu-id="4055c-165">Falso</span><span class="sxs-lookup"><span data-stu-id="4055c-165">False</span></span>                                                           |
| <span data-ttu-id="4055c-166">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="4055c-166">Is Indexed</span></span>             | <span data-ttu-id="4055c-167">Falso</span><span class="sxs-lookup"><span data-stu-id="4055c-167">False</span></span>                                                           |
| <span data-ttu-id="4055c-168">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="4055c-168">In Global Catalog</span></span>      | <span data-ttu-id="4055c-169">Falso</span><span class="sxs-lookup"><span data-stu-id="4055c-169">False</span></span>                                                           |
| <span data-ttu-id="4055c-170">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="4055c-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="4055c-171">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="4055c-171">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="4055c-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4055c-172">Range-Lower</span></span>            | <span data-ttu-id="4055c-173">36</span><span class="sxs-lookup"><span data-stu-id="4055c-173">36</span></span>                                                              |
| <span data-ttu-id="4055c-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4055c-174">Range-Upper</span></span>            | <span data-ttu-id="4055c-175">36</span><span class="sxs-lookup"><span data-stu-id="4055c-175">36</span></span>                                                              |
| <span data-ttu-id="4055c-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4055c-176">Search-Flags</span></span>           | <span data-ttu-id="4055c-177">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4055c-177">0x00000000</span></span>                                                      |
| <span data-ttu-id="4055c-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4055c-178">System-Flags</span></span>           | <span data-ttu-id="4055c-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4055c-179">0x00000010</span></span>                                                      |
| <span data-ttu-id="4055c-180">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="4055c-180">Classes used in</span></span>        | [<span data-ttu-id="4055c-181">**Controllo-accesso-a destra**</span><span class="sxs-lookup"><span data-stu-id="4055c-181">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="adam"></a><span data-ttu-id="4055c-182">ADAM</span><span class="sxs-lookup"><span data-stu-id="4055c-182">ADAM</span></span>



| <span data-ttu-id="4055c-183">Voce</span><span class="sxs-lookup"><span data-stu-id="4055c-183">Entry</span></span> | <span data-ttu-id="4055c-184">Valore</span><span class="sxs-lookup"><span data-stu-id="4055c-184">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="4055c-185">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="4055c-185">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="4055c-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4055c-186">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="4055c-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="4055c-187">System-Only</span></span>            | <span data-ttu-id="4055c-188">Falso</span><span class="sxs-lookup"><span data-stu-id="4055c-188">False</span></span>                                                           |
| <span data-ttu-id="4055c-189">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="4055c-189">Is-Single-Valued</span></span>       | <span data-ttu-id="4055c-190">Falso</span><span class="sxs-lookup"><span data-stu-id="4055c-190">False</span></span>                                                           |
| <span data-ttu-id="4055c-191">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="4055c-191">Is Indexed</span></span>             | <span data-ttu-id="4055c-192">Falso</span><span class="sxs-lookup"><span data-stu-id="4055c-192">False</span></span>                                                           |
| <span data-ttu-id="4055c-193">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="4055c-193">In Global Catalog</span></span>      | <span data-ttu-id="4055c-194">Falso</span><span class="sxs-lookup"><span data-stu-id="4055c-194">False</span></span>                                                           |
| <span data-ttu-id="4055c-195">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="4055c-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="4055c-196">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="4055c-196">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="4055c-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4055c-197">Range-Lower</span></span>            | <span data-ttu-id="4055c-198">36</span><span class="sxs-lookup"><span data-stu-id="4055c-198">36</span></span>                                                              |
| <span data-ttu-id="4055c-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4055c-199">Range-Upper</span></span>            | <span data-ttu-id="4055c-200">36</span><span class="sxs-lookup"><span data-stu-id="4055c-200">36</span></span>                                                              |
| <span data-ttu-id="4055c-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4055c-201">Search-Flags</span></span>           | <span data-ttu-id="4055c-202">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4055c-202">0x00000000</span></span>                                                      |
| <span data-ttu-id="4055c-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4055c-203">System-Flags</span></span>           | <span data-ttu-id="4055c-204">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4055c-204">0x00000010</span></span>                                                      |
| <span data-ttu-id="4055c-205">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="4055c-205">Classes used in</span></span>        | [<span data-ttu-id="4055c-206">**Controllo-accesso-a destra**</span><span class="sxs-lookup"><span data-stu-id="4055c-206">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="4055c-207">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="4055c-207">Windows Server 2003 R2</span></span>



| <span data-ttu-id="4055c-208">Voce</span><span class="sxs-lookup"><span data-stu-id="4055c-208">Entry</span></span> | <span data-ttu-id="4055c-209">Valore</span><span class="sxs-lookup"><span data-stu-id="4055c-209">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="4055c-210">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="4055c-210">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="4055c-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4055c-211">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="4055c-212">System-Only</span><span class="sxs-lookup"><span data-stu-id="4055c-212">System-Only</span></span>            | <span data-ttu-id="4055c-213">Falso</span><span class="sxs-lookup"><span data-stu-id="4055c-213">False</span></span>                                                           |
| <span data-ttu-id="4055c-214">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="4055c-214">Is-Single-Valued</span></span>       | <span data-ttu-id="4055c-215">Falso</span><span class="sxs-lookup"><span data-stu-id="4055c-215">False</span></span>                                                           |
| <span data-ttu-id="4055c-216">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="4055c-216">Is Indexed</span></span>             | <span data-ttu-id="4055c-217">Falso</span><span class="sxs-lookup"><span data-stu-id="4055c-217">False</span></span>                                                           |
| <span data-ttu-id="4055c-218">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="4055c-218">In Global Catalog</span></span>      | <span data-ttu-id="4055c-219">Falso</span><span class="sxs-lookup"><span data-stu-id="4055c-219">False</span></span>                                                           |
| <span data-ttu-id="4055c-220">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="4055c-220">NT-Security-Descriptor</span></span> | <span data-ttu-id="4055c-221">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="4055c-221">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="4055c-222">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4055c-222">Range-Lower</span></span>            | <span data-ttu-id="4055c-223">36</span><span class="sxs-lookup"><span data-stu-id="4055c-223">36</span></span>                                                              |
| <span data-ttu-id="4055c-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4055c-224">Range-Upper</span></span>            | <span data-ttu-id="4055c-225">36</span><span class="sxs-lookup"><span data-stu-id="4055c-225">36</span></span>                                                              |
| <span data-ttu-id="4055c-226">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4055c-226">Search-Flags</span></span>           | <span data-ttu-id="4055c-227">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4055c-227">0x00000000</span></span>                                                      |
| <span data-ttu-id="4055c-228">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4055c-228">System-Flags</span></span>           | <span data-ttu-id="4055c-229">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4055c-229">0x00000010</span></span>                                                      |
| <span data-ttu-id="4055c-230">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="4055c-230">Classes used in</span></span>        | [<span data-ttu-id="4055c-231">**Controllo-accesso-a destra**</span><span class="sxs-lookup"><span data-stu-id="4055c-231">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="4055c-232">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4055c-232">Windows Server 2008</span></span>



| <span data-ttu-id="4055c-233">Voce</span><span class="sxs-lookup"><span data-stu-id="4055c-233">Entry</span></span> | <span data-ttu-id="4055c-234">Valore</span><span class="sxs-lookup"><span data-stu-id="4055c-234">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="4055c-235">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="4055c-235">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="4055c-236">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4055c-236">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="4055c-237">System-Only</span><span class="sxs-lookup"><span data-stu-id="4055c-237">System-Only</span></span>            | <span data-ttu-id="4055c-238">Falso</span><span class="sxs-lookup"><span data-stu-id="4055c-238">False</span></span>                                                           |
| <span data-ttu-id="4055c-239">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="4055c-239">Is-Single-Valued</span></span>       | <span data-ttu-id="4055c-240">Falso</span><span class="sxs-lookup"><span data-stu-id="4055c-240">False</span></span>                                                           |
| <span data-ttu-id="4055c-241">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="4055c-241">Is Indexed</span></span>             | <span data-ttu-id="4055c-242">Falso</span><span class="sxs-lookup"><span data-stu-id="4055c-242">False</span></span>                                                           |
| <span data-ttu-id="4055c-243">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="4055c-243">In Global Catalog</span></span>      | <span data-ttu-id="4055c-244">Falso</span><span class="sxs-lookup"><span data-stu-id="4055c-244">False</span></span>                                                           |
| <span data-ttu-id="4055c-245">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="4055c-245">NT-Security-Descriptor</span></span> | <span data-ttu-id="4055c-246">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="4055c-246">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="4055c-247">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4055c-247">Range-Lower</span></span>            | <span data-ttu-id="4055c-248">36</span><span class="sxs-lookup"><span data-stu-id="4055c-248">36</span></span>                                                              |
| <span data-ttu-id="4055c-249">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4055c-249">Range-Upper</span></span>            | <span data-ttu-id="4055c-250">36</span><span class="sxs-lookup"><span data-stu-id="4055c-250">36</span></span>                                                              |
| <span data-ttu-id="4055c-251">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4055c-251">Search-Flags</span></span>           | <span data-ttu-id="4055c-252">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4055c-252">0x00000000</span></span>                                                      |
| <span data-ttu-id="4055c-253">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4055c-253">System-Flags</span></span>           | <span data-ttu-id="4055c-254">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4055c-254">0x00000010</span></span>                                                      |
| <span data-ttu-id="4055c-255">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="4055c-255">Classes used in</span></span>        | [<span data-ttu-id="4055c-256">**Controllo-accesso-a destra**</span><span class="sxs-lookup"><span data-stu-id="4055c-256">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="4055c-257">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4055c-257">Windows Server 2008 R2</span></span>



| <span data-ttu-id="4055c-258">Voce</span><span class="sxs-lookup"><span data-stu-id="4055c-258">Entry</span></span> | <span data-ttu-id="4055c-259">Valore</span><span class="sxs-lookup"><span data-stu-id="4055c-259">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="4055c-260">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="4055c-260">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="4055c-261">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4055c-261">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="4055c-262">System-Only</span><span class="sxs-lookup"><span data-stu-id="4055c-262">System-Only</span></span>            | <span data-ttu-id="4055c-263">Falso</span><span class="sxs-lookup"><span data-stu-id="4055c-263">False</span></span>                                                           |
| <span data-ttu-id="4055c-264">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="4055c-264">Is-Single-Valued</span></span>       | <span data-ttu-id="4055c-265">Falso</span><span class="sxs-lookup"><span data-stu-id="4055c-265">False</span></span>                                                           |
| <span data-ttu-id="4055c-266">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="4055c-266">Is Indexed</span></span>             | <span data-ttu-id="4055c-267">Falso</span><span class="sxs-lookup"><span data-stu-id="4055c-267">False</span></span>                                                           |
| <span data-ttu-id="4055c-268">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="4055c-268">In Global Catalog</span></span>      | <span data-ttu-id="4055c-269">Falso</span><span class="sxs-lookup"><span data-stu-id="4055c-269">False</span></span>                                                           |
| <span data-ttu-id="4055c-270">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="4055c-270">NT-Security-Descriptor</span></span> | <span data-ttu-id="4055c-271">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="4055c-271">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="4055c-272">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4055c-272">Range-Lower</span></span>            | <span data-ttu-id="4055c-273">36</span><span class="sxs-lookup"><span data-stu-id="4055c-273">36</span></span>                                                              |
| <span data-ttu-id="4055c-274">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4055c-274">Range-Upper</span></span>            | <span data-ttu-id="4055c-275">36</span><span class="sxs-lookup"><span data-stu-id="4055c-275">36</span></span>                                                              |
| <span data-ttu-id="4055c-276">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4055c-276">Search-Flags</span></span>           | <span data-ttu-id="4055c-277">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4055c-277">0x00000000</span></span>                                                      |
| <span data-ttu-id="4055c-278">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4055c-278">System-Flags</span></span>           | <span data-ttu-id="4055c-279">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4055c-279">0x00000010</span></span>                                                      |
| <span data-ttu-id="4055c-280">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="4055c-280">Classes used in</span></span>        | [<span data-ttu-id="4055c-281">**Controllo-accesso-a destra**</span><span class="sxs-lookup"><span data-stu-id="4055c-281">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="4055c-282">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4055c-282">Windows Server 2012</span></span>



| <span data-ttu-id="4055c-283">Voce</span><span class="sxs-lookup"><span data-stu-id="4055c-283">Entry</span></span> | <span data-ttu-id="4055c-284">Valore</span><span class="sxs-lookup"><span data-stu-id="4055c-284">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="4055c-285">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="4055c-285">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="4055c-286">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4055c-286">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="4055c-287">System-Only</span><span class="sxs-lookup"><span data-stu-id="4055c-287">System-Only</span></span>            | <span data-ttu-id="4055c-288">Falso</span><span class="sxs-lookup"><span data-stu-id="4055c-288">False</span></span>                                                           |
| <span data-ttu-id="4055c-289">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="4055c-289">Is-Single-Valued</span></span>       | <span data-ttu-id="4055c-290">Falso</span><span class="sxs-lookup"><span data-stu-id="4055c-290">False</span></span>                                                           |
| <span data-ttu-id="4055c-291">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="4055c-291">Is Indexed</span></span>             | <span data-ttu-id="4055c-292">Falso</span><span class="sxs-lookup"><span data-stu-id="4055c-292">False</span></span>                                                           |
| <span data-ttu-id="4055c-293">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="4055c-293">In Global Catalog</span></span>      | <span data-ttu-id="4055c-294">Falso</span><span class="sxs-lookup"><span data-stu-id="4055c-294">False</span></span>                                                           |
| <span data-ttu-id="4055c-295">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="4055c-295">NT-Security-Descriptor</span></span> | <span data-ttu-id="4055c-296">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="4055c-296">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="4055c-297">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4055c-297">Range-Lower</span></span>            | <span data-ttu-id="4055c-298">36</span><span class="sxs-lookup"><span data-stu-id="4055c-298">36</span></span>                                                              |
| <span data-ttu-id="4055c-299">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4055c-299">Range-Upper</span></span>            | <span data-ttu-id="4055c-300">36</span><span class="sxs-lookup"><span data-stu-id="4055c-300">36</span></span>                                                              |
| <span data-ttu-id="4055c-301">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4055c-301">Search-Flags</span></span>           | <span data-ttu-id="4055c-302">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4055c-302">0x00000000</span></span>                                                      |
| <span data-ttu-id="4055c-303">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4055c-303">System-Flags</span></span>           | <span data-ttu-id="4055c-304">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4055c-304">0x00000010</span></span>                                                      |
| <span data-ttu-id="4055c-305">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="4055c-305">Classes used in</span></span>        | [<span data-ttu-id="4055c-306">**Controllo-accesso-a destra**</span><span class="sxs-lookup"><span data-stu-id="4055c-306">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



 

 





