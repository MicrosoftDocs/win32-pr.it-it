---
title: Attributo Initial-auth-in uscita
description: Contiene informazioni su un'autenticazione in uscita iniziale inviata dal server di autenticazione per questo dominio al client che ha richiesto l'autenticazione.
ms.assetid: cc5ceb14-0424-4caa-bcd9-1e48988af67a
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo iniziale-auth-in uscita
- Schema AD dell'attributo initialAuthOutgoing
topic_type:
- apiref
api_name:
- Initial-Auth-Outgoing
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e84faaa443c9589e04f4998dc41d72fe870b5f2e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104122014"
---
# <a name="initial-auth-outgoing-attribute"></a><span data-ttu-id="114d5-105">Attributo Initial-auth-in uscita</span><span class="sxs-lookup"><span data-stu-id="114d5-105">Initial-Auth-Outgoing attribute</span></span>

<span data-ttu-id="114d5-106">Contiene informazioni su un'autenticazione in uscita iniziale inviata dal server di autenticazione per questo dominio al client che ha richiesto l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="114d5-106">Contains information about an initial outgoing authentication sent by the authentication server for this domain to the client that requested authentication.</span></span> <span data-ttu-id="114d5-107">Il server che utilizza questo attributo riceve l'autorizzazione dal server di autenticazione e lo invia al client.</span><span class="sxs-lookup"><span data-stu-id="114d5-107">The server that uses this attribute receives the authorization from the authentication server and sends it to the client.</span></span>



| <span data-ttu-id="114d5-108">Voce</span><span class="sxs-lookup"><span data-stu-id="114d5-108">Entry</span></span> | <span data-ttu-id="114d5-109">Valore</span><span class="sxs-lookup"><span data-stu-id="114d5-109">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="114d5-110">CN</span><span class="sxs-lookup"><span data-stu-id="114d5-110">CN</span></span>                | <span data-ttu-id="114d5-111">Autenticazione iniziale-in uscita</span><span class="sxs-lookup"><span data-stu-id="114d5-111">Initial-Auth-Outgoing</span></span>                       |
| <span data-ttu-id="114d5-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="114d5-112">Ldap-Display-Name</span></span> | <span data-ttu-id="114d5-113">initialAuthOutgoing</span><span class="sxs-lookup"><span data-stu-id="114d5-113">initialAuthOutgoing</span></span>                         |
| <span data-ttu-id="114d5-114">Dimensione</span><span class="sxs-lookup"><span data-stu-id="114d5-114">Size</span></span>              | \-                                          |
| <span data-ttu-id="114d5-115">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="114d5-115">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="114d5-116">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="114d5-116">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="114d5-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="114d5-117">Attribute-Id</span></span>      | <span data-ttu-id="114d5-118">1.2.840.113556.1.4.540</span><span class="sxs-lookup"><span data-stu-id="114d5-118">1.2.840.113556.1.4.540</span></span>                      |
| <span data-ttu-id="114d5-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="114d5-119">System-Id-Guid</span></span>    | <span data-ttu-id="114d5-120">52458024-ca6a-11D0-AFFF-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="114d5-120">52458024-ca6a-11d0-afff-0000f80367c1</span></span>        |
| <span data-ttu-id="114d5-121">Sintassi</span><span class="sxs-lookup"><span data-stu-id="114d5-121">Syntax</span></span>            | [<span data-ttu-id="114d5-122">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="114d5-122">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="114d5-123">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="114d5-123">Implementations</span></span>

-   [<span data-ttu-id="114d5-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="114d5-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="114d5-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="114d5-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="114d5-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="114d5-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="114d5-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="114d5-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="114d5-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="114d5-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="114d5-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="114d5-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="114d5-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="114d5-130">Windows 2000 Server</span></span>



| <span data-ttu-id="114d5-131">Voce</span><span class="sxs-lookup"><span data-stu-id="114d5-131">Entry</span></span> | <span data-ttu-id="114d5-132">Valore</span><span class="sxs-lookup"><span data-stu-id="114d5-132">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="114d5-133">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="114d5-133">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="114d5-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="114d5-134">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="114d5-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="114d5-135">System-Only</span></span>            | <span data-ttu-id="114d5-136">Falso</span><span class="sxs-lookup"><span data-stu-id="114d5-136">False</span></span>                                                |
| <span data-ttu-id="114d5-137">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="114d5-137">Is-Single-Valued</span></span>       | <span data-ttu-id="114d5-138">Vero</span><span class="sxs-lookup"><span data-stu-id="114d5-138">True</span></span>                                                 |
| <span data-ttu-id="114d5-139">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="114d5-139">Is Indexed</span></span>             | <span data-ttu-id="114d5-140">Falso</span><span class="sxs-lookup"><span data-stu-id="114d5-140">False</span></span>                                                |
| <span data-ttu-id="114d5-141">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="114d5-141">In Global Catalog</span></span>      | <span data-ttu-id="114d5-142">Falso</span><span class="sxs-lookup"><span data-stu-id="114d5-142">False</span></span>                                                |
| <span data-ttu-id="114d5-143">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="114d5-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="114d5-144">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="114d5-144">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="114d5-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="114d5-145">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="114d5-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="114d5-146">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="114d5-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="114d5-147">Search-Flags</span></span>           | <span data-ttu-id="114d5-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="114d5-148">0x00000000</span></span>                                           |
| <span data-ttu-id="114d5-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="114d5-149">System-Flags</span></span>           | <span data-ttu-id="114d5-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="114d5-150">0x00000010</span></span>                                           |
| <span data-ttu-id="114d5-151">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="114d5-151">Classes used in</span></span>        | [<span data-ttu-id="114d5-152">**Dominio trusted**</span><span class="sxs-lookup"><span data-stu-id="114d5-152">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="114d5-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="114d5-153">Windows Server 2003</span></span>



| <span data-ttu-id="114d5-154">Voce</span><span class="sxs-lookup"><span data-stu-id="114d5-154">Entry</span></span> | <span data-ttu-id="114d5-155">Valore</span><span class="sxs-lookup"><span data-stu-id="114d5-155">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="114d5-156">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="114d5-156">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="114d5-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="114d5-157">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="114d5-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="114d5-158">System-Only</span></span>            | <span data-ttu-id="114d5-159">Falso</span><span class="sxs-lookup"><span data-stu-id="114d5-159">False</span></span>                                                |
| <span data-ttu-id="114d5-160">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="114d5-160">Is-Single-Valued</span></span>       | <span data-ttu-id="114d5-161">Vero</span><span class="sxs-lookup"><span data-stu-id="114d5-161">True</span></span>                                                 |
| <span data-ttu-id="114d5-162">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="114d5-162">Is Indexed</span></span>             | <span data-ttu-id="114d5-163">Falso</span><span class="sxs-lookup"><span data-stu-id="114d5-163">False</span></span>                                                |
| <span data-ttu-id="114d5-164">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="114d5-164">In Global Catalog</span></span>      | <span data-ttu-id="114d5-165">Falso</span><span class="sxs-lookup"><span data-stu-id="114d5-165">False</span></span>                                                |
| <span data-ttu-id="114d5-166">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="114d5-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="114d5-167">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="114d5-167">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="114d5-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="114d5-168">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="114d5-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="114d5-169">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="114d5-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="114d5-170">Search-Flags</span></span>           | <span data-ttu-id="114d5-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="114d5-171">0x00000000</span></span>                                           |
| <span data-ttu-id="114d5-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="114d5-172">System-Flags</span></span>           | <span data-ttu-id="114d5-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="114d5-173">0x00000010</span></span>                                           |
| <span data-ttu-id="114d5-174">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="114d5-174">Classes used in</span></span>        | [<span data-ttu-id="114d5-175">**Dominio trusted**</span><span class="sxs-lookup"><span data-stu-id="114d5-175">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="114d5-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="114d5-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="114d5-177">Voce</span><span class="sxs-lookup"><span data-stu-id="114d5-177">Entry</span></span> | <span data-ttu-id="114d5-178">Valore</span><span class="sxs-lookup"><span data-stu-id="114d5-178">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="114d5-179">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="114d5-179">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="114d5-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="114d5-180">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="114d5-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="114d5-181">System-Only</span></span>            | <span data-ttu-id="114d5-182">Falso</span><span class="sxs-lookup"><span data-stu-id="114d5-182">False</span></span>                                                |
| <span data-ttu-id="114d5-183">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="114d5-183">Is-Single-Valued</span></span>       | <span data-ttu-id="114d5-184">Vero</span><span class="sxs-lookup"><span data-stu-id="114d5-184">True</span></span>                                                 |
| <span data-ttu-id="114d5-185">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="114d5-185">Is Indexed</span></span>             | <span data-ttu-id="114d5-186">Falso</span><span class="sxs-lookup"><span data-stu-id="114d5-186">False</span></span>                                                |
| <span data-ttu-id="114d5-187">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="114d5-187">In Global Catalog</span></span>      | <span data-ttu-id="114d5-188">Falso</span><span class="sxs-lookup"><span data-stu-id="114d5-188">False</span></span>                                                |
| <span data-ttu-id="114d5-189">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="114d5-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="114d5-190">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="114d5-190">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="114d5-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="114d5-191">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="114d5-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="114d5-192">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="114d5-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="114d5-193">Search-Flags</span></span>           | <span data-ttu-id="114d5-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="114d5-194">0x00000000</span></span>                                           |
| <span data-ttu-id="114d5-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="114d5-195">System-Flags</span></span>           | <span data-ttu-id="114d5-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="114d5-196">0x00000010</span></span>                                           |
| <span data-ttu-id="114d5-197">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="114d5-197">Classes used in</span></span>        | [<span data-ttu-id="114d5-198">**Dominio trusted**</span><span class="sxs-lookup"><span data-stu-id="114d5-198">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="114d5-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="114d5-199">Windows Server 2008</span></span>



| <span data-ttu-id="114d5-200">Voce</span><span class="sxs-lookup"><span data-stu-id="114d5-200">Entry</span></span> | <span data-ttu-id="114d5-201">Valore</span><span class="sxs-lookup"><span data-stu-id="114d5-201">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="114d5-202">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="114d5-202">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="114d5-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="114d5-203">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="114d5-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="114d5-204">System-Only</span></span>            | <span data-ttu-id="114d5-205">Falso</span><span class="sxs-lookup"><span data-stu-id="114d5-205">False</span></span>                                                |
| <span data-ttu-id="114d5-206">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="114d5-206">Is-Single-Valued</span></span>       | <span data-ttu-id="114d5-207">Vero</span><span class="sxs-lookup"><span data-stu-id="114d5-207">True</span></span>                                                 |
| <span data-ttu-id="114d5-208">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="114d5-208">Is Indexed</span></span>             | <span data-ttu-id="114d5-209">Falso</span><span class="sxs-lookup"><span data-stu-id="114d5-209">False</span></span>                                                |
| <span data-ttu-id="114d5-210">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="114d5-210">In Global Catalog</span></span>      | <span data-ttu-id="114d5-211">Falso</span><span class="sxs-lookup"><span data-stu-id="114d5-211">False</span></span>                                                |
| <span data-ttu-id="114d5-212">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="114d5-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="114d5-213">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="114d5-213">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="114d5-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="114d5-214">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="114d5-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="114d5-215">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="114d5-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="114d5-216">Search-Flags</span></span>           | <span data-ttu-id="114d5-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="114d5-217">0x00000000</span></span>                                           |
| <span data-ttu-id="114d5-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="114d5-218">System-Flags</span></span>           | <span data-ttu-id="114d5-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="114d5-219">0x00000010</span></span>                                           |
| <span data-ttu-id="114d5-220">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="114d5-220">Classes used in</span></span>        | [<span data-ttu-id="114d5-221">**Dominio trusted**</span><span class="sxs-lookup"><span data-stu-id="114d5-221">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="114d5-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="114d5-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="114d5-223">Voce</span><span class="sxs-lookup"><span data-stu-id="114d5-223">Entry</span></span> | <span data-ttu-id="114d5-224">Valore</span><span class="sxs-lookup"><span data-stu-id="114d5-224">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="114d5-225">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="114d5-225">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="114d5-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="114d5-226">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="114d5-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="114d5-227">System-Only</span></span>            | <span data-ttu-id="114d5-228">Falso</span><span class="sxs-lookup"><span data-stu-id="114d5-228">False</span></span>                                                |
| <span data-ttu-id="114d5-229">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="114d5-229">Is-Single-Valued</span></span>       | <span data-ttu-id="114d5-230">Vero</span><span class="sxs-lookup"><span data-stu-id="114d5-230">True</span></span>                                                 |
| <span data-ttu-id="114d5-231">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="114d5-231">Is Indexed</span></span>             | <span data-ttu-id="114d5-232">Falso</span><span class="sxs-lookup"><span data-stu-id="114d5-232">False</span></span>                                                |
| <span data-ttu-id="114d5-233">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="114d5-233">In Global Catalog</span></span>      | <span data-ttu-id="114d5-234">Falso</span><span class="sxs-lookup"><span data-stu-id="114d5-234">False</span></span>                                                |
| <span data-ttu-id="114d5-235">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="114d5-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="114d5-236">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="114d5-236">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="114d5-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="114d5-237">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="114d5-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="114d5-238">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="114d5-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="114d5-239">Search-Flags</span></span>           | <span data-ttu-id="114d5-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="114d5-240">0x00000000</span></span>                                           |
| <span data-ttu-id="114d5-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="114d5-241">System-Flags</span></span>           | <span data-ttu-id="114d5-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="114d5-242">0x00000010</span></span>                                           |
| <span data-ttu-id="114d5-243">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="114d5-243">Classes used in</span></span>        | [<span data-ttu-id="114d5-244">**Dominio trusted**</span><span class="sxs-lookup"><span data-stu-id="114d5-244">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="114d5-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="114d5-245">Windows Server 2012</span></span>



| <span data-ttu-id="114d5-246">Voce</span><span class="sxs-lookup"><span data-stu-id="114d5-246">Entry</span></span> | <span data-ttu-id="114d5-247">Valore</span><span class="sxs-lookup"><span data-stu-id="114d5-247">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="114d5-248">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="114d5-248">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="114d5-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="114d5-249">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="114d5-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="114d5-250">System-Only</span></span>            | <span data-ttu-id="114d5-251">Falso</span><span class="sxs-lookup"><span data-stu-id="114d5-251">False</span></span>                                                |
| <span data-ttu-id="114d5-252">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="114d5-252">Is-Single-Valued</span></span>       | <span data-ttu-id="114d5-253">Vero</span><span class="sxs-lookup"><span data-stu-id="114d5-253">True</span></span>                                                 |
| <span data-ttu-id="114d5-254">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="114d5-254">Is Indexed</span></span>             | <span data-ttu-id="114d5-255">Falso</span><span class="sxs-lookup"><span data-stu-id="114d5-255">False</span></span>                                                |
| <span data-ttu-id="114d5-256">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="114d5-256">In Global Catalog</span></span>      | <span data-ttu-id="114d5-257">Falso</span><span class="sxs-lookup"><span data-stu-id="114d5-257">False</span></span>                                                |
| <span data-ttu-id="114d5-258">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="114d5-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="114d5-259">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="114d5-259">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="114d5-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="114d5-260">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="114d5-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="114d5-261">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="114d5-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="114d5-262">Search-Flags</span></span>           | <span data-ttu-id="114d5-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="114d5-263">0x00000000</span></span>                                           |
| <span data-ttu-id="114d5-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="114d5-264">System-Flags</span></span>           | <span data-ttu-id="114d5-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="114d5-265">0x00000010</span></span>                                           |
| <span data-ttu-id="114d5-266">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="114d5-266">Classes used in</span></span>        | [<span data-ttu-id="114d5-267">**Dominio trusted**</span><span class="sxs-lookup"><span data-stu-id="114d5-267">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



 

 





