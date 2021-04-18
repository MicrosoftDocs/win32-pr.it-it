---
title: Attributo MSMQ-Digests
description: Matrice di digest dei certificati corrispondenti nell'attributo mSMQ-Sign-Certificates. Vengono usati per il mapping di un digest in un certificato.
ms.assetid: a9b03edd-1506-4f2d-afe1-7d953977f6fa
ms.tgt_platform: multiple
keywords:
- Schema AD MSMQ-Digests attribute
- Schema AD dell'attributo mSMQDigests
topic_type:
- apiref
api_name:
- MSMQ-Digests
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06d51c607b1d99af0aed46f259513f4bcf790844
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "106303471"
---
# <a name="msmq-digests-attribute"></a><span data-ttu-id="3d5e9-106">Attributo MSMQ-Digests</span><span class="sxs-lookup"><span data-stu-id="3d5e9-106">MSMQ-Digests attribute</span></span>

<span data-ttu-id="3d5e9-107">Matrice di digest dei certificati corrispondenti nell'attributo mSMQ-Sign-Certificates.</span><span class="sxs-lookup"><span data-stu-id="3d5e9-107">An array of digests of the corresponding certificates in attribute mSMQ-Sign-Certificates.</span></span> <span data-ttu-id="3d5e9-108">Vengono usati per il mapping di un digest in un certificato.</span><span class="sxs-lookup"><span data-stu-id="3d5e9-108">They are used for mapping a digest into a certificate.</span></span>



| <span data-ttu-id="3d5e9-109">Voce</span><span class="sxs-lookup"><span data-stu-id="3d5e9-109">Entry</span></span> | <span data-ttu-id="3d5e9-110">Valore</span><span class="sxs-lookup"><span data-stu-id="3d5e9-110">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="3d5e9-111">CN</span><span class="sxs-lookup"><span data-stu-id="3d5e9-111">CN</span></span>                | <span data-ttu-id="3d5e9-112">MSMQ-Digests</span><span class="sxs-lookup"><span data-stu-id="3d5e9-112">MSMQ-Digests</span></span>                                          |
| <span data-ttu-id="3d5e9-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="3d5e9-113">Ldap-Display-Name</span></span> | <span data-ttu-id="3d5e9-114">mSMQDigests</span><span class="sxs-lookup"><span data-stu-id="3d5e9-114">mSMQDigests</span></span>                                           |
| <span data-ttu-id="3d5e9-115">Dimensione</span><span class="sxs-lookup"><span data-stu-id="3d5e9-115">Size</span></span>              | <span data-ttu-id="3d5e9-116">Ogni digest è pari a 16 byte.</span><span class="sxs-lookup"><span data-stu-id="3d5e9-116">Each digest is 16 bytes.</span></span>                              |
| <span data-ttu-id="3d5e9-117">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="3d5e9-117">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="3d5e9-118">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="3d5e9-118">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="3d5e9-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="3d5e9-119">Attribute-Id</span></span>      | <span data-ttu-id="3d5e9-120">1.2.840.113556.1.4.948</span><span class="sxs-lookup"><span data-stu-id="3d5e9-120">1.2.840.113556.1.4.948</span></span>                                |
| <span data-ttu-id="3d5e9-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="3d5e9-121">System-Id-Guid</span></span>    | <span data-ttu-id="3d5e9-122">9a0dc33c-c100-11d1-bbc5-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="3d5e9-122">9a0dc33c-c100-11d1-bbc5-0080c76670c0</span></span>                  |
| <span data-ttu-id="3d5e9-123">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3d5e9-123">Syntax</span></span>            | [<span data-ttu-id="3d5e9-124">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="3d5e9-124">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="3d5e9-125">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="3d5e9-125">Implementations</span></span>

-   [<span data-ttu-id="3d5e9-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="3d5e9-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="3d5e9-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="3d5e9-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="3d5e9-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="3d5e9-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="3d5e9-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="3d5e9-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="3d5e9-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="3d5e9-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="3d5e9-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="3d5e9-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="3d5e9-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="3d5e9-132">Windows 2000 Server</span></span>



| <span data-ttu-id="3d5e9-133">Voce</span><span class="sxs-lookup"><span data-stu-id="3d5e9-133">Entry</span></span> | <span data-ttu-id="3d5e9-134">Valore</span><span class="sxs-lookup"><span data-stu-id="3d5e9-134">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d5e9-135">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="3d5e9-135">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="3d5e9-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3d5e9-136">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="3d5e9-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="3d5e9-137">System-Only</span></span>            | <span data-ttu-id="3d5e9-138">Falso</span><span class="sxs-lookup"><span data-stu-id="3d5e9-138">False</span></span>                                                                                         |
| <span data-ttu-id="3d5e9-139">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="3d5e9-139">Is-Single-Valued</span></span>       | <span data-ttu-id="3d5e9-140">Falso</span><span class="sxs-lookup"><span data-stu-id="3d5e9-140">False</span></span>                                                                                         |
| <span data-ttu-id="3d5e9-141">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="3d5e9-141">Is Indexed</span></span>             | <span data-ttu-id="3d5e9-142">Vero</span><span class="sxs-lookup"><span data-stu-id="3d5e9-142">True</span></span>                                                                                          |
| <span data-ttu-id="3d5e9-143">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="3d5e9-143">In Global Catalog</span></span>      | <span data-ttu-id="3d5e9-144">Vero</span><span class="sxs-lookup"><span data-stu-id="3d5e9-144">True</span></span>                                                                                          |
| <span data-ttu-id="3d5e9-145">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="3d5e9-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="3d5e9-146">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="3d5e9-146">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="3d5e9-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3d5e9-147">Range-Lower</span></span>            | <span data-ttu-id="3d5e9-148">16</span><span class="sxs-lookup"><span data-stu-id="3d5e9-148">16</span></span>                                                                                            |
| <span data-ttu-id="3d5e9-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3d5e9-149">Range-Upper</span></span>            | <span data-ttu-id="3d5e9-150">16</span><span class="sxs-lookup"><span data-stu-id="3d5e9-150">16</span></span>                                                                                            |
| <span data-ttu-id="3d5e9-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3d5e9-151">Search-Flags</span></span>           | <span data-ttu-id="3d5e9-152">0x00000001</span><span class="sxs-lookup"><span data-stu-id="3d5e9-152">0x00000001</span></span>                                                                                    |
| <span data-ttu-id="3d5e9-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3d5e9-153">System-Flags</span></span>           | <span data-ttu-id="3d5e9-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3d5e9-154">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="3d5e9-155">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="3d5e9-155">Classes used in</span></span>        | [<span data-ttu-id="3d5e9-156">**MSMQ-migrated-utente**</span><span class="sxs-lookup"><span data-stu-id="3d5e9-156">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="3d5e9-157">**Utente**</span><span class="sxs-lookup"><span data-stu-id="3d5e9-157">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="3d5e9-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3d5e9-158">Windows Server 2003</span></span>



| <span data-ttu-id="3d5e9-159">Voce</span><span class="sxs-lookup"><span data-stu-id="3d5e9-159">Entry</span></span> | <span data-ttu-id="3d5e9-160">Valore</span><span class="sxs-lookup"><span data-stu-id="3d5e9-160">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d5e9-161">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="3d5e9-161">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="3d5e9-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3d5e9-162">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="3d5e9-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="3d5e9-163">System-Only</span></span>            | <span data-ttu-id="3d5e9-164">Falso</span><span class="sxs-lookup"><span data-stu-id="3d5e9-164">False</span></span>                                                                                         |
| <span data-ttu-id="3d5e9-165">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="3d5e9-165">Is-Single-Valued</span></span>       | <span data-ttu-id="3d5e9-166">Falso</span><span class="sxs-lookup"><span data-stu-id="3d5e9-166">False</span></span>                                                                                         |
| <span data-ttu-id="3d5e9-167">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="3d5e9-167">Is Indexed</span></span>             | <span data-ttu-id="3d5e9-168">Vero</span><span class="sxs-lookup"><span data-stu-id="3d5e9-168">True</span></span>                                                                                          |
| <span data-ttu-id="3d5e9-169">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="3d5e9-169">In Global Catalog</span></span>      | <span data-ttu-id="3d5e9-170">Vero</span><span class="sxs-lookup"><span data-stu-id="3d5e9-170">True</span></span>                                                                                          |
| <span data-ttu-id="3d5e9-171">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="3d5e9-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="3d5e9-172">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="3d5e9-172">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="3d5e9-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3d5e9-173">Range-Lower</span></span>            | <span data-ttu-id="3d5e9-174">16</span><span class="sxs-lookup"><span data-stu-id="3d5e9-174">16</span></span>                                                                                            |
| <span data-ttu-id="3d5e9-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3d5e9-175">Range-Upper</span></span>            | <span data-ttu-id="3d5e9-176">16</span><span class="sxs-lookup"><span data-stu-id="3d5e9-176">16</span></span>                                                                                            |
| <span data-ttu-id="3d5e9-177">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3d5e9-177">Search-Flags</span></span>           | <span data-ttu-id="3d5e9-178">0x00000001</span><span class="sxs-lookup"><span data-stu-id="3d5e9-178">0x00000001</span></span>                                                                                    |
| <span data-ttu-id="3d5e9-179">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3d5e9-179">System-Flags</span></span>           | <span data-ttu-id="3d5e9-180">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3d5e9-180">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="3d5e9-181">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="3d5e9-181">Classes used in</span></span>        | [<span data-ttu-id="3d5e9-182">**MSMQ-migrated-utente**</span><span class="sxs-lookup"><span data-stu-id="3d5e9-182">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="3d5e9-183">**Utente**</span><span class="sxs-lookup"><span data-stu-id="3d5e9-183">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="3d5e9-184">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="3d5e9-184">Windows Server 2003 R2</span></span>



| <span data-ttu-id="3d5e9-185">Voce</span><span class="sxs-lookup"><span data-stu-id="3d5e9-185">Entry</span></span> | <span data-ttu-id="3d5e9-186">Valore</span><span class="sxs-lookup"><span data-stu-id="3d5e9-186">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d5e9-187">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="3d5e9-187">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="3d5e9-188">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3d5e9-188">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="3d5e9-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="3d5e9-189">System-Only</span></span>            | <span data-ttu-id="3d5e9-190">Falso</span><span class="sxs-lookup"><span data-stu-id="3d5e9-190">False</span></span>                                                                                         |
| <span data-ttu-id="3d5e9-191">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="3d5e9-191">Is-Single-Valued</span></span>       | <span data-ttu-id="3d5e9-192">Falso</span><span class="sxs-lookup"><span data-stu-id="3d5e9-192">False</span></span>                                                                                         |
| <span data-ttu-id="3d5e9-193">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="3d5e9-193">Is Indexed</span></span>             | <span data-ttu-id="3d5e9-194">Vero</span><span class="sxs-lookup"><span data-stu-id="3d5e9-194">True</span></span>                                                                                          |
| <span data-ttu-id="3d5e9-195">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="3d5e9-195">In Global Catalog</span></span>      | <span data-ttu-id="3d5e9-196">Vero</span><span class="sxs-lookup"><span data-stu-id="3d5e9-196">True</span></span>                                                                                          |
| <span data-ttu-id="3d5e9-197">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="3d5e9-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="3d5e9-198">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="3d5e9-198">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="3d5e9-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3d5e9-199">Range-Lower</span></span>            | <span data-ttu-id="3d5e9-200">16</span><span class="sxs-lookup"><span data-stu-id="3d5e9-200">16</span></span>                                                                                            |
| <span data-ttu-id="3d5e9-201">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3d5e9-201">Range-Upper</span></span>            | <span data-ttu-id="3d5e9-202">16</span><span class="sxs-lookup"><span data-stu-id="3d5e9-202">16</span></span>                                                                                            |
| <span data-ttu-id="3d5e9-203">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3d5e9-203">Search-Flags</span></span>           | <span data-ttu-id="3d5e9-204">0x00000001</span><span class="sxs-lookup"><span data-stu-id="3d5e9-204">0x00000001</span></span>                                                                                    |
| <span data-ttu-id="3d5e9-205">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3d5e9-205">System-Flags</span></span>           | <span data-ttu-id="3d5e9-206">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3d5e9-206">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="3d5e9-207">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="3d5e9-207">Classes used in</span></span>        | [<span data-ttu-id="3d5e9-208">**MSMQ-migrated-utente**</span><span class="sxs-lookup"><span data-stu-id="3d5e9-208">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="3d5e9-209">**Utente**</span><span class="sxs-lookup"><span data-stu-id="3d5e9-209">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="3d5e9-210">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3d5e9-210">Windows Server 2008</span></span>



| <span data-ttu-id="3d5e9-211">Voce</span><span class="sxs-lookup"><span data-stu-id="3d5e9-211">Entry</span></span> | <span data-ttu-id="3d5e9-212">Valore</span><span class="sxs-lookup"><span data-stu-id="3d5e9-212">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d5e9-213">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="3d5e9-213">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="3d5e9-214">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3d5e9-214">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="3d5e9-215">System-Only</span><span class="sxs-lookup"><span data-stu-id="3d5e9-215">System-Only</span></span>            | <span data-ttu-id="3d5e9-216">Falso</span><span class="sxs-lookup"><span data-stu-id="3d5e9-216">False</span></span>                                                                                         |
| <span data-ttu-id="3d5e9-217">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="3d5e9-217">Is-Single-Valued</span></span>       | <span data-ttu-id="3d5e9-218">Falso</span><span class="sxs-lookup"><span data-stu-id="3d5e9-218">False</span></span>                                                                                         |
| <span data-ttu-id="3d5e9-219">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="3d5e9-219">Is Indexed</span></span>             | <span data-ttu-id="3d5e9-220">Vero</span><span class="sxs-lookup"><span data-stu-id="3d5e9-220">True</span></span>                                                                                          |
| <span data-ttu-id="3d5e9-221">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="3d5e9-221">In Global Catalog</span></span>      | <span data-ttu-id="3d5e9-222">Vero</span><span class="sxs-lookup"><span data-stu-id="3d5e9-222">True</span></span>                                                                                          |
| <span data-ttu-id="3d5e9-223">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="3d5e9-223">NT-Security-Descriptor</span></span> | <span data-ttu-id="3d5e9-224">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="3d5e9-224">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="3d5e9-225">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3d5e9-225">Range-Lower</span></span>            | <span data-ttu-id="3d5e9-226">16</span><span class="sxs-lookup"><span data-stu-id="3d5e9-226">16</span></span>                                                                                            |
| <span data-ttu-id="3d5e9-227">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3d5e9-227">Range-Upper</span></span>            | <span data-ttu-id="3d5e9-228">16</span><span class="sxs-lookup"><span data-stu-id="3d5e9-228">16</span></span>                                                                                            |
| <span data-ttu-id="3d5e9-229">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3d5e9-229">Search-Flags</span></span>           | <span data-ttu-id="3d5e9-230">0x00000001</span><span class="sxs-lookup"><span data-stu-id="3d5e9-230">0x00000001</span></span>                                                                                    |
| <span data-ttu-id="3d5e9-231">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3d5e9-231">System-Flags</span></span>           | <span data-ttu-id="3d5e9-232">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3d5e9-232">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="3d5e9-233">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="3d5e9-233">Classes used in</span></span>        | [<span data-ttu-id="3d5e9-234">**MSMQ-migrated-utente**</span><span class="sxs-lookup"><span data-stu-id="3d5e9-234">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="3d5e9-235">**Utente**</span><span class="sxs-lookup"><span data-stu-id="3d5e9-235">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="3d5e9-236">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3d5e9-236">Windows Server 2008 R2</span></span>



| <span data-ttu-id="3d5e9-237">Voce</span><span class="sxs-lookup"><span data-stu-id="3d5e9-237">Entry</span></span> | <span data-ttu-id="3d5e9-238">Valore</span><span class="sxs-lookup"><span data-stu-id="3d5e9-238">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d5e9-239">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="3d5e9-239">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="3d5e9-240">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3d5e9-240">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="3d5e9-241">System-Only</span><span class="sxs-lookup"><span data-stu-id="3d5e9-241">System-Only</span></span>            | <span data-ttu-id="3d5e9-242">Falso</span><span class="sxs-lookup"><span data-stu-id="3d5e9-242">False</span></span>                                                                                         |
| <span data-ttu-id="3d5e9-243">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="3d5e9-243">Is-Single-Valued</span></span>       | <span data-ttu-id="3d5e9-244">Falso</span><span class="sxs-lookup"><span data-stu-id="3d5e9-244">False</span></span>                                                                                         |
| <span data-ttu-id="3d5e9-245">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="3d5e9-245">Is Indexed</span></span>             | <span data-ttu-id="3d5e9-246">Vero</span><span class="sxs-lookup"><span data-stu-id="3d5e9-246">True</span></span>                                                                                          |
| <span data-ttu-id="3d5e9-247">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="3d5e9-247">In Global Catalog</span></span>      | <span data-ttu-id="3d5e9-248">Vero</span><span class="sxs-lookup"><span data-stu-id="3d5e9-248">True</span></span>                                                                                          |
| <span data-ttu-id="3d5e9-249">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="3d5e9-249">NT-Security-Descriptor</span></span> | <span data-ttu-id="3d5e9-250">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="3d5e9-250">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="3d5e9-251">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3d5e9-251">Range-Lower</span></span>            | <span data-ttu-id="3d5e9-252">16</span><span class="sxs-lookup"><span data-stu-id="3d5e9-252">16</span></span>                                                                                            |
| <span data-ttu-id="3d5e9-253">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3d5e9-253">Range-Upper</span></span>            | <span data-ttu-id="3d5e9-254">16</span><span class="sxs-lookup"><span data-stu-id="3d5e9-254">16</span></span>                                                                                            |
| <span data-ttu-id="3d5e9-255">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3d5e9-255">Search-Flags</span></span>           | <span data-ttu-id="3d5e9-256">0x00000001</span><span class="sxs-lookup"><span data-stu-id="3d5e9-256">0x00000001</span></span>                                                                                    |
| <span data-ttu-id="3d5e9-257">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3d5e9-257">System-Flags</span></span>           | <span data-ttu-id="3d5e9-258">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3d5e9-258">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="3d5e9-259">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="3d5e9-259">Classes used in</span></span>        | [<span data-ttu-id="3d5e9-260">**MSMQ-migrated-utente**</span><span class="sxs-lookup"><span data-stu-id="3d5e9-260">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="3d5e9-261">**Utente**</span><span class="sxs-lookup"><span data-stu-id="3d5e9-261">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="3d5e9-262">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3d5e9-262">Windows Server 2012</span></span>



| <span data-ttu-id="3d5e9-263">Voce</span><span class="sxs-lookup"><span data-stu-id="3d5e9-263">Entry</span></span> | <span data-ttu-id="3d5e9-264">Valore</span><span class="sxs-lookup"><span data-stu-id="3d5e9-264">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d5e9-265">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="3d5e9-265">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="3d5e9-266">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3d5e9-266">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="3d5e9-267">System-Only</span><span class="sxs-lookup"><span data-stu-id="3d5e9-267">System-Only</span></span>            | <span data-ttu-id="3d5e9-268">Falso</span><span class="sxs-lookup"><span data-stu-id="3d5e9-268">False</span></span>                                                                                         |
| <span data-ttu-id="3d5e9-269">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="3d5e9-269">Is-Single-Valued</span></span>       | <span data-ttu-id="3d5e9-270">Falso</span><span class="sxs-lookup"><span data-stu-id="3d5e9-270">False</span></span>                                                                                         |
| <span data-ttu-id="3d5e9-271">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="3d5e9-271">Is Indexed</span></span>             | <span data-ttu-id="3d5e9-272">Vero</span><span class="sxs-lookup"><span data-stu-id="3d5e9-272">True</span></span>                                                                                          |
| <span data-ttu-id="3d5e9-273">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="3d5e9-273">In Global Catalog</span></span>      | <span data-ttu-id="3d5e9-274">Vero</span><span class="sxs-lookup"><span data-stu-id="3d5e9-274">True</span></span>                                                                                          |
| <span data-ttu-id="3d5e9-275">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="3d5e9-275">NT-Security-Descriptor</span></span> | <span data-ttu-id="3d5e9-276">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="3d5e9-276">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="3d5e9-277">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3d5e9-277">Range-Lower</span></span>            | <span data-ttu-id="3d5e9-278">16</span><span class="sxs-lookup"><span data-stu-id="3d5e9-278">16</span></span>                                                                                            |
| <span data-ttu-id="3d5e9-279">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3d5e9-279">Range-Upper</span></span>            | <span data-ttu-id="3d5e9-280">16</span><span class="sxs-lookup"><span data-stu-id="3d5e9-280">16</span></span>                                                                                            |
| <span data-ttu-id="3d5e9-281">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3d5e9-281">Search-Flags</span></span>           | <span data-ttu-id="3d5e9-282">0x00000001</span><span class="sxs-lookup"><span data-stu-id="3d5e9-282">0x00000001</span></span>                                                                                    |
| <span data-ttu-id="3d5e9-283">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3d5e9-283">System-Flags</span></span>           | <span data-ttu-id="3d5e9-284">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3d5e9-284">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="3d5e9-285">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="3d5e9-285">Classes used in</span></span>        | [<span data-ttu-id="3d5e9-286">**MSMQ-migrated-utente**</span><span class="sxs-lookup"><span data-stu-id="3d5e9-286">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="3d5e9-287">**Utente**</span><span class="sxs-lookup"><span data-stu-id="3d5e9-287">**User**</span></span>](c-user.md)<br/> |



 

 





