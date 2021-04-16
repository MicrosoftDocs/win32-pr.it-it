---
title: Attribute-Security-GUID (attributo)
description: GUID da utilizzare per applicare le credenziali di sicurezza a un set di oggetti.
ms.assetid: df4709ec-273d-4294-8094-f396c10c06e2
ms.tgt_platform: multiple
keywords:
- Attribute-Security-GUID-schema di AD
- Schema AD dell'attributo attributeSecurityGUID
topic_type:
- apiref
api_name:
- Attribute-Security-GUID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7b2ada7c6c806bec1c524b0408750144ca1fd8b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104225289"
---
# <a name="attribute-security-guid-attribute"></a><span data-ttu-id="de1f2-105">Attribute-Security-GUID (attributo)</span><span class="sxs-lookup"><span data-stu-id="de1f2-105">Attribute-Security-GUID attribute</span></span>

<span data-ttu-id="de1f2-106">GUID da utilizzare per applicare le credenziali di sicurezza a un set di oggetti.</span><span class="sxs-lookup"><span data-stu-id="de1f2-106">The GUID to be used to apply security credentials to a set of objects.</span></span>



| <span data-ttu-id="de1f2-107">Voce</span><span class="sxs-lookup"><span data-stu-id="de1f2-107">Entry</span></span> | <span data-ttu-id="de1f2-108">Valore</span><span class="sxs-lookup"><span data-stu-id="de1f2-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="de1f2-109">CN</span><span class="sxs-lookup"><span data-stu-id="de1f2-109">CN</span></span>                | <span data-ttu-id="de1f2-110">Attribute-Security-GUID</span><span class="sxs-lookup"><span data-stu-id="de1f2-110">Attribute-Security-GUID</span></span>                               |
| <span data-ttu-id="de1f2-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="de1f2-111">Ldap-Display-Name</span></span> | <span data-ttu-id="de1f2-112">attributeSecurityGUID</span><span class="sxs-lookup"><span data-stu-id="de1f2-112">attributeSecurityGUID</span></span>                                 |
| <span data-ttu-id="de1f2-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="de1f2-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="de1f2-114">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="de1f2-114">Update Privilege</span></span>  | <span data-ttu-id="de1f2-115">Amministratore schema</span><span class="sxs-lookup"><span data-stu-id="de1f2-115">Schema administrator</span></span>                                  |
| <span data-ttu-id="de1f2-116">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="de1f2-116">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="de1f2-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="de1f2-117">Attribute-Id</span></span>      | <span data-ttu-id="de1f2-118">1.2.840.113556.1.4.149</span><span class="sxs-lookup"><span data-stu-id="de1f2-118">1.2.840.113556.1.4.149</span></span>                                |
| <span data-ttu-id="de1f2-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="de1f2-119">System-Id-Guid</span></span>    | <span data-ttu-id="de1f2-120">bf967924-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="de1f2-120">bf967924-0de6-11d0-a285-00aa003049e2</span></span>                  |
| <span data-ttu-id="de1f2-121">Sintassi</span><span class="sxs-lookup"><span data-stu-id="de1f2-121">Syntax</span></span>            | [<span data-ttu-id="de1f2-122">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="de1f2-122">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="de1f2-123">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="de1f2-123">Implementations</span></span>

-   [<span data-ttu-id="de1f2-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="de1f2-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="de1f2-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="de1f2-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="de1f2-126">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="de1f2-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="de1f2-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="de1f2-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="de1f2-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="de1f2-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="de1f2-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="de1f2-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="de1f2-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="de1f2-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="de1f2-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="de1f2-131">Windows 2000 Server</span></span>



| <span data-ttu-id="de1f2-132">Voce</span><span class="sxs-lookup"><span data-stu-id="de1f2-132">Entry</span></span> | <span data-ttu-id="de1f2-133">Valore</span><span class="sxs-lookup"><span data-stu-id="de1f2-133">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="de1f2-134">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="de1f2-134">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="de1f2-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="de1f2-135">MAPI-Id</span></span>                | \-                                                       |
| <span data-ttu-id="de1f2-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="de1f2-136">System-Only</span></span>            | <span data-ttu-id="de1f2-137">Falso</span><span class="sxs-lookup"><span data-stu-id="de1f2-137">False</span></span>                                                    |
| <span data-ttu-id="de1f2-138">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="de1f2-138">Is-Single-Valued</span></span>       | <span data-ttu-id="de1f2-139">Vero</span><span class="sxs-lookup"><span data-stu-id="de1f2-139">True</span></span>                                                     |
| <span data-ttu-id="de1f2-140">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="de1f2-140">Is Indexed</span></span>             | <span data-ttu-id="de1f2-141">Falso</span><span class="sxs-lookup"><span data-stu-id="de1f2-141">False</span></span>                                                    |
| <span data-ttu-id="de1f2-142">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="de1f2-142">In Global Catalog</span></span>      | <span data-ttu-id="de1f2-143">Falso</span><span class="sxs-lookup"><span data-stu-id="de1f2-143">False</span></span>                                                    |
| <span data-ttu-id="de1f2-144">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="de1f2-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="de1f2-145">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="de1f2-145">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="de1f2-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="de1f2-146">Range-Lower</span></span>            | <span data-ttu-id="de1f2-147">16</span><span class="sxs-lookup"><span data-stu-id="de1f2-147">16</span></span>                                                       |
| <span data-ttu-id="de1f2-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="de1f2-148">Range-Upper</span></span>            | <span data-ttu-id="de1f2-149">16</span><span class="sxs-lookup"><span data-stu-id="de1f2-149">16</span></span>                                                       |
| <span data-ttu-id="de1f2-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="de1f2-150">Search-Flags</span></span>           | <span data-ttu-id="de1f2-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="de1f2-151">0x00000000</span></span>                                               |
| <span data-ttu-id="de1f2-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="de1f2-152">System-Flags</span></span>           | <span data-ttu-id="de1f2-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="de1f2-153">0x00000010</span></span>                                               |
| <span data-ttu-id="de1f2-154">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="de1f2-154">Classes used in</span></span>        | [<span data-ttu-id="de1f2-155">**Attribute-schema**</span><span class="sxs-lookup"><span data-stu-id="de1f2-155">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="de1f2-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="de1f2-156">Windows Server 2003</span></span>



| <span data-ttu-id="de1f2-157">Voce</span><span class="sxs-lookup"><span data-stu-id="de1f2-157">Entry</span></span> | <span data-ttu-id="de1f2-158">Valore</span><span class="sxs-lookup"><span data-stu-id="de1f2-158">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="de1f2-159">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="de1f2-159">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="de1f2-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="de1f2-160">MAPI-Id</span></span>                | \-                                                       |
| <span data-ttu-id="de1f2-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="de1f2-161">System-Only</span></span>            | <span data-ttu-id="de1f2-162">Falso</span><span class="sxs-lookup"><span data-stu-id="de1f2-162">False</span></span>                                                    |
| <span data-ttu-id="de1f2-163">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="de1f2-163">Is-Single-Valued</span></span>       | <span data-ttu-id="de1f2-164">Vero</span><span class="sxs-lookup"><span data-stu-id="de1f2-164">True</span></span>                                                     |
| <span data-ttu-id="de1f2-165">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="de1f2-165">Is Indexed</span></span>             | <span data-ttu-id="de1f2-166">Falso</span><span class="sxs-lookup"><span data-stu-id="de1f2-166">False</span></span>                                                    |
| <span data-ttu-id="de1f2-167">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="de1f2-167">In Global Catalog</span></span>      | <span data-ttu-id="de1f2-168">Falso</span><span class="sxs-lookup"><span data-stu-id="de1f2-168">False</span></span>                                                    |
| <span data-ttu-id="de1f2-169">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="de1f2-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="de1f2-170">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="de1f2-170">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="de1f2-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="de1f2-171">Range-Lower</span></span>            | <span data-ttu-id="de1f2-172">16</span><span class="sxs-lookup"><span data-stu-id="de1f2-172">16</span></span>                                                       |
| <span data-ttu-id="de1f2-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="de1f2-173">Range-Upper</span></span>            | <span data-ttu-id="de1f2-174">16</span><span class="sxs-lookup"><span data-stu-id="de1f2-174">16</span></span>                                                       |
| <span data-ttu-id="de1f2-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="de1f2-175">Search-Flags</span></span>           | <span data-ttu-id="de1f2-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="de1f2-176">0x00000000</span></span>                                               |
| <span data-ttu-id="de1f2-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="de1f2-177">System-Flags</span></span>           | <span data-ttu-id="de1f2-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="de1f2-178">0x00000010</span></span>                                               |
| <span data-ttu-id="de1f2-179">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="de1f2-179">Classes used in</span></span>        | [<span data-ttu-id="de1f2-180">**Attribute-schema**</span><span class="sxs-lookup"><span data-stu-id="de1f2-180">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="de1f2-181">ADAM</span><span class="sxs-lookup"><span data-stu-id="de1f2-181">ADAM</span></span>



| <span data-ttu-id="de1f2-182">Voce</span><span class="sxs-lookup"><span data-stu-id="de1f2-182">Entry</span></span> | <span data-ttu-id="de1f2-183">Valore</span><span class="sxs-lookup"><span data-stu-id="de1f2-183">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="de1f2-184">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="de1f2-184">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="de1f2-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="de1f2-185">MAPI-Id</span></span>                | \-                                                       |
| <span data-ttu-id="de1f2-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="de1f2-186">System-Only</span></span>            | <span data-ttu-id="de1f2-187">Falso</span><span class="sxs-lookup"><span data-stu-id="de1f2-187">False</span></span>                                                    |
| <span data-ttu-id="de1f2-188">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="de1f2-188">Is-Single-Valued</span></span>       | <span data-ttu-id="de1f2-189">Vero</span><span class="sxs-lookup"><span data-stu-id="de1f2-189">True</span></span>                                                     |
| <span data-ttu-id="de1f2-190">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="de1f2-190">Is Indexed</span></span>             | <span data-ttu-id="de1f2-191">Falso</span><span class="sxs-lookup"><span data-stu-id="de1f2-191">False</span></span>                                                    |
| <span data-ttu-id="de1f2-192">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="de1f2-192">In Global Catalog</span></span>      | <span data-ttu-id="de1f2-193">Falso</span><span class="sxs-lookup"><span data-stu-id="de1f2-193">False</span></span>                                                    |
| <span data-ttu-id="de1f2-194">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="de1f2-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="de1f2-195">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="de1f2-195">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="de1f2-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="de1f2-196">Range-Lower</span></span>            | <span data-ttu-id="de1f2-197">16</span><span class="sxs-lookup"><span data-stu-id="de1f2-197">16</span></span>                                                       |
| <span data-ttu-id="de1f2-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="de1f2-198">Range-Upper</span></span>            | <span data-ttu-id="de1f2-199">16</span><span class="sxs-lookup"><span data-stu-id="de1f2-199">16</span></span>                                                       |
| <span data-ttu-id="de1f2-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="de1f2-200">Search-Flags</span></span>           | <span data-ttu-id="de1f2-201">0x00000000</span><span class="sxs-lookup"><span data-stu-id="de1f2-201">0x00000000</span></span>                                               |
| <span data-ttu-id="de1f2-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="de1f2-202">System-Flags</span></span>           | <span data-ttu-id="de1f2-203">0x00000010</span><span class="sxs-lookup"><span data-stu-id="de1f2-203">0x00000010</span></span>                                               |
| <span data-ttu-id="de1f2-204">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="de1f2-204">Classes used in</span></span>        | [<span data-ttu-id="de1f2-205">**Attribute-schema**</span><span class="sxs-lookup"><span data-stu-id="de1f2-205">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="de1f2-206">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="de1f2-206">Windows Server 2003 R2</span></span>



| <span data-ttu-id="de1f2-207">Voce</span><span class="sxs-lookup"><span data-stu-id="de1f2-207">Entry</span></span> | <span data-ttu-id="de1f2-208">Valore</span><span class="sxs-lookup"><span data-stu-id="de1f2-208">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="de1f2-209">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="de1f2-209">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="de1f2-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="de1f2-210">MAPI-Id</span></span>                | \-                                                       |
| <span data-ttu-id="de1f2-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="de1f2-211">System-Only</span></span>            | <span data-ttu-id="de1f2-212">Falso</span><span class="sxs-lookup"><span data-stu-id="de1f2-212">False</span></span>                                                    |
| <span data-ttu-id="de1f2-213">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="de1f2-213">Is-Single-Valued</span></span>       | <span data-ttu-id="de1f2-214">Vero</span><span class="sxs-lookup"><span data-stu-id="de1f2-214">True</span></span>                                                     |
| <span data-ttu-id="de1f2-215">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="de1f2-215">Is Indexed</span></span>             | <span data-ttu-id="de1f2-216">Falso</span><span class="sxs-lookup"><span data-stu-id="de1f2-216">False</span></span>                                                    |
| <span data-ttu-id="de1f2-217">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="de1f2-217">In Global Catalog</span></span>      | <span data-ttu-id="de1f2-218">Falso</span><span class="sxs-lookup"><span data-stu-id="de1f2-218">False</span></span>                                                    |
| <span data-ttu-id="de1f2-219">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="de1f2-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="de1f2-220">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="de1f2-220">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="de1f2-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="de1f2-221">Range-Lower</span></span>            | <span data-ttu-id="de1f2-222">16</span><span class="sxs-lookup"><span data-stu-id="de1f2-222">16</span></span>                                                       |
| <span data-ttu-id="de1f2-223">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="de1f2-223">Range-Upper</span></span>            | <span data-ttu-id="de1f2-224">16</span><span class="sxs-lookup"><span data-stu-id="de1f2-224">16</span></span>                                                       |
| <span data-ttu-id="de1f2-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="de1f2-225">Search-Flags</span></span>           | <span data-ttu-id="de1f2-226">0x00000000</span><span class="sxs-lookup"><span data-stu-id="de1f2-226">0x00000000</span></span>                                               |
| <span data-ttu-id="de1f2-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="de1f2-227">System-Flags</span></span>           | <span data-ttu-id="de1f2-228">0x00000010</span><span class="sxs-lookup"><span data-stu-id="de1f2-228">0x00000010</span></span>                                               |
| <span data-ttu-id="de1f2-229">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="de1f2-229">Classes used in</span></span>        | [<span data-ttu-id="de1f2-230">**Attribute-schema**</span><span class="sxs-lookup"><span data-stu-id="de1f2-230">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="de1f2-231">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="de1f2-231">Windows Server 2008</span></span>



| <span data-ttu-id="de1f2-232">Voce</span><span class="sxs-lookup"><span data-stu-id="de1f2-232">Entry</span></span> | <span data-ttu-id="de1f2-233">Valore</span><span class="sxs-lookup"><span data-stu-id="de1f2-233">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="de1f2-234">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="de1f2-234">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="de1f2-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="de1f2-235">MAPI-Id</span></span>                | \-                                                       |
| <span data-ttu-id="de1f2-236">System-Only</span><span class="sxs-lookup"><span data-stu-id="de1f2-236">System-Only</span></span>            | <span data-ttu-id="de1f2-237">Falso</span><span class="sxs-lookup"><span data-stu-id="de1f2-237">False</span></span>                                                    |
| <span data-ttu-id="de1f2-238">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="de1f2-238">Is-Single-Valued</span></span>       | <span data-ttu-id="de1f2-239">Vero</span><span class="sxs-lookup"><span data-stu-id="de1f2-239">True</span></span>                                                     |
| <span data-ttu-id="de1f2-240">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="de1f2-240">Is Indexed</span></span>             | <span data-ttu-id="de1f2-241">Falso</span><span class="sxs-lookup"><span data-stu-id="de1f2-241">False</span></span>                                                    |
| <span data-ttu-id="de1f2-242">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="de1f2-242">In Global Catalog</span></span>      | <span data-ttu-id="de1f2-243">Falso</span><span class="sxs-lookup"><span data-stu-id="de1f2-243">False</span></span>                                                    |
| <span data-ttu-id="de1f2-244">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="de1f2-244">NT-Security-Descriptor</span></span> | <span data-ttu-id="de1f2-245">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="de1f2-245">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="de1f2-246">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="de1f2-246">Range-Lower</span></span>            | <span data-ttu-id="de1f2-247">16</span><span class="sxs-lookup"><span data-stu-id="de1f2-247">16</span></span>                                                       |
| <span data-ttu-id="de1f2-248">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="de1f2-248">Range-Upper</span></span>            | <span data-ttu-id="de1f2-249">16</span><span class="sxs-lookup"><span data-stu-id="de1f2-249">16</span></span>                                                       |
| <span data-ttu-id="de1f2-250">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="de1f2-250">Search-Flags</span></span>           | <span data-ttu-id="de1f2-251">0x00000000</span><span class="sxs-lookup"><span data-stu-id="de1f2-251">0x00000000</span></span>                                               |
| <span data-ttu-id="de1f2-252">System-Flags</span><span class="sxs-lookup"><span data-stu-id="de1f2-252">System-Flags</span></span>           | <span data-ttu-id="de1f2-253">0x00000010</span><span class="sxs-lookup"><span data-stu-id="de1f2-253">0x00000010</span></span>                                               |
| <span data-ttu-id="de1f2-254">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="de1f2-254">Classes used in</span></span>        | [<span data-ttu-id="de1f2-255">**Attribute-schema**</span><span class="sxs-lookup"><span data-stu-id="de1f2-255">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="de1f2-256">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="de1f2-256">Windows Server 2008 R2</span></span>



| <span data-ttu-id="de1f2-257">Voce</span><span class="sxs-lookup"><span data-stu-id="de1f2-257">Entry</span></span> | <span data-ttu-id="de1f2-258">Valore</span><span class="sxs-lookup"><span data-stu-id="de1f2-258">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="de1f2-259">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="de1f2-259">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="de1f2-260">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="de1f2-260">MAPI-Id</span></span>                | \-                                                       |
| <span data-ttu-id="de1f2-261">System-Only</span><span class="sxs-lookup"><span data-stu-id="de1f2-261">System-Only</span></span>            | <span data-ttu-id="de1f2-262">Falso</span><span class="sxs-lookup"><span data-stu-id="de1f2-262">False</span></span>                                                    |
| <span data-ttu-id="de1f2-263">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="de1f2-263">Is-Single-Valued</span></span>       | <span data-ttu-id="de1f2-264">Vero</span><span class="sxs-lookup"><span data-stu-id="de1f2-264">True</span></span>                                                     |
| <span data-ttu-id="de1f2-265">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="de1f2-265">Is Indexed</span></span>             | <span data-ttu-id="de1f2-266">Falso</span><span class="sxs-lookup"><span data-stu-id="de1f2-266">False</span></span>                                                    |
| <span data-ttu-id="de1f2-267">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="de1f2-267">In Global Catalog</span></span>      | <span data-ttu-id="de1f2-268">Falso</span><span class="sxs-lookup"><span data-stu-id="de1f2-268">False</span></span>                                                    |
| <span data-ttu-id="de1f2-269">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="de1f2-269">NT-Security-Descriptor</span></span> | <span data-ttu-id="de1f2-270">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="de1f2-270">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="de1f2-271">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="de1f2-271">Range-Lower</span></span>            | <span data-ttu-id="de1f2-272">16</span><span class="sxs-lookup"><span data-stu-id="de1f2-272">16</span></span>                                                       |
| <span data-ttu-id="de1f2-273">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="de1f2-273">Range-Upper</span></span>            | <span data-ttu-id="de1f2-274">16</span><span class="sxs-lookup"><span data-stu-id="de1f2-274">16</span></span>                                                       |
| <span data-ttu-id="de1f2-275">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="de1f2-275">Search-Flags</span></span>           | <span data-ttu-id="de1f2-276">0x00000000</span><span class="sxs-lookup"><span data-stu-id="de1f2-276">0x00000000</span></span>                                               |
| <span data-ttu-id="de1f2-277">System-Flags</span><span class="sxs-lookup"><span data-stu-id="de1f2-277">System-Flags</span></span>           | <span data-ttu-id="de1f2-278">0x00000010</span><span class="sxs-lookup"><span data-stu-id="de1f2-278">0x00000010</span></span>                                               |
| <span data-ttu-id="de1f2-279">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="de1f2-279">Classes used in</span></span>        | [<span data-ttu-id="de1f2-280">**Attribute-schema**</span><span class="sxs-lookup"><span data-stu-id="de1f2-280">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="de1f2-281">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="de1f2-281">Windows Server 2012</span></span>



| <span data-ttu-id="de1f2-282">Voce</span><span class="sxs-lookup"><span data-stu-id="de1f2-282">Entry</span></span> | <span data-ttu-id="de1f2-283">Valore</span><span class="sxs-lookup"><span data-stu-id="de1f2-283">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="de1f2-284">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="de1f2-284">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="de1f2-285">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="de1f2-285">MAPI-Id</span></span>                | \-                                                       |
| <span data-ttu-id="de1f2-286">System-Only</span><span class="sxs-lookup"><span data-stu-id="de1f2-286">System-Only</span></span>            | <span data-ttu-id="de1f2-287">Falso</span><span class="sxs-lookup"><span data-stu-id="de1f2-287">False</span></span>                                                    |
| <span data-ttu-id="de1f2-288">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="de1f2-288">Is-Single-Valued</span></span>       | <span data-ttu-id="de1f2-289">Vero</span><span class="sxs-lookup"><span data-stu-id="de1f2-289">True</span></span>                                                     |
| <span data-ttu-id="de1f2-290">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="de1f2-290">Is Indexed</span></span>             | <span data-ttu-id="de1f2-291">Falso</span><span class="sxs-lookup"><span data-stu-id="de1f2-291">False</span></span>                                                    |
| <span data-ttu-id="de1f2-292">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="de1f2-292">In Global Catalog</span></span>      | <span data-ttu-id="de1f2-293">Falso</span><span class="sxs-lookup"><span data-stu-id="de1f2-293">False</span></span>                                                    |
| <span data-ttu-id="de1f2-294">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="de1f2-294">NT-Security-Descriptor</span></span> | <span data-ttu-id="de1f2-295">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="de1f2-295">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="de1f2-296">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="de1f2-296">Range-Lower</span></span>            | <span data-ttu-id="de1f2-297">16</span><span class="sxs-lookup"><span data-stu-id="de1f2-297">16</span></span>                                                       |
| <span data-ttu-id="de1f2-298">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="de1f2-298">Range-Upper</span></span>            | <span data-ttu-id="de1f2-299">16</span><span class="sxs-lookup"><span data-stu-id="de1f2-299">16</span></span>                                                       |
| <span data-ttu-id="de1f2-300">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="de1f2-300">Search-Flags</span></span>           | <span data-ttu-id="de1f2-301">0x00000000</span><span class="sxs-lookup"><span data-stu-id="de1f2-301">0x00000000</span></span>                                               |
| <span data-ttu-id="de1f2-302">System-Flags</span><span class="sxs-lookup"><span data-stu-id="de1f2-302">System-Flags</span></span>           | <span data-ttu-id="de1f2-303">0x00000010</span><span class="sxs-lookup"><span data-stu-id="de1f2-303">0x00000010</span></span>                                               |
| <span data-ttu-id="de1f2-304">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="de1f2-304">Classes used in</span></span>        | [<span data-ttu-id="de1f2-305">**Attribute-schema**</span><span class="sxs-lookup"><span data-stu-id="de1f2-305">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



 

 





