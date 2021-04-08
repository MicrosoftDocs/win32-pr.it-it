---
title: Utente-Shared-Folder-attributo
description: Specifica un percorso UNC della cartella documenti condivisi dell'utente. Il percorso deve essere un percorso UNC di rete della directory di condivisione del server di form \\ \\ \\ \\ . Questo valore può essere una stringa null.
ms.assetid: 23b4177a-0a05-4111-affe-d81bc115580d
ms.tgt_platform: multiple
keywords:
- Schema di AD dell'attributo della cartella condivisa utente
- Schema AD dell'attributo userSharedFolder
topic_type:
- apiref
api_name:
- User-Shared-Folder
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a20e9772302e79837fccd301943554191cf3b862
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103965317"
---
# <a name="user-shared-folder-attribute"></a><span data-ttu-id="71e85-107">Utente-Shared-Folder-attributo</span><span class="sxs-lookup"><span data-stu-id="71e85-107">User-Shared-Folder attribute</span></span>

<span data-ttu-id="71e85-108">Specifica un percorso UNC della cartella documenti condivisi dell'utente.</span><span class="sxs-lookup"><span data-stu-id="71e85-108">Specifies a UNC path to the user's shared documents folder.</span></span> <span data-ttu-id="71e85-109">Il percorso deve essere un percorso UNC di rete della **\\\\** directory di condivisione del _Server_ di form *_\\_*  *_\\_* .</span><span class="sxs-lookup"><span data-stu-id="71e85-109">The path must be a network UNC path of the form **\\\\**_Server_*_\\_*_Share_*_\\_*_Directory_.</span></span> <span data-ttu-id="71e85-110">Questo valore può essere una stringa null.</span><span class="sxs-lookup"><span data-stu-id="71e85-110">This value can be a null string.</span></span>



| <span data-ttu-id="71e85-111">Voce</span><span class="sxs-lookup"><span data-stu-id="71e85-111">Entry</span></span> | <span data-ttu-id="71e85-112">Valore</span><span class="sxs-lookup"><span data-stu-id="71e85-112">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="71e85-113">CN</span><span class="sxs-lookup"><span data-stu-id="71e85-113">CN</span></span>                | <span data-ttu-id="71e85-114">Utente-cartella condivisa</span><span class="sxs-lookup"><span data-stu-id="71e85-114">User-Shared-Folder</span></span>                                                                |
| <span data-ttu-id="71e85-115">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="71e85-115">Ldap-Display-Name</span></span> | <span data-ttu-id="71e85-116">userSharedFolder</span><span class="sxs-lookup"><span data-stu-id="71e85-116">userSharedFolder</span></span>                                                                  |
| <span data-ttu-id="71e85-117">Dimensione</span><span class="sxs-lookup"><span data-stu-id="71e85-117">Size</span></span>              | \-                                                                                |
| <span data-ttu-id="71e85-118">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="71e85-118">Update Privilege</span></span>  | <span data-ttu-id="71e85-119">Amministratore di dominio o proprietario dell'account.</span><span class="sxs-lookup"><span data-stu-id="71e85-119">Domain administrator or account owner.</span></span>                                            |
| <span data-ttu-id="71e85-120">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="71e85-120">Update Frequency</span></span>  | <span data-ttu-id="71e85-121">Quando il record dell'utente viene creato e ogni volta che è necessario modificare la cartella condivisa.</span><span class="sxs-lookup"><span data-stu-id="71e85-121">When the user's record is created and whenever the shared folder needs to change.</span></span> |
| <span data-ttu-id="71e85-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="71e85-122">Attribute-Id</span></span>      | <span data-ttu-id="71e85-123">1.2.840.113556.1.4.751</span><span class="sxs-lookup"><span data-stu-id="71e85-123">1.2.840.113556.1.4.751</span></span>                                                            |
| <span data-ttu-id="71e85-124">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="71e85-124">System-Id-Guid</span></span>    | <span data-ttu-id="71e85-125">9a9a021f-4a5b-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="71e85-125">9a9a021f-4a5b-11d1-a9c3-0000f80367c1</span></span>                                              |
| <span data-ttu-id="71e85-126">Sintassi</span><span class="sxs-lookup"><span data-stu-id="71e85-126">Syntax</span></span>            | [<span data-ttu-id="71e85-127">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="71e85-127">**String(Unicode)**</span></span>](s-string-unicode.md)                                       |



## <a name="implementations"></a><span data-ttu-id="71e85-128">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="71e85-128">Implementations</span></span>

-   [<span data-ttu-id="71e85-129">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="71e85-129">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="71e85-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="71e85-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="71e85-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="71e85-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="71e85-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="71e85-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="71e85-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="71e85-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="71e85-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="71e85-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="71e85-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="71e85-135">Windows 2000 Server</span></span>



| <span data-ttu-id="71e85-136">Voce</span><span class="sxs-lookup"><span data-stu-id="71e85-136">Entry</span></span> | <span data-ttu-id="71e85-137">Valore</span><span class="sxs-lookup"><span data-stu-id="71e85-137">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="71e85-138">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="71e85-138">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="71e85-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="71e85-139">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="71e85-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="71e85-140">System-Only</span></span>            | <span data-ttu-id="71e85-141">Falso</span><span class="sxs-lookup"><span data-stu-id="71e85-141">False</span></span>                             |
| <span data-ttu-id="71e85-142">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="71e85-142">Is-Single-Valued</span></span>       | <span data-ttu-id="71e85-143">Vero</span><span class="sxs-lookup"><span data-stu-id="71e85-143">True</span></span>                              |
| <span data-ttu-id="71e85-144">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="71e85-144">Is Indexed</span></span>             | <span data-ttu-id="71e85-145">Falso</span><span class="sxs-lookup"><span data-stu-id="71e85-145">False</span></span>                             |
| <span data-ttu-id="71e85-146">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="71e85-146">In Global Catalog</span></span>      | <span data-ttu-id="71e85-147">Falso</span><span class="sxs-lookup"><span data-stu-id="71e85-147">False</span></span>                             |
| <span data-ttu-id="71e85-148">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="71e85-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="71e85-149">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="71e85-149">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="71e85-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="71e85-150">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="71e85-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="71e85-151">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="71e85-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="71e85-152">Search-Flags</span></span>           | <span data-ttu-id="71e85-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="71e85-153">0x00000000</span></span>                        |
| <span data-ttu-id="71e85-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="71e85-154">System-Flags</span></span>           | <span data-ttu-id="71e85-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="71e85-155">0x00000010</span></span>                        |
| <span data-ttu-id="71e85-156">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="71e85-156">Classes used in</span></span>        | [<span data-ttu-id="71e85-157">**Utente**</span><span class="sxs-lookup"><span data-stu-id="71e85-157">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="71e85-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="71e85-158">Windows Server 2003</span></span>



| <span data-ttu-id="71e85-159">Voce</span><span class="sxs-lookup"><span data-stu-id="71e85-159">Entry</span></span> | <span data-ttu-id="71e85-160">Valore</span><span class="sxs-lookup"><span data-stu-id="71e85-160">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="71e85-161">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="71e85-161">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="71e85-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="71e85-162">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="71e85-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="71e85-163">System-Only</span></span>            | <span data-ttu-id="71e85-164">Falso</span><span class="sxs-lookup"><span data-stu-id="71e85-164">False</span></span>                             |
| <span data-ttu-id="71e85-165">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="71e85-165">Is-Single-Valued</span></span>       | <span data-ttu-id="71e85-166">Vero</span><span class="sxs-lookup"><span data-stu-id="71e85-166">True</span></span>                              |
| <span data-ttu-id="71e85-167">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="71e85-167">Is Indexed</span></span>             | <span data-ttu-id="71e85-168">Falso</span><span class="sxs-lookup"><span data-stu-id="71e85-168">False</span></span>                             |
| <span data-ttu-id="71e85-169">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="71e85-169">In Global Catalog</span></span>      | <span data-ttu-id="71e85-170">Falso</span><span class="sxs-lookup"><span data-stu-id="71e85-170">False</span></span>                             |
| <span data-ttu-id="71e85-171">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="71e85-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="71e85-172">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="71e85-172">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="71e85-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="71e85-173">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="71e85-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="71e85-174">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="71e85-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="71e85-175">Search-Flags</span></span>           | <span data-ttu-id="71e85-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="71e85-176">0x00000000</span></span>                        |
| <span data-ttu-id="71e85-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="71e85-177">System-Flags</span></span>           | <span data-ttu-id="71e85-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="71e85-178">0x00000010</span></span>                        |
| <span data-ttu-id="71e85-179">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="71e85-179">Classes used in</span></span>        | [<span data-ttu-id="71e85-180">**Utente**</span><span class="sxs-lookup"><span data-stu-id="71e85-180">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="71e85-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="71e85-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="71e85-182">Voce</span><span class="sxs-lookup"><span data-stu-id="71e85-182">Entry</span></span> | <span data-ttu-id="71e85-183">Valore</span><span class="sxs-lookup"><span data-stu-id="71e85-183">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="71e85-184">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="71e85-184">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="71e85-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="71e85-185">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="71e85-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="71e85-186">System-Only</span></span>            | <span data-ttu-id="71e85-187">Falso</span><span class="sxs-lookup"><span data-stu-id="71e85-187">False</span></span>                             |
| <span data-ttu-id="71e85-188">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="71e85-188">Is-Single-Valued</span></span>       | <span data-ttu-id="71e85-189">Vero</span><span class="sxs-lookup"><span data-stu-id="71e85-189">True</span></span>                              |
| <span data-ttu-id="71e85-190">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="71e85-190">Is Indexed</span></span>             | <span data-ttu-id="71e85-191">Falso</span><span class="sxs-lookup"><span data-stu-id="71e85-191">False</span></span>                             |
| <span data-ttu-id="71e85-192">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="71e85-192">In Global Catalog</span></span>      | <span data-ttu-id="71e85-193">Falso</span><span class="sxs-lookup"><span data-stu-id="71e85-193">False</span></span>                             |
| <span data-ttu-id="71e85-194">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="71e85-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="71e85-195">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="71e85-195">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="71e85-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="71e85-196">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="71e85-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="71e85-197">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="71e85-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="71e85-198">Search-Flags</span></span>           | <span data-ttu-id="71e85-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="71e85-199">0x00000000</span></span>                        |
| <span data-ttu-id="71e85-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="71e85-200">System-Flags</span></span>           | <span data-ttu-id="71e85-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="71e85-201">0x00000010</span></span>                        |
| <span data-ttu-id="71e85-202">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="71e85-202">Classes used in</span></span>        | [<span data-ttu-id="71e85-203">**Utente**</span><span class="sxs-lookup"><span data-stu-id="71e85-203">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="71e85-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="71e85-204">Windows Server 2008</span></span>



| <span data-ttu-id="71e85-205">Voce</span><span class="sxs-lookup"><span data-stu-id="71e85-205">Entry</span></span> | <span data-ttu-id="71e85-206">Valore</span><span class="sxs-lookup"><span data-stu-id="71e85-206">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="71e85-207">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="71e85-207">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="71e85-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="71e85-208">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="71e85-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="71e85-209">System-Only</span></span>            | <span data-ttu-id="71e85-210">Falso</span><span class="sxs-lookup"><span data-stu-id="71e85-210">False</span></span>                             |
| <span data-ttu-id="71e85-211">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="71e85-211">Is-Single-Valued</span></span>       | <span data-ttu-id="71e85-212">Vero</span><span class="sxs-lookup"><span data-stu-id="71e85-212">True</span></span>                              |
| <span data-ttu-id="71e85-213">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="71e85-213">Is Indexed</span></span>             | <span data-ttu-id="71e85-214">Falso</span><span class="sxs-lookup"><span data-stu-id="71e85-214">False</span></span>                             |
| <span data-ttu-id="71e85-215">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="71e85-215">In Global Catalog</span></span>      | <span data-ttu-id="71e85-216">Falso</span><span class="sxs-lookup"><span data-stu-id="71e85-216">False</span></span>                             |
| <span data-ttu-id="71e85-217">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="71e85-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="71e85-218">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="71e85-218">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="71e85-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="71e85-219">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="71e85-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="71e85-220">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="71e85-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="71e85-221">Search-Flags</span></span>           | <span data-ttu-id="71e85-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="71e85-222">0x00000000</span></span>                        |
| <span data-ttu-id="71e85-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="71e85-223">System-Flags</span></span>           | <span data-ttu-id="71e85-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="71e85-224">0x00000010</span></span>                        |
| <span data-ttu-id="71e85-225">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="71e85-225">Classes used in</span></span>        | [<span data-ttu-id="71e85-226">**Utente**</span><span class="sxs-lookup"><span data-stu-id="71e85-226">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="71e85-227">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="71e85-227">Windows Server 2008 R2</span></span>



| <span data-ttu-id="71e85-228">Voce</span><span class="sxs-lookup"><span data-stu-id="71e85-228">Entry</span></span> | <span data-ttu-id="71e85-229">Valore</span><span class="sxs-lookup"><span data-stu-id="71e85-229">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="71e85-230">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="71e85-230">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="71e85-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="71e85-231">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="71e85-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="71e85-232">System-Only</span></span>            | <span data-ttu-id="71e85-233">Falso</span><span class="sxs-lookup"><span data-stu-id="71e85-233">False</span></span>                             |
| <span data-ttu-id="71e85-234">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="71e85-234">Is-Single-Valued</span></span>       | <span data-ttu-id="71e85-235">Vero</span><span class="sxs-lookup"><span data-stu-id="71e85-235">True</span></span>                              |
| <span data-ttu-id="71e85-236">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="71e85-236">Is Indexed</span></span>             | <span data-ttu-id="71e85-237">Falso</span><span class="sxs-lookup"><span data-stu-id="71e85-237">False</span></span>                             |
| <span data-ttu-id="71e85-238">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="71e85-238">In Global Catalog</span></span>      | <span data-ttu-id="71e85-239">Falso</span><span class="sxs-lookup"><span data-stu-id="71e85-239">False</span></span>                             |
| <span data-ttu-id="71e85-240">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="71e85-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="71e85-241">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="71e85-241">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="71e85-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="71e85-242">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="71e85-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="71e85-243">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="71e85-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="71e85-244">Search-Flags</span></span>           | <span data-ttu-id="71e85-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="71e85-245">0x00000000</span></span>                        |
| <span data-ttu-id="71e85-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="71e85-246">System-Flags</span></span>           | <span data-ttu-id="71e85-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="71e85-247">0x00000010</span></span>                        |
| <span data-ttu-id="71e85-248">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="71e85-248">Classes used in</span></span>        | [<span data-ttu-id="71e85-249">**Utente**</span><span class="sxs-lookup"><span data-stu-id="71e85-249">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="71e85-250">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="71e85-250">Windows Server 2012</span></span>



| <span data-ttu-id="71e85-251">Voce</span><span class="sxs-lookup"><span data-stu-id="71e85-251">Entry</span></span> | <span data-ttu-id="71e85-252">Valore</span><span class="sxs-lookup"><span data-stu-id="71e85-252">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="71e85-253">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="71e85-253">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="71e85-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="71e85-254">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="71e85-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="71e85-255">System-Only</span></span>            | <span data-ttu-id="71e85-256">Falso</span><span class="sxs-lookup"><span data-stu-id="71e85-256">False</span></span>                             |
| <span data-ttu-id="71e85-257">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="71e85-257">Is-Single-Valued</span></span>       | <span data-ttu-id="71e85-258">Vero</span><span class="sxs-lookup"><span data-stu-id="71e85-258">True</span></span>                              |
| <span data-ttu-id="71e85-259">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="71e85-259">Is Indexed</span></span>             | <span data-ttu-id="71e85-260">Falso</span><span class="sxs-lookup"><span data-stu-id="71e85-260">False</span></span>                             |
| <span data-ttu-id="71e85-261">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="71e85-261">In Global Catalog</span></span>      | <span data-ttu-id="71e85-262">Falso</span><span class="sxs-lookup"><span data-stu-id="71e85-262">False</span></span>                             |
| <span data-ttu-id="71e85-263">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="71e85-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="71e85-264">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="71e85-264">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="71e85-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="71e85-265">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="71e85-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="71e85-266">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="71e85-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="71e85-267">Search-Flags</span></span>           | <span data-ttu-id="71e85-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="71e85-268">0x00000000</span></span>                        |
| <span data-ttu-id="71e85-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="71e85-269">System-Flags</span></span>           | <span data-ttu-id="71e85-270">0x00000010</span><span class="sxs-lookup"><span data-stu-id="71e85-270">0x00000010</span></span>                        |
| <span data-ttu-id="71e85-271">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="71e85-271">Classes used in</span></span>        | [<span data-ttu-id="71e85-272">**Utente**</span><span class="sxs-lookup"><span data-stu-id="71e85-272">**User**</span></span>](c-user.md)<br/> |



 

 





