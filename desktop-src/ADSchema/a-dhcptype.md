---
title: attributo di tipo DHCP
description: Tipo di server DHCP.
ms.assetid: 46ab7db7-a752-45aa-a10b-1195b5cf6f80
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo di tipo DHCP
- Schema AD dell'attributo dhcpType
topic_type:
- apiref
api_name:
- dhcp-Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b5a5a331ff7298854f4ca070799a05e2a3497f2
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103965103"
---
# <a name="dhcp-type-attribute"></a><span data-ttu-id="79c94-105">attributo di tipo DHCP</span><span class="sxs-lookup"><span data-stu-id="79c94-105">dhcp-Type attribute</span></span>

<span data-ttu-id="79c94-106">Tipo di server DHCP.</span><span class="sxs-lookup"><span data-stu-id="79c94-106">The type of DHCP server.</span></span> <span data-ttu-id="79c94-107">Questo attributo è impostato su tutti gli oggetti di objectClass [**dHCPClass**](c-dhcpclass.md).</span><span class="sxs-lookup"><span data-stu-id="79c94-107">This attribute is set on all objects of objectClass [**dHCPClass**](c-dhcpclass.md).</span></span> <span data-ttu-id="79c94-108">Il valore definisce il tipo di oggetto:</span><span class="sxs-lookup"><span data-stu-id="79c94-108">Its value defines the type of object:</span></span>

``` syntax
  0 - DHCP Root Object
  1 - DHCP Server
```



| <span data-ttu-id="79c94-109">Voce</span><span class="sxs-lookup"><span data-stu-id="79c94-109">Entry</span></span> | <span data-ttu-id="79c94-110">Valore</span><span class="sxs-lookup"><span data-stu-id="79c94-110">Value</span></span> |
|-------------------|--------------------------------------------------------|
| <span data-ttu-id="79c94-111">CN</span><span class="sxs-lookup"><span data-stu-id="79c94-111">CN</span></span>                | <span data-ttu-id="79c94-112">Tipo DHCP</span><span class="sxs-lookup"><span data-stu-id="79c94-112">dhcp-Type</span></span>                                              |
| <span data-ttu-id="79c94-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="79c94-113">Ldap-Display-Name</span></span> | <span data-ttu-id="79c94-114">dhcpType</span><span class="sxs-lookup"><span data-stu-id="79c94-114">dhcpType</span></span>                                               |
| <span data-ttu-id="79c94-115">Dimensione</span><span class="sxs-lookup"><span data-stu-id="79c94-115">Size</span></span>              | <span data-ttu-id="79c94-116">4 byte</span><span class="sxs-lookup"><span data-stu-id="79c94-116">4 bytes</span></span>                                                |
| <span data-ttu-id="79c94-117">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="79c94-117">Update Privilege</span></span>  | <span data-ttu-id="79c94-118">Amministratore di dominio.</span><span class="sxs-lookup"><span data-stu-id="79c94-118">Domain administrator.</span></span>                                  |
| <span data-ttu-id="79c94-119">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="79c94-119">Update Frequency</span></span>  | <span data-ttu-id="79c94-120">Quando un nuovo server viene aggiunto o rimosso dalla foresta.</span><span class="sxs-lookup"><span data-stu-id="79c94-120">When a new server is added or removed from the forest.</span></span> |
| <span data-ttu-id="79c94-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="79c94-121">Attribute-Id</span></span>      | <span data-ttu-id="79c94-122">1.2.840.113556.1.4.699</span><span class="sxs-lookup"><span data-stu-id="79c94-122">1.2.840.113556.1.4.699</span></span>                                 |
| <span data-ttu-id="79c94-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="79c94-123">System-Id-Guid</span></span>    | <span data-ttu-id="79c94-124">963d273b-48be-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="79c94-124">963d273b-48be-11d1-a9c3-0000f80367c1</span></span>                   |
| <span data-ttu-id="79c94-125">Sintassi</span><span class="sxs-lookup"><span data-stu-id="79c94-125">Syntax</span></span>            | [<span data-ttu-id="79c94-126">**Enumerazione**</span><span class="sxs-lookup"><span data-stu-id="79c94-126">**Enumeration**</span></span>](s-enumeration.md)                   |



## <a name="implementations"></a><span data-ttu-id="79c94-127">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="79c94-127">Implementations</span></span>

-   [<span data-ttu-id="79c94-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="79c94-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="79c94-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="79c94-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="79c94-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="79c94-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="79c94-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="79c94-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="79c94-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="79c94-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="79c94-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="79c94-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="79c94-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="79c94-134">Windows 2000 Server</span></span>



| <span data-ttu-id="79c94-135">Voce</span><span class="sxs-lookup"><span data-stu-id="79c94-135">Entry</span></span> | <span data-ttu-id="79c94-136">Valore</span><span class="sxs-lookup"><span data-stu-id="79c94-136">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="79c94-137">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="79c94-137">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="79c94-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="79c94-138">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="79c94-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="79c94-139">System-Only</span></span>            | <span data-ttu-id="79c94-140">Falso</span><span class="sxs-lookup"><span data-stu-id="79c94-140">False</span></span>                                        |
| <span data-ttu-id="79c94-141">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="79c94-141">Is-Single-Valued</span></span>       | <span data-ttu-id="79c94-142">Vero</span><span class="sxs-lookup"><span data-stu-id="79c94-142">True</span></span>                                         |
| <span data-ttu-id="79c94-143">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="79c94-143">Is Indexed</span></span>             | <span data-ttu-id="79c94-144">Vero</span><span class="sxs-lookup"><span data-stu-id="79c94-144">True</span></span>                                         |
| <span data-ttu-id="79c94-145">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="79c94-145">In Global Catalog</span></span>      | <span data-ttu-id="79c94-146">Falso</span><span class="sxs-lookup"><span data-stu-id="79c94-146">False</span></span>                                        |
| <span data-ttu-id="79c94-147">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="79c94-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="79c94-148">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="79c94-148">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="79c94-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="79c94-149">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="79c94-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="79c94-150">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="79c94-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="79c94-151">Search-Flags</span></span>           | <span data-ttu-id="79c94-152">0x00000001</span><span class="sxs-lookup"><span data-stu-id="79c94-152">0x00000001</span></span>                                   |
| <span data-ttu-id="79c94-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="79c94-153">System-Flags</span></span>           | <span data-ttu-id="79c94-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="79c94-154">0x00000010</span></span>                                   |
| <span data-ttu-id="79c94-155">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="79c94-155">Classes used in</span></span>        | [<span data-ttu-id="79c94-156">**Classe DHCP**</span><span class="sxs-lookup"><span data-stu-id="79c94-156">**DHCP-Class**</span></span>](c-dhcpclass.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="79c94-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="79c94-157">Windows Server 2003</span></span>



| <span data-ttu-id="79c94-158">Voce</span><span class="sxs-lookup"><span data-stu-id="79c94-158">Entry</span></span> | <span data-ttu-id="79c94-159">Valore</span><span class="sxs-lookup"><span data-stu-id="79c94-159">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="79c94-160">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="79c94-160">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="79c94-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="79c94-161">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="79c94-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="79c94-162">System-Only</span></span>            | <span data-ttu-id="79c94-163">Falso</span><span class="sxs-lookup"><span data-stu-id="79c94-163">False</span></span>                                        |
| <span data-ttu-id="79c94-164">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="79c94-164">Is-Single-Valued</span></span>       | <span data-ttu-id="79c94-165">Vero</span><span class="sxs-lookup"><span data-stu-id="79c94-165">True</span></span>                                         |
| <span data-ttu-id="79c94-166">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="79c94-166">Is Indexed</span></span>             | <span data-ttu-id="79c94-167">Vero</span><span class="sxs-lookup"><span data-stu-id="79c94-167">True</span></span>                                         |
| <span data-ttu-id="79c94-168">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="79c94-168">In Global Catalog</span></span>      | <span data-ttu-id="79c94-169">Falso</span><span class="sxs-lookup"><span data-stu-id="79c94-169">False</span></span>                                        |
| <span data-ttu-id="79c94-170">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="79c94-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="79c94-171">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="79c94-171">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="79c94-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="79c94-172">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="79c94-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="79c94-173">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="79c94-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="79c94-174">Search-Flags</span></span>           | <span data-ttu-id="79c94-175">0x00000001</span><span class="sxs-lookup"><span data-stu-id="79c94-175">0x00000001</span></span>                                   |
| <span data-ttu-id="79c94-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="79c94-176">System-Flags</span></span>           | <span data-ttu-id="79c94-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="79c94-177">0x00000010</span></span>                                   |
| <span data-ttu-id="79c94-178">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="79c94-178">Classes used in</span></span>        | [<span data-ttu-id="79c94-179">**Classe DHCP**</span><span class="sxs-lookup"><span data-stu-id="79c94-179">**DHCP-Class**</span></span>](c-dhcpclass.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="79c94-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="79c94-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="79c94-181">Voce</span><span class="sxs-lookup"><span data-stu-id="79c94-181">Entry</span></span> | <span data-ttu-id="79c94-182">Valore</span><span class="sxs-lookup"><span data-stu-id="79c94-182">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="79c94-183">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="79c94-183">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="79c94-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="79c94-184">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="79c94-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="79c94-185">System-Only</span></span>            | <span data-ttu-id="79c94-186">Falso</span><span class="sxs-lookup"><span data-stu-id="79c94-186">False</span></span>                                        |
| <span data-ttu-id="79c94-187">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="79c94-187">Is-Single-Valued</span></span>       | <span data-ttu-id="79c94-188">Vero</span><span class="sxs-lookup"><span data-stu-id="79c94-188">True</span></span>                                         |
| <span data-ttu-id="79c94-189">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="79c94-189">Is Indexed</span></span>             | <span data-ttu-id="79c94-190">Vero</span><span class="sxs-lookup"><span data-stu-id="79c94-190">True</span></span>                                         |
| <span data-ttu-id="79c94-191">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="79c94-191">In Global Catalog</span></span>      | <span data-ttu-id="79c94-192">Falso</span><span class="sxs-lookup"><span data-stu-id="79c94-192">False</span></span>                                        |
| <span data-ttu-id="79c94-193">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="79c94-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="79c94-194">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="79c94-194">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="79c94-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="79c94-195">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="79c94-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="79c94-196">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="79c94-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="79c94-197">Search-Flags</span></span>           | <span data-ttu-id="79c94-198">0x00000001</span><span class="sxs-lookup"><span data-stu-id="79c94-198">0x00000001</span></span>                                   |
| <span data-ttu-id="79c94-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="79c94-199">System-Flags</span></span>           | <span data-ttu-id="79c94-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="79c94-200">0x00000010</span></span>                                   |
| <span data-ttu-id="79c94-201">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="79c94-201">Classes used in</span></span>        | [<span data-ttu-id="79c94-202">**Classe DHCP**</span><span class="sxs-lookup"><span data-stu-id="79c94-202">**DHCP-Class**</span></span>](c-dhcpclass.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="79c94-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="79c94-203">Windows Server 2008</span></span>



| <span data-ttu-id="79c94-204">Voce</span><span class="sxs-lookup"><span data-stu-id="79c94-204">Entry</span></span> | <span data-ttu-id="79c94-205">Valore</span><span class="sxs-lookup"><span data-stu-id="79c94-205">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="79c94-206">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="79c94-206">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="79c94-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="79c94-207">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="79c94-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="79c94-208">System-Only</span></span>            | <span data-ttu-id="79c94-209">Falso</span><span class="sxs-lookup"><span data-stu-id="79c94-209">False</span></span>                                        |
| <span data-ttu-id="79c94-210">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="79c94-210">Is-Single-Valued</span></span>       | <span data-ttu-id="79c94-211">Vero</span><span class="sxs-lookup"><span data-stu-id="79c94-211">True</span></span>                                         |
| <span data-ttu-id="79c94-212">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="79c94-212">Is Indexed</span></span>             | <span data-ttu-id="79c94-213">Vero</span><span class="sxs-lookup"><span data-stu-id="79c94-213">True</span></span>                                         |
| <span data-ttu-id="79c94-214">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="79c94-214">In Global Catalog</span></span>      | <span data-ttu-id="79c94-215">Falso</span><span class="sxs-lookup"><span data-stu-id="79c94-215">False</span></span>                                        |
| <span data-ttu-id="79c94-216">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="79c94-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="79c94-217">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="79c94-217">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="79c94-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="79c94-218">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="79c94-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="79c94-219">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="79c94-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="79c94-220">Search-Flags</span></span>           | <span data-ttu-id="79c94-221">0x00000001</span><span class="sxs-lookup"><span data-stu-id="79c94-221">0x00000001</span></span>                                   |
| <span data-ttu-id="79c94-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="79c94-222">System-Flags</span></span>           | <span data-ttu-id="79c94-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="79c94-223">0x00000010</span></span>                                   |
| <span data-ttu-id="79c94-224">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="79c94-224">Classes used in</span></span>        | [<span data-ttu-id="79c94-225">**Classe DHCP**</span><span class="sxs-lookup"><span data-stu-id="79c94-225">**DHCP-Class**</span></span>](c-dhcpclass.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="79c94-226">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="79c94-226">Windows Server 2008 R2</span></span>



| <span data-ttu-id="79c94-227">Voce</span><span class="sxs-lookup"><span data-stu-id="79c94-227">Entry</span></span> | <span data-ttu-id="79c94-228">Valore</span><span class="sxs-lookup"><span data-stu-id="79c94-228">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="79c94-229">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="79c94-229">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="79c94-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="79c94-230">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="79c94-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="79c94-231">System-Only</span></span>            | <span data-ttu-id="79c94-232">Falso</span><span class="sxs-lookup"><span data-stu-id="79c94-232">False</span></span>                                        |
| <span data-ttu-id="79c94-233">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="79c94-233">Is-Single-Valued</span></span>       | <span data-ttu-id="79c94-234">Vero</span><span class="sxs-lookup"><span data-stu-id="79c94-234">True</span></span>                                         |
| <span data-ttu-id="79c94-235">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="79c94-235">Is Indexed</span></span>             | <span data-ttu-id="79c94-236">Vero</span><span class="sxs-lookup"><span data-stu-id="79c94-236">True</span></span>                                         |
| <span data-ttu-id="79c94-237">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="79c94-237">In Global Catalog</span></span>      | <span data-ttu-id="79c94-238">Falso</span><span class="sxs-lookup"><span data-stu-id="79c94-238">False</span></span>                                        |
| <span data-ttu-id="79c94-239">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="79c94-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="79c94-240">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="79c94-240">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="79c94-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="79c94-241">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="79c94-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="79c94-242">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="79c94-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="79c94-243">Search-Flags</span></span>           | <span data-ttu-id="79c94-244">0x00000001</span><span class="sxs-lookup"><span data-stu-id="79c94-244">0x00000001</span></span>                                   |
| <span data-ttu-id="79c94-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="79c94-245">System-Flags</span></span>           | <span data-ttu-id="79c94-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="79c94-246">0x00000010</span></span>                                   |
| <span data-ttu-id="79c94-247">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="79c94-247">Classes used in</span></span>        | [<span data-ttu-id="79c94-248">**Classe DHCP**</span><span class="sxs-lookup"><span data-stu-id="79c94-248">**DHCP-Class**</span></span>](c-dhcpclass.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="79c94-249">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="79c94-249">Windows Server 2012</span></span>



| <span data-ttu-id="79c94-250">Voce</span><span class="sxs-lookup"><span data-stu-id="79c94-250">Entry</span></span> | <span data-ttu-id="79c94-251">Valore</span><span class="sxs-lookup"><span data-stu-id="79c94-251">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="79c94-252">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="79c94-252">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="79c94-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="79c94-253">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="79c94-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="79c94-254">System-Only</span></span>            | <span data-ttu-id="79c94-255">Falso</span><span class="sxs-lookup"><span data-stu-id="79c94-255">False</span></span>                                        |
| <span data-ttu-id="79c94-256">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="79c94-256">Is-Single-Valued</span></span>       | <span data-ttu-id="79c94-257">Vero</span><span class="sxs-lookup"><span data-stu-id="79c94-257">True</span></span>                                         |
| <span data-ttu-id="79c94-258">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="79c94-258">Is Indexed</span></span>             | <span data-ttu-id="79c94-259">Vero</span><span class="sxs-lookup"><span data-stu-id="79c94-259">True</span></span>                                         |
| <span data-ttu-id="79c94-260">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="79c94-260">In Global Catalog</span></span>      | <span data-ttu-id="79c94-261">Falso</span><span class="sxs-lookup"><span data-stu-id="79c94-261">False</span></span>                                        |
| <span data-ttu-id="79c94-262">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="79c94-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="79c94-263">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="79c94-263">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="79c94-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="79c94-264">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="79c94-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="79c94-265">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="79c94-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="79c94-266">Search-Flags</span></span>           | <span data-ttu-id="79c94-267">0x00000001</span><span class="sxs-lookup"><span data-stu-id="79c94-267">0x00000001</span></span>                                   |
| <span data-ttu-id="79c94-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="79c94-268">System-Flags</span></span>           | <span data-ttu-id="79c94-269">0x00000010</span><span class="sxs-lookup"><span data-stu-id="79c94-269">0x00000010</span></span>                                   |
| <span data-ttu-id="79c94-270">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="79c94-270">Classes used in</span></span>        | [<span data-ttu-id="79c94-271">**Classe DHCP**</span><span class="sxs-lookup"><span data-stu-id="79c94-271">**DHCP-Class**</span></span>](c-dhcpclass.md)<br/> |



 

 





