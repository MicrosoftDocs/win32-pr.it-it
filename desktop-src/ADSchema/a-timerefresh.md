---
title: Attributo Time-Refresh
description: Questo attributo ha l'intervallo durante il quale un record di risorse contenuto in una Active Directory zona integrata deve essere aggiornato per il server DNS. L'intervallo predefinito è 7 giorni.
ms.assetid: 9e473c29-7fcf-4d6d-8a7c-2791c7822c7d
ms.tgt_platform: multiple
keywords:
- Schema AD Time-Refresh attribute
- Schema AD dell'attributo timeRefresh
topic_type:
- apiref
api_name:
- Time-Refresh
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87bc360686b1692d2dbda1ee23ad6351e69d3afe
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103965323"
---
# <a name="time-refresh-attribute"></a><span data-ttu-id="fabbf-106">Attributo Time-Refresh</span><span class="sxs-lookup"><span data-stu-id="fabbf-106">Time-Refresh attribute</span></span>

<span data-ttu-id="fabbf-107">Questo attributo ha l'intervallo durante il quale un record di risorse contenuto in una Active Directory zona integrata deve essere aggiornato per il server DNS.</span><span class="sxs-lookup"><span data-stu-id="fabbf-107">This attribute has the interval during which a resource record that is contained in an Active Directory integrated zone should be refreshed for the DNS server.</span></span> <span data-ttu-id="fabbf-108">L'intervallo predefinito è 7 giorni.</span><span class="sxs-lookup"><span data-stu-id="fabbf-108">The default interval is 7 days.</span></span>



| <span data-ttu-id="fabbf-109">Voce</span><span class="sxs-lookup"><span data-stu-id="fabbf-109">Entry</span></span> | <span data-ttu-id="fabbf-110">Valore</span><span class="sxs-lookup"><span data-stu-id="fabbf-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="fabbf-111">CN</span><span class="sxs-lookup"><span data-stu-id="fabbf-111">CN</span></span>                | <span data-ttu-id="fabbf-112">Time-Refresh</span><span class="sxs-lookup"><span data-stu-id="fabbf-112">Time-Refresh</span></span>                         |
| <span data-ttu-id="fabbf-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="fabbf-113">Ldap-Display-Name</span></span> | <span data-ttu-id="fabbf-114">timeRefresh</span><span class="sxs-lookup"><span data-stu-id="fabbf-114">timeRefresh</span></span>                          |
| <span data-ttu-id="fabbf-115">Dimensione</span><span class="sxs-lookup"><span data-stu-id="fabbf-115">Size</span></span>              | \-                                   |
| <span data-ttu-id="fabbf-116">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="fabbf-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="fabbf-117">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="fabbf-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="fabbf-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="fabbf-118">Attribute-Id</span></span>      | <span data-ttu-id="fabbf-119">1.2.840.113556.1.4.503</span><span class="sxs-lookup"><span data-stu-id="fabbf-119">1.2.840.113556.1.4.503</span></span>               |
| <span data-ttu-id="fabbf-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="fabbf-120">System-Id-Guid</span></span>    | <span data-ttu-id="fabbf-121">ddac0cf1-af8f-11d0-afeb-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="fabbf-121">ddac0cf1-af8f-11d0-afeb-00c04fd930c9</span></span> |
| <span data-ttu-id="fabbf-122">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fabbf-122">Syntax</span></span>            | [<span data-ttu-id="fabbf-123">**Interval**</span><span class="sxs-lookup"><span data-stu-id="fabbf-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="fabbf-124">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="fabbf-124">Implementations</span></span>

-   [<span data-ttu-id="fabbf-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="fabbf-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="fabbf-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="fabbf-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="fabbf-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="fabbf-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="fabbf-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="fabbf-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="fabbf-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="fabbf-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="fabbf-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="fabbf-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="fabbf-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="fabbf-131">Windows 2000 Server</span></span>



| <span data-ttu-id="fabbf-132">Voce</span><span class="sxs-lookup"><span data-stu-id="fabbf-132">Entry</span></span> | <span data-ttu-id="fabbf-133">Valore</span><span class="sxs-lookup"><span data-stu-id="fabbf-133">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fabbf-134">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="fabbf-134">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="fabbf-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fabbf-135">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="fabbf-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="fabbf-136">System-Only</span></span>            | <span data-ttu-id="fabbf-137">Falso</span><span class="sxs-lookup"><span data-stu-id="fabbf-137">False</span></span>                                                                                                                         |
| <span data-ttu-id="fabbf-138">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="fabbf-138">Is-Single-Valued</span></span>       | <span data-ttu-id="fabbf-139">Vero</span><span class="sxs-lookup"><span data-stu-id="fabbf-139">True</span></span>                                                                                                                          |
| <span data-ttu-id="fabbf-140">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="fabbf-140">Is Indexed</span></span>             | <span data-ttu-id="fabbf-141">Falso</span><span class="sxs-lookup"><span data-stu-id="fabbf-141">False</span></span>                                                                                                                         |
| <span data-ttu-id="fabbf-142">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="fabbf-142">In Global Catalog</span></span>      | <span data-ttu-id="fabbf-143">Falso</span><span class="sxs-lookup"><span data-stu-id="fabbf-143">False</span></span>                                                                                                                         |
| <span data-ttu-id="fabbf-144">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="fabbf-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="fabbf-145">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="fabbf-145">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="fabbf-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fabbf-146">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="fabbf-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fabbf-147">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="fabbf-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fabbf-148">Search-Flags</span></span>           | <span data-ttu-id="fabbf-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fabbf-149">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="fabbf-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fabbf-150">System-Flags</span></span>           | <span data-ttu-id="fabbf-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fabbf-151">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="fabbf-152">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="fabbf-152">Classes used in</span></span>        | [<span data-ttu-id="fabbf-153">**Link-Track-OMT-entry**</span><span class="sxs-lookup"><span data-stu-id="fabbf-153">**Link-Track-OMT-Entry**</span></span>](c-linktrackomtentry.md)<br/> [<span data-ttu-id="fabbf-154">**Link-Track-vol-entry**</span><span class="sxs-lookup"><span data-stu-id="fabbf-154">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="fabbf-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="fabbf-155">Windows Server 2003</span></span>



| <span data-ttu-id="fabbf-156">Voce</span><span class="sxs-lookup"><span data-stu-id="fabbf-156">Entry</span></span> | <span data-ttu-id="fabbf-157">Valore</span><span class="sxs-lookup"><span data-stu-id="fabbf-157">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fabbf-158">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="fabbf-158">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="fabbf-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fabbf-159">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="fabbf-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="fabbf-160">System-Only</span></span>            | <span data-ttu-id="fabbf-161">Falso</span><span class="sxs-lookup"><span data-stu-id="fabbf-161">False</span></span>                                                                                                                         |
| <span data-ttu-id="fabbf-162">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="fabbf-162">Is-Single-Valued</span></span>       | <span data-ttu-id="fabbf-163">Vero</span><span class="sxs-lookup"><span data-stu-id="fabbf-163">True</span></span>                                                                                                                          |
| <span data-ttu-id="fabbf-164">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="fabbf-164">Is Indexed</span></span>             | <span data-ttu-id="fabbf-165">Falso</span><span class="sxs-lookup"><span data-stu-id="fabbf-165">False</span></span>                                                                                                                         |
| <span data-ttu-id="fabbf-166">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="fabbf-166">In Global Catalog</span></span>      | <span data-ttu-id="fabbf-167">Falso</span><span class="sxs-lookup"><span data-stu-id="fabbf-167">False</span></span>                                                                                                                         |
| <span data-ttu-id="fabbf-168">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="fabbf-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="fabbf-169">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="fabbf-169">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="fabbf-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fabbf-170">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="fabbf-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fabbf-171">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="fabbf-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fabbf-172">Search-Flags</span></span>           | <span data-ttu-id="fabbf-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fabbf-173">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="fabbf-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fabbf-174">System-Flags</span></span>           | <span data-ttu-id="fabbf-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fabbf-175">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="fabbf-176">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="fabbf-176">Classes used in</span></span>        | [<span data-ttu-id="fabbf-177">**Link-Track-OMT-entry**</span><span class="sxs-lookup"><span data-stu-id="fabbf-177">**Link-Track-OMT-Entry**</span></span>](c-linktrackomtentry.md)<br/> [<span data-ttu-id="fabbf-178">**Link-Track-vol-entry**</span><span class="sxs-lookup"><span data-stu-id="fabbf-178">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="fabbf-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="fabbf-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="fabbf-180">Voce</span><span class="sxs-lookup"><span data-stu-id="fabbf-180">Entry</span></span> | <span data-ttu-id="fabbf-181">Valore</span><span class="sxs-lookup"><span data-stu-id="fabbf-181">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fabbf-182">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="fabbf-182">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="fabbf-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fabbf-183">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="fabbf-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="fabbf-184">System-Only</span></span>            | <span data-ttu-id="fabbf-185">Falso</span><span class="sxs-lookup"><span data-stu-id="fabbf-185">False</span></span>                                                                                                                         |
| <span data-ttu-id="fabbf-186">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="fabbf-186">Is-Single-Valued</span></span>       | <span data-ttu-id="fabbf-187">Vero</span><span class="sxs-lookup"><span data-stu-id="fabbf-187">True</span></span>                                                                                                                          |
| <span data-ttu-id="fabbf-188">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="fabbf-188">Is Indexed</span></span>             | <span data-ttu-id="fabbf-189">Falso</span><span class="sxs-lookup"><span data-stu-id="fabbf-189">False</span></span>                                                                                                                         |
| <span data-ttu-id="fabbf-190">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="fabbf-190">In Global Catalog</span></span>      | <span data-ttu-id="fabbf-191">Falso</span><span class="sxs-lookup"><span data-stu-id="fabbf-191">False</span></span>                                                                                                                         |
| <span data-ttu-id="fabbf-192">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="fabbf-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="fabbf-193">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="fabbf-193">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="fabbf-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fabbf-194">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="fabbf-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fabbf-195">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="fabbf-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fabbf-196">Search-Flags</span></span>           | <span data-ttu-id="fabbf-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fabbf-197">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="fabbf-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fabbf-198">System-Flags</span></span>           | <span data-ttu-id="fabbf-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fabbf-199">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="fabbf-200">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="fabbf-200">Classes used in</span></span>        | [<span data-ttu-id="fabbf-201">**Link-Track-OMT-entry**</span><span class="sxs-lookup"><span data-stu-id="fabbf-201">**Link-Track-OMT-Entry**</span></span>](c-linktrackomtentry.md)<br/> [<span data-ttu-id="fabbf-202">**Link-Track-vol-entry**</span><span class="sxs-lookup"><span data-stu-id="fabbf-202">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="fabbf-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fabbf-203">Windows Server 2008</span></span>



| <span data-ttu-id="fabbf-204">Voce</span><span class="sxs-lookup"><span data-stu-id="fabbf-204">Entry</span></span> | <span data-ttu-id="fabbf-205">Valore</span><span class="sxs-lookup"><span data-stu-id="fabbf-205">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fabbf-206">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="fabbf-206">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="fabbf-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fabbf-207">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="fabbf-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="fabbf-208">System-Only</span></span>            | <span data-ttu-id="fabbf-209">Falso</span><span class="sxs-lookup"><span data-stu-id="fabbf-209">False</span></span>                                                                                                                         |
| <span data-ttu-id="fabbf-210">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="fabbf-210">Is-Single-Valued</span></span>       | <span data-ttu-id="fabbf-211">Vero</span><span class="sxs-lookup"><span data-stu-id="fabbf-211">True</span></span>                                                                                                                          |
| <span data-ttu-id="fabbf-212">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="fabbf-212">Is Indexed</span></span>             | <span data-ttu-id="fabbf-213">Falso</span><span class="sxs-lookup"><span data-stu-id="fabbf-213">False</span></span>                                                                                                                         |
| <span data-ttu-id="fabbf-214">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="fabbf-214">In Global Catalog</span></span>      | <span data-ttu-id="fabbf-215">Falso</span><span class="sxs-lookup"><span data-stu-id="fabbf-215">False</span></span>                                                                                                                         |
| <span data-ttu-id="fabbf-216">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="fabbf-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="fabbf-217">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="fabbf-217">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="fabbf-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fabbf-218">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="fabbf-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fabbf-219">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="fabbf-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fabbf-220">Search-Flags</span></span>           | <span data-ttu-id="fabbf-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fabbf-221">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="fabbf-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fabbf-222">System-Flags</span></span>           | <span data-ttu-id="fabbf-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fabbf-223">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="fabbf-224">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="fabbf-224">Classes used in</span></span>        | [<span data-ttu-id="fabbf-225">**Link-Track-OMT-entry**</span><span class="sxs-lookup"><span data-stu-id="fabbf-225">**Link-Track-OMT-Entry**</span></span>](c-linktrackomtentry.md)<br/> [<span data-ttu-id="fabbf-226">**Link-Track-vol-entry**</span><span class="sxs-lookup"><span data-stu-id="fabbf-226">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="fabbf-227">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="fabbf-227">Windows Server 2008 R2</span></span>



| <span data-ttu-id="fabbf-228">Voce</span><span class="sxs-lookup"><span data-stu-id="fabbf-228">Entry</span></span> | <span data-ttu-id="fabbf-229">Valore</span><span class="sxs-lookup"><span data-stu-id="fabbf-229">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fabbf-230">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="fabbf-230">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="fabbf-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fabbf-231">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="fabbf-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="fabbf-232">System-Only</span></span>            | <span data-ttu-id="fabbf-233">Falso</span><span class="sxs-lookup"><span data-stu-id="fabbf-233">False</span></span>                                                                                                                         |
| <span data-ttu-id="fabbf-234">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="fabbf-234">Is-Single-Valued</span></span>       | <span data-ttu-id="fabbf-235">Vero</span><span class="sxs-lookup"><span data-stu-id="fabbf-235">True</span></span>                                                                                                                          |
| <span data-ttu-id="fabbf-236">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="fabbf-236">Is Indexed</span></span>             | <span data-ttu-id="fabbf-237">Falso</span><span class="sxs-lookup"><span data-stu-id="fabbf-237">False</span></span>                                                                                                                         |
| <span data-ttu-id="fabbf-238">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="fabbf-238">In Global Catalog</span></span>      | <span data-ttu-id="fabbf-239">Falso</span><span class="sxs-lookup"><span data-stu-id="fabbf-239">False</span></span>                                                                                                                         |
| <span data-ttu-id="fabbf-240">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="fabbf-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="fabbf-241">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="fabbf-241">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="fabbf-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fabbf-242">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="fabbf-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fabbf-243">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="fabbf-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fabbf-244">Search-Flags</span></span>           | <span data-ttu-id="fabbf-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fabbf-245">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="fabbf-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fabbf-246">System-Flags</span></span>           | <span data-ttu-id="fabbf-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fabbf-247">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="fabbf-248">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="fabbf-248">Classes used in</span></span>        | [<span data-ttu-id="fabbf-249">**Link-Track-OMT-entry**</span><span class="sxs-lookup"><span data-stu-id="fabbf-249">**Link-Track-OMT-Entry**</span></span>](c-linktrackomtentry.md)<br/> [<span data-ttu-id="fabbf-250">**Link-Track-vol-entry**</span><span class="sxs-lookup"><span data-stu-id="fabbf-250">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="fabbf-251">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="fabbf-251">Windows Server 2012</span></span>



| <span data-ttu-id="fabbf-252">Voce</span><span class="sxs-lookup"><span data-stu-id="fabbf-252">Entry</span></span> | <span data-ttu-id="fabbf-253">Valore</span><span class="sxs-lookup"><span data-stu-id="fabbf-253">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fabbf-254">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="fabbf-254">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="fabbf-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fabbf-255">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="fabbf-256">System-Only</span><span class="sxs-lookup"><span data-stu-id="fabbf-256">System-Only</span></span>            | <span data-ttu-id="fabbf-257">Falso</span><span class="sxs-lookup"><span data-stu-id="fabbf-257">False</span></span>                                                                                                                         |
| <span data-ttu-id="fabbf-258">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="fabbf-258">Is-Single-Valued</span></span>       | <span data-ttu-id="fabbf-259">Vero</span><span class="sxs-lookup"><span data-stu-id="fabbf-259">True</span></span>                                                                                                                          |
| <span data-ttu-id="fabbf-260">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="fabbf-260">Is Indexed</span></span>             | <span data-ttu-id="fabbf-261">Falso</span><span class="sxs-lookup"><span data-stu-id="fabbf-261">False</span></span>                                                                                                                         |
| <span data-ttu-id="fabbf-262">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="fabbf-262">In Global Catalog</span></span>      | <span data-ttu-id="fabbf-263">Falso</span><span class="sxs-lookup"><span data-stu-id="fabbf-263">False</span></span>                                                                                                                         |
| <span data-ttu-id="fabbf-264">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="fabbf-264">NT-Security-Descriptor</span></span> | <span data-ttu-id="fabbf-265">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="fabbf-265">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="fabbf-266">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fabbf-266">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="fabbf-267">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fabbf-267">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="fabbf-268">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fabbf-268">Search-Flags</span></span>           | <span data-ttu-id="fabbf-269">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fabbf-269">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="fabbf-270">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fabbf-270">System-Flags</span></span>           | <span data-ttu-id="fabbf-271">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fabbf-271">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="fabbf-272">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="fabbf-272">Classes used in</span></span>        | [<span data-ttu-id="fabbf-273">**Link-Track-OMT-entry**</span><span class="sxs-lookup"><span data-stu-id="fabbf-273">**Link-Track-OMT-Entry**</span></span>](c-linktrackomtentry.md)<br/> [<span data-ttu-id="fabbf-274">**Link-Track-vol-entry**</span><span class="sxs-lookup"><span data-stu-id="fabbf-274">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



 

 





