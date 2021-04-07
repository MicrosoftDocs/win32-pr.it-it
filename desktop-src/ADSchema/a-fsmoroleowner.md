---
title: FSMO-Role-Owner-attributo
description: Single-Master flessibile operazione il nome distinto del controller di dominio in cui è possibile modificare lo schema.
ms.assetid: 8eb28524-4bbf-453c-89ab-864ef94b0781
ms.tgt_platform: multiple
keywords:
- FSMO-Role-Owner-schema AD
- Schema AD dell'attributo fSMORoleOwner
topic_type:
- apiref
api_name:
- FSMO-Role-Owner
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56d4439e5ee10fba11db831024d6b1958b75cd81
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103875485"
---
# <a name="fsmo-role-owner-attribute"></a><span data-ttu-id="d07bb-105">FSMO-Role-Owner-attributo</span><span class="sxs-lookup"><span data-stu-id="d07bb-105">FSMO-Role-Owner attribute</span></span>

<span data-ttu-id="d07bb-106">Flexible Single-Master Operation: nome distinto del controller di dominio in cui è possibile modificare lo schema.</span><span class="sxs-lookup"><span data-stu-id="d07bb-106">Flexible Single-Master Operation: The distinguished name of the DC where the schema can be modified.</span></span>



| <span data-ttu-id="d07bb-107">Voce</span><span class="sxs-lookup"><span data-stu-id="d07bb-107">Entry</span></span> | <span data-ttu-id="d07bb-108">Valore</span><span class="sxs-lookup"><span data-stu-id="d07bb-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="d07bb-109">CN</span><span class="sxs-lookup"><span data-stu-id="d07bb-109">CN</span></span>                | <span data-ttu-id="d07bb-110">FSMO-Role-Owner</span><span class="sxs-lookup"><span data-stu-id="d07bb-110">FSMO-Role-Owner</span></span>                         |
| <span data-ttu-id="d07bb-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="d07bb-111">Ldap-Display-Name</span></span> | <span data-ttu-id="d07bb-112">fSMORoleOwner</span><span class="sxs-lookup"><span data-stu-id="d07bb-112">fSMORoleOwner</span></span>                           |
| <span data-ttu-id="d07bb-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="d07bb-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="d07bb-114">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="d07bb-114">Update Privilege</span></span>  | <span data-ttu-id="d07bb-115">Amministratore schema</span><span class="sxs-lookup"><span data-stu-id="d07bb-115">Schema administrator</span></span>                    |
| <span data-ttu-id="d07bb-116">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="d07bb-116">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="d07bb-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="d07bb-117">Attribute-Id</span></span>      | <span data-ttu-id="d07bb-118">1.2.840.113556.1.4.369</span><span class="sxs-lookup"><span data-stu-id="d07bb-118">1.2.840.113556.1.4.369</span></span>                  |
| <span data-ttu-id="d07bb-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="d07bb-119">System-Id-Guid</span></span>    | <span data-ttu-id="d07bb-120">66171887-8f3c-11d0-afda-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="d07bb-120">66171887-8f3c-11d0-afda-00c04fd930c9</span></span>    |
| <span data-ttu-id="d07bb-121">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d07bb-121">Syntax</span></span>            | [<span data-ttu-id="d07bb-122">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="d07bb-122">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="d07bb-123">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="d07bb-123">Implementations</span></span>

-   [<span data-ttu-id="d07bb-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="d07bb-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="d07bb-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="d07bb-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="d07bb-126">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="d07bb-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="d07bb-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="d07bb-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="d07bb-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="d07bb-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="d07bb-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="d07bb-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="d07bb-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="d07bb-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="d07bb-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d07bb-131">Windows 2000 Server</span></span>



| <span data-ttu-id="d07bb-132">Voce</span><span class="sxs-lookup"><span data-stu-id="d07bb-132">Entry</span></span> | <span data-ttu-id="d07bb-133">Valore</span><span class="sxs-lookup"><span data-stu-id="d07bb-133">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="d07bb-134">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="d07bb-134">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="d07bb-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d07bb-135">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="d07bb-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="d07bb-136">System-Only</span></span>            | <span data-ttu-id="d07bb-137">Falso</span><span class="sxs-lookup"><span data-stu-id="d07bb-137">False</span></span>                           |
| <span data-ttu-id="d07bb-138">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="d07bb-138">Is-Single-Valued</span></span>       | <span data-ttu-id="d07bb-139">Vero</span><span class="sxs-lookup"><span data-stu-id="d07bb-139">True</span></span>                            |
| <span data-ttu-id="d07bb-140">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="d07bb-140">Is Indexed</span></span>             | <span data-ttu-id="d07bb-141">Vero</span><span class="sxs-lookup"><span data-stu-id="d07bb-141">True</span></span>                            |
| <span data-ttu-id="d07bb-142">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="d07bb-142">In Global Catalog</span></span>      | <span data-ttu-id="d07bb-143">Falso</span><span class="sxs-lookup"><span data-stu-id="d07bb-143">False</span></span>                           |
| <span data-ttu-id="d07bb-144">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="d07bb-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="d07bb-145">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="d07bb-145">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="d07bb-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d07bb-146">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="d07bb-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d07bb-147">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="d07bb-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d07bb-148">Search-Flags</span></span>           | <span data-ttu-id="d07bb-149">0x00000001</span><span class="sxs-lookup"><span data-stu-id="d07bb-149">0x00000001</span></span>                      |
| <span data-ttu-id="d07bb-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d07bb-150">System-Flags</span></span>           | <span data-ttu-id="d07bb-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d07bb-151">0x00000010</span></span>                      |
| <span data-ttu-id="d07bb-152">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="d07bb-152">Classes used in</span></span>        | [<span data-ttu-id="d07bb-153">**In alto**</span><span class="sxs-lookup"><span data-stu-id="d07bb-153">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="d07bb-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d07bb-154">Windows Server 2003</span></span>



| <span data-ttu-id="d07bb-155">Voce</span><span class="sxs-lookup"><span data-stu-id="d07bb-155">Entry</span></span> | <span data-ttu-id="d07bb-156">Valore</span><span class="sxs-lookup"><span data-stu-id="d07bb-156">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="d07bb-157">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="d07bb-157">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="d07bb-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d07bb-158">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="d07bb-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="d07bb-159">System-Only</span></span>            | <span data-ttu-id="d07bb-160">Falso</span><span class="sxs-lookup"><span data-stu-id="d07bb-160">False</span></span>                           |
| <span data-ttu-id="d07bb-161">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="d07bb-161">Is-Single-Valued</span></span>       | <span data-ttu-id="d07bb-162">Vero</span><span class="sxs-lookup"><span data-stu-id="d07bb-162">True</span></span>                            |
| <span data-ttu-id="d07bb-163">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="d07bb-163">Is Indexed</span></span>             | <span data-ttu-id="d07bb-164">Vero</span><span class="sxs-lookup"><span data-stu-id="d07bb-164">True</span></span>                            |
| <span data-ttu-id="d07bb-165">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="d07bb-165">In Global Catalog</span></span>      | <span data-ttu-id="d07bb-166">Falso</span><span class="sxs-lookup"><span data-stu-id="d07bb-166">False</span></span>                           |
| <span data-ttu-id="d07bb-167">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="d07bb-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="d07bb-168">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="d07bb-168">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="d07bb-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d07bb-169">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="d07bb-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d07bb-170">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="d07bb-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d07bb-171">Search-Flags</span></span>           | <span data-ttu-id="d07bb-172">0x00000001</span><span class="sxs-lookup"><span data-stu-id="d07bb-172">0x00000001</span></span>                      |
| <span data-ttu-id="d07bb-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d07bb-173">System-Flags</span></span>           | <span data-ttu-id="d07bb-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d07bb-174">0x00000010</span></span>                      |
| <span data-ttu-id="d07bb-175">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="d07bb-175">Classes used in</span></span>        | [<span data-ttu-id="d07bb-176">**In alto**</span><span class="sxs-lookup"><span data-stu-id="d07bb-176">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="d07bb-177">ADAM</span><span class="sxs-lookup"><span data-stu-id="d07bb-177">ADAM</span></span>



| <span data-ttu-id="d07bb-178">Voce</span><span class="sxs-lookup"><span data-stu-id="d07bb-178">Entry</span></span> | <span data-ttu-id="d07bb-179">Valore</span><span class="sxs-lookup"><span data-stu-id="d07bb-179">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="d07bb-180">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="d07bb-180">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="d07bb-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d07bb-181">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="d07bb-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="d07bb-182">System-Only</span></span>            | <span data-ttu-id="d07bb-183">Falso</span><span class="sxs-lookup"><span data-stu-id="d07bb-183">False</span></span>                           |
| <span data-ttu-id="d07bb-184">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="d07bb-184">Is-Single-Valued</span></span>       | <span data-ttu-id="d07bb-185">Vero</span><span class="sxs-lookup"><span data-stu-id="d07bb-185">True</span></span>                            |
| <span data-ttu-id="d07bb-186">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="d07bb-186">Is Indexed</span></span>             | <span data-ttu-id="d07bb-187">Vero</span><span class="sxs-lookup"><span data-stu-id="d07bb-187">True</span></span>                            |
| <span data-ttu-id="d07bb-188">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="d07bb-188">In Global Catalog</span></span>      | <span data-ttu-id="d07bb-189">Falso</span><span class="sxs-lookup"><span data-stu-id="d07bb-189">False</span></span>                           |
| <span data-ttu-id="d07bb-190">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="d07bb-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="d07bb-191">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="d07bb-191">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="d07bb-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d07bb-192">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="d07bb-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d07bb-193">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="d07bb-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d07bb-194">Search-Flags</span></span>           | <span data-ttu-id="d07bb-195">0x00000001</span><span class="sxs-lookup"><span data-stu-id="d07bb-195">0x00000001</span></span>                      |
| <span data-ttu-id="d07bb-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d07bb-196">System-Flags</span></span>           | <span data-ttu-id="d07bb-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d07bb-197">0x00000010</span></span>                      |
| <span data-ttu-id="d07bb-198">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="d07bb-198">Classes used in</span></span>        | [<span data-ttu-id="d07bb-199">**In alto**</span><span class="sxs-lookup"><span data-stu-id="d07bb-199">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="d07bb-200">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="d07bb-200">Windows Server 2003 R2</span></span>



| <span data-ttu-id="d07bb-201">Voce</span><span class="sxs-lookup"><span data-stu-id="d07bb-201">Entry</span></span> | <span data-ttu-id="d07bb-202">Valore</span><span class="sxs-lookup"><span data-stu-id="d07bb-202">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="d07bb-203">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="d07bb-203">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="d07bb-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d07bb-204">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="d07bb-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="d07bb-205">System-Only</span></span>            | <span data-ttu-id="d07bb-206">Falso</span><span class="sxs-lookup"><span data-stu-id="d07bb-206">False</span></span>                           |
| <span data-ttu-id="d07bb-207">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="d07bb-207">Is-Single-Valued</span></span>       | <span data-ttu-id="d07bb-208">Vero</span><span class="sxs-lookup"><span data-stu-id="d07bb-208">True</span></span>                            |
| <span data-ttu-id="d07bb-209">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="d07bb-209">Is Indexed</span></span>             | <span data-ttu-id="d07bb-210">Vero</span><span class="sxs-lookup"><span data-stu-id="d07bb-210">True</span></span>                            |
| <span data-ttu-id="d07bb-211">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="d07bb-211">In Global Catalog</span></span>      | <span data-ttu-id="d07bb-212">Falso</span><span class="sxs-lookup"><span data-stu-id="d07bb-212">False</span></span>                           |
| <span data-ttu-id="d07bb-213">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="d07bb-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="d07bb-214">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="d07bb-214">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="d07bb-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d07bb-215">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="d07bb-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d07bb-216">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="d07bb-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d07bb-217">Search-Flags</span></span>           | <span data-ttu-id="d07bb-218">0x00000001</span><span class="sxs-lookup"><span data-stu-id="d07bb-218">0x00000001</span></span>                      |
| <span data-ttu-id="d07bb-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d07bb-219">System-Flags</span></span>           | <span data-ttu-id="d07bb-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d07bb-220">0x00000010</span></span>                      |
| <span data-ttu-id="d07bb-221">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="d07bb-221">Classes used in</span></span>        | [<span data-ttu-id="d07bb-222">**In alto**</span><span class="sxs-lookup"><span data-stu-id="d07bb-222">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="d07bb-223">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d07bb-223">Windows Server 2008</span></span>



| <span data-ttu-id="d07bb-224">Voce</span><span class="sxs-lookup"><span data-stu-id="d07bb-224">Entry</span></span> | <span data-ttu-id="d07bb-225">Valore</span><span class="sxs-lookup"><span data-stu-id="d07bb-225">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="d07bb-226">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="d07bb-226">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="d07bb-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d07bb-227">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="d07bb-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="d07bb-228">System-Only</span></span>            | <span data-ttu-id="d07bb-229">Falso</span><span class="sxs-lookup"><span data-stu-id="d07bb-229">False</span></span>                           |
| <span data-ttu-id="d07bb-230">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="d07bb-230">Is-Single-Valued</span></span>       | <span data-ttu-id="d07bb-231">Vero</span><span class="sxs-lookup"><span data-stu-id="d07bb-231">True</span></span>                            |
| <span data-ttu-id="d07bb-232">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="d07bb-232">Is Indexed</span></span>             | <span data-ttu-id="d07bb-233">Vero</span><span class="sxs-lookup"><span data-stu-id="d07bb-233">True</span></span>                            |
| <span data-ttu-id="d07bb-234">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="d07bb-234">In Global Catalog</span></span>      | <span data-ttu-id="d07bb-235">Falso</span><span class="sxs-lookup"><span data-stu-id="d07bb-235">False</span></span>                           |
| <span data-ttu-id="d07bb-236">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="d07bb-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="d07bb-237">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="d07bb-237">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="d07bb-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d07bb-238">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="d07bb-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d07bb-239">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="d07bb-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d07bb-240">Search-Flags</span></span>           | <span data-ttu-id="d07bb-241">0x00000001</span><span class="sxs-lookup"><span data-stu-id="d07bb-241">0x00000001</span></span>                      |
| <span data-ttu-id="d07bb-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d07bb-242">System-Flags</span></span>           | <span data-ttu-id="d07bb-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d07bb-243">0x00000010</span></span>                      |
| <span data-ttu-id="d07bb-244">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="d07bb-244">Classes used in</span></span>        | [<span data-ttu-id="d07bb-245">**In alto**</span><span class="sxs-lookup"><span data-stu-id="d07bb-245">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="d07bb-246">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d07bb-246">Windows Server 2008 R2</span></span>



| <span data-ttu-id="d07bb-247">Voce</span><span class="sxs-lookup"><span data-stu-id="d07bb-247">Entry</span></span> | <span data-ttu-id="d07bb-248">Valore</span><span class="sxs-lookup"><span data-stu-id="d07bb-248">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="d07bb-249">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="d07bb-249">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="d07bb-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d07bb-250">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="d07bb-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="d07bb-251">System-Only</span></span>            | <span data-ttu-id="d07bb-252">Falso</span><span class="sxs-lookup"><span data-stu-id="d07bb-252">False</span></span>                           |
| <span data-ttu-id="d07bb-253">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="d07bb-253">Is-Single-Valued</span></span>       | <span data-ttu-id="d07bb-254">Vero</span><span class="sxs-lookup"><span data-stu-id="d07bb-254">True</span></span>                            |
| <span data-ttu-id="d07bb-255">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="d07bb-255">Is Indexed</span></span>             | <span data-ttu-id="d07bb-256">Vero</span><span class="sxs-lookup"><span data-stu-id="d07bb-256">True</span></span>                            |
| <span data-ttu-id="d07bb-257">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="d07bb-257">In Global Catalog</span></span>      | <span data-ttu-id="d07bb-258">Falso</span><span class="sxs-lookup"><span data-stu-id="d07bb-258">False</span></span>                           |
| <span data-ttu-id="d07bb-259">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="d07bb-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="d07bb-260">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="d07bb-260">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="d07bb-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d07bb-261">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="d07bb-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d07bb-262">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="d07bb-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d07bb-263">Search-Flags</span></span>           | <span data-ttu-id="d07bb-264">0x00000001</span><span class="sxs-lookup"><span data-stu-id="d07bb-264">0x00000001</span></span>                      |
| <span data-ttu-id="d07bb-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d07bb-265">System-Flags</span></span>           | <span data-ttu-id="d07bb-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d07bb-266">0x00000010</span></span>                      |
| <span data-ttu-id="d07bb-267">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="d07bb-267">Classes used in</span></span>        | [<span data-ttu-id="d07bb-268">**In alto**</span><span class="sxs-lookup"><span data-stu-id="d07bb-268">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="d07bb-269">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d07bb-269">Windows Server 2012</span></span>



| <span data-ttu-id="d07bb-270">Voce</span><span class="sxs-lookup"><span data-stu-id="d07bb-270">Entry</span></span> | <span data-ttu-id="d07bb-271">Valore</span><span class="sxs-lookup"><span data-stu-id="d07bb-271">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="d07bb-272">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="d07bb-272">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="d07bb-273">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d07bb-273">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="d07bb-274">System-Only</span><span class="sxs-lookup"><span data-stu-id="d07bb-274">System-Only</span></span>            | <span data-ttu-id="d07bb-275">Falso</span><span class="sxs-lookup"><span data-stu-id="d07bb-275">False</span></span>                           |
| <span data-ttu-id="d07bb-276">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="d07bb-276">Is-Single-Valued</span></span>       | <span data-ttu-id="d07bb-277">Vero</span><span class="sxs-lookup"><span data-stu-id="d07bb-277">True</span></span>                            |
| <span data-ttu-id="d07bb-278">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="d07bb-278">Is Indexed</span></span>             | <span data-ttu-id="d07bb-279">Vero</span><span class="sxs-lookup"><span data-stu-id="d07bb-279">True</span></span>                            |
| <span data-ttu-id="d07bb-280">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="d07bb-280">In Global Catalog</span></span>      | <span data-ttu-id="d07bb-281">Falso</span><span class="sxs-lookup"><span data-stu-id="d07bb-281">False</span></span>                           |
| <span data-ttu-id="d07bb-282">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="d07bb-282">NT-Security-Descriptor</span></span> | <span data-ttu-id="d07bb-283">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="d07bb-283">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="d07bb-284">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d07bb-284">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="d07bb-285">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d07bb-285">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="d07bb-286">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d07bb-286">Search-Flags</span></span>           | <span data-ttu-id="d07bb-287">0x00000001</span><span class="sxs-lookup"><span data-stu-id="d07bb-287">0x00000001</span></span>                      |
| <span data-ttu-id="d07bb-288">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d07bb-288">System-Flags</span></span>           | <span data-ttu-id="d07bb-289">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d07bb-289">0x00000010</span></span>                      |
| <span data-ttu-id="d07bb-290">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="d07bb-290">Classes used in</span></span>        | [<span data-ttu-id="d07bb-291">**In alto**</span><span class="sxs-lookup"><span data-stu-id="d07bb-291">**Top**</span></span>](c-top.md)<br/> |



 

 





