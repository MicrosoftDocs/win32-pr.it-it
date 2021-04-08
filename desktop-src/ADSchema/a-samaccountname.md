---
title: Attributo SAM-account-name
description: Nome di accesso utilizzato per supportare client e server che eseguono versioni precedenti del sistema operativo, ad esempio Windows NT 4,0, Windows 95, Windows 98 e LAN Manager.
ms.assetid: dc661e59-9a36-4d2b-93f0-f88edf7efd66
ms.tgt_platform: multiple
keywords:
- Attributo SAM-account-name-schema AD
- Schema AD dell'attributo sAMAccountName
topic_type:
- apiref
api_name:
- SAM-Account-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cb64cba7825c3b4400641cdc5c62890f64bc299
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103875541"
---
# <a name="sam-account-name-attribute"></a><span data-ttu-id="bb420-105">Attributo SAM-account-name</span><span class="sxs-lookup"><span data-stu-id="bb420-105">SAM-Account-Name attribute</span></span>

<span data-ttu-id="bb420-106">Nome di accesso utilizzato per supportare client e server che eseguono versioni precedenti del sistema operativo, ad esempio Windows NT 4,0, Windows 95, Windows 98 e LAN Manager.</span><span class="sxs-lookup"><span data-stu-id="bb420-106">The logon name used to support clients and servers running earlier versions of the operating system, such as Windows NT 4.0, Windows 95, Windows 98, and LAN Manager.</span></span>

<span data-ttu-id="bb420-107">Questo attributo deve essere composto da un massimo di 20 caratteri per supportare i client precedenti e non può contenere i caratteri seguenti:</span><span class="sxs-lookup"><span data-stu-id="bb420-107">This attribute must be 20 characters or less to support earlier clients, and cannot contain any of these characters:</span></span>

-   <span data-ttu-id="bb420-108">"/ \\ \[ \] : ; \| = , + \* ?</span><span class="sxs-lookup"><span data-stu-id="bb420-108">"/ \\ \[ \] : ; \| = , + \* ?</span></span> <span data-ttu-id="bb420-109">< ></span><span class="sxs-lookup"><span data-stu-id="bb420-109">< ></span></span>



| <span data-ttu-id="bb420-110">Voce</span><span class="sxs-lookup"><span data-stu-id="bb420-110">Entry</span></span> | <span data-ttu-id="bb420-111">Valore</span><span class="sxs-lookup"><span data-stu-id="bb420-111">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb420-112">CN</span><span class="sxs-lookup"><span data-stu-id="bb420-112">CN</span></span>                | <span data-ttu-id="bb420-113">Nome account SAM</span><span class="sxs-lookup"><span data-stu-id="bb420-113">SAM-Account-Name</span></span>                                                                         |
| <span data-ttu-id="bb420-114">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="bb420-114">Ldap-Display-Name</span></span> | <span data-ttu-id="bb420-115">sAMAccountName</span><span class="sxs-lookup"><span data-stu-id="bb420-115">sAMAccountName</span></span>                                                                           |
| <span data-ttu-id="bb420-116">Dimensione</span><span class="sxs-lookup"><span data-stu-id="bb420-116">Size</span></span>              | <span data-ttu-id="bb420-117">almeno 20 caratteri.</span><span class="sxs-lookup"><span data-stu-id="bb420-117">20 characters or less.</span></span>                                                                   |
| <span data-ttu-id="bb420-118">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="bb420-118">Update Privilege</span></span>  | <span data-ttu-id="bb420-119">Amministratore di dominio</span><span class="sxs-lookup"><span data-stu-id="bb420-119">Domain administrator</span></span>                                                                     |
| <span data-ttu-id="bb420-120">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="bb420-120">Update Frequency</span></span>  | <span data-ttu-id="bb420-121">Questo valore deve essere assegnato quando il record dell'account viene creato e non deve essere modificato.</span><span class="sxs-lookup"><span data-stu-id="bb420-121">This value should be assigned when the account record is created, and should not change.</span></span> |
| <span data-ttu-id="bb420-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="bb420-122">Attribute-Id</span></span>      | <span data-ttu-id="bb420-123">1.2.840.113556.1.4.221</span><span class="sxs-lookup"><span data-stu-id="bb420-123">1.2.840.113556.1.4.221</span></span>                                                                   |
| <span data-ttu-id="bb420-124">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="bb420-124">System-Id-Guid</span></span>    | <span data-ttu-id="bb420-125">3e0abfd0-126a-11d0-a060-00aa006c33ed</span><span class="sxs-lookup"><span data-stu-id="bb420-125">3e0abfd0-126a-11d0-a060-00aa006c33ed</span></span>                                                     |
| <span data-ttu-id="bb420-126">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bb420-126">Syntax</span></span>            | [<span data-ttu-id="bb420-127">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="bb420-127">**String(Unicode)**</span></span>](s-string-unicode.md)                                              |



## <a name="implementations"></a><span data-ttu-id="bb420-128">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="bb420-128">Implementations</span></span>

-   [<span data-ttu-id="bb420-129">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="bb420-129">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="bb420-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="bb420-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="bb420-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="bb420-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="bb420-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="bb420-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="bb420-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="bb420-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="bb420-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="bb420-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="bb420-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="bb420-135">Windows 2000 Server</span></span>



| <span data-ttu-id="bb420-136">Voce</span><span class="sxs-lookup"><span data-stu-id="bb420-136">Entry</span></span> | <span data-ttu-id="bb420-137">Valore</span><span class="sxs-lookup"><span data-stu-id="bb420-137">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="bb420-138">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="bb420-138">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="bb420-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bb420-139">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="bb420-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="bb420-140">System-Only</span></span>            | <span data-ttu-id="bb420-141">Falso</span><span class="sxs-lookup"><span data-stu-id="bb420-141">False</span></span>                                                        |
| <span data-ttu-id="bb420-142">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="bb420-142">Is-Single-Valued</span></span>       | <span data-ttu-id="bb420-143">Vero</span><span class="sxs-lookup"><span data-stu-id="bb420-143">True</span></span>                                                         |
| <span data-ttu-id="bb420-144">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="bb420-144">Is Indexed</span></span>             | <span data-ttu-id="bb420-145">Vero</span><span class="sxs-lookup"><span data-stu-id="bb420-145">True</span></span>                                                         |
| <span data-ttu-id="bb420-146">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="bb420-146">In Global Catalog</span></span>      | <span data-ttu-id="bb420-147">Vero</span><span class="sxs-lookup"><span data-stu-id="bb420-147">True</span></span>                                                         |
| <span data-ttu-id="bb420-148">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="bb420-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="bb420-149">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="bb420-149">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="bb420-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bb420-150">Range-Lower</span></span>            | <span data-ttu-id="bb420-151">0</span><span class="sxs-lookup"><span data-stu-id="bb420-151">0</span></span>                                                            |
| <span data-ttu-id="bb420-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bb420-152">Range-Upper</span></span>            | <span data-ttu-id="bb420-153">256</span><span class="sxs-lookup"><span data-stu-id="bb420-153">256</span></span>                                                          |
| <span data-ttu-id="bb420-154">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bb420-154">Search-Flags</span></span>           | <span data-ttu-id="bb420-155">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="bb420-155">0x0000000D</span></span>                                                   |
| <span data-ttu-id="bb420-156">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bb420-156">System-Flags</span></span>           | <span data-ttu-id="bb420-157">0x00000012</span><span class="sxs-lookup"><span data-stu-id="bb420-157">0x00000012</span></span>                                                   |
| <span data-ttu-id="bb420-158">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="bb420-158">Classes used in</span></span>        | [<span data-ttu-id="bb420-159">**Entità di sicurezza**</span><span class="sxs-lookup"><span data-stu-id="bb420-159">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="bb420-160">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="bb420-160">Windows Server 2003</span></span>



| <span data-ttu-id="bb420-161">Voce</span><span class="sxs-lookup"><span data-stu-id="bb420-161">Entry</span></span> | <span data-ttu-id="bb420-162">Valore</span><span class="sxs-lookup"><span data-stu-id="bb420-162">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="bb420-163">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="bb420-163">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="bb420-164">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bb420-164">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="bb420-165">System-Only</span><span class="sxs-lookup"><span data-stu-id="bb420-165">System-Only</span></span>            | <span data-ttu-id="bb420-166">Falso</span><span class="sxs-lookup"><span data-stu-id="bb420-166">False</span></span>                                                        |
| <span data-ttu-id="bb420-167">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="bb420-167">Is-Single-Valued</span></span>       | <span data-ttu-id="bb420-168">Vero</span><span class="sxs-lookup"><span data-stu-id="bb420-168">True</span></span>                                                         |
| <span data-ttu-id="bb420-169">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="bb420-169">Is Indexed</span></span>             | <span data-ttu-id="bb420-170">Vero</span><span class="sxs-lookup"><span data-stu-id="bb420-170">True</span></span>                                                         |
| <span data-ttu-id="bb420-171">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="bb420-171">In Global Catalog</span></span>      | <span data-ttu-id="bb420-172">Vero</span><span class="sxs-lookup"><span data-stu-id="bb420-172">True</span></span>                                                         |
| <span data-ttu-id="bb420-173">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="bb420-173">NT-Security-Descriptor</span></span> | <span data-ttu-id="bb420-174">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="bb420-174">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="bb420-175">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bb420-175">Range-Lower</span></span>            | <span data-ttu-id="bb420-176">0</span><span class="sxs-lookup"><span data-stu-id="bb420-176">0</span></span>                                                            |
| <span data-ttu-id="bb420-177">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bb420-177">Range-Upper</span></span>            | <span data-ttu-id="bb420-178">256</span><span class="sxs-lookup"><span data-stu-id="bb420-178">256</span></span>                                                          |
| <span data-ttu-id="bb420-179">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bb420-179">Search-Flags</span></span>           | <span data-ttu-id="bb420-180">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="bb420-180">0x0000000D</span></span>                                                   |
| <span data-ttu-id="bb420-181">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bb420-181">System-Flags</span></span>           | <span data-ttu-id="bb420-182">0x00000012</span><span class="sxs-lookup"><span data-stu-id="bb420-182">0x00000012</span></span>                                                   |
| <span data-ttu-id="bb420-183">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="bb420-183">Classes used in</span></span>        | [<span data-ttu-id="bb420-184">**Entità di sicurezza**</span><span class="sxs-lookup"><span data-stu-id="bb420-184">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="bb420-185">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="bb420-185">Windows Server 2003 R2</span></span>



| <span data-ttu-id="bb420-186">Voce</span><span class="sxs-lookup"><span data-stu-id="bb420-186">Entry</span></span> | <span data-ttu-id="bb420-187">Valore</span><span class="sxs-lookup"><span data-stu-id="bb420-187">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="bb420-188">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="bb420-188">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="bb420-189">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bb420-189">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="bb420-190">System-Only</span><span class="sxs-lookup"><span data-stu-id="bb420-190">System-Only</span></span>            | <span data-ttu-id="bb420-191">Falso</span><span class="sxs-lookup"><span data-stu-id="bb420-191">False</span></span>                                                        |
| <span data-ttu-id="bb420-192">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="bb420-192">Is-Single-Valued</span></span>       | <span data-ttu-id="bb420-193">Vero</span><span class="sxs-lookup"><span data-stu-id="bb420-193">True</span></span>                                                         |
| <span data-ttu-id="bb420-194">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="bb420-194">Is Indexed</span></span>             | <span data-ttu-id="bb420-195">Vero</span><span class="sxs-lookup"><span data-stu-id="bb420-195">True</span></span>                                                         |
| <span data-ttu-id="bb420-196">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="bb420-196">In Global Catalog</span></span>      | <span data-ttu-id="bb420-197">Vero</span><span class="sxs-lookup"><span data-stu-id="bb420-197">True</span></span>                                                         |
| <span data-ttu-id="bb420-198">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="bb420-198">NT-Security-Descriptor</span></span> | <span data-ttu-id="bb420-199">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="bb420-199">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="bb420-200">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bb420-200">Range-Lower</span></span>            | <span data-ttu-id="bb420-201">0</span><span class="sxs-lookup"><span data-stu-id="bb420-201">0</span></span>                                                            |
| <span data-ttu-id="bb420-202">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bb420-202">Range-Upper</span></span>            | <span data-ttu-id="bb420-203">256</span><span class="sxs-lookup"><span data-stu-id="bb420-203">256</span></span>                                                          |
| <span data-ttu-id="bb420-204">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bb420-204">Search-Flags</span></span>           | <span data-ttu-id="bb420-205">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="bb420-205">0x0000000D</span></span>                                                   |
| <span data-ttu-id="bb420-206">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bb420-206">System-Flags</span></span>           | <span data-ttu-id="bb420-207">0x00000012</span><span class="sxs-lookup"><span data-stu-id="bb420-207">0x00000012</span></span>                                                   |
| <span data-ttu-id="bb420-208">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="bb420-208">Classes used in</span></span>        | [<span data-ttu-id="bb420-209">**Entità di sicurezza**</span><span class="sxs-lookup"><span data-stu-id="bb420-209">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="bb420-210">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bb420-210">Windows Server 2008</span></span>



| <span data-ttu-id="bb420-211">Voce</span><span class="sxs-lookup"><span data-stu-id="bb420-211">Entry</span></span> | <span data-ttu-id="bb420-212">Valore</span><span class="sxs-lookup"><span data-stu-id="bb420-212">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="bb420-213">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="bb420-213">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="bb420-214">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bb420-214">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="bb420-215">System-Only</span><span class="sxs-lookup"><span data-stu-id="bb420-215">System-Only</span></span>            | <span data-ttu-id="bb420-216">Falso</span><span class="sxs-lookup"><span data-stu-id="bb420-216">False</span></span>                                                        |
| <span data-ttu-id="bb420-217">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="bb420-217">Is-Single-Valued</span></span>       | <span data-ttu-id="bb420-218">Vero</span><span class="sxs-lookup"><span data-stu-id="bb420-218">True</span></span>                                                         |
| <span data-ttu-id="bb420-219">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="bb420-219">Is Indexed</span></span>             | <span data-ttu-id="bb420-220">Vero</span><span class="sxs-lookup"><span data-stu-id="bb420-220">True</span></span>                                                         |
| <span data-ttu-id="bb420-221">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="bb420-221">In Global Catalog</span></span>      | <span data-ttu-id="bb420-222">Vero</span><span class="sxs-lookup"><span data-stu-id="bb420-222">True</span></span>                                                         |
| <span data-ttu-id="bb420-223">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="bb420-223">NT-Security-Descriptor</span></span> | <span data-ttu-id="bb420-224">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="bb420-224">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="bb420-225">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bb420-225">Range-Lower</span></span>            | <span data-ttu-id="bb420-226">0</span><span class="sxs-lookup"><span data-stu-id="bb420-226">0</span></span>                                                            |
| <span data-ttu-id="bb420-227">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bb420-227">Range-Upper</span></span>            | <span data-ttu-id="bb420-228">256</span><span class="sxs-lookup"><span data-stu-id="bb420-228">256</span></span>                                                          |
| <span data-ttu-id="bb420-229">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bb420-229">Search-Flags</span></span>           | <span data-ttu-id="bb420-230">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="bb420-230">0x0000000D</span></span>                                                   |
| <span data-ttu-id="bb420-231">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bb420-231">System-Flags</span></span>           | <span data-ttu-id="bb420-232">0x00000012</span><span class="sxs-lookup"><span data-stu-id="bb420-232">0x00000012</span></span>                                                   |
| <span data-ttu-id="bb420-233">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="bb420-233">Classes used in</span></span>        | [<span data-ttu-id="bb420-234">**Entità di sicurezza**</span><span class="sxs-lookup"><span data-stu-id="bb420-234">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="bb420-235">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="bb420-235">Windows Server 2008 R2</span></span>



| <span data-ttu-id="bb420-236">Voce</span><span class="sxs-lookup"><span data-stu-id="bb420-236">Entry</span></span> | <span data-ttu-id="bb420-237">Valore</span><span class="sxs-lookup"><span data-stu-id="bb420-237">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="bb420-238">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="bb420-238">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="bb420-239">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bb420-239">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="bb420-240">System-Only</span><span class="sxs-lookup"><span data-stu-id="bb420-240">System-Only</span></span>            | <span data-ttu-id="bb420-241">Falso</span><span class="sxs-lookup"><span data-stu-id="bb420-241">False</span></span>                                                        |
| <span data-ttu-id="bb420-242">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="bb420-242">Is-Single-Valued</span></span>       | <span data-ttu-id="bb420-243">Vero</span><span class="sxs-lookup"><span data-stu-id="bb420-243">True</span></span>                                                         |
| <span data-ttu-id="bb420-244">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="bb420-244">Is Indexed</span></span>             | <span data-ttu-id="bb420-245">Vero</span><span class="sxs-lookup"><span data-stu-id="bb420-245">True</span></span>                                                         |
| <span data-ttu-id="bb420-246">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="bb420-246">In Global Catalog</span></span>      | <span data-ttu-id="bb420-247">Vero</span><span class="sxs-lookup"><span data-stu-id="bb420-247">True</span></span>                                                         |
| <span data-ttu-id="bb420-248">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="bb420-248">NT-Security-Descriptor</span></span> | <span data-ttu-id="bb420-249">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="bb420-249">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="bb420-250">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bb420-250">Range-Lower</span></span>            | <span data-ttu-id="bb420-251">0</span><span class="sxs-lookup"><span data-stu-id="bb420-251">0</span></span>                                                            |
| <span data-ttu-id="bb420-252">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bb420-252">Range-Upper</span></span>            | <span data-ttu-id="bb420-253">256</span><span class="sxs-lookup"><span data-stu-id="bb420-253">256</span></span>                                                          |
| <span data-ttu-id="bb420-254">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bb420-254">Search-Flags</span></span>           | <span data-ttu-id="bb420-255">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="bb420-255">0x0000000D</span></span>                                                   |
| <span data-ttu-id="bb420-256">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bb420-256">System-Flags</span></span>           | <span data-ttu-id="bb420-257">0x00000012</span><span class="sxs-lookup"><span data-stu-id="bb420-257">0x00000012</span></span>                                                   |
| <span data-ttu-id="bb420-258">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="bb420-258">Classes used in</span></span>        | [<span data-ttu-id="bb420-259">**Entità di sicurezza**</span><span class="sxs-lookup"><span data-stu-id="bb420-259">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="bb420-260">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="bb420-260">Windows Server 2012</span></span>



| <span data-ttu-id="bb420-261">Voce</span><span class="sxs-lookup"><span data-stu-id="bb420-261">Entry</span></span> | <span data-ttu-id="bb420-262">Valore</span><span class="sxs-lookup"><span data-stu-id="bb420-262">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="bb420-263">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="bb420-263">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="bb420-264">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bb420-264">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="bb420-265">System-Only</span><span class="sxs-lookup"><span data-stu-id="bb420-265">System-Only</span></span>            | <span data-ttu-id="bb420-266">Falso</span><span class="sxs-lookup"><span data-stu-id="bb420-266">False</span></span>                                                        |
| <span data-ttu-id="bb420-267">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="bb420-267">Is-Single-Valued</span></span>       | <span data-ttu-id="bb420-268">Vero</span><span class="sxs-lookup"><span data-stu-id="bb420-268">True</span></span>                                                         |
| <span data-ttu-id="bb420-269">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="bb420-269">Is Indexed</span></span>             | <span data-ttu-id="bb420-270">Vero</span><span class="sxs-lookup"><span data-stu-id="bb420-270">True</span></span>                                                         |
| <span data-ttu-id="bb420-271">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="bb420-271">In Global Catalog</span></span>      | <span data-ttu-id="bb420-272">Vero</span><span class="sxs-lookup"><span data-stu-id="bb420-272">True</span></span>                                                         |
| <span data-ttu-id="bb420-273">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="bb420-273">NT-Security-Descriptor</span></span> | <span data-ttu-id="bb420-274">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="bb420-274">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="bb420-275">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bb420-275">Range-Lower</span></span>            | <span data-ttu-id="bb420-276">0</span><span class="sxs-lookup"><span data-stu-id="bb420-276">0</span></span>                                                            |
| <span data-ttu-id="bb420-277">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bb420-277">Range-Upper</span></span>            | <span data-ttu-id="bb420-278">256</span><span class="sxs-lookup"><span data-stu-id="bb420-278">256</span></span>                                                          |
| <span data-ttu-id="bb420-279">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bb420-279">Search-Flags</span></span>           | <span data-ttu-id="bb420-280">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="bb420-280">0x0000000D</span></span>                                                   |
| <span data-ttu-id="bb420-281">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bb420-281">System-Flags</span></span>           | <span data-ttu-id="bb420-282">0x00000012</span><span class="sxs-lookup"><span data-stu-id="bb420-282">0x00000012</span></span>                                                   |
| <span data-ttu-id="bb420-283">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="bb420-283">Classes used in</span></span>        | [<span data-ttu-id="bb420-284">**Entità di sicurezza**</span><span class="sxs-lookup"><span data-stu-id="bb420-284">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



 

 





