---
title: Attributo additional-trusted-service-names
description: Elenco di servizi del dominio che possono essere considerati attendibili. Non usato da AD.
ms.assetid: 0c574a99-4036-408b-807c-b4b3394624c7
ms.tgt_platform: multiple
keywords:
- Attributo di AD aggiuntivo-trusted-service-names
- Schema AD dell'attributo additionalTrustedServiceNames
topic_type:
- apiref
api_name:
- Additional-Trusted-Service-Names
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8066190082cfe0f1bbb8825768ad135090a7a4f8
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "106303625"
---
# <a name="additional-trusted-service-names-attribute"></a><span data-ttu-id="1daa7-106">Attributo additional-trusted-service-names</span><span class="sxs-lookup"><span data-stu-id="1daa7-106">Additional-Trusted-Service-Names attribute</span></span>

<span data-ttu-id="1daa7-107">Elenco di servizi del dominio che possono essere considerati attendibili.</span><span class="sxs-lookup"><span data-stu-id="1daa7-107">A list of services in the domain that can be trusted.</span></span> <span data-ttu-id="1daa7-108">Non usato da AD.</span><span class="sxs-lookup"><span data-stu-id="1daa7-108">Not used by AD.</span></span>



| <span data-ttu-id="1daa7-109">Voce</span><span class="sxs-lookup"><span data-stu-id="1daa7-109">Entry</span></span> | <span data-ttu-id="1daa7-110">Valore</span><span class="sxs-lookup"><span data-stu-id="1daa7-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="1daa7-111">CN</span><span class="sxs-lookup"><span data-stu-id="1daa7-111">CN</span></span>                | <span data-ttu-id="1daa7-112">Nomi aggiuntivi-attendibili-servizi</span><span class="sxs-lookup"><span data-stu-id="1daa7-112">Additional-Trusted-Service-Names</span></span>            |
| <span data-ttu-id="1daa7-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="1daa7-113">Ldap-Display-Name</span></span> | <span data-ttu-id="1daa7-114">additionalTrustedServiceNames</span><span class="sxs-lookup"><span data-stu-id="1daa7-114">additionalTrustedServiceNames</span></span>               |
| <span data-ttu-id="1daa7-115">Dimensione</span><span class="sxs-lookup"><span data-stu-id="1daa7-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="1daa7-116">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="1daa7-116">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="1daa7-117">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="1daa7-117">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="1daa7-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="1daa7-118">Attribute-Id</span></span>      | <span data-ttu-id="1daa7-119">1.2.840.113556.1.4.889</span><span class="sxs-lookup"><span data-stu-id="1daa7-119">1.2.840.113556.1.4.889</span></span>                      |
| <span data-ttu-id="1daa7-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="1daa7-120">System-Id-Guid</span></span>    | <span data-ttu-id="1daa7-121">032160be-9824-11d1-aec0-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="1daa7-121">032160be-9824-11d1-aec0-0000f80367c1</span></span>        |
| <span data-ttu-id="1daa7-122">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1daa7-122">Syntax</span></span>            | [<span data-ttu-id="1daa7-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="1daa7-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="1daa7-124">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="1daa7-124">Implementations</span></span>

-   [<span data-ttu-id="1daa7-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="1daa7-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="1daa7-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="1daa7-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="1daa7-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="1daa7-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="1daa7-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="1daa7-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="1daa7-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="1daa7-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="1daa7-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="1daa7-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="1daa7-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1daa7-131">Windows 2000 Server</span></span>



| <span data-ttu-id="1daa7-132">Voce</span><span class="sxs-lookup"><span data-stu-id="1daa7-132">Entry</span></span> | <span data-ttu-id="1daa7-133">Valore</span><span class="sxs-lookup"><span data-stu-id="1daa7-133">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="1daa7-134">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="1daa7-134">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="1daa7-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1daa7-135">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="1daa7-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="1daa7-136">System-Only</span></span>            | <span data-ttu-id="1daa7-137">Falso</span><span class="sxs-lookup"><span data-stu-id="1daa7-137">False</span></span>                                                |
| <span data-ttu-id="1daa7-138">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="1daa7-138">Is-Single-Valued</span></span>       | <span data-ttu-id="1daa7-139">Falso</span><span class="sxs-lookup"><span data-stu-id="1daa7-139">False</span></span>                                                |
| <span data-ttu-id="1daa7-140">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="1daa7-140">Is Indexed</span></span>             | <span data-ttu-id="1daa7-141">Falso</span><span class="sxs-lookup"><span data-stu-id="1daa7-141">False</span></span>                                                |
| <span data-ttu-id="1daa7-142">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="1daa7-142">In Global Catalog</span></span>      | <span data-ttu-id="1daa7-143">Falso</span><span class="sxs-lookup"><span data-stu-id="1daa7-143">False</span></span>                                                |
| <span data-ttu-id="1daa7-144">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="1daa7-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="1daa7-145">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="1daa7-145">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="1daa7-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1daa7-146">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="1daa7-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1daa7-147">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="1daa7-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1daa7-148">Search-Flags</span></span>           | <span data-ttu-id="1daa7-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1daa7-149">0x00000000</span></span>                                           |
| <span data-ttu-id="1daa7-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1daa7-150">System-Flags</span></span>           | <span data-ttu-id="1daa7-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1daa7-151">0x00000010</span></span>                                           |
| <span data-ttu-id="1daa7-152">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="1daa7-152">Classes used in</span></span>        | [<span data-ttu-id="1daa7-153">**Dominio trusted**</span><span class="sxs-lookup"><span data-stu-id="1daa7-153">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="1daa7-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1daa7-154">Windows Server 2003</span></span>



| <span data-ttu-id="1daa7-155">Voce</span><span class="sxs-lookup"><span data-stu-id="1daa7-155">Entry</span></span> | <span data-ttu-id="1daa7-156">Valore</span><span class="sxs-lookup"><span data-stu-id="1daa7-156">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="1daa7-157">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="1daa7-157">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="1daa7-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1daa7-158">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="1daa7-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="1daa7-159">System-Only</span></span>            | <span data-ttu-id="1daa7-160">Falso</span><span class="sxs-lookup"><span data-stu-id="1daa7-160">False</span></span>                                                |
| <span data-ttu-id="1daa7-161">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="1daa7-161">Is-Single-Valued</span></span>       | <span data-ttu-id="1daa7-162">Falso</span><span class="sxs-lookup"><span data-stu-id="1daa7-162">False</span></span>                                                |
| <span data-ttu-id="1daa7-163">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="1daa7-163">Is Indexed</span></span>             | <span data-ttu-id="1daa7-164">Falso</span><span class="sxs-lookup"><span data-stu-id="1daa7-164">False</span></span>                                                |
| <span data-ttu-id="1daa7-165">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="1daa7-165">In Global Catalog</span></span>      | <span data-ttu-id="1daa7-166">Falso</span><span class="sxs-lookup"><span data-stu-id="1daa7-166">False</span></span>                                                |
| <span data-ttu-id="1daa7-167">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="1daa7-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="1daa7-168">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="1daa7-168">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="1daa7-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1daa7-169">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="1daa7-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1daa7-170">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="1daa7-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1daa7-171">Search-Flags</span></span>           | <span data-ttu-id="1daa7-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1daa7-172">0x00000000</span></span>                                           |
| <span data-ttu-id="1daa7-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1daa7-173">System-Flags</span></span>           | <span data-ttu-id="1daa7-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1daa7-174">0x00000010</span></span>                                           |
| <span data-ttu-id="1daa7-175">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="1daa7-175">Classes used in</span></span>        | [<span data-ttu-id="1daa7-176">**Dominio trusted**</span><span class="sxs-lookup"><span data-stu-id="1daa7-176">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="1daa7-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="1daa7-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="1daa7-178">Voce</span><span class="sxs-lookup"><span data-stu-id="1daa7-178">Entry</span></span> | <span data-ttu-id="1daa7-179">Valore</span><span class="sxs-lookup"><span data-stu-id="1daa7-179">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="1daa7-180">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="1daa7-180">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="1daa7-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1daa7-181">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="1daa7-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="1daa7-182">System-Only</span></span>            | <span data-ttu-id="1daa7-183">Falso</span><span class="sxs-lookup"><span data-stu-id="1daa7-183">False</span></span>                                                |
| <span data-ttu-id="1daa7-184">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="1daa7-184">Is-Single-Valued</span></span>       | <span data-ttu-id="1daa7-185">Falso</span><span class="sxs-lookup"><span data-stu-id="1daa7-185">False</span></span>                                                |
| <span data-ttu-id="1daa7-186">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="1daa7-186">Is Indexed</span></span>             | <span data-ttu-id="1daa7-187">Falso</span><span class="sxs-lookup"><span data-stu-id="1daa7-187">False</span></span>                                                |
| <span data-ttu-id="1daa7-188">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="1daa7-188">In Global Catalog</span></span>      | <span data-ttu-id="1daa7-189">Falso</span><span class="sxs-lookup"><span data-stu-id="1daa7-189">False</span></span>                                                |
| <span data-ttu-id="1daa7-190">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="1daa7-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="1daa7-191">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="1daa7-191">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="1daa7-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1daa7-192">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="1daa7-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1daa7-193">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="1daa7-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1daa7-194">Search-Flags</span></span>           | <span data-ttu-id="1daa7-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1daa7-195">0x00000000</span></span>                                           |
| <span data-ttu-id="1daa7-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1daa7-196">System-Flags</span></span>           | <span data-ttu-id="1daa7-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1daa7-197">0x00000010</span></span>                                           |
| <span data-ttu-id="1daa7-198">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="1daa7-198">Classes used in</span></span>        | [<span data-ttu-id="1daa7-199">**Dominio trusted**</span><span class="sxs-lookup"><span data-stu-id="1daa7-199">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="1daa7-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1daa7-200">Windows Server 2008</span></span>



| <span data-ttu-id="1daa7-201">Voce</span><span class="sxs-lookup"><span data-stu-id="1daa7-201">Entry</span></span> | <span data-ttu-id="1daa7-202">Valore</span><span class="sxs-lookup"><span data-stu-id="1daa7-202">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="1daa7-203">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="1daa7-203">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="1daa7-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1daa7-204">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="1daa7-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="1daa7-205">System-Only</span></span>            | <span data-ttu-id="1daa7-206">Falso</span><span class="sxs-lookup"><span data-stu-id="1daa7-206">False</span></span>                                                |
| <span data-ttu-id="1daa7-207">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="1daa7-207">Is-Single-Valued</span></span>       | <span data-ttu-id="1daa7-208">Falso</span><span class="sxs-lookup"><span data-stu-id="1daa7-208">False</span></span>                                                |
| <span data-ttu-id="1daa7-209">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="1daa7-209">Is Indexed</span></span>             | <span data-ttu-id="1daa7-210">Falso</span><span class="sxs-lookup"><span data-stu-id="1daa7-210">False</span></span>                                                |
| <span data-ttu-id="1daa7-211">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="1daa7-211">In Global Catalog</span></span>      | <span data-ttu-id="1daa7-212">Falso</span><span class="sxs-lookup"><span data-stu-id="1daa7-212">False</span></span>                                                |
| <span data-ttu-id="1daa7-213">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="1daa7-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="1daa7-214">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="1daa7-214">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="1daa7-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1daa7-215">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="1daa7-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1daa7-216">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="1daa7-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1daa7-217">Search-Flags</span></span>           | <span data-ttu-id="1daa7-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1daa7-218">0x00000000</span></span>                                           |
| <span data-ttu-id="1daa7-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1daa7-219">System-Flags</span></span>           | <span data-ttu-id="1daa7-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1daa7-220">0x00000010</span></span>                                           |
| <span data-ttu-id="1daa7-221">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="1daa7-221">Classes used in</span></span>        | [<span data-ttu-id="1daa7-222">**Dominio trusted**</span><span class="sxs-lookup"><span data-stu-id="1daa7-222">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="1daa7-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1daa7-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="1daa7-224">Voce</span><span class="sxs-lookup"><span data-stu-id="1daa7-224">Entry</span></span> | <span data-ttu-id="1daa7-225">Valore</span><span class="sxs-lookup"><span data-stu-id="1daa7-225">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="1daa7-226">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="1daa7-226">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="1daa7-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1daa7-227">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="1daa7-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="1daa7-228">System-Only</span></span>            | <span data-ttu-id="1daa7-229">Falso</span><span class="sxs-lookup"><span data-stu-id="1daa7-229">False</span></span>                                                |
| <span data-ttu-id="1daa7-230">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="1daa7-230">Is-Single-Valued</span></span>       | <span data-ttu-id="1daa7-231">Falso</span><span class="sxs-lookup"><span data-stu-id="1daa7-231">False</span></span>                                                |
| <span data-ttu-id="1daa7-232">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="1daa7-232">Is Indexed</span></span>             | <span data-ttu-id="1daa7-233">Falso</span><span class="sxs-lookup"><span data-stu-id="1daa7-233">False</span></span>                                                |
| <span data-ttu-id="1daa7-234">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="1daa7-234">In Global Catalog</span></span>      | <span data-ttu-id="1daa7-235">Falso</span><span class="sxs-lookup"><span data-stu-id="1daa7-235">False</span></span>                                                |
| <span data-ttu-id="1daa7-236">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="1daa7-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="1daa7-237">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="1daa7-237">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="1daa7-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1daa7-238">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="1daa7-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1daa7-239">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="1daa7-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1daa7-240">Search-Flags</span></span>           | <span data-ttu-id="1daa7-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1daa7-241">0x00000000</span></span>                                           |
| <span data-ttu-id="1daa7-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1daa7-242">System-Flags</span></span>           | <span data-ttu-id="1daa7-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1daa7-243">0x00000010</span></span>                                           |
| <span data-ttu-id="1daa7-244">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="1daa7-244">Classes used in</span></span>        | [<span data-ttu-id="1daa7-245">**Dominio trusted**</span><span class="sxs-lookup"><span data-stu-id="1daa7-245">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="1daa7-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1daa7-246">Windows Server 2012</span></span>



| <span data-ttu-id="1daa7-247">Voce</span><span class="sxs-lookup"><span data-stu-id="1daa7-247">Entry</span></span> | <span data-ttu-id="1daa7-248">Valore</span><span class="sxs-lookup"><span data-stu-id="1daa7-248">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="1daa7-249">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="1daa7-249">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="1daa7-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1daa7-250">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="1daa7-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="1daa7-251">System-Only</span></span>            | <span data-ttu-id="1daa7-252">Falso</span><span class="sxs-lookup"><span data-stu-id="1daa7-252">False</span></span>                                                |
| <span data-ttu-id="1daa7-253">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="1daa7-253">Is-Single-Valued</span></span>       | <span data-ttu-id="1daa7-254">Falso</span><span class="sxs-lookup"><span data-stu-id="1daa7-254">False</span></span>                                                |
| <span data-ttu-id="1daa7-255">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="1daa7-255">Is Indexed</span></span>             | <span data-ttu-id="1daa7-256">Falso</span><span class="sxs-lookup"><span data-stu-id="1daa7-256">False</span></span>                                                |
| <span data-ttu-id="1daa7-257">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="1daa7-257">In Global Catalog</span></span>      | <span data-ttu-id="1daa7-258">Falso</span><span class="sxs-lookup"><span data-stu-id="1daa7-258">False</span></span>                                                |
| <span data-ttu-id="1daa7-259">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="1daa7-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="1daa7-260">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="1daa7-260">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="1daa7-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1daa7-261">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="1daa7-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1daa7-262">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="1daa7-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1daa7-263">Search-Flags</span></span>           | <span data-ttu-id="1daa7-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1daa7-264">0x00000000</span></span>                                           |
| <span data-ttu-id="1daa7-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1daa7-265">System-Flags</span></span>           | <span data-ttu-id="1daa7-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1daa7-266">0x00000010</span></span>                                           |
| <span data-ttu-id="1daa7-267">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="1daa7-267">Classes used in</span></span>        | [<span data-ttu-id="1daa7-268">**Dominio trusted**</span><span class="sxs-lookup"><span data-stu-id="1daa7-268">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



 

 





