---
title: Attributo Authentication-Options
description: Opzioni di autenticazione utilizzate in ADSI per l'associazione agli oggetti di servizi di directory.
ms.assetid: a6dc4591-d825-456a-8f77-78cb3c91af9f
ms.tgt_platform: multiple
keywords:
- Schema AD Authentication-Options attribute
- Schema AD dell'attributo authenticationOptions
topic_type:
- apiref
api_name:
- Authentication-Options
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cfa9c422dfe196ab002c02c361759461f43965d
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104122179"
---
# <a name="authentication-options-attribute"></a><span data-ttu-id="a5b82-105">Attributo Authentication-Options</span><span class="sxs-lookup"><span data-stu-id="a5b82-105">Authentication-Options attribute</span></span>

<span data-ttu-id="a5b82-106">Opzioni di autenticazione utilizzate in ADSI per l'associazione agli oggetti di servizi di directory.</span><span class="sxs-lookup"><span data-stu-id="a5b82-106">The authentication options used in ADSI to bind to directory services objects.</span></span>



| <span data-ttu-id="a5b82-107">Voce</span><span class="sxs-lookup"><span data-stu-id="a5b82-107">Entry</span></span> | <span data-ttu-id="a5b82-108">Valore</span><span class="sxs-lookup"><span data-stu-id="a5b82-108">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5b82-109">CN</span><span class="sxs-lookup"><span data-stu-id="a5b82-109">CN</span></span>                | <span data-ttu-id="a5b82-110">Authentication-Options</span><span class="sxs-lookup"><span data-stu-id="a5b82-110">Authentication-Options</span></span>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="a5b82-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="a5b82-111">Ldap-Display-Name</span></span> | <span data-ttu-id="a5b82-112">authenticationOptions</span><span class="sxs-lookup"><span data-stu-id="a5b82-112">authenticationOptions</span></span>                                                                                                                                                                                                                                                        |
| <span data-ttu-id="a5b82-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="a5b82-113">Size</span></span>              | <span data-ttu-id="a5b82-114">4 byte.</span><span class="sxs-lookup"><span data-stu-id="a5b82-114">4 bytes.</span></span> <span data-ttu-id="a5b82-115">Valori definiti in IADS. h: ADS \_ Secure \_ Authentication 0x1, Ads \_ use \_ Encryption 0x2, Ads \_ use \_ SSL 0x2, Ads \_ ReadOnly \_ Server 0x4, Ads \_ prompt \_ Credentials 0x8, ADS \_ No \_ Authentication 0x10, Ads \_ Fast \_ Binding 0x20, Ads \_ use \_ signing 0x40, Ads \_ use \_ sealing 0x80</span><span class="sxs-lookup"><span data-stu-id="a5b82-115">Values defined in IADS.h: ADS\_SECURE\_AUTHENTICATION 0x1, ADS\_USE\_ENCRYPTION 0x2, ADS\_USE\_SSL 0x2, ADS\_READONLY\_SERVER 0x4, ADS\_PROMPT\_CREDENTIALS 0x8, ADS\_NO\_AUTHENTICATION 0x10, ADS\_FAST\_BIND 0x20, ADS\_USE\_SIGNING 0x40, ADS\_USE\_SEALING 0x80</span></span> |
| <span data-ttu-id="a5b82-116">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="a5b82-116">Update Privilege</span></span>  | \-                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="a5b82-117">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="a5b82-117">Update Frequency</span></span>  | \-                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="a5b82-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a5b82-118">Attribute-Id</span></span>      | <span data-ttu-id="a5b82-119">1.2.840.113556.1.4.11</span><span class="sxs-lookup"><span data-stu-id="a5b82-119">1.2.840.113556.1.4.11</span></span>                                                                                                                                                                                                                                                        |
| <span data-ttu-id="a5b82-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="a5b82-120">System-Id-Guid</span></span>    | <span data-ttu-id="a5b82-121">bf967928-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="a5b82-121">bf967928-0de6-11d0-a285-00aa003049e2</span></span>                                                                                                                                                                                                                                         |
| <span data-ttu-id="a5b82-122">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a5b82-122">Syntax</span></span>            | [<span data-ttu-id="a5b82-123">**Enumerazione**</span><span class="sxs-lookup"><span data-stu-id="a5b82-123">**Enumeration**</span></span>](s-enumeration.md)                                                                                                                                                                                                                                         |



## <a name="implementations"></a><span data-ttu-id="a5b82-124">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="a5b82-124">Implementations</span></span>

-   [<span data-ttu-id="a5b82-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="a5b82-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="a5b82-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a5b82-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a5b82-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a5b82-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a5b82-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a5b82-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a5b82-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a5b82-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a5b82-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a5b82-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="a5b82-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a5b82-131">Windows 2000 Server</span></span>



| <span data-ttu-id="a5b82-132">Voce</span><span class="sxs-lookup"><span data-stu-id="a5b82-132">Entry</span></span> | <span data-ttu-id="a5b82-133">Valore</span><span class="sxs-lookup"><span data-stu-id="a5b82-133">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="a5b82-134">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="a5b82-134">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="a5b82-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a5b82-135">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="a5b82-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="a5b82-136">System-Only</span></span>            | <span data-ttu-id="a5b82-137">Falso</span><span class="sxs-lookup"><span data-stu-id="a5b82-137">False</span></span>                                              |
| <span data-ttu-id="a5b82-138">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="a5b82-138">Is-Single-Valued</span></span>       | <span data-ttu-id="a5b82-139">Vero</span><span class="sxs-lookup"><span data-stu-id="a5b82-139">True</span></span>                                               |
| <span data-ttu-id="a5b82-140">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="a5b82-140">Is Indexed</span></span>             | <span data-ttu-id="a5b82-141">Falso</span><span class="sxs-lookup"><span data-stu-id="a5b82-141">False</span></span>                                              |
| <span data-ttu-id="a5b82-142">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="a5b82-142">In Global Catalog</span></span>      | <span data-ttu-id="a5b82-143">Falso</span><span class="sxs-lookup"><span data-stu-id="a5b82-143">False</span></span>                                              |
| <span data-ttu-id="a5b82-144">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="a5b82-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="a5b82-145">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="a5b82-145">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="a5b82-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a5b82-146">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="a5b82-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a5b82-147">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="a5b82-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a5b82-148">Search-Flags</span></span>           | <span data-ttu-id="a5b82-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a5b82-149">0x00000000</span></span>                                         |
| <span data-ttu-id="a5b82-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a5b82-150">System-Flags</span></span>           | <span data-ttu-id="a5b82-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a5b82-151">0x00000010</span></span>                                         |
| <span data-ttu-id="a5b82-152">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="a5b82-152">Classes used in</span></span>        | [<span data-ttu-id="a5b82-153">**Criteri di dominio**</span><span class="sxs-lookup"><span data-stu-id="a5b82-153">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="a5b82-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a5b82-154">Windows Server 2003</span></span>



| <span data-ttu-id="a5b82-155">Voce</span><span class="sxs-lookup"><span data-stu-id="a5b82-155">Entry</span></span> | <span data-ttu-id="a5b82-156">Valore</span><span class="sxs-lookup"><span data-stu-id="a5b82-156">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="a5b82-157">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="a5b82-157">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="a5b82-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a5b82-158">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="a5b82-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="a5b82-159">System-Only</span></span>            | <span data-ttu-id="a5b82-160">Falso</span><span class="sxs-lookup"><span data-stu-id="a5b82-160">False</span></span>                                              |
| <span data-ttu-id="a5b82-161">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="a5b82-161">Is-Single-Valued</span></span>       | <span data-ttu-id="a5b82-162">Vero</span><span class="sxs-lookup"><span data-stu-id="a5b82-162">True</span></span>                                               |
| <span data-ttu-id="a5b82-163">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="a5b82-163">Is Indexed</span></span>             | <span data-ttu-id="a5b82-164">Falso</span><span class="sxs-lookup"><span data-stu-id="a5b82-164">False</span></span>                                              |
| <span data-ttu-id="a5b82-165">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="a5b82-165">In Global Catalog</span></span>      | <span data-ttu-id="a5b82-166">Falso</span><span class="sxs-lookup"><span data-stu-id="a5b82-166">False</span></span>                                              |
| <span data-ttu-id="a5b82-167">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="a5b82-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="a5b82-168">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="a5b82-168">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="a5b82-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a5b82-169">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="a5b82-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a5b82-170">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="a5b82-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a5b82-171">Search-Flags</span></span>           | <span data-ttu-id="a5b82-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a5b82-172">0x00000000</span></span>                                         |
| <span data-ttu-id="a5b82-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a5b82-173">System-Flags</span></span>           | <span data-ttu-id="a5b82-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a5b82-174">0x00000010</span></span>                                         |
| <span data-ttu-id="a5b82-175">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="a5b82-175">Classes used in</span></span>        | [<span data-ttu-id="a5b82-176">**Criteri di dominio**</span><span class="sxs-lookup"><span data-stu-id="a5b82-176">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a5b82-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a5b82-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a5b82-178">Voce</span><span class="sxs-lookup"><span data-stu-id="a5b82-178">Entry</span></span> | <span data-ttu-id="a5b82-179">Valore</span><span class="sxs-lookup"><span data-stu-id="a5b82-179">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="a5b82-180">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="a5b82-180">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="a5b82-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a5b82-181">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="a5b82-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="a5b82-182">System-Only</span></span>            | <span data-ttu-id="a5b82-183">Falso</span><span class="sxs-lookup"><span data-stu-id="a5b82-183">False</span></span>                                              |
| <span data-ttu-id="a5b82-184">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="a5b82-184">Is-Single-Valued</span></span>       | <span data-ttu-id="a5b82-185">Vero</span><span class="sxs-lookup"><span data-stu-id="a5b82-185">True</span></span>                                               |
| <span data-ttu-id="a5b82-186">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="a5b82-186">Is Indexed</span></span>             | <span data-ttu-id="a5b82-187">Falso</span><span class="sxs-lookup"><span data-stu-id="a5b82-187">False</span></span>                                              |
| <span data-ttu-id="a5b82-188">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="a5b82-188">In Global Catalog</span></span>      | <span data-ttu-id="a5b82-189">Falso</span><span class="sxs-lookup"><span data-stu-id="a5b82-189">False</span></span>                                              |
| <span data-ttu-id="a5b82-190">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="a5b82-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="a5b82-191">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="a5b82-191">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="a5b82-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a5b82-192">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="a5b82-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a5b82-193">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="a5b82-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a5b82-194">Search-Flags</span></span>           | <span data-ttu-id="a5b82-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a5b82-195">0x00000000</span></span>                                         |
| <span data-ttu-id="a5b82-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a5b82-196">System-Flags</span></span>           | <span data-ttu-id="a5b82-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a5b82-197">0x00000010</span></span>                                         |
| <span data-ttu-id="a5b82-198">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="a5b82-198">Classes used in</span></span>        | [<span data-ttu-id="a5b82-199">**Criteri di dominio**</span><span class="sxs-lookup"><span data-stu-id="a5b82-199">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a5b82-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a5b82-200">Windows Server 2008</span></span>



| <span data-ttu-id="a5b82-201">Voce</span><span class="sxs-lookup"><span data-stu-id="a5b82-201">Entry</span></span> | <span data-ttu-id="a5b82-202">Valore</span><span class="sxs-lookup"><span data-stu-id="a5b82-202">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="a5b82-203">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="a5b82-203">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="a5b82-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a5b82-204">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="a5b82-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="a5b82-205">System-Only</span></span>            | <span data-ttu-id="a5b82-206">Falso</span><span class="sxs-lookup"><span data-stu-id="a5b82-206">False</span></span>                                              |
| <span data-ttu-id="a5b82-207">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="a5b82-207">Is-Single-Valued</span></span>       | <span data-ttu-id="a5b82-208">Vero</span><span class="sxs-lookup"><span data-stu-id="a5b82-208">True</span></span>                                               |
| <span data-ttu-id="a5b82-209">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="a5b82-209">Is Indexed</span></span>             | <span data-ttu-id="a5b82-210">Falso</span><span class="sxs-lookup"><span data-stu-id="a5b82-210">False</span></span>                                              |
| <span data-ttu-id="a5b82-211">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="a5b82-211">In Global Catalog</span></span>      | <span data-ttu-id="a5b82-212">Falso</span><span class="sxs-lookup"><span data-stu-id="a5b82-212">False</span></span>                                              |
| <span data-ttu-id="a5b82-213">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="a5b82-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="a5b82-214">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="a5b82-214">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="a5b82-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a5b82-215">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="a5b82-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a5b82-216">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="a5b82-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a5b82-217">Search-Flags</span></span>           | <span data-ttu-id="a5b82-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a5b82-218">0x00000000</span></span>                                         |
| <span data-ttu-id="a5b82-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a5b82-219">System-Flags</span></span>           | <span data-ttu-id="a5b82-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a5b82-220">0x00000010</span></span>                                         |
| <span data-ttu-id="a5b82-221">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="a5b82-221">Classes used in</span></span>        | [<span data-ttu-id="a5b82-222">**Criteri di dominio**</span><span class="sxs-lookup"><span data-stu-id="a5b82-222">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a5b82-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a5b82-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a5b82-224">Voce</span><span class="sxs-lookup"><span data-stu-id="a5b82-224">Entry</span></span> | <span data-ttu-id="a5b82-225">Valore</span><span class="sxs-lookup"><span data-stu-id="a5b82-225">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="a5b82-226">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="a5b82-226">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="a5b82-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a5b82-227">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="a5b82-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="a5b82-228">System-Only</span></span>            | <span data-ttu-id="a5b82-229">Falso</span><span class="sxs-lookup"><span data-stu-id="a5b82-229">False</span></span>                                              |
| <span data-ttu-id="a5b82-230">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="a5b82-230">Is-Single-Valued</span></span>       | <span data-ttu-id="a5b82-231">Vero</span><span class="sxs-lookup"><span data-stu-id="a5b82-231">True</span></span>                                               |
| <span data-ttu-id="a5b82-232">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="a5b82-232">Is Indexed</span></span>             | <span data-ttu-id="a5b82-233">Falso</span><span class="sxs-lookup"><span data-stu-id="a5b82-233">False</span></span>                                              |
| <span data-ttu-id="a5b82-234">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="a5b82-234">In Global Catalog</span></span>      | <span data-ttu-id="a5b82-235">Falso</span><span class="sxs-lookup"><span data-stu-id="a5b82-235">False</span></span>                                              |
| <span data-ttu-id="a5b82-236">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="a5b82-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="a5b82-237">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="a5b82-237">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="a5b82-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a5b82-238">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="a5b82-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a5b82-239">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="a5b82-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a5b82-240">Search-Flags</span></span>           | <span data-ttu-id="a5b82-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a5b82-241">0x00000000</span></span>                                         |
| <span data-ttu-id="a5b82-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a5b82-242">System-Flags</span></span>           | <span data-ttu-id="a5b82-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a5b82-243">0x00000010</span></span>                                         |
| <span data-ttu-id="a5b82-244">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="a5b82-244">Classes used in</span></span>        | [<span data-ttu-id="a5b82-245">**Criteri di dominio**</span><span class="sxs-lookup"><span data-stu-id="a5b82-245">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a5b82-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a5b82-246">Windows Server 2012</span></span>



| <span data-ttu-id="a5b82-247">Voce</span><span class="sxs-lookup"><span data-stu-id="a5b82-247">Entry</span></span> | <span data-ttu-id="a5b82-248">Valore</span><span class="sxs-lookup"><span data-stu-id="a5b82-248">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="a5b82-249">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="a5b82-249">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="a5b82-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a5b82-250">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="a5b82-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="a5b82-251">System-Only</span></span>            | <span data-ttu-id="a5b82-252">Falso</span><span class="sxs-lookup"><span data-stu-id="a5b82-252">False</span></span>                                              |
| <span data-ttu-id="a5b82-253">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="a5b82-253">Is-Single-Valued</span></span>       | <span data-ttu-id="a5b82-254">Vero</span><span class="sxs-lookup"><span data-stu-id="a5b82-254">True</span></span>                                               |
| <span data-ttu-id="a5b82-255">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="a5b82-255">Is Indexed</span></span>             | <span data-ttu-id="a5b82-256">Falso</span><span class="sxs-lookup"><span data-stu-id="a5b82-256">False</span></span>                                              |
| <span data-ttu-id="a5b82-257">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="a5b82-257">In Global Catalog</span></span>      | <span data-ttu-id="a5b82-258">Falso</span><span class="sxs-lookup"><span data-stu-id="a5b82-258">False</span></span>                                              |
| <span data-ttu-id="a5b82-259">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="a5b82-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="a5b82-260">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="a5b82-260">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="a5b82-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a5b82-261">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="a5b82-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a5b82-262">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="a5b82-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a5b82-263">Search-Flags</span></span>           | <span data-ttu-id="a5b82-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a5b82-264">0x00000000</span></span>                                         |
| <span data-ttu-id="a5b82-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a5b82-265">System-Flags</span></span>           | <span data-ttu-id="a5b82-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a5b82-266">0x00000010</span></span>                                         |
| <span data-ttu-id="a5b82-267">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="a5b82-267">Classes used in</span></span>        | [<span data-ttu-id="a5b82-268">**Criteri di dominio**</span><span class="sxs-lookup"><span data-stu-id="a5b82-268">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



 

 





