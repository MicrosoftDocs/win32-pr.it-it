---
title: Attributo Revisione
description: Livello di revisione per un descrittore di sicurezza o un'altra modifica. Usato solo negli oggetti Sam-server e DS-UI-Settings.
ms.assetid: 480de80f-3e76-4a62-a4a7-29a67f910a62
ms.tgt_platform: multiple
keywords:
- Schema di AD dell'attributo Revisione
- Schema di AD dell'attributo Revisione
topic_type:
- apiref
api_name:
- Revision
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8948bd865db776c52ac021d296792a6f7d0720dc
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104519670"
---
# <a name="revision-attribute"></a><span data-ttu-id="1b9b7-106">Attributo Revisione</span><span class="sxs-lookup"><span data-stu-id="1b9b7-106">Revision attribute</span></span>

<span data-ttu-id="1b9b7-107">Livello di revisione per un descrittore di sicurezza o un'altra modifica.</span><span class="sxs-lookup"><span data-stu-id="1b9b7-107">The revision level for a security descriptor or other change.</span></span> <span data-ttu-id="1b9b7-108">Usato solo negli oggetti Sam-server e DS-UI-Settings.</span><span class="sxs-lookup"><span data-stu-id="1b9b7-108">Only used in the sam-server and ds-ui-settings objects.</span></span>



| <span data-ttu-id="1b9b7-109">Voce</span><span class="sxs-lookup"><span data-stu-id="1b9b7-109">Entry</span></span> | <span data-ttu-id="1b9b7-110">Valore</span><span class="sxs-lookup"><span data-stu-id="1b9b7-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="1b9b7-111">CN</span><span class="sxs-lookup"><span data-stu-id="1b9b7-111">CN</span></span>                | <span data-ttu-id="1b9b7-112">Revisione</span><span class="sxs-lookup"><span data-stu-id="1b9b7-112">Revision</span></span>                             |
| <span data-ttu-id="1b9b7-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="1b9b7-113">Ldap-Display-Name</span></span> | <span data-ttu-id="1b9b7-114">revision</span><span class="sxs-lookup"><span data-stu-id="1b9b7-114">revision</span></span>                             |
| <span data-ttu-id="1b9b7-115">Dimensione</span><span class="sxs-lookup"><span data-stu-id="1b9b7-115">Size</span></span>              | <span data-ttu-id="1b9b7-116">4 byte</span><span class="sxs-lookup"><span data-stu-id="1b9b7-116">4 bytes</span></span>                              |
| <span data-ttu-id="1b9b7-117">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="1b9b7-117">Update Privilege</span></span>  | <span data-ttu-id="1b9b7-118">Questo valore viene impostato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="1b9b7-118">This value is set by the system.</span></span>     |
| <span data-ttu-id="1b9b7-119">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="1b9b7-119">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="1b9b7-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="1b9b7-120">Attribute-Id</span></span>      | <span data-ttu-id="1b9b7-121">1.2.840.113556.1.4.145</span><span class="sxs-lookup"><span data-stu-id="1b9b7-121">1.2.840.113556.1.4.145</span></span>               |
| <span data-ttu-id="1b9b7-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="1b9b7-122">System-Id-Guid</span></span>    | <span data-ttu-id="1b9b7-123">bf967a21-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="1b9b7-123">bf967a21-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="1b9b7-124">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1b9b7-124">Syntax</span></span>            | [<span data-ttu-id="1b9b7-125">**Enumerazione**</span><span class="sxs-lookup"><span data-stu-id="1b9b7-125">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="1b9b7-126">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="1b9b7-126">Implementations</span></span>

-   [<span data-ttu-id="1b9b7-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="1b9b7-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="1b9b7-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="1b9b7-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="1b9b7-129">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="1b9b7-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="1b9b7-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="1b9b7-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="1b9b7-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="1b9b7-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="1b9b7-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="1b9b7-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="1b9b7-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="1b9b7-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="1b9b7-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1b9b7-134">Windows 2000 Server</span></span>



| <span data-ttu-id="1b9b7-135">Voce</span><span class="sxs-lookup"><span data-stu-id="1b9b7-135">Entry</span></span> | <span data-ttu-id="1b9b7-136">Valore</span><span class="sxs-lookup"><span data-stu-id="1b9b7-136">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1b9b7-137">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="1b9b7-137">Link-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="1b9b7-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1b9b7-138">MAPI-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="1b9b7-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="1b9b7-139">System-Only</span></span>            | <span data-ttu-id="1b9b7-140">Falso</span><span class="sxs-lookup"><span data-stu-id="1b9b7-140">False</span></span>                                                                                 |
| <span data-ttu-id="1b9b7-141">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="1b9b7-141">Is-Single-Valued</span></span>       | <span data-ttu-id="1b9b7-142">Vero</span><span class="sxs-lookup"><span data-stu-id="1b9b7-142">True</span></span>                                                                                  |
| <span data-ttu-id="1b9b7-143">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="1b9b7-143">Is Indexed</span></span>             | <span data-ttu-id="1b9b7-144">Falso</span><span class="sxs-lookup"><span data-stu-id="1b9b7-144">False</span></span>                                                                                 |
| <span data-ttu-id="1b9b7-145">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="1b9b7-145">In Global Catalog</span></span>      | <span data-ttu-id="1b9b7-146">Falso</span><span class="sxs-lookup"><span data-stu-id="1b9b7-146">False</span></span>                                                                                 |
| <span data-ttu-id="1b9b7-147">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="1b9b7-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="1b9b7-148">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="1b9b7-148">O:BAG:BAD:S:</span></span>                                                                          |
| <span data-ttu-id="1b9b7-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1b9b7-149">Range-Lower</span></span>            | \-                                                                                    |
| <span data-ttu-id="1b9b7-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1b9b7-150">Range-Upper</span></span>            | \-                                                                                    |
| <span data-ttu-id="1b9b7-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1b9b7-151">Search-Flags</span></span>           | <span data-ttu-id="1b9b7-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1b9b7-152">0x00000000</span></span>                                                                            |
| <span data-ttu-id="1b9b7-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1b9b7-153">System-Flags</span></span>           | <span data-ttu-id="1b9b7-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1b9b7-154">0x00000010</span></span>                                                                            |
| <span data-ttu-id="1b9b7-155">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="1b9b7-155">Classes used in</span></span>        | [<span data-ttu-id="1b9b7-156">**Sam-dominio-base**</span><span class="sxs-lookup"><span data-stu-id="1b9b7-156">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> [<span data-ttu-id="1b9b7-157">**In alto**</span><span class="sxs-lookup"><span data-stu-id="1b9b7-157">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="1b9b7-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1b9b7-158">Windows Server 2003</span></span>



| <span data-ttu-id="1b9b7-159">Voce</span><span class="sxs-lookup"><span data-stu-id="1b9b7-159">Entry</span></span> | <span data-ttu-id="1b9b7-160">Valore</span><span class="sxs-lookup"><span data-stu-id="1b9b7-160">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1b9b7-161">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="1b9b7-161">Link-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="1b9b7-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1b9b7-162">MAPI-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="1b9b7-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="1b9b7-163">System-Only</span></span>            | <span data-ttu-id="1b9b7-164">Falso</span><span class="sxs-lookup"><span data-stu-id="1b9b7-164">False</span></span>                                                                                 |
| <span data-ttu-id="1b9b7-165">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="1b9b7-165">Is-Single-Valued</span></span>       | <span data-ttu-id="1b9b7-166">Vero</span><span class="sxs-lookup"><span data-stu-id="1b9b7-166">True</span></span>                                                                                  |
| <span data-ttu-id="1b9b7-167">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="1b9b7-167">Is Indexed</span></span>             | <span data-ttu-id="1b9b7-168">Falso</span><span class="sxs-lookup"><span data-stu-id="1b9b7-168">False</span></span>                                                                                 |
| <span data-ttu-id="1b9b7-169">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="1b9b7-169">In Global Catalog</span></span>      | <span data-ttu-id="1b9b7-170">Falso</span><span class="sxs-lookup"><span data-stu-id="1b9b7-170">False</span></span>                                                                                 |
| <span data-ttu-id="1b9b7-171">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="1b9b7-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="1b9b7-172">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="1b9b7-172">O:BAG:BAD:S:</span></span>                                                                          |
| <span data-ttu-id="1b9b7-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1b9b7-173">Range-Lower</span></span>            | \-                                                                                    |
| <span data-ttu-id="1b9b7-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1b9b7-174">Range-Upper</span></span>            | \-                                                                                    |
| <span data-ttu-id="1b9b7-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1b9b7-175">Search-Flags</span></span>           | <span data-ttu-id="1b9b7-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1b9b7-176">0x00000000</span></span>                                                                            |
| <span data-ttu-id="1b9b7-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1b9b7-177">System-Flags</span></span>           | <span data-ttu-id="1b9b7-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1b9b7-178">0x00000010</span></span>                                                                            |
| <span data-ttu-id="1b9b7-179">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="1b9b7-179">Classes used in</span></span>        | [<span data-ttu-id="1b9b7-180">**Sam-dominio-base**</span><span class="sxs-lookup"><span data-stu-id="1b9b7-180">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> [<span data-ttu-id="1b9b7-181">**In alto**</span><span class="sxs-lookup"><span data-stu-id="1b9b7-181">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="1b9b7-182">ADAM</span><span class="sxs-lookup"><span data-stu-id="1b9b7-182">ADAM</span></span>



| <span data-ttu-id="1b9b7-183">Voce</span><span class="sxs-lookup"><span data-stu-id="1b9b7-183">Entry</span></span> | <span data-ttu-id="1b9b7-184">Valore</span><span class="sxs-lookup"><span data-stu-id="1b9b7-184">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="1b9b7-185">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="1b9b7-185">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="1b9b7-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1b9b7-186">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="1b9b7-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="1b9b7-187">System-Only</span></span>            | <span data-ttu-id="1b9b7-188">Falso</span><span class="sxs-lookup"><span data-stu-id="1b9b7-188">False</span></span>                           |
| <span data-ttu-id="1b9b7-189">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="1b9b7-189">Is-Single-Valued</span></span>       | <span data-ttu-id="1b9b7-190">Vero</span><span class="sxs-lookup"><span data-stu-id="1b9b7-190">True</span></span>                            |
| <span data-ttu-id="1b9b7-191">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="1b9b7-191">Is Indexed</span></span>             | <span data-ttu-id="1b9b7-192">Falso</span><span class="sxs-lookup"><span data-stu-id="1b9b7-192">False</span></span>                           |
| <span data-ttu-id="1b9b7-193">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="1b9b7-193">In Global Catalog</span></span>      | <span data-ttu-id="1b9b7-194">Falso</span><span class="sxs-lookup"><span data-stu-id="1b9b7-194">False</span></span>                           |
| <span data-ttu-id="1b9b7-195">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="1b9b7-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="1b9b7-196">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="1b9b7-196">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="1b9b7-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1b9b7-197">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="1b9b7-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1b9b7-198">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="1b9b7-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1b9b7-199">Search-Flags</span></span>           | <span data-ttu-id="1b9b7-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1b9b7-200">0x00000000</span></span>                      |
| <span data-ttu-id="1b9b7-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1b9b7-201">System-Flags</span></span>           | <span data-ttu-id="1b9b7-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1b9b7-202">0x00000010</span></span>                      |
| <span data-ttu-id="1b9b7-203">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="1b9b7-203">Classes used in</span></span>        | [<span data-ttu-id="1b9b7-204">**In alto**</span><span class="sxs-lookup"><span data-stu-id="1b9b7-204">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="1b9b7-205">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="1b9b7-205">Windows Server 2003 R2</span></span>



| <span data-ttu-id="1b9b7-206">Voce</span><span class="sxs-lookup"><span data-stu-id="1b9b7-206">Entry</span></span> | <span data-ttu-id="1b9b7-207">Valore</span><span class="sxs-lookup"><span data-stu-id="1b9b7-207">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1b9b7-208">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="1b9b7-208">Link-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="1b9b7-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1b9b7-209">MAPI-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="1b9b7-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="1b9b7-210">System-Only</span></span>            | <span data-ttu-id="1b9b7-211">Falso</span><span class="sxs-lookup"><span data-stu-id="1b9b7-211">False</span></span>                                                                                 |
| <span data-ttu-id="1b9b7-212">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="1b9b7-212">Is-Single-Valued</span></span>       | <span data-ttu-id="1b9b7-213">Vero</span><span class="sxs-lookup"><span data-stu-id="1b9b7-213">True</span></span>                                                                                  |
| <span data-ttu-id="1b9b7-214">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="1b9b7-214">Is Indexed</span></span>             | <span data-ttu-id="1b9b7-215">Falso</span><span class="sxs-lookup"><span data-stu-id="1b9b7-215">False</span></span>                                                                                 |
| <span data-ttu-id="1b9b7-216">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="1b9b7-216">In Global Catalog</span></span>      | <span data-ttu-id="1b9b7-217">Falso</span><span class="sxs-lookup"><span data-stu-id="1b9b7-217">False</span></span>                                                                                 |
| <span data-ttu-id="1b9b7-218">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="1b9b7-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="1b9b7-219">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="1b9b7-219">O:BAG:BAD:S:</span></span>                                                                          |
| <span data-ttu-id="1b9b7-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1b9b7-220">Range-Lower</span></span>            | \-                                                                                    |
| <span data-ttu-id="1b9b7-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1b9b7-221">Range-Upper</span></span>            | \-                                                                                    |
| <span data-ttu-id="1b9b7-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1b9b7-222">Search-Flags</span></span>           | <span data-ttu-id="1b9b7-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1b9b7-223">0x00000000</span></span>                                                                            |
| <span data-ttu-id="1b9b7-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1b9b7-224">System-Flags</span></span>           | <span data-ttu-id="1b9b7-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1b9b7-225">0x00000010</span></span>                                                                            |
| <span data-ttu-id="1b9b7-226">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="1b9b7-226">Classes used in</span></span>        | [<span data-ttu-id="1b9b7-227">**Sam-dominio-base**</span><span class="sxs-lookup"><span data-stu-id="1b9b7-227">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> [<span data-ttu-id="1b9b7-228">**In alto**</span><span class="sxs-lookup"><span data-stu-id="1b9b7-228">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="1b9b7-229">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1b9b7-229">Windows Server 2008</span></span>



| <span data-ttu-id="1b9b7-230">Voce</span><span class="sxs-lookup"><span data-stu-id="1b9b7-230">Entry</span></span> | <span data-ttu-id="1b9b7-231">Valore</span><span class="sxs-lookup"><span data-stu-id="1b9b7-231">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1b9b7-232">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="1b9b7-232">Link-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="1b9b7-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1b9b7-233">MAPI-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="1b9b7-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="1b9b7-234">System-Only</span></span>            | <span data-ttu-id="1b9b7-235">Falso</span><span class="sxs-lookup"><span data-stu-id="1b9b7-235">False</span></span>                                                                                 |
| <span data-ttu-id="1b9b7-236">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="1b9b7-236">Is-Single-Valued</span></span>       | <span data-ttu-id="1b9b7-237">Vero</span><span class="sxs-lookup"><span data-stu-id="1b9b7-237">True</span></span>                                                                                  |
| <span data-ttu-id="1b9b7-238">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="1b9b7-238">Is Indexed</span></span>             | <span data-ttu-id="1b9b7-239">Falso</span><span class="sxs-lookup"><span data-stu-id="1b9b7-239">False</span></span>                                                                                 |
| <span data-ttu-id="1b9b7-240">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="1b9b7-240">In Global Catalog</span></span>      | <span data-ttu-id="1b9b7-241">Falso</span><span class="sxs-lookup"><span data-stu-id="1b9b7-241">False</span></span>                                                                                 |
| <span data-ttu-id="1b9b7-242">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="1b9b7-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="1b9b7-243">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="1b9b7-243">O:BAG:BAD:S:</span></span>                                                                          |
| <span data-ttu-id="1b9b7-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1b9b7-244">Range-Lower</span></span>            | \-                                                                                    |
| <span data-ttu-id="1b9b7-245">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1b9b7-245">Range-Upper</span></span>            | \-                                                                                    |
| <span data-ttu-id="1b9b7-246">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1b9b7-246">Search-Flags</span></span>           | <span data-ttu-id="1b9b7-247">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1b9b7-247">0x00000000</span></span>                                                                            |
| <span data-ttu-id="1b9b7-248">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1b9b7-248">System-Flags</span></span>           | <span data-ttu-id="1b9b7-249">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1b9b7-249">0x00000010</span></span>                                                                            |
| <span data-ttu-id="1b9b7-250">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="1b9b7-250">Classes used in</span></span>        | [<span data-ttu-id="1b9b7-251">**Sam-dominio-base**</span><span class="sxs-lookup"><span data-stu-id="1b9b7-251">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> [<span data-ttu-id="1b9b7-252">**In alto**</span><span class="sxs-lookup"><span data-stu-id="1b9b7-252">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="1b9b7-253">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1b9b7-253">Windows Server 2008 R2</span></span>



| <span data-ttu-id="1b9b7-254">Voce</span><span class="sxs-lookup"><span data-stu-id="1b9b7-254">Entry</span></span> | <span data-ttu-id="1b9b7-255">Valore</span><span class="sxs-lookup"><span data-stu-id="1b9b7-255">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1b9b7-256">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="1b9b7-256">Link-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="1b9b7-257">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1b9b7-257">MAPI-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="1b9b7-258">System-Only</span><span class="sxs-lookup"><span data-stu-id="1b9b7-258">System-Only</span></span>            | <span data-ttu-id="1b9b7-259">Falso</span><span class="sxs-lookup"><span data-stu-id="1b9b7-259">False</span></span>                                                                                 |
| <span data-ttu-id="1b9b7-260">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="1b9b7-260">Is-Single-Valued</span></span>       | <span data-ttu-id="1b9b7-261">Vero</span><span class="sxs-lookup"><span data-stu-id="1b9b7-261">True</span></span>                                                                                  |
| <span data-ttu-id="1b9b7-262">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="1b9b7-262">Is Indexed</span></span>             | <span data-ttu-id="1b9b7-263">Falso</span><span class="sxs-lookup"><span data-stu-id="1b9b7-263">False</span></span>                                                                                 |
| <span data-ttu-id="1b9b7-264">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="1b9b7-264">In Global Catalog</span></span>      | <span data-ttu-id="1b9b7-265">Falso</span><span class="sxs-lookup"><span data-stu-id="1b9b7-265">False</span></span>                                                                                 |
| <span data-ttu-id="1b9b7-266">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="1b9b7-266">NT-Security-Descriptor</span></span> | <span data-ttu-id="1b9b7-267">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="1b9b7-267">O:BAG:BAD:S:</span></span>                                                                          |
| <span data-ttu-id="1b9b7-268">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1b9b7-268">Range-Lower</span></span>            | \-                                                                                    |
| <span data-ttu-id="1b9b7-269">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1b9b7-269">Range-Upper</span></span>            | \-                                                                                    |
| <span data-ttu-id="1b9b7-270">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1b9b7-270">Search-Flags</span></span>           | <span data-ttu-id="1b9b7-271">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1b9b7-271">0x00000000</span></span>                                                                            |
| <span data-ttu-id="1b9b7-272">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1b9b7-272">System-Flags</span></span>           | <span data-ttu-id="1b9b7-273">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1b9b7-273">0x00000010</span></span>                                                                            |
| <span data-ttu-id="1b9b7-274">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="1b9b7-274">Classes used in</span></span>        | [<span data-ttu-id="1b9b7-275">**Sam-dominio-base**</span><span class="sxs-lookup"><span data-stu-id="1b9b7-275">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> [<span data-ttu-id="1b9b7-276">**In alto**</span><span class="sxs-lookup"><span data-stu-id="1b9b7-276">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="1b9b7-277">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1b9b7-277">Windows Server 2012</span></span>



| <span data-ttu-id="1b9b7-278">Voce</span><span class="sxs-lookup"><span data-stu-id="1b9b7-278">Entry</span></span> | <span data-ttu-id="1b9b7-279">Valore</span><span class="sxs-lookup"><span data-stu-id="1b9b7-279">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1b9b7-280">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="1b9b7-280">Link-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="1b9b7-281">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1b9b7-281">MAPI-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="1b9b7-282">System-Only</span><span class="sxs-lookup"><span data-stu-id="1b9b7-282">System-Only</span></span>            | <span data-ttu-id="1b9b7-283">Falso</span><span class="sxs-lookup"><span data-stu-id="1b9b7-283">False</span></span>                                                                                 |
| <span data-ttu-id="1b9b7-284">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="1b9b7-284">Is-Single-Valued</span></span>       | <span data-ttu-id="1b9b7-285">Vero</span><span class="sxs-lookup"><span data-stu-id="1b9b7-285">True</span></span>                                                                                  |
| <span data-ttu-id="1b9b7-286">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="1b9b7-286">Is Indexed</span></span>             | <span data-ttu-id="1b9b7-287">Falso</span><span class="sxs-lookup"><span data-stu-id="1b9b7-287">False</span></span>                                                                                 |
| <span data-ttu-id="1b9b7-288">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="1b9b7-288">In Global Catalog</span></span>      | <span data-ttu-id="1b9b7-289">Falso</span><span class="sxs-lookup"><span data-stu-id="1b9b7-289">False</span></span>                                                                                 |
| <span data-ttu-id="1b9b7-290">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="1b9b7-290">NT-Security-Descriptor</span></span> | <span data-ttu-id="1b9b7-291">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="1b9b7-291">O:BAG:BAD:S:</span></span>                                                                          |
| <span data-ttu-id="1b9b7-292">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1b9b7-292">Range-Lower</span></span>            | \-                                                                                    |
| <span data-ttu-id="1b9b7-293">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1b9b7-293">Range-Upper</span></span>            | \-                                                                                    |
| <span data-ttu-id="1b9b7-294">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1b9b7-294">Search-Flags</span></span>           | <span data-ttu-id="1b9b7-295">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1b9b7-295">0x00000000</span></span>                                                                            |
| <span data-ttu-id="1b9b7-296">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1b9b7-296">System-Flags</span></span>           | <span data-ttu-id="1b9b7-297">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1b9b7-297">0x00000010</span></span>                                                                            |
| <span data-ttu-id="1b9b7-298">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="1b9b7-298">Classes used in</span></span>        | [<span data-ttu-id="1b9b7-299">**Sam-dominio-base**</span><span class="sxs-lookup"><span data-stu-id="1b9b7-299">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> [<span data-ttu-id="1b9b7-300">**In alto**</span><span class="sxs-lookup"><span data-stu-id="1b9b7-300">**Top**</span></span>](c-top.md)<br/> |



 

 





