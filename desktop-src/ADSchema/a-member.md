---
title: Attributo member
description: Elenco di utenti che appartengono al gruppo.
ms.assetid: 0f5e249e-1fa1-4191-90e6-94c0b657b7fc
ms.tgt_platform: multiple
keywords:
- Schema di AD dell'attributo membro
- Schema di AD dell'attributo membro
topic_type:
- apiref
api_name:
- Member
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c237c7cb7b41ae73bcbdff5a13f6cb34f546449b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "106302983"
---
# <a name="member-attribute"></a><span data-ttu-id="b7cf1-105">Attributo member</span><span class="sxs-lookup"><span data-stu-id="b7cf1-105">Member attribute</span></span>

<span data-ttu-id="b7cf1-106">Elenco di utenti che appartengono al gruppo.</span><span class="sxs-lookup"><span data-stu-id="b7cf1-106">The list of users that belong to the group.</span></span>



| <span data-ttu-id="b7cf1-107">Voce</span><span class="sxs-lookup"><span data-stu-id="b7cf1-107">Entry</span></span> | <span data-ttu-id="b7cf1-108">Valore</span><span class="sxs-lookup"><span data-stu-id="b7cf1-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="b7cf1-109">CN</span><span class="sxs-lookup"><span data-stu-id="b7cf1-109">CN</span></span>                | <span data-ttu-id="b7cf1-110">Membro</span><span class="sxs-lookup"><span data-stu-id="b7cf1-110">Member</span></span>                                                |
| <span data-ttu-id="b7cf1-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="b7cf1-111">Ldap-Display-Name</span></span> | <span data-ttu-id="b7cf1-112">member</span><span class="sxs-lookup"><span data-stu-id="b7cf1-112">member</span></span>                                                |
| <span data-ttu-id="b7cf1-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="b7cf1-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="b7cf1-114">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="b7cf1-114">Update Privilege</span></span>  | <span data-ttu-id="b7cf1-115">Amministratore di dominio</span><span class="sxs-lookup"><span data-stu-id="b7cf1-115">Domain administrator</span></span>                                  |
| <span data-ttu-id="b7cf1-116">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="b7cf1-116">Update Frequency</span></span>  | <span data-ttu-id="b7cf1-117">Ogni volta che un utente viene aggiunto o rimosso da un gruppo.</span><span class="sxs-lookup"><span data-stu-id="b7cf1-117">Each time a user is added to or removed from a group.</span></span> |
| <span data-ttu-id="b7cf1-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b7cf1-118">Attribute-Id</span></span>      | <span data-ttu-id="b7cf1-119">2.5.4.31</span><span class="sxs-lookup"><span data-stu-id="b7cf1-119">2.5.4.31</span></span>                                              |
| <span data-ttu-id="b7cf1-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="b7cf1-120">System-Id-Guid</span></span>    | <span data-ttu-id="b7cf1-121">bf9679c0-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="b7cf1-121">bf9679c0-0de6-11d0-a285-00aa003049e2</span></span>                  |
| <span data-ttu-id="b7cf1-122">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b7cf1-122">Syntax</span></span>            | [<span data-ttu-id="b7cf1-123">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="b7cf1-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md)               |



## <a name="implementations"></a><span data-ttu-id="b7cf1-124">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="b7cf1-124">Implementations</span></span>

-   [<span data-ttu-id="b7cf1-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="b7cf1-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="b7cf1-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b7cf1-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b7cf1-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="b7cf1-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="b7cf1-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b7cf1-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b7cf1-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b7cf1-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b7cf1-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b7cf1-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b7cf1-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b7cf1-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="b7cf1-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b7cf1-132">Windows 2000 Server</span></span>



| <span data-ttu-id="b7cf1-133">Voce</span><span class="sxs-lookup"><span data-stu-id="b7cf1-133">Entry</span></span> | <span data-ttu-id="b7cf1-134">Valore</span><span class="sxs-lookup"><span data-stu-id="b7cf1-134">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b7cf1-135">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="b7cf1-135">Link-Id</span></span>                | <span data-ttu-id="b7cf1-136">2</span><span class="sxs-lookup"><span data-stu-id="b7cf1-136">2</span></span>                                                                                       |
| <span data-ttu-id="b7cf1-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b7cf1-137">MAPI-Id</span></span>                | <span data-ttu-id="b7cf1-138">0x8009</span><span class="sxs-lookup"><span data-stu-id="b7cf1-138">0x8009</span></span>                                                                                  |
| <span data-ttu-id="b7cf1-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="b7cf1-139">System-Only</span></span>            | <span data-ttu-id="b7cf1-140">Falso</span><span class="sxs-lookup"><span data-stu-id="b7cf1-140">False</span></span>                                                                                   |
| <span data-ttu-id="b7cf1-141">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="b7cf1-141">Is-Single-Valued</span></span>       | <span data-ttu-id="b7cf1-142">Falso</span><span class="sxs-lookup"><span data-stu-id="b7cf1-142">False</span></span>                                                                                   |
| <span data-ttu-id="b7cf1-143">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="b7cf1-143">Is Indexed</span></span>             | <span data-ttu-id="b7cf1-144">Falso</span><span class="sxs-lookup"><span data-stu-id="b7cf1-144">False</span></span>                                                                                   |
| <span data-ttu-id="b7cf1-145">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="b7cf1-145">In Global Catalog</span></span>      | <span data-ttu-id="b7cf1-146">Vero</span><span class="sxs-lookup"><span data-stu-id="b7cf1-146">True</span></span>                                                                                    |
| <span data-ttu-id="b7cf1-147">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="b7cf1-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="b7cf1-148">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="b7cf1-148">O:BAG:BAD:S:</span></span>                                                                            |
| <span data-ttu-id="b7cf1-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b7cf1-149">Range-Lower</span></span>            | \-                                                                                      |
| <span data-ttu-id="b7cf1-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b7cf1-150">Range-Upper</span></span>            | \-                                                                                      |
| <span data-ttu-id="b7cf1-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b7cf1-151">Search-Flags</span></span>           | <span data-ttu-id="b7cf1-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b7cf1-152">0x00000000</span></span>                                                                              |
| <span data-ttu-id="b7cf1-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b7cf1-153">System-Flags</span></span>           | <span data-ttu-id="b7cf1-154">0x00000012</span><span class="sxs-lookup"><span data-stu-id="b7cf1-154">0x00000012</span></span>                                                                              |
| <span data-ttu-id="b7cf1-155">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="b7cf1-155">Classes used in</span></span>        | [<span data-ttu-id="b7cf1-156">**Group**</span><span class="sxs-lookup"><span data-stu-id="b7cf1-156">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="b7cf1-157">**Gruppo di nomi**</span><span class="sxs-lookup"><span data-stu-id="b7cf1-157">**Group-Of-Names**</span></span>](c-groupofnames.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="b7cf1-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b7cf1-158">Windows Server 2003</span></span>



| <span data-ttu-id="b7cf1-159">Voce</span><span class="sxs-lookup"><span data-stu-id="b7cf1-159">Entry</span></span> | <span data-ttu-id="b7cf1-160">Valore</span><span class="sxs-lookup"><span data-stu-id="b7cf1-160">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7cf1-161">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="b7cf1-161">Link-Id</span></span>                | <span data-ttu-id="b7cf1-162">2</span><span class="sxs-lookup"><span data-stu-id="b7cf1-162">2</span></span>                                                                                                                                     |
| <span data-ttu-id="b7cf1-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b7cf1-163">MAPI-Id</span></span>                | <span data-ttu-id="b7cf1-164">0x8009</span><span class="sxs-lookup"><span data-stu-id="b7cf1-164">0x8009</span></span>                                                                                                                                |
| <span data-ttu-id="b7cf1-165">System-Only</span><span class="sxs-lookup"><span data-stu-id="b7cf1-165">System-Only</span></span>            | <span data-ttu-id="b7cf1-166">Falso</span><span class="sxs-lookup"><span data-stu-id="b7cf1-166">False</span></span>                                                                                                                                 |
| <span data-ttu-id="b7cf1-167">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="b7cf1-167">Is-Single-Valued</span></span>       | <span data-ttu-id="b7cf1-168">Falso</span><span class="sxs-lookup"><span data-stu-id="b7cf1-168">False</span></span>                                                                                                                                 |
| <span data-ttu-id="b7cf1-169">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="b7cf1-169">Is Indexed</span></span>             | <span data-ttu-id="b7cf1-170">Falso</span><span class="sxs-lookup"><span data-stu-id="b7cf1-170">False</span></span>                                                                                                                                 |
| <span data-ttu-id="b7cf1-171">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="b7cf1-171">In Global Catalog</span></span>      | <span data-ttu-id="b7cf1-172">Vero</span><span class="sxs-lookup"><span data-stu-id="b7cf1-172">True</span></span>                                                                                                                                  |
| <span data-ttu-id="b7cf1-173">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="b7cf1-173">NT-Security-Descriptor</span></span> | <span data-ttu-id="b7cf1-174">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="b7cf1-174">O:BAG:BAD:S:</span></span>                                                                                                                          |
| <span data-ttu-id="b7cf1-175">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b7cf1-175">Range-Lower</span></span>            | \-                                                                                                                                    |
| <span data-ttu-id="b7cf1-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b7cf1-176">Range-Upper</span></span>            | \-                                                                                                                                    |
| <span data-ttu-id="b7cf1-177">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b7cf1-177">Search-Flags</span></span>           | <span data-ttu-id="b7cf1-178">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b7cf1-178">0x00000000</span></span>                                                                                                                            |
| <span data-ttu-id="b7cf1-179">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b7cf1-179">System-Flags</span></span>           | <span data-ttu-id="b7cf1-180">0x00000012</span><span class="sxs-lookup"><span data-stu-id="b7cf1-180">0x00000012</span></span>                                                                                                                            |
| <span data-ttu-id="b7cf1-181">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="b7cf1-181">Classes used in</span></span>        | [<span data-ttu-id="b7cf1-182">**Group**</span><span class="sxs-lookup"><span data-stu-id="b7cf1-182">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="b7cf1-183">**Gruppo di nomi**</span><span class="sxs-lookup"><span data-stu-id="b7cf1-183">**Group-Of-Names**</span></span>](c-groupofnames.md)<br/> [<span data-ttu-id="b7cf1-184">**Gruppo MSMQ**</span><span class="sxs-lookup"><span data-stu-id="b7cf1-184">**MSMQ-Group**</span></span>](c-msmq-group.md)<br/> |



## <a name="adam"></a><span data-ttu-id="b7cf1-185">ADAM</span><span class="sxs-lookup"><span data-stu-id="b7cf1-185">ADAM</span></span>



| <span data-ttu-id="b7cf1-186">Voce</span><span class="sxs-lookup"><span data-stu-id="b7cf1-186">Entry</span></span> | <span data-ttu-id="b7cf1-187">Valore</span><span class="sxs-lookup"><span data-stu-id="b7cf1-187">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="b7cf1-188">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="b7cf1-188">Link-Id</span></span>                | <span data-ttu-id="b7cf1-189">2</span><span class="sxs-lookup"><span data-stu-id="b7cf1-189">2</span></span>                                   |
| <span data-ttu-id="b7cf1-190">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b7cf1-190">MAPI-Id</span></span>                | <span data-ttu-id="b7cf1-191">0x8009</span><span class="sxs-lookup"><span data-stu-id="b7cf1-191">0x8009</span></span>                              |
| <span data-ttu-id="b7cf1-192">System-Only</span><span class="sxs-lookup"><span data-stu-id="b7cf1-192">System-Only</span></span>            | <span data-ttu-id="b7cf1-193">Falso</span><span class="sxs-lookup"><span data-stu-id="b7cf1-193">False</span></span>                               |
| <span data-ttu-id="b7cf1-194">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="b7cf1-194">Is-Single-Valued</span></span>       | <span data-ttu-id="b7cf1-195">Falso</span><span class="sxs-lookup"><span data-stu-id="b7cf1-195">False</span></span>                               |
| <span data-ttu-id="b7cf1-196">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="b7cf1-196">Is Indexed</span></span>             | <span data-ttu-id="b7cf1-197">Falso</span><span class="sxs-lookup"><span data-stu-id="b7cf1-197">False</span></span>                               |
| <span data-ttu-id="b7cf1-198">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="b7cf1-198">In Global Catalog</span></span>      | <span data-ttu-id="b7cf1-199">Vero</span><span class="sxs-lookup"><span data-stu-id="b7cf1-199">True</span></span>                                |
| <span data-ttu-id="b7cf1-200">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="b7cf1-200">NT-Security-Descriptor</span></span> | <span data-ttu-id="b7cf1-201">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="b7cf1-201">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="b7cf1-202">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b7cf1-202">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="b7cf1-203">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b7cf1-203">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="b7cf1-204">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b7cf1-204">Search-Flags</span></span>           | <span data-ttu-id="b7cf1-205">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b7cf1-205">0x00000000</span></span>                          |
| <span data-ttu-id="b7cf1-206">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b7cf1-206">System-Flags</span></span>           | <span data-ttu-id="b7cf1-207">0x00000012</span><span class="sxs-lookup"><span data-stu-id="b7cf1-207">0x00000012</span></span>                          |
| <span data-ttu-id="b7cf1-208">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="b7cf1-208">Classes used in</span></span>        | [<span data-ttu-id="b7cf1-209">**Group**</span><span class="sxs-lookup"><span data-stu-id="b7cf1-209">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b7cf1-210">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b7cf1-210">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b7cf1-211">Voce</span><span class="sxs-lookup"><span data-stu-id="b7cf1-211">Entry</span></span> | <span data-ttu-id="b7cf1-212">Valore</span><span class="sxs-lookup"><span data-stu-id="b7cf1-212">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7cf1-213">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="b7cf1-213">Link-Id</span></span>                | <span data-ttu-id="b7cf1-214">2</span><span class="sxs-lookup"><span data-stu-id="b7cf1-214">2</span></span>                                                                                                                                     |
| <span data-ttu-id="b7cf1-215">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b7cf1-215">MAPI-Id</span></span>                | <span data-ttu-id="b7cf1-216">0x8009</span><span class="sxs-lookup"><span data-stu-id="b7cf1-216">0x8009</span></span>                                                                                                                                |
| <span data-ttu-id="b7cf1-217">System-Only</span><span class="sxs-lookup"><span data-stu-id="b7cf1-217">System-Only</span></span>            | <span data-ttu-id="b7cf1-218">Falso</span><span class="sxs-lookup"><span data-stu-id="b7cf1-218">False</span></span>                                                                                                                                 |
| <span data-ttu-id="b7cf1-219">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="b7cf1-219">Is-Single-Valued</span></span>       | <span data-ttu-id="b7cf1-220">Falso</span><span class="sxs-lookup"><span data-stu-id="b7cf1-220">False</span></span>                                                                                                                                 |
| <span data-ttu-id="b7cf1-221">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="b7cf1-221">Is Indexed</span></span>             | <span data-ttu-id="b7cf1-222">Falso</span><span class="sxs-lookup"><span data-stu-id="b7cf1-222">False</span></span>                                                                                                                                 |
| <span data-ttu-id="b7cf1-223">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="b7cf1-223">In Global Catalog</span></span>      | <span data-ttu-id="b7cf1-224">Vero</span><span class="sxs-lookup"><span data-stu-id="b7cf1-224">True</span></span>                                                                                                                                  |
| <span data-ttu-id="b7cf1-225">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="b7cf1-225">NT-Security-Descriptor</span></span> | <span data-ttu-id="b7cf1-226">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="b7cf1-226">O:BAG:BAD:S:</span></span>                                                                                                                          |
| <span data-ttu-id="b7cf1-227">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b7cf1-227">Range-Lower</span></span>            | \-                                                                                                                                    |
| <span data-ttu-id="b7cf1-228">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b7cf1-228">Range-Upper</span></span>            | \-                                                                                                                                    |
| <span data-ttu-id="b7cf1-229">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b7cf1-229">Search-Flags</span></span>           | <span data-ttu-id="b7cf1-230">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b7cf1-230">0x00000000</span></span>                                                                                                                            |
| <span data-ttu-id="b7cf1-231">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b7cf1-231">System-Flags</span></span>           | <span data-ttu-id="b7cf1-232">0x00000012</span><span class="sxs-lookup"><span data-stu-id="b7cf1-232">0x00000012</span></span>                                                                                                                            |
| <span data-ttu-id="b7cf1-233">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="b7cf1-233">Classes used in</span></span>        | [<span data-ttu-id="b7cf1-234">**Group**</span><span class="sxs-lookup"><span data-stu-id="b7cf1-234">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="b7cf1-235">**Gruppo di nomi**</span><span class="sxs-lookup"><span data-stu-id="b7cf1-235">**Group-Of-Names**</span></span>](c-groupofnames.md)<br/> [<span data-ttu-id="b7cf1-236">**Gruppo MSMQ**</span><span class="sxs-lookup"><span data-stu-id="b7cf1-236">**MSMQ-Group**</span></span>](c-msmq-group.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b7cf1-237">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b7cf1-237">Windows Server 2008</span></span>



| <span data-ttu-id="b7cf1-238">Voce</span><span class="sxs-lookup"><span data-stu-id="b7cf1-238">Entry</span></span> | <span data-ttu-id="b7cf1-239">Valore</span><span class="sxs-lookup"><span data-stu-id="b7cf1-239">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7cf1-240">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="b7cf1-240">Link-Id</span></span>                | <span data-ttu-id="b7cf1-241">2</span><span class="sxs-lookup"><span data-stu-id="b7cf1-241">2</span></span>                                                                                                                                     |
| <span data-ttu-id="b7cf1-242">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b7cf1-242">MAPI-Id</span></span>                | <span data-ttu-id="b7cf1-243">0x8009</span><span class="sxs-lookup"><span data-stu-id="b7cf1-243">0x8009</span></span>                                                                                                                                |
| <span data-ttu-id="b7cf1-244">System-Only</span><span class="sxs-lookup"><span data-stu-id="b7cf1-244">System-Only</span></span>            | <span data-ttu-id="b7cf1-245">Falso</span><span class="sxs-lookup"><span data-stu-id="b7cf1-245">False</span></span>                                                                                                                                 |
| <span data-ttu-id="b7cf1-246">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="b7cf1-246">Is-Single-Valued</span></span>       | <span data-ttu-id="b7cf1-247">Falso</span><span class="sxs-lookup"><span data-stu-id="b7cf1-247">False</span></span>                                                                                                                                 |
| <span data-ttu-id="b7cf1-248">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="b7cf1-248">Is Indexed</span></span>             | <span data-ttu-id="b7cf1-249">Falso</span><span class="sxs-lookup"><span data-stu-id="b7cf1-249">False</span></span>                                                                                                                                 |
| <span data-ttu-id="b7cf1-250">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="b7cf1-250">In Global Catalog</span></span>      | <span data-ttu-id="b7cf1-251">Vero</span><span class="sxs-lookup"><span data-stu-id="b7cf1-251">True</span></span>                                                                                                                                  |
| <span data-ttu-id="b7cf1-252">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="b7cf1-252">NT-Security-Descriptor</span></span> | <span data-ttu-id="b7cf1-253">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="b7cf1-253">O:BAG:BAD:S:</span></span>                                                                                                                          |
| <span data-ttu-id="b7cf1-254">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b7cf1-254">Range-Lower</span></span>            | \-                                                                                                                                    |
| <span data-ttu-id="b7cf1-255">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b7cf1-255">Range-Upper</span></span>            | \-                                                                                                                                    |
| <span data-ttu-id="b7cf1-256">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b7cf1-256">Search-Flags</span></span>           | <span data-ttu-id="b7cf1-257">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b7cf1-257">0x00000000</span></span>                                                                                                                            |
| <span data-ttu-id="b7cf1-258">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b7cf1-258">System-Flags</span></span>           | <span data-ttu-id="b7cf1-259">0x00000012</span><span class="sxs-lookup"><span data-stu-id="b7cf1-259">0x00000012</span></span>                                                                                                                            |
| <span data-ttu-id="b7cf1-260">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="b7cf1-260">Classes used in</span></span>        | [<span data-ttu-id="b7cf1-261">**Group**</span><span class="sxs-lookup"><span data-stu-id="b7cf1-261">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="b7cf1-262">**Gruppo di nomi**</span><span class="sxs-lookup"><span data-stu-id="b7cf1-262">**Group-Of-Names**</span></span>](c-groupofnames.md)<br/> [<span data-ttu-id="b7cf1-263">**Gruppo MSMQ**</span><span class="sxs-lookup"><span data-stu-id="b7cf1-263">**MSMQ-Group**</span></span>](c-msmq-group.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b7cf1-264">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b7cf1-264">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b7cf1-265">Voce</span><span class="sxs-lookup"><span data-stu-id="b7cf1-265">Entry</span></span> | <span data-ttu-id="b7cf1-266">Valore</span><span class="sxs-lookup"><span data-stu-id="b7cf1-266">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7cf1-267">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="b7cf1-267">Link-Id</span></span>                | <span data-ttu-id="b7cf1-268">2</span><span class="sxs-lookup"><span data-stu-id="b7cf1-268">2</span></span>                                                                                                                                     |
| <span data-ttu-id="b7cf1-269">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b7cf1-269">MAPI-Id</span></span>                | <span data-ttu-id="b7cf1-270">0x8009</span><span class="sxs-lookup"><span data-stu-id="b7cf1-270">0x8009</span></span>                                                                                                                                |
| <span data-ttu-id="b7cf1-271">System-Only</span><span class="sxs-lookup"><span data-stu-id="b7cf1-271">System-Only</span></span>            | <span data-ttu-id="b7cf1-272">Falso</span><span class="sxs-lookup"><span data-stu-id="b7cf1-272">False</span></span>                                                                                                                                 |
| <span data-ttu-id="b7cf1-273">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="b7cf1-273">Is-Single-Valued</span></span>       | <span data-ttu-id="b7cf1-274">Falso</span><span class="sxs-lookup"><span data-stu-id="b7cf1-274">False</span></span>                                                                                                                                 |
| <span data-ttu-id="b7cf1-275">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="b7cf1-275">Is Indexed</span></span>             | <span data-ttu-id="b7cf1-276">Falso</span><span class="sxs-lookup"><span data-stu-id="b7cf1-276">False</span></span>                                                                                                                                 |
| <span data-ttu-id="b7cf1-277">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="b7cf1-277">In Global Catalog</span></span>      | <span data-ttu-id="b7cf1-278">Vero</span><span class="sxs-lookup"><span data-stu-id="b7cf1-278">True</span></span>                                                                                                                                  |
| <span data-ttu-id="b7cf1-279">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="b7cf1-279">NT-Security-Descriptor</span></span> | <span data-ttu-id="b7cf1-280">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="b7cf1-280">O:BAG:BAD:S:</span></span>                                                                                                                          |
| <span data-ttu-id="b7cf1-281">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b7cf1-281">Range-Lower</span></span>            | \-                                                                                                                                    |
| <span data-ttu-id="b7cf1-282">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b7cf1-282">Range-Upper</span></span>            | \-                                                                                                                                    |
| <span data-ttu-id="b7cf1-283">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b7cf1-283">Search-Flags</span></span>           | <span data-ttu-id="b7cf1-284">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b7cf1-284">0x00000000</span></span>                                                                                                                            |
| <span data-ttu-id="b7cf1-285">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b7cf1-285">System-Flags</span></span>           | <span data-ttu-id="b7cf1-286">0x00000012</span><span class="sxs-lookup"><span data-stu-id="b7cf1-286">0x00000012</span></span>                                                                                                                            |
| <span data-ttu-id="b7cf1-287">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="b7cf1-287">Classes used in</span></span>        | [<span data-ttu-id="b7cf1-288">**Group**</span><span class="sxs-lookup"><span data-stu-id="b7cf1-288">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="b7cf1-289">**Gruppo di nomi**</span><span class="sxs-lookup"><span data-stu-id="b7cf1-289">**Group-Of-Names**</span></span>](c-groupofnames.md)<br/> [<span data-ttu-id="b7cf1-290">**Gruppo MSMQ**</span><span class="sxs-lookup"><span data-stu-id="b7cf1-290">**MSMQ-Group**</span></span>](c-msmq-group.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b7cf1-291">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b7cf1-291">Windows Server 2012</span></span>



| <span data-ttu-id="b7cf1-292">Voce</span><span class="sxs-lookup"><span data-stu-id="b7cf1-292">Entry</span></span> | <span data-ttu-id="b7cf1-293">Valore</span><span class="sxs-lookup"><span data-stu-id="b7cf1-293">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7cf1-294">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="b7cf1-294">Link-Id</span></span>                | <span data-ttu-id="b7cf1-295">2</span><span class="sxs-lookup"><span data-stu-id="b7cf1-295">2</span></span>                                                                                                                                     |
| <span data-ttu-id="b7cf1-296">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b7cf1-296">MAPI-Id</span></span>                | <span data-ttu-id="b7cf1-297">0x8009</span><span class="sxs-lookup"><span data-stu-id="b7cf1-297">0x8009</span></span>                                                                                                                                |
| <span data-ttu-id="b7cf1-298">System-Only</span><span class="sxs-lookup"><span data-stu-id="b7cf1-298">System-Only</span></span>            | <span data-ttu-id="b7cf1-299">Falso</span><span class="sxs-lookup"><span data-stu-id="b7cf1-299">False</span></span>                                                                                                                                 |
| <span data-ttu-id="b7cf1-300">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="b7cf1-300">Is-Single-Valued</span></span>       | <span data-ttu-id="b7cf1-301">Falso</span><span class="sxs-lookup"><span data-stu-id="b7cf1-301">False</span></span>                                                                                                                                 |
| <span data-ttu-id="b7cf1-302">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="b7cf1-302">Is Indexed</span></span>             | <span data-ttu-id="b7cf1-303">Falso</span><span class="sxs-lookup"><span data-stu-id="b7cf1-303">False</span></span>                                                                                                                                 |
| <span data-ttu-id="b7cf1-304">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="b7cf1-304">In Global Catalog</span></span>      | <span data-ttu-id="b7cf1-305">Vero</span><span class="sxs-lookup"><span data-stu-id="b7cf1-305">True</span></span>                                                                                                                                  |
| <span data-ttu-id="b7cf1-306">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="b7cf1-306">NT-Security-Descriptor</span></span> | <span data-ttu-id="b7cf1-307">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="b7cf1-307">O:BAG:BAD:S:</span></span>                                                                                                                          |
| <span data-ttu-id="b7cf1-308">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b7cf1-308">Range-Lower</span></span>            | \-                                                                                                                                    |
| <span data-ttu-id="b7cf1-309">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b7cf1-309">Range-Upper</span></span>            | \-                                                                                                                                    |
| <span data-ttu-id="b7cf1-310">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b7cf1-310">Search-Flags</span></span>           | <span data-ttu-id="b7cf1-311">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b7cf1-311">0x00000000</span></span>                                                                                                                            |
| <span data-ttu-id="b7cf1-312">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b7cf1-312">System-Flags</span></span>           | <span data-ttu-id="b7cf1-313">0x00000012</span><span class="sxs-lookup"><span data-stu-id="b7cf1-313">0x00000012</span></span>                                                                                                                            |
| <span data-ttu-id="b7cf1-314">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="b7cf1-314">Classes used in</span></span>        | [<span data-ttu-id="b7cf1-315">**Group**</span><span class="sxs-lookup"><span data-stu-id="b7cf1-315">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="b7cf1-316">**Gruppo di nomi**</span><span class="sxs-lookup"><span data-stu-id="b7cf1-316">**Group-Of-Names**</span></span>](c-groupofnames.md)<br/> [<span data-ttu-id="b7cf1-317">**Gruppo MSMQ**</span><span class="sxs-lookup"><span data-stu-id="b7cf1-317">**MSMQ-Group**</span></span>](c-msmq-group.md)<br/> |



 

 





