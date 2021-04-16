---
title: attributo MS-IIS-FTP-dir
description: Questo attributo determina la home directory dell'utente relativa alla condivisione file server. Viene usato in combinazione con MS-IIS-FTP-root per determinare la home directory dell'utente FTP.
ms.assetid: 99b22b79-1d42-440d-b92b-33bac3e811cb
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo MS-IIS-FTP-dir
- msIIS-schema AD attributo FTPDir
topic_type:
- apiref
api_name:
- ms-IIS-FTP-Dir
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3067476e7dc275dbe14471d6c3c98fa5445a9dfe
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104519782"
---
# <a name="ms-iis-ftp-dir-attribute"></a><span data-ttu-id="97149-106">attributo MS-IIS-FTP-dir</span><span class="sxs-lookup"><span data-stu-id="97149-106">ms-IIS-FTP-Dir attribute</span></span>

<span data-ttu-id="97149-107">Questo attributo determina la home directory dell'utente relativa alla condivisione file server.</span><span class="sxs-lookup"><span data-stu-id="97149-107">This attribute determines the user home directory relative to the file server share.</span></span> <span data-ttu-id="97149-108">Viene usato in combinazione con MS-IIS-FTP-root per determinare la home directory dell'utente FTP.</span><span class="sxs-lookup"><span data-stu-id="97149-108">It is used in conjunction with ms-IIS-FTP-Root to determine the FTP user home directory.</span></span>



| <span data-ttu-id="97149-109">Voce</span><span class="sxs-lookup"><span data-stu-id="97149-109">Entry</span></span> | <span data-ttu-id="97149-110">Valore</span><span class="sxs-lookup"><span data-stu-id="97149-110">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="97149-111">CN</span><span class="sxs-lookup"><span data-stu-id="97149-111">CN</span></span>                | <span data-ttu-id="97149-112">MS-IIS-FTP-dir</span><span class="sxs-lookup"><span data-stu-id="97149-112">ms-IIS-FTP-Dir</span></span>                                                                                                                  |
| <span data-ttu-id="97149-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="97149-113">Ldap-Display-Name</span></span> | <span data-ttu-id="97149-114">msIIS-FTPDir</span><span class="sxs-lookup"><span data-stu-id="97149-114">msIIS-FTPDir</span></span>                                                                                                                    |
| <span data-ttu-id="97149-115">Dimensione</span><span class="sxs-lookup"><span data-stu-id="97149-115">Size</span></span>              | <span data-ttu-id="97149-116">30-50 caratteri (15-25 caratteri Unicode per ogni proprietà)</span><span class="sxs-lookup"><span data-stu-id="97149-116">30-50 characters (15-25 Unicode characters for each property)</span></span>                                                                   |
| <span data-ttu-id="97149-117">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="97149-117">Update Privilege</span></span>  | <span data-ttu-id="97149-118">Amministratore di dominio & sistema locale</span><span class="sxs-lookup"><span data-stu-id="97149-118">Domain administrator & local system</span></span>                                                                                             |
| <span data-ttu-id="97149-119">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="97149-119">Update Frequency</span></span>  | <span data-ttu-id="97149-120">Questa proprietà viene impostata quando l'amministratore crea il sito Web e imposta l'isolamento FTP.</span><span class="sxs-lookup"><span data-stu-id="97149-120">This property is set when the administrator creates the website and sets FTP isolation.</span></span> <span data-ttu-id="97149-121">In questo modo si modifica raramente.</span><span class="sxs-lookup"><span data-stu-id="97149-121">It's rarely going to change after that.</span></span> |
| <span data-ttu-id="97149-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="97149-122">Attribute-Id</span></span>      | <span data-ttu-id="97149-123">1.2.840.113556.1.4.1786</span><span class="sxs-lookup"><span data-stu-id="97149-123">1.2.840.113556.1.4.1786</span></span>                                                                                                         |
| <span data-ttu-id="97149-124">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="97149-124">System-Id-Guid</span></span>    | <span data-ttu-id="97149-125">8a5c99e9-2230-46eb-b8e8-e59d712eb9ee</span><span class="sxs-lookup"><span data-stu-id="97149-125">8a5c99e9-2230-46eb-b8e8-e59d712eb9ee</span></span>                                                                                            |
| <span data-ttu-id="97149-126">Sintassi</span><span class="sxs-lookup"><span data-stu-id="97149-126">Syntax</span></span>            | [<span data-ttu-id="97149-127">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="97149-127">**String(Unicode)**</span></span>](s-string-unicode.md)                                                                                     |



## <a name="implementations"></a><span data-ttu-id="97149-128">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="97149-128">Implementations</span></span>

-   [<span data-ttu-id="97149-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="97149-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="97149-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="97149-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="97149-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="97149-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="97149-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="97149-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="97149-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="97149-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="97149-134">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="97149-134">Windows Server 2003</span></span>



| <span data-ttu-id="97149-135">Voce</span><span class="sxs-lookup"><span data-stu-id="97149-135">Entry</span></span> | <span data-ttu-id="97149-136">Valore</span><span class="sxs-lookup"><span data-stu-id="97149-136">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="97149-137">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="97149-137">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="97149-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="97149-138">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="97149-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="97149-139">System-Only</span></span>            | <span data-ttu-id="97149-140">Falso</span><span class="sxs-lookup"><span data-stu-id="97149-140">False</span></span>                             |
| <span data-ttu-id="97149-141">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="97149-141">Is-Single-Valued</span></span>       | <span data-ttu-id="97149-142">Vero</span><span class="sxs-lookup"><span data-stu-id="97149-142">True</span></span>                              |
| <span data-ttu-id="97149-143">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="97149-143">Is Indexed</span></span>             | <span data-ttu-id="97149-144">Falso</span><span class="sxs-lookup"><span data-stu-id="97149-144">False</span></span>                             |
| <span data-ttu-id="97149-145">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="97149-145">In Global Catalog</span></span>      | <span data-ttu-id="97149-146">Falso</span><span class="sxs-lookup"><span data-stu-id="97149-146">False</span></span>                             |
| <span data-ttu-id="97149-147">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="97149-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="97149-148">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="97149-148">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="97149-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="97149-149">Range-Lower</span></span>            | <span data-ttu-id="97149-150">1</span><span class="sxs-lookup"><span data-stu-id="97149-150">1</span></span>                                 |
| <span data-ttu-id="97149-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="97149-151">Range-Upper</span></span>            | <span data-ttu-id="97149-152">256</span><span class="sxs-lookup"><span data-stu-id="97149-152">256</span></span>                               |
| <span data-ttu-id="97149-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="97149-153">Search-Flags</span></span>           | <span data-ttu-id="97149-154">0x00000000</span><span class="sxs-lookup"><span data-stu-id="97149-154">0x00000000</span></span>                        |
| <span data-ttu-id="97149-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="97149-155">System-Flags</span></span>           | <span data-ttu-id="97149-156">0x00000010</span><span class="sxs-lookup"><span data-stu-id="97149-156">0x00000010</span></span>                        |
| <span data-ttu-id="97149-157">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="97149-157">Classes used in</span></span>        | [<span data-ttu-id="97149-158">**Utente**</span><span class="sxs-lookup"><span data-stu-id="97149-158">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="97149-159">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="97149-159">Windows Server 2003 R2</span></span>



| <span data-ttu-id="97149-160">Voce</span><span class="sxs-lookup"><span data-stu-id="97149-160">Entry</span></span> | <span data-ttu-id="97149-161">Valore</span><span class="sxs-lookup"><span data-stu-id="97149-161">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="97149-162">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="97149-162">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="97149-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="97149-163">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="97149-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="97149-164">System-Only</span></span>            | <span data-ttu-id="97149-165">Falso</span><span class="sxs-lookup"><span data-stu-id="97149-165">False</span></span>                             |
| <span data-ttu-id="97149-166">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="97149-166">Is-Single-Valued</span></span>       | <span data-ttu-id="97149-167">Vero</span><span class="sxs-lookup"><span data-stu-id="97149-167">True</span></span>                              |
| <span data-ttu-id="97149-168">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="97149-168">Is Indexed</span></span>             | <span data-ttu-id="97149-169">Falso</span><span class="sxs-lookup"><span data-stu-id="97149-169">False</span></span>                             |
| <span data-ttu-id="97149-170">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="97149-170">In Global Catalog</span></span>      | <span data-ttu-id="97149-171">Falso</span><span class="sxs-lookup"><span data-stu-id="97149-171">False</span></span>                             |
| <span data-ttu-id="97149-172">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="97149-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="97149-173">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="97149-173">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="97149-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="97149-174">Range-Lower</span></span>            | <span data-ttu-id="97149-175">1</span><span class="sxs-lookup"><span data-stu-id="97149-175">1</span></span>                                 |
| <span data-ttu-id="97149-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="97149-176">Range-Upper</span></span>            | <span data-ttu-id="97149-177">256</span><span class="sxs-lookup"><span data-stu-id="97149-177">256</span></span>                               |
| <span data-ttu-id="97149-178">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="97149-178">Search-Flags</span></span>           | <span data-ttu-id="97149-179">0x00000000</span><span class="sxs-lookup"><span data-stu-id="97149-179">0x00000000</span></span>                        |
| <span data-ttu-id="97149-180">System-Flags</span><span class="sxs-lookup"><span data-stu-id="97149-180">System-Flags</span></span>           | <span data-ttu-id="97149-181">0x00000010</span><span class="sxs-lookup"><span data-stu-id="97149-181">0x00000010</span></span>                        |
| <span data-ttu-id="97149-182">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="97149-182">Classes used in</span></span>        | [<span data-ttu-id="97149-183">**Utente**</span><span class="sxs-lookup"><span data-stu-id="97149-183">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="97149-184">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="97149-184">Windows Server 2008</span></span>



| <span data-ttu-id="97149-185">Voce</span><span class="sxs-lookup"><span data-stu-id="97149-185">Entry</span></span> | <span data-ttu-id="97149-186">Valore</span><span class="sxs-lookup"><span data-stu-id="97149-186">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="97149-187">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="97149-187">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="97149-188">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="97149-188">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="97149-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="97149-189">System-Only</span></span>            | <span data-ttu-id="97149-190">Falso</span><span class="sxs-lookup"><span data-stu-id="97149-190">False</span></span>                             |
| <span data-ttu-id="97149-191">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="97149-191">Is-Single-Valued</span></span>       | <span data-ttu-id="97149-192">Vero</span><span class="sxs-lookup"><span data-stu-id="97149-192">True</span></span>                              |
| <span data-ttu-id="97149-193">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="97149-193">Is Indexed</span></span>             | <span data-ttu-id="97149-194">Falso</span><span class="sxs-lookup"><span data-stu-id="97149-194">False</span></span>                             |
| <span data-ttu-id="97149-195">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="97149-195">In Global Catalog</span></span>      | <span data-ttu-id="97149-196">Falso</span><span class="sxs-lookup"><span data-stu-id="97149-196">False</span></span>                             |
| <span data-ttu-id="97149-197">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="97149-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="97149-198">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="97149-198">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="97149-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="97149-199">Range-Lower</span></span>            | <span data-ttu-id="97149-200">1</span><span class="sxs-lookup"><span data-stu-id="97149-200">1</span></span>                                 |
| <span data-ttu-id="97149-201">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="97149-201">Range-Upper</span></span>            | <span data-ttu-id="97149-202">256</span><span class="sxs-lookup"><span data-stu-id="97149-202">256</span></span>                               |
| <span data-ttu-id="97149-203">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="97149-203">Search-Flags</span></span>           | <span data-ttu-id="97149-204">0x00000000</span><span class="sxs-lookup"><span data-stu-id="97149-204">0x00000000</span></span>                        |
| <span data-ttu-id="97149-205">System-Flags</span><span class="sxs-lookup"><span data-stu-id="97149-205">System-Flags</span></span>           | <span data-ttu-id="97149-206">0x00000010</span><span class="sxs-lookup"><span data-stu-id="97149-206">0x00000010</span></span>                        |
| <span data-ttu-id="97149-207">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="97149-207">Classes used in</span></span>        | [<span data-ttu-id="97149-208">**Utente**</span><span class="sxs-lookup"><span data-stu-id="97149-208">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="97149-209">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="97149-209">Windows Server 2008 R2</span></span>



| <span data-ttu-id="97149-210">Voce</span><span class="sxs-lookup"><span data-stu-id="97149-210">Entry</span></span> | <span data-ttu-id="97149-211">Valore</span><span class="sxs-lookup"><span data-stu-id="97149-211">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="97149-212">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="97149-212">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="97149-213">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="97149-213">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="97149-214">System-Only</span><span class="sxs-lookup"><span data-stu-id="97149-214">System-Only</span></span>            | <span data-ttu-id="97149-215">Falso</span><span class="sxs-lookup"><span data-stu-id="97149-215">False</span></span>                             |
| <span data-ttu-id="97149-216">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="97149-216">Is-Single-Valued</span></span>       | <span data-ttu-id="97149-217">Vero</span><span class="sxs-lookup"><span data-stu-id="97149-217">True</span></span>                              |
| <span data-ttu-id="97149-218">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="97149-218">Is Indexed</span></span>             | <span data-ttu-id="97149-219">Falso</span><span class="sxs-lookup"><span data-stu-id="97149-219">False</span></span>                             |
| <span data-ttu-id="97149-220">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="97149-220">In Global Catalog</span></span>      | <span data-ttu-id="97149-221">Falso</span><span class="sxs-lookup"><span data-stu-id="97149-221">False</span></span>                             |
| <span data-ttu-id="97149-222">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="97149-222">NT-Security-Descriptor</span></span> | <span data-ttu-id="97149-223">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="97149-223">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="97149-224">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="97149-224">Range-Lower</span></span>            | <span data-ttu-id="97149-225">1</span><span class="sxs-lookup"><span data-stu-id="97149-225">1</span></span>                                 |
| <span data-ttu-id="97149-226">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="97149-226">Range-Upper</span></span>            | <span data-ttu-id="97149-227">256</span><span class="sxs-lookup"><span data-stu-id="97149-227">256</span></span>                               |
| <span data-ttu-id="97149-228">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="97149-228">Search-Flags</span></span>           | <span data-ttu-id="97149-229">0x00000000</span><span class="sxs-lookup"><span data-stu-id="97149-229">0x00000000</span></span>                        |
| <span data-ttu-id="97149-230">System-Flags</span><span class="sxs-lookup"><span data-stu-id="97149-230">System-Flags</span></span>           | <span data-ttu-id="97149-231">0x00000010</span><span class="sxs-lookup"><span data-stu-id="97149-231">0x00000010</span></span>                        |
| <span data-ttu-id="97149-232">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="97149-232">Classes used in</span></span>        | [<span data-ttu-id="97149-233">**Utente**</span><span class="sxs-lookup"><span data-stu-id="97149-233">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="97149-234">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="97149-234">Windows Server 2012</span></span>



| <span data-ttu-id="97149-235">Voce</span><span class="sxs-lookup"><span data-stu-id="97149-235">Entry</span></span> | <span data-ttu-id="97149-236">Valore</span><span class="sxs-lookup"><span data-stu-id="97149-236">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="97149-237">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="97149-237">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="97149-238">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="97149-238">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="97149-239">System-Only</span><span class="sxs-lookup"><span data-stu-id="97149-239">System-Only</span></span>            | <span data-ttu-id="97149-240">Falso</span><span class="sxs-lookup"><span data-stu-id="97149-240">False</span></span>                             |
| <span data-ttu-id="97149-241">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="97149-241">Is-Single-Valued</span></span>       | <span data-ttu-id="97149-242">Vero</span><span class="sxs-lookup"><span data-stu-id="97149-242">True</span></span>                              |
| <span data-ttu-id="97149-243">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="97149-243">Is Indexed</span></span>             | <span data-ttu-id="97149-244">Falso</span><span class="sxs-lookup"><span data-stu-id="97149-244">False</span></span>                             |
| <span data-ttu-id="97149-245">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="97149-245">In Global Catalog</span></span>      | <span data-ttu-id="97149-246">Falso</span><span class="sxs-lookup"><span data-stu-id="97149-246">False</span></span>                             |
| <span data-ttu-id="97149-247">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="97149-247">NT-Security-Descriptor</span></span> | <span data-ttu-id="97149-248">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="97149-248">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="97149-249">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="97149-249">Range-Lower</span></span>            | <span data-ttu-id="97149-250">1</span><span class="sxs-lookup"><span data-stu-id="97149-250">1</span></span>                                 |
| <span data-ttu-id="97149-251">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="97149-251">Range-Upper</span></span>            | <span data-ttu-id="97149-252">256</span><span class="sxs-lookup"><span data-stu-id="97149-252">256</span></span>                               |
| <span data-ttu-id="97149-253">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="97149-253">Search-Flags</span></span>           | <span data-ttu-id="97149-254">0x00000000</span><span class="sxs-lookup"><span data-stu-id="97149-254">0x00000000</span></span>                        |
| <span data-ttu-id="97149-255">System-Flags</span><span class="sxs-lookup"><span data-stu-id="97149-255">System-Flags</span></span>           | <span data-ttu-id="97149-256">0x00000010</span><span class="sxs-lookup"><span data-stu-id="97149-256">0x00000010</span></span>                        |
| <span data-ttu-id="97149-257">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="97149-257">Classes used in</span></span>        | [<span data-ttu-id="97149-258">**Utente**</span><span class="sxs-lookup"><span data-stu-id="97149-258">**User**</span></span>](c-user.md)<br/> |



 

 





