---
title: Attributo Bad-pwd-count
description: Il numero di volte che l'utente ha tentato di accedere all'account con una password non corretta.
ms.assetid: 1161b0c1-1b28-4349-ad43-82ce68428c44
ms.tgt_platform: multiple
keywords:
- Errore-pwd-conteggio attributo AD schema
- Schema AD dell'attributo badPwdCount
topic_type:
- apiref
api_name:
- Bad-Pwd-Count
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e3a406058737773781874a81e9968786e1523d8
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104122174"
---
# <a name="bad-pwd-count-attribute"></a><span data-ttu-id="52ed0-105">Attributo Bad-pwd-count</span><span class="sxs-lookup"><span data-stu-id="52ed0-105">Bad-Pwd-Count attribute</span></span>

<span data-ttu-id="52ed0-106">Il numero di volte che l'utente ha tentato di accedere all'account con una password non corretta.</span><span class="sxs-lookup"><span data-stu-id="52ed0-106">The number of times the user tried to log on to the account using an incorrect password.</span></span> <span data-ttu-id="52ed0-107">Il valore 0 indica che il valore è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="52ed0-107">A value of 0 indicates that the value is unknown.</span></span>



| <span data-ttu-id="52ed0-108">Voce</span><span class="sxs-lookup"><span data-stu-id="52ed0-108">Entry</span></span> | <span data-ttu-id="52ed0-109">Valore</span><span class="sxs-lookup"><span data-stu-id="52ed0-109">Value</span></span> |
|-------------------|-------------------------------------------|
| <span data-ttu-id="52ed0-110">CN</span><span class="sxs-lookup"><span data-stu-id="52ed0-110">CN</span></span>                | <span data-ttu-id="52ed0-111">Numero di PWD non valido</span><span class="sxs-lookup"><span data-stu-id="52ed0-111">Bad-Pwd-Count</span></span>                             |
| <span data-ttu-id="52ed0-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="52ed0-112">Ldap-Display-Name</span></span> | <span data-ttu-id="52ed0-113">badPwdCount</span><span class="sxs-lookup"><span data-stu-id="52ed0-113">badPwdCount</span></span>                               |
| <span data-ttu-id="52ed0-114">Dimensione</span><span class="sxs-lookup"><span data-stu-id="52ed0-114">Size</span></span>              | <span data-ttu-id="52ed0-115">4 byte</span><span class="sxs-lookup"><span data-stu-id="52ed0-115">4 bytes</span></span>                                   |
| <span data-ttu-id="52ed0-116">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="52ed0-116">Update Privilege</span></span>  | <span data-ttu-id="52ed0-117">Questo valore viene impostato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="52ed0-117">This value is set by the system.</span></span>          |
| <span data-ttu-id="52ed0-118">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="52ed0-118">Update Frequency</span></span>  | <span data-ttu-id="52ed0-119">Ogni volta che l'utente immette una password errata.</span><span class="sxs-lookup"><span data-stu-id="52ed0-119">Each time the user enters a bad password.</span></span> |
| <span data-ttu-id="52ed0-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="52ed0-120">Attribute-Id</span></span>      | <span data-ttu-id="52ed0-121">1.2.840.113556.1.4.12</span><span class="sxs-lookup"><span data-stu-id="52ed0-121">1.2.840.113556.1.4.12</span></span>                     |
| <span data-ttu-id="52ed0-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="52ed0-122">System-Id-Guid</span></span>    | <span data-ttu-id="52ed0-123">bf96792e-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="52ed0-123">bf96792e-0de6-11d0-a285-00aa003049e2</span></span>      |
| <span data-ttu-id="52ed0-124">Sintassi</span><span class="sxs-lookup"><span data-stu-id="52ed0-124">Syntax</span></span>            | [<span data-ttu-id="52ed0-125">**Enumerazione**</span><span class="sxs-lookup"><span data-stu-id="52ed0-125">**Enumeration**</span></span>](s-enumeration.md)      |



## <a name="implementations"></a><span data-ttu-id="52ed0-126">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="52ed0-126">Implementations</span></span>

-   [<span data-ttu-id="52ed0-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="52ed0-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="52ed0-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="52ed0-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="52ed0-129">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="52ed0-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="52ed0-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="52ed0-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="52ed0-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="52ed0-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="52ed0-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="52ed0-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="52ed0-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="52ed0-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="52ed0-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="52ed0-134">Windows 2000 Server</span></span>



| <span data-ttu-id="52ed0-135">Voce</span><span class="sxs-lookup"><span data-stu-id="52ed0-135">Entry</span></span> | <span data-ttu-id="52ed0-136">Valore</span><span class="sxs-lookup"><span data-stu-id="52ed0-136">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="52ed0-137">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="52ed0-137">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="52ed0-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="52ed0-138">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="52ed0-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="52ed0-139">System-Only</span></span>            | <span data-ttu-id="52ed0-140">Falso</span><span class="sxs-lookup"><span data-stu-id="52ed0-140">False</span></span>                             |
| <span data-ttu-id="52ed0-141">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="52ed0-141">Is-Single-Valued</span></span>       | <span data-ttu-id="52ed0-142">Vero</span><span class="sxs-lookup"><span data-stu-id="52ed0-142">True</span></span>                              |
| <span data-ttu-id="52ed0-143">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="52ed0-143">Is Indexed</span></span>             | <span data-ttu-id="52ed0-144">Falso</span><span class="sxs-lookup"><span data-stu-id="52ed0-144">False</span></span>                             |
| <span data-ttu-id="52ed0-145">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="52ed0-145">In Global Catalog</span></span>      | <span data-ttu-id="52ed0-146">Falso</span><span class="sxs-lookup"><span data-stu-id="52ed0-146">False</span></span>                             |
| <span data-ttu-id="52ed0-147">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="52ed0-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="52ed0-148">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="52ed0-148">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="52ed0-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="52ed0-149">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="52ed0-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="52ed0-150">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="52ed0-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="52ed0-151">Search-Flags</span></span>           | <span data-ttu-id="52ed0-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="52ed0-152">0x00000000</span></span>                        |
| <span data-ttu-id="52ed0-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="52ed0-153">System-Flags</span></span>           | <span data-ttu-id="52ed0-154">0x00000011</span><span class="sxs-lookup"><span data-stu-id="52ed0-154">0x00000011</span></span>                        |
| <span data-ttu-id="52ed0-155">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="52ed0-155">Classes used in</span></span>        | [<span data-ttu-id="52ed0-156">**Utente**</span><span class="sxs-lookup"><span data-stu-id="52ed0-156">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="52ed0-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="52ed0-157">Windows Server 2003</span></span>



| <span data-ttu-id="52ed0-158">Voce</span><span class="sxs-lookup"><span data-stu-id="52ed0-158">Entry</span></span> | <span data-ttu-id="52ed0-159">Valore</span><span class="sxs-lookup"><span data-stu-id="52ed0-159">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="52ed0-160">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="52ed0-160">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="52ed0-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="52ed0-161">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="52ed0-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="52ed0-162">System-Only</span></span>            | <span data-ttu-id="52ed0-163">Falso</span><span class="sxs-lookup"><span data-stu-id="52ed0-163">False</span></span>                             |
| <span data-ttu-id="52ed0-164">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="52ed0-164">Is-Single-Valued</span></span>       | <span data-ttu-id="52ed0-165">Vero</span><span class="sxs-lookup"><span data-stu-id="52ed0-165">True</span></span>                              |
| <span data-ttu-id="52ed0-166">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="52ed0-166">Is Indexed</span></span>             | <span data-ttu-id="52ed0-167">Falso</span><span class="sxs-lookup"><span data-stu-id="52ed0-167">False</span></span>                             |
| <span data-ttu-id="52ed0-168">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="52ed0-168">In Global Catalog</span></span>      | <span data-ttu-id="52ed0-169">Falso</span><span class="sxs-lookup"><span data-stu-id="52ed0-169">False</span></span>                             |
| <span data-ttu-id="52ed0-170">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="52ed0-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="52ed0-171">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="52ed0-171">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="52ed0-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="52ed0-172">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="52ed0-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="52ed0-173">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="52ed0-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="52ed0-174">Search-Flags</span></span>           | <span data-ttu-id="52ed0-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="52ed0-175">0x00000000</span></span>                        |
| <span data-ttu-id="52ed0-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="52ed0-176">System-Flags</span></span>           | <span data-ttu-id="52ed0-177">0x00000011</span><span class="sxs-lookup"><span data-stu-id="52ed0-177">0x00000011</span></span>                        |
| <span data-ttu-id="52ed0-178">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="52ed0-178">Classes used in</span></span>        | [<span data-ttu-id="52ed0-179">**Utente**</span><span class="sxs-lookup"><span data-stu-id="52ed0-179">**User**</span></span>](c-user.md)<br/> |



## <a name="adam"></a><span data-ttu-id="52ed0-180">ADAM</span><span class="sxs-lookup"><span data-stu-id="52ed0-180">ADAM</span></span>



| <span data-ttu-id="52ed0-181">Voce</span><span class="sxs-lookup"><span data-stu-id="52ed0-181">Entry</span></span> | <span data-ttu-id="52ed0-182">Valore</span><span class="sxs-lookup"><span data-stu-id="52ed0-182">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="52ed0-183">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="52ed0-183">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="52ed0-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="52ed0-184">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="52ed0-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="52ed0-185">System-Only</span></span>            | <span data-ttu-id="52ed0-186">Vero</span><span class="sxs-lookup"><span data-stu-id="52ed0-186">True</span></span>                                                              |
| <span data-ttu-id="52ed0-187">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="52ed0-187">Is-Single-Valued</span></span>       | <span data-ttu-id="52ed0-188">Vero</span><span class="sxs-lookup"><span data-stu-id="52ed0-188">True</span></span>                                                              |
| <span data-ttu-id="52ed0-189">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="52ed0-189">Is Indexed</span></span>             | <span data-ttu-id="52ed0-190">Falso</span><span class="sxs-lookup"><span data-stu-id="52ed0-190">False</span></span>                                                             |
| <span data-ttu-id="52ed0-191">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="52ed0-191">In Global Catalog</span></span>      | <span data-ttu-id="52ed0-192">Falso</span><span class="sxs-lookup"><span data-stu-id="52ed0-192">False</span></span>                                                             |
| <span data-ttu-id="52ed0-193">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="52ed0-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="52ed0-194">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="52ed0-194">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="52ed0-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="52ed0-195">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="52ed0-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="52ed0-196">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="52ed0-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="52ed0-197">Search-Flags</span></span>           | <span data-ttu-id="52ed0-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="52ed0-198">0x00000000</span></span>                                                        |
| <span data-ttu-id="52ed0-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="52ed0-199">System-Flags</span></span>           | <span data-ttu-id="52ed0-200">0x00000011</span><span class="sxs-lookup"><span data-stu-id="52ed0-200">0x00000011</span></span>                                                        |
| <span data-ttu-id="52ed0-201">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="52ed0-201">Classes used in</span></span>        | [<span data-ttu-id="52ed0-202">**ms-DS-associabile-oggetto**</span><span class="sxs-lookup"><span data-stu-id="52ed0-202">**ms-DS-Bindable-Object**</span></span>](c-msds-bindableobject.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="52ed0-203">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="52ed0-203">Windows Server 2003 R2</span></span>



| <span data-ttu-id="52ed0-204">Voce</span><span class="sxs-lookup"><span data-stu-id="52ed0-204">Entry</span></span> | <span data-ttu-id="52ed0-205">Valore</span><span class="sxs-lookup"><span data-stu-id="52ed0-205">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="52ed0-206">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="52ed0-206">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="52ed0-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="52ed0-207">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="52ed0-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="52ed0-208">System-Only</span></span>            | <span data-ttu-id="52ed0-209">Falso</span><span class="sxs-lookup"><span data-stu-id="52ed0-209">False</span></span>                             |
| <span data-ttu-id="52ed0-210">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="52ed0-210">Is-Single-Valued</span></span>       | <span data-ttu-id="52ed0-211">Vero</span><span class="sxs-lookup"><span data-stu-id="52ed0-211">True</span></span>                              |
| <span data-ttu-id="52ed0-212">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="52ed0-212">Is Indexed</span></span>             | <span data-ttu-id="52ed0-213">Falso</span><span class="sxs-lookup"><span data-stu-id="52ed0-213">False</span></span>                             |
| <span data-ttu-id="52ed0-214">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="52ed0-214">In Global Catalog</span></span>      | <span data-ttu-id="52ed0-215">Falso</span><span class="sxs-lookup"><span data-stu-id="52ed0-215">False</span></span>                             |
| <span data-ttu-id="52ed0-216">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="52ed0-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="52ed0-217">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="52ed0-217">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="52ed0-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="52ed0-218">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="52ed0-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="52ed0-219">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="52ed0-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="52ed0-220">Search-Flags</span></span>           | <span data-ttu-id="52ed0-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="52ed0-221">0x00000000</span></span>                        |
| <span data-ttu-id="52ed0-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="52ed0-222">System-Flags</span></span>           | <span data-ttu-id="52ed0-223">0x00000011</span><span class="sxs-lookup"><span data-stu-id="52ed0-223">0x00000011</span></span>                        |
| <span data-ttu-id="52ed0-224">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="52ed0-224">Classes used in</span></span>        | [<span data-ttu-id="52ed0-225">**Utente**</span><span class="sxs-lookup"><span data-stu-id="52ed0-225">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="52ed0-226">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="52ed0-226">Windows Server 2008</span></span>



| <span data-ttu-id="52ed0-227">Voce</span><span class="sxs-lookup"><span data-stu-id="52ed0-227">Entry</span></span> | <span data-ttu-id="52ed0-228">Valore</span><span class="sxs-lookup"><span data-stu-id="52ed0-228">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="52ed0-229">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="52ed0-229">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="52ed0-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="52ed0-230">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="52ed0-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="52ed0-231">System-Only</span></span>            | <span data-ttu-id="52ed0-232">Falso</span><span class="sxs-lookup"><span data-stu-id="52ed0-232">False</span></span>                             |
| <span data-ttu-id="52ed0-233">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="52ed0-233">Is-Single-Valued</span></span>       | <span data-ttu-id="52ed0-234">Vero</span><span class="sxs-lookup"><span data-stu-id="52ed0-234">True</span></span>                              |
| <span data-ttu-id="52ed0-235">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="52ed0-235">Is Indexed</span></span>             | <span data-ttu-id="52ed0-236">Falso</span><span class="sxs-lookup"><span data-stu-id="52ed0-236">False</span></span>                             |
| <span data-ttu-id="52ed0-237">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="52ed0-237">In Global Catalog</span></span>      | <span data-ttu-id="52ed0-238">Falso</span><span class="sxs-lookup"><span data-stu-id="52ed0-238">False</span></span>                             |
| <span data-ttu-id="52ed0-239">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="52ed0-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="52ed0-240">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="52ed0-240">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="52ed0-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="52ed0-241">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="52ed0-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="52ed0-242">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="52ed0-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="52ed0-243">Search-Flags</span></span>           | <span data-ttu-id="52ed0-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="52ed0-244">0x00000000</span></span>                        |
| <span data-ttu-id="52ed0-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="52ed0-245">System-Flags</span></span>           | <span data-ttu-id="52ed0-246">0x00000011</span><span class="sxs-lookup"><span data-stu-id="52ed0-246">0x00000011</span></span>                        |
| <span data-ttu-id="52ed0-247">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="52ed0-247">Classes used in</span></span>        | [<span data-ttu-id="52ed0-248">**Utente**</span><span class="sxs-lookup"><span data-stu-id="52ed0-248">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="52ed0-249">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="52ed0-249">Windows Server 2008 R2</span></span>



| <span data-ttu-id="52ed0-250">Voce</span><span class="sxs-lookup"><span data-stu-id="52ed0-250">Entry</span></span> | <span data-ttu-id="52ed0-251">Valore</span><span class="sxs-lookup"><span data-stu-id="52ed0-251">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="52ed0-252">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="52ed0-252">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="52ed0-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="52ed0-253">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="52ed0-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="52ed0-254">System-Only</span></span>            | <span data-ttu-id="52ed0-255">Falso</span><span class="sxs-lookup"><span data-stu-id="52ed0-255">False</span></span>                             |
| <span data-ttu-id="52ed0-256">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="52ed0-256">Is-Single-Valued</span></span>       | <span data-ttu-id="52ed0-257">Vero</span><span class="sxs-lookup"><span data-stu-id="52ed0-257">True</span></span>                              |
| <span data-ttu-id="52ed0-258">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="52ed0-258">Is Indexed</span></span>             | <span data-ttu-id="52ed0-259">Falso</span><span class="sxs-lookup"><span data-stu-id="52ed0-259">False</span></span>                             |
| <span data-ttu-id="52ed0-260">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="52ed0-260">In Global Catalog</span></span>      | <span data-ttu-id="52ed0-261">Falso</span><span class="sxs-lookup"><span data-stu-id="52ed0-261">False</span></span>                             |
| <span data-ttu-id="52ed0-262">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="52ed0-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="52ed0-263">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="52ed0-263">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="52ed0-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="52ed0-264">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="52ed0-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="52ed0-265">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="52ed0-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="52ed0-266">Search-Flags</span></span>           | <span data-ttu-id="52ed0-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="52ed0-267">0x00000000</span></span>                        |
| <span data-ttu-id="52ed0-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="52ed0-268">System-Flags</span></span>           | <span data-ttu-id="52ed0-269">0x00000011</span><span class="sxs-lookup"><span data-stu-id="52ed0-269">0x00000011</span></span>                        |
| <span data-ttu-id="52ed0-270">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="52ed0-270">Classes used in</span></span>        | [<span data-ttu-id="52ed0-271">**Utente**</span><span class="sxs-lookup"><span data-stu-id="52ed0-271">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="52ed0-272">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="52ed0-272">Windows Server 2012</span></span>



| <span data-ttu-id="52ed0-273">Voce</span><span class="sxs-lookup"><span data-stu-id="52ed0-273">Entry</span></span> | <span data-ttu-id="52ed0-274">Valore</span><span class="sxs-lookup"><span data-stu-id="52ed0-274">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="52ed0-275">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="52ed0-275">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="52ed0-276">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="52ed0-276">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="52ed0-277">System-Only</span><span class="sxs-lookup"><span data-stu-id="52ed0-277">System-Only</span></span>            | <span data-ttu-id="52ed0-278">Falso</span><span class="sxs-lookup"><span data-stu-id="52ed0-278">False</span></span>                             |
| <span data-ttu-id="52ed0-279">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="52ed0-279">Is-Single-Valued</span></span>       | <span data-ttu-id="52ed0-280">Vero</span><span class="sxs-lookup"><span data-stu-id="52ed0-280">True</span></span>                              |
| <span data-ttu-id="52ed0-281">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="52ed0-281">Is Indexed</span></span>             | <span data-ttu-id="52ed0-282">Falso</span><span class="sxs-lookup"><span data-stu-id="52ed0-282">False</span></span>                             |
| <span data-ttu-id="52ed0-283">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="52ed0-283">In Global Catalog</span></span>      | <span data-ttu-id="52ed0-284">Falso</span><span class="sxs-lookup"><span data-stu-id="52ed0-284">False</span></span>                             |
| <span data-ttu-id="52ed0-285">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="52ed0-285">NT-Security-Descriptor</span></span> | <span data-ttu-id="52ed0-286">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="52ed0-286">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="52ed0-287">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="52ed0-287">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="52ed0-288">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="52ed0-288">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="52ed0-289">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="52ed0-289">Search-Flags</span></span>           | <span data-ttu-id="52ed0-290">0x00000000</span><span class="sxs-lookup"><span data-stu-id="52ed0-290">0x00000000</span></span>                        |
| <span data-ttu-id="52ed0-291">System-Flags</span><span class="sxs-lookup"><span data-stu-id="52ed0-291">System-Flags</span></span>           | <span data-ttu-id="52ed0-292">0x00000011</span><span class="sxs-lookup"><span data-stu-id="52ed0-292">0x00000011</span></span>                        |
| <span data-ttu-id="52ed0-293">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="52ed0-293">Classes used in</span></span>        | [<span data-ttu-id="52ed0-294">**Utente**</span><span class="sxs-lookup"><span data-stu-id="52ed0-294">**User**</span></span>](c-user.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="52ed0-295">Commenti</span><span class="sxs-lookup"><span data-stu-id="52ed0-295">Remarks</span></span>

<span data-ttu-id="52ed0-296">Questo attributo non viene replicato e viene mantenuto separatamente in ogni controller di dominio nel dominio.</span><span class="sxs-lookup"><span data-stu-id="52ed0-296">This attribute is not replicated and is maintained separately on each domain controller in the domain.</span></span>

<span data-ttu-id="52ed0-297">Questo attributo viene reimpostato su un controller di dominio specifico quando l'utente accede correttamente a tale controller di dominio.</span><span class="sxs-lookup"><span data-stu-id="52ed0-297">This attribute is reset on a specific domain controller when the user successfully logs onto that domain controller.</span></span>

 

 





