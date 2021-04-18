---
title: Proxy-oggetto-nome attributo
description: Questo attributo viene utilizzato internamente da Active Directory per tenere traccia degli spostamenti tra domini.
ms.assetid: 661ea322-f78c-44dc-8d64-4f28ead1a7aa
ms.tgt_platform: multiple
keywords:
- Oggetto proxy-Object-Name attributo AD schema
- Schema AD dell'attributo proxiedObjectName
topic_type:
- apiref
api_name:
- Proxied-Object-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ffafbbea411c950954102a788226c29589029e1
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "106302859"
---
# <a name="proxied-object-name-attribute"></a><span data-ttu-id="6dcd6-105">Proxy-oggetto-nome attributo</span><span class="sxs-lookup"><span data-stu-id="6dcd6-105">Proxied-Object-Name attribute</span></span>

<span data-ttu-id="6dcd6-106">Questo attributo viene utilizzato internamente da Active Directory per tenere traccia degli spostamenti tra domini.</span><span class="sxs-lookup"><span data-stu-id="6dcd6-106">This attribute is used internally by Active Directory to help track interdomain moves.</span></span>



| <span data-ttu-id="6dcd6-107">Voce</span><span class="sxs-lookup"><span data-stu-id="6dcd6-107">Entry</span></span> | <span data-ttu-id="6dcd6-108">Valore</span><span class="sxs-lookup"><span data-stu-id="6dcd6-108">Value</span></span> |
|-------------------|-------------------------------------------------|
| <span data-ttu-id="6dcd6-109">CN</span><span class="sxs-lookup"><span data-stu-id="6dcd6-109">CN</span></span>                | <span data-ttu-id="6dcd6-110">Nome-oggetto-proxy</span><span class="sxs-lookup"><span data-stu-id="6dcd6-110">Proxied-Object-Name</span></span>                             |
| <span data-ttu-id="6dcd6-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="6dcd6-111">Ldap-Display-Name</span></span> | <span data-ttu-id="6dcd6-112">proxiedObjectName</span><span class="sxs-lookup"><span data-stu-id="6dcd6-112">proxiedObjectName</span></span>                               |
| <span data-ttu-id="6dcd6-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="6dcd6-113">Size</span></span>              | \-                                              |
| <span data-ttu-id="6dcd6-114">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="6dcd6-114">Update Privilege</span></span>  | <span data-ttu-id="6dcd6-115">Viene utilizzato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="6dcd6-115">This is used by the system.</span></span>                     |
| <span data-ttu-id="6dcd6-116">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="6dcd6-116">Update Frequency</span></span>  | \-                                              |
| <span data-ttu-id="6dcd6-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="6dcd6-117">Attribute-Id</span></span>      | <span data-ttu-id="6dcd6-118">1.2.840.113556.1.4.1249</span><span class="sxs-lookup"><span data-stu-id="6dcd6-118">1.2.840.113556.1.4.1249</span></span>                         |
| <span data-ttu-id="6dcd6-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="6dcd6-119">System-Id-Guid</span></span>    | <span data-ttu-id="6dcd6-120">e1aea402-cd5b-11d0-afff-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="6dcd6-120">e1aea402-cd5b-11d0-afff-0000f80367c1</span></span>            |
| <span data-ttu-id="6dcd6-121">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6dcd6-121">Syntax</span></span>            | [<span data-ttu-id="6dcd6-122">**Object(DN-Binary)**</span><span class="sxs-lookup"><span data-stu-id="6dcd6-122">**Object(DN-Binary)**</span></span>](s-object-dn-binary.md) |



## <a name="implementations"></a><span data-ttu-id="6dcd6-123">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="6dcd6-123">Implementations</span></span>

-   [<span data-ttu-id="6dcd6-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="6dcd6-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="6dcd6-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="6dcd6-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="6dcd6-126">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="6dcd6-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="6dcd6-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="6dcd6-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="6dcd6-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="6dcd6-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="6dcd6-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="6dcd6-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="6dcd6-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="6dcd6-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="6dcd6-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6dcd6-131">Windows 2000 Server</span></span>



| <span data-ttu-id="6dcd6-132">Voce</span><span class="sxs-lookup"><span data-stu-id="6dcd6-132">Entry</span></span> | <span data-ttu-id="6dcd6-133">Valore</span><span class="sxs-lookup"><span data-stu-id="6dcd6-133">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="6dcd6-134">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="6dcd6-134">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="6dcd6-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6dcd6-135">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="6dcd6-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="6dcd6-136">System-Only</span></span>            | <span data-ttu-id="6dcd6-137">Vero</span><span class="sxs-lookup"><span data-stu-id="6dcd6-137">True</span></span>                            |
| <span data-ttu-id="6dcd6-138">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="6dcd6-138">Is-Single-Valued</span></span>       | <span data-ttu-id="6dcd6-139">Vero</span><span class="sxs-lookup"><span data-stu-id="6dcd6-139">True</span></span>                            |
| <span data-ttu-id="6dcd6-140">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="6dcd6-140">Is Indexed</span></span>             | <span data-ttu-id="6dcd6-141">Falso</span><span class="sxs-lookup"><span data-stu-id="6dcd6-141">False</span></span>                           |
| <span data-ttu-id="6dcd6-142">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="6dcd6-142">In Global Catalog</span></span>      | <span data-ttu-id="6dcd6-143">Vero</span><span class="sxs-lookup"><span data-stu-id="6dcd6-143">True</span></span>                            |
| <span data-ttu-id="6dcd6-144">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="6dcd6-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="6dcd6-145">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="6dcd6-145">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="6dcd6-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6dcd6-146">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="6dcd6-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6dcd6-147">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="6dcd6-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6dcd6-148">Search-Flags</span></span>           | <span data-ttu-id="6dcd6-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6dcd6-149">0x00000000</span></span>                      |
| <span data-ttu-id="6dcd6-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6dcd6-150">System-Flags</span></span>           | <span data-ttu-id="6dcd6-151">0x00000012</span><span class="sxs-lookup"><span data-stu-id="6dcd6-151">0x00000012</span></span>                      |
| <span data-ttu-id="6dcd6-152">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="6dcd6-152">Classes used in</span></span>        | [<span data-ttu-id="6dcd6-153">**In alto**</span><span class="sxs-lookup"><span data-stu-id="6dcd6-153">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="6dcd6-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6dcd6-154">Windows Server 2003</span></span>



| <span data-ttu-id="6dcd6-155">Voce</span><span class="sxs-lookup"><span data-stu-id="6dcd6-155">Entry</span></span> | <span data-ttu-id="6dcd6-156">Valore</span><span class="sxs-lookup"><span data-stu-id="6dcd6-156">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="6dcd6-157">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="6dcd6-157">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="6dcd6-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6dcd6-158">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="6dcd6-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="6dcd6-159">System-Only</span></span>            | <span data-ttu-id="6dcd6-160">Vero</span><span class="sxs-lookup"><span data-stu-id="6dcd6-160">True</span></span>                            |
| <span data-ttu-id="6dcd6-161">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="6dcd6-161">Is-Single-Valued</span></span>       | <span data-ttu-id="6dcd6-162">Vero</span><span class="sxs-lookup"><span data-stu-id="6dcd6-162">True</span></span>                            |
| <span data-ttu-id="6dcd6-163">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="6dcd6-163">Is Indexed</span></span>             | <span data-ttu-id="6dcd6-164">Falso</span><span class="sxs-lookup"><span data-stu-id="6dcd6-164">False</span></span>                           |
| <span data-ttu-id="6dcd6-165">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="6dcd6-165">In Global Catalog</span></span>      | <span data-ttu-id="6dcd6-166">Vero</span><span class="sxs-lookup"><span data-stu-id="6dcd6-166">True</span></span>                            |
| <span data-ttu-id="6dcd6-167">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="6dcd6-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="6dcd6-168">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="6dcd6-168">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="6dcd6-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6dcd6-169">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="6dcd6-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6dcd6-170">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="6dcd6-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6dcd6-171">Search-Flags</span></span>           | <span data-ttu-id="6dcd6-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6dcd6-172">0x00000000</span></span>                      |
| <span data-ttu-id="6dcd6-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6dcd6-173">System-Flags</span></span>           | <span data-ttu-id="6dcd6-174">0x00000012</span><span class="sxs-lookup"><span data-stu-id="6dcd6-174">0x00000012</span></span>                      |
| <span data-ttu-id="6dcd6-175">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="6dcd6-175">Classes used in</span></span>        | [<span data-ttu-id="6dcd6-176">**In alto**</span><span class="sxs-lookup"><span data-stu-id="6dcd6-176">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="6dcd6-177">ADAM</span><span class="sxs-lookup"><span data-stu-id="6dcd6-177">ADAM</span></span>



| <span data-ttu-id="6dcd6-178">Voce</span><span class="sxs-lookup"><span data-stu-id="6dcd6-178">Entry</span></span> | <span data-ttu-id="6dcd6-179">Valore</span><span class="sxs-lookup"><span data-stu-id="6dcd6-179">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="6dcd6-180">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="6dcd6-180">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="6dcd6-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6dcd6-181">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="6dcd6-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="6dcd6-182">System-Only</span></span>            | <span data-ttu-id="6dcd6-183">Vero</span><span class="sxs-lookup"><span data-stu-id="6dcd6-183">True</span></span>                            |
| <span data-ttu-id="6dcd6-184">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="6dcd6-184">Is-Single-Valued</span></span>       | <span data-ttu-id="6dcd6-185">Vero</span><span class="sxs-lookup"><span data-stu-id="6dcd6-185">True</span></span>                            |
| <span data-ttu-id="6dcd6-186">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="6dcd6-186">Is Indexed</span></span>             | <span data-ttu-id="6dcd6-187">Falso</span><span class="sxs-lookup"><span data-stu-id="6dcd6-187">False</span></span>                           |
| <span data-ttu-id="6dcd6-188">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="6dcd6-188">In Global Catalog</span></span>      | <span data-ttu-id="6dcd6-189">Vero</span><span class="sxs-lookup"><span data-stu-id="6dcd6-189">True</span></span>                            |
| <span data-ttu-id="6dcd6-190">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="6dcd6-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="6dcd6-191">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="6dcd6-191">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="6dcd6-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6dcd6-192">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="6dcd6-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6dcd6-193">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="6dcd6-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6dcd6-194">Search-Flags</span></span>           | <span data-ttu-id="6dcd6-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6dcd6-195">0x00000000</span></span>                      |
| <span data-ttu-id="6dcd6-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6dcd6-196">System-Flags</span></span>           | <span data-ttu-id="6dcd6-197">0x00000012</span><span class="sxs-lookup"><span data-stu-id="6dcd6-197">0x00000012</span></span>                      |
| <span data-ttu-id="6dcd6-198">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="6dcd6-198">Classes used in</span></span>        | [<span data-ttu-id="6dcd6-199">**In alto**</span><span class="sxs-lookup"><span data-stu-id="6dcd6-199">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="6dcd6-200">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="6dcd6-200">Windows Server 2003 R2</span></span>



| <span data-ttu-id="6dcd6-201">Voce</span><span class="sxs-lookup"><span data-stu-id="6dcd6-201">Entry</span></span> | <span data-ttu-id="6dcd6-202">Valore</span><span class="sxs-lookup"><span data-stu-id="6dcd6-202">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="6dcd6-203">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="6dcd6-203">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="6dcd6-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6dcd6-204">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="6dcd6-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="6dcd6-205">System-Only</span></span>            | <span data-ttu-id="6dcd6-206">Vero</span><span class="sxs-lookup"><span data-stu-id="6dcd6-206">True</span></span>                            |
| <span data-ttu-id="6dcd6-207">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="6dcd6-207">Is-Single-Valued</span></span>       | <span data-ttu-id="6dcd6-208">Vero</span><span class="sxs-lookup"><span data-stu-id="6dcd6-208">True</span></span>                            |
| <span data-ttu-id="6dcd6-209">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="6dcd6-209">Is Indexed</span></span>             | <span data-ttu-id="6dcd6-210">Falso</span><span class="sxs-lookup"><span data-stu-id="6dcd6-210">False</span></span>                           |
| <span data-ttu-id="6dcd6-211">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="6dcd6-211">In Global Catalog</span></span>      | <span data-ttu-id="6dcd6-212">Vero</span><span class="sxs-lookup"><span data-stu-id="6dcd6-212">True</span></span>                            |
| <span data-ttu-id="6dcd6-213">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="6dcd6-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="6dcd6-214">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="6dcd6-214">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="6dcd6-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6dcd6-215">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="6dcd6-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6dcd6-216">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="6dcd6-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6dcd6-217">Search-Flags</span></span>           | <span data-ttu-id="6dcd6-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6dcd6-218">0x00000000</span></span>                      |
| <span data-ttu-id="6dcd6-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6dcd6-219">System-Flags</span></span>           | <span data-ttu-id="6dcd6-220">0x00000012</span><span class="sxs-lookup"><span data-stu-id="6dcd6-220">0x00000012</span></span>                      |
| <span data-ttu-id="6dcd6-221">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="6dcd6-221">Classes used in</span></span>        | [<span data-ttu-id="6dcd6-222">**In alto**</span><span class="sxs-lookup"><span data-stu-id="6dcd6-222">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="6dcd6-223">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6dcd6-223">Windows Server 2008</span></span>



| <span data-ttu-id="6dcd6-224">Voce</span><span class="sxs-lookup"><span data-stu-id="6dcd6-224">Entry</span></span> | <span data-ttu-id="6dcd6-225">Valore</span><span class="sxs-lookup"><span data-stu-id="6dcd6-225">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="6dcd6-226">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="6dcd6-226">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="6dcd6-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6dcd6-227">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="6dcd6-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="6dcd6-228">System-Only</span></span>            | <span data-ttu-id="6dcd6-229">Vero</span><span class="sxs-lookup"><span data-stu-id="6dcd6-229">True</span></span>                            |
| <span data-ttu-id="6dcd6-230">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="6dcd6-230">Is-Single-Valued</span></span>       | <span data-ttu-id="6dcd6-231">Vero</span><span class="sxs-lookup"><span data-stu-id="6dcd6-231">True</span></span>                            |
| <span data-ttu-id="6dcd6-232">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="6dcd6-232">Is Indexed</span></span>             | <span data-ttu-id="6dcd6-233">Falso</span><span class="sxs-lookup"><span data-stu-id="6dcd6-233">False</span></span>                           |
| <span data-ttu-id="6dcd6-234">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="6dcd6-234">In Global Catalog</span></span>      | <span data-ttu-id="6dcd6-235">Vero</span><span class="sxs-lookup"><span data-stu-id="6dcd6-235">True</span></span>                            |
| <span data-ttu-id="6dcd6-236">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="6dcd6-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="6dcd6-237">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="6dcd6-237">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="6dcd6-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6dcd6-238">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="6dcd6-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6dcd6-239">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="6dcd6-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6dcd6-240">Search-Flags</span></span>           | <span data-ttu-id="6dcd6-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6dcd6-241">0x00000000</span></span>                      |
| <span data-ttu-id="6dcd6-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6dcd6-242">System-Flags</span></span>           | <span data-ttu-id="6dcd6-243">0x00000012</span><span class="sxs-lookup"><span data-stu-id="6dcd6-243">0x00000012</span></span>                      |
| <span data-ttu-id="6dcd6-244">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="6dcd6-244">Classes used in</span></span>        | [<span data-ttu-id="6dcd6-245">**In alto**</span><span class="sxs-lookup"><span data-stu-id="6dcd6-245">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="6dcd6-246">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6dcd6-246">Windows Server 2008 R2</span></span>



| <span data-ttu-id="6dcd6-247">Voce</span><span class="sxs-lookup"><span data-stu-id="6dcd6-247">Entry</span></span> | <span data-ttu-id="6dcd6-248">Valore</span><span class="sxs-lookup"><span data-stu-id="6dcd6-248">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="6dcd6-249">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="6dcd6-249">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="6dcd6-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6dcd6-250">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="6dcd6-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="6dcd6-251">System-Only</span></span>            | <span data-ttu-id="6dcd6-252">Vero</span><span class="sxs-lookup"><span data-stu-id="6dcd6-252">True</span></span>                            |
| <span data-ttu-id="6dcd6-253">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="6dcd6-253">Is-Single-Valued</span></span>       | <span data-ttu-id="6dcd6-254">Vero</span><span class="sxs-lookup"><span data-stu-id="6dcd6-254">True</span></span>                            |
| <span data-ttu-id="6dcd6-255">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="6dcd6-255">Is Indexed</span></span>             | <span data-ttu-id="6dcd6-256">Falso</span><span class="sxs-lookup"><span data-stu-id="6dcd6-256">False</span></span>                           |
| <span data-ttu-id="6dcd6-257">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="6dcd6-257">In Global Catalog</span></span>      | <span data-ttu-id="6dcd6-258">Vero</span><span class="sxs-lookup"><span data-stu-id="6dcd6-258">True</span></span>                            |
| <span data-ttu-id="6dcd6-259">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="6dcd6-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="6dcd6-260">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="6dcd6-260">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="6dcd6-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6dcd6-261">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="6dcd6-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6dcd6-262">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="6dcd6-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6dcd6-263">Search-Flags</span></span>           | <span data-ttu-id="6dcd6-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6dcd6-264">0x00000000</span></span>                      |
| <span data-ttu-id="6dcd6-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6dcd6-265">System-Flags</span></span>           | <span data-ttu-id="6dcd6-266">0x00000012</span><span class="sxs-lookup"><span data-stu-id="6dcd6-266">0x00000012</span></span>                      |
| <span data-ttu-id="6dcd6-267">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="6dcd6-267">Classes used in</span></span>        | [<span data-ttu-id="6dcd6-268">**In alto**</span><span class="sxs-lookup"><span data-stu-id="6dcd6-268">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="6dcd6-269">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6dcd6-269">Windows Server 2012</span></span>



| <span data-ttu-id="6dcd6-270">Voce</span><span class="sxs-lookup"><span data-stu-id="6dcd6-270">Entry</span></span> | <span data-ttu-id="6dcd6-271">Valore</span><span class="sxs-lookup"><span data-stu-id="6dcd6-271">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="6dcd6-272">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="6dcd6-272">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="6dcd6-273">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6dcd6-273">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="6dcd6-274">System-Only</span><span class="sxs-lookup"><span data-stu-id="6dcd6-274">System-Only</span></span>            | <span data-ttu-id="6dcd6-275">Vero</span><span class="sxs-lookup"><span data-stu-id="6dcd6-275">True</span></span>                            |
| <span data-ttu-id="6dcd6-276">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="6dcd6-276">Is-Single-Valued</span></span>       | <span data-ttu-id="6dcd6-277">Vero</span><span class="sxs-lookup"><span data-stu-id="6dcd6-277">True</span></span>                            |
| <span data-ttu-id="6dcd6-278">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="6dcd6-278">Is Indexed</span></span>             | <span data-ttu-id="6dcd6-279">Falso</span><span class="sxs-lookup"><span data-stu-id="6dcd6-279">False</span></span>                           |
| <span data-ttu-id="6dcd6-280">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="6dcd6-280">In Global Catalog</span></span>      | <span data-ttu-id="6dcd6-281">Vero</span><span class="sxs-lookup"><span data-stu-id="6dcd6-281">True</span></span>                            |
| <span data-ttu-id="6dcd6-282">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="6dcd6-282">NT-Security-Descriptor</span></span> | <span data-ttu-id="6dcd6-283">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="6dcd6-283">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="6dcd6-284">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6dcd6-284">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="6dcd6-285">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6dcd6-285">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="6dcd6-286">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6dcd6-286">Search-Flags</span></span>           | <span data-ttu-id="6dcd6-287">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6dcd6-287">0x00000000</span></span>                      |
| <span data-ttu-id="6dcd6-288">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6dcd6-288">System-Flags</span></span>           | <span data-ttu-id="6dcd6-289">0x00000012</span><span class="sxs-lookup"><span data-stu-id="6dcd6-289">0x00000012</span></span>                      |
| <span data-ttu-id="6dcd6-290">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="6dcd6-290">Classes used in</span></span>        | [<span data-ttu-id="6dcd6-291">**In alto**</span><span class="sxs-lookup"><span data-stu-id="6dcd6-291">**Top**</span></span>](c-top.md)<br/> |



 

 





