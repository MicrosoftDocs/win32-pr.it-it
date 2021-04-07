---
title: Attributo padre-GUID
description: Si tratta di un attributo costruito, inventato per supportare il controllo DirSync. Questo attributo include il objectGuid dell'elemento padre di un oggetto durante la replica della creazione, della ridenominazione o dello spostamento di un oggetto.
ms.assetid: caf2491b-c0bf-4ea1-80ec-d44cf9307551
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo padre-GUID
- Schema AD dell'attributo parentGUID
topic_type:
- apiref
api_name:
- Parent-GUID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38b01faf958f4add9c7788d630321d7c225f5026
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103875581"
---
# <a name="parent-guid-attribute"></a><span data-ttu-id="b0c37-106">Attributo padre-GUID</span><span class="sxs-lookup"><span data-stu-id="b0c37-106">Parent-GUID attribute</span></span>

<span data-ttu-id="b0c37-107">Si tratta di un attributo costruito, inventato per supportare il controllo DirSync.</span><span class="sxs-lookup"><span data-stu-id="b0c37-107">This is a constructed attribute, invented to support the DirSync control.</span></span> <span data-ttu-id="b0c37-108">Questo attributo include il objectGuid dell'elemento padre di un oggetto durante la replica della creazione, della ridenominazione o dello spostamento di un oggetto.</span><span class="sxs-lookup"><span data-stu-id="b0c37-108">This attribute holds the objectGuid of an object's parent when replicating an object's creation, rename, or move.</span></span>



| <span data-ttu-id="b0c37-109">Voce</span><span class="sxs-lookup"><span data-stu-id="b0c37-109">Entry</span></span> | <span data-ttu-id="b0c37-110">Valore</span><span class="sxs-lookup"><span data-stu-id="b0c37-110">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="b0c37-111">CN</span><span class="sxs-lookup"><span data-stu-id="b0c37-111">CN</span></span>                | <span data-ttu-id="b0c37-112">Padre-GUID</span><span class="sxs-lookup"><span data-stu-id="b0c37-112">Parent-GUID</span></span>                                           |
| <span data-ttu-id="b0c37-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="b0c37-113">Ldap-Display-Name</span></span> | <span data-ttu-id="b0c37-114">parentGUID</span><span class="sxs-lookup"><span data-stu-id="b0c37-114">parentGUID</span></span>                                            |
| <span data-ttu-id="b0c37-115">Dimensione</span><span class="sxs-lookup"><span data-stu-id="b0c37-115">Size</span></span>              | <span data-ttu-id="b0c37-116">16 byte</span><span class="sxs-lookup"><span data-stu-id="b0c37-116">16 bytes</span></span>                                              |
| <span data-ttu-id="b0c37-117">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="b0c37-117">Update Privilege</span></span>  | <span data-ttu-id="b0c37-118">Questo valore viene impostato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="b0c37-118">This value is set by the system.</span></span>                      |
| <span data-ttu-id="b0c37-119">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="b0c37-119">Update Frequency</span></span>  | <span data-ttu-id="b0c37-120">Durante la replica</span><span class="sxs-lookup"><span data-stu-id="b0c37-120">During replication</span></span>                                    |
| <span data-ttu-id="b0c37-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b0c37-121">Attribute-Id</span></span>      | <span data-ttu-id="b0c37-122">1.2.840.113556.1.4.1224</span><span class="sxs-lookup"><span data-stu-id="b0c37-122">1.2.840.113556.1.4.1224</span></span>                               |
| <span data-ttu-id="b0c37-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="b0c37-123">System-Id-Guid</span></span>    | <span data-ttu-id="b0c37-124">2df90d74-009f-11d2-aa4c-00c04fd7d83a</span><span class="sxs-lookup"><span data-stu-id="b0c37-124">2df90d74-009f-11d2-aa4c-00c04fd7d83a</span></span>                  |
| <span data-ttu-id="b0c37-125">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b0c37-125">Syntax</span></span>            | [<span data-ttu-id="b0c37-126">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="b0c37-126">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="b0c37-127">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="b0c37-127">Implementations</span></span>

-   [<span data-ttu-id="b0c37-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="b0c37-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="b0c37-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b0c37-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b0c37-130">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="b0c37-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="b0c37-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b0c37-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b0c37-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b0c37-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b0c37-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b0c37-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b0c37-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b0c37-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="b0c37-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b0c37-135">Windows 2000 Server</span></span>



| <span data-ttu-id="b0c37-136">Voce</span><span class="sxs-lookup"><span data-stu-id="b0c37-136">Entry</span></span> | <span data-ttu-id="b0c37-137">Valore</span><span class="sxs-lookup"><span data-stu-id="b0c37-137">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="b0c37-138">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="b0c37-138">Link-Id</span></span>                | \-           |
| <span data-ttu-id="b0c37-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b0c37-139">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="b0c37-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="b0c37-140">System-Only</span></span>            | <span data-ttu-id="b0c37-141">Vero</span><span class="sxs-lookup"><span data-stu-id="b0c37-141">True</span></span>         |
| <span data-ttu-id="b0c37-142">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="b0c37-142">Is-Single-Valued</span></span>       | <span data-ttu-id="b0c37-143">Vero</span><span class="sxs-lookup"><span data-stu-id="b0c37-143">True</span></span>         |
| <span data-ttu-id="b0c37-144">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="b0c37-144">Is Indexed</span></span>             | <span data-ttu-id="b0c37-145">Falso</span><span class="sxs-lookup"><span data-stu-id="b0c37-145">False</span></span>        |
| <span data-ttu-id="b0c37-146">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="b0c37-146">In Global Catalog</span></span>      | <span data-ttu-id="b0c37-147">Falso</span><span class="sxs-lookup"><span data-stu-id="b0c37-147">False</span></span>        |
| <span data-ttu-id="b0c37-148">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="b0c37-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="b0c37-149">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="b0c37-149">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="b0c37-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b0c37-150">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="b0c37-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b0c37-151">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="b0c37-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b0c37-152">Search-Flags</span></span>           | <span data-ttu-id="b0c37-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b0c37-153">0x00000000</span></span>   |
| <span data-ttu-id="b0c37-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b0c37-154">System-Flags</span></span>           | <span data-ttu-id="b0c37-155">0x08000014</span><span class="sxs-lookup"><span data-stu-id="b0c37-155">0x08000014</span></span>   |
| <span data-ttu-id="b0c37-156">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="b0c37-156">Classes used in</span></span>        | \-           |



## <a name="windows-server-2003"></a><span data-ttu-id="b0c37-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b0c37-157">Windows Server 2003</span></span>



| <span data-ttu-id="b0c37-158">Voce</span><span class="sxs-lookup"><span data-stu-id="b0c37-158">Entry</span></span> | <span data-ttu-id="b0c37-159">Valore</span><span class="sxs-lookup"><span data-stu-id="b0c37-159">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="b0c37-160">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="b0c37-160">Link-Id</span></span>                | \-           |
| <span data-ttu-id="b0c37-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b0c37-161">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="b0c37-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="b0c37-162">System-Only</span></span>            | <span data-ttu-id="b0c37-163">Vero</span><span class="sxs-lookup"><span data-stu-id="b0c37-163">True</span></span>         |
| <span data-ttu-id="b0c37-164">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="b0c37-164">Is-Single-Valued</span></span>       | <span data-ttu-id="b0c37-165">Vero</span><span class="sxs-lookup"><span data-stu-id="b0c37-165">True</span></span>         |
| <span data-ttu-id="b0c37-166">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="b0c37-166">Is Indexed</span></span>             | <span data-ttu-id="b0c37-167">Falso</span><span class="sxs-lookup"><span data-stu-id="b0c37-167">False</span></span>        |
| <span data-ttu-id="b0c37-168">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="b0c37-168">In Global Catalog</span></span>      | <span data-ttu-id="b0c37-169">Falso</span><span class="sxs-lookup"><span data-stu-id="b0c37-169">False</span></span>        |
| <span data-ttu-id="b0c37-170">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="b0c37-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="b0c37-171">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="b0c37-171">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="b0c37-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b0c37-172">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="b0c37-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b0c37-173">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="b0c37-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b0c37-174">Search-Flags</span></span>           | <span data-ttu-id="b0c37-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b0c37-175">0x00000000</span></span>   |
| <span data-ttu-id="b0c37-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b0c37-176">System-Flags</span></span>           | <span data-ttu-id="b0c37-177">0x08000014</span><span class="sxs-lookup"><span data-stu-id="b0c37-177">0x08000014</span></span>   |
| <span data-ttu-id="b0c37-178">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="b0c37-178">Classes used in</span></span>        | \-           |



## <a name="adam"></a><span data-ttu-id="b0c37-179">ADAM</span><span class="sxs-lookup"><span data-stu-id="b0c37-179">ADAM</span></span>



| <span data-ttu-id="b0c37-180">Voce</span><span class="sxs-lookup"><span data-stu-id="b0c37-180">Entry</span></span> | <span data-ttu-id="b0c37-181">Valore</span><span class="sxs-lookup"><span data-stu-id="b0c37-181">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="b0c37-182">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="b0c37-182">Link-Id</span></span>                | \-           |
| <span data-ttu-id="b0c37-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b0c37-183">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="b0c37-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="b0c37-184">System-Only</span></span>            | <span data-ttu-id="b0c37-185">Vero</span><span class="sxs-lookup"><span data-stu-id="b0c37-185">True</span></span>         |
| <span data-ttu-id="b0c37-186">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="b0c37-186">Is-Single-Valued</span></span>       | <span data-ttu-id="b0c37-187">Vero</span><span class="sxs-lookup"><span data-stu-id="b0c37-187">True</span></span>         |
| <span data-ttu-id="b0c37-188">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="b0c37-188">Is Indexed</span></span>             | <span data-ttu-id="b0c37-189">Falso</span><span class="sxs-lookup"><span data-stu-id="b0c37-189">False</span></span>        |
| <span data-ttu-id="b0c37-190">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="b0c37-190">In Global Catalog</span></span>      | <span data-ttu-id="b0c37-191">Falso</span><span class="sxs-lookup"><span data-stu-id="b0c37-191">False</span></span>        |
| <span data-ttu-id="b0c37-192">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="b0c37-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="b0c37-193">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="b0c37-193">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="b0c37-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b0c37-194">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="b0c37-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b0c37-195">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="b0c37-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b0c37-196">Search-Flags</span></span>           | <span data-ttu-id="b0c37-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b0c37-197">0x00000000</span></span>   |
| <span data-ttu-id="b0c37-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b0c37-198">System-Flags</span></span>           | <span data-ttu-id="b0c37-199">0x08000014</span><span class="sxs-lookup"><span data-stu-id="b0c37-199">0x08000014</span></span>   |
| <span data-ttu-id="b0c37-200">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="b0c37-200">Classes used in</span></span>        | \-           |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b0c37-201">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b0c37-201">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b0c37-202">Voce</span><span class="sxs-lookup"><span data-stu-id="b0c37-202">Entry</span></span> | <span data-ttu-id="b0c37-203">Valore</span><span class="sxs-lookup"><span data-stu-id="b0c37-203">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="b0c37-204">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="b0c37-204">Link-Id</span></span>                | \-           |
| <span data-ttu-id="b0c37-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b0c37-205">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="b0c37-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="b0c37-206">System-Only</span></span>            | <span data-ttu-id="b0c37-207">Vero</span><span class="sxs-lookup"><span data-stu-id="b0c37-207">True</span></span>         |
| <span data-ttu-id="b0c37-208">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="b0c37-208">Is-Single-Valued</span></span>       | <span data-ttu-id="b0c37-209">Vero</span><span class="sxs-lookup"><span data-stu-id="b0c37-209">True</span></span>         |
| <span data-ttu-id="b0c37-210">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="b0c37-210">Is Indexed</span></span>             | <span data-ttu-id="b0c37-211">Falso</span><span class="sxs-lookup"><span data-stu-id="b0c37-211">False</span></span>        |
| <span data-ttu-id="b0c37-212">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="b0c37-212">In Global Catalog</span></span>      | <span data-ttu-id="b0c37-213">Falso</span><span class="sxs-lookup"><span data-stu-id="b0c37-213">False</span></span>        |
| <span data-ttu-id="b0c37-214">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="b0c37-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="b0c37-215">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="b0c37-215">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="b0c37-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b0c37-216">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="b0c37-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b0c37-217">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="b0c37-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b0c37-218">Search-Flags</span></span>           | <span data-ttu-id="b0c37-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b0c37-219">0x00000000</span></span>   |
| <span data-ttu-id="b0c37-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b0c37-220">System-Flags</span></span>           | <span data-ttu-id="b0c37-221">0x08000014</span><span class="sxs-lookup"><span data-stu-id="b0c37-221">0x08000014</span></span>   |
| <span data-ttu-id="b0c37-222">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="b0c37-222">Classes used in</span></span>        | \-           |



## <a name="windows-server-2008"></a><span data-ttu-id="b0c37-223">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b0c37-223">Windows Server 2008</span></span>



| <span data-ttu-id="b0c37-224">Voce</span><span class="sxs-lookup"><span data-stu-id="b0c37-224">Entry</span></span> | <span data-ttu-id="b0c37-225">Valore</span><span class="sxs-lookup"><span data-stu-id="b0c37-225">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="b0c37-226">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="b0c37-226">Link-Id</span></span>                | \-           |
| <span data-ttu-id="b0c37-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b0c37-227">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="b0c37-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="b0c37-228">System-Only</span></span>            | <span data-ttu-id="b0c37-229">Vero</span><span class="sxs-lookup"><span data-stu-id="b0c37-229">True</span></span>         |
| <span data-ttu-id="b0c37-230">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="b0c37-230">Is-Single-Valued</span></span>       | <span data-ttu-id="b0c37-231">Vero</span><span class="sxs-lookup"><span data-stu-id="b0c37-231">True</span></span>         |
| <span data-ttu-id="b0c37-232">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="b0c37-232">Is Indexed</span></span>             | <span data-ttu-id="b0c37-233">Falso</span><span class="sxs-lookup"><span data-stu-id="b0c37-233">False</span></span>        |
| <span data-ttu-id="b0c37-234">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="b0c37-234">In Global Catalog</span></span>      | <span data-ttu-id="b0c37-235">Falso</span><span class="sxs-lookup"><span data-stu-id="b0c37-235">False</span></span>        |
| <span data-ttu-id="b0c37-236">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="b0c37-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="b0c37-237">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="b0c37-237">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="b0c37-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b0c37-238">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="b0c37-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b0c37-239">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="b0c37-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b0c37-240">Search-Flags</span></span>           | <span data-ttu-id="b0c37-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b0c37-241">0x00000000</span></span>   |
| <span data-ttu-id="b0c37-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b0c37-242">System-Flags</span></span>           | <span data-ttu-id="b0c37-243">0x08000014</span><span class="sxs-lookup"><span data-stu-id="b0c37-243">0x08000014</span></span>   |
| <span data-ttu-id="b0c37-244">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="b0c37-244">Classes used in</span></span>        | \-           |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b0c37-245">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b0c37-245">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b0c37-246">Voce</span><span class="sxs-lookup"><span data-stu-id="b0c37-246">Entry</span></span> | <span data-ttu-id="b0c37-247">Valore</span><span class="sxs-lookup"><span data-stu-id="b0c37-247">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="b0c37-248">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="b0c37-248">Link-Id</span></span>                | \-           |
| <span data-ttu-id="b0c37-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b0c37-249">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="b0c37-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="b0c37-250">System-Only</span></span>            | <span data-ttu-id="b0c37-251">Vero</span><span class="sxs-lookup"><span data-stu-id="b0c37-251">True</span></span>         |
| <span data-ttu-id="b0c37-252">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="b0c37-252">Is-Single-Valued</span></span>       | <span data-ttu-id="b0c37-253">Vero</span><span class="sxs-lookup"><span data-stu-id="b0c37-253">True</span></span>         |
| <span data-ttu-id="b0c37-254">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="b0c37-254">Is Indexed</span></span>             | <span data-ttu-id="b0c37-255">Falso</span><span class="sxs-lookup"><span data-stu-id="b0c37-255">False</span></span>        |
| <span data-ttu-id="b0c37-256">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="b0c37-256">In Global Catalog</span></span>      | <span data-ttu-id="b0c37-257">Falso</span><span class="sxs-lookup"><span data-stu-id="b0c37-257">False</span></span>        |
| <span data-ttu-id="b0c37-258">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="b0c37-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="b0c37-259">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="b0c37-259">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="b0c37-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b0c37-260">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="b0c37-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b0c37-261">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="b0c37-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b0c37-262">Search-Flags</span></span>           | <span data-ttu-id="b0c37-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b0c37-263">0x00000000</span></span>   |
| <span data-ttu-id="b0c37-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b0c37-264">System-Flags</span></span>           | <span data-ttu-id="b0c37-265">0x08000014</span><span class="sxs-lookup"><span data-stu-id="b0c37-265">0x08000014</span></span>   |
| <span data-ttu-id="b0c37-266">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="b0c37-266">Classes used in</span></span>        | \-           |



## <a name="windows-server-2012"></a><span data-ttu-id="b0c37-267">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b0c37-267">Windows Server 2012</span></span>



| <span data-ttu-id="b0c37-268">Voce</span><span class="sxs-lookup"><span data-stu-id="b0c37-268">Entry</span></span> | <span data-ttu-id="b0c37-269">Valore</span><span class="sxs-lookup"><span data-stu-id="b0c37-269">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="b0c37-270">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="b0c37-270">Link-Id</span></span>                | \-           |
| <span data-ttu-id="b0c37-271">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b0c37-271">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="b0c37-272">System-Only</span><span class="sxs-lookup"><span data-stu-id="b0c37-272">System-Only</span></span>            | <span data-ttu-id="b0c37-273">Vero</span><span class="sxs-lookup"><span data-stu-id="b0c37-273">True</span></span>         |
| <span data-ttu-id="b0c37-274">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="b0c37-274">Is-Single-Valued</span></span>       | <span data-ttu-id="b0c37-275">Vero</span><span class="sxs-lookup"><span data-stu-id="b0c37-275">True</span></span>         |
| <span data-ttu-id="b0c37-276">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="b0c37-276">Is Indexed</span></span>             | <span data-ttu-id="b0c37-277">Falso</span><span class="sxs-lookup"><span data-stu-id="b0c37-277">False</span></span>        |
| <span data-ttu-id="b0c37-278">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="b0c37-278">In Global Catalog</span></span>      | <span data-ttu-id="b0c37-279">Falso</span><span class="sxs-lookup"><span data-stu-id="b0c37-279">False</span></span>        |
| <span data-ttu-id="b0c37-280">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="b0c37-280">NT-Security-Descriptor</span></span> | <span data-ttu-id="b0c37-281">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="b0c37-281">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="b0c37-282">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b0c37-282">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="b0c37-283">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b0c37-283">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="b0c37-284">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b0c37-284">Search-Flags</span></span>           | <span data-ttu-id="b0c37-285">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b0c37-285">0x00000000</span></span>   |
| <span data-ttu-id="b0c37-286">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b0c37-286">System-Flags</span></span>           | <span data-ttu-id="b0c37-287">0x08000014</span><span class="sxs-lookup"><span data-stu-id="b0c37-287">0x08000014</span></span>   |
| <span data-ttu-id="b0c37-288">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="b0c37-288">Classes used in</span></span>        | \-           |



 

 




