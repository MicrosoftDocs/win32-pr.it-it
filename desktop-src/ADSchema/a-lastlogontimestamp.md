---
title: Attributo Last-Logon-timestamp
description: Indica l'ora dell'ultimo accesso dell'utente al dominio.
ms.assetid: 6c94bccb-1e0a-421c-a00c-5f6e6389690f
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo Last-Logon-timestamp
- Schema AD dell'attributo lastLogonTimestamp
topic_type:
- apiref
api_name:
- Last-Logon-Timestamp
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a6d7668891d008e1b16b7dc148462498e9210b4
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104122143"
---
# <a name="last-logon-timestamp-attribute"></a><span data-ttu-id="6b8be-105">Attributo Last-Logon-timestamp</span><span class="sxs-lookup"><span data-stu-id="6b8be-105">Last-Logon-Timestamp attribute</span></span>

<span data-ttu-id="6b8be-106">Indica l'ora dell'ultimo accesso dell'utente al dominio.</span><span class="sxs-lookup"><span data-stu-id="6b8be-106">This is the time that the user last logged into the domain.</span></span> <span data-ttu-id="6b8be-107">Questo valore viene archiviato come intero grande che rappresenta il numero di intervalli di 100-nanosecondi a partire dal 1 ° gennaio 1601 (UTC).</span><span class="sxs-lookup"><span data-stu-id="6b8be-107">This value is stored as a large integer that represents the number of 100-nanosecond intervals since January 1, 1601 (UTC).</span></span> <span data-ttu-id="6b8be-108">Ogni volta che un utente esegue l'accesso, il valore di questo attributo viene letto dal controller di dominio.</span><span class="sxs-lookup"><span data-stu-id="6b8be-108">Whenever a user logs on, the value of this attribute is read from the DC.</span></span> <span data-ttu-id="6b8be-109">Se il valore è precedente \[ `current_time - msDS-LogonTimeSyncInterval` \] , il valore viene aggiornato.</span><span class="sxs-lookup"><span data-stu-id="6b8be-109">If the value is older \[ `current_time - msDS-LogonTimeSyncInterval` \], the value is updated.</span></span> <span data-ttu-id="6b8be-110">L'aggiornamento iniziale dopo la generazione del livello di funzionalità del dominio viene calcolato come 14 giorni meno la percentuale casuale di 5 giorni.</span><span class="sxs-lookup"><span data-stu-id="6b8be-110">The initial update after the raise of the domain functional level is calculated as 14 days minus random percentage of 5 days.</span></span>



| <span data-ttu-id="6b8be-111">Voce</span><span class="sxs-lookup"><span data-stu-id="6b8be-111">Entry</span></span> | <span data-ttu-id="6b8be-112">Valore</span><span class="sxs-lookup"><span data-stu-id="6b8be-112">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b8be-113">CN</span><span class="sxs-lookup"><span data-stu-id="6b8be-113">CN</span></span>                | <span data-ttu-id="6b8be-114">Ultimo accesso-timestamp</span><span class="sxs-lookup"><span data-stu-id="6b8be-114">Last-Logon-Timestamp</span></span>                                                                                                   |
| <span data-ttu-id="6b8be-115">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="6b8be-115">Ldap-Display-Name</span></span> | <span data-ttu-id="6b8be-116">lastLogonTimestamp</span><span class="sxs-lookup"><span data-stu-id="6b8be-116">lastLogonTimestamp</span></span>                                                                                                     |
| <span data-ttu-id="6b8be-117">Dimensione</span><span class="sxs-lookup"><span data-stu-id="6b8be-117">Size</span></span>              | \-                                                                                                                     |
| <span data-ttu-id="6b8be-118">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="6b8be-118">Update Privilege</span></span>  | <span data-ttu-id="6b8be-119">Questo valore viene impostato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="6b8be-119">This value is set by the system.</span></span>                                                                                       |
| <span data-ttu-id="6b8be-120">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="6b8be-120">Update Frequency</span></span>  | <span data-ttu-id="6b8be-121">Quando l'utente esegue l'accesso e se questo valore è precedente all'ora corrente meno il valore di msDS-LogonTimeSyncInterval.</span><span class="sxs-lookup"><span data-stu-id="6b8be-121">When the user logs on, and if this value is older than the current time minus the value of msDS-LogonTimeSyncInterval.</span></span> |
| <span data-ttu-id="6b8be-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="6b8be-122">Attribute-Id</span></span>      | <span data-ttu-id="6b8be-123">1.2.840.113556.1.4.1696</span><span class="sxs-lookup"><span data-stu-id="6b8be-123">1.2.840.113556.1.4.1696</span></span>                                                                                                |
| <span data-ttu-id="6b8be-124">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="6b8be-124">System-Id-Guid</span></span>    | <span data-ttu-id="6b8be-125">c0e20a04-0e5a-4ff3-9482-5efeaecd7060</span><span class="sxs-lookup"><span data-stu-id="6b8be-125">c0e20a04-0e5a-4ff3-9482-5efeaecd7060</span></span>                                                                                   |
| <span data-ttu-id="6b8be-126">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6b8be-126">Syntax</span></span>            | [<span data-ttu-id="6b8be-127">**Interval**</span><span class="sxs-lookup"><span data-stu-id="6b8be-127">**Interval**</span></span>](s-interval.md)                                                                                         |



## <a name="implementations"></a><span data-ttu-id="6b8be-128">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="6b8be-128">Implementations</span></span>

-   [<span data-ttu-id="6b8be-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="6b8be-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="6b8be-130">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="6b8be-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="6b8be-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="6b8be-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="6b8be-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="6b8be-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="6b8be-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="6b8be-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="6b8be-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="6b8be-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="6b8be-135">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6b8be-135">Windows Server 2003</span></span>



| <span data-ttu-id="6b8be-136">Voce</span><span class="sxs-lookup"><span data-stu-id="6b8be-136">Entry</span></span> | <span data-ttu-id="6b8be-137">Valore</span><span class="sxs-lookup"><span data-stu-id="6b8be-137">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="6b8be-138">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="6b8be-138">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="6b8be-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6b8be-139">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="6b8be-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="6b8be-140">System-Only</span></span>            | <span data-ttu-id="6b8be-141">Falso</span><span class="sxs-lookup"><span data-stu-id="6b8be-141">False</span></span>                             |
| <span data-ttu-id="6b8be-142">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="6b8be-142">Is-Single-Valued</span></span>       | <span data-ttu-id="6b8be-143">Vero</span><span class="sxs-lookup"><span data-stu-id="6b8be-143">True</span></span>                              |
| <span data-ttu-id="6b8be-144">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="6b8be-144">Is Indexed</span></span>             | <span data-ttu-id="6b8be-145">Falso</span><span class="sxs-lookup"><span data-stu-id="6b8be-145">False</span></span>                             |
| <span data-ttu-id="6b8be-146">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="6b8be-146">In Global Catalog</span></span>      | <span data-ttu-id="6b8be-147">Falso</span><span class="sxs-lookup"><span data-stu-id="6b8be-147">False</span></span>                             |
| <span data-ttu-id="6b8be-148">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="6b8be-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="6b8be-149">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="6b8be-149">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="6b8be-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6b8be-150">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="6b8be-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6b8be-151">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="6b8be-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6b8be-152">Search-Flags</span></span>           | <span data-ttu-id="6b8be-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6b8be-153">0x00000000</span></span>                        |
| <span data-ttu-id="6b8be-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6b8be-154">System-Flags</span></span>           | <span data-ttu-id="6b8be-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6b8be-155">0x00000010</span></span>                        |
| <span data-ttu-id="6b8be-156">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="6b8be-156">Classes used in</span></span>        | [<span data-ttu-id="6b8be-157">**Utente**</span><span class="sxs-lookup"><span data-stu-id="6b8be-157">**User**</span></span>](c-user.md)<br/> |



## <a name="adam"></a><span data-ttu-id="6b8be-158">ADAM</span><span class="sxs-lookup"><span data-stu-id="6b8be-158">ADAM</span></span>



| <span data-ttu-id="6b8be-159">Voce</span><span class="sxs-lookup"><span data-stu-id="6b8be-159">Entry</span></span> | <span data-ttu-id="6b8be-160">Valore</span><span class="sxs-lookup"><span data-stu-id="6b8be-160">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="6b8be-161">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="6b8be-161">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="6b8be-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6b8be-162">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="6b8be-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="6b8be-163">System-Only</span></span>            | <span data-ttu-id="6b8be-164">Vero</span><span class="sxs-lookup"><span data-stu-id="6b8be-164">True</span></span>                                                              |
| <span data-ttu-id="6b8be-165">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="6b8be-165">Is-Single-Valued</span></span>       | <span data-ttu-id="6b8be-166">Vero</span><span class="sxs-lookup"><span data-stu-id="6b8be-166">True</span></span>                                                              |
| <span data-ttu-id="6b8be-167">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="6b8be-167">Is Indexed</span></span>             | <span data-ttu-id="6b8be-168">Falso</span><span class="sxs-lookup"><span data-stu-id="6b8be-168">False</span></span>                                                             |
| <span data-ttu-id="6b8be-169">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="6b8be-169">In Global Catalog</span></span>      | <span data-ttu-id="6b8be-170">Falso</span><span class="sxs-lookup"><span data-stu-id="6b8be-170">False</span></span>                                                             |
| <span data-ttu-id="6b8be-171">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="6b8be-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="6b8be-172">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="6b8be-172">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="6b8be-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6b8be-173">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="6b8be-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6b8be-174">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="6b8be-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6b8be-175">Search-Flags</span></span>           | <span data-ttu-id="6b8be-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6b8be-176">0x00000000</span></span>                                                        |
| <span data-ttu-id="6b8be-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6b8be-177">System-Flags</span></span>           | <span data-ttu-id="6b8be-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6b8be-178">0x00000010</span></span>                                                        |
| <span data-ttu-id="6b8be-179">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="6b8be-179">Classes used in</span></span>        | [<span data-ttu-id="6b8be-180">**ms-DS-associabile-oggetto**</span><span class="sxs-lookup"><span data-stu-id="6b8be-180">**ms-DS-Bindable-Object**</span></span>](c-msds-bindableobject.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="6b8be-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="6b8be-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="6b8be-182">Voce</span><span class="sxs-lookup"><span data-stu-id="6b8be-182">Entry</span></span> | <span data-ttu-id="6b8be-183">Valore</span><span class="sxs-lookup"><span data-stu-id="6b8be-183">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="6b8be-184">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="6b8be-184">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="6b8be-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6b8be-185">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="6b8be-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="6b8be-186">System-Only</span></span>            | <span data-ttu-id="6b8be-187">Falso</span><span class="sxs-lookup"><span data-stu-id="6b8be-187">False</span></span>                             |
| <span data-ttu-id="6b8be-188">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="6b8be-188">Is-Single-Valued</span></span>       | <span data-ttu-id="6b8be-189">Vero</span><span class="sxs-lookup"><span data-stu-id="6b8be-189">True</span></span>                              |
| <span data-ttu-id="6b8be-190">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="6b8be-190">Is Indexed</span></span>             | <span data-ttu-id="6b8be-191">Falso</span><span class="sxs-lookup"><span data-stu-id="6b8be-191">False</span></span>                             |
| <span data-ttu-id="6b8be-192">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="6b8be-192">In Global Catalog</span></span>      | <span data-ttu-id="6b8be-193">Falso</span><span class="sxs-lookup"><span data-stu-id="6b8be-193">False</span></span>                             |
| <span data-ttu-id="6b8be-194">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="6b8be-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="6b8be-195">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="6b8be-195">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="6b8be-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6b8be-196">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="6b8be-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6b8be-197">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="6b8be-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6b8be-198">Search-Flags</span></span>           | <span data-ttu-id="6b8be-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6b8be-199">0x00000000</span></span>                        |
| <span data-ttu-id="6b8be-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6b8be-200">System-Flags</span></span>           | <span data-ttu-id="6b8be-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6b8be-201">0x00000010</span></span>                        |
| <span data-ttu-id="6b8be-202">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="6b8be-202">Classes used in</span></span>        | [<span data-ttu-id="6b8be-203">**Utente**</span><span class="sxs-lookup"><span data-stu-id="6b8be-203">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="6b8be-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6b8be-204">Windows Server 2008</span></span>



| <span data-ttu-id="6b8be-205">Voce</span><span class="sxs-lookup"><span data-stu-id="6b8be-205">Entry</span></span> | <span data-ttu-id="6b8be-206">Valore</span><span class="sxs-lookup"><span data-stu-id="6b8be-206">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="6b8be-207">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="6b8be-207">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="6b8be-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6b8be-208">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="6b8be-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="6b8be-209">System-Only</span></span>            | <span data-ttu-id="6b8be-210">Falso</span><span class="sxs-lookup"><span data-stu-id="6b8be-210">False</span></span>                             |
| <span data-ttu-id="6b8be-211">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="6b8be-211">Is-Single-Valued</span></span>       | <span data-ttu-id="6b8be-212">Vero</span><span class="sxs-lookup"><span data-stu-id="6b8be-212">True</span></span>                              |
| <span data-ttu-id="6b8be-213">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="6b8be-213">Is Indexed</span></span>             | <span data-ttu-id="6b8be-214">Vero</span><span class="sxs-lookup"><span data-stu-id="6b8be-214">True</span></span>                              |
| <span data-ttu-id="6b8be-215">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="6b8be-215">In Global Catalog</span></span>      | <span data-ttu-id="6b8be-216">Vero</span><span class="sxs-lookup"><span data-stu-id="6b8be-216">True</span></span>                              |
| <span data-ttu-id="6b8be-217">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="6b8be-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="6b8be-218">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="6b8be-218">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="6b8be-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6b8be-219">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="6b8be-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6b8be-220">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="6b8be-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6b8be-221">Search-Flags</span></span>           | <span data-ttu-id="6b8be-222">0x00000001</span><span class="sxs-lookup"><span data-stu-id="6b8be-222">0x00000001</span></span>                        |
| <span data-ttu-id="6b8be-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6b8be-223">System-Flags</span></span>           | <span data-ttu-id="6b8be-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6b8be-224">0x00000010</span></span>                        |
| <span data-ttu-id="6b8be-225">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="6b8be-225">Classes used in</span></span>        | [<span data-ttu-id="6b8be-226">**Utente**</span><span class="sxs-lookup"><span data-stu-id="6b8be-226">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="6b8be-227">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6b8be-227">Windows Server 2008 R2</span></span>



| <span data-ttu-id="6b8be-228">Voce</span><span class="sxs-lookup"><span data-stu-id="6b8be-228">Entry</span></span> | <span data-ttu-id="6b8be-229">Valore</span><span class="sxs-lookup"><span data-stu-id="6b8be-229">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="6b8be-230">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="6b8be-230">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="6b8be-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6b8be-231">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="6b8be-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="6b8be-232">System-Only</span></span>            | <span data-ttu-id="6b8be-233">Falso</span><span class="sxs-lookup"><span data-stu-id="6b8be-233">False</span></span>                             |
| <span data-ttu-id="6b8be-234">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="6b8be-234">Is-Single-Valued</span></span>       | <span data-ttu-id="6b8be-235">Vero</span><span class="sxs-lookup"><span data-stu-id="6b8be-235">True</span></span>                              |
| <span data-ttu-id="6b8be-236">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="6b8be-236">Is Indexed</span></span>             | <span data-ttu-id="6b8be-237">Vero</span><span class="sxs-lookup"><span data-stu-id="6b8be-237">True</span></span>                              |
| <span data-ttu-id="6b8be-238">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="6b8be-238">In Global Catalog</span></span>      | <span data-ttu-id="6b8be-239">Vero</span><span class="sxs-lookup"><span data-stu-id="6b8be-239">True</span></span>                              |
| <span data-ttu-id="6b8be-240">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="6b8be-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="6b8be-241">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="6b8be-241">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="6b8be-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6b8be-242">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="6b8be-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6b8be-243">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="6b8be-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6b8be-244">Search-Flags</span></span>           | <span data-ttu-id="6b8be-245">0x00000001</span><span class="sxs-lookup"><span data-stu-id="6b8be-245">0x00000001</span></span>                        |
| <span data-ttu-id="6b8be-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6b8be-246">System-Flags</span></span>           | <span data-ttu-id="6b8be-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6b8be-247">0x00000010</span></span>                        |
| <span data-ttu-id="6b8be-248">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="6b8be-248">Classes used in</span></span>        | [<span data-ttu-id="6b8be-249">**Utente**</span><span class="sxs-lookup"><span data-stu-id="6b8be-249">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="6b8be-250">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6b8be-250">Windows Server 2012</span></span>



| <span data-ttu-id="6b8be-251">Voce</span><span class="sxs-lookup"><span data-stu-id="6b8be-251">Entry</span></span> | <span data-ttu-id="6b8be-252">Valore</span><span class="sxs-lookup"><span data-stu-id="6b8be-252">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="6b8be-253">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="6b8be-253">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="6b8be-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6b8be-254">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="6b8be-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="6b8be-255">System-Only</span></span>            | <span data-ttu-id="6b8be-256">Falso</span><span class="sxs-lookup"><span data-stu-id="6b8be-256">False</span></span>                             |
| <span data-ttu-id="6b8be-257">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="6b8be-257">Is-Single-Valued</span></span>       | <span data-ttu-id="6b8be-258">Vero</span><span class="sxs-lookup"><span data-stu-id="6b8be-258">True</span></span>                              |
| <span data-ttu-id="6b8be-259">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="6b8be-259">Is Indexed</span></span>             | <span data-ttu-id="6b8be-260">Vero</span><span class="sxs-lookup"><span data-stu-id="6b8be-260">True</span></span>                              |
| <span data-ttu-id="6b8be-261">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="6b8be-261">In Global Catalog</span></span>      | <span data-ttu-id="6b8be-262">Vero</span><span class="sxs-lookup"><span data-stu-id="6b8be-262">True</span></span>                              |
| <span data-ttu-id="6b8be-263">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="6b8be-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="6b8be-264">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="6b8be-264">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="6b8be-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6b8be-265">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="6b8be-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6b8be-266">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="6b8be-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6b8be-267">Search-Flags</span></span>           | <span data-ttu-id="6b8be-268">0x00000001</span><span class="sxs-lookup"><span data-stu-id="6b8be-268">0x00000001</span></span>                        |
| <span data-ttu-id="6b8be-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6b8be-269">System-Flags</span></span>           | <span data-ttu-id="6b8be-270">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6b8be-270">0x00000010</span></span>                        |
| <span data-ttu-id="6b8be-271">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="6b8be-271">Classes used in</span></span>        | [<span data-ttu-id="6b8be-272">**Utente**</span><span class="sxs-lookup"><span data-stu-id="6b8be-272">**User**</span></span>](c-user.md)<br/> |



 

 





