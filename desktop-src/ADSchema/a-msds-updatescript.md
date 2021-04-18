---
title: attributo ms-DS-UpdateScript
description: Viene utilizzato per mantenere lo script con le istruzioni di ristrutturazione del dominio.
ms.assetid: a9dd205d-f6c3-4eeb-95dc-491bfe30ab8b
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo ms-DS-UpdateScript
- attributo msDS-UpdateScript-schema AD
topic_type:
- apiref
api_name:
- ms-DS-UpdateScript
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7809bf6fdbaabb38976068d1998cacfb12bdaf3
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "106303488"
---
# <a name="ms-ds-updatescript-attribute"></a><span data-ttu-id="e89ae-105">attributo ms-DS-UpdateScript</span><span class="sxs-lookup"><span data-stu-id="e89ae-105">ms-DS-UpdateScript attribute</span></span>

<span data-ttu-id="e89ae-106">Viene utilizzato per mantenere lo script con le istruzioni di ristrutturazione del dominio.</span><span class="sxs-lookup"><span data-stu-id="e89ae-106">This is used to hold the script with the domain restructure instructions.</span></span>



| <span data-ttu-id="e89ae-107">Voce</span><span class="sxs-lookup"><span data-stu-id="e89ae-107">Entry</span></span> | <span data-ttu-id="e89ae-108">Valore</span><span class="sxs-lookup"><span data-stu-id="e89ae-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="e89ae-109">CN</span><span class="sxs-lookup"><span data-stu-id="e89ae-109">CN</span></span>                | <span data-ttu-id="e89ae-110">ms-DS-UpdateScript</span><span class="sxs-lookup"><span data-stu-id="e89ae-110">ms-DS-UpdateScript</span></span>                          |
| <span data-ttu-id="e89ae-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="e89ae-111">Ldap-Display-Name</span></span> | <span data-ttu-id="e89ae-112">msDS-UpdateScript</span><span class="sxs-lookup"><span data-stu-id="e89ae-112">msDS-UpdateScript</span></span>                           |
| <span data-ttu-id="e89ae-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="e89ae-113">Size</span></span>              | <span data-ttu-id="e89ae-114">Dimensioni massime di 10.000 byte.</span><span class="sxs-lookup"><span data-stu-id="e89ae-114">Maximum size 10K bytes.</span></span>                     |
| <span data-ttu-id="e89ae-115">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="e89ae-115">Update Privilege</span></span>  | <span data-ttu-id="e89ae-116">Questo valore viene impostato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="e89ae-116">This value is set by the system.</span></span>            |
| <span data-ttu-id="e89ae-117">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="e89ae-117">Update Frequency</span></span>  | <span data-ttu-id="e89ae-118">Solo durante la ristrutturazione del dominio.</span><span class="sxs-lookup"><span data-stu-id="e89ae-118">Only during domain restructure.</span></span>             |
| <span data-ttu-id="e89ae-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e89ae-119">Attribute-Id</span></span>      | <span data-ttu-id="e89ae-120">1.2.840.113556.1.4.1721</span><span class="sxs-lookup"><span data-stu-id="e89ae-120">1.2.840.113556.1.4.1721</span></span>                     |
| <span data-ttu-id="e89ae-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="e89ae-121">System-Id-Guid</span></span>    | <span data-ttu-id="e89ae-122">146eb639-bb9f-4fc1-a825-e29e00c77920</span><span class="sxs-lookup"><span data-stu-id="e89ae-122">146eb639-bb9f-4fc1-a825-e29e00c77920</span></span>        |
| <span data-ttu-id="e89ae-123">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e89ae-123">Syntax</span></span>            | [<span data-ttu-id="e89ae-124">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="e89ae-124">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="e89ae-125">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="e89ae-125">Implementations</span></span>

-   [<span data-ttu-id="e89ae-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e89ae-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e89ae-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="e89ae-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="e89ae-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e89ae-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e89ae-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e89ae-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e89ae-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e89ae-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e89ae-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e89ae-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="e89ae-132">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e89ae-132">Windows Server 2003</span></span>



| <span data-ttu-id="e89ae-133">Voce</span><span class="sxs-lookup"><span data-stu-id="e89ae-133">Entry</span></span> | <span data-ttu-id="e89ae-134">Valore</span><span class="sxs-lookup"><span data-stu-id="e89ae-134">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="e89ae-135">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="e89ae-135">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="e89ae-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e89ae-136">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="e89ae-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="e89ae-137">System-Only</span></span>            | <span data-ttu-id="e89ae-138">Falso</span><span class="sxs-lookup"><span data-stu-id="e89ae-138">False</span></span>                                                         |
| <span data-ttu-id="e89ae-139">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="e89ae-139">Is-Single-Valued</span></span>       | <span data-ttu-id="e89ae-140">Vero</span><span class="sxs-lookup"><span data-stu-id="e89ae-140">True</span></span>                                                          |
| <span data-ttu-id="e89ae-141">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="e89ae-141">Is Indexed</span></span>             | <span data-ttu-id="e89ae-142">Falso</span><span class="sxs-lookup"><span data-stu-id="e89ae-142">False</span></span>                                                         |
| <span data-ttu-id="e89ae-143">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="e89ae-143">In Global Catalog</span></span>      | <span data-ttu-id="e89ae-144">Falso</span><span class="sxs-lookup"><span data-stu-id="e89ae-144">False</span></span>                                                         |
| <span data-ttu-id="e89ae-145">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="e89ae-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="e89ae-146">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="e89ae-146">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="e89ae-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e89ae-147">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="e89ae-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e89ae-148">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="e89ae-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e89ae-149">Search-Flags</span></span>           | <span data-ttu-id="e89ae-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e89ae-150">0x00000000</span></span>                                                    |
| <span data-ttu-id="e89ae-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e89ae-151">System-Flags</span></span>           | <span data-ttu-id="e89ae-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e89ae-152">0x00000010</span></span>                                                    |
| <span data-ttu-id="e89ae-153">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="e89ae-153">Classes used in</span></span>        | [<span data-ttu-id="e89ae-154">**Cross-Ref-container**</span><span class="sxs-lookup"><span data-stu-id="e89ae-154">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



## <a name="adam"></a><span data-ttu-id="e89ae-155">ADAM</span><span class="sxs-lookup"><span data-stu-id="e89ae-155">ADAM</span></span>



| <span data-ttu-id="e89ae-156">Voce</span><span class="sxs-lookup"><span data-stu-id="e89ae-156">Entry</span></span> | <span data-ttu-id="e89ae-157">Valore</span><span class="sxs-lookup"><span data-stu-id="e89ae-157">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="e89ae-158">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="e89ae-158">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="e89ae-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e89ae-159">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="e89ae-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="e89ae-160">System-Only</span></span>            | <span data-ttu-id="e89ae-161">Falso</span><span class="sxs-lookup"><span data-stu-id="e89ae-161">False</span></span>                                                         |
| <span data-ttu-id="e89ae-162">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="e89ae-162">Is-Single-Valued</span></span>       | <span data-ttu-id="e89ae-163">Vero</span><span class="sxs-lookup"><span data-stu-id="e89ae-163">True</span></span>                                                          |
| <span data-ttu-id="e89ae-164">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="e89ae-164">Is Indexed</span></span>             | <span data-ttu-id="e89ae-165">Falso</span><span class="sxs-lookup"><span data-stu-id="e89ae-165">False</span></span>                                                         |
| <span data-ttu-id="e89ae-166">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="e89ae-166">In Global Catalog</span></span>      | <span data-ttu-id="e89ae-167">Falso</span><span class="sxs-lookup"><span data-stu-id="e89ae-167">False</span></span>                                                         |
| <span data-ttu-id="e89ae-168">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="e89ae-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="e89ae-169">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="e89ae-169">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="e89ae-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e89ae-170">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="e89ae-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e89ae-171">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="e89ae-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e89ae-172">Search-Flags</span></span>           | <span data-ttu-id="e89ae-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e89ae-173">0x00000000</span></span>                                                    |
| <span data-ttu-id="e89ae-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e89ae-174">System-Flags</span></span>           | <span data-ttu-id="e89ae-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e89ae-175">0x00000010</span></span>                                                    |
| <span data-ttu-id="e89ae-176">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="e89ae-176">Classes used in</span></span>        | [<span data-ttu-id="e89ae-177">**Cross-Ref-container**</span><span class="sxs-lookup"><span data-stu-id="e89ae-177">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e89ae-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e89ae-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e89ae-179">Voce</span><span class="sxs-lookup"><span data-stu-id="e89ae-179">Entry</span></span> | <span data-ttu-id="e89ae-180">Valore</span><span class="sxs-lookup"><span data-stu-id="e89ae-180">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="e89ae-181">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="e89ae-181">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="e89ae-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e89ae-182">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="e89ae-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="e89ae-183">System-Only</span></span>            | <span data-ttu-id="e89ae-184">Falso</span><span class="sxs-lookup"><span data-stu-id="e89ae-184">False</span></span>                                                         |
| <span data-ttu-id="e89ae-185">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="e89ae-185">Is-Single-Valued</span></span>       | <span data-ttu-id="e89ae-186">Vero</span><span class="sxs-lookup"><span data-stu-id="e89ae-186">True</span></span>                                                          |
| <span data-ttu-id="e89ae-187">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="e89ae-187">Is Indexed</span></span>             | <span data-ttu-id="e89ae-188">Falso</span><span class="sxs-lookup"><span data-stu-id="e89ae-188">False</span></span>                                                         |
| <span data-ttu-id="e89ae-189">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="e89ae-189">In Global Catalog</span></span>      | <span data-ttu-id="e89ae-190">Falso</span><span class="sxs-lookup"><span data-stu-id="e89ae-190">False</span></span>                                                         |
| <span data-ttu-id="e89ae-191">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="e89ae-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="e89ae-192">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="e89ae-192">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="e89ae-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e89ae-193">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="e89ae-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e89ae-194">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="e89ae-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e89ae-195">Search-Flags</span></span>           | <span data-ttu-id="e89ae-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e89ae-196">0x00000000</span></span>                                                    |
| <span data-ttu-id="e89ae-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e89ae-197">System-Flags</span></span>           | <span data-ttu-id="e89ae-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e89ae-198">0x00000010</span></span>                                                    |
| <span data-ttu-id="e89ae-199">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="e89ae-199">Classes used in</span></span>        | [<span data-ttu-id="e89ae-200">**Cross-Ref-container**</span><span class="sxs-lookup"><span data-stu-id="e89ae-200">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="e89ae-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e89ae-201">Windows Server 2008</span></span>



| <span data-ttu-id="e89ae-202">Voce</span><span class="sxs-lookup"><span data-stu-id="e89ae-202">Entry</span></span> | <span data-ttu-id="e89ae-203">Valore</span><span class="sxs-lookup"><span data-stu-id="e89ae-203">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="e89ae-204">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="e89ae-204">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="e89ae-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e89ae-205">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="e89ae-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="e89ae-206">System-Only</span></span>            | <span data-ttu-id="e89ae-207">Falso</span><span class="sxs-lookup"><span data-stu-id="e89ae-207">False</span></span>                                                         |
| <span data-ttu-id="e89ae-208">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="e89ae-208">Is-Single-Valued</span></span>       | <span data-ttu-id="e89ae-209">Vero</span><span class="sxs-lookup"><span data-stu-id="e89ae-209">True</span></span>                                                          |
| <span data-ttu-id="e89ae-210">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="e89ae-210">Is Indexed</span></span>             | <span data-ttu-id="e89ae-211">Falso</span><span class="sxs-lookup"><span data-stu-id="e89ae-211">False</span></span>                                                         |
| <span data-ttu-id="e89ae-212">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="e89ae-212">In Global Catalog</span></span>      | <span data-ttu-id="e89ae-213">Falso</span><span class="sxs-lookup"><span data-stu-id="e89ae-213">False</span></span>                                                         |
| <span data-ttu-id="e89ae-214">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="e89ae-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="e89ae-215">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="e89ae-215">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="e89ae-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e89ae-216">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="e89ae-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e89ae-217">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="e89ae-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e89ae-218">Search-Flags</span></span>           | <span data-ttu-id="e89ae-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e89ae-219">0x00000000</span></span>                                                    |
| <span data-ttu-id="e89ae-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e89ae-220">System-Flags</span></span>           | <span data-ttu-id="e89ae-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e89ae-221">0x00000010</span></span>                                                    |
| <span data-ttu-id="e89ae-222">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="e89ae-222">Classes used in</span></span>        | [<span data-ttu-id="e89ae-223">**Cross-Ref-container**</span><span class="sxs-lookup"><span data-stu-id="e89ae-223">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e89ae-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e89ae-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e89ae-225">Voce</span><span class="sxs-lookup"><span data-stu-id="e89ae-225">Entry</span></span> | <span data-ttu-id="e89ae-226">Valore</span><span class="sxs-lookup"><span data-stu-id="e89ae-226">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="e89ae-227">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="e89ae-227">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="e89ae-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e89ae-228">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="e89ae-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="e89ae-229">System-Only</span></span>            | <span data-ttu-id="e89ae-230">Falso</span><span class="sxs-lookup"><span data-stu-id="e89ae-230">False</span></span>                                                         |
| <span data-ttu-id="e89ae-231">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="e89ae-231">Is-Single-Valued</span></span>       | <span data-ttu-id="e89ae-232">Vero</span><span class="sxs-lookup"><span data-stu-id="e89ae-232">True</span></span>                                                          |
| <span data-ttu-id="e89ae-233">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="e89ae-233">Is Indexed</span></span>             | <span data-ttu-id="e89ae-234">Falso</span><span class="sxs-lookup"><span data-stu-id="e89ae-234">False</span></span>                                                         |
| <span data-ttu-id="e89ae-235">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="e89ae-235">In Global Catalog</span></span>      | <span data-ttu-id="e89ae-236">Falso</span><span class="sxs-lookup"><span data-stu-id="e89ae-236">False</span></span>                                                         |
| <span data-ttu-id="e89ae-237">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="e89ae-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="e89ae-238">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="e89ae-238">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="e89ae-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e89ae-239">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="e89ae-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e89ae-240">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="e89ae-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e89ae-241">Search-Flags</span></span>           | <span data-ttu-id="e89ae-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e89ae-242">0x00000000</span></span>                                                    |
| <span data-ttu-id="e89ae-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e89ae-243">System-Flags</span></span>           | <span data-ttu-id="e89ae-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e89ae-244">0x00000010</span></span>                                                    |
| <span data-ttu-id="e89ae-245">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="e89ae-245">Classes used in</span></span>        | [<span data-ttu-id="e89ae-246">**Cross-Ref-container**</span><span class="sxs-lookup"><span data-stu-id="e89ae-246">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e89ae-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e89ae-247">Windows Server 2012</span></span>



| <span data-ttu-id="e89ae-248">Voce</span><span class="sxs-lookup"><span data-stu-id="e89ae-248">Entry</span></span> | <span data-ttu-id="e89ae-249">Valore</span><span class="sxs-lookup"><span data-stu-id="e89ae-249">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="e89ae-250">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="e89ae-250">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="e89ae-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e89ae-251">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="e89ae-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="e89ae-252">System-Only</span></span>            | <span data-ttu-id="e89ae-253">Falso</span><span class="sxs-lookup"><span data-stu-id="e89ae-253">False</span></span>                                                         |
| <span data-ttu-id="e89ae-254">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="e89ae-254">Is-Single-Valued</span></span>       | <span data-ttu-id="e89ae-255">Vero</span><span class="sxs-lookup"><span data-stu-id="e89ae-255">True</span></span>                                                          |
| <span data-ttu-id="e89ae-256">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="e89ae-256">Is Indexed</span></span>             | <span data-ttu-id="e89ae-257">Falso</span><span class="sxs-lookup"><span data-stu-id="e89ae-257">False</span></span>                                                         |
| <span data-ttu-id="e89ae-258">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="e89ae-258">In Global Catalog</span></span>      | <span data-ttu-id="e89ae-259">Falso</span><span class="sxs-lookup"><span data-stu-id="e89ae-259">False</span></span>                                                         |
| <span data-ttu-id="e89ae-260">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="e89ae-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="e89ae-261">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="e89ae-261">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="e89ae-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e89ae-262">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="e89ae-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e89ae-263">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="e89ae-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e89ae-264">Search-Flags</span></span>           | <span data-ttu-id="e89ae-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e89ae-265">0x00000000</span></span>                                                    |
| <span data-ttu-id="e89ae-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e89ae-266">System-Flags</span></span>           | <span data-ttu-id="e89ae-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e89ae-267">0x00000010</span></span>                                                    |
| <span data-ttu-id="e89ae-268">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="e89ae-268">Classes used in</span></span>        | [<span data-ttu-id="e89ae-269">**Cross-Ref-container**</span><span class="sxs-lookup"><span data-stu-id="e89ae-269">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



 

 





