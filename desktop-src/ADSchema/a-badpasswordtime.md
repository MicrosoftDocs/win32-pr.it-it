---
title: Attributo password-Time non valido
description: Data e ora dell'ultima esecuzione di un tentativo di accesso a questo account con una password non valida.
ms.assetid: 8e8c5b73-b42d-4a62-89af-c0ff2fe106d8
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo time-password non valido
- Schema AD dell'attributo badPasswordTime
topic_type:
- apiref
api_name:
- Bad-Password-Time
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47df09d0ff2d82a9180c43721aa09e5363884e24
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104480472"
---
# <a name="bad-password-time-attribute"></a><span data-ttu-id="cee29-105">Attributo password-Time non valido</span><span class="sxs-lookup"><span data-stu-id="cee29-105">Bad-Password-Time attribute</span></span>

<span data-ttu-id="cee29-106">Data e ora dell'ultima esecuzione di un tentativo di accesso a questo account con una password non valida.</span><span class="sxs-lookup"><span data-stu-id="cee29-106">The last time and date that an attempt to log on to this account was made with a password that is not valid.</span></span> <span data-ttu-id="cee29-107">Questo valore viene archiviato come intero grande che rappresenta il numero di intervalli di 100-nanosecondi a partire dal 1 ° gennaio 1601 (UTC).</span><span class="sxs-lookup"><span data-stu-id="cee29-107">This value is stored as a large integer that represents the number of 100-nanosecond intervals since January 1, 1601 (UTC).</span></span> <span data-ttu-id="cee29-108">Un valore pari a zero indica che l'ultima volta che è stata usata una password non corretta è sconosciuta.</span><span class="sxs-lookup"><span data-stu-id="cee29-108">A value of zero means that the last time a incorrect password was used is unknown.</span></span>



| <span data-ttu-id="cee29-109">Voce</span><span class="sxs-lookup"><span data-stu-id="cee29-109">Entry</span></span> | <span data-ttu-id="cee29-110">Valore</span><span class="sxs-lookup"><span data-stu-id="cee29-110">Value</span></span> |
|-------------------|-------------------------------------------|
| <span data-ttu-id="cee29-111">CN</span><span class="sxs-lookup"><span data-stu-id="cee29-111">CN</span></span>                | <span data-ttu-id="cee29-112">Password-ora non valida</span><span class="sxs-lookup"><span data-stu-id="cee29-112">Bad-Password-Time</span></span>                         |
| <span data-ttu-id="cee29-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="cee29-113">Ldap-Display-Name</span></span> | <span data-ttu-id="cee29-114">badPasswordTime</span><span class="sxs-lookup"><span data-stu-id="cee29-114">badPasswordTime</span></span>                           |
| <span data-ttu-id="cee29-115">Dimensione</span><span class="sxs-lookup"><span data-stu-id="cee29-115">Size</span></span>              | <span data-ttu-id="cee29-116">8 byte</span><span class="sxs-lookup"><span data-stu-id="cee29-116">8 bytes</span></span>                                   |
| <span data-ttu-id="cee29-117">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="cee29-117">Update Privilege</span></span>  | <span data-ttu-id="cee29-118">Questo valore viene impostato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="cee29-118">This value is set by the system.</span></span>          |
| <span data-ttu-id="cee29-119">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="cee29-119">Update Frequency</span></span>  | <span data-ttu-id="cee29-120">Ogni volta che l'utente immette una password errata.</span><span class="sxs-lookup"><span data-stu-id="cee29-120">Each time the user enters a bad password.</span></span> |
| <span data-ttu-id="cee29-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="cee29-121">Attribute-Id</span></span>      | <span data-ttu-id="cee29-122">1.2.840.113556.1.4.49</span><span class="sxs-lookup"><span data-stu-id="cee29-122">1.2.840.113556.1.4.49</span></span>                     |
| <span data-ttu-id="cee29-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="cee29-123">System-Id-Guid</span></span>    | <span data-ttu-id="cee29-124">bf96792d-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="cee29-124">bf96792d-0de6-11d0-a285-00aa003049e2</span></span>      |
| <span data-ttu-id="cee29-125">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cee29-125">Syntax</span></span>            | [<span data-ttu-id="cee29-126">**Interval**</span><span class="sxs-lookup"><span data-stu-id="cee29-126">**Interval**</span></span>](s-interval.md)            |



## <a name="implementations"></a><span data-ttu-id="cee29-127">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="cee29-127">Implementations</span></span>

-   [<span data-ttu-id="cee29-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="cee29-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="cee29-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="cee29-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="cee29-130">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="cee29-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="cee29-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="cee29-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="cee29-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="cee29-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="cee29-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="cee29-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="cee29-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="cee29-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="cee29-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="cee29-135">Windows 2000 Server</span></span>



| <span data-ttu-id="cee29-136">Voce</span><span class="sxs-lookup"><span data-stu-id="cee29-136">Entry</span></span> | <span data-ttu-id="cee29-137">Valore</span><span class="sxs-lookup"><span data-stu-id="cee29-137">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="cee29-138">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="cee29-138">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="cee29-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cee29-139">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="cee29-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="cee29-140">System-Only</span></span>            | <span data-ttu-id="cee29-141">Falso</span><span class="sxs-lookup"><span data-stu-id="cee29-141">False</span></span>                             |
| <span data-ttu-id="cee29-142">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="cee29-142">Is-Single-Valued</span></span>       | <span data-ttu-id="cee29-143">Vero</span><span class="sxs-lookup"><span data-stu-id="cee29-143">True</span></span>                              |
| <span data-ttu-id="cee29-144">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="cee29-144">Is Indexed</span></span>             | <span data-ttu-id="cee29-145">Falso</span><span class="sxs-lookup"><span data-stu-id="cee29-145">False</span></span>                             |
| <span data-ttu-id="cee29-146">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="cee29-146">In Global Catalog</span></span>      | <span data-ttu-id="cee29-147">Falso</span><span class="sxs-lookup"><span data-stu-id="cee29-147">False</span></span>                             |
| <span data-ttu-id="cee29-148">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="cee29-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="cee29-149">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="cee29-149">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="cee29-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cee29-150">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="cee29-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cee29-151">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="cee29-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cee29-152">Search-Flags</span></span>           | <span data-ttu-id="cee29-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cee29-153">0x00000000</span></span>                        |
| <span data-ttu-id="cee29-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cee29-154">System-Flags</span></span>           | <span data-ttu-id="cee29-155">0x00000011</span><span class="sxs-lookup"><span data-stu-id="cee29-155">0x00000011</span></span>                        |
| <span data-ttu-id="cee29-156">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="cee29-156">Classes used in</span></span>        | [<span data-ttu-id="cee29-157">**Utente**</span><span class="sxs-lookup"><span data-stu-id="cee29-157">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="cee29-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="cee29-158">Windows Server 2003</span></span>



| <span data-ttu-id="cee29-159">Voce</span><span class="sxs-lookup"><span data-stu-id="cee29-159">Entry</span></span> | <span data-ttu-id="cee29-160">Valore</span><span class="sxs-lookup"><span data-stu-id="cee29-160">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="cee29-161">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="cee29-161">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="cee29-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cee29-162">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="cee29-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="cee29-163">System-Only</span></span>            | <span data-ttu-id="cee29-164">Falso</span><span class="sxs-lookup"><span data-stu-id="cee29-164">False</span></span>                             |
| <span data-ttu-id="cee29-165">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="cee29-165">Is-Single-Valued</span></span>       | <span data-ttu-id="cee29-166">Vero</span><span class="sxs-lookup"><span data-stu-id="cee29-166">True</span></span>                              |
| <span data-ttu-id="cee29-167">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="cee29-167">Is Indexed</span></span>             | <span data-ttu-id="cee29-168">Falso</span><span class="sxs-lookup"><span data-stu-id="cee29-168">False</span></span>                             |
| <span data-ttu-id="cee29-169">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="cee29-169">In Global Catalog</span></span>      | <span data-ttu-id="cee29-170">Falso</span><span class="sxs-lookup"><span data-stu-id="cee29-170">False</span></span>                             |
| <span data-ttu-id="cee29-171">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="cee29-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="cee29-172">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="cee29-172">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="cee29-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cee29-173">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="cee29-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cee29-174">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="cee29-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cee29-175">Search-Flags</span></span>           | <span data-ttu-id="cee29-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cee29-176">0x00000000</span></span>                        |
| <span data-ttu-id="cee29-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cee29-177">System-Flags</span></span>           | <span data-ttu-id="cee29-178">0x00000011</span><span class="sxs-lookup"><span data-stu-id="cee29-178">0x00000011</span></span>                        |
| <span data-ttu-id="cee29-179">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="cee29-179">Classes used in</span></span>        | [<span data-ttu-id="cee29-180">**Utente**</span><span class="sxs-lookup"><span data-stu-id="cee29-180">**User**</span></span>](c-user.md)<br/> |



## <a name="adam"></a><span data-ttu-id="cee29-181">ADAM</span><span class="sxs-lookup"><span data-stu-id="cee29-181">ADAM</span></span>



| <span data-ttu-id="cee29-182">Voce</span><span class="sxs-lookup"><span data-stu-id="cee29-182">Entry</span></span> | <span data-ttu-id="cee29-183">Valore</span><span class="sxs-lookup"><span data-stu-id="cee29-183">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="cee29-184">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="cee29-184">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="cee29-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cee29-185">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="cee29-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="cee29-186">System-Only</span></span>            | <span data-ttu-id="cee29-187">Vero</span><span class="sxs-lookup"><span data-stu-id="cee29-187">True</span></span>                                                              |
| <span data-ttu-id="cee29-188">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="cee29-188">Is-Single-Valued</span></span>       | <span data-ttu-id="cee29-189">Vero</span><span class="sxs-lookup"><span data-stu-id="cee29-189">True</span></span>                                                              |
| <span data-ttu-id="cee29-190">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="cee29-190">Is Indexed</span></span>             | <span data-ttu-id="cee29-191">Falso</span><span class="sxs-lookup"><span data-stu-id="cee29-191">False</span></span>                                                             |
| <span data-ttu-id="cee29-192">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="cee29-192">In Global Catalog</span></span>      | <span data-ttu-id="cee29-193">Falso</span><span class="sxs-lookup"><span data-stu-id="cee29-193">False</span></span>                                                             |
| <span data-ttu-id="cee29-194">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="cee29-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="cee29-195">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="cee29-195">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="cee29-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cee29-196">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="cee29-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cee29-197">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="cee29-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cee29-198">Search-Flags</span></span>           | <span data-ttu-id="cee29-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cee29-199">0x00000000</span></span>                                                        |
| <span data-ttu-id="cee29-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cee29-200">System-Flags</span></span>           | <span data-ttu-id="cee29-201">0x00000011</span><span class="sxs-lookup"><span data-stu-id="cee29-201">0x00000011</span></span>                                                        |
| <span data-ttu-id="cee29-202">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="cee29-202">Classes used in</span></span>        | [<span data-ttu-id="cee29-203">**ms-DS-associabile-oggetto**</span><span class="sxs-lookup"><span data-stu-id="cee29-203">**ms-DS-Bindable-Object**</span></span>](c-msds-bindableobject.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="cee29-204">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="cee29-204">Windows Server 2003 R2</span></span>



| <span data-ttu-id="cee29-205">Voce</span><span class="sxs-lookup"><span data-stu-id="cee29-205">Entry</span></span> | <span data-ttu-id="cee29-206">Valore</span><span class="sxs-lookup"><span data-stu-id="cee29-206">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="cee29-207">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="cee29-207">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="cee29-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cee29-208">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="cee29-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="cee29-209">System-Only</span></span>            | <span data-ttu-id="cee29-210">Falso</span><span class="sxs-lookup"><span data-stu-id="cee29-210">False</span></span>                             |
| <span data-ttu-id="cee29-211">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="cee29-211">Is-Single-Valued</span></span>       | <span data-ttu-id="cee29-212">Vero</span><span class="sxs-lookup"><span data-stu-id="cee29-212">True</span></span>                              |
| <span data-ttu-id="cee29-213">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="cee29-213">Is Indexed</span></span>             | <span data-ttu-id="cee29-214">Falso</span><span class="sxs-lookup"><span data-stu-id="cee29-214">False</span></span>                             |
| <span data-ttu-id="cee29-215">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="cee29-215">In Global Catalog</span></span>      | <span data-ttu-id="cee29-216">Falso</span><span class="sxs-lookup"><span data-stu-id="cee29-216">False</span></span>                             |
| <span data-ttu-id="cee29-217">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="cee29-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="cee29-218">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="cee29-218">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="cee29-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cee29-219">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="cee29-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cee29-220">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="cee29-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cee29-221">Search-Flags</span></span>           | <span data-ttu-id="cee29-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cee29-222">0x00000000</span></span>                        |
| <span data-ttu-id="cee29-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cee29-223">System-Flags</span></span>           | <span data-ttu-id="cee29-224">0x00000011</span><span class="sxs-lookup"><span data-stu-id="cee29-224">0x00000011</span></span>                        |
| <span data-ttu-id="cee29-225">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="cee29-225">Classes used in</span></span>        | [<span data-ttu-id="cee29-226">**Utente**</span><span class="sxs-lookup"><span data-stu-id="cee29-226">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="cee29-227">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cee29-227">Windows Server 2008</span></span>



| <span data-ttu-id="cee29-228">Voce</span><span class="sxs-lookup"><span data-stu-id="cee29-228">Entry</span></span> | <span data-ttu-id="cee29-229">Valore</span><span class="sxs-lookup"><span data-stu-id="cee29-229">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="cee29-230">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="cee29-230">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="cee29-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cee29-231">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="cee29-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="cee29-232">System-Only</span></span>            | <span data-ttu-id="cee29-233">Falso</span><span class="sxs-lookup"><span data-stu-id="cee29-233">False</span></span>                             |
| <span data-ttu-id="cee29-234">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="cee29-234">Is-Single-Valued</span></span>       | <span data-ttu-id="cee29-235">Vero</span><span class="sxs-lookup"><span data-stu-id="cee29-235">True</span></span>                              |
| <span data-ttu-id="cee29-236">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="cee29-236">Is Indexed</span></span>             | <span data-ttu-id="cee29-237">Falso</span><span class="sxs-lookup"><span data-stu-id="cee29-237">False</span></span>                             |
| <span data-ttu-id="cee29-238">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="cee29-238">In Global Catalog</span></span>      | <span data-ttu-id="cee29-239">Falso</span><span class="sxs-lookup"><span data-stu-id="cee29-239">False</span></span>                             |
| <span data-ttu-id="cee29-240">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="cee29-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="cee29-241">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="cee29-241">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="cee29-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cee29-242">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="cee29-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cee29-243">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="cee29-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cee29-244">Search-Flags</span></span>           | <span data-ttu-id="cee29-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cee29-245">0x00000000</span></span>                        |
| <span data-ttu-id="cee29-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cee29-246">System-Flags</span></span>           | <span data-ttu-id="cee29-247">0x00000011</span><span class="sxs-lookup"><span data-stu-id="cee29-247">0x00000011</span></span>                        |
| <span data-ttu-id="cee29-248">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="cee29-248">Classes used in</span></span>        | [<span data-ttu-id="cee29-249">**Utente**</span><span class="sxs-lookup"><span data-stu-id="cee29-249">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="cee29-250">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="cee29-250">Windows Server 2008 R2</span></span>



| <span data-ttu-id="cee29-251">Voce</span><span class="sxs-lookup"><span data-stu-id="cee29-251">Entry</span></span> | <span data-ttu-id="cee29-252">Valore</span><span class="sxs-lookup"><span data-stu-id="cee29-252">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="cee29-253">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="cee29-253">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="cee29-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cee29-254">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="cee29-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="cee29-255">System-Only</span></span>            | <span data-ttu-id="cee29-256">Falso</span><span class="sxs-lookup"><span data-stu-id="cee29-256">False</span></span>                             |
| <span data-ttu-id="cee29-257">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="cee29-257">Is-Single-Valued</span></span>       | <span data-ttu-id="cee29-258">Vero</span><span class="sxs-lookup"><span data-stu-id="cee29-258">True</span></span>                              |
| <span data-ttu-id="cee29-259">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="cee29-259">Is Indexed</span></span>             | <span data-ttu-id="cee29-260">Falso</span><span class="sxs-lookup"><span data-stu-id="cee29-260">False</span></span>                             |
| <span data-ttu-id="cee29-261">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="cee29-261">In Global Catalog</span></span>      | <span data-ttu-id="cee29-262">Falso</span><span class="sxs-lookup"><span data-stu-id="cee29-262">False</span></span>                             |
| <span data-ttu-id="cee29-263">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="cee29-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="cee29-264">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="cee29-264">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="cee29-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cee29-265">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="cee29-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cee29-266">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="cee29-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cee29-267">Search-Flags</span></span>           | <span data-ttu-id="cee29-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cee29-268">0x00000000</span></span>                        |
| <span data-ttu-id="cee29-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cee29-269">System-Flags</span></span>           | <span data-ttu-id="cee29-270">0x00000011</span><span class="sxs-lookup"><span data-stu-id="cee29-270">0x00000011</span></span>                        |
| <span data-ttu-id="cee29-271">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="cee29-271">Classes used in</span></span>        | [<span data-ttu-id="cee29-272">**Utente**</span><span class="sxs-lookup"><span data-stu-id="cee29-272">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="cee29-273">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="cee29-273">Windows Server 2012</span></span>



| <span data-ttu-id="cee29-274">Voce</span><span class="sxs-lookup"><span data-stu-id="cee29-274">Entry</span></span> | <span data-ttu-id="cee29-275">Valore</span><span class="sxs-lookup"><span data-stu-id="cee29-275">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="cee29-276">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="cee29-276">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="cee29-277">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cee29-277">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="cee29-278">System-Only</span><span class="sxs-lookup"><span data-stu-id="cee29-278">System-Only</span></span>            | <span data-ttu-id="cee29-279">Falso</span><span class="sxs-lookup"><span data-stu-id="cee29-279">False</span></span>                             |
| <span data-ttu-id="cee29-280">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="cee29-280">Is-Single-Valued</span></span>       | <span data-ttu-id="cee29-281">Vero</span><span class="sxs-lookup"><span data-stu-id="cee29-281">True</span></span>                              |
| <span data-ttu-id="cee29-282">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="cee29-282">Is Indexed</span></span>             | <span data-ttu-id="cee29-283">Falso</span><span class="sxs-lookup"><span data-stu-id="cee29-283">False</span></span>                             |
| <span data-ttu-id="cee29-284">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="cee29-284">In Global Catalog</span></span>      | <span data-ttu-id="cee29-285">Falso</span><span class="sxs-lookup"><span data-stu-id="cee29-285">False</span></span>                             |
| <span data-ttu-id="cee29-286">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="cee29-286">NT-Security-Descriptor</span></span> | <span data-ttu-id="cee29-287">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="cee29-287">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="cee29-288">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cee29-288">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="cee29-289">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cee29-289">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="cee29-290">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cee29-290">Search-Flags</span></span>           | <span data-ttu-id="cee29-291">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cee29-291">0x00000000</span></span>                        |
| <span data-ttu-id="cee29-292">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cee29-292">System-Flags</span></span>           | <span data-ttu-id="cee29-293">0x00000011</span><span class="sxs-lookup"><span data-stu-id="cee29-293">0x00000011</span></span>                        |
| <span data-ttu-id="cee29-294">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="cee29-294">Classes used in</span></span>        | [<span data-ttu-id="cee29-295">**Utente**</span><span class="sxs-lookup"><span data-stu-id="cee29-295">**User**</span></span>](c-user.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="cee29-296">Commenti</span><span class="sxs-lookup"><span data-stu-id="cee29-296">Remarks</span></span>

<span data-ttu-id="cee29-297">La parte alta di questo Integer di grandi dimensioni corrisponde al membro **dwHighDateTime** della struttura [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) e la parte bassa corrisponde al membro **dwLowDateTime** della struttura **FILETIME** .</span><span class="sxs-lookup"><span data-stu-id="cee29-297">The high part of this large integer corresponds to the **dwHighDateTime** member of the [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) structure and the low part corresponds to the **dwLowDateTime** member of the **FILETIME** structure.</span></span>

<span data-ttu-id="cee29-298">Questo attributo non viene replicato e viene mantenuto separatamente in ogni controller di dominio nel dominio.</span><span class="sxs-lookup"><span data-stu-id="cee29-298">This attribute is not replicated and is maintained separately on each domain controller in the domain.</span></span> <span data-ttu-id="cee29-299">Per ottenere un valore accurato per l'ora dell'ultima password errata dell'utente nel dominio, è necessario eseguire una query su ogni controller di dominio nel dominio.</span><span class="sxs-lookup"><span data-stu-id="cee29-299">To get an accurate value for the user's last bad password time in the domain, each domain controller in the domain must be queried.</span></span> <span data-ttu-id="cee29-300">Il valore più grande ottenuto rappresenta l'ora effettiva della password errata.</span><span class="sxs-lookup"><span data-stu-id="cee29-300">The largest value that is obtained represents the true bad password time.</span></span>

 

