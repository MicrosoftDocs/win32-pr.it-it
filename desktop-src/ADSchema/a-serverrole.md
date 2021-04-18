---
title: Attributo Server-Role
description: Per la compatibilità con i server precedenti a Windows Server 2000. Un computer che esegue Windows NT Server può essere un server autonomo, un controller di dominio primario (PDC) o un controller di dominio di backup (BDC).
ms.assetid: 0c2e5b18-14ad-4f77-a62c-eeb95aabbb99
ms.tgt_platform: multiple
keywords:
- Schema AD Server-Role attribute
- Schema AD dell'attributo serverRole
topic_type:
- apiref
api_name:
- Server-Role
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58a127a94cd1ecc2bfce3701c11ee2a5e0c2376c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "106303362"
---
# <a name="server-role-attribute"></a><span data-ttu-id="bb3f5-106">Attributo Server-Role</span><span class="sxs-lookup"><span data-stu-id="bb3f5-106">Server-Role attribute</span></span>

<span data-ttu-id="bb3f5-107">Per la compatibilità con i server precedenti a Windows Server 2000.</span><span class="sxs-lookup"><span data-stu-id="bb3f5-107">For compatibility with pre-Windows 2000 Server servers.</span></span> <span data-ttu-id="bb3f5-108">Un computer che esegue Windows NT Server può essere un server autonomo, un controller di dominio primario (PDC) o un controller di dominio di backup (BDC).</span><span class="sxs-lookup"><span data-stu-id="bb3f5-108">A computer running Windows NT Server can be a standalone server, a primary domain controller (PDC), or a backup domain controller (BDC).</span></span>



| <span data-ttu-id="bb3f5-109">Voce</span><span class="sxs-lookup"><span data-stu-id="bb3f5-109">Entry</span></span> | <span data-ttu-id="bb3f5-110">Valore</span><span class="sxs-lookup"><span data-stu-id="bb3f5-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="bb3f5-111">CN</span><span class="sxs-lookup"><span data-stu-id="bb3f5-111">CN</span></span>                | <span data-ttu-id="bb3f5-112">Server-Role</span><span class="sxs-lookup"><span data-stu-id="bb3f5-112">Server-Role</span></span>                          |
| <span data-ttu-id="bb3f5-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="bb3f5-113">Ldap-Display-Name</span></span> | <span data-ttu-id="bb3f5-114">serverRole</span><span class="sxs-lookup"><span data-stu-id="bb3f5-114">serverRole</span></span>                           |
| <span data-ttu-id="bb3f5-115">Dimensione</span><span class="sxs-lookup"><span data-stu-id="bb3f5-115">Size</span></span>              | \-                                   |
| <span data-ttu-id="bb3f5-116">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="bb3f5-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="bb3f5-117">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="bb3f5-117">Update Frequency</span></span>  | <span data-ttu-id="bb3f5-118">4 byte</span><span class="sxs-lookup"><span data-stu-id="bb3f5-118">4 bytes</span></span>                              |
| <span data-ttu-id="bb3f5-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="bb3f5-119">Attribute-Id</span></span>      | <span data-ttu-id="bb3f5-120">1.2.840.113556.1.4.157</span><span class="sxs-lookup"><span data-stu-id="bb3f5-120">1.2.840.113556.1.4.157</span></span>               |
| <span data-ttu-id="bb3f5-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="bb3f5-121">System-Id-Guid</span></span>    | <span data-ttu-id="bb3f5-122">bf967a33-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="bb3f5-122">bf967a33-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="bb3f5-123">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bb3f5-123">Syntax</span></span>            | [<span data-ttu-id="bb3f5-124">**Enumerazione**</span><span class="sxs-lookup"><span data-stu-id="bb3f5-124">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="bb3f5-125">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="bb3f5-125">Implementations</span></span>

-   [<span data-ttu-id="bb3f5-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="bb3f5-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="bb3f5-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="bb3f5-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="bb3f5-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="bb3f5-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="bb3f5-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="bb3f5-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="bb3f5-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="bb3f5-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="bb3f5-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="bb3f5-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="bb3f5-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="bb3f5-132">Windows 2000 Server</span></span>



| <span data-ttu-id="bb3f5-133">Voce</span><span class="sxs-lookup"><span data-stu-id="bb3f5-133">Entry</span></span> | <span data-ttu-id="bb3f5-134">Valore</span><span class="sxs-lookup"><span data-stu-id="bb3f5-134">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="bb3f5-135">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="bb3f5-135">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="bb3f5-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bb3f5-136">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="bb3f5-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="bb3f5-137">System-Only</span></span>            | <span data-ttu-id="bb3f5-138">Falso</span><span class="sxs-lookup"><span data-stu-id="bb3f5-138">False</span></span>                                                 |
| <span data-ttu-id="bb3f5-139">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="bb3f5-139">Is-Single-Valued</span></span>       | <span data-ttu-id="bb3f5-140">Vero</span><span class="sxs-lookup"><span data-stu-id="bb3f5-140">True</span></span>                                                  |
| <span data-ttu-id="bb3f5-141">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="bb3f5-141">Is Indexed</span></span>             | <span data-ttu-id="bb3f5-142">Falso</span><span class="sxs-lookup"><span data-stu-id="bb3f5-142">False</span></span>                                                 |
| <span data-ttu-id="bb3f5-143">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="bb3f5-143">In Global Catalog</span></span>      | <span data-ttu-id="bb3f5-144">Falso</span><span class="sxs-lookup"><span data-stu-id="bb3f5-144">False</span></span>                                                 |
| <span data-ttu-id="bb3f5-145">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="bb3f5-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="bb3f5-146">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="bb3f5-146">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="bb3f5-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bb3f5-147">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="bb3f5-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bb3f5-148">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="bb3f5-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bb3f5-149">Search-Flags</span></span>           | <span data-ttu-id="bb3f5-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bb3f5-150">0x00000000</span></span>                                            |
| <span data-ttu-id="bb3f5-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bb3f5-151">System-Flags</span></span>           | <span data-ttu-id="bb3f5-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bb3f5-152">0x00000010</span></span>                                            |
| <span data-ttu-id="bb3f5-153">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="bb3f5-153">Classes used in</span></span>        | [<span data-ttu-id="bb3f5-154">**Sam-dominio-base**</span><span class="sxs-lookup"><span data-stu-id="bb3f5-154">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="bb3f5-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="bb3f5-155">Windows Server 2003</span></span>



| <span data-ttu-id="bb3f5-156">Voce</span><span class="sxs-lookup"><span data-stu-id="bb3f5-156">Entry</span></span> | <span data-ttu-id="bb3f5-157">Valore</span><span class="sxs-lookup"><span data-stu-id="bb3f5-157">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="bb3f5-158">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="bb3f5-158">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="bb3f5-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bb3f5-159">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="bb3f5-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="bb3f5-160">System-Only</span></span>            | <span data-ttu-id="bb3f5-161">Falso</span><span class="sxs-lookup"><span data-stu-id="bb3f5-161">False</span></span>                                                 |
| <span data-ttu-id="bb3f5-162">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="bb3f5-162">Is-Single-Valued</span></span>       | <span data-ttu-id="bb3f5-163">Vero</span><span class="sxs-lookup"><span data-stu-id="bb3f5-163">True</span></span>                                                  |
| <span data-ttu-id="bb3f5-164">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="bb3f5-164">Is Indexed</span></span>             | <span data-ttu-id="bb3f5-165">Falso</span><span class="sxs-lookup"><span data-stu-id="bb3f5-165">False</span></span>                                                 |
| <span data-ttu-id="bb3f5-166">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="bb3f5-166">In Global Catalog</span></span>      | <span data-ttu-id="bb3f5-167">Falso</span><span class="sxs-lookup"><span data-stu-id="bb3f5-167">False</span></span>                                                 |
| <span data-ttu-id="bb3f5-168">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="bb3f5-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="bb3f5-169">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="bb3f5-169">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="bb3f5-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bb3f5-170">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="bb3f5-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bb3f5-171">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="bb3f5-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bb3f5-172">Search-Flags</span></span>           | <span data-ttu-id="bb3f5-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bb3f5-173">0x00000000</span></span>                                            |
| <span data-ttu-id="bb3f5-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bb3f5-174">System-Flags</span></span>           | <span data-ttu-id="bb3f5-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bb3f5-175">0x00000010</span></span>                                            |
| <span data-ttu-id="bb3f5-176">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="bb3f5-176">Classes used in</span></span>        | [<span data-ttu-id="bb3f5-177">**Sam-dominio-base**</span><span class="sxs-lookup"><span data-stu-id="bb3f5-177">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="bb3f5-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="bb3f5-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="bb3f5-179">Voce</span><span class="sxs-lookup"><span data-stu-id="bb3f5-179">Entry</span></span> | <span data-ttu-id="bb3f5-180">Valore</span><span class="sxs-lookup"><span data-stu-id="bb3f5-180">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="bb3f5-181">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="bb3f5-181">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="bb3f5-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bb3f5-182">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="bb3f5-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="bb3f5-183">System-Only</span></span>            | <span data-ttu-id="bb3f5-184">Falso</span><span class="sxs-lookup"><span data-stu-id="bb3f5-184">False</span></span>                                                 |
| <span data-ttu-id="bb3f5-185">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="bb3f5-185">Is-Single-Valued</span></span>       | <span data-ttu-id="bb3f5-186">Vero</span><span class="sxs-lookup"><span data-stu-id="bb3f5-186">True</span></span>                                                  |
| <span data-ttu-id="bb3f5-187">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="bb3f5-187">Is Indexed</span></span>             | <span data-ttu-id="bb3f5-188">Falso</span><span class="sxs-lookup"><span data-stu-id="bb3f5-188">False</span></span>                                                 |
| <span data-ttu-id="bb3f5-189">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="bb3f5-189">In Global Catalog</span></span>      | <span data-ttu-id="bb3f5-190">Falso</span><span class="sxs-lookup"><span data-stu-id="bb3f5-190">False</span></span>                                                 |
| <span data-ttu-id="bb3f5-191">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="bb3f5-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="bb3f5-192">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="bb3f5-192">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="bb3f5-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bb3f5-193">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="bb3f5-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bb3f5-194">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="bb3f5-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bb3f5-195">Search-Flags</span></span>           | <span data-ttu-id="bb3f5-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bb3f5-196">0x00000000</span></span>                                            |
| <span data-ttu-id="bb3f5-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bb3f5-197">System-Flags</span></span>           | <span data-ttu-id="bb3f5-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bb3f5-198">0x00000010</span></span>                                            |
| <span data-ttu-id="bb3f5-199">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="bb3f5-199">Classes used in</span></span>        | [<span data-ttu-id="bb3f5-200">**Sam-dominio-base**</span><span class="sxs-lookup"><span data-stu-id="bb3f5-200">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="bb3f5-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bb3f5-201">Windows Server 2008</span></span>



| <span data-ttu-id="bb3f5-202">Voce</span><span class="sxs-lookup"><span data-stu-id="bb3f5-202">Entry</span></span> | <span data-ttu-id="bb3f5-203">Valore</span><span class="sxs-lookup"><span data-stu-id="bb3f5-203">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="bb3f5-204">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="bb3f5-204">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="bb3f5-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bb3f5-205">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="bb3f5-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="bb3f5-206">System-Only</span></span>            | <span data-ttu-id="bb3f5-207">Falso</span><span class="sxs-lookup"><span data-stu-id="bb3f5-207">False</span></span>                                                 |
| <span data-ttu-id="bb3f5-208">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="bb3f5-208">Is-Single-Valued</span></span>       | <span data-ttu-id="bb3f5-209">Vero</span><span class="sxs-lookup"><span data-stu-id="bb3f5-209">True</span></span>                                                  |
| <span data-ttu-id="bb3f5-210">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="bb3f5-210">Is Indexed</span></span>             | <span data-ttu-id="bb3f5-211">Falso</span><span class="sxs-lookup"><span data-stu-id="bb3f5-211">False</span></span>                                                 |
| <span data-ttu-id="bb3f5-212">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="bb3f5-212">In Global Catalog</span></span>      | <span data-ttu-id="bb3f5-213">Falso</span><span class="sxs-lookup"><span data-stu-id="bb3f5-213">False</span></span>                                                 |
| <span data-ttu-id="bb3f5-214">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="bb3f5-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="bb3f5-215">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="bb3f5-215">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="bb3f5-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bb3f5-216">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="bb3f5-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bb3f5-217">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="bb3f5-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bb3f5-218">Search-Flags</span></span>           | <span data-ttu-id="bb3f5-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bb3f5-219">0x00000000</span></span>                                            |
| <span data-ttu-id="bb3f5-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bb3f5-220">System-Flags</span></span>           | <span data-ttu-id="bb3f5-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bb3f5-221">0x00000010</span></span>                                            |
| <span data-ttu-id="bb3f5-222">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="bb3f5-222">Classes used in</span></span>        | [<span data-ttu-id="bb3f5-223">**Sam-dominio-base**</span><span class="sxs-lookup"><span data-stu-id="bb3f5-223">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="bb3f5-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="bb3f5-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="bb3f5-225">Voce</span><span class="sxs-lookup"><span data-stu-id="bb3f5-225">Entry</span></span> | <span data-ttu-id="bb3f5-226">Valore</span><span class="sxs-lookup"><span data-stu-id="bb3f5-226">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="bb3f5-227">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="bb3f5-227">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="bb3f5-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bb3f5-228">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="bb3f5-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="bb3f5-229">System-Only</span></span>            | <span data-ttu-id="bb3f5-230">Falso</span><span class="sxs-lookup"><span data-stu-id="bb3f5-230">False</span></span>                                                 |
| <span data-ttu-id="bb3f5-231">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="bb3f5-231">Is-Single-Valued</span></span>       | <span data-ttu-id="bb3f5-232">Vero</span><span class="sxs-lookup"><span data-stu-id="bb3f5-232">True</span></span>                                                  |
| <span data-ttu-id="bb3f5-233">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="bb3f5-233">Is Indexed</span></span>             | <span data-ttu-id="bb3f5-234">Falso</span><span class="sxs-lookup"><span data-stu-id="bb3f5-234">False</span></span>                                                 |
| <span data-ttu-id="bb3f5-235">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="bb3f5-235">In Global Catalog</span></span>      | <span data-ttu-id="bb3f5-236">Falso</span><span class="sxs-lookup"><span data-stu-id="bb3f5-236">False</span></span>                                                 |
| <span data-ttu-id="bb3f5-237">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="bb3f5-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="bb3f5-238">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="bb3f5-238">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="bb3f5-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bb3f5-239">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="bb3f5-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bb3f5-240">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="bb3f5-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bb3f5-241">Search-Flags</span></span>           | <span data-ttu-id="bb3f5-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bb3f5-242">0x00000000</span></span>                                            |
| <span data-ttu-id="bb3f5-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bb3f5-243">System-Flags</span></span>           | <span data-ttu-id="bb3f5-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bb3f5-244">0x00000010</span></span>                                            |
| <span data-ttu-id="bb3f5-245">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="bb3f5-245">Classes used in</span></span>        | [<span data-ttu-id="bb3f5-246">**Sam-dominio-base**</span><span class="sxs-lookup"><span data-stu-id="bb3f5-246">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="bb3f5-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="bb3f5-247">Windows Server 2012</span></span>



| <span data-ttu-id="bb3f5-248">Voce</span><span class="sxs-lookup"><span data-stu-id="bb3f5-248">Entry</span></span> | <span data-ttu-id="bb3f5-249">Valore</span><span class="sxs-lookup"><span data-stu-id="bb3f5-249">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="bb3f5-250">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="bb3f5-250">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="bb3f5-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bb3f5-251">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="bb3f5-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="bb3f5-252">System-Only</span></span>            | <span data-ttu-id="bb3f5-253">Falso</span><span class="sxs-lookup"><span data-stu-id="bb3f5-253">False</span></span>                                                 |
| <span data-ttu-id="bb3f5-254">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="bb3f5-254">Is-Single-Valued</span></span>       | <span data-ttu-id="bb3f5-255">Vero</span><span class="sxs-lookup"><span data-stu-id="bb3f5-255">True</span></span>                                                  |
| <span data-ttu-id="bb3f5-256">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="bb3f5-256">Is Indexed</span></span>             | <span data-ttu-id="bb3f5-257">Falso</span><span class="sxs-lookup"><span data-stu-id="bb3f5-257">False</span></span>                                                 |
| <span data-ttu-id="bb3f5-258">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="bb3f5-258">In Global Catalog</span></span>      | <span data-ttu-id="bb3f5-259">Falso</span><span class="sxs-lookup"><span data-stu-id="bb3f5-259">False</span></span>                                                 |
| <span data-ttu-id="bb3f5-260">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="bb3f5-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="bb3f5-261">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="bb3f5-261">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="bb3f5-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bb3f5-262">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="bb3f5-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bb3f5-263">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="bb3f5-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bb3f5-264">Search-Flags</span></span>           | <span data-ttu-id="bb3f5-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bb3f5-265">0x00000000</span></span>                                            |
| <span data-ttu-id="bb3f5-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bb3f5-266">System-Flags</span></span>           | <span data-ttu-id="bb3f5-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bb3f5-267">0x00000010</span></span>                                            |
| <span data-ttu-id="bb3f5-268">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="bb3f5-268">Classes used in</span></span>        | [<span data-ttu-id="bb3f5-269">**Sam-dominio-base**</span><span class="sxs-lookup"><span data-stu-id="bb3f5-269">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



 

 





