---
title: Alt-Security-identitys (attributo)
description: Contiene i mapping per i certificati X. 509 o gli account utente Kerberos esterni a questo utente ai fini dell'autenticazione.
ms.assetid: 40b2af9c-fd4f-4883-8494-2b64682ee50c
ms.tgt_platform: multiple
keywords:
- Alt-Security-identitys attributo AD schema
- Schema AD dell'attributo altSecurityIdentities
topic_type:
- apiref
api_name:
- Alt-Security-Identities
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2548e337f29778400bb173a8c15d928d7b06d988
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103965144"
---
# <a name="alt-security-identities-attribute"></a><span data-ttu-id="92ac1-105">Alt-Security-identitys (attributo)</span><span class="sxs-lookup"><span data-stu-id="92ac1-105">Alt-Security-Identities attribute</span></span>

<span data-ttu-id="92ac1-106">Contiene i mapping per i certificati X. 509 o gli account utente Kerberos esterni a questo utente ai fini dell'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="92ac1-106">Contains mappings for X.509 certificates or external Kerberos user accounts to this user for the purpose of authentication.</span></span>



| <span data-ttu-id="92ac1-107">Voce</span><span class="sxs-lookup"><span data-stu-id="92ac1-107">Entry</span></span> | <span data-ttu-id="92ac1-108">Valore</span><span class="sxs-lookup"><span data-stu-id="92ac1-108">Value</span></span> |
|-------------------|-----------------------------------------------------|
| <span data-ttu-id="92ac1-109">CN</span><span class="sxs-lookup"><span data-stu-id="92ac1-109">CN</span></span>                | <span data-ttu-id="92ac1-110">Alt-sicurezza-identità</span><span class="sxs-lookup"><span data-stu-id="92ac1-110">Alt-Security-Identities</span></span>                             |
| <span data-ttu-id="92ac1-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="92ac1-111">Ldap-Display-Name</span></span> | <span data-ttu-id="92ac1-112">altSecurityIdentities</span><span class="sxs-lookup"><span data-stu-id="92ac1-112">altSecurityIdentities</span></span>                               |
| <span data-ttu-id="92ac1-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="92ac1-113">Size</span></span>              | \-                                                  |
| <span data-ttu-id="92ac1-114">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="92ac1-114">Update Privilege</span></span>  | <span data-ttu-id="92ac1-115">Amministratore di dominio</span><span class="sxs-lookup"><span data-stu-id="92ac1-115">Domain administrator</span></span>                                |
| <span data-ttu-id="92ac1-116">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="92ac1-116">Update Frequency</span></span>  | <span data-ttu-id="92ac1-117">Ogni volta che è necessario un nuovo meccanismo di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="92ac1-117">Each time a new authentication mechanism is needed.</span></span> |
| <span data-ttu-id="92ac1-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="92ac1-118">Attribute-Id</span></span>      | <span data-ttu-id="92ac1-119">1.2.840.113556.1.4.867</span><span class="sxs-lookup"><span data-stu-id="92ac1-119">1.2.840.113556.1.4.867</span></span>                              |
| <span data-ttu-id="92ac1-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="92ac1-120">System-Id-Guid</span></span>    | <span data-ttu-id="92ac1-121">00fbf30c-91fe-11d1-aebc-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="92ac1-121">00fbf30c-91fe-11d1-aebc-0000f80367c1</span></span>                |
| <span data-ttu-id="92ac1-122">Sintassi</span><span class="sxs-lookup"><span data-stu-id="92ac1-122">Syntax</span></span>            | [<span data-ttu-id="92ac1-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="92ac1-123">**String(Unicode)**</span></span>](s-string-unicode.md)         |



## <a name="implementations"></a><span data-ttu-id="92ac1-124">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="92ac1-124">Implementations</span></span>

-   [<span data-ttu-id="92ac1-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="92ac1-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="92ac1-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="92ac1-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="92ac1-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="92ac1-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="92ac1-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="92ac1-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="92ac1-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="92ac1-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="92ac1-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="92ac1-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="92ac1-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="92ac1-131">Windows 2000 Server</span></span>



| <span data-ttu-id="92ac1-132">Voce</span><span class="sxs-lookup"><span data-stu-id="92ac1-132">Entry</span></span> | <span data-ttu-id="92ac1-133">Valore</span><span class="sxs-lookup"><span data-stu-id="92ac1-133">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="92ac1-134">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="92ac1-134">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="92ac1-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="92ac1-135">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="92ac1-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="92ac1-136">System-Only</span></span>            | <span data-ttu-id="92ac1-137">Falso</span><span class="sxs-lookup"><span data-stu-id="92ac1-137">False</span></span>                                                        |
| <span data-ttu-id="92ac1-138">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="92ac1-138">Is-Single-Valued</span></span>       | <span data-ttu-id="92ac1-139">Falso</span><span class="sxs-lookup"><span data-stu-id="92ac1-139">False</span></span>                                                        |
| <span data-ttu-id="92ac1-140">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="92ac1-140">Is Indexed</span></span>             | <span data-ttu-id="92ac1-141">Vero</span><span class="sxs-lookup"><span data-stu-id="92ac1-141">True</span></span>                                                         |
| <span data-ttu-id="92ac1-142">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="92ac1-142">In Global Catalog</span></span>      | <span data-ttu-id="92ac1-143">Vero</span><span class="sxs-lookup"><span data-stu-id="92ac1-143">True</span></span>                                                         |
| <span data-ttu-id="92ac1-144">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="92ac1-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="92ac1-145">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="92ac1-145">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="92ac1-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="92ac1-146">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="92ac1-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="92ac1-147">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="92ac1-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="92ac1-148">Search-Flags</span></span>           | <span data-ttu-id="92ac1-149">0x00000001</span><span class="sxs-lookup"><span data-stu-id="92ac1-149">0x00000001</span></span>                                                   |
| <span data-ttu-id="92ac1-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="92ac1-150">System-Flags</span></span>           | <span data-ttu-id="92ac1-151">0x00000012</span><span class="sxs-lookup"><span data-stu-id="92ac1-151">0x00000012</span></span>                                                   |
| <span data-ttu-id="92ac1-152">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="92ac1-152">Classes used in</span></span>        | [<span data-ttu-id="92ac1-153">**Entità di sicurezza**</span><span class="sxs-lookup"><span data-stu-id="92ac1-153">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="92ac1-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="92ac1-154">Windows Server 2003</span></span>



| <span data-ttu-id="92ac1-155">Voce</span><span class="sxs-lookup"><span data-stu-id="92ac1-155">Entry</span></span> | <span data-ttu-id="92ac1-156">Valore</span><span class="sxs-lookup"><span data-stu-id="92ac1-156">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="92ac1-157">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="92ac1-157">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="92ac1-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="92ac1-158">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="92ac1-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="92ac1-159">System-Only</span></span>            | <span data-ttu-id="92ac1-160">Falso</span><span class="sxs-lookup"><span data-stu-id="92ac1-160">False</span></span>                                                        |
| <span data-ttu-id="92ac1-161">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="92ac1-161">Is-Single-Valued</span></span>       | <span data-ttu-id="92ac1-162">Falso</span><span class="sxs-lookup"><span data-stu-id="92ac1-162">False</span></span>                                                        |
| <span data-ttu-id="92ac1-163">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="92ac1-163">Is Indexed</span></span>             | <span data-ttu-id="92ac1-164">Vero</span><span class="sxs-lookup"><span data-stu-id="92ac1-164">True</span></span>                                                         |
| <span data-ttu-id="92ac1-165">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="92ac1-165">In Global Catalog</span></span>      | <span data-ttu-id="92ac1-166">Vero</span><span class="sxs-lookup"><span data-stu-id="92ac1-166">True</span></span>                                                         |
| <span data-ttu-id="92ac1-167">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="92ac1-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="92ac1-168">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="92ac1-168">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="92ac1-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="92ac1-169">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="92ac1-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="92ac1-170">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="92ac1-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="92ac1-171">Search-Flags</span></span>           | <span data-ttu-id="92ac1-172">0x00000001</span><span class="sxs-lookup"><span data-stu-id="92ac1-172">0x00000001</span></span>                                                   |
| <span data-ttu-id="92ac1-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="92ac1-173">System-Flags</span></span>           | <span data-ttu-id="92ac1-174">0x00000012</span><span class="sxs-lookup"><span data-stu-id="92ac1-174">0x00000012</span></span>                                                   |
| <span data-ttu-id="92ac1-175">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="92ac1-175">Classes used in</span></span>        | [<span data-ttu-id="92ac1-176">**Entità di sicurezza**</span><span class="sxs-lookup"><span data-stu-id="92ac1-176">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="92ac1-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="92ac1-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="92ac1-178">Voce</span><span class="sxs-lookup"><span data-stu-id="92ac1-178">Entry</span></span> | <span data-ttu-id="92ac1-179">Valore</span><span class="sxs-lookup"><span data-stu-id="92ac1-179">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="92ac1-180">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="92ac1-180">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="92ac1-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="92ac1-181">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="92ac1-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="92ac1-182">System-Only</span></span>            | <span data-ttu-id="92ac1-183">Falso</span><span class="sxs-lookup"><span data-stu-id="92ac1-183">False</span></span>                                                        |
| <span data-ttu-id="92ac1-184">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="92ac1-184">Is-Single-Valued</span></span>       | <span data-ttu-id="92ac1-185">Falso</span><span class="sxs-lookup"><span data-stu-id="92ac1-185">False</span></span>                                                        |
| <span data-ttu-id="92ac1-186">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="92ac1-186">Is Indexed</span></span>             | <span data-ttu-id="92ac1-187">Vero</span><span class="sxs-lookup"><span data-stu-id="92ac1-187">True</span></span>                                                         |
| <span data-ttu-id="92ac1-188">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="92ac1-188">In Global Catalog</span></span>      | <span data-ttu-id="92ac1-189">Vero</span><span class="sxs-lookup"><span data-stu-id="92ac1-189">True</span></span>                                                         |
| <span data-ttu-id="92ac1-190">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="92ac1-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="92ac1-191">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="92ac1-191">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="92ac1-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="92ac1-192">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="92ac1-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="92ac1-193">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="92ac1-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="92ac1-194">Search-Flags</span></span>           | <span data-ttu-id="92ac1-195">0x00000001</span><span class="sxs-lookup"><span data-stu-id="92ac1-195">0x00000001</span></span>                                                   |
| <span data-ttu-id="92ac1-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="92ac1-196">System-Flags</span></span>           | <span data-ttu-id="92ac1-197">0x00000012</span><span class="sxs-lookup"><span data-stu-id="92ac1-197">0x00000012</span></span>                                                   |
| <span data-ttu-id="92ac1-198">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="92ac1-198">Classes used in</span></span>        | [<span data-ttu-id="92ac1-199">**Entità di sicurezza**</span><span class="sxs-lookup"><span data-stu-id="92ac1-199">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="92ac1-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="92ac1-200">Windows Server 2008</span></span>



| <span data-ttu-id="92ac1-201">Voce</span><span class="sxs-lookup"><span data-stu-id="92ac1-201">Entry</span></span> | <span data-ttu-id="92ac1-202">Valore</span><span class="sxs-lookup"><span data-stu-id="92ac1-202">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="92ac1-203">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="92ac1-203">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="92ac1-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="92ac1-204">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="92ac1-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="92ac1-205">System-Only</span></span>            | <span data-ttu-id="92ac1-206">Falso</span><span class="sxs-lookup"><span data-stu-id="92ac1-206">False</span></span>                                                        |
| <span data-ttu-id="92ac1-207">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="92ac1-207">Is-Single-Valued</span></span>       | <span data-ttu-id="92ac1-208">Falso</span><span class="sxs-lookup"><span data-stu-id="92ac1-208">False</span></span>                                                        |
| <span data-ttu-id="92ac1-209">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="92ac1-209">Is Indexed</span></span>             | <span data-ttu-id="92ac1-210">Vero</span><span class="sxs-lookup"><span data-stu-id="92ac1-210">True</span></span>                                                         |
| <span data-ttu-id="92ac1-211">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="92ac1-211">In Global Catalog</span></span>      | <span data-ttu-id="92ac1-212">Vero</span><span class="sxs-lookup"><span data-stu-id="92ac1-212">True</span></span>                                                         |
| <span data-ttu-id="92ac1-213">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="92ac1-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="92ac1-214">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="92ac1-214">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="92ac1-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="92ac1-215">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="92ac1-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="92ac1-216">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="92ac1-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="92ac1-217">Search-Flags</span></span>           | <span data-ttu-id="92ac1-218">0x00000001</span><span class="sxs-lookup"><span data-stu-id="92ac1-218">0x00000001</span></span>                                                   |
| <span data-ttu-id="92ac1-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="92ac1-219">System-Flags</span></span>           | <span data-ttu-id="92ac1-220">0x00000012</span><span class="sxs-lookup"><span data-stu-id="92ac1-220">0x00000012</span></span>                                                   |
| <span data-ttu-id="92ac1-221">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="92ac1-221">Classes used in</span></span>        | [<span data-ttu-id="92ac1-222">**Entità di sicurezza**</span><span class="sxs-lookup"><span data-stu-id="92ac1-222">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="92ac1-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="92ac1-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="92ac1-224">Voce</span><span class="sxs-lookup"><span data-stu-id="92ac1-224">Entry</span></span> | <span data-ttu-id="92ac1-225">Valore</span><span class="sxs-lookup"><span data-stu-id="92ac1-225">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="92ac1-226">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="92ac1-226">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="92ac1-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="92ac1-227">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="92ac1-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="92ac1-228">System-Only</span></span>            | <span data-ttu-id="92ac1-229">Falso</span><span class="sxs-lookup"><span data-stu-id="92ac1-229">False</span></span>                                                        |
| <span data-ttu-id="92ac1-230">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="92ac1-230">Is-Single-Valued</span></span>       | <span data-ttu-id="92ac1-231">Falso</span><span class="sxs-lookup"><span data-stu-id="92ac1-231">False</span></span>                                                        |
| <span data-ttu-id="92ac1-232">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="92ac1-232">Is Indexed</span></span>             | <span data-ttu-id="92ac1-233">Vero</span><span class="sxs-lookup"><span data-stu-id="92ac1-233">True</span></span>                                                         |
| <span data-ttu-id="92ac1-234">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="92ac1-234">In Global Catalog</span></span>      | <span data-ttu-id="92ac1-235">Vero</span><span class="sxs-lookup"><span data-stu-id="92ac1-235">True</span></span>                                                         |
| <span data-ttu-id="92ac1-236">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="92ac1-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="92ac1-237">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="92ac1-237">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="92ac1-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="92ac1-238">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="92ac1-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="92ac1-239">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="92ac1-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="92ac1-240">Search-Flags</span></span>           | <span data-ttu-id="92ac1-241">0x00000001</span><span class="sxs-lookup"><span data-stu-id="92ac1-241">0x00000001</span></span>                                                   |
| <span data-ttu-id="92ac1-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="92ac1-242">System-Flags</span></span>           | <span data-ttu-id="92ac1-243">0x00000012</span><span class="sxs-lookup"><span data-stu-id="92ac1-243">0x00000012</span></span>                                                   |
| <span data-ttu-id="92ac1-244">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="92ac1-244">Classes used in</span></span>        | [<span data-ttu-id="92ac1-245">**Entità di sicurezza**</span><span class="sxs-lookup"><span data-stu-id="92ac1-245">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="92ac1-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="92ac1-246">Windows Server 2012</span></span>



| <span data-ttu-id="92ac1-247">Voce</span><span class="sxs-lookup"><span data-stu-id="92ac1-247">Entry</span></span> | <span data-ttu-id="92ac1-248">Valore</span><span class="sxs-lookup"><span data-stu-id="92ac1-248">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="92ac1-249">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="92ac1-249">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="92ac1-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="92ac1-250">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="92ac1-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="92ac1-251">System-Only</span></span>            | <span data-ttu-id="92ac1-252">Falso</span><span class="sxs-lookup"><span data-stu-id="92ac1-252">False</span></span>                                                        |
| <span data-ttu-id="92ac1-253">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="92ac1-253">Is-Single-Valued</span></span>       | <span data-ttu-id="92ac1-254">Falso</span><span class="sxs-lookup"><span data-stu-id="92ac1-254">False</span></span>                                                        |
| <span data-ttu-id="92ac1-255">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="92ac1-255">Is Indexed</span></span>             | <span data-ttu-id="92ac1-256">Vero</span><span class="sxs-lookup"><span data-stu-id="92ac1-256">True</span></span>                                                         |
| <span data-ttu-id="92ac1-257">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="92ac1-257">In Global Catalog</span></span>      | <span data-ttu-id="92ac1-258">Vero</span><span class="sxs-lookup"><span data-stu-id="92ac1-258">True</span></span>                                                         |
| <span data-ttu-id="92ac1-259">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="92ac1-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="92ac1-260">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="92ac1-260">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="92ac1-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="92ac1-261">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="92ac1-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="92ac1-262">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="92ac1-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="92ac1-263">Search-Flags</span></span>           | <span data-ttu-id="92ac1-264">0x00000001</span><span class="sxs-lookup"><span data-stu-id="92ac1-264">0x00000001</span></span>                                                   |
| <span data-ttu-id="92ac1-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="92ac1-265">System-Flags</span></span>           | <span data-ttu-id="92ac1-266">0x00000012</span><span class="sxs-lookup"><span data-stu-id="92ac1-266">0x00000012</span></span>                                                   |
| <span data-ttu-id="92ac1-267">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="92ac1-267">Classes used in</span></span>        | [<span data-ttu-id="92ac1-268">**Entità di sicurezza**</span><span class="sxs-lookup"><span data-stu-id="92ac1-268">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



 

 





