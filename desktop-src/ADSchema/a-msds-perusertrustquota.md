---
title: Attributo MS-DS-per-User-Trust-quota
description: Consente di applicare una quota per utente per la creazione di oggetti Trusted-Domain autorizzati dal nuovo diritto di accesso al controllo, create-inbound-Forest-Trust.
ms.assetid: 3b198b24-5282-4d13-8d35-88f34c11ce94
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo MS-DS-per-User-Trust-quota
- attributo msDS-PerUserTrustQuota-schema AD
topic_type:
- apiref
api_name:
- MS-DS-Per-User-Trust-Quota
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3bd6ffcac01de8997f806e6aa8a8e3bd6afbb66
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "106303508"
---
# <a name="ms-ds-per-user-trust-quota-attribute"></a><span data-ttu-id="d2c84-105">Attributo MS-DS-per-User-Trust-quota</span><span class="sxs-lookup"><span data-stu-id="d2c84-105">MS-DS-Per-User-Trust-Quota attribute</span></span>

<span data-ttu-id="d2c84-106">Consente di applicare una quota per utente per la creazione di oggetti Trusted-Domain autorizzati dal nuovo diritto di accesso al controllo, create-inbound-Forest-Trust.</span><span class="sxs-lookup"><span data-stu-id="d2c84-106">Used to enforce a per-user quota for creating Trusted-Domain objects that are authorized by the new control access right, Create-Inbound-Forest-Trust.</span></span> <span data-ttu-id="d2c84-107">Questo attributo limita il numero di oggetti Trusted-Domain che possono essere creati da un singolo utente non amministratore.</span><span class="sxs-lookup"><span data-stu-id="d2c84-107">This attribute limits the number of Trusted-Domain objects that can be created by a single non-admin user.</span></span>



| <span data-ttu-id="d2c84-108">Voce</span><span class="sxs-lookup"><span data-stu-id="d2c84-108">Entry</span></span> | <span data-ttu-id="d2c84-109">Valore</span><span class="sxs-lookup"><span data-stu-id="d2c84-109">Value</span></span> |
|-------------------|-------------------------------------------|
| <span data-ttu-id="d2c84-110">CN</span><span class="sxs-lookup"><span data-stu-id="d2c84-110">CN</span></span>                | <span data-ttu-id="d2c84-111">MS-DS-per utente-attendibilità-quota</span><span class="sxs-lookup"><span data-stu-id="d2c84-111">MS-DS-Per-User-Trust-Quota</span></span>                |
| <span data-ttu-id="d2c84-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="d2c84-112">Ldap-Display-Name</span></span> | <span data-ttu-id="d2c84-113">msDS-PerUserTrustQuota</span><span class="sxs-lookup"><span data-stu-id="d2c84-113">msDS-PerUserTrustQuota</span></span>                    |
| <span data-ttu-id="d2c84-114">Dimensione</span><span class="sxs-lookup"><span data-stu-id="d2c84-114">Size</span></span>              | \-                                        |
| <span data-ttu-id="d2c84-115">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="d2c84-115">Update Privilege</span></span>  | <span data-ttu-id="d2c84-116">Amministratore di dominio</span><span class="sxs-lookup"><span data-stu-id="d2c84-116">Domain administrator</span></span>                      |
| <span data-ttu-id="d2c84-117">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="d2c84-117">Update Frequency</span></span>  | <span data-ttu-id="d2c84-118">Alla creazione della foresta e, successivamente, raramente.</span><span class="sxs-lookup"><span data-stu-id="d2c84-118">At forest creation and rarely after that.</span></span> |
| <span data-ttu-id="d2c84-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="d2c84-119">Attribute-Id</span></span>      | <span data-ttu-id="d2c84-120">1.2.840.113556.1.4.1788</span><span class="sxs-lookup"><span data-stu-id="d2c84-120">1.2.840.113556.1.4.1788</span></span>                   |
| <span data-ttu-id="d2c84-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="d2c84-121">System-Id-Guid</span></span>    | <span data-ttu-id="d2c84-122">d161adf0-ca24-4993-a3aa-8b2c981302e8</span><span class="sxs-lookup"><span data-stu-id="d2c84-122">d161adf0-ca24-4993-a3aa-8b2c981302e8</span></span>      |
| <span data-ttu-id="d2c84-123">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d2c84-123">Syntax</span></span>            | [<span data-ttu-id="d2c84-124">**Enumerazione**</span><span class="sxs-lookup"><span data-stu-id="d2c84-124">**Enumeration**</span></span>](s-enumeration.md)      |



## <a name="implementations"></a><span data-ttu-id="d2c84-125">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="d2c84-125">Implementations</span></span>

-   [<span data-ttu-id="d2c84-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="d2c84-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="d2c84-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="d2c84-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="d2c84-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="d2c84-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="d2c84-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="d2c84-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="d2c84-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="d2c84-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="d2c84-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d2c84-131">Windows Server 2003</span></span>



| <span data-ttu-id="d2c84-132">Voce</span><span class="sxs-lookup"><span data-stu-id="d2c84-132">Entry</span></span> | <span data-ttu-id="d2c84-133">Valore</span><span class="sxs-lookup"><span data-stu-id="d2c84-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="d2c84-134">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="d2c84-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="d2c84-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d2c84-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="d2c84-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="d2c84-136">System-Only</span></span>            | <span data-ttu-id="d2c84-137">Falso</span><span class="sxs-lookup"><span data-stu-id="d2c84-137">False</span></span>                                        |
| <span data-ttu-id="d2c84-138">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="d2c84-138">Is-Single-Valued</span></span>       | <span data-ttu-id="d2c84-139">Vero</span><span class="sxs-lookup"><span data-stu-id="d2c84-139">True</span></span>                                         |
| <span data-ttu-id="d2c84-140">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="d2c84-140">Is Indexed</span></span>             | <span data-ttu-id="d2c84-141">Falso</span><span class="sxs-lookup"><span data-stu-id="d2c84-141">False</span></span>                                        |
| <span data-ttu-id="d2c84-142">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="d2c84-142">In Global Catalog</span></span>      | <span data-ttu-id="d2c84-143">Falso</span><span class="sxs-lookup"><span data-stu-id="d2c84-143">False</span></span>                                        |
| <span data-ttu-id="d2c84-144">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="d2c84-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="d2c84-145">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="d2c84-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="d2c84-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d2c84-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="d2c84-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d2c84-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="d2c84-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d2c84-148">Search-Flags</span></span>           | <span data-ttu-id="d2c84-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d2c84-149">0x00000000</span></span>                                   |
| <span data-ttu-id="d2c84-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d2c84-150">System-Flags</span></span>           | <span data-ttu-id="d2c84-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d2c84-151">0x00000010</span></span>                                   |
| <span data-ttu-id="d2c84-152">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="d2c84-152">Classes used in</span></span>        | [<span data-ttu-id="d2c84-153">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="d2c84-153">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="d2c84-154">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="d2c84-154">Windows Server 2003 R2</span></span>



| <span data-ttu-id="d2c84-155">Voce</span><span class="sxs-lookup"><span data-stu-id="d2c84-155">Entry</span></span> | <span data-ttu-id="d2c84-156">Valore</span><span class="sxs-lookup"><span data-stu-id="d2c84-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="d2c84-157">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="d2c84-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="d2c84-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d2c84-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="d2c84-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="d2c84-159">System-Only</span></span>            | <span data-ttu-id="d2c84-160">Falso</span><span class="sxs-lookup"><span data-stu-id="d2c84-160">False</span></span>                                        |
| <span data-ttu-id="d2c84-161">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="d2c84-161">Is-Single-Valued</span></span>       | <span data-ttu-id="d2c84-162">Vero</span><span class="sxs-lookup"><span data-stu-id="d2c84-162">True</span></span>                                         |
| <span data-ttu-id="d2c84-163">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="d2c84-163">Is Indexed</span></span>             | <span data-ttu-id="d2c84-164">Falso</span><span class="sxs-lookup"><span data-stu-id="d2c84-164">False</span></span>                                        |
| <span data-ttu-id="d2c84-165">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="d2c84-165">In Global Catalog</span></span>      | <span data-ttu-id="d2c84-166">Falso</span><span class="sxs-lookup"><span data-stu-id="d2c84-166">False</span></span>                                        |
| <span data-ttu-id="d2c84-167">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="d2c84-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="d2c84-168">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="d2c84-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="d2c84-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d2c84-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="d2c84-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d2c84-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="d2c84-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d2c84-171">Search-Flags</span></span>           | <span data-ttu-id="d2c84-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d2c84-172">0x00000000</span></span>                                   |
| <span data-ttu-id="d2c84-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d2c84-173">System-Flags</span></span>           | <span data-ttu-id="d2c84-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d2c84-174">0x00000010</span></span>                                   |
| <span data-ttu-id="d2c84-175">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="d2c84-175">Classes used in</span></span>        | [<span data-ttu-id="d2c84-176">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="d2c84-176">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="d2c84-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d2c84-177">Windows Server 2008</span></span>



| <span data-ttu-id="d2c84-178">Voce</span><span class="sxs-lookup"><span data-stu-id="d2c84-178">Entry</span></span> | <span data-ttu-id="d2c84-179">Valore</span><span class="sxs-lookup"><span data-stu-id="d2c84-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="d2c84-180">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="d2c84-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="d2c84-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d2c84-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="d2c84-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="d2c84-182">System-Only</span></span>            | <span data-ttu-id="d2c84-183">Falso</span><span class="sxs-lookup"><span data-stu-id="d2c84-183">False</span></span>                                        |
| <span data-ttu-id="d2c84-184">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="d2c84-184">Is-Single-Valued</span></span>       | <span data-ttu-id="d2c84-185">Vero</span><span class="sxs-lookup"><span data-stu-id="d2c84-185">True</span></span>                                         |
| <span data-ttu-id="d2c84-186">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="d2c84-186">Is Indexed</span></span>             | <span data-ttu-id="d2c84-187">Falso</span><span class="sxs-lookup"><span data-stu-id="d2c84-187">False</span></span>                                        |
| <span data-ttu-id="d2c84-188">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="d2c84-188">In Global Catalog</span></span>      | <span data-ttu-id="d2c84-189">Falso</span><span class="sxs-lookup"><span data-stu-id="d2c84-189">False</span></span>                                        |
| <span data-ttu-id="d2c84-190">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="d2c84-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="d2c84-191">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="d2c84-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="d2c84-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d2c84-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="d2c84-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d2c84-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="d2c84-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d2c84-194">Search-Flags</span></span>           | <span data-ttu-id="d2c84-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d2c84-195">0x00000000</span></span>                                   |
| <span data-ttu-id="d2c84-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d2c84-196">System-Flags</span></span>           | <span data-ttu-id="d2c84-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d2c84-197">0x00000010</span></span>                                   |
| <span data-ttu-id="d2c84-198">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="d2c84-198">Classes used in</span></span>        | [<span data-ttu-id="d2c84-199">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="d2c84-199">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="d2c84-200">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d2c84-200">Windows Server 2008 R2</span></span>



| <span data-ttu-id="d2c84-201">Voce</span><span class="sxs-lookup"><span data-stu-id="d2c84-201">Entry</span></span> | <span data-ttu-id="d2c84-202">Valore</span><span class="sxs-lookup"><span data-stu-id="d2c84-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="d2c84-203">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="d2c84-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="d2c84-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d2c84-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="d2c84-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="d2c84-205">System-Only</span></span>            | <span data-ttu-id="d2c84-206">Falso</span><span class="sxs-lookup"><span data-stu-id="d2c84-206">False</span></span>                                        |
| <span data-ttu-id="d2c84-207">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="d2c84-207">Is-Single-Valued</span></span>       | <span data-ttu-id="d2c84-208">Vero</span><span class="sxs-lookup"><span data-stu-id="d2c84-208">True</span></span>                                         |
| <span data-ttu-id="d2c84-209">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="d2c84-209">Is Indexed</span></span>             | <span data-ttu-id="d2c84-210">Falso</span><span class="sxs-lookup"><span data-stu-id="d2c84-210">False</span></span>                                        |
| <span data-ttu-id="d2c84-211">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="d2c84-211">In Global Catalog</span></span>      | <span data-ttu-id="d2c84-212">Falso</span><span class="sxs-lookup"><span data-stu-id="d2c84-212">False</span></span>                                        |
| <span data-ttu-id="d2c84-213">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="d2c84-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="d2c84-214">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="d2c84-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="d2c84-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d2c84-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="d2c84-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d2c84-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="d2c84-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d2c84-217">Search-Flags</span></span>           | <span data-ttu-id="d2c84-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d2c84-218">0x00000000</span></span>                                   |
| <span data-ttu-id="d2c84-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d2c84-219">System-Flags</span></span>           | <span data-ttu-id="d2c84-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d2c84-220">0x00000010</span></span>                                   |
| <span data-ttu-id="d2c84-221">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="d2c84-221">Classes used in</span></span>        | [<span data-ttu-id="d2c84-222">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="d2c84-222">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="d2c84-223">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d2c84-223">Windows Server 2012</span></span>



| <span data-ttu-id="d2c84-224">Voce</span><span class="sxs-lookup"><span data-stu-id="d2c84-224">Entry</span></span> | <span data-ttu-id="d2c84-225">Valore</span><span class="sxs-lookup"><span data-stu-id="d2c84-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="d2c84-226">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="d2c84-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="d2c84-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d2c84-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="d2c84-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="d2c84-228">System-Only</span></span>            | <span data-ttu-id="d2c84-229">Falso</span><span class="sxs-lookup"><span data-stu-id="d2c84-229">False</span></span>                                        |
| <span data-ttu-id="d2c84-230">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="d2c84-230">Is-Single-Valued</span></span>       | <span data-ttu-id="d2c84-231">Vero</span><span class="sxs-lookup"><span data-stu-id="d2c84-231">True</span></span>                                         |
| <span data-ttu-id="d2c84-232">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="d2c84-232">Is Indexed</span></span>             | <span data-ttu-id="d2c84-233">Falso</span><span class="sxs-lookup"><span data-stu-id="d2c84-233">False</span></span>                                        |
| <span data-ttu-id="d2c84-234">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="d2c84-234">In Global Catalog</span></span>      | <span data-ttu-id="d2c84-235">Falso</span><span class="sxs-lookup"><span data-stu-id="d2c84-235">False</span></span>                                        |
| <span data-ttu-id="d2c84-236">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="d2c84-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="d2c84-237">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="d2c84-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="d2c84-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d2c84-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="d2c84-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d2c84-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="d2c84-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d2c84-240">Search-Flags</span></span>           | <span data-ttu-id="d2c84-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d2c84-241">0x00000000</span></span>                                   |
| <span data-ttu-id="d2c84-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d2c84-242">System-Flags</span></span>           | <span data-ttu-id="d2c84-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d2c84-243">0x00000010</span></span>                                   |
| <span data-ttu-id="d2c84-244">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="d2c84-244">Classes used in</span></span>        | [<span data-ttu-id="d2c84-245">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="d2c84-245">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



 

 





