---
title: Attributo MS-DS-All-Users-Trust-quota
description: Consente di applicare una quota di utenti combinati per il numero totale di oggetti Trusted-Domain creati usando il nuovo diritto di accesso di controllo, create-inbound-Forest-Trust.
ms.assetid: 77e70a26-99b4-4b49-a984-6809d02f6fb8
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo MS-DS-All-Users-Trust-quota
- attributo msDS-AllUsersTrustQuota-schema AD
topic_type:
- apiref
api_name:
- MS-DS-All-Users-Trust-Quota
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0538ff38f1eb57f339a8e0e244a378a36dd92498
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103745186"
---
# <a name="ms-ds-all-users-trust-quota-attribute"></a><span data-ttu-id="d6edd-105">Attributo MS-DS-All-Users-Trust-quota</span><span class="sxs-lookup"><span data-stu-id="d6edd-105">MS-DS-All-Users-Trust-Quota attribute</span></span>

<span data-ttu-id="d6edd-106">Consente di applicare una quota di utenti combinati per il numero totale di oggetti Trusted-Domain creati usando il nuovo diritto di accesso di controllo, create-inbound-Forest-Trust.</span><span class="sxs-lookup"><span data-stu-id="d6edd-106">Used to enforce a combined users quota on the total number of Trusted-Domain objects created by using the new control access right, Create-Inbound-Forest-Trust.</span></span>



| <span data-ttu-id="d6edd-107">Voce</span><span class="sxs-lookup"><span data-stu-id="d6edd-107">Entry</span></span> | <span data-ttu-id="d6edd-108">Valore</span><span class="sxs-lookup"><span data-stu-id="d6edd-108">Value</span></span> |
|-------------------|-------------------------------------------|
| <span data-ttu-id="d6edd-109">CN</span><span class="sxs-lookup"><span data-stu-id="d6edd-109">CN</span></span>                | <span data-ttu-id="d6edd-110">MS-DS-All-Users-Trust-quota</span><span class="sxs-lookup"><span data-stu-id="d6edd-110">MS-DS-All-Users-Trust-Quota</span></span>               |
| <span data-ttu-id="d6edd-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="d6edd-111">Ldap-Display-Name</span></span> | <span data-ttu-id="d6edd-112">msDS-AllUsersTrustQuota</span><span class="sxs-lookup"><span data-stu-id="d6edd-112">msDS-AllUsersTrustQuota</span></span>                   |
| <span data-ttu-id="d6edd-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="d6edd-113">Size</span></span>              | \-                                        |
| <span data-ttu-id="d6edd-114">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="d6edd-114">Update Privilege</span></span>  | <span data-ttu-id="d6edd-115">Amministratore di dominio</span><span class="sxs-lookup"><span data-stu-id="d6edd-115">Domain administrator</span></span>                      |
| <span data-ttu-id="d6edd-116">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="d6edd-116">Update Frequency</span></span>  | <span data-ttu-id="d6edd-117">Alla creazione della foresta e, successivamente, raramente.</span><span class="sxs-lookup"><span data-stu-id="d6edd-117">At forest creation and rarely after that.</span></span> |
| <span data-ttu-id="d6edd-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="d6edd-118">Attribute-Id</span></span>      | <span data-ttu-id="d6edd-119">1.2.840.113556.1.4.1789</span><span class="sxs-lookup"><span data-stu-id="d6edd-119">1.2.840.113556.1.4.1789</span></span>                   |
| <span data-ttu-id="d6edd-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="d6edd-120">System-Id-Guid</span></span>    | <span data-ttu-id="d6edd-121">d3aa4a5c-4e03-4810-97aa-2b339e7a434b</span><span class="sxs-lookup"><span data-stu-id="d6edd-121">d3aa4a5c-4e03-4810-97aa-2b339e7a434b</span></span>      |
| <span data-ttu-id="d6edd-122">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d6edd-122">Syntax</span></span>            | [<span data-ttu-id="d6edd-123">**Enumerazione**</span><span class="sxs-lookup"><span data-stu-id="d6edd-123">**Enumeration**</span></span>](s-enumeration.md)      |



## <a name="implementations"></a><span data-ttu-id="d6edd-124">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="d6edd-124">Implementations</span></span>

-   [<span data-ttu-id="d6edd-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="d6edd-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="d6edd-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="d6edd-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="d6edd-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="d6edd-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="d6edd-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="d6edd-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="d6edd-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="d6edd-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="d6edd-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d6edd-130">Windows Server 2003</span></span>



| <span data-ttu-id="d6edd-131">Voce</span><span class="sxs-lookup"><span data-stu-id="d6edd-131">Entry</span></span> | <span data-ttu-id="d6edd-132">Valore</span><span class="sxs-lookup"><span data-stu-id="d6edd-132">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="d6edd-133">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="d6edd-133">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="d6edd-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d6edd-134">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="d6edd-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="d6edd-135">System-Only</span></span>            | <span data-ttu-id="d6edd-136">Falso</span><span class="sxs-lookup"><span data-stu-id="d6edd-136">False</span></span>                                        |
| <span data-ttu-id="d6edd-137">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="d6edd-137">Is-Single-Valued</span></span>       | <span data-ttu-id="d6edd-138">Vero</span><span class="sxs-lookup"><span data-stu-id="d6edd-138">True</span></span>                                         |
| <span data-ttu-id="d6edd-139">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="d6edd-139">Is Indexed</span></span>             | <span data-ttu-id="d6edd-140">Falso</span><span class="sxs-lookup"><span data-stu-id="d6edd-140">False</span></span>                                        |
| <span data-ttu-id="d6edd-141">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="d6edd-141">In Global Catalog</span></span>      | <span data-ttu-id="d6edd-142">Falso</span><span class="sxs-lookup"><span data-stu-id="d6edd-142">False</span></span>                                        |
| <span data-ttu-id="d6edd-143">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="d6edd-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="d6edd-144">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="d6edd-144">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="d6edd-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d6edd-145">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="d6edd-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d6edd-146">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="d6edd-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d6edd-147">Search-Flags</span></span>           | <span data-ttu-id="d6edd-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d6edd-148">0x00000000</span></span>                                   |
| <span data-ttu-id="d6edd-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d6edd-149">System-Flags</span></span>           | <span data-ttu-id="d6edd-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d6edd-150">0x00000010</span></span>                                   |
| <span data-ttu-id="d6edd-151">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="d6edd-151">Classes used in</span></span>        | [<span data-ttu-id="d6edd-152">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="d6edd-152">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="d6edd-153">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="d6edd-153">Windows Server 2003 R2</span></span>



| <span data-ttu-id="d6edd-154">Voce</span><span class="sxs-lookup"><span data-stu-id="d6edd-154">Entry</span></span> | <span data-ttu-id="d6edd-155">Valore</span><span class="sxs-lookup"><span data-stu-id="d6edd-155">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="d6edd-156">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="d6edd-156">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="d6edd-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d6edd-157">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="d6edd-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="d6edd-158">System-Only</span></span>            | <span data-ttu-id="d6edd-159">Falso</span><span class="sxs-lookup"><span data-stu-id="d6edd-159">False</span></span>                                        |
| <span data-ttu-id="d6edd-160">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="d6edd-160">Is-Single-Valued</span></span>       | <span data-ttu-id="d6edd-161">Vero</span><span class="sxs-lookup"><span data-stu-id="d6edd-161">True</span></span>                                         |
| <span data-ttu-id="d6edd-162">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="d6edd-162">Is Indexed</span></span>             | <span data-ttu-id="d6edd-163">Falso</span><span class="sxs-lookup"><span data-stu-id="d6edd-163">False</span></span>                                        |
| <span data-ttu-id="d6edd-164">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="d6edd-164">In Global Catalog</span></span>      | <span data-ttu-id="d6edd-165">Falso</span><span class="sxs-lookup"><span data-stu-id="d6edd-165">False</span></span>                                        |
| <span data-ttu-id="d6edd-166">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="d6edd-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="d6edd-167">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="d6edd-167">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="d6edd-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d6edd-168">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="d6edd-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d6edd-169">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="d6edd-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d6edd-170">Search-Flags</span></span>           | <span data-ttu-id="d6edd-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d6edd-171">0x00000000</span></span>                                   |
| <span data-ttu-id="d6edd-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d6edd-172">System-Flags</span></span>           | <span data-ttu-id="d6edd-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d6edd-173">0x00000010</span></span>                                   |
| <span data-ttu-id="d6edd-174">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="d6edd-174">Classes used in</span></span>        | [<span data-ttu-id="d6edd-175">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="d6edd-175">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="d6edd-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d6edd-176">Windows Server 2008</span></span>



| <span data-ttu-id="d6edd-177">Voce</span><span class="sxs-lookup"><span data-stu-id="d6edd-177">Entry</span></span> | <span data-ttu-id="d6edd-178">Valore</span><span class="sxs-lookup"><span data-stu-id="d6edd-178">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="d6edd-179">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="d6edd-179">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="d6edd-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d6edd-180">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="d6edd-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="d6edd-181">System-Only</span></span>            | <span data-ttu-id="d6edd-182">Falso</span><span class="sxs-lookup"><span data-stu-id="d6edd-182">False</span></span>                                        |
| <span data-ttu-id="d6edd-183">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="d6edd-183">Is-Single-Valued</span></span>       | <span data-ttu-id="d6edd-184">Vero</span><span class="sxs-lookup"><span data-stu-id="d6edd-184">True</span></span>                                         |
| <span data-ttu-id="d6edd-185">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="d6edd-185">Is Indexed</span></span>             | <span data-ttu-id="d6edd-186">Falso</span><span class="sxs-lookup"><span data-stu-id="d6edd-186">False</span></span>                                        |
| <span data-ttu-id="d6edd-187">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="d6edd-187">In Global Catalog</span></span>      | <span data-ttu-id="d6edd-188">Falso</span><span class="sxs-lookup"><span data-stu-id="d6edd-188">False</span></span>                                        |
| <span data-ttu-id="d6edd-189">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="d6edd-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="d6edd-190">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="d6edd-190">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="d6edd-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d6edd-191">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="d6edd-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d6edd-192">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="d6edd-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d6edd-193">Search-Flags</span></span>           | <span data-ttu-id="d6edd-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d6edd-194">0x00000000</span></span>                                   |
| <span data-ttu-id="d6edd-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d6edd-195">System-Flags</span></span>           | <span data-ttu-id="d6edd-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d6edd-196">0x00000010</span></span>                                   |
| <span data-ttu-id="d6edd-197">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="d6edd-197">Classes used in</span></span>        | [<span data-ttu-id="d6edd-198">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="d6edd-198">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="d6edd-199">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d6edd-199">Windows Server 2008 R2</span></span>



| <span data-ttu-id="d6edd-200">Voce</span><span class="sxs-lookup"><span data-stu-id="d6edd-200">Entry</span></span> | <span data-ttu-id="d6edd-201">Valore</span><span class="sxs-lookup"><span data-stu-id="d6edd-201">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="d6edd-202">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="d6edd-202">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="d6edd-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d6edd-203">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="d6edd-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="d6edd-204">System-Only</span></span>            | <span data-ttu-id="d6edd-205">Falso</span><span class="sxs-lookup"><span data-stu-id="d6edd-205">False</span></span>                                        |
| <span data-ttu-id="d6edd-206">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="d6edd-206">Is-Single-Valued</span></span>       | <span data-ttu-id="d6edd-207">Vero</span><span class="sxs-lookup"><span data-stu-id="d6edd-207">True</span></span>                                         |
| <span data-ttu-id="d6edd-208">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="d6edd-208">Is Indexed</span></span>             | <span data-ttu-id="d6edd-209">Falso</span><span class="sxs-lookup"><span data-stu-id="d6edd-209">False</span></span>                                        |
| <span data-ttu-id="d6edd-210">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="d6edd-210">In Global Catalog</span></span>      | <span data-ttu-id="d6edd-211">Falso</span><span class="sxs-lookup"><span data-stu-id="d6edd-211">False</span></span>                                        |
| <span data-ttu-id="d6edd-212">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="d6edd-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="d6edd-213">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="d6edd-213">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="d6edd-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d6edd-214">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="d6edd-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d6edd-215">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="d6edd-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d6edd-216">Search-Flags</span></span>           | <span data-ttu-id="d6edd-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d6edd-217">0x00000000</span></span>                                   |
| <span data-ttu-id="d6edd-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d6edd-218">System-Flags</span></span>           | <span data-ttu-id="d6edd-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d6edd-219">0x00000010</span></span>                                   |
| <span data-ttu-id="d6edd-220">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="d6edd-220">Classes used in</span></span>        | [<span data-ttu-id="d6edd-221">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="d6edd-221">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="d6edd-222">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d6edd-222">Windows Server 2012</span></span>



| <span data-ttu-id="d6edd-223">Voce</span><span class="sxs-lookup"><span data-stu-id="d6edd-223">Entry</span></span> | <span data-ttu-id="d6edd-224">Valore</span><span class="sxs-lookup"><span data-stu-id="d6edd-224">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="d6edd-225">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="d6edd-225">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="d6edd-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d6edd-226">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="d6edd-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="d6edd-227">System-Only</span></span>            | <span data-ttu-id="d6edd-228">Falso</span><span class="sxs-lookup"><span data-stu-id="d6edd-228">False</span></span>                                        |
| <span data-ttu-id="d6edd-229">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="d6edd-229">Is-Single-Valued</span></span>       | <span data-ttu-id="d6edd-230">Vero</span><span class="sxs-lookup"><span data-stu-id="d6edd-230">True</span></span>                                         |
| <span data-ttu-id="d6edd-231">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="d6edd-231">Is Indexed</span></span>             | <span data-ttu-id="d6edd-232">Falso</span><span class="sxs-lookup"><span data-stu-id="d6edd-232">False</span></span>                                        |
| <span data-ttu-id="d6edd-233">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="d6edd-233">In Global Catalog</span></span>      | <span data-ttu-id="d6edd-234">Falso</span><span class="sxs-lookup"><span data-stu-id="d6edd-234">False</span></span>                                        |
| <span data-ttu-id="d6edd-235">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="d6edd-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="d6edd-236">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="d6edd-236">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="d6edd-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d6edd-237">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="d6edd-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d6edd-238">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="d6edd-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d6edd-239">Search-Flags</span></span>           | <span data-ttu-id="d6edd-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d6edd-240">0x00000000</span></span>                                   |
| <span data-ttu-id="d6edd-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d6edd-241">System-Flags</span></span>           | <span data-ttu-id="d6edd-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d6edd-242">0x00000010</span></span>                                   |
| <span data-ttu-id="d6edd-243">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="d6edd-243">Classes used in</span></span>        | [<span data-ttu-id="d6edd-244">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="d6edd-244">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



 

 





