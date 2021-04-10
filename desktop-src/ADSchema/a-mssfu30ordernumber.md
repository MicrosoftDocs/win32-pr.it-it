---
title: Attributo msSFU-30-Order-Number-attributo
description: Contiene un valore utilizzato da NIS per verificare se la mappa è stata modificata.
ms.assetid: b2e83980-2de4-4001-b65a-8073c9258b27
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo attributo msSFU-30-Order-Number
- Schema AD dell'attributo msSFU30OrderNumber
topic_type:
- apiref
api_name:
- msSFU-30-Order-Number
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af67f1b5d6fdff8ca4a7739276443d67fa35679f
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104122454"
---
# <a name="mssfu-30-order-number-attribute"></a><span data-ttu-id="c4c8d-105">Attributo msSFU-30-Order-Number-attributo</span><span class="sxs-lookup"><span data-stu-id="c4c8d-105">msSFU-30-Order-Number attribute</span></span>

<span data-ttu-id="c4c8d-106">Contiene un valore utilizzato da NIS per verificare se la mappa è stata modificata.</span><span class="sxs-lookup"><span data-stu-id="c4c8d-106">Contains a value that is used by NIS to check if the map has changed.</span></span> <span data-ttu-id="c4c8d-107">Ogni volta che i dati archiviati nell'oggetto [**attributo msSFU-30-Domain-Info**](c-mssfu30domaininfo.md) cambiano, questo valore viene incrementato.</span><span class="sxs-lookup"><span data-stu-id="c4c8d-107">Every time the data stored in the [**msSFU-30-Domain-Info**](c-mssfu30domaininfo.md) object changes, this value is incremented.</span></span> <span data-ttu-id="c4c8d-108">Questo valore viene usato per tenere traccia delle modifiche dei dati tra le chiamate a **ypxfer** .</span><span class="sxs-lookup"><span data-stu-id="c4c8d-108">This value is used to track data changes between **ypxfer** calls.</span></span>



| <span data-ttu-id="c4c8d-109">Voce</span><span class="sxs-lookup"><span data-stu-id="c4c8d-109">Entry</span></span> | <span data-ttu-id="c4c8d-110">Valore</span><span class="sxs-lookup"><span data-stu-id="c4c8d-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="c4c8d-111">CN</span><span class="sxs-lookup"><span data-stu-id="c4c8d-111">CN</span></span>                | <span data-ttu-id="c4c8d-112">Attributo msSFU-30-Order-Number</span><span class="sxs-lookup"><span data-stu-id="c4c8d-112">msSFU-30-Order-Number</span></span>                       |
| <span data-ttu-id="c4c8d-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="c4c8d-113">Ldap-Display-Name</span></span> | <span data-ttu-id="c4c8d-114">msSFU30OrderNumber</span><span class="sxs-lookup"><span data-stu-id="c4c8d-114">msSFU30OrderNumber</span></span>                          |
| <span data-ttu-id="c4c8d-115">Dimensione</span><span class="sxs-lookup"><span data-stu-id="c4c8d-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="c4c8d-116">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="c4c8d-116">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="c4c8d-117">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="c4c8d-117">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="c4c8d-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c4c8d-118">Attribute-Id</span></span>      | <span data-ttu-id="c4c8d-119">1.2.840.113556.1.6.18.1.308</span><span class="sxs-lookup"><span data-stu-id="c4c8d-119">1.2.840.113556.1.6.18.1.308</span></span>                 |
| <span data-ttu-id="c4c8d-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="c4c8d-120">System-Id-Guid</span></span>    | <span data-ttu-id="c4c8d-121">02625f05-d1ee-4f9f-b366-55266becb95c</span><span class="sxs-lookup"><span data-stu-id="c4c8d-121">02625f05-d1ee-4f9f-b366-55266becb95c</span></span>        |
| <span data-ttu-id="c4c8d-122">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c4c8d-122">Syntax</span></span>            | [<span data-ttu-id="c4c8d-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="c4c8d-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="c4c8d-124">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="c4c8d-124">Implementations</span></span>

-   [<span data-ttu-id="c4c8d-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c4c8d-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c4c8d-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c4c8d-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c4c8d-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c4c8d-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c4c8d-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c4c8d-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003-r2"></a><span data-ttu-id="c4c8d-129">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c4c8d-129">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c4c8d-130">Voce</span><span class="sxs-lookup"><span data-stu-id="c4c8d-130">Entry</span></span> | <span data-ttu-id="c4c8d-131">Valore</span><span class="sxs-lookup"><span data-stu-id="c4c8d-131">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="c4c8d-132">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="c4c8d-132">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="c4c8d-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c4c8d-133">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="c4c8d-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="c4c8d-134">System-Only</span></span>            | <span data-ttu-id="c4c8d-135">Falso</span><span class="sxs-lookup"><span data-stu-id="c4c8d-135">False</span></span>                                                          |
| <span data-ttu-id="c4c8d-136">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="c4c8d-136">Is-Single-Valued</span></span>       | <span data-ttu-id="c4c8d-137">Vero</span><span class="sxs-lookup"><span data-stu-id="c4c8d-137">True</span></span>                                                           |
| <span data-ttu-id="c4c8d-138">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="c4c8d-138">Is Indexed</span></span>             | <span data-ttu-id="c4c8d-139">Vero</span><span class="sxs-lookup"><span data-stu-id="c4c8d-139">True</span></span>                                                           |
| <span data-ttu-id="c4c8d-140">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="c4c8d-140">In Global Catalog</span></span>      | <span data-ttu-id="c4c8d-141">Falso</span><span class="sxs-lookup"><span data-stu-id="c4c8d-141">False</span></span>                                                          |
| <span data-ttu-id="c4c8d-142">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="c4c8d-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="c4c8d-143">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="c4c8d-143">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="c4c8d-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c4c8d-144">Range-Lower</span></span>            | \-                                                             |
| <span data-ttu-id="c4c8d-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c4c8d-145">Range-Upper</span></span>            | \-                                                             |
| <span data-ttu-id="c4c8d-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c4c8d-146">Search-Flags</span></span>           | <span data-ttu-id="c4c8d-147">0x00000001</span><span class="sxs-lookup"><span data-stu-id="c4c8d-147">0x00000001</span></span>                                                     |
| <span data-ttu-id="c4c8d-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c4c8d-148">System-Flags</span></span>           | <span data-ttu-id="c4c8d-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c4c8d-149">0x00000000</span></span>                                                     |
| <span data-ttu-id="c4c8d-150">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="c4c8d-150">Classes used in</span></span>        | [<span data-ttu-id="c4c8d-151">**Attributo msSFU-30-Domain-Info**</span><span class="sxs-lookup"><span data-stu-id="c4c8d-151">**msSFU-30-Domain-Info**</span></span>](c-mssfu30domaininfo.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c4c8d-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c4c8d-152">Windows Server 2008</span></span>



| <span data-ttu-id="c4c8d-153">Voce</span><span class="sxs-lookup"><span data-stu-id="c4c8d-153">Entry</span></span> | <span data-ttu-id="c4c8d-154">Valore</span><span class="sxs-lookup"><span data-stu-id="c4c8d-154">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="c4c8d-155">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="c4c8d-155">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="c4c8d-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c4c8d-156">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="c4c8d-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="c4c8d-157">System-Only</span></span>            | <span data-ttu-id="c4c8d-158">Falso</span><span class="sxs-lookup"><span data-stu-id="c4c8d-158">False</span></span>                                                          |
| <span data-ttu-id="c4c8d-159">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="c4c8d-159">Is-Single-Valued</span></span>       | <span data-ttu-id="c4c8d-160">Vero</span><span class="sxs-lookup"><span data-stu-id="c4c8d-160">True</span></span>                                                           |
| <span data-ttu-id="c4c8d-161">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="c4c8d-161">Is Indexed</span></span>             | <span data-ttu-id="c4c8d-162">Vero</span><span class="sxs-lookup"><span data-stu-id="c4c8d-162">True</span></span>                                                           |
| <span data-ttu-id="c4c8d-163">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="c4c8d-163">In Global Catalog</span></span>      | <span data-ttu-id="c4c8d-164">Falso</span><span class="sxs-lookup"><span data-stu-id="c4c8d-164">False</span></span>                                                          |
| <span data-ttu-id="c4c8d-165">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="c4c8d-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="c4c8d-166">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="c4c8d-166">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="c4c8d-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c4c8d-167">Range-Lower</span></span>            | \-                                                             |
| <span data-ttu-id="c4c8d-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c4c8d-168">Range-Upper</span></span>            | \-                                                             |
| <span data-ttu-id="c4c8d-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c4c8d-169">Search-Flags</span></span>           | <span data-ttu-id="c4c8d-170">0x00000001</span><span class="sxs-lookup"><span data-stu-id="c4c8d-170">0x00000001</span></span>                                                     |
| <span data-ttu-id="c4c8d-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c4c8d-171">System-Flags</span></span>           | <span data-ttu-id="c4c8d-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c4c8d-172">0x00000000</span></span>                                                     |
| <span data-ttu-id="c4c8d-173">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="c4c8d-173">Classes used in</span></span>        | [<span data-ttu-id="c4c8d-174">**Attributo msSFU-30-Domain-Info**</span><span class="sxs-lookup"><span data-stu-id="c4c8d-174">**msSFU-30-Domain-Info**</span></span>](c-mssfu30domaininfo.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c4c8d-175">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c4c8d-175">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c4c8d-176">Voce</span><span class="sxs-lookup"><span data-stu-id="c4c8d-176">Entry</span></span> | <span data-ttu-id="c4c8d-177">Valore</span><span class="sxs-lookup"><span data-stu-id="c4c8d-177">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="c4c8d-178">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="c4c8d-178">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="c4c8d-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c4c8d-179">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="c4c8d-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="c4c8d-180">System-Only</span></span>            | <span data-ttu-id="c4c8d-181">Falso</span><span class="sxs-lookup"><span data-stu-id="c4c8d-181">False</span></span>                                                          |
| <span data-ttu-id="c4c8d-182">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="c4c8d-182">Is-Single-Valued</span></span>       | <span data-ttu-id="c4c8d-183">Vero</span><span class="sxs-lookup"><span data-stu-id="c4c8d-183">True</span></span>                                                           |
| <span data-ttu-id="c4c8d-184">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="c4c8d-184">Is Indexed</span></span>             | <span data-ttu-id="c4c8d-185">Vero</span><span class="sxs-lookup"><span data-stu-id="c4c8d-185">True</span></span>                                                           |
| <span data-ttu-id="c4c8d-186">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="c4c8d-186">In Global Catalog</span></span>      | <span data-ttu-id="c4c8d-187">Falso</span><span class="sxs-lookup"><span data-stu-id="c4c8d-187">False</span></span>                                                          |
| <span data-ttu-id="c4c8d-188">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="c4c8d-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="c4c8d-189">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="c4c8d-189">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="c4c8d-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c4c8d-190">Range-Lower</span></span>            | \-                                                             |
| <span data-ttu-id="c4c8d-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c4c8d-191">Range-Upper</span></span>            | \-                                                             |
| <span data-ttu-id="c4c8d-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c4c8d-192">Search-Flags</span></span>           | <span data-ttu-id="c4c8d-193">0x00000001</span><span class="sxs-lookup"><span data-stu-id="c4c8d-193">0x00000001</span></span>                                                     |
| <span data-ttu-id="c4c8d-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c4c8d-194">System-Flags</span></span>           | <span data-ttu-id="c4c8d-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c4c8d-195">0x00000000</span></span>                                                     |
| <span data-ttu-id="c4c8d-196">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="c4c8d-196">Classes used in</span></span>        | [<span data-ttu-id="c4c8d-197">**Attributo msSFU-30-Domain-Info**</span><span class="sxs-lookup"><span data-stu-id="c4c8d-197">**msSFU-30-Domain-Info**</span></span>](c-mssfu30domaininfo.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c4c8d-198">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c4c8d-198">Windows Server 2012</span></span>



| <span data-ttu-id="c4c8d-199">Voce</span><span class="sxs-lookup"><span data-stu-id="c4c8d-199">Entry</span></span> | <span data-ttu-id="c4c8d-200">Valore</span><span class="sxs-lookup"><span data-stu-id="c4c8d-200">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="c4c8d-201">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="c4c8d-201">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="c4c8d-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c4c8d-202">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="c4c8d-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="c4c8d-203">System-Only</span></span>            | <span data-ttu-id="c4c8d-204">Falso</span><span class="sxs-lookup"><span data-stu-id="c4c8d-204">False</span></span>                                                          |
| <span data-ttu-id="c4c8d-205">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="c4c8d-205">Is-Single-Valued</span></span>       | <span data-ttu-id="c4c8d-206">Vero</span><span class="sxs-lookup"><span data-stu-id="c4c8d-206">True</span></span>                                                           |
| <span data-ttu-id="c4c8d-207">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="c4c8d-207">Is Indexed</span></span>             | <span data-ttu-id="c4c8d-208">Vero</span><span class="sxs-lookup"><span data-stu-id="c4c8d-208">True</span></span>                                                           |
| <span data-ttu-id="c4c8d-209">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="c4c8d-209">In Global Catalog</span></span>      | <span data-ttu-id="c4c8d-210">Falso</span><span class="sxs-lookup"><span data-stu-id="c4c8d-210">False</span></span>                                                          |
| <span data-ttu-id="c4c8d-211">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="c4c8d-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="c4c8d-212">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="c4c8d-212">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="c4c8d-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c4c8d-213">Range-Lower</span></span>            | \-                                                             |
| <span data-ttu-id="c4c8d-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c4c8d-214">Range-Upper</span></span>            | \-                                                             |
| <span data-ttu-id="c4c8d-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c4c8d-215">Search-Flags</span></span>           | <span data-ttu-id="c4c8d-216">0x00000001</span><span class="sxs-lookup"><span data-stu-id="c4c8d-216">0x00000001</span></span>                                                     |
| <span data-ttu-id="c4c8d-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c4c8d-217">System-Flags</span></span>           | <span data-ttu-id="c4c8d-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c4c8d-218">0x00000000</span></span>                                                     |
| <span data-ttu-id="c4c8d-219">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="c4c8d-219">Classes used in</span></span>        | [<span data-ttu-id="c4c8d-220">**Attributo msSFU-30-Domain-Info**</span><span class="sxs-lookup"><span data-stu-id="c4c8d-220">**msSFU-30-Domain-Info**</span></span>](c-mssfu30domaininfo.md)<br/> |



 

 





