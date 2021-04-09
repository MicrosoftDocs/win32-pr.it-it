---
title: Attributo Security-Identifier
description: Valore univoco di lunghezza variabile usato per identificare un account utente, un account di gruppo o una sessione di accesso a cui si applica una voce ACE.
ms.assetid: bb6a16f6-d2c1-48f1-af9a-40fe2a59f281
ms.tgt_platform: multiple
keywords:
- Schema AD Security-Identifier attribute
- Schema AD dell'attributo securityIdentifier
topic_type:
- apiref
api_name:
- Security-Identifier
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4dd921d0bcba08c2174475007476add8e8787456
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744530"
---
# <a name="security-identifier-attribute"></a><span data-ttu-id="04e79-105">Attributo Security-Identifier</span><span class="sxs-lookup"><span data-stu-id="04e79-105">Security-Identifier attribute</span></span>

<span data-ttu-id="04e79-106">Valore univoco di lunghezza variabile usato per identificare un account utente, un account di gruppo o una sessione di accesso a cui si applica una voce ACE.</span><span class="sxs-lookup"><span data-stu-id="04e79-106">A unique value of variable length used to identify a user account, group account, or logon session to which an ACE applies.</span></span>



| <span data-ttu-id="04e79-107">Voce</span><span class="sxs-lookup"><span data-stu-id="04e79-107">Entry</span></span> | <span data-ttu-id="04e79-108">Valore</span><span class="sxs-lookup"><span data-stu-id="04e79-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="04e79-109">CN</span><span class="sxs-lookup"><span data-stu-id="04e79-109">CN</span></span>                | <span data-ttu-id="04e79-110">Security-Identifier</span><span class="sxs-lookup"><span data-stu-id="04e79-110">Security-Identifier</span></span>                  |
| <span data-ttu-id="04e79-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="04e79-111">Ldap-Display-Name</span></span> | <span data-ttu-id="04e79-112">securityIdentifier</span><span class="sxs-lookup"><span data-stu-id="04e79-112">securityIdentifier</span></span>                   |
| <span data-ttu-id="04e79-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="04e79-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="04e79-114">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="04e79-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="04e79-115">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="04e79-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="04e79-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="04e79-116">Attribute-Id</span></span>      | <span data-ttu-id="04e79-117">1.2.840.113556.1.4.121</span><span class="sxs-lookup"><span data-stu-id="04e79-117">1.2.840.113556.1.4.121</span></span>               |
| <span data-ttu-id="04e79-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="04e79-118">System-Id-Guid</span></span>    | <span data-ttu-id="04e79-119">bf967a2f-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="04e79-119">bf967a2f-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="04e79-120">Sintassi</span><span class="sxs-lookup"><span data-stu-id="04e79-120">Syntax</span></span>            | [<span data-ttu-id="04e79-121">**Stringa (SID)**</span><span class="sxs-lookup"><span data-stu-id="04e79-121">**String(Sid)**</span></span>](s-string-sid.md)  |



## <a name="implementations"></a><span data-ttu-id="04e79-122">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="04e79-122">Implementations</span></span>

-   [<span data-ttu-id="04e79-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="04e79-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="04e79-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="04e79-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="04e79-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="04e79-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="04e79-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="04e79-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="04e79-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="04e79-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="04e79-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="04e79-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="04e79-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="04e79-129">Windows 2000 Server</span></span>



| <span data-ttu-id="04e79-130">Voce</span><span class="sxs-lookup"><span data-stu-id="04e79-130">Entry</span></span> | <span data-ttu-id="04e79-131">Valore</span><span class="sxs-lookup"><span data-stu-id="04e79-131">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04e79-132">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="04e79-132">Link-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="04e79-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="04e79-133">MAPI-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="04e79-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="04e79-134">System-Only</span></span>            | <span data-ttu-id="04e79-135">Falso</span><span class="sxs-lookup"><span data-stu-id="04e79-135">False</span></span>                                                                                                             |
| <span data-ttu-id="04e79-136">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="04e79-136">Is-Single-Valued</span></span>       | <span data-ttu-id="04e79-137">Vero</span><span class="sxs-lookup"><span data-stu-id="04e79-137">True</span></span>                                                                                                              |
| <span data-ttu-id="04e79-138">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="04e79-138">Is Indexed</span></span>             | <span data-ttu-id="04e79-139">Falso</span><span class="sxs-lookup"><span data-stu-id="04e79-139">False</span></span>                                                                                                             |
| <span data-ttu-id="04e79-140">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="04e79-140">In Global Catalog</span></span>      | <span data-ttu-id="04e79-141">Falso</span><span class="sxs-lookup"><span data-stu-id="04e79-141">False</span></span>                                                                                                             |
| <span data-ttu-id="04e79-142">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="04e79-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="04e79-143">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="04e79-143">O:BAG:BAD:S:</span></span>                                                                                                      |
| <span data-ttu-id="04e79-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="04e79-144">Range-Lower</span></span>            | \-                                                                                                                |
| <span data-ttu-id="04e79-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="04e79-145">Range-Upper</span></span>            | \-                                                                                                                |
| <span data-ttu-id="04e79-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="04e79-146">Search-Flags</span></span>           | <span data-ttu-id="04e79-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="04e79-147">0x00000000</span></span>                                                                                                        |
| <span data-ttu-id="04e79-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="04e79-148">System-Flags</span></span>           | <span data-ttu-id="04e79-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="04e79-149">0x00000010</span></span>                                                                                                        |
| <span data-ttu-id="04e79-150">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="04e79-150">Classes used in</span></span>        | [<span data-ttu-id="04e79-151">**Entità di sicurezza**</span><span class="sxs-lookup"><span data-stu-id="04e79-151">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> [<span data-ttu-id="04e79-152">**Dominio trusted**</span><span class="sxs-lookup"><span data-stu-id="04e79-152">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="04e79-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="04e79-153">Windows Server 2003</span></span>



| <span data-ttu-id="04e79-154">Voce</span><span class="sxs-lookup"><span data-stu-id="04e79-154">Entry</span></span> | <span data-ttu-id="04e79-155">Valore</span><span class="sxs-lookup"><span data-stu-id="04e79-155">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04e79-156">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="04e79-156">Link-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="04e79-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="04e79-157">MAPI-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="04e79-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="04e79-158">System-Only</span></span>            | <span data-ttu-id="04e79-159">Falso</span><span class="sxs-lookup"><span data-stu-id="04e79-159">False</span></span>                                                                                                             |
| <span data-ttu-id="04e79-160">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="04e79-160">Is-Single-Valued</span></span>       | <span data-ttu-id="04e79-161">Vero</span><span class="sxs-lookup"><span data-stu-id="04e79-161">True</span></span>                                                                                                              |
| <span data-ttu-id="04e79-162">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="04e79-162">Is Indexed</span></span>             | <span data-ttu-id="04e79-163">Falso</span><span class="sxs-lookup"><span data-stu-id="04e79-163">False</span></span>                                                                                                             |
| <span data-ttu-id="04e79-164">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="04e79-164">In Global Catalog</span></span>      | <span data-ttu-id="04e79-165">Vero</span><span class="sxs-lookup"><span data-stu-id="04e79-165">True</span></span>                                                                                                              |
| <span data-ttu-id="04e79-166">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="04e79-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="04e79-167">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="04e79-167">O:BAG:BAD:S:</span></span>                                                                                                      |
| <span data-ttu-id="04e79-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="04e79-168">Range-Lower</span></span>            | \-                                                                                                                |
| <span data-ttu-id="04e79-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="04e79-169">Range-Upper</span></span>            | \-                                                                                                                |
| <span data-ttu-id="04e79-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="04e79-170">Search-Flags</span></span>           | <span data-ttu-id="04e79-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="04e79-171">0x00000000</span></span>                                                                                                        |
| <span data-ttu-id="04e79-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="04e79-172">System-Flags</span></span>           | <span data-ttu-id="04e79-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="04e79-173">0x00000010</span></span>                                                                                                        |
| <span data-ttu-id="04e79-174">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="04e79-174">Classes used in</span></span>        | [<span data-ttu-id="04e79-175">**Entità di sicurezza**</span><span class="sxs-lookup"><span data-stu-id="04e79-175">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> [<span data-ttu-id="04e79-176">**Dominio trusted**</span><span class="sxs-lookup"><span data-stu-id="04e79-176">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="04e79-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="04e79-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="04e79-178">Voce</span><span class="sxs-lookup"><span data-stu-id="04e79-178">Entry</span></span> | <span data-ttu-id="04e79-179">Valore</span><span class="sxs-lookup"><span data-stu-id="04e79-179">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04e79-180">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="04e79-180">Link-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="04e79-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="04e79-181">MAPI-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="04e79-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="04e79-182">System-Only</span></span>            | <span data-ttu-id="04e79-183">Falso</span><span class="sxs-lookup"><span data-stu-id="04e79-183">False</span></span>                                                                                                             |
| <span data-ttu-id="04e79-184">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="04e79-184">Is-Single-Valued</span></span>       | <span data-ttu-id="04e79-185">Vero</span><span class="sxs-lookup"><span data-stu-id="04e79-185">True</span></span>                                                                                                              |
| <span data-ttu-id="04e79-186">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="04e79-186">Is Indexed</span></span>             | <span data-ttu-id="04e79-187">Falso</span><span class="sxs-lookup"><span data-stu-id="04e79-187">False</span></span>                                                                                                             |
| <span data-ttu-id="04e79-188">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="04e79-188">In Global Catalog</span></span>      | <span data-ttu-id="04e79-189">Vero</span><span class="sxs-lookup"><span data-stu-id="04e79-189">True</span></span>                                                                                                              |
| <span data-ttu-id="04e79-190">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="04e79-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="04e79-191">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="04e79-191">O:BAG:BAD:S:</span></span>                                                                                                      |
| <span data-ttu-id="04e79-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="04e79-192">Range-Lower</span></span>            | \-                                                                                                                |
| <span data-ttu-id="04e79-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="04e79-193">Range-Upper</span></span>            | \-                                                                                                                |
| <span data-ttu-id="04e79-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="04e79-194">Search-Flags</span></span>           | <span data-ttu-id="04e79-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="04e79-195">0x00000000</span></span>                                                                                                        |
| <span data-ttu-id="04e79-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="04e79-196">System-Flags</span></span>           | <span data-ttu-id="04e79-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="04e79-197">0x00000010</span></span>                                                                                                        |
| <span data-ttu-id="04e79-198">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="04e79-198">Classes used in</span></span>        | [<span data-ttu-id="04e79-199">**Entità di sicurezza**</span><span class="sxs-lookup"><span data-stu-id="04e79-199">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> [<span data-ttu-id="04e79-200">**Dominio trusted**</span><span class="sxs-lookup"><span data-stu-id="04e79-200">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="04e79-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="04e79-201">Windows Server 2008</span></span>



| <span data-ttu-id="04e79-202">Voce</span><span class="sxs-lookup"><span data-stu-id="04e79-202">Entry</span></span> | <span data-ttu-id="04e79-203">Valore</span><span class="sxs-lookup"><span data-stu-id="04e79-203">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04e79-204">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="04e79-204">Link-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="04e79-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="04e79-205">MAPI-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="04e79-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="04e79-206">System-Only</span></span>            | <span data-ttu-id="04e79-207">Falso</span><span class="sxs-lookup"><span data-stu-id="04e79-207">False</span></span>                                                                                                             |
| <span data-ttu-id="04e79-208">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="04e79-208">Is-Single-Valued</span></span>       | <span data-ttu-id="04e79-209">Vero</span><span class="sxs-lookup"><span data-stu-id="04e79-209">True</span></span>                                                                                                              |
| <span data-ttu-id="04e79-210">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="04e79-210">Is Indexed</span></span>             | <span data-ttu-id="04e79-211">Falso</span><span class="sxs-lookup"><span data-stu-id="04e79-211">False</span></span>                                                                                                             |
| <span data-ttu-id="04e79-212">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="04e79-212">In Global Catalog</span></span>      | <span data-ttu-id="04e79-213">Vero</span><span class="sxs-lookup"><span data-stu-id="04e79-213">True</span></span>                                                                                                              |
| <span data-ttu-id="04e79-214">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="04e79-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="04e79-215">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="04e79-215">O:BAG:BAD:S:</span></span>                                                                                                      |
| <span data-ttu-id="04e79-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="04e79-216">Range-Lower</span></span>            | \-                                                                                                                |
| <span data-ttu-id="04e79-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="04e79-217">Range-Upper</span></span>            | \-                                                                                                                |
| <span data-ttu-id="04e79-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="04e79-218">Search-Flags</span></span>           | <span data-ttu-id="04e79-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="04e79-219">0x00000000</span></span>                                                                                                        |
| <span data-ttu-id="04e79-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="04e79-220">System-Flags</span></span>           | <span data-ttu-id="04e79-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="04e79-221">0x00000010</span></span>                                                                                                        |
| <span data-ttu-id="04e79-222">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="04e79-222">Classes used in</span></span>        | [<span data-ttu-id="04e79-223">**Entità di sicurezza**</span><span class="sxs-lookup"><span data-stu-id="04e79-223">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> [<span data-ttu-id="04e79-224">**Dominio trusted**</span><span class="sxs-lookup"><span data-stu-id="04e79-224">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="04e79-225">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="04e79-225">Windows Server 2008 R2</span></span>



| <span data-ttu-id="04e79-226">Voce</span><span class="sxs-lookup"><span data-stu-id="04e79-226">Entry</span></span> | <span data-ttu-id="04e79-227">Valore</span><span class="sxs-lookup"><span data-stu-id="04e79-227">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04e79-228">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="04e79-228">Link-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="04e79-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="04e79-229">MAPI-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="04e79-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="04e79-230">System-Only</span></span>            | <span data-ttu-id="04e79-231">Falso</span><span class="sxs-lookup"><span data-stu-id="04e79-231">False</span></span>                                                                                                             |
| <span data-ttu-id="04e79-232">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="04e79-232">Is-Single-Valued</span></span>       | <span data-ttu-id="04e79-233">Vero</span><span class="sxs-lookup"><span data-stu-id="04e79-233">True</span></span>                                                                                                              |
| <span data-ttu-id="04e79-234">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="04e79-234">Is Indexed</span></span>             | <span data-ttu-id="04e79-235">Falso</span><span class="sxs-lookup"><span data-stu-id="04e79-235">False</span></span>                                                                                                             |
| <span data-ttu-id="04e79-236">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="04e79-236">In Global Catalog</span></span>      | <span data-ttu-id="04e79-237">Vero</span><span class="sxs-lookup"><span data-stu-id="04e79-237">True</span></span>                                                                                                              |
| <span data-ttu-id="04e79-238">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="04e79-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="04e79-239">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="04e79-239">O:BAG:BAD:S:</span></span>                                                                                                      |
| <span data-ttu-id="04e79-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="04e79-240">Range-Lower</span></span>            | \-                                                                                                                |
| <span data-ttu-id="04e79-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="04e79-241">Range-Upper</span></span>            | \-                                                                                                                |
| <span data-ttu-id="04e79-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="04e79-242">Search-Flags</span></span>           | <span data-ttu-id="04e79-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="04e79-243">0x00000000</span></span>                                                                                                        |
| <span data-ttu-id="04e79-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="04e79-244">System-Flags</span></span>           | <span data-ttu-id="04e79-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="04e79-245">0x00000010</span></span>                                                                                                        |
| <span data-ttu-id="04e79-246">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="04e79-246">Classes used in</span></span>        | [<span data-ttu-id="04e79-247">**Entità di sicurezza**</span><span class="sxs-lookup"><span data-stu-id="04e79-247">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> [<span data-ttu-id="04e79-248">**Dominio trusted**</span><span class="sxs-lookup"><span data-stu-id="04e79-248">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="04e79-249">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="04e79-249">Windows Server 2012</span></span>



| <span data-ttu-id="04e79-250">Voce</span><span class="sxs-lookup"><span data-stu-id="04e79-250">Entry</span></span> | <span data-ttu-id="04e79-251">Valore</span><span class="sxs-lookup"><span data-stu-id="04e79-251">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04e79-252">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="04e79-252">Link-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="04e79-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="04e79-253">MAPI-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="04e79-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="04e79-254">System-Only</span></span>            | <span data-ttu-id="04e79-255">Falso</span><span class="sxs-lookup"><span data-stu-id="04e79-255">False</span></span>                                                                                                             |
| <span data-ttu-id="04e79-256">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="04e79-256">Is-Single-Valued</span></span>       | <span data-ttu-id="04e79-257">Vero</span><span class="sxs-lookup"><span data-stu-id="04e79-257">True</span></span>                                                                                                              |
| <span data-ttu-id="04e79-258">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="04e79-258">Is Indexed</span></span>             | <span data-ttu-id="04e79-259">Falso</span><span class="sxs-lookup"><span data-stu-id="04e79-259">False</span></span>                                                                                                             |
| <span data-ttu-id="04e79-260">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="04e79-260">In Global Catalog</span></span>      | <span data-ttu-id="04e79-261">Vero</span><span class="sxs-lookup"><span data-stu-id="04e79-261">True</span></span>                                                                                                              |
| <span data-ttu-id="04e79-262">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="04e79-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="04e79-263">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="04e79-263">O:BAG:BAD:S:</span></span>                                                                                                      |
| <span data-ttu-id="04e79-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="04e79-264">Range-Lower</span></span>            | \-                                                                                                                |
| <span data-ttu-id="04e79-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="04e79-265">Range-Upper</span></span>            | \-                                                                                                                |
| <span data-ttu-id="04e79-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="04e79-266">Search-Flags</span></span>           | <span data-ttu-id="04e79-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="04e79-267">0x00000000</span></span>                                                                                                        |
| <span data-ttu-id="04e79-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="04e79-268">System-Flags</span></span>           | <span data-ttu-id="04e79-269">0x00000010</span><span class="sxs-lookup"><span data-stu-id="04e79-269">0x00000010</span></span>                                                                                                        |
| <span data-ttu-id="04e79-270">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="04e79-270">Classes used in</span></span>        | [<span data-ttu-id="04e79-271">**Entità di sicurezza**</span><span class="sxs-lookup"><span data-stu-id="04e79-271">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> [<span data-ttu-id="04e79-272">**Dominio trusted**</span><span class="sxs-lookup"><span data-stu-id="04e79-272">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



 

 





