---
title: Attributo MSMQ-Sign-Certificates
description: Questo attributo contiene un numero di certificati. Un utente può generare un certificato per ogni computer. Per ogni certificato viene anche mantenuto un digest.
ms.assetid: 70e182c7-3544-43d7-b27a-6e8d03bd2d47
ms.tgt_platform: multiple
keywords:
- Attributo MSMQ-Sign-Certificates-schema AD
- Schema AD dell'attributo mSMQSignCertificates
topic_type:
- apiref
api_name:
- MSMQ-Sign-Certificates
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dd7e81cf145ac249b78e0a3e20be657df68b4af
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103875309"
---
# <a name="msmq-sign-certificates-attribute"></a><span data-ttu-id="42ccb-107">Attributo MSMQ-Sign-Certificates</span><span class="sxs-lookup"><span data-stu-id="42ccb-107">MSMQ-Sign-Certificates attribute</span></span>

<span data-ttu-id="42ccb-108">Questo attributo contiene un numero di certificati.</span><span class="sxs-lookup"><span data-stu-id="42ccb-108">This attribute contains a number of certificates.</span></span> <span data-ttu-id="42ccb-109">Un utente può generare un certificato per ogni computer.</span><span class="sxs-lookup"><span data-stu-id="42ccb-109">A user can generate a certificate per computer.</span></span> <span data-ttu-id="42ccb-110">Per ogni certificato viene anche mantenuto un digest.</span><span class="sxs-lookup"><span data-stu-id="42ccb-110">For each certificate we also keep a digest.</span></span>



| <span data-ttu-id="42ccb-111">Voce</span><span class="sxs-lookup"><span data-stu-id="42ccb-111">Entry</span></span> | <span data-ttu-id="42ccb-112">Valore</span><span class="sxs-lookup"><span data-stu-id="42ccb-112">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="42ccb-113">CN</span><span class="sxs-lookup"><span data-stu-id="42ccb-113">CN</span></span>                | <span data-ttu-id="42ccb-114">MSMQ-Sign-Certificates</span><span class="sxs-lookup"><span data-stu-id="42ccb-114">MSMQ-Sign-Certificates</span></span>                                                                 |
| <span data-ttu-id="42ccb-115">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="42ccb-115">Ldap-Display-Name</span></span> | <span data-ttu-id="42ccb-116">mSMQSignCertificates</span><span class="sxs-lookup"><span data-stu-id="42ccb-116">mSMQSignCertificates</span></span>                                                                   |
| <span data-ttu-id="42ccb-117">Dimensione</span><span class="sxs-lookup"><span data-stu-id="42ccb-117">Size</span></span>              | <span data-ttu-id="42ccb-118">Il tipo di attributo è un BLOB, le dimensioni non sono limitate e i dati vengono mantenuti nel formato personalizzato.</span><span class="sxs-lookup"><span data-stu-id="42ccb-118">The attribute type is a BLOB, size is not limited, and data is kept in our own format.</span></span> |
| <span data-ttu-id="42ccb-119">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="42ccb-119">Update Privilege</span></span>  | \-                                                                                     |
| <span data-ttu-id="42ccb-120">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="42ccb-120">Update Frequency</span></span>  | \-                                                                                     |
| <span data-ttu-id="42ccb-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="42ccb-121">Attribute-Id</span></span>      | <span data-ttu-id="42ccb-122">1.2.840.113556.1.4.947</span><span class="sxs-lookup"><span data-stu-id="42ccb-122">1.2.840.113556.1.4.947</span></span>                                                                 |
| <span data-ttu-id="42ccb-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="42ccb-123">System-Id-Guid</span></span>    | <span data-ttu-id="42ccb-124">9a0dc33b-c100-11d1-bbc5-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="42ccb-124">9a0dc33b-c100-11d1-bbc5-0080c76670c0</span></span>                                                   |
| <span data-ttu-id="42ccb-125">Sintassi</span><span class="sxs-lookup"><span data-stu-id="42ccb-125">Syntax</span></span>            | [<span data-ttu-id="42ccb-126">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="42ccb-126">**Object(Replica-Link)**</span></span>](s-object-replica-link.md)                                  |



## <a name="implementations"></a><span data-ttu-id="42ccb-127">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="42ccb-127">Implementations</span></span>

-   [<span data-ttu-id="42ccb-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="42ccb-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="42ccb-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="42ccb-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="42ccb-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="42ccb-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="42ccb-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="42ccb-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="42ccb-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="42ccb-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="42ccb-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="42ccb-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="42ccb-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="42ccb-134">Windows 2000 Server</span></span>



| <span data-ttu-id="42ccb-135">Voce</span><span class="sxs-lookup"><span data-stu-id="42ccb-135">Entry</span></span> | <span data-ttu-id="42ccb-136">Valore</span><span class="sxs-lookup"><span data-stu-id="42ccb-136">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="42ccb-137">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="42ccb-137">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="42ccb-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="42ccb-138">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="42ccb-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="42ccb-139">System-Only</span></span>            | <span data-ttu-id="42ccb-140">Falso</span><span class="sxs-lookup"><span data-stu-id="42ccb-140">False</span></span>                                                                                         |
| <span data-ttu-id="42ccb-141">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="42ccb-141">Is-Single-Valued</span></span>       | <span data-ttu-id="42ccb-142">Vero</span><span class="sxs-lookup"><span data-stu-id="42ccb-142">True</span></span>                                                                                          |
| <span data-ttu-id="42ccb-143">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="42ccb-143">Is Indexed</span></span>             | <span data-ttu-id="42ccb-144">Falso</span><span class="sxs-lookup"><span data-stu-id="42ccb-144">False</span></span>                                                                                         |
| <span data-ttu-id="42ccb-145">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="42ccb-145">In Global Catalog</span></span>      | <span data-ttu-id="42ccb-146">Vero</span><span class="sxs-lookup"><span data-stu-id="42ccb-146">True</span></span>                                                                                          |
| <span data-ttu-id="42ccb-147">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="42ccb-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="42ccb-148">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="42ccb-148">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="42ccb-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="42ccb-149">Range-Lower</span></span>            | \-                                                                                            |
| <span data-ttu-id="42ccb-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="42ccb-150">Range-Upper</span></span>            | \-                                                                                            |
| <span data-ttu-id="42ccb-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="42ccb-151">Search-Flags</span></span>           | <span data-ttu-id="42ccb-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="42ccb-152">0x00000000</span></span>                                                                                    |
| <span data-ttu-id="42ccb-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="42ccb-153">System-Flags</span></span>           | <span data-ttu-id="42ccb-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="42ccb-154">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="42ccb-155">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="42ccb-155">Classes used in</span></span>        | [<span data-ttu-id="42ccb-156">**MSMQ-migrated-utente**</span><span class="sxs-lookup"><span data-stu-id="42ccb-156">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="42ccb-157">**Utente**</span><span class="sxs-lookup"><span data-stu-id="42ccb-157">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="42ccb-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="42ccb-158">Windows Server 2003</span></span>



| <span data-ttu-id="42ccb-159">Voce</span><span class="sxs-lookup"><span data-stu-id="42ccb-159">Entry</span></span> | <span data-ttu-id="42ccb-160">Valore</span><span class="sxs-lookup"><span data-stu-id="42ccb-160">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="42ccb-161">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="42ccb-161">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="42ccb-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="42ccb-162">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="42ccb-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="42ccb-163">System-Only</span></span>            | <span data-ttu-id="42ccb-164">Falso</span><span class="sxs-lookup"><span data-stu-id="42ccb-164">False</span></span>                                                                                         |
| <span data-ttu-id="42ccb-165">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="42ccb-165">Is-Single-Valued</span></span>       | <span data-ttu-id="42ccb-166">Vero</span><span class="sxs-lookup"><span data-stu-id="42ccb-166">True</span></span>                                                                                          |
| <span data-ttu-id="42ccb-167">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="42ccb-167">Is Indexed</span></span>             | <span data-ttu-id="42ccb-168">Falso</span><span class="sxs-lookup"><span data-stu-id="42ccb-168">False</span></span>                                                                                         |
| <span data-ttu-id="42ccb-169">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="42ccb-169">In Global Catalog</span></span>      | <span data-ttu-id="42ccb-170">Vero</span><span class="sxs-lookup"><span data-stu-id="42ccb-170">True</span></span>                                                                                          |
| <span data-ttu-id="42ccb-171">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="42ccb-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="42ccb-172">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="42ccb-172">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="42ccb-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="42ccb-173">Range-Lower</span></span>            | \-                                                                                            |
| <span data-ttu-id="42ccb-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="42ccb-174">Range-Upper</span></span>            | \-                                                                                            |
| <span data-ttu-id="42ccb-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="42ccb-175">Search-Flags</span></span>           | <span data-ttu-id="42ccb-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="42ccb-176">0x00000000</span></span>                                                                                    |
| <span data-ttu-id="42ccb-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="42ccb-177">System-Flags</span></span>           | <span data-ttu-id="42ccb-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="42ccb-178">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="42ccb-179">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="42ccb-179">Classes used in</span></span>        | [<span data-ttu-id="42ccb-180">**MSMQ-migrated-utente**</span><span class="sxs-lookup"><span data-stu-id="42ccb-180">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="42ccb-181">**Utente**</span><span class="sxs-lookup"><span data-stu-id="42ccb-181">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="42ccb-182">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="42ccb-182">Windows Server 2003 R2</span></span>



| <span data-ttu-id="42ccb-183">Voce</span><span class="sxs-lookup"><span data-stu-id="42ccb-183">Entry</span></span> | <span data-ttu-id="42ccb-184">Valore</span><span class="sxs-lookup"><span data-stu-id="42ccb-184">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="42ccb-185">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="42ccb-185">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="42ccb-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="42ccb-186">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="42ccb-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="42ccb-187">System-Only</span></span>            | <span data-ttu-id="42ccb-188">Falso</span><span class="sxs-lookup"><span data-stu-id="42ccb-188">False</span></span>                                                                                         |
| <span data-ttu-id="42ccb-189">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="42ccb-189">Is-Single-Valued</span></span>       | <span data-ttu-id="42ccb-190">Vero</span><span class="sxs-lookup"><span data-stu-id="42ccb-190">True</span></span>                                                                                          |
| <span data-ttu-id="42ccb-191">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="42ccb-191">Is Indexed</span></span>             | <span data-ttu-id="42ccb-192">Falso</span><span class="sxs-lookup"><span data-stu-id="42ccb-192">False</span></span>                                                                                         |
| <span data-ttu-id="42ccb-193">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="42ccb-193">In Global Catalog</span></span>      | <span data-ttu-id="42ccb-194">Vero</span><span class="sxs-lookup"><span data-stu-id="42ccb-194">True</span></span>                                                                                          |
| <span data-ttu-id="42ccb-195">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="42ccb-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="42ccb-196">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="42ccb-196">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="42ccb-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="42ccb-197">Range-Lower</span></span>            | \-                                                                                            |
| <span data-ttu-id="42ccb-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="42ccb-198">Range-Upper</span></span>            | \-                                                                                            |
| <span data-ttu-id="42ccb-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="42ccb-199">Search-Flags</span></span>           | <span data-ttu-id="42ccb-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="42ccb-200">0x00000000</span></span>                                                                                    |
| <span data-ttu-id="42ccb-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="42ccb-201">System-Flags</span></span>           | <span data-ttu-id="42ccb-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="42ccb-202">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="42ccb-203">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="42ccb-203">Classes used in</span></span>        | [<span data-ttu-id="42ccb-204">**MSMQ-migrated-utente**</span><span class="sxs-lookup"><span data-stu-id="42ccb-204">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="42ccb-205">**Utente**</span><span class="sxs-lookup"><span data-stu-id="42ccb-205">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="42ccb-206">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="42ccb-206">Windows Server 2008</span></span>



| <span data-ttu-id="42ccb-207">Voce</span><span class="sxs-lookup"><span data-stu-id="42ccb-207">Entry</span></span> | <span data-ttu-id="42ccb-208">Valore</span><span class="sxs-lookup"><span data-stu-id="42ccb-208">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="42ccb-209">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="42ccb-209">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="42ccb-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="42ccb-210">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="42ccb-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="42ccb-211">System-Only</span></span>            | <span data-ttu-id="42ccb-212">Falso</span><span class="sxs-lookup"><span data-stu-id="42ccb-212">False</span></span>                                                                                         |
| <span data-ttu-id="42ccb-213">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="42ccb-213">Is-Single-Valued</span></span>       | <span data-ttu-id="42ccb-214">Vero</span><span class="sxs-lookup"><span data-stu-id="42ccb-214">True</span></span>                                                                                          |
| <span data-ttu-id="42ccb-215">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="42ccb-215">Is Indexed</span></span>             | <span data-ttu-id="42ccb-216">Falso</span><span class="sxs-lookup"><span data-stu-id="42ccb-216">False</span></span>                                                                                         |
| <span data-ttu-id="42ccb-217">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="42ccb-217">In Global Catalog</span></span>      | <span data-ttu-id="42ccb-218">Vero</span><span class="sxs-lookup"><span data-stu-id="42ccb-218">True</span></span>                                                                                          |
| <span data-ttu-id="42ccb-219">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="42ccb-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="42ccb-220">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="42ccb-220">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="42ccb-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="42ccb-221">Range-Lower</span></span>            | \-                                                                                            |
| <span data-ttu-id="42ccb-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="42ccb-222">Range-Upper</span></span>            | \-                                                                                            |
| <span data-ttu-id="42ccb-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="42ccb-223">Search-Flags</span></span>           | <span data-ttu-id="42ccb-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="42ccb-224">0x00000000</span></span>                                                                                    |
| <span data-ttu-id="42ccb-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="42ccb-225">System-Flags</span></span>           | <span data-ttu-id="42ccb-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="42ccb-226">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="42ccb-227">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="42ccb-227">Classes used in</span></span>        | [<span data-ttu-id="42ccb-228">**MSMQ-migrated-utente**</span><span class="sxs-lookup"><span data-stu-id="42ccb-228">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="42ccb-229">**Utente**</span><span class="sxs-lookup"><span data-stu-id="42ccb-229">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="42ccb-230">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="42ccb-230">Windows Server 2008 R2</span></span>



| <span data-ttu-id="42ccb-231">Voce</span><span class="sxs-lookup"><span data-stu-id="42ccb-231">Entry</span></span> | <span data-ttu-id="42ccb-232">Valore</span><span class="sxs-lookup"><span data-stu-id="42ccb-232">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="42ccb-233">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="42ccb-233">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="42ccb-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="42ccb-234">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="42ccb-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="42ccb-235">System-Only</span></span>            | <span data-ttu-id="42ccb-236">Falso</span><span class="sxs-lookup"><span data-stu-id="42ccb-236">False</span></span>                                                                                         |
| <span data-ttu-id="42ccb-237">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="42ccb-237">Is-Single-Valued</span></span>       | <span data-ttu-id="42ccb-238">Vero</span><span class="sxs-lookup"><span data-stu-id="42ccb-238">True</span></span>                                                                                          |
| <span data-ttu-id="42ccb-239">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="42ccb-239">Is Indexed</span></span>             | <span data-ttu-id="42ccb-240">Falso</span><span class="sxs-lookup"><span data-stu-id="42ccb-240">False</span></span>                                                                                         |
| <span data-ttu-id="42ccb-241">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="42ccb-241">In Global Catalog</span></span>      | <span data-ttu-id="42ccb-242">Vero</span><span class="sxs-lookup"><span data-stu-id="42ccb-242">True</span></span>                                                                                          |
| <span data-ttu-id="42ccb-243">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="42ccb-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="42ccb-244">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="42ccb-244">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="42ccb-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="42ccb-245">Range-Lower</span></span>            | \-                                                                                            |
| <span data-ttu-id="42ccb-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="42ccb-246">Range-Upper</span></span>            | \-                                                                                            |
| <span data-ttu-id="42ccb-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="42ccb-247">Search-Flags</span></span>           | <span data-ttu-id="42ccb-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="42ccb-248">0x00000000</span></span>                                                                                    |
| <span data-ttu-id="42ccb-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="42ccb-249">System-Flags</span></span>           | <span data-ttu-id="42ccb-250">0x00000010</span><span class="sxs-lookup"><span data-stu-id="42ccb-250">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="42ccb-251">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="42ccb-251">Classes used in</span></span>        | [<span data-ttu-id="42ccb-252">**MSMQ-migrated-utente**</span><span class="sxs-lookup"><span data-stu-id="42ccb-252">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="42ccb-253">**Utente**</span><span class="sxs-lookup"><span data-stu-id="42ccb-253">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="42ccb-254">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="42ccb-254">Windows Server 2012</span></span>



| <span data-ttu-id="42ccb-255">Voce</span><span class="sxs-lookup"><span data-stu-id="42ccb-255">Entry</span></span> | <span data-ttu-id="42ccb-256">Valore</span><span class="sxs-lookup"><span data-stu-id="42ccb-256">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="42ccb-257">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="42ccb-257">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="42ccb-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="42ccb-258">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="42ccb-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="42ccb-259">System-Only</span></span>            | <span data-ttu-id="42ccb-260">Falso</span><span class="sxs-lookup"><span data-stu-id="42ccb-260">False</span></span>                                                                                         |
| <span data-ttu-id="42ccb-261">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="42ccb-261">Is-Single-Valued</span></span>       | <span data-ttu-id="42ccb-262">Vero</span><span class="sxs-lookup"><span data-stu-id="42ccb-262">True</span></span>                                                                                          |
| <span data-ttu-id="42ccb-263">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="42ccb-263">Is Indexed</span></span>             | <span data-ttu-id="42ccb-264">Falso</span><span class="sxs-lookup"><span data-stu-id="42ccb-264">False</span></span>                                                                                         |
| <span data-ttu-id="42ccb-265">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="42ccb-265">In Global Catalog</span></span>      | <span data-ttu-id="42ccb-266">Vero</span><span class="sxs-lookup"><span data-stu-id="42ccb-266">True</span></span>                                                                                          |
| <span data-ttu-id="42ccb-267">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="42ccb-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="42ccb-268">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="42ccb-268">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="42ccb-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="42ccb-269">Range-Lower</span></span>            | \-                                                                                            |
| <span data-ttu-id="42ccb-270">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="42ccb-270">Range-Upper</span></span>            | \-                                                                                            |
| <span data-ttu-id="42ccb-271">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="42ccb-271">Search-Flags</span></span>           | <span data-ttu-id="42ccb-272">0x00000000</span><span class="sxs-lookup"><span data-stu-id="42ccb-272">0x00000000</span></span>                                                                                    |
| <span data-ttu-id="42ccb-273">System-Flags</span><span class="sxs-lookup"><span data-stu-id="42ccb-273">System-Flags</span></span>           | <span data-ttu-id="42ccb-274">0x00000010</span><span class="sxs-lookup"><span data-stu-id="42ccb-274">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="42ccb-275">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="42ccb-275">Classes used in</span></span>        | [<span data-ttu-id="42ccb-276">**MSMQ-migrated-utente**</span><span class="sxs-lookup"><span data-stu-id="42ccb-276">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="42ccb-277">**Utente**</span><span class="sxs-lookup"><span data-stu-id="42ccb-277">**User**</span></span>](c-user.md)<br/> |



 

 





