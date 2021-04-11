---
title: attributo msNPAllowDialin
description: Indica se l'account dispone dell'autorizzazione per la connessione al server RAS.
ms.assetid: 8e0d98b4-93b1-4a76-a8b7-d6017028b48a
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo msNPAllowDialin
topic_type:
- apiref
api_name:
- msNPAllowDialin
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e56f9fe3817053e3e1e49611fb76934acbbcba9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104122865"
---
# <a name="msnpallowdialin-attribute"></a><span data-ttu-id="fd7b2-104">attributo msNPAllowDialin</span><span class="sxs-lookup"><span data-stu-id="fd7b2-104">msNPAllowDialin attribute</span></span>

<span data-ttu-id="fd7b2-105">Indica se l'account dispone dell'autorizzazione per la connessione al server RAS.</span><span class="sxs-lookup"><span data-stu-id="fd7b2-105">Indicates whether the account has permission to dial in to the RAS server.</span></span> <span data-ttu-id="fd7b2-106">Non modificare direttamente questo valore.</span><span class="sxs-lookup"><span data-stu-id="fd7b2-106">Do not modify this value directly.</span></span> <span data-ttu-id="fd7b2-107">Utilizzare la [funzione di amministrazione RAS](/windows/desktop/RRAS/ras-administration-functions) appropriata per modificare questo valore.</span><span class="sxs-lookup"><span data-stu-id="fd7b2-107">Use the appropriate [RAS administration function](/windows/desktop/RRAS/ras-administration-functions) to modify this value.</span></span>



| <span data-ttu-id="fd7b2-108">Voce</span><span class="sxs-lookup"><span data-stu-id="fd7b2-108">Entry</span></span> | <span data-ttu-id="fd7b2-109">Valore</span><span class="sxs-lookup"><span data-stu-id="fd7b2-109">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="fd7b2-110">CN</span><span class="sxs-lookup"><span data-stu-id="fd7b2-110">CN</span></span>                | <span data-ttu-id="fd7b2-111">msNPAllowDialin</span><span class="sxs-lookup"><span data-stu-id="fd7b2-111">msNPAllowDialin</span></span>                      |
| <span data-ttu-id="fd7b2-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="fd7b2-112">Ldap-Display-Name</span></span> | <span data-ttu-id="fd7b2-113">msNPAllowDialin</span><span class="sxs-lookup"><span data-stu-id="fd7b2-113">msNPAllowDialin</span></span>                      |
| <span data-ttu-id="fd7b2-114">Dimensione</span><span class="sxs-lookup"><span data-stu-id="fd7b2-114">Size</span></span>              | <span data-ttu-id="fd7b2-115">4 byte</span><span class="sxs-lookup"><span data-stu-id="fd7b2-115">4 bytes</span></span>                              |
| <span data-ttu-id="fd7b2-116">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="fd7b2-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="fd7b2-117">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="fd7b2-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="fd7b2-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="fd7b2-118">Attribute-Id</span></span>      | <span data-ttu-id="fd7b2-119">1.2.840.113556.1.4.1119</span><span class="sxs-lookup"><span data-stu-id="fd7b2-119">1.2.840.113556.1.4.1119</span></span>              |
| <span data-ttu-id="fd7b2-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="fd7b2-120">System-Id-Guid</span></span>    | <span data-ttu-id="fd7b2-121">db0c9085-c1f2-11d1-bbc5-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="fd7b2-121">db0c9085-c1f2-11d1-bbc5-0080c76670c0</span></span> |
| <span data-ttu-id="fd7b2-122">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fd7b2-122">Syntax</span></span>            | [<span data-ttu-id="fd7b2-123">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="fd7b2-123">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="fd7b2-124">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="fd7b2-124">Implementations</span></span>

-   [<span data-ttu-id="fd7b2-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="fd7b2-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="fd7b2-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="fd7b2-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="fd7b2-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="fd7b2-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="fd7b2-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="fd7b2-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="fd7b2-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="fd7b2-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="fd7b2-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="fd7b2-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="fd7b2-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="fd7b2-131">Windows 2000 Server</span></span>



| <span data-ttu-id="fd7b2-132">Voce</span><span class="sxs-lookup"><span data-stu-id="fd7b2-132">Entry</span></span> | <span data-ttu-id="fd7b2-133">Valore</span><span class="sxs-lookup"><span data-stu-id="fd7b2-133">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="fd7b2-134">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="fd7b2-134">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="fd7b2-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fd7b2-135">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="fd7b2-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="fd7b2-136">System-Only</span></span>            | <span data-ttu-id="fd7b2-137">Falso</span><span class="sxs-lookup"><span data-stu-id="fd7b2-137">False</span></span>                             |
| <span data-ttu-id="fd7b2-138">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="fd7b2-138">Is-Single-Valued</span></span>       | <span data-ttu-id="fd7b2-139">Vero</span><span class="sxs-lookup"><span data-stu-id="fd7b2-139">True</span></span>                              |
| <span data-ttu-id="fd7b2-140">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="fd7b2-140">Is Indexed</span></span>             | <span data-ttu-id="fd7b2-141">Falso</span><span class="sxs-lookup"><span data-stu-id="fd7b2-141">False</span></span>                             |
| <span data-ttu-id="fd7b2-142">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="fd7b2-142">In Global Catalog</span></span>      | <span data-ttu-id="fd7b2-143">Falso</span><span class="sxs-lookup"><span data-stu-id="fd7b2-143">False</span></span>                             |
| <span data-ttu-id="fd7b2-144">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="fd7b2-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="fd7b2-145">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="fd7b2-145">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="fd7b2-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fd7b2-146">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="fd7b2-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fd7b2-147">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="fd7b2-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fd7b2-148">Search-Flags</span></span>           | <span data-ttu-id="fd7b2-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fd7b2-149">0x00000000</span></span>                        |
| <span data-ttu-id="fd7b2-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fd7b2-150">System-Flags</span></span>           | <span data-ttu-id="fd7b2-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fd7b2-151">0x00000010</span></span>                        |
| <span data-ttu-id="fd7b2-152">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="fd7b2-152">Classes used in</span></span>        | [<span data-ttu-id="fd7b2-153">**Utente**</span><span class="sxs-lookup"><span data-stu-id="fd7b2-153">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="fd7b2-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="fd7b2-154">Windows Server 2003</span></span>



| <span data-ttu-id="fd7b2-155">Voce</span><span class="sxs-lookup"><span data-stu-id="fd7b2-155">Entry</span></span> | <span data-ttu-id="fd7b2-156">Valore</span><span class="sxs-lookup"><span data-stu-id="fd7b2-156">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="fd7b2-157">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="fd7b2-157">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="fd7b2-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fd7b2-158">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="fd7b2-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="fd7b2-159">System-Only</span></span>            | <span data-ttu-id="fd7b2-160">Falso</span><span class="sxs-lookup"><span data-stu-id="fd7b2-160">False</span></span>                             |
| <span data-ttu-id="fd7b2-161">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="fd7b2-161">Is-Single-Valued</span></span>       | <span data-ttu-id="fd7b2-162">Vero</span><span class="sxs-lookup"><span data-stu-id="fd7b2-162">True</span></span>                              |
| <span data-ttu-id="fd7b2-163">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="fd7b2-163">Is Indexed</span></span>             | <span data-ttu-id="fd7b2-164">Falso</span><span class="sxs-lookup"><span data-stu-id="fd7b2-164">False</span></span>                             |
| <span data-ttu-id="fd7b2-165">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="fd7b2-165">In Global Catalog</span></span>      | <span data-ttu-id="fd7b2-166">Falso</span><span class="sxs-lookup"><span data-stu-id="fd7b2-166">False</span></span>                             |
| <span data-ttu-id="fd7b2-167">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="fd7b2-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="fd7b2-168">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="fd7b2-168">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="fd7b2-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fd7b2-169">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="fd7b2-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fd7b2-170">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="fd7b2-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fd7b2-171">Search-Flags</span></span>           | <span data-ttu-id="fd7b2-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fd7b2-172">0x00000000</span></span>                        |
| <span data-ttu-id="fd7b2-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fd7b2-173">System-Flags</span></span>           | <span data-ttu-id="fd7b2-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fd7b2-174">0x00000010</span></span>                        |
| <span data-ttu-id="fd7b2-175">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="fd7b2-175">Classes used in</span></span>        | [<span data-ttu-id="fd7b2-176">**Utente**</span><span class="sxs-lookup"><span data-stu-id="fd7b2-176">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="fd7b2-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="fd7b2-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="fd7b2-178">Voce</span><span class="sxs-lookup"><span data-stu-id="fd7b2-178">Entry</span></span> | <span data-ttu-id="fd7b2-179">Valore</span><span class="sxs-lookup"><span data-stu-id="fd7b2-179">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="fd7b2-180">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="fd7b2-180">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="fd7b2-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fd7b2-181">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="fd7b2-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="fd7b2-182">System-Only</span></span>            | <span data-ttu-id="fd7b2-183">Falso</span><span class="sxs-lookup"><span data-stu-id="fd7b2-183">False</span></span>                             |
| <span data-ttu-id="fd7b2-184">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="fd7b2-184">Is-Single-Valued</span></span>       | <span data-ttu-id="fd7b2-185">Vero</span><span class="sxs-lookup"><span data-stu-id="fd7b2-185">True</span></span>                              |
| <span data-ttu-id="fd7b2-186">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="fd7b2-186">Is Indexed</span></span>             | <span data-ttu-id="fd7b2-187">Falso</span><span class="sxs-lookup"><span data-stu-id="fd7b2-187">False</span></span>                             |
| <span data-ttu-id="fd7b2-188">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="fd7b2-188">In Global Catalog</span></span>      | <span data-ttu-id="fd7b2-189">Falso</span><span class="sxs-lookup"><span data-stu-id="fd7b2-189">False</span></span>                             |
| <span data-ttu-id="fd7b2-190">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="fd7b2-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="fd7b2-191">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="fd7b2-191">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="fd7b2-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fd7b2-192">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="fd7b2-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fd7b2-193">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="fd7b2-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fd7b2-194">Search-Flags</span></span>           | <span data-ttu-id="fd7b2-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fd7b2-195">0x00000000</span></span>                        |
| <span data-ttu-id="fd7b2-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fd7b2-196">System-Flags</span></span>           | <span data-ttu-id="fd7b2-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fd7b2-197">0x00000010</span></span>                        |
| <span data-ttu-id="fd7b2-198">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="fd7b2-198">Classes used in</span></span>        | [<span data-ttu-id="fd7b2-199">**Utente**</span><span class="sxs-lookup"><span data-stu-id="fd7b2-199">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="fd7b2-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fd7b2-200">Windows Server 2008</span></span>



| <span data-ttu-id="fd7b2-201">Voce</span><span class="sxs-lookup"><span data-stu-id="fd7b2-201">Entry</span></span> | <span data-ttu-id="fd7b2-202">Valore</span><span class="sxs-lookup"><span data-stu-id="fd7b2-202">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="fd7b2-203">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="fd7b2-203">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="fd7b2-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fd7b2-204">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="fd7b2-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="fd7b2-205">System-Only</span></span>            | <span data-ttu-id="fd7b2-206">Falso</span><span class="sxs-lookup"><span data-stu-id="fd7b2-206">False</span></span>                             |
| <span data-ttu-id="fd7b2-207">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="fd7b2-207">Is-Single-Valued</span></span>       | <span data-ttu-id="fd7b2-208">Vero</span><span class="sxs-lookup"><span data-stu-id="fd7b2-208">True</span></span>                              |
| <span data-ttu-id="fd7b2-209">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="fd7b2-209">Is Indexed</span></span>             | <span data-ttu-id="fd7b2-210">Falso</span><span class="sxs-lookup"><span data-stu-id="fd7b2-210">False</span></span>                             |
| <span data-ttu-id="fd7b2-211">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="fd7b2-211">In Global Catalog</span></span>      | <span data-ttu-id="fd7b2-212">Falso</span><span class="sxs-lookup"><span data-stu-id="fd7b2-212">False</span></span>                             |
| <span data-ttu-id="fd7b2-213">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="fd7b2-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="fd7b2-214">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="fd7b2-214">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="fd7b2-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fd7b2-215">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="fd7b2-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fd7b2-216">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="fd7b2-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fd7b2-217">Search-Flags</span></span>           | <span data-ttu-id="fd7b2-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fd7b2-218">0x00000010</span></span>                        |
| <span data-ttu-id="fd7b2-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fd7b2-219">System-Flags</span></span>           | <span data-ttu-id="fd7b2-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fd7b2-220">0x00000010</span></span>                        |
| <span data-ttu-id="fd7b2-221">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="fd7b2-221">Classes used in</span></span>        | [<span data-ttu-id="fd7b2-222">**Utente**</span><span class="sxs-lookup"><span data-stu-id="fd7b2-222">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="fd7b2-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="fd7b2-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="fd7b2-224">Voce</span><span class="sxs-lookup"><span data-stu-id="fd7b2-224">Entry</span></span> | <span data-ttu-id="fd7b2-225">Valore</span><span class="sxs-lookup"><span data-stu-id="fd7b2-225">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="fd7b2-226">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="fd7b2-226">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="fd7b2-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fd7b2-227">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="fd7b2-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="fd7b2-228">System-Only</span></span>            | <span data-ttu-id="fd7b2-229">Falso</span><span class="sxs-lookup"><span data-stu-id="fd7b2-229">False</span></span>                             |
| <span data-ttu-id="fd7b2-230">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="fd7b2-230">Is-Single-Valued</span></span>       | <span data-ttu-id="fd7b2-231">Vero</span><span class="sxs-lookup"><span data-stu-id="fd7b2-231">True</span></span>                              |
| <span data-ttu-id="fd7b2-232">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="fd7b2-232">Is Indexed</span></span>             | <span data-ttu-id="fd7b2-233">Falso</span><span class="sxs-lookup"><span data-stu-id="fd7b2-233">False</span></span>                             |
| <span data-ttu-id="fd7b2-234">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="fd7b2-234">In Global Catalog</span></span>      | <span data-ttu-id="fd7b2-235">Falso</span><span class="sxs-lookup"><span data-stu-id="fd7b2-235">False</span></span>                             |
| <span data-ttu-id="fd7b2-236">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="fd7b2-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="fd7b2-237">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="fd7b2-237">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="fd7b2-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fd7b2-238">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="fd7b2-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fd7b2-239">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="fd7b2-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fd7b2-240">Search-Flags</span></span>           | <span data-ttu-id="fd7b2-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fd7b2-241">0x00000010</span></span>                        |
| <span data-ttu-id="fd7b2-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fd7b2-242">System-Flags</span></span>           | <span data-ttu-id="fd7b2-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fd7b2-243">0x00000010</span></span>                        |
| <span data-ttu-id="fd7b2-244">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="fd7b2-244">Classes used in</span></span>        | [<span data-ttu-id="fd7b2-245">**Utente**</span><span class="sxs-lookup"><span data-stu-id="fd7b2-245">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="fd7b2-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="fd7b2-246">Windows Server 2012</span></span>



| <span data-ttu-id="fd7b2-247">Voce</span><span class="sxs-lookup"><span data-stu-id="fd7b2-247">Entry</span></span> | <span data-ttu-id="fd7b2-248">Valore</span><span class="sxs-lookup"><span data-stu-id="fd7b2-248">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="fd7b2-249">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="fd7b2-249">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="fd7b2-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fd7b2-250">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="fd7b2-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="fd7b2-251">System-Only</span></span>            | <span data-ttu-id="fd7b2-252">Falso</span><span class="sxs-lookup"><span data-stu-id="fd7b2-252">False</span></span>                             |
| <span data-ttu-id="fd7b2-253">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="fd7b2-253">Is-Single-Valued</span></span>       | <span data-ttu-id="fd7b2-254">Vero</span><span class="sxs-lookup"><span data-stu-id="fd7b2-254">True</span></span>                              |
| <span data-ttu-id="fd7b2-255">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="fd7b2-255">Is Indexed</span></span>             | <span data-ttu-id="fd7b2-256">Falso</span><span class="sxs-lookup"><span data-stu-id="fd7b2-256">False</span></span>                             |
| <span data-ttu-id="fd7b2-257">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="fd7b2-257">In Global Catalog</span></span>      | <span data-ttu-id="fd7b2-258">Falso</span><span class="sxs-lookup"><span data-stu-id="fd7b2-258">False</span></span>                             |
| <span data-ttu-id="fd7b2-259">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="fd7b2-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="fd7b2-260">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="fd7b2-260">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="fd7b2-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fd7b2-261">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="fd7b2-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fd7b2-262">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="fd7b2-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fd7b2-263">Search-Flags</span></span>           | <span data-ttu-id="fd7b2-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fd7b2-264">0x00000010</span></span>                        |
| <span data-ttu-id="fd7b2-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fd7b2-265">System-Flags</span></span>           | <span data-ttu-id="fd7b2-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fd7b2-266">0x00000010</span></span>                        |
| <span data-ttu-id="fd7b2-267">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="fd7b2-267">Classes used in</span></span>        | [<span data-ttu-id="fd7b2-268">**Utente**</span><span class="sxs-lookup"><span data-stu-id="fd7b2-268">**User**</span></span>](c-user.md)<br/> |



## <a name="see-also"></a><span data-ttu-id="fd7b2-269">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fd7b2-269">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd7b2-270">Funzioni di amministrazione RAS</span><span class="sxs-lookup"><span data-stu-id="fd7b2-270">RAS Administration Functions</span></span>](/windows/desktop/RRAS/ras-administration-functions)
</dt> </dl>

 

