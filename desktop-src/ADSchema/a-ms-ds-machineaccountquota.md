---
title: Attributo MS-DS-machine-account-quota
description: Il numero di account computer che possono essere creati da un utente in un dominio.
ms.assetid: bcfc6a9c-b891-48c2-9c42-8154345caf08
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo MS-DS-machine-account-quota
- Schema AD dell'attributo ms-DS-MachineAccountQuota
topic_type:
- apiref
api_name:
- MS-DS-Machine-Account-Quota
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b86de012aa876e5a0d52ac866048801872a365f1
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104122566"
---
# <a name="ms-ds-machine-account-quota-attribute"></a><span data-ttu-id="93ebe-105">Attributo MS-DS-machine-account-quota</span><span class="sxs-lookup"><span data-stu-id="93ebe-105">MS-DS-Machine-Account-Quota attribute</span></span>

<span data-ttu-id="93ebe-106">Il numero di account computer che possono essere creati da un utente in un dominio.</span><span class="sxs-lookup"><span data-stu-id="93ebe-106">The number of computer accounts that a user is allowed to create in a domain.</span></span>



| <span data-ttu-id="93ebe-107">Voce</span><span class="sxs-lookup"><span data-stu-id="93ebe-107">Entry</span></span> | <span data-ttu-id="93ebe-108">Valore</span><span class="sxs-lookup"><span data-stu-id="93ebe-108">Value</span></span> |
|-------------------|--------------------------------------------------|
| <span data-ttu-id="93ebe-109">CN</span><span class="sxs-lookup"><span data-stu-id="93ebe-109">CN</span></span>                | <span data-ttu-id="93ebe-110">MS-DS-machine-account-quota</span><span class="sxs-lookup"><span data-stu-id="93ebe-110">MS-DS-Machine-Account-Quota</span></span>                      |
| <span data-ttu-id="93ebe-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="93ebe-111">Ldap-Display-Name</span></span> | <span data-ttu-id="93ebe-112">ms-DS-MachineAccountQuota</span><span class="sxs-lookup"><span data-stu-id="93ebe-112">ms-DS-MachineAccountQuota</span></span>                        |
| <span data-ttu-id="93ebe-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="93ebe-113">Size</span></span>              | <span data-ttu-id="93ebe-114">4 byte</span><span class="sxs-lookup"><span data-stu-id="93ebe-114">4 bytes</span></span>                                          |
| <span data-ttu-id="93ebe-115">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="93ebe-115">Update Privilege</span></span>  | <span data-ttu-id="93ebe-116">Amministratore di dominio</span><span class="sxs-lookup"><span data-stu-id="93ebe-116">Domain administrator</span></span>                             |
| <span data-ttu-id="93ebe-117">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="93ebe-117">Update Frequency</span></span>  | <span data-ttu-id="93ebe-118">Ogni volta che è necessario modificare la quota di un dominio.</span><span class="sxs-lookup"><span data-stu-id="93ebe-118">Whenever the quota for a domain needs to change.</span></span> |
| <span data-ttu-id="93ebe-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="93ebe-119">Attribute-Id</span></span>      | <span data-ttu-id="93ebe-120">1.2.840.113556.1.4.1411</span><span class="sxs-lookup"><span data-stu-id="93ebe-120">1.2.840.113556.1.4.1411</span></span>                          |
| <span data-ttu-id="93ebe-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="93ebe-121">System-Id-Guid</span></span>    | <span data-ttu-id="93ebe-122">d064fb68-1480-11d3-91c1-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="93ebe-122">d064fb68-1480-11d3-91c1-0000f87a57d4</span></span>             |
| <span data-ttu-id="93ebe-123">Sintassi</span><span class="sxs-lookup"><span data-stu-id="93ebe-123">Syntax</span></span>            | [<span data-ttu-id="93ebe-124">**Enumerazione**</span><span class="sxs-lookup"><span data-stu-id="93ebe-124">**Enumeration**</span></span>](s-enumeration.md)             |



## <a name="implementations"></a><span data-ttu-id="93ebe-125">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="93ebe-125">Implementations</span></span>

-   [<span data-ttu-id="93ebe-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="93ebe-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="93ebe-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="93ebe-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="93ebe-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="93ebe-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="93ebe-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="93ebe-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="93ebe-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="93ebe-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="93ebe-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="93ebe-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="93ebe-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="93ebe-132">Windows 2000 Server</span></span>



| <span data-ttu-id="93ebe-133">Voce</span><span class="sxs-lookup"><span data-stu-id="93ebe-133">Entry</span></span> | <span data-ttu-id="93ebe-134">Valore</span><span class="sxs-lookup"><span data-stu-id="93ebe-134">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="93ebe-135">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="93ebe-135">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="93ebe-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="93ebe-136">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="93ebe-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="93ebe-137">System-Only</span></span>            | <span data-ttu-id="93ebe-138">Falso</span><span class="sxs-lookup"><span data-stu-id="93ebe-138">False</span></span>                                        |
| <span data-ttu-id="93ebe-139">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="93ebe-139">Is-Single-Valued</span></span>       | <span data-ttu-id="93ebe-140">Vero</span><span class="sxs-lookup"><span data-stu-id="93ebe-140">True</span></span>                                         |
| <span data-ttu-id="93ebe-141">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="93ebe-141">Is Indexed</span></span>             | <span data-ttu-id="93ebe-142">Falso</span><span class="sxs-lookup"><span data-stu-id="93ebe-142">False</span></span>                                        |
| <span data-ttu-id="93ebe-143">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="93ebe-143">In Global Catalog</span></span>      | <span data-ttu-id="93ebe-144">Falso</span><span class="sxs-lookup"><span data-stu-id="93ebe-144">False</span></span>                                        |
| <span data-ttu-id="93ebe-145">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="93ebe-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="93ebe-146">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="93ebe-146">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="93ebe-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="93ebe-147">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="93ebe-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="93ebe-148">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="93ebe-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="93ebe-149">Search-Flags</span></span>           | <span data-ttu-id="93ebe-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="93ebe-150">0x00000000</span></span>                                   |
| <span data-ttu-id="93ebe-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="93ebe-151">System-Flags</span></span>           | <span data-ttu-id="93ebe-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="93ebe-152">0x00000010</span></span>                                   |
| <span data-ttu-id="93ebe-153">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="93ebe-153">Classes used in</span></span>        | [<span data-ttu-id="93ebe-154">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="93ebe-154">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="93ebe-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="93ebe-155">Windows Server 2003</span></span>



| <span data-ttu-id="93ebe-156">Voce</span><span class="sxs-lookup"><span data-stu-id="93ebe-156">Entry</span></span> | <span data-ttu-id="93ebe-157">Valore</span><span class="sxs-lookup"><span data-stu-id="93ebe-157">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="93ebe-158">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="93ebe-158">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="93ebe-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="93ebe-159">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="93ebe-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="93ebe-160">System-Only</span></span>            | <span data-ttu-id="93ebe-161">Falso</span><span class="sxs-lookup"><span data-stu-id="93ebe-161">False</span></span>                                        |
| <span data-ttu-id="93ebe-162">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="93ebe-162">Is-Single-Valued</span></span>       | <span data-ttu-id="93ebe-163">Vero</span><span class="sxs-lookup"><span data-stu-id="93ebe-163">True</span></span>                                         |
| <span data-ttu-id="93ebe-164">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="93ebe-164">Is Indexed</span></span>             | <span data-ttu-id="93ebe-165">Falso</span><span class="sxs-lookup"><span data-stu-id="93ebe-165">False</span></span>                                        |
| <span data-ttu-id="93ebe-166">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="93ebe-166">In Global Catalog</span></span>      | <span data-ttu-id="93ebe-167">Falso</span><span class="sxs-lookup"><span data-stu-id="93ebe-167">False</span></span>                                        |
| <span data-ttu-id="93ebe-168">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="93ebe-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="93ebe-169">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="93ebe-169">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="93ebe-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="93ebe-170">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="93ebe-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="93ebe-171">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="93ebe-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="93ebe-172">Search-Flags</span></span>           | <span data-ttu-id="93ebe-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="93ebe-173">0x00000000</span></span>                                   |
| <span data-ttu-id="93ebe-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="93ebe-174">System-Flags</span></span>           | <span data-ttu-id="93ebe-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="93ebe-175">0x00000010</span></span>                                   |
| <span data-ttu-id="93ebe-176">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="93ebe-176">Classes used in</span></span>        | [<span data-ttu-id="93ebe-177">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="93ebe-177">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="93ebe-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="93ebe-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="93ebe-179">Voce</span><span class="sxs-lookup"><span data-stu-id="93ebe-179">Entry</span></span> | <span data-ttu-id="93ebe-180">Valore</span><span class="sxs-lookup"><span data-stu-id="93ebe-180">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="93ebe-181">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="93ebe-181">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="93ebe-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="93ebe-182">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="93ebe-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="93ebe-183">System-Only</span></span>            | <span data-ttu-id="93ebe-184">Falso</span><span class="sxs-lookup"><span data-stu-id="93ebe-184">False</span></span>                                        |
| <span data-ttu-id="93ebe-185">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="93ebe-185">Is-Single-Valued</span></span>       | <span data-ttu-id="93ebe-186">Vero</span><span class="sxs-lookup"><span data-stu-id="93ebe-186">True</span></span>                                         |
| <span data-ttu-id="93ebe-187">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="93ebe-187">Is Indexed</span></span>             | <span data-ttu-id="93ebe-188">Falso</span><span class="sxs-lookup"><span data-stu-id="93ebe-188">False</span></span>                                        |
| <span data-ttu-id="93ebe-189">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="93ebe-189">In Global Catalog</span></span>      | <span data-ttu-id="93ebe-190">Falso</span><span class="sxs-lookup"><span data-stu-id="93ebe-190">False</span></span>                                        |
| <span data-ttu-id="93ebe-191">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="93ebe-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="93ebe-192">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="93ebe-192">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="93ebe-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="93ebe-193">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="93ebe-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="93ebe-194">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="93ebe-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="93ebe-195">Search-Flags</span></span>           | <span data-ttu-id="93ebe-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="93ebe-196">0x00000000</span></span>                                   |
| <span data-ttu-id="93ebe-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="93ebe-197">System-Flags</span></span>           | <span data-ttu-id="93ebe-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="93ebe-198">0x00000010</span></span>                                   |
| <span data-ttu-id="93ebe-199">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="93ebe-199">Classes used in</span></span>        | [<span data-ttu-id="93ebe-200">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="93ebe-200">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="93ebe-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="93ebe-201">Windows Server 2008</span></span>



| <span data-ttu-id="93ebe-202">Voce</span><span class="sxs-lookup"><span data-stu-id="93ebe-202">Entry</span></span> | <span data-ttu-id="93ebe-203">Valore</span><span class="sxs-lookup"><span data-stu-id="93ebe-203">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="93ebe-204">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="93ebe-204">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="93ebe-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="93ebe-205">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="93ebe-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="93ebe-206">System-Only</span></span>            | <span data-ttu-id="93ebe-207">Falso</span><span class="sxs-lookup"><span data-stu-id="93ebe-207">False</span></span>                                        |
| <span data-ttu-id="93ebe-208">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="93ebe-208">Is-Single-Valued</span></span>       | <span data-ttu-id="93ebe-209">Vero</span><span class="sxs-lookup"><span data-stu-id="93ebe-209">True</span></span>                                         |
| <span data-ttu-id="93ebe-210">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="93ebe-210">Is Indexed</span></span>             | <span data-ttu-id="93ebe-211">Falso</span><span class="sxs-lookup"><span data-stu-id="93ebe-211">False</span></span>                                        |
| <span data-ttu-id="93ebe-212">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="93ebe-212">In Global Catalog</span></span>      | <span data-ttu-id="93ebe-213">Falso</span><span class="sxs-lookup"><span data-stu-id="93ebe-213">False</span></span>                                        |
| <span data-ttu-id="93ebe-214">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="93ebe-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="93ebe-215">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="93ebe-215">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="93ebe-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="93ebe-216">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="93ebe-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="93ebe-217">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="93ebe-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="93ebe-218">Search-Flags</span></span>           | <span data-ttu-id="93ebe-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="93ebe-219">0x00000000</span></span>                                   |
| <span data-ttu-id="93ebe-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="93ebe-220">System-Flags</span></span>           | <span data-ttu-id="93ebe-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="93ebe-221">0x00000010</span></span>                                   |
| <span data-ttu-id="93ebe-222">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="93ebe-222">Classes used in</span></span>        | [<span data-ttu-id="93ebe-223">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="93ebe-223">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="93ebe-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="93ebe-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="93ebe-225">Voce</span><span class="sxs-lookup"><span data-stu-id="93ebe-225">Entry</span></span> | <span data-ttu-id="93ebe-226">Valore</span><span class="sxs-lookup"><span data-stu-id="93ebe-226">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="93ebe-227">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="93ebe-227">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="93ebe-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="93ebe-228">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="93ebe-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="93ebe-229">System-Only</span></span>            | <span data-ttu-id="93ebe-230">Falso</span><span class="sxs-lookup"><span data-stu-id="93ebe-230">False</span></span>                                        |
| <span data-ttu-id="93ebe-231">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="93ebe-231">Is-Single-Valued</span></span>       | <span data-ttu-id="93ebe-232">Vero</span><span class="sxs-lookup"><span data-stu-id="93ebe-232">True</span></span>                                         |
| <span data-ttu-id="93ebe-233">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="93ebe-233">Is Indexed</span></span>             | <span data-ttu-id="93ebe-234">Falso</span><span class="sxs-lookup"><span data-stu-id="93ebe-234">False</span></span>                                        |
| <span data-ttu-id="93ebe-235">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="93ebe-235">In Global Catalog</span></span>      | <span data-ttu-id="93ebe-236">Falso</span><span class="sxs-lookup"><span data-stu-id="93ebe-236">False</span></span>                                        |
| <span data-ttu-id="93ebe-237">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="93ebe-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="93ebe-238">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="93ebe-238">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="93ebe-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="93ebe-239">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="93ebe-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="93ebe-240">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="93ebe-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="93ebe-241">Search-Flags</span></span>           | <span data-ttu-id="93ebe-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="93ebe-242">0x00000000</span></span>                                   |
| <span data-ttu-id="93ebe-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="93ebe-243">System-Flags</span></span>           | <span data-ttu-id="93ebe-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="93ebe-244">0x00000010</span></span>                                   |
| <span data-ttu-id="93ebe-245">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="93ebe-245">Classes used in</span></span>        | [<span data-ttu-id="93ebe-246">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="93ebe-246">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="93ebe-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="93ebe-247">Windows Server 2012</span></span>



| <span data-ttu-id="93ebe-248">Voce</span><span class="sxs-lookup"><span data-stu-id="93ebe-248">Entry</span></span> | <span data-ttu-id="93ebe-249">Valore</span><span class="sxs-lookup"><span data-stu-id="93ebe-249">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="93ebe-250">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="93ebe-250">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="93ebe-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="93ebe-251">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="93ebe-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="93ebe-252">System-Only</span></span>            | <span data-ttu-id="93ebe-253">Falso</span><span class="sxs-lookup"><span data-stu-id="93ebe-253">False</span></span>                                        |
| <span data-ttu-id="93ebe-254">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="93ebe-254">Is-Single-Valued</span></span>       | <span data-ttu-id="93ebe-255">Vero</span><span class="sxs-lookup"><span data-stu-id="93ebe-255">True</span></span>                                         |
| <span data-ttu-id="93ebe-256">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="93ebe-256">Is Indexed</span></span>             | <span data-ttu-id="93ebe-257">Falso</span><span class="sxs-lookup"><span data-stu-id="93ebe-257">False</span></span>                                        |
| <span data-ttu-id="93ebe-258">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="93ebe-258">In Global Catalog</span></span>      | <span data-ttu-id="93ebe-259">Falso</span><span class="sxs-lookup"><span data-stu-id="93ebe-259">False</span></span>                                        |
| <span data-ttu-id="93ebe-260">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="93ebe-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="93ebe-261">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="93ebe-261">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="93ebe-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="93ebe-262">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="93ebe-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="93ebe-263">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="93ebe-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="93ebe-264">Search-Flags</span></span>           | <span data-ttu-id="93ebe-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="93ebe-265">0x00000000</span></span>                                   |
| <span data-ttu-id="93ebe-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="93ebe-266">System-Flags</span></span>           | <span data-ttu-id="93ebe-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="93ebe-267">0x00000010</span></span>                                   |
| <span data-ttu-id="93ebe-268">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="93ebe-268">Classes used in</span></span>        | [<span data-ttu-id="93ebe-269">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="93ebe-269">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



 

 





