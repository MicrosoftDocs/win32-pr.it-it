---
title: attributo DHCP-servers
description: Contiene un elenco di server autorizzati nell'azienda.
ms.assetid: f712b2d2-ff9c-4ee2-aede-b68023e3e6b6
ms.tgt_platform: multiple
keywords:
- DHCP-schema di AD attributo Server
- Schema AD dell'attributo dhcpServers
topic_type:
- apiref
api_name:
- dhcp-Servers
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e43018c91e5bb495ee39476f07f40756cfcf097
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103965105"
---
# <a name="dhcp-servers-attribute"></a><span data-ttu-id="e661c-105">attributo DHCP-servers</span><span class="sxs-lookup"><span data-stu-id="e661c-105">dhcp-Servers attribute</span></span>

<span data-ttu-id="e661c-106">Contiene un elenco di server autorizzati nell'azienda.</span><span class="sxs-lookup"><span data-stu-id="e661c-106">Contains a list of servers that are authorized in the enterprise.</span></span>



| <span data-ttu-id="e661c-107">Voce</span><span class="sxs-lookup"><span data-stu-id="e661c-107">Entry</span></span> | <span data-ttu-id="e661c-108">Valore</span><span class="sxs-lookup"><span data-stu-id="e661c-108">Value</span></span> |
|-------------------|--------------------------------------------------------|
| <span data-ttu-id="e661c-109">CN</span><span class="sxs-lookup"><span data-stu-id="e661c-109">CN</span></span>                | <span data-ttu-id="e661c-110">Server DHCP</span><span class="sxs-lookup"><span data-stu-id="e661c-110">dhcp-Servers</span></span>                                           |
| <span data-ttu-id="e661c-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="e661c-111">Ldap-Display-Name</span></span> | <span data-ttu-id="e661c-112">dhcpServers</span><span class="sxs-lookup"><span data-stu-id="e661c-112">dhcpServers</span></span>                                            |
| <span data-ttu-id="e661c-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="e661c-113">Size</span></span>              | \-                                                     |
| <span data-ttu-id="e661c-114">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="e661c-114">Update Privilege</span></span>  | <span data-ttu-id="e661c-115">Amministratore di dominio.</span><span class="sxs-lookup"><span data-stu-id="e661c-115">Domain administrator.</span></span>                                  |
| <span data-ttu-id="e661c-116">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="e661c-116">Update Frequency</span></span>  | <span data-ttu-id="e661c-117">Quando un nuovo server viene aggiunto o rimosso dalla foresta.</span><span class="sxs-lookup"><span data-stu-id="e661c-117">When a new server is added or removed from the forest.</span></span> |
| <span data-ttu-id="e661c-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e661c-118">Attribute-Id</span></span>      | <span data-ttu-id="e661c-119">1.2.840.113556.1.4.704</span><span class="sxs-lookup"><span data-stu-id="e661c-119">1.2.840.113556.1.4.704</span></span>                                 |
| <span data-ttu-id="e661c-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="e661c-120">System-Id-Guid</span></span>    | <span data-ttu-id="e661c-121">963d2745-48be-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="e661c-121">963d2745-48be-11d1-a9c3-0000f80367c1</span></span>                   |
| <span data-ttu-id="e661c-122">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e661c-122">Syntax</span></span>            | [<span data-ttu-id="e661c-123">**String(IA5)**</span><span class="sxs-lookup"><span data-stu-id="e661c-123">**String(IA5)**</span></span>](s-string-ia5.md)                    |



## <a name="implementations"></a><span data-ttu-id="e661c-124">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="e661c-124">Implementations</span></span>

-   [<span data-ttu-id="e661c-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="e661c-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="e661c-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e661c-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e661c-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e661c-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e661c-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e661c-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e661c-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e661c-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e661c-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e661c-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="e661c-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e661c-131">Windows 2000 Server</span></span>



| <span data-ttu-id="e661c-132">Voce</span><span class="sxs-lookup"><span data-stu-id="e661c-132">Entry</span></span> | <span data-ttu-id="e661c-133">Valore</span><span class="sxs-lookup"><span data-stu-id="e661c-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="e661c-134">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="e661c-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="e661c-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e661c-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="e661c-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="e661c-136">System-Only</span></span>            | <span data-ttu-id="e661c-137">Falso</span><span class="sxs-lookup"><span data-stu-id="e661c-137">False</span></span>                                        |
| <span data-ttu-id="e661c-138">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="e661c-138">Is-Single-Valued</span></span>       | <span data-ttu-id="e661c-139">Falso</span><span class="sxs-lookup"><span data-stu-id="e661c-139">False</span></span>                                        |
| <span data-ttu-id="e661c-140">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="e661c-140">Is Indexed</span></span>             | <span data-ttu-id="e661c-141">Falso</span><span class="sxs-lookup"><span data-stu-id="e661c-141">False</span></span>                                        |
| <span data-ttu-id="e661c-142">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="e661c-142">In Global Catalog</span></span>      | <span data-ttu-id="e661c-143">Falso</span><span class="sxs-lookup"><span data-stu-id="e661c-143">False</span></span>                                        |
| <span data-ttu-id="e661c-144">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="e661c-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="e661c-145">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="e661c-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="e661c-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e661c-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="e661c-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e661c-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="e661c-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e661c-148">Search-Flags</span></span>           | <span data-ttu-id="e661c-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e661c-149">0x00000000</span></span>                                   |
| <span data-ttu-id="e661c-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e661c-150">System-Flags</span></span>           | <span data-ttu-id="e661c-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e661c-151">0x00000010</span></span>                                   |
| <span data-ttu-id="e661c-152">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="e661c-152">Classes used in</span></span>        | [<span data-ttu-id="e661c-153">**Classe DHCP**</span><span class="sxs-lookup"><span data-stu-id="e661c-153">**DHCP-Class**</span></span>](c-dhcpclass.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="e661c-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e661c-154">Windows Server 2003</span></span>



| <span data-ttu-id="e661c-155">Voce</span><span class="sxs-lookup"><span data-stu-id="e661c-155">Entry</span></span> | <span data-ttu-id="e661c-156">Valore</span><span class="sxs-lookup"><span data-stu-id="e661c-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="e661c-157">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="e661c-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="e661c-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e661c-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="e661c-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="e661c-159">System-Only</span></span>            | <span data-ttu-id="e661c-160">Falso</span><span class="sxs-lookup"><span data-stu-id="e661c-160">False</span></span>                                        |
| <span data-ttu-id="e661c-161">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="e661c-161">Is-Single-Valued</span></span>       | <span data-ttu-id="e661c-162">Falso</span><span class="sxs-lookup"><span data-stu-id="e661c-162">False</span></span>                                        |
| <span data-ttu-id="e661c-163">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="e661c-163">Is Indexed</span></span>             | <span data-ttu-id="e661c-164">Falso</span><span class="sxs-lookup"><span data-stu-id="e661c-164">False</span></span>                                        |
| <span data-ttu-id="e661c-165">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="e661c-165">In Global Catalog</span></span>      | <span data-ttu-id="e661c-166">Falso</span><span class="sxs-lookup"><span data-stu-id="e661c-166">False</span></span>                                        |
| <span data-ttu-id="e661c-167">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="e661c-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="e661c-168">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="e661c-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="e661c-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e661c-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="e661c-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e661c-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="e661c-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e661c-171">Search-Flags</span></span>           | <span data-ttu-id="e661c-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e661c-172">0x00000000</span></span>                                   |
| <span data-ttu-id="e661c-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e661c-173">System-Flags</span></span>           | <span data-ttu-id="e661c-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e661c-174">0x00000010</span></span>                                   |
| <span data-ttu-id="e661c-175">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="e661c-175">Classes used in</span></span>        | [<span data-ttu-id="e661c-176">**Classe DHCP**</span><span class="sxs-lookup"><span data-stu-id="e661c-176">**DHCP-Class**</span></span>](c-dhcpclass.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e661c-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e661c-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e661c-178">Voce</span><span class="sxs-lookup"><span data-stu-id="e661c-178">Entry</span></span> | <span data-ttu-id="e661c-179">Valore</span><span class="sxs-lookup"><span data-stu-id="e661c-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="e661c-180">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="e661c-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="e661c-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e661c-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="e661c-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="e661c-182">System-Only</span></span>            | <span data-ttu-id="e661c-183">Falso</span><span class="sxs-lookup"><span data-stu-id="e661c-183">False</span></span>                                        |
| <span data-ttu-id="e661c-184">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="e661c-184">Is-Single-Valued</span></span>       | <span data-ttu-id="e661c-185">Falso</span><span class="sxs-lookup"><span data-stu-id="e661c-185">False</span></span>                                        |
| <span data-ttu-id="e661c-186">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="e661c-186">Is Indexed</span></span>             | <span data-ttu-id="e661c-187">Falso</span><span class="sxs-lookup"><span data-stu-id="e661c-187">False</span></span>                                        |
| <span data-ttu-id="e661c-188">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="e661c-188">In Global Catalog</span></span>      | <span data-ttu-id="e661c-189">Falso</span><span class="sxs-lookup"><span data-stu-id="e661c-189">False</span></span>                                        |
| <span data-ttu-id="e661c-190">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="e661c-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="e661c-191">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="e661c-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="e661c-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e661c-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="e661c-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e661c-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="e661c-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e661c-194">Search-Flags</span></span>           | <span data-ttu-id="e661c-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e661c-195">0x00000000</span></span>                                   |
| <span data-ttu-id="e661c-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e661c-196">System-Flags</span></span>           | <span data-ttu-id="e661c-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e661c-197">0x00000010</span></span>                                   |
| <span data-ttu-id="e661c-198">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="e661c-198">Classes used in</span></span>        | [<span data-ttu-id="e661c-199">**Classe DHCP**</span><span class="sxs-lookup"><span data-stu-id="e661c-199">**DHCP-Class**</span></span>](c-dhcpclass.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="e661c-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e661c-200">Windows Server 2008</span></span>



| <span data-ttu-id="e661c-201">Voce</span><span class="sxs-lookup"><span data-stu-id="e661c-201">Entry</span></span> | <span data-ttu-id="e661c-202">Valore</span><span class="sxs-lookup"><span data-stu-id="e661c-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="e661c-203">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="e661c-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="e661c-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e661c-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="e661c-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="e661c-205">System-Only</span></span>            | <span data-ttu-id="e661c-206">Falso</span><span class="sxs-lookup"><span data-stu-id="e661c-206">False</span></span>                                        |
| <span data-ttu-id="e661c-207">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="e661c-207">Is-Single-Valued</span></span>       | <span data-ttu-id="e661c-208">Falso</span><span class="sxs-lookup"><span data-stu-id="e661c-208">False</span></span>                                        |
| <span data-ttu-id="e661c-209">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="e661c-209">Is Indexed</span></span>             | <span data-ttu-id="e661c-210">Falso</span><span class="sxs-lookup"><span data-stu-id="e661c-210">False</span></span>                                        |
| <span data-ttu-id="e661c-211">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="e661c-211">In Global Catalog</span></span>      | <span data-ttu-id="e661c-212">Falso</span><span class="sxs-lookup"><span data-stu-id="e661c-212">False</span></span>                                        |
| <span data-ttu-id="e661c-213">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="e661c-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="e661c-214">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="e661c-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="e661c-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e661c-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="e661c-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e661c-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="e661c-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e661c-217">Search-Flags</span></span>           | <span data-ttu-id="e661c-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e661c-218">0x00000000</span></span>                                   |
| <span data-ttu-id="e661c-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e661c-219">System-Flags</span></span>           | <span data-ttu-id="e661c-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e661c-220">0x00000010</span></span>                                   |
| <span data-ttu-id="e661c-221">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="e661c-221">Classes used in</span></span>        | [<span data-ttu-id="e661c-222">**Classe DHCP**</span><span class="sxs-lookup"><span data-stu-id="e661c-222">**DHCP-Class**</span></span>](c-dhcpclass.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e661c-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e661c-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e661c-224">Voce</span><span class="sxs-lookup"><span data-stu-id="e661c-224">Entry</span></span> | <span data-ttu-id="e661c-225">Valore</span><span class="sxs-lookup"><span data-stu-id="e661c-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="e661c-226">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="e661c-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="e661c-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e661c-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="e661c-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="e661c-228">System-Only</span></span>            | <span data-ttu-id="e661c-229">Falso</span><span class="sxs-lookup"><span data-stu-id="e661c-229">False</span></span>                                        |
| <span data-ttu-id="e661c-230">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="e661c-230">Is-Single-Valued</span></span>       | <span data-ttu-id="e661c-231">Falso</span><span class="sxs-lookup"><span data-stu-id="e661c-231">False</span></span>                                        |
| <span data-ttu-id="e661c-232">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="e661c-232">Is Indexed</span></span>             | <span data-ttu-id="e661c-233">Falso</span><span class="sxs-lookup"><span data-stu-id="e661c-233">False</span></span>                                        |
| <span data-ttu-id="e661c-234">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="e661c-234">In Global Catalog</span></span>      | <span data-ttu-id="e661c-235">Falso</span><span class="sxs-lookup"><span data-stu-id="e661c-235">False</span></span>                                        |
| <span data-ttu-id="e661c-236">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="e661c-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="e661c-237">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="e661c-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="e661c-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e661c-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="e661c-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e661c-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="e661c-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e661c-240">Search-Flags</span></span>           | <span data-ttu-id="e661c-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e661c-241">0x00000000</span></span>                                   |
| <span data-ttu-id="e661c-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e661c-242">System-Flags</span></span>           | <span data-ttu-id="e661c-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e661c-243">0x00000010</span></span>                                   |
| <span data-ttu-id="e661c-244">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="e661c-244">Classes used in</span></span>        | [<span data-ttu-id="e661c-245">**Classe DHCP**</span><span class="sxs-lookup"><span data-stu-id="e661c-245">**DHCP-Class**</span></span>](c-dhcpclass.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e661c-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e661c-246">Windows Server 2012</span></span>



| <span data-ttu-id="e661c-247">Voce</span><span class="sxs-lookup"><span data-stu-id="e661c-247">Entry</span></span> | <span data-ttu-id="e661c-248">Valore</span><span class="sxs-lookup"><span data-stu-id="e661c-248">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="e661c-249">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="e661c-249">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="e661c-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e661c-250">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="e661c-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="e661c-251">System-Only</span></span>            | <span data-ttu-id="e661c-252">Falso</span><span class="sxs-lookup"><span data-stu-id="e661c-252">False</span></span>                                        |
| <span data-ttu-id="e661c-253">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="e661c-253">Is-Single-Valued</span></span>       | <span data-ttu-id="e661c-254">Falso</span><span class="sxs-lookup"><span data-stu-id="e661c-254">False</span></span>                                        |
| <span data-ttu-id="e661c-255">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="e661c-255">Is Indexed</span></span>             | <span data-ttu-id="e661c-256">Falso</span><span class="sxs-lookup"><span data-stu-id="e661c-256">False</span></span>                                        |
| <span data-ttu-id="e661c-257">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="e661c-257">In Global Catalog</span></span>      | <span data-ttu-id="e661c-258">Falso</span><span class="sxs-lookup"><span data-stu-id="e661c-258">False</span></span>                                        |
| <span data-ttu-id="e661c-259">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="e661c-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="e661c-260">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="e661c-260">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="e661c-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e661c-261">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="e661c-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e661c-262">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="e661c-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e661c-263">Search-Flags</span></span>           | <span data-ttu-id="e661c-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e661c-264">0x00000000</span></span>                                   |
| <span data-ttu-id="e661c-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e661c-265">System-Flags</span></span>           | <span data-ttu-id="e661c-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e661c-266">0x00000010</span></span>                                   |
| <span data-ttu-id="e661c-267">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="e661c-267">Classes used in</span></span>        | [<span data-ttu-id="e661c-268">**Classe DHCP**</span><span class="sxs-lookup"><span data-stu-id="e661c-268">**DHCP-Class**</span></span>](c-dhcpclass.md)<br/> |



 

 





