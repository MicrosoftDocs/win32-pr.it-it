---
title: Attributo PEK-Key-Change-Interval
description: Intervallo di modifica della chiave di crittografia della password.
ms.assetid: 2031feda-3f5d-4c76-bb45-42157fd5cb84
ms.tgt_platform: multiple
keywords:
- Attributo PEK-Key-Change-Interval
- Schema AD dell'attributo pekKeyChangeInterval
topic_type:
- apiref
api_name:
- Pek-Key-Change-Interval
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2259bdd4dfee24bbccfeafa6d5bb06490c24c25c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "106303164"
---
# <a name="pek-key-change-interval-attribute"></a><span data-ttu-id="a9f65-105">Attributo PEK-Key-Change-Interval</span><span class="sxs-lookup"><span data-stu-id="a9f65-105">Pek-Key-Change-Interval attribute</span></span>

<span data-ttu-id="a9f65-106">Intervallo di modifica della chiave di crittografia della password.</span><span class="sxs-lookup"><span data-stu-id="a9f65-106">Password encryption key change interval.</span></span>



| <span data-ttu-id="a9f65-107">Voce</span><span class="sxs-lookup"><span data-stu-id="a9f65-107">Entry</span></span> | <span data-ttu-id="a9f65-108">Valore</span><span class="sxs-lookup"><span data-stu-id="a9f65-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="a9f65-109">CN</span><span class="sxs-lookup"><span data-stu-id="a9f65-109">CN</span></span>                | <span data-ttu-id="a9f65-110">PEK-Key-Change-Interval</span><span class="sxs-lookup"><span data-stu-id="a9f65-110">Pek-Key-Change-Interval</span></span>              |
| <span data-ttu-id="a9f65-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="a9f65-111">Ldap-Display-Name</span></span> | <span data-ttu-id="a9f65-112">pekKeyChangeInterval</span><span class="sxs-lookup"><span data-stu-id="a9f65-112">pekKeyChangeInterval</span></span>                 |
| <span data-ttu-id="a9f65-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="a9f65-113">Size</span></span>              | <span data-ttu-id="a9f65-114">8 byte</span><span class="sxs-lookup"><span data-stu-id="a9f65-114">8 bytes</span></span>                              |
| <span data-ttu-id="a9f65-115">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="a9f65-115">Update Privilege</span></span>  | <span data-ttu-id="a9f65-116">Questo valore viene impostato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="a9f65-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="a9f65-117">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="a9f65-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="a9f65-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a9f65-118">Attribute-Id</span></span>      | <span data-ttu-id="a9f65-119">1.2.840.113556.1.4.866</span><span class="sxs-lookup"><span data-stu-id="a9f65-119">1.2.840.113556.1.4.866</span></span>               |
| <span data-ttu-id="a9f65-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="a9f65-120">System-Id-Guid</span></span>    | <span data-ttu-id="a9f65-121">07383084-91df-11d1-aebc-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="a9f65-121">07383084-91df-11d1-aebc-0000f80367c1</span></span> |
| <span data-ttu-id="a9f65-122">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a9f65-122">Syntax</span></span>            | [<span data-ttu-id="a9f65-123">**Interval**</span><span class="sxs-lookup"><span data-stu-id="a9f65-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="a9f65-124">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="a9f65-124">Implementations</span></span>

-   [<span data-ttu-id="a9f65-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="a9f65-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="a9f65-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a9f65-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a9f65-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a9f65-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a9f65-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a9f65-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a9f65-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a9f65-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a9f65-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a9f65-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="a9f65-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a9f65-131">Windows 2000 Server</span></span>



| <span data-ttu-id="a9f65-132">Voce</span><span class="sxs-lookup"><span data-stu-id="a9f65-132">Entry</span></span> | <span data-ttu-id="a9f65-133">Valore</span><span class="sxs-lookup"><span data-stu-id="a9f65-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="a9f65-134">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="a9f65-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="a9f65-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a9f65-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="a9f65-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="a9f65-136">System-Only</span></span>            | <span data-ttu-id="a9f65-137">Falso</span><span class="sxs-lookup"><span data-stu-id="a9f65-137">False</span></span>                                        |
| <span data-ttu-id="a9f65-138">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="a9f65-138">Is-Single-Valued</span></span>       | <span data-ttu-id="a9f65-139">Vero</span><span class="sxs-lookup"><span data-stu-id="a9f65-139">True</span></span>                                         |
| <span data-ttu-id="a9f65-140">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="a9f65-140">Is Indexed</span></span>             | <span data-ttu-id="a9f65-141">Falso</span><span class="sxs-lookup"><span data-stu-id="a9f65-141">False</span></span>                                        |
| <span data-ttu-id="a9f65-142">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="a9f65-142">In Global Catalog</span></span>      | <span data-ttu-id="a9f65-143">Falso</span><span class="sxs-lookup"><span data-stu-id="a9f65-143">False</span></span>                                        |
| <span data-ttu-id="a9f65-144">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="a9f65-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="a9f65-145">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="a9f65-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="a9f65-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a9f65-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="a9f65-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a9f65-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="a9f65-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a9f65-148">Search-Flags</span></span>           | <span data-ttu-id="a9f65-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a9f65-149">0x00000000</span></span>                                   |
| <span data-ttu-id="a9f65-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a9f65-150">System-Flags</span></span>           | <span data-ttu-id="a9f65-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a9f65-151">0x00000010</span></span>                                   |
| <span data-ttu-id="a9f65-152">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="a9f65-152">Classes used in</span></span>        | [<span data-ttu-id="a9f65-153">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="a9f65-153">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="a9f65-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a9f65-154">Windows Server 2003</span></span>



| <span data-ttu-id="a9f65-155">Voce</span><span class="sxs-lookup"><span data-stu-id="a9f65-155">Entry</span></span> | <span data-ttu-id="a9f65-156">Valore</span><span class="sxs-lookup"><span data-stu-id="a9f65-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="a9f65-157">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="a9f65-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="a9f65-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a9f65-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="a9f65-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="a9f65-159">System-Only</span></span>            | <span data-ttu-id="a9f65-160">Falso</span><span class="sxs-lookup"><span data-stu-id="a9f65-160">False</span></span>                                        |
| <span data-ttu-id="a9f65-161">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="a9f65-161">Is-Single-Valued</span></span>       | <span data-ttu-id="a9f65-162">Vero</span><span class="sxs-lookup"><span data-stu-id="a9f65-162">True</span></span>                                         |
| <span data-ttu-id="a9f65-163">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="a9f65-163">Is Indexed</span></span>             | <span data-ttu-id="a9f65-164">Falso</span><span class="sxs-lookup"><span data-stu-id="a9f65-164">False</span></span>                                        |
| <span data-ttu-id="a9f65-165">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="a9f65-165">In Global Catalog</span></span>      | <span data-ttu-id="a9f65-166">Falso</span><span class="sxs-lookup"><span data-stu-id="a9f65-166">False</span></span>                                        |
| <span data-ttu-id="a9f65-167">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="a9f65-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="a9f65-168">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="a9f65-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="a9f65-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a9f65-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="a9f65-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a9f65-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="a9f65-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a9f65-171">Search-Flags</span></span>           | <span data-ttu-id="a9f65-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a9f65-172">0x00000000</span></span>                                   |
| <span data-ttu-id="a9f65-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a9f65-173">System-Flags</span></span>           | <span data-ttu-id="a9f65-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a9f65-174">0x00000010</span></span>                                   |
| <span data-ttu-id="a9f65-175">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="a9f65-175">Classes used in</span></span>        | [<span data-ttu-id="a9f65-176">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="a9f65-176">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a9f65-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a9f65-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a9f65-178">Voce</span><span class="sxs-lookup"><span data-stu-id="a9f65-178">Entry</span></span> | <span data-ttu-id="a9f65-179">Valore</span><span class="sxs-lookup"><span data-stu-id="a9f65-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="a9f65-180">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="a9f65-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="a9f65-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a9f65-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="a9f65-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="a9f65-182">System-Only</span></span>            | <span data-ttu-id="a9f65-183">Falso</span><span class="sxs-lookup"><span data-stu-id="a9f65-183">False</span></span>                                        |
| <span data-ttu-id="a9f65-184">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="a9f65-184">Is-Single-Valued</span></span>       | <span data-ttu-id="a9f65-185">Vero</span><span class="sxs-lookup"><span data-stu-id="a9f65-185">True</span></span>                                         |
| <span data-ttu-id="a9f65-186">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="a9f65-186">Is Indexed</span></span>             | <span data-ttu-id="a9f65-187">Falso</span><span class="sxs-lookup"><span data-stu-id="a9f65-187">False</span></span>                                        |
| <span data-ttu-id="a9f65-188">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="a9f65-188">In Global Catalog</span></span>      | <span data-ttu-id="a9f65-189">Falso</span><span class="sxs-lookup"><span data-stu-id="a9f65-189">False</span></span>                                        |
| <span data-ttu-id="a9f65-190">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="a9f65-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="a9f65-191">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="a9f65-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="a9f65-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a9f65-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="a9f65-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a9f65-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="a9f65-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a9f65-194">Search-Flags</span></span>           | <span data-ttu-id="a9f65-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a9f65-195">0x00000000</span></span>                                   |
| <span data-ttu-id="a9f65-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a9f65-196">System-Flags</span></span>           | <span data-ttu-id="a9f65-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a9f65-197">0x00000010</span></span>                                   |
| <span data-ttu-id="a9f65-198">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="a9f65-198">Classes used in</span></span>        | [<span data-ttu-id="a9f65-199">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="a9f65-199">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a9f65-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a9f65-200">Windows Server 2008</span></span>



| <span data-ttu-id="a9f65-201">Voce</span><span class="sxs-lookup"><span data-stu-id="a9f65-201">Entry</span></span> | <span data-ttu-id="a9f65-202">Valore</span><span class="sxs-lookup"><span data-stu-id="a9f65-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="a9f65-203">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="a9f65-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="a9f65-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a9f65-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="a9f65-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="a9f65-205">System-Only</span></span>            | <span data-ttu-id="a9f65-206">Falso</span><span class="sxs-lookup"><span data-stu-id="a9f65-206">False</span></span>                                        |
| <span data-ttu-id="a9f65-207">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="a9f65-207">Is-Single-Valued</span></span>       | <span data-ttu-id="a9f65-208">Vero</span><span class="sxs-lookup"><span data-stu-id="a9f65-208">True</span></span>                                         |
| <span data-ttu-id="a9f65-209">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="a9f65-209">Is Indexed</span></span>             | <span data-ttu-id="a9f65-210">Falso</span><span class="sxs-lookup"><span data-stu-id="a9f65-210">False</span></span>                                        |
| <span data-ttu-id="a9f65-211">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="a9f65-211">In Global Catalog</span></span>      | <span data-ttu-id="a9f65-212">Falso</span><span class="sxs-lookup"><span data-stu-id="a9f65-212">False</span></span>                                        |
| <span data-ttu-id="a9f65-213">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="a9f65-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="a9f65-214">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="a9f65-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="a9f65-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a9f65-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="a9f65-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a9f65-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="a9f65-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a9f65-217">Search-Flags</span></span>           | <span data-ttu-id="a9f65-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a9f65-218">0x00000000</span></span>                                   |
| <span data-ttu-id="a9f65-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a9f65-219">System-Flags</span></span>           | <span data-ttu-id="a9f65-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a9f65-220">0x00000010</span></span>                                   |
| <span data-ttu-id="a9f65-221">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="a9f65-221">Classes used in</span></span>        | [<span data-ttu-id="a9f65-222">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="a9f65-222">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a9f65-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a9f65-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a9f65-224">Voce</span><span class="sxs-lookup"><span data-stu-id="a9f65-224">Entry</span></span> | <span data-ttu-id="a9f65-225">Valore</span><span class="sxs-lookup"><span data-stu-id="a9f65-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="a9f65-226">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="a9f65-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="a9f65-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a9f65-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="a9f65-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="a9f65-228">System-Only</span></span>            | <span data-ttu-id="a9f65-229">Falso</span><span class="sxs-lookup"><span data-stu-id="a9f65-229">False</span></span>                                        |
| <span data-ttu-id="a9f65-230">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="a9f65-230">Is-Single-Valued</span></span>       | <span data-ttu-id="a9f65-231">Vero</span><span class="sxs-lookup"><span data-stu-id="a9f65-231">True</span></span>                                         |
| <span data-ttu-id="a9f65-232">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="a9f65-232">Is Indexed</span></span>             | <span data-ttu-id="a9f65-233">Falso</span><span class="sxs-lookup"><span data-stu-id="a9f65-233">False</span></span>                                        |
| <span data-ttu-id="a9f65-234">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="a9f65-234">In Global Catalog</span></span>      | <span data-ttu-id="a9f65-235">Falso</span><span class="sxs-lookup"><span data-stu-id="a9f65-235">False</span></span>                                        |
| <span data-ttu-id="a9f65-236">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="a9f65-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="a9f65-237">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="a9f65-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="a9f65-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a9f65-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="a9f65-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a9f65-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="a9f65-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a9f65-240">Search-Flags</span></span>           | <span data-ttu-id="a9f65-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a9f65-241">0x00000000</span></span>                                   |
| <span data-ttu-id="a9f65-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a9f65-242">System-Flags</span></span>           | <span data-ttu-id="a9f65-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a9f65-243">0x00000010</span></span>                                   |
| <span data-ttu-id="a9f65-244">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="a9f65-244">Classes used in</span></span>        | [<span data-ttu-id="a9f65-245">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="a9f65-245">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a9f65-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a9f65-246">Windows Server 2012</span></span>



| <span data-ttu-id="a9f65-247">Voce</span><span class="sxs-lookup"><span data-stu-id="a9f65-247">Entry</span></span> | <span data-ttu-id="a9f65-248">Valore</span><span class="sxs-lookup"><span data-stu-id="a9f65-248">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="a9f65-249">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="a9f65-249">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="a9f65-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a9f65-250">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="a9f65-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="a9f65-251">System-Only</span></span>            | <span data-ttu-id="a9f65-252">Falso</span><span class="sxs-lookup"><span data-stu-id="a9f65-252">False</span></span>                                        |
| <span data-ttu-id="a9f65-253">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="a9f65-253">Is-Single-Valued</span></span>       | <span data-ttu-id="a9f65-254">Vero</span><span class="sxs-lookup"><span data-stu-id="a9f65-254">True</span></span>                                         |
| <span data-ttu-id="a9f65-255">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="a9f65-255">Is Indexed</span></span>             | <span data-ttu-id="a9f65-256">Falso</span><span class="sxs-lookup"><span data-stu-id="a9f65-256">False</span></span>                                        |
| <span data-ttu-id="a9f65-257">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="a9f65-257">In Global Catalog</span></span>      | <span data-ttu-id="a9f65-258">Falso</span><span class="sxs-lookup"><span data-stu-id="a9f65-258">False</span></span>                                        |
| <span data-ttu-id="a9f65-259">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="a9f65-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="a9f65-260">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="a9f65-260">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="a9f65-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a9f65-261">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="a9f65-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a9f65-262">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="a9f65-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a9f65-263">Search-Flags</span></span>           | <span data-ttu-id="a9f65-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a9f65-264">0x00000000</span></span>                                   |
| <span data-ttu-id="a9f65-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a9f65-265">System-Flags</span></span>           | <span data-ttu-id="a9f65-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a9f65-266">0x00000010</span></span>                                   |
| <span data-ttu-id="a9f65-267">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="a9f65-267">Classes used in</span></span>        | [<span data-ttu-id="a9f65-268">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="a9f65-268">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



 

 





