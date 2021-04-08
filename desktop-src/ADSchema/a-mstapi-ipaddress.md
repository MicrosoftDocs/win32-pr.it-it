---
title: attributo ms-TAPI-IP-Address
description: Indirizzi IP di un computer client TAPI a cui è connesso un utente. Questo attributo può essere utilizzato come attributo generico per contenere gli indirizzi IP del computer.
ms.assetid: 4ea850ad-d54a-4b5f-a37d-68817432d874
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo ms-TAPI-IP-Address
- msTAPI-schema AD dell'attributo IpAddress
topic_type:
- apiref
api_name:
- ms-TAPI-Ip-Address
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 078afde8200468df7e996e096deeef4bfd1b7ec0
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103965235"
---
# <a name="ms-tapi-ip-address-attribute"></a><span data-ttu-id="dd239-106">attributo ms-TAPI-IP-Address</span><span class="sxs-lookup"><span data-stu-id="dd239-106">ms-TAPI-Ip-Address attribute</span></span>

<span data-ttu-id="dd239-107">Indirizzi IP di un computer client TAPI a cui è connesso un utente.</span><span class="sxs-lookup"><span data-stu-id="dd239-107">IP addresses of a TAPI client computer that a user is logged into.</span></span> <span data-ttu-id="dd239-108">Questo attributo può essere utilizzato come attributo generico per contenere gli indirizzi IP del computer.</span><span class="sxs-lookup"><span data-stu-id="dd239-108">This attribute can be used as a generic attribute to hold computer IP addresses.</span></span>



| <span data-ttu-id="dd239-109">Voce</span><span class="sxs-lookup"><span data-stu-id="dd239-109">Entry</span></span> | <span data-ttu-id="dd239-110">Valore</span><span class="sxs-lookup"><span data-stu-id="dd239-110">Value</span></span> |
|-------------------|------------------------------------------------------------|
| <span data-ttu-id="dd239-111">CN</span><span class="sxs-lookup"><span data-stu-id="dd239-111">CN</span></span>                | <span data-ttu-id="dd239-112">MS-TAPI-IP-Address</span><span class="sxs-lookup"><span data-stu-id="dd239-112">ms-TAPI-Ip-Address</span></span>                                         |
| <span data-ttu-id="dd239-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="dd239-113">Ldap-Display-Name</span></span> | <span data-ttu-id="dd239-114">msTAPI-IpAddress</span><span class="sxs-lookup"><span data-stu-id="dd239-114">msTAPI-IpAddress</span></span>                                           |
| <span data-ttu-id="dd239-115">Dimensione</span><span class="sxs-lookup"><span data-stu-id="dd239-115">Size</span></span>              | <span data-ttu-id="dd239-116">Ogni indirizzo IP viene archiviato come stringa in una notazione. B. C. D.</span><span class="sxs-lookup"><span data-stu-id="dd239-116">Each IP address is stored as a string in A.B.C.D notation.</span></span> |
| <span data-ttu-id="dd239-117">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="dd239-117">Update Privilege</span></span>  | <span data-ttu-id="dd239-118">Non sono richiesti privilegi speciali.</span><span class="sxs-lookup"><span data-stu-id="dd239-118">No special privileges required.</span></span>                            |
| <span data-ttu-id="dd239-119">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="dd239-119">Update Frequency</span></span>  | <span data-ttu-id="dd239-120">In genere molto bassa.</span><span class="sxs-lookup"><span data-stu-id="dd239-120">Typically very low.</span></span>                                        |
| <span data-ttu-id="dd239-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="dd239-121">Attribute-Id</span></span>      | <span data-ttu-id="dd239-122">1.2.840.113556.1.4.1701</span><span class="sxs-lookup"><span data-stu-id="dd239-122">1.2.840.113556.1.4.1701</span></span>                                    |
| <span data-ttu-id="dd239-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="dd239-123">System-Id-Guid</span></span>    | <span data-ttu-id="dd239-124">efd7d7f7-178e-4767-87fa-f8a16b840544</span><span class="sxs-lookup"><span data-stu-id="dd239-124">efd7d7f7-178e-4767-87fa-f8a16b840544</span></span>                       |
| <span data-ttu-id="dd239-125">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dd239-125">Syntax</span></span>            | [<span data-ttu-id="dd239-126">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="dd239-126">**String(Unicode)**</span></span>](s-string-unicode.md)                |



## <a name="implementations"></a><span data-ttu-id="dd239-127">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="dd239-127">Implementations</span></span>

-   [<span data-ttu-id="dd239-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="dd239-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="dd239-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="dd239-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="dd239-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="dd239-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="dd239-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="dd239-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="dd239-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="dd239-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="dd239-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="dd239-133">Windows Server 2003</span></span>



| <span data-ttu-id="dd239-134">Voce</span><span class="sxs-lookup"><span data-stu-id="dd239-134">Entry</span></span> | <span data-ttu-id="dd239-135">Valore</span><span class="sxs-lookup"><span data-stu-id="dd239-135">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="dd239-136">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="dd239-136">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="dd239-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dd239-137">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="dd239-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="dd239-138">System-Only</span></span>            | <span data-ttu-id="dd239-139">Falso</span><span class="sxs-lookup"><span data-stu-id="dd239-139">False</span></span>                                                     |
| <span data-ttu-id="dd239-140">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="dd239-140">Is-Single-Valued</span></span>       | <span data-ttu-id="dd239-141">Falso</span><span class="sxs-lookup"><span data-stu-id="dd239-141">False</span></span>                                                     |
| <span data-ttu-id="dd239-142">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="dd239-142">Is Indexed</span></span>             | <span data-ttu-id="dd239-143">Falso</span><span class="sxs-lookup"><span data-stu-id="dd239-143">False</span></span>                                                     |
| <span data-ttu-id="dd239-144">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="dd239-144">In Global Catalog</span></span>      | <span data-ttu-id="dd239-145">Falso</span><span class="sxs-lookup"><span data-stu-id="dd239-145">False</span></span>                                                     |
| <span data-ttu-id="dd239-146">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="dd239-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="dd239-147">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="dd239-147">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="dd239-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dd239-148">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="dd239-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dd239-149">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="dd239-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dd239-150">Search-Flags</span></span>           | <span data-ttu-id="dd239-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dd239-151">0x00000000</span></span>                                                |
| <span data-ttu-id="dd239-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dd239-152">System-Flags</span></span>           | <span data-ttu-id="dd239-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dd239-153">0x00000010</span></span>                                                |
| <span data-ttu-id="dd239-154">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="dd239-154">Classes used in</span></span>        | [<span data-ttu-id="dd239-155">**MS-TAPI-RT-person**</span><span class="sxs-lookup"><span data-stu-id="dd239-155">**ms-TAPI-Rt-Person**</span></span>](c-mstapi-rtperson.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="dd239-156">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="dd239-156">Windows Server 2003 R2</span></span>



| <span data-ttu-id="dd239-157">Voce</span><span class="sxs-lookup"><span data-stu-id="dd239-157">Entry</span></span> | <span data-ttu-id="dd239-158">Valore</span><span class="sxs-lookup"><span data-stu-id="dd239-158">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="dd239-159">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="dd239-159">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="dd239-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dd239-160">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="dd239-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="dd239-161">System-Only</span></span>            | <span data-ttu-id="dd239-162">Falso</span><span class="sxs-lookup"><span data-stu-id="dd239-162">False</span></span>                                                     |
| <span data-ttu-id="dd239-163">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="dd239-163">Is-Single-Valued</span></span>       | <span data-ttu-id="dd239-164">Falso</span><span class="sxs-lookup"><span data-stu-id="dd239-164">False</span></span>                                                     |
| <span data-ttu-id="dd239-165">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="dd239-165">Is Indexed</span></span>             | <span data-ttu-id="dd239-166">Falso</span><span class="sxs-lookup"><span data-stu-id="dd239-166">False</span></span>                                                     |
| <span data-ttu-id="dd239-167">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="dd239-167">In Global Catalog</span></span>      | <span data-ttu-id="dd239-168">Falso</span><span class="sxs-lookup"><span data-stu-id="dd239-168">False</span></span>                                                     |
| <span data-ttu-id="dd239-169">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="dd239-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="dd239-170">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="dd239-170">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="dd239-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dd239-171">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="dd239-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dd239-172">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="dd239-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dd239-173">Search-Flags</span></span>           | <span data-ttu-id="dd239-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dd239-174">0x00000000</span></span>                                                |
| <span data-ttu-id="dd239-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dd239-175">System-Flags</span></span>           | <span data-ttu-id="dd239-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dd239-176">0x00000010</span></span>                                                |
| <span data-ttu-id="dd239-177">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="dd239-177">Classes used in</span></span>        | [<span data-ttu-id="dd239-178">**MS-TAPI-RT-person**</span><span class="sxs-lookup"><span data-stu-id="dd239-178">**ms-TAPI-Rt-Person**</span></span>](c-mstapi-rtperson.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="dd239-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dd239-179">Windows Server 2008</span></span>



| <span data-ttu-id="dd239-180">Voce</span><span class="sxs-lookup"><span data-stu-id="dd239-180">Entry</span></span> | <span data-ttu-id="dd239-181">Valore</span><span class="sxs-lookup"><span data-stu-id="dd239-181">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="dd239-182">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="dd239-182">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="dd239-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dd239-183">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="dd239-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="dd239-184">System-Only</span></span>            | <span data-ttu-id="dd239-185">Falso</span><span class="sxs-lookup"><span data-stu-id="dd239-185">False</span></span>                                                     |
| <span data-ttu-id="dd239-186">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="dd239-186">Is-Single-Valued</span></span>       | <span data-ttu-id="dd239-187">Falso</span><span class="sxs-lookup"><span data-stu-id="dd239-187">False</span></span>                                                     |
| <span data-ttu-id="dd239-188">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="dd239-188">Is Indexed</span></span>             | <span data-ttu-id="dd239-189">Falso</span><span class="sxs-lookup"><span data-stu-id="dd239-189">False</span></span>                                                     |
| <span data-ttu-id="dd239-190">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="dd239-190">In Global Catalog</span></span>      | <span data-ttu-id="dd239-191">Falso</span><span class="sxs-lookup"><span data-stu-id="dd239-191">False</span></span>                                                     |
| <span data-ttu-id="dd239-192">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="dd239-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="dd239-193">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="dd239-193">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="dd239-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dd239-194">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="dd239-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dd239-195">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="dd239-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dd239-196">Search-Flags</span></span>           | <span data-ttu-id="dd239-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dd239-197">0x00000000</span></span>                                                |
| <span data-ttu-id="dd239-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dd239-198">System-Flags</span></span>           | <span data-ttu-id="dd239-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dd239-199">0x00000010</span></span>                                                |
| <span data-ttu-id="dd239-200">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="dd239-200">Classes used in</span></span>        | [<span data-ttu-id="dd239-201">**MS-TAPI-RT-person**</span><span class="sxs-lookup"><span data-stu-id="dd239-201">**ms-TAPI-Rt-Person**</span></span>](c-mstapi-rtperson.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="dd239-202">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="dd239-202">Windows Server 2008 R2</span></span>



| <span data-ttu-id="dd239-203">Voce</span><span class="sxs-lookup"><span data-stu-id="dd239-203">Entry</span></span> | <span data-ttu-id="dd239-204">Valore</span><span class="sxs-lookup"><span data-stu-id="dd239-204">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="dd239-205">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="dd239-205">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="dd239-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dd239-206">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="dd239-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="dd239-207">System-Only</span></span>            | <span data-ttu-id="dd239-208">Falso</span><span class="sxs-lookup"><span data-stu-id="dd239-208">False</span></span>                                                     |
| <span data-ttu-id="dd239-209">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="dd239-209">Is-Single-Valued</span></span>       | <span data-ttu-id="dd239-210">Falso</span><span class="sxs-lookup"><span data-stu-id="dd239-210">False</span></span>                                                     |
| <span data-ttu-id="dd239-211">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="dd239-211">Is Indexed</span></span>             | <span data-ttu-id="dd239-212">Falso</span><span class="sxs-lookup"><span data-stu-id="dd239-212">False</span></span>                                                     |
| <span data-ttu-id="dd239-213">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="dd239-213">In Global Catalog</span></span>      | <span data-ttu-id="dd239-214">Falso</span><span class="sxs-lookup"><span data-stu-id="dd239-214">False</span></span>                                                     |
| <span data-ttu-id="dd239-215">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="dd239-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="dd239-216">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="dd239-216">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="dd239-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dd239-217">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="dd239-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dd239-218">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="dd239-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dd239-219">Search-Flags</span></span>           | <span data-ttu-id="dd239-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dd239-220">0x00000000</span></span>                                                |
| <span data-ttu-id="dd239-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dd239-221">System-Flags</span></span>           | <span data-ttu-id="dd239-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dd239-222">0x00000010</span></span>                                                |
| <span data-ttu-id="dd239-223">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="dd239-223">Classes used in</span></span>        | [<span data-ttu-id="dd239-224">**MS-TAPI-RT-person**</span><span class="sxs-lookup"><span data-stu-id="dd239-224">**ms-TAPI-Rt-Person**</span></span>](c-mstapi-rtperson.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="dd239-225">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="dd239-225">Windows Server 2012</span></span>



| <span data-ttu-id="dd239-226">Voce</span><span class="sxs-lookup"><span data-stu-id="dd239-226">Entry</span></span> | <span data-ttu-id="dd239-227">Valore</span><span class="sxs-lookup"><span data-stu-id="dd239-227">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="dd239-228">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="dd239-228">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="dd239-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dd239-229">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="dd239-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="dd239-230">System-Only</span></span>            | <span data-ttu-id="dd239-231">Falso</span><span class="sxs-lookup"><span data-stu-id="dd239-231">False</span></span>                                                     |
| <span data-ttu-id="dd239-232">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="dd239-232">Is-Single-Valued</span></span>       | <span data-ttu-id="dd239-233">Falso</span><span class="sxs-lookup"><span data-stu-id="dd239-233">False</span></span>                                                     |
| <span data-ttu-id="dd239-234">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="dd239-234">Is Indexed</span></span>             | <span data-ttu-id="dd239-235">Falso</span><span class="sxs-lookup"><span data-stu-id="dd239-235">False</span></span>                                                     |
| <span data-ttu-id="dd239-236">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="dd239-236">In Global Catalog</span></span>      | <span data-ttu-id="dd239-237">Falso</span><span class="sxs-lookup"><span data-stu-id="dd239-237">False</span></span>                                                     |
| <span data-ttu-id="dd239-238">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="dd239-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="dd239-239">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="dd239-239">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="dd239-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dd239-240">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="dd239-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dd239-241">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="dd239-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dd239-242">Search-Flags</span></span>           | <span data-ttu-id="dd239-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dd239-243">0x00000000</span></span>                                                |
| <span data-ttu-id="dd239-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dd239-244">System-Flags</span></span>           | <span data-ttu-id="dd239-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dd239-245">0x00000010</span></span>                                                |
| <span data-ttu-id="dd239-246">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="dd239-246">Classes used in</span></span>        | [<span data-ttu-id="dd239-247">**MS-TAPI-RT-person**</span><span class="sxs-lookup"><span data-stu-id="dd239-247">**ms-TAPI-Rt-Person**</span></span>](c-mstapi-rtperson.md)<br/> |



 

 





