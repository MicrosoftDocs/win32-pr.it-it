---
title: Attributo User-Account-Control
description: Flag che controllano il comportamento dell'account utente.
ms.assetid: fc81a16a-f537-44cc-957c-5d7ca66b9755
ms.tgt_platform: multiple
keywords:
- Schema di AD dell'attributo di controllo dell'account utente
- Schema AD dell'attributo userAccountControl
topic_type:
- apiref
api_name:
- User-Account-Control
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f60297d22aad76b229c691a667ac22a87271402c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104122634"
---
# <a name="user-account-control-attribute"></a><span data-ttu-id="7e9d3-105">Attributo User-Account-Control</span><span class="sxs-lookup"><span data-stu-id="7e9d3-105">User-Account-Control attribute</span></span>

<span data-ttu-id="7e9d3-106">Flag che controllano il comportamento dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="7e9d3-106">Flags that control the behavior of the user account.</span></span>



| <span data-ttu-id="7e9d3-107">Voce</span><span class="sxs-lookup"><span data-stu-id="7e9d3-107">Entry</span></span> | <span data-ttu-id="7e9d3-108">Valore</span><span class="sxs-lookup"><span data-stu-id="7e9d3-108">Value</span></span> |
|-------------------|---------------------------------------|
| <span data-ttu-id="7e9d3-109">CN</span><span class="sxs-lookup"><span data-stu-id="7e9d3-109">CN</span></span>                | <span data-ttu-id="7e9d3-110">Controllo account utente</span><span class="sxs-lookup"><span data-stu-id="7e9d3-110">User-Account-Control</span></span>                  |
| <span data-ttu-id="7e9d3-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="7e9d3-111">Ldap-Display-Name</span></span> | <span data-ttu-id="7e9d3-112">userAccountControl</span><span class="sxs-lookup"><span data-stu-id="7e9d3-112">userAccountControl</span></span>                    |
| <span data-ttu-id="7e9d3-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="7e9d3-113">Size</span></span>              | <span data-ttu-id="7e9d3-114">4 byte.</span><span class="sxs-lookup"><span data-stu-id="7e9d3-114">4 bytes.</span></span>                              |
| <span data-ttu-id="7e9d3-115">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="7e9d3-115">Update Privilege</span></span>  | <span data-ttu-id="7e9d3-116">Questo valore viene impostato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="7e9d3-116">This value is set by the system.</span></span>      |
| <span data-ttu-id="7e9d3-117">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="7e9d3-117">Update Frequency</span></span>  | <span data-ttu-id="7e9d3-118">Ogni volta che i criteri dell'account cambiano.</span><span class="sxs-lookup"><span data-stu-id="7e9d3-118">Each time the account policy changes.</span></span> |
| <span data-ttu-id="7e9d3-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="7e9d3-119">Attribute-Id</span></span>      | <span data-ttu-id="7e9d3-120">1.2.840.113556.1.4.8</span><span class="sxs-lookup"><span data-stu-id="7e9d3-120">1.2.840.113556.1.4.8</span></span>                  |
| <span data-ttu-id="7e9d3-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="7e9d3-121">System-Id-Guid</span></span>    | <span data-ttu-id="7e9d3-122">bf967a68-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="7e9d3-122">bf967a68-0de6-11d0-a285-00aa003049e2</span></span>  |
| <span data-ttu-id="7e9d3-123">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7e9d3-123">Syntax</span></span>            | [<span data-ttu-id="7e9d3-124">**Enumerazione**</span><span class="sxs-lookup"><span data-stu-id="7e9d3-124">**Enumeration**</span></span>](s-enumeration.md)  |



## <a name="implementations"></a><span data-ttu-id="7e9d3-125">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="7e9d3-125">Implementations</span></span>

-   [<span data-ttu-id="7e9d3-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="7e9d3-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="7e9d3-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="7e9d3-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="7e9d3-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="7e9d3-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="7e9d3-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="7e9d3-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="7e9d3-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="7e9d3-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="7e9d3-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="7e9d3-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="7e9d3-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7e9d3-132">Windows 2000 Server</span></span>



| <span data-ttu-id="7e9d3-133">Voce</span><span class="sxs-lookup"><span data-stu-id="7e9d3-133">Entry</span></span> | <span data-ttu-id="7e9d3-134">Valore</span><span class="sxs-lookup"><span data-stu-id="7e9d3-134">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="7e9d3-135">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="7e9d3-135">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="7e9d3-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7e9d3-136">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="7e9d3-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="7e9d3-137">System-Only</span></span>            | <span data-ttu-id="7e9d3-138">Falso</span><span class="sxs-lookup"><span data-stu-id="7e9d3-138">False</span></span>                             |
| <span data-ttu-id="7e9d3-139">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="7e9d3-139">Is-Single-Valued</span></span>       | <span data-ttu-id="7e9d3-140">Vero</span><span class="sxs-lookup"><span data-stu-id="7e9d3-140">True</span></span>                              |
| <span data-ttu-id="7e9d3-141">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="7e9d3-141">Is Indexed</span></span>             | <span data-ttu-id="7e9d3-142">Vero</span><span class="sxs-lookup"><span data-stu-id="7e9d3-142">True</span></span>                              |
| <span data-ttu-id="7e9d3-143">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="7e9d3-143">In Global Catalog</span></span>      | <span data-ttu-id="7e9d3-144">Vero</span><span class="sxs-lookup"><span data-stu-id="7e9d3-144">True</span></span>                              |
| <span data-ttu-id="7e9d3-145">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="7e9d3-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="7e9d3-146">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="7e9d3-146">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="7e9d3-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7e9d3-147">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="7e9d3-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7e9d3-148">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="7e9d3-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7e9d3-149">Search-Flags</span></span>           | <span data-ttu-id="7e9d3-150">0x00000019</span><span class="sxs-lookup"><span data-stu-id="7e9d3-150">0x00000019</span></span>                        |
| <span data-ttu-id="7e9d3-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7e9d3-151">System-Flags</span></span>           | <span data-ttu-id="7e9d3-152">0x00000012</span><span class="sxs-lookup"><span data-stu-id="7e9d3-152">0x00000012</span></span>                        |
| <span data-ttu-id="7e9d3-153">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="7e9d3-153">Classes used in</span></span>        | [<span data-ttu-id="7e9d3-154">**Utente**</span><span class="sxs-lookup"><span data-stu-id="7e9d3-154">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="7e9d3-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7e9d3-155">Windows Server 2003</span></span>



| <span data-ttu-id="7e9d3-156">Voce</span><span class="sxs-lookup"><span data-stu-id="7e9d3-156">Entry</span></span> | <span data-ttu-id="7e9d3-157">Valore</span><span class="sxs-lookup"><span data-stu-id="7e9d3-157">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="7e9d3-158">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="7e9d3-158">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="7e9d3-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7e9d3-159">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="7e9d3-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="7e9d3-160">System-Only</span></span>            | <span data-ttu-id="7e9d3-161">Falso</span><span class="sxs-lookup"><span data-stu-id="7e9d3-161">False</span></span>                             |
| <span data-ttu-id="7e9d3-162">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="7e9d3-162">Is-Single-Valued</span></span>       | <span data-ttu-id="7e9d3-163">Vero</span><span class="sxs-lookup"><span data-stu-id="7e9d3-163">True</span></span>                              |
| <span data-ttu-id="7e9d3-164">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="7e9d3-164">Is Indexed</span></span>             | <span data-ttu-id="7e9d3-165">Vero</span><span class="sxs-lookup"><span data-stu-id="7e9d3-165">True</span></span>                              |
| <span data-ttu-id="7e9d3-166">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="7e9d3-166">In Global Catalog</span></span>      | <span data-ttu-id="7e9d3-167">Vero</span><span class="sxs-lookup"><span data-stu-id="7e9d3-167">True</span></span>                              |
| <span data-ttu-id="7e9d3-168">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="7e9d3-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="7e9d3-169">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="7e9d3-169">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="7e9d3-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7e9d3-170">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="7e9d3-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7e9d3-171">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="7e9d3-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7e9d3-172">Search-Flags</span></span>           | <span data-ttu-id="7e9d3-173">0x00000019</span><span class="sxs-lookup"><span data-stu-id="7e9d3-173">0x00000019</span></span>                        |
| <span data-ttu-id="7e9d3-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7e9d3-174">System-Flags</span></span>           | <span data-ttu-id="7e9d3-175">0x00000012</span><span class="sxs-lookup"><span data-stu-id="7e9d3-175">0x00000012</span></span>                        |
| <span data-ttu-id="7e9d3-176">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="7e9d3-176">Classes used in</span></span>        | [<span data-ttu-id="7e9d3-177">**Utente**</span><span class="sxs-lookup"><span data-stu-id="7e9d3-177">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="7e9d3-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="7e9d3-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="7e9d3-179">Voce</span><span class="sxs-lookup"><span data-stu-id="7e9d3-179">Entry</span></span> | <span data-ttu-id="7e9d3-180">Valore</span><span class="sxs-lookup"><span data-stu-id="7e9d3-180">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="7e9d3-181">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="7e9d3-181">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="7e9d3-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7e9d3-182">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="7e9d3-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="7e9d3-183">System-Only</span></span>            | <span data-ttu-id="7e9d3-184">Falso</span><span class="sxs-lookup"><span data-stu-id="7e9d3-184">False</span></span>                             |
| <span data-ttu-id="7e9d3-185">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="7e9d3-185">Is-Single-Valued</span></span>       | <span data-ttu-id="7e9d3-186">Vero</span><span class="sxs-lookup"><span data-stu-id="7e9d3-186">True</span></span>                              |
| <span data-ttu-id="7e9d3-187">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="7e9d3-187">Is Indexed</span></span>             | <span data-ttu-id="7e9d3-188">Vero</span><span class="sxs-lookup"><span data-stu-id="7e9d3-188">True</span></span>                              |
| <span data-ttu-id="7e9d3-189">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="7e9d3-189">In Global Catalog</span></span>      | <span data-ttu-id="7e9d3-190">Vero</span><span class="sxs-lookup"><span data-stu-id="7e9d3-190">True</span></span>                              |
| <span data-ttu-id="7e9d3-191">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="7e9d3-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="7e9d3-192">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="7e9d3-192">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="7e9d3-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7e9d3-193">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="7e9d3-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7e9d3-194">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="7e9d3-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7e9d3-195">Search-Flags</span></span>           | <span data-ttu-id="7e9d3-196">0x00000019</span><span class="sxs-lookup"><span data-stu-id="7e9d3-196">0x00000019</span></span>                        |
| <span data-ttu-id="7e9d3-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7e9d3-197">System-Flags</span></span>           | <span data-ttu-id="7e9d3-198">0x00000012</span><span class="sxs-lookup"><span data-stu-id="7e9d3-198">0x00000012</span></span>                        |
| <span data-ttu-id="7e9d3-199">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="7e9d3-199">Classes used in</span></span>        | [<span data-ttu-id="7e9d3-200">**Utente**</span><span class="sxs-lookup"><span data-stu-id="7e9d3-200">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="7e9d3-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7e9d3-201">Windows Server 2008</span></span>



| <span data-ttu-id="7e9d3-202">Voce</span><span class="sxs-lookup"><span data-stu-id="7e9d3-202">Entry</span></span> | <span data-ttu-id="7e9d3-203">Valore</span><span class="sxs-lookup"><span data-stu-id="7e9d3-203">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="7e9d3-204">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="7e9d3-204">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="7e9d3-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7e9d3-205">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="7e9d3-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="7e9d3-206">System-Only</span></span>            | <span data-ttu-id="7e9d3-207">Falso</span><span class="sxs-lookup"><span data-stu-id="7e9d3-207">False</span></span>                             |
| <span data-ttu-id="7e9d3-208">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="7e9d3-208">Is-Single-Valued</span></span>       | <span data-ttu-id="7e9d3-209">Vero</span><span class="sxs-lookup"><span data-stu-id="7e9d3-209">True</span></span>                              |
| <span data-ttu-id="7e9d3-210">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="7e9d3-210">Is Indexed</span></span>             | <span data-ttu-id="7e9d3-211">Vero</span><span class="sxs-lookup"><span data-stu-id="7e9d3-211">True</span></span>                              |
| <span data-ttu-id="7e9d3-212">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="7e9d3-212">In Global Catalog</span></span>      | <span data-ttu-id="7e9d3-213">Vero</span><span class="sxs-lookup"><span data-stu-id="7e9d3-213">True</span></span>                              |
| <span data-ttu-id="7e9d3-214">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="7e9d3-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="7e9d3-215">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="7e9d3-215">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="7e9d3-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7e9d3-216">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="7e9d3-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7e9d3-217">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="7e9d3-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7e9d3-218">Search-Flags</span></span>           | <span data-ttu-id="7e9d3-219">0x00000019</span><span class="sxs-lookup"><span data-stu-id="7e9d3-219">0x00000019</span></span>                        |
| <span data-ttu-id="7e9d3-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7e9d3-220">System-Flags</span></span>           | <span data-ttu-id="7e9d3-221">0x00000012</span><span class="sxs-lookup"><span data-stu-id="7e9d3-221">0x00000012</span></span>                        |
| <span data-ttu-id="7e9d3-222">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="7e9d3-222">Classes used in</span></span>        | [<span data-ttu-id="7e9d3-223">**Utente**</span><span class="sxs-lookup"><span data-stu-id="7e9d3-223">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="7e9d3-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7e9d3-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="7e9d3-225">Voce</span><span class="sxs-lookup"><span data-stu-id="7e9d3-225">Entry</span></span> | <span data-ttu-id="7e9d3-226">Valore</span><span class="sxs-lookup"><span data-stu-id="7e9d3-226">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="7e9d3-227">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="7e9d3-227">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="7e9d3-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7e9d3-228">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="7e9d3-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="7e9d3-229">System-Only</span></span>            | <span data-ttu-id="7e9d3-230">Falso</span><span class="sxs-lookup"><span data-stu-id="7e9d3-230">False</span></span>                             |
| <span data-ttu-id="7e9d3-231">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="7e9d3-231">Is-Single-Valued</span></span>       | <span data-ttu-id="7e9d3-232">Vero</span><span class="sxs-lookup"><span data-stu-id="7e9d3-232">True</span></span>                              |
| <span data-ttu-id="7e9d3-233">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="7e9d3-233">Is Indexed</span></span>             | <span data-ttu-id="7e9d3-234">Vero</span><span class="sxs-lookup"><span data-stu-id="7e9d3-234">True</span></span>                              |
| <span data-ttu-id="7e9d3-235">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="7e9d3-235">In Global Catalog</span></span>      | <span data-ttu-id="7e9d3-236">Vero</span><span class="sxs-lookup"><span data-stu-id="7e9d3-236">True</span></span>                              |
| <span data-ttu-id="7e9d3-237">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="7e9d3-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="7e9d3-238">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="7e9d3-238">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="7e9d3-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7e9d3-239">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="7e9d3-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7e9d3-240">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="7e9d3-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7e9d3-241">Search-Flags</span></span>           | <span data-ttu-id="7e9d3-242">0x00000019</span><span class="sxs-lookup"><span data-stu-id="7e9d3-242">0x00000019</span></span>                        |
| <span data-ttu-id="7e9d3-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7e9d3-243">System-Flags</span></span>           | <span data-ttu-id="7e9d3-244">0x00000012</span><span class="sxs-lookup"><span data-stu-id="7e9d3-244">0x00000012</span></span>                        |
| <span data-ttu-id="7e9d3-245">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="7e9d3-245">Classes used in</span></span>        | [<span data-ttu-id="7e9d3-246">**Utente**</span><span class="sxs-lookup"><span data-stu-id="7e9d3-246">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="7e9d3-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7e9d3-247">Windows Server 2012</span></span>



| <span data-ttu-id="7e9d3-248">Voce</span><span class="sxs-lookup"><span data-stu-id="7e9d3-248">Entry</span></span> | <span data-ttu-id="7e9d3-249">Valore</span><span class="sxs-lookup"><span data-stu-id="7e9d3-249">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="7e9d3-250">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="7e9d3-250">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="7e9d3-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7e9d3-251">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="7e9d3-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="7e9d3-252">System-Only</span></span>            | <span data-ttu-id="7e9d3-253">Falso</span><span class="sxs-lookup"><span data-stu-id="7e9d3-253">False</span></span>                             |
| <span data-ttu-id="7e9d3-254">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="7e9d3-254">Is-Single-Valued</span></span>       | <span data-ttu-id="7e9d3-255">Vero</span><span class="sxs-lookup"><span data-stu-id="7e9d3-255">True</span></span>                              |
| <span data-ttu-id="7e9d3-256">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="7e9d3-256">Is Indexed</span></span>             | <span data-ttu-id="7e9d3-257">Vero</span><span class="sxs-lookup"><span data-stu-id="7e9d3-257">True</span></span>                              |
| <span data-ttu-id="7e9d3-258">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="7e9d3-258">In Global Catalog</span></span>      | <span data-ttu-id="7e9d3-259">Vero</span><span class="sxs-lookup"><span data-stu-id="7e9d3-259">True</span></span>                              |
| <span data-ttu-id="7e9d3-260">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="7e9d3-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="7e9d3-261">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="7e9d3-261">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="7e9d3-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7e9d3-262">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="7e9d3-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7e9d3-263">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="7e9d3-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7e9d3-264">Search-Flags</span></span>           | <span data-ttu-id="7e9d3-265">0x00000019</span><span class="sxs-lookup"><span data-stu-id="7e9d3-265">0x00000019</span></span>                        |
| <span data-ttu-id="7e9d3-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7e9d3-266">System-Flags</span></span>           | <span data-ttu-id="7e9d3-267">0x00000012</span><span class="sxs-lookup"><span data-stu-id="7e9d3-267">0x00000012</span></span>                        |
| <span data-ttu-id="7e9d3-268">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="7e9d3-268">Classes used in</span></span>        | [<span data-ttu-id="7e9d3-269">**Utente**</span><span class="sxs-lookup"><span data-stu-id="7e9d3-269">**User**</span></span>](c-user.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="7e9d3-270">Commenti</span><span class="sxs-lookup"><span data-stu-id="7e9d3-270">Remarks</span></span>

<span data-ttu-id="7e9d3-271">Il valore di questo attributo può essere zero o una combinazione di uno o più dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="7e9d3-271">This attribute value can be zero or a combination of one or more of the following values.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7e9d3-272">Valore esadecimale</span><span class="sxs-lookup"><span data-stu-id="7e9d3-272">Hexadecimal value</span></span></th>
<th><span data-ttu-id="7e9d3-273">Identificatore (definito in IADs. h)</span><span class="sxs-lookup"><span data-stu-id="7e9d3-273">Identifier (defined in iads.h)</span></span></th>
<th><span data-ttu-id="7e9d3-274">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7e9d3-274">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7e9d3-275">0x00000001</span><span class="sxs-lookup"><span data-stu-id="7e9d3-275">0x00000001</span></span></td>
<td><span data-ttu-id="7e9d3-276"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_SCRIPT</strong></a></span><span class="sxs-lookup"><span data-stu-id="7e9d3-276"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_SCRIPT</strong></a></span></span></td>
<td><span data-ttu-id="7e9d3-277">Lo script di accesso viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7e9d3-277">The logon script is executed.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7e9d3-278">0x00000002</span><span class="sxs-lookup"><span data-stu-id="7e9d3-278">0x00000002</span></span></td>
<td><span data-ttu-id="7e9d3-279"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_ACCOUNTDISABLE</strong></a></span><span class="sxs-lookup"><span data-stu-id="7e9d3-279"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_ACCOUNTDISABLE</strong></a></span></span></td>
<td><span data-ttu-id="7e9d3-280">L'account utente è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="7e9d3-280">The user account is disabled.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7e9d3-281">0x00000008</span><span class="sxs-lookup"><span data-stu-id="7e9d3-281">0x00000008</span></span></td>
<td><span data-ttu-id="7e9d3-282"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_HOMEDIR_REQUIRED</strong></a></span><span class="sxs-lookup"><span data-stu-id="7e9d3-282"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_HOMEDIR_REQUIRED</strong></a></span></span></td>
<td><span data-ttu-id="7e9d3-283">La home directory è obbligatoria.</span><span class="sxs-lookup"><span data-stu-id="7e9d3-283">The home directory is required.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7e9d3-284">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7e9d3-284">0x00000010</span></span></td>
<td><span data-ttu-id="7e9d3-285"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_LOCKOUT</strong></a></span><span class="sxs-lookup"><span data-stu-id="7e9d3-285"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_LOCKOUT</strong></a></span></span></td>
<td><span data-ttu-id="7e9d3-286">L'account è attualmente bloccato.</span><span class="sxs-lookup"><span data-stu-id="7e9d3-286">The account is currently locked out.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7e9d3-287">0x00000020</span><span class="sxs-lookup"><span data-stu-id="7e9d3-287">0x00000020</span></span></td>
<td><span data-ttu-id="7e9d3-288"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_PASSWD_NOTREQD</strong></a></span><span class="sxs-lookup"><span data-stu-id="7e9d3-288"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_PASSWD_NOTREQD</strong></a></span></span></td>
<td><span data-ttu-id="7e9d3-289">Non è necessaria alcuna password.</span><span class="sxs-lookup"><span data-stu-id="7e9d3-289">No password is required.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7e9d3-290">0x00000040</span><span class="sxs-lookup"><span data-stu-id="7e9d3-290">0x00000040</span></span></td>
<td><span data-ttu-id="7e9d3-291"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_PASSWD_CANT_CHANGE</strong></a></span><span class="sxs-lookup"><span data-stu-id="7e9d3-291"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_PASSWD_CANT_CHANGE</strong></a></span></span></td>
<td><span data-ttu-id="7e9d3-292">L'utente non può modificare la password.</span><span class="sxs-lookup"><span data-stu-id="7e9d3-292">The user cannot change the password.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="7e9d3-293">Non è possibile assegnare le impostazioni delle autorizzazioni di PASSWD_CANT_CHANGE modificando direttamente l'attributo UserAccountControl.</span><span class="sxs-lookup"><span data-stu-id="7e9d3-293">You cannot assign the permission settings of PASSWD_CANT_CHANGE by directly modifying the UserAccountControl attribute.</span></span> <span data-ttu-id="7e9d3-294">Per ulteriori informazioni e un esempio di codice in cui viene illustrato come impedire a un utente di modificare la password, vedere l' <a href="/windows/desktop/ADSI/user-cannot-change-password">utente non può modificare la password</a>.</span><span class="sxs-lookup"><span data-stu-id="7e9d3-294">For more information and a code example that shows how to prevent a user from changing the password, see <a href="/windows/desktop/ADSI/user-cannot-change-password">User Cannot Change Password</a>.</span></span>
</blockquote>
<br/> <span data-ttu-id="7e9d3-295">:</span><span class="sxs-lookup"><span data-stu-id="7e9d3-295">:</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7e9d3-296">0x00000080</span><span class="sxs-lookup"><span data-stu-id="7e9d3-296">0x00000080</span></span></td>
<td><span data-ttu-id="7e9d3-297"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_ENCRYPTED_TEXT_PASSWORD_ALLOWED</strong></a></span><span class="sxs-lookup"><span data-stu-id="7e9d3-297"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_ENCRYPTED_TEXT_PASSWORD_ALLOWED</strong></a></span></span></td>
<td><span data-ttu-id="7e9d3-298">L'utente può inviare una password crittografata.</span><span class="sxs-lookup"><span data-stu-id="7e9d3-298">The user can send an encrypted password.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7e9d3-299">0x00000100</span><span class="sxs-lookup"><span data-stu-id="7e9d3-299">0x00000100</span></span></td>
<td><span data-ttu-id="7e9d3-300"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_TEMP_DUPLICATE_ACCOUNT</strong></a></span><span class="sxs-lookup"><span data-stu-id="7e9d3-300"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_TEMP_DUPLICATE_ACCOUNT</strong></a></span></span></td>
<td><span data-ttu-id="7e9d3-301">Si tratta di un account per gli utenti il cui account primario si trova in un altro dominio.</span><span class="sxs-lookup"><span data-stu-id="7e9d3-301">This is an account for users whose primary account is in another domain.</span></span> <span data-ttu-id="7e9d3-302">Questo account fornisce l'accesso utente al dominio, ma non a un dominio che considera attendibile il dominio.</span><span class="sxs-lookup"><span data-stu-id="7e9d3-302">This account provides user access to this domain, but not to any domain that trusts this domain.</span></span> <span data-ttu-id="7e9d3-303">Noto anche come account utente locale.</span><span class="sxs-lookup"><span data-stu-id="7e9d3-303">Also known as a local user account.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7e9d3-304">0x00000200</span><span class="sxs-lookup"><span data-stu-id="7e9d3-304">0x00000200</span></span></td>
<td><span data-ttu-id="7e9d3-305"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_NORMAL_ACCOUNT</strong></a></span><span class="sxs-lookup"><span data-stu-id="7e9d3-305"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_NORMAL_ACCOUNT</strong></a></span></span></td>
<td><span data-ttu-id="7e9d3-306">Si tratta di un tipo di account predefinito che rappresenta un utente tipico.</span><span class="sxs-lookup"><span data-stu-id="7e9d3-306">This is a default account type that represents a typical user.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7e9d3-307">0x00000800</span><span class="sxs-lookup"><span data-stu-id="7e9d3-307">0x00000800</span></span></td>
<td><span data-ttu-id="7e9d3-308"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_INTERDOMAIN_TRUST_ACCOUNT</strong></a></span><span class="sxs-lookup"><span data-stu-id="7e9d3-308"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_INTERDOMAIN_TRUST_ACCOUNT</strong></a></span></span></td>
<td><span data-ttu-id="7e9d3-309">Si tratta di un permesso per considerare attendibile un dominio di sistema che considera attendibili altri domini.</span><span class="sxs-lookup"><span data-stu-id="7e9d3-309">This is a permit to trust account for a system domain that trusts other domains.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7e9d3-310">0x00001000</span><span class="sxs-lookup"><span data-stu-id="7e9d3-310">0x00001000</span></span></td>
<td><span data-ttu-id="7e9d3-311"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_WORKSTATION_TRUST_ACCOUNT</strong></a></span><span class="sxs-lookup"><span data-stu-id="7e9d3-311"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_WORKSTATION_TRUST_ACCOUNT</strong></a></span></span></td>
<td><span data-ttu-id="7e9d3-312">Si tratta di un account computer di un computer membro di questo dominio.</span><span class="sxs-lookup"><span data-stu-id="7e9d3-312">This is a computer account for a computer that is a member of this domain.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7e9d3-313">0x00002000</span><span class="sxs-lookup"><span data-stu-id="7e9d3-313">0x00002000</span></span></td>
<td><span data-ttu-id="7e9d3-314"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_SERVER_TRUST_ACCOUNT</strong></a></span><span class="sxs-lookup"><span data-stu-id="7e9d3-314"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_SERVER_TRUST_ACCOUNT</strong></a></span></span></td>
<td><span data-ttu-id="7e9d3-315">Si tratta di un account computer di un controller di dominio di backup del sistema che è membro di questo dominio.</span><span class="sxs-lookup"><span data-stu-id="7e9d3-315">This is a computer account for a system backup domain controller that is a member of this domain.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7e9d3-316">0x00004000</span><span class="sxs-lookup"><span data-stu-id="7e9d3-316">0x00004000</span></span></td>
<td><span data-ttu-id="7e9d3-317">N/D</span><span class="sxs-lookup"><span data-stu-id="7e9d3-317">N/A</span></span></td>
<td><span data-ttu-id="7e9d3-318">Non usato.</span><span class="sxs-lookup"><span data-stu-id="7e9d3-318">Not used.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7e9d3-319">0x00008000</span><span class="sxs-lookup"><span data-stu-id="7e9d3-319">0x00008000</span></span></td>
<td><span data-ttu-id="7e9d3-320">N/D</span><span class="sxs-lookup"><span data-stu-id="7e9d3-320">N/A</span></span></td>
<td><span data-ttu-id="7e9d3-321">Non usato.</span><span class="sxs-lookup"><span data-stu-id="7e9d3-321">Not used.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7e9d3-322">0x00010000</span><span class="sxs-lookup"><span data-stu-id="7e9d3-322">0x00010000</span></span></td>
<td><span data-ttu-id="7e9d3-323"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_DONT_EXPIRE_PASSWD</strong></a></span><span class="sxs-lookup"><span data-stu-id="7e9d3-323"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_DONT_EXPIRE_PASSWD</strong></a></span></span></td>
<td><span data-ttu-id="7e9d3-324">La password per questo account non scadrà mai.</span><span class="sxs-lookup"><span data-stu-id="7e9d3-324">The password for this account will never expire.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7e9d3-325">0x00020000</span><span class="sxs-lookup"><span data-stu-id="7e9d3-325">0x00020000</span></span></td>
<td><span data-ttu-id="7e9d3-326"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_MNS_LOGON_ACCOUNT</strong></a></span><span class="sxs-lookup"><span data-stu-id="7e9d3-326"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_MNS_LOGON_ACCOUNT</strong></a></span></span></td>
<td><span data-ttu-id="7e9d3-327">Si tratta di un account di accesso MNS.</span><span class="sxs-lookup"><span data-stu-id="7e9d3-327">This is an MNS logon account.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7e9d3-328">0x00040000</span><span class="sxs-lookup"><span data-stu-id="7e9d3-328">0x00040000</span></span></td>
<td><span data-ttu-id="7e9d3-329"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_SMARTCARD_REQUIRED</strong></a></span><span class="sxs-lookup"><span data-stu-id="7e9d3-329"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_SMARTCARD_REQUIRED</strong></a></span></span></td>
<td><span data-ttu-id="7e9d3-330">L'utente deve accedere usando una smart card.</span><span class="sxs-lookup"><span data-stu-id="7e9d3-330">The user must log on using a smart card.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7e9d3-331">0x00080000</span><span class="sxs-lookup"><span data-stu-id="7e9d3-331">0x00080000</span></span></td>
<td><span data-ttu-id="7e9d3-332"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_TRUSTED_FOR_DELEGATION</strong></a></span><span class="sxs-lookup"><span data-stu-id="7e9d3-332"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_TRUSTED_FOR_DELEGATION</strong></a></span></span></td>
<td><span data-ttu-id="7e9d3-333">L'account di servizio (utente o account computer) in cui viene eseguito un servizio è considerato attendibile per la delega Kerberos.</span><span class="sxs-lookup"><span data-stu-id="7e9d3-333">The service account (user or computer account), under which a service runs, is trusted for Kerberos delegation.</span></span> <span data-ttu-id="7e9d3-334">Un servizio di questo tipo può rappresentare un client che richiede il servizio.</span><span class="sxs-lookup"><span data-stu-id="7e9d3-334">Any such service can impersonate a client requesting the service.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7e9d3-335">0x00100000</span><span class="sxs-lookup"><span data-stu-id="7e9d3-335">0x00100000</span></span></td>
<td><span data-ttu-id="7e9d3-336"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_NOT_DELEGATED</strong></a></span><span class="sxs-lookup"><span data-stu-id="7e9d3-336"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_NOT_DELEGATED</strong></a></span></span></td>
<td><span data-ttu-id="7e9d3-337">Il contesto di sicurezza dell'utente non verrà delegato a un servizio, anche se l'account del servizio è impostato come attendibile per la delega Kerberos.</span><span class="sxs-lookup"><span data-stu-id="7e9d3-337">The security context of the user will not be delegated to a service even if the service account is set as trusted for Kerberos delegation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7e9d3-338">0x00200000</span><span class="sxs-lookup"><span data-stu-id="7e9d3-338">0x00200000</span></span></td>
<td><span data-ttu-id="7e9d3-339"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_USE_DES_KEY_ONLY</strong></a></span><span class="sxs-lookup"><span data-stu-id="7e9d3-339"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_USE_DES_KEY_ONLY</strong></a></span></span></td>
<td><span data-ttu-id="7e9d3-340">Limitare questa entità all'uso solo dei tipi di crittografia DES (Data Encryption Standard) per le chiavi.</span><span class="sxs-lookup"><span data-stu-id="7e9d3-340">Restrict this principal to use only Data Encryption Standard (DES) encryption types for keys.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7e9d3-341">0x00400000</span><span class="sxs-lookup"><span data-stu-id="7e9d3-341">0x00400000</span></span></td>
<td><span data-ttu-id="7e9d3-342"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_DONT_REQUIRE_PREAUTH</strong></a></span><span class="sxs-lookup"><span data-stu-id="7e9d3-342"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_DONT_REQUIRE_PREAUTH</strong></a></span></span></td>
<td><span data-ttu-id="7e9d3-343">Questo account non richiede l'autenticazione preliminare Kerberos per l'accesso.</span><span class="sxs-lookup"><span data-stu-id="7e9d3-343">This account does not require Kerberos pre-authentication for logon.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7e9d3-344">0x00800000</span><span class="sxs-lookup"><span data-stu-id="7e9d3-344">0x00800000</span></span></td>
<td><span data-ttu-id="7e9d3-345"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_PASSWORD_EXPIRED</strong></a></span><span class="sxs-lookup"><span data-stu-id="7e9d3-345"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_PASSWORD_EXPIRED</strong></a></span></span></td>
<td><span data-ttu-id="7e9d3-346">La password dell'utente è scaduta.</span><span class="sxs-lookup"><span data-stu-id="7e9d3-346">The user password has expired.</span></span> <span data-ttu-id="7e9d3-347">Questo flag viene creato dal sistema utilizzando i dati dell'attributo <a href="a-pwdlastset.md"><strong>pwd-Last-Set</strong></a> e dei criteri di dominio.</span><span class="sxs-lookup"><span data-stu-id="7e9d3-347">This flag is created by the system using data from the <a href="a-pwdlastset.md"><strong>Pwd-Last-Set</strong></a> attribute and the domain policy.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7e9d3-348">0x01000000</span><span class="sxs-lookup"><span data-stu-id="7e9d3-348">0x01000000</span></span></td>
<td><span data-ttu-id="7e9d3-349"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_TRUSTED_TO_AUTHENTICATE_FOR_DELEGATION</strong></a></span><span class="sxs-lookup"><span data-stu-id="7e9d3-349"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_TRUSTED_TO_AUTHENTICATE_FOR_DELEGATION</strong></a></span></span></td>
<td><span data-ttu-id="7e9d3-350">L'account è abilitato per la delega.</span><span class="sxs-lookup"><span data-stu-id="7e9d3-350">The account is enabled for delegation.</span></span> <span data-ttu-id="7e9d3-351">Si tratta di un'impostazione sensibile alla sicurezza. gli account con questa opzione abilitata devono essere controllati rigorosamente.</span><span class="sxs-lookup"><span data-stu-id="7e9d3-351">This is a security-sensitive setting; accounts with this option enabled should be strictly controlled.</span></span> <span data-ttu-id="7e9d3-352">Questa impostazione consente a un servizio in esecuzione con l'account di assumere un'identità client ed eseguire l'autenticazione come tale utente per altri server remoti nella rete.</span><span class="sxs-lookup"><span data-stu-id="7e9d3-352">This setting enables a service running under the account to assume a client identity and authenticate as that user to other remote servers on the network.</span></span></td>
</tr>
</tbody>
</table>



 

