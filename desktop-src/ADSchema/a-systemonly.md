---
title: Attributo System-Only
description: Valore booleano che specifica se solo Active Directory possibile modificare la classe. Solo le classi di sistema possono essere create o eliminate dall'agente del sistema di directory.
ms.assetid: 78d2da1f-bdf1-452b-bc64-78088f3630dd
ms.tgt_platform: multiple
keywords:
- Schema AD System-Only attribute
- Schema AD dell'attributo systemOnly
topic_type:
- apiref
api_name:
- System-Only
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1310eb5f13da3c17c20ac9c01f337ff2a018a545
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103875142"
---
# <a name="system-only-attribute"></a><span data-ttu-id="83e4f-106">Attributo System-Only</span><span class="sxs-lookup"><span data-stu-id="83e4f-106">System-Only attribute</span></span>

<span data-ttu-id="83e4f-107">Valore booleano che specifica se solo Active Directory possibile modificare la classe.</span><span class="sxs-lookup"><span data-stu-id="83e4f-107">A Boolean value that specifies whether only Active Directory can modify the class.</span></span> <span data-ttu-id="83e4f-108">Solo le classi di sistema possono essere create o eliminate dall'agente del sistema di directory.</span><span class="sxs-lookup"><span data-stu-id="83e4f-108">System-only classes can only be created or deleted by the Directory System Agent.</span></span>



| <span data-ttu-id="83e4f-109">Voce</span><span class="sxs-lookup"><span data-stu-id="83e4f-109">Entry</span></span> | <span data-ttu-id="83e4f-110">Valore</span><span class="sxs-lookup"><span data-stu-id="83e4f-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="83e4f-111">CN</span><span class="sxs-lookup"><span data-stu-id="83e4f-111">CN</span></span>                | <span data-ttu-id="83e4f-112">System-Only</span><span class="sxs-lookup"><span data-stu-id="83e4f-112">System-Only</span></span>                          |
| <span data-ttu-id="83e4f-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="83e4f-113">Ldap-Display-Name</span></span> | <span data-ttu-id="83e4f-114">systemOnly</span><span class="sxs-lookup"><span data-stu-id="83e4f-114">systemOnly</span></span>                           |
| <span data-ttu-id="83e4f-115">Dimensione</span><span class="sxs-lookup"><span data-stu-id="83e4f-115">Size</span></span>              | <span data-ttu-id="83e4f-116">4 byte</span><span class="sxs-lookup"><span data-stu-id="83e4f-116">4 bytes</span></span>                              |
| <span data-ttu-id="83e4f-117">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="83e4f-117">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="83e4f-118">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="83e4f-118">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="83e4f-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="83e4f-119">Attribute-Id</span></span>      | <span data-ttu-id="83e4f-120">1.2.840.113556.1.4.170</span><span class="sxs-lookup"><span data-stu-id="83e4f-120">1.2.840.113556.1.4.170</span></span>               |
| <span data-ttu-id="83e4f-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="83e4f-121">System-Id-Guid</span></span>    | <span data-ttu-id="83e4f-122">bf967a46-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="83e4f-122">bf967a46-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="83e4f-123">Sintassi</span><span class="sxs-lookup"><span data-stu-id="83e4f-123">Syntax</span></span>            | [<span data-ttu-id="83e4f-124">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="83e4f-124">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="83e4f-125">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="83e4f-125">Implementations</span></span>

-   [<span data-ttu-id="83e4f-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="83e4f-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="83e4f-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="83e4f-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="83e4f-128">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="83e4f-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="83e4f-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="83e4f-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="83e4f-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="83e4f-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="83e4f-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="83e4f-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="83e4f-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="83e4f-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="83e4f-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="83e4f-133">Windows 2000 Server</span></span>



| <span data-ttu-id="83e4f-134">Voce</span><span class="sxs-lookup"><span data-stu-id="83e4f-134">Entry</span></span> | <span data-ttu-id="83e4f-135">Valore</span><span class="sxs-lookup"><span data-stu-id="83e4f-135">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83e4f-136">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="83e4f-136">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="83e4f-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="83e4f-137">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="83e4f-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="83e4f-138">System-Only</span></span>            | <span data-ttu-id="83e4f-139">Vero</span><span class="sxs-lookup"><span data-stu-id="83e4f-139">True</span></span>                                                                                                      |
| <span data-ttu-id="83e4f-140">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="83e4f-140">Is-Single-Valued</span></span>       | <span data-ttu-id="83e4f-141">Vero</span><span class="sxs-lookup"><span data-stu-id="83e4f-141">True</span></span>                                                                                                      |
| <span data-ttu-id="83e4f-142">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="83e4f-142">Is Indexed</span></span>             | <span data-ttu-id="83e4f-143">Falso</span><span class="sxs-lookup"><span data-stu-id="83e4f-143">False</span></span>                                                                                                     |
| <span data-ttu-id="83e4f-144">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="83e4f-144">In Global Catalog</span></span>      | <span data-ttu-id="83e4f-145">Falso</span><span class="sxs-lookup"><span data-stu-id="83e4f-145">False</span></span>                                                                                                     |
| <span data-ttu-id="83e4f-146">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="83e4f-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="83e4f-147">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="83e4f-147">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="83e4f-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="83e4f-148">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="83e4f-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="83e4f-149">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="83e4f-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="83e4f-150">Search-Flags</span></span>           | <span data-ttu-id="83e4f-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="83e4f-151">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="83e4f-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="83e4f-152">System-Flags</span></span>           | <span data-ttu-id="83e4f-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="83e4f-153">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="83e4f-154">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="83e4f-154">Classes used in</span></span>        | [<span data-ttu-id="83e4f-155">**Attribute-schema**</span><span class="sxs-lookup"><span data-stu-id="83e4f-155">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="83e4f-156">**Classe-schema**</span><span class="sxs-lookup"><span data-stu-id="83e4f-156">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="83e4f-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="83e4f-157">Windows Server 2003</span></span>



| <span data-ttu-id="83e4f-158">Voce</span><span class="sxs-lookup"><span data-stu-id="83e4f-158">Entry</span></span> | <span data-ttu-id="83e4f-159">Valore</span><span class="sxs-lookup"><span data-stu-id="83e4f-159">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83e4f-160">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="83e4f-160">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="83e4f-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="83e4f-161">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="83e4f-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="83e4f-162">System-Only</span></span>            | <span data-ttu-id="83e4f-163">Vero</span><span class="sxs-lookup"><span data-stu-id="83e4f-163">True</span></span>                                                                                                      |
| <span data-ttu-id="83e4f-164">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="83e4f-164">Is-Single-Valued</span></span>       | <span data-ttu-id="83e4f-165">Vero</span><span class="sxs-lookup"><span data-stu-id="83e4f-165">True</span></span>                                                                                                      |
| <span data-ttu-id="83e4f-166">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="83e4f-166">Is Indexed</span></span>             | <span data-ttu-id="83e4f-167">Falso</span><span class="sxs-lookup"><span data-stu-id="83e4f-167">False</span></span>                                                                                                     |
| <span data-ttu-id="83e4f-168">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="83e4f-168">In Global Catalog</span></span>      | <span data-ttu-id="83e4f-169">Falso</span><span class="sxs-lookup"><span data-stu-id="83e4f-169">False</span></span>                                                                                                     |
| <span data-ttu-id="83e4f-170">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="83e4f-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="83e4f-171">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="83e4f-171">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="83e4f-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="83e4f-172">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="83e4f-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="83e4f-173">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="83e4f-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="83e4f-174">Search-Flags</span></span>           | <span data-ttu-id="83e4f-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="83e4f-175">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="83e4f-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="83e4f-176">System-Flags</span></span>           | <span data-ttu-id="83e4f-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="83e4f-177">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="83e4f-178">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="83e4f-178">Classes used in</span></span>        | [<span data-ttu-id="83e4f-179">**Attribute-schema**</span><span class="sxs-lookup"><span data-stu-id="83e4f-179">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="83e4f-180">**Classe-schema**</span><span class="sxs-lookup"><span data-stu-id="83e4f-180">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="83e4f-181">ADAM</span><span class="sxs-lookup"><span data-stu-id="83e4f-181">ADAM</span></span>



| <span data-ttu-id="83e4f-182">Voce</span><span class="sxs-lookup"><span data-stu-id="83e4f-182">Entry</span></span> | <span data-ttu-id="83e4f-183">Valore</span><span class="sxs-lookup"><span data-stu-id="83e4f-183">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83e4f-184">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="83e4f-184">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="83e4f-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="83e4f-185">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="83e4f-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="83e4f-186">System-Only</span></span>            | <span data-ttu-id="83e4f-187">Vero</span><span class="sxs-lookup"><span data-stu-id="83e4f-187">True</span></span>                                                                                                      |
| <span data-ttu-id="83e4f-188">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="83e4f-188">Is-Single-Valued</span></span>       | <span data-ttu-id="83e4f-189">Vero</span><span class="sxs-lookup"><span data-stu-id="83e4f-189">True</span></span>                                                                                                      |
| <span data-ttu-id="83e4f-190">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="83e4f-190">Is Indexed</span></span>             | <span data-ttu-id="83e4f-191">Falso</span><span class="sxs-lookup"><span data-stu-id="83e4f-191">False</span></span>                                                                                                     |
| <span data-ttu-id="83e4f-192">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="83e4f-192">In Global Catalog</span></span>      | <span data-ttu-id="83e4f-193">Falso</span><span class="sxs-lookup"><span data-stu-id="83e4f-193">False</span></span>                                                                                                     |
| <span data-ttu-id="83e4f-194">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="83e4f-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="83e4f-195">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="83e4f-195">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="83e4f-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="83e4f-196">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="83e4f-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="83e4f-197">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="83e4f-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="83e4f-198">Search-Flags</span></span>           | <span data-ttu-id="83e4f-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="83e4f-199">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="83e4f-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="83e4f-200">System-Flags</span></span>           | <span data-ttu-id="83e4f-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="83e4f-201">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="83e4f-202">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="83e4f-202">Classes used in</span></span>        | [<span data-ttu-id="83e4f-203">**Attribute-schema**</span><span class="sxs-lookup"><span data-stu-id="83e4f-203">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="83e4f-204">**Classe-schema**</span><span class="sxs-lookup"><span data-stu-id="83e4f-204">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="83e4f-205">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="83e4f-205">Windows Server 2003 R2</span></span>



| <span data-ttu-id="83e4f-206">Voce</span><span class="sxs-lookup"><span data-stu-id="83e4f-206">Entry</span></span> | <span data-ttu-id="83e4f-207">Valore</span><span class="sxs-lookup"><span data-stu-id="83e4f-207">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83e4f-208">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="83e4f-208">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="83e4f-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="83e4f-209">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="83e4f-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="83e4f-210">System-Only</span></span>            | <span data-ttu-id="83e4f-211">Vero</span><span class="sxs-lookup"><span data-stu-id="83e4f-211">True</span></span>                                                                                                      |
| <span data-ttu-id="83e4f-212">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="83e4f-212">Is-Single-Valued</span></span>       | <span data-ttu-id="83e4f-213">Vero</span><span class="sxs-lookup"><span data-stu-id="83e4f-213">True</span></span>                                                                                                      |
| <span data-ttu-id="83e4f-214">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="83e4f-214">Is Indexed</span></span>             | <span data-ttu-id="83e4f-215">Falso</span><span class="sxs-lookup"><span data-stu-id="83e4f-215">False</span></span>                                                                                                     |
| <span data-ttu-id="83e4f-216">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="83e4f-216">In Global Catalog</span></span>      | <span data-ttu-id="83e4f-217">Falso</span><span class="sxs-lookup"><span data-stu-id="83e4f-217">False</span></span>                                                                                                     |
| <span data-ttu-id="83e4f-218">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="83e4f-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="83e4f-219">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="83e4f-219">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="83e4f-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="83e4f-220">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="83e4f-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="83e4f-221">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="83e4f-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="83e4f-222">Search-Flags</span></span>           | <span data-ttu-id="83e4f-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="83e4f-223">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="83e4f-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="83e4f-224">System-Flags</span></span>           | <span data-ttu-id="83e4f-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="83e4f-225">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="83e4f-226">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="83e4f-226">Classes used in</span></span>        | [<span data-ttu-id="83e4f-227">**Attribute-schema**</span><span class="sxs-lookup"><span data-stu-id="83e4f-227">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="83e4f-228">**Classe-schema**</span><span class="sxs-lookup"><span data-stu-id="83e4f-228">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="83e4f-229">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="83e4f-229">Windows Server 2008</span></span>



| <span data-ttu-id="83e4f-230">Voce</span><span class="sxs-lookup"><span data-stu-id="83e4f-230">Entry</span></span> | <span data-ttu-id="83e4f-231">Valore</span><span class="sxs-lookup"><span data-stu-id="83e4f-231">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83e4f-232">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="83e4f-232">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="83e4f-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="83e4f-233">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="83e4f-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="83e4f-234">System-Only</span></span>            | <span data-ttu-id="83e4f-235">Vero</span><span class="sxs-lookup"><span data-stu-id="83e4f-235">True</span></span>                                                                                                      |
| <span data-ttu-id="83e4f-236">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="83e4f-236">Is-Single-Valued</span></span>       | <span data-ttu-id="83e4f-237">Vero</span><span class="sxs-lookup"><span data-stu-id="83e4f-237">True</span></span>                                                                                                      |
| <span data-ttu-id="83e4f-238">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="83e4f-238">Is Indexed</span></span>             | <span data-ttu-id="83e4f-239">Falso</span><span class="sxs-lookup"><span data-stu-id="83e4f-239">False</span></span>                                                                                                     |
| <span data-ttu-id="83e4f-240">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="83e4f-240">In Global Catalog</span></span>      | <span data-ttu-id="83e4f-241">Falso</span><span class="sxs-lookup"><span data-stu-id="83e4f-241">False</span></span>                                                                                                     |
| <span data-ttu-id="83e4f-242">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="83e4f-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="83e4f-243">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="83e4f-243">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="83e4f-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="83e4f-244">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="83e4f-245">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="83e4f-245">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="83e4f-246">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="83e4f-246">Search-Flags</span></span>           | <span data-ttu-id="83e4f-247">0x00000000</span><span class="sxs-lookup"><span data-stu-id="83e4f-247">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="83e4f-248">System-Flags</span><span class="sxs-lookup"><span data-stu-id="83e4f-248">System-Flags</span></span>           | <span data-ttu-id="83e4f-249">0x00000010</span><span class="sxs-lookup"><span data-stu-id="83e4f-249">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="83e4f-250">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="83e4f-250">Classes used in</span></span>        | [<span data-ttu-id="83e4f-251">**Attribute-schema**</span><span class="sxs-lookup"><span data-stu-id="83e4f-251">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="83e4f-252">**Classe-schema**</span><span class="sxs-lookup"><span data-stu-id="83e4f-252">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="83e4f-253">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="83e4f-253">Windows Server 2008 R2</span></span>



| <span data-ttu-id="83e4f-254">Voce</span><span class="sxs-lookup"><span data-stu-id="83e4f-254">Entry</span></span> | <span data-ttu-id="83e4f-255">Valore</span><span class="sxs-lookup"><span data-stu-id="83e4f-255">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83e4f-256">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="83e4f-256">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="83e4f-257">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="83e4f-257">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="83e4f-258">System-Only</span><span class="sxs-lookup"><span data-stu-id="83e4f-258">System-Only</span></span>            | <span data-ttu-id="83e4f-259">Vero</span><span class="sxs-lookup"><span data-stu-id="83e4f-259">True</span></span>                                                                                                      |
| <span data-ttu-id="83e4f-260">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="83e4f-260">Is-Single-Valued</span></span>       | <span data-ttu-id="83e4f-261">Vero</span><span class="sxs-lookup"><span data-stu-id="83e4f-261">True</span></span>                                                                                                      |
| <span data-ttu-id="83e4f-262">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="83e4f-262">Is Indexed</span></span>             | <span data-ttu-id="83e4f-263">Falso</span><span class="sxs-lookup"><span data-stu-id="83e4f-263">False</span></span>                                                                                                     |
| <span data-ttu-id="83e4f-264">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="83e4f-264">In Global Catalog</span></span>      | <span data-ttu-id="83e4f-265">Falso</span><span class="sxs-lookup"><span data-stu-id="83e4f-265">False</span></span>                                                                                                     |
| <span data-ttu-id="83e4f-266">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="83e4f-266">NT-Security-Descriptor</span></span> | <span data-ttu-id="83e4f-267">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="83e4f-267">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="83e4f-268">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="83e4f-268">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="83e4f-269">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="83e4f-269">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="83e4f-270">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="83e4f-270">Search-Flags</span></span>           | <span data-ttu-id="83e4f-271">0x00000000</span><span class="sxs-lookup"><span data-stu-id="83e4f-271">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="83e4f-272">System-Flags</span><span class="sxs-lookup"><span data-stu-id="83e4f-272">System-Flags</span></span>           | <span data-ttu-id="83e4f-273">0x00000010</span><span class="sxs-lookup"><span data-stu-id="83e4f-273">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="83e4f-274">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="83e4f-274">Classes used in</span></span>        | [<span data-ttu-id="83e4f-275">**Attribute-schema**</span><span class="sxs-lookup"><span data-stu-id="83e4f-275">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="83e4f-276">**Classe-schema**</span><span class="sxs-lookup"><span data-stu-id="83e4f-276">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="83e4f-277">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="83e4f-277">Windows Server 2012</span></span>



| <span data-ttu-id="83e4f-278">Voce</span><span class="sxs-lookup"><span data-stu-id="83e4f-278">Entry</span></span> | <span data-ttu-id="83e4f-279">Valore</span><span class="sxs-lookup"><span data-stu-id="83e4f-279">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83e4f-280">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="83e4f-280">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="83e4f-281">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="83e4f-281">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="83e4f-282">System-Only</span><span class="sxs-lookup"><span data-stu-id="83e4f-282">System-Only</span></span>            | <span data-ttu-id="83e4f-283">Vero</span><span class="sxs-lookup"><span data-stu-id="83e4f-283">True</span></span>                                                                                                      |
| <span data-ttu-id="83e4f-284">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="83e4f-284">Is-Single-Valued</span></span>       | <span data-ttu-id="83e4f-285">Vero</span><span class="sxs-lookup"><span data-stu-id="83e4f-285">True</span></span>                                                                                                      |
| <span data-ttu-id="83e4f-286">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="83e4f-286">Is Indexed</span></span>             | <span data-ttu-id="83e4f-287">Falso</span><span class="sxs-lookup"><span data-stu-id="83e4f-287">False</span></span>                                                                                                     |
| <span data-ttu-id="83e4f-288">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="83e4f-288">In Global Catalog</span></span>      | <span data-ttu-id="83e4f-289">Falso</span><span class="sxs-lookup"><span data-stu-id="83e4f-289">False</span></span>                                                                                                     |
| <span data-ttu-id="83e4f-290">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="83e4f-290">NT-Security-Descriptor</span></span> | <span data-ttu-id="83e4f-291">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="83e4f-291">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="83e4f-292">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="83e4f-292">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="83e4f-293">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="83e4f-293">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="83e4f-294">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="83e4f-294">Search-Flags</span></span>           | <span data-ttu-id="83e4f-295">0x00000000</span><span class="sxs-lookup"><span data-stu-id="83e4f-295">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="83e4f-296">System-Flags</span><span class="sxs-lookup"><span data-stu-id="83e4f-296">System-Flags</span></span>           | <span data-ttu-id="83e4f-297">0x00000010</span><span class="sxs-lookup"><span data-stu-id="83e4f-297">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="83e4f-298">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="83e4f-298">Classes used in</span></span>        | [<span data-ttu-id="83e4f-299">**Attribute-schema**</span><span class="sxs-lookup"><span data-stu-id="83e4f-299">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="83e4f-300">**Classe-schema**</span><span class="sxs-lookup"><span data-stu-id="83e4f-300">**Class-Schema**</span></span>](c-classschema.md)<br/> |



 

 





