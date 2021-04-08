---
title: Utente-Shared-Folder-altro attributo
description: Specifica un percorso UNC della cartella documenti condivisi aggiuntivi dell'utente. Il percorso deve essere un percorso UNC di rete della directory di condivisione del server di form \\ \\ \\ \\ . Questo valore può essere una stringa null.
ms.assetid: 7d546cda-b2c1-46a6-a3cf-a7c78ddb1422
ms.tgt_platform: multiple
keywords:
- Utente-Shared-Folder-Other schema AD dell'attributo
- Schema AD dell'attributo userSharedFolderOther
topic_type:
- apiref
api_name:
- User-Shared-Folder-Other
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6087a28df474ff06c1d8bf54d694176df8591b5
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744514"
---
# <a name="user-shared-folder-other-attribute"></a><span data-ttu-id="4a023-107">Utente-Shared-Folder-altro attributo</span><span class="sxs-lookup"><span data-stu-id="4a023-107">User-Shared-Folder-Other attribute</span></span>

<span data-ttu-id="4a023-108">Specifica un percorso UNC della cartella documenti condivisi aggiuntivi dell'utente.</span><span class="sxs-lookup"><span data-stu-id="4a023-108">Specifies a UNC path to the user's additional shared documents folder.</span></span> <span data-ttu-id="4a023-109">Il percorso deve essere un percorso UNC di rete della **\\\\** directory di condivisione del _Server_ di form *_\\_*  *_\\_* .</span><span class="sxs-lookup"><span data-stu-id="4a023-109">The path must be a network UNC path of the form **\\\\**_Server_*_\\_*_Share_*_\\_*_Directory_.</span></span> <span data-ttu-id="4a023-110">Questo valore può essere una stringa null.</span><span class="sxs-lookup"><span data-stu-id="4a023-110">This value can be a null string.</span></span>



| <span data-ttu-id="4a023-111">Voce</span><span class="sxs-lookup"><span data-stu-id="4a023-111">Entry</span></span> | <span data-ttu-id="4a023-112">Valore</span><span class="sxs-lookup"><span data-stu-id="4a023-112">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="4a023-113">CN</span><span class="sxs-lookup"><span data-stu-id="4a023-113">CN</span></span>                | <span data-ttu-id="4a023-114">Utente-condiviso-cartella-altro</span><span class="sxs-lookup"><span data-stu-id="4a023-114">User-Shared-Folder-Other</span></span>                                                          |
| <span data-ttu-id="4a023-115">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="4a023-115">Ldap-Display-Name</span></span> | <span data-ttu-id="4a023-116">userSharedFolderOther</span><span class="sxs-lookup"><span data-stu-id="4a023-116">userSharedFolderOther</span></span>                                                             |
| <span data-ttu-id="4a023-117">Dimensione</span><span class="sxs-lookup"><span data-stu-id="4a023-117">Size</span></span>              | \-                                                                                |
| <span data-ttu-id="4a023-118">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="4a023-118">Update Privilege</span></span>  | <span data-ttu-id="4a023-119">Amministratore di dominio o proprietario dell'account.</span><span class="sxs-lookup"><span data-stu-id="4a023-119">Domain administrator or account owner.</span></span>                                            |
| <span data-ttu-id="4a023-120">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="4a023-120">Update Frequency</span></span>  | <span data-ttu-id="4a023-121">Quando il record dell'utente viene creato e ogni volta che è necessario modificare la cartella condivisa.</span><span class="sxs-lookup"><span data-stu-id="4a023-121">When the user's record is created and whenever the shared folder needs to change.</span></span> |
| <span data-ttu-id="4a023-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="4a023-122">Attribute-Id</span></span>      | <span data-ttu-id="4a023-123">1.2.840.113556.1.4.752</span><span class="sxs-lookup"><span data-stu-id="4a023-123">1.2.840.113556.1.4.752</span></span>                                                            |
| <span data-ttu-id="4a023-124">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="4a023-124">System-Id-Guid</span></span>    | <span data-ttu-id="4a023-125">9a9a0220-4a5b-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="4a023-125">9a9a0220-4a5b-11d1-a9c3-0000f80367c1</span></span>                                              |
| <span data-ttu-id="4a023-126">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4a023-126">Syntax</span></span>            | [<span data-ttu-id="4a023-127">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="4a023-127">**String(Unicode)**</span></span>](s-string-unicode.md)                                       |



## <a name="implementations"></a><span data-ttu-id="4a023-128">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="4a023-128">Implementations</span></span>

-   [<span data-ttu-id="4a023-129">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="4a023-129">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="4a023-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="4a023-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="4a023-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="4a023-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="4a023-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="4a023-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="4a023-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="4a023-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="4a023-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="4a023-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="4a023-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4a023-135">Windows 2000 Server</span></span>



| <span data-ttu-id="4a023-136">Voce</span><span class="sxs-lookup"><span data-stu-id="4a023-136">Entry</span></span> | <span data-ttu-id="4a023-137">Valore</span><span class="sxs-lookup"><span data-stu-id="4a023-137">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="4a023-138">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="4a023-138">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="4a023-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4a023-139">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="4a023-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="4a023-140">System-Only</span></span>            | <span data-ttu-id="4a023-141">Falso</span><span class="sxs-lookup"><span data-stu-id="4a023-141">False</span></span>                             |
| <span data-ttu-id="4a023-142">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="4a023-142">Is-Single-Valued</span></span>       | <span data-ttu-id="4a023-143">Falso</span><span class="sxs-lookup"><span data-stu-id="4a023-143">False</span></span>                             |
| <span data-ttu-id="4a023-144">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="4a023-144">Is Indexed</span></span>             | <span data-ttu-id="4a023-145">Falso</span><span class="sxs-lookup"><span data-stu-id="4a023-145">False</span></span>                             |
| <span data-ttu-id="4a023-146">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="4a023-146">In Global Catalog</span></span>      | <span data-ttu-id="4a023-147">Falso</span><span class="sxs-lookup"><span data-stu-id="4a023-147">False</span></span>                             |
| <span data-ttu-id="4a023-148">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="4a023-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="4a023-149">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="4a023-149">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="4a023-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4a023-150">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="4a023-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4a023-151">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="4a023-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4a023-152">Search-Flags</span></span>           | <span data-ttu-id="4a023-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4a023-153">0x00000000</span></span>                        |
| <span data-ttu-id="4a023-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4a023-154">System-Flags</span></span>           | <span data-ttu-id="4a023-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4a023-155">0x00000010</span></span>                        |
| <span data-ttu-id="4a023-156">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="4a023-156">Classes used in</span></span>        | [<span data-ttu-id="4a023-157">**Utente**</span><span class="sxs-lookup"><span data-stu-id="4a023-157">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="4a023-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4a023-158">Windows Server 2003</span></span>



| <span data-ttu-id="4a023-159">Voce</span><span class="sxs-lookup"><span data-stu-id="4a023-159">Entry</span></span> | <span data-ttu-id="4a023-160">Valore</span><span class="sxs-lookup"><span data-stu-id="4a023-160">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="4a023-161">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="4a023-161">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="4a023-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4a023-162">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="4a023-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="4a023-163">System-Only</span></span>            | <span data-ttu-id="4a023-164">Falso</span><span class="sxs-lookup"><span data-stu-id="4a023-164">False</span></span>                             |
| <span data-ttu-id="4a023-165">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="4a023-165">Is-Single-Valued</span></span>       | <span data-ttu-id="4a023-166">Falso</span><span class="sxs-lookup"><span data-stu-id="4a023-166">False</span></span>                             |
| <span data-ttu-id="4a023-167">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="4a023-167">Is Indexed</span></span>             | <span data-ttu-id="4a023-168">Falso</span><span class="sxs-lookup"><span data-stu-id="4a023-168">False</span></span>                             |
| <span data-ttu-id="4a023-169">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="4a023-169">In Global Catalog</span></span>      | <span data-ttu-id="4a023-170">Falso</span><span class="sxs-lookup"><span data-stu-id="4a023-170">False</span></span>                             |
| <span data-ttu-id="4a023-171">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="4a023-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="4a023-172">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="4a023-172">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="4a023-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4a023-173">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="4a023-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4a023-174">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="4a023-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4a023-175">Search-Flags</span></span>           | <span data-ttu-id="4a023-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4a023-176">0x00000000</span></span>                        |
| <span data-ttu-id="4a023-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4a023-177">System-Flags</span></span>           | <span data-ttu-id="4a023-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4a023-178">0x00000010</span></span>                        |
| <span data-ttu-id="4a023-179">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="4a023-179">Classes used in</span></span>        | [<span data-ttu-id="4a023-180">**Utente**</span><span class="sxs-lookup"><span data-stu-id="4a023-180">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="4a023-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="4a023-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="4a023-182">Voce</span><span class="sxs-lookup"><span data-stu-id="4a023-182">Entry</span></span> | <span data-ttu-id="4a023-183">Valore</span><span class="sxs-lookup"><span data-stu-id="4a023-183">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="4a023-184">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="4a023-184">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="4a023-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4a023-185">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="4a023-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="4a023-186">System-Only</span></span>            | <span data-ttu-id="4a023-187">Falso</span><span class="sxs-lookup"><span data-stu-id="4a023-187">False</span></span>                             |
| <span data-ttu-id="4a023-188">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="4a023-188">Is-Single-Valued</span></span>       | <span data-ttu-id="4a023-189">Falso</span><span class="sxs-lookup"><span data-stu-id="4a023-189">False</span></span>                             |
| <span data-ttu-id="4a023-190">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="4a023-190">Is Indexed</span></span>             | <span data-ttu-id="4a023-191">Falso</span><span class="sxs-lookup"><span data-stu-id="4a023-191">False</span></span>                             |
| <span data-ttu-id="4a023-192">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="4a023-192">In Global Catalog</span></span>      | <span data-ttu-id="4a023-193">Falso</span><span class="sxs-lookup"><span data-stu-id="4a023-193">False</span></span>                             |
| <span data-ttu-id="4a023-194">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="4a023-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="4a023-195">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="4a023-195">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="4a023-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4a023-196">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="4a023-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4a023-197">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="4a023-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4a023-198">Search-Flags</span></span>           | <span data-ttu-id="4a023-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4a023-199">0x00000000</span></span>                        |
| <span data-ttu-id="4a023-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4a023-200">System-Flags</span></span>           | <span data-ttu-id="4a023-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4a023-201">0x00000010</span></span>                        |
| <span data-ttu-id="4a023-202">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="4a023-202">Classes used in</span></span>        | [<span data-ttu-id="4a023-203">**Utente**</span><span class="sxs-lookup"><span data-stu-id="4a023-203">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="4a023-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4a023-204">Windows Server 2008</span></span>



| <span data-ttu-id="4a023-205">Voce</span><span class="sxs-lookup"><span data-stu-id="4a023-205">Entry</span></span> | <span data-ttu-id="4a023-206">Valore</span><span class="sxs-lookup"><span data-stu-id="4a023-206">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="4a023-207">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="4a023-207">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="4a023-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4a023-208">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="4a023-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="4a023-209">System-Only</span></span>            | <span data-ttu-id="4a023-210">Falso</span><span class="sxs-lookup"><span data-stu-id="4a023-210">False</span></span>                             |
| <span data-ttu-id="4a023-211">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="4a023-211">Is-Single-Valued</span></span>       | <span data-ttu-id="4a023-212">Falso</span><span class="sxs-lookup"><span data-stu-id="4a023-212">False</span></span>                             |
| <span data-ttu-id="4a023-213">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="4a023-213">Is Indexed</span></span>             | <span data-ttu-id="4a023-214">Falso</span><span class="sxs-lookup"><span data-stu-id="4a023-214">False</span></span>                             |
| <span data-ttu-id="4a023-215">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="4a023-215">In Global Catalog</span></span>      | <span data-ttu-id="4a023-216">Falso</span><span class="sxs-lookup"><span data-stu-id="4a023-216">False</span></span>                             |
| <span data-ttu-id="4a023-217">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="4a023-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="4a023-218">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="4a023-218">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="4a023-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4a023-219">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="4a023-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4a023-220">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="4a023-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4a023-221">Search-Flags</span></span>           | <span data-ttu-id="4a023-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4a023-222">0x00000000</span></span>                        |
| <span data-ttu-id="4a023-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4a023-223">System-Flags</span></span>           | <span data-ttu-id="4a023-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4a023-224">0x00000010</span></span>                        |
| <span data-ttu-id="4a023-225">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="4a023-225">Classes used in</span></span>        | [<span data-ttu-id="4a023-226">**Utente**</span><span class="sxs-lookup"><span data-stu-id="4a023-226">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="4a023-227">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4a023-227">Windows Server 2008 R2</span></span>



| <span data-ttu-id="4a023-228">Voce</span><span class="sxs-lookup"><span data-stu-id="4a023-228">Entry</span></span> | <span data-ttu-id="4a023-229">Valore</span><span class="sxs-lookup"><span data-stu-id="4a023-229">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="4a023-230">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="4a023-230">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="4a023-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4a023-231">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="4a023-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="4a023-232">System-Only</span></span>            | <span data-ttu-id="4a023-233">Falso</span><span class="sxs-lookup"><span data-stu-id="4a023-233">False</span></span>                             |
| <span data-ttu-id="4a023-234">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="4a023-234">Is-Single-Valued</span></span>       | <span data-ttu-id="4a023-235">Falso</span><span class="sxs-lookup"><span data-stu-id="4a023-235">False</span></span>                             |
| <span data-ttu-id="4a023-236">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="4a023-236">Is Indexed</span></span>             | <span data-ttu-id="4a023-237">Falso</span><span class="sxs-lookup"><span data-stu-id="4a023-237">False</span></span>                             |
| <span data-ttu-id="4a023-238">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="4a023-238">In Global Catalog</span></span>      | <span data-ttu-id="4a023-239">Falso</span><span class="sxs-lookup"><span data-stu-id="4a023-239">False</span></span>                             |
| <span data-ttu-id="4a023-240">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="4a023-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="4a023-241">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="4a023-241">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="4a023-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4a023-242">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="4a023-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4a023-243">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="4a023-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4a023-244">Search-Flags</span></span>           | <span data-ttu-id="4a023-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4a023-245">0x00000000</span></span>                        |
| <span data-ttu-id="4a023-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4a023-246">System-Flags</span></span>           | <span data-ttu-id="4a023-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4a023-247">0x00000010</span></span>                        |
| <span data-ttu-id="4a023-248">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="4a023-248">Classes used in</span></span>        | [<span data-ttu-id="4a023-249">**Utente**</span><span class="sxs-lookup"><span data-stu-id="4a023-249">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="4a023-250">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4a023-250">Windows Server 2012</span></span>



| <span data-ttu-id="4a023-251">Voce</span><span class="sxs-lookup"><span data-stu-id="4a023-251">Entry</span></span> | <span data-ttu-id="4a023-252">Valore</span><span class="sxs-lookup"><span data-stu-id="4a023-252">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="4a023-253">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="4a023-253">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="4a023-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4a023-254">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="4a023-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="4a023-255">System-Only</span></span>            | <span data-ttu-id="4a023-256">Falso</span><span class="sxs-lookup"><span data-stu-id="4a023-256">False</span></span>                             |
| <span data-ttu-id="4a023-257">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="4a023-257">Is-Single-Valued</span></span>       | <span data-ttu-id="4a023-258">Falso</span><span class="sxs-lookup"><span data-stu-id="4a023-258">False</span></span>                             |
| <span data-ttu-id="4a023-259">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="4a023-259">Is Indexed</span></span>             | <span data-ttu-id="4a023-260">Falso</span><span class="sxs-lookup"><span data-stu-id="4a023-260">False</span></span>                             |
| <span data-ttu-id="4a023-261">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="4a023-261">In Global Catalog</span></span>      | <span data-ttu-id="4a023-262">Falso</span><span class="sxs-lookup"><span data-stu-id="4a023-262">False</span></span>                             |
| <span data-ttu-id="4a023-263">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="4a023-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="4a023-264">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="4a023-264">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="4a023-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4a023-265">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="4a023-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4a023-266">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="4a023-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4a023-267">Search-Flags</span></span>           | <span data-ttu-id="4a023-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4a023-268">0x00000000</span></span>                        |
| <span data-ttu-id="4a023-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4a023-269">System-Flags</span></span>           | <span data-ttu-id="4a023-270">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4a023-270">0x00000010</span></span>                        |
| <span data-ttu-id="4a023-271">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="4a023-271">Classes used in</span></span>        | [<span data-ttu-id="4a023-272">**Utente**</span><span class="sxs-lookup"><span data-stu-id="4a023-272">**User**</span></span>](c-user.md)<br/> |



 

 





