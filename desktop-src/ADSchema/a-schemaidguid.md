---
title: Attributo schema-ID-GUID
description: Identificatore univoco per un attributo.
ms.assetid: 50f0a4b6-dded-42db-9ac5-123f2885c658
ms.tgt_platform: multiple
keywords:
- Schema-ID-GUID attributo schema AD
- Schema AD dell'attributo schemaIDGUID
topic_type:
- apiref
api_name:
- Schema-ID-GUID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72f0b16cc45ecfbcd03e2104cbc6c5b5b41bd813
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104122347"
---
# <a name="schema-id-guid-attribute"></a><span data-ttu-id="9e446-105">Attributo schema-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="9e446-105">Schema-ID-GUID attribute</span></span>

<span data-ttu-id="9e446-106">Identificatore univoco per un attributo.</span><span class="sxs-lookup"><span data-stu-id="9e446-106">The unique identifier for an attribute.</span></span>



| <span data-ttu-id="9e446-107">Voce</span><span class="sxs-lookup"><span data-stu-id="9e446-107">Entry</span></span> | <span data-ttu-id="9e446-108">Valore</span><span class="sxs-lookup"><span data-stu-id="9e446-108">Value</span></span> |
|-------------------|---------------------------------------------------------------------|
| <span data-ttu-id="9e446-109">CN</span><span class="sxs-lookup"><span data-stu-id="9e446-109">CN</span></span>                | <span data-ttu-id="9e446-110">Schema-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="9e446-110">Schema-ID-GUID</span></span>                                                      |
| <span data-ttu-id="9e446-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="9e446-111">Ldap-Display-Name</span></span> | <span data-ttu-id="9e446-112">schemaIDGUID</span><span class="sxs-lookup"><span data-stu-id="9e446-112">schemaIDGUID</span></span>                                                        |
| <span data-ttu-id="9e446-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="9e446-113">Size</span></span>              | <span data-ttu-id="9e446-114">16 byte</span><span class="sxs-lookup"><span data-stu-id="9e446-114">16 bytes</span></span>                                                            |
| <span data-ttu-id="9e446-115">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="9e446-115">Update Privilege</span></span>  | <span data-ttu-id="9e446-116">Questo valore viene impostato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="9e446-116">This value is set by the system.</span></span>                                    |
| <span data-ttu-id="9e446-117">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="9e446-117">Update Frequency</span></span>  | <span data-ttu-id="9e446-118">Questo valore viene impostato quando l'oggetto viene creato e non può essere modificato.</span><span class="sxs-lookup"><span data-stu-id="9e446-118">This value is set when the object is created and cannot be changed.</span></span> |
| <span data-ttu-id="9e446-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="9e446-119">Attribute-Id</span></span>      | <span data-ttu-id="9e446-120">1.2.840.113556.1.4.148</span><span class="sxs-lookup"><span data-stu-id="9e446-120">1.2.840.113556.1.4.148</span></span>                                              |
| <span data-ttu-id="9e446-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="9e446-121">System-Id-Guid</span></span>    | <span data-ttu-id="9e446-122">bf967923-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="9e446-122">bf967923-0de6-11d0-a285-00aa003049e2</span></span>                                |
| <span data-ttu-id="9e446-123">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9e446-123">Syntax</span></span>            | [<span data-ttu-id="9e446-124">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="9e446-124">**Object(Replica-Link)**</span></span>](s-object-replica-link.md)               |



## <a name="implementations"></a><span data-ttu-id="9e446-125">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="9e446-125">Implementations</span></span>

-   [<span data-ttu-id="9e446-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="9e446-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="9e446-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="9e446-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="9e446-128">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="9e446-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="9e446-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="9e446-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="9e446-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="9e446-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="9e446-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="9e446-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="9e446-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="9e446-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="9e446-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9e446-133">Windows 2000 Server</span></span>



| <span data-ttu-id="9e446-134">Voce</span><span class="sxs-lookup"><span data-stu-id="9e446-134">Entry</span></span> | <span data-ttu-id="9e446-135">Valore</span><span class="sxs-lookup"><span data-stu-id="9e446-135">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e446-136">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="9e446-136">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="9e446-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9e446-137">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="9e446-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="9e446-138">System-Only</span></span>            | <span data-ttu-id="9e446-139">Vero</span><span class="sxs-lookup"><span data-stu-id="9e446-139">True</span></span>                                                                                                      |
| <span data-ttu-id="9e446-140">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="9e446-140">Is-Single-Valued</span></span>       | <span data-ttu-id="9e446-141">Vero</span><span class="sxs-lookup"><span data-stu-id="9e446-141">True</span></span>                                                                                                      |
| <span data-ttu-id="9e446-142">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="9e446-142">Is Indexed</span></span>             | <span data-ttu-id="9e446-143">Falso</span><span class="sxs-lookup"><span data-stu-id="9e446-143">False</span></span>                                                                                                     |
| <span data-ttu-id="9e446-144">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="9e446-144">In Global Catalog</span></span>      | <span data-ttu-id="9e446-145">Falso</span><span class="sxs-lookup"><span data-stu-id="9e446-145">False</span></span>                                                                                                     |
| <span data-ttu-id="9e446-146">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="9e446-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="9e446-147">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="9e446-147">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="9e446-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9e446-148">Range-Lower</span></span>            | <span data-ttu-id="9e446-149">16</span><span class="sxs-lookup"><span data-stu-id="9e446-149">16</span></span>                                                                                                        |
| <span data-ttu-id="9e446-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9e446-150">Range-Upper</span></span>            | <span data-ttu-id="9e446-151">16</span><span class="sxs-lookup"><span data-stu-id="9e446-151">16</span></span>                                                                                                        |
| <span data-ttu-id="9e446-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9e446-152">Search-Flags</span></span>           | <span data-ttu-id="9e446-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9e446-153">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="9e446-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9e446-154">System-Flags</span></span>           | <span data-ttu-id="9e446-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9e446-155">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="9e446-156">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="9e446-156">Classes used in</span></span>        | [<span data-ttu-id="9e446-157">**Attribute-schema**</span><span class="sxs-lookup"><span data-stu-id="9e446-157">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="9e446-158">**Classe-schema**</span><span class="sxs-lookup"><span data-stu-id="9e446-158">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="9e446-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9e446-159">Windows Server 2003</span></span>



| <span data-ttu-id="9e446-160">Voce</span><span class="sxs-lookup"><span data-stu-id="9e446-160">Entry</span></span> | <span data-ttu-id="9e446-161">Valore</span><span class="sxs-lookup"><span data-stu-id="9e446-161">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e446-162">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="9e446-162">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="9e446-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9e446-163">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="9e446-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="9e446-164">System-Only</span></span>            | <span data-ttu-id="9e446-165">Vero</span><span class="sxs-lookup"><span data-stu-id="9e446-165">True</span></span>                                                                                                      |
| <span data-ttu-id="9e446-166">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="9e446-166">Is-Single-Valued</span></span>       | <span data-ttu-id="9e446-167">Vero</span><span class="sxs-lookup"><span data-stu-id="9e446-167">True</span></span>                                                                                                      |
| <span data-ttu-id="9e446-168">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="9e446-168">Is Indexed</span></span>             | <span data-ttu-id="9e446-169">Falso</span><span class="sxs-lookup"><span data-stu-id="9e446-169">False</span></span>                                                                                                     |
| <span data-ttu-id="9e446-170">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="9e446-170">In Global Catalog</span></span>      | <span data-ttu-id="9e446-171">Falso</span><span class="sxs-lookup"><span data-stu-id="9e446-171">False</span></span>                                                                                                     |
| <span data-ttu-id="9e446-172">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="9e446-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="9e446-173">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="9e446-173">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="9e446-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9e446-174">Range-Lower</span></span>            | <span data-ttu-id="9e446-175">16</span><span class="sxs-lookup"><span data-stu-id="9e446-175">16</span></span>                                                                                                        |
| <span data-ttu-id="9e446-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9e446-176">Range-Upper</span></span>            | <span data-ttu-id="9e446-177">16</span><span class="sxs-lookup"><span data-stu-id="9e446-177">16</span></span>                                                                                                        |
| <span data-ttu-id="9e446-178">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9e446-178">Search-Flags</span></span>           | <span data-ttu-id="9e446-179">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9e446-179">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="9e446-180">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9e446-180">System-Flags</span></span>           | <span data-ttu-id="9e446-181">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9e446-181">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="9e446-182">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="9e446-182">Classes used in</span></span>        | [<span data-ttu-id="9e446-183">**Attribute-schema**</span><span class="sxs-lookup"><span data-stu-id="9e446-183">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="9e446-184">**Classe-schema**</span><span class="sxs-lookup"><span data-stu-id="9e446-184">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="9e446-185">ADAM</span><span class="sxs-lookup"><span data-stu-id="9e446-185">ADAM</span></span>



| <span data-ttu-id="9e446-186">Voce</span><span class="sxs-lookup"><span data-stu-id="9e446-186">Entry</span></span> | <span data-ttu-id="9e446-187">Valore</span><span class="sxs-lookup"><span data-stu-id="9e446-187">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e446-188">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="9e446-188">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="9e446-189">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9e446-189">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="9e446-190">System-Only</span><span class="sxs-lookup"><span data-stu-id="9e446-190">System-Only</span></span>            | <span data-ttu-id="9e446-191">Vero</span><span class="sxs-lookup"><span data-stu-id="9e446-191">True</span></span>                                                                                                      |
| <span data-ttu-id="9e446-192">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="9e446-192">Is-Single-Valued</span></span>       | <span data-ttu-id="9e446-193">Vero</span><span class="sxs-lookup"><span data-stu-id="9e446-193">True</span></span>                                                                                                      |
| <span data-ttu-id="9e446-194">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="9e446-194">Is Indexed</span></span>             | <span data-ttu-id="9e446-195">Falso</span><span class="sxs-lookup"><span data-stu-id="9e446-195">False</span></span>                                                                                                     |
| <span data-ttu-id="9e446-196">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="9e446-196">In Global Catalog</span></span>      | <span data-ttu-id="9e446-197">Falso</span><span class="sxs-lookup"><span data-stu-id="9e446-197">False</span></span>                                                                                                     |
| <span data-ttu-id="9e446-198">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="9e446-198">NT-Security-Descriptor</span></span> | <span data-ttu-id="9e446-199">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="9e446-199">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="9e446-200">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9e446-200">Range-Lower</span></span>            | <span data-ttu-id="9e446-201">16</span><span class="sxs-lookup"><span data-stu-id="9e446-201">16</span></span>                                                                                                        |
| <span data-ttu-id="9e446-202">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9e446-202">Range-Upper</span></span>            | <span data-ttu-id="9e446-203">16</span><span class="sxs-lookup"><span data-stu-id="9e446-203">16</span></span>                                                                                                        |
| <span data-ttu-id="9e446-204">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9e446-204">Search-Flags</span></span>           | <span data-ttu-id="9e446-205">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9e446-205">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="9e446-206">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9e446-206">System-Flags</span></span>           | <span data-ttu-id="9e446-207">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9e446-207">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="9e446-208">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="9e446-208">Classes used in</span></span>        | [<span data-ttu-id="9e446-209">**Attribute-schema**</span><span class="sxs-lookup"><span data-stu-id="9e446-209">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="9e446-210">**Classe-schema**</span><span class="sxs-lookup"><span data-stu-id="9e446-210">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="9e446-211">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="9e446-211">Windows Server 2003 R2</span></span>



| <span data-ttu-id="9e446-212">Voce</span><span class="sxs-lookup"><span data-stu-id="9e446-212">Entry</span></span> | <span data-ttu-id="9e446-213">Valore</span><span class="sxs-lookup"><span data-stu-id="9e446-213">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e446-214">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="9e446-214">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="9e446-215">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9e446-215">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="9e446-216">System-Only</span><span class="sxs-lookup"><span data-stu-id="9e446-216">System-Only</span></span>            | <span data-ttu-id="9e446-217">Vero</span><span class="sxs-lookup"><span data-stu-id="9e446-217">True</span></span>                                                                                                      |
| <span data-ttu-id="9e446-218">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="9e446-218">Is-Single-Valued</span></span>       | <span data-ttu-id="9e446-219">Vero</span><span class="sxs-lookup"><span data-stu-id="9e446-219">True</span></span>                                                                                                      |
| <span data-ttu-id="9e446-220">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="9e446-220">Is Indexed</span></span>             | <span data-ttu-id="9e446-221">Falso</span><span class="sxs-lookup"><span data-stu-id="9e446-221">False</span></span>                                                                                                     |
| <span data-ttu-id="9e446-222">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="9e446-222">In Global Catalog</span></span>      | <span data-ttu-id="9e446-223">Falso</span><span class="sxs-lookup"><span data-stu-id="9e446-223">False</span></span>                                                                                                     |
| <span data-ttu-id="9e446-224">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="9e446-224">NT-Security-Descriptor</span></span> | <span data-ttu-id="9e446-225">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="9e446-225">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="9e446-226">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9e446-226">Range-Lower</span></span>            | <span data-ttu-id="9e446-227">16</span><span class="sxs-lookup"><span data-stu-id="9e446-227">16</span></span>                                                                                                        |
| <span data-ttu-id="9e446-228">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9e446-228">Range-Upper</span></span>            | <span data-ttu-id="9e446-229">16</span><span class="sxs-lookup"><span data-stu-id="9e446-229">16</span></span>                                                                                                        |
| <span data-ttu-id="9e446-230">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9e446-230">Search-Flags</span></span>           | <span data-ttu-id="9e446-231">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9e446-231">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="9e446-232">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9e446-232">System-Flags</span></span>           | <span data-ttu-id="9e446-233">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9e446-233">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="9e446-234">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="9e446-234">Classes used in</span></span>        | [<span data-ttu-id="9e446-235">**Attribute-schema**</span><span class="sxs-lookup"><span data-stu-id="9e446-235">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="9e446-236">**Classe-schema**</span><span class="sxs-lookup"><span data-stu-id="9e446-236">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="9e446-237">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9e446-237">Windows Server 2008</span></span>



| <span data-ttu-id="9e446-238">Voce</span><span class="sxs-lookup"><span data-stu-id="9e446-238">Entry</span></span> | <span data-ttu-id="9e446-239">Valore</span><span class="sxs-lookup"><span data-stu-id="9e446-239">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e446-240">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="9e446-240">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="9e446-241">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9e446-241">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="9e446-242">System-Only</span><span class="sxs-lookup"><span data-stu-id="9e446-242">System-Only</span></span>            | <span data-ttu-id="9e446-243">Vero</span><span class="sxs-lookup"><span data-stu-id="9e446-243">True</span></span>                                                                                                      |
| <span data-ttu-id="9e446-244">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="9e446-244">Is-Single-Valued</span></span>       | <span data-ttu-id="9e446-245">Vero</span><span class="sxs-lookup"><span data-stu-id="9e446-245">True</span></span>                                                                                                      |
| <span data-ttu-id="9e446-246">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="9e446-246">Is Indexed</span></span>             | <span data-ttu-id="9e446-247">Falso</span><span class="sxs-lookup"><span data-stu-id="9e446-247">False</span></span>                                                                                                     |
| <span data-ttu-id="9e446-248">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="9e446-248">In Global Catalog</span></span>      | <span data-ttu-id="9e446-249">Falso</span><span class="sxs-lookup"><span data-stu-id="9e446-249">False</span></span>                                                                                                     |
| <span data-ttu-id="9e446-250">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="9e446-250">NT-Security-Descriptor</span></span> | <span data-ttu-id="9e446-251">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="9e446-251">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="9e446-252">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9e446-252">Range-Lower</span></span>            | <span data-ttu-id="9e446-253">16</span><span class="sxs-lookup"><span data-stu-id="9e446-253">16</span></span>                                                                                                        |
| <span data-ttu-id="9e446-254">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9e446-254">Range-Upper</span></span>            | <span data-ttu-id="9e446-255">16</span><span class="sxs-lookup"><span data-stu-id="9e446-255">16</span></span>                                                                                                        |
| <span data-ttu-id="9e446-256">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9e446-256">Search-Flags</span></span>           | <span data-ttu-id="9e446-257">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9e446-257">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="9e446-258">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9e446-258">System-Flags</span></span>           | <span data-ttu-id="9e446-259">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9e446-259">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="9e446-260">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="9e446-260">Classes used in</span></span>        | [<span data-ttu-id="9e446-261">**Attribute-schema**</span><span class="sxs-lookup"><span data-stu-id="9e446-261">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="9e446-262">**Classe-schema**</span><span class="sxs-lookup"><span data-stu-id="9e446-262">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="9e446-263">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9e446-263">Windows Server 2008 R2</span></span>



| <span data-ttu-id="9e446-264">Voce</span><span class="sxs-lookup"><span data-stu-id="9e446-264">Entry</span></span> | <span data-ttu-id="9e446-265">Valore</span><span class="sxs-lookup"><span data-stu-id="9e446-265">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e446-266">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="9e446-266">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="9e446-267">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9e446-267">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="9e446-268">System-Only</span><span class="sxs-lookup"><span data-stu-id="9e446-268">System-Only</span></span>            | <span data-ttu-id="9e446-269">Vero</span><span class="sxs-lookup"><span data-stu-id="9e446-269">True</span></span>                                                                                                      |
| <span data-ttu-id="9e446-270">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="9e446-270">Is-Single-Valued</span></span>       | <span data-ttu-id="9e446-271">Vero</span><span class="sxs-lookup"><span data-stu-id="9e446-271">True</span></span>                                                                                                      |
| <span data-ttu-id="9e446-272">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="9e446-272">Is Indexed</span></span>             | <span data-ttu-id="9e446-273">Falso</span><span class="sxs-lookup"><span data-stu-id="9e446-273">False</span></span>                                                                                                     |
| <span data-ttu-id="9e446-274">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="9e446-274">In Global Catalog</span></span>      | <span data-ttu-id="9e446-275">Falso</span><span class="sxs-lookup"><span data-stu-id="9e446-275">False</span></span>                                                                                                     |
| <span data-ttu-id="9e446-276">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="9e446-276">NT-Security-Descriptor</span></span> | <span data-ttu-id="9e446-277">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="9e446-277">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="9e446-278">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9e446-278">Range-Lower</span></span>            | <span data-ttu-id="9e446-279">16</span><span class="sxs-lookup"><span data-stu-id="9e446-279">16</span></span>                                                                                                        |
| <span data-ttu-id="9e446-280">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9e446-280">Range-Upper</span></span>            | <span data-ttu-id="9e446-281">16</span><span class="sxs-lookup"><span data-stu-id="9e446-281">16</span></span>                                                                                                        |
| <span data-ttu-id="9e446-282">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9e446-282">Search-Flags</span></span>           | <span data-ttu-id="9e446-283">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9e446-283">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="9e446-284">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9e446-284">System-Flags</span></span>           | <span data-ttu-id="9e446-285">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9e446-285">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="9e446-286">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="9e446-286">Classes used in</span></span>        | [<span data-ttu-id="9e446-287">**Attribute-schema**</span><span class="sxs-lookup"><span data-stu-id="9e446-287">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="9e446-288">**Classe-schema**</span><span class="sxs-lookup"><span data-stu-id="9e446-288">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="9e446-289">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9e446-289">Windows Server 2012</span></span>



| <span data-ttu-id="9e446-290">Voce</span><span class="sxs-lookup"><span data-stu-id="9e446-290">Entry</span></span> | <span data-ttu-id="9e446-291">Valore</span><span class="sxs-lookup"><span data-stu-id="9e446-291">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e446-292">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="9e446-292">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="9e446-293">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9e446-293">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="9e446-294">System-Only</span><span class="sxs-lookup"><span data-stu-id="9e446-294">System-Only</span></span>            | <span data-ttu-id="9e446-295">Vero</span><span class="sxs-lookup"><span data-stu-id="9e446-295">True</span></span>                                                                                                      |
| <span data-ttu-id="9e446-296">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="9e446-296">Is-Single-Valued</span></span>       | <span data-ttu-id="9e446-297">Vero</span><span class="sxs-lookup"><span data-stu-id="9e446-297">True</span></span>                                                                                                      |
| <span data-ttu-id="9e446-298">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="9e446-298">Is Indexed</span></span>             | <span data-ttu-id="9e446-299">Falso</span><span class="sxs-lookup"><span data-stu-id="9e446-299">False</span></span>                                                                                                     |
| <span data-ttu-id="9e446-300">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="9e446-300">In Global Catalog</span></span>      | <span data-ttu-id="9e446-301">Falso</span><span class="sxs-lookup"><span data-stu-id="9e446-301">False</span></span>                                                                                                     |
| <span data-ttu-id="9e446-302">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="9e446-302">NT-Security-Descriptor</span></span> | <span data-ttu-id="9e446-303">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="9e446-303">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="9e446-304">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9e446-304">Range-Lower</span></span>            | <span data-ttu-id="9e446-305">16</span><span class="sxs-lookup"><span data-stu-id="9e446-305">16</span></span>                                                                                                        |
| <span data-ttu-id="9e446-306">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9e446-306">Range-Upper</span></span>            | <span data-ttu-id="9e446-307">16</span><span class="sxs-lookup"><span data-stu-id="9e446-307">16</span></span>                                                                                                        |
| <span data-ttu-id="9e446-308">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9e446-308">Search-Flags</span></span>           | <span data-ttu-id="9e446-309">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9e446-309">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="9e446-310">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9e446-310">System-Flags</span></span>           | <span data-ttu-id="9e446-311">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9e446-311">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="9e446-312">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="9e446-312">Classes used in</span></span>        | [<span data-ttu-id="9e446-313">**Attribute-schema**</span><span class="sxs-lookup"><span data-stu-id="9e446-313">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="9e446-314">**Classe-schema**</span><span class="sxs-lookup"><span data-stu-id="9e446-314">**Class-Schema**</span></span>](c-classschema.md)<br/> |



 

 





