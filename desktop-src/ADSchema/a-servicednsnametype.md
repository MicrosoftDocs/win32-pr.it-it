---
title: Attributo Service-DNS-Name-Type
description: Tipo di record DNS da cercare per il servizio. Ad esempio, A o SRV.
ms.assetid: 9a1ab2ae-b63f-4c70-b0df-de97c482bc5a
ms.tgt_platform: multiple
keywords:
- Servizio-DNS-Name-Type-schema AD
- Schema AD dell'attributo serviceDNSNameType
topic_type:
- apiref
api_name:
- Service-DNS-Name-Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 369bf644cac226788332cb4a2935973a5d5ffeae
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103875150"
---
# <a name="service-dns-name-type-attribute"></a><span data-ttu-id="3c17a-106">Attributo Service-DNS-Name-Type</span><span class="sxs-lookup"><span data-stu-id="3c17a-106">Service-DNS-Name-Type attribute</span></span>

<span data-ttu-id="3c17a-107">Tipo di record DNS da cercare per il servizio.</span><span class="sxs-lookup"><span data-stu-id="3c17a-107">Type of DNS Record to look up for this service.</span></span> <span data-ttu-id="3c17a-108">Ad esempio, A o SRV.</span><span class="sxs-lookup"><span data-stu-id="3c17a-108">For example, A or SRV.</span></span>



| <span data-ttu-id="3c17a-109">Voce</span><span class="sxs-lookup"><span data-stu-id="3c17a-109">Entry</span></span> | <span data-ttu-id="3c17a-110">Valore</span><span class="sxs-lookup"><span data-stu-id="3c17a-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="3c17a-111">CN</span><span class="sxs-lookup"><span data-stu-id="3c17a-111">CN</span></span>                | <span data-ttu-id="3c17a-112">Servizio-DNS-nome-tipo</span><span class="sxs-lookup"><span data-stu-id="3c17a-112">Service-DNS-Name-Type</span></span>                       |
| <span data-ttu-id="3c17a-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="3c17a-113">Ldap-Display-Name</span></span> | <span data-ttu-id="3c17a-114">serviceDNSNameType</span><span class="sxs-lookup"><span data-stu-id="3c17a-114">serviceDNSNameType</span></span>                          |
| <span data-ttu-id="3c17a-115">Dimensione</span><span class="sxs-lookup"><span data-stu-id="3c17a-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="3c17a-116">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="3c17a-116">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="3c17a-117">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="3c17a-117">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="3c17a-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="3c17a-118">Attribute-Id</span></span>      | <span data-ttu-id="3c17a-119">1.2.840.113556.1.4.659</span><span class="sxs-lookup"><span data-stu-id="3c17a-119">1.2.840.113556.1.4.659</span></span>                      |
| <span data-ttu-id="3c17a-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="3c17a-120">System-Id-Guid</span></span>    | <span data-ttu-id="3c17a-121">28630eba-41d5-11d1-a9c1-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="3c17a-121">28630eba-41d5-11d1-a9c1-0000f80367c1</span></span>        |
| <span data-ttu-id="3c17a-122">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3c17a-122">Syntax</span></span>            | [<span data-ttu-id="3c17a-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="3c17a-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="3c17a-124">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="3c17a-124">Implementations</span></span>

-   [<span data-ttu-id="3c17a-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="3c17a-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="3c17a-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="3c17a-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="3c17a-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="3c17a-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="3c17a-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="3c17a-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="3c17a-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="3c17a-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="3c17a-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="3c17a-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="3c17a-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="3c17a-131">Windows 2000 Server</span></span>



| <span data-ttu-id="3c17a-132">Voce</span><span class="sxs-lookup"><span data-stu-id="3c17a-132">Entry</span></span> | <span data-ttu-id="3c17a-133">Valore</span><span class="sxs-lookup"><span data-stu-id="3c17a-133">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="3c17a-134">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="3c17a-134">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="3c17a-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3c17a-135">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="3c17a-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="3c17a-136">System-Only</span></span>            | <span data-ttu-id="3c17a-137">Falso</span><span class="sxs-lookup"><span data-stu-id="3c17a-137">False</span></span>                                                                   |
| <span data-ttu-id="3c17a-138">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="3c17a-138">Is-Single-Valued</span></span>       | <span data-ttu-id="3c17a-139">Vero</span><span class="sxs-lookup"><span data-stu-id="3c17a-139">True</span></span>                                                                    |
| <span data-ttu-id="3c17a-140">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="3c17a-140">Is Indexed</span></span>             | <span data-ttu-id="3c17a-141">Falso</span><span class="sxs-lookup"><span data-stu-id="3c17a-141">False</span></span>                                                                   |
| <span data-ttu-id="3c17a-142">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="3c17a-142">In Global Catalog</span></span>      | <span data-ttu-id="3c17a-143">Falso</span><span class="sxs-lookup"><span data-stu-id="3c17a-143">False</span></span>                                                                   |
| <span data-ttu-id="3c17a-144">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="3c17a-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="3c17a-145">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="3c17a-145">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="3c17a-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3c17a-146">Range-Lower</span></span>            | <span data-ttu-id="3c17a-147">1</span><span class="sxs-lookup"><span data-stu-id="3c17a-147">1</span></span>                                                                       |
| <span data-ttu-id="3c17a-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3c17a-148">Range-Upper</span></span>            | <span data-ttu-id="3c17a-149">256</span><span class="sxs-lookup"><span data-stu-id="3c17a-149">256</span></span>                                                                     |
| <span data-ttu-id="3c17a-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3c17a-150">Search-Flags</span></span>           | <span data-ttu-id="3c17a-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3c17a-151">0x00000000</span></span>                                                              |
| <span data-ttu-id="3c17a-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3c17a-152">System-Flags</span></span>           | <span data-ttu-id="3c17a-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3c17a-153">0x00000010</span></span>                                                              |
| <span data-ttu-id="3c17a-154">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="3c17a-154">Classes used in</span></span>        | [<span data-ttu-id="3c17a-155">**Punto di connessione del servizio**</span><span class="sxs-lookup"><span data-stu-id="3c17a-155">**Service-Connection-Point**</span></span>](c-serviceconnectionpoint.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="3c17a-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3c17a-156">Windows Server 2003</span></span>



| <span data-ttu-id="3c17a-157">Voce</span><span class="sxs-lookup"><span data-stu-id="3c17a-157">Entry</span></span> | <span data-ttu-id="3c17a-158">Valore</span><span class="sxs-lookup"><span data-stu-id="3c17a-158">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="3c17a-159">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="3c17a-159">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="3c17a-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3c17a-160">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="3c17a-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="3c17a-161">System-Only</span></span>            | <span data-ttu-id="3c17a-162">Falso</span><span class="sxs-lookup"><span data-stu-id="3c17a-162">False</span></span>                                                                   |
| <span data-ttu-id="3c17a-163">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="3c17a-163">Is-Single-Valued</span></span>       | <span data-ttu-id="3c17a-164">Vero</span><span class="sxs-lookup"><span data-stu-id="3c17a-164">True</span></span>                                                                    |
| <span data-ttu-id="3c17a-165">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="3c17a-165">Is Indexed</span></span>             | <span data-ttu-id="3c17a-166">Falso</span><span class="sxs-lookup"><span data-stu-id="3c17a-166">False</span></span>                                                                   |
| <span data-ttu-id="3c17a-167">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="3c17a-167">In Global Catalog</span></span>      | <span data-ttu-id="3c17a-168">Falso</span><span class="sxs-lookup"><span data-stu-id="3c17a-168">False</span></span>                                                                   |
| <span data-ttu-id="3c17a-169">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="3c17a-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="3c17a-170">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="3c17a-170">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="3c17a-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3c17a-171">Range-Lower</span></span>            | <span data-ttu-id="3c17a-172">1</span><span class="sxs-lookup"><span data-stu-id="3c17a-172">1</span></span>                                                                       |
| <span data-ttu-id="3c17a-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3c17a-173">Range-Upper</span></span>            | <span data-ttu-id="3c17a-174">256</span><span class="sxs-lookup"><span data-stu-id="3c17a-174">256</span></span>                                                                     |
| <span data-ttu-id="3c17a-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3c17a-175">Search-Flags</span></span>           | <span data-ttu-id="3c17a-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3c17a-176">0x00000000</span></span>                                                              |
| <span data-ttu-id="3c17a-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3c17a-177">System-Flags</span></span>           | <span data-ttu-id="3c17a-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3c17a-178">0x00000010</span></span>                                                              |
| <span data-ttu-id="3c17a-179">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="3c17a-179">Classes used in</span></span>        | [<span data-ttu-id="3c17a-180">**Punto di connessione del servizio**</span><span class="sxs-lookup"><span data-stu-id="3c17a-180">**Service-Connection-Point**</span></span>](c-serviceconnectionpoint.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="3c17a-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="3c17a-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="3c17a-182">Voce</span><span class="sxs-lookup"><span data-stu-id="3c17a-182">Entry</span></span> | <span data-ttu-id="3c17a-183">Valore</span><span class="sxs-lookup"><span data-stu-id="3c17a-183">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="3c17a-184">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="3c17a-184">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="3c17a-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3c17a-185">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="3c17a-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="3c17a-186">System-Only</span></span>            | <span data-ttu-id="3c17a-187">Falso</span><span class="sxs-lookup"><span data-stu-id="3c17a-187">False</span></span>                                                                   |
| <span data-ttu-id="3c17a-188">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="3c17a-188">Is-Single-Valued</span></span>       | <span data-ttu-id="3c17a-189">Vero</span><span class="sxs-lookup"><span data-stu-id="3c17a-189">True</span></span>                                                                    |
| <span data-ttu-id="3c17a-190">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="3c17a-190">Is Indexed</span></span>             | <span data-ttu-id="3c17a-191">Falso</span><span class="sxs-lookup"><span data-stu-id="3c17a-191">False</span></span>                                                                   |
| <span data-ttu-id="3c17a-192">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="3c17a-192">In Global Catalog</span></span>      | <span data-ttu-id="3c17a-193">Falso</span><span class="sxs-lookup"><span data-stu-id="3c17a-193">False</span></span>                                                                   |
| <span data-ttu-id="3c17a-194">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="3c17a-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="3c17a-195">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="3c17a-195">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="3c17a-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3c17a-196">Range-Lower</span></span>            | <span data-ttu-id="3c17a-197">1</span><span class="sxs-lookup"><span data-stu-id="3c17a-197">1</span></span>                                                                       |
| <span data-ttu-id="3c17a-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3c17a-198">Range-Upper</span></span>            | <span data-ttu-id="3c17a-199">256</span><span class="sxs-lookup"><span data-stu-id="3c17a-199">256</span></span>                                                                     |
| <span data-ttu-id="3c17a-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3c17a-200">Search-Flags</span></span>           | <span data-ttu-id="3c17a-201">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3c17a-201">0x00000000</span></span>                                                              |
| <span data-ttu-id="3c17a-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3c17a-202">System-Flags</span></span>           | <span data-ttu-id="3c17a-203">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3c17a-203">0x00000010</span></span>                                                              |
| <span data-ttu-id="3c17a-204">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="3c17a-204">Classes used in</span></span>        | [<span data-ttu-id="3c17a-205">**Punto di connessione del servizio**</span><span class="sxs-lookup"><span data-stu-id="3c17a-205">**Service-Connection-Point**</span></span>](c-serviceconnectionpoint.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="3c17a-206">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3c17a-206">Windows Server 2008</span></span>



| <span data-ttu-id="3c17a-207">Voce</span><span class="sxs-lookup"><span data-stu-id="3c17a-207">Entry</span></span> | <span data-ttu-id="3c17a-208">Valore</span><span class="sxs-lookup"><span data-stu-id="3c17a-208">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="3c17a-209">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="3c17a-209">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="3c17a-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3c17a-210">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="3c17a-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="3c17a-211">System-Only</span></span>            | <span data-ttu-id="3c17a-212">Falso</span><span class="sxs-lookup"><span data-stu-id="3c17a-212">False</span></span>                                                                   |
| <span data-ttu-id="3c17a-213">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="3c17a-213">Is-Single-Valued</span></span>       | <span data-ttu-id="3c17a-214">Vero</span><span class="sxs-lookup"><span data-stu-id="3c17a-214">True</span></span>                                                                    |
| <span data-ttu-id="3c17a-215">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="3c17a-215">Is Indexed</span></span>             | <span data-ttu-id="3c17a-216">Falso</span><span class="sxs-lookup"><span data-stu-id="3c17a-216">False</span></span>                                                                   |
| <span data-ttu-id="3c17a-217">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="3c17a-217">In Global Catalog</span></span>      | <span data-ttu-id="3c17a-218">Falso</span><span class="sxs-lookup"><span data-stu-id="3c17a-218">False</span></span>                                                                   |
| <span data-ttu-id="3c17a-219">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="3c17a-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="3c17a-220">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="3c17a-220">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="3c17a-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3c17a-221">Range-Lower</span></span>            | <span data-ttu-id="3c17a-222">1</span><span class="sxs-lookup"><span data-stu-id="3c17a-222">1</span></span>                                                                       |
| <span data-ttu-id="3c17a-223">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3c17a-223">Range-Upper</span></span>            | <span data-ttu-id="3c17a-224">256</span><span class="sxs-lookup"><span data-stu-id="3c17a-224">256</span></span>                                                                     |
| <span data-ttu-id="3c17a-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3c17a-225">Search-Flags</span></span>           | <span data-ttu-id="3c17a-226">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3c17a-226">0x00000000</span></span>                                                              |
| <span data-ttu-id="3c17a-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3c17a-227">System-Flags</span></span>           | <span data-ttu-id="3c17a-228">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3c17a-228">0x00000010</span></span>                                                              |
| <span data-ttu-id="3c17a-229">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="3c17a-229">Classes used in</span></span>        | [<span data-ttu-id="3c17a-230">**Punto di connessione del servizio**</span><span class="sxs-lookup"><span data-stu-id="3c17a-230">**Service-Connection-Point**</span></span>](c-serviceconnectionpoint.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="3c17a-231">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3c17a-231">Windows Server 2008 R2</span></span>



| <span data-ttu-id="3c17a-232">Voce</span><span class="sxs-lookup"><span data-stu-id="3c17a-232">Entry</span></span> | <span data-ttu-id="3c17a-233">Valore</span><span class="sxs-lookup"><span data-stu-id="3c17a-233">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="3c17a-234">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="3c17a-234">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="3c17a-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3c17a-235">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="3c17a-236">System-Only</span><span class="sxs-lookup"><span data-stu-id="3c17a-236">System-Only</span></span>            | <span data-ttu-id="3c17a-237">Falso</span><span class="sxs-lookup"><span data-stu-id="3c17a-237">False</span></span>                                                                   |
| <span data-ttu-id="3c17a-238">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="3c17a-238">Is-Single-Valued</span></span>       | <span data-ttu-id="3c17a-239">Vero</span><span class="sxs-lookup"><span data-stu-id="3c17a-239">True</span></span>                                                                    |
| <span data-ttu-id="3c17a-240">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="3c17a-240">Is Indexed</span></span>             | <span data-ttu-id="3c17a-241">Falso</span><span class="sxs-lookup"><span data-stu-id="3c17a-241">False</span></span>                                                                   |
| <span data-ttu-id="3c17a-242">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="3c17a-242">In Global Catalog</span></span>      | <span data-ttu-id="3c17a-243">Falso</span><span class="sxs-lookup"><span data-stu-id="3c17a-243">False</span></span>                                                                   |
| <span data-ttu-id="3c17a-244">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="3c17a-244">NT-Security-Descriptor</span></span> | <span data-ttu-id="3c17a-245">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="3c17a-245">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="3c17a-246">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3c17a-246">Range-Lower</span></span>            | <span data-ttu-id="3c17a-247">1</span><span class="sxs-lookup"><span data-stu-id="3c17a-247">1</span></span>                                                                       |
| <span data-ttu-id="3c17a-248">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3c17a-248">Range-Upper</span></span>            | <span data-ttu-id="3c17a-249">256</span><span class="sxs-lookup"><span data-stu-id="3c17a-249">256</span></span>                                                                     |
| <span data-ttu-id="3c17a-250">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3c17a-250">Search-Flags</span></span>           | <span data-ttu-id="3c17a-251">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3c17a-251">0x00000000</span></span>                                                              |
| <span data-ttu-id="3c17a-252">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3c17a-252">System-Flags</span></span>           | <span data-ttu-id="3c17a-253">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3c17a-253">0x00000010</span></span>                                                              |
| <span data-ttu-id="3c17a-254">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="3c17a-254">Classes used in</span></span>        | [<span data-ttu-id="3c17a-255">**Punto di connessione del servizio**</span><span class="sxs-lookup"><span data-stu-id="3c17a-255">**Service-Connection-Point**</span></span>](c-serviceconnectionpoint.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="3c17a-256">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3c17a-256">Windows Server 2012</span></span>



| <span data-ttu-id="3c17a-257">Voce</span><span class="sxs-lookup"><span data-stu-id="3c17a-257">Entry</span></span> | <span data-ttu-id="3c17a-258">Valore</span><span class="sxs-lookup"><span data-stu-id="3c17a-258">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="3c17a-259">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="3c17a-259">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="3c17a-260">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3c17a-260">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="3c17a-261">System-Only</span><span class="sxs-lookup"><span data-stu-id="3c17a-261">System-Only</span></span>            | <span data-ttu-id="3c17a-262">Falso</span><span class="sxs-lookup"><span data-stu-id="3c17a-262">False</span></span>                                                                   |
| <span data-ttu-id="3c17a-263">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="3c17a-263">Is-Single-Valued</span></span>       | <span data-ttu-id="3c17a-264">Vero</span><span class="sxs-lookup"><span data-stu-id="3c17a-264">True</span></span>                                                                    |
| <span data-ttu-id="3c17a-265">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="3c17a-265">Is Indexed</span></span>             | <span data-ttu-id="3c17a-266">Falso</span><span class="sxs-lookup"><span data-stu-id="3c17a-266">False</span></span>                                                                   |
| <span data-ttu-id="3c17a-267">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="3c17a-267">In Global Catalog</span></span>      | <span data-ttu-id="3c17a-268">Falso</span><span class="sxs-lookup"><span data-stu-id="3c17a-268">False</span></span>                                                                   |
| <span data-ttu-id="3c17a-269">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="3c17a-269">NT-Security-Descriptor</span></span> | <span data-ttu-id="3c17a-270">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="3c17a-270">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="3c17a-271">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3c17a-271">Range-Lower</span></span>            | <span data-ttu-id="3c17a-272">1</span><span class="sxs-lookup"><span data-stu-id="3c17a-272">1</span></span>                                                                       |
| <span data-ttu-id="3c17a-273">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3c17a-273">Range-Upper</span></span>            | <span data-ttu-id="3c17a-274">256</span><span class="sxs-lookup"><span data-stu-id="3c17a-274">256</span></span>                                                                     |
| <span data-ttu-id="3c17a-275">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3c17a-275">Search-Flags</span></span>           | <span data-ttu-id="3c17a-276">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3c17a-276">0x00000000</span></span>                                                              |
| <span data-ttu-id="3c17a-277">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3c17a-277">System-Flags</span></span>           | <span data-ttu-id="3c17a-278">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3c17a-278">0x00000010</span></span>                                                              |
| <span data-ttu-id="3c17a-279">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="3c17a-279">Classes used in</span></span>        | [<span data-ttu-id="3c17a-280">**Punto di connessione del servizio**</span><span class="sxs-lookup"><span data-stu-id="3c17a-280">**Service-Connection-Point**</span></span>](c-serviceconnectionpoint.md)<br/> |



 

 





