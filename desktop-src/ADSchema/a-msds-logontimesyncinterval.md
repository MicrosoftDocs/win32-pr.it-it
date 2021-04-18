---
title: attributo ms-DS-login-Time-Sync-Interval
description: Questo attributo controlla la granularità, in giorni, in cui l'ora dell'ultimo accesso per un utente o un computer, registrato nell'attributo lastLogonTimestamp, viene replicata in tutti i controller di dominio in un dominio.
ms.assetid: f1f9f1f8-df60-44b5-965d-631c4dd4ef84
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo ms-DS-login-Time-Sync-Interval
- attributo msDS-LogonTimeSyncInterval-schema AD
topic_type:
- apiref
api_name:
- ms-DS-Logon-Time-Sync-Interval
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5dbf23ca77bda9dac76f02986be1c05c80559199
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104520166"
---
# <a name="ms-ds-logon-time-sync-interval-attribute"></a><span data-ttu-id="a42b0-105">attributo ms-DS-login-Time-Sync-Interval</span><span class="sxs-lookup"><span data-stu-id="a42b0-105">ms-DS-Logon-Time-Sync-Interval attribute</span></span>

<span data-ttu-id="a42b0-106">Questo attributo controlla la granularità, in giorni, in cui l'ora dell'ultimo accesso per un utente o un computer, registrato nell'attributo lastLogonTimestamp, viene replicata in tutti i controller di dominio in un dominio.</span><span class="sxs-lookup"><span data-stu-id="a42b0-106">This attribute controls the granularity, in days, with which the last logon time for a user or computer, recorded in the lastLogonTimestamp attribute, is replicated to all DCs in a domain.</span></span>



| <span data-ttu-id="a42b0-107">Voce</span><span class="sxs-lookup"><span data-stu-id="a42b0-107">Entry</span></span> | <span data-ttu-id="a42b0-108">Valore</span><span class="sxs-lookup"><span data-stu-id="a42b0-108">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a42b0-109">CN</span><span class="sxs-lookup"><span data-stu-id="a42b0-109">CN</span></span>                | <span data-ttu-id="a42b0-110">ms-DS-Access-Time-Sync-Interval</span><span class="sxs-lookup"><span data-stu-id="a42b0-110">ms-DS-Logon-Time-Sync-Interval</span></span>                                                                             |
| <span data-ttu-id="a42b0-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="a42b0-111">Ldap-Display-Name</span></span> | <span data-ttu-id="a42b0-112">msDS-LogonTimeSyncInterval</span><span class="sxs-lookup"><span data-stu-id="a42b0-112">msDS-LogonTimeSyncInterval</span></span>                                                                                 |
| <span data-ttu-id="a42b0-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="a42b0-113">Size</span></span>              | <span data-ttu-id="a42b0-114">4 byte</span><span class="sxs-lookup"><span data-stu-id="a42b0-114">4 bytes</span></span>                                                                                                    |
| <span data-ttu-id="a42b0-115">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="a42b0-115">Update Privilege</span></span>  | <span data-ttu-id="a42b0-116">Amministratore di dominio</span><span class="sxs-lookup"><span data-stu-id="a42b0-116">Domain administrator</span></span>                                                                                       |
| <span data-ttu-id="a42b0-117">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="a42b0-117">Update Frequency</span></span>  | <span data-ttu-id="a42b0-118">Raramente, poiché si tratta di un'impostazione di criteri, viene aggiornata solo quando si desidera modificare i criteri a livello di dominio.</span><span class="sxs-lookup"><span data-stu-id="a42b0-118">Rarely, since this is a policy setting, it is updated only when a change in domain-wide policy is desired.</span></span> |
| <span data-ttu-id="a42b0-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a42b0-119">Attribute-Id</span></span>      | <span data-ttu-id="a42b0-120">1.2.840.113556.1.4.1784</span><span class="sxs-lookup"><span data-stu-id="a42b0-120">1.2.840.113556.1.4.1784</span></span>                                                                                    |
| <span data-ttu-id="a42b0-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="a42b0-121">System-Id-Guid</span></span>    | <span data-ttu-id="a42b0-122">ad7940f8-e43a-4a42-83bc-d688e59ea605</span><span class="sxs-lookup"><span data-stu-id="a42b0-122">ad7940f8-e43a-4a42-83bc-d688e59ea605</span></span>                                                                       |
| <span data-ttu-id="a42b0-123">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a42b0-123">Syntax</span></span>            | [<span data-ttu-id="a42b0-124">**Enumerazione**</span><span class="sxs-lookup"><span data-stu-id="a42b0-124">**Enumeration**</span></span>](s-enumeration.md)                                                                       |



## <a name="implementations"></a><span data-ttu-id="a42b0-125">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="a42b0-125">Implementations</span></span>

-   [<span data-ttu-id="a42b0-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a42b0-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a42b0-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a42b0-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a42b0-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a42b0-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a42b0-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a42b0-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a42b0-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a42b0-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="a42b0-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a42b0-131">Windows Server 2003</span></span>



| <span data-ttu-id="a42b0-132">Voce</span><span class="sxs-lookup"><span data-stu-id="a42b0-132">Entry</span></span> | <span data-ttu-id="a42b0-133">Valore</span><span class="sxs-lookup"><span data-stu-id="a42b0-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="a42b0-134">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="a42b0-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="a42b0-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a42b0-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="a42b0-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="a42b0-136">System-Only</span></span>            | <span data-ttu-id="a42b0-137">Falso</span><span class="sxs-lookup"><span data-stu-id="a42b0-137">False</span></span>                                        |
| <span data-ttu-id="a42b0-138">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="a42b0-138">Is-Single-Valued</span></span>       | <span data-ttu-id="a42b0-139">Vero</span><span class="sxs-lookup"><span data-stu-id="a42b0-139">True</span></span>                                         |
| <span data-ttu-id="a42b0-140">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="a42b0-140">Is Indexed</span></span>             | <span data-ttu-id="a42b0-141">Falso</span><span class="sxs-lookup"><span data-stu-id="a42b0-141">False</span></span>                                        |
| <span data-ttu-id="a42b0-142">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="a42b0-142">In Global Catalog</span></span>      | <span data-ttu-id="a42b0-143">Falso</span><span class="sxs-lookup"><span data-stu-id="a42b0-143">False</span></span>                                        |
| <span data-ttu-id="a42b0-144">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="a42b0-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="a42b0-145">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="a42b0-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="a42b0-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a42b0-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="a42b0-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a42b0-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="a42b0-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a42b0-148">Search-Flags</span></span>           | <span data-ttu-id="a42b0-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a42b0-149">0x00000000</span></span>                                   |
| <span data-ttu-id="a42b0-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a42b0-150">System-Flags</span></span>           | <span data-ttu-id="a42b0-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a42b0-151">0x00000010</span></span>                                   |
| <span data-ttu-id="a42b0-152">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="a42b0-152">Classes used in</span></span>        | [<span data-ttu-id="a42b0-153">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="a42b0-153">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a42b0-154">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a42b0-154">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a42b0-155">Voce</span><span class="sxs-lookup"><span data-stu-id="a42b0-155">Entry</span></span> | <span data-ttu-id="a42b0-156">Valore</span><span class="sxs-lookup"><span data-stu-id="a42b0-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="a42b0-157">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="a42b0-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="a42b0-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a42b0-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="a42b0-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="a42b0-159">System-Only</span></span>            | <span data-ttu-id="a42b0-160">Falso</span><span class="sxs-lookup"><span data-stu-id="a42b0-160">False</span></span>                                        |
| <span data-ttu-id="a42b0-161">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="a42b0-161">Is-Single-Valued</span></span>       | <span data-ttu-id="a42b0-162">Vero</span><span class="sxs-lookup"><span data-stu-id="a42b0-162">True</span></span>                                         |
| <span data-ttu-id="a42b0-163">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="a42b0-163">Is Indexed</span></span>             | <span data-ttu-id="a42b0-164">Falso</span><span class="sxs-lookup"><span data-stu-id="a42b0-164">False</span></span>                                        |
| <span data-ttu-id="a42b0-165">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="a42b0-165">In Global Catalog</span></span>      | <span data-ttu-id="a42b0-166">Falso</span><span class="sxs-lookup"><span data-stu-id="a42b0-166">False</span></span>                                        |
| <span data-ttu-id="a42b0-167">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="a42b0-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="a42b0-168">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="a42b0-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="a42b0-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a42b0-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="a42b0-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a42b0-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="a42b0-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a42b0-171">Search-Flags</span></span>           | <span data-ttu-id="a42b0-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a42b0-172">0x00000000</span></span>                                   |
| <span data-ttu-id="a42b0-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a42b0-173">System-Flags</span></span>           | <span data-ttu-id="a42b0-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a42b0-174">0x00000010</span></span>                                   |
| <span data-ttu-id="a42b0-175">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="a42b0-175">Classes used in</span></span>        | [<span data-ttu-id="a42b0-176">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="a42b0-176">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a42b0-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a42b0-177">Windows Server 2008</span></span>



| <span data-ttu-id="a42b0-178">Voce</span><span class="sxs-lookup"><span data-stu-id="a42b0-178">Entry</span></span> | <span data-ttu-id="a42b0-179">Valore</span><span class="sxs-lookup"><span data-stu-id="a42b0-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="a42b0-180">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="a42b0-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="a42b0-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a42b0-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="a42b0-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="a42b0-182">System-Only</span></span>            | <span data-ttu-id="a42b0-183">Falso</span><span class="sxs-lookup"><span data-stu-id="a42b0-183">False</span></span>                                        |
| <span data-ttu-id="a42b0-184">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="a42b0-184">Is-Single-Valued</span></span>       | <span data-ttu-id="a42b0-185">Vero</span><span class="sxs-lookup"><span data-stu-id="a42b0-185">True</span></span>                                         |
| <span data-ttu-id="a42b0-186">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="a42b0-186">Is Indexed</span></span>             | <span data-ttu-id="a42b0-187">Falso</span><span class="sxs-lookup"><span data-stu-id="a42b0-187">False</span></span>                                        |
| <span data-ttu-id="a42b0-188">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="a42b0-188">In Global Catalog</span></span>      | <span data-ttu-id="a42b0-189">Falso</span><span class="sxs-lookup"><span data-stu-id="a42b0-189">False</span></span>                                        |
| <span data-ttu-id="a42b0-190">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="a42b0-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="a42b0-191">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="a42b0-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="a42b0-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a42b0-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="a42b0-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a42b0-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="a42b0-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a42b0-194">Search-Flags</span></span>           | <span data-ttu-id="a42b0-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a42b0-195">0x00000000</span></span>                                   |
| <span data-ttu-id="a42b0-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a42b0-196">System-Flags</span></span>           | <span data-ttu-id="a42b0-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a42b0-197">0x00000010</span></span>                                   |
| <span data-ttu-id="a42b0-198">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="a42b0-198">Classes used in</span></span>        | [<span data-ttu-id="a42b0-199">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="a42b0-199">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a42b0-200">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a42b0-200">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a42b0-201">Voce</span><span class="sxs-lookup"><span data-stu-id="a42b0-201">Entry</span></span> | <span data-ttu-id="a42b0-202">Valore</span><span class="sxs-lookup"><span data-stu-id="a42b0-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="a42b0-203">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="a42b0-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="a42b0-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a42b0-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="a42b0-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="a42b0-205">System-Only</span></span>            | <span data-ttu-id="a42b0-206">Falso</span><span class="sxs-lookup"><span data-stu-id="a42b0-206">False</span></span>                                        |
| <span data-ttu-id="a42b0-207">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="a42b0-207">Is-Single-Valued</span></span>       | <span data-ttu-id="a42b0-208">Vero</span><span class="sxs-lookup"><span data-stu-id="a42b0-208">True</span></span>                                         |
| <span data-ttu-id="a42b0-209">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="a42b0-209">Is Indexed</span></span>             | <span data-ttu-id="a42b0-210">Falso</span><span class="sxs-lookup"><span data-stu-id="a42b0-210">False</span></span>                                        |
| <span data-ttu-id="a42b0-211">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="a42b0-211">In Global Catalog</span></span>      | <span data-ttu-id="a42b0-212">Falso</span><span class="sxs-lookup"><span data-stu-id="a42b0-212">False</span></span>                                        |
| <span data-ttu-id="a42b0-213">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="a42b0-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="a42b0-214">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="a42b0-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="a42b0-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a42b0-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="a42b0-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a42b0-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="a42b0-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a42b0-217">Search-Flags</span></span>           | <span data-ttu-id="a42b0-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a42b0-218">0x00000000</span></span>                                   |
| <span data-ttu-id="a42b0-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a42b0-219">System-Flags</span></span>           | <span data-ttu-id="a42b0-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a42b0-220">0x00000010</span></span>                                   |
| <span data-ttu-id="a42b0-221">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="a42b0-221">Classes used in</span></span>        | [<span data-ttu-id="a42b0-222">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="a42b0-222">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a42b0-223">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a42b0-223">Windows Server 2012</span></span>



| <span data-ttu-id="a42b0-224">Voce</span><span class="sxs-lookup"><span data-stu-id="a42b0-224">Entry</span></span> | <span data-ttu-id="a42b0-225">Valore</span><span class="sxs-lookup"><span data-stu-id="a42b0-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="a42b0-226">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="a42b0-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="a42b0-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a42b0-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="a42b0-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="a42b0-228">System-Only</span></span>            | <span data-ttu-id="a42b0-229">Falso</span><span class="sxs-lookup"><span data-stu-id="a42b0-229">False</span></span>                                        |
| <span data-ttu-id="a42b0-230">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="a42b0-230">Is-Single-Valued</span></span>       | <span data-ttu-id="a42b0-231">Vero</span><span class="sxs-lookup"><span data-stu-id="a42b0-231">True</span></span>                                         |
| <span data-ttu-id="a42b0-232">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="a42b0-232">Is Indexed</span></span>             | <span data-ttu-id="a42b0-233">Falso</span><span class="sxs-lookup"><span data-stu-id="a42b0-233">False</span></span>                                        |
| <span data-ttu-id="a42b0-234">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="a42b0-234">In Global Catalog</span></span>      | <span data-ttu-id="a42b0-235">Falso</span><span class="sxs-lookup"><span data-stu-id="a42b0-235">False</span></span>                                        |
| <span data-ttu-id="a42b0-236">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="a42b0-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="a42b0-237">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="a42b0-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="a42b0-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a42b0-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="a42b0-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a42b0-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="a42b0-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a42b0-240">Search-Flags</span></span>           | <span data-ttu-id="a42b0-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a42b0-241">0x00000000</span></span>                                   |
| <span data-ttu-id="a42b0-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a42b0-242">System-Flags</span></span>           | <span data-ttu-id="a42b0-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a42b0-243">0x00000010</span></span>                                   |
| <span data-ttu-id="a42b0-244">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="a42b0-244">Classes used in</span></span>        | [<span data-ttu-id="a42b0-245">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="a42b0-245">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



 

 





