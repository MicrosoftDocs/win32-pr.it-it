---
title: Attributo Max-Storage
description: Quantità massima di spazio su disco che l'utente può utilizzare. Usare il valore specificato in USER \_ MAXSTORAGE \_ Unlimited per usare tutto lo spazio disponibile su disco.
ms.assetid: 69302641-ecfc-4b0f-81f8-f69b48c6faa7
ms.tgt_platform: multiple
keywords:
- Schema AD Max-Storage attribute
- Schema AD dell'attributo maxStorage
topic_type:
- apiref
api_name:
- Max-Storage
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac6caff3f85de7073818096324445b63a3c1c9be
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103875450"
---
# <a name="max-storage-attribute"></a><span data-ttu-id="fe8a4-106">Attributo Max-Storage</span><span class="sxs-lookup"><span data-stu-id="fe8a4-106">Max-Storage attribute</span></span>

<span data-ttu-id="fe8a4-107">Quantità massima di spazio su disco che l'utente può utilizzare.</span><span class="sxs-lookup"><span data-stu-id="fe8a4-107">The maximum amount of disk space the user can use.</span></span> <span data-ttu-id="fe8a4-108">Usare il valore specificato in USER \_ MAXSTORAGE \_ Unlimited per usare tutto lo spazio disponibile su disco.</span><span class="sxs-lookup"><span data-stu-id="fe8a4-108">Use the value specified in USER\_MAXSTORAGE\_UNLIMITED to use all available disk space.</span></span>



| <span data-ttu-id="fe8a4-109">Voce</span><span class="sxs-lookup"><span data-stu-id="fe8a4-109">Entry</span></span> | <span data-ttu-id="fe8a4-110">Valore</span><span class="sxs-lookup"><span data-stu-id="fe8a4-110">Value</span></span> |
|-------------------|------------------------------------------------------------|
| <span data-ttu-id="fe8a4-111">CN</span><span class="sxs-lookup"><span data-stu-id="fe8a4-111">CN</span></span>                | <span data-ttu-id="fe8a4-112">Max-Storage</span><span class="sxs-lookup"><span data-stu-id="fe8a4-112">Max-Storage</span></span>                                                |
| <span data-ttu-id="fe8a4-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="fe8a4-113">Ldap-Display-Name</span></span> | <span data-ttu-id="fe8a4-114">maxStorage</span><span class="sxs-lookup"><span data-stu-id="fe8a4-114">maxStorage</span></span>                                                 |
| <span data-ttu-id="fe8a4-115">Dimensione</span><span class="sxs-lookup"><span data-stu-id="fe8a4-115">Size</span></span>              | <span data-ttu-id="fe8a4-116">8 byte: utente \_ MAXSTORAGE \_ illimitato ((unsigned long)-1L)</span><span class="sxs-lookup"><span data-stu-id="fe8a4-116">8 bytes: USER\_MAXSTORAGE\_UNLIMITED ((unsigned long) -1L)</span></span> |
| <span data-ttu-id="fe8a4-117">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="fe8a4-117">Update Privilege</span></span>  | <span data-ttu-id="fe8a4-118">Amministratore di dominio</span><span class="sxs-lookup"><span data-stu-id="fe8a4-118">Domain administrator</span></span>                                       |
| <span data-ttu-id="fe8a4-119">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="fe8a4-119">Update Frequency</span></span>  | <span data-ttu-id="fe8a4-120">Ogni volta che è necessario modificare la quota del disco.</span><span class="sxs-lookup"><span data-stu-id="fe8a4-120">Whenever the disk quota needs to change.</span></span>                   |
| <span data-ttu-id="fe8a4-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="fe8a4-121">Attribute-Id</span></span>      | <span data-ttu-id="fe8a4-122">1.2.840.113556.1.4.76</span><span class="sxs-lookup"><span data-stu-id="fe8a4-122">1.2.840.113556.1.4.76</span></span>                                      |
| <span data-ttu-id="fe8a4-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="fe8a4-123">System-Id-Guid</span></span>    | <span data-ttu-id="fe8a4-124">bf9679bd-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="fe8a4-124">bf9679bd-0de6-11d0-a285-00aa003049e2</span></span>                       |
| <span data-ttu-id="fe8a4-125">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fe8a4-125">Syntax</span></span>            | [<span data-ttu-id="fe8a4-126">**Interval**</span><span class="sxs-lookup"><span data-stu-id="fe8a4-126">**Interval**</span></span>](s-interval.md)                             |



## <a name="implementations"></a><span data-ttu-id="fe8a4-127">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="fe8a4-127">Implementations</span></span>

-   [<span data-ttu-id="fe8a4-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="fe8a4-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="fe8a4-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="fe8a4-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="fe8a4-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="fe8a4-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="fe8a4-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="fe8a4-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="fe8a4-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="fe8a4-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="fe8a4-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="fe8a4-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="fe8a4-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="fe8a4-134">Windows 2000 Server</span></span>



| <span data-ttu-id="fe8a4-135">Voce</span><span class="sxs-lookup"><span data-stu-id="fe8a4-135">Entry</span></span> | <span data-ttu-id="fe8a4-136">Valore</span><span class="sxs-lookup"><span data-stu-id="fe8a4-136">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="fe8a4-137">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="fe8a4-137">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="fe8a4-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fe8a4-138">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="fe8a4-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="fe8a4-139">System-Only</span></span>            | <span data-ttu-id="fe8a4-140">Falso</span><span class="sxs-lookup"><span data-stu-id="fe8a4-140">False</span></span>                             |
| <span data-ttu-id="fe8a4-141">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="fe8a4-141">Is-Single-Valued</span></span>       | <span data-ttu-id="fe8a4-142">Vero</span><span class="sxs-lookup"><span data-stu-id="fe8a4-142">True</span></span>                              |
| <span data-ttu-id="fe8a4-143">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="fe8a4-143">Is Indexed</span></span>             | <span data-ttu-id="fe8a4-144">Falso</span><span class="sxs-lookup"><span data-stu-id="fe8a4-144">False</span></span>                             |
| <span data-ttu-id="fe8a4-145">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="fe8a4-145">In Global Catalog</span></span>      | <span data-ttu-id="fe8a4-146">Falso</span><span class="sxs-lookup"><span data-stu-id="fe8a4-146">False</span></span>                             |
| <span data-ttu-id="fe8a4-147">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="fe8a4-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="fe8a4-148">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="fe8a4-148">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="fe8a4-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fe8a4-149">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="fe8a4-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fe8a4-150">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="fe8a4-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fe8a4-151">Search-Flags</span></span>           | <span data-ttu-id="fe8a4-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fe8a4-152">0x00000010</span></span>                        |
| <span data-ttu-id="fe8a4-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fe8a4-153">System-Flags</span></span>           | <span data-ttu-id="fe8a4-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fe8a4-154">0x00000010</span></span>                        |
| <span data-ttu-id="fe8a4-155">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="fe8a4-155">Classes used in</span></span>        | [<span data-ttu-id="fe8a4-156">**Utente**</span><span class="sxs-lookup"><span data-stu-id="fe8a4-156">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="fe8a4-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="fe8a4-157">Windows Server 2003</span></span>



| <span data-ttu-id="fe8a4-158">Voce</span><span class="sxs-lookup"><span data-stu-id="fe8a4-158">Entry</span></span> | <span data-ttu-id="fe8a4-159">Valore</span><span class="sxs-lookup"><span data-stu-id="fe8a4-159">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="fe8a4-160">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="fe8a4-160">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="fe8a4-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fe8a4-161">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="fe8a4-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="fe8a4-162">System-Only</span></span>            | <span data-ttu-id="fe8a4-163">Falso</span><span class="sxs-lookup"><span data-stu-id="fe8a4-163">False</span></span>                             |
| <span data-ttu-id="fe8a4-164">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="fe8a4-164">Is-Single-Valued</span></span>       | <span data-ttu-id="fe8a4-165">Vero</span><span class="sxs-lookup"><span data-stu-id="fe8a4-165">True</span></span>                              |
| <span data-ttu-id="fe8a4-166">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="fe8a4-166">Is Indexed</span></span>             | <span data-ttu-id="fe8a4-167">Falso</span><span class="sxs-lookup"><span data-stu-id="fe8a4-167">False</span></span>                             |
| <span data-ttu-id="fe8a4-168">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="fe8a4-168">In Global Catalog</span></span>      | <span data-ttu-id="fe8a4-169">Falso</span><span class="sxs-lookup"><span data-stu-id="fe8a4-169">False</span></span>                             |
| <span data-ttu-id="fe8a4-170">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="fe8a4-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="fe8a4-171">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="fe8a4-171">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="fe8a4-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fe8a4-172">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="fe8a4-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fe8a4-173">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="fe8a4-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fe8a4-174">Search-Flags</span></span>           | <span data-ttu-id="fe8a4-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fe8a4-175">0x00000010</span></span>                        |
| <span data-ttu-id="fe8a4-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fe8a4-176">System-Flags</span></span>           | <span data-ttu-id="fe8a4-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fe8a4-177">0x00000010</span></span>                        |
| <span data-ttu-id="fe8a4-178">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="fe8a4-178">Classes used in</span></span>        | [<span data-ttu-id="fe8a4-179">**Utente**</span><span class="sxs-lookup"><span data-stu-id="fe8a4-179">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="fe8a4-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="fe8a4-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="fe8a4-181">Voce</span><span class="sxs-lookup"><span data-stu-id="fe8a4-181">Entry</span></span> | <span data-ttu-id="fe8a4-182">Valore</span><span class="sxs-lookup"><span data-stu-id="fe8a4-182">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="fe8a4-183">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="fe8a4-183">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="fe8a4-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fe8a4-184">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="fe8a4-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="fe8a4-185">System-Only</span></span>            | <span data-ttu-id="fe8a4-186">Falso</span><span class="sxs-lookup"><span data-stu-id="fe8a4-186">False</span></span>                             |
| <span data-ttu-id="fe8a4-187">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="fe8a4-187">Is-Single-Valued</span></span>       | <span data-ttu-id="fe8a4-188">Vero</span><span class="sxs-lookup"><span data-stu-id="fe8a4-188">True</span></span>                              |
| <span data-ttu-id="fe8a4-189">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="fe8a4-189">Is Indexed</span></span>             | <span data-ttu-id="fe8a4-190">Falso</span><span class="sxs-lookup"><span data-stu-id="fe8a4-190">False</span></span>                             |
| <span data-ttu-id="fe8a4-191">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="fe8a4-191">In Global Catalog</span></span>      | <span data-ttu-id="fe8a4-192">Falso</span><span class="sxs-lookup"><span data-stu-id="fe8a4-192">False</span></span>                             |
| <span data-ttu-id="fe8a4-193">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="fe8a4-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="fe8a4-194">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="fe8a4-194">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="fe8a4-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fe8a4-195">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="fe8a4-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fe8a4-196">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="fe8a4-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fe8a4-197">Search-Flags</span></span>           | <span data-ttu-id="fe8a4-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fe8a4-198">0x00000010</span></span>                        |
| <span data-ttu-id="fe8a4-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fe8a4-199">System-Flags</span></span>           | <span data-ttu-id="fe8a4-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fe8a4-200">0x00000010</span></span>                        |
| <span data-ttu-id="fe8a4-201">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="fe8a4-201">Classes used in</span></span>        | [<span data-ttu-id="fe8a4-202">**Utente**</span><span class="sxs-lookup"><span data-stu-id="fe8a4-202">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="fe8a4-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fe8a4-203">Windows Server 2008</span></span>



| <span data-ttu-id="fe8a4-204">Voce</span><span class="sxs-lookup"><span data-stu-id="fe8a4-204">Entry</span></span> | <span data-ttu-id="fe8a4-205">Valore</span><span class="sxs-lookup"><span data-stu-id="fe8a4-205">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="fe8a4-206">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="fe8a4-206">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="fe8a4-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fe8a4-207">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="fe8a4-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="fe8a4-208">System-Only</span></span>            | <span data-ttu-id="fe8a4-209">Falso</span><span class="sxs-lookup"><span data-stu-id="fe8a4-209">False</span></span>                             |
| <span data-ttu-id="fe8a4-210">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="fe8a4-210">Is-Single-Valued</span></span>       | <span data-ttu-id="fe8a4-211">Vero</span><span class="sxs-lookup"><span data-stu-id="fe8a4-211">True</span></span>                              |
| <span data-ttu-id="fe8a4-212">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="fe8a4-212">Is Indexed</span></span>             | <span data-ttu-id="fe8a4-213">Falso</span><span class="sxs-lookup"><span data-stu-id="fe8a4-213">False</span></span>                             |
| <span data-ttu-id="fe8a4-214">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="fe8a4-214">In Global Catalog</span></span>      | <span data-ttu-id="fe8a4-215">Falso</span><span class="sxs-lookup"><span data-stu-id="fe8a4-215">False</span></span>                             |
| <span data-ttu-id="fe8a4-216">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="fe8a4-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="fe8a4-217">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="fe8a4-217">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="fe8a4-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fe8a4-218">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="fe8a4-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fe8a4-219">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="fe8a4-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fe8a4-220">Search-Flags</span></span>           | <span data-ttu-id="fe8a4-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fe8a4-221">0x00000010</span></span>                        |
| <span data-ttu-id="fe8a4-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fe8a4-222">System-Flags</span></span>           | <span data-ttu-id="fe8a4-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fe8a4-223">0x00000010</span></span>                        |
| <span data-ttu-id="fe8a4-224">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="fe8a4-224">Classes used in</span></span>        | [<span data-ttu-id="fe8a4-225">**Utente**</span><span class="sxs-lookup"><span data-stu-id="fe8a4-225">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="fe8a4-226">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="fe8a4-226">Windows Server 2008 R2</span></span>



| <span data-ttu-id="fe8a4-227">Voce</span><span class="sxs-lookup"><span data-stu-id="fe8a4-227">Entry</span></span> | <span data-ttu-id="fe8a4-228">Valore</span><span class="sxs-lookup"><span data-stu-id="fe8a4-228">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="fe8a4-229">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="fe8a4-229">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="fe8a4-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fe8a4-230">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="fe8a4-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="fe8a4-231">System-Only</span></span>            | <span data-ttu-id="fe8a4-232">Falso</span><span class="sxs-lookup"><span data-stu-id="fe8a4-232">False</span></span>                             |
| <span data-ttu-id="fe8a4-233">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="fe8a4-233">Is-Single-Valued</span></span>       | <span data-ttu-id="fe8a4-234">Vero</span><span class="sxs-lookup"><span data-stu-id="fe8a4-234">True</span></span>                              |
| <span data-ttu-id="fe8a4-235">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="fe8a4-235">Is Indexed</span></span>             | <span data-ttu-id="fe8a4-236">Falso</span><span class="sxs-lookup"><span data-stu-id="fe8a4-236">False</span></span>                             |
| <span data-ttu-id="fe8a4-237">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="fe8a4-237">In Global Catalog</span></span>      | <span data-ttu-id="fe8a4-238">Falso</span><span class="sxs-lookup"><span data-stu-id="fe8a4-238">False</span></span>                             |
| <span data-ttu-id="fe8a4-239">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="fe8a4-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="fe8a4-240">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="fe8a4-240">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="fe8a4-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fe8a4-241">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="fe8a4-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fe8a4-242">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="fe8a4-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fe8a4-243">Search-Flags</span></span>           | <span data-ttu-id="fe8a4-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fe8a4-244">0x00000010</span></span>                        |
| <span data-ttu-id="fe8a4-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fe8a4-245">System-Flags</span></span>           | <span data-ttu-id="fe8a4-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fe8a4-246">0x00000010</span></span>                        |
| <span data-ttu-id="fe8a4-247">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="fe8a4-247">Classes used in</span></span>        | [<span data-ttu-id="fe8a4-248">**Utente**</span><span class="sxs-lookup"><span data-stu-id="fe8a4-248">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="fe8a4-249">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="fe8a4-249">Windows Server 2012</span></span>



| <span data-ttu-id="fe8a4-250">Voce</span><span class="sxs-lookup"><span data-stu-id="fe8a4-250">Entry</span></span> | <span data-ttu-id="fe8a4-251">Valore</span><span class="sxs-lookup"><span data-stu-id="fe8a4-251">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="fe8a4-252">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="fe8a4-252">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="fe8a4-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fe8a4-253">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="fe8a4-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="fe8a4-254">System-Only</span></span>            | <span data-ttu-id="fe8a4-255">Falso</span><span class="sxs-lookup"><span data-stu-id="fe8a4-255">False</span></span>                             |
| <span data-ttu-id="fe8a4-256">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="fe8a4-256">Is-Single-Valued</span></span>       | <span data-ttu-id="fe8a4-257">Vero</span><span class="sxs-lookup"><span data-stu-id="fe8a4-257">True</span></span>                              |
| <span data-ttu-id="fe8a4-258">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="fe8a4-258">Is Indexed</span></span>             | <span data-ttu-id="fe8a4-259">Falso</span><span class="sxs-lookup"><span data-stu-id="fe8a4-259">False</span></span>                             |
| <span data-ttu-id="fe8a4-260">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="fe8a4-260">In Global Catalog</span></span>      | <span data-ttu-id="fe8a4-261">Falso</span><span class="sxs-lookup"><span data-stu-id="fe8a4-261">False</span></span>                             |
| <span data-ttu-id="fe8a4-262">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="fe8a4-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="fe8a4-263">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="fe8a4-263">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="fe8a4-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fe8a4-264">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="fe8a4-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fe8a4-265">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="fe8a4-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fe8a4-266">Search-Flags</span></span>           | <span data-ttu-id="fe8a4-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fe8a4-267">0x00000010</span></span>                        |
| <span data-ttu-id="fe8a4-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fe8a4-268">System-Flags</span></span>           | <span data-ttu-id="fe8a4-269">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fe8a4-269">0x00000010</span></span>                        |
| <span data-ttu-id="fe8a4-270">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="fe8a4-270">Classes used in</span></span>        | [<span data-ttu-id="fe8a4-271">**Utente**</span><span class="sxs-lookup"><span data-stu-id="fe8a4-271">**User**</span></span>](c-user.md)<br/> |



 

 





