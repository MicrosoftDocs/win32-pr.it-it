---
title: Attributo Home-Directory
description: La Home Directory per l'account.
ms.assetid: 7fd431f2-f2e0-476f-82ed-04f776c234eb
ms.tgt_platform: multiple
keywords:
- Schema AD Home-Directory attribute
- Schema AD dell'attributo homeDirectory
topic_type:
- apiref
api_name:
- Home-Directory
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 070285336284e6d07b6333d28eff5c85c4dc6c5a
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744850"
---
# <a name="home-directory-attribute"></a><span data-ttu-id="63a60-105">Attributo Home-Directory</span><span class="sxs-lookup"><span data-stu-id="63a60-105">Home-Directory attribute</span></span>

<span data-ttu-id="63a60-106">La Home Directory per l'account.</span><span class="sxs-lookup"><span data-stu-id="63a60-106">The home directory for the account.</span></span> <span data-ttu-id="63a60-107">Se [**homeDrive**](a-homedrive.md) è impostato e specifica una lettera di unità, **HomeDirectory** deve essere un percorso UNC.</span><span class="sxs-lookup"><span data-stu-id="63a60-107">If [**homeDrive**](a-homedrive.md) is set and specifies a drive letter, **homeDirectory** must be a UNC path.</span></span> <span data-ttu-id="63a60-108">In caso contrario, **HomeDirectory** è un percorso locale completo, inclusa la lettera di unità (ad esempio, \*LetteraUnità ***\\ :*** _\\_ \* _cartella_ directory).</span><span class="sxs-lookup"><span data-stu-id="63a60-108">Otherwise, **homeDirectory** is a fully qualified local path including the drive letter (for example, *DriveLetter\***:\\**_Directory_*_\\_\*_Folder_).</span></span> <span data-ttu-id="63a60-109">Questo valore può essere una stringa null.</span><span class="sxs-lookup"><span data-stu-id="63a60-109">This value can be a null string.</span></span>



| <span data-ttu-id="63a60-110">Voce</span><span class="sxs-lookup"><span data-stu-id="63a60-110">Entry</span></span> | <span data-ttu-id="63a60-111">Valore</span><span class="sxs-lookup"><span data-stu-id="63a60-111">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="63a60-112">CN</span><span class="sxs-lookup"><span data-stu-id="63a60-112">CN</span></span>                | <span data-ttu-id="63a60-113">Home-Directory</span><span class="sxs-lookup"><span data-stu-id="63a60-113">Home-Directory</span></span>                                                                     |
| <span data-ttu-id="63a60-114">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="63a60-114">Ldap-Display-Name</span></span> | <span data-ttu-id="63a60-115">homeDirectory</span><span class="sxs-lookup"><span data-stu-id="63a60-115">homeDirectory</span></span>                                                                      |
| <span data-ttu-id="63a60-116">Dimensione</span><span class="sxs-lookup"><span data-stu-id="63a60-116">Size</span></span>              | \-                                                                                 |
| <span data-ttu-id="63a60-117">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="63a60-117">Update Privilege</span></span>  | <span data-ttu-id="63a60-118">Amministratore di dominio</span><span class="sxs-lookup"><span data-stu-id="63a60-118">Domain administrator</span></span>                                                               |
| <span data-ttu-id="63a60-119">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="63a60-119">Update Frequency</span></span>  | <span data-ttu-id="63a60-120">Quando viene creato il record dell'utente e ogni volta che la home directory deve cambiare.</span><span class="sxs-lookup"><span data-stu-id="63a60-120">When the user's record is created and whenever the home directory needs to change.</span></span> |
| <span data-ttu-id="63a60-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="63a60-121">Attribute-Id</span></span>      | <span data-ttu-id="63a60-122">1.2.840.113556.1.4.44</span><span class="sxs-lookup"><span data-stu-id="63a60-122">1.2.840.113556.1.4.44</span></span>                                                              |
| <span data-ttu-id="63a60-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="63a60-123">System-Id-Guid</span></span>    | <span data-ttu-id="63a60-124">bf967985-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="63a60-124">bf967985-0de6-11d0-a285-00aa003049e2</span></span>                                               |
| <span data-ttu-id="63a60-125">Sintassi</span><span class="sxs-lookup"><span data-stu-id="63a60-125">Syntax</span></span>            | [<span data-ttu-id="63a60-126">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="63a60-126">**String(Unicode)**</span></span>](s-string-unicode.md)                                        |



## <a name="implementations"></a><span data-ttu-id="63a60-127">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="63a60-127">Implementations</span></span>

-   [<span data-ttu-id="63a60-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="63a60-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="63a60-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="63a60-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="63a60-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="63a60-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="63a60-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="63a60-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="63a60-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="63a60-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="63a60-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="63a60-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="63a60-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="63a60-134">Windows 2000 Server</span></span>



| <span data-ttu-id="63a60-135">Voce</span><span class="sxs-lookup"><span data-stu-id="63a60-135">Entry</span></span> | <span data-ttu-id="63a60-136">Valore</span><span class="sxs-lookup"><span data-stu-id="63a60-136">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="63a60-137">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="63a60-137">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="63a60-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="63a60-138">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="63a60-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="63a60-139">System-Only</span></span>            | <span data-ttu-id="63a60-140">Falso</span><span class="sxs-lookup"><span data-stu-id="63a60-140">False</span></span>                             |
| <span data-ttu-id="63a60-141">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="63a60-141">Is-Single-Valued</span></span>       | <span data-ttu-id="63a60-142">Vero</span><span class="sxs-lookup"><span data-stu-id="63a60-142">True</span></span>                              |
| <span data-ttu-id="63a60-143">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="63a60-143">Is Indexed</span></span>             | <span data-ttu-id="63a60-144">Falso</span><span class="sxs-lookup"><span data-stu-id="63a60-144">False</span></span>                             |
| <span data-ttu-id="63a60-145">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="63a60-145">In Global Catalog</span></span>      | <span data-ttu-id="63a60-146">Falso</span><span class="sxs-lookup"><span data-stu-id="63a60-146">False</span></span>                             |
| <span data-ttu-id="63a60-147">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="63a60-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="63a60-148">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="63a60-148">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="63a60-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="63a60-149">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="63a60-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="63a60-150">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="63a60-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="63a60-151">Search-Flags</span></span>           | <span data-ttu-id="63a60-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="63a60-152">0x00000010</span></span>                        |
| <span data-ttu-id="63a60-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="63a60-153">System-Flags</span></span>           | <span data-ttu-id="63a60-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="63a60-154">0x00000010</span></span>                        |
| <span data-ttu-id="63a60-155">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="63a60-155">Classes used in</span></span>        | [<span data-ttu-id="63a60-156">**Utente**</span><span class="sxs-lookup"><span data-stu-id="63a60-156">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="63a60-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="63a60-157">Windows Server 2003</span></span>



| <span data-ttu-id="63a60-158">Voce</span><span class="sxs-lookup"><span data-stu-id="63a60-158">Entry</span></span> | <span data-ttu-id="63a60-159">Valore</span><span class="sxs-lookup"><span data-stu-id="63a60-159">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="63a60-160">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="63a60-160">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="63a60-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="63a60-161">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="63a60-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="63a60-162">System-Only</span></span>            | <span data-ttu-id="63a60-163">Falso</span><span class="sxs-lookup"><span data-stu-id="63a60-163">False</span></span>                             |
| <span data-ttu-id="63a60-164">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="63a60-164">Is-Single-Valued</span></span>       | <span data-ttu-id="63a60-165">Vero</span><span class="sxs-lookup"><span data-stu-id="63a60-165">True</span></span>                              |
| <span data-ttu-id="63a60-166">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="63a60-166">Is Indexed</span></span>             | <span data-ttu-id="63a60-167">Falso</span><span class="sxs-lookup"><span data-stu-id="63a60-167">False</span></span>                             |
| <span data-ttu-id="63a60-168">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="63a60-168">In Global Catalog</span></span>      | <span data-ttu-id="63a60-169">Falso</span><span class="sxs-lookup"><span data-stu-id="63a60-169">False</span></span>                             |
| <span data-ttu-id="63a60-170">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="63a60-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="63a60-171">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="63a60-171">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="63a60-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="63a60-172">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="63a60-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="63a60-173">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="63a60-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="63a60-174">Search-Flags</span></span>           | <span data-ttu-id="63a60-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="63a60-175">0x00000010</span></span>                        |
| <span data-ttu-id="63a60-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="63a60-176">System-Flags</span></span>           | <span data-ttu-id="63a60-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="63a60-177">0x00000010</span></span>                        |
| <span data-ttu-id="63a60-178">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="63a60-178">Classes used in</span></span>        | [<span data-ttu-id="63a60-179">**Utente**</span><span class="sxs-lookup"><span data-stu-id="63a60-179">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="63a60-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="63a60-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="63a60-181">Voce</span><span class="sxs-lookup"><span data-stu-id="63a60-181">Entry</span></span> | <span data-ttu-id="63a60-182">Valore</span><span class="sxs-lookup"><span data-stu-id="63a60-182">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="63a60-183">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="63a60-183">Link-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="63a60-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="63a60-184">MAPI-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="63a60-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="63a60-185">System-Only</span></span>            | <span data-ttu-id="63a60-186">Falso</span><span class="sxs-lookup"><span data-stu-id="63a60-186">False</span></span>                                                                               |
| <span data-ttu-id="63a60-187">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="63a60-187">Is-Single-Valued</span></span>       | <span data-ttu-id="63a60-188">Vero</span><span class="sxs-lookup"><span data-stu-id="63a60-188">True</span></span>                                                                                |
| <span data-ttu-id="63a60-189">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="63a60-189">Is Indexed</span></span>             | <span data-ttu-id="63a60-190">Falso</span><span class="sxs-lookup"><span data-stu-id="63a60-190">False</span></span>                                                                               |
| <span data-ttu-id="63a60-191">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="63a60-191">In Global Catalog</span></span>      | <span data-ttu-id="63a60-192">Falso</span><span class="sxs-lookup"><span data-stu-id="63a60-192">False</span></span>                                                                               |
| <span data-ttu-id="63a60-193">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="63a60-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="63a60-194">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="63a60-194">O:BAG:BAD:S:</span></span>                                                                        |
| <span data-ttu-id="63a60-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="63a60-195">Range-Lower</span></span>            | \-                                                                                  |
| <span data-ttu-id="63a60-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="63a60-196">Range-Upper</span></span>            | \-                                                                                  |
| <span data-ttu-id="63a60-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="63a60-197">Search-Flags</span></span>           | <span data-ttu-id="63a60-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="63a60-198">0x00000010</span></span>                                                                          |
| <span data-ttu-id="63a60-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="63a60-199">System-Flags</span></span>           | <span data-ttu-id="63a60-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="63a60-200">0x00000010</span></span>                                                                          |
| <span data-ttu-id="63a60-201">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="63a60-201">Classes used in</span></span>        | [<span data-ttu-id="63a60-202">**Utente**</span><span class="sxs-lookup"><span data-stu-id="63a60-202">**User**</span></span>](c-user.md)<br/> [<span data-ttu-id="63a60-203">**posixAccount**</span><span class="sxs-lookup"><span data-stu-id="63a60-203">**posixAccount**</span></span>](c-posixaccount.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="63a60-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="63a60-204">Windows Server 2008</span></span>



| <span data-ttu-id="63a60-205">Voce</span><span class="sxs-lookup"><span data-stu-id="63a60-205">Entry</span></span> | <span data-ttu-id="63a60-206">Valore</span><span class="sxs-lookup"><span data-stu-id="63a60-206">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="63a60-207">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="63a60-207">Link-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="63a60-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="63a60-208">MAPI-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="63a60-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="63a60-209">System-Only</span></span>            | <span data-ttu-id="63a60-210">Falso</span><span class="sxs-lookup"><span data-stu-id="63a60-210">False</span></span>                                                                               |
| <span data-ttu-id="63a60-211">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="63a60-211">Is-Single-Valued</span></span>       | <span data-ttu-id="63a60-212">Vero</span><span class="sxs-lookup"><span data-stu-id="63a60-212">True</span></span>                                                                                |
| <span data-ttu-id="63a60-213">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="63a60-213">Is Indexed</span></span>             | <span data-ttu-id="63a60-214">Falso</span><span class="sxs-lookup"><span data-stu-id="63a60-214">False</span></span>                                                                               |
| <span data-ttu-id="63a60-215">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="63a60-215">In Global Catalog</span></span>      | <span data-ttu-id="63a60-216">Falso</span><span class="sxs-lookup"><span data-stu-id="63a60-216">False</span></span>                                                                               |
| <span data-ttu-id="63a60-217">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="63a60-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="63a60-218">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="63a60-218">O:BAG:BAD:S:</span></span>                                                                        |
| <span data-ttu-id="63a60-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="63a60-219">Range-Lower</span></span>            | \-                                                                                  |
| <span data-ttu-id="63a60-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="63a60-220">Range-Upper</span></span>            | \-                                                                                  |
| <span data-ttu-id="63a60-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="63a60-221">Search-Flags</span></span>           | <span data-ttu-id="63a60-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="63a60-222">0x00000010</span></span>                                                                          |
| <span data-ttu-id="63a60-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="63a60-223">System-Flags</span></span>           | <span data-ttu-id="63a60-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="63a60-224">0x00000010</span></span>                                                                          |
| <span data-ttu-id="63a60-225">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="63a60-225">Classes used in</span></span>        | [<span data-ttu-id="63a60-226">**Utente**</span><span class="sxs-lookup"><span data-stu-id="63a60-226">**User**</span></span>](c-user.md)<br/> [<span data-ttu-id="63a60-227">**posixAccount**</span><span class="sxs-lookup"><span data-stu-id="63a60-227">**posixAccount**</span></span>](c-posixaccount.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="63a60-228">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="63a60-228">Windows Server 2008 R2</span></span>



| <span data-ttu-id="63a60-229">Voce</span><span class="sxs-lookup"><span data-stu-id="63a60-229">Entry</span></span> | <span data-ttu-id="63a60-230">Valore</span><span class="sxs-lookup"><span data-stu-id="63a60-230">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="63a60-231">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="63a60-231">Link-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="63a60-232">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="63a60-232">MAPI-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="63a60-233">System-Only</span><span class="sxs-lookup"><span data-stu-id="63a60-233">System-Only</span></span>            | <span data-ttu-id="63a60-234">Falso</span><span class="sxs-lookup"><span data-stu-id="63a60-234">False</span></span>                                                                               |
| <span data-ttu-id="63a60-235">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="63a60-235">Is-Single-Valued</span></span>       | <span data-ttu-id="63a60-236">Vero</span><span class="sxs-lookup"><span data-stu-id="63a60-236">True</span></span>                                                                                |
| <span data-ttu-id="63a60-237">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="63a60-237">Is Indexed</span></span>             | <span data-ttu-id="63a60-238">Falso</span><span class="sxs-lookup"><span data-stu-id="63a60-238">False</span></span>                                                                               |
| <span data-ttu-id="63a60-239">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="63a60-239">In Global Catalog</span></span>      | <span data-ttu-id="63a60-240">Falso</span><span class="sxs-lookup"><span data-stu-id="63a60-240">False</span></span>                                                                               |
| <span data-ttu-id="63a60-241">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="63a60-241">NT-Security-Descriptor</span></span> | <span data-ttu-id="63a60-242">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="63a60-242">O:BAG:BAD:S:</span></span>                                                                        |
| <span data-ttu-id="63a60-243">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="63a60-243">Range-Lower</span></span>            | \-                                                                                  |
| <span data-ttu-id="63a60-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="63a60-244">Range-Upper</span></span>            | \-                                                                                  |
| <span data-ttu-id="63a60-245">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="63a60-245">Search-Flags</span></span>           | <span data-ttu-id="63a60-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="63a60-246">0x00000010</span></span>                                                                          |
| <span data-ttu-id="63a60-247">System-Flags</span><span class="sxs-lookup"><span data-stu-id="63a60-247">System-Flags</span></span>           | <span data-ttu-id="63a60-248">0x00000010</span><span class="sxs-lookup"><span data-stu-id="63a60-248">0x00000010</span></span>                                                                          |
| <span data-ttu-id="63a60-249">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="63a60-249">Classes used in</span></span>        | [<span data-ttu-id="63a60-250">**Utente**</span><span class="sxs-lookup"><span data-stu-id="63a60-250">**User**</span></span>](c-user.md)<br/> [<span data-ttu-id="63a60-251">**posixAccount**</span><span class="sxs-lookup"><span data-stu-id="63a60-251">**posixAccount**</span></span>](c-posixaccount.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="63a60-252">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="63a60-252">Windows Server 2012</span></span>



| <span data-ttu-id="63a60-253">Voce</span><span class="sxs-lookup"><span data-stu-id="63a60-253">Entry</span></span> | <span data-ttu-id="63a60-254">Valore</span><span class="sxs-lookup"><span data-stu-id="63a60-254">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="63a60-255">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="63a60-255">Link-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="63a60-256">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="63a60-256">MAPI-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="63a60-257">System-Only</span><span class="sxs-lookup"><span data-stu-id="63a60-257">System-Only</span></span>            | <span data-ttu-id="63a60-258">Falso</span><span class="sxs-lookup"><span data-stu-id="63a60-258">False</span></span>                                                                               |
| <span data-ttu-id="63a60-259">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="63a60-259">Is-Single-Valued</span></span>       | <span data-ttu-id="63a60-260">Vero</span><span class="sxs-lookup"><span data-stu-id="63a60-260">True</span></span>                                                                                |
| <span data-ttu-id="63a60-261">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="63a60-261">Is Indexed</span></span>             | <span data-ttu-id="63a60-262">Falso</span><span class="sxs-lookup"><span data-stu-id="63a60-262">False</span></span>                                                                               |
| <span data-ttu-id="63a60-263">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="63a60-263">In Global Catalog</span></span>      | <span data-ttu-id="63a60-264">Falso</span><span class="sxs-lookup"><span data-stu-id="63a60-264">False</span></span>                                                                               |
| <span data-ttu-id="63a60-265">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="63a60-265">NT-Security-Descriptor</span></span> | <span data-ttu-id="63a60-266">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="63a60-266">O:BAG:BAD:S:</span></span>                                                                        |
| <span data-ttu-id="63a60-267">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="63a60-267">Range-Lower</span></span>            | \-                                                                                  |
| <span data-ttu-id="63a60-268">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="63a60-268">Range-Upper</span></span>            | \-                                                                                  |
| <span data-ttu-id="63a60-269">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="63a60-269">Search-Flags</span></span>           | <span data-ttu-id="63a60-270">0x00000010</span><span class="sxs-lookup"><span data-stu-id="63a60-270">0x00000010</span></span>                                                                          |
| <span data-ttu-id="63a60-271">System-Flags</span><span class="sxs-lookup"><span data-stu-id="63a60-271">System-Flags</span></span>           | <span data-ttu-id="63a60-272">0x00000010</span><span class="sxs-lookup"><span data-stu-id="63a60-272">0x00000010</span></span>                                                                          |
| <span data-ttu-id="63a60-273">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="63a60-273">Classes used in</span></span>        | [<span data-ttu-id="63a60-274">**Utente**</span><span class="sxs-lookup"><span data-stu-id="63a60-274">**User**</span></span>](c-user.md)<br/> [<span data-ttu-id="63a60-275">**posixAccount**</span><span class="sxs-lookup"><span data-stu-id="63a60-275">**posixAccount**</span></span>](c-posixaccount.md)<br/> |



## <a name="see-also"></a><span data-ttu-id="63a60-276">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="63a60-276">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63a60-277">**homeDrive**</span><span class="sxs-lookup"><span data-stu-id="63a60-277">**homeDrive**</span></span>](a-homedrive.md)
</dt> </dl>

 

 





