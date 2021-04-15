---
title: attributo ms-DS-cache-Membership
description: L'attributo ms-DS-cache-Membership viene utilizzato da Gestione account di sicurezza per l'espansione del gruppo durante la valutazione del token.
ms.assetid: e54c5d55-d292-4a6e-942a-3818f5d75301
ms.tgt_platform: multiple
keywords:
- Schema di AD dell'attributo ms-DS-Cached-Membership
- msDS-cache-attributo appartenenza-schema AD
topic_type:
- apiref
api_name:
- ms-DS-Cached-Membership
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 936c5c21d33d19ee51dba7f1dec0b03299cee346
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104520174"
---
# <a name="ms-ds-cached-membership-attribute"></a><span data-ttu-id="0f29a-105">attributo ms-DS-cache-Membership</span><span class="sxs-lookup"><span data-stu-id="0f29a-105">ms-DS-Cached-Membership attribute</span></span>

<span data-ttu-id="0f29a-106">L'attributo **ms-DS-cache-Membership** viene utilizzato da Gestione account di sicurezza per l'espansione del gruppo durante la valutazione del token.</span><span class="sxs-lookup"><span data-stu-id="0f29a-106">The **ms-DS-Cached-Membership** attribute is used by the Security Accounts Manager for group expansion during token evaluation.</span></span>



| <span data-ttu-id="0f29a-107">Voce</span><span class="sxs-lookup"><span data-stu-id="0f29a-107">Entry</span></span> | <span data-ttu-id="0f29a-108">Valore</span><span class="sxs-lookup"><span data-stu-id="0f29a-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="0f29a-109">CN</span><span class="sxs-lookup"><span data-stu-id="0f29a-109">CN</span></span>                | <span data-ttu-id="0f29a-110">ms-DS-memorizzato nella cache-appartenenza</span><span class="sxs-lookup"><span data-stu-id="0f29a-110">ms-DS-Cached-Membership</span></span>                               |
| <span data-ttu-id="0f29a-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="0f29a-111">Ldap-Display-Name</span></span> | <span data-ttu-id="0f29a-112">msDS-memorizzato nella cache-appartenenza</span><span class="sxs-lookup"><span data-stu-id="0f29a-112">msDS-Cached-Membership</span></span>                                |
| <span data-ttu-id="0f29a-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="0f29a-113">Size</span></span>              | <span data-ttu-id="0f29a-114">BLOB binario costituito da un massimo di 3 kilobyte.</span><span class="sxs-lookup"><span data-stu-id="0f29a-114">Binary BLOB of up to 3 kilobytes.</span></span>                     |
| <span data-ttu-id="0f29a-115">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="0f29a-115">Update Privilege</span></span>  | <span data-ttu-id="0f29a-116">Questo valore viene impostato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="0f29a-116">This value is set by the system.</span></span>                      |
| <span data-ttu-id="0f29a-117">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="0f29a-117">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="0f29a-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="0f29a-118">Attribute-Id</span></span>      | <span data-ttu-id="0f29a-119">1.2.840.113556.1.4.1441</span><span class="sxs-lookup"><span data-stu-id="0f29a-119">1.2.840.113556.1.4.1441</span></span>                               |
| <span data-ttu-id="0f29a-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="0f29a-120">System-Id-Guid</span></span>    | <span data-ttu-id="0f29a-121">69cab008-cdd4-4bc9-bab8-0ff37efe1b20</span><span class="sxs-lookup"><span data-stu-id="0f29a-121">69cab008-cdd4-4bc9-bab8-0ff37efe1b20</span></span>                  |
| <span data-ttu-id="0f29a-122">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0f29a-122">Syntax</span></span>            | [<span data-ttu-id="0f29a-123">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="0f29a-123">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="0f29a-124">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="0f29a-124">Implementations</span></span>

-   [<span data-ttu-id="0f29a-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="0f29a-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="0f29a-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="0f29a-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="0f29a-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="0f29a-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="0f29a-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="0f29a-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="0f29a-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="0f29a-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="0f29a-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0f29a-130">Windows Server 2003</span></span>



| <span data-ttu-id="0f29a-131">Voce</span><span class="sxs-lookup"><span data-stu-id="0f29a-131">Entry</span></span> | <span data-ttu-id="0f29a-132">Valore</span><span class="sxs-lookup"><span data-stu-id="0f29a-132">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="0f29a-133">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="0f29a-133">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="0f29a-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0f29a-134">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="0f29a-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="0f29a-135">System-Only</span></span>            | <span data-ttu-id="0f29a-136">Falso</span><span class="sxs-lookup"><span data-stu-id="0f29a-136">False</span></span>                             |
| <span data-ttu-id="0f29a-137">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="0f29a-137">Is-Single-Valued</span></span>       | <span data-ttu-id="0f29a-138">Vero</span><span class="sxs-lookup"><span data-stu-id="0f29a-138">True</span></span>                              |
| <span data-ttu-id="0f29a-139">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="0f29a-139">Is Indexed</span></span>             | <span data-ttu-id="0f29a-140">Falso</span><span class="sxs-lookup"><span data-stu-id="0f29a-140">False</span></span>                             |
| <span data-ttu-id="0f29a-141">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="0f29a-141">In Global Catalog</span></span>      | <span data-ttu-id="0f29a-142">Falso</span><span class="sxs-lookup"><span data-stu-id="0f29a-142">False</span></span>                             |
| <span data-ttu-id="0f29a-143">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="0f29a-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="0f29a-144">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="0f29a-144">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="0f29a-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0f29a-145">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="0f29a-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0f29a-146">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="0f29a-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0f29a-147">Search-Flags</span></span>           | <span data-ttu-id="0f29a-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0f29a-148">0x00000000</span></span>                        |
| <span data-ttu-id="0f29a-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0f29a-149">System-Flags</span></span>           | <span data-ttu-id="0f29a-150">0x00000011</span><span class="sxs-lookup"><span data-stu-id="0f29a-150">0x00000011</span></span>                        |
| <span data-ttu-id="0f29a-151">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="0f29a-151">Classes used in</span></span>        | [<span data-ttu-id="0f29a-152">**Utente**</span><span class="sxs-lookup"><span data-stu-id="0f29a-152">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="0f29a-153">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="0f29a-153">Windows Server 2003 R2</span></span>



| <span data-ttu-id="0f29a-154">Voce</span><span class="sxs-lookup"><span data-stu-id="0f29a-154">Entry</span></span> | <span data-ttu-id="0f29a-155">Valore</span><span class="sxs-lookup"><span data-stu-id="0f29a-155">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="0f29a-156">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="0f29a-156">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="0f29a-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0f29a-157">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="0f29a-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="0f29a-158">System-Only</span></span>            | <span data-ttu-id="0f29a-159">Falso</span><span class="sxs-lookup"><span data-stu-id="0f29a-159">False</span></span>                             |
| <span data-ttu-id="0f29a-160">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="0f29a-160">Is-Single-Valued</span></span>       | <span data-ttu-id="0f29a-161">Vero</span><span class="sxs-lookup"><span data-stu-id="0f29a-161">True</span></span>                              |
| <span data-ttu-id="0f29a-162">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="0f29a-162">Is Indexed</span></span>             | <span data-ttu-id="0f29a-163">Falso</span><span class="sxs-lookup"><span data-stu-id="0f29a-163">False</span></span>                             |
| <span data-ttu-id="0f29a-164">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="0f29a-164">In Global Catalog</span></span>      | <span data-ttu-id="0f29a-165">Falso</span><span class="sxs-lookup"><span data-stu-id="0f29a-165">False</span></span>                             |
| <span data-ttu-id="0f29a-166">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="0f29a-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="0f29a-167">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="0f29a-167">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="0f29a-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0f29a-168">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="0f29a-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0f29a-169">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="0f29a-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0f29a-170">Search-Flags</span></span>           | <span data-ttu-id="0f29a-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0f29a-171">0x00000000</span></span>                        |
| <span data-ttu-id="0f29a-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0f29a-172">System-Flags</span></span>           | <span data-ttu-id="0f29a-173">0x00000011</span><span class="sxs-lookup"><span data-stu-id="0f29a-173">0x00000011</span></span>                        |
| <span data-ttu-id="0f29a-174">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="0f29a-174">Classes used in</span></span>        | [<span data-ttu-id="0f29a-175">**Utente**</span><span class="sxs-lookup"><span data-stu-id="0f29a-175">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="0f29a-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0f29a-176">Windows Server 2008</span></span>



| <span data-ttu-id="0f29a-177">Voce</span><span class="sxs-lookup"><span data-stu-id="0f29a-177">Entry</span></span> | <span data-ttu-id="0f29a-178">Valore</span><span class="sxs-lookup"><span data-stu-id="0f29a-178">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="0f29a-179">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="0f29a-179">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="0f29a-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0f29a-180">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="0f29a-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="0f29a-181">System-Only</span></span>            | <span data-ttu-id="0f29a-182">Falso</span><span class="sxs-lookup"><span data-stu-id="0f29a-182">False</span></span>                             |
| <span data-ttu-id="0f29a-183">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="0f29a-183">Is-Single-Valued</span></span>       | <span data-ttu-id="0f29a-184">Vero</span><span class="sxs-lookup"><span data-stu-id="0f29a-184">True</span></span>                              |
| <span data-ttu-id="0f29a-185">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="0f29a-185">Is Indexed</span></span>             | <span data-ttu-id="0f29a-186">Falso</span><span class="sxs-lookup"><span data-stu-id="0f29a-186">False</span></span>                             |
| <span data-ttu-id="0f29a-187">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="0f29a-187">In Global Catalog</span></span>      | <span data-ttu-id="0f29a-188">Falso</span><span class="sxs-lookup"><span data-stu-id="0f29a-188">False</span></span>                             |
| <span data-ttu-id="0f29a-189">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="0f29a-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="0f29a-190">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="0f29a-190">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="0f29a-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0f29a-191">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="0f29a-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0f29a-192">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="0f29a-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0f29a-193">Search-Flags</span></span>           | <span data-ttu-id="0f29a-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0f29a-194">0x00000000</span></span>                        |
| <span data-ttu-id="0f29a-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0f29a-195">System-Flags</span></span>           | <span data-ttu-id="0f29a-196">0x00000011</span><span class="sxs-lookup"><span data-stu-id="0f29a-196">0x00000011</span></span>                        |
| <span data-ttu-id="0f29a-197">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="0f29a-197">Classes used in</span></span>        | [<span data-ttu-id="0f29a-198">**Utente**</span><span class="sxs-lookup"><span data-stu-id="0f29a-198">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="0f29a-199">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="0f29a-199">Windows Server 2008 R2</span></span>



| <span data-ttu-id="0f29a-200">Voce</span><span class="sxs-lookup"><span data-stu-id="0f29a-200">Entry</span></span> | <span data-ttu-id="0f29a-201">Valore</span><span class="sxs-lookup"><span data-stu-id="0f29a-201">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="0f29a-202">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="0f29a-202">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="0f29a-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0f29a-203">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="0f29a-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="0f29a-204">System-Only</span></span>            | <span data-ttu-id="0f29a-205">Falso</span><span class="sxs-lookup"><span data-stu-id="0f29a-205">False</span></span>                             |
| <span data-ttu-id="0f29a-206">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="0f29a-206">Is-Single-Valued</span></span>       | <span data-ttu-id="0f29a-207">Vero</span><span class="sxs-lookup"><span data-stu-id="0f29a-207">True</span></span>                              |
| <span data-ttu-id="0f29a-208">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="0f29a-208">Is Indexed</span></span>             | <span data-ttu-id="0f29a-209">Falso</span><span class="sxs-lookup"><span data-stu-id="0f29a-209">False</span></span>                             |
| <span data-ttu-id="0f29a-210">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="0f29a-210">In Global Catalog</span></span>      | <span data-ttu-id="0f29a-211">Falso</span><span class="sxs-lookup"><span data-stu-id="0f29a-211">False</span></span>                             |
| <span data-ttu-id="0f29a-212">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="0f29a-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="0f29a-213">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="0f29a-213">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="0f29a-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0f29a-214">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="0f29a-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0f29a-215">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="0f29a-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0f29a-216">Search-Flags</span></span>           | <span data-ttu-id="0f29a-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0f29a-217">0x00000000</span></span>                        |
| <span data-ttu-id="0f29a-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0f29a-218">System-Flags</span></span>           | <span data-ttu-id="0f29a-219">0x00000011</span><span class="sxs-lookup"><span data-stu-id="0f29a-219">0x00000011</span></span>                        |
| <span data-ttu-id="0f29a-220">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="0f29a-220">Classes used in</span></span>        | [<span data-ttu-id="0f29a-221">**Utente**</span><span class="sxs-lookup"><span data-stu-id="0f29a-221">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="0f29a-222">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0f29a-222">Windows Server 2012</span></span>



| <span data-ttu-id="0f29a-223">Voce</span><span class="sxs-lookup"><span data-stu-id="0f29a-223">Entry</span></span> | <span data-ttu-id="0f29a-224">Valore</span><span class="sxs-lookup"><span data-stu-id="0f29a-224">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="0f29a-225">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="0f29a-225">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="0f29a-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0f29a-226">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="0f29a-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="0f29a-227">System-Only</span></span>            | <span data-ttu-id="0f29a-228">Falso</span><span class="sxs-lookup"><span data-stu-id="0f29a-228">False</span></span>                             |
| <span data-ttu-id="0f29a-229">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="0f29a-229">Is-Single-Valued</span></span>       | <span data-ttu-id="0f29a-230">Vero</span><span class="sxs-lookup"><span data-stu-id="0f29a-230">True</span></span>                              |
| <span data-ttu-id="0f29a-231">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="0f29a-231">Is Indexed</span></span>             | <span data-ttu-id="0f29a-232">Falso</span><span class="sxs-lookup"><span data-stu-id="0f29a-232">False</span></span>                             |
| <span data-ttu-id="0f29a-233">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="0f29a-233">In Global Catalog</span></span>      | <span data-ttu-id="0f29a-234">Falso</span><span class="sxs-lookup"><span data-stu-id="0f29a-234">False</span></span>                             |
| <span data-ttu-id="0f29a-235">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="0f29a-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="0f29a-236">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="0f29a-236">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="0f29a-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0f29a-237">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="0f29a-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0f29a-238">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="0f29a-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0f29a-239">Search-Flags</span></span>           | <span data-ttu-id="0f29a-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0f29a-240">0x00000000</span></span>                        |
| <span data-ttu-id="0f29a-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0f29a-241">System-Flags</span></span>           | <span data-ttu-id="0f29a-242">0x00000011</span><span class="sxs-lookup"><span data-stu-id="0f29a-242">0x00000011</span></span>                        |
| <span data-ttu-id="0f29a-243">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="0f29a-243">Classes used in</span></span>        | [<span data-ttu-id="0f29a-244">**Utente**</span><span class="sxs-lookup"><span data-stu-id="0f29a-244">**User**</span></span>](c-user.md)<br/> |



 

 





