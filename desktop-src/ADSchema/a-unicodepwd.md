---
title: Attributo Unicode-Pwd
description: Password dell'utente in formato unidirezionale Windows NT (OWF). Windows 2000 usa Windows NT OWF. Questa proprietà viene utilizzata solo dal sistema operativo. Si noti che non è possibile derivare la password non crittografata dal modulo OWF della password.
ms.assetid: 07b29a0c-aff2-4abd-8ca8-95f1ce5b566b
ms.tgt_platform: multiple
keywords:
- Schema AD Unicode-Pwd attribute
- Schema AD dell'attributo unicodePwd
topic_type:
- apiref
api_name:
- Unicode-Pwd
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d00a1df180b7a30b56bdf198a78edc77cc99755
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104122643"
---
# <a name="unicode-pwd-attribute"></a><span data-ttu-id="6b0f5-108">Attributo Unicode-Pwd</span><span class="sxs-lookup"><span data-stu-id="6b0f5-108">Unicode-Pwd attribute</span></span>

<span data-ttu-id="6b0f5-109">Password dell'utente in formato unidirezionale Windows NT (OWF).</span><span class="sxs-lookup"><span data-stu-id="6b0f5-109">The password of the user in Windows NT one-way format (OWF).</span></span> <span data-ttu-id="6b0f5-110">Windows 2000 usa Windows NT OWF.</span><span class="sxs-lookup"><span data-stu-id="6b0f5-110">Windows 2000 uses the Windows NT OWF.</span></span> <span data-ttu-id="6b0f5-111">Questa proprietà viene utilizzata solo dal sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="6b0f5-111">This property is used only by the operating system.</span></span> <span data-ttu-id="6b0f5-112">Si noti che non è possibile derivare la password non crittografata dal modulo OWF della password.</span><span class="sxs-lookup"><span data-stu-id="6b0f5-112">Note that you cannot derive the clear password back from the OWF form of the password.</span></span>



| <span data-ttu-id="6b0f5-113">Voce</span><span class="sxs-lookup"><span data-stu-id="6b0f5-113">Entry</span></span> | <span data-ttu-id="6b0f5-114">Valore</span><span class="sxs-lookup"><span data-stu-id="6b0f5-114">Value</span></span> |
|-------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="6b0f5-115">CN</span><span class="sxs-lookup"><span data-stu-id="6b0f5-115">CN</span></span>                | <span data-ttu-id="6b0f5-116">Unicode-Pwd</span><span class="sxs-lookup"><span data-stu-id="6b0f5-116">Unicode-Pwd</span></span>                                                                  |
| <span data-ttu-id="6b0f5-117">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="6b0f5-117">Ldap-Display-Name</span></span> | <span data-ttu-id="6b0f5-118">unicodePwd</span><span class="sxs-lookup"><span data-stu-id="6b0f5-118">unicodePwd</span></span>                                                                   |
| <span data-ttu-id="6b0f5-119">Dimensione</span><span class="sxs-lookup"><span data-stu-id="6b0f5-119">Size</span></span>              | \-                                                                           |
| <span data-ttu-id="6b0f5-120">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="6b0f5-120">Update Privilege</span></span>  | <span data-ttu-id="6b0f5-121">Amministratore di dominio o proprietario dell'account.</span><span class="sxs-lookup"><span data-stu-id="6b0f5-121">Domain administrator or account owner.</span></span>                                       |
| <span data-ttu-id="6b0f5-122">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="6b0f5-122">Update Frequency</span></span>  | <span data-ttu-id="6b0f5-123">Quando viene creato il record dell'utente e ogni volta che è necessario modificare la password.</span><span class="sxs-lookup"><span data-stu-id="6b0f5-123">When the user's record is created and whenever the password needs to change.</span></span> |
| <span data-ttu-id="6b0f5-124">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="6b0f5-124">Attribute-Id</span></span>      | <span data-ttu-id="6b0f5-125">1.2.840.113556.1.4.90</span><span class="sxs-lookup"><span data-stu-id="6b0f5-125">1.2.840.113556.1.4.90</span></span>                                                        |
| <span data-ttu-id="6b0f5-126">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="6b0f5-126">System-Id-Guid</span></span>    | <span data-ttu-id="6b0f5-127">bf9679e1-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="6b0f5-127">bf9679e1-0de6-11d0-a285-00aa003049e2</span></span>                                         |
| <span data-ttu-id="6b0f5-128">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6b0f5-128">Syntax</span></span>            | [<span data-ttu-id="6b0f5-129">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="6b0f5-129">**Object(Replica-Link)**</span></span>](s-object-replica-link.md)                        |



## <a name="implementations"></a><span data-ttu-id="6b0f5-130">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="6b0f5-130">Implementations</span></span>

-   [<span data-ttu-id="6b0f5-131">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="6b0f5-131">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="6b0f5-132">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="6b0f5-132">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="6b0f5-133">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="6b0f5-133">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="6b0f5-134">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="6b0f5-134">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="6b0f5-135">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="6b0f5-135">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="6b0f5-136">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="6b0f5-136">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="6b0f5-137">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="6b0f5-137">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="6b0f5-138">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6b0f5-138">Windows 2000 Server</span></span>



| <span data-ttu-id="6b0f5-139">Voce</span><span class="sxs-lookup"><span data-stu-id="6b0f5-139">Entry</span></span> | <span data-ttu-id="6b0f5-140">Valore</span><span class="sxs-lookup"><span data-stu-id="6b0f5-140">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="6b0f5-141">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="6b0f5-141">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="6b0f5-142">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6b0f5-142">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="6b0f5-143">System-Only</span><span class="sxs-lookup"><span data-stu-id="6b0f5-143">System-Only</span></span>            | <span data-ttu-id="6b0f5-144">Falso</span><span class="sxs-lookup"><span data-stu-id="6b0f5-144">False</span></span>                             |
| <span data-ttu-id="6b0f5-145">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="6b0f5-145">Is-Single-Valued</span></span>       | <span data-ttu-id="6b0f5-146">Vero</span><span class="sxs-lookup"><span data-stu-id="6b0f5-146">True</span></span>                              |
| <span data-ttu-id="6b0f5-147">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="6b0f5-147">Is Indexed</span></span>             | <span data-ttu-id="6b0f5-148">Falso</span><span class="sxs-lookup"><span data-stu-id="6b0f5-148">False</span></span>                             |
| <span data-ttu-id="6b0f5-149">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="6b0f5-149">In Global Catalog</span></span>      | <span data-ttu-id="6b0f5-150">Falso</span><span class="sxs-lookup"><span data-stu-id="6b0f5-150">False</span></span>                             |
| <span data-ttu-id="6b0f5-151">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="6b0f5-151">NT-Security-Descriptor</span></span> | <span data-ttu-id="6b0f5-152">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="6b0f5-152">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="6b0f5-153">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6b0f5-153">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="6b0f5-154">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6b0f5-154">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="6b0f5-155">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6b0f5-155">Search-Flags</span></span>           | <span data-ttu-id="6b0f5-156">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6b0f5-156">0x00000000</span></span>                        |
| <span data-ttu-id="6b0f5-157">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6b0f5-157">System-Flags</span></span>           | <span data-ttu-id="6b0f5-158">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6b0f5-158">0x00000010</span></span>                        |
| <span data-ttu-id="6b0f5-159">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="6b0f5-159">Classes used in</span></span>        | [<span data-ttu-id="6b0f5-160">**Utente**</span><span class="sxs-lookup"><span data-stu-id="6b0f5-160">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="6b0f5-161">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6b0f5-161">Windows Server 2003</span></span>



| <span data-ttu-id="6b0f5-162">Voce</span><span class="sxs-lookup"><span data-stu-id="6b0f5-162">Entry</span></span> | <span data-ttu-id="6b0f5-163">Valore</span><span class="sxs-lookup"><span data-stu-id="6b0f5-163">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="6b0f5-164">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="6b0f5-164">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="6b0f5-165">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6b0f5-165">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="6b0f5-166">System-Only</span><span class="sxs-lookup"><span data-stu-id="6b0f5-166">System-Only</span></span>            | <span data-ttu-id="6b0f5-167">Falso</span><span class="sxs-lookup"><span data-stu-id="6b0f5-167">False</span></span>                             |
| <span data-ttu-id="6b0f5-168">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="6b0f5-168">Is-Single-Valued</span></span>       | <span data-ttu-id="6b0f5-169">Vero</span><span class="sxs-lookup"><span data-stu-id="6b0f5-169">True</span></span>                              |
| <span data-ttu-id="6b0f5-170">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="6b0f5-170">Is Indexed</span></span>             | <span data-ttu-id="6b0f5-171">Falso</span><span class="sxs-lookup"><span data-stu-id="6b0f5-171">False</span></span>                             |
| <span data-ttu-id="6b0f5-172">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="6b0f5-172">In Global Catalog</span></span>      | <span data-ttu-id="6b0f5-173">Falso</span><span class="sxs-lookup"><span data-stu-id="6b0f5-173">False</span></span>                             |
| <span data-ttu-id="6b0f5-174">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="6b0f5-174">NT-Security-Descriptor</span></span> | <span data-ttu-id="6b0f5-175">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="6b0f5-175">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="6b0f5-176">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6b0f5-176">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="6b0f5-177">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6b0f5-177">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="6b0f5-178">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6b0f5-178">Search-Flags</span></span>           | <span data-ttu-id="6b0f5-179">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6b0f5-179">0x00000000</span></span>                        |
| <span data-ttu-id="6b0f5-180">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6b0f5-180">System-Flags</span></span>           | <span data-ttu-id="6b0f5-181">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6b0f5-181">0x00000010</span></span>                        |
| <span data-ttu-id="6b0f5-182">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="6b0f5-182">Classes used in</span></span>        | [<span data-ttu-id="6b0f5-183">**Utente**</span><span class="sxs-lookup"><span data-stu-id="6b0f5-183">**User**</span></span>](c-user.md)<br/> |



## <a name="adam"></a><span data-ttu-id="6b0f5-184">ADAM</span><span class="sxs-lookup"><span data-stu-id="6b0f5-184">ADAM</span></span>



| <span data-ttu-id="6b0f5-185">Voce</span><span class="sxs-lookup"><span data-stu-id="6b0f5-185">Entry</span></span> | <span data-ttu-id="6b0f5-186">Valore</span><span class="sxs-lookup"><span data-stu-id="6b0f5-186">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="6b0f5-187">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="6b0f5-187">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="6b0f5-188">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6b0f5-188">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="6b0f5-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="6b0f5-189">System-Only</span></span>            | <span data-ttu-id="6b0f5-190">Falso</span><span class="sxs-lookup"><span data-stu-id="6b0f5-190">False</span></span>                                                             |
| <span data-ttu-id="6b0f5-191">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="6b0f5-191">Is-Single-Valued</span></span>       | <span data-ttu-id="6b0f5-192">Vero</span><span class="sxs-lookup"><span data-stu-id="6b0f5-192">True</span></span>                                                              |
| <span data-ttu-id="6b0f5-193">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="6b0f5-193">Is Indexed</span></span>             | <span data-ttu-id="6b0f5-194">Falso</span><span class="sxs-lookup"><span data-stu-id="6b0f5-194">False</span></span>                                                             |
| <span data-ttu-id="6b0f5-195">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="6b0f5-195">In Global Catalog</span></span>      | <span data-ttu-id="6b0f5-196">Falso</span><span class="sxs-lookup"><span data-stu-id="6b0f5-196">False</span></span>                                                             |
| <span data-ttu-id="6b0f5-197">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="6b0f5-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="6b0f5-198">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="6b0f5-198">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="6b0f5-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6b0f5-199">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="6b0f5-200">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6b0f5-200">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="6b0f5-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6b0f5-201">Search-Flags</span></span>           | <span data-ttu-id="6b0f5-202">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6b0f5-202">0x00000000</span></span>                                                        |
| <span data-ttu-id="6b0f5-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6b0f5-203">System-Flags</span></span>           | <span data-ttu-id="6b0f5-204">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6b0f5-204">0x00000010</span></span>                                                        |
| <span data-ttu-id="6b0f5-205">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="6b0f5-205">Classes used in</span></span>        | [<span data-ttu-id="6b0f5-206">**ms-DS-associabile-oggetto**</span><span class="sxs-lookup"><span data-stu-id="6b0f5-206">**ms-DS-Bindable-Object**</span></span>](c-msds-bindableobject.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="6b0f5-207">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="6b0f5-207">Windows Server 2003 R2</span></span>



| <span data-ttu-id="6b0f5-208">Voce</span><span class="sxs-lookup"><span data-stu-id="6b0f5-208">Entry</span></span> | <span data-ttu-id="6b0f5-209">Valore</span><span class="sxs-lookup"><span data-stu-id="6b0f5-209">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="6b0f5-210">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="6b0f5-210">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="6b0f5-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6b0f5-211">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="6b0f5-212">System-Only</span><span class="sxs-lookup"><span data-stu-id="6b0f5-212">System-Only</span></span>            | <span data-ttu-id="6b0f5-213">Falso</span><span class="sxs-lookup"><span data-stu-id="6b0f5-213">False</span></span>                             |
| <span data-ttu-id="6b0f5-214">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="6b0f5-214">Is-Single-Valued</span></span>       | <span data-ttu-id="6b0f5-215">Vero</span><span class="sxs-lookup"><span data-stu-id="6b0f5-215">True</span></span>                              |
| <span data-ttu-id="6b0f5-216">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="6b0f5-216">Is Indexed</span></span>             | <span data-ttu-id="6b0f5-217">Falso</span><span class="sxs-lookup"><span data-stu-id="6b0f5-217">False</span></span>                             |
| <span data-ttu-id="6b0f5-218">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="6b0f5-218">In Global Catalog</span></span>      | <span data-ttu-id="6b0f5-219">Falso</span><span class="sxs-lookup"><span data-stu-id="6b0f5-219">False</span></span>                             |
| <span data-ttu-id="6b0f5-220">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="6b0f5-220">NT-Security-Descriptor</span></span> | <span data-ttu-id="6b0f5-221">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="6b0f5-221">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="6b0f5-222">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6b0f5-222">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="6b0f5-223">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6b0f5-223">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="6b0f5-224">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6b0f5-224">Search-Flags</span></span>           | <span data-ttu-id="6b0f5-225">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6b0f5-225">0x00000000</span></span>                        |
| <span data-ttu-id="6b0f5-226">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6b0f5-226">System-Flags</span></span>           | <span data-ttu-id="6b0f5-227">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6b0f5-227">0x00000010</span></span>                        |
| <span data-ttu-id="6b0f5-228">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="6b0f5-228">Classes used in</span></span>        | [<span data-ttu-id="6b0f5-229">**Utente**</span><span class="sxs-lookup"><span data-stu-id="6b0f5-229">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="6b0f5-230">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6b0f5-230">Windows Server 2008</span></span>



| <span data-ttu-id="6b0f5-231">Voce</span><span class="sxs-lookup"><span data-stu-id="6b0f5-231">Entry</span></span> | <span data-ttu-id="6b0f5-232">Valore</span><span class="sxs-lookup"><span data-stu-id="6b0f5-232">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="6b0f5-233">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="6b0f5-233">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="6b0f5-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6b0f5-234">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="6b0f5-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="6b0f5-235">System-Only</span></span>            | <span data-ttu-id="6b0f5-236">Falso</span><span class="sxs-lookup"><span data-stu-id="6b0f5-236">False</span></span>                             |
| <span data-ttu-id="6b0f5-237">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="6b0f5-237">Is-Single-Valued</span></span>       | <span data-ttu-id="6b0f5-238">Vero</span><span class="sxs-lookup"><span data-stu-id="6b0f5-238">True</span></span>                              |
| <span data-ttu-id="6b0f5-239">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="6b0f5-239">Is Indexed</span></span>             | <span data-ttu-id="6b0f5-240">Falso</span><span class="sxs-lookup"><span data-stu-id="6b0f5-240">False</span></span>                             |
| <span data-ttu-id="6b0f5-241">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="6b0f5-241">In Global Catalog</span></span>      | <span data-ttu-id="6b0f5-242">Falso</span><span class="sxs-lookup"><span data-stu-id="6b0f5-242">False</span></span>                             |
| <span data-ttu-id="6b0f5-243">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="6b0f5-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="6b0f5-244">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="6b0f5-244">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="6b0f5-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6b0f5-245">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="6b0f5-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6b0f5-246">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="6b0f5-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6b0f5-247">Search-Flags</span></span>           | <span data-ttu-id="6b0f5-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6b0f5-248">0x00000000</span></span>                        |
| <span data-ttu-id="6b0f5-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6b0f5-249">System-Flags</span></span>           | <span data-ttu-id="6b0f5-250">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6b0f5-250">0x00000010</span></span>                        |
| <span data-ttu-id="6b0f5-251">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="6b0f5-251">Classes used in</span></span>        | [<span data-ttu-id="6b0f5-252">**Utente**</span><span class="sxs-lookup"><span data-stu-id="6b0f5-252">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="6b0f5-253">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6b0f5-253">Windows Server 2008 R2</span></span>



| <span data-ttu-id="6b0f5-254">Voce</span><span class="sxs-lookup"><span data-stu-id="6b0f5-254">Entry</span></span> | <span data-ttu-id="6b0f5-255">Valore</span><span class="sxs-lookup"><span data-stu-id="6b0f5-255">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="6b0f5-256">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="6b0f5-256">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="6b0f5-257">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6b0f5-257">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="6b0f5-258">System-Only</span><span class="sxs-lookup"><span data-stu-id="6b0f5-258">System-Only</span></span>            | <span data-ttu-id="6b0f5-259">Falso</span><span class="sxs-lookup"><span data-stu-id="6b0f5-259">False</span></span>                             |
| <span data-ttu-id="6b0f5-260">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="6b0f5-260">Is-Single-Valued</span></span>       | <span data-ttu-id="6b0f5-261">Vero</span><span class="sxs-lookup"><span data-stu-id="6b0f5-261">True</span></span>                              |
| <span data-ttu-id="6b0f5-262">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="6b0f5-262">Is Indexed</span></span>             | <span data-ttu-id="6b0f5-263">Falso</span><span class="sxs-lookup"><span data-stu-id="6b0f5-263">False</span></span>                             |
| <span data-ttu-id="6b0f5-264">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="6b0f5-264">In Global Catalog</span></span>      | <span data-ttu-id="6b0f5-265">Falso</span><span class="sxs-lookup"><span data-stu-id="6b0f5-265">False</span></span>                             |
| <span data-ttu-id="6b0f5-266">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="6b0f5-266">NT-Security-Descriptor</span></span> | <span data-ttu-id="6b0f5-267">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="6b0f5-267">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="6b0f5-268">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6b0f5-268">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="6b0f5-269">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6b0f5-269">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="6b0f5-270">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6b0f5-270">Search-Flags</span></span>           | <span data-ttu-id="6b0f5-271">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6b0f5-271">0x00000000</span></span>                        |
| <span data-ttu-id="6b0f5-272">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6b0f5-272">System-Flags</span></span>           | <span data-ttu-id="6b0f5-273">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6b0f5-273">0x00000010</span></span>                        |
| <span data-ttu-id="6b0f5-274">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="6b0f5-274">Classes used in</span></span>        | [<span data-ttu-id="6b0f5-275">**Utente**</span><span class="sxs-lookup"><span data-stu-id="6b0f5-275">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="6b0f5-276">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6b0f5-276">Windows Server 2012</span></span>



| <span data-ttu-id="6b0f5-277">Voce</span><span class="sxs-lookup"><span data-stu-id="6b0f5-277">Entry</span></span> | <span data-ttu-id="6b0f5-278">Valore</span><span class="sxs-lookup"><span data-stu-id="6b0f5-278">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="6b0f5-279">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="6b0f5-279">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="6b0f5-280">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6b0f5-280">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="6b0f5-281">System-Only</span><span class="sxs-lookup"><span data-stu-id="6b0f5-281">System-Only</span></span>            | <span data-ttu-id="6b0f5-282">Falso</span><span class="sxs-lookup"><span data-stu-id="6b0f5-282">False</span></span>                             |
| <span data-ttu-id="6b0f5-283">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="6b0f5-283">Is-Single-Valued</span></span>       | <span data-ttu-id="6b0f5-284">Vero</span><span class="sxs-lookup"><span data-stu-id="6b0f5-284">True</span></span>                              |
| <span data-ttu-id="6b0f5-285">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="6b0f5-285">Is Indexed</span></span>             | <span data-ttu-id="6b0f5-286">Falso</span><span class="sxs-lookup"><span data-stu-id="6b0f5-286">False</span></span>                             |
| <span data-ttu-id="6b0f5-287">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="6b0f5-287">In Global Catalog</span></span>      | <span data-ttu-id="6b0f5-288">Falso</span><span class="sxs-lookup"><span data-stu-id="6b0f5-288">False</span></span>                             |
| <span data-ttu-id="6b0f5-289">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="6b0f5-289">NT-Security-Descriptor</span></span> | <span data-ttu-id="6b0f5-290">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="6b0f5-290">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="6b0f5-291">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6b0f5-291">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="6b0f5-292">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6b0f5-292">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="6b0f5-293">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6b0f5-293">Search-Flags</span></span>           | <span data-ttu-id="6b0f5-294">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6b0f5-294">0x00000000</span></span>                        |
| <span data-ttu-id="6b0f5-295">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6b0f5-295">System-Flags</span></span>           | <span data-ttu-id="6b0f5-296">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6b0f5-296">0x00000010</span></span>                        |
| <span data-ttu-id="6b0f5-297">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="6b0f5-297">Classes used in</span></span>        | [<span data-ttu-id="6b0f5-298">**Utente**</span><span class="sxs-lookup"><span data-stu-id="6b0f5-298">**User**</span></span>](c-user.md)<br/> |



 

 





