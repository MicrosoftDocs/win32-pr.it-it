---
title: MSMQ-Sign-Certificates-MIG (attributo)
description: In modalità mista MSMQ, l'attributo contiene il valore precedente di mSMQSignCertificates. MSMQ supporta la migrazione da MSMQ 1,0 DS a Windows 2000 DS e la modalità mista specifica uno stato in cui alcuni dei servizi di dominio Active Directory non sono stati aggiornati a Windows 2000.
ms.assetid: 0dbc5d97-39e6-4863-a386-541ea2abaadc
ms.tgt_platform: multiple
keywords:
- MSMQ-Sign-Certificates-schema AD dell'attributo MIG
- Schema AD dell'attributo mSMQSignCertificatesMig
topic_type:
- apiref
api_name:
- MSMQ-Sign-Certificates-Mig
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91a1916cf98d15da1bd84603a2305543e899d868
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "106303463"
---
# <a name="msmq-sign-certificates-mig-attribute"></a><span data-ttu-id="78a76-106">MSMQ-Sign-Certificates-MIG (attributo)</span><span class="sxs-lookup"><span data-stu-id="78a76-106">MSMQ-Sign-Certificates-Mig attribute</span></span>

<span data-ttu-id="78a76-107">In modalità mista MSMQ, l'attributo contiene il valore precedente di mSMQSignCertificates.</span><span class="sxs-lookup"><span data-stu-id="78a76-107">In MSMQ mixed-mode, the attribute contains the previous value of mSMQSignCertificates.</span></span> <span data-ttu-id="78a76-108">MSMQ supporta la migrazione da MSMQ 1,0 DS a Windows 2000 DS e la modalità mista specifica uno stato in cui alcuni dei servizi di dominio Active Directory non sono stati aggiornati a Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="78a76-108">MSMQ supports migration from the MSMQ 1.0 DS to the Windows 2000 DS, and mixed mode specifies a state in which some of the DS severs were not upgraded to Windows 2000.</span></span>



| <span data-ttu-id="78a76-109">Voce</span><span class="sxs-lookup"><span data-stu-id="78a76-109">Entry</span></span> | <span data-ttu-id="78a76-110">Valore</span><span class="sxs-lookup"><span data-stu-id="78a76-110">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="78a76-111">CN</span><span class="sxs-lookup"><span data-stu-id="78a76-111">CN</span></span>                | <span data-ttu-id="78a76-112">MSMQ-Sign-Certificates-MIG</span><span class="sxs-lookup"><span data-stu-id="78a76-112">MSMQ-Sign-Certificates-Mig</span></span>                            |
| <span data-ttu-id="78a76-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="78a76-113">Ldap-Display-Name</span></span> | <span data-ttu-id="78a76-114">mSMQSignCertificatesMig</span><span class="sxs-lookup"><span data-stu-id="78a76-114">mSMQSignCertificatesMig</span></span>                               |
| <span data-ttu-id="78a76-115">Dimensione</span><span class="sxs-lookup"><span data-stu-id="78a76-115">Size</span></span>              | \-                                                    |
| <span data-ttu-id="78a76-116">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="78a76-116">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="78a76-117">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="78a76-117">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="78a76-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="78a76-118">Attribute-Id</span></span>      | <span data-ttu-id="78a76-119">1.2.840.113556.1.4.967</span><span class="sxs-lookup"><span data-stu-id="78a76-119">1.2.840.113556.1.4.967</span></span>                                |
| <span data-ttu-id="78a76-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="78a76-120">System-Id-Guid</span></span>    | <span data-ttu-id="78a76-121">3881b8ea-da3b-11d1-90a5-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="78a76-121">3881b8ea-da3b-11d1-90a5-00c04fd91ab1</span></span>                  |
| <span data-ttu-id="78a76-122">Sintassi</span><span class="sxs-lookup"><span data-stu-id="78a76-122">Syntax</span></span>            | [<span data-ttu-id="78a76-123">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="78a76-123">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="78a76-124">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="78a76-124">Implementations</span></span>

-   [<span data-ttu-id="78a76-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="78a76-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="78a76-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="78a76-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="78a76-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="78a76-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="78a76-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="78a76-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="78a76-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="78a76-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="78a76-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="78a76-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="78a76-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="78a76-131">Windows 2000 Server</span></span>



| <span data-ttu-id="78a76-132">Voce</span><span class="sxs-lookup"><span data-stu-id="78a76-132">Entry</span></span> | <span data-ttu-id="78a76-133">Valore</span><span class="sxs-lookup"><span data-stu-id="78a76-133">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="78a76-134">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="78a76-134">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="78a76-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="78a76-135">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="78a76-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="78a76-136">System-Only</span></span>            | <span data-ttu-id="78a76-137">Falso</span><span class="sxs-lookup"><span data-stu-id="78a76-137">False</span></span>                                                                                         |
| <span data-ttu-id="78a76-138">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="78a76-138">Is-Single-Valued</span></span>       | <span data-ttu-id="78a76-139">Vero</span><span class="sxs-lookup"><span data-stu-id="78a76-139">True</span></span>                                                                                          |
| <span data-ttu-id="78a76-140">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="78a76-140">Is Indexed</span></span>             | <span data-ttu-id="78a76-141">Falso</span><span class="sxs-lookup"><span data-stu-id="78a76-141">False</span></span>                                                                                         |
| <span data-ttu-id="78a76-142">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="78a76-142">In Global Catalog</span></span>      | <span data-ttu-id="78a76-143">Vero</span><span class="sxs-lookup"><span data-stu-id="78a76-143">True</span></span>                                                                                          |
| <span data-ttu-id="78a76-144">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="78a76-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="78a76-145">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="78a76-145">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="78a76-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="78a76-146">Range-Lower</span></span>            | \-                                                                                            |
| <span data-ttu-id="78a76-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="78a76-147">Range-Upper</span></span>            | \-                                                                                            |
| <span data-ttu-id="78a76-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="78a76-148">Search-Flags</span></span>           | <span data-ttu-id="78a76-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="78a76-149">0x00000000</span></span>                                                                                    |
| <span data-ttu-id="78a76-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="78a76-150">System-Flags</span></span>           | <span data-ttu-id="78a76-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="78a76-151">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="78a76-152">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="78a76-152">Classes used in</span></span>        | [<span data-ttu-id="78a76-153">**MSMQ-migrated-utente**</span><span class="sxs-lookup"><span data-stu-id="78a76-153">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="78a76-154">**Utente**</span><span class="sxs-lookup"><span data-stu-id="78a76-154">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="78a76-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="78a76-155">Windows Server 2003</span></span>



| <span data-ttu-id="78a76-156">Voce</span><span class="sxs-lookup"><span data-stu-id="78a76-156">Entry</span></span> | <span data-ttu-id="78a76-157">Valore</span><span class="sxs-lookup"><span data-stu-id="78a76-157">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="78a76-158">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="78a76-158">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="78a76-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="78a76-159">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="78a76-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="78a76-160">System-Only</span></span>            | <span data-ttu-id="78a76-161">Falso</span><span class="sxs-lookup"><span data-stu-id="78a76-161">False</span></span>                                                                                         |
| <span data-ttu-id="78a76-162">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="78a76-162">Is-Single-Valued</span></span>       | <span data-ttu-id="78a76-163">Vero</span><span class="sxs-lookup"><span data-stu-id="78a76-163">True</span></span>                                                                                          |
| <span data-ttu-id="78a76-164">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="78a76-164">Is Indexed</span></span>             | <span data-ttu-id="78a76-165">Falso</span><span class="sxs-lookup"><span data-stu-id="78a76-165">False</span></span>                                                                                         |
| <span data-ttu-id="78a76-166">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="78a76-166">In Global Catalog</span></span>      | <span data-ttu-id="78a76-167">Vero</span><span class="sxs-lookup"><span data-stu-id="78a76-167">True</span></span>                                                                                          |
| <span data-ttu-id="78a76-168">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="78a76-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="78a76-169">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="78a76-169">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="78a76-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="78a76-170">Range-Lower</span></span>            | \-                                                                                            |
| <span data-ttu-id="78a76-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="78a76-171">Range-Upper</span></span>            | \-                                                                                            |
| <span data-ttu-id="78a76-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="78a76-172">Search-Flags</span></span>           | <span data-ttu-id="78a76-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="78a76-173">0x00000000</span></span>                                                                                    |
| <span data-ttu-id="78a76-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="78a76-174">System-Flags</span></span>           | <span data-ttu-id="78a76-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="78a76-175">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="78a76-176">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="78a76-176">Classes used in</span></span>        | [<span data-ttu-id="78a76-177">**MSMQ-migrated-utente**</span><span class="sxs-lookup"><span data-stu-id="78a76-177">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="78a76-178">**Utente**</span><span class="sxs-lookup"><span data-stu-id="78a76-178">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="78a76-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="78a76-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="78a76-180">Voce</span><span class="sxs-lookup"><span data-stu-id="78a76-180">Entry</span></span> | <span data-ttu-id="78a76-181">Valore</span><span class="sxs-lookup"><span data-stu-id="78a76-181">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="78a76-182">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="78a76-182">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="78a76-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="78a76-183">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="78a76-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="78a76-184">System-Only</span></span>            | <span data-ttu-id="78a76-185">Falso</span><span class="sxs-lookup"><span data-stu-id="78a76-185">False</span></span>                                                                                         |
| <span data-ttu-id="78a76-186">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="78a76-186">Is-Single-Valued</span></span>       | <span data-ttu-id="78a76-187">Vero</span><span class="sxs-lookup"><span data-stu-id="78a76-187">True</span></span>                                                                                          |
| <span data-ttu-id="78a76-188">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="78a76-188">Is Indexed</span></span>             | <span data-ttu-id="78a76-189">Falso</span><span class="sxs-lookup"><span data-stu-id="78a76-189">False</span></span>                                                                                         |
| <span data-ttu-id="78a76-190">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="78a76-190">In Global Catalog</span></span>      | <span data-ttu-id="78a76-191">Vero</span><span class="sxs-lookup"><span data-stu-id="78a76-191">True</span></span>                                                                                          |
| <span data-ttu-id="78a76-192">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="78a76-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="78a76-193">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="78a76-193">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="78a76-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="78a76-194">Range-Lower</span></span>            | \-                                                                                            |
| <span data-ttu-id="78a76-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="78a76-195">Range-Upper</span></span>            | \-                                                                                            |
| <span data-ttu-id="78a76-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="78a76-196">Search-Flags</span></span>           | <span data-ttu-id="78a76-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="78a76-197">0x00000000</span></span>                                                                                    |
| <span data-ttu-id="78a76-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="78a76-198">System-Flags</span></span>           | <span data-ttu-id="78a76-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="78a76-199">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="78a76-200">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="78a76-200">Classes used in</span></span>        | [<span data-ttu-id="78a76-201">**MSMQ-migrated-utente**</span><span class="sxs-lookup"><span data-stu-id="78a76-201">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="78a76-202">**Utente**</span><span class="sxs-lookup"><span data-stu-id="78a76-202">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="78a76-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="78a76-203">Windows Server 2008</span></span>



| <span data-ttu-id="78a76-204">Voce</span><span class="sxs-lookup"><span data-stu-id="78a76-204">Entry</span></span> | <span data-ttu-id="78a76-205">Valore</span><span class="sxs-lookup"><span data-stu-id="78a76-205">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="78a76-206">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="78a76-206">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="78a76-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="78a76-207">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="78a76-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="78a76-208">System-Only</span></span>            | <span data-ttu-id="78a76-209">Falso</span><span class="sxs-lookup"><span data-stu-id="78a76-209">False</span></span>                                                                                         |
| <span data-ttu-id="78a76-210">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="78a76-210">Is-Single-Valued</span></span>       | <span data-ttu-id="78a76-211">Vero</span><span class="sxs-lookup"><span data-stu-id="78a76-211">True</span></span>                                                                                          |
| <span data-ttu-id="78a76-212">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="78a76-212">Is Indexed</span></span>             | <span data-ttu-id="78a76-213">Falso</span><span class="sxs-lookup"><span data-stu-id="78a76-213">False</span></span>                                                                                         |
| <span data-ttu-id="78a76-214">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="78a76-214">In Global Catalog</span></span>      | <span data-ttu-id="78a76-215">Vero</span><span class="sxs-lookup"><span data-stu-id="78a76-215">True</span></span>                                                                                          |
| <span data-ttu-id="78a76-216">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="78a76-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="78a76-217">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="78a76-217">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="78a76-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="78a76-218">Range-Lower</span></span>            | \-                                                                                            |
| <span data-ttu-id="78a76-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="78a76-219">Range-Upper</span></span>            | \-                                                                                            |
| <span data-ttu-id="78a76-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="78a76-220">Search-Flags</span></span>           | <span data-ttu-id="78a76-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="78a76-221">0x00000000</span></span>                                                                                    |
| <span data-ttu-id="78a76-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="78a76-222">System-Flags</span></span>           | <span data-ttu-id="78a76-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="78a76-223">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="78a76-224">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="78a76-224">Classes used in</span></span>        | [<span data-ttu-id="78a76-225">**MSMQ-migrated-utente**</span><span class="sxs-lookup"><span data-stu-id="78a76-225">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="78a76-226">**Utente**</span><span class="sxs-lookup"><span data-stu-id="78a76-226">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="78a76-227">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="78a76-227">Windows Server 2008 R2</span></span>



| <span data-ttu-id="78a76-228">Voce</span><span class="sxs-lookup"><span data-stu-id="78a76-228">Entry</span></span> | <span data-ttu-id="78a76-229">Valore</span><span class="sxs-lookup"><span data-stu-id="78a76-229">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="78a76-230">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="78a76-230">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="78a76-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="78a76-231">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="78a76-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="78a76-232">System-Only</span></span>            | <span data-ttu-id="78a76-233">Falso</span><span class="sxs-lookup"><span data-stu-id="78a76-233">False</span></span>                                                                                         |
| <span data-ttu-id="78a76-234">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="78a76-234">Is-Single-Valued</span></span>       | <span data-ttu-id="78a76-235">Vero</span><span class="sxs-lookup"><span data-stu-id="78a76-235">True</span></span>                                                                                          |
| <span data-ttu-id="78a76-236">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="78a76-236">Is Indexed</span></span>             | <span data-ttu-id="78a76-237">Falso</span><span class="sxs-lookup"><span data-stu-id="78a76-237">False</span></span>                                                                                         |
| <span data-ttu-id="78a76-238">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="78a76-238">In Global Catalog</span></span>      | <span data-ttu-id="78a76-239">Vero</span><span class="sxs-lookup"><span data-stu-id="78a76-239">True</span></span>                                                                                          |
| <span data-ttu-id="78a76-240">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="78a76-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="78a76-241">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="78a76-241">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="78a76-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="78a76-242">Range-Lower</span></span>            | \-                                                                                            |
| <span data-ttu-id="78a76-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="78a76-243">Range-Upper</span></span>            | \-                                                                                            |
| <span data-ttu-id="78a76-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="78a76-244">Search-Flags</span></span>           | <span data-ttu-id="78a76-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="78a76-245">0x00000000</span></span>                                                                                    |
| <span data-ttu-id="78a76-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="78a76-246">System-Flags</span></span>           | <span data-ttu-id="78a76-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="78a76-247">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="78a76-248">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="78a76-248">Classes used in</span></span>        | [<span data-ttu-id="78a76-249">**MSMQ-migrated-utente**</span><span class="sxs-lookup"><span data-stu-id="78a76-249">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="78a76-250">**Utente**</span><span class="sxs-lookup"><span data-stu-id="78a76-250">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="78a76-251">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="78a76-251">Windows Server 2012</span></span>



| <span data-ttu-id="78a76-252">Voce</span><span class="sxs-lookup"><span data-stu-id="78a76-252">Entry</span></span> | <span data-ttu-id="78a76-253">Valore</span><span class="sxs-lookup"><span data-stu-id="78a76-253">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="78a76-254">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="78a76-254">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="78a76-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="78a76-255">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="78a76-256">System-Only</span><span class="sxs-lookup"><span data-stu-id="78a76-256">System-Only</span></span>            | <span data-ttu-id="78a76-257">Falso</span><span class="sxs-lookup"><span data-stu-id="78a76-257">False</span></span>                                                                                         |
| <span data-ttu-id="78a76-258">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="78a76-258">Is-Single-Valued</span></span>       | <span data-ttu-id="78a76-259">Vero</span><span class="sxs-lookup"><span data-stu-id="78a76-259">True</span></span>                                                                                          |
| <span data-ttu-id="78a76-260">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="78a76-260">Is Indexed</span></span>             | <span data-ttu-id="78a76-261">Falso</span><span class="sxs-lookup"><span data-stu-id="78a76-261">False</span></span>                                                                                         |
| <span data-ttu-id="78a76-262">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="78a76-262">In Global Catalog</span></span>      | <span data-ttu-id="78a76-263">Vero</span><span class="sxs-lookup"><span data-stu-id="78a76-263">True</span></span>                                                                                          |
| <span data-ttu-id="78a76-264">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="78a76-264">NT-Security-Descriptor</span></span> | <span data-ttu-id="78a76-265">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="78a76-265">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="78a76-266">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="78a76-266">Range-Lower</span></span>            | \-                                                                                            |
| <span data-ttu-id="78a76-267">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="78a76-267">Range-Upper</span></span>            | \-                                                                                            |
| <span data-ttu-id="78a76-268">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="78a76-268">Search-Flags</span></span>           | <span data-ttu-id="78a76-269">0x00000000</span><span class="sxs-lookup"><span data-stu-id="78a76-269">0x00000000</span></span>                                                                                    |
| <span data-ttu-id="78a76-270">System-Flags</span><span class="sxs-lookup"><span data-stu-id="78a76-270">System-Flags</span></span>           | <span data-ttu-id="78a76-271">0x00000010</span><span class="sxs-lookup"><span data-stu-id="78a76-271">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="78a76-272">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="78a76-272">Classes used in</span></span>        | [<span data-ttu-id="78a76-273">**MSMQ-migrated-utente**</span><span class="sxs-lookup"><span data-stu-id="78a76-273">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="78a76-274">**Utente**</span><span class="sxs-lookup"><span data-stu-id="78a76-274">**User**</span></span>](c-user.md)<br/> |



 

 





