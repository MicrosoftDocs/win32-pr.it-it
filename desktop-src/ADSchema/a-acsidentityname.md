---
title: ACS-Identity-name-attributo
description: Questo attributo contiene il DN di un utente o di un'unità organizzativa ed è l'identità di un utente o di un gruppo di utenti a cui si applicano i criteri QoS.
ms.assetid: 00e6e2bd-aec8-426f-b89e-0661c15cfd46
ms.tgt_platform: multiple
keywords:
- ACS-Identity-name attributo AD schema
- Schema AD dell'attributo aCSIdentityName
topic_type:
- apiref
api_name:
- ACS-Identity-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33ef1db92b908ef8474dfb125aca678d3c22d09f
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104123222"
---
# <a name="acs-identity-name-attribute"></a><span data-ttu-id="25955-105">ACS-Identity-name-attributo</span><span class="sxs-lookup"><span data-stu-id="25955-105">ACS-Identity-Name attribute</span></span>

<span data-ttu-id="25955-106">Questo attributo contiene il DN di un utente o di un'unità organizzativa ed è l'identità di un utente o di un gruppo di utenti a cui si applicano i criteri QoS.</span><span class="sxs-lookup"><span data-stu-id="25955-106">This attribute contains the DN of a user or OU and is the identity of a user or a group of users to which this QoS policy applies.</span></span>



| <span data-ttu-id="25955-107">Voce</span><span class="sxs-lookup"><span data-stu-id="25955-107">Entry</span></span> | <span data-ttu-id="25955-108">Valore</span><span class="sxs-lookup"><span data-stu-id="25955-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="25955-109">CN</span><span class="sxs-lookup"><span data-stu-id="25955-109">CN</span></span>                | <span data-ttu-id="25955-110">Nome-identità ACS</span><span class="sxs-lookup"><span data-stu-id="25955-110">ACS-Identity-Name</span></span>                           |
| <span data-ttu-id="25955-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="25955-111">Ldap-Display-Name</span></span> | <span data-ttu-id="25955-112">aCSIdentityName</span><span class="sxs-lookup"><span data-stu-id="25955-112">aCSIdentityName</span></span>                             |
| <span data-ttu-id="25955-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="25955-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="25955-114">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="25955-114">Update Privilege</span></span>  | <span data-ttu-id="25955-115">Amministratore di dominio</span><span class="sxs-lookup"><span data-stu-id="25955-115">Domain administrator</span></span>                        |
| <span data-ttu-id="25955-116">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="25955-116">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="25955-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="25955-117">Attribute-Id</span></span>      | <span data-ttu-id="25955-118">1.2.840.113556.1.4.784</span><span class="sxs-lookup"><span data-stu-id="25955-118">1.2.840.113556.1.4.784</span></span>                      |
| <span data-ttu-id="25955-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="25955-119">System-Id-Guid</span></span>    | <span data-ttu-id="25955-120">dab029b6-ddf7-11d1-90a5-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="25955-120">dab029b6-ddf7-11d1-90a5-00c04fd91ab1</span></span>        |
| <span data-ttu-id="25955-121">Sintassi</span><span class="sxs-lookup"><span data-stu-id="25955-121">Syntax</span></span>            | [<span data-ttu-id="25955-122">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="25955-122">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="25955-123">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="25955-123">Implementations</span></span>

-   [<span data-ttu-id="25955-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="25955-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="25955-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="25955-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="25955-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="25955-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="25955-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="25955-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="25955-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="25955-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="25955-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="25955-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="25955-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="25955-130">Windows 2000 Server</span></span>



| <span data-ttu-id="25955-131">Voce</span><span class="sxs-lookup"><span data-stu-id="25955-131">Entry</span></span> | <span data-ttu-id="25955-132">Valore</span><span class="sxs-lookup"><span data-stu-id="25955-132">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="25955-133">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="25955-133">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="25955-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="25955-134">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="25955-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="25955-135">System-Only</span></span>            | <span data-ttu-id="25955-136">Falso</span><span class="sxs-lookup"><span data-stu-id="25955-136">False</span></span>                                        |
| <span data-ttu-id="25955-137">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="25955-137">Is-Single-Valued</span></span>       | <span data-ttu-id="25955-138">Falso</span><span class="sxs-lookup"><span data-stu-id="25955-138">False</span></span>                                        |
| <span data-ttu-id="25955-139">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="25955-139">Is Indexed</span></span>             | <span data-ttu-id="25955-140">Falso</span><span class="sxs-lookup"><span data-stu-id="25955-140">False</span></span>                                        |
| <span data-ttu-id="25955-141">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="25955-141">In Global Catalog</span></span>      | <span data-ttu-id="25955-142">Falso</span><span class="sxs-lookup"><span data-stu-id="25955-142">False</span></span>                                        |
| <span data-ttu-id="25955-143">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="25955-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="25955-144">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="25955-144">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="25955-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="25955-145">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="25955-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="25955-146">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="25955-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="25955-147">Search-Flags</span></span>           | <span data-ttu-id="25955-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="25955-148">0x00000000</span></span>                                   |
| <span data-ttu-id="25955-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="25955-149">System-Flags</span></span>           | <span data-ttu-id="25955-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="25955-150">0x00000010</span></span>                                   |
| <span data-ttu-id="25955-151">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="25955-151">Classes used in</span></span>        | [<span data-ttu-id="25955-152">**ACS-criteri**</span><span class="sxs-lookup"><span data-stu-id="25955-152">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="25955-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="25955-153">Windows Server 2003</span></span>



| <span data-ttu-id="25955-154">Voce</span><span class="sxs-lookup"><span data-stu-id="25955-154">Entry</span></span> | <span data-ttu-id="25955-155">Valore</span><span class="sxs-lookup"><span data-stu-id="25955-155">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="25955-156">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="25955-156">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="25955-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="25955-157">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="25955-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="25955-158">System-Only</span></span>            | <span data-ttu-id="25955-159">Falso</span><span class="sxs-lookup"><span data-stu-id="25955-159">False</span></span>                                        |
| <span data-ttu-id="25955-160">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="25955-160">Is-Single-Valued</span></span>       | <span data-ttu-id="25955-161">Falso</span><span class="sxs-lookup"><span data-stu-id="25955-161">False</span></span>                                        |
| <span data-ttu-id="25955-162">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="25955-162">Is Indexed</span></span>             | <span data-ttu-id="25955-163">Falso</span><span class="sxs-lookup"><span data-stu-id="25955-163">False</span></span>                                        |
| <span data-ttu-id="25955-164">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="25955-164">In Global Catalog</span></span>      | <span data-ttu-id="25955-165">Falso</span><span class="sxs-lookup"><span data-stu-id="25955-165">False</span></span>                                        |
| <span data-ttu-id="25955-166">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="25955-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="25955-167">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="25955-167">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="25955-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="25955-168">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="25955-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="25955-169">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="25955-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="25955-170">Search-Flags</span></span>           | <span data-ttu-id="25955-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="25955-171">0x00000000</span></span>                                   |
| <span data-ttu-id="25955-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="25955-172">System-Flags</span></span>           | <span data-ttu-id="25955-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="25955-173">0x00000010</span></span>                                   |
| <span data-ttu-id="25955-174">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="25955-174">Classes used in</span></span>        | [<span data-ttu-id="25955-175">**ACS-criteri**</span><span class="sxs-lookup"><span data-stu-id="25955-175">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="25955-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="25955-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="25955-177">Voce</span><span class="sxs-lookup"><span data-stu-id="25955-177">Entry</span></span> | <span data-ttu-id="25955-178">Valore</span><span class="sxs-lookup"><span data-stu-id="25955-178">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="25955-179">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="25955-179">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="25955-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="25955-180">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="25955-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="25955-181">System-Only</span></span>            | <span data-ttu-id="25955-182">Falso</span><span class="sxs-lookup"><span data-stu-id="25955-182">False</span></span>                                        |
| <span data-ttu-id="25955-183">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="25955-183">Is-Single-Valued</span></span>       | <span data-ttu-id="25955-184">Falso</span><span class="sxs-lookup"><span data-stu-id="25955-184">False</span></span>                                        |
| <span data-ttu-id="25955-185">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="25955-185">Is Indexed</span></span>             | <span data-ttu-id="25955-186">Falso</span><span class="sxs-lookup"><span data-stu-id="25955-186">False</span></span>                                        |
| <span data-ttu-id="25955-187">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="25955-187">In Global Catalog</span></span>      | <span data-ttu-id="25955-188">Falso</span><span class="sxs-lookup"><span data-stu-id="25955-188">False</span></span>                                        |
| <span data-ttu-id="25955-189">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="25955-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="25955-190">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="25955-190">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="25955-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="25955-191">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="25955-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="25955-192">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="25955-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="25955-193">Search-Flags</span></span>           | <span data-ttu-id="25955-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="25955-194">0x00000000</span></span>                                   |
| <span data-ttu-id="25955-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="25955-195">System-Flags</span></span>           | <span data-ttu-id="25955-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="25955-196">0x00000010</span></span>                                   |
| <span data-ttu-id="25955-197">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="25955-197">Classes used in</span></span>        | [<span data-ttu-id="25955-198">**ACS-criteri**</span><span class="sxs-lookup"><span data-stu-id="25955-198">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="25955-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="25955-199">Windows Server 2008</span></span>



| <span data-ttu-id="25955-200">Voce</span><span class="sxs-lookup"><span data-stu-id="25955-200">Entry</span></span> | <span data-ttu-id="25955-201">Valore</span><span class="sxs-lookup"><span data-stu-id="25955-201">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="25955-202">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="25955-202">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="25955-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="25955-203">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="25955-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="25955-204">System-Only</span></span>            | <span data-ttu-id="25955-205">Falso</span><span class="sxs-lookup"><span data-stu-id="25955-205">False</span></span>                                        |
| <span data-ttu-id="25955-206">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="25955-206">Is-Single-Valued</span></span>       | <span data-ttu-id="25955-207">Falso</span><span class="sxs-lookup"><span data-stu-id="25955-207">False</span></span>                                        |
| <span data-ttu-id="25955-208">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="25955-208">Is Indexed</span></span>             | <span data-ttu-id="25955-209">Falso</span><span class="sxs-lookup"><span data-stu-id="25955-209">False</span></span>                                        |
| <span data-ttu-id="25955-210">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="25955-210">In Global Catalog</span></span>      | <span data-ttu-id="25955-211">Falso</span><span class="sxs-lookup"><span data-stu-id="25955-211">False</span></span>                                        |
| <span data-ttu-id="25955-212">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="25955-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="25955-213">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="25955-213">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="25955-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="25955-214">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="25955-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="25955-215">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="25955-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="25955-216">Search-Flags</span></span>           | <span data-ttu-id="25955-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="25955-217">0x00000000</span></span>                                   |
| <span data-ttu-id="25955-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="25955-218">System-Flags</span></span>           | <span data-ttu-id="25955-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="25955-219">0x00000010</span></span>                                   |
| <span data-ttu-id="25955-220">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="25955-220">Classes used in</span></span>        | [<span data-ttu-id="25955-221">**ACS-criteri**</span><span class="sxs-lookup"><span data-stu-id="25955-221">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="25955-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="25955-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="25955-223">Voce</span><span class="sxs-lookup"><span data-stu-id="25955-223">Entry</span></span> | <span data-ttu-id="25955-224">Valore</span><span class="sxs-lookup"><span data-stu-id="25955-224">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="25955-225">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="25955-225">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="25955-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="25955-226">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="25955-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="25955-227">System-Only</span></span>            | <span data-ttu-id="25955-228">Falso</span><span class="sxs-lookup"><span data-stu-id="25955-228">False</span></span>                                        |
| <span data-ttu-id="25955-229">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="25955-229">Is-Single-Valued</span></span>       | <span data-ttu-id="25955-230">Falso</span><span class="sxs-lookup"><span data-stu-id="25955-230">False</span></span>                                        |
| <span data-ttu-id="25955-231">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="25955-231">Is Indexed</span></span>             | <span data-ttu-id="25955-232">Falso</span><span class="sxs-lookup"><span data-stu-id="25955-232">False</span></span>                                        |
| <span data-ttu-id="25955-233">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="25955-233">In Global Catalog</span></span>      | <span data-ttu-id="25955-234">Falso</span><span class="sxs-lookup"><span data-stu-id="25955-234">False</span></span>                                        |
| <span data-ttu-id="25955-235">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="25955-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="25955-236">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="25955-236">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="25955-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="25955-237">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="25955-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="25955-238">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="25955-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="25955-239">Search-Flags</span></span>           | <span data-ttu-id="25955-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="25955-240">0x00000000</span></span>                                   |
| <span data-ttu-id="25955-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="25955-241">System-Flags</span></span>           | <span data-ttu-id="25955-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="25955-242">0x00000010</span></span>                                   |
| <span data-ttu-id="25955-243">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="25955-243">Classes used in</span></span>        | [<span data-ttu-id="25955-244">**ACS-criteri**</span><span class="sxs-lookup"><span data-stu-id="25955-244">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="25955-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="25955-245">Windows Server 2012</span></span>



| <span data-ttu-id="25955-246">Voce</span><span class="sxs-lookup"><span data-stu-id="25955-246">Entry</span></span> | <span data-ttu-id="25955-247">Valore</span><span class="sxs-lookup"><span data-stu-id="25955-247">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="25955-248">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="25955-248">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="25955-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="25955-249">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="25955-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="25955-250">System-Only</span></span>            | <span data-ttu-id="25955-251">Falso</span><span class="sxs-lookup"><span data-stu-id="25955-251">False</span></span>                                        |
| <span data-ttu-id="25955-252">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="25955-252">Is-Single-Valued</span></span>       | <span data-ttu-id="25955-253">Falso</span><span class="sxs-lookup"><span data-stu-id="25955-253">False</span></span>                                        |
| <span data-ttu-id="25955-254">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="25955-254">Is Indexed</span></span>             | <span data-ttu-id="25955-255">Falso</span><span class="sxs-lookup"><span data-stu-id="25955-255">False</span></span>                                        |
| <span data-ttu-id="25955-256">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="25955-256">In Global Catalog</span></span>      | <span data-ttu-id="25955-257">Falso</span><span class="sxs-lookup"><span data-stu-id="25955-257">False</span></span>                                        |
| <span data-ttu-id="25955-258">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="25955-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="25955-259">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="25955-259">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="25955-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="25955-260">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="25955-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="25955-261">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="25955-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="25955-262">Search-Flags</span></span>           | <span data-ttu-id="25955-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="25955-263">0x00000000</span></span>                                   |
| <span data-ttu-id="25955-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="25955-264">System-Flags</span></span>           | <span data-ttu-id="25955-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="25955-265">0x00000010</span></span>                                   |
| <span data-ttu-id="25955-266">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="25955-266">Classes used in</span></span>        | [<span data-ttu-id="25955-267">**ACS-criteri**</span><span class="sxs-lookup"><span data-stu-id="25955-267">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



 

 





