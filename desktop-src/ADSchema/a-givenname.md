---
title: Attributo Given-Name
description: Contiene il nome specificato (nome) dell'utente.
ms.assetid: acffe751-9911-4e80-8a26-351a21a6385e
ms.tgt_platform: multiple
keywords:
- Schema AD Given-Name attribute
- Schema AD dell'attributo datoname
topic_type:
- apiref
api_name:
- Given-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a76ab181c6aaf03c2a497be1718df789bfddc6b0
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103875477"
---
# <a name="given-name-attribute"></a><span data-ttu-id="34b63-105">Attributo Given-Name</span><span class="sxs-lookup"><span data-stu-id="34b63-105">Given-Name attribute</span></span>

<span data-ttu-id="34b63-106">Contiene il nome specificato (nome) dell'utente.</span><span class="sxs-lookup"><span data-stu-id="34b63-106">Contains the given name (first name) of the user.</span></span>



| <span data-ttu-id="34b63-107">Voce</span><span class="sxs-lookup"><span data-stu-id="34b63-107">Entry</span></span> | <span data-ttu-id="34b63-108">Valore</span><span class="sxs-lookup"><span data-stu-id="34b63-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="34b63-109">CN</span><span class="sxs-lookup"><span data-stu-id="34b63-109">CN</span></span>                | <span data-ttu-id="34b63-110">Given-Name</span><span class="sxs-lookup"><span data-stu-id="34b63-110">Given-Name</span></span>                                  |
| <span data-ttu-id="34b63-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="34b63-111">Ldap-Display-Name</span></span> | <span data-ttu-id="34b63-112">givenName</span><span class="sxs-lookup"><span data-stu-id="34b63-112">givenName</span></span>                                   |
| <span data-ttu-id="34b63-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="34b63-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="34b63-114">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="34b63-114">Update Privilege</span></span>  | <span data-ttu-id="34b63-115">Amministratore di dominio o proprietario dell'account.</span><span class="sxs-lookup"><span data-stu-id="34b63-115">Domain administrator or account owner.</span></span>      |
| <span data-ttu-id="34b63-116">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="34b63-116">Update Frequency</span></span>  | <span data-ttu-id="34b63-117">Quando viene creato il record dell'utente.</span><span class="sxs-lookup"><span data-stu-id="34b63-117">When the user's record is created.</span></span>          |
| <span data-ttu-id="34b63-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="34b63-118">Attribute-Id</span></span>      | <span data-ttu-id="34b63-119">2.5.4.42</span><span class="sxs-lookup"><span data-stu-id="34b63-119">2.5.4.42</span></span>                                    |
| <span data-ttu-id="34b63-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="34b63-120">System-Id-Guid</span></span>    | <span data-ttu-id="34b63-121">f0f8ff8e-1191-11d0-a060-00aa006c33ed</span><span class="sxs-lookup"><span data-stu-id="34b63-121">f0f8ff8e-1191-11d0-a060-00aa006c33ed</span></span>        |
| <span data-ttu-id="34b63-122">Sintassi</span><span class="sxs-lookup"><span data-stu-id="34b63-122">Syntax</span></span>            | [<span data-ttu-id="34b63-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="34b63-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="34b63-124">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="34b63-124">Implementations</span></span>

-   [<span data-ttu-id="34b63-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="34b63-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="34b63-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="34b63-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="34b63-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="34b63-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="34b63-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="34b63-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="34b63-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="34b63-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="34b63-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="34b63-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="34b63-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="34b63-131">Windows 2000 Server</span></span>



| <span data-ttu-id="34b63-132">Voce</span><span class="sxs-lookup"><span data-stu-id="34b63-132">Entry</span></span> | <span data-ttu-id="34b63-133">Valore</span><span class="sxs-lookup"><span data-stu-id="34b63-133">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="34b63-134">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="34b63-134">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="34b63-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="34b63-135">MAPI-Id</span></span>                | <span data-ttu-id="34b63-136">0x3A06</span><span class="sxs-lookup"><span data-stu-id="34b63-136">0x3A06</span></span>                                                             |
| <span data-ttu-id="34b63-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="34b63-137">System-Only</span></span>            | <span data-ttu-id="34b63-138">Falso</span><span class="sxs-lookup"><span data-stu-id="34b63-138">False</span></span>                                                              |
| <span data-ttu-id="34b63-139">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="34b63-139">Is-Single-Valued</span></span>       | <span data-ttu-id="34b63-140">Vero</span><span class="sxs-lookup"><span data-stu-id="34b63-140">True</span></span>                                                               |
| <span data-ttu-id="34b63-141">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="34b63-141">Is Indexed</span></span>             | <span data-ttu-id="34b63-142">Vero</span><span class="sxs-lookup"><span data-stu-id="34b63-142">True</span></span>                                                               |
| <span data-ttu-id="34b63-143">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="34b63-143">In Global Catalog</span></span>      | <span data-ttu-id="34b63-144">Vero</span><span class="sxs-lookup"><span data-stu-id="34b63-144">True</span></span>                                                               |
| <span data-ttu-id="34b63-145">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="34b63-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="34b63-146">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="34b63-146">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="34b63-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="34b63-147">Range-Lower</span></span>            | <span data-ttu-id="34b63-148">1</span><span class="sxs-lookup"><span data-stu-id="34b63-148">1</span></span>                                                                  |
| <span data-ttu-id="34b63-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="34b63-149">Range-Upper</span></span>            | <span data-ttu-id="34b63-150">64</span><span class="sxs-lookup"><span data-stu-id="34b63-150">64</span></span>                                                                 |
| <span data-ttu-id="34b63-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="34b63-151">Search-Flags</span></span>           | <span data-ttu-id="34b63-152">0x00000005</span><span class="sxs-lookup"><span data-stu-id="34b63-152">0x00000005</span></span>                                                         |
| <span data-ttu-id="34b63-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="34b63-153">System-Flags</span></span>           | <span data-ttu-id="34b63-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="34b63-154">0x00000010</span></span>                                                         |
| <span data-ttu-id="34b63-155">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="34b63-155">Classes used in</span></span>        | [<span data-ttu-id="34b63-156">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="34b63-156">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="34b63-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="34b63-157">Windows Server 2003</span></span>



| <span data-ttu-id="34b63-158">Voce</span><span class="sxs-lookup"><span data-stu-id="34b63-158">Entry</span></span> | <span data-ttu-id="34b63-159">Valore</span><span class="sxs-lookup"><span data-stu-id="34b63-159">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34b63-160">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="34b63-160">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="34b63-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="34b63-161">MAPI-Id</span></span>                | <span data-ttu-id="34b63-162">0x3A06</span><span class="sxs-lookup"><span data-stu-id="34b63-162">0x3A06</span></span>                                                                                                                 |
| <span data-ttu-id="34b63-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="34b63-163">System-Only</span></span>            | <span data-ttu-id="34b63-164">Falso</span><span class="sxs-lookup"><span data-stu-id="34b63-164">False</span></span>                                                                                                                  |
| <span data-ttu-id="34b63-165">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="34b63-165">Is-Single-Valued</span></span>       | <span data-ttu-id="34b63-166">Vero</span><span class="sxs-lookup"><span data-stu-id="34b63-166">True</span></span>                                                                                                                   |
| <span data-ttu-id="34b63-167">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="34b63-167">Is Indexed</span></span>             | <span data-ttu-id="34b63-168">Vero</span><span class="sxs-lookup"><span data-stu-id="34b63-168">True</span></span>                                                                                                                   |
| <span data-ttu-id="34b63-169">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="34b63-169">In Global Catalog</span></span>      | <span data-ttu-id="34b63-170">Vero</span><span class="sxs-lookup"><span data-stu-id="34b63-170">True</span></span>                                                                                                                   |
| <span data-ttu-id="34b63-171">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="34b63-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="34b63-172">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="34b63-172">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="34b63-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="34b63-173">Range-Lower</span></span>            | <span data-ttu-id="34b63-174">1</span><span class="sxs-lookup"><span data-stu-id="34b63-174">1</span></span>                                                                                                                      |
| <span data-ttu-id="34b63-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="34b63-175">Range-Upper</span></span>            | <span data-ttu-id="34b63-176">64</span><span class="sxs-lookup"><span data-stu-id="34b63-176">64</span></span>                                                                                                                     |
| <span data-ttu-id="34b63-177">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="34b63-177">Search-Flags</span></span>           | <span data-ttu-id="34b63-178">0x00000005</span><span class="sxs-lookup"><span data-stu-id="34b63-178">0x00000005</span></span>                                                                                                             |
| <span data-ttu-id="34b63-179">System-Flags</span><span class="sxs-lookup"><span data-stu-id="34b63-179">System-Flags</span></span>           | <span data-ttu-id="34b63-180">0x00000010</span><span class="sxs-lookup"><span data-stu-id="34b63-180">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="34b63-181">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="34b63-181">Classes used in</span></span>        | [<span data-ttu-id="34b63-182">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="34b63-182">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="34b63-183">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="34b63-183">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="34b63-184">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="34b63-184">Windows Server 2003 R2</span></span>



| <span data-ttu-id="34b63-185">Voce</span><span class="sxs-lookup"><span data-stu-id="34b63-185">Entry</span></span> | <span data-ttu-id="34b63-186">Valore</span><span class="sxs-lookup"><span data-stu-id="34b63-186">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34b63-187">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="34b63-187">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="34b63-188">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="34b63-188">MAPI-Id</span></span>                | <span data-ttu-id="34b63-189">0x3A06</span><span class="sxs-lookup"><span data-stu-id="34b63-189">0x3A06</span></span>                                                                                                                 |
| <span data-ttu-id="34b63-190">System-Only</span><span class="sxs-lookup"><span data-stu-id="34b63-190">System-Only</span></span>            | <span data-ttu-id="34b63-191">Falso</span><span class="sxs-lookup"><span data-stu-id="34b63-191">False</span></span>                                                                                                                  |
| <span data-ttu-id="34b63-192">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="34b63-192">Is-Single-Valued</span></span>       | <span data-ttu-id="34b63-193">Vero</span><span class="sxs-lookup"><span data-stu-id="34b63-193">True</span></span>                                                                                                                   |
| <span data-ttu-id="34b63-194">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="34b63-194">Is Indexed</span></span>             | <span data-ttu-id="34b63-195">Vero</span><span class="sxs-lookup"><span data-stu-id="34b63-195">True</span></span>                                                                                                                   |
| <span data-ttu-id="34b63-196">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="34b63-196">In Global Catalog</span></span>      | <span data-ttu-id="34b63-197">Vero</span><span class="sxs-lookup"><span data-stu-id="34b63-197">True</span></span>                                                                                                                   |
| <span data-ttu-id="34b63-198">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="34b63-198">NT-Security-Descriptor</span></span> | <span data-ttu-id="34b63-199">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="34b63-199">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="34b63-200">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="34b63-200">Range-Lower</span></span>            | <span data-ttu-id="34b63-201">1</span><span class="sxs-lookup"><span data-stu-id="34b63-201">1</span></span>                                                                                                                      |
| <span data-ttu-id="34b63-202">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="34b63-202">Range-Upper</span></span>            | <span data-ttu-id="34b63-203">64</span><span class="sxs-lookup"><span data-stu-id="34b63-203">64</span></span>                                                                                                                     |
| <span data-ttu-id="34b63-204">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="34b63-204">Search-Flags</span></span>           | <span data-ttu-id="34b63-205">0x00000005</span><span class="sxs-lookup"><span data-stu-id="34b63-205">0x00000005</span></span>                                                                                                             |
| <span data-ttu-id="34b63-206">System-Flags</span><span class="sxs-lookup"><span data-stu-id="34b63-206">System-Flags</span></span>           | <span data-ttu-id="34b63-207">0x00000010</span><span class="sxs-lookup"><span data-stu-id="34b63-207">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="34b63-208">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="34b63-208">Classes used in</span></span>        | [<span data-ttu-id="34b63-209">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="34b63-209">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="34b63-210">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="34b63-210">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="34b63-211">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="34b63-211">Windows Server 2008</span></span>



| <span data-ttu-id="34b63-212">Voce</span><span class="sxs-lookup"><span data-stu-id="34b63-212">Entry</span></span> | <span data-ttu-id="34b63-213">Valore</span><span class="sxs-lookup"><span data-stu-id="34b63-213">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34b63-214">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="34b63-214">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="34b63-215">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="34b63-215">MAPI-Id</span></span>                | <span data-ttu-id="34b63-216">0x3A06</span><span class="sxs-lookup"><span data-stu-id="34b63-216">0x3A06</span></span>                                                                                                                 |
| <span data-ttu-id="34b63-217">System-Only</span><span class="sxs-lookup"><span data-stu-id="34b63-217">System-Only</span></span>            | <span data-ttu-id="34b63-218">Falso</span><span class="sxs-lookup"><span data-stu-id="34b63-218">False</span></span>                                                                                                                  |
| <span data-ttu-id="34b63-219">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="34b63-219">Is-Single-Valued</span></span>       | <span data-ttu-id="34b63-220">Vero</span><span class="sxs-lookup"><span data-stu-id="34b63-220">True</span></span>                                                                                                                   |
| <span data-ttu-id="34b63-221">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="34b63-221">Is Indexed</span></span>             | <span data-ttu-id="34b63-222">Vero</span><span class="sxs-lookup"><span data-stu-id="34b63-222">True</span></span>                                                                                                                   |
| <span data-ttu-id="34b63-223">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="34b63-223">In Global Catalog</span></span>      | <span data-ttu-id="34b63-224">Vero</span><span class="sxs-lookup"><span data-stu-id="34b63-224">True</span></span>                                                                                                                   |
| <span data-ttu-id="34b63-225">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="34b63-225">NT-Security-Descriptor</span></span> | <span data-ttu-id="34b63-226">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="34b63-226">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="34b63-227">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="34b63-227">Range-Lower</span></span>            | <span data-ttu-id="34b63-228">1</span><span class="sxs-lookup"><span data-stu-id="34b63-228">1</span></span>                                                                                                                      |
| <span data-ttu-id="34b63-229">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="34b63-229">Range-Upper</span></span>            | <span data-ttu-id="34b63-230">64</span><span class="sxs-lookup"><span data-stu-id="34b63-230">64</span></span>                                                                                                                     |
| <span data-ttu-id="34b63-231">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="34b63-231">Search-Flags</span></span>           | <span data-ttu-id="34b63-232">0x00000005</span><span class="sxs-lookup"><span data-stu-id="34b63-232">0x00000005</span></span>                                                                                                             |
| <span data-ttu-id="34b63-233">System-Flags</span><span class="sxs-lookup"><span data-stu-id="34b63-233">System-Flags</span></span>           | <span data-ttu-id="34b63-234">0x00000010</span><span class="sxs-lookup"><span data-stu-id="34b63-234">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="34b63-235">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="34b63-235">Classes used in</span></span>        | [<span data-ttu-id="34b63-236">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="34b63-236">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="34b63-237">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="34b63-237">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="34b63-238">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="34b63-238">Windows Server 2008 R2</span></span>



| <span data-ttu-id="34b63-239">Voce</span><span class="sxs-lookup"><span data-stu-id="34b63-239">Entry</span></span> | <span data-ttu-id="34b63-240">Valore</span><span class="sxs-lookup"><span data-stu-id="34b63-240">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34b63-241">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="34b63-241">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="34b63-242">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="34b63-242">MAPI-Id</span></span>                | <span data-ttu-id="34b63-243">0x3A06</span><span class="sxs-lookup"><span data-stu-id="34b63-243">0x3A06</span></span>                                                                                                                 |
| <span data-ttu-id="34b63-244">System-Only</span><span class="sxs-lookup"><span data-stu-id="34b63-244">System-Only</span></span>            | <span data-ttu-id="34b63-245">Falso</span><span class="sxs-lookup"><span data-stu-id="34b63-245">False</span></span>                                                                                                                  |
| <span data-ttu-id="34b63-246">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="34b63-246">Is-Single-Valued</span></span>       | <span data-ttu-id="34b63-247">Vero</span><span class="sxs-lookup"><span data-stu-id="34b63-247">True</span></span>                                                                                                                   |
| <span data-ttu-id="34b63-248">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="34b63-248">Is Indexed</span></span>             | <span data-ttu-id="34b63-249">Vero</span><span class="sxs-lookup"><span data-stu-id="34b63-249">True</span></span>                                                                                                                   |
| <span data-ttu-id="34b63-250">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="34b63-250">In Global Catalog</span></span>      | <span data-ttu-id="34b63-251">Vero</span><span class="sxs-lookup"><span data-stu-id="34b63-251">True</span></span>                                                                                                                   |
| <span data-ttu-id="34b63-252">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="34b63-252">NT-Security-Descriptor</span></span> | <span data-ttu-id="34b63-253">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="34b63-253">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="34b63-254">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="34b63-254">Range-Lower</span></span>            | <span data-ttu-id="34b63-255">1</span><span class="sxs-lookup"><span data-stu-id="34b63-255">1</span></span>                                                                                                                      |
| <span data-ttu-id="34b63-256">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="34b63-256">Range-Upper</span></span>            | <span data-ttu-id="34b63-257">64</span><span class="sxs-lookup"><span data-stu-id="34b63-257">64</span></span>                                                                                                                     |
| <span data-ttu-id="34b63-258">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="34b63-258">Search-Flags</span></span>           | <span data-ttu-id="34b63-259">0x00000005</span><span class="sxs-lookup"><span data-stu-id="34b63-259">0x00000005</span></span>                                                                                                             |
| <span data-ttu-id="34b63-260">System-Flags</span><span class="sxs-lookup"><span data-stu-id="34b63-260">System-Flags</span></span>           | <span data-ttu-id="34b63-261">0x00000010</span><span class="sxs-lookup"><span data-stu-id="34b63-261">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="34b63-262">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="34b63-262">Classes used in</span></span>        | [<span data-ttu-id="34b63-263">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="34b63-263">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="34b63-264">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="34b63-264">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="34b63-265">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="34b63-265">Windows Server 2012</span></span>



| <span data-ttu-id="34b63-266">Voce</span><span class="sxs-lookup"><span data-stu-id="34b63-266">Entry</span></span> | <span data-ttu-id="34b63-267">Valore</span><span class="sxs-lookup"><span data-stu-id="34b63-267">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34b63-268">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="34b63-268">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="34b63-269">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="34b63-269">MAPI-Id</span></span>                | <span data-ttu-id="34b63-270">0x3A06</span><span class="sxs-lookup"><span data-stu-id="34b63-270">0x3A06</span></span>                                                                                                                 |
| <span data-ttu-id="34b63-271">System-Only</span><span class="sxs-lookup"><span data-stu-id="34b63-271">System-Only</span></span>            | <span data-ttu-id="34b63-272">Falso</span><span class="sxs-lookup"><span data-stu-id="34b63-272">False</span></span>                                                                                                                  |
| <span data-ttu-id="34b63-273">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="34b63-273">Is-Single-Valued</span></span>       | <span data-ttu-id="34b63-274">Vero</span><span class="sxs-lookup"><span data-stu-id="34b63-274">True</span></span>                                                                                                                   |
| <span data-ttu-id="34b63-275">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="34b63-275">Is Indexed</span></span>             | <span data-ttu-id="34b63-276">Vero</span><span class="sxs-lookup"><span data-stu-id="34b63-276">True</span></span>                                                                                                                   |
| <span data-ttu-id="34b63-277">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="34b63-277">In Global Catalog</span></span>      | <span data-ttu-id="34b63-278">Vero</span><span class="sxs-lookup"><span data-stu-id="34b63-278">True</span></span>                                                                                                                   |
| <span data-ttu-id="34b63-279">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="34b63-279">NT-Security-Descriptor</span></span> | <span data-ttu-id="34b63-280">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="34b63-280">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="34b63-281">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="34b63-281">Range-Lower</span></span>            | <span data-ttu-id="34b63-282">1</span><span class="sxs-lookup"><span data-stu-id="34b63-282">1</span></span>                                                                                                                      |
| <span data-ttu-id="34b63-283">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="34b63-283">Range-Upper</span></span>            | <span data-ttu-id="34b63-284">64</span><span class="sxs-lookup"><span data-stu-id="34b63-284">64</span></span>                                                                                                                     |
| <span data-ttu-id="34b63-285">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="34b63-285">Search-Flags</span></span>           | <span data-ttu-id="34b63-286">0x00000005</span><span class="sxs-lookup"><span data-stu-id="34b63-286">0x00000005</span></span>                                                                                                             |
| <span data-ttu-id="34b63-287">System-Flags</span><span class="sxs-lookup"><span data-stu-id="34b63-287">System-Flags</span></span>           | <span data-ttu-id="34b63-288">0x00000010</span><span class="sxs-lookup"><span data-stu-id="34b63-288">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="34b63-289">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="34b63-289">Classes used in</span></span>        | [<span data-ttu-id="34b63-290">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="34b63-290">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="34b63-291">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="34b63-291">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



 

 





