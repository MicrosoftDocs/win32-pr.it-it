---
title: Attributo DN-Reference-Update
description: Se un oggetto viene rinominato, questo attributo viene utilizzato per tenere traccia di tutti i nomi precedenti e correnti assegnati a un oggetto in modo che gli oggetti collegati possano ancora trovarlo.
ms.assetid: 28e02a38-eed8-475c-a381-145857477ec6
ms.tgt_platform: multiple
keywords:
- DN-Reference-Aggiorna schema AD dell'attributo
- Schema AD dell'attributo dNReferenceUpdate
topic_type:
- apiref
api_name:
- DN-Reference-Update
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a71e8360be6e7ed6697363daa0f6ff32e2ec5fb9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "106303574"
---
# <a name="dn-reference-update-attribute"></a><span data-ttu-id="6f2ea-105">Attributo DN-Reference-Update</span><span class="sxs-lookup"><span data-stu-id="6f2ea-105">DN-Reference-Update attribute</span></span>

<span data-ttu-id="6f2ea-106">Se un oggetto viene rinominato, questo attributo viene utilizzato per tenere traccia di tutti i nomi precedenti e correnti assegnati a un oggetto in modo che gli oggetti collegati possano ancora trovarlo.</span><span class="sxs-lookup"><span data-stu-id="6f2ea-106">If an object is renamed, this attribute is used to track all of the previous and current names that have been assigned to an object so that linked objects can still find it.</span></span>



| <span data-ttu-id="6f2ea-107">Voce</span><span class="sxs-lookup"><span data-stu-id="6f2ea-107">Entry</span></span> | <span data-ttu-id="6f2ea-108">Valore</span><span class="sxs-lookup"><span data-stu-id="6f2ea-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="6f2ea-109">CN</span><span class="sxs-lookup"><span data-stu-id="6f2ea-109">CN</span></span>                | <span data-ttu-id="6f2ea-110">DN-riferimento-aggiornamento</span><span class="sxs-lookup"><span data-stu-id="6f2ea-110">DN-Reference-Update</span></span>                     |
| <span data-ttu-id="6f2ea-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="6f2ea-111">Ldap-Display-Name</span></span> | <span data-ttu-id="6f2ea-112">dNReferenceUpdate</span><span class="sxs-lookup"><span data-stu-id="6f2ea-112">dNReferenceUpdate</span></span>                       |
| <span data-ttu-id="6f2ea-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="6f2ea-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="6f2ea-114">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="6f2ea-114">Update Privilege</span></span>  | <span data-ttu-id="6f2ea-115">Questa impostazione viene impostata dal sistema.</span><span class="sxs-lookup"><span data-stu-id="6f2ea-115">This is set by the system.</span></span>              |
| <span data-ttu-id="6f2ea-116">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="6f2ea-116">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="6f2ea-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="6f2ea-117">Attribute-Id</span></span>      | <span data-ttu-id="6f2ea-118">1.2.840.113556.1.4.1242</span><span class="sxs-lookup"><span data-stu-id="6f2ea-118">1.2.840.113556.1.4.1242</span></span>                 |
| <span data-ttu-id="6f2ea-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="6f2ea-119">System-Id-Guid</span></span>    | <span data-ttu-id="6f2ea-120">2df90d86-009f-11d2-aa4c-00c04fd7d83a</span><span class="sxs-lookup"><span data-stu-id="6f2ea-120">2df90d86-009f-11d2-aa4c-00c04fd7d83a</span></span>    |
| <span data-ttu-id="6f2ea-121">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6f2ea-121">Syntax</span></span>            | [<span data-ttu-id="6f2ea-122">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="6f2ea-122">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="6f2ea-123">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="6f2ea-123">Implementations</span></span>

-   [<span data-ttu-id="6f2ea-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="6f2ea-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="6f2ea-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="6f2ea-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="6f2ea-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="6f2ea-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="6f2ea-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="6f2ea-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="6f2ea-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="6f2ea-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="6f2ea-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="6f2ea-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="6f2ea-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6f2ea-130">Windows 2000 Server</span></span>



| <span data-ttu-id="6f2ea-131">Voce</span><span class="sxs-lookup"><span data-stu-id="6f2ea-131">Entry</span></span> | <span data-ttu-id="6f2ea-132">Valore</span><span class="sxs-lookup"><span data-stu-id="6f2ea-132">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="6f2ea-133">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="6f2ea-133">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="6f2ea-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6f2ea-134">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="6f2ea-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="6f2ea-135">System-Only</span></span>            | <span data-ttu-id="6f2ea-136">Vero</span><span class="sxs-lookup"><span data-stu-id="6f2ea-136">True</span></span>                                                               |
| <span data-ttu-id="6f2ea-137">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="6f2ea-137">Is-Single-Valued</span></span>       | <span data-ttu-id="6f2ea-138">Falso</span><span class="sxs-lookup"><span data-stu-id="6f2ea-138">False</span></span>                                                              |
| <span data-ttu-id="6f2ea-139">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="6f2ea-139">Is Indexed</span></span>             | <span data-ttu-id="6f2ea-140">Falso</span><span class="sxs-lookup"><span data-stu-id="6f2ea-140">False</span></span>                                                              |
| <span data-ttu-id="6f2ea-141">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="6f2ea-141">In Global Catalog</span></span>      | <span data-ttu-id="6f2ea-142">Falso</span><span class="sxs-lookup"><span data-stu-id="6f2ea-142">False</span></span>                                                              |
| <span data-ttu-id="6f2ea-143">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="6f2ea-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="6f2ea-144">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="6f2ea-144">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="6f2ea-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6f2ea-145">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="6f2ea-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6f2ea-146">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="6f2ea-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6f2ea-147">Search-Flags</span></span>           | <span data-ttu-id="6f2ea-148">0x00000008</span><span class="sxs-lookup"><span data-stu-id="6f2ea-148">0x00000008</span></span>                                                         |
| <span data-ttu-id="6f2ea-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6f2ea-149">System-Flags</span></span>           | <span data-ttu-id="6f2ea-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6f2ea-150">0x00000010</span></span>                                                         |
| <span data-ttu-id="6f2ea-151">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="6f2ea-151">Classes used in</span></span>        | [<span data-ttu-id="6f2ea-152">**Infrastruttura-aggiornamento**</span><span class="sxs-lookup"><span data-stu-id="6f2ea-152">**Infrastructure-Update**</span></span>](c-infrastructureupdate.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="6f2ea-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6f2ea-153">Windows Server 2003</span></span>



| <span data-ttu-id="6f2ea-154">Voce</span><span class="sxs-lookup"><span data-stu-id="6f2ea-154">Entry</span></span> | <span data-ttu-id="6f2ea-155">Valore</span><span class="sxs-lookup"><span data-stu-id="6f2ea-155">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="6f2ea-156">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="6f2ea-156">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="6f2ea-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6f2ea-157">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="6f2ea-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="6f2ea-158">System-Only</span></span>            | <span data-ttu-id="6f2ea-159">Vero</span><span class="sxs-lookup"><span data-stu-id="6f2ea-159">True</span></span>                                                               |
| <span data-ttu-id="6f2ea-160">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="6f2ea-160">Is-Single-Valued</span></span>       | <span data-ttu-id="6f2ea-161">Falso</span><span class="sxs-lookup"><span data-stu-id="6f2ea-161">False</span></span>                                                              |
| <span data-ttu-id="6f2ea-162">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="6f2ea-162">Is Indexed</span></span>             | <span data-ttu-id="6f2ea-163">Falso</span><span class="sxs-lookup"><span data-stu-id="6f2ea-163">False</span></span>                                                              |
| <span data-ttu-id="6f2ea-164">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="6f2ea-164">In Global Catalog</span></span>      | <span data-ttu-id="6f2ea-165">Falso</span><span class="sxs-lookup"><span data-stu-id="6f2ea-165">False</span></span>                                                              |
| <span data-ttu-id="6f2ea-166">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="6f2ea-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="6f2ea-167">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="6f2ea-167">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="6f2ea-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6f2ea-168">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="6f2ea-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6f2ea-169">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="6f2ea-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6f2ea-170">Search-Flags</span></span>           | <span data-ttu-id="6f2ea-171">0x00000008</span><span class="sxs-lookup"><span data-stu-id="6f2ea-171">0x00000008</span></span>                                                         |
| <span data-ttu-id="6f2ea-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6f2ea-172">System-Flags</span></span>           | <span data-ttu-id="6f2ea-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6f2ea-173">0x00000010</span></span>                                                         |
| <span data-ttu-id="6f2ea-174">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="6f2ea-174">Classes used in</span></span>        | [<span data-ttu-id="6f2ea-175">**Infrastruttura-aggiornamento**</span><span class="sxs-lookup"><span data-stu-id="6f2ea-175">**Infrastructure-Update**</span></span>](c-infrastructureupdate.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="6f2ea-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="6f2ea-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="6f2ea-177">Voce</span><span class="sxs-lookup"><span data-stu-id="6f2ea-177">Entry</span></span> | <span data-ttu-id="6f2ea-178">Valore</span><span class="sxs-lookup"><span data-stu-id="6f2ea-178">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="6f2ea-179">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="6f2ea-179">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="6f2ea-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6f2ea-180">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="6f2ea-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="6f2ea-181">System-Only</span></span>            | <span data-ttu-id="6f2ea-182">Vero</span><span class="sxs-lookup"><span data-stu-id="6f2ea-182">True</span></span>                                                               |
| <span data-ttu-id="6f2ea-183">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="6f2ea-183">Is-Single-Valued</span></span>       | <span data-ttu-id="6f2ea-184">Falso</span><span class="sxs-lookup"><span data-stu-id="6f2ea-184">False</span></span>                                                              |
| <span data-ttu-id="6f2ea-185">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="6f2ea-185">Is Indexed</span></span>             | <span data-ttu-id="6f2ea-186">Falso</span><span class="sxs-lookup"><span data-stu-id="6f2ea-186">False</span></span>                                                              |
| <span data-ttu-id="6f2ea-187">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="6f2ea-187">In Global Catalog</span></span>      | <span data-ttu-id="6f2ea-188">Falso</span><span class="sxs-lookup"><span data-stu-id="6f2ea-188">False</span></span>                                                              |
| <span data-ttu-id="6f2ea-189">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="6f2ea-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="6f2ea-190">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="6f2ea-190">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="6f2ea-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6f2ea-191">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="6f2ea-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6f2ea-192">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="6f2ea-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6f2ea-193">Search-Flags</span></span>           | <span data-ttu-id="6f2ea-194">0x00000008</span><span class="sxs-lookup"><span data-stu-id="6f2ea-194">0x00000008</span></span>                                                         |
| <span data-ttu-id="6f2ea-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6f2ea-195">System-Flags</span></span>           | <span data-ttu-id="6f2ea-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6f2ea-196">0x00000010</span></span>                                                         |
| <span data-ttu-id="6f2ea-197">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="6f2ea-197">Classes used in</span></span>        | [<span data-ttu-id="6f2ea-198">**Infrastruttura-aggiornamento**</span><span class="sxs-lookup"><span data-stu-id="6f2ea-198">**Infrastructure-Update**</span></span>](c-infrastructureupdate.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="6f2ea-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6f2ea-199">Windows Server 2008</span></span>



| <span data-ttu-id="6f2ea-200">Voce</span><span class="sxs-lookup"><span data-stu-id="6f2ea-200">Entry</span></span> | <span data-ttu-id="6f2ea-201">Valore</span><span class="sxs-lookup"><span data-stu-id="6f2ea-201">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="6f2ea-202">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="6f2ea-202">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="6f2ea-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6f2ea-203">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="6f2ea-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="6f2ea-204">System-Only</span></span>            | <span data-ttu-id="6f2ea-205">Vero</span><span class="sxs-lookup"><span data-stu-id="6f2ea-205">True</span></span>                                                               |
| <span data-ttu-id="6f2ea-206">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="6f2ea-206">Is-Single-Valued</span></span>       | <span data-ttu-id="6f2ea-207">Falso</span><span class="sxs-lookup"><span data-stu-id="6f2ea-207">False</span></span>                                                              |
| <span data-ttu-id="6f2ea-208">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="6f2ea-208">Is Indexed</span></span>             | <span data-ttu-id="6f2ea-209">Falso</span><span class="sxs-lookup"><span data-stu-id="6f2ea-209">False</span></span>                                                              |
| <span data-ttu-id="6f2ea-210">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="6f2ea-210">In Global Catalog</span></span>      | <span data-ttu-id="6f2ea-211">Falso</span><span class="sxs-lookup"><span data-stu-id="6f2ea-211">False</span></span>                                                              |
| <span data-ttu-id="6f2ea-212">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="6f2ea-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="6f2ea-213">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="6f2ea-213">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="6f2ea-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6f2ea-214">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="6f2ea-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6f2ea-215">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="6f2ea-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6f2ea-216">Search-Flags</span></span>           | <span data-ttu-id="6f2ea-217">0x00000008</span><span class="sxs-lookup"><span data-stu-id="6f2ea-217">0x00000008</span></span>                                                         |
| <span data-ttu-id="6f2ea-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6f2ea-218">System-Flags</span></span>           | <span data-ttu-id="6f2ea-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6f2ea-219">0x00000010</span></span>                                                         |
| <span data-ttu-id="6f2ea-220">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="6f2ea-220">Classes used in</span></span>        | [<span data-ttu-id="6f2ea-221">**Infrastruttura-aggiornamento**</span><span class="sxs-lookup"><span data-stu-id="6f2ea-221">**Infrastructure-Update**</span></span>](c-infrastructureupdate.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="6f2ea-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6f2ea-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="6f2ea-223">Voce</span><span class="sxs-lookup"><span data-stu-id="6f2ea-223">Entry</span></span> | <span data-ttu-id="6f2ea-224">Valore</span><span class="sxs-lookup"><span data-stu-id="6f2ea-224">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="6f2ea-225">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="6f2ea-225">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="6f2ea-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6f2ea-226">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="6f2ea-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="6f2ea-227">System-Only</span></span>            | <span data-ttu-id="6f2ea-228">Vero</span><span class="sxs-lookup"><span data-stu-id="6f2ea-228">True</span></span>                                                               |
| <span data-ttu-id="6f2ea-229">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="6f2ea-229">Is-Single-Valued</span></span>       | <span data-ttu-id="6f2ea-230">Falso</span><span class="sxs-lookup"><span data-stu-id="6f2ea-230">False</span></span>                                                              |
| <span data-ttu-id="6f2ea-231">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="6f2ea-231">Is Indexed</span></span>             | <span data-ttu-id="6f2ea-232">Falso</span><span class="sxs-lookup"><span data-stu-id="6f2ea-232">False</span></span>                                                              |
| <span data-ttu-id="6f2ea-233">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="6f2ea-233">In Global Catalog</span></span>      | <span data-ttu-id="6f2ea-234">Falso</span><span class="sxs-lookup"><span data-stu-id="6f2ea-234">False</span></span>                                                              |
| <span data-ttu-id="6f2ea-235">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="6f2ea-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="6f2ea-236">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="6f2ea-236">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="6f2ea-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6f2ea-237">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="6f2ea-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6f2ea-238">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="6f2ea-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6f2ea-239">Search-Flags</span></span>           | <span data-ttu-id="6f2ea-240">0x00000008</span><span class="sxs-lookup"><span data-stu-id="6f2ea-240">0x00000008</span></span>                                                         |
| <span data-ttu-id="6f2ea-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6f2ea-241">System-Flags</span></span>           | <span data-ttu-id="6f2ea-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6f2ea-242">0x00000010</span></span>                                                         |
| <span data-ttu-id="6f2ea-243">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="6f2ea-243">Classes used in</span></span>        | [<span data-ttu-id="6f2ea-244">**Infrastruttura-aggiornamento**</span><span class="sxs-lookup"><span data-stu-id="6f2ea-244">**Infrastructure-Update**</span></span>](c-infrastructureupdate.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="6f2ea-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6f2ea-245">Windows Server 2012</span></span>



| <span data-ttu-id="6f2ea-246">Voce</span><span class="sxs-lookup"><span data-stu-id="6f2ea-246">Entry</span></span> | <span data-ttu-id="6f2ea-247">Valore</span><span class="sxs-lookup"><span data-stu-id="6f2ea-247">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="6f2ea-248">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="6f2ea-248">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="6f2ea-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6f2ea-249">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="6f2ea-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="6f2ea-250">System-Only</span></span>            | <span data-ttu-id="6f2ea-251">Vero</span><span class="sxs-lookup"><span data-stu-id="6f2ea-251">True</span></span>                                                               |
| <span data-ttu-id="6f2ea-252">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="6f2ea-252">Is-Single-Valued</span></span>       | <span data-ttu-id="6f2ea-253">Falso</span><span class="sxs-lookup"><span data-stu-id="6f2ea-253">False</span></span>                                                              |
| <span data-ttu-id="6f2ea-254">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="6f2ea-254">Is Indexed</span></span>             | <span data-ttu-id="6f2ea-255">Falso</span><span class="sxs-lookup"><span data-stu-id="6f2ea-255">False</span></span>                                                              |
| <span data-ttu-id="6f2ea-256">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="6f2ea-256">In Global Catalog</span></span>      | <span data-ttu-id="6f2ea-257">Falso</span><span class="sxs-lookup"><span data-stu-id="6f2ea-257">False</span></span>                                                              |
| <span data-ttu-id="6f2ea-258">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="6f2ea-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="6f2ea-259">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="6f2ea-259">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="6f2ea-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6f2ea-260">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="6f2ea-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6f2ea-261">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="6f2ea-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6f2ea-262">Search-Flags</span></span>           | <span data-ttu-id="6f2ea-263">0x00000008</span><span class="sxs-lookup"><span data-stu-id="6f2ea-263">0x00000008</span></span>                                                         |
| <span data-ttu-id="6f2ea-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6f2ea-264">System-Flags</span></span>           | <span data-ttu-id="6f2ea-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6f2ea-265">0x00000010</span></span>                                                         |
| <span data-ttu-id="6f2ea-266">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="6f2ea-266">Classes used in</span></span>        | [<span data-ttu-id="6f2ea-267">**Infrastruttura-aggiornamento**</span><span class="sxs-lookup"><span data-stu-id="6f2ea-267">**Infrastructure-Update**</span></span>](c-infrastructureupdate.md)<br/> |



 

 





