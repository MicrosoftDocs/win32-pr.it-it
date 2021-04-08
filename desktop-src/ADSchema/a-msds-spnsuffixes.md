---
title: attributo ms-DS-SPN-suffissi
description: Questo attributo descrive i suffissi dei nomi host DNS utilizzati dai server della foresta. Questi suffissi DNS verranno condivisi con altre foreste con trust tra foreste e questa foresta.
ms.assetid: 56153832-1228-419f-99d4-eb1ce3edc867
ms.tgt_platform: multiple
keywords:
- ms-DS-SPN-suffissi attributo AD schema
- attributo msDS-SPNSuffixes-schema AD
topic_type:
- apiref
api_name:
- ms-DS-SPN-Suffixes
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c91f7ce8c92e8a81437d90bb0d80383b9ad334ee
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103965260"
---
# <a name="ms-ds-spn-suffixes-attribute"></a><span data-ttu-id="3be77-106">attributo ms-DS-SPN-suffissi</span><span class="sxs-lookup"><span data-stu-id="3be77-106">ms-DS-SPN-Suffixes attribute</span></span>

<span data-ttu-id="3be77-107">Questo attributo descrive i suffissi dei nomi host DNS utilizzati dai server della foresta.</span><span class="sxs-lookup"><span data-stu-id="3be77-107">This attribute describes the suffixes of DNS host names used by servers in the forest.</span></span> <span data-ttu-id="3be77-108">Questi suffissi DNS verranno condivisi con altre foreste con trust tra foreste e questa foresta.</span><span class="sxs-lookup"><span data-stu-id="3be77-108">These DNS suffixes will be shared with other forests that have cross-forest trust with this forest.</span></span>



| <span data-ttu-id="3be77-109">Voce</span><span class="sxs-lookup"><span data-stu-id="3be77-109">Entry</span></span> | <span data-ttu-id="3be77-110">Valore</span><span class="sxs-lookup"><span data-stu-id="3be77-110">Value</span></span> |
|-------------------|----------------------------------------------|
| <span data-ttu-id="3be77-111">CN</span><span class="sxs-lookup"><span data-stu-id="3be77-111">CN</span></span>                | <span data-ttu-id="3be77-112">ms-DS-SPN-suffissi</span><span class="sxs-lookup"><span data-stu-id="3be77-112">ms-DS-SPN-Suffixes</span></span>                           |
| <span data-ttu-id="3be77-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="3be77-113">Ldap-Display-Name</span></span> | <span data-ttu-id="3be77-114">msDS-SPNSuffixes</span><span class="sxs-lookup"><span data-stu-id="3be77-114">msDS-SPNSuffixes</span></span>                             |
| <span data-ttu-id="3be77-115">Dimensione</span><span class="sxs-lookup"><span data-stu-id="3be77-115">Size</span></span>              | <span data-ttu-id="3be77-116">255 byte</span><span class="sxs-lookup"><span data-stu-id="3be77-116">255 bytes</span></span>                                    |
| <span data-ttu-id="3be77-117">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="3be77-117">Update Privilege</span></span>  | <span data-ttu-id="3be77-118">Amministratore di dominio</span><span class="sxs-lookup"><span data-stu-id="3be77-118">Domain administrator</span></span>                         |
| <span data-ttu-id="3be77-119">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="3be77-119">Update Frequency</span></span>  | <span data-ttu-id="3be77-120">Quando i server nella foresta ottengono un nuovo suffisso.</span><span class="sxs-lookup"><span data-stu-id="3be77-120">When servers in the forest get a new suffix.</span></span> |
| <span data-ttu-id="3be77-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="3be77-121">Attribute-Id</span></span>      | <span data-ttu-id="3be77-122">1.2.840.113556.1.4.1715</span><span class="sxs-lookup"><span data-stu-id="3be77-122">1.2.840.113556.1.4.1715</span></span>                      |
| <span data-ttu-id="3be77-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="3be77-123">System-Id-Guid</span></span>    | <span data-ttu-id="3be77-124">789ee1eb-8c8e-4e4c-8cec-79b31b7617b5</span><span class="sxs-lookup"><span data-stu-id="3be77-124">789ee1eb-8c8e-4e4c-8cec-79b31b7617b5</span></span>         |
| <span data-ttu-id="3be77-125">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3be77-125">Syntax</span></span>            | [<span data-ttu-id="3be77-126">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="3be77-126">**String(Unicode)**</span></span>](s-string-unicode.md)  |



## <a name="implementations"></a><span data-ttu-id="3be77-127">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="3be77-127">Implementations</span></span>

-   [<span data-ttu-id="3be77-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="3be77-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="3be77-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="3be77-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="3be77-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="3be77-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="3be77-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="3be77-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="3be77-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="3be77-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="3be77-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3be77-133">Windows Server 2003</span></span>



| <span data-ttu-id="3be77-134">Voce</span><span class="sxs-lookup"><span data-stu-id="3be77-134">Entry</span></span> | <span data-ttu-id="3be77-135">Valore</span><span class="sxs-lookup"><span data-stu-id="3be77-135">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="3be77-136">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="3be77-136">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="3be77-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3be77-137">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="3be77-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="3be77-138">System-Only</span></span>            | <span data-ttu-id="3be77-139">Falso</span><span class="sxs-lookup"><span data-stu-id="3be77-139">False</span></span>                                                         |
| <span data-ttu-id="3be77-140">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="3be77-140">Is-Single-Valued</span></span>       | <span data-ttu-id="3be77-141">Falso</span><span class="sxs-lookup"><span data-stu-id="3be77-141">False</span></span>                                                         |
| <span data-ttu-id="3be77-142">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="3be77-142">Is Indexed</span></span>             | <span data-ttu-id="3be77-143">Falso</span><span class="sxs-lookup"><span data-stu-id="3be77-143">False</span></span>                                                         |
| <span data-ttu-id="3be77-144">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="3be77-144">In Global Catalog</span></span>      | <span data-ttu-id="3be77-145">Falso</span><span class="sxs-lookup"><span data-stu-id="3be77-145">False</span></span>                                                         |
| <span data-ttu-id="3be77-146">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="3be77-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="3be77-147">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="3be77-147">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="3be77-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3be77-148">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="3be77-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3be77-149">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="3be77-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3be77-150">Search-Flags</span></span>           | <span data-ttu-id="3be77-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3be77-151">0x00000000</span></span>                                                    |
| <span data-ttu-id="3be77-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3be77-152">System-Flags</span></span>           | <span data-ttu-id="3be77-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3be77-153">0x00000010</span></span>                                                    |
| <span data-ttu-id="3be77-154">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="3be77-154">Classes used in</span></span>        | [<span data-ttu-id="3be77-155">**Cross-Ref-container**</span><span class="sxs-lookup"><span data-stu-id="3be77-155">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="3be77-156">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="3be77-156">Windows Server 2003 R2</span></span>



| <span data-ttu-id="3be77-157">Voce</span><span class="sxs-lookup"><span data-stu-id="3be77-157">Entry</span></span> | <span data-ttu-id="3be77-158">Valore</span><span class="sxs-lookup"><span data-stu-id="3be77-158">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="3be77-159">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="3be77-159">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="3be77-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3be77-160">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="3be77-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="3be77-161">System-Only</span></span>            | <span data-ttu-id="3be77-162">Falso</span><span class="sxs-lookup"><span data-stu-id="3be77-162">False</span></span>                                                         |
| <span data-ttu-id="3be77-163">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="3be77-163">Is-Single-Valued</span></span>       | <span data-ttu-id="3be77-164">Falso</span><span class="sxs-lookup"><span data-stu-id="3be77-164">False</span></span>                                                         |
| <span data-ttu-id="3be77-165">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="3be77-165">Is Indexed</span></span>             | <span data-ttu-id="3be77-166">Falso</span><span class="sxs-lookup"><span data-stu-id="3be77-166">False</span></span>                                                         |
| <span data-ttu-id="3be77-167">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="3be77-167">In Global Catalog</span></span>      | <span data-ttu-id="3be77-168">Falso</span><span class="sxs-lookup"><span data-stu-id="3be77-168">False</span></span>                                                         |
| <span data-ttu-id="3be77-169">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="3be77-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="3be77-170">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="3be77-170">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="3be77-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3be77-171">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="3be77-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3be77-172">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="3be77-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3be77-173">Search-Flags</span></span>           | <span data-ttu-id="3be77-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3be77-174">0x00000000</span></span>                                                    |
| <span data-ttu-id="3be77-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3be77-175">System-Flags</span></span>           | <span data-ttu-id="3be77-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3be77-176">0x00000010</span></span>                                                    |
| <span data-ttu-id="3be77-177">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="3be77-177">Classes used in</span></span>        | [<span data-ttu-id="3be77-178">**Cross-Ref-container**</span><span class="sxs-lookup"><span data-stu-id="3be77-178">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="3be77-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3be77-179">Windows Server 2008</span></span>



| <span data-ttu-id="3be77-180">Voce</span><span class="sxs-lookup"><span data-stu-id="3be77-180">Entry</span></span> | <span data-ttu-id="3be77-181">Valore</span><span class="sxs-lookup"><span data-stu-id="3be77-181">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="3be77-182">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="3be77-182">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="3be77-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3be77-183">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="3be77-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="3be77-184">System-Only</span></span>            | <span data-ttu-id="3be77-185">Falso</span><span class="sxs-lookup"><span data-stu-id="3be77-185">False</span></span>                                                         |
| <span data-ttu-id="3be77-186">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="3be77-186">Is-Single-Valued</span></span>       | <span data-ttu-id="3be77-187">Falso</span><span class="sxs-lookup"><span data-stu-id="3be77-187">False</span></span>                                                         |
| <span data-ttu-id="3be77-188">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="3be77-188">Is Indexed</span></span>             | <span data-ttu-id="3be77-189">Falso</span><span class="sxs-lookup"><span data-stu-id="3be77-189">False</span></span>                                                         |
| <span data-ttu-id="3be77-190">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="3be77-190">In Global Catalog</span></span>      | <span data-ttu-id="3be77-191">Falso</span><span class="sxs-lookup"><span data-stu-id="3be77-191">False</span></span>                                                         |
| <span data-ttu-id="3be77-192">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="3be77-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="3be77-193">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="3be77-193">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="3be77-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3be77-194">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="3be77-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3be77-195">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="3be77-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3be77-196">Search-Flags</span></span>           | <span data-ttu-id="3be77-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3be77-197">0x00000000</span></span>                                                    |
| <span data-ttu-id="3be77-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3be77-198">System-Flags</span></span>           | <span data-ttu-id="3be77-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3be77-199">0x00000010</span></span>                                                    |
| <span data-ttu-id="3be77-200">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="3be77-200">Classes used in</span></span>        | [<span data-ttu-id="3be77-201">**Cross-Ref-container**</span><span class="sxs-lookup"><span data-stu-id="3be77-201">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="3be77-202">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3be77-202">Windows Server 2008 R2</span></span>



| <span data-ttu-id="3be77-203">Voce</span><span class="sxs-lookup"><span data-stu-id="3be77-203">Entry</span></span> | <span data-ttu-id="3be77-204">Valore</span><span class="sxs-lookup"><span data-stu-id="3be77-204">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="3be77-205">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="3be77-205">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="3be77-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3be77-206">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="3be77-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="3be77-207">System-Only</span></span>            | <span data-ttu-id="3be77-208">Falso</span><span class="sxs-lookup"><span data-stu-id="3be77-208">False</span></span>                                                         |
| <span data-ttu-id="3be77-209">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="3be77-209">Is-Single-Valued</span></span>       | <span data-ttu-id="3be77-210">Falso</span><span class="sxs-lookup"><span data-stu-id="3be77-210">False</span></span>                                                         |
| <span data-ttu-id="3be77-211">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="3be77-211">Is Indexed</span></span>             | <span data-ttu-id="3be77-212">Falso</span><span class="sxs-lookup"><span data-stu-id="3be77-212">False</span></span>                                                         |
| <span data-ttu-id="3be77-213">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="3be77-213">In Global Catalog</span></span>      | <span data-ttu-id="3be77-214">Falso</span><span class="sxs-lookup"><span data-stu-id="3be77-214">False</span></span>                                                         |
| <span data-ttu-id="3be77-215">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="3be77-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="3be77-216">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="3be77-216">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="3be77-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3be77-217">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="3be77-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3be77-218">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="3be77-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3be77-219">Search-Flags</span></span>           | <span data-ttu-id="3be77-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3be77-220">0x00000000</span></span>                                                    |
| <span data-ttu-id="3be77-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3be77-221">System-Flags</span></span>           | <span data-ttu-id="3be77-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3be77-222">0x00000010</span></span>                                                    |
| <span data-ttu-id="3be77-223">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="3be77-223">Classes used in</span></span>        | [<span data-ttu-id="3be77-224">**Cross-Ref-container**</span><span class="sxs-lookup"><span data-stu-id="3be77-224">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="3be77-225">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3be77-225">Windows Server 2012</span></span>



| <span data-ttu-id="3be77-226">Voce</span><span class="sxs-lookup"><span data-stu-id="3be77-226">Entry</span></span> | <span data-ttu-id="3be77-227">Valore</span><span class="sxs-lookup"><span data-stu-id="3be77-227">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="3be77-228">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="3be77-228">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="3be77-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3be77-229">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="3be77-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="3be77-230">System-Only</span></span>            | <span data-ttu-id="3be77-231">Falso</span><span class="sxs-lookup"><span data-stu-id="3be77-231">False</span></span>                                                         |
| <span data-ttu-id="3be77-232">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="3be77-232">Is-Single-Valued</span></span>       | <span data-ttu-id="3be77-233">Falso</span><span class="sxs-lookup"><span data-stu-id="3be77-233">False</span></span>                                                         |
| <span data-ttu-id="3be77-234">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="3be77-234">Is Indexed</span></span>             | <span data-ttu-id="3be77-235">Falso</span><span class="sxs-lookup"><span data-stu-id="3be77-235">False</span></span>                                                         |
| <span data-ttu-id="3be77-236">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="3be77-236">In Global Catalog</span></span>      | <span data-ttu-id="3be77-237">Falso</span><span class="sxs-lookup"><span data-stu-id="3be77-237">False</span></span>                                                         |
| <span data-ttu-id="3be77-238">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="3be77-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="3be77-239">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="3be77-239">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="3be77-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3be77-240">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="3be77-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3be77-241">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="3be77-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3be77-242">Search-Flags</span></span>           | <span data-ttu-id="3be77-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3be77-243">0x00000000</span></span>                                                    |
| <span data-ttu-id="3be77-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3be77-244">System-Flags</span></span>           | <span data-ttu-id="3be77-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3be77-245">0x00000010</span></span>                                                    |
| <span data-ttu-id="3be77-246">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="3be77-246">Classes used in</span></span>        | [<span data-ttu-id="3be77-247">**Cross-Ref-container**</span><span class="sxs-lookup"><span data-stu-id="3be77-247">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



 

 





