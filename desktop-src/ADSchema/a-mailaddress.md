---
title: SMTP-mail-address-attributo
description: Attributo indirizzo di posta elettronica generico. Utilizzato nella casella come attributo facoltativo di oggetti server, in cui viene utilizzata dalla replica DS basata sulla posta elettronica (se i computer sono stati configurati).
ms.assetid: 54fd710c-d140-4d46-9db3-0c72fb5fb08c
ms.tgt_platform: multiple
keywords:
- SMTP-mail-address-schema AD attributo
- Schema AD dell'attributo mailAddress
topic_type:
- apiref
api_name:
- SMTP-Mail-Address
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e1828c59af346ab5a5741aaa03358b711484089
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104122135"
---
# <a name="smtp-mail-address-attribute"></a><span data-ttu-id="4dd1f-106">SMTP-mail-address-attributo</span><span class="sxs-lookup"><span data-stu-id="4dd1f-106">SMTP-Mail-Address attribute</span></span>

<span data-ttu-id="4dd1f-107">Attributo indirizzo di posta elettronica generico.</span><span class="sxs-lookup"><span data-stu-id="4dd1f-107">Generic mail address attribute.</span></span> <span data-ttu-id="4dd1f-108">Utilizzato nella casella come attributo facoltativo di oggetti server, in cui viene utilizzata dalla replica DS basata sulla posta elettronica (se i computer sono stati configurati).</span><span class="sxs-lookup"><span data-stu-id="4dd1f-108">Used in the box as an optional attribute of server objects, where it is consumed by mail-based DS replication (if the computers are so configured).</span></span>



| <span data-ttu-id="4dd1f-109">Voce</span><span class="sxs-lookup"><span data-stu-id="4dd1f-109">Entry</span></span> | <span data-ttu-id="4dd1f-110">Valore</span><span class="sxs-lookup"><span data-stu-id="4dd1f-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="4dd1f-111">CN</span><span class="sxs-lookup"><span data-stu-id="4dd1f-111">CN</span></span>                | <span data-ttu-id="4dd1f-112">SMTP-indirizzo posta elettronica</span><span class="sxs-lookup"><span data-stu-id="4dd1f-112">SMTP-Mail-Address</span></span>                           |
| <span data-ttu-id="4dd1f-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="4dd1f-113">Ldap-Display-Name</span></span> | <span data-ttu-id="4dd1f-114">mailAddress</span><span class="sxs-lookup"><span data-stu-id="4dd1f-114">mailAddress</span></span>                                 |
| <span data-ttu-id="4dd1f-115">Dimensione</span><span class="sxs-lookup"><span data-stu-id="4dd1f-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="4dd1f-116">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="4dd1f-116">Update Privilege</span></span>  | <span data-ttu-id="4dd1f-117">Amministratore di dominio</span><span class="sxs-lookup"><span data-stu-id="4dd1f-117">Domain administrator</span></span>                        |
| <span data-ttu-id="4dd1f-118">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="4dd1f-118">Update Frequency</span></span>  | <span data-ttu-id="4dd1f-119">Quasi mai</span><span class="sxs-lookup"><span data-stu-id="4dd1f-119">Almost never</span></span>                                |
| <span data-ttu-id="4dd1f-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="4dd1f-120">Attribute-Id</span></span>      | <span data-ttu-id="4dd1f-121">1.2.840.113556.1.4.786</span><span class="sxs-lookup"><span data-stu-id="4dd1f-121">1.2.840.113556.1.4.786</span></span>                      |
| <span data-ttu-id="4dd1f-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="4dd1f-122">System-Id-Guid</span></span>    | <span data-ttu-id="4dd1f-123">26d9736f-6070-11d1-a9c6-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="4dd1f-123">26d9736f-6070-11d1-a9c6-0000f80367c1</span></span>        |
| <span data-ttu-id="4dd1f-124">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4dd1f-124">Syntax</span></span>            | [<span data-ttu-id="4dd1f-125">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="4dd1f-125">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="4dd1f-126">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="4dd1f-126">Implementations</span></span>

-   [<span data-ttu-id="4dd1f-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="4dd1f-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="4dd1f-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="4dd1f-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="4dd1f-129">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="4dd1f-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="4dd1f-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="4dd1f-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="4dd1f-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="4dd1f-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="4dd1f-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="4dd1f-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="4dd1f-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="4dd1f-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="4dd1f-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4dd1f-134">Windows 2000 Server</span></span>



| <span data-ttu-id="4dd1f-135">Voce</span><span class="sxs-lookup"><span data-stu-id="4dd1f-135">Entry</span></span> | <span data-ttu-id="4dd1f-136">Valore</span><span class="sxs-lookup"><span data-stu-id="4dd1f-136">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="4dd1f-137">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="4dd1f-137">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="4dd1f-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4dd1f-138">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="4dd1f-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="4dd1f-139">System-Only</span></span>            | <span data-ttu-id="4dd1f-140">Falso</span><span class="sxs-lookup"><span data-stu-id="4dd1f-140">False</span></span>                                 |
| <span data-ttu-id="4dd1f-141">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="4dd1f-141">Is-Single-Valued</span></span>       | <span data-ttu-id="4dd1f-142">Vero</span><span class="sxs-lookup"><span data-stu-id="4dd1f-142">True</span></span>                                  |
| <span data-ttu-id="4dd1f-143">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="4dd1f-143">Is Indexed</span></span>             | <span data-ttu-id="4dd1f-144">Falso</span><span class="sxs-lookup"><span data-stu-id="4dd1f-144">False</span></span>                                 |
| <span data-ttu-id="4dd1f-145">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="4dd1f-145">In Global Catalog</span></span>      | <span data-ttu-id="4dd1f-146">Falso</span><span class="sxs-lookup"><span data-stu-id="4dd1f-146">False</span></span>                                 |
| <span data-ttu-id="4dd1f-147">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="4dd1f-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="4dd1f-148">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="4dd1f-148">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="4dd1f-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4dd1f-149">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="4dd1f-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4dd1f-150">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="4dd1f-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4dd1f-151">Search-Flags</span></span>           | <span data-ttu-id="4dd1f-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4dd1f-152">0x00000000</span></span>                            |
| <span data-ttu-id="4dd1f-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4dd1f-153">System-Flags</span></span>           | <span data-ttu-id="4dd1f-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4dd1f-154">0x00000010</span></span>                            |
| <span data-ttu-id="4dd1f-155">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="4dd1f-155">Classes used in</span></span>        | [<span data-ttu-id="4dd1f-156">**Server**</span><span class="sxs-lookup"><span data-stu-id="4dd1f-156">**Server**</span></span>](c-server.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="4dd1f-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4dd1f-157">Windows Server 2003</span></span>



| <span data-ttu-id="4dd1f-158">Voce</span><span class="sxs-lookup"><span data-stu-id="4dd1f-158">Entry</span></span> | <span data-ttu-id="4dd1f-159">Valore</span><span class="sxs-lookup"><span data-stu-id="4dd1f-159">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="4dd1f-160">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="4dd1f-160">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="4dd1f-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4dd1f-161">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="4dd1f-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="4dd1f-162">System-Only</span></span>            | <span data-ttu-id="4dd1f-163">Falso</span><span class="sxs-lookup"><span data-stu-id="4dd1f-163">False</span></span>                                 |
| <span data-ttu-id="4dd1f-164">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="4dd1f-164">Is-Single-Valued</span></span>       | <span data-ttu-id="4dd1f-165">Vero</span><span class="sxs-lookup"><span data-stu-id="4dd1f-165">True</span></span>                                  |
| <span data-ttu-id="4dd1f-166">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="4dd1f-166">Is Indexed</span></span>             | <span data-ttu-id="4dd1f-167">Falso</span><span class="sxs-lookup"><span data-stu-id="4dd1f-167">False</span></span>                                 |
| <span data-ttu-id="4dd1f-168">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="4dd1f-168">In Global Catalog</span></span>      | <span data-ttu-id="4dd1f-169">Falso</span><span class="sxs-lookup"><span data-stu-id="4dd1f-169">False</span></span>                                 |
| <span data-ttu-id="4dd1f-170">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="4dd1f-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="4dd1f-171">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="4dd1f-171">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="4dd1f-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4dd1f-172">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="4dd1f-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4dd1f-173">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="4dd1f-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4dd1f-174">Search-Flags</span></span>           | <span data-ttu-id="4dd1f-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4dd1f-175">0x00000000</span></span>                            |
| <span data-ttu-id="4dd1f-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4dd1f-176">System-Flags</span></span>           | <span data-ttu-id="4dd1f-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4dd1f-177">0x00000010</span></span>                            |
| <span data-ttu-id="4dd1f-178">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="4dd1f-178">Classes used in</span></span>        | [<span data-ttu-id="4dd1f-179">**Server**</span><span class="sxs-lookup"><span data-stu-id="4dd1f-179">**Server**</span></span>](c-server.md)<br/> |



## <a name="adam"></a><span data-ttu-id="4dd1f-180">ADAM</span><span class="sxs-lookup"><span data-stu-id="4dd1f-180">ADAM</span></span>



| <span data-ttu-id="4dd1f-181">Voce</span><span class="sxs-lookup"><span data-stu-id="4dd1f-181">Entry</span></span> | <span data-ttu-id="4dd1f-182">Valore</span><span class="sxs-lookup"><span data-stu-id="4dd1f-182">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="4dd1f-183">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="4dd1f-183">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="4dd1f-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4dd1f-184">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="4dd1f-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="4dd1f-185">System-Only</span></span>            | <span data-ttu-id="4dd1f-186">Falso</span><span class="sxs-lookup"><span data-stu-id="4dd1f-186">False</span></span>                                 |
| <span data-ttu-id="4dd1f-187">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="4dd1f-187">Is-Single-Valued</span></span>       | <span data-ttu-id="4dd1f-188">Vero</span><span class="sxs-lookup"><span data-stu-id="4dd1f-188">True</span></span>                                  |
| <span data-ttu-id="4dd1f-189">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="4dd1f-189">Is Indexed</span></span>             | <span data-ttu-id="4dd1f-190">Falso</span><span class="sxs-lookup"><span data-stu-id="4dd1f-190">False</span></span>                                 |
| <span data-ttu-id="4dd1f-191">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="4dd1f-191">In Global Catalog</span></span>      | <span data-ttu-id="4dd1f-192">Falso</span><span class="sxs-lookup"><span data-stu-id="4dd1f-192">False</span></span>                                 |
| <span data-ttu-id="4dd1f-193">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="4dd1f-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="4dd1f-194">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="4dd1f-194">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="4dd1f-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4dd1f-195">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="4dd1f-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4dd1f-196">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="4dd1f-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4dd1f-197">Search-Flags</span></span>           | <span data-ttu-id="4dd1f-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4dd1f-198">0x00000000</span></span>                            |
| <span data-ttu-id="4dd1f-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4dd1f-199">System-Flags</span></span>           | <span data-ttu-id="4dd1f-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4dd1f-200">0x00000010</span></span>                            |
| <span data-ttu-id="4dd1f-201">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="4dd1f-201">Classes used in</span></span>        | [<span data-ttu-id="4dd1f-202">**Server**</span><span class="sxs-lookup"><span data-stu-id="4dd1f-202">**Server**</span></span>](c-server.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="4dd1f-203">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="4dd1f-203">Windows Server 2003 R2</span></span>



| <span data-ttu-id="4dd1f-204">Voce</span><span class="sxs-lookup"><span data-stu-id="4dd1f-204">Entry</span></span> | <span data-ttu-id="4dd1f-205">Valore</span><span class="sxs-lookup"><span data-stu-id="4dd1f-205">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="4dd1f-206">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="4dd1f-206">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="4dd1f-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4dd1f-207">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="4dd1f-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="4dd1f-208">System-Only</span></span>            | <span data-ttu-id="4dd1f-209">Falso</span><span class="sxs-lookup"><span data-stu-id="4dd1f-209">False</span></span>                                 |
| <span data-ttu-id="4dd1f-210">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="4dd1f-210">Is-Single-Valued</span></span>       | <span data-ttu-id="4dd1f-211">Vero</span><span class="sxs-lookup"><span data-stu-id="4dd1f-211">True</span></span>                                  |
| <span data-ttu-id="4dd1f-212">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="4dd1f-212">Is Indexed</span></span>             | <span data-ttu-id="4dd1f-213">Falso</span><span class="sxs-lookup"><span data-stu-id="4dd1f-213">False</span></span>                                 |
| <span data-ttu-id="4dd1f-214">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="4dd1f-214">In Global Catalog</span></span>      | <span data-ttu-id="4dd1f-215">Falso</span><span class="sxs-lookup"><span data-stu-id="4dd1f-215">False</span></span>                                 |
| <span data-ttu-id="4dd1f-216">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="4dd1f-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="4dd1f-217">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="4dd1f-217">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="4dd1f-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4dd1f-218">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="4dd1f-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4dd1f-219">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="4dd1f-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4dd1f-220">Search-Flags</span></span>           | <span data-ttu-id="4dd1f-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4dd1f-221">0x00000000</span></span>                            |
| <span data-ttu-id="4dd1f-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4dd1f-222">System-Flags</span></span>           | <span data-ttu-id="4dd1f-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4dd1f-223">0x00000010</span></span>                            |
| <span data-ttu-id="4dd1f-224">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="4dd1f-224">Classes used in</span></span>        | [<span data-ttu-id="4dd1f-225">**Server**</span><span class="sxs-lookup"><span data-stu-id="4dd1f-225">**Server**</span></span>](c-server.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="4dd1f-226">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4dd1f-226">Windows Server 2008</span></span>



| <span data-ttu-id="4dd1f-227">Voce</span><span class="sxs-lookup"><span data-stu-id="4dd1f-227">Entry</span></span> | <span data-ttu-id="4dd1f-228">Valore</span><span class="sxs-lookup"><span data-stu-id="4dd1f-228">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="4dd1f-229">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="4dd1f-229">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="4dd1f-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4dd1f-230">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="4dd1f-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="4dd1f-231">System-Only</span></span>            | <span data-ttu-id="4dd1f-232">Falso</span><span class="sxs-lookup"><span data-stu-id="4dd1f-232">False</span></span>                                 |
| <span data-ttu-id="4dd1f-233">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="4dd1f-233">Is-Single-Valued</span></span>       | <span data-ttu-id="4dd1f-234">Vero</span><span class="sxs-lookup"><span data-stu-id="4dd1f-234">True</span></span>                                  |
| <span data-ttu-id="4dd1f-235">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="4dd1f-235">Is Indexed</span></span>             | <span data-ttu-id="4dd1f-236">Falso</span><span class="sxs-lookup"><span data-stu-id="4dd1f-236">False</span></span>                                 |
| <span data-ttu-id="4dd1f-237">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="4dd1f-237">In Global Catalog</span></span>      | <span data-ttu-id="4dd1f-238">Falso</span><span class="sxs-lookup"><span data-stu-id="4dd1f-238">False</span></span>                                 |
| <span data-ttu-id="4dd1f-239">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="4dd1f-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="4dd1f-240">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="4dd1f-240">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="4dd1f-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4dd1f-241">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="4dd1f-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4dd1f-242">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="4dd1f-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4dd1f-243">Search-Flags</span></span>           | <span data-ttu-id="4dd1f-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4dd1f-244">0x00000000</span></span>                            |
| <span data-ttu-id="4dd1f-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4dd1f-245">System-Flags</span></span>           | <span data-ttu-id="4dd1f-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4dd1f-246">0x00000010</span></span>                            |
| <span data-ttu-id="4dd1f-247">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="4dd1f-247">Classes used in</span></span>        | [<span data-ttu-id="4dd1f-248">**Server**</span><span class="sxs-lookup"><span data-stu-id="4dd1f-248">**Server**</span></span>](c-server.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="4dd1f-249">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4dd1f-249">Windows Server 2008 R2</span></span>



| <span data-ttu-id="4dd1f-250">Voce</span><span class="sxs-lookup"><span data-stu-id="4dd1f-250">Entry</span></span> | <span data-ttu-id="4dd1f-251">Valore</span><span class="sxs-lookup"><span data-stu-id="4dd1f-251">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="4dd1f-252">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="4dd1f-252">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="4dd1f-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4dd1f-253">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="4dd1f-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="4dd1f-254">System-Only</span></span>            | <span data-ttu-id="4dd1f-255">Falso</span><span class="sxs-lookup"><span data-stu-id="4dd1f-255">False</span></span>                                 |
| <span data-ttu-id="4dd1f-256">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="4dd1f-256">Is-Single-Valued</span></span>       | <span data-ttu-id="4dd1f-257">Vero</span><span class="sxs-lookup"><span data-stu-id="4dd1f-257">True</span></span>                                  |
| <span data-ttu-id="4dd1f-258">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="4dd1f-258">Is Indexed</span></span>             | <span data-ttu-id="4dd1f-259">Falso</span><span class="sxs-lookup"><span data-stu-id="4dd1f-259">False</span></span>                                 |
| <span data-ttu-id="4dd1f-260">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="4dd1f-260">In Global Catalog</span></span>      | <span data-ttu-id="4dd1f-261">Falso</span><span class="sxs-lookup"><span data-stu-id="4dd1f-261">False</span></span>                                 |
| <span data-ttu-id="4dd1f-262">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="4dd1f-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="4dd1f-263">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="4dd1f-263">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="4dd1f-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4dd1f-264">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="4dd1f-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4dd1f-265">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="4dd1f-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4dd1f-266">Search-Flags</span></span>           | <span data-ttu-id="4dd1f-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4dd1f-267">0x00000000</span></span>                            |
| <span data-ttu-id="4dd1f-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4dd1f-268">System-Flags</span></span>           | <span data-ttu-id="4dd1f-269">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4dd1f-269">0x00000010</span></span>                            |
| <span data-ttu-id="4dd1f-270">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="4dd1f-270">Classes used in</span></span>        | [<span data-ttu-id="4dd1f-271">**Server**</span><span class="sxs-lookup"><span data-stu-id="4dd1f-271">**Server**</span></span>](c-server.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="4dd1f-272">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4dd1f-272">Windows Server 2012</span></span>



| <span data-ttu-id="4dd1f-273">Voce</span><span class="sxs-lookup"><span data-stu-id="4dd1f-273">Entry</span></span> | <span data-ttu-id="4dd1f-274">Valore</span><span class="sxs-lookup"><span data-stu-id="4dd1f-274">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="4dd1f-275">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="4dd1f-275">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="4dd1f-276">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4dd1f-276">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="4dd1f-277">System-Only</span><span class="sxs-lookup"><span data-stu-id="4dd1f-277">System-Only</span></span>            | <span data-ttu-id="4dd1f-278">Falso</span><span class="sxs-lookup"><span data-stu-id="4dd1f-278">False</span></span>                                 |
| <span data-ttu-id="4dd1f-279">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="4dd1f-279">Is-Single-Valued</span></span>       | <span data-ttu-id="4dd1f-280">Vero</span><span class="sxs-lookup"><span data-stu-id="4dd1f-280">True</span></span>                                  |
| <span data-ttu-id="4dd1f-281">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="4dd1f-281">Is Indexed</span></span>             | <span data-ttu-id="4dd1f-282">Falso</span><span class="sxs-lookup"><span data-stu-id="4dd1f-282">False</span></span>                                 |
| <span data-ttu-id="4dd1f-283">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="4dd1f-283">In Global Catalog</span></span>      | <span data-ttu-id="4dd1f-284">Falso</span><span class="sxs-lookup"><span data-stu-id="4dd1f-284">False</span></span>                                 |
| <span data-ttu-id="4dd1f-285">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="4dd1f-285">NT-Security-Descriptor</span></span> | <span data-ttu-id="4dd1f-286">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="4dd1f-286">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="4dd1f-287">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4dd1f-287">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="4dd1f-288">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4dd1f-288">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="4dd1f-289">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4dd1f-289">Search-Flags</span></span>           | <span data-ttu-id="4dd1f-290">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4dd1f-290">0x00000000</span></span>                            |
| <span data-ttu-id="4dd1f-291">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4dd1f-291">System-Flags</span></span>           | <span data-ttu-id="4dd1f-292">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4dd1f-292">0x00000010</span></span>                            |
| <span data-ttu-id="4dd1f-293">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="4dd1f-293">Classes used in</span></span>        | [<span data-ttu-id="4dd1f-294">**Server**</span><span class="sxs-lookup"><span data-stu-id="4dd1f-294">**Server**</span></span>](c-server.md)<br/> |



 

 





