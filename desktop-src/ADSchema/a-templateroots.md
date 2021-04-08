---
title: Attributo Template-Roots
description: Questo attributo viene usato nel contenitore di configurazione di Exchange per indicare la posizione in cui vengono archiviati i contenitori di modelli. Queste informazioni vengono utilizzate dal provider MAPI Active Directory.
ms.assetid: 1416ce4a-ca07-4ca9-8ea1-e1a6ad19e7ad
ms.tgt_platform: multiple
keywords:
- Schema AD Template-Roots attribute
- Schema AD dell'attributo templateRoots
topic_type:
- apiref
api_name:
- Template-Roots
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 761c6d3d79bbf45e9a4d391b612956d6893cd314
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744898"
---
# <a name="template-roots-attribute"></a><span data-ttu-id="dc6ab-106">Attributo Template-Roots</span><span class="sxs-lookup"><span data-stu-id="dc6ab-106">Template-Roots attribute</span></span>

<span data-ttu-id="dc6ab-107">Questo attributo viene usato nel contenitore di configurazione di Exchange per indicare la posizione in cui vengono archiviati i contenitori di modelli.</span><span class="sxs-lookup"><span data-stu-id="dc6ab-107">This attribute is used on the Exchange config container to indicate where the template containers are stored.</span></span> <span data-ttu-id="dc6ab-108">Queste informazioni vengono utilizzate dal provider MAPI Active Directory.</span><span class="sxs-lookup"><span data-stu-id="dc6ab-108">This information is used by the Active Directory MAPI provider.</span></span>



| <span data-ttu-id="dc6ab-109">Voce</span><span class="sxs-lookup"><span data-stu-id="dc6ab-109">Entry</span></span> | <span data-ttu-id="dc6ab-110">Valore</span><span class="sxs-lookup"><span data-stu-id="dc6ab-110">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="dc6ab-111">CN</span><span class="sxs-lookup"><span data-stu-id="dc6ab-111">CN</span></span>                | <span data-ttu-id="dc6ab-112">Template-Roots</span><span class="sxs-lookup"><span data-stu-id="dc6ab-112">Template-Roots</span></span>                          |
| <span data-ttu-id="dc6ab-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="dc6ab-113">Ldap-Display-Name</span></span> | <span data-ttu-id="dc6ab-114">templateRoots</span><span class="sxs-lookup"><span data-stu-id="dc6ab-114">templateRoots</span></span>                           |
| <span data-ttu-id="dc6ab-115">Dimensione</span><span class="sxs-lookup"><span data-stu-id="dc6ab-115">Size</span></span>              | \-                                      |
| <span data-ttu-id="dc6ab-116">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="dc6ab-116">Update Privilege</span></span>  | <span data-ttu-id="dc6ab-117">Viene utilizzato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="dc6ab-117">This is used by the system.</span></span>             |
| <span data-ttu-id="dc6ab-118">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="dc6ab-118">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="dc6ab-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="dc6ab-119">Attribute-Id</span></span>      | <span data-ttu-id="dc6ab-120">1.2.840.113556.1.4.1346</span><span class="sxs-lookup"><span data-stu-id="dc6ab-120">1.2.840.113556.1.4.1346</span></span>                 |
| <span data-ttu-id="dc6ab-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="dc6ab-121">System-Id-Guid</span></span>    | <span data-ttu-id="dc6ab-122">ed9de9a0-7041-11d2-9905-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="dc6ab-122">ed9de9a0-7041-11d2-9905-0000f87a57d4</span></span>    |
| <span data-ttu-id="dc6ab-123">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dc6ab-123">Syntax</span></span>            | [<span data-ttu-id="dc6ab-124">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="dc6ab-124">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="dc6ab-125">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="dc6ab-125">Implementations</span></span>

-   [<span data-ttu-id="dc6ab-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="dc6ab-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="dc6ab-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="dc6ab-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="dc6ab-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="dc6ab-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="dc6ab-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="dc6ab-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="dc6ab-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="dc6ab-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="dc6ab-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="dc6ab-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="dc6ab-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="dc6ab-132">Windows 2000 Server</span></span>



| <span data-ttu-id="dc6ab-133">Voce</span><span class="sxs-lookup"><span data-stu-id="dc6ab-133">Entry</span></span> | <span data-ttu-id="dc6ab-134">Valore</span><span class="sxs-lookup"><span data-stu-id="dc6ab-134">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="dc6ab-135">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="dc6ab-135">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="dc6ab-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dc6ab-136">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="dc6ab-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="dc6ab-137">System-Only</span></span>            | <span data-ttu-id="dc6ab-138">Falso</span><span class="sxs-lookup"><span data-stu-id="dc6ab-138">False</span></span>                                                                                |
| <span data-ttu-id="dc6ab-139">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="dc6ab-139">Is-Single-Valued</span></span>       | <span data-ttu-id="dc6ab-140">Falso</span><span class="sxs-lookup"><span data-stu-id="dc6ab-140">False</span></span>                                                                                |
| <span data-ttu-id="dc6ab-141">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="dc6ab-141">Is Indexed</span></span>             | <span data-ttu-id="dc6ab-142">Falso</span><span class="sxs-lookup"><span data-stu-id="dc6ab-142">False</span></span>                                                                                |
| <span data-ttu-id="dc6ab-143">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="dc6ab-143">In Global Catalog</span></span>      | <span data-ttu-id="dc6ab-144">Falso</span><span class="sxs-lookup"><span data-stu-id="dc6ab-144">False</span></span>                                                                                |
| <span data-ttu-id="dc6ab-145">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="dc6ab-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="dc6ab-146">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="dc6ab-146">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="dc6ab-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dc6ab-147">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="dc6ab-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dc6ab-148">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="dc6ab-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dc6ab-149">Search-Flags</span></span>           | <span data-ttu-id="dc6ab-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dc6ab-150">0x00000000</span></span>                                                                           |
| <span data-ttu-id="dc6ab-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dc6ab-151">System-Flags</span></span>           | <span data-ttu-id="dc6ab-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dc6ab-152">0x00000010</span></span>                                                                           |
| <span data-ttu-id="dc6ab-153">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="dc6ab-153">Classes used in</span></span>        | [<span data-ttu-id="dc6ab-154">**ms-Exch-Configuration-container**</span><span class="sxs-lookup"><span data-stu-id="dc6ab-154">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="dc6ab-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="dc6ab-155">Windows Server 2003</span></span>



| <span data-ttu-id="dc6ab-156">Voce</span><span class="sxs-lookup"><span data-stu-id="dc6ab-156">Entry</span></span> | <span data-ttu-id="dc6ab-157">Valore</span><span class="sxs-lookup"><span data-stu-id="dc6ab-157">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="dc6ab-158">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="dc6ab-158">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="dc6ab-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dc6ab-159">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="dc6ab-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="dc6ab-160">System-Only</span></span>            | <span data-ttu-id="dc6ab-161">Falso</span><span class="sxs-lookup"><span data-stu-id="dc6ab-161">False</span></span>                                                                                |
| <span data-ttu-id="dc6ab-162">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="dc6ab-162">Is-Single-Valued</span></span>       | <span data-ttu-id="dc6ab-163">Falso</span><span class="sxs-lookup"><span data-stu-id="dc6ab-163">False</span></span>                                                                                |
| <span data-ttu-id="dc6ab-164">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="dc6ab-164">Is Indexed</span></span>             | <span data-ttu-id="dc6ab-165">Falso</span><span class="sxs-lookup"><span data-stu-id="dc6ab-165">False</span></span>                                                                                |
| <span data-ttu-id="dc6ab-166">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="dc6ab-166">In Global Catalog</span></span>      | <span data-ttu-id="dc6ab-167">Falso</span><span class="sxs-lookup"><span data-stu-id="dc6ab-167">False</span></span>                                                                                |
| <span data-ttu-id="dc6ab-168">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="dc6ab-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="dc6ab-169">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="dc6ab-169">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="dc6ab-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dc6ab-170">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="dc6ab-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dc6ab-171">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="dc6ab-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dc6ab-172">Search-Flags</span></span>           | <span data-ttu-id="dc6ab-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dc6ab-173">0x00000000</span></span>                                                                           |
| <span data-ttu-id="dc6ab-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dc6ab-174">System-Flags</span></span>           | <span data-ttu-id="dc6ab-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dc6ab-175">0x00000010</span></span>                                                                           |
| <span data-ttu-id="dc6ab-176">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="dc6ab-176">Classes used in</span></span>        | [<span data-ttu-id="dc6ab-177">**ms-Exch-Configuration-container**</span><span class="sxs-lookup"><span data-stu-id="dc6ab-177">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="dc6ab-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="dc6ab-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="dc6ab-179">Voce</span><span class="sxs-lookup"><span data-stu-id="dc6ab-179">Entry</span></span> | <span data-ttu-id="dc6ab-180">Valore</span><span class="sxs-lookup"><span data-stu-id="dc6ab-180">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="dc6ab-181">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="dc6ab-181">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="dc6ab-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dc6ab-182">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="dc6ab-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="dc6ab-183">System-Only</span></span>            | <span data-ttu-id="dc6ab-184">Falso</span><span class="sxs-lookup"><span data-stu-id="dc6ab-184">False</span></span>                                                                                |
| <span data-ttu-id="dc6ab-185">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="dc6ab-185">Is-Single-Valued</span></span>       | <span data-ttu-id="dc6ab-186">Falso</span><span class="sxs-lookup"><span data-stu-id="dc6ab-186">False</span></span>                                                                                |
| <span data-ttu-id="dc6ab-187">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="dc6ab-187">Is Indexed</span></span>             | <span data-ttu-id="dc6ab-188">Falso</span><span class="sxs-lookup"><span data-stu-id="dc6ab-188">False</span></span>                                                                                |
| <span data-ttu-id="dc6ab-189">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="dc6ab-189">In Global Catalog</span></span>      | <span data-ttu-id="dc6ab-190">Falso</span><span class="sxs-lookup"><span data-stu-id="dc6ab-190">False</span></span>                                                                                |
| <span data-ttu-id="dc6ab-191">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="dc6ab-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="dc6ab-192">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="dc6ab-192">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="dc6ab-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dc6ab-193">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="dc6ab-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dc6ab-194">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="dc6ab-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dc6ab-195">Search-Flags</span></span>           | <span data-ttu-id="dc6ab-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dc6ab-196">0x00000000</span></span>                                                                           |
| <span data-ttu-id="dc6ab-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dc6ab-197">System-Flags</span></span>           | <span data-ttu-id="dc6ab-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dc6ab-198">0x00000010</span></span>                                                                           |
| <span data-ttu-id="dc6ab-199">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="dc6ab-199">Classes used in</span></span>        | [<span data-ttu-id="dc6ab-200">**ms-Exch-Configuration-container**</span><span class="sxs-lookup"><span data-stu-id="dc6ab-200">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="dc6ab-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dc6ab-201">Windows Server 2008</span></span>



| <span data-ttu-id="dc6ab-202">Voce</span><span class="sxs-lookup"><span data-stu-id="dc6ab-202">Entry</span></span> | <span data-ttu-id="dc6ab-203">Valore</span><span class="sxs-lookup"><span data-stu-id="dc6ab-203">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="dc6ab-204">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="dc6ab-204">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="dc6ab-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dc6ab-205">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="dc6ab-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="dc6ab-206">System-Only</span></span>            | <span data-ttu-id="dc6ab-207">Falso</span><span class="sxs-lookup"><span data-stu-id="dc6ab-207">False</span></span>                                                                                |
| <span data-ttu-id="dc6ab-208">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="dc6ab-208">Is-Single-Valued</span></span>       | <span data-ttu-id="dc6ab-209">Falso</span><span class="sxs-lookup"><span data-stu-id="dc6ab-209">False</span></span>                                                                                |
| <span data-ttu-id="dc6ab-210">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="dc6ab-210">Is Indexed</span></span>             | <span data-ttu-id="dc6ab-211">Falso</span><span class="sxs-lookup"><span data-stu-id="dc6ab-211">False</span></span>                                                                                |
| <span data-ttu-id="dc6ab-212">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="dc6ab-212">In Global Catalog</span></span>      | <span data-ttu-id="dc6ab-213">Falso</span><span class="sxs-lookup"><span data-stu-id="dc6ab-213">False</span></span>                                                                                |
| <span data-ttu-id="dc6ab-214">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="dc6ab-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="dc6ab-215">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="dc6ab-215">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="dc6ab-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dc6ab-216">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="dc6ab-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dc6ab-217">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="dc6ab-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dc6ab-218">Search-Flags</span></span>           | <span data-ttu-id="dc6ab-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dc6ab-219">0x00000000</span></span>                                                                           |
| <span data-ttu-id="dc6ab-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dc6ab-220">System-Flags</span></span>           | <span data-ttu-id="dc6ab-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dc6ab-221">0x00000010</span></span>                                                                           |
| <span data-ttu-id="dc6ab-222">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="dc6ab-222">Classes used in</span></span>        | [<span data-ttu-id="dc6ab-223">**ms-Exch-Configuration-container**</span><span class="sxs-lookup"><span data-stu-id="dc6ab-223">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="dc6ab-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="dc6ab-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="dc6ab-225">Voce</span><span class="sxs-lookup"><span data-stu-id="dc6ab-225">Entry</span></span> | <span data-ttu-id="dc6ab-226">Valore</span><span class="sxs-lookup"><span data-stu-id="dc6ab-226">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="dc6ab-227">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="dc6ab-227">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="dc6ab-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dc6ab-228">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="dc6ab-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="dc6ab-229">System-Only</span></span>            | <span data-ttu-id="dc6ab-230">Falso</span><span class="sxs-lookup"><span data-stu-id="dc6ab-230">False</span></span>                                                                                |
| <span data-ttu-id="dc6ab-231">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="dc6ab-231">Is-Single-Valued</span></span>       | <span data-ttu-id="dc6ab-232">Falso</span><span class="sxs-lookup"><span data-stu-id="dc6ab-232">False</span></span>                                                                                |
| <span data-ttu-id="dc6ab-233">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="dc6ab-233">Is Indexed</span></span>             | <span data-ttu-id="dc6ab-234">Falso</span><span class="sxs-lookup"><span data-stu-id="dc6ab-234">False</span></span>                                                                                |
| <span data-ttu-id="dc6ab-235">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="dc6ab-235">In Global Catalog</span></span>      | <span data-ttu-id="dc6ab-236">Falso</span><span class="sxs-lookup"><span data-stu-id="dc6ab-236">False</span></span>                                                                                |
| <span data-ttu-id="dc6ab-237">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="dc6ab-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="dc6ab-238">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="dc6ab-238">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="dc6ab-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dc6ab-239">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="dc6ab-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dc6ab-240">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="dc6ab-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dc6ab-241">Search-Flags</span></span>           | <span data-ttu-id="dc6ab-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dc6ab-242">0x00000000</span></span>                                                                           |
| <span data-ttu-id="dc6ab-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dc6ab-243">System-Flags</span></span>           | <span data-ttu-id="dc6ab-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dc6ab-244">0x00000010</span></span>                                                                           |
| <span data-ttu-id="dc6ab-245">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="dc6ab-245">Classes used in</span></span>        | [<span data-ttu-id="dc6ab-246">**ms-Exch-Configuration-container**</span><span class="sxs-lookup"><span data-stu-id="dc6ab-246">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="dc6ab-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="dc6ab-247">Windows Server 2012</span></span>



| <span data-ttu-id="dc6ab-248">Voce</span><span class="sxs-lookup"><span data-stu-id="dc6ab-248">Entry</span></span> | <span data-ttu-id="dc6ab-249">Valore</span><span class="sxs-lookup"><span data-stu-id="dc6ab-249">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="dc6ab-250">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="dc6ab-250">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="dc6ab-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dc6ab-251">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="dc6ab-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="dc6ab-252">System-Only</span></span>            | <span data-ttu-id="dc6ab-253">Falso</span><span class="sxs-lookup"><span data-stu-id="dc6ab-253">False</span></span>                                                                                |
| <span data-ttu-id="dc6ab-254">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="dc6ab-254">Is-Single-Valued</span></span>       | <span data-ttu-id="dc6ab-255">Falso</span><span class="sxs-lookup"><span data-stu-id="dc6ab-255">False</span></span>                                                                                |
| <span data-ttu-id="dc6ab-256">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="dc6ab-256">Is Indexed</span></span>             | <span data-ttu-id="dc6ab-257">Falso</span><span class="sxs-lookup"><span data-stu-id="dc6ab-257">False</span></span>                                                                                |
| <span data-ttu-id="dc6ab-258">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="dc6ab-258">In Global Catalog</span></span>      | <span data-ttu-id="dc6ab-259">Falso</span><span class="sxs-lookup"><span data-stu-id="dc6ab-259">False</span></span>                                                                                |
| <span data-ttu-id="dc6ab-260">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="dc6ab-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="dc6ab-261">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="dc6ab-261">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="dc6ab-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dc6ab-262">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="dc6ab-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dc6ab-263">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="dc6ab-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dc6ab-264">Search-Flags</span></span>           | <span data-ttu-id="dc6ab-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dc6ab-265">0x00000000</span></span>                                                                           |
| <span data-ttu-id="dc6ab-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dc6ab-266">System-Flags</span></span>           | <span data-ttu-id="dc6ab-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dc6ab-267">0x00000010</span></span>                                                                           |
| <span data-ttu-id="dc6ab-268">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="dc6ab-268">Classes used in</span></span>        | [<span data-ttu-id="dc6ab-269">**ms-Exch-Configuration-container**</span><span class="sxs-lookup"><span data-stu-id="dc6ab-269">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



 

 





