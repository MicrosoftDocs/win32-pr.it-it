---
title: Attributo User-Parameters
description: Parametri dell'utente.
ms.assetid: e3d6d22d-5112-4dfe-af55-a17a63e5f2e4
ms.tgt_platform: multiple
keywords:
- Schema AD User-Parameters attribute
- Schema AD dell'attributo userParameters
topic_type:
- apiref
api_name:
- User-Parameters
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7c1d593f0a655dea4fa3ddb25753de712ab83cd
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104519958"
---
# <a name="user-parameters-attribute"></a><span data-ttu-id="58f2d-105">Attributo User-Parameters</span><span class="sxs-lookup"><span data-stu-id="58f2d-105">User-Parameters attribute</span></span>

<span data-ttu-id="58f2d-106">Parametri dell'utente.</span><span class="sxs-lookup"><span data-stu-id="58f2d-106">Parameters of the user.</span></span> <span data-ttu-id="58f2d-107">Punta a una stringa Unicode riservata per l'utilizzo da parte delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="58f2d-107">Points to a Unicode string that is set aside for use by applications.</span></span> <span data-ttu-id="58f2d-108">Questa stringa può essere una stringa null oppure può contenere un numero qualsiasi di caratteri prima del carattere null di terminazione.</span><span class="sxs-lookup"><span data-stu-id="58f2d-108">This string can be a null string, or it can have any number of characters before the terminating null character.</span></span> <span data-ttu-id="58f2d-109">I prodotti Microsoft utilizzano questo membro per archiviare i dati utente specifici del singolo programma.</span><span class="sxs-lookup"><span data-stu-id="58f2d-109">Microsoft products use this member to store user data specific to the individual program.</span></span>



| <span data-ttu-id="58f2d-110">Voce</span><span class="sxs-lookup"><span data-stu-id="58f2d-110">Entry</span></span> | <span data-ttu-id="58f2d-111">Valore</span><span class="sxs-lookup"><span data-stu-id="58f2d-111">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="58f2d-112">CN</span><span class="sxs-lookup"><span data-stu-id="58f2d-112">CN</span></span>                | <span data-ttu-id="58f2d-113">User-Parameters</span><span class="sxs-lookup"><span data-stu-id="58f2d-113">User-Parameters</span></span>                             |
| <span data-ttu-id="58f2d-114">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="58f2d-114">Ldap-Display-Name</span></span> | <span data-ttu-id="58f2d-115">userParameters</span><span class="sxs-lookup"><span data-stu-id="58f2d-115">userParameters</span></span>                              |
| <span data-ttu-id="58f2d-116">Dimensione</span><span class="sxs-lookup"><span data-stu-id="58f2d-116">Size</span></span>              | \-                                          |
| <span data-ttu-id="58f2d-117">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="58f2d-117">Update Privilege</span></span>  | <span data-ttu-id="58f2d-118">Modificato da applicazioni.</span><span class="sxs-lookup"><span data-stu-id="58f2d-118">Modified by applications.</span></span>                   |
| <span data-ttu-id="58f2d-119">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="58f2d-119">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="58f2d-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="58f2d-120">Attribute-Id</span></span>      | <span data-ttu-id="58f2d-121">1.2.840.113556.1.4.138</span><span class="sxs-lookup"><span data-stu-id="58f2d-121">1.2.840.113556.1.4.138</span></span>                      |
| <span data-ttu-id="58f2d-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="58f2d-122">System-Id-Guid</span></span>    | <span data-ttu-id="58f2d-123">bf967a6d-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="58f2d-123">bf967a6d-0de6-11d0-a285-00aa003049e2</span></span>        |
| <span data-ttu-id="58f2d-124">Sintassi</span><span class="sxs-lookup"><span data-stu-id="58f2d-124">Syntax</span></span>            | [<span data-ttu-id="58f2d-125">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="58f2d-125">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="58f2d-126">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="58f2d-126">Implementations</span></span>

-   [<span data-ttu-id="58f2d-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="58f2d-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="58f2d-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="58f2d-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="58f2d-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="58f2d-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="58f2d-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="58f2d-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="58f2d-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="58f2d-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="58f2d-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="58f2d-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="58f2d-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="58f2d-133">Windows 2000 Server</span></span>



| <span data-ttu-id="58f2d-134">Voce</span><span class="sxs-lookup"><span data-stu-id="58f2d-134">Entry</span></span> | <span data-ttu-id="58f2d-135">Valore</span><span class="sxs-lookup"><span data-stu-id="58f2d-135">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="58f2d-136">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="58f2d-136">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="58f2d-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="58f2d-137">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="58f2d-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="58f2d-138">System-Only</span></span>            | <span data-ttu-id="58f2d-139">Falso</span><span class="sxs-lookup"><span data-stu-id="58f2d-139">False</span></span>                             |
| <span data-ttu-id="58f2d-140">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="58f2d-140">Is-Single-Valued</span></span>       | <span data-ttu-id="58f2d-141">Vero</span><span class="sxs-lookup"><span data-stu-id="58f2d-141">True</span></span>                              |
| <span data-ttu-id="58f2d-142">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="58f2d-142">Is Indexed</span></span>             | <span data-ttu-id="58f2d-143">Falso</span><span class="sxs-lookup"><span data-stu-id="58f2d-143">False</span></span>                             |
| <span data-ttu-id="58f2d-144">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="58f2d-144">In Global Catalog</span></span>      | <span data-ttu-id="58f2d-145">Falso</span><span class="sxs-lookup"><span data-stu-id="58f2d-145">False</span></span>                             |
| <span data-ttu-id="58f2d-146">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="58f2d-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="58f2d-147">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="58f2d-147">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="58f2d-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="58f2d-148">Range-Lower</span></span>            | <span data-ttu-id="58f2d-149">0</span><span class="sxs-lookup"><span data-stu-id="58f2d-149">0</span></span>                                 |
| <span data-ttu-id="58f2d-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="58f2d-150">Range-Upper</span></span>            | <span data-ttu-id="58f2d-151">32767</span><span class="sxs-lookup"><span data-stu-id="58f2d-151">32767</span></span>                             |
| <span data-ttu-id="58f2d-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="58f2d-152">Search-Flags</span></span>           | <span data-ttu-id="58f2d-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="58f2d-153">0x00000000</span></span>                        |
| <span data-ttu-id="58f2d-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="58f2d-154">System-Flags</span></span>           | <span data-ttu-id="58f2d-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="58f2d-155">0x00000010</span></span>                        |
| <span data-ttu-id="58f2d-156">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="58f2d-156">Classes used in</span></span>        | [<span data-ttu-id="58f2d-157">**Utente**</span><span class="sxs-lookup"><span data-stu-id="58f2d-157">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="58f2d-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="58f2d-158">Windows Server 2003</span></span>



| <span data-ttu-id="58f2d-159">Voce</span><span class="sxs-lookup"><span data-stu-id="58f2d-159">Entry</span></span> | <span data-ttu-id="58f2d-160">Valore</span><span class="sxs-lookup"><span data-stu-id="58f2d-160">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="58f2d-161">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="58f2d-161">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="58f2d-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="58f2d-162">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="58f2d-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="58f2d-163">System-Only</span></span>            | <span data-ttu-id="58f2d-164">Falso</span><span class="sxs-lookup"><span data-stu-id="58f2d-164">False</span></span>                             |
| <span data-ttu-id="58f2d-165">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="58f2d-165">Is-Single-Valued</span></span>       | <span data-ttu-id="58f2d-166">Vero</span><span class="sxs-lookup"><span data-stu-id="58f2d-166">True</span></span>                              |
| <span data-ttu-id="58f2d-167">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="58f2d-167">Is Indexed</span></span>             | <span data-ttu-id="58f2d-168">Falso</span><span class="sxs-lookup"><span data-stu-id="58f2d-168">False</span></span>                             |
| <span data-ttu-id="58f2d-169">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="58f2d-169">In Global Catalog</span></span>      | <span data-ttu-id="58f2d-170">Falso</span><span class="sxs-lookup"><span data-stu-id="58f2d-170">False</span></span>                             |
| <span data-ttu-id="58f2d-171">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="58f2d-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="58f2d-172">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="58f2d-172">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="58f2d-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="58f2d-173">Range-Lower</span></span>            | <span data-ttu-id="58f2d-174">0</span><span class="sxs-lookup"><span data-stu-id="58f2d-174">0</span></span>                                 |
| <span data-ttu-id="58f2d-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="58f2d-175">Range-Upper</span></span>            | <span data-ttu-id="58f2d-176">32767</span><span class="sxs-lookup"><span data-stu-id="58f2d-176">32767</span></span>                             |
| <span data-ttu-id="58f2d-177">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="58f2d-177">Search-Flags</span></span>           | <span data-ttu-id="58f2d-178">0x00000000</span><span class="sxs-lookup"><span data-stu-id="58f2d-178">0x00000000</span></span>                        |
| <span data-ttu-id="58f2d-179">System-Flags</span><span class="sxs-lookup"><span data-stu-id="58f2d-179">System-Flags</span></span>           | <span data-ttu-id="58f2d-180">0x00000010</span><span class="sxs-lookup"><span data-stu-id="58f2d-180">0x00000010</span></span>                        |
| <span data-ttu-id="58f2d-181">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="58f2d-181">Classes used in</span></span>        | [<span data-ttu-id="58f2d-182">**Utente**</span><span class="sxs-lookup"><span data-stu-id="58f2d-182">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="58f2d-183">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="58f2d-183">Windows Server 2003 R2</span></span>



| <span data-ttu-id="58f2d-184">Voce</span><span class="sxs-lookup"><span data-stu-id="58f2d-184">Entry</span></span> | <span data-ttu-id="58f2d-185">Valore</span><span class="sxs-lookup"><span data-stu-id="58f2d-185">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="58f2d-186">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="58f2d-186">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="58f2d-187">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="58f2d-187">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="58f2d-188">System-Only</span><span class="sxs-lookup"><span data-stu-id="58f2d-188">System-Only</span></span>            | <span data-ttu-id="58f2d-189">Falso</span><span class="sxs-lookup"><span data-stu-id="58f2d-189">False</span></span>                             |
| <span data-ttu-id="58f2d-190">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="58f2d-190">Is-Single-Valued</span></span>       | <span data-ttu-id="58f2d-191">Vero</span><span class="sxs-lookup"><span data-stu-id="58f2d-191">True</span></span>                              |
| <span data-ttu-id="58f2d-192">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="58f2d-192">Is Indexed</span></span>             | <span data-ttu-id="58f2d-193">Falso</span><span class="sxs-lookup"><span data-stu-id="58f2d-193">False</span></span>                             |
| <span data-ttu-id="58f2d-194">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="58f2d-194">In Global Catalog</span></span>      | <span data-ttu-id="58f2d-195">Falso</span><span class="sxs-lookup"><span data-stu-id="58f2d-195">False</span></span>                             |
| <span data-ttu-id="58f2d-196">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="58f2d-196">NT-Security-Descriptor</span></span> | <span data-ttu-id="58f2d-197">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="58f2d-197">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="58f2d-198">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="58f2d-198">Range-Lower</span></span>            | <span data-ttu-id="58f2d-199">0</span><span class="sxs-lookup"><span data-stu-id="58f2d-199">0</span></span>                                 |
| <span data-ttu-id="58f2d-200">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="58f2d-200">Range-Upper</span></span>            | <span data-ttu-id="58f2d-201">32767</span><span class="sxs-lookup"><span data-stu-id="58f2d-201">32767</span></span>                             |
| <span data-ttu-id="58f2d-202">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="58f2d-202">Search-Flags</span></span>           | <span data-ttu-id="58f2d-203">0x00000000</span><span class="sxs-lookup"><span data-stu-id="58f2d-203">0x00000000</span></span>                        |
| <span data-ttu-id="58f2d-204">System-Flags</span><span class="sxs-lookup"><span data-stu-id="58f2d-204">System-Flags</span></span>           | <span data-ttu-id="58f2d-205">0x00000010</span><span class="sxs-lookup"><span data-stu-id="58f2d-205">0x00000010</span></span>                        |
| <span data-ttu-id="58f2d-206">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="58f2d-206">Classes used in</span></span>        | [<span data-ttu-id="58f2d-207">**Utente**</span><span class="sxs-lookup"><span data-stu-id="58f2d-207">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="58f2d-208">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="58f2d-208">Windows Server 2008</span></span>



| <span data-ttu-id="58f2d-209">Voce</span><span class="sxs-lookup"><span data-stu-id="58f2d-209">Entry</span></span> | <span data-ttu-id="58f2d-210">Valore</span><span class="sxs-lookup"><span data-stu-id="58f2d-210">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="58f2d-211">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="58f2d-211">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="58f2d-212">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="58f2d-212">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="58f2d-213">System-Only</span><span class="sxs-lookup"><span data-stu-id="58f2d-213">System-Only</span></span>            | <span data-ttu-id="58f2d-214">Falso</span><span class="sxs-lookup"><span data-stu-id="58f2d-214">False</span></span>                             |
| <span data-ttu-id="58f2d-215">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="58f2d-215">Is-Single-Valued</span></span>       | <span data-ttu-id="58f2d-216">Vero</span><span class="sxs-lookup"><span data-stu-id="58f2d-216">True</span></span>                              |
| <span data-ttu-id="58f2d-217">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="58f2d-217">Is Indexed</span></span>             | <span data-ttu-id="58f2d-218">Falso</span><span class="sxs-lookup"><span data-stu-id="58f2d-218">False</span></span>                             |
| <span data-ttu-id="58f2d-219">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="58f2d-219">In Global Catalog</span></span>      | <span data-ttu-id="58f2d-220">Falso</span><span class="sxs-lookup"><span data-stu-id="58f2d-220">False</span></span>                             |
| <span data-ttu-id="58f2d-221">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="58f2d-221">NT-Security-Descriptor</span></span> | <span data-ttu-id="58f2d-222">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="58f2d-222">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="58f2d-223">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="58f2d-223">Range-Lower</span></span>            | <span data-ttu-id="58f2d-224">0</span><span class="sxs-lookup"><span data-stu-id="58f2d-224">0</span></span>                                 |
| <span data-ttu-id="58f2d-225">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="58f2d-225">Range-Upper</span></span>            | <span data-ttu-id="58f2d-226">32767</span><span class="sxs-lookup"><span data-stu-id="58f2d-226">32767</span></span>                             |
| <span data-ttu-id="58f2d-227">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="58f2d-227">Search-Flags</span></span>           | <span data-ttu-id="58f2d-228">0x00000000</span><span class="sxs-lookup"><span data-stu-id="58f2d-228">0x00000000</span></span>                        |
| <span data-ttu-id="58f2d-229">System-Flags</span><span class="sxs-lookup"><span data-stu-id="58f2d-229">System-Flags</span></span>           | <span data-ttu-id="58f2d-230">0x00000010</span><span class="sxs-lookup"><span data-stu-id="58f2d-230">0x00000010</span></span>                        |
| <span data-ttu-id="58f2d-231">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="58f2d-231">Classes used in</span></span>        | [<span data-ttu-id="58f2d-232">**Utente**</span><span class="sxs-lookup"><span data-stu-id="58f2d-232">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="58f2d-233">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="58f2d-233">Windows Server 2008 R2</span></span>



| <span data-ttu-id="58f2d-234">Voce</span><span class="sxs-lookup"><span data-stu-id="58f2d-234">Entry</span></span> | <span data-ttu-id="58f2d-235">Valore</span><span class="sxs-lookup"><span data-stu-id="58f2d-235">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="58f2d-236">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="58f2d-236">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="58f2d-237">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="58f2d-237">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="58f2d-238">System-Only</span><span class="sxs-lookup"><span data-stu-id="58f2d-238">System-Only</span></span>            | <span data-ttu-id="58f2d-239">Falso</span><span class="sxs-lookup"><span data-stu-id="58f2d-239">False</span></span>                             |
| <span data-ttu-id="58f2d-240">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="58f2d-240">Is-Single-Valued</span></span>       | <span data-ttu-id="58f2d-241">Vero</span><span class="sxs-lookup"><span data-stu-id="58f2d-241">True</span></span>                              |
| <span data-ttu-id="58f2d-242">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="58f2d-242">Is Indexed</span></span>             | <span data-ttu-id="58f2d-243">Falso</span><span class="sxs-lookup"><span data-stu-id="58f2d-243">False</span></span>                             |
| <span data-ttu-id="58f2d-244">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="58f2d-244">In Global Catalog</span></span>      | <span data-ttu-id="58f2d-245">Falso</span><span class="sxs-lookup"><span data-stu-id="58f2d-245">False</span></span>                             |
| <span data-ttu-id="58f2d-246">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="58f2d-246">NT-Security-Descriptor</span></span> | <span data-ttu-id="58f2d-247">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="58f2d-247">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="58f2d-248">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="58f2d-248">Range-Lower</span></span>            | <span data-ttu-id="58f2d-249">0</span><span class="sxs-lookup"><span data-stu-id="58f2d-249">0</span></span>                                 |
| <span data-ttu-id="58f2d-250">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="58f2d-250">Range-Upper</span></span>            | <span data-ttu-id="58f2d-251">32767</span><span class="sxs-lookup"><span data-stu-id="58f2d-251">32767</span></span>                             |
| <span data-ttu-id="58f2d-252">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="58f2d-252">Search-Flags</span></span>           | <span data-ttu-id="58f2d-253">0x00000000</span><span class="sxs-lookup"><span data-stu-id="58f2d-253">0x00000000</span></span>                        |
| <span data-ttu-id="58f2d-254">System-Flags</span><span class="sxs-lookup"><span data-stu-id="58f2d-254">System-Flags</span></span>           | <span data-ttu-id="58f2d-255">0x00000010</span><span class="sxs-lookup"><span data-stu-id="58f2d-255">0x00000010</span></span>                        |
| <span data-ttu-id="58f2d-256">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="58f2d-256">Classes used in</span></span>        | [<span data-ttu-id="58f2d-257">**Utente**</span><span class="sxs-lookup"><span data-stu-id="58f2d-257">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="58f2d-258">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="58f2d-258">Windows Server 2012</span></span>



| <span data-ttu-id="58f2d-259">Voce</span><span class="sxs-lookup"><span data-stu-id="58f2d-259">Entry</span></span> | <span data-ttu-id="58f2d-260">Valore</span><span class="sxs-lookup"><span data-stu-id="58f2d-260">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="58f2d-261">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="58f2d-261">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="58f2d-262">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="58f2d-262">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="58f2d-263">System-Only</span><span class="sxs-lookup"><span data-stu-id="58f2d-263">System-Only</span></span>            | <span data-ttu-id="58f2d-264">Falso</span><span class="sxs-lookup"><span data-stu-id="58f2d-264">False</span></span>                             |
| <span data-ttu-id="58f2d-265">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="58f2d-265">Is-Single-Valued</span></span>       | <span data-ttu-id="58f2d-266">Vero</span><span class="sxs-lookup"><span data-stu-id="58f2d-266">True</span></span>                              |
| <span data-ttu-id="58f2d-267">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="58f2d-267">Is Indexed</span></span>             | <span data-ttu-id="58f2d-268">Falso</span><span class="sxs-lookup"><span data-stu-id="58f2d-268">False</span></span>                             |
| <span data-ttu-id="58f2d-269">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="58f2d-269">In Global Catalog</span></span>      | <span data-ttu-id="58f2d-270">Falso</span><span class="sxs-lookup"><span data-stu-id="58f2d-270">False</span></span>                             |
| <span data-ttu-id="58f2d-271">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="58f2d-271">NT-Security-Descriptor</span></span> | <span data-ttu-id="58f2d-272">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="58f2d-272">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="58f2d-273">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="58f2d-273">Range-Lower</span></span>            | <span data-ttu-id="58f2d-274">0</span><span class="sxs-lookup"><span data-stu-id="58f2d-274">0</span></span>                                 |
| <span data-ttu-id="58f2d-275">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="58f2d-275">Range-Upper</span></span>            | <span data-ttu-id="58f2d-276">32767</span><span class="sxs-lookup"><span data-stu-id="58f2d-276">32767</span></span>                             |
| <span data-ttu-id="58f2d-277">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="58f2d-277">Search-Flags</span></span>           | <span data-ttu-id="58f2d-278">0x00000000</span><span class="sxs-lookup"><span data-stu-id="58f2d-278">0x00000000</span></span>                        |
| <span data-ttu-id="58f2d-279">System-Flags</span><span class="sxs-lookup"><span data-stu-id="58f2d-279">System-Flags</span></span>           | <span data-ttu-id="58f2d-280">0x00000010</span><span class="sxs-lookup"><span data-stu-id="58f2d-280">0x00000010</span></span>                        |
| <span data-ttu-id="58f2d-281">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="58f2d-281">Classes used in</span></span>        | [<span data-ttu-id="58f2d-282">**Utente**</span><span class="sxs-lookup"><span data-stu-id="58f2d-282">**User**</span></span>](c-user.md)<br/> |



 

 





