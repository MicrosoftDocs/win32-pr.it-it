---
title: Attributo MS-DS-Creator-SID
description: ID di sicurezza del creatore dell'oggetto che contiene l'attributo.
ms.assetid: 5e643c56-bfe9-4489-89a9-5ce56f90f288
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo MS-DS-Creator-SID
- Schema AD dell'attributo mS-DS-CreatorSID
topic_type:
- apiref
api_name:
- MS-DS-Creator-SID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73b5b5635773271c4864ac2c8ec1898edcc9a9f9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103965122"
---
# <a name="ms-ds-creator-sid-attribute"></a><span data-ttu-id="008c5-105">Attributo MS-DS-Creator-SID</span><span class="sxs-lookup"><span data-stu-id="008c5-105">MS-DS-Creator-SID attribute</span></span>

<span data-ttu-id="008c5-106">ID di sicurezza del creatore dell'oggetto che contiene l'attributo.</span><span class="sxs-lookup"><span data-stu-id="008c5-106">The security ID of the creator of the object that contains this attribute.</span></span>



| <span data-ttu-id="008c5-107">Voce</span><span class="sxs-lookup"><span data-stu-id="008c5-107">Entry</span></span> | <span data-ttu-id="008c5-108">Valore</span><span class="sxs-lookup"><span data-stu-id="008c5-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="008c5-109">CN</span><span class="sxs-lookup"><span data-stu-id="008c5-109">CN</span></span>                | <span data-ttu-id="008c5-110">MS-DS-Creator-SID</span><span class="sxs-lookup"><span data-stu-id="008c5-110">MS-DS-Creator-SID</span></span>                    |
| <span data-ttu-id="008c5-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="008c5-111">Ldap-Display-Name</span></span> | <span data-ttu-id="008c5-112">mS-DS-CreatorSID</span><span class="sxs-lookup"><span data-stu-id="008c5-112">mS-DS-CreatorSID</span></span>                     |
| <span data-ttu-id="008c5-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="008c5-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="008c5-114">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="008c5-114">Update Privilege</span></span>  | <span data-ttu-id="008c5-115">Questo valore viene impostato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="008c5-115">This value is set by the system.</span></span>     |
| <span data-ttu-id="008c5-116">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="008c5-116">Update Frequency</span></span>  | <span data-ttu-id="008c5-117">Ogni volta che viene creato un nuovo oggetto.</span><span class="sxs-lookup"><span data-stu-id="008c5-117">Whenever a new object is created.</span></span>    |
| <span data-ttu-id="008c5-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="008c5-118">Attribute-Id</span></span>      | <span data-ttu-id="008c5-119">1.2.840.113556.1.4.1410</span><span class="sxs-lookup"><span data-stu-id="008c5-119">1.2.840.113556.1.4.1410</span></span>              |
| <span data-ttu-id="008c5-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="008c5-120">System-Id-Guid</span></span>    | <span data-ttu-id="008c5-121">c5e60132-1480-11d3-91c1-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="008c5-121">c5e60132-1480-11d3-91c1-0000f87a57d4</span></span> |
| <span data-ttu-id="008c5-122">Sintassi</span><span class="sxs-lookup"><span data-stu-id="008c5-122">Syntax</span></span>            | [<span data-ttu-id="008c5-123">**Stringa (SID)**</span><span class="sxs-lookup"><span data-stu-id="008c5-123">**String(Sid)**</span></span>](s-string-sid.md)  |



## <a name="implementations"></a><span data-ttu-id="008c5-124">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="008c5-124">Implementations</span></span>

-   [<span data-ttu-id="008c5-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="008c5-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="008c5-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="008c5-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="008c5-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="008c5-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="008c5-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="008c5-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="008c5-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="008c5-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="008c5-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="008c5-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="008c5-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="008c5-131">Windows 2000 Server</span></span>



| <span data-ttu-id="008c5-132">Voce</span><span class="sxs-lookup"><span data-stu-id="008c5-132">Entry</span></span> | <span data-ttu-id="008c5-133">Valore</span><span class="sxs-lookup"><span data-stu-id="008c5-133">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="008c5-134">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="008c5-134">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="008c5-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="008c5-135">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="008c5-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="008c5-136">System-Only</span></span>            | <span data-ttu-id="008c5-137">Vero</span><span class="sxs-lookup"><span data-stu-id="008c5-137">True</span></span>                              |
| <span data-ttu-id="008c5-138">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="008c5-138">Is-Single-Valued</span></span>       | <span data-ttu-id="008c5-139">Vero</span><span class="sxs-lookup"><span data-stu-id="008c5-139">True</span></span>                              |
| <span data-ttu-id="008c5-140">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="008c5-140">Is Indexed</span></span>             | <span data-ttu-id="008c5-141">Vero</span><span class="sxs-lookup"><span data-stu-id="008c5-141">True</span></span>                              |
| <span data-ttu-id="008c5-142">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="008c5-142">In Global Catalog</span></span>      | <span data-ttu-id="008c5-143">Falso</span><span class="sxs-lookup"><span data-stu-id="008c5-143">False</span></span>                             |
| <span data-ttu-id="008c5-144">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="008c5-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="008c5-145">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="008c5-145">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="008c5-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="008c5-146">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="008c5-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="008c5-147">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="008c5-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="008c5-148">Search-Flags</span></span>           | <span data-ttu-id="008c5-149">0x00000001</span><span class="sxs-lookup"><span data-stu-id="008c5-149">0x00000001</span></span>                        |
| <span data-ttu-id="008c5-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="008c5-150">System-Flags</span></span>           | <span data-ttu-id="008c5-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="008c5-151">0x00000010</span></span>                        |
| <span data-ttu-id="008c5-152">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="008c5-152">Classes used in</span></span>        | [<span data-ttu-id="008c5-153">**Utente**</span><span class="sxs-lookup"><span data-stu-id="008c5-153">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="008c5-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="008c5-154">Windows Server 2003</span></span>



| <span data-ttu-id="008c5-155">Voce</span><span class="sxs-lookup"><span data-stu-id="008c5-155">Entry</span></span> | <span data-ttu-id="008c5-156">Valore</span><span class="sxs-lookup"><span data-stu-id="008c5-156">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="008c5-157">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="008c5-157">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="008c5-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="008c5-158">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="008c5-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="008c5-159">System-Only</span></span>            | <span data-ttu-id="008c5-160">Vero</span><span class="sxs-lookup"><span data-stu-id="008c5-160">True</span></span>                              |
| <span data-ttu-id="008c5-161">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="008c5-161">Is-Single-Valued</span></span>       | <span data-ttu-id="008c5-162">Vero</span><span class="sxs-lookup"><span data-stu-id="008c5-162">True</span></span>                              |
| <span data-ttu-id="008c5-163">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="008c5-163">Is Indexed</span></span>             | <span data-ttu-id="008c5-164">Vero</span><span class="sxs-lookup"><span data-stu-id="008c5-164">True</span></span>                              |
| <span data-ttu-id="008c5-165">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="008c5-165">In Global Catalog</span></span>      | <span data-ttu-id="008c5-166">Falso</span><span class="sxs-lookup"><span data-stu-id="008c5-166">False</span></span>                             |
| <span data-ttu-id="008c5-167">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="008c5-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="008c5-168">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="008c5-168">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="008c5-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="008c5-169">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="008c5-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="008c5-170">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="008c5-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="008c5-171">Search-Flags</span></span>           | <span data-ttu-id="008c5-172">0x00000001</span><span class="sxs-lookup"><span data-stu-id="008c5-172">0x00000001</span></span>                        |
| <span data-ttu-id="008c5-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="008c5-173">System-Flags</span></span>           | <span data-ttu-id="008c5-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="008c5-174">0x00000010</span></span>                        |
| <span data-ttu-id="008c5-175">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="008c5-175">Classes used in</span></span>        | [<span data-ttu-id="008c5-176">**Utente**</span><span class="sxs-lookup"><span data-stu-id="008c5-176">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="008c5-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="008c5-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="008c5-178">Voce</span><span class="sxs-lookup"><span data-stu-id="008c5-178">Entry</span></span> | <span data-ttu-id="008c5-179">Valore</span><span class="sxs-lookup"><span data-stu-id="008c5-179">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="008c5-180">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="008c5-180">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="008c5-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="008c5-181">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="008c5-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="008c5-182">System-Only</span></span>            | <span data-ttu-id="008c5-183">Vero</span><span class="sxs-lookup"><span data-stu-id="008c5-183">True</span></span>                              |
| <span data-ttu-id="008c5-184">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="008c5-184">Is-Single-Valued</span></span>       | <span data-ttu-id="008c5-185">Vero</span><span class="sxs-lookup"><span data-stu-id="008c5-185">True</span></span>                              |
| <span data-ttu-id="008c5-186">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="008c5-186">Is Indexed</span></span>             | <span data-ttu-id="008c5-187">Vero</span><span class="sxs-lookup"><span data-stu-id="008c5-187">True</span></span>                              |
| <span data-ttu-id="008c5-188">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="008c5-188">In Global Catalog</span></span>      | <span data-ttu-id="008c5-189">Falso</span><span class="sxs-lookup"><span data-stu-id="008c5-189">False</span></span>                             |
| <span data-ttu-id="008c5-190">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="008c5-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="008c5-191">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="008c5-191">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="008c5-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="008c5-192">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="008c5-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="008c5-193">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="008c5-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="008c5-194">Search-Flags</span></span>           | <span data-ttu-id="008c5-195">0x00000001</span><span class="sxs-lookup"><span data-stu-id="008c5-195">0x00000001</span></span>                        |
| <span data-ttu-id="008c5-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="008c5-196">System-Flags</span></span>           | <span data-ttu-id="008c5-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="008c5-197">0x00000010</span></span>                        |
| <span data-ttu-id="008c5-198">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="008c5-198">Classes used in</span></span>        | [<span data-ttu-id="008c5-199">**Utente**</span><span class="sxs-lookup"><span data-stu-id="008c5-199">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="008c5-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="008c5-200">Windows Server 2008</span></span>



| <span data-ttu-id="008c5-201">Voce</span><span class="sxs-lookup"><span data-stu-id="008c5-201">Entry</span></span> | <span data-ttu-id="008c5-202">Valore</span><span class="sxs-lookup"><span data-stu-id="008c5-202">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="008c5-203">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="008c5-203">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="008c5-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="008c5-204">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="008c5-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="008c5-205">System-Only</span></span>            | <span data-ttu-id="008c5-206">Vero</span><span class="sxs-lookup"><span data-stu-id="008c5-206">True</span></span>                              |
| <span data-ttu-id="008c5-207">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="008c5-207">Is-Single-Valued</span></span>       | <span data-ttu-id="008c5-208">Vero</span><span class="sxs-lookup"><span data-stu-id="008c5-208">True</span></span>                              |
| <span data-ttu-id="008c5-209">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="008c5-209">Is Indexed</span></span>             | <span data-ttu-id="008c5-210">Vero</span><span class="sxs-lookup"><span data-stu-id="008c5-210">True</span></span>                              |
| <span data-ttu-id="008c5-211">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="008c5-211">In Global Catalog</span></span>      | <span data-ttu-id="008c5-212">Falso</span><span class="sxs-lookup"><span data-stu-id="008c5-212">False</span></span>                             |
| <span data-ttu-id="008c5-213">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="008c5-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="008c5-214">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="008c5-214">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="008c5-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="008c5-215">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="008c5-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="008c5-216">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="008c5-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="008c5-217">Search-Flags</span></span>           | <span data-ttu-id="008c5-218">0x00000001</span><span class="sxs-lookup"><span data-stu-id="008c5-218">0x00000001</span></span>                        |
| <span data-ttu-id="008c5-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="008c5-219">System-Flags</span></span>           | <span data-ttu-id="008c5-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="008c5-220">0x00000010</span></span>                        |
| <span data-ttu-id="008c5-221">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="008c5-221">Classes used in</span></span>        | [<span data-ttu-id="008c5-222">**Utente**</span><span class="sxs-lookup"><span data-stu-id="008c5-222">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="008c5-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="008c5-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="008c5-224">Voce</span><span class="sxs-lookup"><span data-stu-id="008c5-224">Entry</span></span> | <span data-ttu-id="008c5-225">Valore</span><span class="sxs-lookup"><span data-stu-id="008c5-225">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="008c5-226">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="008c5-226">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="008c5-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="008c5-227">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="008c5-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="008c5-228">System-Only</span></span>            | <span data-ttu-id="008c5-229">Vero</span><span class="sxs-lookup"><span data-stu-id="008c5-229">True</span></span>                              |
| <span data-ttu-id="008c5-230">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="008c5-230">Is-Single-Valued</span></span>       | <span data-ttu-id="008c5-231">Vero</span><span class="sxs-lookup"><span data-stu-id="008c5-231">True</span></span>                              |
| <span data-ttu-id="008c5-232">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="008c5-232">Is Indexed</span></span>             | <span data-ttu-id="008c5-233">Vero</span><span class="sxs-lookup"><span data-stu-id="008c5-233">True</span></span>                              |
| <span data-ttu-id="008c5-234">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="008c5-234">In Global Catalog</span></span>      | <span data-ttu-id="008c5-235">Falso</span><span class="sxs-lookup"><span data-stu-id="008c5-235">False</span></span>                             |
| <span data-ttu-id="008c5-236">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="008c5-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="008c5-237">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="008c5-237">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="008c5-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="008c5-238">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="008c5-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="008c5-239">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="008c5-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="008c5-240">Search-Flags</span></span>           | <span data-ttu-id="008c5-241">0x00000001</span><span class="sxs-lookup"><span data-stu-id="008c5-241">0x00000001</span></span>                        |
| <span data-ttu-id="008c5-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="008c5-242">System-Flags</span></span>           | <span data-ttu-id="008c5-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="008c5-243">0x00000010</span></span>                        |
| <span data-ttu-id="008c5-244">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="008c5-244">Classes used in</span></span>        | [<span data-ttu-id="008c5-245">**Utente**</span><span class="sxs-lookup"><span data-stu-id="008c5-245">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="008c5-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="008c5-246">Windows Server 2012</span></span>



| <span data-ttu-id="008c5-247">Voce</span><span class="sxs-lookup"><span data-stu-id="008c5-247">Entry</span></span> | <span data-ttu-id="008c5-248">Valore</span><span class="sxs-lookup"><span data-stu-id="008c5-248">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="008c5-249">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="008c5-249">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="008c5-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="008c5-250">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="008c5-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="008c5-251">System-Only</span></span>            | <span data-ttu-id="008c5-252">Vero</span><span class="sxs-lookup"><span data-stu-id="008c5-252">True</span></span>                              |
| <span data-ttu-id="008c5-253">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="008c5-253">Is-Single-Valued</span></span>       | <span data-ttu-id="008c5-254">Vero</span><span class="sxs-lookup"><span data-stu-id="008c5-254">True</span></span>                              |
| <span data-ttu-id="008c5-255">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="008c5-255">Is Indexed</span></span>             | <span data-ttu-id="008c5-256">Vero</span><span class="sxs-lookup"><span data-stu-id="008c5-256">True</span></span>                              |
| <span data-ttu-id="008c5-257">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="008c5-257">In Global Catalog</span></span>      | <span data-ttu-id="008c5-258">Falso</span><span class="sxs-lookup"><span data-stu-id="008c5-258">False</span></span>                             |
| <span data-ttu-id="008c5-259">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="008c5-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="008c5-260">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="008c5-260">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="008c5-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="008c5-261">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="008c5-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="008c5-262">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="008c5-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="008c5-263">Search-Flags</span></span>           | <span data-ttu-id="008c5-264">0x00000001</span><span class="sxs-lookup"><span data-stu-id="008c5-264">0x00000001</span></span>                        |
| <span data-ttu-id="008c5-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="008c5-265">System-Flags</span></span>           | <span data-ttu-id="008c5-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="008c5-266">0x00000010</span></span>                        |
| <span data-ttu-id="008c5-267">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="008c5-267">Classes used in</span></span>        | [<span data-ttu-id="008c5-268">**Utente**</span><span class="sxs-lookup"><span data-stu-id="008c5-268">**User**</span></span>](c-user.md)<br/> |



 

 





