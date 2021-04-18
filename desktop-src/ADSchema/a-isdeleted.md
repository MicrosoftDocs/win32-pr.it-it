---
title: Attributo Is-Deleted
description: Se TRUE, l'oggetto è stato contrassegnato per l'eliminazione e non è possibile crearne un'istanza. Una volta scaduto, il periodo di rimozione definitiva verrà rimosso dal sistema.
ms.assetid: 549b5161-5d2f-47d7-8192-4480334ef13d
ms.tgt_platform: multiple
keywords:
- Schema AD Is-Deleted attribute
- Schema AD dell'attributo eliminato
topic_type:
- apiref
api_name:
- Is-Deleted
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66b30dec5ed139da60853324b82cc6e0f55fcc70
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "106302881"
---
# <a name="is-deleted-attribute"></a><span data-ttu-id="fc9d0-106">Attributo Is-Deleted</span><span class="sxs-lookup"><span data-stu-id="fc9d0-106">Is-Deleted attribute</span></span>

<span data-ttu-id="fc9d0-107">Se **true**, l'oggetto è stato contrassegnato per l'eliminazione e non è possibile crearne un'istanza.</span><span class="sxs-lookup"><span data-stu-id="fc9d0-107">If **TRUE**, this object has been marked for deletion and cannot be instantiated.</span></span> <span data-ttu-id="fc9d0-108">Una volta scaduto, il periodo di rimozione definitiva verrà rimosso dal sistema.</span><span class="sxs-lookup"><span data-stu-id="fc9d0-108">After the tombstone period has expired, it will be removed from the system.</span></span>



| <span data-ttu-id="fc9d0-109">Voce</span><span class="sxs-lookup"><span data-stu-id="fc9d0-109">Entry</span></span> | <span data-ttu-id="fc9d0-110">Valore</span><span class="sxs-lookup"><span data-stu-id="fc9d0-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="fc9d0-111">CN</span><span class="sxs-lookup"><span data-stu-id="fc9d0-111">CN</span></span>                | <span data-ttu-id="fc9d0-112">Is-Deleted</span><span class="sxs-lookup"><span data-stu-id="fc9d0-112">Is-Deleted</span></span>                           |
| <span data-ttu-id="fc9d0-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="fc9d0-113">Ldap-Display-Name</span></span> | <span data-ttu-id="fc9d0-114">isDeleted</span><span class="sxs-lookup"><span data-stu-id="fc9d0-114">isDeleted</span></span>                            |
| <span data-ttu-id="fc9d0-115">Dimensione</span><span class="sxs-lookup"><span data-stu-id="fc9d0-115">Size</span></span>              | \-                                   |
| <span data-ttu-id="fc9d0-116">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="fc9d0-116">Update Privilege</span></span>  | <span data-ttu-id="fc9d0-117">Amministratore di dominio</span><span class="sxs-lookup"><span data-stu-id="fc9d0-117">Domain administrator</span></span>                 |
| <span data-ttu-id="fc9d0-118">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="fc9d0-118">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="fc9d0-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="fc9d0-119">Attribute-Id</span></span>      | <span data-ttu-id="fc9d0-120">1.2.840.113556.1.2.48</span><span class="sxs-lookup"><span data-stu-id="fc9d0-120">1.2.840.113556.1.2.48</span></span>                |
| <span data-ttu-id="fc9d0-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="fc9d0-121">System-Id-Guid</span></span>    | <span data-ttu-id="fc9d0-122">bf96798f-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="fc9d0-122">bf96798f-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="fc9d0-123">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fc9d0-123">Syntax</span></span>            | [<span data-ttu-id="fc9d0-124">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="fc9d0-124">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="fc9d0-125">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="fc9d0-125">Implementations</span></span>

-   [<span data-ttu-id="fc9d0-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="fc9d0-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="fc9d0-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="fc9d0-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="fc9d0-128">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="fc9d0-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="fc9d0-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="fc9d0-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="fc9d0-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="fc9d0-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="fc9d0-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="fc9d0-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="fc9d0-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="fc9d0-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="fc9d0-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="fc9d0-133">Windows 2000 Server</span></span>



| <span data-ttu-id="fc9d0-134">Voce</span><span class="sxs-lookup"><span data-stu-id="fc9d0-134">Entry</span></span> | <span data-ttu-id="fc9d0-135">Valore</span><span class="sxs-lookup"><span data-stu-id="fc9d0-135">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="fc9d0-136">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="fc9d0-136">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="fc9d0-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fc9d0-137">MAPI-Id</span></span>                | <span data-ttu-id="fc9d0-138">0x80C0</span><span class="sxs-lookup"><span data-stu-id="fc9d0-138">0x80C0</span></span>                          |
| <span data-ttu-id="fc9d0-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="fc9d0-139">System-Only</span></span>            | <span data-ttu-id="fc9d0-140">Vero</span><span class="sxs-lookup"><span data-stu-id="fc9d0-140">True</span></span>                            |
| <span data-ttu-id="fc9d0-141">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="fc9d0-141">Is-Single-Valued</span></span>       | <span data-ttu-id="fc9d0-142">Vero</span><span class="sxs-lookup"><span data-stu-id="fc9d0-142">True</span></span>                            |
| <span data-ttu-id="fc9d0-143">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="fc9d0-143">Is Indexed</span></span>             | <span data-ttu-id="fc9d0-144">Falso</span><span class="sxs-lookup"><span data-stu-id="fc9d0-144">False</span></span>                           |
| <span data-ttu-id="fc9d0-145">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="fc9d0-145">In Global Catalog</span></span>      | <span data-ttu-id="fc9d0-146">Vero</span><span class="sxs-lookup"><span data-stu-id="fc9d0-146">True</span></span>                            |
| <span data-ttu-id="fc9d0-147">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="fc9d0-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="fc9d0-148">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="fc9d0-148">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="fc9d0-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fc9d0-149">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="fc9d0-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fc9d0-150">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="fc9d0-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fc9d0-151">Search-Flags</span></span>           | <span data-ttu-id="fc9d0-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fc9d0-152">0x00000000</span></span>                      |
| <span data-ttu-id="fc9d0-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fc9d0-153">System-Flags</span></span>           | <span data-ttu-id="fc9d0-154">0x00000012</span><span class="sxs-lookup"><span data-stu-id="fc9d0-154">0x00000012</span></span>                      |
| <span data-ttu-id="fc9d0-155">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="fc9d0-155">Classes used in</span></span>        | [<span data-ttu-id="fc9d0-156">**In alto**</span><span class="sxs-lookup"><span data-stu-id="fc9d0-156">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="fc9d0-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="fc9d0-157">Windows Server 2003</span></span>



| <span data-ttu-id="fc9d0-158">Voce</span><span class="sxs-lookup"><span data-stu-id="fc9d0-158">Entry</span></span> | <span data-ttu-id="fc9d0-159">Valore</span><span class="sxs-lookup"><span data-stu-id="fc9d0-159">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="fc9d0-160">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="fc9d0-160">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="fc9d0-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fc9d0-161">MAPI-Id</span></span>                | <span data-ttu-id="fc9d0-162">0x80C0</span><span class="sxs-lookup"><span data-stu-id="fc9d0-162">0x80C0</span></span>                          |
| <span data-ttu-id="fc9d0-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="fc9d0-163">System-Only</span></span>            | <span data-ttu-id="fc9d0-164">Vero</span><span class="sxs-lookup"><span data-stu-id="fc9d0-164">True</span></span>                            |
| <span data-ttu-id="fc9d0-165">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="fc9d0-165">Is-Single-Valued</span></span>       | <span data-ttu-id="fc9d0-166">Vero</span><span class="sxs-lookup"><span data-stu-id="fc9d0-166">True</span></span>                            |
| <span data-ttu-id="fc9d0-167">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="fc9d0-167">Is Indexed</span></span>             | <span data-ttu-id="fc9d0-168">Falso</span><span class="sxs-lookup"><span data-stu-id="fc9d0-168">False</span></span>                           |
| <span data-ttu-id="fc9d0-169">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="fc9d0-169">In Global Catalog</span></span>      | <span data-ttu-id="fc9d0-170">Vero</span><span class="sxs-lookup"><span data-stu-id="fc9d0-170">True</span></span>                            |
| <span data-ttu-id="fc9d0-171">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="fc9d0-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="fc9d0-172">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="fc9d0-172">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="fc9d0-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fc9d0-173">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="fc9d0-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fc9d0-174">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="fc9d0-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fc9d0-175">Search-Flags</span></span>           | <span data-ttu-id="fc9d0-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fc9d0-176">0x00000000</span></span>                      |
| <span data-ttu-id="fc9d0-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fc9d0-177">System-Flags</span></span>           | <span data-ttu-id="fc9d0-178">0x00000012</span><span class="sxs-lookup"><span data-stu-id="fc9d0-178">0x00000012</span></span>                      |
| <span data-ttu-id="fc9d0-179">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="fc9d0-179">Classes used in</span></span>        | [<span data-ttu-id="fc9d0-180">**In alto**</span><span class="sxs-lookup"><span data-stu-id="fc9d0-180">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="fc9d0-181">ADAM</span><span class="sxs-lookup"><span data-stu-id="fc9d0-181">ADAM</span></span>



| <span data-ttu-id="fc9d0-182">Voce</span><span class="sxs-lookup"><span data-stu-id="fc9d0-182">Entry</span></span> | <span data-ttu-id="fc9d0-183">Valore</span><span class="sxs-lookup"><span data-stu-id="fc9d0-183">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="fc9d0-184">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="fc9d0-184">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="fc9d0-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fc9d0-185">MAPI-Id</span></span>                | <span data-ttu-id="fc9d0-186">0x80C0</span><span class="sxs-lookup"><span data-stu-id="fc9d0-186">0x80C0</span></span>                          |
| <span data-ttu-id="fc9d0-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="fc9d0-187">System-Only</span></span>            | <span data-ttu-id="fc9d0-188">Vero</span><span class="sxs-lookup"><span data-stu-id="fc9d0-188">True</span></span>                            |
| <span data-ttu-id="fc9d0-189">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="fc9d0-189">Is-Single-Valued</span></span>       | <span data-ttu-id="fc9d0-190">Vero</span><span class="sxs-lookup"><span data-stu-id="fc9d0-190">True</span></span>                            |
| <span data-ttu-id="fc9d0-191">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="fc9d0-191">Is Indexed</span></span>             | <span data-ttu-id="fc9d0-192">Falso</span><span class="sxs-lookup"><span data-stu-id="fc9d0-192">False</span></span>                           |
| <span data-ttu-id="fc9d0-193">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="fc9d0-193">In Global Catalog</span></span>      | <span data-ttu-id="fc9d0-194">Vero</span><span class="sxs-lookup"><span data-stu-id="fc9d0-194">True</span></span>                            |
| <span data-ttu-id="fc9d0-195">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="fc9d0-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="fc9d0-196">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="fc9d0-196">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="fc9d0-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fc9d0-197">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="fc9d0-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fc9d0-198">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="fc9d0-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fc9d0-199">Search-Flags</span></span>           | <span data-ttu-id="fc9d0-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fc9d0-200">0x00000000</span></span>                      |
| <span data-ttu-id="fc9d0-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fc9d0-201">System-Flags</span></span>           | <span data-ttu-id="fc9d0-202">0x00000012</span><span class="sxs-lookup"><span data-stu-id="fc9d0-202">0x00000012</span></span>                      |
| <span data-ttu-id="fc9d0-203">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="fc9d0-203">Classes used in</span></span>        | [<span data-ttu-id="fc9d0-204">**In alto**</span><span class="sxs-lookup"><span data-stu-id="fc9d0-204">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="fc9d0-205">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="fc9d0-205">Windows Server 2003 R2</span></span>



| <span data-ttu-id="fc9d0-206">Voce</span><span class="sxs-lookup"><span data-stu-id="fc9d0-206">Entry</span></span> | <span data-ttu-id="fc9d0-207">Valore</span><span class="sxs-lookup"><span data-stu-id="fc9d0-207">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="fc9d0-208">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="fc9d0-208">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="fc9d0-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fc9d0-209">MAPI-Id</span></span>                | <span data-ttu-id="fc9d0-210">0x80C0</span><span class="sxs-lookup"><span data-stu-id="fc9d0-210">0x80C0</span></span>                          |
| <span data-ttu-id="fc9d0-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="fc9d0-211">System-Only</span></span>            | <span data-ttu-id="fc9d0-212">Vero</span><span class="sxs-lookup"><span data-stu-id="fc9d0-212">True</span></span>                            |
| <span data-ttu-id="fc9d0-213">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="fc9d0-213">Is-Single-Valued</span></span>       | <span data-ttu-id="fc9d0-214">Vero</span><span class="sxs-lookup"><span data-stu-id="fc9d0-214">True</span></span>                            |
| <span data-ttu-id="fc9d0-215">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="fc9d0-215">Is Indexed</span></span>             | <span data-ttu-id="fc9d0-216">Falso</span><span class="sxs-lookup"><span data-stu-id="fc9d0-216">False</span></span>                           |
| <span data-ttu-id="fc9d0-217">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="fc9d0-217">In Global Catalog</span></span>      | <span data-ttu-id="fc9d0-218">Vero</span><span class="sxs-lookup"><span data-stu-id="fc9d0-218">True</span></span>                            |
| <span data-ttu-id="fc9d0-219">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="fc9d0-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="fc9d0-220">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="fc9d0-220">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="fc9d0-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fc9d0-221">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="fc9d0-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fc9d0-222">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="fc9d0-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fc9d0-223">Search-Flags</span></span>           | <span data-ttu-id="fc9d0-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fc9d0-224">0x00000000</span></span>                      |
| <span data-ttu-id="fc9d0-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fc9d0-225">System-Flags</span></span>           | <span data-ttu-id="fc9d0-226">0x00000012</span><span class="sxs-lookup"><span data-stu-id="fc9d0-226">0x00000012</span></span>                      |
| <span data-ttu-id="fc9d0-227">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="fc9d0-227">Classes used in</span></span>        | [<span data-ttu-id="fc9d0-228">**In alto**</span><span class="sxs-lookup"><span data-stu-id="fc9d0-228">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="fc9d0-229">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fc9d0-229">Windows Server 2008</span></span>



| <span data-ttu-id="fc9d0-230">Voce</span><span class="sxs-lookup"><span data-stu-id="fc9d0-230">Entry</span></span> | <span data-ttu-id="fc9d0-231">Valore</span><span class="sxs-lookup"><span data-stu-id="fc9d0-231">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="fc9d0-232">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="fc9d0-232">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="fc9d0-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fc9d0-233">MAPI-Id</span></span>                | <span data-ttu-id="fc9d0-234">0x80C0</span><span class="sxs-lookup"><span data-stu-id="fc9d0-234">0x80C0</span></span>                          |
| <span data-ttu-id="fc9d0-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="fc9d0-235">System-Only</span></span>            | <span data-ttu-id="fc9d0-236">Vero</span><span class="sxs-lookup"><span data-stu-id="fc9d0-236">True</span></span>                            |
| <span data-ttu-id="fc9d0-237">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="fc9d0-237">Is-Single-Valued</span></span>       | <span data-ttu-id="fc9d0-238">Vero</span><span class="sxs-lookup"><span data-stu-id="fc9d0-238">True</span></span>                            |
| <span data-ttu-id="fc9d0-239">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="fc9d0-239">Is Indexed</span></span>             | <span data-ttu-id="fc9d0-240">Falso</span><span class="sxs-lookup"><span data-stu-id="fc9d0-240">False</span></span>                           |
| <span data-ttu-id="fc9d0-241">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="fc9d0-241">In Global Catalog</span></span>      | <span data-ttu-id="fc9d0-242">Vero</span><span class="sxs-lookup"><span data-stu-id="fc9d0-242">True</span></span>                            |
| <span data-ttu-id="fc9d0-243">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="fc9d0-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="fc9d0-244">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="fc9d0-244">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="fc9d0-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fc9d0-245">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="fc9d0-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fc9d0-246">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="fc9d0-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fc9d0-247">Search-Flags</span></span>           | <span data-ttu-id="fc9d0-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fc9d0-248">0x00000000</span></span>                      |
| <span data-ttu-id="fc9d0-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fc9d0-249">System-Flags</span></span>           | <span data-ttu-id="fc9d0-250">0x00000012</span><span class="sxs-lookup"><span data-stu-id="fc9d0-250">0x00000012</span></span>                      |
| <span data-ttu-id="fc9d0-251">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="fc9d0-251">Classes used in</span></span>        | [<span data-ttu-id="fc9d0-252">**In alto**</span><span class="sxs-lookup"><span data-stu-id="fc9d0-252">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="fc9d0-253">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="fc9d0-253">Windows Server 2008 R2</span></span>



| <span data-ttu-id="fc9d0-254">Voce</span><span class="sxs-lookup"><span data-stu-id="fc9d0-254">Entry</span></span> | <span data-ttu-id="fc9d0-255">Valore</span><span class="sxs-lookup"><span data-stu-id="fc9d0-255">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="fc9d0-256">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="fc9d0-256">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="fc9d0-257">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fc9d0-257">MAPI-Id</span></span>                | <span data-ttu-id="fc9d0-258">0x80C0</span><span class="sxs-lookup"><span data-stu-id="fc9d0-258">0x80C0</span></span>                          |
| <span data-ttu-id="fc9d0-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="fc9d0-259">System-Only</span></span>            | <span data-ttu-id="fc9d0-260">Vero</span><span class="sxs-lookup"><span data-stu-id="fc9d0-260">True</span></span>                            |
| <span data-ttu-id="fc9d0-261">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="fc9d0-261">Is-Single-Valued</span></span>       | <span data-ttu-id="fc9d0-262">Vero</span><span class="sxs-lookup"><span data-stu-id="fc9d0-262">True</span></span>                            |
| <span data-ttu-id="fc9d0-263">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="fc9d0-263">Is Indexed</span></span>             | <span data-ttu-id="fc9d0-264">Falso</span><span class="sxs-lookup"><span data-stu-id="fc9d0-264">False</span></span>                           |
| <span data-ttu-id="fc9d0-265">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="fc9d0-265">In Global Catalog</span></span>      | <span data-ttu-id="fc9d0-266">Vero</span><span class="sxs-lookup"><span data-stu-id="fc9d0-266">True</span></span>                            |
| <span data-ttu-id="fc9d0-267">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="fc9d0-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="fc9d0-268">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="fc9d0-268">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="fc9d0-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fc9d0-269">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="fc9d0-270">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fc9d0-270">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="fc9d0-271">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fc9d0-271">Search-Flags</span></span>           | <span data-ttu-id="fc9d0-272">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fc9d0-272">0x00000000</span></span>                      |
| <span data-ttu-id="fc9d0-273">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fc9d0-273">System-Flags</span></span>           | <span data-ttu-id="fc9d0-274">0x00000012</span><span class="sxs-lookup"><span data-stu-id="fc9d0-274">0x00000012</span></span>                      |
| <span data-ttu-id="fc9d0-275">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="fc9d0-275">Classes used in</span></span>        | [<span data-ttu-id="fc9d0-276">**In alto**</span><span class="sxs-lookup"><span data-stu-id="fc9d0-276">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="fc9d0-277">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="fc9d0-277">Windows Server 2012</span></span>



| <span data-ttu-id="fc9d0-278">Voce</span><span class="sxs-lookup"><span data-stu-id="fc9d0-278">Entry</span></span> | <span data-ttu-id="fc9d0-279">Valore</span><span class="sxs-lookup"><span data-stu-id="fc9d0-279">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="fc9d0-280">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="fc9d0-280">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="fc9d0-281">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fc9d0-281">MAPI-Id</span></span>                | <span data-ttu-id="fc9d0-282">0x80C0</span><span class="sxs-lookup"><span data-stu-id="fc9d0-282">0x80C0</span></span>                          |
| <span data-ttu-id="fc9d0-283">System-Only</span><span class="sxs-lookup"><span data-stu-id="fc9d0-283">System-Only</span></span>            | <span data-ttu-id="fc9d0-284">Vero</span><span class="sxs-lookup"><span data-stu-id="fc9d0-284">True</span></span>                            |
| <span data-ttu-id="fc9d0-285">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="fc9d0-285">Is-Single-Valued</span></span>       | <span data-ttu-id="fc9d0-286">Vero</span><span class="sxs-lookup"><span data-stu-id="fc9d0-286">True</span></span>                            |
| <span data-ttu-id="fc9d0-287">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="fc9d0-287">Is Indexed</span></span>             | <span data-ttu-id="fc9d0-288">Falso</span><span class="sxs-lookup"><span data-stu-id="fc9d0-288">False</span></span>                           |
| <span data-ttu-id="fc9d0-289">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="fc9d0-289">In Global Catalog</span></span>      | <span data-ttu-id="fc9d0-290">Vero</span><span class="sxs-lookup"><span data-stu-id="fc9d0-290">True</span></span>                            |
| <span data-ttu-id="fc9d0-291">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="fc9d0-291">NT-Security-Descriptor</span></span> | <span data-ttu-id="fc9d0-292">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="fc9d0-292">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="fc9d0-293">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fc9d0-293">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="fc9d0-294">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fc9d0-294">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="fc9d0-295">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fc9d0-295">Search-Flags</span></span>           | <span data-ttu-id="fc9d0-296">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fc9d0-296">0x00000000</span></span>                      |
| <span data-ttu-id="fc9d0-297">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fc9d0-297">System-Flags</span></span>           | <span data-ttu-id="fc9d0-298">0x00000012</span><span class="sxs-lookup"><span data-stu-id="fc9d0-298">0x00000012</span></span>                      |
| <span data-ttu-id="fc9d0-299">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="fc9d0-299">Classes used in</span></span>        | [<span data-ttu-id="fc9d0-300">**In alto**</span><span class="sxs-lookup"><span data-stu-id="fc9d0-300">**Top**</span></span>](c-top.md)<br/> |



 

 





